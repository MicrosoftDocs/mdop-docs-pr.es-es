---
title: Lista de comprobación de implementación de MBAM 2.5
description: Lista de comprobación de implementación de MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822831"
---
# <span data-ttu-id="2aff3-103">Lista de comprobación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-103">MBAM 2.5 Deployment Checklist</span></span>


<span data-ttu-id="2aff3-104">Puede usar esta lista de comprobación para ayudarle durante la implementación de Microsoft BitLocker Administration and Monitoring (MBAM) con una topología independiente.</span><span class="sxs-lookup"><span data-stu-id="2aff3-104">You can use this checklist to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="2aff3-105">Nota</span><span class="sxs-lookup"><span data-stu-id="2aff3-105">Note</span></span>**  
<span data-ttu-id="2aff3-106">En esta lista de comprobación se describen los pasos recomendados y una lista de alto nivel de los elementos que hay que tener en cuenta al implementar las características de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2aff3-106">This checklist outlines the recommended steps and a high-level list of items to consider when you deploy Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="2aff3-107">Le recomendamos copiar esta lista de comprobación en un programa de hoja de cálculo y personalizarla para su uso.</span><span class="sxs-lookup"><span data-stu-id="2aff3-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="2aff3-108">Tarea</span><span class="sxs-lookup"><span data-stu-id="2aff3-108">Task</span></span></th>
<th align="left"><span data-ttu-id="2aff3-109">Referencias</span><span class="sxs-lookup"><span data-stu-id="2aff3-109">References</span></span></th>
<th align="left"><span data-ttu-id="2aff3-110">Notas</span><span class="sxs-lookup"><span data-stu-id="2aff3-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-111">Revise y complete todos los pasos de planificación para preparar el entorno para la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2aff3-111">Review and complete all planning steps to prepare your environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)"><span data-ttu-id="2aff3-112">Lista de comprobación de planificación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-112">MBAM 2.5 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-113">Revise la información de configuraciones compatibles para asegurarse de que MBAM admita los equipos cliente y servidor seleccionados.</span><span class="sxs-lookup"><span data-stu-id="2aff3-113">Review the supported configurations information to ensure that MBAM supports the selected client and server computers.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="2aff3-114">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-115">Instale el software de servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="2aff3-115">Install the MBAM Server software.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="2aff3-116">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-116">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-117">Configure las características del servidor de MBAM:</span><span class="sxs-lookup"><span data-stu-id="2aff3-117">Configure the MBAM Server features:</span></span></p>
<ul>
<li><p><span data-ttu-id="2aff3-118">Base de datos de comprobación y cumplimiento de normas y bases de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="2aff3-118">Compliance and Audit Database and Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="2aff3-119">Informes</span><span class="sxs-lookup"><span data-stu-id="2aff3-119">Reports</span></span></p></li>
<li><p><span data-ttu-id="2aff3-120">Aplicaciones Web</span><span class="sxs-lookup"><span data-stu-id="2aff3-120">Web applications</span></span></p></li>
<li><p><span data-ttu-id="2aff3-121">Topología de integración de Configuration Manager (solo es necesario si está ejecutando MBAM con esta topología)</span><span class="sxs-lookup"><span data-stu-id="2aff3-121">Configuration Manager Integration topology (needed only if you are running MBAM with this topology)</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="2aff3-122">Nota</span><span class="sxs-lookup"><span data-stu-id="2aff3-122">Note</span></span></strong><br/><p><span data-ttu-id="2aff3-123">Anote los nombres de los servidores en los que va a configurar cada característica.</span><span class="sxs-lookup"><span data-stu-id="2aff3-123">Note the names of the servers on which you configure each feature.</span></span> <span data-ttu-id="2aff3-124">Usará esta información durante el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="2aff3-124">You will use this information throughout the configuration process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)"><span data-ttu-id="2aff3-125">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-125">Configuring the MBAM 2.5 Server Features</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-126">Valide la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2aff3-126">Validate the MBAM configuration.</span></span></p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)"><span data-ttu-id="2aff3-127">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-127">Validating the MBAM 2.5 Server Feature Configuration</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-128">Copie la plantilla de directiva de grupo MBAM y edite la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2aff3-128">Copy the MBAM Group Policy Template and edit the Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="2aff3-129">Copiar las plantillas de directiva de grupo MBAM 2,5 </a> y <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> editar la configuración de la Directiva de grupo de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="2aff3-129">Copying the MBAM 2.5 Group Policy Templates</a> and <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="2aff3-130">Implemente el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2aff3-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="2aff3-131">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-131">Deploying the MBAM 2.5 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="2aff3-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2aff3-132">Related topics</span></span>


[<span data-ttu-id="2aff3-133">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2aff3-133">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)




## <span data-ttu-id="2aff3-134">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="2aff3-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2aff3-135">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2aff3-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2aff3-136">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2aff3-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




