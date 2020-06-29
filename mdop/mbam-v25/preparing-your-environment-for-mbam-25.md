---
title: Preparación del entorno para MBAM 2.5
description: Preparación del entorno para MBAM 2.5
author: dansimp
ms.assetid: 7552ba08-9dbf-40cd-8920-203d733fd242
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b18c9853035018c2e36dd447fbf0effbf49c45cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825491"
---
# <span data-ttu-id="36cf8-103">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="36cf8-103">Preparing your Environment for MBAM 2.5</span></span>


<span data-ttu-id="36cf8-104">Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), debe asegurarse de que cumple los requisitos previos para instalar el producto.</span><span class="sxs-lookup"><span data-stu-id="36cf8-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="36cf8-105">Cuando sepa Cuáles son los requisitos previos, puede implementar el producto de forma eficaz y habilitar sus características para que sea más eficaz la compatibilidad de los objetivos empresariales de su organización.</span><span class="sxs-lookup"><span data-stu-id="36cf8-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="36cf8-106">Si implementa la administración y la supervisión de Microsoft BitLocker con Configuration Manager, asegúrese de cumplir con los requisitos adicionales para Configuration Manager, que se enumeran más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="36cf8-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Configuration Manager, ensure that you meet the additional requirements for Configuration Manager, which are listed later in this topic.</span></span>

## <span data-ttu-id="36cf8-107">Revisar los requisitos previos de implementación de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="36cf8-107">Review MBAM 2.5 deployment prerequisites</span></span>


<span data-ttu-id="36cf8-108">Para asegurarse de que la implementación de MBAM se realice correctamente, asegúrese de revisar y completar los requisitos previos de software necesarios antes de instalar el cliente de MBAM y configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="36cf8-108">To ensure that your MBAM deployment is successful, make sure that you review and complete the required software prerequisites before you install the MBAM Client and configure the MBAM Server features.</span></span>

[<span data-ttu-id="36cf8-109">Requisitos previos de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="36cf8-109">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)

## <span data-ttu-id="36cf8-110">Plan for MBAM 2,5 requisitos de la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="36cf8-110">Plan for MBAM 2.5 Group Policy requirements</span></span>


<span data-ttu-id="36cf8-111">Antes de que MBAM pueda administrar clientes en la empresa, debe descargar y configurar plantillas de directiva de grupo que sean específicas de MBAM y, después, configurar las opciones de directiva de grupo que desee para su entorno.</span><span class="sxs-lookup"><span data-stu-id="36cf8-111">Before MBAM can manage clients in the enterprise, you must download and configure Group Policy templates that are specific to MBAM, and then configure the Group Policy settings that you want for your environment.</span></span>

[<span data-ttu-id="36cf8-112">Planificación para requisitos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="36cf8-112">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

## <span data-ttu-id="36cf8-113">Planear los roles y las cuentas de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="36cf8-113">Plan for MBAM 2.5 roles and accounts</span></span>


<span data-ttu-id="36cf8-114">Como parte de los requisitos previos, debe definir determinadas funciones y cuentas, que se usan en MBAM para proporcionar seguridad y derechos de acceso a características y servidores específicos, como las bases de datos que se ejecutan en SQL Server y las aplicaciones web que se ejecutan en el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="36cf8-114">As part of the prerequisites, you must define certain roles and accounts, which are used in MBAM to provide security and access rights to specific servers and features, such as the databases running on SQL Server and the web applications running on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="36cf8-115">Planificación para cuentas y grupos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="36cf8-115">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)

## <span data-ttu-id="36cf8-116">Otros recursos para la planeación de MBAM</span><span class="sxs-lookup"><span data-stu-id="36cf8-116">Other resources for MBAM planning</span></span>


[<span data-ttu-id="36cf8-117">Planificación para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="36cf8-117">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="36cf8-118">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="36cf8-118">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="36cf8-119">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="36cf8-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="36cf8-120">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="36cf8-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="36cf8-121">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="36cf8-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





