---
title: Cómo crear un grupo de conexión
description: Cómo crear un grupo de conexión
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814334"
---
# Cómo crear un grupo de conexión


Siga estos pasos para crear un grupo de conexión mediante la consola de administración de App-V. Para usar PowerShell para crear grupos de conexión, consulte [Cómo administrar grupos de conexión en un equipo independiente con PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).

Al colocar paquetes en un grupo de conexión, se fusionan sus rutas de raíz del paquete. Si quita paquetes, solo los paquetes restantes mantienen la raíz combinada.

**Para crear un grupo de conexión**

1.  En la consola de administración de App-V 5,1, seleccione **grupos de conexión** para mostrar la biblioteca de grupos de conexión.

2.  Seleccione **Agregar grupo de conexiones** para crear un nuevo grupo de conexiones.

3.  En el panel **nuevo grupo de conexiones** , escriba una descripción para el grupo.

4.  Haga clic en **Editar** en el panel de **paquetes conectados** para agregar una nueva aplicación al grupo de conexiones.

5.  En el panel **paquetes completos** de la biblioteca, seleccione la aplicación que quiere agregar y haga clic en la flecha para agregar la aplicación.

    Para quitar una aplicación, seleccione la aplicación que se va a quitar en el panel **paquetes en** y haga clic en la flecha.

    Para reestablecer la prioridad de las aplicaciones en el grupo de conexión, use las flechas del panel **paquetes en** .

    **Importante**  De forma predeterminada, las configuraciones de acceso a los servicios de dominio de Active Directory que están asociadas a una aplicación específica no se agregan al grupo de conexiones. Para transferir la configuración de acceso de Active Directory, seleccione **Agregar acceso de paquete a acceso de grupo**, que se encuentra en el panel **paquetes en** .

     

6.  Después de agregar todas las aplicaciones y configurar el acceso a Active Directory, haga clic en **aplicar**.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

[Administración de grupos de conexión](managing-connection-groups51.md)

 

 





