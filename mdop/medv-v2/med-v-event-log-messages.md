---
title: Mensajes de registro de eventos de MED-V
description: Mensajes de registro de eventos de MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823080"
---
# <span data-ttu-id="a1db3-103">Mensajes de registro de eventos de MED-V</span><span class="sxs-lookup"><span data-stu-id="a1db3-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="a1db3-104">Los archivos de registro de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 proporcionan información detallada sobre cómo implementar y administrar MED-V en su empresa y ayudar a comprobar la funcionalidad o a solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="a1db3-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="a1db3-105">Identificadores de evento</span><span class="sxs-lookup"><span data-stu-id="a1db3-105">Event IDs</span></span>


<span data-ttu-id="a1db3-106">A continuación se muestra una lista de identificadores de eventos de MED-V para ayudar a solucionar problemas que pueden surgir al implementar o administrar MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="a1db3-107">Generan</span><span class="sxs-lookup"><span data-stu-id="a1db3-107">Fts</span></span>

<span data-ttu-id="a1db3-108">Muestra los identificadores de evento para la configuración de primera vez.</span><span class="sxs-lookup"><span data-stu-id="a1db3-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="a1db3-109">IDENTIFICADOR de evento 3066</span><span class="sxs-lookup"><span data-stu-id="a1db3-109">Event ID 3066</span></span>

<span data-ttu-id="a1db3-110">Error en la operación iniciar máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-111">Description</span></span>**  
<span data-ttu-id="a1db3-112">Existe un posible problema con el disco duro virtual (VHD) que usa para crear un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-113">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-113">Solution</span></span>**  
<span data-ttu-id="a1db3-114">Compruebe que puede crear una máquina virtual con el VHD para MED-V y que se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="a1db3-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="a1db3-115">IDENTIFICADOR de evento 3071</span><span class="sxs-lookup"><span data-stu-id="a1db3-115">Event ID 3071</span></span>

<span data-ttu-id="a1db3-116">Error en la preparación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-117">Description</span></span>**  
<span data-ttu-id="a1db3-118">Se produjo un problema con la configuración por primera vez que puede haber sido causada por muchos problemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="a1db3-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="a1db3-119">Esto incluye problemas con la conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="a1db3-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-120">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-120">Solution</span></span>**  
<span data-ttu-id="a1db3-121">Reinicie el agente de host MED-V para volver a ejecutar la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="a1db3-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="a1db3-122">IDENTIFICADOR de evento 3078</span><span class="sxs-lookup"><span data-stu-id="a1db3-122">Event ID 3078</span></span>

<span data-ttu-id="a1db3-123">Error en la preparación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-124">Description</span></span>**  
<span data-ttu-id="a1db3-125">Existe un posible problema con el VHD que está usando para crear un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-126">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-126">Solution</span></span>**  
<span data-ttu-id="a1db3-127">Compruebe que puede crear una máquina virtual con el VHD para MED-V y que se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="a1db3-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="a1db3-128">IDENTIFICADOR de evento 3079</span><span class="sxs-lookup"><span data-stu-id="a1db3-128">Event ID 3079</span></span>

<span data-ttu-id="a1db3-129">Reintentando la preparación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-130">Description</span></span>**  
<span data-ttu-id="a1db3-131">MED-V está intentando preparar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-132">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-132">Solution</span></span>**  
<span data-ttu-id="a1db3-133">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="a1db3-133">No action is required.</span></span> <span data-ttu-id="a1db3-134">Permitir que finalice la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="a1db3-134">Let first time setup finish.</span></span>

### <span data-ttu-id="a1db3-135">IDENTIFICADOR de evento 3080</span><span class="sxs-lookup"><span data-stu-id="a1db3-135">Event ID 3080</span></span>

<span data-ttu-id="a1db3-136">El cliente se detuvo al preparar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-137">Description</span></span>**  
<span data-ttu-id="a1db3-138">MED-V se detiene de forma inesperada cuando intenta preparar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-139">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-139">Solution</span></span>**  
<span data-ttu-id="a1db3-140">Iniciar el agente de host MED-V y permitir que se complete la configuración por primera vez</span><span class="sxs-lookup"><span data-stu-id="a1db3-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="a1db3-141">IDENTIFICADOR de evento 3084</span><span class="sxs-lookup"><span data-stu-id="a1db3-141">Event ID 3084</span></span>

