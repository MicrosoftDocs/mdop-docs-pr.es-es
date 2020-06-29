---
title: Introducción a las herramientas de DaRT 8.0
description: Introducción a las herramientas de DaRT 8.0
author: dansimp
ms.assetid: 1766c82e-c099-47d4-b186-4689b026a7e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: a058f6018888f446782aa8f3a18ee89570840c2a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824620"
---
# <span data-ttu-id="afbfc-103">Introducción a las herramientas de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="afbfc-103">Overview of the Tools in DaRT 8.0</span></span>


<span data-ttu-id="afbfc-104">Desde la ventana conjunto de herramientas de diagnóstico **y recuperación** de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, puede iniciar cualquiera de las herramientas individuales que incluye al crear la imagen de recuperación de DART 8,0.</span><span class="sxs-lookup"><span data-stu-id="afbfc-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you can start any of the individual tools that you include when you create the DaRT 8.0 recovery image.</span></span> <span data-ttu-id="afbfc-105">Para obtener información sobre cómo obtener acceso a la ventana **conjunto de herramientas de diagnóstico y recuperación** , consulte [Cómo recuperar equipos locales con la imagen de recuperación de DART](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="afbfc-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="afbfc-106">Si está disponible, puede usar el Asistente para **soluciones** en la ventana **conjunto de herramientas de diagnóstico y recuperación** para seleccionar la herramienta que se adapte mejor a su problema particular, en función de una breve entrevista que proporciona el asistente.</span><span class="sxs-lookup"><span data-stu-id="afbfc-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="afbfc-107">Explorar las herramientas de DaRT</span><span class="sxs-lookup"><span data-stu-id="afbfc-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="afbfc-108">A continuación, se ofrece una descripción de las herramientas de DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="afbfc-108">A description of the DaRT 8.0 tools follows.</span></span>

### <span data-ttu-id="afbfc-109">Administración de equipos</span><span class="sxs-lookup"><span data-stu-id="afbfc-109">Computer Management</span></span>

<span data-ttu-id="afbfc-110">**Administración de equipos** es un conjunto de herramientas administrativas de Windows que le ayudan a solucionar problemas de equipos.</span><span class="sxs-lookup"><span data-stu-id="afbfc-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="afbfc-111">Puede usar las herramientas de **Administración de equipos** de DART para ver la información del sistema y los registros de eventos, administrar discos, Mostrar Autoruns y administrar servicios y drivers.</span><span class="sxs-lookup"><span data-stu-id="afbfc-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="afbfc-112">La consola de **Administración de equipos** está personalizada para ayudarle a diagnosticar y reparar problemas que podrían impedir el inicio del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="afbfc-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="afbfc-113">**Nota:**  No se admite la recuperación de discos dinámicos con DaRT.</span><span class="sxs-lookup"><span data-stu-id="afbfc-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="afbfc-114">Analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="afbfc-114">Crash Analyzer</span></span>

<span data-ttu-id="afbfc-115">Use el **Asistente** de análisis de bloqueo para determinar rápidamente la causa de un error en el equipo analizando el archivo de volcado de memoria en el sistema operativo Windows que está reparando.</span><span class="sxs-lookup"><span data-stu-id="afbfc-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="afbfc-116">**Crash Analyzer** examina el archivo de volcado de memoria del controlador que causó el error de un equipo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="afbfc-117">Después, puede deshabilitar el controlador de dispositivo con el problema mediante el nodo **servicios y controladores** de la herramienta **Administración de equipos** .</span><span class="sxs-lookup"><span data-stu-id="afbfc-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="afbfc-118">El **Asistente del analizador de bloqueo** requiere las herramientas de depuración para Windows y los archivos de símbolos para el sistema operativo que está reparando.</span><span class="sxs-lookup"><span data-stu-id="afbfc-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="afbfc-119">Puede incluir ambos requisitos al crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="afbfc-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="afbfc-120">Si no se incluyen en la imagen de recuperación y no tiene acceso a ellos en el equipo que está reparando, puede copiar el archivo de volcado de memoria en otro equipo y usar la versión independiente del **analizador de bloqueo** para diagnosticar el problema.</span><span class="sxs-lookup"><span data-stu-id="afbfc-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="afbfc-121">Ejecutar **Crash Analyzer** es una buena idea incluso si tiene previsto rehacer la imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="afbfc-122">La imagen podría tener un controlador defectuoso que está causando problemas en su entorno.</span><span class="sxs-lookup"><span data-stu-id="afbfc-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="afbfc-123">Al ejecutar el **analizador de bloqueo**, puede identificar los problemas y mejorar la estabilidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="afbfc-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="afbfc-124">Para obtener más información acerca del **analizador de bloqueo**, consulte [diagnosticar errores del sistema con el analizador de bloqueos](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="afbfc-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span></span>

