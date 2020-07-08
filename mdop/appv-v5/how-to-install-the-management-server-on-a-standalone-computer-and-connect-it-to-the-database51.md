---
title: Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos
description: Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814014"
---
# Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos


Use el siguiente procedimiento para instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos.

**Para instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos**

1.  Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,1, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.

2.  En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.

3.  En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4.  En la página **selección de características** , seleccione la casilla servidor de **Administración** y haga clic en **siguiente**.

5.  En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.

6.  En la página **configurar una base de datos de administración existente** , seleccione **usar un servidor SQL Server remoto**y escriba el nombre del equipo que ejecuta Microsoft SQL SQL, por ejemplo, **SqlServerMachine**.

    **Nota**  
    Si Microsoft SQL Server está implementado en el mismo servidor, seleccione **usar SQL Server local**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. En la página **configurar el servidor de administración** , especifique el grupo de ad o la cuenta que se conectará a la consola de administración por razones administrativas, por ejemplo, **MyDomain\\MyUser** o **MyDomain\\AdminGroup**. La cuenta o el grupo de AD que especifique se habilitarán para administrar el servidor a través de la consola de administración. Puede Agregar usuarios o grupos adicionales con la consola de administración después de la instalación

   Especifique el **nombre del sitio web** que desea usar para el servicio de administración. Acepte el valor predeterminado si no tiene un nombre personalizado. Para el **enlace de puertos**, especifique el número de puerto que se va a usar, por ejemplo **12345**.

8. Haz clic en **Instalar**.

9. Para confirmar que la configuración se ha completado correctamente, abra un explorador Web y escriba la siguiente dirección URL: http://managementserver:portnumber/Console . Si la instalación se realizó correctamente, debería ver que la **consola de administración** aparece sin ningún mensaje de error ni advertencia en pantalla.

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación de App-V 5.1](deploying-app-v-51.md)