<span data-ttu-id="a1db3-142">La máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="a1db3-142">Virtual machine is not valid.</span></span> <span data-ttu-id="a1db3-143">Es necesario volver a ejecutar la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="a1db3-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-144">Description</span></span>**  
<span data-ttu-id="a1db3-145">El agente de host MED-V detectó un problema con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-146">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-146">Solution</span></span>**  
<span data-ttu-id="a1db3-147">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="a1db3-147">No action is required.</span></span> <span data-ttu-id="a1db3-148">Permitir que finalice la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="a1db3-148">Let first time setup finish.</span></span>

### <span data-ttu-id="a1db3-149">IDENTIFICADOR de evento 3099</span><span class="sxs-lookup"><span data-stu-id="a1db3-149">Event ID 3099</span></span>

<span data-ttu-id="a1db3-150">Error al llamar a la máquina virtual de inicio.</span><span class="sxs-lookup"><span data-stu-id="a1db3-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-151">Description</span></span>**  
<span data-ttu-id="a1db3-152">Existe un posible problema con el VHD que usas para crear un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-153">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-153">Solution</span></span>**  
<span data-ttu-id="a1db3-154">Compruebe que puede crear una máquina virtual con el VHD para MED-V y que se puede abrir.</span><span class="sxs-lookup"><span data-stu-id="a1db3-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="a1db3-155">Administración de VM</span><span class="sxs-lookup"><span data-stu-id="a1db3-155">VM Management</span></span>

### <span data-ttu-id="a1db3-156">IDENTIFICADOR de evento 4022</span><span class="sxs-lookup"><span data-stu-id="a1db3-156">Event ID 4022</span></span>

<span data-ttu-id="a1db3-157">VMManagerException error grave al emitir el comando a la VM.</span><span class="sxs-lookup"><span data-stu-id="a1db3-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-158">Description</span></span>**  
<span data-ttu-id="a1db3-159">El usuario final ha intentado salir de MED-V cerrando sesión o cerrando el host MED-V y se ha superado la configuración de configuración VMTaskTimeout.</span><span class="sxs-lookup"><span data-stu-id="a1db3-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-160">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-160">Solution</span></span>**  
<span data-ttu-id="a1db3-161">Reinicie MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-161">Restart MED-V.</span></span>

### <span data-ttu-id="a1db3-162">IDENTIFICADOR de evento 4028</span><span class="sxs-lookup"><span data-stu-id="a1db3-162">Event ID 4028</span></span>

<span data-ttu-id="a1db3-163">Se agotó el tiempo de espera de la operación de VM.</span><span class="sxs-lookup"><span data-stu-id="a1db3-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-164">Description</span></span>**  
<span data-ttu-id="a1db3-165">El usuario final intentó salir de MED-V al cerrar sesión o apagar el host, y se superó la configuración de configuración VMTaskTimeout.</span><span class="sxs-lookup"><span data-stu-id="a1db3-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-166">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-166">Solution</span></span>**  
<span data-ttu-id="a1db3-167">Reinicie MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-167">Restart MED-V.</span></span>

### <span data-ttu-id="a1db3-168">IDENTIFICADOR de evento 4038</span><span class="sxs-lookup"><span data-stu-id="a1db3-168">Event ID 4038</span></span>

<span data-ttu-id="a1db3-169">Vmsal publicó un mensaje de error para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a1db3-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-170">Description</span></span>**  
<span data-ttu-id="a1db3-171">Se muestra un mensaje de error al usuario final en el que se indica que MED-V no pudo iniciar la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-172">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-172">Solution</span></span>**  
<span data-ttu-id="a1db3-173">Si el error se registra dos o más veces en una fila, detenga MED-V y conéctese a la máquina virtual con la consola de Virtual PC e intente iniciar la aplicación en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="a1db3-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="a1db3-174">IDENTIFICADOR de evento 4040</span><span class="sxs-lookup"><span data-stu-id="a1db3-174">Event ID 4040</span></span>

<span data-ttu-id="a1db3-175">Las adiciones de reciclaje porque TerminalServices no está inicializado en el invitado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-176">Description</span></span>**  
<span data-ttu-id="a1db3-177">MED-V reinició la máquina virtual porque no se inicializaron los servicios de escritorio remoto en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-178">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-178">Solution</span></span>**  
<span data-ttu-id="a1db3-179">Si el error se registra dos o más veces seguidas, detenga MED-V y conéctese a la máquina virtual mediante la consola de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a1db3-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="a1db3-180">IDENTIFICADOR de evento 4042</span><span class="sxs-lookup"><span data-stu-id="a1db3-180">Event ID 4042</span></span>

