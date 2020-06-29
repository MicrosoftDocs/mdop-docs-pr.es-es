---
title: Acerca de App-V 5.0 SP2
description: Acerca de App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814990"
---
# <span data-ttu-id="1e48c-103">Acerca de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="1e48c-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="1e48c-104">App-V 5.0 SP2 proporciona una plataforma integrada mejorada, virtualización más flexible y una administración eficaz para aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="1e48c-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="1e48c-105">Para obtener más información, consulte [Descripción general de App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="1e48c-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="1e48c-106">Cambios en la funcionalidad estándar de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="1e48c-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="1e48c-107">Las secciones siguientes contienen información sobre los cambios en la funcionalidad estándar de App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="1e48c-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="1e48c-108">Compatibilidad con Windows Server 2012 R2 y Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="1e48c-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="1e48c-109">App-V 5,0 incluye compatibilidad con Windows Server 2012 R2 y Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="1e48c-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="1e48c-110">App-V 5.0 SP2 ahora admite el redireccionamiento de carpetas para el directorio AppData de roaming del usuario</span><span class="sxs-lookup"><span data-stu-id="1e48c-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="1e48c-111">App-V 5.0 SP2 es compatible con roaming (roaming) AppData (% AppData%) redireccionamiento de carpetas.</span><span class="sxs-lookup"><span data-stu-id="1e48c-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="1e48c-112">Para obtener más información, consulte el [planeamiento para usar la redirección de carpetas con App-V](planning-to-use-folder-redirection-with-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="1e48c-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="1e48c-113">Mejoras de actualización de paquetes y tareas pendientes</span><span class="sxs-lookup"><span data-stu-id="1e48c-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="1e48c-114">En App-V 5.0 SP2, ya no se le pedirá que cierre una aplicación virtual en ejecución cuando se publique una versión más reciente del paquete o grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="1e48c-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="1e48c-115">Si se está usando un paquete o grupo de conexión al intentar realizar una tarea relacionada, aparecerá un mensaje para indicar que el objeto está en uso y que la operación se intentará más adelante.</span><span class="sxs-lookup"><span data-stu-id="1e48c-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="1e48c-116">Las tareas que se hayan puesto en un estado pendiente se realizarán de acuerdo con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="1e48c-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1e48c-117">Tipo de tarea</span><span class="sxs-lookup"><span data-stu-id="1e48c-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="1e48c-118">Regla aplicable</span><span class="sxs-lookup"><span data-stu-id="1e48c-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e48c-119">Tarea basada en el usuario, por ejemplo, publicar un paquete para un usuario</span><span class="sxs-lookup"><span data-stu-id="1e48c-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e48c-120">La tarea pendiente se realizará después de que el usuario cierre sesión y vuelva a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="1e48c-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e48c-121">Tarea basada en todo el mundo, por ejemplo, habilitar globalmente un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="1e48c-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e48c-122">La tarea pendiente se realizará cuando el equipo se cierre y se reinicie.</span><span class="sxs-lookup"><span data-stu-id="1e48c-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1e48c-123">Cuando una tarea se coloca en un estado pendiente, el cliente de App-V también genera una clave del registro para la tarea pendiente de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1e48c-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1e48c-124">Tarea basada en usuarios o en todo el mundo</span><span class="sxs-lookup"><span data-stu-id="1e48c-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="1e48c-125">Dónde se genera la clave del registro</span><span class="sxs-lookup"><span data-stu-id="1e48c-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e48c-126">Tareas basadas en usuarios</span><span class="sxs-lookup"><span data-stu-id="1e48c-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e48c-127">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="1e48c-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e48c-128">Tareas basadas en todo el mundo</span><span class="sxs-lookup"><span data-stu-id="1e48c-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e48c-129">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="1e48c-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1e48c-130">Virtualización de Microsoft Office 2013 y Microsoft Office 2010 con App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1e48c-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="1e48c-131">Use el siguiente vínculo para obtener más información sobre los escenarios admitidos de App-V 5,0 de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="1e48c-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="1e48c-132">Virtualización de Microsoft Office 2013 para virtualización de aplicaciones (App-V) 5.0</span><span class="sxs-lookup"><span data-stu-id="1e48c-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="1e48c-133">**Nota:**  Este documento se centra en la creación de un paquete de Microsoft Office 2013 App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e48c-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="1e48c-134">Sin embargo, también proporciona información sobre escenarios de Microsoft Office 2010 con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e48c-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="1e48c-135">Aplicación de la interfaz de usuario de administración de clientes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1e48c-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="1e48c-136">En versiones anteriores de App-V 5,0, la interfaz de usuario de administración de cliente (UI) se proporcionó con la instalación del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e48c-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="1e48c-137">Con App-V 5.0 SP2 ya no es así.</span><span class="sxs-lookup"><span data-stu-id="1e48c-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="1e48c-138">Ahora, los administradores tienen la opción de implementar la interfaz de usuario del cliente de App-V 5,0 como una aplicación virtual (con todas las configuraciones de implementación de App-V compatibles) o como una aplicación instalada.</span><span class="sxs-lookup"><span data-stu-id="1e48c-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="1e48c-139">Para obtener más información, vea [aplicación de UI Client de Microsoft Application virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="1e48c-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="1e48c-140">Empaquetado y distribución automáticos en paralelo (SxS)</span><span class="sxs-lookup"><span data-stu-id="1e48c-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="1e48c-141">App-V 5.0 SP2 detecta automáticamente los ensamblados en paralelo (SxS) y la implementación en el equipo que ejecuta el cliente de App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="1e48c-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="1e48c-142">Un ensamblado SxS consta principalmente de dependencias en tiempo de ejecución de VC + + o MSXML.</span><span class="sxs-lookup"><span data-stu-id="1e48c-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="1e48c-143">En versiones anteriores de App-V, las aplicaciones virtuales que tenían dependencias en los tiempos de ejecución de VC requerían que estas dependencias estuvieran localmente en el equipo que ejecuta el cliente de App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="1e48c-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="1e48c-144">Ahora se admiten las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="1e48c-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="1e48c-145">El secuenciador de 5,0 de App-V captura automáticamente el ensamblado SxS en el paquete, independientemente de si el tiempo de ejecución de VC ya está instalado en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="1e48c-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="1e48c-146">El cliente App-V 5,0 instala automáticamente el ensamblado SxS requerido en el equipo que ejecuta el cliente según sea necesario en el momento de la publicación.</span><span class="sxs-lookup"><span data-stu-id="1e48c-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="1e48c-147">El secuenciador de 5,0 de App-V informa de la dependencia en tiempo de ejecución de VC mediante el mecanismo de informes del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="1e48c-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="1e48c-148">El secuenciador de 5,0 de App-V ahora le permite excluir la dependencia en tiempo de ejecución de VC en el caso de que la dependencia ya esté disponible en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="1e48c-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="1e48c-149">Mejoras en la actualización de publicaciones</span><span class="sxs-lookup"><span data-stu-id="1e48c-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="1e48c-150">App-V 5,0 permite agregar varias características para mejorar la experiencia general de actualizar un conjunto de aplicaciones para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="1e48c-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="1e48c-151">En la siguiente lista se muestran las mejoras en la actualización de publicaciones:</span><span class="sxs-lookup"><span data-stu-id="1e48c-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="1e48c-152">La siguiente lista contiene más información sobre cómo habilitar las nuevas mejoras en la actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="1e48c-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="1e48c-153">**EnablePublishingRefreshUI** : habilita la barra de progreso de actualización de publicaciones para el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e48c-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="1e48c-154">**HideUI** : oculta la barra de progreso de actualización de publicaciones durante una sincronización manual.</span><span class="sxs-lookup"><span data-stu-id="1e48c-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="1e48c-155">Nueva configuración de cliente</span><span class="sxs-lookup"><span data-stu-id="1e48c-155">New Client Configuration Setting</span></span>

