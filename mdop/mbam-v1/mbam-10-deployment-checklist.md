---
title: Lista de comprobación de implementación de MBAM 1.0
description: Lista de comprobación de implementación de MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812535"
---
# <span data-ttu-id="8071a-103">Lista de comprobación de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="8071a-104">Esta lista de comprobación está diseñada para facilitar la implementación de la supervisión y administración de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="8071a-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="8071a-105">Nota</span><span class="sxs-lookup"><span data-stu-id="8071a-105">Note</span></span>**  
<span data-ttu-id="8071a-106">En esta lista de comprobación se describen los pasos recomendados y se proporciona una lista de nivel superior de los elementos que se deben tener en cuenta al implementar las características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8071a-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="8071a-107">Le recomendamos que copie esta lista de comprobación en un programa de hoja de cálculo y la Personalice según sus necesidades específicas.</span><span class="sxs-lookup"><span data-stu-id="8071a-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="8071a-108">Tarea</span><span class="sxs-lookup"><span data-stu-id="8071a-108">Task</span></span></th>
<th align="left"><span data-ttu-id="8071a-109">Referencias</span><span class="sxs-lookup"><span data-stu-id="8071a-109">References</span></span></th>
<th align="left"><span data-ttu-id="8071a-110">Notas</span><span class="sxs-lookup"><span data-stu-id="8071a-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8071a-111">Complete la fase de planeamiento para preparar el entorno informático para la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8071a-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="8071a-112">Lista de comprobación de planificación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8071a-113">Revise la información de MBAM configuraciones compatibles para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8071a-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="8071a-114">Configuraciones admitidas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8071a-115">Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="8071a-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="8071a-116">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="8071a-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="8071a-117">Base de datos de estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8071a-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="8071a-118">Auditoría y informes de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8071a-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="8071a-119">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="8071a-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="8071a-120">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8071a-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="8071a-121">Nota</span><span class="sxs-lookup"><span data-stu-id="8071a-121">Note</span></span></strong><br/><p><span data-ttu-id="8071a-122">Realice un seguimiento de los nombres de los servidores en los que está instalado cada característica.</span><span class="sxs-lookup"><span data-stu-id="8071a-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="8071a-123">Usará esta información durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="8071a-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="8071a-124">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8071a-125">Agregue los grupos de seguridad de los servicios de dominio de Active Directory creados durante la fase de planeación al grupo de administradores de características del servidor de MBAM local adecuado en los servidores correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8071a-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="8071a-126">Planificación de los roles de administrador de MBAM 1,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="8071a-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8071a-127">Cree e implemente los objetos de directiva de grupo MBAM obligatorios.</span><span class="sxs-lookup"><span data-stu-id="8071a-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="8071a-128">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8071a-129">Implemente el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8071a-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="8071a-130">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8071a-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8071a-131">Related topics</span></span>


[<span data-ttu-id="8071a-132">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8071a-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









