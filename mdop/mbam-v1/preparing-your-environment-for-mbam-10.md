---
title: Preparación del entorno para MBAM 1.0
description: Preparación del entorno para MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823191"
---
# <span data-ttu-id="bab55-103">Preparación del entorno para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bab55-103">Preparing your Environment for MBAM 1.0</span></span>


<span data-ttu-id="bab55-104">Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), asegúrese de cumplir los requisitos previos necesarios para instalar el producto.</span><span class="sxs-lookup"><span data-stu-id="bab55-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you have met the necessary prerequisites to install the product.</span></span> <span data-ttu-id="bab55-105">Si conoce los requisitos previos previamente, puede implementar el producto de forma eficaz y habilitar sus características, que pueden admitir los objetivos empresariales de su organización de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="bab55-105">If you know the prerequisites in advance, you can efficiently deploy the product and enable its features, which can support the business objectives of your organization more effectively.</span></span>

## <span data-ttu-id="bab55-106">Revisar los requisitos previos de implementación de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="bab55-106">Review MBAM 1.0 deployment prerequisites</span></span>


<span data-ttu-id="bab55-107">El cliente MBAM y cada una de las características de servidor de MBAM tienen requisitos previos específicos que deben cumplirse para poder instalarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="bab55-107">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="bab55-108">Para garantizar una instalación correcta de los clientes de MBAM y las características de MBAM Server, debe asegurarse de que la instalación de las características de los equipos especificados para MBAM cliente o MBAM Server se haya preparado correctamente para la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bab55-108">To ensure successful installation of MBAM Clients and MBAM Server features, you should plan to ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="bab55-109">**Nota:**  El programa de instalación de MBAM verifica si se cumplen todos los requisitos previos antes de que se inicie la instalación.</span><span class="sxs-lookup"><span data-stu-id="bab55-109">**Note** MBAM Setup verifies if all prerequisites are met before installation starts.</span></span> <span data-ttu-id="bab55-110">Si no se cumplen, se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="bab55-110">If they are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="bab55-111">Requisitos previos de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bab55-111">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)

## <span data-ttu-id="bab55-112">Plan for MBAM 1,0 requisitos de la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="bab55-112">Plan for MBAM 1.0 Group Policy requirements</span></span>


<span data-ttu-id="bab55-113">Antes de que MBAM pueda administrar clientes en la empresa, debe definir la Directiva de grupo para los requisitos de cifrado de su entorno.</span><span class="sxs-lookup"><span data-stu-id="bab55-113">Before MBAM can manage clients in the enterprise, you must define the Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="bab55-114">**Importante**  MBAM no funcionará con directivas para el cifrado de unidad BitLocker independiente.</span><span class="sxs-lookup"><span data-stu-id="bab55-114">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="bab55-115">La Directiva de grupo debe definirse para MBAM; de lo contrario, se producirá un error en el cifrado y la aplicación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bab55-115">Group Policy must be defined for MBAM; otherwise, the BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="bab55-116">Planificación de los requisitos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bab55-116">Planning for MBAM 1.0 Group Policy Requirements</span></span>](planning-for-mbam-10-group-policy-requirements.md)

## <span data-ttu-id="bab55-117">Planear los roles de administrador de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="bab55-117">Plan for MBAM 1.0 administrator roles</span></span>


<span data-ttu-id="bab55-118">Los roles de administrador de MBAM se administran por grupos locales creados por el programa de instalación de MBAM al instalar lo siguiente: servidor de administración y administración de BitLocker, la característica informes de cumplimiento y de auditoría, y la base de datos de estado de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="bab55-118">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the following: BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="bab55-119">La pertenencia de roles de MBAM se puede administrar más eficazmente si crea grupos de seguridad en ActiveDirectoryDomainServices, agrega las cuentas de administrador apropiadas a esos grupos y, a continuación, agrega esos grupos de seguridad a los grupos locales de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bab55-119">The membership of MBAM roles can be managed more effectively if you create security groups in ActiveDirectoryDomainServices, add the appropriate administrator accounts to those groups, and then add those security groups to the MBAM local groups.</span></span> <span data-ttu-id="bab55-120">Para obtener más información, consulte [Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="bab55-120">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md).</span></span>

[<span data-ttu-id="bab55-121">Planificación de roles de administrador de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bab55-121">Planning for MBAM 1.0 Administrator Roles</span></span>](planning-for-mbam-10-administrator-roles.md)

## <span data-ttu-id="bab55-122">Otros recursos para la planeación de MBAM</span><span class="sxs-lookup"><span data-stu-id="bab55-122">Other resources for MBAM planning</span></span>


[<span data-ttu-id="bab55-123">Planificación para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bab55-123">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





