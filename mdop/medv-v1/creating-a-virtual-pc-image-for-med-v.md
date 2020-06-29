---
title: Creación de una imagen de Virtual PC para MED-V
description: Creación de una imagen de Virtual PC para MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823661"
---
# <span data-ttu-id="d1582-103">Creación de una imagen de Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="d1582-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="d1582-104">Para crear una imagen de Virtual PC (VPC) para MED-V, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1582-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="d1582-105">[Cree una imagen de VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="d1582-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="d1582-106">[Instale el paquete de área de trabajo. msi MED-V en la imagen VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).</span><span class="sxs-lookup"><span data-stu-id="d1582-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="d1582-107">[Ejecute la herramienta de requisitos previos de las máquinas virtuales MED-V en la imagen de VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).</span><span class="sxs-lookup"><span data-stu-id="d1582-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="d1582-108">[Configure manualmente los requisitos previos de las máquinas virtuales en la imagen de VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span><span class="sxs-lookup"><span data-stu-id="d1582-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="d1582-109">[Configurar Sysprep para imágenes de MED-V](#bkmk-howtoconfiguresysprepformedvimages) (opcional).</span><span class="sxs-lookup"><span data-stu-id="d1582-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="d1582-110">[Desactive Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="d1582-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="d1582-111">Creación de una imagen de Virtual PC con Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1582-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="d1582-112">Para crear una imagen de Virtual PC con Microsoft Virtual PC, consulte la documentación de Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d1582-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="d1582-113">Para obtener más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="d1582-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="d1582-114">Ayuda de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1582-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="d1582-115">Crear una máquina virtual e instalar un sistema operativo invitado</span><span class="sxs-lookup"><span data-stu-id="d1582-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="d1582-116">Cómo instalar el paquete de área de trabajo. msi de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1582-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="d1582-117">Después de crear la imagen de Virtual PC, instale el paquete de área de trabajo. msi de MED-V en la imagen.</span><span class="sxs-lookup"><span data-stu-id="d1582-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="d1582-118">Para instalar la imagen del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1582-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="d1582-119">Inicie la máquina virtual y copie el paquete de área de trabajo. msi de MED-V en el interior.</span><span class="sxs-lookup"><span data-stu-id="d1582-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="d1582-120">El paquete de área de trabajo. msi MED-V se llama *MED-V\_workspace\_x.msi*, donde *x* es el número de versión.</span><span class="sxs-lookup"><span data-stu-id="d1582-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="d1582-121">Por ejemplo, *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="d1582-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="d1582-122">Haga doble clic en el paquete de área de trabajo. msi de MED-V y siga las instrucciones del Asistente para instalación.</span><span class="sxs-lookup"><span data-stu-id="d1582-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="d1582-123">Nota</span><span class="sxs-lookup"><span data-stu-id="d1582-123">Note</span></span>**  
    <span data-ttu-id="d1582-124">Cuando se publique una nueva versión de MED-V y se actualice una imagen de Virtual PC existente, desinstale el paquete. msi del área de trabajo de MED-V existente, reinicie el equipo e instale el nuevo paquete de área de trabajo de MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="d1582-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="d1582-125">Cómo ejecutar la herramienta de requisitos previos para máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="d1582-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="d1582-126">La herramienta de requisitos previos de la máquina virtual (VM) es un asistente que automatiza varios de los requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="d1582-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="d1582-127">Nota</span><span class="sxs-lookup"><span data-stu-id="d1582-127">Note</span></span>**  
<span data-ttu-id="d1582-128">Aunque muchos parámetros se pueden configurar en el asistente, no se pueden configurar las propiedades necesarias para el funcionamiento correcto de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1582-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="d1582-129">Para ejecutar la herramienta de requisitos previos de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d1582-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="d1582-130">Después de instalar el paquete de área de trabajo de MED-V. msi, en el menú **Inicio** de Windows, seleccione **herramienta de &gt; &gt; requisitos previos de los programas MED-v VM**.</span><span class="sxs-lookup"><span data-stu-id="d1582-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="d1582-131">Nota</span><span class="sxs-lookup"><span data-stu-id="d1582-131">Note</span></span>**  
    <span data-ttu-id="d1582-132">El usuario que ejecuta la herramienta de requisitos previos de las máquinas virtuales debe tener derechos de administrador local y debe ser el único usuario que haya iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="d1582-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="d1582-133">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d1582-133">Click **Next**.</span></span>

3. <span data-ttu-id="d1582-134">En la página **configuración de Windows** , en las siguientes propiedades configurables, seleccione las que desea configurar:</span><span class="sxs-lookup"><span data-stu-id="d1582-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="d1582-135">Borrar la información del historial personal de los usuarios</span><span class="sxs-lookup"><span data-stu-id="d1582-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="d1582-136">Borrar directorio temporal de perfiles locales</span><span class="sxs-lookup"><span data-stu-id="d1582-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="d1582-137">Deshabilitar sonidos en los siguientes eventos de Windows: Inicio, Inicio de sesión y cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="d1582-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="d1582-138">Nota</span><span class="sxs-lookup"><span data-stu-id="d1582-138">Note</span></span>**  
   <span data-ttu-id="d1582-139">No habilitar el protector de páginas de Windows en una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d1582-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="d1582-140">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d1582-140">Click **Next**.</span></span>

