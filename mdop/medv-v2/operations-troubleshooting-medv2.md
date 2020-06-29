---
title: Solución de problemas de operaciones
description: Solución de problemas de operaciones
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812742"
---
# <span data-ttu-id="1675d-103">Solución de problemas de operaciones</span><span class="sxs-lookup"><span data-stu-id="1675d-103">Operations Troubleshooting</span></span>


<span data-ttu-id="1675d-104">En este tema se incluye información que puede usar para ayudar a solucionar problemas generales operativos en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="1675d-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="1675d-105">Solución de problemas en las operaciones de MED-V</span><span class="sxs-lookup"><span data-stu-id="1675d-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="1675d-106">A continuación se muestran algunos problemas que pueden encontrar los usuarios finales al ejecutar MED-V y soluciones para ayudarle a solucionar estos problemas:</span><span class="sxs-lookup"><span data-stu-id="1675d-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="1675d-107">**Error en el redireccionamiento de documentación**.</span><span class="sxs-lookup"><span data-stu-id="1675d-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="1675d-108">Este problema suele ocurrir cuando la carpeta Mis documentos de un usuario final apunta a una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="1675d-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="1675d-109">Windows no admite la creación de un recurso compartido desde otra carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="1675d-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="1675d-110">Cuando una unidad o una carpeta se redirigen al invitado, RDP\\Windows Virtual PC crea un recurso compartido para esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="1675d-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="1675d-111">Por lo tanto, si la carpeta Mis documentos en el host ya está apuntando a un recurso compartido, RDP\\Windows Virtual PC no puede crear un recurso compartido de un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="1675d-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="1675d-112">Otra causa posible de este problema es que las credenciales necesarias para conectarse al recurso de red sean diferentes de las credenciales del dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="1675d-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="1675d-113">MED-V puede estar detectando que los documentos se redirigen al host, envía esa información al invitado y, a continuación, intenta volver a conectar el recurso de red.</span><span class="sxs-lookup"><span data-stu-id="1675d-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="1675d-114">Si las credenciales del usuario no se autentican, es posible que MED-V deje de intentar autenticar.</span><span class="sxs-lookup"><span data-stu-id="1675d-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="1675d-115">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-115">Solution</span></span>**

<span data-ttu-id="1675d-116">Pruebe una de las siguientes acciones para resolver este problema:</span><span class="sxs-lookup"><span data-stu-id="1675d-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="1675d-117">Establezca el directorio raíz del usuario dentro de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1675d-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="1675d-118">Después, el invitado y el anfitrión deben conectarse al mismo recurso de red.</span><span class="sxs-lookup"><span data-stu-id="1675d-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="1675d-119">En lugar de redirigir la carpeta Mis documentos a una ruta UNC, asígnela a una letra de unidad (en el host, asigne una unidad que apunte al recurso de red).</span><span class="sxs-lookup"><span data-stu-id="1675d-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="1675d-120">Después, la carpeta Mis documentos se puede configurar para que use la letra de unidad en lugar de la ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="1675d-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="1675d-121">El invitado se redirigirá a la misma unidad asignada de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="1675d-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="1675d-122">Cree un script de inicio en el invitado que redirija la carpeta Mis documentos al recurso de red y proporcione las credenciales adicionales según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1675d-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="1675d-123">**Error en el redireccionamiento de URL**.</span><span class="sxs-lookup"><span data-stu-id="1675d-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="1675d-124">Una dirección URL que ha especificado para el redireccionamiento desde el host al invitado no se redirige como se pretende o devuelve un mensaje de error que indica que el sitio web no existe.</span><span class="sxs-lookup"><span data-stu-id="1675d-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="1675d-125">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-125">Solution</span></span>**

<span data-ttu-id="1675d-126">Este error puede producirse cuando hay un uso incorrecto o incorrecto de caracteres, como un asterisco (\ \*), en la información sobre el redireccionamiento de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1675d-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="1675d-127">Compruebe el valor del registro para el redireccionamiento de direcciones URL y corrija los errores.</span><span class="sxs-lookup"><span data-stu-id="1675d-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="1675d-128">La clave del registro se llama `RedirectUrls` y suele encontrarse en:</span><span class="sxs-lookup"><span data-stu-id="1675d-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="1675d-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="1675d-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="1675d-130">**Icono de la barra de tareas que se ha provocado erróneamente**.</span><span class="sxs-lookup"><span data-stu-id="1675d-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="1675d-131">De forma predeterminada, el icono que aparece en la barra de tareas del usuario final para las aplicaciones publicadas y las direcciones URL redirigidas es el icono de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1675d-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="1675d-132">Si un usuario final no reconoce este comportamiento predeterminado, se puede confundir al mirar la barra de tareas para localizar su aplicación.</span><span class="sxs-lookup"><span data-stu-id="1675d-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="1675d-133">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-133">Solution</span></span>**

