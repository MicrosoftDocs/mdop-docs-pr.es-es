---
title: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
description: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825541"
---
# <span data-ttu-id="6cdb9-103">Cómo implementar al cliente MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="6cdb9-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="6cdb9-104">El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="6cdb9-105">El cliente de MBAM se puede integrar en una organización implementando el cliente a través de herramientas, como servicios de dominio de Active Directory o una herramienta de implementación de software empresarial, como MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="6cdb9-106">**Nota:**  Para consultar los requisitos del sistema del cliente de MBAM, consulte [configuraciones compatibles con MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="6cdb9-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="6cdb9-107">Para implementar el cliente de MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="6cdb9-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="6cdb9-108">Ubique los archivos de instalación del cliente MBAM que se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="6cdb9-109">Implemente el paquete de Windows Installer en equipos de destino con servicios de dominio de Active Directory o una herramienta de implementación de software empresarial, como MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="6cdb9-110">**Nota:**  No debe usar una directiva de grupo para implementar el paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="6cdb9-111">Configure la configuración de distribución o la Directiva de grupo para ejecutar el archivo de instalación del cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="6cdb9-112">Después de una instalación correcta, el cliente de MBAM aplica la configuración de directiva de grupo que se recibe de un controlador de dominio para iniciar las funciones de cifrado y administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="6cdb9-113">Para obtener más información sobre la configuración de directiva de grupo de MBAM, consulte [requisitos de la Directiva de grupo de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6cdb9-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="6cdb9-114">**Importante**  El cliente de MBAM no iniciará las acciones de cifrado de BitLocker si una conexión de protocolo de escritorio remoto está activa.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="6cdb9-115">Todas las conexiones de consola remota deben cerrarse antes de que se inicie el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6cdb9-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="6cdb9-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6cdb9-116">Related topics</span></span>


[<span data-ttu-id="6cdb9-117">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="6cdb9-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





