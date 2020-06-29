---
title: Lista de comprobación administrar el servidor y el archivo de AGPM
description: Lista de comprobación administrar el servidor y el archivo de AGPM
author: dansimp
ms.assetid: 0b2eb536-c3cc-462f-a42f-27a53f57bc55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f872a476a4a8ddd93546778c6278c175ec715850
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819151"
---
# <span data-ttu-id="085b2-103">Lista de comprobación: administrar el servidor y el archivo AGPM</span><span class="sxs-lookup"><span data-stu-id="085b2-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="085b2-104">En la administración de directivas de grupo (AGPM) avanzada, el servicio AGPM y el archivo son administrados por administradores de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="085b2-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="085b2-105">Las siguientes son tareas típicas para un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="085b2-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="085b2-106">Tarea frecuente</span><span class="sxs-lookup"><span data-stu-id="085b2-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="085b2-107">Referencia</span><span class="sxs-lookup"><span data-stu-id="085b2-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="085b2-108">Delegue el acceso a objetos de directiva de grupo (GPO) en el archivo.</span><span class="sxs-lookup"><span data-stu-id="085b2-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm30ops.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm30ops.md)"><span data-ttu-id="085b2-109">Delegar acceso a nivel de dominio al archivo</span><span class="sxs-lookup"><span data-stu-id="085b2-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md)"><span data-ttu-id="085b2-110">Delegar acceso a un GPO individual en el archivo</span><span class="sxs-lookup"><span data-stu-id="085b2-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="085b2-111">Haga una copia de seguridad del archivo para habilitar la recuperación ante desastres.</span><span class="sxs-lookup"><span data-stu-id="085b2-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive.md" data-raw-source="[Back Up the Archive](back-up-the-archive.md)"><span data-ttu-id="085b2-112">Copia de seguridad del archivo</span><span class="sxs-lookup"><span data-stu-id="085b2-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="085b2-113">Tarea poco frecuente</span><span class="sxs-lookup"><span data-stu-id="085b2-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="085b2-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="085b2-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="085b2-115">Restaure el archivo desde una copia de seguridad para recuperarlo de un desastre.</span><span class="sxs-lookup"><span data-stu-id="085b2-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup.md)"><span data-ttu-id="085b2-116">Restaurar el archivo desde una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="085b2-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="085b2-117">Mueva el servicio AGPM, el archivo o ambos a otro servidor.</span><span class="sxs-lookup"><span data-stu-id="085b2-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md)"><span data-ttu-id="085b2-118">Mover el servidor AGPM y el archivo</span><span class="sxs-lookup"><span data-stu-id="085b2-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="085b2-119">Cambie la ruta de acceso al archivo, la cuenta del servicio AGPM o el puerto en el que escucha el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="085b2-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm30ops.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md)"><span data-ttu-id="085b2-120">Modificar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="085b2-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="085b2-121">Solucione problemas comunes con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="085b2-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-advanced-group-policy-management-agpm30ops.md" data-raw-source="[Troubleshooting Advanced Group Policy Management](troubleshooting-advanced-group-policy-management-agpm30ops.md)"><span data-ttu-id="085b2-122">Solución de problemas de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="085b2-122">Troubleshooting Advanced Group Policy Management</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm30ops.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm30ops.md)"><span data-ttu-id="085b2-123">Configurar el registro y el seguimiento</span><span class="sxs-lookup"><span data-stu-id="085b2-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="085b2-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="085b2-124">Additional references</span></span>

-   [<span data-ttu-id="085b2-125">Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0</span><span class="sxs-lookup"><span data-stu-id="085b2-125">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