<span data-ttu-id="1675d-134">La única manera de evitar este comportamiento predeterminado es cambiar la configuración de usuario de las propiedades de la barra de tareas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1675d-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="1675d-135">Haga clic con el botón secundario en la barra de tareas y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="1675d-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="1675d-136">En el cuadro de diálogo Propiedades de la **barra de tareas y el menú Inicio** , haga clic en la pestaña **barra de tareas** .</span><span class="sxs-lookup"><span data-stu-id="1675d-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="1675d-137">En la barra desplegable del cuadro botones de la **barra de tareas** , seleccione no **combinar nunca**.</span><span class="sxs-lookup"><span data-stu-id="1675d-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="1675d-138">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1675d-138">Click **OK**.</span></span>

<span data-ttu-id="1675d-139">Se muestran los iconos esperados para las aplicaciones publicadas y las direcciones URL redirigidas.</span><span class="sxs-lookup"><span data-stu-id="1675d-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="1675d-140">**ADVERTENCIA emitida si el segundo usuario intenta iniciar sesión o si la máquina virtual está en uso**.</span><span class="sxs-lookup"><span data-stu-id="1675d-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="1675d-141">Se emite un mensaje de advertencia cuando un segundo usuario inicia sesión en un área de trabajo de MED-V mientras un primer usuario sigue ejecutando MED-V.</span><span class="sxs-lookup"><span data-stu-id="1675d-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="1675d-142">La advertencia también se emite si se inicia MED-V mientras se usa la máquina virtual, por ejemplo, si la máquina virtual se inició a través de Virtual PC de Windows en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="1675d-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="1675d-143">Cuando el usuario final acepta el mensaje de advertencia, MED-V se cierra.</span><span class="sxs-lookup"><span data-stu-id="1675d-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="1675d-144">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-144">Solution</span></span>**

<span data-ttu-id="1675d-145">Un usuario final debe comprobar que todos los demás usuarios han cerrado la sesión MED-V antes de intentar iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="1675d-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="1675d-146">Esto garantiza que ninguna otra instancia de MED-V se esté ejecutando y que Windows Virtual PC no esté bajo el control de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1675d-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="1675d-147">**Sonidos sonoros leídos durante la configuración de primera vez**.</span><span class="sxs-lookup"><span data-stu-id="1675d-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="1675d-148">En ocasiones, los sonidos se escuchan mientras MED-V se está ejecutando por primera vez.</span><span class="sxs-lookup"><span data-stu-id="1675d-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="1675d-149">Esto puede resultar confuso para un usuario final.</span><span class="sxs-lookup"><span data-stu-id="1675d-149">This can be confusing to an end user.</span></span> <span data-ttu-id="1675d-150">Los pitidos se originan en la máquina virtual cuando realiza determinadas acciones, como, por ejemplo, apagar.</span><span class="sxs-lookup"><span data-stu-id="1675d-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="1675d-151">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-151">Solution</span></span>**

<span data-ttu-id="1675d-152">Puede detener el servicio de pitidos si especifica el comando "net stop beep" al principio de cada secuencia de inicio de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1675d-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="1675d-153">También puede deshabilitar el servicio pitido especificando el comando "SC config beep Start = Disabled".</span><span class="sxs-lookup"><span data-stu-id="1675d-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="1675d-154">Puede especificar estos comandos antes de sellar la imagen o como parte de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="1675d-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="1675d-155">**Varias conexiones de red creadas para áreas de trabajo de MED-V en modo puente**.</span><span class="sxs-lookup"><span data-stu-id="1675d-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="1675d-156">Si la primera configuración está creando un área de trabajo de MED-V que está configurada para el modo NAT, solo crea una única conexión de red en Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1675d-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="1675d-157">Sin embargo, si la primera configuración está creando un área de trabajo de MED-V que está configurada para el modo de puente, crea una conexión de red independiente para cada adaptador de red instalado en el equipo, porque MED-V no puede determinar qué adaptador de red está activo.</span><span class="sxs-lookup"><span data-stu-id="1675d-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="1675d-158">Esto también garantiza que los usuarios móviles siempre dispongan de un adaptador de red disponible para las conexiones cableadas e inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="1675d-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="1675d-159">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-159">Solution</span></span>**

<span data-ttu-id="1675d-160">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1675d-160">None.</span></span>

<span data-ttu-id="1675d-161">**La aplicación MED-V no responde demasiado tiempo al cerrar**.</span><span class="sxs-lookup"><span data-stu-id="1675d-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="1675d-162">En algunos casos, una aplicación de MED-V deja de responder cuando está intentando cerrarse.</span><span class="sxs-lookup"><span data-stu-id="1675d-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="1675d-163">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-163">Solution</span></span>**