<span data-ttu-id="a1db3-181">Error al reciclar adiciones en el invitado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-182">Description</span></span>**  
<span data-ttu-id="a1db3-183">MED-V no pudo reciclar las adiciones de máquina virtual en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-184">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-184">Solution</span></span>**  
<span data-ttu-id="a1db3-185">Si el error se registra dos o más veces seguidas, detenga MED-V y conéctese a la máquina virtual mediante la consola de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a1db3-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="a1db3-186">IDENTIFICADOR de evento 4043</span><span class="sxs-lookup"><span data-stu-id="a1db3-186">Event ID 4043</span></span>

<span data-ttu-id="a1db3-187">Error al restablecer la contraseña expirada en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-188">Description</span></span>**  
<span data-ttu-id="a1db3-189">El usuario final no restableció la contraseña en la máquina virtual antes de que expirara.</span><span class="sxs-lookup"><span data-stu-id="a1db3-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="a1db3-190">Como resultado, es posible que el usuario no pueda obtener acceso a los recursos de red ni guardar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-191">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-191">Solution</span></span>**  
<span data-ttu-id="a1db3-192">Cierre el invitado MED-V y reinícielo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="a1db3-193">Redireccionamiento de URL</span><span class="sxs-lookup"><span data-stu-id="a1db3-193">URL Redirection</span></span>

### <span data-ttu-id="a1db3-194">IDENTIFICADOR de evento 5005</span><span class="sxs-lookup"><span data-stu-id="a1db3-194">Event ID 5005</span></span>

<span data-ttu-id="a1db3-195">No se puede obtener el nombre de la VM de la configuración; no se puede iniciar el explorador invitado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-196">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-196">Description</span></span>**  
<span data-ttu-id="a1db3-197">El redireccionamiento de URL no pudo obtener el nombre del área de trabajo MED-V de la configuración.</span><span class="sxs-lookup"><span data-stu-id="a1db3-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="a1db3-198">Por lo tanto, no puede informar a Windows Virtual PC para que abra la dirección URL redirigida en el explorador de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-199">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-199">Solution</span></span>**  
<span data-ttu-id="a1db3-200">Asegúrese de que el nombre del área de trabajo MED-V está establecido y que coincide con el nombre de una máquina virtual en el directorio C:\\Users\\ de \\Virtual de &lt; *usuario*de &gt; equipos.</span><span class="sxs-lookup"><span data-stu-id="a1db3-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="a1db3-201">El nombre del área de trabajo MED-V se encuentra en HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="a1db3-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="a1db3-202">Por ejemplo, si el usuario es "Matt" y el nombre del área de trabajo es "mattsworkspace", el valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name debe ser "mattsworkspace" y debe haber un archivo denominado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.VCMX.</span><span class="sxs-lookup"><span data-stu-id="a1db3-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="a1db3-203">IDENTIFICADOR de evento 5006</span><span class="sxs-lookup"><span data-stu-id="a1db3-203">Event ID 5006</span></span>

<span data-ttu-id="a1db3-204">Error al crear el servidor de canalización.</span><span class="sxs-lookup"><span data-stu-id="a1db3-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-205">Description</span></span>**  
<span data-ttu-id="a1db3-206">El servicio de redireccionamiento de URL no pudo crear el servidor de canalización para comunicarse con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a1db3-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-207">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-207">Solution</span></span>**  
<span data-ttu-id="a1db3-208">Consulte los registros de eventos del sistema para intentar crear un archivo o recurso cuya ruta de acceso empiece de forma similar a la siguiente: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" y termine con el nombre de usuario y el nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="a1db3-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="a1db3-209">Si no está presente en el registro de eventos, reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="a1db3-210">ConfigMgr (invitado)</span><span class="sxs-lookup"><span data-stu-id="a1db3-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="a1db3-211">IDENTIFICADOR de evento 7001</span><span class="sxs-lookup"><span data-stu-id="a1db3-211">Event ID 7001</span></span>

<span data-ttu-id="a1db3-212">Los datos de configuración de la red de hospedaje no tienen el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="a1db3-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-213">Description</span></span>**  
<span data-ttu-id="a1db3-214">La configuración de red recibida del host es una cadena XML con formato incorrecto o la información de red devuelta del host no se puede escribir en un documento XML.</span><span class="sxs-lookup"><span data-stu-id="a1db3-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-215">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-215">Solution</span></span>**  
<span data-ttu-id="a1db3-216">Reinicie el equipo host y la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="a1db3-217">IDENTIFICADOR de evento 7005</span><span class="sxs-lookup"><span data-stu-id="a1db3-217">Event ID 7005</span></span>

