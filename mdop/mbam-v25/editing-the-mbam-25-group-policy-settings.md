---
title: Edición de configuración de directiva de grupo de MBAM 2.5
description: Edición de configuración de directiva de grupo de MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812598"
---
# <span data-ttu-id="a24d1-103">Edición de configuración de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a24d1-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="a24d1-104">Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), tiene que:</span><span class="sxs-lookup"><span data-stu-id="a24d1-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a24d1-105">Tarea</span><span class="sxs-lookup"><span data-stu-id="a24d1-105">Task</span></span></th>
<th align="left"><span data-ttu-id="a24d1-106">Más información</span><span class="sxs-lookup"><span data-stu-id="a24d1-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a24d1-107">Copie las plantillas de directiva de grupo MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="a24d1-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="a24d1-108">Copia de plantillas de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a24d1-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a24d1-109">Determine los objetos de directiva de grupo (GPO) que desea usar en la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a24d1-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="a24d1-110">Según las necesidades de su organización, es posible que tenga que configurar otras opciones de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a24d1-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="a24d1-111">Planificación de requisitos de la Directiva de grupo de MBAM 2,5 </a> : contiene descripciones de los GPO</span><span class="sxs-lookup"><span data-stu-id="a24d1-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a24d1-112">Establezca la configuración de directiva de grupo para su organización.</span><span class="sxs-lookup"><span data-stu-id="a24d1-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a24d1-113">**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** o MBAM no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="a24d1-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="a24d1-114">Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.</span><span class="sxs-lookup"><span data-stu-id="a24d1-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="a24d1-115">Para editar la configuración de directiva de grupo del cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="a24d1-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="a24d1-116">En un equipo que tenga instaladas las plantillas de directiva de grupo MBAM, asegúrese de que los servicios de MBAM estén habilitados.</span><span class="sxs-lookup"><span data-stu-id="a24d1-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="a24d1-117">Con la consola de administración de directivas de grupo (GPMC. msc) o el producto MDOP de administración avanzada de directivas de grupo de Microsoft en un equipo que tenga instaladas las plantillas de directiva de grupo MBAM, seleccione directivas de **configuración de equipo** de &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="a24d1-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="a24d1-118">Edite la configuración de directiva de grupo que se requiere para habilitar los servicios de cliente de MBAM en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="a24d1-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="a24d1-119">Para cada directiva de la tabla siguiente, seleccione **grupo de directivas**, haga clic en la **Directiva** que desee y, a continuación, configure las opciones.</span><span class="sxs-lookup"><span data-stu-id="a24d1-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a24d1-120">Grupo de directivas</span><span class="sxs-lookup"><span data-stu-id="a24d1-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="a24d1-121">Directiva</span><span class="sxs-lookup"><span data-stu-id="a24d1-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a24d1-122">Administración de cliente</span><span class="sxs-lookup"><span data-stu-id="a24d1-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a24d1-123">Configurar servicios de MBAM</span><span class="sxs-lookup"><span data-stu-id="a24d1-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a24d1-124">Unidad de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a24d1-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a24d1-125">Configuración de cifrado de unidad del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a24d1-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a24d1-126">Unidad extraíble</span><span class="sxs-lookup"><span data-stu-id="a24d1-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a24d1-127">Controlar el uso de BitLocker en unidades extraíbles</span><span class="sxs-lookup"><span data-stu-id="a24d1-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a24d1-128">Unidad fija</span><span class="sxs-lookup"><span data-stu-id="a24d1-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a24d1-129">Controlar el uso de BitLocker en unidades fijas</span><span class="sxs-lookup"><span data-stu-id="a24d1-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="a24d1-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a24d1-130">Related topics</span></span>


[<span data-ttu-id="a24d1-131">Planificación para requisitos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a24d1-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="a24d1-132">Copia de plantillas de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a24d1-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="a24d1-133">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="a24d1-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a24d1-134">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a24d1-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a24d1-135">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a24d1-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