5. <span data-ttu-id="d1582-141">En la página **configuración de Internet Explorer** , en las siguientes propiedades configurables, seleccione las que desea configurar:</span><span class="sxs-lookup"><span data-stu-id="d1582-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="d1582-142">No uses características de autocompletar</span><span class="sxs-lookup"><span data-stu-id="d1582-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="d1582-143">Deshabilitar la reutilización de Windows para iniciar accesos directos</span><span class="sxs-lookup"><span data-stu-id="d1582-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="d1582-144">Borrar el historial de navegación</span><span class="sxs-lookup"><span data-stu-id="d1582-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="d1582-145">Habilitar la exploración por pestañas en Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="d1582-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="d1582-146">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d1582-146">Click **Next**.</span></span>

7. <span data-ttu-id="d1582-147">En la página **servicios de Windows** , en las siguientes propiedades configurables, seleccione las que desea configurar:</span><span class="sxs-lookup"><span data-stu-id="d1582-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="d1582-148">Servicio centro de seguridad</span><span class="sxs-lookup"><span data-stu-id="d1582-148">Security center service</span></span>**

   -   **<span data-ttu-id="d1582-149">Servicio Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d1582-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="d1582-150">Servicio actualizaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="d1582-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="d1582-151">Servicio de restaurar sistema</span><span class="sxs-lookup"><span data-stu-id="d1582-151">System restore service</span></span>**

   -   **<span data-ttu-id="d1582-152">Servicio de Index Server</span><span class="sxs-lookup"><span data-stu-id="d1582-152">Indexing service</span></span>**

   -   **<span data-ttu-id="d1582-153">Configuración inalámbrica rápida</span><span class="sxs-lookup"><span data-stu-id="d1582-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="d1582-154">Compatibilidad con la conmutación rápida de usuarios</span><span class="sxs-lookup"><span data-stu-id="d1582-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="d1582-155">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d1582-155">Click **Next**.</span></span>

9. <span data-ttu-id="d1582-156">En la página de **Inicio de sesión automático de Windows** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1582-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="d1582-157">Active la casilla de verificación **Habilitar el inicio de sesión automático de Windows** .</span><span class="sxs-lookup"><span data-stu-id="d1582-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="d1582-158">Asigne un **nombre de usuario** y una **contraseña**.</span><span class="sxs-lookup"><span data-stu-id="d1582-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="d1582-159">Haga clic en **aplicar**y, en el cuadro de confirmación que aparece, haga clic en **sí**.</span><span class="sxs-lookup"><span data-stu-id="d1582-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="d1582-160">En la página **Resumen** , haga clic en **Finalizar** para salir del asistente</span><span class="sxs-lookup"><span data-stu-id="d1582-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="d1582-161">Nota</span><span class="sxs-lookup"><span data-stu-id="d1582-161">Note</span></span>**  
<span data-ttu-id="d1582-162">Compruebe que las directivas de grupo no sobrescriben la configuración obligatoria establecida en la herramienta requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="d1582-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="d1582-163">Cómo configurar los requisitos previos de instalación manual de máquinas virtuales de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1582-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="d1582-164">Algunas de las configuraciones no se pueden configurar a través de la herramienta de requisitos previos de máquina virtual y se deben realizar de forma manual.</span><span class="sxs-lookup"><span data-stu-id="d1582-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="d1582-165">Configuración de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d1582-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="d1582-166">Se recomienda configurar las siguientes opciones de la máquina virtual en la consola de Microsoft Virtual PC:</span><span class="sxs-lookup"><span data-stu-id="d1582-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="d1582-167">Deshabilitar unidades de disquete.</span><span class="sxs-lookup"><span data-stu-id="d1582-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="d1582-168">Deshabilitar deshacer discos (**configuración &gt; , deshacer-discos**).</span><span class="sxs-lookup"><span data-stu-id="d1582-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="d1582-169">Asegúrese de que la imagen tiene solo una CPU virtual.</span><span class="sxs-lookup"><span data-stu-id="d1582-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="d1582-170">Elimine las interacciones entre la máquina virtual y el usuario, donde no están relacionadas con las aplicaciones publicadas (como los mensajes que requieren la intervención del usuario).</span><span class="sxs-lookup"><span data-stu-id="d1582-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="d1582-171">Configuración de imagen</span><span class="sxs-lookup"><span data-stu-id="d1582-171">Image Settings</span></span>

    <span data-ttu-id="d1582-172">Configure las siguientes opciones de configuración manuales dentro de la imagen:</span><span class="sxs-lookup"><span data-stu-id="d1582-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="d1582-173">En la ventana de **propiedades de opciones de energía** , deshabilite la hibernación y la suspensión.</span><span class="sxs-lookup"><span data-stu-id="d1582-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="d1582-174">Aplique las actualizaciones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="d1582-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="d1582-175">En el cuadro de diálogo **Inicio y recuperación de Windows** , en la sección **error del sistema** , desactive la casilla **reiniciar automáticamente** .</span><span class="sxs-lookup"><span data-stu-id="d1582-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="d1582-176">Asegúrese de que la imagen use una clave de licencia VLK.</span><span class="sxs-lookup"><span data-stu-id="d1582-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="d1582-177">Instalar complementos de VPC</span><span class="sxs-lookup"><span data-stu-id="d1582-177">Installing VPC Additions</span></span>

    <span data-ttu-id="d1582-178">En el menú **acción** , seleccione **instalar o actualizar Virtual Machine Additions**.</span><span class="sxs-lookup"><span data-stu-id="d1582-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="d1582-179">Configuración de la impresión</span><span class="sxs-lookup"><span data-stu-id="d1582-179">Configuring Printing</span></span>

    <span data-ttu-id="d1582-180">Puede configurar la impresión desde el área de trabajo MED-V de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="d1582-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="d1582-181">Agregue una impresora a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d1582-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="d1582-182">Permitir la impresión con impresoras que estén configuradas en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="d1582-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="d1582-183">Cómo configurar Sysprep para imágenes de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1582-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="d1582-184">En un área de trabajo de MED-V, se puede configurar Sysprep para asignar un identificador de seguridad único (SID), especialmente cuando se ejecutan varias áreas de trabajo de MED-V en un solo equipo.</span><span class="sxs-lookup"><span data-stu-id="d1582-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="d1582-185">No se recomienda usar Sysprep para unirse a un dominio; en su lugar, use la acción de script de dominio de combinación MED-V, como se describe en [Cómo configurar acciones de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d1582-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="d1582-186">Nota</span><span class="sxs-lookup"><span data-stu-id="d1582-186">Note</span></span>**  
