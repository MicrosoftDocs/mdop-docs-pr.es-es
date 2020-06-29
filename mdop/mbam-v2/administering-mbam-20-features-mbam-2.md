---
title: Administración de funciones de MBAM 2.0
description: Administración de funciones de MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823510"
---
# <span data-ttu-id="63648-103">Administración de funciones de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="63648-103">Administering MBAM 2.0 Features</span></span>


<span data-ttu-id="63648-104">Después de completar todo el planeamiento necesario y, a continuación, implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurarlo y usarlo para administrar el cifrado de BitLocker en toda la empresa. la información de esta sección describe las tareas de operaciones de supervisión y administración de BitLocker posteriores a la instalación.</span><span class="sxs-lookup"><span data-stu-id="63648-104">After completing all necessary planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker encryption across the enterprise The information in this section describes post-installation day-to-day Microsoft BitLocker Administration and Monitoring feature operations tasks.</span></span>

## <span data-ttu-id="63648-105">Administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="63648-105">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="63648-106">Una vez completada la configuración de MBAM para todas las características del servidor, se debe conceder acceso a los usuarios administrativos.</span><span class="sxs-lookup"><span data-stu-id="63648-106">After MBAM Setup is complete for all server features, administrative users have to be granted access to them.</span></span> <span data-ttu-id="63648-107">Como práctica recomendada, los administradores que administrarán o usarán las características de servidor de MBAM deben asignarse a grupos de seguridad de los servicios de dominio de Active Directory y, a continuación, esos grupos deben agregarse al grupo local administrativo de MBAM adecuado.</span><span class="sxs-lookup"><span data-stu-id="63648-107">As a best practice, administrators who will manage or use MBAM server features should be assigned to Active Directory Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="63648-108">Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="63648-108">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-2.md)

## <span data-ttu-id="63648-109">Administrar exenciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="63648-109">Manage BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="63648-110">MBAM le permite conceder exenciones de cifrado a usuarios específicos que no necesitan o quieren que sus unidades estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="63648-110">MBAM lets you grant encryption exemptions to specific users who do not need or want their drives encrypted.</span></span> <span data-ttu-id="63648-111">La exención de equipo se usa normalmente cuando una empresa tiene equipos que no tienen que cifrarse, como equipos que se usan en el desarrollo o la prueba, o equipos anteriores que no son compatibles con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="63648-111">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="63648-112">En algunos casos, la legislación local también puede requerir que determinados equipos no estén cifrados.</span><span class="sxs-lookup"><span data-stu-id="63648-112">In some cases, local law may also require that certain computers are not encrypted.</span></span>

[<span data-ttu-id="63648-113">Cómo administrar exenciones de cifrado de BitLocker de usuario</span><span class="sxs-lookup"><span data-stu-id="63648-113">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## <span data-ttu-id="63648-114">Administrar las opciones de cifrado de BitLocker de MBAM con el panel de control</span><span class="sxs-lookup"><span data-stu-id="63648-114">Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="63648-115">MBAM proporciona un panel de control personalizado, denominado opciones de cifrado de BitLocker, que aparecerá en **sistema y seguridad**.</span><span class="sxs-lookup"><span data-stu-id="63648-115">MBAM provides a custom control panel, called BitLocker Encryption Options, that will appear under **System and Security**.</span></span> <span data-ttu-id="63648-116">El panel de control de MBAM se puede usar para desbloquear unidades cifradas y extraíbles, y también para administrar su PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="63648-116">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span>

<span data-ttu-id="63648-117">**Nota:**  Este panel de control personalizado no reemplaza al panel de control predeterminado de BitLocker de Windows.</span><span class="sxs-lookup"><span data-stu-id="63648-117">**Note** This customized control panel does not replace the default Windows BitLocker control panel.</span></span>

 

[<span data-ttu-id="63648-118">Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="63648-118">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## <span data-ttu-id="63648-119">Otros recursos para administrar características de MBAM</span><span class="sxs-lookup"><span data-stu-id="63648-119">Other Resources for Administering MBAM Features</span></span>


[<span data-ttu-id="63648-120">Operaciones para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="63648-120">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





