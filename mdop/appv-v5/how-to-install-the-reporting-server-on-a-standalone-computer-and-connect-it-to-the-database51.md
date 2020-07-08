---
title: Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos
description: Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813974"
---
# Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos

Use el siguiente procedimiento para instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos.

**Importante** Antes de realizar el siguiente procedimiento, debe leer y comprender [acerca de los informes de App-V 5,1](about-app-v-51-reporting.md).

## Para instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos

1. Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,1, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.

2. En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.

3. En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4. En la página **selección de características** , seleccione la casilla servidor de **informes** y haga clic en **siguiente**.

5. En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.

6. En la página **configurar una base de datos de informes existente** , seleccione **usar un servidor SQL Server remoto**y escriba el nombre del equipo que ejecuta Microsoft SQL Server, por ejemplo, **SqlServerMachine**.

    > [!NOTE]
    > Si Microsoft SQL Server está implementado en el mismo servidor, seleccione **usar SQL Server local**.

    Para la instancia de SQL Server, seleccione **usar la instancia predeterminada**. Si está usando una instancia personalizada de Microsoft SQL Server, debe seleccionar **usar una instancia personalizada** y, a continuación, escribir el nombre de la instancia.

    Especifique el **nombre de la base de datos de SQL Server** que usará este servidor de informes, por ejemplo **AppvReporting**.

7. En la página **configurar el servidor de informes** .

   - Especifique el nombre del sitio web que desea usar para el servicio de informes. Deje el valor predeterminado sin modificar si no tiene un nombre personalizado.

   - Para el **enlace de Puerto**, especifique un número de puerto único que usará App-V 5,1, por ejemplo, **55555**. También debe asegurarse de que el puerto especificado no esté siendo usado por otro sitio Web.

8. Haz clic en **Instalar**.

**¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados

[Acerca de la generación de informes de App-V5.1](about-app-v-51-reporting.md)

[Implementación de App-V 5.1](deploying-app-v-51.md)

[Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
