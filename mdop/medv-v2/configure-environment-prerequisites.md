---
title: Configurar los requisitos previos de entorno
description: Configurar los requisitos previos de entorno
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826450"
---
# <span data-ttu-id="fffa8-103">Configurar los requisitos previos de entorno</span><span class="sxs-lookup"><span data-stu-id="fffa8-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="fffa8-104">Antes de que pueda implementar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, debe asegurarse de que su entorno cumple los siguientes requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="fffa8-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="fffa8-105">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fffa8-105">Windows 7</span></span>**

<span data-ttu-id="fffa8-106">El agente de hospedaje de MED-V y el Empaquetador de área de trabajo MED-V solo se admiten en Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fffa8-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="fffa8-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="fffa8-107">Windows XP SP3</span></span>**

<span data-ttu-id="fffa8-108">El agente invitado MED-V solo se admite en Windows XP SP3.</span><span class="sxs-lookup"><span data-stu-id="fffa8-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="fffa8-109">.NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="fffa8-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="fffa8-110">Los agentes de host y de hospedaje MED-V y el Empaquetador de área de trabajo MED-V requieren Microsoft .NET Framework 3,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="fffa8-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="fffa8-111">**Importante**  También debe instalar la actualización [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , que resuelve varios problemas de compatibilidad de aplicaciones conocidos.</span><span class="sxs-lookup"><span data-stu-id="fffa8-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="fffa8-112">**Nota:**  Debe instalar manualmente .NET Framework 3,5 SP1 y la actualización KB959209 en la imagen de Windows Virtual PC que preparará para usar con MED-V.</span><span class="sxs-lookup"><span data-stu-id="fffa8-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="fffa8-113">Sin embargo, de forma predeterminada, Microsoft .NET Framework 3,5 SP1 y la actualización se incluyen al instalar Windows 7 en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="fffa8-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="fffa8-114">Una infraestructura de Active Directory</span><span class="sxs-lookup"><span data-stu-id="fffa8-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="fffa8-115">La Directiva de grupo proporciona la administración centralizada y la configuración de los sistemas operativos, las aplicaciones y la configuración de los usuarios en un entorno de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fffa8-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="fffa8-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fffa8-116">Related topics</span></span>


[<span data-ttu-id="fffa8-117">Configurar los requisitos previos de instalación</span><span class="sxs-lookup"><span data-stu-id="fffa8-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="fffa8-118">Arquitectura de alto nivel</span><span class="sxs-lookup"><span data-stu-id="fffa8-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="fffa8-119">Configuraciones admitidas de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="fffa8-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





