---
title: Administración de funciones de MBAM 1.0
description: Administración de funciones de MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821221"
---
# <span data-ttu-id="f442f-103">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f442f-103">Administering MBAM 1.0 Features</span></span>


<span data-ttu-id="f442f-104">Después de completar toda la planeación y la implementación de Microsoft BitLocker (MBAM), puede configurar y usar MBAM para administrar el cifrado de BitLocker empresarial.</span><span class="sxs-lookup"><span data-stu-id="f442f-104">After you complete all necessary Microsoft BitLocker Administration and Monitoring (MBAM) planning and deployment, you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="f442f-105">En la información de esta sección se describen las tareas posteriores a la instalación de las funciones de la MBAM.</span><span class="sxs-lookup"><span data-stu-id="f442f-105">The information in this section describes post-installation day-to-day MBAM feature operations tasks.</span></span>

## <span data-ttu-id="f442f-106">Administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="f442f-106">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="f442f-107">Una vez completada la configuración de MBAM para todas las características del servidor, se debe conceder acceso a los usuarios administrativos a estas características de servidor.</span><span class="sxs-lookup"><span data-stu-id="f442f-107">After MBAM Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="f442f-108">Como práctica recomendada, los administradores que administrarán o usarán características de servidor de MBAM se deben asignar a grupos de seguridad de Active Directory y, a continuación, esos grupos deben agregarse al grupo local administrativo de MBAM adecuado.</span><span class="sxs-lookup"><span data-stu-id="f442f-108">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="f442f-109">Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="f442f-109">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-1.md)

## <span data-ttu-id="f442f-110">Administrar la compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="f442f-110">Manage Hardware Compatibility</span></span>


<span data-ttu-id="f442f-111">La característica de compatibilidad de hardware de MBAM puede ayudarle a garantizar que solo se cifrará el hardware del equipo que especifique como compatible con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f442f-111">The MBAM Hardware Compatibility feature can help you to ensure that only the computer hardware that you specify as supporting BitLocker will be encrypted.</span></span> <span data-ttu-id="f442f-112">Cuando esta característica está activada, bit \ _admmontla cifrará solo los equipos que estén marcados como compatibles.</span><span class="sxs-lookup"><span data-stu-id="f442f-112">When this feature is turned on, bit\_admmontla will encrypt only computers that are marked as Compatible.</span></span>

<span data-ttu-id="f442f-113">**Importante**  Cuando esta característica está desactivada, todos los equipos en los que se implemente la Directiva MBAM estarán cifrados.</span><span class="sxs-lookup"><span data-stu-id="f442f-113">**Important** When this feature is turned off, all computers where the MBAM policy is deployed will be encrypted.</span></span>

 

<span data-ttu-id="f442f-114">MBAM puede recopilar información sobre la marca y el modelo de equipos cliente si implementa la Directiva de grupo "permitir comprobación de compatibilidad de hardware".</span><span class="sxs-lookup"><span data-stu-id="f442f-114">MBAM can collect information on both the make and model of client computers if you deploy the “Allow Hardware Compatibility Checking” Group Policy.</span></span> <span data-ttu-id="f442f-115">Si configura esta Directiva, el agente de MBAM notifica la marca del equipo y la información del modelo al servidor de MBAM cuando se implementa el cliente MBAM en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="f442f-115">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

[<span data-ttu-id="f442f-116">Cómo administrar la compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="f442f-116">How to Manage Hardware Compatibility</span></span>](how-to-manage-hardware-compatibility-mbam-1.md)

[<span data-ttu-id="f442f-117">Cómo administrar exenciones de cifrado de BitLocker de usuario</span><span class="sxs-lookup"><span data-stu-id="f442f-117">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## <span data-ttu-id="f442f-118">Administrar exenciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="f442f-118">Manage BitLocker encryption exemptions</span></span>


<span data-ttu-id="f442f-119">MBAM puede conceder dos formas de exención del cifrado de BitLocker: exención de equipos y exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="f442f-119">MBAM can grant two forms of exemption from BitLocker encryption: computer exemption and user exemption.</span></span> <span data-ttu-id="f442f-120">La exención de equipo se usa normalmente cuando una empresa tiene equipos que no tienen que cifrarse, como equipos que se usan en el desarrollo o la prueba, o equipos anteriores que no son compatibles con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f442f-120">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="f442f-121">En algunos casos, la legislación local también puede requerir que determinados equipos no estén cifrados.</span><span class="sxs-lookup"><span data-stu-id="f442f-121">In some cases, local law may also require that certain computers are not encrypted.</span></span> <span data-ttu-id="f442f-122">También puede optar por eximir a los usuarios que no necesiten o deseen que sus unidades estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="f442f-122">You may also choose to exempt users who do not need or want their drives encrypted.</span></span>

[<span data-ttu-id="f442f-123">Cómo administrar exenciones de cifrado de BitLocker de equipo</span><span class="sxs-lookup"><span data-stu-id="f442f-123">How to Manage Computer BitLocker Encryption Exemptions</span></span>](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## <span data-ttu-id="f442f-124">Administrar las opciones de cifrado de BitLocker de MBAM con el panel de control</span><span class="sxs-lookup"><span data-stu-id="f442f-124">Manage MBAM Client BitLocker Encryption Options by using the Control Panel</span></span>


<span data-ttu-id="f442f-125">Si se habilita mediante objetos de directiva de grupo (GPO), un panel de control de MBAM personalizado que se denomine opciones de cifrado de BitLocker estará disponible en **sistema y seguridad**.</span><span class="sxs-lookup"><span data-stu-id="f442f-125">If enabled through a Group Policy Objects (GPO), a custom MBAM control panel that is named BitLocker Encryption Options will be available under **System and Security**.</span></span> <span data-ttu-id="f442f-126">Este panel de control personalizado reemplaza al panel de control predeterminado de BitLocker de Windows.</span><span class="sxs-lookup"><span data-stu-id="f442f-126">This customized control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="f442f-127">El panel de control de MBAM te permite desbloquear unidades cifradas (fijas y extraíbles) y también te ayuda a administrar tu PIN o tu contraseña.</span><span class="sxs-lookup"><span data-stu-id="f442f-127">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span>

[<span data-ttu-id="f442f-128">Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="f442f-128">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## <span data-ttu-id="f442f-129">Otros recursos para administrar características de MBAM</span><span class="sxs-lookup"><span data-stu-id="f442f-129">Other resources for Administering MBAM features</span></span>


[<span data-ttu-id="f442f-130">Operaciones para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f442f-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