<span data-ttu-id="1675d-164">Puede especificar la cantidad de tiempo que esperará MED-V para cerrar las aplicaciones que no responden mediante la configuración de la clave de registro WaitToKillAppTimeout en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="1675d-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="1675d-165">Para obtener más información, consulte [Cómo aumentar el tiempo de apagado para que los procesos puedan cerrarse correctamente en Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="1675d-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="1675d-166">**Al cambiar el nombre de un acceso directo a una aplicación publicada en la máquina virtual invitada, no se cambia el nombre publicado en el host**.</span><span class="sxs-lookup"><span data-stu-id="1675d-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="1675d-167">Al publicar una aplicación mediante la creación de un acceso directo y, a continuación, cambiar el nombre del acceso directo en la máquina virtual invitada, el nombre de la aplicación original permanece en el menú **Inicio** de host.</span><span class="sxs-lookup"><span data-stu-id="1675d-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="1675d-168">El programa continúa ejecutándose según lo esperado, pero el programa siempre conservará el nombre original.</span><span class="sxs-lookup"><span data-stu-id="1675d-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="1675d-169">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-169">Solution</span></span>**

<span data-ttu-id="1675d-170">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1675d-170">None.</span></span> <span data-ttu-id="1675d-171">Este es un comportamiento conocido de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1675d-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="1675d-172">Al **mover un acceso directo en la máquina virtual invitada no se actualiza la ubicación en el menú Inicio del equipo host**.</span><span class="sxs-lookup"><span data-stu-id="1675d-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="1675d-173">Los accesos directos a aplicaciones de MED-V que se publican en el menú **Inicio** del equipo host se catalogan en el registro.</span><span class="sxs-lookup"><span data-stu-id="1675d-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="1675d-174">Si mueve un acceso directo de la aplicación a una subcarpeta, el registro no se actualizará para reflejar el cambio.</span><span class="sxs-lookup"><span data-stu-id="1675d-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="1675d-175">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-175">Solution</span></span>**

<span data-ttu-id="1675d-176">Siga estos pasos para cambiar la ubicación de un acceso directo a la aplicación MED-V:</span><span class="sxs-lookup"><span data-stu-id="1675d-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="1675d-177">Cuando se esté ejecutando MED-V, abra el explorador de Windows en la máquina virtual invitada MED-V.</span><span class="sxs-lookup"><span data-stu-id="1675d-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="1675d-178">Vaya al directorio "%ALLUSERSPROFILE%\\Start Menu\\Programs".</span><span class="sxs-lookup"><span data-stu-id="1675d-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="1675d-179">Mueva los accesos directos de la aplicación fuera de las carpetas StartMenu o programas.</span><span class="sxs-lookup"><span data-stu-id="1675d-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="1675d-180">Después de unos 30 segundos, valide que los métodos abreviados se quitan del menú **Inicio** del equipo host.</span><span class="sxs-lookup"><span data-stu-id="1675d-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="1675d-181">Vuelva a mover los accesos directos de la aplicación a las carpetas del programa nuevo en el directorio Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="1675d-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="1675d-182">Después de unos 30 segundos, valide que los métodos abreviados se actualizan en el menú **Inicio** del equipo host.</span><span class="sxs-lookup"><span data-stu-id="1675d-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="1675d-183">**Las aplicaciones publicadas pueden agotar el tiempo de espera después de sentarse en reposo**.</span><span class="sxs-lookup"><span data-stu-id="1675d-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="1675d-184">En algunos casos, las aplicaciones publicadas agotarán el tiempo de espera si están inactivas durante algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="1675d-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="1675d-185">Esta situación solo se produce si IPsec está habilitado y el área de trabajo MED-V está configurada para el modo NAT.</span><span class="sxs-lookup"><span data-stu-id="1675d-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="1675d-186">Esta situación no se produce si se ejecuta en modo BRIDGEd (puente).</span><span class="sxs-lookup"><span data-stu-id="1675d-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="1675d-187">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-187">Solution</span></span>**

<span data-ttu-id="1675d-188">Deshabilite IPsec cuando ejecute el área de trabajo de MED-V en el modo NAT.</span><span class="sxs-lookup"><span data-stu-id="1675d-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="1675d-189">**Al anclar una aplicación publicada en la barra de tareas, se omite MED-V**.</span><span class="sxs-lookup"><span data-stu-id="1675d-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="1675d-190">Si un usuario final ancla una aplicación publicada a la barra de tareas y, a continuación, cierra MED-V, se pasará por alto la próxima vez que se abra la aplicación desde el icono de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="1675d-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="1675d-191">En su lugar, la aplicación se abre directamente en una ventana de VMSAL.</span><span class="sxs-lookup"><span data-stu-id="1675d-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="1675d-192">Solución</span><span class="sxs-lookup"><span data-stu-id="1675d-192">Solution</span></span>**

<span data-ttu-id="1675d-193">No ancle las aplicaciones publicadas en MED-V a la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="1675d-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="1675d-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1675d-194">Related topics</span></span>


[<span data-ttu-id="1675d-195">Procedimientos recomendados de seguridad para las operaciones de MED-V</span><span class="sxs-lookup"><span data-stu-id="1675d-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="1675d-196">Solución de problemas de implementación</span><span class="sxs-lookup"><span data-stu-id="1675d-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





