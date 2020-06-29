---
title: Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración
description: Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814023"
---
# Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración


Use el siguiente procedimiento para instalar el servidor de base de datos y el servidor de administración en equipos diferentes. El equipo en el que va a instalar el servidor de base de datos debe estar ejecutando una versión compatible de Microsoft SQL o se producirá un error en la instalación.

**Nota**  
Una vez completada la implementación, el administrador que instala el servicio necesitará el nombre de **Microsoft SQL Server**, el nombre de la **instancia** y el nombre de la **base de datos** instalando el servicio para poder conectarse a estas bases de datos.



**Para instalar la base de datos de administración y el servidor de administración en equipos independientes**

1.  Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.

2.  En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.

3.  En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4.  En la página **selección de características** , seleccione los componentes que desea instalar seleccionando la casilla de la base de datos del servidor de **Administración** y haga clic en **siguiente**.

5.  En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.

6.  En la **Página inicial crear nueva base de datos del servidor de administración**, acepte las selecciones predeterminadas, si corresponde, y haga clic en **siguiente**.

    Si está usando una instancia de SQL Server personalizada, seleccione **usar una instancia personalizada** y escriba el nombre de la instancia.

    Si está usando un nombre de base de datos personalizado, seleccione **Configuración personalizada** y escriba el nombre de la base de datos.

7.  En la siguiente página **crear nueva base de datos del servidor de administración** , seleccione **usar un equipo remoto**y escriba la cuenta de la máquina remota con el siguiente formato: **Domain\\MachineAccount**.

    **Nota**  
    Si planea implementar el servidor de administración en el mismo equipo, debe seleccionar **usar este equipo local**.



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. Para iniciar la instalación, haga clic en **instalar**.

**Para instalar la base de datos de informes y el servidor de informes en equipos independientes**

1.  Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.

2.  En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.

3.  En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4.  En la página **selección de características** , seleccione los componentes que desea instalar seleccionando la casilla de la base de datos del servidor de **informes** y haga clic en **siguiente**.

5.  En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.

6.  En la página **crear nueva base de datos del servidor de informes** , acepte las selecciones predeterminadas, si es necesario, y haga clic en **siguiente**.

    Si está usando una instancia de SQL Server personalizada, seleccione **usar una instancia personalizada** y escriba el nombre de la instancia.

    Si está usando un nombre de base de datos personalizado, seleccione **Configuración personalizada** y escriba el nombre de la base de datos.

7.  En la página **crear nueva base de datos del servidor de informes** , seleccione **usar un equipo remoto**y escriba la cuenta de la máquina remota con el siguiente formato: **Domain\\MachineAccount**.

    **Nota**  
    Si planea implementar el servidor de informes en el mismo equipo, debe seleccionar **usar este equipo local**.



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. Para iniciar la instalación, haga clic en **instalar**.

**Para instalar las bases de datos de administración y informes con scripts de base de datos de 5,0 de App-V**

1.  Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo.

2.  Para extraer las secuencias de comandos de la base de datos de App-V 5,0, abra un símbolo del sistema y especifique la ubicación donde se guardan los archivos de instalación y ejecute el siguiente comando:

    **appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

3.  Una vez completada la extracción, para acceder a los scripts de base de datos de App-V 5,0 y al archivo Léame:

    -   El Léame de las secuencias de comandos e instrucciones de la base de datos de administración de APP **InstallationExtractionLocation**-V 5,0 se encuentra en la siguiente carpeta: base de datos de administración de  \\  **scripts**de InstallationExtractionLocation  \\  **Management Database**.

    -   Los scripts e instrucciones README de la base de datos de App-V 5,0 se encuentran en la siguiente carpeta: **InstallationExtractionLocation**base de datos de informes de  \\  **scripts de base de datos**  \\  **Reporting Database**.

4.  Para cada base de datos, copie las secuencias de comandos en un recurso compartido y modifíquelas siguiendo las instrucciones del archivo README (Léame).

    **Nota**  
    Para obtener más información sobre cómo modificar los SID necesarios que se incluyen en los scripts, vea [Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).



5.  Ejecute los scripts en el equipo que ejecuta Microsoft SQL Server.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación de App-V 5.0](deploying-app-v-50.md)









