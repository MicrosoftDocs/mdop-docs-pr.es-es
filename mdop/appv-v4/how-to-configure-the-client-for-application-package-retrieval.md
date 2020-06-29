---
title: Cómo configurar al cliente para la recuperación del paquete de aplicación
description: Cómo configurar al cliente para la recuperación del paquete de aplicación
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817830"
---
# <span data-ttu-id="4d231-103">Cómo configurar al cliente para la recuperación del paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="4d231-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="4d231-104">Cuando el cliente está configurado con un servidor de administración de Application Virtualization (App-V) como su servidor de publicación, de forma predeterminada en el siguiente ciclo de actualización de publicaciones, el cliente recupera del servidor los archivos de manifiesto del paquete y el descriptor de software abierto para cada paquete que el usuario tiene autorizado.</span><span class="sxs-lookup"><span data-stu-id="4d231-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="4d231-105">El cliente usa la información de origen del paquete que se define en estos archivos para determinar dónde encontrar el contenido del paquete, los iconos y las asociaciones de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="4d231-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="4d231-106">Si desea que el cliente obtenga el contenido del paquete (archivo SFT) de un servidor de streaming de App-V local u otra fuente alternativa, como un servidor web o un servidor de archivos, en lugar de desde el servidor de administración de App-V, puede configurar el valor de la clave del registro ApplicationSourceRoot en el equipo para que apunte al recurso compartido de contenido local del otro servidor.</span><span class="sxs-lookup"><span data-stu-id="4d231-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="4d231-107">El archivo OSD aún define la ruta de acceso de origen original para el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="4d231-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="4d231-108">Sin embargo, el cliente usa el valor de la configuración ApplicationSourceRoot en lugar del servidor y el recurso compartido que se especifican en la ruta de contenido en el archivo OSD.</span><span class="sxs-lookup"><span data-stu-id="4d231-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="4d231-109">Esto redirige al cliente para que recupere el contenido del otro servidor.</span><span class="sxs-lookup"><span data-stu-id="4d231-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="4d231-110">También puede configurar los valores de la clave de registro OSDSourceRoot y IconSourceRoot si desea invalidar esta configuración en el archivo de manifiesto del paquete o en las rutas enviadas por un servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="4d231-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="4d231-111">El OSDSourceRoot especifica una ubicación de origen para la recuperación de archivos OSD para un paquete de aplicación durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="4d231-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="4d231-112">El IconSourceRoot especifica una ubicación de origen para la recuperación de iconos para un paquete de la aplicación durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="4d231-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="4d231-113">Nota</span><span class="sxs-lookup"><span data-stu-id="4d231-113">Note</span></span>**  
-   <span data-ttu-id="4d231-114">La configuración de IconSourceRoot y OSDSourceRoot reemplaza los valores del archivo de manifiesto del paquete, por lo que si intenta implementar un paquete con el método de archivo de Windows Installer (. msi), también invalidará los valores en el archivo de manifiesto del paquete contenido en dicho archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="4d231-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="4d231-115">Durante tanto la publicación como las operaciones de transmisión HTTP (S), los clientes de App-V 4,5 SP1 usan la configuración del servidor proxy que está configurada en Internet Explorer en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="4d231-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="4d231-116">Para configurar el valor de la clave del registro ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="4d231-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="4d231-117">Configure el ApplicationSourceRoot en el siguiente valor de la clave del registro con una ruta UNC o una dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4d231-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="4d231-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="4d231-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="4d231-119">El formato correcto para la ruta de acceso de la Convención de nomenclatura universal (UNC) es **\\\\computername\\sharefolder\\\ [carpeta \] \ [\ \ \]**, donde **carpeta** es opcional.</span><span class="sxs-lookup"><span data-stu-id="4d231-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="4d231-120">El **ComputerName** puede ser un nombre de dominio completo (FQDN) o una dirección IP, y **ShareFolder** puede ser una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="4d231-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="4d231-121">Solo se reemplaza la parte de **\\\\computername\\sharedfolder** o letra de unidad de la ruta de acceso de la OSD.</span><span class="sxs-lookup"><span data-stu-id="4d231-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="4d231-122">El formato correcto para la ruta de acceso de la dirección URL es **Protocolo: \ [puerto \] \ [/path\] \ [/\]**, donde **Puerto** y **ruta de acceso** son opcionales.</span><span class="sxs-lookup"><span data-stu-id="4d231-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="4d231-123">Si no se especifica el **Puerto** , se usa el puerto predeterminado para el protocolo.</span><span class="sxs-lookup"><span data-stu-id="4d231-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="4d231-124">Solo se reemplaza la parte **Protocol://Server: Port** de la dirección URL de la OSD.</span><span class="sxs-lookup"><span data-stu-id="4d231-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="4d231-125">Importante</span><span class="sxs-lookup"><span data-stu-id="4d231-125">Important</span></span>**  
    <span data-ttu-id="4d231-126">Las variables de entorno no se admiten en la definición de ApplicationSourceRoot.</span><span class="sxs-lookup"><span data-stu-id="4d231-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="4d231-127">Para configurar el valor de OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="4d231-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="4d231-128">Configure el OSDSourceRoot en el siguiente valor de la clave del registro con una ruta UNC o una dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4d231-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="4d231-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="4d231-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="4d231-130">Los formatos aceptados para el OSDSourceRoot incluyen rutas de direcciones y direcciones URL UNC, como en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4d231-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="4d231-131">**\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o \*\* &lt; unidad &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="4d231-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="4d231-132">**http://computername/productivity/** ni**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="4d231-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="4d231-133">Para configurar el valor de IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="4d231-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="4d231-134">Configure el IconSourceRoot en el siguiente valor de la clave del registro con una ruta UNC o una dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4d231-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="4d231-135">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="4d231-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="4d231-136">Los formatos aceptados para el IconSourceRoot incluyen rutas de direcciones y direcciones URL UNC, como en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4d231-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="4d231-137">**\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o \*\* &lt; unidad &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="4d231-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="4d231-138">**http://computername/productivity/** ni**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="4d231-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="4d231-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d231-139">Related topics</span></span>


[<span data-ttu-id="4d231-140">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="4d231-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









