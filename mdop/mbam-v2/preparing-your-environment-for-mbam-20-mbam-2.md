---
title: Preparación del entorno para MBAM 2.0
description: Preparación del entorno para MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825610"
---
# <span data-ttu-id="47d08-103">Preparación del entorno para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47d08-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="47d08-104">Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), debe asegurarse de que cumple los requisitos previos para instalar el producto.</span><span class="sxs-lookup"><span data-stu-id="47d08-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="47d08-105">Cuando sepa Cuáles son los requisitos previos, puede implementar el producto de forma eficaz y habilitar sus características para que sea más eficaz la compatibilidad de los objetivos empresariales de su organización.</span><span class="sxs-lookup"><span data-stu-id="47d08-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="47d08-106">Si implementa la administración y administración de Microsoft BitLocker con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="47d08-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="47d08-107">Revisar los requisitos previos de implementación de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="47d08-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="47d08-108">El cliente MBAM y cada una de las características de servidor de MBAM tienen requisitos previos específicos que deben cumplirse para poder instalarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="47d08-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="47d08-109">Para garantizar una instalación correcta de los clientes de MBAM y las características de MBAM Server, asegúrese de que los equipos especificados para la instalación de características de servidor o cliente de MBAM MBAM se hayan preparado correctamente para la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="47d08-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="47d08-110">**Nota:**  El programa de instalación de MBAM verifica que se cumplan todos los requisitos previos antes de que se inicie la instalación.</span><span class="sxs-lookup"><span data-stu-id="47d08-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="47d08-111">Si no se cumplen todos los requisitos previos, se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="47d08-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="47d08-112">Requisitos previos de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47d08-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="47d08-113">Plan for MBAM 2,0 requisitos de la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="47d08-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="47d08-114">Antes de que MBAM pueda administrar clientes en la empresa, debe definir una directiva de grupo para los requisitos de cifrado de su entorno.</span><span class="sxs-lookup"><span data-stu-id="47d08-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="47d08-115">**Importante**  MBAM no funcionará con directivas para el cifrado de unidad BitLocker independiente.</span><span class="sxs-lookup"><span data-stu-id="47d08-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="47d08-116">Es necesario definir la configuración de la Directiva de grupo para MBAM, o el cifrado y la aplicación de BitLocker producirán errores.</span><span class="sxs-lookup"><span data-stu-id="47d08-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="47d08-117">Planificación de los requisitos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47d08-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="47d08-118">Planear los roles de administrador de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="47d08-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="47d08-119">Los roles de administrador de MBAM se administran por grupos locales creados por el programa de instalación de MBAM al instalar el servidor de administración y administración de BitLocker, la característica informes de cumplimiento y de auditoría, y la base de datos de estado de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="47d08-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="47d08-120">La pertenencia a los roles de administración y supervisión de Microsoft BitLocker puede administrarse mejor creando grupos de seguridad en ActiveDirectoryDomainServices, agregando las cuentas de administrador adecuadas a esos grupos y, a continuación, agregando esos grupos de seguridad a los grupos locales administración y supervisión de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="47d08-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="47d08-121">Para obtener más información, consulte [Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="47d08-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="47d08-122">Otros recursos para la planeación de MBAM</span><span class="sxs-lookup"><span data-stu-id="47d08-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="47d08-123">Planificación para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47d08-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="47d08-124">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47d08-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





