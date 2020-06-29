---
title: Solución de problemas de MED-V
description: Solución de problemas de MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825861"
---
# <span data-ttu-id="5f212-103">Solución de problemas de MED-V</span><span class="sxs-lookup"><span data-stu-id="5f212-103">Troubleshooting MED-V</span></span>


<span data-ttu-id="5f212-104">Esta sección proporciona información para ayudar a solucionar problemas generales con la virtualización de escritorio de Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="5f212-104">This section provides information to help troubleshoot general issues with Microsoft Enterprise Desktop Virtualization (MED-V).</span></span>

## <span data-ttu-id="5f212-105">Cambiar la resolución del host y, a continuación, maximizar el área de trabajo de MED-V hace que el escritorio aparezca en negro</span><span class="sxs-lookup"><span data-stu-id="5f212-105">Changing the host resolution and then maximizing the MED-V workspace causes the desktop to appear black</span></span>


<span data-ttu-id="5f212-106">Al trabajar en el modo de escritorio completo, si cambia la resolución del host y, a continuación, maximiza la ventana del área de trabajo de MED-V, el escritorio aparecerá en negro y el área de trabajo de MED-V podría no responder.</span><span class="sxs-lookup"><span data-stu-id="5f212-106">When working in full desktop mode, if you change the host resolution and then maximize the MED-V workspace window, the desktop appears black and the MED-V workspace might not respond.</span></span>

### <span data-ttu-id="5f212-107">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-107">Solution</span></span>

<span data-ttu-id="5f212-108">Detenga y, a continuación, inicie el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-108">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="5f212-109">Iniciar un área de trabajo de MED-V con un adaptador de red deshabilitado y, posteriormente, habilitar el adaptador no restaura la conectividad de red</span><span class="sxs-lookup"><span data-stu-id="5f212-109">Starting a MED-V workspace with a network adapter disabled and then later enabling the adapter does not restore network connectivity</span></span>


<span data-ttu-id="5f212-110">Si configura un área de trabajo de MED-V en modo puente y, a continuación, inicia el área de trabajo de MED-V mientras un adaptador de red está deshabilitado, si el adaptador está habilitado posteriormente, no se restaurará la conectividad de red a través de ese adaptador.</span><span class="sxs-lookup"><span data-stu-id="5f212-110">If you configure a MED-V workspace in bridge mode and then start the MED-V workspace while a network adapter is disabled, if the adapter is later enabled, the network connectivity through that adapter is not restored.</span></span>

### <span data-ttu-id="5f212-111">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-111">Solution</span></span>

<span data-ttu-id="5f212-112">Detenga y, a continuación, inicie el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-112">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="5f212-113">Solo un usuario de Windows por equipo puede usar una imagen</span><span class="sxs-lookup"><span data-stu-id="5f212-113">An image can be used by only one Windows user per computer</span></span>


<span data-ttu-id="5f212-114">Una imagen del área de trabajo de MED-V solo la puede usar el usuario de Windows que haya descargado o importado la imagen.</span><span class="sxs-lookup"><span data-stu-id="5f212-114">A MED-V workspace image can be used only by the Windows user who downloaded or imported the image.</span></span> <span data-ttu-id="5f212-115">Este usuario es el único usuario aparte de los administradores que tienen permisos en la carpeta donde se encuentran las imágenes descargadas.</span><span class="sxs-lookup"><span data-stu-id="5f212-115">This user is the only user aside from administrators who have permissions to the folder where the downloaded images are located.</span></span>

### <span data-ttu-id="5f212-116">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-116">Solution</span></span>

<span data-ttu-id="5f212-117">Cambie manualmente la lista de control de acceso (ACL) en el almacén de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5f212-117">Manually change the access control list (ACL) on the image store.</span></span>

## <span data-ttu-id="5f212-118">Al instalar MED-V mediante el administrador de configuración con derechos de usuario habilitados, se produce un error en la desinstalación</span><span class="sxs-lookup"><span data-stu-id="5f212-118">When installing MED-V by using Configuration Manager with users rights enabled, uninstall fails</span></span>


