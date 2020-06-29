---
title: Procedimientos recomendados de MED-V 2.0
description: Procedimientos recomendados de MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826111"
---
# <span data-ttu-id="c565b-103">Procedimientos recomendados de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="c565b-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="c565b-104">Al planear, implementar y administrar MED-V en su empresa, es posible que las recomendaciones de procedimientos recomendados sean útiles.</span><span class="sxs-lookup"><span data-stu-id="c565b-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="c565b-105">Configurar la configuración de primera vez para ejecutarse de forma desatendida</span><span class="sxs-lookup"><span data-stu-id="c565b-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="c565b-106">Aunque puede especificar la configuración que prefiera, una práctica recomendada de MED-V es crear el archivo Sysprep. inf para que la primera configuración se pueda ejecutar en modo **desatendido** .</span><span class="sxs-lookup"><span data-stu-id="c565b-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="c565b-107">Esto requiere que proporcione toda la información de configuración necesaria a medida que continúa con el Asistente para **Administración de instalación** .</span><span class="sxs-lookup"><span data-stu-id="c565b-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="c565b-108">Para obtener más información sobre cómo configurar la imagen de MED-V, vea [configurar una imagen de Windows Virtual PC para Med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="c565b-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="c565b-109">Deshabilitar puntos de restauración en la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c565b-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="c565b-110">Antes de crear el paquete de área de trabajo MED-V, le recomendamos que deshabilite los puntos de restauración en la máquina virtual para evitar que el disco de diferenciación crezca sin límites.</span><span class="sxs-lookup"><span data-stu-id="c565b-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="c565b-111">Para obtener más información, consulte [Cómo desactivar y activar Restaurar sistema en Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="c565b-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="c565b-112">Configurar la imagen de MED-V para usar perfiles locales</span><span class="sxs-lookup"><span data-stu-id="c565b-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="c565b-113">Le recomendamos que aplique solo las directivas que tengan sentido en un entorno de compatibilidad de aplicaciones para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c565b-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="c565b-114">Por ejemplo, las directivas de personalización de escritorio no tienen que aplicarse por lo general y deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="c565b-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="c565b-115">Para obtener más información sobre cómo permitir solo perfiles locales, consulte [configuración de directiva de grupo para perfiles de usuarios móviles](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="c565b-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="c565b-116">Configurar una actualización de rendimiento de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="c565b-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="c565b-117">De forma predeterminada, la Directiva de grupo se descarga en un equipo de un byte cada vez.</span><span class="sxs-lookup"><span data-stu-id="c565b-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="c565b-118">Esto provoca retrasos cuando se une MED-V al dominio.</span><span class="sxs-lookup"><span data-stu-id="c565b-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="c565b-119">Para aumentar el rendimiento de la Directiva de grupo, le recomendamos que establezca el valor de la siguiente clave del registro en el registro:</span><span class="sxs-lookup"><span data-stu-id="c565b-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="c565b-120">Subclave del registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="c565b-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="c565b-121">Entrada: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="c565b-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="c565b-122">Tipo: DWORD</span><span class="sxs-lookup"><span data-stu-id="c565b-122">Type: DWORD</span></span>

<span data-ttu-id="c565b-123">Valor: 1</span><span class="sxs-lookup"><span data-stu-id="c565b-123">Value: 1</span></span>

