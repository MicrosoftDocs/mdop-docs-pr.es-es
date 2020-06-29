---
title: Alta disponibilidad de MBAM 2.0
description: Alta disponibilidad de MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824730"
---
# <span data-ttu-id="6ab1f-103">Alta disponibilidad de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6ab1f-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="6ab1f-104">En este tema se proporciona información básica sobre una instalación de alta disponibilidad de administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="6ab1f-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="6ab1f-105">Los escenarios de alta disponibilidad no son totalmente compatibles con esta versión de MBAM, por lo que no se describen aquí.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="6ab1f-106">Se recomienda buscar en blogs y foros relacionados, en los que los usuarios describen cómo han configurado correctamente una alta disponibilidad para MBAM en sus entornos.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="6ab1f-107">Escenarios de alta disponibilidad para MBAM</span><span class="sxs-lookup"><span data-stu-id="6ab1f-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="6ab1f-108">La administración y supervisión de Microsoft BitLocker está diseñada para ser tolerante a errores.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="6ab1f-109">Si un servidor no está disponible, los usuarios no se verán afectados de forma negativa.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="6ab1f-110">Por ejemplo, si el agente de MBAM no se puede conectar al servidor Web de MBAM, no se le pedirá que lo solicite.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="6ab1f-111">Cuando planee su instalación de MBAM, tenga en cuenta los siguientes elementos, que pueden afectar a la disponibilidad del servicio MBAM:</span><span class="sxs-lookup"><span data-stu-id="6ab1f-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="6ab1f-112">Cifrado de unidad y contraseña de recuperación: Si no se puede enviar una contraseña de recuperación, el cifrado no se inicia en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="6ab1f-113">Carga de datos del estado de cumplimiento: Si el servidor que hospeda el servicio informe de estado de cumplimiento no está disponible, los datos de cumplimiento no permanecen actualizados.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="6ab1f-114">Acceso a clave de recuperación del servicio de asistencia: Si el servicio de asistencia no puede acceder a la información de la base de datos MBAM, el servicio de asistencia no puede proporcionar claves de recuperación a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="6ab1f-115">Disponibilidad de los informes: Si el servidor que hospeda los informes de cumplimiento y cumplimiento no está disponible, los informes no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="6ab1f-116">Cómo usa la copia de seguridad de MBAM el servicio de instantáneas de volumen (VSS)</span><span class="sxs-lookup"><span data-stu-id="6ab1f-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="6ab1f-117">MBAM 2.0 proporciona un escritor de servicio de instantáneas de volumen (VSS), denominado escritor de administración y administración de Microsoft BitLocker, que facilita la copia de seguridad de la base de datos de cumplimiento y la auditoría y la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="6ab1f-118">El servidor de MBAM Windows Installer registra el escritor de VSS de MBAM.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="6ab1f-119">Cualquier error durante el registro de VSS Writer hace que la instalación de MBAM Server se revierta.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="6ab1f-120">En una topología en la que las bases de datos de cumplimiento y comprobación y la base de datos de recuperación están instaladas en diferentes servidores, se registra una instancia independiente de MBAM VSS Writer en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="6ab1f-121">El escritor de VSS de MBAM depende de SQL Server VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="6ab1f-122">El escritor de VSS de SQL Server se registra como parte de la instalación de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="6ab1f-123">Cualquier tecnología de copia de seguridad que use escritores de VSS para realizar copias de seguridad puede descubrir el MBAM VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="6ab1f-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="6ab1f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ab1f-124">Related topics</span></span>


[<span data-ttu-id="6ab1f-125">Mantenimiento de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6ab1f-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 





