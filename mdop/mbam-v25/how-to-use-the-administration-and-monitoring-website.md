---
title: Cómo usar el sitio web de administración y supervisión
description: Cómo usar el sitio web de administración y supervisión
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813046"
---
# <span data-ttu-id="756e2-103">Cómo usar el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="756e2-103">How to Use the Administration and Monitoring Website</span></span>


<span data-ttu-id="756e2-104">El sitio web de administración y supervisión, también conocido como soporte técnico, es una interfaz administrativa para el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="756e2-104">The Administration and Monitoring Website, also referred to as the Help Desk, is an administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="756e2-105">Use el sitio web para revisar los informes, recuperar las unidades de los usuarios finales y administrar los TPMs de los usuarios finales, tal y como se describe en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="756e2-105">Use the website to review reports, recover end users’ drives, and manage end users’ TPMs, as described in the following sections.</span></span>

<span data-ttu-id="756e2-106">**Nota:**  Si está usando MBAM en la topología independiente, verá todos los informes del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="756e2-106">**Note** If you are using MBAM in the Stand-alone topology, you view all reports from the Administration and Monitoring Website.</span></span> <span data-ttu-id="756e2-107">Si está usando la topología de integración de Configuration Manager, verá todos los informes en Configuration Manager, excepto el informe de auditoría de recuperación, que se sigue visualizando desde el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="756e2-107">If you are using the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit report, which you continue to view from the Administration and Monitoring Website.</span></span> <span data-ttu-id="756e2-108">Para obtener más información sobre los informes, consulte [supervisión e informes de compatibilidad con BitLocker con MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="756e2-108">For more information about reports, see [Monitoring and Reporting BitLocker Compliance with MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span></span>

 

## <span data-ttu-id="756e2-109">Roles necesarios para usar el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="756e2-109">Required roles for using the Administration and Monitoring Website</span></span>


<span data-ttu-id="756e2-110">Para acceder a áreas específicas del sitio web de administración y supervisión, debe tener uno de los siguientes roles, que son grupos que ha creado en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="756e2-110">To access specific areas of the Administration and Monitoring Website, you must have one of the following roles, which are groups that you create in Active Directory.</span></span> <span data-ttu-id="756e2-111">Puede usar cualquier nombre para estos grupos.</span><span class="sxs-lookup"><span data-stu-id="756e2-111">You can use any name for these groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="756e2-112">Cuenta</span><span class="sxs-lookup"><span data-stu-id="756e2-112">Account</span></span></th>
<th align="left"><span data-ttu-id="756e2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="756e2-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="756e2-114">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="756e2-114">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-115">Proporciona acceso a todas las áreas del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="756e2-115">Provides access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="756e2-116">Los usuarios que tienen este rol solo tienen que escribir la clave de recuperación, y no el dominio del usuario final y el nombre de usuario, al ayudar a los usuarios finales a recuperar sus unidades.</span><span class="sxs-lookup"><span data-stu-id="756e2-116">Users who have this role enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="756e2-117">Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo usuarios del servicio de asistencia avanzada anularán los permisos del grupo MBAM de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="756e2-117">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="756e2-118">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="756e2-118">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-119">Proporciona acceso a las áreas administrar TPM y recuperación de unidades del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="756e2-119">Provides access to the Manage TPM and Drive Recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="756e2-120">Las personas que tienen este rol deben rellenar todos los campos, incluidos el dominio y el nombre de la cuenta del usuario final, cuando usan cualquiera de los dos áreas.</span><span class="sxs-lookup"><span data-stu-id="756e2-120">Individuals who have this role must fill in all fields, including the end-user’s domain and account name, when they use either area.</span></span></p>
<p><span data-ttu-id="756e2-121">Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo usuarios del servicio de asistencia avanzada anularán los permisos del grupo MBAM de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="756e2-121">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="756e2-122">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="756e2-122">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-123">Proporciona acceso a los informes en el <strong> </strong> área informes del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="756e2-123">Provides access to the reports in the <strong>Reports</strong> area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="756e2-124">Tareas que puede realizar en el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="756e2-124">Tasks you can perform on the Administration and Monitoring Website</span></span>


<span data-ttu-id="756e2-125">En la tabla siguiente se resumen las tareas que puede realizar en el sitio web de administración y supervisión, y se proporcionan vínculos a más información sobre cada tarea.</span><span class="sxs-lookup"><span data-stu-id="756e2-125">The following table summarizes the tasks you can perform on the Administration and Monitoring Website and provides links to more information about each task.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="756e2-126">Tarea</span><span class="sxs-lookup"><span data-stu-id="756e2-126">Task</span></span></th>
<th align="left"><span data-ttu-id="756e2-127">Área del sitio web donde se accede a la tarea</span><span class="sxs-lookup"><span data-stu-id="756e2-127">Area of the Website where you access the task</span></span></th>
<th align="left"><span data-ttu-id="756e2-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="756e2-128">Description</span></span></th>
<th align="left"><span data-ttu-id="756e2-129">Para más información</span><span class="sxs-lookup"><span data-stu-id="756e2-129">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="756e2-130">Ver informes</span><span class="sxs-lookup"><span data-stu-id="756e2-130">View reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-131">Informes</span><span class="sxs-lookup"><span data-stu-id="756e2-131">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-132">Le permite ejecutar informes para supervisar el uso de BitLocker, el cumplimiento y la actividad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="756e2-132">Enables you to run reports to monitor BitLocker usage, compliance, and key recovery activity.</span></span> <span data-ttu-id="756e2-133">Los informes proporcionan datos sobre el cumplimiento de la empresa, los equipos individuales y los que solicitaron claves de recuperación o el paquete de OwnerAuth de TPM para un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="756e2-133">Reports provide data about enterprise compliance, individual computers, and who requested recovery keys or the TPM OwnerAuth package for a specific computer.</span></span></p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)"><span data-ttu-id="756e2-134">Visualización de informes MBAM 2.5 para topología independiente</span><span class="sxs-lookup"><span data-stu-id="756e2-134">Viewing MBAM 2.5 Reports for the Stand-alone Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="756e2-135">Determinar el estado de cifrado de BitLocker de equipos perdidos o robados</span><span class="sxs-lookup"><span data-stu-id="756e2-135">Determine the BitLocker encryption status of lost or stolen computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-136">Informes</span><span class="sxs-lookup"><span data-stu-id="756e2-136">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-137">Determine si un volumen se cifró si el equipo se ha perdido o ha sido robado.</span><span class="sxs-lookup"><span data-stu-id="756e2-137">Determine if a volume was encrypted if the computer is lost or stolen.</span></span></p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)"><span data-ttu-id="756e2-138">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="756e2-138">How to Determine BitLocker Encryption State of Lost Computers</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="756e2-139">Recuperar unidades perdidas</span><span class="sxs-lookup"><span data-stu-id="756e2-139">Recover lost drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-140">Recuperación de unidades</span><span class="sxs-lookup"><span data-stu-id="756e2-140">Drive Recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-141">Recuperar unidades que son:</span><span class="sxs-lookup"><span data-stu-id="756e2-141">Recover drives that are:</span></span></p>
<ul>
<li><p><span data-ttu-id="756e2-142">En modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="756e2-142">In recovery mode</span></span></p></li>
<li><p><span data-ttu-id="756e2-143">Se han movido</span><span class="sxs-lookup"><span data-stu-id="756e2-143">Have been moved</span></span></p></li>
<li><p><span data-ttu-id="756e2-144">Están dañados</span><span class="sxs-lookup"><span data-stu-id="756e2-144">Are corrupted</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)"><span data-ttu-id="756e2-145">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="756e2-145">How to Recover a Drive in Recovery Mode</span></span></a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)"><span data-ttu-id="756e2-146">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="756e2-146">How to Recover a Moved Drive</span></span></a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)"><span data-ttu-id="756e2-147">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="756e2-147">How to Recover a Corrupted Drive</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="756e2-148">Restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="756e2-148">Reset a TPM lockout</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-149">Administrar TPM</span><span class="sxs-lookup"><span data-stu-id="756e2-149">Manage TPM</span></span></p></td>
<td align="left"><p><span data-ttu-id="756e2-150">Proporciona acceso a datos de TPM recopilados por el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="756e2-150">Provides access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="756e2-151">En un bloqueo de TPM, use el sitio web de administración y supervisión para recuperar el archivo de contraseñas necesario para desbloquear el TPM.</span><span class="sxs-lookup"><span data-stu-id="756e2-151">In a TPM lockout, use the Administration and Monitoring Website to retrieve the necessary password file to unlock the TPM.</span></span></p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)"><span data-ttu-id="756e2-152">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="756e2-152">How to Reset a TPM Lockout</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="756e2-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="756e2-153">Related topics</span></span>


[<span data-ttu-id="756e2-154">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="756e2-154">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="756e2-155">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="756e2-155">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="756e2-156">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="756e2-156">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="756e2-157">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="756e2-157">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





