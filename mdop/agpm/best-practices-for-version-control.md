---
title: Procedimientos recomendados para el control de versiones
description: Procedimientos recomendados para el control de versiones
author: dansimp
ms.assetid: 89067f6a-f7ea-4dad-999d-118284cf6c5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ed91408faeb8968175976382f9dd97d45becddb5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819201"
---
# <span data-ttu-id="8214f-103">Procedimientos recomendados para el control de versiones</span><span class="sxs-lookup"><span data-stu-id="8214f-103">Best Practices for Version Control</span></span>


<span data-ttu-id="8214f-104">Administración avanzada de directivas de grupo (AGPM) de Microsoft proporciona control de versiones para objetos de directiva de grupo (GPO) de forma similar a Microsoft Visual SourceSafe® ofrece control de versiones para el código fuente.</span><span class="sxs-lookup"><span data-stu-id="8214f-104">Microsoft Advanced Group Policy Management (AGPM) provides version control for Group Policy Objects (GPOs) much like Microsoft Visual SourceSafe® provides version control for source code.</span></span> <span data-ttu-id="8214f-105">Los programadores pueden usar Visual SourceSafe para administrar varias versiones de cada archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="8214f-105">Developers can use Visual SourceSafe to manage multiple versions of each source file.</span></span> <span data-ttu-id="8214f-106">Los administradores de directivas de grupo pueden usar AGPM para hacer lo mismo para los GPO.</span><span class="sxs-lookup"><span data-stu-id="8214f-106">Group Policy administrators can use AGPM to do the same for GPOs.</span></span> <span data-ttu-id="8214f-107">Al usar AGPM, los administradores de directivas de grupo deben tener en cuenta los procedimientos recomendados que se aplican a cualquier sistema de control de versiones:</span><span class="sxs-lookup"><span data-stu-id="8214f-107">When you use AGPM, Group Policy administrators should be aware of best practices that apply to any version control system:</span></span>

-   <span data-ttu-id="8214f-108">**Fecha y hora:** AGPM sella cada versión de un GPO con la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="8214f-108">**Date and time:** AGPM stamps each version of a GPO with the date and time.</span></span> <span data-ttu-id="8214f-109">Para asegurarse de que el historial sea preciso, sobre todo cuando se modifican los GPO en más de un equipo, asegúrese de que cada equipo sincroniza su reloj con una fuente de tiempo autorizada.</span><span class="sxs-lookup"><span data-stu-id="8214f-109">To ensure that history is accurate, especially when you edit GPOs on more than one computer, make sure that each computer synchronizes its clock with one authoritative time source.</span></span>

-   <span data-ttu-id="8214f-110">**Proteja los GPO cuando haya terminado de modificarlos:** Es común que los editores desprotejan los GPO y se olviden de volver a protegerlos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="8214f-110">**Check in GPOs when you are finished editing them:** It is common for Editors to check out GPOs and forget to check them back into the archive.</span></span> <span data-ttu-id="8214f-111">Sin embargo, esto puede impedir que otros administradores de directivas de grupo cambien el GPO.</span><span class="sxs-lookup"><span data-stu-id="8214f-111">However, this can prevent other Group Policy administrators from changing the GPO.</span></span> <span data-ttu-id="8214f-112">Siempre vuelve a comprobar inmediatamente los objetos de directiva de grupo en AGPM cuando haya terminado de modificarlos.</span><span class="sxs-lookup"><span data-stu-id="8214f-112">Always check GPOs back in to AGPM immediately when you are finished editing.</span></span>

