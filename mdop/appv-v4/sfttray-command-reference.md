---
title: Referencia de comandos SFTTRAY
description: Referencia de comandos SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815351"
---
# <span data-ttu-id="dc745-103">Referencia de comandos SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="dc745-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="dc745-104">La aplicación de bandeja del cliente de Microsoft Application Virtualization (App-V), sfttray.exe, es el elemento principal de la interfaz de usuario del cliente de App-V con el que los usuarios interactuarán durante el uso normal.</span><span class="sxs-lookup"><span data-stu-id="dc745-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="dc745-105">Este programa controla la transmisión e inicia todas las aplicaciones virtuales y se accede a ellas haciendo clic con el botón secundario del ratón en el icono que aparece en el área de notificación para mostrar el menú de funciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="dc745-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="dc745-106">El menú permite al usuario cargar aplicaciones, iniciar una actualización de publicaciones, cancelar una solicitud o cambiar el cliente a modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dc745-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="dc745-107">El usuario también puede cerrar la aplicación de la bandeja del cliente de virtualización de aplicaciones y todas las aplicaciones activas haciendo clic en **salir**.</span><span class="sxs-lookup"><span data-stu-id="dc745-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="dc745-108">De forma predeterminada, el icono se muestra siempre que se inicia una aplicación virtual, aunque se puede controlar mediante comandos de SFTTRAY.</span><span class="sxs-lookup"><span data-stu-id="dc745-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="dc745-109">La aplicación de la bandeja del cliente de virtualización de Applications también muestra una barra de progreso para cada aplicación que se inicia, así como mensajes de estado sobre las aplicaciones activas.</span><span class="sxs-lookup"><span data-stu-id="dc745-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="dc745-110">Al hacer clic en la barra de progreso se muestra un mensaje que le permite cancelar la carga o el inicio de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc745-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="dc745-111">Comandos de SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="dc745-111">SFTTRAY Commands</span></span>


<span data-ttu-id="dc745-112">La lista de comandos y modificadores de línea de comandos se puede mostrar ejecutando el siguiente comando desde una ventana de comandos.</span><span class="sxs-lookup"><span data-stu-id="dc745-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="dc745-113">Nota</span><span class="sxs-lookup"><span data-stu-id="dc745-113">Note</span></span>**  
<span data-ttu-id="dc745-114">Solo hay una instancia de bandeja del cliente de virtualización de aplicaciones para cada contexto de usuario, por lo que si inicia un nuevo comando SFTTRAY, se pasará al programa que ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="dc745-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="dc745-115">Uso del comando</span><span class="sxs-lookup"><span data-stu-id="dc745-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="dc745-116">Modificadores de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="dc745-116">Command-Line Switches</span></span>

