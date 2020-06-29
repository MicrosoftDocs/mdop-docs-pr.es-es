---
title: Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración
description: Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812566"
---
# <span data-ttu-id="68bad-103">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="68bad-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="68bad-104">Si va a instalar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 mediante la característica de integración de System Center Configuration Manager, debe completar los requisitos previos que se describen en este tema, además de los de [MBAM 2,5 Server Prerequisites para las topologías de integración independiente y de configuración](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="68bad-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="68bad-105">También debe crear o modificar archivos. mof necesarios para la topología de integración del administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="68bad-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="68bad-106">Requisitos previos de la función de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="68bad-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="68bad-107">Si está configurando MBAM con la topología de integración de System Center Configuration Manager, debe completar los requisitos previos adicionales que se requieren para Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="68bad-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="68bad-108">Requisitos previos de la función de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="68bad-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="68bad-109">Editar el archivo Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="68bad-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="68bad-110">Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo Configuration. mof para SystemCenter2012 ConfigurationManager y Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="68bad-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="68bad-111">Editar el archivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="68bad-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="68bad-112">Crear o editar el archivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="68bad-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="68bad-113">Para permitir que los equipos cliente informen de los detalles de cumplimiento de BitLocker en los informes de MBAM Configuration Manager, tiene que crear o editar el archivo SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="68bad-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="68bad-114">Si está usando SystemCenter2012 ConfigurationManager, debe crear el archivo.</span><span class="sxs-lookup"><span data-stu-id="68bad-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="68bad-115">En el administrador de configuración 2007, el archivo ya existe, por lo que tendrá que editar, pero no sobrescribir, el archivo existente.</span><span class="sxs-lookup"><span data-stu-id="68bad-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="68bad-116">Crear o editar el archivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="68bad-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="68bad-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68bad-117">Related topics</span></span>


[<span data-ttu-id="68bad-118">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="68bad-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="68bad-119">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="68bad-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="68bad-120">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="68bad-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="68bad-121">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="68bad-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="68bad-122">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="68bad-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="68bad-123">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="68bad-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