### <span data-ttu-id="c565b-124">Distribuir avisos legales mediante la Directiva de grupo en lugar de hacerlo en la imagen MED-V</span><span class="sxs-lookup"><span data-stu-id="c565b-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="c565b-125">Si desea que los usuarios finales vean un contrato de nivel de servicio (SLA) antes de que tengan acceso a MED-V, le recomendamos que aplique el SLA mediante la Directiva de grupo más adelante para que se muestre el SLA al usuario final después de que finalice la primera configuración.</span><span class="sxs-lookup"><span data-stu-id="c565b-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="c565b-126">**PRECAUCIÓN**  Aunque un procedimiento recomendado es ejecutar la configuración por primera vez en modo **desatendido** , si decide establecer la directiva local o la entrada del registro para incluir un SLA en la imagen (disco duro virtual), también debe especificar que la primera configuración se ejecute en modo **atendido** o que la primera vez que se produzcan errores.</span><span class="sxs-lookup"><span data-stu-id="c565b-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="c565b-127">Compactar el disco duro virtual</span><span class="sxs-lookup"><span data-stu-id="c565b-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="c565b-128">Le recomendamos que compacte el disco duro virtual para recuperar espacio en disco vacío y reduzca el tamaño del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="c565b-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="c565b-129">Para obtener más información sobre cómo compactar el disco duro virtual, vea [compactar el disco duro virtual de MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="c565b-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="c565b-130">Configurar la máquina virtual para que se reinicie en pantalla azul</span><span class="sxs-lookup"><span data-stu-id="c565b-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="c565b-131">Le recomendamos que configure la máquina virtual de área de trabajo de MED-V para que se reinicie automáticamente cuando detecte un bloqueo de pantalla azul.</span><span class="sxs-lookup"><span data-stu-id="c565b-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="c565b-132">Para configurar esta opción en el invitado, establezca el valor AutoReboot en la clave HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl en "1".</span><span class="sxs-lookup"><span data-stu-id="c565b-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="c565b-133">También puede configurar esta opción si hace clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **sistema**.</span><span class="sxs-lookup"><span data-stu-id="c565b-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="c565b-134">A continuación, en el área **Inicio y recuperación** de la pestaña **avanzadas** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="c565b-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="c565b-135">Seleccione la casilla **reinicio automático** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c565b-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="c565b-136">Hacer una copia de seguridad de la imagen de MED-V antes de sellarla</span><span class="sxs-lookup"><span data-stu-id="c565b-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="c565b-137">Le recomendamos que cree una copia de seguridad de la imagen de MED-V antes de sellarla.</span><span class="sxs-lookup"><span data-stu-id="c565b-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="c565b-138">Para obtener más información sobre cómo sellar la imagen de MED-V, vea [configurar una imagen de Windows Virtual PC para Med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="c565b-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="c565b-139">Instalar Windows Virtual PC al instalar desde un archivo por lotes</span><span class="sxs-lookup"><span data-stu-id="c565b-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="c565b-140">Al instalar los componentes de MED-V mediante un archivo por lotes, especifique que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="c565b-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="c565b-141">Esto garantiza que Windows Update no cause ninguna interferencia con el proceso de instalación al requerir un reinicio.</span><span class="sxs-lookup"><span data-stu-id="c565b-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="c565b-142">Instalar el área de trabajo de MED-V desde una carpeta local</span><span class="sxs-lookup"><span data-stu-id="c565b-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="c565b-143">Debido a problemas que se pueden producir al instalar MED-V desde una ubicación de red, le recomendamos que copie los archivos de configuración del área de trabajo de MED-V localmente y, a continuación, ejecute setup.exe.</span><span class="sxs-lookup"><span data-stu-id="c565b-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="c565b-144">Administrar la redirección de la impresora solo de una manera</span><span class="sxs-lookup"><span data-stu-id="c565b-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="c565b-145">Si una impresora se instala manualmente en la máquina virtual invitado MED-V, y la misma impresora se instala posteriormente en el equipo host, el resultado es que se instala dos veces en el invitado.</span><span class="sxs-lookup"><span data-stu-id="c565b-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="c565b-146">Para evitar esta situación, le recomendamos que el procedimiento recomendado es MED-V para administrar el redireccionamiento de impresoras solo de una manera: deshabilite el redireccionamiento e instale las impresoras manualmente en el invitado, o bien habilite el redireccionamiento y no instale las impresoras de forma manual en el invitado.</span><span class="sxs-lookup"><span data-stu-id="c565b-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="c565b-147">Establecer la configuración de la revisión de invitados de MED-V</span><span class="sxs-lookup"><span data-stu-id="c565b-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="c565b-148">Puede controlar cuándo y durante cuánto tiempo despierta la máquina virtual de MED-V para recibir actualizaciones automáticas definiendo los valores de configuración pertinentes en el registro.</span><span class="sxs-lookup"><span data-stu-id="c565b-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="c565b-149">Un procedimiento recomendado de MED-V es configurar el intervalo de activación para que coincida con el momento en el que se han programado las actualizaciones regulares para las máquinas virtuales de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c565b-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="c565b-150">Además, le recomendamos que configure estas opciones de forma que se asemeje al comportamiento del equipo host.</span><span class="sxs-lookup"><span data-stu-id="c565b-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="c565b-151">Para obtener más información sobre cómo configurar las opciones para la revisión de invitados de MED-V, consulte [administrar actualizaciones automáticas para áreas de trabajo de Med-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="c565b-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="c565b-152">Configurar software antivirus y de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="c565b-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="c565b-153">Para evitar que la actividad antivirus afecte al rendimiento del escritorio virtual, le recomendamos que, cuando pueda, excluya los siguientes tipos de archivo de máquina virtual de cualquier proceso de copia de seguridad o antivirus que se ejecute en el equipo host MED-V:</span><span class="sxs-lookup"><span data-stu-id="c565b-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="c565b-154">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="c565b-154">\*.VMC</span></span>

-   <span data-ttu-id="c565b-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="c565b-155">\*.VUD</span></span>

-   <span data-ttu-id="c565b-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="c565b-156">\*.VSV</span></span>

-   <span data-ttu-id="c565b-157">\*. EXPIRA</span><span class="sxs-lookup"><span data-stu-id="c565b-157">\*.VHD</span></span>

## <span data-ttu-id="c565b-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c565b-158">Related topics</span></span>


[<span data-ttu-id="c565b-159">Seguridad y protección de MED-V</span><span class="sxs-lookup"><span data-stu-id="c565b-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





