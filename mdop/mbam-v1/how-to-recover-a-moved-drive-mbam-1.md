---
title: Cómo recuperar una unidad que se ha movido
description: Cómo recuperar una unidad que se ha movido
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812927"
---
# <span data-ttu-id="965e0-103">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="965e0-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="965e0-104">Al mover una unidad de sistema operativo que ha sido cifrada anteriormente mediante Microsoft BitLocker Administration and Monitoring (MBAM), debe resolver determinados problemas.</span><span class="sxs-lookup"><span data-stu-id="965e0-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="965e0-105">Una vez que se ha conectado un PIN al nuevo equipo, la unidad no aceptará el PIN de inicio que se usó en el equipo anterior.</span><span class="sxs-lookup"><span data-stu-id="965e0-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="965e0-106">El sistema considera que el PIN no es válido debido al cambio en el chip módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="965e0-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="965e0-107">Para poder usar la unidad movida, debe obtener un identificador de clave de recuperación para recuperar la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="965e0-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="965e0-108">Para ello, use el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="965e0-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="965e0-109">Para recuperar una unidad movida</span><span class="sxs-lookup"><span data-stu-id="965e0-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="965e0-110">En el equipo que contiene la unidad movida, inicie en el modo entorno de recuperación de Windows (WinRE) o inicie el equipo con el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="965e0-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="965e0-111">Una vez que el equipo se haya iniciado con WinRE o DaRT, MBAM tratará la unidad de sistema operativo movida como una unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="965e0-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="965e0-112">MBAM mostrará el identificador de la contraseña de recuperación de la unidad y le pedirá la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="965e0-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="965e0-113">**Nota:**  En algunos casos, es posible que pueda hacer clic en **olvidar el PIN** durante el proceso de inicio para entrar en el modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="965e0-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="965e0-114">También se muestra la identificación de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="965e0-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="965e0-115">En el sitio web de administración de MBAM, use la identificación de la clave de recuperación para recuperar la contraseña de recuperación y desbloquear la unidad.</span><span class="sxs-lookup"><span data-stu-id="965e0-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="965e0-116">Si la unidad movida se configuró para usar un chip de TPM en el equipo original, debe realizar pasos adicionales después de desbloquear la unidad y completar el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="965e0-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="965e0-117">En el modo de WinRE, abra un símbolo del sistema y use la herramienta **Manage-BDE** para descifrar la unidad.</span><span class="sxs-lookup"><span data-stu-id="965e0-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="965e0-118">El uso de esta herramienta es la única forma de quitar la protección de TPM con PIN sin el chip de TPM original.</span><span class="sxs-lookup"><span data-stu-id="965e0-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="965e0-119">Una vez completada la eliminación, inicie el sistema normalmente.</span><span class="sxs-lookup"><span data-stu-id="965e0-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="965e0-120">El agente de MBAM continuará aplicando la Directiva para cifrar la unidad con el TPM y el PIN del nuevo equipo.</span><span class="sxs-lookup"><span data-stu-id="965e0-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="965e0-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="965e0-121">Related topics</span></span>


[<span data-ttu-id="965e0-122">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="965e0-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





