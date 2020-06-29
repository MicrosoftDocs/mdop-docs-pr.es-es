---
title: Realizar la administración de BitLocker con MBAM
description: Realizar la administración de BitLocker con MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826500"
---
# <span data-ttu-id="2d324-103">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="2d324-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="2d324-104">Después de planear y de implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurarlo y usarlo para administrar el cifrado de BitLocker empresarial.</span><span class="sxs-lookup"><span data-stu-id="2d324-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="2d324-105">La información de esta sección describe las tareas posteriores a la instalación de la administración de cifrado de BitLocker que se realizan mediante la administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2d324-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="2d324-106">Restablecer un bloqueo de TPM mediante MBAM</span><span class="sxs-lookup"><span data-stu-id="2d324-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="2d324-107">Un módulo de plataforma segura (TPM) es un microchip diseñado para proporcionar funciones básicas de seguridad, principalmente relacionadas con las claves de cifrado.</span><span class="sxs-lookup"><span data-stu-id="2d324-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="2d324-108">El TPM suele instalarse en la placa base de un equipo o portátil y se comunica con el resto del sistema mediante un bus de hardware.</span><span class="sxs-lookup"><span data-stu-id="2d324-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="2d324-109">Los equipos que incorporan un TPM tienen la capacidad de crear claves criptográficas y cifrarlas para que solo el TPM pueda descifrarlas.</span><span class="sxs-lookup"><span data-stu-id="2d324-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="2d324-110">Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces.</span><span class="sxs-lookup"><span data-stu-id="2d324-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="2d324-111">El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro.</span><span class="sxs-lookup"><span data-stu-id="2d324-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="2d324-112">Puede usar MBAM para acceder al sistema de datos de recuperación de claves centralizado en el sitio web de administración y supervisión, donde puede recuperar un archivo de contraseña de propietario de TPM al proporcionar un identificador de equipo y el identificador de usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="2d324-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="2d324-113">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="2d324-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="2d324-114">Recuperar unidades con MBAM</span><span class="sxs-lookup"><span data-stu-id="2d324-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="2d324-115">Cuando trabaje con el cifrado de datos, especialmente en un entorno empresarial, considere cómo se pueden recuperar los datos en caso de que se produzca un error de hardware, cambios en el personal u otras situaciones en las que se puedan perder las claves de cifrado.</span><span class="sxs-lookup"><span data-stu-id="2d324-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="2d324-116">Las características de recuperación de unidades cifradas de MBAM garantizan que los datos se pueden capturar y almacenar y que las herramientas necesarias están disponibles para acceder a un volumen protegido por BitLocker cuando se produce el modo de recuperación de BitLocker, se mueve o se daña.</span><span class="sxs-lookup"><span data-stu-id="2d324-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="2d324-117">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="2d324-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="2d324-118">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="2d324-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="2d324-119">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="2d324-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="2d324-120">Determinar el estado de cifrado de BitLocker de equipos perdidos con MBAM</span><span class="sxs-lookup"><span data-stu-id="2d324-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="2d324-121">Con MBAM, puede determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.</span><span class="sxs-lookup"><span data-stu-id="2d324-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="2d324-122">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="2d324-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="2d324-123">Usar el portal de autoservicio para recuperar el acceso a un equipo</span><span class="sxs-lookup"><span data-stu-id="2d324-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="2d324-124">Si los usuarios finales se bloquean en Windows mediante BitLocker, pueden usar las instrucciones de esta sección para obtener una clave de recuperación de BitLocker para volver a obtener acceso a su equipo.</span><span class="sxs-lookup"><span data-stu-id="2d324-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="2d324-125">Cómo usar el portal de autoservicio para recuperar el acceso a un equipo</span><span class="sxs-lookup"><span data-stu-id="2d324-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="2d324-126">Otros recursos para realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="2d324-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="2d324-127">Operaciones para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d324-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





