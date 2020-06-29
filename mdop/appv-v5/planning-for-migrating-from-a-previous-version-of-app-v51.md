---
title: Planificación para migrar desde una versión anterior de App-V
description: Planificación para migrar desde una versión anterior de App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813470"
---
# <span data-ttu-id="a6190-103">Planificación para migrar desde una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="a6190-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="a6190-104">Use la siguiente información para planear cómo migrar a Microsoft Application Virtualization (App-V) 5,1 desde versiones anteriores de App-V.</span><span class="sxs-lookup"><span data-stu-id="a6190-104">Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) 5.1 from previous versions of App-V.</span></span>

## <span data-ttu-id="a6190-105">Requisitos de migración</span><span class="sxs-lookup"><span data-stu-id="a6190-105">Migration requirements</span></span>


<span data-ttu-id="a6190-106">Antes de iniciar cualquier actualización, revise los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="a6190-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="a6190-107">Si está actualizando una versión anterior a App-V 4,6 SP2, actualice a la versión App-V 4,6 SP3 en primer lugar antes de actualizar a App-V 5,1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a6190-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.1 or later.</span></span> <span data-ttu-id="a6190-108">En este escenario, actualice los clientes de App-V en primer lugar y, a continuación, actualice los componentes del servidor.</span><span class="sxs-lookup"><span data-stu-id="a6190-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="a6190-109">**Nota:** App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="a6190-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="a6190-110">App-V 5,1 solo admite paquetes creados con App-V 5,0 o App-V 5,1, o paquetes que se han convertido al formato **. appv** .</span><span class="sxs-lookup"><span data-stu-id="a6190-110">App-V 5.1 supports only packages that are created using App-V 5.0 or App-V 5.1, or packages that have been converted to the **.appv** format.</span></span>

-   <span data-ttu-id="a6190-111">Si está actualizando el servidor de App-V de App-V 5,0 SP1, consulte [acerca de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="a6190-111">If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51) for instructions.</span></span>

## <span data-ttu-id="a6190-112">Ejecutar el cliente de App-V 5,1 de forma simultánea con App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="a6190-112">Running the App-V 5.1 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="a6190-113">Puede ejecutar el cliente de App-V 5,1 de forma simultánea en el mismo equipo que el cliente de App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="a6190-113">You can run the App-V 5.1 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="a6190-114">Al ejecutar los clientes coexistentes de App-V, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a6190-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="a6190-115">Convierta un paquete de App-V 4,6 SP3 al formato de App-V 5,1 y publique ambos paquetes cuando tenga ambos clientes ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="a6190-115">Convert an App-V 4.6 SP3 package to the App-V 5.1 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="a6190-116">Defina la Directiva de migración para el paquete convertido, lo que permite que el paquete de App-V 5,1 convertido asuma las asociaciones de tipo de archivo y los accesos directos del paquete de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="a6190-116">Define the migration policy for the converted package, which allows the converted App-V 5.1 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="a6190-117">Escenarios de coexistencia compatibles</span><span class="sxs-lookup"><span data-stu-id="a6190-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="a6190-118">En la siguiente tabla se muestran los escenarios de coexistencia de App-V admitidos.</span><span class="sxs-lookup"><span data-stu-id="a6190-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="a6190-119">Le recomendamos que instale las últimas actualizaciones disponibles de una versión determinada cuando esté ejecutando usuarios coexistentes.</span><span class="sxs-lookup"><span data-stu-id="a6190-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a6190-120">Tipo de cliente de App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="a6190-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="a6190-121">Tipo de cliente de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a6190-121">App-V 5.1 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a6190-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="a6190-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="a6190-123">5.1 de App-V</span><span class="sxs-lookup"><span data-stu-id="a6190-123">App-V 5.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a6190-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="a6190-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="a6190-125">App-V 5,1 RDS</span><span class="sxs-lookup"><span data-stu-id="a6190-125">App-V 5.1 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a6190-126">Requisitos para ejecutar clientes coexistentes</span><span class="sxs-lookup"><span data-stu-id="a6190-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="a6190-127">Para ejecutar los clientes coexistentes, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a6190-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="a6190-128">Instale el cliente de App-V 4.6 antes de instalar el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a6190-128">Install the App-V4.6 client before you install the App-V 5.1 client.</span></span>

