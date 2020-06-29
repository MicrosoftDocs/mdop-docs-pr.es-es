---
title: Planificación para la implementación de clientes de MBAM 1.0
description: Planificación para la implementación de clientes de MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825880"
---
# <span data-ttu-id="945d8-103">Planificación para la implementación de clientes de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="945d8-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="945d8-104">Según el momento en que implemente el cliente de administración y supervisión de Microsoft BitLocker (MBAM), puede habilitar el cifrado de BitLocker en un equipo de su organización, ya sea antes de que el usuario final reciba el equipo o posteriormente.</span><span class="sxs-lookup"><span data-stu-id="945d8-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="945d8-105">Para habilitar el cifrado de BitLocker después de que el usuario final reciba el equipo, configure la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="945d8-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="945d8-106">Para habilitar el cifrado de BitLocker antes de que el usuario final reciba el equipo, implemente el software de cliente de MBAM mediante un sistema de implementación de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="945d8-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="945d8-107">Puede usar uno de los métodos o ambos en su organización.</span><span class="sxs-lookup"><span data-stu-id="945d8-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="945d8-108">Si usa ambos métodos, puede mejorar la compatibilidad, la elaboración de informes y la compatibilidad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="945d8-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="945d8-109">**Nota:**  Para consultar los requisitos del sistema del cliente de MBAM, consulte [configuraciones compatibles con MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="945d8-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="945d8-110">Implementar el cliente MBAM para habilitar el cifrado de BitLocker después de la distribución de equipos a los usuarios finales</span><span class="sxs-lookup"><span data-stu-id="945d8-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="945d8-111">Después de configurar la Directiva de grupo, puede usar un producto de sistema de implementación de software empresarial, como Microsoft System Center Configuration Manager 2012 o servicios de dominio de Active Directory, para implementar los archivos de Windows Installer de la instalación de cliente MBAM en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="945d8-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="945d8-112">Los dos archivos de Windows Installer de la instalación de cliente de MBAM son MBAMClient-64bit.msi y MBAMClient-32bit.msi, que se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="945d8-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="945d8-113">Para obtener más información sobre cómo implementar MBAM objetos de directiva de grupo, consulte [implementar objetos de directiva de grupo de MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="945d8-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="945d8-114">Al implementar el cliente MBAM, después de distribuir los equipos a los usuarios finales, se pide a los usuarios finales que cifren sus equipos.</span><span class="sxs-lookup"><span data-stu-id="945d8-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="945d8-115">Esto le permite a MBAM recopilar los datos, incluir el PIN y la contraseña y, a continuación, comenzar el proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="945d8-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="945d8-116">**Nota:**  En este enfoque, a los usuarios se les pide activar e inicializar el chip módulo de plataforma segura (TPM), si aún no se ha activado.</span><span class="sxs-lookup"><span data-stu-id="945d8-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="945d8-117">Usar el cliente MBAM para habilitar el cifrado de BitLocker antes de la distribución de equipos a usuarios finales</span><span class="sxs-lookup"><span data-stu-id="945d8-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="945d8-118">En las organizaciones donde los equipos se reciben y configuran de forma centralizada, puede instalar el cliente de MBAM para administrar el cifrado de BitLocker en cada equipo antes de que se escriban datos de usuario en él.</span><span class="sxs-lookup"><span data-stu-id="945d8-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="945d8-119">La ventaja de este proceso es que cada equipo será compatible con el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="945d8-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="945d8-120">Este método no depende de la acción del usuario porque el administrador ya cifró el equipo.</span><span class="sxs-lookup"><span data-stu-id="945d8-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="945d8-121">Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.</span><span class="sxs-lookup"><span data-stu-id="945d8-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="945d8-122">Si su organización quiere usar (TPM) para cifrar equipos, el administrador debe cifrar el volumen del sistema operativo del equipo con el protector TPM.</span><span class="sxs-lookup"><span data-stu-id="945d8-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="945d8-123">Si su organización desea usar el chip de TPM y un protector de PIN, el administrador debe cifrar el volumen del sistema con el protector TPM y, a continuación, los usuarios seleccionan un PIN la primera vez que inician sesión.</span><span class="sxs-lookup"><span data-stu-id="945d8-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="945d8-124">Si su organización decide usar solo el protector del PIN, el administrador no tiene que cifrar el volumen en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="945d8-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="945d8-125">Cuando los usuarios inician sesión en sus equipos, MBAM les pide que proporcionen un PIN o un PIN y una contraseña que usarán cuando reinicien su equipo más tarde.</span><span class="sxs-lookup"><span data-stu-id="945d8-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="945d8-126">**Nota:**  La opción de protector del TPM requiere que el administrador acepte el indicador BIOS para activar e inicializar TPM antes de entregar el equipo al usuario.</span><span class="sxs-lookup"><span data-stu-id="945d8-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="945d8-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="945d8-127">Related topics</span></span>


[<span data-ttu-id="945d8-128">Planificar la implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="945d8-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="945d8-129">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="945d8-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





