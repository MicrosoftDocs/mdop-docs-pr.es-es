---
title: Cómo cambiar los niveles de informes de registro y restablecer los archivos de registro
description: Cómo cambiar los niveles de informes de registro y restablecer los archivos de registro
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818050"
---
# Cómo cambiar los niveles de informes de registro y restablecer los archivos de registro


Puede usar el siguiente procedimiento para cambiar el nivel de informes de registro del nodo **Application Virtualization** en la consola de administración de virtualización de aplicaciones. Cuando el archivo de registro alcanza el tamaño máximo (el valor predeterminado es 256 MB), se fuerza el restablecimiento cuando se produce la siguiente escritura en el registro. Un restablecimiento hace que se cree un nuevo archivo de registro y el nombre del archivo antiguo es de copia de seguridad.

**Para cambiar el nivel de informes de registro**

1.  Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.

2.  En la pestaña **General** del cuadro de diálogo **propiedades** , en la lista desplegable **nivel de registro** , seleccione el nivel de registro que desee.

    **Nota:**  Si elige **detallado** como nivel de registro, los archivos de registro crecerán muy rápidamente. Esto puede desactivar el rendimiento del cliente, de modo que la práctica recomendada es usar este nivel de registro solo para diagnosticar problemas específicos.

     

3.  En la pestaña **General** del cuadro de diálogo **propiedades** , en la lista desplegable **nivel de registro del sistema** , seleccione el nivel de registro que desee.

    **Nota:**  La configuración del **nivel de registro del sistema** controla el nivel de los mensajes enviados al registro de eventos del sistema. Los mensajes registrados son idénticos a los mensajes que se registran en el registro de eventos del cliente, pero se almacenan en una ubicación diferente.

     

4.  Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.

**Para restablecer el archivo de registro**

1.  Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.

2.  En la pestaña **General** del cuadro de diálogo **propiedades** , haga clic en **restablecer registro** para realizar una copia de seguridad del archivo de registro actual e iniciar inmediatamente un nuevo archivo de registro. Los archivos de registro de la copia de seguridad se almacenan en la misma carpeta.

3.  Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.

## Temas relacionados


[Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[Permisos de acceso de usuario en el cliente de virtualización de aplicaciones](user-access-permissions-in-application-virtualization-client.md)

 

 





