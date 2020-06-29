---
title: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
description: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813007"
---
# <span data-ttu-id="fbd32-103">Cómo implementar al cliente MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="fbd32-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="fbd32-104">El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="fbd32-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="fbd32-105">El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema electrónico de distribución de software, como servicios de dominio de Active Directory o MicrosoftSystemCenterConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="fbd32-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="fbd32-106">**Nota:**  Para revisar los requisitos del sistema cliente de administración y supervisión de Microsoft BitLocker, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="fbd32-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="fbd32-107">Para implementar el cliente de MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="fbd32-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="fbd32-108">Ubique los archivos de instalación del cliente MBAM que se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="fbd32-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="fbd32-109">Use servicios de dominio de Active Directory o una herramienta de implementación de software empresarial como MicrosoftSystemCenterConfigurationManager para implementar el paquete de Windows Installer en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="fbd32-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="fbd32-110">Configure la configuración de distribución o la Directiva de grupo para ejecutar el archivo de instalación del cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="fbd32-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="fbd32-111">Después de una instalación correcta, el cliente de MBAM aplica la configuración de directiva de grupo que se recibe de un controlador de dominio para iniciar las funciones de cifrado y administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fbd32-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="fbd32-112">Para obtener más información sobre la configuración de directiva de grupo de MBAM, consulte [requisitos de la Directiva de grupo de MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="fbd32-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="fbd32-113">**Importante**  El cliente de MBAM no iniciará las acciones de cifrado de BitLocker si una conexión de protocolo de escritorio remoto está activa.</span><span class="sxs-lookup"><span data-stu-id="fbd32-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="fbd32-114">Todas las conexiones de consola remota deben cerrarse antes de que se inicie el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fbd32-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="fbd32-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbd32-115">Related topics</span></span>


[<span data-ttu-id="fbd32-116">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="fbd32-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





