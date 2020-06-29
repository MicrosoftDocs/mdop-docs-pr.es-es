---
title: Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras
description: Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821880"
---
# <span data-ttu-id="33fda-103">Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras</span><span class="sxs-lookup"><span data-stu-id="33fda-103">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>


<span data-ttu-id="33fda-104">Si no se aprovisionó el certificado adecuado antes de instalar el servidor de administración de App-V o el servidor de streaming de App-V, App-V puede configurarse para mejorar la seguridad después de la instalación inicial.</span><span class="sxs-lookup"><span data-stu-id="33fda-104">If the proper certificate was not provisioned before the installation of the App-V Management Server or the App-V Streaming Server, App-V can be configured for enhanced security after the initial installation.</span></span> <span data-ttu-id="33fda-105">Puede configurar el servidor de administración de App-V a través de la consola de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="33fda-105">You can configure the App-V Management Server through the App-V Management Console.</span></span> <span data-ttu-id="33fda-106">Sin embargo, el servidor de streaming de App-V se administra a través del registro.</span><span class="sxs-lookup"><span data-stu-id="33fda-106">However, the App-V Streaming Server is managed through the registry.</span></span> <span data-ttu-id="33fda-107">En cualquier caso, el certificado debe incluir el *uso de clave extendida* (EKU) adecuado para la autenticación del servidor y el servicio de red debe tener acceso de lectura a la clave privada.</span><span class="sxs-lookup"><span data-stu-id="33fda-107">In either case, the certificate must include the proper *extended key usage* (EKU) for Server authentication and the Network Service must have read access to the private key.</span></span>

## <span data-ttu-id="33fda-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="33fda-108">In This Section</span></span>


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[<span data-ttu-id="33fda-109">Cómo configurar la postinstalación de seguridad del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="33fda-109">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)  
<span data-ttu-id="33fda-110">Proporciona un procedimiento que se puede ejecutar después de la instalación, usando la consola de administración de App-V, para agregar el certificado y configurar el servidor de administración de App-V para mejorar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="33fda-110">Provides a procedure that can be performed post-installation, using the App-V Management Console, to add the certificate and configure the App-V Management Server for enhanced security.</span></span>

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[<span data-ttu-id="33fda-111">Cómo configurar la postinstalación de seguridad del servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="33fda-111">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)  
<span data-ttu-id="33fda-112">Proporciona un procedimiento que se puede ejecutar después de la instalación, para agregar el certificado y configurar el servidor de streaming de App-V para mejorar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="33fda-112">Provides a procedure that can be performed post-installation, to add the certificate and configure the App-V Streaming Server for enhanced security.</span></span>

<a href="" id="troubleshooting-certificate-permission-issues"></a>[<span data-ttu-id="33fda-113">Solución de problemas de permisos de certificado</span><span class="sxs-lookup"><span data-stu-id="33fda-113">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)  
<span data-ttu-id="33fda-114">Proporciona instrucciones para la solución de problemas cuando la clave privada no se ha configurado con la ACL adecuada para el servicio de red.</span><span class="sxs-lookup"><span data-stu-id="33fda-114">Provides troubleshooting guidance for when the private key has not been configured with the proper ACL for the Network Service.</span></span>

 

 





