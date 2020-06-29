---
title: Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos
description: Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813983"
---
# Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos


Use el siguiente procedimiento para instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos.

**Importante**  
Antes de realizar el siguiente procedimiento, debe leer y comprender [acerca de los informes de App-V 5,0](about-app-v-50-reporting.md).



**Para instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos**

1.  Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.

2.  En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.

3.  En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4.  En la página **selección de características** , seleccione la casilla servidor de **informes** y haga clic en **siguiente**.

5.  En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.

6.  En la página **configurar una base de datos de informes existente** , seleccione **usar un servidor SQL Server remoto**y escriba el nombre del equipo que ejecuta Microsoft SQL Server, por ejemplo, **SqlServerMachine**.

    **Nota**  
    Si Microsoft SQL Server está implementado en el mismo servidor, seleccione **usar SQL Server local**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. En la página **configurar el servidor de informes** .

   -   Especifique el nombre del sitio web que desea usar para el servicio de informes. Deje el valor predeterminado sin modificar si no tiene un nombre personalizado.

   -   Para el **enlace de Puerto**, especifique un número de puerto único que usará App-V 5,0, por ejemplo, **55555**. También debe asegurarse de que el puerto especificado no esté siendo usado por otro sitio Web.

8. Haz clic en **Instalar**.

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Acerca de la generación de informes de App-V5.0](about-app-v-50-reporting.md)

[Implementación de App-V 5.0](deploying-app-v-50.md)

[Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