<span data-ttu-id="a1db3-218">Se detectó un cambio en la configuración de la red de hospedaje, pero no se pudo aplicar porque los datos de configuración de la red de hospedaje no tienen el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="a1db3-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-219">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-219">Description</span></span>**  
<span data-ttu-id="a1db3-220">Se comunicó un cambio en la configuración de la red de hospedaje a la máquina virtual, pero no se pudo procesar en la máquina virtual debido a un error.</span><span class="sxs-lookup"><span data-stu-id="a1db3-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="a1db3-221">Este error puede deberse a datos con formato incorrecto o a la incapacidad de establecer la información en la instancia CCMNetworkAdapter de instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a1db3-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-222">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-222">Solution</span></span>**  
<span data-ttu-id="a1db3-223">Reinicie el host y la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="a1db3-224">ConfigMgr (host)</span><span class="sxs-lookup"><span data-stu-id="a1db3-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="a1db3-225">IDENTIFICADOR de evento 8006</span><span class="sxs-lookup"><span data-stu-id="a1db3-225">Event ID 8006</span></span>

<span data-ttu-id="a1db3-226">No se puede encontrar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-227">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-227">Description</span></span>**  
<span data-ttu-id="a1db3-228">Windows Virtual PC 7 no puede ubicar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="a1db3-229">Es posible que la máquina virtual haya sido eliminada, movida, eliminada o que se haya denegado el acceso.</span><span class="sxs-lookup"><span data-stu-id="a1db3-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-230">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-230">Solution</span></span>**  
<span data-ttu-id="a1db3-231">Vuelva a instalar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="a1db3-232">IDENTIFICADOR de evento 8008</span><span class="sxs-lookup"><span data-stu-id="a1db3-232">Event ID 8008</span></span>

<span data-ttu-id="a1db3-233">No se pudo recuperar la información de configuración de red de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-234">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-234">Description</span></span>**  
<span data-ttu-id="a1db3-235">No se pudo recopilar la información de configuración de red del host MED-V, probablemente a causa de un error de llamada del sistema en .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a1db3-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="a1db3-236">Este error también se puede producir si la información de red devuelta desde el host MED-V no se puede escribir en un documento XML.</span><span class="sxs-lookup"><span data-stu-id="a1db3-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-237">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-237">Solution</span></span>**  
<span data-ttu-id="a1db3-238">Reinicie la estación de trabajo host.</span><span class="sxs-lookup"><span data-stu-id="a1db3-238">Restart the host workstation.</span></span>

### <span data-ttu-id="a1db3-239">IDENTIFICADOR de evento 8010</span><span class="sxs-lookup"><span data-stu-id="a1db3-239">Event ID 8010</span></span>

<span data-ttu-id="a1db3-240">No se pudieron establecer los datos de configuración de red en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-241">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-241">Description</span></span>**  
<span data-ttu-id="a1db3-242">La traducción de direcciones hostnetwork (NAT) MED-V no se pudo comunicar a la máquina virtual, probablemente porque la máquina virtual se encuentra en mal estado o no se instalaron o habilitaron las adiciones de Virtual PC de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1db3-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-243">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-243">Solution</span></span>**  
<span data-ttu-id="a1db3-244">Apague y reinicie la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="a1db3-245">Además, es posible que tenga que volver a instalar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="a1db3-246">IDENTIFICADOR de evento 8011</span><span class="sxs-lookup"><span data-stu-id="a1db3-246">Event ID 8011</span></span>

<span data-ttu-id="a1db3-247">No se pudieron restablecer los datos de configuración de red en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-248">Description</span></span>**  
<span data-ttu-id="a1db3-249">La configuración hostnetwork de MED-V (puente) no se pudo comunicar a la máquina virtual, probablemente porque la máquina virtual se encuentra en estado incorrecto o no se instalaron o habilitaron las adiciones de Virtual PC de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1db3-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-250">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-250">Solution</span></span>**  
<span data-ttu-id="a1db3-251">Apague y reinicie la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="a1db3-252">Además, es posible que tenga que volver a instalar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1db3-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="a1db3-253">Redirección de impresora</span><span class="sxs-lookup"><span data-stu-id="a1db3-253">Printer Redirection</span></span>

### <span data-ttu-id="a1db3-254">IDENTIFICADOR de evento 9001</span><span class="sxs-lookup"><span data-stu-id="a1db3-254">Event ID 9001</span></span>

