---
title: Implementación de cliente de MBAM 2.5
description: Implementación de cliente de MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826280"
---
# <span data-ttu-id="22cf1-103">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22cf1-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="22cf1-104">El software cliente de supervisión y administración de Microsoft BitLocker (MBAM) permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="22cf1-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="22cf1-105">El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de distribución de software electrónico, como servicios de dominio de Active Directory, o bien cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.</span><span class="sxs-lookup"><span data-stu-id="22cf1-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="22cf1-106">Según el momento en que implemente el software cliente de supervisión y administración de BitLocker de Microsoft, puede habilitar el cifrado de unidad BitLocker en un equipo de su organización antes de que el usuario reciba el equipo o posteriormente mediante la configuración de la Directiva de grupo e implementar el software de cliente de MBAM mediante un sistema de implementación de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="22cf1-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="22cf1-107">Implementar el cliente de MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="22cf1-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="22cf1-108">Una vez configurada la configuración de directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como MicrosoftSystemCenter2012 ConfigurationManager o Active Directory Domain Services para implementar los archivos de Windows Installer de instalación del cliente MBAM en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="22cf1-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="22cf1-109">Puede usar los archivos de 32 o 64 bits de MbamClientSetup.exe o los archivos de MBAMClient.msi de 32 bits o 64, que se proporcionan con el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="22cf1-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="22cf1-110">Para obtener más información acerca de la implementación de la configuración de directiva de grupo de MBAM, consulte [implementar objetos de directiva de grupo de MBAM 2,5](deploying-mbam-25-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="22cf1-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="22cf1-111">**Nota:**  A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM.</span><span class="sxs-lookup"><span data-stu-id="22cf1-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="22cf1-112">Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto.</span><span class="sxs-lookup"><span data-stu-id="22cf1-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="22cf1-113">Cómo implementar al cliente MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="22cf1-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="22cf1-114">Implementar el cliente de MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="22cf1-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="22cf1-115">En las organizaciones donde los equipos se reciben y configuran de forma centralizada, puede instalar el cliente MBAM para administrar el cifrado de unidad BitLocker en cada equipo antes de que se escriban datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="22cf1-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="22cf1-116">La ventaja de este proceso es que cada equipo es compatible con el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="22cf1-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="22cf1-117">Este método no depende de la acción del usuario porque el administrador ya cifró el equipo.</span><span class="sxs-lookup"><span data-stu-id="22cf1-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="22cf1-118">Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.</span><span class="sxs-lookup"><span data-stu-id="22cf1-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="22cf1-119">Si la configuración de directiva de grupo se ha configurado para requerir un PIN, se les pedirá a los usuarios que establezcan un PIN después de que reciban la Directiva.</span><span class="sxs-lookup"><span data-stu-id="22cf1-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="22cf1-120">Cómo habilitar BitLocker utilizando MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="22cf1-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="22cf1-121">Cómo implementar el cliente de MBAM mediante una línea de comandos</span><span class="sxs-lookup"><span data-stu-id="22cf1-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="22cf1-122">En esta sección se explica cómo instalar el cliente de MBAM mediante una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="22cf1-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="22cf1-123">Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos</span><span class="sxs-lookup"><span data-stu-id="22cf1-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="22cf1-124">Otros recursos para implementar el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="22cf1-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="22cf1-125">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22cf1-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="22cf1-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22cf1-126">Related topics</span></span>


[<span data-ttu-id="22cf1-127">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22cf1-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="22cf1-128">Planificación para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22cf1-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="22cf1-129">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="22cf1-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="22cf1-130">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="22cf1-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="22cf1-131">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="22cf1-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





