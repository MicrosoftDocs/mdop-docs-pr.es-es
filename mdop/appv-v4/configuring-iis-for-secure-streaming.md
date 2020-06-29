---
title: Configuración de IIS para streaming seguro
description: Configuración de IIS para streaming seguro
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821881"
---
# <span data-ttu-id="5aa63-103">Configuración de IIS para streaming seguro</span><span class="sxs-lookup"><span data-stu-id="5aa63-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="5aa63-104">Con el lanzamiento de Microsoft Application Virtualization (App-V) versión 4,5, puede usar HTTP y HTTPS como protocolos para transmitir paquetes de aplicaciones a los clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="5aa63-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="5aa63-105">Esta opción permite a las organizaciones aprovechar la escalabilidad adicional que suele ofrecer IIS.</span><span class="sxs-lookup"><span data-stu-id="5aa63-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="5aa63-106">Al usar IIS como servidor de transmisión, puede ayudar a proteger las comunicaciones entre el cliente y el servidor mediante HTTPS en lugar de HTTP.</span><span class="sxs-lookup"><span data-stu-id="5aa63-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="5aa63-107">**Nota:**  Si desea transmitir aplicaciones desde un servidor de archivos, debe mejorar la seguridad de las comunicaciones con los paquetes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5aa63-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="5aa63-108">Esto se puede lograr con IPsec.</span><span class="sxs-lookup"><span data-stu-id="5aa63-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="5aa63-109">Para obtener más información, consulte los siguientes temas en la biblioteca de TechNet:</span><span class="sxs-lookup"><span data-stu-id="5aa63-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="5aa63-110">Para Windows Server2003,</span><span class="sxs-lookup"><span data-stu-id="5aa63-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="5aa63-111">Para Windows Server 2008,</span><span class="sxs-lookup"><span data-stu-id="5aa63-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="5aa63-112">Tipos MIME</span><span class="sxs-lookup"><span data-stu-id="5aa63-112">MIME Types</span></span>


<span data-ttu-id="5aa63-113">Al usar IIS para transmitir en secuencias aplicaciones virtuales con HTTP o HTTPS, para admitir App-V, se deben agregar los siguientes tipos MIME al servidor IIS:</span><span class="sxs-lookup"><span data-stu-id="5aa63-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="5aa63-114">. OSD = TXT</span><span class="sxs-lookup"><span data-stu-id="5aa63-114">.OSD=TXT</span></span>

-   <span data-ttu-id="5aa63-115">. SFT = Binary</span><span class="sxs-lookup"><span data-stu-id="5aa63-115">.SFT=Binary</span></span>

<span data-ttu-id="5aa63-116">Use los siguientes artículos de KB como instrucciones para agregar tipos MIME:</span><span class="sxs-lookup"><span data-stu-id="5aa63-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="5aa63-117">IIS 6,0:</span><span class="sxs-lookup"><span data-stu-id="5aa63-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="5aa63-118">IIS 7,0:</span><span class="sxs-lookup"><span data-stu-id="5aa63-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="5aa63-119">Autenticación Kerberos</span><span class="sxs-lookup"><span data-stu-id="5aa63-119">Kerberos Authentication</span></span>


<span data-ttu-id="5aa63-120">Cuando usa HTTP o HTTPS y la autenticación Kerberos para transmitir archivos ICO, OSD o SFT, está mejorando la seguridad de su entorno.</span><span class="sxs-lookup"><span data-stu-id="5aa63-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="5aa63-121">Sin embargo, para que IIS admita la autenticación Kerberos, debe configurar un nombre principal de servicio (SPN) adecuado.</span><span class="sxs-lookup"><span data-stu-id="5aa63-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="5aa63-122">La `setspn.exe` herramienta está disponible para Windows Server2003 en las herramientas de soporte técnico del CD de instalación y está integrada en Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="5aa63-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="5aa63-123">Para crear un SPN, ejecute `setspn.exe` desde un símbolo del sistema al iniciar sesión como miembro de administradores de dominio, por ejemplo, `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="5aa63-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="5aa63-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5aa63-124">Related topics</span></span>


[<span data-ttu-id="5aa63-125">Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras</span><span class="sxs-lookup"><span data-stu-id="5aa63-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





