---
title: Implementación de cliente de MBAM 1.0
description: Implementación de cliente de MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822901"
---
# <span data-ttu-id="b1b78-103">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="b1b78-103">Deploying the MBAM 1.0 Client</span></span>


<span data-ttu-id="b1b78-104">El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="b1b78-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="b1b78-105">El cliente de BitLocker puede integrarse en una organización implementando el cliente a través de herramientas como Active Directory Domain Services o cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.</span><span class="sxs-lookup"><span data-stu-id="b1b78-105">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="b1b78-106">Según el momento en que implemente el cliente MBAM, puede habilitar el cifrado de BitLocker en un equipo de su organización, ya sea antes o después de que el usuario final reciba el equipo.</span><span class="sxs-lookup"><span data-stu-id="b1b78-106">Depending on when you deploy the MBAM Client, you can enable BitLocker encryption on a computer in your organization either before or after the end user receives the computer.</span></span> <span data-ttu-id="b1b78-107">Para controlar estos intervalos, debe configurar la Directiva de grupo e implementar el software de cliente de MBAM mediante un sistema de implementación de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="b1b78-107">To control this timing, you configure Group Policy and deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="b1b78-108">Puede usar uno de estos métodos o ambos en su organización.</span><span class="sxs-lookup"><span data-stu-id="b1b78-108">You can use either or both of these methods in your organization.</span></span> <span data-ttu-id="b1b78-109">Si usa ambos métodos, puede mejorar la compatibilidad, la elaboración de informes y la compatibilidad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="b1b78-109">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

## <span data-ttu-id="b1b78-110">Implementar el cliente de MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="b1b78-110">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="b1b78-111">Una vez configurada la Directiva de grupo, puede implementar los archivos de Windows Installer de instalación del cliente MBAM en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="b1b78-111">After you have configured Group Policy, you can deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="b1b78-112">Para ello, puede usar un producto de sistema de implementación de software empresarial como Microsoft System Center 2012 Configuration Manager o servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1b78-112">You can do this by use of an enterprise software deployment system product like Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services.</span></span> <span data-ttu-id="b1b78-113">Los dos archivos de Windows Installer de la instalación de cliente de MBAM están MBAMClient-64bit.msi y MBAMClient-32bit.msi.</span><span class="sxs-lookup"><span data-stu-id="b1b78-113">The two available MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi.</span></span> <span data-ttu-id="b1b78-114">Estos archivos se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="b1b78-114">These files are provided with the MBAM software.</span></span> <span data-ttu-id="b1b78-115">Para obtener más información sobre cómo implementar MBAM objetos de directiva de grupo, consulte [implementar objetos de directiva de grupo de MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b1b78-115">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

[<span data-ttu-id="b1b78-116">Cómo implementar al cliente MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="b1b78-116">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## <span data-ttu-id="b1b78-117">Implementar el cliente de MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="b1b78-117">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="b1b78-118">En algunas organizaciones, los nuevos equipos se reciben y configuran de forma centralizada.</span><span class="sxs-lookup"><span data-stu-id="b1b78-118">In some organizations, new computers are received and configured centrally.</span></span> <span data-ttu-id="b1b78-119">Esta situación permite a los administradores instalar el cliente de MBAM para administrar el cifrado de BitLocker en cada equipo antes de que los datos de usuario se escriban en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b1b78-119">This situation enables administrators to install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to the computer.</span></span> <span data-ttu-id="b1b78-120">Este enfoque ayuda a garantizar que los equipos estén correctamente cifrados, ya que el administrador realiza la acción sin depender de la acción del usuario final.</span><span class="sxs-lookup"><span data-stu-id="b1b78-120">This approach helps to ensure that computers are properly encrypted because the administrator performs the action without reliance on end-user action.</span></span> <span data-ttu-id="b1b78-121">Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.</span><span class="sxs-lookup"><span data-stu-id="b1b78-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

[<span data-ttu-id="b1b78-122">Cómo implementar al cliente MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="b1b78-122">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## <span data-ttu-id="b1b78-123">Otros recursos para implementar el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="b1b78-123">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="b1b78-124">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="b1b78-124">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

[<span data-ttu-id="b1b78-125">Planificación para la implementación de clientes de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="b1b78-125">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

 

 





