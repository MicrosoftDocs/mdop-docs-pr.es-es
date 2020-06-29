---
title: Planificación para migrar desde una versión anterior de App-V
description: Planificación para migrar desde una versión anterior de App-V
author: dansimp
ms.assetid: d4ca8f09-86fd-456f-8ec2-242ff94ae9a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2242f58a29473e116506ec013b94a79d1bb814a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813471"
---
# <span data-ttu-id="6349c-103">Planificación para migrar desde una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="6349c-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="6349c-104">Use la siguiente información para planear cómo migrar a App-V 5,0 desde versiones anteriores de App-V.</span><span class="sxs-lookup"><span data-stu-id="6349c-104">Use the following information to plan how to migrate to App-V 5.0 from previous versions of App-V.</span></span>

## <span data-ttu-id="6349c-105">Requisitos de migración</span><span class="sxs-lookup"><span data-stu-id="6349c-105">Migration requirements</span></span>


<span data-ttu-id="6349c-106">Antes de iniciar cualquier actualización, revise los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="6349c-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="6349c-107">Si está actualizando una versión anterior a App-V 4,6 SP2, actualice a la versión App-V 4,6 SP3 en primer lugar antes de actualizar a App-V 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6349c-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.0 or later.</span></span> <span data-ttu-id="6349c-108">En este escenario, actualice los clientes de App-V en primer lugar y, a continuación, actualice los componentes del servidor.</span><span class="sxs-lookup"><span data-stu-id="6349c-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="6349c-109">**Nota:** App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="6349c-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="6349c-110">App-V 5,0 solo admite paquetes que se crean con App-V 5,0 o paquetes que se han convertido al formato App-V 5,0 (**. appv**).</span><span class="sxs-lookup"><span data-stu-id="6349c-110">App-V 5.0 supports only packages that are created using App-V 5.0, or packages that have been converted to the App-V 5.0 (**.appv**) format.</span></span>

-   <span data-ttu-id="6349c-111">App-V 5,0 SP3 solamente: Si va a actualizar el servidor de App-V de App-V 5,0 SP1, consulte [acerca de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="6349c-111">App-V 5.0 SP3 only: If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) for instructions.</span></span>

## <span data-ttu-id="6349c-112">Ejecutar el cliente de App-V 5,0 de forma simultánea con App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="6349c-112">Running the App-V 5.0 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="6349c-113">Puede ejecutar el cliente de App-V 5,0 de forma simultánea en el mismo equipo que el cliente de App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="6349c-113">You can run the App-V 5.0 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="6349c-114">Al ejecutar los clientes coexistentes de App-V, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6349c-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="6349c-115">Convierta un paquete de App-V 4,6 SP3 al formato de App-V 5,0 y publique ambos paquetes cuando tenga ambos clientes ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="6349c-115">Convert an App-V 4.6 SP3 package to the App-V 5.0 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="6349c-116">Defina la Directiva de migración para el paquete convertido, lo que permite que el paquete de App-V 5,0 convertido asuma las asociaciones de tipo de archivo y los accesos directos del paquete de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="6349c-116">Define the migration policy for the converted package, which allows the converted App-V 5.0 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="6349c-117">Escenarios de coexistencia compatibles</span><span class="sxs-lookup"><span data-stu-id="6349c-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="6349c-118">En la siguiente tabla se muestran los escenarios de coexistencia de App-V admitidos.</span><span class="sxs-lookup"><span data-stu-id="6349c-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="6349c-119">Le recomendamos que instale las últimas actualizaciones disponibles de una versión determinada cuando esté ejecutando usuarios coexistentes.</span><span class="sxs-lookup"><span data-stu-id="6349c-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6349c-120">Tipo de cliente de App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="6349c-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="6349c-121">Tipo de cliente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6349c-121">App-V 5.0 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6349c-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="6349c-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="6349c-123">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6349c-123">App-V 5.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6349c-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="6349c-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="6349c-125">App-V 5,0 RDS</span><span class="sxs-lookup"><span data-stu-id="6349c-125">App-V 5.0 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6349c-126">Requisitos para ejecutar clientes coexistentes</span><span class="sxs-lookup"><span data-stu-id="6349c-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="6349c-127">Para ejecutar los clientes coexistentes, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6349c-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="6349c-128">Instale el cliente de App-V 4.6 antes de instalar el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6349c-128">Install the App-V4.6 client before you install the App-V 5.0 client.</span></span>

