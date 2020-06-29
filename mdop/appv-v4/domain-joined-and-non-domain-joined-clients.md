---
title: Clientes unidos a un dominio y no unidos a un dominio
description: Clientes unidos a un dominio y no unidos a un dominio
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821631"
---
# <span data-ttu-id="369b6-103">Clientes unidos a un dominio y no unidos a un dominio</span><span class="sxs-lookup"><span data-stu-id="369b6-103">Domain-Joined and Non-Domain-Joined Clients</span></span>


<span data-ttu-id="369b6-104">El cliente de escritorio de App-V puede configurarse para permitir la conexión a una red, independientemente de si el cliente está unido a un dominio o no.</span><span class="sxs-lookup"><span data-stu-id="369b6-104">The App-V Desktop Client can be configured to allow connection to a network regardless of whether the client is domain joined or non-domain joined.</span></span>

## <span data-ttu-id="369b6-105">Clientes Unidos a un dominio</span><span class="sxs-lookup"><span data-stu-id="369b6-105">Domain-Joined Clients</span></span>


<span data-ttu-id="369b6-106">Los clientes Unidos a un dominio, pero fuera de la red interna, pueden comunicarse con la infraestructura de App-V mediante una conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="369b6-106">Clients that are domain joined, but outside the internal network, can communicate with the App-V infrastructure by using a VPN connection.</span></span> <span data-ttu-id="369b6-107">Cuando desee proporcionar a los usuarios la capacidad de abandonar la red interna pero seguir comunicándose en una infraestructura de App-V, su entorno requiere muy poca configuración.</span><span class="sxs-lookup"><span data-stu-id="369b6-107">When you want to provide users the ability to leave the internal network but still communicate in an App-V infrastructure, your environment requires very little setup.</span></span> <span data-ttu-id="369b6-108">Como los usuarios ya forman parte del dominio, simplemente debe asegurarse de que se admitan las credenciales almacenadas en caché en el cliente.</span><span class="sxs-lookup"><span data-stu-id="369b6-108">Because the users are already part of the domain, you simply need to ensure that Cached Credentials are supported on the client.</span></span> <span data-ttu-id="369b6-109">Esta es la configuración predeterminada y los cambios realizados en esta configuración se pueden realizar desde directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="369b6-109">This is the default configuration, and any changes to this setting can be accomplished from Group Policies.</span></span>

<span data-ttu-id="369b6-110">Tal como se mencionó en la guía de procedimientos recomendados de seguridad de App-V, el usuario intentará enviar su vale de usuario a la infraestructura de App-V para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="369b6-110">As mentioned in the App-V Security Best Practices Guide, the user will attempt to send their user ticket to the App-V infrastructure for authentication.</span></span> <span data-ttu-id="369b6-111">Si el vale ha expirado, volverá a usar NTLM y las credenciales almacenadas en caché en el equipo.</span><span class="sxs-lookup"><span data-stu-id="369b6-111">If the ticket is expired, it will revert to using NTLM and the cached credentials on the computer.</span></span> <span data-ttu-id="369b6-112">Para permitir el uso de roaming, los administradores deben asegurarse de que el servidor de publicación al que se tiene acceso internamente está disponible en el mismo nombre de forma externa para que los nombres se resuelvan correctamente.</span><span class="sxs-lookup"><span data-stu-id="369b6-112">To allow roaming, administrators must ensure that the publishing server being accessed internally is available at the same name externally for the names to resolve properly.</span></span>

## <span data-ttu-id="369b6-113">Clientes no Unidos a un dominio</span><span class="sxs-lookup"><span data-stu-id="369b6-113">Non-Domain-Joined Clients</span></span>


<span data-ttu-id="369b6-114">Los clientes que no tienen un dominio Unido pero deben comunicarse en la infraestructura de App-V deben estar configurados para garantizar que la autenticación de la infraestructura de App-V se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="369b6-114">Clients that are non-domain joined but need to communicate in the App-V infrastructure must be configured to ensure that authentication to the App-V infrastructure is successful.</span></span> <span data-ttu-id="369b6-115">El cliente de escritorio de App-V no permite solicitar el proceso de actualización de publicación, por lo que el cliente debe estar configurado para presentar las credenciales apropiadas al servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="369b6-115">The App-V Desktop Client does not permit prompting for the publishing refresh process, so the client must be configured to present the proper credentials to the App-V Management Server.</span></span>

<span data-ttu-id="369b6-116">El servidor de publicación, que está configurado para la actualización de publicaciones desde el cliente que no está unido a un dominio, requiere que el nombre externo en el que se encuentra configurado el acceso de los clientes sea el nombre común o un nombre alternativo de asunto (SAN) en el certificado del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="369b6-116">The publishing server, which is configured for publishing refresh from the non-domain joined client, requires that the external name that clients access is configured as the common name or a subject alternate name (SAN) on the publishing server’s certificate.</span></span>

## <span data-ttu-id="369b6-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="369b6-117">Related topics</span></span>


[<span data-ttu-id="369b6-118">Cómo asignar las credenciales correctas para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="369b6-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

[<span data-ttu-id="369b6-119">Cómo asignar las credenciales correctas para Windows XP</span><span class="sxs-lookup"><span data-stu-id="369b6-119">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





