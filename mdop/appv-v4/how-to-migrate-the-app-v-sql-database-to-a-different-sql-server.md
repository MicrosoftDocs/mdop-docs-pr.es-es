---
title: Cómo migrar la base de datos SQL de App-V a un servidor SQL Server diferente
description: Cómo migrar la base de datos SQL de App-V a un servidor SQL Server diferente
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817071"
---
# Cómo migrar la base de datos SQL de App-V a un servidor SQL Server diferente


En los procedimientos siguientes se describe detalladamente cómo migrar la base de datos de SQL del servidor de administración de Microsoft Application Virtualization (App-V) a otro SQL Server.

**Importante**  Este procedimiento requiere que el servicio de servidor de App-V esté detenido y esto evitará que los usuarios finales puedan usar sus aplicaciones.

 

**Para realizar una copia de seguridad de la base de datos de SQL App-V**

1.  Abra el programa Services. msc y detenga el servicio de App-V Management Server en todos los servidores de administración que usen la base de datos que se va a migrar.

2.  En el equipo en el que se encuentra la base de datos de App-V, abra SQL Server Management Studio.

3.  Expanda el nodo **bases** de datos y busque la base de datos de App-V (el nombre predeterminado es APPVIRT).

4.  Haga clic con el botón derecho en la base de datos y seleccione **tareas** y seleccione **copia de seguridad**.

5.  Compruebe que el **modelo de recuperación** está establecido en **simple** y el tipo de **copia de seguridad** es **completo**. Cambie el **conjunto de copia de seguridad** y la configuración de **destino** si es necesario.

6.  Haga clic en **Aceptar** para hacer una copia de seguridad de la base de datos. Una vez completada la copia de seguridad correctamente, haga clic en **Aceptar**.

7.  Abra el explorador de Windows y vaya a la carpeta que contiene el archivo de copia de seguridad de la base de datos, por ejemplo APPVIRT. Bak. Copie el archivo de copia de seguridad de la base de datos en el equipo de destino que ejecuta SQL Server.

**Para restaurar la base de datos de SQL App-V en el equipo de destino**

1.  En el equipo de destino, abra SQL Server Management Studio, haga clic con el botón derecho en el nodo **bases** de datos y seleccione **restaurar base de datos**.

2.  En **origen para restaurar**, elija **desde el dispositivo** y, a continuación, haga clic en el "**...**" de puntos suspensivos (...).

3.  En el cuadro de diálogo **especificar copia de seguridad** , asegúrese de que el **medio de copia de seguridad** está establecido en **archivo** y, después, haga clic en **Agregar**.

4.  Seleccione el archivo de copia de seguridad que ha copiado del equipo original que está ejecutando SQL Server y, a continuación, haga clic en **Aceptar**.

5.  Haga clic en **Aceptar** y, a continuación, haga clic para seleccionar el conjunto de copia de seguridad que desea restaurar.

6.  En **destino de la restauración**, haga clic en el menú desplegable para la **base de datos** y seleccione el nombre de la base de datos de App-V, por ejemplo APPVIRT.

7.  Haga clic en **Aceptar** para iniciar la restauración. Después de que la restauración se haya completado correctamente, haga clic en **Aceptar**.

8.  Expanda el nodo **seguridad** , haga clic con el botón derecho en **inicios de sesión** y seleccione **nuevo inicio de sesión**.

9.  En el campo **nombre de inicio de sesión** , escriba los detalles de la cuenta servicio de red para el servidor de administración de App-V en el formato DOMAIN\\SERVERNAME $.

10. En la página **General** , en **base de datos predeterminada** , seleccione el nombre de la base de datos de App-V, por ejemplo, APPVIRT, y haga clic en **Aceptar**.

11. En **seleccionar una página**, haga clic para seleccionar la página **asignación de usuario** . En **usuarios asignados a este inicio de sesión**, haga clic en la casilla de la columna **map** para seleccionar la base de datos de App-V.

12. En **pertenencia de rol de base de datos para: &lt; &gt; appvdatabasename**, haga clic para seleccionar **SFTEveryone** y, después, haga clic en **Aceptar**.

13. Asegúrese de que el Firewall de Windows en el nuevo equipo que ejecuta SQL Server está configurado para permitir que el servidor de administración de App-V acceda al sistema. En **herramientas administrativas**, use el **firewall de Windows con seguridad avanzada** para crear una **regla de entrada** para el puerto que usa SQL Server (el puerto predeterminado es 1433).

**Para migrar los trabajos de App-V del Agente SQL Server**

1.  En el equipo original que ejecuta SQL Server, en SQL Server Management Studio, expanda el nodo **Agente SQL Server** y, a continuación, expanda el nodo **tareas** .

2.  Haga clic con el botón derecho en los siguientes cuatro trabajos de App-V y seleccione **trabajo de script como | CREAR en | Archivo**y guarde cada script en una carpeta y asigne un nombre descriptivo a cada secuencia de comandos.

    -   **Base de datos de SoftGrid (appvdbname) comprobar historial de uso**

    -   **Base de datos de SoftGrid (appvdbname) cerrar sesiones huérfanas**

    -   **Base de datos de SoftGrid (appvdbname) exigir límite de tamaño**

    -   **Base de datos de SoftGrid (appvdbname) supervisar el estado del trabajo y la alerta**

3.  Copie los cuatro archivos de script (. SQL) en el equipo de destino que ejecuta SQL Server y abra SQL Server Management Studio.

4.  En el explorador de Windows, haga clic con el botón secundario en cada archivo. SQL y después haga clic en **Ejecutar**. Cada script se abrirá en una ventana de consulta en SQL Server Management Studio. Haga clic en **Ejecutar** para cada script y compruebe que cada uno se complete correctamente.

5.  Actualice el nodo **Jobs** del nodo **Agente SQL Server** y confirme que los cuatro trabajos se han creado correctamente.

**Para actualizar la configuración del servidor de administración de App-V**

1.  En el servidor de administración de App-V, modifique las siguientes claves del registro:

    -   **SQLServerName**  =  SQLServerName &lt; newservername&gt;

    -   **SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;

    Después, reinicie el servicio de servidor de App-V.

2.  Busque el archivo SftMgmt. udl en el directorio de instalación de App-V Management Server (el valor predeterminado es C:\\Archivos de Programa\\microsoft System Center de la aplicación virt Management Server\\App virt Management Service). Haga clic con el botón derecho en el archivo y seleccione **abrir**.

3.  En la pestaña **conexión** , escriba el nombre del equipo de destino que está ejecutando SQL Server y, a continuación, haga clic en **probar conexión**. Cuando la prueba se haya realizado correctamente, haga clic en **Aceptar** y, a continuación, vuelva a hacer clic en **Aceptar** .

4.  Para las versiones de App-V Management Server antes 4,5 SP2, debe actualizar la configuración de registro de SQL. En **grupos de servidores**, haga clic con el botón secundario en el grupo de servidores del que es miembro el servidor y seleccione **propiedades**.

5.  En la pestaña **registro** , haga clic para seleccionar la entrada de la **base de datos SQL** y, a continuación, haga clic en **Editar**.

6.  Cambie el **nombre de host DNS** por el nombre de host del nuevo equipo que está ejecutando SQL Server y, a continuación, haga clic en **Aceptar**. Haga clic en **Aceptar** dos veces más y, a continuación, reinicie el servicio de servidor de App-V.

7.  Abra la consola de administración de App-V, haga clic con el botón derecho en el nodo **aplicaciones** y seleccione **Actualizar**. La lista de aplicaciones debe mostrarse como antes.

 

 





