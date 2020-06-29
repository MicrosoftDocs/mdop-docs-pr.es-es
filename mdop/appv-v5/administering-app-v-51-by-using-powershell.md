---
title: Administrar 5.1 de App-V mediante el uso de PowerShell
description: Administrar 5.1 de App-V mediante el uso de PowerShell
author: dansimp
ms.assetid: 9e10ff07-2cd9-4dc1-9e99-582f90c36081
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0c64d7e0330ff5d737dfa02d87f156cc3236b04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814871"
---
# <span data-ttu-id="13957-103">Administrar 5.1 de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-103">Administering App-V 5.1 by Using PowerShell</span></span>


<span data-ttu-id="13957-104">Microsoft Application Virtualization (App-V) 5,1 proporciona cmdlets de Windows PowerShell, que pueden ayudar a los administradores a realizar varias tareas de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="13957-104">Microsoft Application Virtualization (App-V) 5.1 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.1 tasks.</span></span> <span data-ttu-id="13957-105">En las siguientes secciones se proporciona más información sobre cómo usar PowerShell con App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="13957-105">The following sections provide more information about using PowerShell with App-V 5.1.</span></span>

## <span data-ttu-id="13957-106">Cómo administrar App-V 5,1 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-106">How to administer App-V 5.1 by using PowerShell</span></span>


<span data-ttu-id="13957-107">Use los siguientes procedimientos de PowerShell para realizar varias tareas de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="13957-107">Use the following PowerShell procedures to perform various App-V 5.1 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13957-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="13957-108">Name</span></span></th>
<th align="left"><span data-ttu-id="13957-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="13957-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)"><span data-ttu-id="13957-110">Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet</span><span class="sxs-lookup"><span data-stu-id="13957-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-111">Describe cómo instalar los cmdlets de PowerShell y cómo encontrar ayuda y ejemplos de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13957-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="13957-112">Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-112">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-113">Describe cómo administrar el ciclo de vida de paquetes del cliente en un equipo independiente con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md)"><span data-ttu-id="13957-114">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-115">Describe cómo administrar grupos de conexión con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell51.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md)"><span data-ttu-id="13957-116">Cómo modificar la configuración de cliente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-117">Describe cómo modificar el cliente con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)"><span data-ttu-id="13957-118">Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-119">Describe cómo aplicar un archivo de configuración de usuario con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)"><span data-ttu-id="13957-120">Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-121">Describe cómo aplicar un archivo de configuración de implementación con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-51.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-51.md)"><span data-ttu-id="13957-122">Cómo hacer una secuencia de un paquete con PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-123">Describe cómo crear un paquete nuevo con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell51.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md)"><span data-ttu-id="13957-124">Cómo crear un acelerador de paquetes mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-125">Describe cómo crear un acelerador de paquetes con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="13957-126">Puede usar aceleradores de paquetes para hacer secuencias de aplicaciones grandes y complejas de forma automática.</span><span class="sxs-lookup"><span data-stu-id="13957-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)"><span data-ttu-id="13957-127">Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-127">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-128">Describe cómo habilitar el equipo que ejecuta el 5,1 de App-V para enviar información de informes.</span><span class="sxs-lookup"><span data-stu-id="13957-128">Describes how to enable the computer running the App-V 5.1 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md)"><span data-ttu-id="13957-129">Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="13957-130">Describe cómo tomar una matriz de nombres de cuenta y convertir cada una de ellas en el SID correspondiente en formatos hexadecimales y estándar.</span><span class="sxs-lookup"><span data-stu-id="13957-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="13957-131">**Importante**  Asegúrese de que todas las secuencias de comandos que ejecute con los paquetes de App-V coincidan con la Directiva de ejecución que haya configurado para PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-131">**Important** Make sure that any script you execute with your App-V packages matches the execution policy that you have configured for PowerShell.</span></span>

 

## <span data-ttu-id="13957-132">Control de errores de PowerShell</span><span class="sxs-lookup"><span data-stu-id="13957-132">PowerShell Error Handling</span></span>


<span data-ttu-id="13957-133">Use la tabla siguiente para obtener información sobre el control de errores de App-V 5,1 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13957-133">Use the following table for information about App-V 5.1 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13957-134">Evento</span><span class="sxs-lookup"><span data-stu-id="13957-134">Event</span></span></th>
<th align="left"><span data-ttu-id="13957-135">Acción</span><span class="sxs-lookup"><span data-stu-id="13957-135">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13957-136">Usar el atributo RollbackOnError con scripts incrustados</span><span class="sxs-lookup"><span data-stu-id="13957-136">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="13957-137">Al usar el <strong> atributo RollbackOnError </strong> con scripts incrustados, el atributo se omite para los eventos siguientes:</span><span class="sxs-lookup"><span data-stu-id="13957-137">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="13957-138">Quitar un paquete</span><span class="sxs-lookup"><span data-stu-id="13957-138">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="13957-139">Anulando la publicación de un paquete</span><span class="sxs-lookup"><span data-stu-id="13957-139">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="13957-140">Finalizar un entorno virtual</span><span class="sxs-lookup"><span data-stu-id="13957-140">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="13957-141">Finalizar un proceso</span><span class="sxs-lookup"><span data-stu-id="13957-141">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13957-142">El nombre del paquete contiene<strong>$</span><span class="sxs-lookup"><span data-stu-id="13957-142">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="13957-143">Si un nombre de paquete contiene el carácter ( <strong> $ </strong> ), debe usar una comilla simple ( <strong> ' </strong> ); por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="13957-143">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="13957-144">Add-AppvClientPackage ' contoso $ app. appv '</span><span class="sxs-lookup"><span data-stu-id="13957-144">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="13957-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13957-145">Related topics</span></span>


[<span data-ttu-id="13957-146">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="13957-146">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





