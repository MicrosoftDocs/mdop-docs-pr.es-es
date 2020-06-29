---
title: Configuración de certificados para admitir streaming seguro
description: Configuración de certificados para admitir streaming seguro
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821891"
---
# <span data-ttu-id="a055d-103">Configuración de certificados para admitir streaming seguro</span><span class="sxs-lookup"><span data-stu-id="a055d-103">Configuring Certificates to Support Secure Streaming</span></span>


<span data-ttu-id="a055d-104">De forma predeterminada, el servicio App-V se ejecuta en la cuenta servicio de red.</span><span class="sxs-lookup"><span data-stu-id="a055d-104">By default, the App-V service runs under the Network Service account.</span></span> <span data-ttu-id="a055d-105">Sin embargo, puede crear una cuenta de servicio en servicios de dominio de Active Directory y reemplazar la cuenta de servicio de red con la cuenta de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a055d-105">However, you can create a service account in Active Directory Domain Services and replace the Network Service account with the Active Directory Domain account.</span></span>

<span data-ttu-id="a055d-106">El contexto de seguridad en el que se ejecuta el servicio es importante para configurar las comunicaciones seguras mejoradas.</span><span class="sxs-lookup"><span data-stu-id="a055d-106">The security context under which the service runs is important for configuring enhanced secure communications.</span></span> <span data-ttu-id="a055d-107">Este contexto de seguridad debe tener permisos de lectura para la clave privada del certificado.</span><span class="sxs-lookup"><span data-stu-id="a055d-107">This security context must have read permissions for the certificate private key.</span></span> <span data-ttu-id="a055d-108">Cuando se genera una *solicitud de firma de certificado* (CSR) PKCS \ #10 para el servidor de App-V, se llama al proveedor de *servicios criptográficos* de Windows y se genera una clave privada.</span><span class="sxs-lookup"><span data-stu-id="a055d-108">When a PKCS\#10 *Certificate Signing Request* (CSR) is generated for the App-V server, the Windows *Cryptographic Service Provider* is called and a private key is generated.</span></span> <span data-ttu-id="a055d-109">La clave privada está protegida con permisos otorgados únicamente a las cuentas del sistema y del administrador.</span><span class="sxs-lookup"><span data-stu-id="a055d-109">The private key is secured with permissions given to the System and Administrator accounts only.</span></span>

<span data-ttu-id="a055d-110">Debe modificar las listas de control de acceso (ACL) en la clave privada para permitir que el servidor de administración o streaming de App-V acceda a la clave privada necesaria para una comunicación segura de TLS correcta.</span><span class="sxs-lookup"><span data-stu-id="a055d-110">You must modify the access control lists (ACLs) on the private key to let the App-V Management or Streaming Server access the private key required for successful TLS secured communication.</span></span>

## <span data-ttu-id="a055d-111">Obtener e instalar un certificado</span><span class="sxs-lookup"><span data-stu-id="a055d-111">Obtaining and Installing a Certificate</span></span>


<span data-ttu-id="a055d-112">Los escenarios para obtener e instalar un certificado para App-V son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a055d-112">The scenarios for obtaining and installing a certificate for App-V are as follows:</span></span>

-   <span data-ttu-id="a055d-113">Infraestructura de clave pública (PKI) interna.</span><span class="sxs-lookup"><span data-stu-id="a055d-113">Internal public key infrastructure (PKI).</span></span>

-   <span data-ttu-id="a055d-114">Certificado de terceros que emite la entidad de certificación (CA).</span><span class="sxs-lookup"><span data-stu-id="a055d-114">Third-party certificate issuing certification authority (CA).</span></span>

    <span data-ttu-id="a055d-115">**Nota:**  Si necesita obtener un certificado de una entidad emisora de certificados de terceros, siga la documentación disponible en el sitio web de dicha entidad.</span><span class="sxs-lookup"><span data-stu-id="a055d-115">**Note** If you need to obtain a certificate from a third-party CA, follow the documentation available on that CA’s Web site.</span></span>

     

<span data-ttu-id="a055d-116">Si se ha implementado una infraestructura PKI, consulte a los administradores de PKI para adquirir un certificado que cumpla con los requisitos que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="a055d-116">If a PKI infrastructure has been deployed, consult with the PKI administrators to acquire a certificate that complies with the requirements described in this topic.</span></span> <span data-ttu-id="a055d-117">Si la infraestructura de PKI no está disponible, use una entidad de certificación de terceros para obtener un certificado válido.</span><span class="sxs-lookup"><span data-stu-id="a055d-117">If a PKI infrastructure is not available, use a third-party CA to obtain a valid certificate.</span></span>

<span data-ttu-id="a055d-118">Para obtener instrucciones paso a paso para obtener e instalar un certificado, consulte <https://go.microsoft.com/fwlink/?LinkId=151969> .</span><span class="sxs-lookup"><span data-stu-id="a055d-118">For step-by-step guidance for obtaining and installing a certificate, see <https://go.microsoft.com/fwlink/?LinkId=151969>.</span></span>

## <span data-ttu-id="a055d-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a055d-119">Related topics</span></span>


<span data-ttu-id="a055d-120">Configurar certificados para admitir la transmisión por secuencias segura [Cómo modificar los permisos de clave privada para admitir el servidor de administración o el servidor de transmisión](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span><span class="sxs-lookup"><span data-stu-id="a055d-120">Configuring Certificates to Support Secure Streaming [How to Modify Private Key Permissions to Support Management Server or Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span></span>

 

 





