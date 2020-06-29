---
title: Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT
description: Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT
author: dansimp
ms.assetid: c0062208-39cd-4e01-adf8-36a11386e2ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 42d49c6c5c494da866785764e1c93a6bda2d667e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822591"
---
# <span data-ttu-id="61f40-103">Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="61f40-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="61f40-104">Use la característica de conexión remota de Microsoft Diagnostics and Recovery Toolset (DaRT) 10 para ejecutar las herramientas de DaRT de forma remota en un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="61f40-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="61f40-105">Una vez que el usuario final proporciona a un administrador o a un trabajador del servicio de asistencia información, el administrador de ti o el trabajador del servicio de asistencia pueden tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.</span><span class="sxs-lookup"><span data-stu-id="61f40-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="61f40-106">Si ha deshabilitado las herramientas de DaRT al crear la imagen de recuperación, aún tiene acceso a todas las herramientas.</span><span class="sxs-lookup"><span data-stu-id="61f40-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="61f40-107">Todas las herramientas, excepto la conexión remota, no están disponibles para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="61f40-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="61f40-108">Para recuperar un equipo remoto con la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="61f40-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="61f40-109">Inicie un equipo de usuario final con la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="61f40-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="61f40-110">Por lo general, puede usar uno de los siguientes métodos para arrancar DaRT y recuperar un equipo remoto, en función de cómo implemente la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="61f40-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="61f40-111">Para obtener más información sobre la implementación de la imagen de recuperación de DaRT, consulte [implementación de DART 10](deploying-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="61f40-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 10](deploying-dart-10.md).</span></span>

    -   <span data-ttu-id="61f40-112">Inicie DaRT desde una partición de recuperación en el equipo con problemas.</span><span class="sxs-lookup"><span data-stu-id="61f40-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="61f40-113">Inicie en DaRT desde una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="61f40-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="61f40-114">Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="61f40-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

    <span data-ttu-id="61f40-115">Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="61f40-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="61f40-116">Nota</span><span class="sxs-lookup"><span data-stu-id="61f40-116">Note</span></span>**  
    <span data-ttu-id="61f40-117">La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.</span><span class="sxs-lookup"><span data-stu-id="61f40-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="61f40-118">Cuando se le pregunte si desea inicializar los servicios de red, seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="61f40-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="61f40-119">**Sí** : se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="61f40-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="61f40-120">Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.</span><span class="sxs-lookup"><span data-stu-id="61f40-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="61f40-121">**No** , omitir el proceso de inicialización de red.</span><span class="sxs-lookup"><span data-stu-id="61f40-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="61f40-122">Indique si desea volver a asignar las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="61f40-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="61f40-123">Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión.</span><span class="sxs-lookup"><span data-stu-id="61f40-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="61f40-124">Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea.</span><span class="sxs-lookup"><span data-stu-id="61f40-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="61f40-125">La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="61f40-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="61f40-126">En el cuadro de diálogo **Opciones de recuperación del sistema** , seleccione una distribución de teclado.</span><span class="sxs-lookup"><span data-stu-id="61f40-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="61f40-127">Compruebe el directorio raíz del sistema que se muestra, el tipo de sistema operativo instalado y el tamaño de la partición.</span><span class="sxs-lookup"><span data-stu-id="61f40-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="61f40-128">Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos y, a continuación, inserte los medios de instalación para el dispositivo y seleccione el controlador.</span><span class="sxs-lookup"><span data-stu-id="61f40-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="61f40-129">Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="61f40-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="61f40-130">Nota</span><span class="sxs-lookup"><span data-stu-id="61f40-130">Note</span></span>**  
   <span data-ttu-id="61f40-131">Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 10 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="61f40-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="61f40-132">Para obtener más información sobre cómo resolver este problema, consulte [solución de problemas de DART 10](troubleshooting-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="61f40-132">For information about how to resolve this issue, see [Troubleshooting DaRT 10](troubleshooting-dart-10.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="61f40-133">En la ventana **Opciones de recuperación del sistema** , haga clic en **Microsoft Diagnostics and Recovery Toolset** para abrir el **conjunto de herramientas de diagnóstico y recuperación**.</span><span class="sxs-lookup"><span data-stu-id="61f40-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="61f40-134">En la ventana **conjunto de herramientas de diagnóstico y recuperación** , haga clic en **conexión remota** para abrir la ventana **conexión remota de DART** .</span><span class="sxs-lookup"><span data-stu-id="61f40-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="61f40-135">Si se le pide que proporcione el acceso remoto del Departamento de soporte técnico, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="61f40-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="61f40-136">Se abrirá la ventana conexión remota de DaRT, que muestra un número de ticket, una dirección IP e información de puerto.</span><span class="sxs-lookup"><span data-stu-id="61f40-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="61f40-137">En el equipo de asistencia, abra el **visor de conexión remota de DART**.</span><span class="sxs-lookup"><span data-stu-id="61f40-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="61f40-138">Haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft DART 10**y, a continuación, haga clic en **visor de conexión remota DART**.</span><span class="sxs-lookup"><span data-stu-id="61f40-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 10**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="61f40-139">En la ventana **conexión remota de DART** , escriba el vale, la dirección IP y la información del puerto que desee.</span><span class="sxs-lookup"><span data-stu-id="61f40-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="61f40-140">Nota</span><span class="sxs-lookup"><span data-stu-id="61f40-140">Note</span></span>**  
   <span data-ttu-id="61f40-141">Esta información se crea en el equipo del usuario final y debe ser proporcionada por el usuario final.</span><span class="sxs-lookup"><span data-stu-id="61f40-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="61f40-142">Es posible que haya varias direcciones IP para elegir, en función de cuántos estén disponibles en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="61f40-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="61f40-143">Haz clic en **Connect**.</span><span class="sxs-lookup"><span data-stu-id="61f40-143">Click **Connect**.</span></span>

