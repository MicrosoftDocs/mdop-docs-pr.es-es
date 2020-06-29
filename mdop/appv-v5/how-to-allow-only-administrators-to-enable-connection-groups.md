---
title: Cómo permitir que solo los administradores habiliten los grupos de conexión
description: Cómo permitir que solo los administradores habiliten los grupos de conexión
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814462"
---
# <span data-ttu-id="a00e4-103">Cómo permitir que solo los administradores habiliten los grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="a00e4-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="a00e4-104">Puede configurar el cliente de App-V para que solo los administradores (no los usuarios finales) puedan habilitar o deshabilitar grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="a00e4-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="a00e4-105">En versiones anteriores de App-V, no es posible evitar que los usuarios finales realicen estas tareas.</span><span class="sxs-lookup"><span data-stu-id="a00e4-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="a00e4-106">**Nota:** 
 **Esta característica se admite a partir de App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="a00e4-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="a00e4-107">Use uno de los siguientes métodos para permitir que solo los administradores habiliten o deshabiliten grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="a00e4-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a00e4-108">Método</span><span class="sxs-lookup"><span data-stu-id="a00e4-108">Method</span></span></th>
<th align="left"><span data-ttu-id="a00e4-109">Pasos</span><span class="sxs-lookup"><span data-stu-id="a00e4-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a00e4-110">Configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="a00e4-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="a00e4-111">Habilite la configuración de directiva de grupo "requerir publicación como administrador", que se encuentra en el siguiente nodo de objeto de directiva de Grupo:</span><span class="sxs-lookup"><span data-stu-id="a00e4-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="a00e4-112">&gt;Directivas de configuración &gt; del equipo Plantillas administrativas &gt; del sistema &gt; App-V &gt; Publishing</span><span class="sxs-lookup"><span data-stu-id="a00e4-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a00e4-113">Cmdlet de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a00e4-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="a00e4-114">Ejecute el <strong> cmdlet Set-AppvClientConfiguration </strong> con el <strong> parámetro – RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="a00e4-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="a00e4-115">Valores de parámetro:</span><span class="sxs-lookup"><span data-stu-id="a00e4-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="a00e4-116">0-falso</span><span class="sxs-lookup"><span data-stu-id="a00e4-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="a00e4-117">1-verdadero</span><span class="sxs-lookup"><span data-stu-id="a00e4-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="a00e4-118">Ejemplo: </strong> : set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="a00e4-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a00e4-119">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="a00e4-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a00e4-120">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a00e4-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a00e4-121">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="a00e4-121">Got an App-V issue?</span></span>** <span data-ttu-id="a00e4-122">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a00e4-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a00e4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a00e4-123">Related topics</span></span>


[<span data-ttu-id="a00e4-124">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="a00e4-124">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





