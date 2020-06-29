---
title: Administrar impresoras en un área de trabajo de MED-V
description: Administrar impresoras en un área de trabajo de MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826120"
---
# <span data-ttu-id="f2ae2-103">Administrar impresoras en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="f2ae2-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="f2ae2-104">En Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, la redirección de impresora proporciona a los usuarios finales una experiencia de impresión coherente entre la máquina virtual MED-V y el equipo host.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="f2ae2-105">Este tema proporciona información sobre cómo administrar la impresión en un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="f2ae2-106">Administración de impresoras en áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="f2ae2-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="f2ae2-107">En la mayoría de los casos, MED-V controla automáticamente el redireccionamiento de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="f2ae2-108">Después de que finalice la configuración por primera vez, MED-V identifica todas las impresoras de red instaladas en el host, recupera los drivers correspondientes del servidor de impresión de red y, si lo encuentra, instala los drivers relevantes en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="f2ae2-109">Una vez que se han encontrado e instalado todos los drivers, MED-V reinicia el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="f2ae2-110">Solo después de que se reinicie el área de trabajo de MED-V, las impresoras de host estarán presentes y disponibles en el invitado, generalmente en unos minutos.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="f2ae2-111">**Nota:**  Si las aplicaciones se ejecutan en el área de trabajo de MED-V, se solicita al usuario final que continúe o pospongala hasta más tarde.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="f2ae2-112">Si no se está ejecutando ninguna aplicación, el reinicio es automático y no se muestra al usuario final.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="f2ae2-113">Cada vez que se reinicie MED-V, se comprueba si hay instaladas nuevas impresoras en el host y, si las encuentra, se recuperan los drivers correspondientes del servidor de impresión de red y se instalan en el invitado.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="f2ae2-114">A continuación, MED-V reinicia el área de trabajo MED-V como la primera vez que se completó la configuración.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="f2ae2-115">**Importante**  Una vez que los drivers correspondientes estén instalados en el invitado, las impresoras solo estarán visibles en el invitado después de que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="f2ae2-116">Si en cualquier momento no se puede ubicar ni instalar un controlador, debe instalarlo manualmente en el invitado para que la impresora de red esté disponible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="f2ae2-117">La siguiente lista ofrece instrucciones adicionales:</span><span class="sxs-lookup"><span data-stu-id="f2ae2-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="f2ae2-118">**MED-V solo administra impresoras de red**.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="f2ae2-119">Los drivers de las impresoras instaladas de forma local en el host no se instalan automáticamente en el invitado.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="f2ae2-120">**MED-V solo instala drivers de impresora si se encuentran en el servidor de impresión**.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="f2ae2-121">Si no se encuentra, los drivers de impresora deben instalarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="f2ae2-122">**Las impresoras instaladas manualmente en el invitado no son accesibles para el host**.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="f2ae2-123">De forma predeterminada, MED-V solo admite el redireccionamiento de impresoras desde el invitado al host.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="f2ae2-124">**ADVERTENCIA**  Si una impresora se instala manualmente en el invitado y la misma impresora se instala posteriormente en el host, el resultado es que la impresora se instala dos veces en el invitado.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="f2ae2-125">Para evitar esta situación, una práctica recomendada de MED-V es administrar el redireccionamiento de la impresora de una manera: deshabilite la redirección e instale las impresoras manualmente en el invitado, o bien habilite el redireccionamiento y no instale las impresoras de forma manual en el invitado.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="f2ae2-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2ae2-126">Related topics</span></span>


[<span data-ttu-id="f2ae2-127">Administrar la configuración del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="f2ae2-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