<span data-ttu-id="61f40-144">El administrador de TI ahora asume el control del equipo de usuario final y puede ejecutar las herramientas de DaRT de forma remota.</span><span class="sxs-lookup"><span data-stu-id="61f40-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="61f40-145">Nota</span><span class="sxs-lookup"><span data-stu-id="61f40-145">Note</span></span>**  
<span data-ttu-id="61f40-146">Se proporciona un archivo que se denomina inv32.xml y contiene información de conexión remota, como el número de puerto y la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="61f40-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="61f40-147">De forma predeterminada, el archivo suele encontrarse en%WINDIR%\\system32.</span><span class="sxs-lookup"><span data-stu-id="61f40-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="61f40-148">Para personalizar el proceso de conexión remota</span><span class="sxs-lookup"><span data-stu-id="61f40-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="61f40-149">Puede personalizar el proceso de conexión remota editando el archivo winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="61f40-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="61f40-150">Para obtener más información sobre cómo editar el archivo de winpeshl.ini, consulte [Winpeshl.ini archivos](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="61f40-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="61f40-151">Especifique los siguientes comandos y parámetros para personalizar cómo se establece una conexión remota con un equipo de usuario final:</span><span class="sxs-lookup"><span data-stu-id="61f40-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="61f40-152">Comando</span><span class="sxs-lookup"><span data-stu-id="61f40-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="61f40-153">Parámetro</span><span class="sxs-lookup"><span data-stu-id="61f40-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="61f40-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="61f40-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="61f40-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="61f40-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="61f40-156">-nomessage</span><span class="sxs-lookup"><span data-stu-id="61f40-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="61f40-157">Especifica que no se muestre la pregunta de confirmación.</span><span class="sxs-lookup"><span data-stu-id="61f40-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="61f40-158">La conexión remota </strong> continúa como si el usuario final hubiera respondido &quot; afirmativamente &quot; a la pregunta de confirmación.</span><span class="sxs-lookup"><span data-stu-id="61f40-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="61f40-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="61f40-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="61f40-160">ninguno</span><span class="sxs-lookup"><span data-stu-id="61f40-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="61f40-161">Impide que un script personalizado continúe hasta que <strong> no se esté ejecutando una conexión remota </strong> o se haya establecido una conexión válida con el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="61f40-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="61f40-162">Importante</span><span class="sxs-lookup"><span data-stu-id="61f40-162">Important</span></span></strong><br/><p><span data-ttu-id="61f40-163">Este comando no funciona si se especifica de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="61f40-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="61f40-164">Debe especificarse en un script para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="61f40-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="61f40-165">Este es un ejemplo de un archivo de winpeshl.ini que se personaliza para abrir la herramienta de **conexión remota** tan pronto como se intente iniciar en DART:</span><span class="sxs-lookup"><span data-stu-id="61f40-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="61f40-166">Cuando se inicia DaRT, crea el archivo inv32.xml en \\Windows\\System32\\ en el disco RAM.</span><span class="sxs-lookup"><span data-stu-id="61f40-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="61f40-167">Este archivo contiene información de conexión: dirección IP, puerto y número de incidencia.</span><span class="sxs-lookup"><span data-stu-id="61f40-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="61f40-168">Puede copiar este archivo en un recurso compartido de red para desencadenar un flujo de trabajo de asistencia.</span><span class="sxs-lookup"><span data-stu-id="61f40-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="61f40-169">Por ejemplo, un programa personalizado puede comprobar el recurso compartido de red para los archivos de conexión y, después, crear una incidencia de soporte técnico o enviar notificaciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="61f40-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="61f40-170">Para ejecutar el visor de conexión remota en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="61f40-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="61f40-171">Para ejecutar el **visor de conexión remota de DART** en el símbolo del sistema, especifique el comando **DartRemoteViewer.exe** y use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="61f40-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="61f40-172">Parámetro</span><span class="sxs-lookup"><span data-stu-id="61f40-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="61f40-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="61f40-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="61f40-174">-Ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="61f40-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="61f40-175">Donde &lt; <em> ticketnumber </em> &gt; es el número de la incidencia, incluidos los guiones, que genera la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="61f40-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="61f40-176">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="61f40-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="61f40-177">Donde &lt; <em> direcciónIP </em> &gt; es la dirección IP generada por la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="61f40-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="61f40-178">-Port = &lt; <em> Puerto</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="61f40-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="61f40-179">Donde &lt; <em> Puerto </em> &gt; es el puerto que corresponde a la dirección IP especificada.</span><span class="sxs-lookup"><span data-stu-id="61f40-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="61f40-180">Si se especifican los tres parámetros y los datos son válidos, se intentará inmediatamente una conexión cuando se inicie el programa.</span><span class="sxs-lookup"><span data-stu-id="61f40-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="61f40-181">Si alguno de los parámetros no es válido, el programa se inicia como si no se hubiera especificado ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="61f40-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="61f40-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61f40-182">Related topics</span></span>


[<span data-ttu-id="61f40-183">Operaciones para DaRT 10</span><span class="sxs-lookup"><span data-stu-id="61f40-183">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="61f40-184">Equipos de recuperación que usan DaRT 10</span><span class="sxs-lookup"><span data-stu-id="61f40-184">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









