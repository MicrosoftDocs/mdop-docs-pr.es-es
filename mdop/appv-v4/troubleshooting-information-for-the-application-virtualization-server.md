---
title: Información de solución de problemas del servidor de virtualización de aplicaciones
description: Información de solución de problemas del servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815190"
---
# <span data-ttu-id="f102a-103">Información de solución de problemas del servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f102a-103">Troubleshooting Information for the Application Virtualization Server</span></span>


<span data-ttu-id="f102a-104">En este tema se incluye información que puede usar para solucionar varios problemas en los servidores de virtualización de aplicaciones (App-V).</span><span class="sxs-lookup"><span data-stu-id="f102a-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Servers.</span></span>

## <span data-ttu-id="f102a-105">Mensaje de advertencia 25017 en el registro de instalación después de instalar el servidor</span><span class="sxs-lookup"><span data-stu-id="f102a-105">Warning Message 25017 in Setup Log After Installing the Server</span></span>


<span data-ttu-id="f102a-106">Es posible que encuentre el siguiente mensaje en el registro de configuración del servidor después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="f102a-106">You might find the following message in the server setup log after installation.</span></span>

*<span data-ttu-id="f102a-107">ADVERTENCIA 25017.</span><span class="sxs-lookup"><span data-stu-id="f102a-107">Warning 25017.</span></span> <span data-ttu-id="f102a-108">El programa de instalación no pudo crear el objeto de marcador de Active Directory para el servidor.</span><span class="sxs-lookup"><span data-stu-id="f102a-108">The installation Program could not create the Active Directory marker object for the server.</span></span> <span data-ttu-id="f102a-109">La cuenta que se usó para instalar no tenía los derechos suficientes para escribir en Active Directory o Active Directory no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="f102a-109">The account used to install did not have the sufficient rights to write to Active Directory or Active Directory was unavailable.</span></span>*

<span data-ttu-id="f102a-110">El instalador de la administración de App-V o de Streaming Server crea una entrada de punto de conexión de servicio bajo el objeto de equipo en servicios de dominio de Active Directory (ADDS) que corresponde al equipo en el que está instalado el servidor si la cuenta usada para ejecutar el instalador tiene los derechos apropiados.</span><span class="sxs-lookup"><span data-stu-id="f102a-110">The App-V Management or Streaming Server installer creates a Service Connection Point entry under the Computer object in Active Directory Domain Services (ADDS) that corresponds to the computer on which the server is installed if the account used to run the installer has the appropriate rights.</span></span> <span data-ttu-id="f102a-111">Si no crea esta entrada, no se producirá un error en la instalación y esto no debería afectar al funcionamiento del producto.</span><span class="sxs-lookup"><span data-stu-id="f102a-111">Failure to create this entry will not cause the install to fail and this should not otherwise affect the functioning of the product.</span></span> <span data-ttu-id="f102a-112">La causa probable de cualquier error es que la cuenta de usuario usada para ejecutar la instalación no tenía suficientes derechos para escribir en ADDS.</span><span class="sxs-lookup"><span data-stu-id="f102a-112">The likely cause of any failure is that the user account used to run the install did not have sufficient rights to write to ADDS.</span></span> <span data-ttu-id="f102a-113">Aunque el registro del servidor de App-V en ADDS es opcional, una de las ventajas de hacerlo permite a las herramientas de administración centralizadas ubicar el servidor de App-V con fines de inventario y administración.</span><span class="sxs-lookup"><span data-stu-id="f102a-113">Although registering the App-V server in ADDS is optional, one benefit of doing so enables centralized management tools to locate the App-V server for inventory and management purposes.</span></span>

## <span data-ttu-id="f102a-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f102a-114">Related topics</span></span>


[<span data-ttu-id="f102a-115">Servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f102a-115">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





