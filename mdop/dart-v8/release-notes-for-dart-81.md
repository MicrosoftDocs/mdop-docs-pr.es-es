---
title: Notas de la versión de DaRT 8.1
description: Notas de la versión de DaRT 8.1
author: dansimp
ms.assetid: 44303107-60f4-485c-848a-7e0529f142d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d0ba817ddd5bbdefcf7fed833f4c47e7b9d9ce0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824761"
---
# <span data-ttu-id="50928-103">Notas de la versión de DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="50928-103">Release Notes for DaRT 8.1</span></span>


**<span data-ttu-id="50928-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="50928-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="50928-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 8,1.</span><span class="sxs-lookup"><span data-stu-id="50928-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1.</span></span>

<span data-ttu-id="50928-106">Estas notas de la versión contienen información necesaria para instalar correctamente los diagnósticos y el conjunto de herramientas de recuperación 8,1.</span><span class="sxs-lookup"><span data-stu-id="50928-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.1.</span></span> <span data-ttu-id="50928-107">Las notas de la versión también contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="50928-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="50928-108">Si hay una diferencia entre estas notas de la versión y otra documentación de DaRT, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="50928-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="50928-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="50928-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="50928-110">Problemas conocidos con DaRT 8,1</span><span class="sxs-lookup"><span data-stu-id="50928-110">Known issues with DaRT 8.1</span></span>


### <span data-ttu-id="50928-111">Disk Commander no puede reparar un registro de inicio maestro dañado en una partición física en Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="50928-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 8.1</span></span>

<span data-ttu-id="50928-112">En Windows 8,1, la opción "restaurar el registro de inicio maestro (MBR) o el encabezado de la tabla de particiones GUID (GPT)" en Disk Commander no puede reparar un registro de inicio maestro dañado en una partición física y, por lo tanto, no puede arrancar el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="50928-112">In Windows 8.1, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="50928-113">**Solución alternativa:** Inicie **reparación de inicio**, haga clic en **solución de problemas**, **Opciones avanzadas**y, a continuación, haga clic en **iniciar reparación**.</span><span class="sxs-lookup"><span data-stu-id="50928-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="50928-114">Varias instancias de borrado de disco dirigidas a la misma unidad hacen que todas las instancias, excepto la última, notifiquen un error</span><span class="sxs-lookup"><span data-stu-id="50928-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="50928-115">Si inicia varias instancias de borrado de disco y, a continuación, intenta borrar la misma unidad con dos instancias de borrado de disco separadas, todas las instancias excepto la última informarán de que se ha producido un error al borrar la unidad.</span><span class="sxs-lookup"><span data-stu-id="50928-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="50928-116">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="50928-116">**Workaround:** None.</span></span>

### <span data-ttu-id="50928-117">El borrado del disco puede no borrar todos los datos de las unidades de estado sólido que tienen memoria Flash</span><span class="sxs-lookup"><span data-stu-id="50928-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="50928-118">Si usa el borrado de disco para borrar los datos en una unidad de estado sólido (SSD) que tiene memoria Flash, es posible que no se eliminen todos los datos.</span><span class="sxs-lookup"><span data-stu-id="50928-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="50928-119">Este problema se produce porque el firmware SSD controla la ubicación física de las escrituras mientras se ejecuta el borrador de disco.</span><span class="sxs-lookup"><span data-stu-id="50928-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="50928-120">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="50928-120">**Workaround:** None.</span></span>

### <span data-ttu-id="50928-121">Restaurar sistema falla al ejecutar el Asistente para locksmith o el editor del registro</span><span class="sxs-lookup"><span data-stu-id="50928-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="50928-122">Si ejecuta el Asistente de locksmith, el editor del registro y posiblemente otras herramientas, se producirá un error en Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="50928-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="50928-123">**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="50928-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="50928-124">El comprobador de archivos de sistema (SFC) no se puede ejecutar después de iniciar y cerrar el Asistente de locksmith o la administración de equipos</span><span class="sxs-lookup"><span data-stu-id="50928-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="50928-125">Si inicia y cierra Asistente para locksmith o herramientas en administración de equipos, el comprobador de archivos de sistema no podrá ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="50928-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="50928-126">**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie el comprobador de archivos de sistema.</span><span class="sxs-lookup"><span data-stu-id="50928-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="50928-127">El instalador de DaRT no falla cuando no está instalado el Windows Assessment and Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="50928-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="50928-128">Si instala DaRT 8,1 mediante la línea de comandos para ejecutar Windows Installer (. msi) y no se ha instalado el Windows Assessment and Deployment Kit (WindowsADK), la instalación de DaRT debería fallar.</span><span class="sxs-lookup"><span data-stu-id="50928-128">If you install DaRT 8.1 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="50928-129">En la actualidad, el instalador de DaRT 8,1 instala todos los componentes excepto la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="50928-129">Currently, the DaRT 8.1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="50928-130">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="50928-130">**Workaround:** None.</span></span>

### <span data-ttu-id="50928-131">Windows Defender no se puede iniciar una vez iniciado el Asistente para locksmith, el editor del registro, el analizador de bloqueo y la administración de equipos</span><span class="sxs-lookup"><span data-stu-id="50928-131">Windows Defender cannot start after Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management are started</span></span>

<span data-ttu-id="50928-132">Windows Defender no se inicia si ya ha iniciado el Asistente de locksmith, el editor del registro, el analizador de bloqueo y la administración de equipos.</span><span class="sxs-lookup"><span data-stu-id="50928-132">Windows Defender does not start if you have already started Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="50928-133">**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="50928-133">**Workaround:** Close and restart DaRT, and then start Windows Defender.</span></span>

### <span data-ttu-id="50928-134">Windows Defender puede tardar más en iniciarse</span><span class="sxs-lookup"><span data-stu-id="50928-134">Windows Defender may be slow to start</span></span>

<span data-ttu-id="50928-135">En ocasiones, Windows Defender tarda unos minutos en iniciarse.</span><span class="sxs-lookup"><span data-stu-id="50928-135">Windows Defender sometimes takes a few minutes to start.</span></span> <span data-ttu-id="50928-136">La barra de progreso indica el estado de carga actual.</span><span class="sxs-lookup"><span data-stu-id="50928-136">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="50928-137">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="50928-137">**Workaround:** None.</span></span>

## <span data-ttu-id="50928-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50928-138">Related topics</span></span>


[<span data-ttu-id="50928-139">Acerca de DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="50928-139">About DaRT 8.1</span></span>](about-dart-81.md)

 

 





