---
title: Instalación de servidor de administración de App-V o servidor de streaming de forma segura
description: Instalación de servidor de administración de App-V o servidor de streaming de forma segura
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816330"
---
# <span data-ttu-id="5ad59-103">Instalación de servidor de administración de App-V o servidor de streaming de forma segura</span><span class="sxs-lookup"><span data-stu-id="5ad59-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="5ad59-104">Los temas de esta sección proporcionan información para instalar una versión de seguridad mejorada del servidor de administración de App-v o del servidor de streaming de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad59-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="5ad59-105">**Nota:**  La instalación o configuración de un servidor de administración o streaming de App-V para usar seguridad mejorada (por ejemplo, la seguridad de la capa de transporte o TLS) requiere que se haya aprovisionado un certificado X. 509 V3 en el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad59-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="5ad59-106">Cuando se prepare para instalar o configurar un servidor de administración o streaming seguro, tenga en cuenta los siguientes requisitos técnicos:</span><span class="sxs-lookup"><span data-stu-id="5ad59-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="5ad59-107">El certificado debe ser válido.</span><span class="sxs-lookup"><span data-stu-id="5ad59-107">The certificate must be valid.</span></span> <span data-ttu-id="5ad59-108">Si el certificado no es válido, el cliente finaliza la conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad59-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="5ad59-109">El certificado debe contener el *uso de clave mejorada* (EKU) correcto: autenticación de servidor (OID 1.3.6.1.5.5.7.3.1).</span><span class="sxs-lookup"><span data-stu-id="5ad59-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="5ad59-110">Si el certificado no contiene este EKU, el cliente finaliza la conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad59-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="5ad59-111">El nombre de dominio completo (FQDN) del certificado debe coincidir con el servidor en el que está instalado.</span><span class="sxs-lookup"><span data-stu-id="5ad59-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="5ad59-112">Por ejemplo, si el cliente está llamando `RTSPS://Myserver.mycompany.com/content/MyApp.sft` y se establece el valor de certificado **emitido para** `Server1.mycompany.com` , el cliente no se conectará al servidor y la sesión finalizará.</span><span class="sxs-lookup"><span data-stu-id="5ad59-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="5ad59-113">El error se notifica al usuario.</span><span class="sxs-lookup"><span data-stu-id="5ad59-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="5ad59-114">**Nota:**  Si está usando App-V en un clúster de equilibrio de carga de red, debe configurar el certificado con nombres alternativos de asunto (San) para admitir RTSPs.</span><span class="sxs-lookup"><span data-stu-id="5ad59-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="5ad59-115">Para obtener información sobre la configuración de la entidad emisora de certificados (CA) y la creación de certificados con redes SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="5ad59-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="5ad59-116">El cliente y el servidor necesitan confiar en la entidad emisora raíz (la CA que emite el certificado al servidor de App-V debe confiar en el cliente que se conecta al servidor).</span><span class="sxs-lookup"><span data-stu-id="5ad59-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="5ad59-117">En caso contrario, el cliente finaliza la conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad59-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="5ad59-118">La clave privada del certificado debe tener permisos cambiados para permitir que la cuenta de servicio de App-V pueda acceder al certificado.</span><span class="sxs-lookup"><span data-stu-id="5ad59-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="5ad59-119">De forma predeterminada, App-V usa la cuenta servicio de red y, de forma predeterminada, la cuenta servicio de red no tiene permiso para obtener acceso a la clave privada, lo que evitará conexiones seguras.</span><span class="sxs-lookup"><span data-stu-id="5ad59-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="5ad59-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5ad59-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="5ad59-121">Configuración de certificados para admitir streaming seguro</span><span class="sxs-lookup"><span data-stu-id="5ad59-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="5ad59-122">Proporciona información sobre cómo obtener, configurar e instalar certificados para admitir la transmisión por secuencias segura.</span><span class="sxs-lookup"><span data-stu-id="5ad59-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="5ad59-123">Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="5ad59-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="5ad59-124">Proporciona procedimientos que puede usar para modificar claves en Windows Server2003 y Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="5ad59-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="5ad59-125">Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="5ad59-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="5ad59-126">Proporciona información sobre cómo configurar certificados para los servidores de administración o streaming de App-V, incluida información sobre la configuración de certificados para entornos de equilibrio de carga de red.</span><span class="sxs-lookup"><span data-stu-id="5ad59-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 





