---
title: Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT
description: Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822791"
---
# <span data-ttu-id="ae46e-103">Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="ae46e-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="ae46e-104">La característica de conexión remota de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 permite a un administrador de ti ejecutar las herramientas de DaRT de forma remota en un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="ae46e-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="ae46e-105">Después de que el usuario final proporcione determinada información (o de un profesional del Departamento de soporte técnico que trabaje en el equipo del usuario final), el administrador de ti o el agente de asistencia pueden tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.</span><span class="sxs-lookup"><span data-stu-id="ae46e-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="ae46e-106">Importante</span><span class="sxs-lookup"><span data-stu-id="ae46e-106">Important</span></span>**  
<span data-ttu-id="ae46e-107">Los dos equipos que establecen una conexión remota deben formar parte de la misma red.</span><span class="sxs-lookup"><span data-stu-id="ae46e-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="ae46e-108">Para recuperar un equipo remoto con DaRT</span><span class="sxs-lookup"><span data-stu-id="ae46e-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="ae46e-109">Inicie un equipo de usuario final con la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="ae46e-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="ae46e-110">Por lo general, puede usar uno de los siguientes métodos para arrancar DaRT y recuperar un equipo remoto, en función de cómo implemente la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="ae46e-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="ae46e-111">Para obtener más información sobre la implementación de la imagen de recuperación de DaRT, consulte [implementación de la imagen de recuperación de dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="ae46e-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="ae46e-112">Inicie DaRT desde una partición de recuperación en el equipo con problemas.</span><span class="sxs-lookup"><span data-stu-id="ae46e-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="ae46e-113">Inicie en DaRT desde una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="ae46e-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="ae46e-114">Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="ae46e-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="ae46e-115">Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="ae46e-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="ae46e-116">Nota</span><span class="sxs-lookup"><span data-stu-id="ae46e-116">Note</span></span>**  
    <span data-ttu-id="ae46e-117">La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.</span><span class="sxs-lookup"><span data-stu-id="ae46e-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="ae46e-118">Mientras se inicia el equipo en la imagen de recuperación de DaRT, aparece el cuadro de diálogo **netstart** .</span><span class="sxs-lookup"><span data-stu-id="ae46e-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="ae46e-119">Se le pregunta si desea inicializar los servicios de red.</span><span class="sxs-lookup"><span data-stu-id="ae46e-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="ae46e-120">Si hace clic en **sí**, se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="ae46e-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="ae46e-121">Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.</span><span class="sxs-lookup"><span data-stu-id="ae46e-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="ae46e-122">Para omitir el proceso de inicialización de red, haga clic en **no**.</span><span class="sxs-lookup"><span data-stu-id="ae46e-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="ae46e-123">Siguiendo el cuadro de diálogo inicialización de red, se le preguntará si desea volver a asignar las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="ae46e-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="ae46e-124">Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión.</span><span class="sxs-lookup"><span data-stu-id="ae46e-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="ae46e-125">Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea.</span><span class="sxs-lookup"><span data-stu-id="ae46e-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="ae46e-126">La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="ae46e-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="ae46e-127">Siguiendo el cuadro de diálogo reasignación, aparece un cuadro de diálogo **Opciones de recuperación del sistema** y le pide que seleccione una distribución de teclado.</span><span class="sxs-lookup"><span data-stu-id="ae46e-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="ae46e-128">Después, se muestra el directorio raíz del sistema, el tipo de sistema operativo instalado y el tamaño de la partición.</span><span class="sxs-lookup"><span data-stu-id="ae46e-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="ae46e-129">Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos.</span><span class="sxs-lookup"><span data-stu-id="ae46e-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="ae46e-130">Esto le pedirá que inserte los medios de instalación para el dispositivo y que seleccione el controlador.</span><span class="sxs-lookup"><span data-stu-id="ae46e-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="ae46e-131">Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ae46e-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="ae46e-132">Nota</span><span class="sxs-lookup"><span data-stu-id="ae46e-132">Note</span></span>**  
    <span data-ttu-id="ae46e-133">Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 7 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ae46e-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="ae46e-134">Para obtener más información sobre cómo resolver este problema, consulte [solución de problemas de DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="ae46e-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="ae46e-135">En la ventana **Opciones de recuperación del sistema** , seleccione **Microsoft Diagnostics and Recovery Toolset** para abrir la ventana **conjunto de herramientas de diagnóstico y recuperación** .</span><span class="sxs-lookup"><span data-stu-id="ae46e-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="ae46e-136">En la ventana **conjunto de herramientas de diagnóstico y recuperación** , haga clic en **conexión remota** para abrir la ventana **conexión remota de DART** .</span><span class="sxs-lookup"><span data-stu-id="ae46e-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="ae46e-137">Si se le pide que proporcione el acceso remoto del Departamento de soporte técnico, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ae46e-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="ae46e-138">Se abrirá la ventana conexión remota de DaRT, que muestra un número de ticket, una dirección IP e información de puerto.</span><span class="sxs-lookup"><span data-stu-id="ae46e-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="ae46e-139">En el equipo agente de asistencia, abra el **visor de conexión remota de DART**.</span><span class="sxs-lookup"><span data-stu-id="ae46e-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="ae46e-140">Haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft DART 7**y, a continuación, haga clic en **visor de conexión remota DART**.</span><span class="sxs-lookup"><span data-stu-id="ae46e-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="ae46e-141">En la ventana **conexión remota de DART** , escriba el vale, la dirección IP y la información del puerto que desee.</span><span class="sxs-lookup"><span data-stu-id="ae46e-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="ae46e-142">Nota</span><span class="sxs-lookup"><span data-stu-id="ae46e-142">Note</span></span>**  
   <span data-ttu-id="ae46e-143">Esta información se crea en el equipo del usuario final y debe ser proporcionada por el usuario final.</span><span class="sxs-lookup"><span data-stu-id="ae46e-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="ae46e-144">Es posible que haya varias direcciones IP para elegir, en función de cuántos estén disponibles en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="ae46e-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="ae46e-145">Haz clic en **Connect**.</span><span class="sxs-lookup"><span data-stu-id="ae46e-145">Click **Connect**.</span></span>

<span data-ttu-id="ae46e-146">El administrador de TI ahora asume el control del equipo de usuario final y puede ejecutar las herramientas de DaRT de forma remota.</span><span class="sxs-lookup"><span data-stu-id="ae46e-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="ae46e-147">Nota</span><span class="sxs-lookup"><span data-stu-id="ae46e-147">Note</span></span>**  
<span data-ttu-id="ae46e-148">Se proporciona un archivo que se denomina inv32.xml y contiene información de conexión remota, como el número de puerto y la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="ae46e-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="ae46e-149">De forma predeterminada, el archivo suele encontrarse en%WINDIR%\\system32.</span><span class="sxs-lookup"><span data-stu-id="ae46e-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="ae46e-150">Para personalizar el proceso de conexión remota</span><span class="sxs-lookup"><span data-stu-id="ae46e-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="ae46e-151">Puede personalizar el proceso de conexión remota editando el archivo winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="ae46e-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="ae46e-152">Para obtener más información sobre cómo editar el archivo de winpeshl.ini, consulte [Winpeshl.ini archivos](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="ae46e-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="ae46e-153">Especifique los siguientes comandos y parámetros para personalizar cómo se establece una conexión remota con un equipo de usuario final:</span><span class="sxs-lookup"><span data-stu-id="ae46e-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="ae46e-154">Comando</span><span class="sxs-lookup"><span data-stu-id="ae46e-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="ae46e-155">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ae46e-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="ae46e-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae46e-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ae46e-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="ae46e-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ae46e-158">-nomessage</span><span class="sxs-lookup"><span data-stu-id="ae46e-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ae46e-159">Especifica que no se muestre la pregunta de confirmación.</span><span class="sxs-lookup"><span data-stu-id="ae46e-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="ae46e-160">La conexión remota </strong> continúa como si el usuario final hubiera respondido &quot; afirmativamente &quot; a la pregunta de confirmación.</span><span class="sxs-lookup"><span data-stu-id="ae46e-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ae46e-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="ae46e-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ae46e-162">ninguno</span><span class="sxs-lookup"><span data-stu-id="ae46e-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ae46e-163">Impide que un script personalizado continúe hasta que <strong> no se esté ejecutando una conexión remota </strong> o se haya establecido una conexión válida con el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="ae46e-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="ae46e-164">Importante</span><span class="sxs-lookup"><span data-stu-id="ae46e-164">Important</span></span></strong><br/><p><span data-ttu-id="ae46e-165">Este comando no funciona si se especifica de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="ae46e-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="ae46e-166">Debe especificarse en un script para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae46e-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="ae46e-167">Este es un ejemplo de un archivo de winpeshl.ini que se personaliza para abrir la herramienta de **conexión remota** tan pronto como se intente iniciar en DART:</span><span class="sxs-lookup"><span data-stu-id="ae46e-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="ae46e-168">Para ejecutar el visor de conexión remota en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="ae46e-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="ae46e-169">Puede ejecutar el **visor de conexión remota de DART** en el símbolo del sistema especificando el comando **DartRemoteViewer.exe** y usando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="ae46e-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="ae46e-170">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ae46e-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="ae46e-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae46e-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ae46e-172">-Ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="ae46e-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ae46e-173">Donde &lt; <em> ticketnumber </em> &gt; es el número de la incidencia, incluidos los guiones, que genera la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="ae46e-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ae46e-174">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="ae46e-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ae46e-175">Donde &lt; <em> direcciónIP </em> &gt; es la dirección IP generada por la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="ae46e-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ae46e-176">-Port = &lt; <em> Puerto</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="ae46e-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ae46e-177">Donde &lt; <em> Puerto </em> &gt; es el puerto que corresponde a la dirección IP especificada.</span><span class="sxs-lookup"><span data-stu-id="ae46e-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="ae46e-178">Si se especifican los tres parámetros y los datos son válidos, se intentará inmediatamente una conexión cuando se inicie el programa.</span><span class="sxs-lookup"><span data-stu-id="ae46e-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="ae46e-179">Si alguno de los parámetros no es válido, el programa se inicia como si no se hubiera especificado ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="ae46e-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="ae46e-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae46e-180">Related topics</span></span>


[<span data-ttu-id="ae46e-181">Equipos de recuperación que usan DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ae46e-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