<span data-ttu-id="1e48c-156">La siguiente configuración de cliente nueva está disponible con App-V 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="1e48c-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="1e48c-157">**EnableDynamicVirtualization** : permite virtualizar las extensiones de Shell, los objetos de ayuda del explorador y los controles de Active X compatibles y ejecutar aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="1e48c-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="1e48c-158">Para obtener más información, consulte [acerca de la configuración de cliente](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="1e48c-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="1e48c-159">Extensiones de Shell de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1e48c-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="1e48c-160">App-V 5,0 SP2 ahora es compatible con las extensiones de Shell.</span><span class="sxs-lookup"><span data-stu-id="1e48c-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="1e48c-161">Para obtener más información, consulte la sección compatibilidad de la **extensión Shell de App-v 5.0 SP2** de [creación y administración de aplicaciones virtualizadas de app-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="1e48c-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="1e48c-162">Actualizaciones de la documentación de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1e48c-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="1e48c-163">App-V 5,0 SP2 proporciona documentación actualizada para los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="1e48c-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="1e48c-164">Migrar desde una versión anterior</span><span class="sxs-lookup"><span data-stu-id="1e48c-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="1e48c-165">Acerca de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1e48c-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="1e48c-166">[Acerca de App-V 5,0 Reporting](about-app-v-50-reporting.md) (sección Preguntas más frecuentes)</span><span class="sxs-lookup"><span data-stu-id="1e48c-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="1e48c-167">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="1e48c-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="1e48c-168">App-V 5,0 es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="1e48c-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="1e48c-169">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="1e48c-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="1e48c-170">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="1e48c-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="1e48c-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e48c-171">Related topics</span></span>


[<span data-ttu-id="1e48c-172">Notas de la versión de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="1e48c-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





