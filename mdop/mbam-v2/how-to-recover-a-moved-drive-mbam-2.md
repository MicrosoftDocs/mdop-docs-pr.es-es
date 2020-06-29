---
title: Cómo recuperar una unidad que se ha movido
description: Cómo recuperar una unidad que se ha movido
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825061"
---
# <span data-ttu-id="af885-103">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="af885-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="af885-104">Al mover una unidad de sistema operativo cifrada mediante Microsoft BitLocker Administration and Monitoring (MBAM), la unidad no aceptará el PIN que se usó en un equipo anterior debido al cambio en el módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="af885-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="af885-105">Para usar la unidad movida, necesitará una forma de obtener la identificación de la clave de recuperación para recuperar la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="af885-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="af885-106">Use el siguiente procedimiento para recuperar una unidad que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="af885-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="af885-107">Para recuperar una unidad movida</span><span class="sxs-lookup"><span data-stu-id="af885-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="af885-108">En el equipo que contiene la unidad movida, inicie el equipo en modo entorno de recuperación de Windows (WinRE) o inicie el equipo con el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="af885-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="af885-109">Una vez que el equipo se haya iniciado con WinRE o DaRT, la administración y la supervisión de Microsoft BitLocker tratarán la unidad de sistema operativo movida como una unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="af885-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="af885-110">MBAM mostrará el identificador de la contraseña de recuperación de la unidad y le pedirá la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="af885-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="af885-111">**Nota:**  En algunos casos, es posible que pueda hacer clic en **olvidé el PIN** durante el proceso de inicio y, después, especificar el modo de recuperación para mostrar la identificación de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="af885-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="af885-112">Use la identificación de la clave de recuperación para recuperar la contraseña de recuperación y desbloquear la unidad desde el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="af885-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="af885-113">Si la unidad movida se configuró para usar un chip de TPM en el equipo original, debe realizar pasos adicionales después de desbloquear la unidad y completar el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="af885-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="af885-114">En el modo de WinRE, abra un símbolo del sistema y use la herramienta **Manage-BDE** para descifrar la unidad.</span><span class="sxs-lookup"><span data-stu-id="af885-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="af885-115">Usar esta herramienta es la única forma de quitar el TPM más el protector del PIN sin el chip TPM original.</span><span class="sxs-lookup"><span data-stu-id="af885-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="af885-116">Una vez completada la eliminación, inicie el equipo de forma normal.</span><span class="sxs-lookup"><span data-stu-id="af885-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="af885-117">El agente de MBAM aplicará ahora la Directiva para cifrar la unidad con el TPM y el PIN del nuevo equipo.</span><span class="sxs-lookup"><span data-stu-id="af885-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="af885-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af885-118">Related topics</span></span>


[<span data-ttu-id="af885-119">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="af885-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





