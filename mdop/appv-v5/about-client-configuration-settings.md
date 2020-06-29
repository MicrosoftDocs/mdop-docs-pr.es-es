---
title: Información acerca de la configuración de cliente
description: Información acerca de la configuración de cliente
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814942"
---
# <span data-ttu-id="53cb9-103">Información acerca de la configuración de cliente</span><span class="sxs-lookup"><span data-stu-id="53cb9-103">About Client Configuration Settings</span></span>


<span data-ttu-id="53cb9-104">El cliente de Microsoft Application Virtualization (App-V) 5,0 almacena su configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="53cb9-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="53cb9-105">Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="53cb9-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="53cb9-106">También puede configurar muchas acciones de cliente cambiando las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="53cb9-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="53cb9-107">En este tema se enumeran los valores de configuración del cliente de App-V 5,0 y se explica su uso.</span><span class="sxs-lookup"><span data-stu-id="53cb9-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="53cb9-108">Puede usar PowerShell para modificar la configuración del cliente.</span><span class="sxs-lookup"><span data-stu-id="53cb9-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="53cb9-109">Para obtener más información sobre cómo usar PowerShell y App-V 5,0 [, consulte Administración de App-v con PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="53cb9-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="53cb9-110">Configuración de cliente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="53cb9-111">En la siguiente tabla se muestra información sobre la configuración del cliente de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="53cb9-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="53cb9-112">Nombre de configuración</span><span class="sxs-lookup"><span data-stu-id="53cb9-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="53cb9-113">Marca de configuración</span><span class="sxs-lookup"><span data-stu-id="53cb9-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="53cb9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="53cb9-114">Description</span></span></th>
<th align="left"><span data-ttu-id="53cb9-115">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="53cb9-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="53cb9-116">Valor de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="53cb9-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="53cb9-117">Valores y claves de estado de directiva deshabilitados</span><span class="sxs-lookup"><span data-stu-id="53cb9-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-118">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="53cb9-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-119">PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="53cb9-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-120">Especifica el directorio donde se instalarán todas las nuevas aplicaciones y actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="53cb9-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="53cb9-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-123">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="53cb9-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="53cb9-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-126">Invalida la ubicación de origen para descargar el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="53cb9-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="53cb9-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-129">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="53cb9-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-131">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-132">Esta opción controla si las aplicaciones virtualizadas se inician en equipos Windows 8 conectados a través de una conexión de red de uso medido (por ejemplo, 4G).</span><span class="sxs-lookup"><span data-stu-id="53cb9-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-133">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="53cb9-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-135">,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="53cb9-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-137">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-138">Especifica el número de veces que se debe volver a intentar una sesión interrumpida.</span><span class="sxs-lookup"><span data-stu-id="53cb9-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-139">Entero (0-99)</span><span class="sxs-lookup"><span data-stu-id="53cb9-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="53cb9-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-141">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-143">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-144">Especifica el número de segundos entre intentos para restablecer una sesión eliminada.</span><span class="sxs-lookup"><span data-stu-id="53cb9-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-145">Entero (0-3600)</span><span class="sxs-lookup"><span data-stu-id="53cb9-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-147">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-148">Autocargar</span><span class="sxs-lookup"><span data-stu-id="53cb9-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-149">Autocargar</span><span class="sxs-lookup"><span data-stu-id="53cb9-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-150">Especifica cómo App-V debe cargar automáticamente los paquetes nuevos en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="53cb9-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-151">(0X0) ninguno; (0x1) previamente usado; (0X2) todos</span><span class="sxs-lookup"><span data-stu-id="53cb9-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="53cb9-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-153">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-154">LocationProvider</span><span class="sxs-lookup"><span data-stu-id="53cb9-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-155">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-156">Especifica el CLSID de una implementación compatible de la interfaz IAppvPackageLocationProvider.</span><span class="sxs-lookup"><span data-stu-id="53cb9-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="53cb9-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-159">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="53cb9-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-161">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-162">Especifica la ruta de acceso a un certificado válido en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="53cb9-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="53cb9-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-165">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="53cb9-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-167">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-168">Comprueba el estado de revocación del certificado de servidor antes de hervir con HTTPS.</span><span class="sxs-lookup"><span data-stu-id="53cb9-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-169">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="53cb9-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-171">,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="53cb9-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="53cb9-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-174">Especifica que el contenido del paquete transmitido no se guardará en el disco duro local.</span><span class="sxs-lookup"><span data-stu-id="53cb9-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-175">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="53cb9-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-177">,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-178">Nombre</span><span class="sxs-lookup"><span data-stu-id="53cb9-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-179">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-179">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-180">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-181">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="53cb9-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-183">Muestra el nombre del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="53cb9-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-184">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-185">Publishing\Servers {serverId} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="53cb9-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-186">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-187">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="53cb9-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-188">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-188">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-189">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-190">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="53cb9-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-192">Muestra la URL del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="53cb9-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-194">Publishing\Servers {serverId} \ URL</span><span class="sxs-lookup"><span data-stu-id="53cb9-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-195">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="53cb9-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-197">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-197">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-198">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-199">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="53cb9-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-201">Permite la actualización global de publicaciones (booleana)</span><span class="sxs-lookup"><span data-stu-id="53cb9-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-202">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-203">Publishing\Servers {serverId} \ GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="53cb9-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-204">Falso</span><span class="sxs-lookup"><span data-stu-id="53cb9-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="53cb9-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-206">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-206">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-207">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-208">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="53cb9-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-210">Desencadena una actualización de publicación global al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="53cb9-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="53cb9-211">Booleana</span><span class="sxs-lookup"><span data-stu-id="53cb9-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-212">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-213">Publishing\Servers {serverId} \ GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="53cb9-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-214">Falso</span><span class="sxs-lookup"><span data-stu-id="53cb9-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-216">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-216">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-217">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-218">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="53cb9-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="53cb9-220">Especifica el intervalo de actualización de publicación mediante el GlobalRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="53cb9-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="53cb9-221">Para deshabilitar la actualización del paquete, seleccione 0.</span><span class="sxs-lookup"><span data-stu-id="53cb9-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-222">Entero (0-744</span><span class="sxs-lookup"><span data-stu-id="53cb9-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-223">Publishing\Servers {serverId} \ GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-224">,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="53cb9-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-226">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-226">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-227">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-228">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="53cb9-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-230">Especifica la unidad de intervalo (hour 0-23, Day 0-31).</span><span class="sxs-lookup"><span data-stu-id="53cb9-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="53cb9-231">0 para la hora, 1 para el día</span><span class="sxs-lookup"><span data-stu-id="53cb9-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-232">Publishing\Servers {serverId} \ GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="53cb9-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-233">uno</span><span class="sxs-lookup"><span data-stu-id="53cb9-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="53cb9-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-235">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-235">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-236">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-237">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="53cb9-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="53cb9-239">Habilita la actualización de publicaciones de usuario (booleana)</span><span class="sxs-lookup"><span data-stu-id="53cb9-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-240">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-241">Publishing\Servers {serverId} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="53cb9-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-242">Falso</span><span class="sxs-lookup"><span data-stu-id="53cb9-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="53cb9-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-244">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-244">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-245">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-246">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="53cb9-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-248">Desencadena una actualización de publicación de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="53cb9-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="53cb9-249">Booleana</span><span class="sxs-lookup"><span data-stu-id="53cb9-249">( Boolean)</span></span></p>
<p><span data-ttu-id="53cb9-250">Recuento de palabras (con espacios): 60</span><span class="sxs-lookup"><span data-stu-id="53cb9-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-251">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-252">Publishing\Servers {serverId} \ UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="53cb9-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-253">Falso</span><span class="sxs-lookup"><span data-stu-id="53cb9-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-255">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-255">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-256">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-257">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="53cb9-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="53cb9-259">Especifica el intervalo de actualización de publicación mediante el UserRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="53cb9-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="53cb9-260">Para deshabilitar la actualización del paquete, seleccione 0.</span><span class="sxs-lookup"><span data-stu-id="53cb9-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="53cb9-261">Recuento de palabras (con espacios): 85</span><span class="sxs-lookup"><span data-stu-id="53cb9-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-262">Entero (0-744 horas)</span><span class="sxs-lookup"><span data-stu-id="53cb9-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-263">Publishing\Servers {serverId} \ UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-264">,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="53cb9-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-266">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-266">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-267">Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="53cb9-268">Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="53cb9-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="53cb9-270">Especifica la unidad de intervalo (hour 0-23, Day 0-31).</span><span class="sxs-lookup"><span data-stu-id="53cb9-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="53cb9-271">0 para la hora, 1 para el día</span><span class="sxs-lookup"><span data-stu-id="53cb9-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-272">Publishing\Servers {serverId} \ UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="53cb9-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-273">uno</span><span class="sxs-lookup"><span data-stu-id="53cb9-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-274">MigrationMode</span><span class="sxs-lookup"><span data-stu-id="53cb9-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-275">MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="53cb9-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-276">El modo de migración permite que el cliente de App-V modifique los accesos directos y los FTA para los paquetes creados con una versión anterior de App-V.</span><span class="sxs-lookup"><span data-stu-id="53cb9-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-277">Verdadero (estado habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="53cb9-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="53cb9-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="53cb9-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-281">Permite que el equipo que ejecuta el cliente de App-V 5,0 recopile y devuelva determinada información de uso para ayudar a mejorar aún más la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53cb9-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-282">0 para deshabilitado; 1 para habilitado</span><span class="sxs-lookup"><span data-stu-id="53cb9-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="53cb9-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-284">,0</span><span class="sxs-lookup"><span data-stu-id="53cb9-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="53cb9-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="53cb9-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-287">Habilita los scripts definidos en el manifiesto del paquete de los archivos de configuración que se deben ejecutar.</span><span class="sxs-lookup"><span data-stu-id="53cb9-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-288">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="53cb9-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="53cb9-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="53cb9-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-292">Especifica las rutas de archivo relativas a% userprofile% que no se mueven con un perfil de usuario&#39;s.</span><span class="sxs-lookup"><span data-stu-id="53cb9-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="53cb9-293">Ejemplo de uso:/ROAMINGFILEEXCLUSIONS =&#39;Desktop; mis imágenes&#39;</span><span class="sxs-lookup"><span data-stu-id="53cb9-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="53cb9-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="53cb9-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-296">Especifica las rutas de registro que no se mueven con un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="53cb9-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="53cb9-297">Ejemplo de uso:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="53cb9-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-298">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="53cb9-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-300">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="53cb9-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-302">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-303">Especifica la ubicación para crear vínculos simbólicos asociados a la versión actual de un paquete publicado por usuario.</span><span class="sxs-lookup"><span data-stu-id="53cb9-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="53cb9-304">todas las extensiones de aplicaciones virtuales, por ejemplo, los accesos directos y las asociaciones de tipos de archivo, señalarán a esta ruta.</span><span class="sxs-lookup"><span data-stu-id="53cb9-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="53cb9-305">Si no especifica una ruta de acceso, los vínculos simbólicos no se usarán al publicar el paquete.</span><span class="sxs-lookup"><span data-stu-id="53cb9-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="53cb9-306">Por ejemplo:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="53cb9-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-307">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="53cb9-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-309">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="53cb9-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-311">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-312">Especifica la ubicación para crear vínculos simbólicos asociados a la versión actual de un paquete publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="53cb9-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="53cb9-313">todas las extensiones de aplicaciones virtuales, por ejemplo, los accesos directos y las asociaciones de tipos de archivo, señalarán a esta ruta.</span><span class="sxs-lookup"><span data-stu-id="53cb9-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="53cb9-314">Si no especifica una ruta de acceso, los vínculos simbólicos no se usarán al publicar el paquete.</span><span class="sxs-lookup"><span data-stu-id="53cb9-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="53cb9-315">Por ejemplo:%allusersprofile%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="53cb9-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-316">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="53cb9-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-318">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="53cb9-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-320">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-321">Una lista delimitada por comas de extensiones de nombre de archivo que se pueden usar para determinar si una aplicación instalada de forma local se puede ejecutar en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="53cb9-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="53cb9-322">Cuando se crean accesos directos, FTAs y otros puntos de extensión durante la publicación, App-V comparará la extensión de nombre de archivo con la lista si la aplicación que está asociada con el punto de extensión está instalada de forma local.</span><span class="sxs-lookup"><span data-stu-id="53cb9-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="53cb9-323">Si se encuentra la extensión, se <strong> </strong> agregará el parámetro de la línea de comandos RunVirtual y la aplicación se ejecutará prácticamente.</span><span class="sxs-lookup"><span data-stu-id="53cb9-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="53cb9-324">Para obtener más información sobre <strong> el </strong> parámetro RunVirtual, vea <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> ejecutar una aplicación instalada de forma local dentro de un entorno virtual con aplicaciones virtualizadas </a> .</span><span class="sxs-lookup"><span data-stu-id="53cb9-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-325">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="53cb9-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-327">Valor de Directiva no escrito</span><span class="sxs-lookup"><span data-stu-id="53cb9-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="53cb9-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-329">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-330">Permite al cliente devolver información a un servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="53cb9-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-331">Verdadero (habilitado); Falso (Estado deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="53cb9-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-333">Falso</span><span class="sxs-lookup"><span data-stu-id="53cb9-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="53cb9-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-335">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-336">Especifica la ubicación en el servidor de informes donde se guarda la información del cliente.</span><span class="sxs-lookup"><span data-stu-id="53cb9-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-337">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="53cb9-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-339">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="53cb9-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-341">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-342">Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes.</span><span class="sxs-lookup"><span data-stu-id="53cb9-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="53cb9-343">El tamaño se aplica a la memoria caché en memoria.</span><span class="sxs-lookup"><span data-stu-id="53cb9-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="53cb9-344">Cuando se alcance el límite, el archivo de registro se retirará.</span><span class="sxs-lookup"><span data-stu-id="53cb9-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="53cb9-345">Establecer entre 0 y 1024.</span><span class="sxs-lookup"><span data-stu-id="53cb9-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-346">Entero [0-1024]</span><span class="sxs-lookup"><span data-stu-id="53cb9-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="53cb9-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-348">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="53cb9-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-350">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-351">Especifica el tamaño máximo en bytes que se va a transmitir al servidor para notificar las solicitudes de carga.</span><span class="sxs-lookup"><span data-stu-id="53cb9-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="53cb9-352">Esto puede ayudar a evitar errores de transmisión permanentes cuando el registro ha alcanzado un tamaño significativo.</span><span class="sxs-lookup"><span data-stu-id="53cb9-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="53cb9-353">Establecer entre 1024 y sin límites.</span><span class="sxs-lookup"><span data-stu-id="53cb9-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-354">Entero [1024-Unlimited]</span><span class="sxs-lookup"><span data-stu-id="53cb9-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="53cb9-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-356">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="53cb9-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-358">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-359">Especifica la hora de inicio del cliente para enviar datos al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="53cb9-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="53cb9-360">Debe especificar un entero válido entre 0-23 que corresponda a la hora del día.</span><span class="sxs-lookup"><span data-stu-id="53cb9-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="53cb9-361">De forma predeterminada, el ReportingStartTime comenzará <strong> </strong> en el día en curso a 10 P. M. o 22.</span><span class="sxs-lookup"><span data-stu-id="53cb9-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-362">Nota</span><span class="sxs-lookup"><span data-stu-id="53cb9-362">Note</span></span></strong><br/><p><span data-ttu-id="53cb9-363">Debe configurar esta opción en una hora en la que es menos probable que los equipos que ejecutan el cliente de App-V 5,0 estén desconectados.</span><span class="sxs-lookup"><span data-stu-id="53cb9-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-364">Entero (0-23)</span><span class="sxs-lookup"><span data-stu-id="53cb9-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-365">Informes \ StartTime</span><span class="sxs-lookup"><span data-stu-id="53cb9-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-366">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-368">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-369">Especifica el intervalo de reintento que usará el cliente para volver a enviar datos al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="53cb9-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-370">Integer</span><span class="sxs-lookup"><span data-stu-id="53cb9-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="53cb9-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-372">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="53cb9-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-374">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-375">Especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="53cb9-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="53cb9-376">Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre 0 y <strong> ReportingRandomDelay, </strong> y esperará la duración especificada antes de enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="53cb9-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="53cb9-377">Esto puede ayudar a evitar colisiones en el servidor.</span><span class="sxs-lookup"><span data-stu-id="53cb9-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-378">Entero [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="53cb9-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="53cb9-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-380">Valor de Directiva no escrito (igual que no configurado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="53cb9-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-382">Importante</span><span class="sxs-lookup"><span data-stu-id="53cb9-382">Important</span></span></strong><br/><p><span data-ttu-id="53cb9-383">Esta opción solo está disponible con App-V 5,0 SP2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="53cb9-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-384">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-385">Permite virtualizar las extensiones de Shell, los objetos de ayuda del explorador y los controles de Active X admitidos y ejecutar las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="53cb9-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-386">1 (habilitado), 0 (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-387">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</span><span class="sxs-lookup"><span data-stu-id="53cb9-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="53cb9-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-389">Importante</span><span class="sxs-lookup"><span data-stu-id="53cb9-389">Important</span></span></strong><br/><p><span data-ttu-id="53cb9-390">Esta opción solo está disponible con App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="53cb9-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-391">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-392">Habilita la barra de progreso de actualización de publicaciones para el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="53cb9-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-393">1 (habilitado), 0 (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-394">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</span><span class="sxs-lookup"><span data-stu-id="53cb9-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cb9-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="53cb9-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="53cb9-396">Importante</span><span class="sxs-lookup"><span data-stu-id="53cb9-396">Important</span></span></strong><br/><p><span data-ttu-id="53cb9-397">Esta opción solo está disponible con App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="53cb9-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="53cb9-398">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-399">Oculta la barra de progreso de actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="53cb9-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-400">1 (habilitado), 0 (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="53cb9-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cb9-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="53cb9-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-402">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="53cb9-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-403">Especifica una lista de rutas de procesos (que pueden contener caracteres comodín), que son candidatas para usar la virtualización dinámica (extensiones de Shell admitidas, objetos auxiliares del explorador y controles ActiveX).</span><span class="sxs-lookup"><span data-stu-id="53cb9-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="53cb9-404">Solo los procesos cuya ruta completa coincida con uno de estos elementos pueden usar la virtualización dinámica.</span><span class="sxs-lookup"><span data-stu-id="53cb9-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-405">Cadena</span><span class="sxs-lookup"><span data-stu-id="53cb9-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="53cb9-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cb9-407">Cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="53cb9-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="53cb9-408">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53cb9-408">Related topics</span></span>


[<span data-ttu-id="53cb9-409">Implementación del secuenciador y del cliente de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="53cb9-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="53cb9-410">Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="53cb9-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="53cb9-411">Cómo implementar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="53cb9-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









