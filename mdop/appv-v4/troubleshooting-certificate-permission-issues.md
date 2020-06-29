---
title: Solución de problemas de permisos de certificado
description: Solución de problemas de permisos de certificado
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815210"
---
# <span data-ttu-id="14ec3-103">Solución de problemas de permisos de certificado</span><span class="sxs-lookup"><span data-stu-id="14ec3-103">Troubleshooting Certificate Permission Issues</span></span>


<span data-ttu-id="14ec3-104">Después de la instalación de App-V 4.5, si la clave privada no se ha configurado con la ACL adecuada para el servicio de red, se registra un evento en el registro de eventos de NT y se coloca una entrada en el `Sft-server.log` archivo.</span><span class="sxs-lookup"><span data-stu-id="14ec3-104">After the installation of App-V4.5, if the private key has not been configured with the proper ACL for the Network Service, an event is logged in the NT Event Log and an entry is placed in the `Sft-server.log` file.</span></span>

## <span data-ttu-id="14ec3-105">Mensajes de error</span><span class="sxs-lookup"><span data-stu-id="14ec3-105">Error Messages</span></span>


### <span data-ttu-id="14ec3-106">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="14ec3-106">Windows Server2003</span></span>

<span data-ttu-id="14ec3-107">IDENTIFICADOR de evento 36870: se ha producido un error grave al intentar obtener acceso a la clave privada de la credencial del servidor SSL.</span><span class="sxs-lookup"><span data-stu-id="14ec3-107">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="14ec3-108">El código de error devuelto del módulo criptográfico es 0x80090016.</span><span class="sxs-lookup"><span data-stu-id="14ec3-108">The error code returned from the cryptographic module is 0x80090016.</span></span>

### <span data-ttu-id="14ec3-109">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="14ec3-109">Windows Server2008</span></span>

<span data-ttu-id="14ec3-110">IDENTIFICADOR de evento 36870: se ha producido un error grave al intentar obtener acceso a la clave privada de la credencial del servidor SSL.</span><span class="sxs-lookup"><span data-stu-id="14ec3-110">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="14ec3-111">El código de error devuelto del módulo criptográfico es 0x8009030d.</span><span class="sxs-lookup"><span data-stu-id="14ec3-111">The error code returned from the cryptographic module is 0x8009030d.</span></span>

## <span data-ttu-id="14ec3-112">SFT-Server. log</span><span class="sxs-lookup"><span data-stu-id="14ec3-112">Sft-server.log</span></span>


<span data-ttu-id="14ec3-113">El error siguiente se coloca en el `sft-server.log` archivo que se encuentra en el `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` Directorio:</span><span class="sxs-lookup"><span data-stu-id="14ec3-113">The following error is placed in the `sft-server.log` file located in the `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` directory:</span></span>

<span data-ttu-id="14ec3-114">No se pudo cargar el certificado.</span><span class="sxs-lookup"><span data-stu-id="14ec3-114">Certificate could not be loaded.</span></span> <span data-ttu-id="14ec3-115">Código de error \ [-2146893043 \].</span><span class="sxs-lookup"><span data-stu-id="14ec3-115">Error code \[-2146893043\].</span></span> <span data-ttu-id="14ec3-116">Asegúrese de que la cuenta de servicio de red tiene acceso adecuado al certificado y al archivo de clave privada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="14ec3-116">Make sure that the Network Service account has proper access to the certificate and its corresponding private key file.</span></span>

 

 





