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
# <span data-ttu-id="fbb10-103">Cómo habilitar solo a los administradores para publicar paquetes mediante una ESD</span><span class="sxs-lookup"><span data-stu-id="fbb10-103">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span>


<span data-ttu-id="fbb10-104">A partir de App-V 5,0 SP3, puede configurar el cliente de App-V para que solo los administradores (no los usuarios finales) puedan publicar o anular la publicación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="fbb10-104">Starting in App-V 5.0 SP3, you can configure the App-V client so that only administrators (not end users) can publish or unpublish packages.</span></span> <span data-ttu-id="fbb10-105">En versiones anteriores de App-V, no es posible evitar que los usuarios finales realicen estas tareas.</span><span class="sxs-lookup"><span data-stu-id="fbb10-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

**<span data-ttu-id="fbb10-106">Para permitir que solo los administradores publiquen o despubliquen paquetes</span><span class="sxs-lookup"><span data-stu-id="fbb10-106">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="fbb10-107">Desplácese hasta el nodo de objeto de directiva de grupo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fbb10-107">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="fbb10-108">**Configuración &gt; del equipo Directivas &gt; plantillas administrativas &gt; sistema &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="fbb10-108">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="fbb10-109">Habilite la configuración de directiva de grupo **requerir publicación como administrador** .</span><span class="sxs-lookup"><span data-stu-id="fbb10-109">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="fbb10-110">Para usar PowerShell como alternativa para establecer este elemento, vea [Cómo administrar paquetes de App-V 5,1 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="fbb10-110">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="fbb10-111">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="fbb10-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fbb10-112">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="fbb10-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fbb10-113">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="fbb10-113">Got an App-V issue?</span></span>** <span data-ttu-id="fbb10-114">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="fbb10-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