<span data-ttu-id="5f212-119">Si MED-V se instala con Microsoft System Center Configuration Manager y el modo de ejecución del paquete se establece en derechos de usuario, se producirá un error durante la desinstalación con un mensaje de error que indica que solo los usuarios administrativos pueden desinstalar MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-119">If MED-V is installed by using Microsoft System Center Configuration Manager and the run mode of the package is set to users rights, uninstall fails with an error message that says that only administrative users can uninstall MED-V.</span></span>

### <span data-ttu-id="5f212-120">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-120">Solution</span></span>

<span data-ttu-id="5f212-121">Al crear un paquete de Configuration Manager para MED-V, establezca el modo de ejecución en derechos administrativos.</span><span class="sxs-lookup"><span data-stu-id="5f212-121">When creating a Configuration Manager package for MED-V, set the run mode to administrative rights.</span></span>

## <span data-ttu-id="5f212-122">Al instalar MED-V mediante un sistema de implementación corporativa, si la instalación está configurada para ejecutar el cliente después de la instalación, no podrá ejecutar el cliente.</span><span class="sxs-lookup"><span data-stu-id="5f212-122">When installing MED-V by using a corporate deployment system, where the installation is configured to run the client following installation, you cannot run the client</span></span>


<span data-ttu-id="5f212-123">Si MED-V se instala mediante un sistema de implementación empresarial y el paquete de instalación está configurado para ejecutar el cliente de MED-V después de la instalación, después de que el cliente se esté ejecutando en la cuenta del sistema, no podrá ver que el cliente está ejecutándose (excepto en el área de notificación) y no podrá interactuar con él.</span><span class="sxs-lookup"><span data-stu-id="5f212-123">If MED-V is installed by using a corporate deployment system and the installation package is configured to run MED-V client following the installation, after the client is running under the system account, you cannot see that the client is running (except in the notification area), and you cannot interact with it.</span></span>

### <span data-ttu-id="5f212-124">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-124">Solution</span></span>

<span data-ttu-id="5f212-125">Al instalar MED-V mediante un sistema de implementación corporativa, use el parámetro *iniciar \ _MEDV = 0* . msi.</span><span class="sxs-lookup"><span data-stu-id="5f212-125">When installing MED-V by using a corporate deployment system, use the *START\_MEDV=0* .msi parameter.</span></span>

## <span data-ttu-id="5f212-126">La imagen de prueba de MED-V no se inicia</span><span class="sxs-lookup"><span data-stu-id="5f212-126">MED-V test image fails to start</span></span>


<span data-ttu-id="5f212-127">Si una imagen de prueba de MED-V no se inicia, nunca se recuperará y se producirá un error en todas las iniciaciones futuras con el mensaje de error "GINA no se cargó".</span><span class="sxs-lookup"><span data-stu-id="5f212-127">If a MED-V test image fails to start, it will never recover and all future startups will fail with a “GINA fail to load” error message.</span></span>

### <span data-ttu-id="5f212-128">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-128">Solution</span></span>

<span data-ttu-id="5f212-129">Elimine la imagen de prueba existente y, a continuación, vuelva a crearla.</span><span class="sxs-lookup"><span data-stu-id="5f212-129">Delete the existing test image and then re-create it.</span></span>

## <span data-ttu-id="5f212-130">Después de intentar unirse a un dominio con las credenciales incorrectas, la imagen nunca se puede unir al dominio.</span><span class="sxs-lookup"><span data-stu-id="5f212-130">After attempting to join a domain with the wrong credentials, the image never succeeds in joining the domain</span></span>


<span data-ttu-id="5f212-131">Si hay un error de configuración en el bloque de creación de dominio de unirse, que forma parte de la secuencia de comandos de configuración de primera hora de la máquina virtual, se produce un error en el área de trabajo de MED-V al intentar unirse a un dominio.</span><span class="sxs-lookup"><span data-stu-id="5f212-131">If there is a configuration error in the join domain building block, which is part of the virtual machine first-time setup script, it causes the MED-V workspace to fail when attempting to join a domain.</span></span> <span data-ttu-id="5f212-132">Después de que se repare el error de configuración, la imagen incluida en el área de trabajo de MED-V no se puede unir al dominio.</span><span class="sxs-lookup"><span data-stu-id="5f212-132">After the configuration error is repaired, the image included in the MED-V workspace cannot join the domain.</span></span>

