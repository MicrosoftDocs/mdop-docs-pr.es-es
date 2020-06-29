---
title: Cómo recuperar una unidad que se ha movido
description: Cómo recuperar una unidad que se ha movido
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823341"
---
# <span data-ttu-id="a50b6-103">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="a50b6-103">How to Recover a Moved Drive</span></span>
<span data-ttu-id="a50b6-104">En este tema se explica cómo usar el sitio web de administración y supervisión (también conocido como servicio de asistencia) para recuperar una unidad de sistema operativo que se movió después de ser cifrada por la supervisión y administración de BitLocker de Microsoft (MBAM).</span><span class="sxs-lookup"><span data-stu-id="a50b6-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to recover an operating system drive that was moved after being encrypted by Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="a50b6-105">Cuando se mueve una unidad, ya no acepta el PIN que se usó en el equipo anterior porque el chip módulo de plataforma segura (TPM) ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a50b6-105">When a drive is moved, it no longer accepts the PIN that was used in the previous computer because the Trusted Platform Module (TPM) chip has changed.</span></span> <span data-ttu-id="a50b6-106">Para recuperar la unidad movida, debe obtener la identificación de la clave de recuperación para recuperar la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a50b6-106">To recover the moved drive, you must obtain the recovery key ID to retrieve the recovery password.</span></span>

<span data-ttu-id="a50b6-107">Para recuperar una unidad movida, debe usar el área de **recuperación de unidad** del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="a50b6-107">To recover a moved drive, you must use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="a50b6-108">Para acceder al área de **recuperación de unidades** , debe tener asignado el rol de usuarios del Departamento de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a50b6-108">To access the **Drive Recovery** area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="a50b6-109">Para obtener más información sobre estos roles, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="a50b6-109">For more information about these roles, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

**<span data-ttu-id="a50b6-110">Para recuperar una unidad movida</span><span class="sxs-lookup"><span data-stu-id="a50b6-110">To recover a moved drive</span></span>**
1.  <span data-ttu-id="a50b6-111">En el equipo que contiene la unidad movida, inicie el equipo en modo entorno de recuperación de Windows (WinRE) o inicie el equipo con el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="a50b6-111">On the computer that contains the moved drive, start the computer in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="a50b6-112">Una vez que el equipo se haya iniciado con WinRE o DaRT, MBAM tratará la unidad de sistema operativo movida como una unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="a50b6-112">After the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a fixed data drive.</span></span> <span data-ttu-id="a50b6-113">MBAM mostrará el identificador de la contraseña de recuperación de la unidad y le pedirá la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a50b6-113">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="a50b6-114">**Nota:**  En algunos casos, es posible que pueda hacer clic en **olvidé el PIN** durante el proceso de inicio y, después, especificar el modo de recuperación para mostrar la identificación de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a50b6-114">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="a50b6-115">Use la identificación de la clave de recuperación para recuperar la contraseña de recuperación y desbloquear la unidad desde el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="a50b6-115">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring Website.</span></span> <span data-ttu-id="a50b6-116">Para obtener instrucciones, consulte [Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="a50b6-116">For instructions, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span></span>

    <span data-ttu-id="a50b6-117">Si la unidad movida se configuró para usar un chip TPM en el equipo original, complete los siguientes pasos adicionales.</span><span class="sxs-lookup"><span data-stu-id="a50b6-117">If the moved drive was configured to use a TPM chip on the original computer, complete the following additional steps.</span></span> <span data-ttu-id="a50b6-118">En caso contrario, el proceso de recuperación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="a50b6-118">Otherwise, the recovery process is complete.</span></span>

4.  <span data-ttu-id="a50b6-119">Después de desbloquear la unidad y completar el proceso de inicio, abra un símbolo del sistema en el modo de WinRE y use el `manage-bde` comando para descifrar la unidad.</span><span class="sxs-lookup"><span data-stu-id="a50b6-119">After unlocking the drive and completing the start process, open a command prompt in WinRE mode and use the `manage-bde` command to decrypt the drive.</span></span> <span data-ttu-id="a50b6-120">El uso de esta herramienta es la única forma de quitar el TPM más el protector del PIN sin el chip TPM original.</span><span class="sxs-lookup"><span data-stu-id="a50b6-120">Using this tool is the only way to remove the TPM plus the PIN protector without the original TPM chip.</span></span> <span data-ttu-id="a50b6-121">Para obtener información sobre el `manage-bde` comando, consulte [Manage-BDE](https://go.microsoft.com/fwlink/?LinkId=393567).</span><span class="sxs-lookup"><span data-stu-id="a50b6-121">For information about the `manage-bde` command, see [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span></span>

5.  <span data-ttu-id="a50b6-122">Una vez completada la eliminación, inicie el equipo de forma normal.</span><span class="sxs-lookup"><span data-stu-id="a50b6-122">When the removal is completed, start the computer normally.</span></span> <span data-ttu-id="a50b6-123">El agente de MBAM aplicará ahora la Directiva para cifrar la unidad con el TPM del nuevo equipo más el PIN.</span><span class="sxs-lookup"><span data-stu-id="a50b6-123">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus the PIN.</span></span>



## <span data-ttu-id="a50b6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a50b6-124">Related topics</span></span>


[<span data-ttu-id="a50b6-125">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a50b6-125">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="a50b6-126">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="a50b6-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a50b6-127">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a50b6-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a50b6-128">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a50b6-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





