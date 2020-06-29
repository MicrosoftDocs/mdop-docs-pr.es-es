---
title: Identificación del número y los tipos de áreas de trabajo de MED-V
description: Identificación del número y los tipos de áreas de trabajo de MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827261"
---
# <span data-ttu-id="2c61e-103">Identificación del número y los tipos de áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c61e-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="2c61e-104">MED-V crea un entorno virtual para ejecutar aplicaciones que requieren Windows XP o que requieren una versión de Internet Explorer diferente de la de la versión del equipo host.</span><span class="sxs-lookup"><span data-stu-id="2c61e-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="2c61e-105">Este entorno virtual se conoce como área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="2c61e-106">En función de los requisitos de compatibilidad de la aplicación a los que se enfrenta la organización al migrar a Windows 7, solo algunos usuarios o departamentos pueden requerir áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="2c61e-107">Mientras planea la implementación, debe determinar el número de áreas de trabajo de MED-V que necesita su empresa.</span><span class="sxs-lookup"><span data-stu-id="2c61e-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="2c61e-108">También debe definir los requisitos de cada área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="2c61e-109">Identificar el número y los tipos de áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c61e-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="2c61e-110">Identifique los equipos y grupos de su empresa para los que va a crear áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="2c61e-111">Normalmente, estos son los usuarios que requieren acceso a las aplicaciones que no se pueden migrar a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c61e-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="2c61e-112">Identifique las aplicaciones que no se pueden migrar y los usuarios que necesitan un área de trabajo de MED-V para ejecutar estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2c61e-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="2c61e-113">Es posible que también tenga direcciones de intranet que aún no se hayan optimizado para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c61e-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="2c61e-114">El área de trabajo de MED-V proporciona un explorador Internet Explorer a través del cual los usuarios finales pueden obtener mejores acceso a las direcciones web que aún no están listas para la migración a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c61e-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="2c61e-115">Mientras está preparando y planificando su implementación de MED-V, tendrá que identificar y compilar una lista de direcciones URL para redirigir desde Internet Explorer en el equipo host a Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="2c61e-116">Por último, debe evaluar los requisitos de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="2c61e-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="2c61e-117">La mayoría de las áreas de trabajo de MED-V son de 2 gigabytes (GB) o más.</span><span class="sxs-lookup"><span data-stu-id="2c61e-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="2c61e-118">El espacio en disco disponible en un sistema se puede consumir rápidamente, según el número de usuarios y la configuración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="2c61e-119">Además, la forma preferida de distribución de su empresa puede requerir espacio adicional.</span><span class="sxs-lookup"><span data-stu-id="2c61e-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="2c61e-120">Generalmente, debe liberar un mínimo de 10 GB de espacio en disco para un área de trabajo MED-V, pero esto varía en gran medida según el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c61e-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="2c61e-121">Calcular los requisitos de espacio en disco para áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c61e-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="2c61e-122">Un área de trabajo de MED-V requiere memoria y espacio en disco del equipo host en el que está instalada.</span><span class="sxs-lookup"><span data-stu-id="2c61e-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="2c61e-123">Como mínimo, se necesitan 2 GB de espacio en disco en el host.</span><span class="sxs-lookup"><span data-stu-id="2c61e-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="2c61e-124">El espacio en disco es variable y depende del número de aplicaciones y de los datos en el área de trabajo de MED-V del usuario.</span><span class="sxs-lookup"><span data-stu-id="2c61e-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="2c61e-125">Le recomendamos un mínimo de 10 GB de espacio en disco para MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="2c61e-126">Este monto permite un área de trabajo básica de Windows XP y algunas aplicaciones y redireccionamiento web básicos instalados.</span><span class="sxs-lookup"><span data-stu-id="2c61e-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="2c61e-127">También proporciona espacio disponible para la unidad de intercambio del host.</span><span class="sxs-lookup"><span data-stu-id="2c61e-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="2c61e-128">En una configuración básica, MED-V y un área de trabajo de MED-V implementada ocupan hasta 6 GB.</span><span class="sxs-lookup"><span data-stu-id="2c61e-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="2c61e-129">Si incluye una gran cantidad de aplicaciones en el área de trabajo de MED-V o tiene más de un usuario por equipo, puede usar el siguiente cálculo para determinar con mayor precisión el espacio en disco que necesita su área de trabajo de MED-V:</span><span class="sxs-lookup"><span data-stu-id="2c61e-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="2c61e-130">Base VHD + (usuario por equipo x (diferencia de disco + estado guardado))</span><span class="sxs-lookup"><span data-stu-id="2c61e-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="2c61e-131">Para calcular el espacio en disco necesario, determine lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2c61e-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="2c61e-132">**Tamaño del VHD base** : el disco duro virtual que se usó para crear el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="2c61e-133">**Importante**  No use el tamaño de archivo. medv para el cálculo porque el archivo. medv está comprimido.</span><span class="sxs-lookup"><span data-stu-id="2c61e-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="2c61e-134">**Usuarios por equipo** : Med-v crea un área de trabajo de Med-v para cada usuario de un equipo; el área de trabajo de MED-V consume espacio en disco cuando cada usuario inicia sesión y se crea el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="2c61e-135">**Tamaño del disco de diferenciación** : se usa para realizar un seguimiento de la diferencia entre el VHD de base.</span><span class="sxs-lookup"><span data-stu-id="2c61e-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="2c61e-136">Este tamaño varía a medida que se agregan aplicaciones y actualizaciones de software en el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="2c61e-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="2c61e-137">Se crea un disco de diferenciación para cada usuario de MED-V cuando inicia MED-V por primera vez.</span><span class="sxs-lookup"><span data-stu-id="2c61e-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="2c61e-138">**Tamaño del archivo de estado guardado** : se usa para mantener el estado en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2c61e-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="2c61e-139">Por lo general, este es un poco más grande que la memoria RAM asignada para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2c61e-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="2c61e-140">Por ejemplo, 1 GB de RAM asignada crea un archivo sobre 1.081.000 KB.</span><span class="sxs-lookup"><span data-stu-id="2c61e-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="2c61e-141">En el ejemplo siguiente se muestra un cálculo basado en tres usuarios de un área de trabajo de MED-V que tiene un disco duro virtual de 2,6 GB:</span><span class="sxs-lookup"><span data-stu-id="2c61e-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="2c61e-142">2,6 GB + (3 x (1,5 GB + 1 GB)) = 10.1 GB</span><span class="sxs-lookup"><span data-stu-id="2c61e-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="2c61e-143">**Nota:**  Una práctica recomendada de MED-V es calcular el espacio necesario mediante una implementación de laboratorio para validar los requisitos.</span><span class="sxs-lookup"><span data-stu-id="2c61e-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="2c61e-144">Buscar los archivos para determinar el tamaño de archivo</span><span class="sxs-lookup"><span data-stu-id="2c61e-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="2c61e-145">Las siguientes ubicaciones contienen los archivos de la configuración del usuario y del equipo:</span><span class="sxs-lookup"><span data-stu-id="2c61e-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2c61e-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c61e-146">Type</span></span></th>
<th align="left"><span data-ttu-id="2c61e-147">Ubicación</span><span class="sxs-lookup"><span data-stu-id="2c61e-147">Location</span></span></th>
<th align="left"><span data-ttu-id="2c61e-148">Archivos</span><span class="sxs-lookup"><span data-stu-id="2c61e-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c61e-149">VHD base</span><span class="sxs-lookup"><span data-stu-id="2c61e-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c61e-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="2c61e-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="2c61e-151">InternalName </em> . vhd: donde <em> InternalName </em> es el nombre del disco duro virtual que seleccionó en el empaquetador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2c61e-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c61e-152">Disco de diferenciación</span><span class="sxs-lookup"><span data-stu-id="2c61e-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c61e-153">Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="2c61e-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="2c61e-154">WorkspaceName </em> . vhd</span><span class="sxs-lookup"><span data-stu-id="2c61e-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c61e-155">Archivo de estado guardado</span><span class="sxs-lookup"><span data-stu-id="2c61e-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c61e-156">Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="2c61e-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="2c61e-157">WorkspaceName </em> . VSV</span><span class="sxs-lookup"><span data-stu-id="2c61e-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2c61e-158">Calcular los requisitos de espacio en disco para áreas de trabajo compartidas de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c61e-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="2c61e-159">Si está calculando una implementación de un área de trabajo de MED-V compartida en un único equipo, el número de usuarios por equipo en el cálculo es siempre "1", ya que MED-V solo configura un único disco de diferenciación para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="2c61e-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="2c61e-160">Puede encontrar el disco de diferenciación y el archivo de estado guardado para áreas de trabajo compartidas de MED-V en%ProgramData%\\Microsoft\\Medv\\AllUsers.</span><span class="sxs-lookup"><span data-stu-id="2c61e-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="2c61e-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c61e-161">Related topics</span></span>


[<span data-ttu-id="2c61e-162">Definir y planificar la implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c61e-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="2c61e-163">Planificación de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c61e-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





