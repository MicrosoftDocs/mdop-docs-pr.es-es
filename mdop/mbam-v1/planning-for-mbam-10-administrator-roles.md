---
title: Planificación de roles de administrador de MBAM 1.0
description: Planificación de roles de administrador de MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825890"
---
# <span data-ttu-id="10d76-103">Planificación de roles de administrador de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="10d76-103">Planning for MBAM 1.0 Administrator Roles</span></span>


<span data-ttu-id="10d76-104">En este tema se incluyen y describen los roles de administrador que están disponibles en administración y supervisión de Microsoft BitLocker (MBAM), así como las ubicaciones de servidor donde se crean los grupos locales.</span><span class="sxs-lookup"><span data-stu-id="10d76-104">This topic includes and describes the administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM), as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="10d76-105">Roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="10d76-105">MBAM Administrator roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="10d76-106">Administradores del sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="10d76-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="10d76-107">Los administradores de este rol tienen acceso a todas las características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="10d76-107">Administrators in this role have access to all MBAM features.</span></span> <span data-ttu-id="10d76-108">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="10d76-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-hardware-users"></a> **<span data-ttu-id="10d76-109">Usuarios de hardware de MBAM</span><span class="sxs-lookup"><span data-stu-id="10d76-109">MBAM Hardware Users</span></span>**  
<span data-ttu-id="10d76-110">Los administradores de este rol tienen acceso a las características de capacidad de hardware de MBAM.</span><span class="sxs-lookup"><span data-stu-id="10d76-110">Administrators in this role have access to the Hardware Capability features from MBAM.</span></span> <span data-ttu-id="10d76-111">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="10d76-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="10d76-112">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="10d76-112">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="10d76-113">Los administradores de este rol tienen acceso a las características del Departamento de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="10d76-113">Administrators in this role have access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="10d76-114">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="10d76-114">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam--report-users"></a> **<span data-ttu-id="10d76-115">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="10d76-115">MBAM Report Users</span></span>**  
<span data-ttu-id="10d76-116">Los administradores de este rol tienen acceso a la característica informes de cumplimiento y auditoría de MBAM.</span><span class="sxs-lookup"><span data-stu-id="10d76-116">Administrators in this role have access to the Compliance and Audit Reports feature from MBAM.</span></span> <span data-ttu-id="10d76-117">El grupo local para este rol está instalado en el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="10d76-117">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **<span data-ttu-id="10d76-118">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="10d76-118">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="10d76-119">Los administradores de este rol han aumentado el acceso a las características del Departamento de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="10d76-119">Administrators in this role have increased access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="10d76-120">El grupo local para este rol está instalado en el servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="10d76-120">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="10d76-121">Si un usuario es miembro de MBAM y usuarios del Departamento de soporte técnico avanzado, los permisos de los usuarios avanzados de soporte técnico de MBAM se sobrescribirán a los permisos de usuario de MBAM Helpdesk.</span><span class="sxs-lookup"><span data-stu-id="10d76-121">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will overwrite the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="10d76-122">**Importante**  Para ver los informes, un usuario administrativo debe ser miembro del grupo de seguridad de **usuarios de informes de MBAM** en el servidor de administración y supervisión, la base de datos de cumplimiento y auditoría, y en el servidor que hospeda la característica de cumplimiento e informes.</span><span class="sxs-lookup"><span data-stu-id="10d76-122">**Important** To view the reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Reports feature.</span></span> <span data-ttu-id="10d76-123">Como práctica recomendada, cree un grupo de seguridad en Active Directory con derechos en el grupo de seguridad local de **usuarios de MBAM** en el servidor de administración y supervisión, y en el servidor que hospeda el cumplimiento y los informes.</span><span class="sxs-lookup"><span data-stu-id="10d76-123">As a best practice, create a security group in Active Directory with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and on the server that hosts the Compliance and Reports.</span></span>

 

## <span data-ttu-id="10d76-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10d76-124">Related topics</span></span>


[<span data-ttu-id="10d76-125">Preparación del entorno para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="10d76-125">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)

 

 