-   <span data-ttu-id="a6190-129">Habilite la opción **Habilitar modo de migración** de la Directiva de grupo, que se encuentra en el nodo de coexistencia de cliente **de App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="a6190-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="a6190-130">Para implementar la plantilla. ADMX, consulte [Cómo descargar e implementar las plantillas de la Directiva de grupo de MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6190-130">To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

<span data-ttu-id="a6190-131">**Nota:**  Los paquetes de App-V 5,1 se pueden ejecutar en paralelo con los paquetes de App-V 4,6 Si tiene instalaciones coexistentes de App-V 5,1 y 4,6.</span><span class="sxs-lookup"><span data-stu-id="a6190-131">**Note** App-V 5.1 packages can run side by side with App-V 4.6 packages if you have coexisting installations of App-V 5.1 and 4.6.</span></span> <span data-ttu-id="a6190-132">Sin embargo, los paquetes de App-V 5,1 no pueden interactuar con paquetes de App-V 4,6 en el mismo entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="a6190-132">However, App-V 5.1 packages cannot interact with App-V 4.6 packages in the same virtual environment.</span></span>

 

### <span data-ttu-id="a6190-133">Descargas y documentación de clientes</span><span class="sxs-lookup"><span data-stu-id="a6190-133">Client downloads and documentation</span></span>

<span data-ttu-id="a6190-134">La siguiente tabla proporciona vínculos a las descargas de los clientes de App-V 4,6 y a la documentación de TechNet acerca de las versiones.</span><span class="sxs-lookup"><span data-stu-id="a6190-134">The following table provides links to the App-V 4.6 client downloads and to the TechNet documentation about the releases.</span></span> <span data-ttu-id="a6190-135">Entre las descargas se incluyen los clientes "normales" de App-V y RDS.</span><span class="sxs-lookup"><span data-stu-id="a6190-135">The downloads include the App-V “regular” and RDS clients.</span></span> <span data-ttu-id="a6190-136">La documentación de TechNet sobre el cliente de App-V se aplica a ambos clientes, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="a6190-136">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a6190-137">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="a6190-137">App-V version</span></span></th>
<th align="left"><span data-ttu-id="a6190-138">Vínculo a la documentación de TechNet</span><span class="sxs-lookup"><span data-stu-id="a6190-138">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a6190-139">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="a6190-139">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="a6190-140">Acerca de Microsoft Application Virtualization4.6SP3</span><span class="sxs-lookup"><span data-stu-id="a6190-140">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a6190-141">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="a6190-141">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)"><span data-ttu-id="a6190-142">Acerca de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="a6190-142">About Microsoft Application Virtualization 5.1</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a6190-143">Para obtener más información sobre cómo configurar la coexistencia de clientes 5,1 de App-V, consulte:</span><span class="sxs-lookup"><span data-stu-id="a6190-143">For more information about how to configure App-V 5.1 client coexistence, see:</span></span>

-   [<span data-ttu-id="a6190-144">Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="a6190-144">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [<span data-ttu-id="a6190-145">Coexistencia y migración de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a6190-145">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="a6190-146">Conversión de paquetes "versión anterior" con el conversor de paquetes</span><span class="sxs-lookup"><span data-stu-id="a6190-146">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="a6190-147">Antes de migrar un paquete, creado con App-4.6 SP2 o una versión anterior, a App-V 5,1, revise los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="a6190-147">Before migrating a package, created using App-4.6SP2 or earlier, to App-V 5.1, review the following requirements:</span></span>

-   <span data-ttu-id="a6190-148">Debe convertir el paquete al formato de archivo **. appv** .</span><span class="sxs-lookup"><span data-stu-id="a6190-148">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="a6190-149">El convertidor de paquetes solo admite la conversión directa de paquetes que se crearon con App-V 4,5 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6190-149">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="a6190-150">Para usar el convertidor de paquetes en un paquete que se creó con una versión anterior, debe usar una versión de App-V 4.5 o posterior del secuenciador para actualizar el paquete y, a continuación, puede realizar la conversión del paquete.</span><span class="sxs-lookup"><span data-stu-id="a6190-150">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="a6190-151">Para obtener más información sobre cómo usar el conversor de paquetes para convertir un paquete, consulte [Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="a6190-151">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span></span> <span data-ttu-id="a6190-152">Después de convertir el archivo, puede implementarlo en equipos de destino que ejecuten el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a6190-152">After you convert the file, you can deploy it to target computers that run the App-V 5.1 client.</span></span>






## <span data-ttu-id="a6190-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6190-153">Related topics</span></span>


[<span data-ttu-id="a6190-154">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="a6190-154">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





