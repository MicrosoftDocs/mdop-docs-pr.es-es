---
title: Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1
description: Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814326"
---
# Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1


Puede usar una configuración dinámica para personalizar un paquete de App-V 5,1 para un usuario específico. Sin embargo, primero debe crear el archivo de configuración de usuario dinámica (. xml) o el archivo de configuración de implementación dinámica antes de poder usar los archivos. La creación del archivo es una operación manual avanzada. Para obtener información general sobre los archivos de configuración de usuario dinámicos, consulte [configuración dinámica de App-V 5,1](about-app-v-51-dynamic-configuration.md).

Use el siguiente procedimiento para crear un archivo de configuración de usuario dinámico con la consola de administración de App-V 5,1.

**Para crear un archivo de configuración de usuario dinámico**

1.  Haga clic con el botón secundario en el nombre del paquete que desea ver y seleccione **Editar acceso de Active Directory** para ver la configuración asignada a un grupo de usuarios determinado. Como alternativa, seleccione el paquete y haga clic en **Editar**.

2.  Con la lista de **entidades de ad con Access**, seleccione el grupo de ad que desea personalizar. Seleccione **personalizado** en la lista desplegable, si aún no está seleccionado. Aparecerá un vínculo con el nombre **Editar** .

3.  Haz clic en **Editar**. Se mostrará la configuración de usuario dinámica que está asignada al grupo de AD.

4.  Haga clic en **avanzadas**y, a continuación, en **exportar configuración**. Escriba un nombre de archivo y haga clic en **Guardar**. Ahora puede editar el archivo para configurar un paquete para un usuario.

    **Nota**  
    Para exportar una configuración mientras se ejecuta en Windows Server, debe deshabilitar la "configuración de seguridad mejorada de Internet". Si esta opción está habilitada y está configurada para bloquear las descargas, no podrás descargar nada desde el servidor de App-V.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)









