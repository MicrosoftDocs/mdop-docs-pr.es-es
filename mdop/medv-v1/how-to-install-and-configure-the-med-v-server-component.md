---
title: Cómo instalar y configurar el componente de servidor MED-V
description: Cómo instalar y configurar el componente de servidor MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826980"
---
# Cómo instalar y configurar el componente de servidor MED-V


En esta sección se explica cómo [instalar](#bkmk-howtoinstallthemedvserver) y [configurar](#bkmk-howtoconfigurethemedvserver) el servidor de MED-V.

## <a href="" id="bkmk-howtoinstallthemedvserver"></a>Cómo instalar el servidor MED-V


**Para instalar el servidor MED-V**

1.  Instale el paquete MED-V Server. msi.

    El paquete MED-V Server. msi se llama *MED-V\_Server\_x.msi*, donde x es el número de versión.

    Por ejemplo, *MED-V\_Server\_1.0.65.msi*.

2.  Cuando aparezca la pantalla de **bienvenida del asistente de InstallShield** , haga clic en **siguiente**.

3.  En la pantalla **contrato de licencia** , lea el contrato de licencia, haga clic en Acepto **las condiciones del contrato de licencia**y, a continuación, haga clic en **siguiente**.

    Aparece la pantalla **carpeta de destino** , donde se muestra la carpeta de instalación predeterminada.

    La carpeta de instalación predeterminada es *%SystemDrive%\\Program de escritorio de Programa\\microsoft Enterprise Virtualization\\*.

    -   Para cambiar la carpeta donde se debe instalar MED-V, haga clic en **cambiar** y vaya a una carpeta existente.

4.  Haz clic en **Siguiente**.

5.  En la pantalla **preparado para instalar el programa** , haga clic en **instalar**.

    Se iniciará la instalación del servidor de MED-V. Esto puede demorar varios minutos y es posible que no se muestre el texto en la pantalla. Durante la instalación, aparecen varias pantallas de progreso. Si aparece un mensaje, siga las instrucciones proporcionadas.

6.  Cuando aparezca la pantalla **Asistente InstallShield completado** , haga clic en **Finalizar** para completar el asistente.

**Nota**  
Si va a instalar el servidor MED-V a través de Microsoft Remote Desktop, use la siguiente sintaxis: **mstsc/admin**. Asegúrese de que la sesión RDP se dirija a la consola.



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a>Cómo configurar el servidor MED-V


Puede configurar las siguientes opciones del servidor:

-   [Conexiones](#bkmk-configuringconnections)

-   [Imágenes](#bkmk-configuringimages)

-   [Permisos](#bkmk-configuringpermissions)

-   [Informes](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a>Configurar conexiones

**Para configurar conexiones**

1.  En el menú Inicio de Windows, seleccione **todos los programas &gt; Med-v &gt; Med-v Server Configuration Manager**.

    **Nota**  
    Nota: Si ha activado la casilla de verificación **iniciar administrador de configuración del servidor Med-v** durante la instalación del servidor, el administrador de configuración del servidor Med-v se inicia automáticamente después de que se complete la instalación del servidor.



~~~
The MED-V Server Configuration Manager appears.
~~~

2. En la pestaña **conexiones** , configure las siguientes opciones de conexión de cliente:

   -   **Habilitar conexiones no cifradas (http), mediante puerto**: Seleccione esta casilla para habilitar las conexiones sin cifrar con un puerto específico. En el cuadro puerto, escriba el puerto de servidor en el que se aceptarán las conexiones no cifradas (http).

   -   **Habilitar conexiones cifradas (https), usando puerto**: Seleccione esta casilla para habilitar conexiones cifradas que usen un puerto específico. En el cuadro puerto, escriba el puerto de servidor en el que desea aceptar las conexiones cifradas (https).

       Https es una configuración opcional que se puede establecer para garantizar transacciones seguras entre los clientes de MED-V Server y MED-V. Para configurar https, debe realizar los siguientes procedimientos:

       -   Configurar un certificado en el servidor.

       -   Asociar el certificado de servidor con el puerto especificado mediante netsh. Para obtener más información, vea lo siguiente:

           -   [Comandos Netsh para el protocolo de transferencia de hipertexto (HTTP)](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [Cómo configurar un puerto con un certificado SSL](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [Cómo configurar un puerto con un certificado SSL](https://msdn.microsoft.com/library/ms733791.aspx)

3. Haga clic en **Aceptar**.

### <a href="" id="bkmk-configuringimages"></a>Configurar imágenes

**Para configurar imágenes**

1.  Haga clic en la pestaña **imágenes** .

2.  Configure las siguientes opciones de administración de imágenes:

    -   **Directorio VMS**: el directorio de la máquina virtual (el directorio donde se almacenan las imágenes). Este campo contiene una ruta de acceso UNC al directorio de la imagen en el servidor de distribución de imágenes al que se debería obtener acceso desde el servidor MED-V.

    -   **Dirección URL de MV**: la ubicación del servidor donde se almacenan las imágenes.

3.  Haga clic en **Aceptar**.

### <a href="" id="bkmk-configuringpermissions"></a>Configurar permisos

**Para configurar permisos**

1.  Haga clic en la pestaña **permisos** .

2.  Se proporciona una lista de todos los usuarios que pueden iniciar sesión. Para aplicar permisos de lectura y escritura a un usuario, active la casilla situada junto al usuario. Para aplicar permisos de solo lectura a un usuario, desactive la casilla.

3.  Para agregar usuarios o grupos del dominio, haga clic en **Agregar**.

    Aparece el cuadro de diálogo **Escriba los nombres de los usuarios o grupos** .

    1.  Seleccione usuarios del dominio o grupos mediante una de las siguientes acciones:

        -   En el campo **introducir nombre de usuario o grupo** , escriba un usuario o grupo que exista en el dominio o exista como usuario o grupo local en el equipo. A continuación, haga clic en **Comprobar nombres** para resolver el nombre completo.

        -   Haga clic en **Buscar** para abrir el cuadro de diálogo **Seleccionar usuarios o grupos** estándar. Después, seleccione usuarios o grupos del dominio.

    2.  Haga clic en **Aceptar**.

4.  Para quitar usuarios o grupos del dominio, seleccione un usuario o grupo y haga clic en **quitar**.

5.  Haga clic en **Aceptar**.

### <a href="" id="bkmk-configuringreports"></a>Configuración de informes

**Para configurar informes**

1.  Haga clic en la pestaña **informes** .

2.  Para admitir los informes, seleccione **Habilitar informes**.

3.  En el cuadro **cadena de conexión** , escriba una cadena de conexión para la base de datos MSSQL.

    -   Cuando SQL Server está instalado en un servidor remoto, use la siguiente cadena de conexión:

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **Nota**  
        Nota: para conectarse a SQL Express, use: `Data Source=<ServerName>\sqlexpress.`



4.  Para crear la base de datos, haga clic en **crear base de datos**.

5.  Para comprobar la conexión, haga clic en **probar conexión**.

6.  Para configurar las opciones de borrado de la base de datos, haga clic en **Borrar opciones**.

    Aparece el cuadro de diálogo **Borrar opciones de base de datos** .

    1.  Elija una de las siguientes opciones:

        -   **Borrar datos anteriores a**: borre todos los datos anteriores al número de días especificado; en el cuadro número, escriba un número de días.

        -   **Borrar todos los datos de la base de**datos: borrar todos los datos existentes en la base de datos.

        -   **Drop Database**: Elimine la base de datos.

    2.  Haga clic en **Aceptar** para aplicar los cambios y cerrar el cuadro de diálogo.

7.  Haga clic en **Aceptar** para guardar los cambios, o haga clic en **Cancelar** para cerrar el cuadro de diálogo sin guardar los cambios.

8.  Si se le solicita, reinicie el servicio de servidor de MED-V para aplicar los cambios en la configuración de red.

## Temas relacionados


[Configuraciones admitidas](supported-configurationsmedv-orientation.md)

[Diseñar la infraestructura de servidor MED-V](design-the-med-v-server-infrastructure.md)









