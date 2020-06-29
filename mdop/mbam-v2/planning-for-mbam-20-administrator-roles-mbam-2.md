---
title: Planificación de roles de administrador de MBAM 2.0
description: Planificación de roles de administrador de MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824891"
---
# <span data-ttu-id="09164-103">Planificación de roles de administrador de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="09164-103">Planning for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="09164-104">En este tema se enumeran y describen los roles de administrador disponibles en administración y supervisión de BitLocker de Microsoft (MBAM), así como las ubicaciones de servidor donde se crean los grupos locales.</span><span class="sxs-lookup"><span data-stu-id="09164-104">This topic lists and describes the available administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM) as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="09164-105">Roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="09164-105">MBAM Administrator Roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="09164-106">Administradores del sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="09164-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="09164-107">Los administradores de este rol tienen acceso a todas las características de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="09164-107">Administrators in this role have access to all Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="09164-108">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="09164-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="09164-109">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="09164-109">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="09164-110">Los administradores de este rol tienen acceso a las características de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="09164-110">Administrators in this role have access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="09164-111">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="09164-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-report-users"></a> **<span data-ttu-id="09164-112">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="09164-112">MBAM Report Users</span></span>**  
<span data-ttu-id="09164-113">Los administradores de este rol tienen acceso a los informes de cumplimiento y cumplimiento de la MBAM.</span><span class="sxs-lookup"><span data-stu-id="09164-113">Administrators in this role have access to the Compliance and Audit Reports from MBAM.</span></span> <span data-ttu-id="09164-114">El grupo local para este rol está instalado en el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="09164-114">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **<span data-ttu-id="09164-115">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="09164-115">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="09164-116">Los administradores de este rol han aumentado el acceso a las características de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="09164-116">Administrators in this role have increased access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="09164-117">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="09164-117">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="09164-118">Si un usuario es miembro de MBAM y usuarios del Departamento de soporte técnico avanzado, los permisos de usuario del servicio de asistencia al MBAM avanzado sobrescribirán los permisos de usuario de MBAM Helpdesk.</span><span class="sxs-lookup"><span data-stu-id="09164-118">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will override the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="09164-119">**Importante**  Para ver los informes, un usuario administrativo debe ser miembro del grupo de seguridad de **usuarios de informes de MBAM** en el servidor de administración y supervisión, la base de datos de cumplimiento y auditoría, y en el servidor que hospeda la característica informes de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="09164-119">**Important** To view reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports feature.</span></span> <span data-ttu-id="09164-120">Como práctica recomendada, cree un grupo de seguridad en los servicios de dominio de Active Directory con derechos en el grupo de seguridad local de **los usuarios de MBAM** en el servidor de supervisión y administración y en el servidor que hospeda los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="09164-120">As a best practice, create a security group in Active Directory Domain Services with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and the server that hosts the Compliance and Audit Reports.</span></span>

 

## <span data-ttu-id="09164-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09164-121">Related topics</span></span>


[<span data-ttu-id="09164-122">Preparación del entorno para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="09164-122">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





