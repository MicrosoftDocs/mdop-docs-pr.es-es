---
title: Implementación de la actualización de versión de idioma de MBAM 1.0
description: Implementación de la actualización de versión de idioma de MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812823"
---
# <span data-ttu-id="dd9f4-103">Implementación de la actualización de versión de idioma de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="dd9f4-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="dd9f4-104">Administración y supervisión de Microsoft BitLocker (MBAM) 1.0 versión de idioma es una actualización de MBAM e incluye compatibilidad con nuevos idiomas.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="dd9f4-105">Los nuevos idiomas son:</span><span class="sxs-lookup"><span data-stu-id="dd9f4-105">The new languages are:</span></span>

-   <span data-ttu-id="dd9f4-106">Inglés (es-es)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-106">English (en-us)</span></span>

-   <span data-ttu-id="dd9f4-107">Francés (fr)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-107">French (fr)</span></span>

-   <span data-ttu-id="dd9f4-108">Italiano (it)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-108">Italian (it)</span></span>

-   <span data-ttu-id="dd9f4-109">Alemán (de)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-109">German (de)</span></span>

-   <span data-ttu-id="dd9f4-110">Español (es)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-110">Spanish (es)</span></span>

-   <span data-ttu-id="dd9f4-111">Coreano (KO)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-111">Korean (ko)</span></span>

-   <span data-ttu-id="dd9f4-112">Japonés (JA)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-112">Japanese (ja)</span></span>

-   <span data-ttu-id="dd9f4-113">Portugués brasileño (pt-br)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="dd9f4-114">Ruso (RU)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-114">Russian (ru)</span></span>

-   <span data-ttu-id="dd9f4-115">Chino tradicional (zh-TW)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="dd9f4-116">Chino simplificado (zh-CN)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="dd9f4-117">La actualización del idioma de MBAM 1.0 cambiará el número de versión de MBAM 1.0.1237.1 a MBAM 1.0.2001.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="dd9f4-118">No es necesario volver a instalar todas las características de MBAM para agregar estos idiomas adicionales.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="dd9f4-119">Este tema define los pasos necesarios para agregar los nuevos idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="dd9f4-120">Implementar la versión internacional de MBAM en las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="dd9f4-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="dd9f4-121">Para comenzar, debe actualizar las siguientes características del servidor de MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd9f4-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="dd9f4-122">Informe de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="dd9f4-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="dd9f4-123">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="dd9f4-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="dd9f4-124">Plantillas de Directiva</span><span class="sxs-lookup"><span data-stu-id="dd9f4-124">Policy Templates</span></span>

<span data-ttu-id="dd9f4-125">A continuación, debe ejecutar **MbamSetup.exe** para actualizar las características de MBAM que se ejecutan en el mismo servidor al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="dd9f4-126">Cómo instalar la actualización de lenguaje MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="dd9f4-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="dd9f4-127">Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos</span><span class="sxs-lookup"><span data-stu-id="dd9f4-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="dd9f4-128">Instalar la actualización de idioma MBAM para las directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="dd9f4-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="dd9f4-129">Las plantillas de directiva de grupo MBAM se pueden instalar en cada estación de trabajo de administración o se pueden copiar en el almacén central de directivas de grupo para que las plantillas estén disponibles para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="dd9f4-130">Las plantillas de Directiva no se pueden instalar directamente en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="dd9f4-131">Si no usa una tienda central de directivas de grupo, debe copiar las directivas manualmente en cada controlador de dominio que administre la Directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="dd9f4-132">Para agregar las plantillas de directivas de idioma de MBAM, copie los archivos de idioma de directiva de grupo de%SystemRoot%\\PolicyDefinitions en el equipo donde se instaló la función "plantillas de directiva" en la misma ubicación del equipo de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="dd9f4-133">A continuación se muestran algunos ejemplos de archivos de directiva de Grupo:</span><span class="sxs-lookup"><span data-stu-id="dd9f4-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="dd9f4-134">BitLockerManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="dd9f4-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="dd9f4-135">BitLockerUserManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="dd9f4-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="dd9f4-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="dd9f4-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="dd9f4-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="dd9f4-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="dd9f4-138">fr-fr\\ BitLockerManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="dd9f4-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="dd9f4-139">fr-fr\\ BitLockerUserManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="dd9f4-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="dd9f4-140">(y de forma similar para cada idioma admitido)</span><span class="sxs-lookup"><span data-stu-id="dd9f4-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="dd9f4-141">Problemas conocidos de la versión internacional de MBAM</span><span class="sxs-lookup"><span data-stu-id="dd9f4-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="dd9f4-142">Este tema contiene problemas conocidos de la versión internacional de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="dd9f4-143">Problemas conocidos de la versión internacional de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd9f4-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="dd9f4-144">Otros recursos para implementar la actualización de idioma MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="dd9f4-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="dd9f4-145">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="dd9f4-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