-   <span data-ttu-id="8214f-113">**Guarde los cambios con frecuencia:** Cuando edite un GPO, guarde los cambios con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="8214f-113">**Save changes frequently:** When you edit a GPO, save changes frequently.</span></span> <span data-ttu-id="8214f-114">La mayoría de los editores desprotegen un GPO, hacen muchos cambios y, a continuación, comprueban el GPO en el archivo.</span><span class="sxs-lookup"><span data-stu-id="8214f-114">Most Editors check out a GPO, make many changes, and then check the GPO into the archive.</span></span> <span data-ttu-id="8214f-115">En su lugar, compruebe el GPO en el archivo de forma periódica y luego vuelva a desprotegerlo.</span><span class="sxs-lookup"><span data-stu-id="8214f-115">Instead, check the GPO into the archive regularly, and then check it out again.</span></span> <span data-ttu-id="8214f-116">El detalle puede ser tan pequeño como comprobar el GPO después de cambiar cada opción (no recomendado) o de proteger el GPO después de crear grupos de cambios relacionados.</span><span class="sxs-lookup"><span data-stu-id="8214f-116">The detail can be as small as checking in the GPO after you change every setting (not recommended) or checking in the GPO after you make groups of related changes.</span></span> <span data-ttu-id="8214f-117">El resultado es un historial mejor documentado para cada objeto de directiva de grupo que puede ayudarle a solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="8214f-117">The result is a better-documented history for each GPO that can help when troubleshooting issues.</span></span>

-   <span data-ttu-id="8214f-118">**Implemente GPO con frecuencia:** No permita que los GPO nuevos y editados que aún no se hayan implementado se acumulen en números grandes en el archivo.</span><span class="sxs-lookup"><span data-stu-id="8214f-118">**Deploy GPOs frequently:** Do not let new and edited GPOs that have not yet been deployed accumulate in large numbers in the archive.</span></span> <span data-ttu-id="8214f-119">En su lugar, implemente GPO nuevos y editados lo antes posible para que tengan un efecto mínimo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="8214f-119">Instead, deploy new and edited GPOs as soon as possible so that they have a minimum effect on the production environment.</span></span> <span data-ttu-id="8214f-120">Implementar muchos GPO nuevos y editados a la vez puede poner en peligro el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="8214f-120">Deploying many new and edited GPOs at one time can jeopardize the production environment.</span></span>

-   <span data-ttu-id="8214f-121">**Documente el propósito de los cambios cuando proteja los GPO:** Cualquier revisor puede comparar versiones de un objeto de directiva de grupo para ver los cambios específicos entre los dos.</span><span class="sxs-lookup"><span data-stu-id="8214f-121">**Document the purpose of changes when you check in GPOs:** Any Reviewer can compare versions of a GPO to see specific changes between the two.</span></span> <span data-ttu-id="8214f-122">La documentación de esos cambios específicos no suma ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8214f-122">Documenting those specific changes adds no value.</span></span> <span data-ttu-id="8214f-123">En su lugar, documente la intención y el propósito de un cambio en lugar de documentar lo que los revisores pueden ver consultando los informes de diferencias.</span><span class="sxs-lookup"><span data-stu-id="8214f-123">Instead, document the intent and purpose of a change instead of documenting what Reviewers can see by viewing difference reports.</span></span> <span data-ttu-id="8214f-124">Comentarios de versión debe agregar valor al informe de comparación y ayudar a un revisor a comprender por qué el editor cambió el GPO.</span><span class="sxs-lookup"><span data-stu-id="8214f-124">Version comments should add value to the comparison report and help a Reviewer understand why the Editor changed the GPO.</span></span>

-   <span data-ttu-id="8214f-125">**Probar los GPO en un laboratorio antes de implementarlo:** La implementación de GPO en el entorno de producción sin antes probarlos es arriesgada.</span><span class="sxs-lookup"><span data-stu-id="8214f-125">**Test GPOs in a lab before you deploy:** Deploying GPOs to the production environment without first testing them is risky.</span></span> <span data-ttu-id="8214f-126">En su lugar, pruebe los GPO en un entorno de laboratorio vinculándolos a una unidad organizativa que contiene equipos de prueba y usuarios y, a continuación, verificando que funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="8214f-126">Instead, test GPOs in a lab environment by linking them to an organizational unit that contains test computers and users, and then verifying that they function correctly.</span></span> <span data-ttu-id="8214f-127">Después de comprobar cada GPO en el laboratorio, implemente el GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="8214f-127">After verifying each GPO in the lab, deploy the GPO to the production environment.</span></span>

### <span data-ttu-id="8214f-128">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="8214f-128">Additional references</span></span>

-   [<span data-ttu-id="8214f-129">Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0</span><span class="sxs-lookup"><span data-stu-id="8214f-129">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