<span data-ttu-id="a1db3-255">Error de permisos de archivo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-256">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-256">Description</span></span>**  
<span data-ttu-id="a1db3-257">El usuario final no tiene autorización para acceder a la carpeta requerida para abrir o crear el archivo de impresora MED-V para leerlo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-258">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-258">Solution</span></span>**  
<span data-ttu-id="a1db3-259">Compruebe que se puede tener acceso a la ruta de User\\AppData\\ y que el usuario tiene permiso para leer y escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="a1db3-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="a1db3-260">Por ejemplo, si el usuario es "Matt", la ruta de acceso C:\\Users\\Matt\\AppData\\ y todos los archivos que contenga deben tener permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="a1db3-261">Y, si existe, la ruta de acceso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ y todos los archivos que allí deberían tener permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="a1db3-262">IDENTIFICADOR de evento 9002</span><span class="sxs-lookup"><span data-stu-id="a1db3-262">Event ID 9002</span></span>

<span data-ttu-id="a1db3-263">Error de permisos de archivo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-264">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-264">Description</span></span>**  
<span data-ttu-id="a1db3-265">El usuario final no tiene autorización para acceder a la carpeta requerida para abrir o crear el archivo de impresora MED-V para escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-266">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-266">Solution</span></span>**  
<span data-ttu-id="a1db3-267">Asegúrese de que se puede acceder a la ruta de User\\AppData\\ y de que el usuario tiene permiso para leer y escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="a1db3-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="a1db3-268">Por ejemplo, si el usuario es "Matt", la ruta de acceso C:\\Users\\Matt\\AppData\\ y todos los archivos que contenga deben tener permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="a1db3-269">Y, si existe, la ruta de acceso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ y todos los archivos que allí deberían tener permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="a1db3-270">IDENTIFICADOR de evento 9004</span><span class="sxs-lookup"><span data-stu-id="a1db3-270">Event ID 9004</span></span>

<span data-ttu-id="a1db3-271">No se puede crear la ruta para almacenar archivos de impresora MEDV.</span><span class="sxs-lookup"><span data-stu-id="a1db3-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-272">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-272">Description</span></span>**  
<span data-ttu-id="a1db3-273">El servicio de redirección de impresoras no pudo acceder a los archivos o crear directorios necesarios para almacenar la información de la impresora.</span><span class="sxs-lookup"><span data-stu-id="a1db3-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-274">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-274">Solution</span></span>**  
<span data-ttu-id="a1db3-275">Compruebe que se puede tener acceso a la ruta de User\\AppData\\ y que el usuario tiene permiso para leer y escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="a1db3-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="a1db3-276">Por ejemplo, si el usuario es "Matt", la ruta de acceso C:\\Users\\Matt\\AppData\\ y todos los archivos que contenga deben tener permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="a1db3-277">Y, si existe, la ruta de acceso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ y todos los archivos que allí deberían tener permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a1db3-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="a1db3-278">IDENTIFICADOR de evento 9005</span><span class="sxs-lookup"><span data-stu-id="a1db3-278">Event ID 9005</span></span>

<span data-ttu-id="a1db3-279">No se puede obtener el nombre de la VM de la configuración; no se puede iniciar el instalador invitado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="a1db3-280">No se puede actualizar MED-V: no se detectó ninguna red de host.</span><span class="sxs-lookup"><span data-stu-id="a1db3-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-281">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-281">Description</span></span>**  
<span data-ttu-id="a1db3-282">El servicio de redirección de impresoras no pudo obtener el nombre del área de trabajo de MED-V de la configuración de MED-V y no puede notificar al equipo virtual de Windows que inicie el instalador en el invitado MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-283">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-283">Solution</span></span>**  
<span data-ttu-id="a1db3-284">Asegúrese de que el nombre del área de trabajo MED-V está establecido y que coincide con el nombre de una máquina virtual en el directorio C:\\Users\\ de \\Virtual de &lt; *usuario*de &gt; equipos.</span><span class="sxs-lookup"><span data-stu-id="a1db3-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="a1db3-285">El nombre del área de trabajo MED-V se encuentra en HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="a1db3-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="a1db3-286">Por ejemplo, si el usuario es "Matt" y el nombre del área de trabajo es "mattsworkspace", el valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name debe ser "mattsworkspace" y debe haber un archivo denominado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.VCMX.</span><span class="sxs-lookup"><span data-stu-id="a1db3-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="a1db3-287">Publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a1db3-287">Application Publishing</span></span>

