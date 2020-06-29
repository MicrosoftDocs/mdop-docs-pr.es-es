---
title: Cambiar la configuración del GPO de MBAM 1.0
description: Cambiar la configuración del GPO de MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824281"
---
# <span data-ttu-id="97816-103">Cambiar la configuración del GPO de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97816-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="97816-104">Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero debe determinar las directivas de grupo que usará en la implementación de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="97816-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="97816-105">Para obtener más información sobre las diversas directivas disponibles, consulte [requisitos de la Directiva de grupo planificación de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="97816-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="97816-106">Una vez que haya determinado las directivas que va a usar, debe modificar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="97816-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="97816-107">Los pasos siguientes describen cómo configurar la configuración de objeto de directiva de grupo (GPO) básica y recomendada para permitir que MBAM administre el cifrado de BitLocker para los equipos cliente de su organización.</span><span class="sxs-lookup"><span data-stu-id="97816-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="97816-108">Para editar la configuración de GPO del cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="97816-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="97816-109">En un equipo que tenga instalada una plantilla de directiva de grupo de MBAM, asegúrese de que los servicios de MBAM estén habilitados.</span><span class="sxs-lookup"><span data-stu-id="97816-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="97816-110">Use la consola de administración de directivas de grupo (GPMC. msc) o el producto de MDOP de administración avanzada de directivas de grupo (AGPM) para estas acciones: seleccione **configuración del equipo**, seleccione **directivas**, haga clic en **plantillas administrativas**, seleccione **componentes de Windows**y, a continuación, haga clic en **MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="97816-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="97816-111">Edite la configuración del objeto de directiva de grupo que se requiere para habilitar los servicios de cliente de MBAM en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="97816-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="97816-112">Para cada directiva de la tabla que sigue, seleccione **grupo de directivas**, haga clic en la **Directiva**y, a continuación, configure la **opción**.</span><span class="sxs-lookup"><span data-stu-id="97816-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="97816-113">Grupo de directivas</span><span class="sxs-lookup"><span data-stu-id="97816-113">Policy Group</span></span>

    <span data-ttu-id="97816-114">Directiva</span><span class="sxs-lookup"><span data-stu-id="97816-114">Policy</span></span>

    <span data-ttu-id="97816-115">Configuración</span><span class="sxs-lookup"><span data-stu-id="97816-115">Setting</span></span>

    <span data-ttu-id="97816-116">Administración de cliente</span><span class="sxs-lookup"><span data-stu-id="97816-116">Client Management</span></span>

    <span data-ttu-id="97816-117">Configurar servicios de MBAM</span><span class="sxs-lookup"><span data-stu-id="97816-117">Configure MBAM Services</span></span>

    <span data-ttu-id="97816-118">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="97816-118">Enabled.</span></span> <span data-ttu-id="97816-119">Configure el **extremo del servicio de hardware y recuperación de MBAM** y **Seleccione información de recuperación de BitLocker para almacenar**.</span><span class="sxs-lookup"><span data-stu-id="97816-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="97816-120">Establezca el **extremo del servicio de cumplimiento normativo de MBAM** e introduzca la **frecuencia del informe de estado en (minutos)**.</span><span class="sxs-lookup"><span data-stu-id="97816-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="97816-121">Permitir la comprobación de compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="97816-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="97816-122">Deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="97816-122">Disabled.</span></span> <span data-ttu-id="97816-123">Esta directiva está habilitada de forma predeterminada, pero no es necesaria para una implementación básica de MBAM.</span><span class="sxs-lookup"><span data-stu-id="97816-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="97816-124">Unidad de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="97816-124">Operating System Drive</span></span>

    <span data-ttu-id="97816-125">Configuración de cifrado de unidad del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="97816-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="97816-126">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="97816-126">Enabled.</span></span> <span data-ttu-id="97816-127">Establezca el **protector seleccionado para la unidad del sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="97816-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="97816-128">Esto es necesario para guardar los datos de la unidad del sistema operativo en el servidor de recuperación de claves MBAM.</span><span class="sxs-lookup"><span data-stu-id="97816-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="97816-129">Unidad extraíble</span><span class="sxs-lookup"><span data-stu-id="97816-129">Removable Drive</span></span>

    <span data-ttu-id="97816-130">Controlar el uso de BitLocker en unidades extraíbles</span><span class="sxs-lookup"><span data-stu-id="97816-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="97816-131">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="97816-131">Enabled.</span></span> <span data-ttu-id="97816-132">Esto es necesario si MBAM guardará los datos de unidades extraíbles en el servidor de recuperación de claves de MBAM.</span><span class="sxs-lookup"><span data-stu-id="97816-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="97816-133">Unidad fija</span><span class="sxs-lookup"><span data-stu-id="97816-133">Fixed Drive</span></span>

    <span data-ttu-id="97816-134">Controlar el uso de BitLocker en unidades fijas</span><span class="sxs-lookup"><span data-stu-id="97816-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="97816-135">Habilitada.</span><span class="sxs-lookup"><span data-stu-id="97816-135">Enabled.</span></span> <span data-ttu-id="97816-136">Esto es necesario si MBAM guardará los datos del disco fijo en el servidor de recuperación de claves de MBAM.</span><span class="sxs-lookup"><span data-stu-id="97816-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="97816-137">Establecer: **Elija cómo se pueden recuperar las unidades protegidas con BitLocker** y **permitir el agente de recuperación de datos**.</span><span class="sxs-lookup"><span data-stu-id="97816-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="97816-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97816-138">Related topics</span></span>


[<span data-ttu-id="97816-139">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97816-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)









