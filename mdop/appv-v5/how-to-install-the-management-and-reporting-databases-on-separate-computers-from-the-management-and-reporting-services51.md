---
title: Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración
description: Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración
author: dansimp
ms.assetid: 2a67402e-3119-40ea-a247-24d166af1ced
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2332f674f10a9b60aa1cee814c6eac4ddbe4f5af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814031"
---
# Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración

Use el siguiente procedimiento para instalar el servidor de base de datos y el servidor de administración en equipos diferentes. El equipo en el que va a instalar el servidor de base de datos debe estar ejecutando una versión compatible de Microsoft SQL o se producirá un error en la instalación.

> [!NOTE]
> Una vez completada la implementación, el administrador que instala el servicio necesitará el nombre de **Microsoft SQL Server**, el nombre de la **instancia** y el nombre de la **base de datos** instalando el servicio para poder conectarse a estas bases de datos.

## Para instalar la base de datos de administración y el servidor de administración en equipos independientes

1. Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,1, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.
1. En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.
1. En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.
1. En la página **selección de características** , seleccione los componentes que desea instalar seleccionando la casilla de la base de datos del servidor de **Administración** y haga clic en **siguiente**.
1. En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.
1. En la **Página inicial crear nueva base de datos del servidor de administración**, acepte las selecciones predeterminadas, si corresponde, y haga clic en **siguiente**.

    Si está usando una instancia de SQL Server personalizada, seleccione **usar una instancia personalizada** y escriba el nombre de la instancia. \
    Si está usando un nombre de base de datos personalizado, seleccione **Configuración personalizada** y escriba el nombre de la base de datos.

1. En la siguiente página **crear nueva base de datos del servidor de administración** , seleccione **usar un equipo remoto**y escriba la cuenta de la máquina remota con el siguiente formato: **Domain\\MachineAccount**.

    > [!NOTE]
    > Si planea implementar el servidor de administración en el mismo equipo, debe seleccionar **usar este equipo local**.

1. Especifique el nombre de usuario del administrador de **instalación** del servidor de administración con el siguiente formato: **Domain\\AdministratorLoginName**. Haz clic en **Siguiente**.
1. Para iniciar la instalación, haga clic en **instalar**.

## Para instalar la base de datos de informes y el servidor de informes en equipos independientes

1. Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,1, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.
1. En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.
1. En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.
1. En la página **selección de características** , seleccione los componentes que desea instalar seleccionando la casilla de la base de datos del servidor de **informes** y haga clic en **siguiente**.
1. En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.
1. En la página **crear nueva base de datos del servidor de informes** , acepte las selecciones predeterminadas, si es necesario, y haga clic en **siguiente**.

    Si está usando una instancia de SQL Server personalizada, seleccione **usar una instancia personalizada** y escriba el nombre de la instancia.
    Si está usando un nombre de base de datos personalizado, seleccione **Configuración personalizada** y escriba el nombre de la base de datos.

1. En la página **crear nueva base de datos del servidor de informes** , seleccione **usar un equipo remoto**y escriba la cuenta de la máquina remota con el siguiente formato: **Domain\\MachineAccount**.

    > [!NOTE]
    > Si planea implementar el servidor de informes en el mismo equipo, debe seleccionar **usar este equipo local**.

1. Especifique el nombre de usuario para el **Administrador de instalación** de reporting Server con el siguiente formato: **Domain\\AdministratorLoginName**. Haz clic en **Siguiente**.
1. Para iniciar la instalación, haga clic en **instalar**.

## Para instalar las bases de datos de administración y informes con scripts de base de datos de 5,1 de App-V

1. Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo.
1. Para extraer las secuencias de comandos de la base de datos de App-V 5,1, abra un símbolo del sistema y especifique la ubicación donde se guardan los archivos de instalación y ejecute el siguiente comando:

    **appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

1. Una vez completada la extracción, para acceder a los scripts de base de datos de App-V 5,1 y al archivo Léame:

    - El Léame de las secuencias de comandos e instrucciones de la base de datos de administración de APP **InstallationExtractionLocation**-V 5,1 se encuentra en la siguiente carpeta: base de datos de administración de  \\  **scripts**de InstallationExtractionLocation  \\  **Management Database**.
    - Los scripts e instrucciones README de la base de datos de App-V 5,1 se encuentran en la siguiente carpeta: **InstallationExtractionLocation**base de datos de informes de  \\  **scripts de base de datos**  \\  **Reporting Database**.

1. Para cada base de datos, copie las secuencias de comandos en un recurso compartido y modifíquelas siguiendo las instrucciones del archivo README (Léame).

    > [!NOTE]
    > Para obtener más información sobre cómo modificar los SID necesarios que se incluyen en los scripts, vea [Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md).

1. Ejecute los scripts en el equipo que ejecuta Microsoft SQL Server.

**¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados

[Implementación de App-V 5.1](deploying-app-v-51.md)
