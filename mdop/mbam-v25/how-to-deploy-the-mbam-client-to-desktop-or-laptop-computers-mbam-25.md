---
title: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
description: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824480"
---
# <span data-ttu-id="0d717-103">Cómo implementar al cliente MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="0d717-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="0d717-104">En este tema se explica cómo implementar el cliente MBAM en los equipos de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="0d717-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="0d717-105">Puede implementar el cliente de MBAM a través de un sistema electrónico de distribución de software, como servicios de dominio de Active Directory o administrador de MicrosoftSystemCenterConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d717-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="0d717-106">Para implementar el cliente de MBAM como parte de una implementación de Windows, consulte [Cómo habilitar BitLocker con MBAM como parte de una implementación de Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="0d717-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="0d717-107">Antes de iniciar la implementación del cliente de MBAM, revise las [configuraciones admitidas de MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0d717-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="0d717-108">Para implementar el cliente de MBAM en equipos portátiles o de escritorio</span><span class="sxs-lookup"><span data-stu-id="0d717-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="0d717-109">Ubique los archivos de instalación del cliente MBAM que se proporcionan con el software MBAM.</span><span class="sxs-lookup"><span data-stu-id="0d717-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="0d717-110">Use servicios de dominio de Active Directory o una herramienta de implementación de software empresarial como el administrador de MicrosoftSystemCenterConfiguration para implementar el paquete de Windows Installer en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="0d717-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="0d717-111">Establezca la configuración de distribución o la configuración de directiva de grupo para ejecutar el archivo de instalación del cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="0d717-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="0d717-112">Después de una instalación correcta, el cliente de MBAM aplica la configuración de directiva de grupo que se recibe de un controlador de dominio para iniciar el cifrado de unidad BitLocker y las funciones de administración.</span><span class="sxs-lookup"><span data-stu-id="0d717-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="0d717-113">**Importante**  El cliente MBAM no inicia las acciones de cifrado de unidad BitLocker si una conexión de protocolo de escritorio remoto está activa.</span><span class="sxs-lookup"><span data-stu-id="0d717-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="0d717-114">Todas las conexiones de consola remota deben cerrarse y un usuario debe haber iniciado sesión en una sesión de consola física antes de que se inicie el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0d717-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="0d717-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d717-115">Related topics</span></span>
[<span data-ttu-id="0d717-116">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0d717-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="0d717-117">Planificación para la implementación de clientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0d717-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="0d717-118">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="0d717-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0d717-119">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="0d717-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0d717-120">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0d717-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





