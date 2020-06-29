---
title: Administrar las actualizaciones automáticas para áreas de trabajo de MED-V
description: Administrar las actualizaciones automáticas para áreas de trabajo de MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825291"
---
# <span data-ttu-id="e45c8-103">Administrar las actualizaciones automáticas para áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e45c8-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="e45c8-104">El área de trabajo de MED-V es una máquina virtual que contiene un sistema operativo independiente, cuyo proceso de actualización automática de software debe administrarse como los equipos físicos de su empresa.</span><span class="sxs-lookup"><span data-stu-id="e45c8-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="e45c8-105">Dado que el sistema operativo invitado no siempre se ejecuta cuando el sistema operativo del host se está ejecutando, debe asegurarse de que la máquina virtual de MED-V está configurada de tal manera que las actualizaciones de software se pueden aplicar al sistema operativo invitado según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e45c8-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="e45c8-106">La solución de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 proporciona la funcionalidad que le permite determinar cómo se procesan las actualizaciones de software automáticas en un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e45c8-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="e45c8-107">Administración de la Directiva de reactivación del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e45c8-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="e45c8-108">La Directiva de reactivación del área de trabajo de MED-V garantiza que la máquina virtual de MED-V estará disponible para las actualizaciones durante el tiempo que especifique en la configuración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e45c8-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="e45c8-109">Esto se aplica a las actualizaciones publicadas desde Microsoft a través de Windows Update y las actualizaciones implementadas y controladas por soluciones que no son de Microsoft, como las aplicaciones antivirus.</span><span class="sxs-lookup"><span data-stu-id="e45c8-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="e45c8-110">**Importante**  La Directiva de reactivación del área de trabajo de MED-V está optimizada para la infraestructura de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="e45c8-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="e45c8-111">Si usa Microsoft System Center Configuration Manager para implementar actualizaciones que no son de Microsoft, le recomendamos que use también el editor de actualizaciones de System Center, que aprovecha la misma infraestructura que Microsoft Update y, por lo tanto, las ventajas de la Directiva de activación de áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e45c8-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="e45c8-112">Para obtener más información, consulte [System Center updates Publishing](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="e45c8-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="e45c8-113">Al crear el paquete de área de trabajo de MED-V, se ha configurado el y el modo en que se inicia cuando el usuario final inicia sesión (**Inicio rápido**) o cuando el usuario final abre por primera vez una aplicación publicada (**Inicio normal**).</span><span class="sxs-lookup"><span data-stu-id="e45c8-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="e45c8-114">También puedes establecer la opción de permitir que el usuario final controle esta configuración.</span><span class="sxs-lookup"><span data-stu-id="e45c8-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="e45c8-115">De cualquier forma, siempre que se seleccione la opción **Inicio rápido** , la máquina virtual continuará ejecutándose siempre que el host MED-V haya iniciado sesión como usuario.</span><span class="sxs-lookup"><span data-stu-id="e45c8-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="e45c8-116">En esta configuración, dado que MED-V está activo cuando el host está activo, se aplican actualizaciones automáticas sin que sea necesario ningún procesamiento adicional de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e45c8-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="e45c8-117">Sin embargo, para aquellos casos en los que no se especifica el **Inicio rápido** o que la máquina virtual hiberna o detiene, Med-v garantiza la Directiva de reactivación del área de trabajo de Med-v que el sistema operativo invitado se actualiza periódicamente incluso cuando no se usa de forma regular.</span><span class="sxs-lookup"><span data-stu-id="e45c8-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="e45c8-118">MED-V realiza esta función al activar de forma regular la máquina virtual en función de la configuración que especifique.</span><span class="sxs-lookup"><span data-stu-id="e45c8-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="e45c8-119">Esto permite que los clientes de actualizaciones automáticas de la máquina virtual se ejecuten en función de sus configuraciones.</span><span class="sxs-lookup"><span data-stu-id="e45c8-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="e45c8-120">Una vez transcurrido el período de tiempo definido por la configuración de configuración de MED-V, MED-V devuelve la máquina virtual a su estado anterior.</span><span class="sxs-lookup"><span data-stu-id="e45c8-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="e45c8-121">**Nota:**  Si el usuario final abre una aplicación publicada durante el período de actualización, se aplican las actualizaciones necesarias, pero MED-V no se hiberna automáticamente ni se apaga después de que finalice el período de actualización.</span><span class="sxs-lookup"><span data-stu-id="e45c8-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="e45c8-122">En su lugar, MED-V continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="e45c8-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="e45c8-123">La Directiva de reactivación del área de trabajo de MED-V incluye tres componentes principales:</span><span class="sxs-lookup"><span data-stu-id="e45c8-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="e45c8-124">Administrador de actualizaciones de invitados</span><span class="sxs-lookup"><span data-stu-id="e45c8-124">Guest Update Manager</span></span>**

