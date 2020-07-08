---
title: Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración
description: Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración
author: dansimp
ms.assetid: 4fd39bc2-d814-46de-a108-1c21fa404e8a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c6c8f930fb1fbd82432f6d43dae8b9bed7a563c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814415"
---
# Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración


Antes de implementar un paquete virtualizado de App-V 5,1, debe configurar los grupos de seguridad de servicios de dominio de Active Directory (AD DS) a los que se permitirá el acceso y la ejecución de las aplicaciones. Los grupos de seguridad pueden contener equipos o usuarios. La titulación de un paquete a un grupo de equipos publica el paquete de forma global en todos los equipos del grupo.

Use el siguiente procedimiento para configurar el acceso a paquetes virtualizados.

**Para conceder acceso a un paquete de App-V 5,1**

1.  Busque el paquete que desea configurar:

    1.  Abra la consola de administración de App-V 5,1.

    2.  Para mostrar la página **acceso a ad** , haga clic con el botón derecho en el paquete que desea configurar y seleccione **Editar acceso a Active Directory**. Como alternativa, seleccione el paquete y haga clic en **Editar** en el panel de **acceso ad** .

2.  Aprovisionar un grupo de seguridad para el paquete:

    1.  Vaya a la página **buscar nombres de Active Directory válidos y conceder acceso** .

    2.  Con el formato **mydomain**  \\  **Nombredegrupo**, escriba el nombre o parte del nombre de un objeto de grupo de Active Directory y haga clic en **comprobar**.

        **Nota:**  Asegúrese de proporcionar un nombre de dominio asociado para el grupo que está buscando.

         

3.  Para conceder acceso al paquete, seleccione el grupo que desee y haga clic en **conceder acceso**. El grupo que acaba de agregar se muestra en el panel **entidades de ad con Access** .

4.  

    Para aceptar la configuración predeterminada y cerrar la página de **acceso a ad** , haga clic en **cerrar**.

    Para personalizar la configuración de un grupo específico, haga clic en la lista desplegable **configuraciones asignadas** y seleccione **personalizado**. Para configurar las configuraciones personalizadas, haga clic en **Editar**. Después de conceder acceso, haga clic en **cerrar**.

**Para quitar el acceso a un paquete de App-V 5,1**

1.  Busque el paquete que desea configurar:

    1.  Abra la consola de administración de App-V 5,1.

    2.  Para mostrar la página **acceso a ad** , haga clic con el botón derecho en el paquete que desea configurar y seleccione **Editar acceso a Active Directory**. Como alternativa, seleccione el paquete y haga clic en **Editar** en el panel de **acceso ad** .

2.  Seleccione el grupo que desee quitar y haga clic en **eliminar**.

3.  Para cerrar la página **acceso a ad** , haga clic en **cerrar**.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





