---
title: Planificación para la implementación de clientes de MBAM 2.5
description: Planificación para la implementación de clientes de MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825991"
---
# <span data-ttu-id="8f08a-103">Planificación para la implementación de clientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8f08a-103">Planning for MBAM 2.5 Client Deployment</span></span>


<span data-ttu-id="8f08a-104">Según el momento en que implemente el software de cliente de supervisión y administración de Microsoft BitLocker (MBAM), puede habilitar el cifrado de unidad BitLocker en un equipo de su organización antes de que el usuario final reciba el equipo o posteriormente.</span><span class="sxs-lookup"><span data-stu-id="8f08a-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="8f08a-105">Tanto para la MBAM independiente como para las topologías de integración de System Center Configuration Manager, tiene que establecer la configuración de la Directiva de grupo para MBAM.</span><span class="sxs-lookup"><span data-stu-id="8f08a-105">For both the MBAM Stand-alone and the System Center Configuration Manager Integration topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="8f08a-106">Si está usando la topología independiente MBAM, le recomendamos que use un sistema de implementación de software empresarial para implementar el software de cliente de MBAM en equipos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="8f08a-106">If you are using the MBAM Stand-alone topology, we recommend that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="8f08a-107">Si implementa MBAM con la topología de integración de Configuration Manager, puede usar Configuration Manager para implementar el software de cliente de MBAM en equipos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="8f08a-107">If you deploy MBAM with the Configuration Manager Integration topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="8f08a-108">En el administrador de configuración, la instalación de MBAM crea una colección de equipos que MBAM puede administrar.</span><span class="sxs-lookup"><span data-stu-id="8f08a-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="8f08a-109">Esta colección incluye estaciones de trabajo y dispositivos que no tienen un módulo de plataforma segura (TPM), pero que ejecutan Windows 8, Windows 8,1 o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8f08a-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8, Windows 8.1, or Windows 10.</span></span>

<span data-ttu-id="8f08a-110">**Nota:**  Windows to go no es compatible con la instalación de la topología de integración de Configuration Manager al usar el administrador de configuración 2007.</span><span class="sxs-lookup"><span data-stu-id="8f08a-110">**Note** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="8f08a-111">Implementar el cliente MBAM para habilitar el cifrado de unidad BitLocker después de la distribución de equipos a usuarios finales</span><span class="sxs-lookup"><span data-stu-id="8f08a-111">Deploying the MBAM Client to enable BitLocker Drive Encryption after computer distribution to end users</span></span>


<span data-ttu-id="8f08a-112">Después de configurar la Directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como Microsoft System Center Configuration Manager o servicios de dominio de Active Directory (AD DS) para implementar los archivos de Windows Installer de la instalación del cliente de MBAM en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="8f08a-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="8f08a-113">Para implementar el cliente MBAM, puede usar los archivos de 32 o 64 bits de MbamClientSetup.exe o MBAMClient.msi, que se proporcionan con el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8f08a-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM Client software.</span></span>

<span data-ttu-id="8f08a-114">**Nota:**  A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM.</span><span class="sxs-lookup"><span data-stu-id="8f08a-114">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="8f08a-115">Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto.</span><span class="sxs-lookup"><span data-stu-id="8f08a-115">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

<span data-ttu-id="8f08a-116">Al implementar el cliente de MBAM después de distribuir los equipos a los equipos cliente, se pide a los usuarios finales que cifren su equipo.</span><span class="sxs-lookup"><span data-stu-id="8f08a-116">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="8f08a-117">Esta acción permite que MBAM recopile los datos, lo que incluye el PIN y la contraseña (si lo exige la Directiva) y, a continuación, iniciar el proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8f08a-117">This action enables MBAM to collect the data, which includes the PIN and password (if required by policy), and then to begin the encryption process.</span></span>

