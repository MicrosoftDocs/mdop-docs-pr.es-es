---
title: Implementación de objetos de directiva de grupo de MBAM 2.0
description: Implementación de objetos de directiva de grupo de MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823491"
---
# <span data-ttu-id="6e1cb-103">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-103">Deploying MBAM 2.0 Group Policy Objects</span></span>


<span data-ttu-id="6e1cb-104">Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero tiene que determinar las directivas de grupo que usará en la implementación de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="6e1cb-105">Consulte [planificación de requisitos de la Directiva de grupo de MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obtener más información sobre las diferentes directivas disponibles.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="6e1cb-106">Cuando haya determinado las directivas que va a usar, deberá crear e implementar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de la Directiva para MBAM mediante la plantilla de directiva de grupo MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-106">When you have determined the policies that you are going to use, you then must create and deploy one or more Group Policy Objects (GPO) that include the policy settings for MBAM by using the MBAM 2.0 Group Policy template.</span></span>

## <span data-ttu-id="6e1cb-107">Instalar la plantilla de directiva de grupo MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-107">Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="6e1cb-108">Además de las características de supervisión y administración de Microsoft BitLocker relacionadas con el servidor, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-108">In addition to the server-related Microsoft BitLocker Administration and Monitoring features, the server setup application includes a MBAM Group Policy template.</span></span> <span data-ttu-id="6e1cb-109">Esta plantilla se puede instalar en cualquier equipo capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="6e1cb-109">This template can be installed on any computer able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="6e1cb-110">Instalación de la plantilla de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-110">How to Install the MBAM 2.0 Group Policy Template</span></span>](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## <span data-ttu-id="6e1cb-111">Implementar la configuración de directiva de grupo de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-111">Deploy MBAM 2.0 Group Policy Settings</span></span>


<span data-ttu-id="6e1cb-112">Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="6e1cb-113">Cómo editar la configuración del GPO de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-113">How to Edit MBAM 2.0 GPO Settings</span></span>](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## <span data-ttu-id="6e1cb-114">Mostrar el panel de control de MBAM en Windows</span><span class="sxs-lookup"><span data-stu-id="6e1cb-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="6e1cb-115">Como MBAM ofrece un panel de control de MBAM personalizado que puede reemplazar el panel de control predeterminado de BitLocker de Windows, también puede elegir ocultar el panel de control predeterminado de BitLocker de los usuarios finales mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="6e1cb-116">Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows</span><span class="sxs-lookup"><span data-stu-id="6e1cb-116">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## <span data-ttu-id="6e1cb-117">Otros recursos para implementar objetos de directiva de grupo de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-117">Other Resources for Deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="6e1cb-118">Implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6e1cb-118">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