<span data-ttu-id="d1582-187">Sysprep es la utilidad de preparación del sistema de Microsoft para el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d1582-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="d1582-188">Para configurar Sysprep en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1582-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="d1582-189">Cree un directorio en la raíz de la unidad del sistema denominada *Sysprep*.</span><span class="sxs-lookup"><span data-stu-id="d1582-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="d1582-190">Desde el CD de instalación de Windows, extraiga *deploy.cab* a la raíz de la unidad del sistema o descargue la actualización más reciente de las herramientas de implementación desde el sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1582-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="d1582-191">Para Windows 2000, consulte [actualización de las herramientas de implementación para windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span><span class="sxs-lookup"><span data-stu-id="d1582-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="d1582-192">Para Windows XP, consulte [actualización de las herramientas de implementación para Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span><span class="sxs-lookup"><span data-stu-id="d1582-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="d1582-193">Ejecute el **Administrador de instalación** (setupmgr.exe).</span><span class="sxs-lookup"><span data-stu-id="d1582-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="d1582-194">Siga los instrucciones del Asistente para administración de instalación.</span><span class="sxs-lookup"><span data-stu-id="d1582-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="d1582-195">Una vez que se ha configurado Sysprep y creado el área de trabajo de MED-V, debe ejecutarse Sysprep.</span><span class="sxs-lookup"><span data-stu-id="d1582-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="d1582-196">Para ejecutar Sysprep</span><span class="sxs-lookup"><span data-stu-id="d1582-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="d1582-197">Desde la carpeta Sysprep ubicada en la raíz de la unidad del sistema, ejecute la herramienta de preparación del sistema (Sysprep.exe).</span><span class="sxs-lookup"><span data-stu-id="d1582-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="d1582-198">En el cuadro de mensaje de advertencia que aparece, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d1582-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="d1582-199">En el cuadro de diálogo **propiedades de Sysprep** , active las casillas **de verificación no restablecer período de gracia para activación** y uso de la **instalación mínima** .</span><span class="sxs-lookup"><span data-stu-id="d1582-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="d1582-200">Haga clic en volver a **sellar**.</span><span class="sxs-lookup"><span data-stu-id="d1582-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="d1582-201">Si no está satisfecho con la información que se muestra en el cuadro de mensaje de confirmación que aparece, haga clic en **Cancelar** y cambie las selecciones.</span><span class="sxs-lookup"><span data-stu-id="d1582-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="d1582-202">Haga clic en **Aceptar** para completar el proceso de preparación del sistema.</span><span class="sxs-lookup"><span data-stu-id="d1582-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="d1582-203">Desactivar Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1582-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="d1582-204">Después de instalar y configurar todos los componentes, cierre Microsoft Virtual PC y seleccione **desactivar**.</span><span class="sxs-lookup"><span data-stu-id="d1582-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="d1582-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1582-205">Related topics</span></span>


<span data-ttu-id="d1582-206">Creación de una imagen de MED-V [Cómo configurar acciones de script](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="d1582-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>