-   <span data-ttu-id="6349c-129">Habilite la opción **Habilitar modo de migración** de la Directiva de grupo, que se encuentra en el nodo de coexistencia de cliente **de App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="6349c-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="6349c-130">Para obtener la plantilla implementar la. ADMX, consulte [Cómo descargar e implementar las plantillas de la Directiva de grupo de MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="6349c-130">To get the deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

### <span data-ttu-id="6349c-131">Descargas y documentación de clientes</span><span class="sxs-lookup"><span data-stu-id="6349c-131">Client downloads and documentation</span></span>

<span data-ttu-id="6349c-132">En la tabla siguiente se proporciona un vínculo a la documentación de TechNet acerca de las versiones.</span><span class="sxs-lookup"><span data-stu-id="6349c-132">The following table provides link to the TechNet documentation about the releases.</span></span> <span data-ttu-id="6349c-133">La documentación de TechNet sobre el cliente de App-V se aplica a ambos clientes, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="6349c-133">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6349c-134">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="6349c-134">App-V version</span></span></th>
<th align="left"><span data-ttu-id="6349c-135">Vínculo a la documentación de TechNet</span><span class="sxs-lookup"><span data-stu-id="6349c-135">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6349c-136">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="6349c-136">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="6349c-137">Acerca de Microsoft Application Virtualization4.6SP3</span><span class="sxs-lookup"><span data-stu-id="6349c-137">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6349c-138">App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6349c-138">App-V 5.0SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-50-sp3.md" data-raw-source="[About Microsoft Application Virtualization 5.0 SP3](about-app-v-50-sp3.md)"><span data-ttu-id="6349c-139">Acerca de Microsoft Application Virtualization 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6349c-139">About Microsoft Application Virtualization 5.0 SP3</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6349c-140">Para obtener más información sobre cómo configurar la coexistencia de clientes 5,0 de App-V, consulte:</span><span class="sxs-lookup"><span data-stu-id="6349c-140">For more information about how to configure App-V 5.0 client coexistence, see:</span></span>

-   [<span data-ttu-id="6349c-141">Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="6349c-141">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

-   [<span data-ttu-id="6349c-142">Coexistencia y migración de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6349c-142">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="6349c-143">Conversión de paquetes "versión anterior" con el conversor de paquetes</span><span class="sxs-lookup"><span data-stu-id="6349c-143">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="6349c-144">Antes de migrar un paquete, creado con App-V 4.6 SP3 o una versión anterior, a App-V 5,0, revise los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="6349c-144">Before migrating a package, created using App-V4.6SP3 or earlier, to App-V 5.0, review the following requirements:</span></span>

-   <span data-ttu-id="6349c-145">Debe convertir el paquete al formato de archivo **. appv** .</span><span class="sxs-lookup"><span data-stu-id="6349c-145">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="6349c-146">El convertidor de paquetes solo admite la conversión directa de paquetes que se crearon con App-V 4,5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6349c-146">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="6349c-147">Para usar el convertidor de paquetes en un paquete que se creó con una versión anterior, debe usar una versión de App-V 4.5 o posterior del secuenciador para actualizar el paquete y, a continuación, puede realizar la conversión del paquete.</span><span class="sxs-lookup"><span data-stu-id="6349c-147">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="6349c-148">Para obtener más información sobre cómo usar el conversor de paquetes para convertir un paquete, consulte [Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="6349c-148">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span></span> <span data-ttu-id="6349c-149">Después de convertir el archivo, puede implementarlo en equipos de destino que ejecuten el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6349c-149">After you convert the file, you can deploy it to target computers that run the App-V 5.0 client.</span></span>






## <span data-ttu-id="6349c-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6349c-150">Related topics</span></span>


[<span data-ttu-id="6349c-151">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="6349c-151">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