<span data-ttu-id="8f08a-118">**Nota:**  En este enfoque, se pide a los usuarios finales que tengan equipos con un chip de TPM activar e inicializar el chip de TPM si el chip no se ha activado previamente.</span><span class="sxs-lookup"><span data-stu-id="8f08a-118">**Note** In this approach, end users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="8f08a-119">Usar el cliente MBAM para habilitar el cifrado de unidad BitLocker antes de la distribución de equipos a usuarios finales</span><span class="sxs-lookup"><span data-stu-id="8f08a-119">Using the MBAM Client to enable BitLocker Drive Encryption before computer distribution to end users</span></span>


<span data-ttu-id="8f08a-120">En las organizaciones donde los equipos se reciban y configuren de forma centralizada y donde los equipos tengan un chip TPM compatible, puede usar el cliente de MBAM para administrar el cifrado de unidad BitLocker en cada equipo antes de que se escriban datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f08a-120">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can use the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="8f08a-121">La ventaja de este proceso es que cada equipo es compatible.</span><span class="sxs-lookup"><span data-stu-id="8f08a-121">The benefit of this process is that every computer is then compliant.</span></span> <span data-ttu-id="8f08a-122">Este método no depende de la acción del usuario final porque el administrador ya cifró el equipo.</span><span class="sxs-lookup"><span data-stu-id="8f08a-122">This method does not rely on end-user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="8f08a-123">Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario final.</span><span class="sxs-lookup"><span data-stu-id="8f08a-123">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the end user.</span></span>

<span data-ttu-id="8f08a-124">Si su organización desea usar el chip TPM para cifrar los equipos, el administrador agrega el protector TPM para cifrar el volumen del sistema operativo del equipo.</span><span class="sxs-lookup"><span data-stu-id="8f08a-124">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="8f08a-125">Si su organización desea usar el chip TPM y un protector con PIN, el administrador cifra el volumen del sistema operativo con el protector TPM y, a continuación, los usuarios finales seleccionan un PIN cuando inician sesión por primera vez.</span><span class="sxs-lookup"><span data-stu-id="8f08a-125">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then end users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="8f08a-126">Si su organización decide usar solo el protector del PIN, el administrador no tiene que cifrar el volumen en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="8f08a-126">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="8f08a-127">Cuando los usuarios finales inicien sesión, la administración y la supervisión de Microsoft BitLocker les pedirá que proporcionen un PIN, o un PIN y una contraseña para usarlos en posteriores reinicios del equipo.</span><span class="sxs-lookup"><span data-stu-id="8f08a-127">When end users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="8f08a-128">**Nota:**  La opción de protector TPM requiere que el administrador acepte el indicador de BIOS para activar e inicializar TPM antes de que el equipo se entregue al usuario final.</span><span class="sxs-lookup"><span data-stu-id="8f08a-128">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the end user.</span></span>

 

## <span data-ttu-id="8f08a-129">Compatibilidad con el cliente de MBAM para unidades de disco duro cifradas</span><span class="sxs-lookup"><span data-stu-id="8f08a-129">MBAM Client support for Encrypted Hard Drives</span></span>


<span data-ttu-id="8f08a-130">MBAM es compatible con BitLocker en unidades de disco duro cifradas que cumplen los requisitos de especificación de TCG para Opal y las normas IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="8f08a-130">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="8f08a-131">Cuando BitLocker está habilitado en estos dispositivos, generará claves y realizará funciones de administración en la unidad cifrada.</span><span class="sxs-lookup"><span data-stu-id="8f08a-131">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="8f08a-132">Para obtener más información, consulta [unidad de disco duro cifrada](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8f08a-132">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>


## <span data-ttu-id="8f08a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f08a-133">Related topics</span></span>


[<span data-ttu-id="8f08a-134">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8f08a-134">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="8f08a-135">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8f08a-135">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="8f08a-136">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="8f08a-136">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8f08a-137">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8f08a-137">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8f08a-138">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8f08a-138">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