### <span data-ttu-id="a1db3-288">IDENTIFICADOR de evento 10015</span><span class="sxs-lookup"><span data-stu-id="a1db3-288">Event ID 10015</span></span>

<span data-ttu-id="a1db3-289">Se produjo un error en el sistema de archivos durante el proceso de conciliación.</span><span class="sxs-lookup"><span data-stu-id="a1db3-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="a1db3-290">El proceso de conciliación no procesará el nombre de archivo, &lt; *filename* &gt; pero continuará procesando cualquier otro cambio.</span><span class="sxs-lookup"><span data-stu-id="a1db3-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-291">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-291">Description</span></span>**  
<span data-ttu-id="a1db3-292">Se produjo un error de e/s o de acceso no autorizado al crear o eliminar un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-293">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-293">Solution</span></span>**  
<span data-ttu-id="a1db3-294">Compruebe que se puede tener acceso a la ruta de acceso del archivo y que el usuario tiene permisos para crear o eliminar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="a1db3-295">IDENTIFICADOR de evento 10021</span><span class="sxs-lookup"><span data-stu-id="a1db3-295">Event ID 10021</span></span>

<span data-ttu-id="a1db3-296">Error &lt; *\ _information* &gt; para la operación de operación de archivo &lt; *\ _name* &gt; en el nombre de archivo &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-297">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-297">Description</span></span>**  
<span data-ttu-id="a1db3-298">Se produjo un error de e/s o de acceso no autorizado al crear o eliminar un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-299">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-299">Solution</span></span>**  
<span data-ttu-id="a1db3-300">Compruebe que se puede tener acceso a la ruta de acceso del archivo y que el usuario tiene permisos para crear o eliminar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="a1db3-301">Revisiones de invitados</span><span class="sxs-lookup"><span data-stu-id="a1db3-301">Guest Patching</span></span>

### <span data-ttu-id="a1db3-302">IDENTIFICADOR de evento 11001</span><span class="sxs-lookup"><span data-stu-id="a1db3-302">Event ID 11001</span></span>

<span data-ttu-id="a1db3-303">Mensaje de uso de la tarea de activación del invitado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-304">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-304">Description</span></span>**  
<span data-ttu-id="a1db3-305">MedvHost.exe con la opción/GuestWakeup se ejecutó incorrectamente o el comando no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="a1db3-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-306">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-306">Solution</span></span>**  
<span data-ttu-id="a1db3-307">Asegúrese de que el comando se ejecuta con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="a1db3-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="a1db3-308">Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *Workspace \ _name* &gt; " donde</span><span class="sxs-lookup"><span data-stu-id="a1db3-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="a1db3-309">&lt;*Duration \ _in \ _minutes* &gt; es el número de minutos que la máquina virtual debe permanecer en activo (el valor predeterminado es 240) y</span><span class="sxs-lookup"><span data-stu-id="a1db3-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="a1db3-310">&lt;*área de trabajo \ _name* &gt; es el nombre de la máquina virtual que se debe reactivar.</span><span class="sxs-lookup"><span data-stu-id="a1db3-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="a1db3-311">IDENTIFICADOR de evento 11002</span><span class="sxs-lookup"><span data-stu-id="a1db3-311">Event ID 11002</span></span>

<span data-ttu-id="a1db3-312">No se puede actualizar MED-V: no se detectó ninguna red de host.</span><span class="sxs-lookup"><span data-stu-id="a1db3-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-313">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-313">Description</span></span>**  
<span data-ttu-id="a1db3-314">No se pudo completar la revisión de invitados porque no se detectó ninguna conexión de red de host.</span><span class="sxs-lookup"><span data-stu-id="a1db3-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-315">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-315">Solution</span></span>**  
<span data-ttu-id="a1db3-316">Conecte el host MED-V a una conexión de red activa antes de ejecutar la revisión de invitados.</span><span class="sxs-lookup"><span data-stu-id="a1db3-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="a1db3-317">IDENTIFICADOR de evento 11003</span><span class="sxs-lookup"><span data-stu-id="a1db3-317">Event ID 11003</span></span>