### <span data-ttu-id="5f212-133">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-133">Solution</span></span>

<span data-ttu-id="5f212-134">Si la imagen se ha implementado, redistribuya la imagen.</span><span class="sxs-lookup"><span data-stu-id="5f212-134">If the image was deployed, redistribute the image.</span></span> <span data-ttu-id="5f212-135">Si la imagen era una imagen de prueba, vuelva a crear la imagen.</span><span class="sxs-lookup"><span data-stu-id="5f212-135">If the image was a test image, re-create the image.</span></span>

## <span data-ttu-id="5f212-136">MED-V no admite varios monitores</span><span class="sxs-lookup"><span data-stu-id="5f212-136">MED-V does not support multiple monitors</span></span>


<span data-ttu-id="5f212-137">MED-V no admite la visualización de aplicaciones publicadas en varios monitores.</span><span class="sxs-lookup"><span data-stu-id="5f212-137">MED-V does not support displaying published applications across multiple monitors.</span></span> <span data-ttu-id="5f212-138">Es posible que las aplicaciones publicadas y otras ventanas cliente se muestren en la pantalla incorrecta y, a veces, después de que una pantalla se desconecte, MED-V intenta enviar la pantalla al monitor para que el monitor conectado aparezca en blanco.</span><span class="sxs-lookup"><span data-stu-id="5f212-138">Published applications and other client windows may be displayed in the wrong screen, and sometimes after a screen is disconnected, MED-V attempts to send the screen to the monitor so that the connected monitor appears blank.</span></span>

### <span data-ttu-id="5f212-139">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-139">Solution</span></span>

<span data-ttu-id="5f212-140">Desconecte la pantalla adicional y reinicie el cliente.</span><span class="sxs-lookup"><span data-stu-id="5f212-140">Disconnect the additional screen, and restart the client.</span></span>

## <span data-ttu-id="5f212-141">Es posible que el área de trabajo de MED-V no se inicie si el host se bloquea durante el inicio del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5f212-141">MED-V workspace might fail to start if the host crashes during MED-V workspace startup</span></span>


<span data-ttu-id="5f212-142">Si el host se bloquea durante el proceso de inicio del área de trabajo de MED-V y aparece un mensaje de error que dice "falta el elemento raíz", el área de trabajo de MED-V puede agregar datos a un archivo de configuración de máquina virtual (VMC) vacío, lo que provocará errores en el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="5f212-142">If the host crashes during the MED-V workspace startup process and an error message appears that says “Root element is missing,” the MED-V workspace might add data to an empty virtual machine configuration (VMC) file, which will cause the startup process to fail.</span></span>

### <span data-ttu-id="5f212-143">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-143">Solution</span></span>

<span data-ttu-id="5f212-144">Reemplace el archivo VMC vacío por un archivo VMC de la imagen base.</span><span class="sxs-lookup"><span data-stu-id="5f212-144">Replace the empty VMC file with a VMC file from the base image.</span></span>

## <span data-ttu-id="5f212-145">El teclado no responde en las ventanas de la aplicación publicadas</span><span class="sxs-lookup"><span data-stu-id="5f212-145">The keyboard does not respond in published application windows</span></span>


<span data-ttu-id="5f212-146">En un área de trabajo de MED-V, si presiona la tecla del logotipo de Windows cuando una aplicación publicada está en el foco, el teclado ya no responde en las ventanas de la aplicación publicadas.</span><span class="sxs-lookup"><span data-stu-id="5f212-146">In a MED-V workspace, if you press the Windows logo key when a published application is in focus, the keyboard no longer responds in published application windows.</span></span>

### <span data-ttu-id="5f212-147">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-147">Solution</span></span>

<span data-ttu-id="5f212-148">Presione la tecla del logotipo de Windows mientras una aplicación publicada está en el foco.</span><span class="sxs-lookup"><span data-stu-id="5f212-148">Press the Windows logo key while a published application is in focus.</span></span>

