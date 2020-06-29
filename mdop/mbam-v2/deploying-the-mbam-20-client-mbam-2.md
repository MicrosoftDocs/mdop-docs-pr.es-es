---
title: Implementación de cliente de MBAM 2.0
description: Implementación de cliente de MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823450"
---
# <span data-ttu-id="29622-103">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="29622-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="29622-104">El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="29622-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="29622-105">El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de distribución de software electrónico, como servicios de dominio de Active Directory, o bien cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.</span><span class="sxs-lookup"><span data-stu-id="29622-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="29622-106">Según el momento en que implemente el cliente de supervisión y administración de BitLocker de Microsoft, puede habilitar el cifrado de BitLocker en un equipo de su organización antes de que el usuario reciba el equipo o, posteriormente, configurando la Directiva de grupo e implementando el software de cliente de MBAM mediante un sistema de implementación de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="29622-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="29622-107">Implementar el cliente de MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="29622-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="29622-108">Después de configurar la Directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como Microsoft System Center Configuration Manager 2012 o los servicios de dominio de Active Directory para implementar los archivos de Windows Installer de la instalación de cliente MBAM en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="29622-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="29622-109">Puede implementar el cliente con los archivos de 32 bits o 64 bits MbamClientSetup.exe o los archivos de MBAMClient.msi de 32 bits o 64, que se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="29622-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="29622-110">Para obtener más información sobre cómo implementar MBAM objetos de directiva de grupo, consulte [implementar objetos de directiva de grupo de MBAM 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="29622-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="29622-111">Cómo implementar al cliente MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="29622-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="29622-112">Implementar el cliente de MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="29622-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="29622-113">En las organizaciones donde los equipos se reciben y configuran de forma centralizada, puede instalar el cliente de MBAM para administrar el cifrado de BitLocker en cada equipo antes de que se escriban datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="29622-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="29622-114">La ventaja de este proceso es que cada equipo es entonces compatible con el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29622-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="29622-115">Este método no depende de la acción del usuario porque el administrador ya cifró el equipo.</span><span class="sxs-lookup"><span data-stu-id="29622-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="29622-116">Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.</span><span class="sxs-lookup"><span data-stu-id="29622-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="29622-117">Si la Directiva de grupo se ha configurado para requerir un PIN, se les pedirá a los usuarios que configuren un PIN después de que reciban la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="29622-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="29622-118">Cómo implementar al cliente MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="29622-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="29622-119">Cómo usar una línea de comandos para instalar el cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="29622-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="29622-120">En esta sección se explica cómo instalar el cliente de MBAM mediante una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="29622-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="29622-121">Cómo usar una línea de comandos para instalar el cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="29622-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="29622-122">Otros recursos para implementar el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="29622-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="29622-123">Implementación de la planificación de [MBAM 2,0](deploying-mbam-20-mbam-2.md)[para la implementación de cliente de MBAM 2,0](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="29622-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