<span data-ttu-id="a1db3-318">No se puede actualizar MED-V – el host no se está ejecutando en el/C powerFailed para crear el servidor de canalización.</span><span class="sxs-lookup"><span data-stu-id="a1db3-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-319">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-319">Description</span></span>**  
<span data-ttu-id="a1db3-320">No se pudo completar la revisión de invitados porque el host parece estar funcionando con batería en lugar de un cable de alimentación.</span><span class="sxs-lookup"><span data-stu-id="a1db3-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-321">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-321">Solution</span></span>**  
<span data-ttu-id="a1db3-322">Conecte el equipo host a un cable de alimentación antes de ejecutar la revisión de invitados.</span><span class="sxs-lookup"><span data-stu-id="a1db3-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="a1db3-323">UX de cliente</span><span class="sxs-lookup"><span data-stu-id="a1db3-323">Client UX</span></span>

### <span data-ttu-id="a1db3-324">IDENTIFICADOR de evento 14003</span><span class="sxs-lookup"><span data-stu-id="a1db3-324">Event ID 14003</span></span>

<span data-ttu-id="a1db3-325">El siguiente mensaje de estado de la bandeja era demasiado largo y no se pudo mostrar: &lt; *bandeja \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="a1db3-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-326">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-326">Description</span></span>**  
<span data-ttu-id="a1db3-327">MED-V creó una cadena inesperada demasiado larga para la información sobre herramientas de la bandeja o el mensaje del globo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="a1db3-328">Como resultado, se truncó el mensaje que se muestra.</span><span class="sxs-lookup"><span data-stu-id="a1db3-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-329">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-329">Solution</span></span>**  
<span data-ttu-id="a1db3-330">Se trata de un error poco frecuente que puede ocurrir cuando MED-V está creando de forma aleatoria el texto de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="a1db3-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="a1db3-331">No hay ninguna solución.</span><span class="sxs-lookup"><span data-stu-id="a1db3-331">There is no solution.</span></span>

### <span data-ttu-id="a1db3-332">IDENTIFICADOR de evento 14004</span><span class="sxs-lookup"><span data-stu-id="a1db3-332">Event ID 14004</span></span>

<span data-ttu-id="a1db3-333">MED-V detenidas debido a una excepción no controlada.</span><span class="sxs-lookup"><span data-stu-id="a1db3-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-334">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-334">Description</span></span>**  
<span data-ttu-id="a1db3-335">Una excepción no controlada hizo que MED-V se detuviera de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="a1db3-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-336">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-336">Solution</span></span>**  
<span data-ttu-id="a1db3-337">Reinicie MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-337">Restart MED-V.</span></span>

### <span data-ttu-id="a1db3-338">IDENTIFICADOR de evento 14005</span><span class="sxs-lookup"><span data-stu-id="a1db3-338">Event ID 14005</span></span>

<span data-ttu-id="a1db3-339">El servidor ha intentado crear una exclusión mutua, pero ya existía.</span><span class="sxs-lookup"><span data-stu-id="a1db3-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-340">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-340">Description</span></span>**  
<span data-ttu-id="a1db3-341">Una segunda instancia de MedvHost.exe se bloquea en la memoria.</span><span class="sxs-lookup"><span data-stu-id="a1db3-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-342">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-342">Solution</span></span>**  
<span data-ttu-id="a1db3-343">Abra TaskManager y finalice todos los procesos de MedvHost.exe.</span><span class="sxs-lookup"><span data-stu-id="a1db3-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="a1db3-344">IDENTIFICADOR de evento 14006</span><span class="sxs-lookup"><span data-stu-id="a1db3-344">Event ID 14006</span></span>

<span data-ttu-id="a1db3-345">Error al modificar o eliminar registro de valores de registro &lt; *\ _value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-346">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-346">Description</span></span>**  
<span data-ttu-id="a1db3-347">MED-V no puede modificar la entrada especificada en el registro.</span><span class="sxs-lookup"><span data-stu-id="a1db3-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-348">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-348">Solution</span></span>**  
<span data-ttu-id="a1db3-349">Asegúrese de instalar o desinstalar MED-V con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="a1db3-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="a1db3-350">IDENTIFICADOR de evento 14007</span><span class="sxs-lookup"><span data-stu-id="a1db3-350">Event ID 14007</span></span>

<span data-ttu-id="a1db3-351">El archivo especificado ( &lt; *filename* &gt; ) no es válido.</span><span class="sxs-lookup"><span data-stu-id="a1db3-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-352">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-352">Description</span></span>**  
<span data-ttu-id="a1db3-353">Durante la instalación o desinstalación, se pasó un archivo temporal dañado al host MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-354">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-354">Solution</span></span>**  
<span data-ttu-id="a1db3-355">Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="a1db3-356">IDENTIFICADOR de evento 14008</span><span class="sxs-lookup"><span data-stu-id="a1db3-356">Event ID 14008</span></span>