## <span data-ttu-id="5f212-149">Un área de trabajo de dominio MED-V no actualiza las credenciales de dominio</span><span class="sxs-lookup"><span data-stu-id="5f212-149">A domain MED-V workspace does not update domain credentials</span></span>


<span data-ttu-id="5f212-150">Al usar un área de trabajo de MED-V persistente en un entorno de dominio, si cambia la contraseña de dominio, el cliente de MED-v no actualiza las credenciales de dominio del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-150">When using a persistent MED-V workspace in a domain environment, if you change your domain password, the MED-V client does not update the MED-V workspace domain credentials.</span></span> <span data-ttu-id="5f212-151">Cuando una aplicación publicada intenta acceder a un recurso de red, recibirá un mensaje de error que le notificará que sus credenciales han expirado.</span><span class="sxs-lookup"><span data-stu-id="5f212-151">When a published application attempts to access a network resource, you will receive an error message notifying you that your credentials expired.</span></span>

### <span data-ttu-id="5f212-152">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-152">Solution</span></span>

<span data-ttu-id="5f212-153">Reinicie el sistema operativo de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-153">Restart the MED-V workspace operating system.</span></span>

## <span data-ttu-id="5f212-154">Las ventanas de aplicaciones publicadas maximizadas cubren la barra de tareas del anfitrión</span><span class="sxs-lookup"><span data-stu-id="5f212-154">Maximized published application windows cover the host taskbar</span></span>


<span data-ttu-id="5f212-155">Si maximiza una ventana publicada de la aplicación a pantalla completa, puede que cubra la barra de tareas host.</span><span class="sxs-lookup"><span data-stu-id="5f212-155">If you maximize a published application window to full screen, it might cover the host taskbar.</span></span>

### <span data-ttu-id="5f212-156">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-156">Solution</span></span>

<span data-ttu-id="5f212-157">Realiza una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="5f212-157">Do one of the following:</span></span>

<span data-ttu-id="5f212-158">Minimice la ventana publicada de la aplicación para obtener acceso al área de notificación y reinicie el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-158">Minimize the published application window to gain access to the notification area, and restart the MED-V workspace.</span></span>

<span data-ttu-id="5f212-159">Minimice la ventana publicada de la aplicación y, a continuación, restaure la ventana a su estado maximizado.</span><span class="sxs-lookup"><span data-stu-id="5f212-159">Minimize the published application window, and then restore the window to its maximized state.</span></span>

## <span data-ttu-id="5f212-160">No funciona la adición de usuarios o grupos en el administrador de configuración de servidor de MED-V</span><span class="sxs-lookup"><span data-stu-id="5f212-160">Adding users or groups in the MED-V Server Configuration Manager does not work</span></span>


<span data-ttu-id="5f212-161">Al agregar usuarios o grupos en el cuadro de diálogo **Seleccionar usuarios o grupos** , los usuarios o grupos seleccionados no se agregan a la lista de control de acceso en el administrador de configuración de MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="5f212-161">When adding users or groups in the **Select Users or Groups** dialog box, the selected users or groups are not added to the access control list in the MED-V Server Configuration Manager.</span></span>

### <span data-ttu-id="5f212-162">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-162">Solution</span></span>