<span data-ttu-id="dc745-117">Los modificadores de la línea de comandos de SFTTRAY se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc745-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc745-118">Conmutador</span><span class="sxs-lookup"><span data-stu-id="dc745-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="dc745-119">descripción</span><span class="sxs-lookup"><span data-stu-id="dc745-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc745-120">/HIDE</span><span class="sxs-lookup"><span data-stu-id="dc745-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-121">Oculta el icono SFTTRAY en el área de notificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc745-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc745-122">/SHOW</span><span class="sxs-lookup"><span data-stu-id="dc745-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-123">Muestra el icono SFTTRAY en el área de notificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc745-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc745-124">/QUIET</span><span class="sxs-lookup"><span data-stu-id="dc745-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-125">Es compatible con el uso desatendido evitando que se muestren cuadros de mensaje que requieran confirmación de usuario.</span><span class="sxs-lookup"><span data-stu-id="dc745-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc745-126">/EXE &lt; Alt-exe&gt;</span><span class="sxs-lookup"><span data-stu-id="dc745-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-127">Se usa con/LAUNCH para especificar que un programa ejecutable debe iniciarse en el entorno virtual cuando se inicia una aplicación virtual en lugar del archivo de destino especificado en el OSD.</span><span class="sxs-lookup"><span data-stu-id="dc745-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dc745-128">Nota</span><span class="sxs-lookup"><span data-stu-id="dc745-128">Note</span></span></strong><br/><p><span data-ttu-id="dc745-129">Por ejemplo, use "SFTTRAY.EXE/EXE REGEDIT.EXE &lt; aplicación/Launch &gt; " para poder examinar el registro del entorno virtual en el que se está ejecutando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc745-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc745-130">&lt;Aplicación/Launch &gt; [ &lt; args &gt; ]</span><span class="sxs-lookup"><span data-stu-id="dc745-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-131">Inicia una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="dc745-131">Starts a virtual application.</span></span> <span data-ttu-id="dc745-132">Especifique el nombre y la versión de una aplicación o la ruta de acceso a un archivo OSD.</span><span class="sxs-lookup"><span data-stu-id="dc745-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="dc745-133">Opcionalmente, los argumentos de la línea de comandos se pueden pasar a la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="dc745-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dc745-134">Nota</span><span class="sxs-lookup"><span data-stu-id="dc745-134">Note</span></span></strong><br/><p><span data-ttu-id="dc745-135">Use el comando "SFTMIME.EXE/QUERY OBJ: APP/SHORT" para obtener una lista de los nombres y las versiones de las aplicaciones virtuales disponibles.</span><span class="sxs-lookup"><span data-stu-id="dc745-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc745-136">/LOAD</span><span class="sxs-lookup"><span data-stu-id="dc745-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-137">Carga o importa una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="dc745-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc745-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="dc745-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-139">Carga todas las aplicaciones en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="dc745-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc745-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="dc745-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-141">Inicia una actualización de publicación para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dc745-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc745-142">&lt;identificador exclusivo de/LAUNCHRESULT&gt;</span><span class="sxs-lookup"><span data-stu-id="dc745-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-143">Devuelve el código de resultado de inicio del proceso que inicia sfttray.exe mediante un evento global y un archivo asignado en memoria que se basan en el nombre de raíz especificado para el identificador único. ¹</span><span class="sxs-lookup"><span data-stu-id="dc745-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc745-144">/SFTFILE &lt; SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="dc745-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-145">Modificador opcional usado con/LOAD para especificar la ruta de acceso al archivo SFT de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc745-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="dc745-146">Si se especifica, la aplicación se importa en lugar de cargarse.</span><span class="sxs-lookup"><span data-stu-id="dc745-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc745-147">/EXIT</span><span class="sxs-lookup"><span data-stu-id="dc745-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc745-148">Cierra el programa SFTTRAY y todas las aplicaciones virtuales activas y quita el icono del área de notificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc745-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="dc745-149">Nota</span><span class="sxs-lookup"><span data-stu-id="dc745-149">Note</span></span>**  
<span data-ttu-id="dc745-150">¹ el parámetro de la línea de comandos */LAUNCHRESULT* proporciona un medio para el proceso que inicia sfttray.exe para especificar el nombre de raíz de un evento global y un archivo asignado en memoria que se usan para devolver el código de resultado de inicio al proceso.</span><span class="sxs-lookup"><span data-stu-id="dc745-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="dc745-151">El nombre del identificador único debe comenzar con "SFT-" para evitar que el nombre del evento se obtenga virtualmente cuando el proceso de inicio se invoca en un entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="dc745-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="dc745-152">La región asignada de memoria tendrá un tamaño de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dc745-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="dc745-153">Para usar este parámetro, el proceso de inicio crea un evento con el nombre " &lt; identificador exclusivo &gt; -resultado \ _Event", un archivo asignado a la memoria con el nombre "identificador exclusivo- &lt; &gt; resultado \ _value" y, opcionalmente, un evento con el nombre " &lt; identificador exclusivo &gt; -apagado \ _Event" y, a continuación, se inicia el proceso de inicio sfttray.exe y espera que se Señalice el evento.</span><span class="sxs-lookup"><span data-stu-id="dc745-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="dc745-154">Una vez señalizado el evento " &lt; identificador exclusivo &gt; : resultado \ _Event", el proceso de inicio recupera el código devuelto de 64 bits de la región asignada en memoria.</span><span class="sxs-lookup"><span data-stu-id="dc745-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="dc745-155">Si existe el evento opcional " &lt; identificador exclusivo &gt; -apagado \ _Event" cuando se cierra la aplicación virtual, sfttray.exe abre e indica el evento.</span><span class="sxs-lookup"><span data-stu-id="dc745-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="dc745-156">El proceso de inicio espera en este evento Shutdown si necesita determinar cuándo se cierra la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="dc745-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











