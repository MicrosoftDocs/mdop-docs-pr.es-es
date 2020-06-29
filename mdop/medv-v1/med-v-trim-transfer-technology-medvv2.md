---
title: Tecnología de transferencia de recorte de MED-V
description: Tecnología de transferencia de recorte de MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826190"
---
# <span data-ttu-id="10026-103">Tecnología de transferencia de recorte de MED-V</span><span class="sxs-lookup"><span data-stu-id="10026-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="10026-104">La tecnología de desduplicación avanzada de transferencia de guarnecidos de MED-V acelera la descarga de las imágenes de máquina virtual iniciales y actualizadas a través de LAN o WAN, lo que reduce el ancho de banda de red necesario para transportar una máquina virtual de área de trabajo de MED-V a varios usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="10026-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="10026-105">Esta tecnología innovadora usa datos locales existentes para crear la imagen de la máquina virtual, aprovechando el hecho de que, en muchos casos, una gran parte de la máquina virtual (por ejemplo, archivos del sistema y de la aplicación) ya existe en el disco del usuario final.</span><span class="sxs-lookup"><span data-stu-id="10026-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="10026-106">Por ejemplo, si se envía una máquina virtual que contiene WindowsXP a un cliente que ejecuta una copia local de WindowsXP, MED-V eliminará automáticamente los elementos de WindowsXP redundantes de la transferencia.</span><span class="sxs-lookup"><span data-stu-id="10026-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="10026-107">Para garantizar un área de trabajo válida y funcional, el cliente MED-V comprueba de forma criptográfica la integridad de los datos locales antes de su uso, garantizando que los bloques locales de datos son absolutamente bits a los de la imagen de la máquina virtual deseada.</span><span class="sxs-lookup"><span data-stu-id="10026-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="10026-108">Los bloques que no coinciden no se usan.</span><span class="sxs-lookup"><span data-stu-id="10026-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="10026-109">El proceso es transparente y de ancho de banda, y las transferencias se ejecutan en segundo plano, usando recursos de red y de CPU no usados.</span><span class="sxs-lookup"><span data-stu-id="10026-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="10026-110">Al actualizar a una nueva versión de la imagen (por ejemplo, cuando los administradores desean distribuir una nueva aplicación o parche), solo se descargan los elementos que han cambiado ("deltas") y no toda la máquina virtual, lo que reduce significativamente el ancho de banda de red requerido y el tiempo de entrega.</span><span class="sxs-lookup"><span data-stu-id="10026-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="10026-111">Puede configurar qué carpetas se indizan en el host como parte del Protocolo de transferencia de recorte, en función del sistema operativo del host.</span><span class="sxs-lookup"><span data-stu-id="10026-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="10026-112">Estas opciones se configuran en el archivo *ClientSettings.xml* , que se encuentra en la carpeta de **Server\\ de Servers\\Configuration** .</span><span class="sxs-lookup"><span data-stu-id="10026-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="10026-113">Al aplicar la nueva configuración, se debe reiniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="10026-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