### <span data-ttu-id="afbfc-125">Defender</span><span class="sxs-lookup"><span data-stu-id="afbfc-125">Defender</span></span>

<span data-ttu-id="afbfc-126">**Importante**  Los entornos con DaRT defender implementado deberían usar en su lugar la imagen de protección sin conexión de Microsoft defender (WDO) para la detección de malware.</span><span class="sxs-lookup"><span data-stu-id="afbfc-126">**Important** Environments with the DaRT Defender deployed should instead use the Microsoft Defender Offline (WDO) protection image for malware detection.</span></span> <span data-ttu-id="afbfc-127">Debido a la integración de la herramienta de defender en DaRT, todas las implementaciones de la versión de DaRT compatibles no pueden aplicar estas actualizaciones antimalware a sus imágenes de DaRT.</span><span class="sxs-lookup"><span data-stu-id="afbfc-127">Because of how the Defender tool integrates into DaRT, all supported DaRT version deployments cannot apply these anti-malware updates to their DaRT images.</span></span> <span data-ttu-id="afbfc-128">Para obtener más información, consulte [Microsoft Diagnostics and Recovery Toolset (DART) los usuarios deben usar Microsoft defender offline (WDO) para la detección de malware: >](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span><span class="sxs-lookup"><span data-stu-id="afbfc-128">For more information, see  [Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span></span>

 

<span data-ttu-id="afbfc-129">**Defender** puede ayudar a detectar malware y software no deseado y avisarle de los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="afbfc-129">**Defender** can help detect malware and unwanted software and warn you of security risks.</span></span> <span data-ttu-id="afbfc-130">Puede usar esta herramienta para explorar un equipo y quitar malware incluso cuando no se está ejecutando el sistema operativo Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="afbfc-130">You can use this tool to scan a computer for and remove malware even when the installed Windows operating system is not running.</span></span> <span data-ttu-id="afbfc-131">Cuando **defender** detecta software malintencionado o no deseado, le preguntará si desea quitar, poner en cuarentena o permitir para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="afbfc-131">When **Defender** detects malicious or unwanted software, it prompts you to remove, quarantine, or allow for each item.</span></span>

<span data-ttu-id="afbfc-132">El código malintencionado que usa rootkits puede enmascararse en el sistema operativo en ejecución.</span><span class="sxs-lookup"><span data-stu-id="afbfc-132">Malware that uses rootkits can mask itself from the running operating system.</span></span> <span data-ttu-id="afbfc-133">Si hay un virus o spyware habilitado para rootkits en un equipo, la mayoría de las herramientas de análisis y eliminación en tiempo real ya no podrán verlo o quitarlo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-133">If a rootkit-enabled virus or spyware is in a computer, most real-time scanning and removal tools can no longer see it or remove it.</span></span> <span data-ttu-id="afbfc-134">Como usted inicia el equipo problemático en DaRT y el sistema operativo instalado está desconectado, puede detectar el rootkit sin que sea capaz de enmascararse.</span><span class="sxs-lookup"><span data-stu-id="afbfc-134">Because you boot the problem computer into DaRT and the installed operating system is offline, you can detect the rootkit without it being able to mask itself.</span></span>

### <span data-ttu-id="afbfc-135">Disk Commander</span><span class="sxs-lookup"><span data-stu-id="afbfc-135">Disk Commander</span></span>

<span data-ttu-id="afbfc-136">**Disk Commander** le permite recuperar y reparar particiones o volúmenes de disco mediante uno de los siguientes procesos de recuperación:</span><span class="sxs-lookup"><span data-stu-id="afbfc-136">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="afbfc-137">Restaurar el registro de inicio maestro (MBR)</span><span class="sxs-lookup"><span data-stu-id="afbfc-137">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="afbfc-138">Recuperar uno o más volúmenes perdidos</span><span class="sxs-lookup"><span data-stu-id="afbfc-138">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="afbfc-139">Restaurar tablas de particiones de copia de seguridad de **Disk Commander**</span><span class="sxs-lookup"><span data-stu-id="afbfc-139">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="afbfc-140">Guardar tablas de particiones en backup de **Disk Commander**</span><span class="sxs-lookup"><span data-stu-id="afbfc-140">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="afbfc-141">**ADVERTENCIA**  Le recomendamos que haga una copia de seguridad de un disco antes de usar **Disk Commander** para repararlo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-141">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="afbfc-142">Con **Disk Commander**, puede dañar los volúmenes y hacerlos inaccesibles.</span><span class="sxs-lookup"><span data-stu-id="afbfc-142">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="afbfc-143">Además, los cambios en un volumen pueden afectar a otros volúmenes porque los volúmenes de un disco comparten una tabla de particiones.</span><span class="sxs-lookup"><span data-stu-id="afbfc-143">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="afbfc-144">**Nota:**  No se admite la recuperación de discos dinámicos con DaRT.</span><span class="sxs-lookup"><span data-stu-id="afbfc-144">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="afbfc-145">Borrado de disco</span><span class="sxs-lookup"><span data-stu-id="afbfc-145">Disk Wipe</span></span>

<span data-ttu-id="afbfc-146">Puede usar el **borrado de disco** para eliminar todos los datos de un disco o un volumen, incluso los datos que quedan después de cambiar el formato de una unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="afbfc-146">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="afbfc-147">El **borrado de disco** le permite seleccionar de una sobrescritura de paso único o de una sobrescritura de cuatro pases, que cumple con los estándares actuales del Departamento de defensa de los Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="afbfc-147">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="afbfc-148">**ADVERTENCIA**  Después de borrar un disco o un volumen, no puede recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="afbfc-148">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="afbfc-149">Compruebe el tamaño y la etiqueta de un volumen antes de borrarlo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-149">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="afbfc-150">Internet</span><span class="sxs-lookup"><span data-stu-id="afbfc-150">Explorer</span></span>

<span data-ttu-id="afbfc-151">La herramienta **Explorador** le permite examinar el sistema de archivos del equipo y los recursos compartidos de red para que pueda quitar los datos importantes que el usuario haya almacenado en la unidad local antes de intentar reparar o rehacer la imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-151">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="afbfc-152">Y como puede asignar Letras de unidad a recursos compartidos de red, puede copiar y mover fácilmente los archivos del equipo a la red para guardarlos o de la red al equipo para restaurarlos.</span><span class="sxs-lookup"><span data-stu-id="afbfc-152">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="afbfc-153">Restauración de archivos</span><span class="sxs-lookup"><span data-stu-id="afbfc-153">File Restore</span></span>

<span data-ttu-id="afbfc-154">La **restauración de archivos** le permite intentar restaurar los archivos que se han eliminado por error o que son demasiado grandes para la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="afbfc-154">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="afbfc-155">La **restauración de archivos** no se limita a los volúmenes de disco normales, pero puede buscar y restaurar archivos en volúmenes perdidos o en volúmenes cifrados con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="afbfc-155">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="afbfc-156">**Nota:**  No se admite la recuperación de discos dinámicos con DaRT.</span><span class="sxs-lookup"><span data-stu-id="afbfc-156">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="afbfc-157">Búsqueda de archivos</span><span class="sxs-lookup"><span data-stu-id="afbfc-157">File Search</span></span>

<span data-ttu-id="afbfc-158">Antes de volver a crear imágenes en un equipo, es importante recuperar los archivos del disco duro local, especialmente cuando es posible que el usuario no haya realizado una copia de seguridad ni guardado los archivos en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="afbfc-158">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="afbfc-159">La herramienta de **búsqueda** abre una ventana de **búsqueda de archivos** que puede usar para buscar documentos cuando no conoce la ruta de acceso del archivo o para buscar tipos generales de archivos en todos los discos duros locales.</span><span class="sxs-lookup"><span data-stu-id="afbfc-159">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="afbfc-160">Puede buscar patrones de nombres de archivo específicos en rutas de archivo específicas.</span><span class="sxs-lookup"><span data-stu-id="afbfc-160">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="afbfc-161">También puede limitar los resultados a un intervalo de fechas o a un intervalo de tamaño.</span><span class="sxs-lookup"><span data-stu-id="afbfc-161">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="afbfc-162">Desinstalación de Hotfix</span><span class="sxs-lookup"><span data-stu-id="afbfc-162">Hotfix Uninstall</span></span>

<span data-ttu-id="afbfc-163">El **Asistente para desinstalación de revisiones** le permite quitar revisiones o Service Packs del sistema operativo Windows en el equipo que está reparando.</span><span class="sxs-lookup"><span data-stu-id="afbfc-163">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="afbfc-164">Use esta herramienta cuando se sospeche que un hotfix o un Service Pack impide que el sistema operativo se inicie.</span><span class="sxs-lookup"><span data-stu-id="afbfc-164">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="afbfc-165">Le recomendamos que desinstale solo una revisión a la vez, aunque la herramienta le permita desinstalar más de una.</span><span class="sxs-lookup"><span data-stu-id="afbfc-165">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="afbfc-166">**Importante**  Es posible que los programas que se instalaron o actualizaron después de instalar una revisión no funcionen correctamente después de desinstalar una revisión.</span><span class="sxs-lookup"><span data-stu-id="afbfc-166">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="afbfc-167">Locksmith</span><span class="sxs-lookup"><span data-stu-id="afbfc-167">Locksmith</span></span>

<span data-ttu-id="afbfc-168">El **Asistente para locksmith** le permite establecer o cambiar la contraseña de cualquier cuenta local en el sistema operativo Windows que esté analizando o reparando.</span><span class="sxs-lookup"><span data-stu-id="afbfc-168">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="afbfc-169">No es necesario que conozcas la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="afbfc-169">You do not have to know the current password.</span></span> <span data-ttu-id="afbfc-170">Sin embargo, la contraseña que establezca debe cumplir con todos los requisitos definidos por un objeto de directiva de grupo local.</span><span class="sxs-lookup"><span data-stu-id="afbfc-170">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="afbfc-171">Esto incluye la longitud y la complejidad de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="afbfc-171">This includes password length and complexity.</span></span>

<span data-ttu-id="afbfc-172">Puede usar **locksmith** cuando se desconoce la contraseña de una cuenta local, como la cuenta de administrador local.</span><span class="sxs-lookup"><span data-stu-id="afbfc-172">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="afbfc-173">No puede usar **locksmith** para establecer contraseñas para cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="afbfc-173">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="afbfc-174">Editor del registro</span><span class="sxs-lookup"><span data-stu-id="afbfc-174">Registry Editor</span></span>

<span data-ttu-id="afbfc-175">Puede usar el **Editor del registro** para obtener acceso y cambiar el registro del sistema operativo Windows que está analizando o reparando.</span><span class="sxs-lookup"><span data-stu-id="afbfc-175">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="afbfc-176">Esto incluye agregar, quitar y modificar claves y valores, e importar archivos de registro (. reg).</span><span class="sxs-lookup"><span data-stu-id="afbfc-176">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="afbfc-177">**ADVERTENCIA**  Pueden surgir problemas graves si cambia incorrectamente el registro con el **Editor del registro**.</span><span class="sxs-lookup"><span data-stu-id="afbfc-177">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="afbfc-178">Estos problemas pueden requerir que haya que volver a instalar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-178">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="afbfc-179">Antes de realizar cambios en el registro, debe hacer una copia de seguridad de los datos valiosos del equipo.</span><span class="sxs-lookup"><span data-stu-id="afbfc-179">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="afbfc-180">Cambie el registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="afbfc-180">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="afbfc-181">Examen de SFC</span><span class="sxs-lookup"><span data-stu-id="afbfc-181">SFC Scan</span></span>

<span data-ttu-id="afbfc-182">La herramienta de **análisis SFC** inicia el **Asistente para la reparación de archivos de sistema** y le permite reparar archivos de sistema que impiden que se inicie el sistema operativo Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="afbfc-182">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="afbfc-183">El **Asistente de reparación de archivos del sistema** puede reparar automáticamente los archivos del sistema dañados o que no se encuentran, o bien puede preguntarle antes de realizar cualquier reparación.</span><span class="sxs-lookup"><span data-stu-id="afbfc-183">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="afbfc-184">Asistente para soluciones</span><span class="sxs-lookup"><span data-stu-id="afbfc-184">Solution Wizard</span></span>

<span data-ttu-id="afbfc-185">El **Asistente para soluciones** presenta una serie de preguntas y, a continuación, recomienda la mejor herramienta para la situación, en función de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="afbfc-185">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="afbfc-186">Este asistente le ayuda a determinar qué herramienta usar cuando no está familiarizado con las herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="afbfc-186">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="afbfc-187">Configuración de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="afbfc-187">TCP/IP Config</span></span>

<span data-ttu-id="afbfc-188">Cuando arranca un equipo problemático en DaRT, se configura para obtener automáticamente su configuración TCP/IP (dirección IP y servidor DNS) del Protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="afbfc-188">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="afbfc-189">Si DHCP no está disponible, puede configurar manualmente TCP/IP con la herramienta de **configuración de TCP/IP** .</span><span class="sxs-lookup"><span data-stu-id="afbfc-189">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="afbfc-190">En primer lugar, seleccione un adaptador de red y, a continuación, configure la dirección IP y el servidor DNS para ese adaptador.</span><span class="sxs-lookup"><span data-stu-id="afbfc-190">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="afbfc-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="afbfc-191">Related topics</span></span>


[<span data-ttu-id="afbfc-192">Tareas iniciales con DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="afbfc-192">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

 

 





