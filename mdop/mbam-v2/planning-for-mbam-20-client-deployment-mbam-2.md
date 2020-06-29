---
title: Planeación para la implementación de clientes de MBAM 2.0
description: Planeación para la implementación de clientes de MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812622"
---
# <span data-ttu-id="9667e-103">Planeación para la implementación de clientes de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9667e-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="9667e-104">Según el momento en que implemente el cliente de administración y supervisión de Microsoft BitLocker (MBAM), puede habilitar el cifrado de unidad BitLocker en un equipo de su organización, ya sea antes de que el usuario final reciba el equipo o posteriormente.</span><span class="sxs-lookup"><span data-stu-id="9667e-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="9667e-105">Tanto para la MBAM independiente como para las topologías de Configuration Manager, debe configurar la configuración de directiva de grupo para MBAM.</span><span class="sxs-lookup"><span data-stu-id="9667e-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="9667e-106">Si está usando la topología independiente MBAM, le recomendamos que use un sistema de implementación de software empresarial para implementar el software de cliente de MBAM en equipos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="9667e-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="9667e-107">Si implementa MBAM con la topología de Configuration Manager, puede usar Configuration Manager para implementar el software de cliente de MBAM en equipos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="9667e-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="9667e-108">En el administrador de configuración, la instalación de MBAM crea una colección de equipos que MBAM puede administrar.</span><span class="sxs-lookup"><span data-stu-id="9667e-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="9667e-109">Esta colección incluye estaciones de trabajo y dispositivos que no tienen un módulo de plataforma segura (TPM), pero que ejecutan Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9667e-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="9667e-110">**Nota:**  Windows to go no es compatible con las instalaciones integradas de Configuration Manager de MBAM si está usando Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="9667e-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="9667e-111">Implementar el cliente MBAM para habilitar el cifrado de BitLocker después de la distribución de equipos a los usuarios finales</span><span class="sxs-lookup"><span data-stu-id="9667e-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="9667e-112">Después de configurar la Directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como Microsoft System Center Configuration Manager o servicios de dominio de Active Directory (AD DS) para implementar los archivos de Windows Installer de la instalación del cliente de MBAM en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="9667e-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="9667e-113">Para implementar el cliente MBAM, puede usar los archivos de 32 o 64 bits de MbamClientSetup.exe o MBAMClient.msi, que se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="9667e-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="9667e-114">Al implementar el cliente de MBAM después de distribuir los equipos a los equipos cliente, se pide a los usuarios finales que cifren su equipo.</span><span class="sxs-lookup"><span data-stu-id="9667e-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="9667e-115">Esto permite que MBAM recopile los datos, que incluyen el PIN y la contraseña y, a continuación, comenzar el proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="9667e-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="9667e-116">**Nota:**  En este enfoque, se pide a los usuarios que tengan equipos con un chip de TPM activar e inicializar el chip de TPM si el chip no se ha activado previamente.</span><span class="sxs-lookup"><span data-stu-id="9667e-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="9667e-117">Usar el cliente MBAM para habilitar el cifrado de BitLocker antes de la distribución de equipos a usuarios finales</span><span class="sxs-lookup"><span data-stu-id="9667e-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="9667e-118">En las organizaciones donde los equipos se reciben y configuran de forma centralizada y donde los equipos tienen un chip TPM compatible, puede instalar el cliente MBAM para administrar el cifrado de BitLocker en cada equipo antes de que se escriban datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9667e-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="9667e-119">La ventaja de este proceso es que cada equipo será compatible con el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9667e-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="9667e-120">Este método no depende de la acción del usuario porque el administrador ya cifró el equipo.</span><span class="sxs-lookup"><span data-stu-id="9667e-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="9667e-121">Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.</span><span class="sxs-lookup"><span data-stu-id="9667e-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="9667e-122">Si su organización desea usar el chip TPM para cifrar los equipos, el administrador agrega el protector TPM para cifrar el volumen del sistema operativo del equipo.</span><span class="sxs-lookup"><span data-stu-id="9667e-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="9667e-123">Si su organización desea usar el chip de TPM y un protector de PIN, el administrador cifra el volumen del sistema operativo con el protector de TPM y, a continuación, los usuarios seleccionan un PIN cuando inician sesión por primera vez.</span><span class="sxs-lookup"><span data-stu-id="9667e-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="9667e-124">Si su organización decide usar solo el protector del PIN, el administrador no tiene que cifrar el volumen en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="9667e-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="9667e-125">Cuando los usuarios inician sesión, administración y supervisión de Microsoft BitLocker les pide que proporcionen un PIN, o un PIN y una contraseña para usarlos en posteriores reinicios del equipo.</span><span class="sxs-lookup"><span data-stu-id="9667e-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="9667e-126">**Nota:**  La opción de protector TPM requiere que el administrador acepte el indicador de BIOS para activar e inicializar TPM antes de que el equipo se entregue al usuario.</span><span class="sxs-lookup"><span data-stu-id="9667e-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="9667e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9667e-127">Related topics</span></span>


[<span data-ttu-id="9667e-128">Planificación de la implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9667e-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="9667e-129">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9667e-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





