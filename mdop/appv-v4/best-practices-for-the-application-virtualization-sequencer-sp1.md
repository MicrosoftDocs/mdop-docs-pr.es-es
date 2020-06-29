---
title: Procedimientos recomendados para el secuenciador de virtualización de aplicaciones
description: Procedimientos recomendados para el secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822000"
---
# <span data-ttu-id="c1807-103">Procedimientos recomendados para el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c1807-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="c1807-104">En este tema se proporcionan los procedimientos recomendados para ejecutar el secuenciador de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="c1807-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="c1807-105">Revise y tenga en cuenta las siguientes recomendaciones al planear y usar el secuenciador en su entorno.</span><span class="sxs-lookup"><span data-stu-id="c1807-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="c1807-106">Procedimientos recomendados de configuración de la secuencia de equipos</span><span class="sxs-lookup"><span data-stu-id="c1807-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="c1807-107">Es necesario tener en cuenta los siguientes procedimientos recomendados al configurar el equipo que ejecuta el secuenciador de App-V:</span><span class="sxs-lookup"><span data-stu-id="c1807-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="c1807-108">Secuencia en un equipo que tenga una configuración similar y que esté ejecutando una versión anterior del sistema operativo que los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="c1807-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="c1807-109">Asegúrese de que el equipo que ejecuta el secuenciador ejecuta una versión anterior del sistema operativo que los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="c1807-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="c1807-110">Esto incluye el Service Pack y las versiones de actualización.</span><span class="sxs-lookup"><span data-stu-id="c1807-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="c1807-111">Por ejemplo, si los equipos de destino ejecutan vista y WindowsXP, debe secuenciar las aplicaciones en un equipo que ejecute WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="c1807-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="c1807-112">No se garantiza la posibilidad de realizar una secuencia en un sistema operativo y ejecutar la aplicación virtualizada en un sistema operativo diferente, y depende de la aplicación y el sistema operativo en particular.</span><span class="sxs-lookup"><span data-stu-id="c1807-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="c1807-113">Si encuentra problemas, es posible que tenga que realizar una secuencia en el mismo entorno de sistema operativo que el cliente de App-V que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c1807-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="c1807-114">Configure el equipo que ejecuta el secuenciador con varias particiones.</span><span class="sxs-lookup"><span data-stu-id="c1807-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="c1807-115">Debe configurar el equipo que ejecuta el secuenciador con al menos dos particiones primarias.</span><span class="sxs-lookup"><span data-stu-id="c1807-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="c1807-116">La primera partición (**C:**) debe contener el sistema operativo y debe tener el formato del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="c1807-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="c1807-117">La segunda partición (**Q:**) se usa como la ruta de acceso de destino para la instalación de la aplicación virtual y también se debe dar formato con el sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="c1807-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="c1807-118">Configure el directorio Temp con suficiente espacio libre en el disco.</span><span class="sxs-lookup"><span data-stu-id="c1807-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="c1807-119">El secuenciador utiliza el directorio **% tmp%** o **% temp%** y el directorio de **borradores** para almacenar los archivos temporales durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="c1807-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="c1807-120">Debe configurar estos directorios en el equipo que ejecuta el secuenciador con espacio libre en el disco equivalente a los requisitos estimados de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1807-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="c1807-121">Para comprobar la ubicación del directorio de **borrador** , abra la consola del secuenciador y seleccione **herramientas**, **Opciones**y, a continuación, seleccione la pestaña **rutas** . la configuración de los directorios temporales y el directorio de **borrador** en particiones de disco duro diferentes puede mejorar el rendimiento durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="c1807-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="c1807-122">Secuenciar aplicaciones con Microsoft VirtualPC.</span><span class="sxs-lookup"><span data-stu-id="c1807-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="c1807-123">La mayoría de las aplicaciones se secuencian más de una vez.</span><span class="sxs-lookup"><span data-stu-id="c1807-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="c1807-124">Para ayudarle a simplificarlo, debe considerar la posibilidad de realizar secuencias en un equipo que funcione en un entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="c1807-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="c1807-125">Esto le permitirá secuenciar una aplicación y volver a un estado limpio, con una reconfiguración mínima, en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="c1807-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="c1807-126">Si está ejecutando Microsoft Hyper-V en su entorno, el secuenciador de App-V se ejecutará cuando el equipo virtual Hyper-V en el que se esté ejecutando sea:</span><span class="sxs-lookup"><span data-stu-id="c1807-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="c1807-127">pausado y reanudado.</span><span class="sxs-lookup"><span data-stu-id="c1807-127">paused and resumed.</span></span>

    -   <span data-ttu-id="c1807-128">tiene su estado guardado y restaurado.</span><span class="sxs-lookup"><span data-stu-id="c1807-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="c1807-129">se ha guardado como una instantánea y se ha restaurado.</span><span class="sxs-lookup"><span data-stu-id="c1807-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="c1807-130">migrado a hardware diferente como parte de una migración en vivo.</span><span class="sxs-lookup"><span data-stu-id="c1807-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="c1807-131">Antes de secuenciar una nueva aplicación, cierre otros programas que se estén ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c1807-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="c1807-132">Los procesos y las tareas programadas que normalmente se ejecutan en el equipo de secuencias pueden ralentizar el proceso de secuencia y provocar que se recopilen datos irrelevantes durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="c1807-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="c1807-133">Antes de comenzar a realizar la secuencia, se deben cerrar todas las aplicaciones y programas innecesarios.</span><span class="sxs-lookup"><span data-stu-id="c1807-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="c1807-134">Secuencia en un equipo que ejecuta servicios de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="c1807-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="c1807-135">No debe configurar el modo de instalación en un equipo que ejecuta servicios de terminal antes de instalar el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="c1807-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="c1807-136">Procedimientos recomendados para la secuencia</span><span class="sxs-lookup"><span data-stu-id="c1807-136">Sequencing Best Practices</span></span>


