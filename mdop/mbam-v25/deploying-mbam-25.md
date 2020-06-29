---
title: Implementación de MBAM 2.5
description: Implementación de MBAM 2.5
author: dansimp
ms.assetid: 45403607-1f4d-42fe-8413-0d4da01808a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0cfa0a190530186211cd96884b2e32e9c65881f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826281"
---
# <span data-ttu-id="63b7a-103">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-103">Deploying MBAM 2.5</span></span>


<span data-ttu-id="63b7a-104">Use esta información para identificar los procedimientos que puede seguir para implementar y configurar las características de servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 para actualizar a MBAM 2,5 desde versiones anteriores o para quitar las características de servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="63b7a-104">Use this information to identify the procedures you can follow to deploy and configure Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features to upgrade to MBAM 2.5 from previous versions, or to remove MBAM Server features.</span></span>

## <span data-ttu-id="63b7a-105">Información de implementación</span><span class="sxs-lookup"><span data-stu-id="63b7a-105">Deployment information</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63b7a-106">Descripción del tema</span><span class="sxs-lookup"><span data-stu-id="63b7a-106">Topic description</span></span></th>
<th align="left"><span data-ttu-id="63b7a-107">Vínculos a temas</span><span class="sxs-lookup"><span data-stu-id="63b7a-107">Links to topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="63b7a-108">Opciones de topología de implementación.</span><span class="sxs-lookup"><span data-stu-id="63b7a-108">Deployment topology options.</span></span></p></li>
<li><p><span data-ttu-id="63b7a-109">Cómo instalar el software del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="63b7a-109">How to install the MBAM Server software.</span></span></p></li>
<li><p><span data-ttu-id="63b7a-110">Cómo configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="63b7a-110">How to configure the MBAM Server features.</span></span></p></li>
</ul></td>
<td align="left"><p><a href="deploying-the-mbam-25-server-infrastructure.md" data-raw-source="[Deploying the MBAM 2.5 Server Infrastructure](deploying-the-mbam-25-server-infrastructure.md)"><span data-ttu-id="63b7a-111">Implementación de la infraestructura de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-111">Deploying the MBAM 2.5 Server Infrastructure</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63b7a-112">Cómo descargar e implementar las plantillas de directiva de grupo MBAM, que son necesarias para administrar los clientes de MBAM y las directivas de cifrado de BitLocker en la empresa.</span><span class="sxs-lookup"><span data-stu-id="63b7a-112">How to download and deploy the MBAM Group Policy Templates, which are required to manage MBAM Clients and BitLocker encryption policies in the enterprise.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-25-group-policy-objects.md" data-raw-source="[Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md)"><span data-ttu-id="63b7a-113">Implementación de objetos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-113">Deploying MBAM 2.5 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63b7a-114">Cómo usar los archivos del cliente de Windows Installer de MBAM para implementar el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="63b7a-114">How to use the MBAM Client Windows Installer files to deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="63b7a-115">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-115">Deploying the MBAM 2.5 Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63b7a-116">Lista de comprobación que puede ayudarle a implementar las características del servidor de MBAM y MBAM cliente.</span><span class="sxs-lookup"><span data-stu-id="63b7a-116">Checklist that can assist you in deploying the MBAM Server features and MBAM Client.</span></span></p></td>
<td align="left"><p><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"><span data-ttu-id="63b7a-117">Lista de comprobación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-117">MBAM 2.5 Deployment Checklist</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63b7a-118">Cómo actualizar MBAM desde versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="63b7a-118">How to upgrade MBAM from previous versions.</span></span></p></td>
<td align="left"><p><a href="upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md" data-raw-source="[Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)"><span data-ttu-id="63b7a-119">Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="63b7a-119">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63b7a-120">Cómo quitar el software o las características de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="63b7a-120">How to remove MBAM Server features or software.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="63b7a-121">Quitar las funciones o software de servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="63b7a-121">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="63b7a-122">Otros recursos para implementar MBAM</span><span class="sxs-lookup"><span data-stu-id="63b7a-122">Other resources for deploying MBAM</span></span>


[<span data-ttu-id="63b7a-123">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-123">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="63b7a-124">Introducción a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-124">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="63b7a-125">Planificación para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-125">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="63b7a-126">Operaciones para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-126">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

[<span data-ttu-id="63b7a-127">Solución de problemas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-127">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)

[<span data-ttu-id="63b7a-128">Referencia técnica de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="63b7a-128">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="63b7a-129">Implementar MBAM 2.5 en una configuración independiente</span><span class="sxs-lookup"><span data-stu-id="63b7a-129">Deploying MBAM 2.5 in a stand-alone configuration</span></span>](https://support.microsoft.com/kb/3046555)

## <span data-ttu-id="63b7a-130">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="63b7a-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="63b7a-131">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="63b7a-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="63b7a-132">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="63b7a-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





