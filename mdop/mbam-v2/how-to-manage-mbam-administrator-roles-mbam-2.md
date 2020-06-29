---
title: Cómo administrar los roles de administrador de MBAM
description: Cómo administrar los roles de administrador de MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825120"
---
# <span data-ttu-id="92061-103">Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="92061-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="92061-104">Una vez completada la configuración administración y supervisión de Microsoft BitLocker (MBAM) para todas las características del servidor, los usuarios administrativos tendrán que tener permiso de acceso.</span><span class="sxs-lookup"><span data-stu-id="92061-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users will have to be granted access to them.</span></span> <span data-ttu-id="92061-105">Como práctica recomendada, los administradores que administrarán o usarán las características de servidor de supervisión y administración de Microsoft BitLocker deben asignarse a grupos de seguridad de servicios de dominio y, después, esos grupos deben agregarse al grupo local administrativo de MBAM correspondiente.</span><span class="sxs-lookup"><span data-stu-id="92061-105">As a best practice, administrators who will manage or use Microsoft BitLocker Administration and Monitoring Server features should be assigned to Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="92061-106">Para administrar MBAM pertenencias a roles de administrador</span><span class="sxs-lookup"><span data-stu-id="92061-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="92061-107">Asignar usuarios administrativos a grupos de seguridad en servicios de dominio de ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="92061-107">Assign administrative users to security groups in ActiveDirectory Domain Services.</span></span>

2.  <span data-ttu-id="92061-108">Agregue grupos de seguridad de ActiveDirectory a los roles de los grupos locales administrativos de MBAM en el servidor de MBAM para las características respectivas.</span><span class="sxs-lookup"><span data-stu-id="92061-108">Add ActiveDirectory security groups to the roles for MBAM administrative local groups on the MBAM server for the respective features.</span></span>

    -   <span data-ttu-id="92061-109">**MBAM los administradores del sistema** tienen acceso a todas las características de MBAM en el sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="92061-109">**MBAM System Administrators** have access to all MBAM features in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="92061-110">**Los usuarios del Departamento de soporte técnico de MBAM** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración y supervisión de MBAM, pero deben rellenar todos los campos cuando usen ambas opciones.</span><span class="sxs-lookup"><span data-stu-id="92061-110">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="92061-111">**Los usuarios de informes de MBAM** tienen acceso a los informes de cumplimiento y cumplimiento en el sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="92061-111">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="92061-112">**Los usuarios avanzados de MBAM** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración y supervisión de MBAM, pero no necesitan rellenar todos los campos cuando usan ambas opciones.</span><span class="sxs-lookup"><span data-stu-id="92061-112">**MBAM Advanced Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="92061-113">Para obtener más información acerca de los roles de administración y supervisión de Microsoft BitLocker, consulte [roles de planeación de MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="92061-113">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="92061-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92061-114">Related topics</span></span>


[<span data-ttu-id="92061-115">Administración de funciones de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="92061-115">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





