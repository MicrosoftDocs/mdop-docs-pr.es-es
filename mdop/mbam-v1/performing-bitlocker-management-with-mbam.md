---
title: Realizar la administración de BitLocker con MBAM
description: Realizar la administración de BitLocker con MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825891"
---
# <span data-ttu-id="cf0dd-103">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="cf0dd-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="cf0dd-104">Después de implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurar y usar MBAM para administrar el cifrado de BitLocker empresarial.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-104">After you deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="cf0dd-105">En esta sección se describen las tareas de administración de cifrado de BitLocker posteriores a la instalación que se pueden llevar a cabo con MBAM.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-105">This section describes post-installation, day-to-day BitLocker encryption management tasks that can be accomplished by using MBAM.</span></span>

## <span data-ttu-id="cf0dd-106">Restablecer un bloqueo de TPM con MBAM</span><span class="sxs-lookup"><span data-stu-id="cf0dd-106">Reset a TPM Lockout with MBAM</span></span>


<span data-ttu-id="cf0dd-107">Un microchip de módulo de plataforma segura (TPM) proporciona funciones básicas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-107">A Trusted Platform Module (TPM) microchip provides basic security-related functions.</span></span> <span data-ttu-id="cf0dd-108">Estas funciones se realizan principalmente mediante el uso de claves de cifrado.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-108">These functions are accomplished primarily by the use of encryption keys.</span></span> <span data-ttu-id="cf0dd-109">El TPM suele instalarse en la placa base de un equipo o portátil y se comunica con el resto del sistema mediante un bus de hardware.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-109">The TPM is typically installed on the motherboard of a computer or laptop and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="cf0dd-110">Los equipos que incorporan un TPM pueden crear claves criptográficas que solo TPM puede descifrar.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-110">Computers that incorporate a TPM can create cryptographic keys that can be decrypted only by the TPM.</span></span> <span data-ttu-id="cf0dd-111">Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-111">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="cf0dd-112">El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-112">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="cf0dd-113">El sistema de datos de recuperación de claves del sitio web de administración de MBAM le permite obtener un archivo de contraseña de propietario de TPM restablecido.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-113">The Key Recovery data system on the MBAM administration website enables you to obtain a reset TPM owner password file.</span></span>

[<span data-ttu-id="cf0dd-114">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="cf0dd-114">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-1.md)

## <span data-ttu-id="cf0dd-115">Recuperar unidades con MBAM</span><span class="sxs-lookup"><span data-stu-id="cf0dd-115">Recover drives with MBAM</span></span>


<span data-ttu-id="cf0dd-116">Asegúrese de que sabe cómo intentar recuperar datos desde unidades cifradas en el caso de que se produzca un error de hardware, cambios en el personal u otras situaciones en las que se pierdan las claves de cifrado.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-116">Make sure that you know how to attempt data recovery from encrypted drives in the event of hardware failure, changes in personnel, or other situations in which encryption keys are lost.</span></span> <span data-ttu-id="cf0dd-117">Las características de recuperación de unidades cifradas de MBAM proporcionan la captura y el almacenamiento de los datos y la disponibilidad de las herramientas necesarias para acceder a un volumen protegido por BitLocker cuando el volumen pasa al modo de recuperación, se mueve o se daña.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-117">The Encrypted Drive Recovery features of MBAM provide the capture and storage of data and availability of tools required to access a BitLocker-protected volume when the volume goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="cf0dd-118">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="cf0dd-118">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[<span data-ttu-id="cf0dd-119">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="cf0dd-119">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-1.md)

[<span data-ttu-id="cf0dd-120">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="cf0dd-120">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-1.md)

## <span data-ttu-id="cf0dd-121">Determinar el estado de cifrado de BitLocker de equipos perdidos con MBAM</span><span class="sxs-lookup"><span data-stu-id="cf0dd-121">Determine BitLocker Encryption State of lost computers by Using MBAM</span></span>


<span data-ttu-id="cf0dd-122">Al usar MBAM, puede determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.</span><span class="sxs-lookup"><span data-stu-id="cf0dd-122">When you use MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="cf0dd-123">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="cf0dd-123">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## <span data-ttu-id="cf0dd-124">Otros recursos para realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="cf0dd-124">Other resources for performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="cf0dd-125">Operaciones para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="cf0dd-125">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





