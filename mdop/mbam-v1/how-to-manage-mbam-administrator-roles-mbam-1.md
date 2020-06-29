---
title: Cómo administrar los roles de administrador de MBAM
description: Cómo administrar los roles de administrador de MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812967"
---
# <span data-ttu-id="49342-103">Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="49342-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="49342-104">Una vez completada la configuración administración y supervisión de Microsoft BitLocker (MBAM) para todas las características del servidor, se debe conceder acceso a los usuarios administrativos a estas características de servidor.</span><span class="sxs-lookup"><span data-stu-id="49342-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="49342-105">Como práctica recomendada, los administradores que administrarán o usarán características de servidor de MBAM se deben asignar a grupos de seguridad de Active Directory y, a continuación, esos grupos deben agregarse al grupo local administrativo de MBAM adecuado.</span><span class="sxs-lookup"><span data-stu-id="49342-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="49342-106">Para administrar MBAM pertenencias a roles de administrador</span><span class="sxs-lookup"><span data-stu-id="49342-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="49342-107">Asignar usuarios administrativos a grupos de seguridad en servicios de ActiveDirectoryDomain.</span><span class="sxs-lookup"><span data-stu-id="49342-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="49342-108">Agregue los grupos de seguridad servicios de ActiveDirectoryDomain a los roles de MBAM grupos locales administrativos en el servidor administración y supervisión de Microsoft BitLocker para las características respectivas.</span><span class="sxs-lookup"><span data-stu-id="49342-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="49342-109">Los roles de usuario son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="49342-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="49342-110">**MBAM los administradores del sistema** tienen acceso a todas las características de supervisión y administración de Microsoft BitLocker en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="49342-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="49342-111">**Los usuarios de hardware de MBAM** tienen acceso a las características de compatibilidad de hardware en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="49342-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="49342-112">**MBAM los usuarios del Departamento de soporte** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración de MBAM, pero deben rellenar todos los campos cuando usen ambas opciones.</span><span class="sxs-lookup"><span data-stu-id="49342-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="49342-113">**Los usuarios de informes de MBAM** tienen acceso a los informes de cumplimiento y cumplimiento en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="49342-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="49342-114">**MBAM uso avanzado de los departamentos de soporte técnico** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="49342-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="49342-115">No es necesario que estos usuarios rellenen todos los campos cuando usan una de las dos opciones.</span><span class="sxs-lookup"><span data-stu-id="49342-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="49342-116">Para obtener más información acerca de los roles de administración y supervisión de Microsoft BitLocker, consulte [roles de planeación de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="49342-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="49342-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49342-117">Related topics</span></span>


[<span data-ttu-id="49342-118">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="49342-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





