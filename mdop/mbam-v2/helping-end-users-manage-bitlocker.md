---
title: Ayuda a los usuarios finales para administrar BitLocker
description: Ayuda a los usuarios finales para administrar BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824780"
---
# <span data-ttu-id="e65e7-103">Ayuda a los usuarios finales para administrar BitLocker</span><span class="sxs-lookup"><span data-stu-id="e65e7-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="e65e7-104">El contenido de un equipo perdido o robado es vulnerable a acceso no autorizado, que puede presentar un riesgo de seguridad tanto para personas como para empresas.</span><span class="sxs-lookup"><span data-stu-id="e65e7-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="e65e7-105">Administración y supervisión de Microsoft BitLocker (MBAM) usa BitLocker para ayudar a evitar el acceso no autorizado bloqueando el equipo con el fin de proteger los datos confidenciales de usuarios maliciosos.</span><span class="sxs-lookup"><span data-stu-id="e65e7-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="e65e7-106">¿Qué es BitLocker?</span><span class="sxs-lookup"><span data-stu-id="e65e7-106">What is BitLocker?</span></span>


<span data-ttu-id="e65e7-107">El cifrado de unidad BitLocker puede proporcionar protección a las unidades de sistema operativo, unidades de datos y unidades extraíbles (por ejemplo, una unidad USB) mediante el cifrado de las unidades.</span><span class="sxs-lookup"><span data-stu-id="e65e7-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="e65e7-108">Según el modo en que se configure BitLocker, los usuarios pueden tener que proporcionar una clave (una contraseña o PIN) para desbloquear la información almacenada en las unidades cifradas.</span><span class="sxs-lookup"><span data-stu-id="e65e7-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="e65e7-109">Al agregar nuevos archivos a una unidad cifrada con BitLocker, BitLocker los cifra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e65e7-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="e65e7-110">Los archivos permanecen cifrados mientras se almacenan en la unidad cifrada.</span><span class="sxs-lookup"><span data-stu-id="e65e7-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="e65e7-111">Los archivos que se copian a otra unidad o equipo se descifran.</span><span class="sxs-lookup"><span data-stu-id="e65e7-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="e65e7-112">Si comparte archivos con otros usuarios, como a través de una red, estos archivos se cifran y se almacenan en la unidad cifrada, pero los usuarios autorizados pueden obtener acceso a ellos en forma normal.</span><span class="sxs-lookup"><span data-stu-id="e65e7-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="e65e7-113">Si cifra la unidad del sistema operativo, BitLocker comprueba el equipo durante el inicio en busca de condiciones que puedan representar un riesgo de seguridad (por ejemplo, un cambio en el BIOS o en los archivos de inicio).</span><span class="sxs-lookup"><span data-stu-id="e65e7-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="e65e7-114">Si se detecta un riesgo potencial de seguridad, BitLocker bloqueará la unidad del sistema operativo y requerirá una clave de recuperación de BitLocker especial para desbloquearla.</span><span class="sxs-lookup"><span data-stu-id="e65e7-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="e65e7-115">Asegúrese de crear esta clave de recuperación al activar BitLocker por primera vez.</span><span class="sxs-lookup"><span data-stu-id="e65e7-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="e65e7-116">De lo contrario, podrás perder el acceso a tus archivos de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="e65e7-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="e65e7-117">Si cifra las unidades de datos (fijas o extraíbles), puede desbloquear una unidad cifrada con una contraseña o una tarjeta inteligente, o configurar la unidad para que se desbloquee automáticamente cuando inicie sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="e65e7-118">Además de las contraseñas y los pin, BitLocker puede usar el chip módulo de plataforma segura (TPM) que se proporciona en muchos equipos más nuevos.</span><span class="sxs-lookup"><span data-stu-id="e65e7-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="e65e7-119">El chip de TPM se usa para asegurarse de que el equipo no ha sido manipulado antes de que BitLocker desbloquee la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="e65e7-120">Durante el proceso de cifrado, es posible que tenga que habilitar el chip TPM.</span><span class="sxs-lookup"><span data-stu-id="e65e7-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="e65e7-121">Al iniciar el equipo, BitLocker pide a TPM las teclas a la unidad y la desbloquea.</span><span class="sxs-lookup"><span data-stu-id="e65e7-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="e65e7-122">Para habilitar el chip TPM, tendrá que reiniciar el equipo y, a continuación, cambiar una configuración en el BIOS, una capa anterior a Windows del software de su equipo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="e65e7-123">Para obtener más información sobre el TPM, consulte [acerca del chip TPM del equipo](about-the-computer-tpm-chip.md).</span><span class="sxs-lookup"><span data-stu-id="e65e7-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="e65e7-124">Una vez que su equipo esté protegido por BitLocker, es posible que tenga que escribir un PIN o una contraseña cada vez que el equipo se reactive tras la hibernación o el inicio.</span><span class="sxs-lookup"><span data-stu-id="e65e7-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="e65e7-125">El Departamento de soporte técnico de su empresa u organización puede ayudarle si alguna vez olvida su PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="e65e7-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="e65e7-126">Puede desactivar BitLocker, ya sea de forma temporal, al suspenderlo, o de forma permanente, descifrando la unidad.</span><span class="sxs-lookup"><span data-stu-id="e65e7-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="e65e7-127">**Nota:**  Como BitLocker cifra toda la unidad y no solo los archivos individuales, tenga cuidado al mover datos confidenciales entre unidades.</span><span class="sxs-lookup"><span data-stu-id="e65e7-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="e65e7-128">Si mueve un archivo de una unidad protegida con BitLocker a una unidad no cifrada, el archivo ya no se cifrará.</span><span class="sxs-lookup"><span data-stu-id="e65e7-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="e65e7-129">Acerca de la aplicación de opciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="e65e7-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="e65e7-130">Para desbloquear las unidades de disco duro de su equipo y administrar el PIN y las contraseñas, use la aplicación de opciones de cifrado de BitLocker en el panel de control de Windows siguiendo el procedimiento que se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="e65e7-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="e65e7-131">Puede escribir contraseñas para desbloquear unidades protegidas y puede comprobar el estado de BitLocker de las unidades conectadas mediante esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e65e7-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="e65e7-132">Para abrir la aplicación de opciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="e65e7-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="e65e7-133">Haga clic en **Inicio**y seleccione **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="e65e7-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="e65e7-134">El panel de control se abre en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="e65e7-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="e65e7-135">En el **Panel de control**, seleccione **sistema y seguridad**.</span><span class="sxs-lookup"><span data-stu-id="e65e7-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="e65e7-136">Seleccione **Opciones de cifrado de BitLocker** para abrir la aplicación de opciones de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e65e7-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="e65e7-137">Para obtener una descripción de las opciones disponibles, consulte la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="e65e7-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="e65e7-138">Opciones de la aplicación de opciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="e65e7-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="e65e7-139">La aplicación de opciones de cifrado de BitLocker del panel de control le permite administrar el PIN y las contraseñas, que BitLocker usa para proteger el equipo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="e65e7-140">Cifrado de unidad BitLocker: unidades de disco fijo:</span><span class="sxs-lookup"><span data-stu-id="e65e7-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="e65e7-141">En esta sección, puede ver información sobre las unidades de disco duro conectadas a su equipo y su estado de cifrado actual de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e65e7-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="e65e7-142">**Administrar su PIN** : cambia el PIN usado por BitLocker para desbloquear la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="e65e7-143">**Administrar la contraseña** : cambia la contraseña que usa BitLocker para desbloquear las otras unidades internas.</span><span class="sxs-lookup"><span data-stu-id="e65e7-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="e65e7-144">Cifrado de unidad BitLocker: unidades externas:</span><span class="sxs-lookup"><span data-stu-id="e65e7-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="e65e7-145">En esta sección, puede ver información sobre las unidades externas (como una unidad USB) conectada a su equipo y su estado actual de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e65e7-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="e65e7-146">**Administrar la contraseña** : cambia la contraseña que usa BitLocker para desbloquear las otras unidades internas.</span><span class="sxs-lookup"><span data-stu-id="e65e7-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="e65e7-147">Expertos</span><span class="sxs-lookup"><span data-stu-id="e65e7-147">Advanced:</span></span>**

-   <span data-ttu-id="e65e7-148">**Administración de TPM** : abre la herramienta de administración de TPM en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="e65e7-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="e65e7-149">Desde aquí puede configurar tareas comunes de TPM y obtener información sobre el conjunto de chips de TPM.</span><span class="sxs-lookup"><span data-stu-id="e65e7-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="e65e7-150">Para tener acceso a esta herramienta, debe tener permisos administrativos en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="e65e7-151">**Administración de discos** : Abra la herramienta Administración de discos.</span><span class="sxs-lookup"><span data-stu-id="e65e7-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="e65e7-152">Desde aquí puede ver la información de todos los discos duros conectados al equipo y configurar las particiones y las opciones de unidad.</span><span class="sxs-lookup"><span data-stu-id="e65e7-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="e65e7-153">Para obtener acceso a esta herramienta, debe tener derechos administrativos en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e65e7-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





