---
title: Cómo editar la configuración del GPO de MBAM 2.0
description: Cómo editar la configuración del GPO de MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824090"
---
# <span data-ttu-id="57382-103">Cómo editar la configuración del GPO de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57382-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="57382-104">Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero tiene que determinar las directivas de grupo que usará en la implementación de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="57382-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="57382-105">Consulte [planificación de requisitos de la Directiva de grupo de MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obtener más información sobre las diferentes directivas disponibles.</span><span class="sxs-lookup"><span data-stu-id="57382-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="57382-106">Una vez que haya determinado las directivas que va a usar, debe modificar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de la Directiva para MBAM.</span><span class="sxs-lookup"><span data-stu-id="57382-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="57382-107">Puede usar los siguientes pasos para configurar la configuración de GPO recomendada básica para habilitar MBAM para administrar el cifrado de BitLocker para los equipos cliente de su organización.</span><span class="sxs-lookup"><span data-stu-id="57382-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="57382-108">Para editar la configuración de GPO del cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="57382-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="57382-109">En un equipo que tenga instalada una plantilla de directiva de grupo de MBAM, asegúrese de que los servicios de MBAM estén habilitados.</span><span class="sxs-lookup"><span data-stu-id="57382-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="57382-110">Con la consola de administración de directivas de grupo (GPMC. msc) o el producto MDOP de administración avanzada de directivas de grupo (AGPM) en un equipo con la plantilla de directiva de grupo MBAM instalada, seleccione **configuración del equipo**, elija **directivas**, haga clic en **plantillas administrativas**, seleccione **componentes de Windows**y, a continuación, haga clic en **MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="57382-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="57382-111">Edite la configuración del objeto de directiva de grupo que se requiere para habilitar los servicios de cliente de MBAM en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="57382-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="57382-112">Para cada directiva de la tabla que sigue, seleccione **grupo de directivas**, haga clic en la **Directiva**y, a continuación, configure la **opción**:</span><span class="sxs-lookup"><span data-stu-id="57382-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="57382-113">Grupo de directivas</span><span class="sxs-lookup"><span data-stu-id="57382-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="57382-114">Directiva</span><span class="sxs-lookup"><span data-stu-id="57382-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="57382-115">Configuración</span><span class="sxs-lookup"><span data-stu-id="57382-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="57382-116">Administración de cliente</span><span class="sxs-lookup"><span data-stu-id="57382-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-117">Configurar servicios de MBAM</span><span class="sxs-lookup"><span data-stu-id="57382-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-118">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="57382-118">Enabled.</span></span> <span data-ttu-id="57382-119">Configure el <strong> extremo del servicio de hardware y recuperación de MBAM </strong> y <strong> Seleccione información de recuperación de BitLocker para almacenar </strong> .</span><span class="sxs-lookup"><span data-stu-id="57382-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="57382-120">Establezca el <strong> extremo del servicio de cumplimiento normativo </strong> de MBAM e introduzca la frecuencia del informe de estado en (minutos).</span><span class="sxs-lookup"><span data-stu-id="57382-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="57382-121">Unidad de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="57382-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-122">Configuración de cifrado de unidad del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="57382-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-123">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="57382-123">Enabled.</span></span> <span data-ttu-id="57382-124">Establezca el <strong> protector seleccionado para la unidad del sistema operativo </strong> .</span><span class="sxs-lookup"><span data-stu-id="57382-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="57382-125">Necesario para guardar los datos de la unidad del sistema operativo en el servidor de recuperación de MBAMKey.</span><span class="sxs-lookup"><span data-stu-id="57382-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="57382-126">Unidad extraíble</span><span class="sxs-lookup"><span data-stu-id="57382-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-127">Controlar el uso de BitLocker en unidades extraíbles</span><span class="sxs-lookup"><span data-stu-id="57382-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-128">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="57382-128">Enabled.</span></span> <span data-ttu-id="57382-129">Necesario si MBAM guardará los datos de unidades extraíbles en el servidor de recuperación de claves de MBAM.</span><span class="sxs-lookup"><span data-stu-id="57382-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="57382-130">Unidad fija</span><span class="sxs-lookup"><span data-stu-id="57382-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-131">Controlar el uso de BitLocker en unidades fijas</span><span class="sxs-lookup"><span data-stu-id="57382-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="57382-132">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="57382-132">Enabled.</span></span> <span data-ttu-id="57382-133">Necesario si MBAM guardará los datos del disco fijo en el servidor de recuperación de claves de MBAM.</span><span class="sxs-lookup"><span data-stu-id="57382-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="57382-134">Establecer <strong> : elija cómo se pueden recuperar las unidades protegidas con BitLocker </strong> y <strong> permitir el agente de recuperación de datos </strong> .</span><span class="sxs-lookup"><span data-stu-id="57382-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="57382-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57382-135">Related topics</span></span>


[<span data-ttu-id="57382-136">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="57382-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)









