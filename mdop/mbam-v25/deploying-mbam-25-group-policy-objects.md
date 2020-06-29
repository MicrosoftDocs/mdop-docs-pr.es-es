---
title: Implementación de objetos de directiva de grupo de MBAM 2.5
description: Implementación de objetos de directiva de grupo de MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824390"
---
# <span data-ttu-id="4daeb-103">Implementación de objetos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4daeb-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="4daeb-104">Para implementar MBAM, tiene que establecer la configuración de directiva de grupo que define MBAM configuración de implementación para el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4daeb-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="4daeb-105">Para completar esta tarea, debe copiar las plantillas de directiva de grupo MBAM en un servidor o estación de trabajo capaces de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) y, a continuación, editar la configuración.</span><span class="sxs-lookup"><span data-stu-id="4daeb-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="4daeb-106">**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** o MBAM no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="4daeb-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="4daeb-107">Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.</span><span class="sxs-lookup"><span data-stu-id="4daeb-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="4daeb-108">Copia de plantillas de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4daeb-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="4daeb-109">Antes de instalar el cliente de MBAM, debe copiar los objetos de directiva de grupo (GPO) específicos de MBAM en la estación de trabajo de administración.</span><span class="sxs-lookup"><span data-stu-id="4daeb-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="4daeb-110">Estos GPO definen la configuración de implementación de MBAM para el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4daeb-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="4daeb-111">Puede copiar las plantillas de directiva de grupo en cualquier servidor o estación de trabajo que sea un servidor de Windows o un equipo cliente de Windows compatible y que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="4daeb-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="4daeb-112">Copia de plantillas de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4daeb-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="4daeb-113">Editar la configuración de GPO de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="4daeb-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="4daeb-114">Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización.</span><span class="sxs-lookup"><span data-stu-id="4daeb-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="4daeb-115">Para ver y crear GPO, debe tener instalada la consola de administración de directivas de grupo (GPMC) o la administración de directivas de grupo (AGPM) avanzada.</span><span class="sxs-lookup"><span data-stu-id="4daeb-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="4daeb-116">Edición de configuración de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4daeb-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="4daeb-117">Mostrar u ocultar el panel de control de MBAM en el panel de control de Windows</span><span class="sxs-lookup"><span data-stu-id="4daeb-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="4daeb-118">Puesto que MBAM ofrece un panel de control personalizado de MBAM que puede reemplazar el panel de control predeterminado de BitLocker de Windows, también puede elegir mostrar u ocultar el panel de control predeterminado de BitLocker a los usuarios finales mediante la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4daeb-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="4daeb-119">Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="4daeb-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="4daeb-120">Otros recursos para implementar objetos de directiva de grupo de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="4daeb-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="4daeb-121">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4daeb-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="4daeb-122">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="4daeb-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4daeb-123">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4daeb-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4daeb-124">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4daeb-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





