---
title: Visualización y configuración de los registros de MED-V
description: Visualización y configuración de los registros de MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823730"
---
# <span data-ttu-id="04a92-103">Visualización y configuración de los registros de MED-V</span><span class="sxs-lookup"><span data-stu-id="04a92-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="04a92-104">Cuando está solucionando problemas y problemas de MED-V, puede que le resulte útil o necesario acceder a los registros de eventos de MED-V.</span><span class="sxs-lookup"><span data-stu-id="04a92-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="04a92-105">Puede abrir el visor de eventos para el equipo host y la máquina virtual invitada con el kit de herramientas de administración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="04a92-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="04a92-106">También puede usar el kit de herramientas de administración de MED-V para establecer el nivel de registro en el que los eventos MED-V registran informes de eventos MED-V.</span><span class="sxs-lookup"><span data-stu-id="04a92-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="04a92-107">Para obtener información sobre cómo abrir el kit de herramientas de administración de MED-V, consulte [solución de problemas de Med-v mediante el kit de herramientas de administración](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="04a92-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="04a92-108">Ver registros de eventos de MED-V</span><span class="sxs-lookup"><span data-stu-id="04a92-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="04a92-109">En la ventana del **Kit de herramientas de administración de MED-V** , haga clic en **eventos de host** para abrir el visor de eventos del equipo host.</span><span class="sxs-lookup"><span data-stu-id="04a92-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="04a92-110">O bien, haga clic en **eventos de invitado** para abrir el visor de eventos para la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="04a92-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="04a92-111">El visor de eventos se abre y muestra los registros de eventos correspondientes que puede usar para solucionar los problemas que pueden surgir al implementar o administrar MED-V.</span><span class="sxs-lookup"><span data-stu-id="04a92-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="04a92-112">De forma predeterminada, solo se muestran los errores y las advertencias.</span><span class="sxs-lookup"><span data-stu-id="04a92-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="04a92-113">Para obtener más información sobre los identificadores de eventos y mensajes específicos, vea [mensajes de registro de eventos de MED-V](med-v-event-log-messages.md).</span><span class="sxs-lookup"><span data-stu-id="04a92-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="04a92-114">**Nota:**  Los usuarios finales solo pueden guardar archivos de registro de eventos en el invitado si tienen permisos administrativos.</span><span class="sxs-lookup"><span data-stu-id="04a92-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="04a92-115">Para abrir manualmente el visor de eventos en el equipo host</span><span class="sxs-lookup"><span data-stu-id="04a92-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="04a92-116">Haga clic en **Inicio**, seleccione **Panel de control**y, a continuación, haga clic en **herramientas administrativas**.</span><span class="sxs-lookup"><span data-stu-id="04a92-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="04a92-117">Haga doble clic en **visor de eventos**y, a continuación, haga clic en **registros de aplicaciones y servicios**.</span><span class="sxs-lookup"><span data-stu-id="04a92-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="04a92-118">Haga doble clic en **MEDV**.</span><span class="sxs-lookup"><span data-stu-id="04a92-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="04a92-119">Configuración de registros de eventos de MED-V</span><span class="sxs-lookup"><span data-stu-id="04a92-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="04a92-120">Puede especificar el nivel de registro de eventos de MED-V seleccionando el botón de opción correspondiente en el kit de herramientas de administración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="04a92-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="04a92-121">Puede decidir si el registro de eventos incluye solo errores, errores y advertencias, o errores, advertencias y mensajes informativos.</span><span class="sxs-lookup"><span data-stu-id="04a92-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="04a92-122">El nivel de registro de eventos especificado se establece tanto en el equipo host como en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="04a92-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="04a92-123">También puede especificar el nivel de registro de eventos editando el valor de registro EventLogLevel.</span><span class="sxs-lookup"><span data-stu-id="04a92-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="04a92-124">Para obtener más información, vea Administración de las [Opciones de configuración del área de trabajo de MED-V](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="04a92-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="04a92-125">**Nota:**  El nivel que especifique en la ventana del **Kit de herramientas de administración de Med-v** se aplicará al registro de eventos de Med-v en el futuro.</span><span class="sxs-lookup"><span data-stu-id="04a92-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="04a92-126">Si establece el nivel para capturar todos los errores, advertencias y mensajes informativos, los registros de eventos se eliminarán más rápidamente y los eventos anteriores se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="04a92-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="04a92-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04a92-127">Related topics</span></span>


[<span data-ttu-id="04a92-128">Reinicio y restablecimiento de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="04a92-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="04a92-129">Visualización de las configuraciones del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="04a92-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





