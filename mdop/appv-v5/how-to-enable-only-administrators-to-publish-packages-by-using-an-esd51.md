---
title: Cómo habilitar solo a los administradores para publicar paquetes mediante una ESD
description: Cómo habilitar solo a los administradores para publicar paquetes mediante una ESD
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814094"
---
# Cómo habilitar solo a los administradores para publicar paquetes mediante una ESD


A partir de App-V 5,0 SP3, puede configurar el cliente de App-V para que solo los administradores (no los usuarios finales) puedan publicar o anular la publicación de paquetes. En versiones anteriores de App-V, no es posible evitar que los usuarios finales realicen estas tareas.

**Para permitir que solo los administradores publiquen o despubliquen paquetes**

1.  Desplácese hasta el nodo de objeto de directiva de grupo siguiente:

    **Configuración &gt; del equipo Directivas &gt; plantillas administrativas &gt; sistema &gt; App-V &gt; Publishing**.

2.  Habilite la configuración de directiva de grupo **requerir publicación como administrador** .

    Para usar PowerShell como alternativa para establecer este elemento, vea [Cómo administrar paquetes de App-V 5,1 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





