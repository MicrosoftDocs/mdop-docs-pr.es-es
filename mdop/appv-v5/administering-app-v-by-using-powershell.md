---
title: Administración de App-V mediante el uso de PowerShell
description: Administración de App-V mediante el uso de PowerShell
author: dansimp
ms.assetid: 1ff4686a-1e19-4eff-b648-ada091281094
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e7f9171e0ac5589d8f1935e715dfdb9c349192d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814862"
---
# <span data-ttu-id="28a1b-103">Administración de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-103">Administering App-V by Using PowerShell</span></span>


<span data-ttu-id="28a1b-104">Microsoft Application Virtualization (App-V) 5,0 proporciona cmdlets de Windows PowerShell, que pueden ayudar a los administradores a realizar varias tareas de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="28a1b-104">Microsoft Application Virtualization (App-V) 5.0 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.0 tasks.</span></span> <span data-ttu-id="28a1b-105">En las siguientes secciones se proporciona más información sobre cómo usar PowerShell con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="28a1b-105">The following sections provide more information about using PowerShell with App-V 5.0.</span></span>

## <span data-ttu-id="28a1b-106">Cómo administrar App-V 5,0 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-106">How to administer App-V 5.0 by using PowerShell</span></span>


<span data-ttu-id="28a1b-107">Use los siguientes procedimientos de PowerShell para realizar varias tareas de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="28a1b-107">Use the following PowerShell procedures to perform various App-V 5.0 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28a1b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="28a1b-108">Name</span></span></th>
<th align="left"><span data-ttu-id="28a1b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="28a1b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md)"><span data-ttu-id="28a1b-110">Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet</span><span class="sxs-lookup"><span data-stu-id="28a1b-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-111">Describe cómo instalar los cmdlets de PowerShell y cómo encontrar ayuda y ejemplos de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28a1b-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="28a1b-112">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-112">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-113">Describe cómo administrar el ciclo de vida de paquetes del cliente en un equipo independiente con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="28a1b-114">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-115">Describe cómo administrar grupos de conexión con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md)"><span data-ttu-id="28a1b-116">Cómo modificar la configuración de cliente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-117">Describe cómo modificar el cliente con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)"><span data-ttu-id="28a1b-118">Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-119">Describe cómo aplicar un archivo de configuración de usuario con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)"><span data-ttu-id="28a1b-120">Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-121">Describe cómo aplicar un archivo de configuración de implementación con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-50.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-50.md)"><span data-ttu-id="28a1b-122">Cómo hacer una secuencia de un paquete con PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-123">Describe cómo crear un paquete nuevo con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md)"><span data-ttu-id="28a1b-124">Cómo crear un acelerador de paquetes mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-125">Describe cómo crear un acelerador de paquetes con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="28a1b-126">Puede usar aceleradores de paquetes para hacer secuencias de aplicaciones grandes y complejas de forma automática.</span><span class="sxs-lookup"><span data-stu-id="28a1b-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)"><span data-ttu-id="28a1b-127">Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-127">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-128">Describe cómo habilitar el equipo que ejecuta el 5,0 de App-V para enviar información de informes.</span><span class="sxs-lookup"><span data-stu-id="28a1b-128">Describes how to enable the computer running the App-V 5.0 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md)"><span data-ttu-id="28a1b-129">Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="28a1b-130">Describe cómo tomar una matriz de nombres de cuenta y convertir cada una de ellas en el SID correspondiente en formatos hexadecimales y estándar.</span><span class="sxs-lookup"><span data-stu-id="28a1b-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="28a1b-131">Control de errores de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a1b-131">PowerShell Error Handling</span></span>


<span data-ttu-id="28a1b-132">Use la tabla siguiente para obtener información sobre el control de errores de App-V 5,0 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28a1b-132">Use the following table for information about App-V 5.0 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="28a1b-133">Evento</span><span class="sxs-lookup"><span data-stu-id="28a1b-133">Event</span></span></th>
<th align="left"><span data-ttu-id="28a1b-134">Acción</span><span class="sxs-lookup"><span data-stu-id="28a1b-134">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28a1b-135">Usar el atributo RollbackOnError con scripts incrustados</span><span class="sxs-lookup"><span data-stu-id="28a1b-135">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="28a1b-136">Al usar el <strong> atributo RollbackOnError </strong> con scripts incrustados, el atributo se omite para los eventos siguientes:</span><span class="sxs-lookup"><span data-stu-id="28a1b-136">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="28a1b-137">Quitar un paquete</span><span class="sxs-lookup"><span data-stu-id="28a1b-137">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="28a1b-138">Anulando la publicación de un paquete</span><span class="sxs-lookup"><span data-stu-id="28a1b-138">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="28a1b-139">Finalizar un entorno virtual</span><span class="sxs-lookup"><span data-stu-id="28a1b-139">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="28a1b-140">Finalizar un proceso</span><span class="sxs-lookup"><span data-stu-id="28a1b-140">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28a1b-141">El nombre del paquete contiene<strong>$</span><span class="sxs-lookup"><span data-stu-id="28a1b-141">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="28a1b-142">Si un nombre de paquete contiene el carácter ( <strong> $ </strong> ), debe usar una comilla simple ( <strong> ' </strong> ); por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="28a1b-142">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="28a1b-143">Add-AppvClientPackage ' contoso $ app. appv '</span><span class="sxs-lookup"><span data-stu-id="28a1b-143">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="28a1b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28a1b-144">Related topics</span></span>


[<span data-ttu-id="28a1b-145">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="28a1b-145">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





