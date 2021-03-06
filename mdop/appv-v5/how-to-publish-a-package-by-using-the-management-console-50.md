---
title: Cómo publicar un paquete mediante el uso de la consola de administración
description: Cómo publicar un paquete mediante el uso de la consola de administración
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813783"
---
# Cómo publicar un paquete mediante el uso de la consola de administración


Use el siguiente procedimiento para publicar un paquete de App-V 5,0. Una vez que publique un paquete, los equipos que ejecuten el cliente App-V 5,0 pueden acceder a las aplicaciones de ese paquete y ejecutarlas.

**Nota:**  La capacidad de habilitar solo a los administradores para publicar o anular la publicación de paquetes (descritos a continuación) se permite a partir de App-V 5,0 SP3.

 

**Para publicar un paquete de App-V 5,0**

1.  En la consola de administración de App-V 5,0. Haga clic con el botón derecho en el nombre del paquete que se va a publicar y seleccione **publicar**.

2.  Revise la columna **Estado** para comprobar que el paquete se ha publicado y que ya está disponible. Si el paquete está disponible, se muestra el estado **publicado** .

    Si el paquete no se publica correctamente, se muestra el estado sin **publicar** , junto con el texto del error que explica por qué el paquete no está disponible.

**Para permitir que solo los administradores publiquen o despubliquen paquetes**

1.  Desplácese hasta el nodo de objeto de directiva de grupo siguiente:

    **Configuración &gt; del equipo Directivas &gt; plantillas administrativas &gt; sistema &gt; App-V &gt; Publishing**.

2.  Habilite la configuración de directiva de grupo **requerir publicación como administrador** .

    Para usar PowerShell como alternativa para establecer este elemento, vea [Cómo administrar paquetes de App-V 5,0 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

[Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





