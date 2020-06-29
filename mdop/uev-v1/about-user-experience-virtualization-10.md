---
title: Acerca de la virtualización de la experiencia del usuario 1.0
description: Acerca de la virtualización de la experiencia del usuario 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822711"
---
# <span data-ttu-id="634a0-103">Acerca de la virtualización de la experiencia del usuario 1.0</span><span class="sxs-lookup"><span data-stu-id="634a0-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="634a0-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) supervisa los cambios realizados por los usuarios en la configuración de la aplicación y en la configuración del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="634a0-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="634a0-105">La configuración de usuario se captura y centraliza en una ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="634a0-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="634a0-106">Esta configuración se puede aplicar a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="634a0-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="634a0-107">La virtualización de la experiencia del usuario usa plantillas de ubicación de configuración para especificar las aplicaciones y la configuración de Windows de los equipos de los usuarios que se supervisan y se centralizan.</span><span class="sxs-lookup"><span data-stu-id="634a0-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="634a0-108">La plantilla de ubicación de configuración es un archivo XML que especifica qué ubicaciones de archivos y registros se asocian con cada configuración de aplicación o sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="634a0-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="634a0-109">La plantilla no contiene valores para la configuración; contiene solo las ubicaciones de la configuración que se va a supervisar.</span><span class="sxs-lookup"><span data-stu-id="634a0-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="634a0-110">UE-V supervisa la configuración de la aplicación y la configuración de Windows cuando los usuarios trabajan en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="634a0-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="634a0-111">Los valores de la configuración de la aplicación se almacenan en el servidor de almacenamiento de configuración cuando el usuario cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="634a0-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="634a0-112">Los valores de configuración de Windows se almacenan cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando se desconecta de forma remota desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="634a0-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="634a0-113">Un administrador puede crear una plantilla de ubicación de configuración de UE-V para especificar la configuración de la aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="634a0-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="634a0-114">UE-V incluye un conjunto de plantillas de ubicación de configuración para algunas aplicaciones de Microsoft y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="634a0-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="634a0-115">Para obtener una lista de las aplicaciones y configuraciones predeterminadas en UE-V, consulte [planear las aplicaciones que se van a sincronizar con UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="634a0-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="634a0-116">Notas de la versión de UEV 1,0</span><span class="sxs-lookup"><span data-stu-id="634a0-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="634a0-117">Para obtener más información y para obtener noticias de última hora que no se han incorporado en la documentación, consulte notas de la [versión 1,0 de Microsoft User Experience Virtualization (UE-V)](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="634a0-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="634a0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="634a0-118">Related topics</span></span>


[<span data-ttu-id="634a0-119">Introducción a la virtualización de la experiencia del usuario 1.0</span><span class="sxs-lookup"><span data-stu-id="634a0-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="634a0-120">Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="634a0-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="634a0-121">Arquitectura de alto nivel para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="634a0-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