<span data-ttu-id="c1807-137">Al secuenciar una nueva aplicación, deben tenerse en cuenta los siguientes procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="c1807-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="c1807-138">**Nota:**  Si está ejecutando App-V 4,6 SP1, no necesita secuenciar a un directorio que siga la Convención de nomenclatura de 8,3.</span><span class="sxs-lookup"><span data-stu-id="c1807-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="c1807-139">Secuencia a un directorio único que sigue la Convención de nomenclatura de 8,3.</span><span class="sxs-lookup"><span data-stu-id="c1807-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="c1807-140">Debe secuenciar todas las aplicaciones en un directorio que siga la Convención de nomenclatura de 8,3.</span><span class="sxs-lookup"><span data-stu-id="c1807-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="c1807-141">El nombre de directorio especificado no puede contener más de ocho caracteres, seguido de una extensión de nombre de archivo de tres caracteres; por ejemplo, **Q:\\MYAPP. ABC**.</span><span class="sxs-lookup"><span data-stu-id="c1807-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="c1807-142">Secuencia en una carpeta de destino en la raíz de la unidad, no en un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="c1807-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="c1807-143">Si el conjunto de aplicaciones tiene varias partes, Instale cada aplicación en un subdirectorio del directorio principal.</span><span class="sxs-lookup"><span data-stu-id="c1807-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="c1807-144">Por ejemplo, si un paquete contiene una aplicación junto con un cliente, use **Q:\\AppSuite** como directorio principal y ordene la aplicación principal a **Q:\\AppSuite\\Main**, y ordene el cliente a **Q:\\AppSuite\\Client**.</span><span class="sxs-lookup"><span data-stu-id="c1807-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="c1807-145">Configure y pruebe la aplicación durante la fase de instalación.</span><span class="sxs-lookup"><span data-stu-id="c1807-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="c1807-146">Completar la instalación de una aplicación a menudo requiere realizar varios pasos manuales que no forman parte del proceso de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1807-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="c1807-147">Estos pasos pueden implicar la configuración de una conexión a una base de datos o la copia de archivos actualizados.</span><span class="sxs-lookup"><span data-stu-id="c1807-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="c1807-148">Debe realizar estas configuraciones durante la fase de instalación y, a continuación, ejecutar la aplicación para asegurarse de que funciona.</span><span class="sxs-lookup"><span data-stu-id="c1807-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="c1807-149">Ejecute la aplicación varias veces si es necesario, hasta que el programa sea estable.</span><span class="sxs-lookup"><span data-stu-id="c1807-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="c1807-150">Debe ejecutar la aplicación varias veces durante la instalación para asegurarse de que se han completado todas las configuraciones de registro y de cuadro de diálogo asociadas.</span><span class="sxs-lookup"><span data-stu-id="c1807-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="c1807-151">Si abres la aplicación varias veces durante la instalación, se asegurará de que solo se cargan las características de la aplicación correspondiente en el **bloque de características principal**.</span><span class="sxs-lookup"><span data-stu-id="c1807-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="c1807-152">Deshabilite todas las características de actualizaciones automáticas asociadas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1807-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="c1807-153">Algunas aplicaciones tienen la capacidad de comprobar las actualizaciones más recientes de forma automática durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c1807-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="c1807-154">Para ayudarle con el control de versiones de paquetes de aplicaciones virtuales, debe deshabilitar esta característica durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="c1807-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="c1807-155">Si hay actualizaciones necesarias, deberás secuenciar un nuevo paquete de aplicación virtual con las actualizaciones asociadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="c1807-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="c1807-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1807-156">Related topics</span></span>


[<span data-ttu-id="c1807-157">Planificación de la implementación del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c1807-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





