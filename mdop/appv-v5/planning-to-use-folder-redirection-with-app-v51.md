---
title: Planificación para usar Redirección de carpetas con App-V
description: Planificación para usar Redirección de carpetas con App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813383"
---
# <span data-ttu-id="b5759-103">Planificación para usar Redirección de carpetas con App-V</span><span class="sxs-lookup"><span data-stu-id="b5759-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="b5759-104">Microsoft Application Virtualization (App-V) 5,1 admite el uso de la redirección de carpetas, una característica que permite a los usuarios y administradores redirigir la ruta de acceso de una carpeta a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="b5759-104">Microsoft Application Virtualization (App-V) 5.1 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="b5759-105">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="b5759-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b5759-106">Requisitos para usar el redireccionamiento de carpetas</span><span class="sxs-lookup"><span data-stu-id="b5759-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="b5759-107">Cómo configurar el redireccionamiento de carpetas para su uso con App-V</span><span class="sxs-lookup"><span data-stu-id="b5759-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="b5759-108">Cómo funciona el redireccionamiento de carpetas con App-V</span><span class="sxs-lookup"><span data-stu-id="b5759-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="b5759-109">Información general sobre el redireccionamiento de carpetas</span><span class="sxs-lookup"><span data-stu-id="b5759-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="b5759-110">Requisitos y escenarios no admitidos para usar el redireccionamiento de carpetas</span><span class="sxs-lookup"><span data-stu-id="b5759-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5759-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5759-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-112">Para usar el redireccionamiento de la carpeta% AppData%, debe:</span><span class="sxs-lookup"><span data-stu-id="b5759-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5759-113">Tener un paquete de App-V que tenga una carpeta de sistema de archivos virtual (VFS) de AppData.</span><span class="sxs-lookup"><span data-stu-id="b5759-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="b5759-114">Habilitar el redireccionamiento de carpetas y redirigir las carpetas de los usuarios a una carpeta compartida, normalmente una carpeta de red.</span><span class="sxs-lookup"><span data-stu-id="b5759-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="b5759-115">Mueva ambos o ninguno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b5759-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5759-116">Archivos en%appdata%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="b5759-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="b5759-117">Configuración del registro en HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</span><span class="sxs-lookup"><span data-stu-id="b5759-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="b5759-118">Para obtener más información, consulte <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> publicación de aplicaciones e interacción de clientes </a> .</span><span class="sxs-lookup"><span data-stu-id="b5759-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="b5759-119">Asegúrese de que las siguientes carpetas estén disponibles para todos los usuarios que inicien sesión en el equipo que ejecuta el cliente de App-V 5,0 SP2 o posterior:</span><span class="sxs-lookup"><span data-stu-id="b5759-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5759-120">% AppData% se ha configurado en la ubicación de red deseada (con o sin <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> compatibilidad con archivos sin conexión </a> ).</span><span class="sxs-lookup"><span data-stu-id="b5759-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="b5759-121">% LocalAppData% está configurado en la carpeta local deseada.</span><span class="sxs-lookup"><span data-stu-id="b5759-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5759-122">Escenarios no admitidos</span><span class="sxs-lookup"><span data-stu-id="b5759-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b5759-123">Configurando% LocalAppData% como unidad de red.</span><span class="sxs-lookup"><span data-stu-id="b5759-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="b5759-124">Redirigir el menú Inicio a una única carpeta para varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="b5759-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="b5759-125">Si AppData de roaming (% AppData%) se redirige a un recurso compartido de red que no está disponible, las aplicaciones de App-V no se iniciarán de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b5759-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5759-126">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="b5759-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="b5759-127">Descripción del escenario</span><span class="sxs-lookup"><span data-stu-id="b5759-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5759-128">En App-V 5,0 a través de App-V 5,0 SP2 Plus revisados</span><span class="sxs-lookup"><span data-stu-id="b5759-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-129">Este error se producirá independientemente de si está habilitada la opción archivos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b5759-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5759-130">En App-V 5,0 SP3 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b5759-130">In App-V 5.0 SP3 and later</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-131">Si el recurso compartido de red no disponible está habilitado para archivos sin conexión, la aplicación de App-V se iniciará correctamente.</span><span class="sxs-lookup"><span data-stu-id="b5759-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="b5759-132">Cómo configurar el redireccionamiento de carpetas para su uso con App-V</span><span class="sxs-lookup"><span data-stu-id="b5759-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="b5759-133">El redireccionamiento de carpetas se puede aplicar a diferentes carpetas, como escritorio, mis documentos, mis imágenes, etc. Sin embargo, la única carpeta que afecta al uso de las aplicaciones de App-V es la carpeta de roaming del usuario (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="b5759-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="b5759-134">Puede aplicar el redireccionamiento de carpetas a cualquier otra carpeta compatible sin afectar a App-V.</span><span class="sxs-lookup"><span data-stu-id="b5759-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="b5759-135">Cómo funciona el redireccionamiento de carpetas con App-V</span><span class="sxs-lookup"><span data-stu-id="b5759-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="b5759-136">En la tabla siguiente se describe cómo funciona el redireccionamiento de carpetas cuando% AppData% se redirige a una red y cuando se cumplen los requisitos mencionados anteriormente en este artículo.</span><span class="sxs-lookup"><span data-stu-id="b5759-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5759-137">Estado de entorno virtual</span><span class="sxs-lookup"><span data-stu-id="b5759-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="b5759-138">Acción que se produce</span><span class="sxs-lookup"><span data-stu-id="b5759-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5759-139">Cuando se inicia el entorno virtual</span><span class="sxs-lookup"><span data-stu-id="b5759-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-140">La carpeta del sistema de archivos virtual (VFS) está asignada a la carpeta local AppData (% LocalAppData%) en lugar de en la carpeta AppData del usuario (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="b5759-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="b5759-141">LocalAppData contiene una caché local de la carpeta de roaming de roaming del usuario para el paquete en uso.</span><span class="sxs-lookup"><span data-stu-id="b5759-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="b5759-142">La memoria caché local se encuentra en:</span><span class="sxs-lookup"><span data-stu-id="b5759-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="b5759-143">Los datos más recientes de la carpeta de usuarios móviles AppData se copian y reemplazan a los datos que se encuentran actualmente en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="b5759-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="b5759-144">Mientras el entorno virtual se está ejecutando, los datos continúan guardándose en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="b5759-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="b5759-145">Los datos se atienden solo de% LocalAppData% y no se mueven o se sincronizan con% AppData% hasta que el usuario final apague el equipo.</span><span class="sxs-lookup"><span data-stu-id="b5759-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="b5759-146">Las entradas de la carpeta AppData se realizan con el contexto del usuario, no con el contexto del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5759-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="b5759-147">Nota</span><span class="sxs-lookup"><span data-stu-id="b5759-147">Note</span></span></strong><br/><p><span data-ttu-id="b5759-148">En ocasiones, el redireccionamiento de carpetas del cliente de App-V no mueve los archivos de% AppData% a% LocalAppData%.</span><span class="sxs-lookup"><span data-stu-id="b5759-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="b5759-149">Consulte las <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> notas de la versión de App-V 5,0 SP2 </a> .</span><span class="sxs-lookup"><span data-stu-id="b5759-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5759-150">Cuando se apaga el entorno virtual</span><span class="sxs-lookup"><span data-stu-id="b5759-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-151">Los datos locales almacenados en la caché de AppData (roaming) se comprimen y se copian en la carpeta "real" roaming de itinerancia de% AppData%.</span><span class="sxs-lookup"><span data-stu-id="b5759-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="b5759-152">Una marca de tiempo, que indica la última carga conocida, se guarda de forma simultánea como una clave del registro en:</span><span class="sxs-lookup"><span data-stu-id="b5759-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="b5759-153">Para proporcionar redundancia, App-V mantiene las tres copias más recientes de los datos comprimidos en% AppData%.</span><span class="sxs-lookup"><span data-stu-id="b5759-153">To provide redundancy, App-V keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="b5759-154">Información general sobre el redireccionamiento de carpetas</span><span class="sxs-lookup"><span data-stu-id="b5759-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5759-155">Propósito</span><span class="sxs-lookup"><span data-stu-id="b5759-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-156">Permite a los usuarios finales trabajar con archivos, que se han redirigido a otra carpeta, como si los archivos siguen existiendo en la unidad local.</span><span class="sxs-lookup"><span data-stu-id="b5759-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5759-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5759-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-158">El redireccionamiento de carpetas permite a los usuarios y administradores redirigir la ruta de acceso de una carpeta a una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="b5759-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="b5759-159">Los documentos de la carpeta están disponibles para el usuario desde cualquier PC de la red.</span><span class="sxs-lookup"><span data-stu-id="b5759-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="b5759-160">El redireccionamiento de carpetas permite a los usuarios y administradores redirigir la ruta de acceso de una carpeta a una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="b5759-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="b5759-161">Los documentos de la carpeta están disponibles para el usuario desde cualquier PC de la red.</span><span class="sxs-lookup"><span data-stu-id="b5759-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="b5759-162">La nueva ubicación puede ser una carpeta en el equipo local o una carpeta en una red compartida.</span><span class="sxs-lookup"><span data-stu-id="b5759-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="b5759-163">El redireccionamiento de carpetas actualiza los archivos inmediatamente, mientras que los datos de itinerancia suelen sincronizarse cuando el usuario inicia sesión o cierra sesión.</span><span class="sxs-lookup"><span data-stu-id="b5759-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5759-164">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="b5759-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5759-165">Puede redirigir la carpeta documentos, que normalmente se almacena en el disco duro local del equipo&#39;s, a una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="b5759-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="b5759-166">El usuario puede acceder a los documentos de la carpeta desde cualquier equipo de la red.</span><span class="sxs-lookup"><span data-stu-id="b5759-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5759-167">Más recursos</span><span class="sxs-lookup"><span data-stu-id="b5759-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="b5759-168">Información general sobre el redireccionamiento de carpetas</span><span class="sxs-lookup"><span data-stu-id="b5759-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>
















