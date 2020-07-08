---
title: Cómo configurar el soporte técnico en duplicación de Microsoft SQL Server para App-V
description: Cómo configurar el soporte técnico en duplicación de Microsoft SQL Server para App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817931"
---
# Cómo configurar el soporte técnico en duplicación de Microsoft SQL Server para App-V


Puede usar el siguiente procedimiento para configurar el entorno de Microsoft Application Virtualization (App-V) para usar el reflejo de base de datos de Microsoft SQL Server. La configuración de la creación de reflejos de base de datos puede ayudar en situaciones de recuperación ante desastres y conmutación. App-V 4,5 SP2 admite todos los modos de creación de reflejo de base de datos disponibles actualmente para Microsoft SQL Server 2005 y SQL Server 2008.

**Nota**  
Este procedimiento está escrito para los administradores familiarizados con la configuración y la configuración de la creación de bases de datos y las bases de datos de SQL Server con Microsoft SQL Server y, por consiguiente, solo cubren las opciones de configuración específicas de App-V.



**Para configurar el entorno de App-V para usar la creación de reflejo de base de datos de Microsoft SQL Server**

1.  Configure el reflejo de la base de datos de SQL Server de la base de datos de App-V siguiendo los procedimientos empresariales estándar para la creación de reflejo de base de datos. Use los siguientes vínculos para obtener información general sobre cómo implementar el reflejo de bases de datos de Microsoft SQL Server:

    -   **Microsoft SQL 2005**:[configuración de la creación de reflejo de la base de datos](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)

    -   **Microsoft SQL 2008**:[configuración de la creación de reflejo de la base de datos](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)

    Además, puede encontrar la información de procedimientos recomendados en [procedimientos recomendados y rendimiento de la creación de reflejos de bases de datos](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .

2.  Una vez que se haya configurado el reflejo, compruebe que la base de datos de App-V muestre el estado **(principal, sincronizado)** y que la base de datos reflejada muestra un estado **(reflejado, sincronizado/restaurado)**. Solucione cualquier problema de duplicación antes de continuar con el siguiente paso. Para obtener más información sobre cómo supervisar el estado, consulte [supervisión del estado del reflejo](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .

3.  En el equipo de SQL Server que hospeda el reflejo de la base de datos de App-v, cree el inicio de sesión de SQL Server para la cuenta de servicio de red del servidor de administración de App-v con el nombre de cuenta ** &lt; domain &gt; \\ &lt; ManagementServerHostName &gt; $ **.

4.  Instale el cliente nativo de Microsoft SQL Server en el servidor de administración de App-V y, en el equipo que ejecute el servicio Web de administración de App-V, si está instalado en otro equipo. Si tiene previsto que los servidores de administración de App-V adicionales se conecten a la base de datos SQL reflejada para el equilibrio de carga, debe instalar también el cliente nativo de Microsoft SQL Server en esos equipos. Puede descargar el cliente nativo de Microsoft SQL Server desde la página del [Feature Pack de Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=187479) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .

5.  Compruebe la clave del registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** y asegúrese de que contiene solo el nombre de host del servidor SQL Server. Si incluye un nombre de instancia, por ejemplo *serverhostname\\instancename*, debe quitarse el nombre de instancia.

    **Importante**  
    El servidor de administración de App-V usa la biblioteca de redes TCP/IP para comunicarse con el servidor SQL Server cuando la creación de reflejo de la base de datos está habilitada y, por lo tanto, no se pueden usar los nombres de instancia. En su lugar, los números de Puerto deben especificarse en las claves del registro.



6.  Compruebe la clave del registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** y asegúrese de que contiene el número de puerto que se usa para SQL en el equipo de SQL Server. Si está usando una instancia con nombre, este valor de clave debe establecerse en el puerto que se usa para la instancia con nombre.

7.  Cree la clave del registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** como REG \ _SZ y, a continuación, establezca el valor en el nombre de host del servidor SQL Server que hospeda el reflejo.

8.  Cree la clave del registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** como DWORD y, a continuación, establezca el valor en el número de puerto que se usa para SQL en el equipo que ejecuta SQL Server para hospedar el reflejo. Si está usando una instancia con nombre para el reflejo, este valor de clave debe establecerse en el número de puerto que se usa para la instancia con nombre.

9.  En el equipo que ejecuta el servicio Web de administración de App-V, configure el archivo de texto UDL (Universal Data Link). En el directorio donde está instalado App-V, haga doble clic en **SftMgmt. udl** y especifique los valores siguientes:

    -   En la pestaña **proveedor** , seleccione el proveedor OLE DB de **SQL Server Native Client 10,0**.

    -   Haga clic en **siguiente** para seleccionar la ficha **conexión** . En el cuadro **nombre del servidor** , escriba el nombre del servidor SQL Server. A continuación, seleccione **usar seguridad integrada de Windows NT**. Por último, haga clic en la lista, **Seleccione la base de datos**y, después, seleccione el nombre de la base de datos de App-V.

    -   Haga clic en la pestaña **todas** y, a continuación, seleccione el **asociado de conmutación por error**de entrada. Haga clic en **Editar valor**y, a continuación, escriba el nombre del servidor SQL Server de conmutación por error. Haga clic en **Aceptar**.

    **Importante**  
    El sistema App-V usa la autenticación Kerberos. Por lo tanto, al configurar el reflejo SQL donde la autenticación Kerberos está habilitada en SQL Server y el servicio SQL Server se ejecuta en una cuenta de usuario de dominio, debe configurar manualmente un SPN. Para obtener más información, vea "cuando el servicio SQL usa una cuenta basada en el dominio" en el artículo [configurar la administración de App-V para un entorno distribuido](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .



10. Para comprobar que el reflejo de la base de datos se está ejecutando correctamente, pruebe la conmutación por error y confirme que el servidor de administración de App-V continúa funcionando correctamente.

    **Importante**  
    Continúe con la atención y siga sus prácticas empresariales estándar para asegurarse de que no se interrumpan las operaciones del sistema en caso de que se produzca un error.



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## Temas relacionados


[Cómo realizar tareas administrativas en la consola de administración de servidor de virtualización de aplicaciones](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