<span data-ttu-id="5f212-163">Agregue usuarios o grupos mediante el cuadro de diálogo **Escriba los nombres de usuario o grupo** .</span><span class="sxs-lookup"><span data-stu-id="5f212-163">Add users or groups using the **Enter User or Group names** dialog box.</span></span> <span data-ttu-id="5f212-164">Para obtener información detallada, vea [Cómo instalar y configurar el componente de servidor MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span><span class="sxs-lookup"><span data-stu-id="5f212-164">For detailed information, see [How to Install and Configure the MED-V Server Component](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span></span>

## <span data-ttu-id="5f212-165">MED-V no funciona en equipos con Windows Virtual PC para Windows 7 instalado</span><span class="sxs-lookup"><span data-stu-id="5f212-165">MED-V does not work on computers with Windows Virtual PC for Windows 7 installed</span></span>


<span data-ttu-id="5f212-166">MED-V requiere PC2007 virtual de Windows.</span><span class="sxs-lookup"><span data-stu-id="5f212-166">MED-V requires Windows Virtual PC2007.</span></span> <span data-ttu-id="5f212-167">Windows Virtual PC para Windows7 y virtual PC2007 SP1 no se puede instalar en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="5f212-167">Windows Virtual PC for Windows7 and Virtual PC2007 SP1 cannot be installed on the same computer.</span></span>

### <span data-ttu-id="5f212-168">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-168">Solution</span></span>

<span data-ttu-id="5f212-169">Desinstale Virtual PC para Windows7 antes de instalar virtual PC2007 SP1 y MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-169">Uninstall Virtual PC for Windows7 before installing Virtual PC2007 SP1 and MED-V.</span></span>

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a><span data-ttu-id="5f212-170">MED-V no admite imágenes de modo virtual PC y WindowsXP</span><span class="sxs-lookup"><span data-stu-id="5f212-170">MED-V does not support Virtual PC and WindowsXP Mode images</span></span>


<span data-ttu-id="5f212-171">MED-V 1.0 SP1 no admite imágenes creadas por Windows Virtual PC para Windows7.</span><span class="sxs-lookup"><span data-stu-id="5f212-171">MED-V1.0 SP1 does not support images created by Windows Virtual PC for Windows7.</span></span> <span data-ttu-id="5f212-172">Si se usa una imagen de Virtual PC para Windows7, se producirá un error en el cliente durante el inicio.</span><span class="sxs-lookup"><span data-stu-id="5f212-172">If a Virtual PC for Windows7 image is used, the client will fail during startup.</span></span>

### <span data-ttu-id="5f212-173">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-173">Solution</span></span>

<span data-ttu-id="5f212-174">Cree imágenes de MED-V mediante el uso de virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="5f212-174">Create MED-V images by using Virtual PC2007 SP1.</span></span>

## <span data-ttu-id="5f212-175">Firewall de Windows bloquea la actividad de red de virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="5f212-175">Windows firewall blocks Virtual PC2007 SP1 network activity</span></span>


<span data-ttu-id="5f212-176">De forma predeterminada, Firewall de Windows bloquea la actividad de red de virtual PC2007 SP1 y, cuando virtual PC2007 SP1 se inicia en el equipo cliente, hay un mensaje de firewall que bloquea su secuencia de inicio y todo el acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="5f212-176">By default, Windows firewall blocks Virtual PC2007 SP1 network activity, and when Virtual PC2007 SP1 initiates on the client computer, there is a firewall message that blocks its startup sequence and all network access.</span></span>

### <span data-ttu-id="5f212-177">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-177">Solution</span></span>

<span data-ttu-id="5f212-178">Actualice la excepción del firewall mediante la Directiva de grupo antes de que el usuario final use el MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-178">Update the firewall exception by using Group Policy before MED-V is used by the end user.</span></span>

## <span data-ttu-id="5f212-179">Al actualizar al cliente, aparece un mensaje de error</span><span class="sxs-lookup"><span data-stu-id="5f212-179">When upgrading the client an error message appears</span></span>


<span data-ttu-id="5f212-180">Al actualizar el cliente de MED-V 1.0 a MED-V 1.0 SP1, puede que aparezca un mensaje que le notifique que no se ha definido ningún área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f212-180">When upgrading the client from MED-V1.0 to MED-V1.0 SP1, a message may appear notifying you that no MED-V workspace is defined.</span></span>

### <span data-ttu-id="5f212-181">Solución</span><span class="sxs-lookup"><span data-stu-id="5f212-181">Solution</span></span>

<span data-ttu-id="5f212-182">Cierre el cliente y reinícielo.</span><span class="sxs-lookup"><span data-stu-id="5f212-182">Close the client and restart it.</span></span>

## <span data-ttu-id="5f212-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f212-183">Related topics</span></span>


[<span data-ttu-id="5f212-184">Notas de la versión de MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="5f212-184">MED-V 1.0 Release Notes</span></span>](med-v-10-release-notesmedv-10.md)

[<span data-ttu-id="5f212-185">MED-V 1.0 SP1 y notas de la versión de SP2</span><span class="sxs-lookup"><span data-stu-id="5f212-185">MED-V 1.0 SP1 and SP2 Release Notes</span></span>](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