<span data-ttu-id="e45c8-125">En el host MED-V, este programa ejecutable independiente es responsable de activar la máquina virtual según una programación preconfigurada y configurable.</span><span class="sxs-lookup"><span data-stu-id="e45c8-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="e45c8-126">Especificar las opciones de configuración para indicar en qué momento el administrador de actualizaciones debe reactivar la máquina virtual todos los días y cuánto tiempo se debe mantener la máquina virtual activa (en minutos) para permitir la aplicación de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="e45c8-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="e45c8-127">Una vez que se haya alcanzado el número de minutos especificado, el administrador de actualizaciones invitado pondrá la máquina virtual en hibernación, preparada para el siguiente uso.</span><span class="sxs-lookup"><span data-stu-id="e45c8-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="e45c8-128">Puede programar la ejecución de este programa ejecutable a través del administrador de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="e45c8-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="e45c8-129">Servicio de administración de reinicio de invitado</span><span class="sxs-lookup"><span data-stu-id="e45c8-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="e45c8-130">Este servicio reside en el host MED-V y tiene tres responsabilidades principales.</span><span class="sxs-lookup"><span data-stu-id="e45c8-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="e45c8-131">Junto con el administrador de actualizaciones de invitados, administra el reinicio de la máquina virtual cuando el usuario inicia sesión, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e45c8-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="e45c8-132">Detecta cuándo se necesitan los reinicios de máquina virtual causados por las actualizaciones que se instalan.</span><span class="sxs-lookup"><span data-stu-id="e45c8-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="e45c8-133">Además, se asegura de que la tarea del administrador de actualizaciones de invitados se programe siempre de acuerdo con la configuración.</span><span class="sxs-lookup"><span data-stu-id="e45c8-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="e45c8-134">Servicio de actualización de invitado</span><span class="sxs-lookup"><span data-stu-id="e45c8-134">Guest Update Service</span></span>**

<span data-ttu-id="e45c8-135">Este servicio de Windows, que reside en la máquina virtual de MED-V, tiene la responsabilidad de supervisar Cuándo las actualizaciones instaladas requieren que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="e45c8-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="e45c8-136">Después de que el servicio tenga conocimiento de la necesidad de reiniciar, notificará al servicio de administración de reinicios invitados en el host.</span><span class="sxs-lookup"><span data-stu-id="e45c8-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="e45c8-137">Opciones de configuración para la Directiva de reactivación del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e45c8-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="e45c8-138">Usted controla cuándo y durante cuánto tiempo la máquina virtual despierta para recibir actualizaciones automáticas definiendo los dos siguientes valores de configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="e45c8-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="e45c8-139">Ambos valores se encuentran bajo la tecla HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="e45c8-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="e45c8-140">**GuestUpdateTime** : configura la hora y el minuto cada día cuando MED-V debe reactivar la máquina virtual para actualizarla según el estándar de reloj de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="e45c8-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="e45c8-141">Especifique la hora con el formato HH: MM.</span><span class="sxs-lookup"><span data-stu-id="e45c8-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="e45c8-142">El valor predeterminado es 00:00 (medianoche).</span><span class="sxs-lookup"><span data-stu-id="e45c8-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="e45c8-143">**GuestUpdateDuration** : configura el número de minutos que MED-V debe mantener la máquina virtual activa para actualizarse, a partir de la hora especificada en la opción de configuración GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="e45c8-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="e45c8-144">El valor predeterminado es 240 (4 horas).</span><span class="sxs-lookup"><span data-stu-id="e45c8-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="e45c8-145">Si este valor se establece en cero (0), se deshabilita la Directiva de reactivación del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e45c8-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="e45c8-146">Para obtener más información sobre cómo definir los valores de configuración de MED-V, consulte [Managing Med-v Workspace Settings](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e45c8-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="e45c8-147">**Nota:**  Un procedimiento recomendado para MED-V es configurar el intervalo de reactivación de forma que coincida con el momento en que se planea que las máquinas virtuales de MED-V se actualicen con regularidad.</span><span class="sxs-lookup"><span data-stu-id="e45c8-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="e45c8-148">Además, le recomendamos que configure estas opciones de forma que se asemeje al comportamiento del equipo host.</span><span class="sxs-lookup"><span data-stu-id="e45c8-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="e45c8-149">Notificaciones de reinicio con su sistema ESD</span><span class="sxs-lookup"><span data-stu-id="e45c8-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="e45c8-150">Puede configurar su sistema de ESD para que notifique MED-V siempre que se necesite un reinicio para el área de trabajo de MED-V después de aplicar las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="e45c8-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="e45c8-151">Cuando se aplican actualizaciones automáticas a través de un sistema de ESD que sabe que es necesario reiniciar, debe escribir un script para indicar el siguiente evento global en el área de trabajo de MED-V:</span><span class="sxs-lookup"><span data-stu-id="e45c8-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="e45c8-152">**Importante**  Debe abrir el evento con los derechos de modificar solo y, a continuación, señalizarlo.</span><span class="sxs-lookup"><span data-stu-id="e45c8-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="e45c8-153">Si no lo abre con los permisos correctos, no funcionará.</span><span class="sxs-lookup"><span data-stu-id="e45c8-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="e45c8-154">Cuando se señala este evento, MED-V lo captura e informa a la máquina virtual de que se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="e45c8-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="e45c8-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e45c8-155">Related topics</span></span>


[<span data-ttu-id="e45c8-156">Administrar las actualizaciones de Software para áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e45c8-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





