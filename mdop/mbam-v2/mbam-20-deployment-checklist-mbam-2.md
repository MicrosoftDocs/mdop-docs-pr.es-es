---
title: Lista de comprobación de implementación de MBAM 2.0
description: Lista de comprobación de implementación de MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826440"
---
# <span data-ttu-id="2ad57-103">Lista de comprobación de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="2ad57-104">Esta lista de comprobación se puede usar para ayudarle durante la implementación de administración y supervisión de Microsoft BitLocker (MBAM) con una topología independiente.</span><span class="sxs-lookup"><span data-stu-id="2ad57-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="2ad57-105">Nota</span><span class="sxs-lookup"><span data-stu-id="2ad57-105">Note</span></span>**  
<span data-ttu-id="2ad57-106">En esta lista de comprobación se describen los pasos recomendados y una lista de nivel superior de elementos que se deben tener en cuenta al implementar las características de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2ad57-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="2ad57-107">Se recomienda copiar esta lista de comprobación en un programa de hoja de cálculo y personalizarla para su uso.</span><span class="sxs-lookup"><span data-stu-id="2ad57-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="2ad57-108">Tarea</span><span class="sxs-lookup"><span data-stu-id="2ad57-108">Task</span></span></th>
<th align="left"><span data-ttu-id="2ad57-109">Referencias</span><span class="sxs-lookup"><span data-stu-id="2ad57-109">References</span></span></th>
<th align="left"><span data-ttu-id="2ad57-110">Notas</span><span class="sxs-lookup"><span data-stu-id="2ad57-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2ad57-111">Complete la fase de planeamiento para preparar el entorno informático para la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2ad57-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="2ad57-112">Lista de comprobación de planificación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2ad57-113">Revise la información de configuración admitida de MBAM para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2ad57-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="2ad57-114">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2ad57-115">Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="2ad57-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="2ad57-116">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="2ad57-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="2ad57-117">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="2ad57-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="2ad57-118">Auditoría y informes de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="2ad57-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="2ad57-119">Servidor de autoservicio</span><span class="sxs-lookup"><span data-stu-id="2ad57-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="2ad57-120">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="2ad57-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="2ad57-121">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="2ad57-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="2ad57-122">Nota</span><span class="sxs-lookup"><span data-stu-id="2ad57-122">Note</span></span></strong><br/><p><span data-ttu-id="2ad57-123">Realice un seguimiento de los nombres de los servidores en los que está instalado cada característica.</span><span class="sxs-lookup"><span data-stu-id="2ad57-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="2ad57-124">Esta información se utilizará durante todo el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="2ad57-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="2ad57-125">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2ad57-126">Agregue los grupos de seguridad de los servicios de dominio de Active Directory creados durante la fase de planeación al servidor de MBAM local adecuado los administradores de características se agrupan en servidores apropiados.</span><span class="sxs-lookup"><span data-stu-id="2ad57-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="2ad57-127">Planificación de los roles de administrador de MBAM 2,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="2ad57-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2ad57-128">Cree e implemente objetos de directiva de grupo MBAM obligatorios.</span><span class="sxs-lookup"><span data-stu-id="2ad57-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="2ad57-129">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2ad57-130">Implemente el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2ad57-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="2ad57-131">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2ad57-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ad57-132">Related topics</span></span>


[<span data-ttu-id="2ad57-133">Implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2ad57-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









