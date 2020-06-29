---
title: Implementación de objetos de directiva de grupo de MBAM 1.0
description: Implementación de objetos de directiva de grupo de MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821220"
---
# <span data-ttu-id="5929b-103">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5929b-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="5929b-104">Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero debe determinar las directivas de grupo que va a usar en la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="5929b-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="5929b-105">Para obtener más información sobre las diversas directivas disponibles, consulte [requisitos de la Directiva de grupo planificación de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5929b-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="5929b-106">Cuando haya determinado las directivas que va a usar, debe usar la plantilla de directiva de grupo MBAM 1,0 para crear e implementar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de directiva de MBAM.</span><span class="sxs-lookup"><span data-stu-id="5929b-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="5929b-107">Instalar la plantilla de directiva de grupo MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5929b-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="5929b-108">Además de ofrecer características relacionadas con el servidor de MBAM, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="5929b-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="5929b-109">Puede instalar esta plantilla en cualquier equipo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="5929b-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="5929b-110">Instalación de la plantilla de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5929b-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="5929b-111">Implementar la configuración de directiva de grupo de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5929b-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="5929b-112">Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización.</span><span class="sxs-lookup"><span data-stu-id="5929b-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="5929b-113">Cambiar la configuración del GPO de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5929b-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="5929b-114">Mostrar el panel de control de MBAM en Windows</span><span class="sxs-lookup"><span data-stu-id="5929b-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="5929b-115">Como MBAM ofrece un panel de control de MBAM personalizado que puede reemplazar el panel de control predeterminado de BitLocker de Windows, también puede elegir ocultar el panel de control predeterminado de BitLocker de los usuarios finales mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5929b-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="5929b-116">Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows</span><span class="sxs-lookup"><span data-stu-id="5929b-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="5929b-117">Otros recursos para implementar objetos de directiva de grupo de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5929b-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="5929b-118">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5929b-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