<span data-ttu-id="a1db3-357">Archivo no encontrado: &lt; *nombre*de archivo &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-358">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-358">Description</span></span>**  
<span data-ttu-id="a1db3-359">Durante la instalación o desinstalación, no se encontró una ruta de acceso al archivo temporal requerido.</span><span class="sxs-lookup"><span data-stu-id="a1db3-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-360">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-360">Solution</span></span>**  
<span data-ttu-id="a1db3-361">Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="a1db3-362">IDENTIFICADOR de evento 14009</span><span class="sxs-lookup"><span data-stu-id="a1db3-362">Event ID 14009</span></span>

<span data-ttu-id="a1db3-363">No se puede leer el nombre de archivo del parámetro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-364">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-364">Description</span></span>**  
<span data-ttu-id="a1db3-365">Durante el proceso de instalación o desinstalación, MED-V no pudo leer un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="a1db3-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-366">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-366">Solution</span></span>**  
<span data-ttu-id="a1db3-367">Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="a1db3-368">Además, compruebe que el usuario tiene los derechos y permisos necesarios para la carpeta Temp.</span><span class="sxs-lookup"><span data-stu-id="a1db3-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="a1db3-369">IDENTIFICADOR de evento 14010</span><span class="sxs-lookup"><span data-stu-id="a1db3-369">Event ID 14010</span></span>

<span data-ttu-id="a1db3-370">Error al deserializar el nombre de archivo del parámetro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-371">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-371">Description</span></span>**  
<span data-ttu-id="a1db3-372">Durante el proceso de instalación o desinstalación, MED-V encontró un archivo temporal dañado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-373">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-373">Solution</span></span>**  
<span data-ttu-id="a1db3-374">Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="a1db3-375">Además, compruebe que el usuario tiene los derechos y permisos necesarios para la carpeta Temp.</span><span class="sxs-lookup"><span data-stu-id="a1db3-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="a1db3-376">IDENTIFICADOR de evento 14011</span><span class="sxs-lookup"><span data-stu-id="a1db3-376">Event ID 14011</span></span>

<span data-ttu-id="a1db3-377">Error inesperado al deserializar el nombre de archivo del parámetro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-378">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-378">Description</span></span>**  
<span data-ttu-id="a1db3-379">Durante el proceso de instalación o desinstalación, MED-V encontró un archivo temporal dañado.</span><span class="sxs-lookup"><span data-stu-id="a1db3-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-380">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-380">Solution</span></span>**  
<span data-ttu-id="a1db3-381">Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1db3-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="a1db3-382">Además, compruebe que el usuario tiene los derechos y permisos necesarios para la carpeta Temp.</span><span class="sxs-lookup"><span data-stu-id="a1db3-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="a1db3-383">IDENTIFICADOR de evento 14012</span><span class="sxs-lookup"><span data-stu-id="a1db3-383">Event ID 14012</span></span>

<span data-ttu-id="a1db3-384">Error inesperado al configurar los derechos de la &lt; *carpeta \ _name* &gt; de usuario para el nombre de usuario &lt; *username* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1db3-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-385">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-385">Description</span></span>**  
<span data-ttu-id="a1db3-386">Se produce un error cuando MED-V no puede establecer derechos ni permisos en determinadas carpetas durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="a1db3-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-387">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-387">Solution</span></span>**  
<span data-ttu-id="a1db3-388">Compruebe los derechos de administrador en las carpetas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1db3-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="a1db3-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="a1db3-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="a1db3-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="a1db3-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="a1db3-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="a1db3-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="a1db3-392">IDENTIFICADOR de evento 14013</span><span class="sxs-lookup"><span data-stu-id="a1db3-392">Event ID 14013</span></span>

<span data-ttu-id="a1db3-393">Error inesperado al crear el archivo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a1db3-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1db3-394">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1db3-394">Description</span></span>**  
<span data-ttu-id="a1db3-395">Se produce un error cuando MED-V no puede crear un archivo en la carpeta @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="a1db3-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1db3-396">Solución</span><span class="sxs-lookup"><span data-stu-id="a1db3-396">Solution</span></span>**  
<span data-ttu-id="a1db3-397">Compruebe los derechos de administrador en la carpeta MedvLock.</span><span class="sxs-lookup"><span data-stu-id="a1db3-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="a1db3-398">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1db3-398">Related topics</span></span>


[<span data-ttu-id="a1db3-399">Solución de problemas de MED-V</span><span class="sxs-lookup"><span data-stu-id="a1db3-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





