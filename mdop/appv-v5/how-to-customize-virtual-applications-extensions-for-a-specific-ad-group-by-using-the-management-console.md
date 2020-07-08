---
title: Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración
description: Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración
author: dansimp
ms.assetid: 4f249ee3-cc2d-4b1e-afe5-d1cbf9cabd88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57ce4b82cc552e0a4adc2272f849111d8da0be71
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814254"
---
# Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración


Use el siguiente procedimiento para personalizar las extensiones de aplicación virtual para un grupo de Active Directory (AD).

**Para personalizar las extensiones de aplicaciones virtuales para un grupo de AD**

1.  Para ver el paquete que desea configurar, abra la consola de administración de App-V 5,0. Para ver la configuración que está asignada a un grupo de usuarios determinado, seleccione el paquete y haga clic con el botón secundario en el nombre del paquete y seleccione **Editar acceso de Active**Directory. Como alternativa, seleccione el paquete y haga clic en **Editar** en el panel de **acceso ad** .

2.  Para personalizar un grupo de AD, puede buscar el grupo en la lista de **entidades de ad con Access**. Después, con el cuadro desplegable en el panel **configuración asignada** , seleccione **personalizado**y, a continuación, haga clic en **Editar**.

3.  Para deshabilitar todas las extensiones para una aplicación determinada, desactive **Habilitar**.

    Para agregar un nuevo acceso directo para la aplicación seleccionada, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Agregar nuevo acceso directo**. Para quitar un acceso directo, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Quitar acceso directo**. Para editar un acceso directo existente, haga clic con el botón derecho en la aplicación y seleccione **Editar acceso directo**.

4.  Para ver cualquier otra extensión de la aplicación, haga clic en **avanzadas**y en **exportar configuración**. Escriba un nombre de archivo y haga clic en **Guardar**. Puede ver todas las extensiones de aplicaciones asociadas con el paquete mediante el archivo de configuración.

5.  Para editar extensiones de aplicación adicionales, modifique el archivo de configuración y haga clic en **importar y sobrescriba esta configuración**. Seleccione el archivo modificado y haga clic en **abrir**. En el cuadro de diálogo, haga clic en **sobrescribir** para completar el proceso.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





