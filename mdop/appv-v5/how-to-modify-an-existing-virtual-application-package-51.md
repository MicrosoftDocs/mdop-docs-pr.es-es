---
title: Cómo modificar un paquete de aplicaciones virtuales existentes
description: Cómo modificar un paquete de aplicaciones virtuales existentes
author: dansimp
ms.assetid: 6cdeec00-e4fe-4210-b4c7-6ca1ac643ddd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 95963610c8b725412f6d516ee22b1c2f4e186df6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813863"
---
# <span data-ttu-id="5df62-103">Cómo modificar un paquete de aplicaciones virtuales existentes</span><span class="sxs-lookup"><span data-stu-id="5df62-103">How to Modify an Existing Virtual Application Package</span></span>


<span data-ttu-id="5df62-104">En este tema se explica cómo:</span><span class="sxs-lookup"><span data-stu-id="5df62-104">This topic explains how to:</span></span>

-   [<span data-ttu-id="5df62-105">Actualizar una aplicación en un paquete de aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="5df62-105">Update an application in an existing virtual application package</span></span>](#bkmk-update-app-in-pkg)

-   [<span data-ttu-id="5df62-106">Modificar las propiedades asociadas a un paquete de aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="5df62-106">Modify the properties associated with an existing virtual application package</span></span>](#bkmk-chg-props-in-pkg)

-   [<span data-ttu-id="5df62-107">Agregar una nueva aplicación a un paquete de aplicaciones virtual existente</span><span class="sxs-lookup"><span data-stu-id="5df62-107">Add a new application to an existing virtual application package</span></span>](#bkmk-add-app-to-pkg)

**<span data-ttu-id="5df62-108">Antes de actualizar un paquete:</span><span class="sxs-lookup"><span data-stu-id="5df62-108">Before you update a package:</span></span>**

-   <span data-ttu-id="5df62-109">Asegúrese de que ha instalado el secuenciador Microsoft Application Virtualization (App-V), que es necesario para modificar un paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="5df62-109">Ensure that you’ve installed the Microsoft Application Virtualization (App-V) Sequencer, which is required for modifying a virtual application package.</span></span> <span data-ttu-id="5df62-110">Para instalar el secuenciador de App-V, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="5df62-110">To install the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

-   <span data-ttu-id="5df62-111">Guarde el archivo. appv en una ubicación segura y confíe siempre en el origen antes de intentar abrir el paquete para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="5df62-111">Save the .appv file in a secure location and always trust the source before trying to open the package for editing.</span></span>

-   <span data-ttu-id="5df62-112">La sección autoridad de administración se quita erróneamente del archivo de configuración de implementación al actualizar un paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-112">The Managing Authority section is erroneously removed from the deployment configuration file when you update a package.</span></span> <span data-ttu-id="5df62-113">Antes de iniciar la actualización, copie la sección autoridad de administración del archivo de configuración de implementación existente y, a continuación, pegue la sección copiada en el nuevo archivo de configuración una vez completada la conversión.</span><span class="sxs-lookup"><span data-stu-id="5df62-113">Before starting the update, copy the Managing Authority section from the existing deployment configuration file, and then paste the copied section into the new configuration file after the conversion is complete.</span></span>

-   <span data-ttu-id="5df62-114">Si hace clic en **modificar un paquete de aplicación virtual existente** en el secuenciador para editar un paquete, pero no realiza cambios y cierra el paquete, cambiará el comportamiento de la transmisión por secuencias del paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-114">If you click **Modify an Existing Virtual Application Package** in the Sequencer in order to edit a package, but then make no changes and close the package, the streaming behavior of the package is changed.</span></span> <span data-ttu-id="5df62-115">El bloque de características principal se quita del archivo de StreamMap.xml y se quitan todos los archivos enumerados en el bloque de características de publicación.</span><span class="sxs-lookup"><span data-stu-id="5df62-115">The primary feature block is removed from the StreamMap.xml file, and any files that were listed in the publishing feature block are removed.</span></span> <span data-ttu-id="5df62-116">Usuarios que reciban la experiencia de paquete editada como si se tratara de errores de flujo, independientemente de cómo se haya configurado el paquete original.</span><span class="sxs-lookup"><span data-stu-id="5df62-116">Users who receive the edited package experience that package as if it were stream-faulted, regardless of how the original package was configured.</span></span>

<a href="" id="bkmk-update-app-in-pkg"></a>**<span data-ttu-id="5df62-117">Actualizar una aplicación en un paquete de aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="5df62-117">Update an application in an existing virtual application package</span></span>**

1.  <span data-ttu-id="5df62-118">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**, seleccione **Microsoft Application Virtualization**y, a continuación, haga clic en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="5df62-118">On the computer that runs the sequencer, click **All Programs**, point to **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5df62-119">En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente** a &gt; **continuación**.</span><span class="sxs-lookup"><span data-stu-id="5df62-119">In the App-V Sequencer, click **Modify an Existing Virtual Application Package** &gt; **Next**.</span></span>

3.  <span data-ttu-id="5df62-120">En la página **seleccionar tarea** , haga clic en **actualizar la aplicación en el paquete existente** &gt; **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-120">On the **Select Task** page, click **Update Application in Existing Package** &gt; **Next**.</span></span>

4.  <span data-ttu-id="5df62-121">En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual que contiene la aplicación que desea actualizar y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-121">On the **Select Package** page, click **Browse** to locate the virtual application package that contains the application to update, and then click **Next**.</span></span>

5.  <span data-ttu-id="5df62-122">En la página **preparar el equipo** , revise los problemas que podrían provocar errores en la actualización de la aplicación o que la aplicación actualizada contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="5df62-122">On the **Prepare Computer** page, review the issues that could cause the application update to fail or cause the updated application to contain unnecessary data.</span></span> <span data-ttu-id="5df62-123">Solucione todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5df62-123">Resolve all potential issues before you continue.</span></span> <span data-ttu-id="5df62-124">Después de realizar correcciones y resolver todos los problemas potenciales, haga clic en **Actualizar** &gt; **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-124">After making any corrections and resolving all potential issues, click **Refresh** &gt; **Next**.</span></span>

    <span data-ttu-id="5df62-125">**Importante**  Si se le pide que deshabilite el software de detección de virus, primero examine el equipo que ejecuta el secuenciador para asegurarse de que no se agreguen archivos no deseados ni malintencionados al paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-125">**Important** If you are required to disable virus scanning software, first scan the computer that runs the sequencer to ensure that no unwanted or malicious files are added to the package.</span></span>

6.  <span data-ttu-id="5df62-126">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de actualización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5df62-126">On the **Select Installer** page, click **Browse** and specify the update installation file for the application.</span></span> <span data-ttu-id="5df62-127">Si la actualización no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-127">If the update does not have an associated installer file, and if you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

7.  <span data-ttu-id="5df62-128">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede proceder a instalar la actualización de la aplicación para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="5df62-128">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application update so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="5df62-129">Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**y, a continuación, busque y ejecute los archivos de instalación adicionales.</span><span class="sxs-lookup"><span data-stu-id="5df62-129">If additional installation files must be run as part of the installation, click **Run**, and then locate and run the additional installation files.</span></span> <span data-ttu-id="5df62-130">Cuando haya finalizado la instalación, seleccione **he terminado de instalar**.</span><span class="sxs-lookup"><span data-stu-id="5df62-130">When you are finished with the installation, select **I am finished installing**.</span></span> <span data-ttu-id="5df62-131">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-131">Click **Next**.</span></span>

    <span data-ttu-id="5df62-132">**Nota:**  El secuenciador supervisa todos los cambios e instalaciones que se producen en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="5df62-132">**Note** The sequencer monitors all changes and installations that occur on the computer that runs the sequencer.</span></span> <span data-ttu-id="5df62-133">Esto incluye los cambios y las instalaciones que se realizan fuera del asistente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="5df62-133">This includes any changes and installations that are performed outside of the sequencing wizard.</span></span>

8.  <span data-ttu-id="5df62-134">En la página del **Informe de instalación** , puede revisar la información sobre la aplicación virtual actualizada.</span><span class="sxs-lookup"><span data-stu-id="5df62-134">On the **Installation Report** page, you can review information about the updated virtual application.</span></span> <span data-ttu-id="5df62-135">En **información adicional**, haga doble clic en el evento para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="5df62-135">In **Additional Information**, double-click the event to obtain more detailed information.</span></span> <span data-ttu-id="5df62-136">Para continuar, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-136">To proceed, click **Next**.</span></span>

9.  <span data-ttu-id="5df62-137">En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5df62-137">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="5df62-138">Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5df62-138">It can take several minutes for all of the applications to run.</span></span> <span data-ttu-id="5df62-139">Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-139">After all applications have run, close each of the applications, and then click **Next**.</span></span>

    <span data-ttu-id="5df62-140">**Nota:**  Puede detener la carga de una aplicación durante este paso.</span><span class="sxs-lookup"><span data-stu-id="5df62-140">**Note** You can stop an application from loading during this step.</span></span> <span data-ttu-id="5df62-141">En el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener**y, a continuación, seleccione **detener todas las aplicaciones** o **detener solo esta aplicación**.</span><span class="sxs-lookup"><span data-stu-id="5df62-141">In the **Application Launch** dialog box, click **Stop**, and then select either **Stop all applications** or **Stop this application only**.</span></span>   

10. <span data-ttu-id="5df62-142">En la página **crear paquete** , para modificar el paquete sin guardarlo, active la casilla de verificación **continuar para modificar el paquete sin guardar con el editor de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="5df62-142">On the **Create Package** page, to modify the package without saving it, select the check box for **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="5df62-143">Cuando selecciona esta opción, el paquete se abre en la consola del secuenciador de App-V, donde puede modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="5df62-143">When you select this option, the package opens in the App-V Sequencer console, where you can modify the package before it is saved.</span></span> <span data-ttu-id="5df62-144">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-144">Click **Next**.</span></span>

    <span data-ttu-id="5df62-145">Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora.</span><span class="sxs-lookup"><span data-stu-id="5df62-145">To save the package immediately, select the default **Save the package now**.</span></span> <span data-ttu-id="5df62-146">Agregue **comentarios** opcionales para asociarlos con el paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-146">Add optional **Comments** to associate with the package.</span></span> <span data-ttu-id="5df62-147">Los comentarios son útiles para identificar la versión de la aplicación y proporcionar otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-147">Comments are useful to identify the application version and provide other information about the package.</span></span> <span data-ttu-id="5df62-148">También se muestra la **Ubicación de almacenamiento** predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5df62-148">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="5df62-149">Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="5df62-149">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="5df62-150">Haga clic en **Crear**.</span><span class="sxs-lookup"><span data-stu-id="5df62-150">Click **Create**.</span></span>

11. <span data-ttu-id="5df62-151">En la página de **finalización** , haga clic en **cerrar** para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="5df62-151">On the **Completion** page, click **Close** to close the wizard.</span></span> <span data-ttu-id="5df62-152">El paquete está ahora disponible en el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="5df62-152">The package is now available in the sequencer.</span></span>

<a href="" id="bkmk-chg-props-in-pkg"></a>**<span data-ttu-id="5df62-153">Modificar las propiedades asociadas a un paquete de aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="5df62-153">Modify the properties associated with an existing virtual application package</span></span>**

1.  <span data-ttu-id="5df62-154">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**, seleccione **Microsoft Application Virtualization**y, a continuación, haga clic en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="5df62-154">On the computer that runs the sequencer, click **All Programs**, point to **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5df62-155">En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente** a &gt; **continuación**.</span><span class="sxs-lookup"><span data-stu-id="5df62-155">In the App-V Sequencer, click **Modify an Existing Virtual Application Package** &gt; **Next**.</span></span>

3.  <span data-ttu-id="5df62-156">En la página **seleccionar tarea** , haga clic en **Editar paquete** &gt; **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-156">On the **Select Task** page, click **Edit Package** &gt; **Next**.</span></span>

4.  <span data-ttu-id="5df62-157">En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual que contiene las propiedades de la aplicación que desea modificar y, a continuación, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="5df62-157">On the **Select Package** page, click **Browse** to locate the virtual application package that contains the application properties to modify, and then click **Edit**.</span></span>

5.  <span data-ttu-id="5df62-158">En la consola del secuenciador de App-V, realice cualquiera de las siguientes tareas según sea necesario:</span><span class="sxs-lookup"><span data-stu-id="5df62-158">In the App-V Sequencer console, perform any of the following tasks as needed:</span></span>

    -   <span data-ttu-id="5df62-159">Importar y exportar el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="5df62-159">Import and export the manifest file.</span></span>

    -   <span data-ttu-id="5df62-160">Habilitar o deshabilitar objetos auxiliares del explorador.</span><span class="sxs-lookup"><span data-stu-id="5df62-160">Enable or disable Browser Helper Objects.</span></span>

    -   <span data-ttu-id="5df62-161">Importar o exportar un archivo VFS.</span><span class="sxs-lookup"><span data-stu-id="5df62-161">Import or export a VFS file.</span></span>

    -   <span data-ttu-id="5df62-162">Importar un directorio al sistema de archivos virtual.</span><span class="sxs-lookup"><span data-stu-id="5df62-162">Import a directory into the virtual file system.</span></span>

    -   <span data-ttu-id="5df62-163">Importar y exportar claves de registro virtuales.</span><span class="sxs-lookup"><span data-stu-id="5df62-163">Import and export virtual registry keys.</span></span>

    -   <span data-ttu-id="5df62-164">Ver las propiedades del paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-164">View package properties.</span></span>

    -   <span data-ttu-id="5df62-165">Ver archivos de paquetes asociados.</span><span class="sxs-lookup"><span data-stu-id="5df62-165">View associated package files.</span></span>

    -   <span data-ttu-id="5df62-166">Edite la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="5df62-166">Edit registry settings.</span></span>

    -   <span data-ttu-id="5df62-167">Revise la configuración adicional del paquete (excepto las propiedades del archivo del sistema operativo).</span><span class="sxs-lookup"><span data-stu-id="5df62-167">Review additional package settings (except operating system file properties).</span></span>

    -   <span data-ttu-id="5df62-168">Establezca el estado de la clave del registro virtualizado (override or Merge).</span><span class="sxs-lookup"><span data-stu-id="5df62-168">Set virtualized registry key state (override or merge).</span></span>

    -   <span data-ttu-id="5df62-169">Establecer el estado de carpeta virtualizado.</span><span class="sxs-lookup"><span data-stu-id="5df62-169">Set virtualized folder state.</span></span>

    -   <span data-ttu-id="5df62-170">Agregar o editar accesos directos y asociaciones de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="5df62-170">Add or edit shortcuts and file type associations.</span></span>

        <span data-ttu-id="5df62-171">**Nota:**  Para modificar los accesos directos o las asociaciones de los tipos de archivo, primero debe abrir el paquete para actualizar para agregar una nueva aplicación y, a continuación, ir a la página de edición final.</span><span class="sxs-lookup"><span data-stu-id="5df62-171">**Note** To edit shortcuts or file type associations, you must first open the package for upgrade to add a new application, and then proceed to the final editing page.</span></span>

6.  <span data-ttu-id="5df62-172">Cuando termine de cambiar las propiedades del paquete, **File** haga clic en &gt; **Guardar** archivo para guardar el paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-172">When you finish changing the package properties, click **File** &gt; **Save** to save the package.</span></span>

<a href="" id="bkmk-add-app-to-pkg"></a>**<span data-ttu-id="5df62-173">Agregar una nueva aplicación a un paquete de aplicaciones virtual existente</span><span class="sxs-lookup"><span data-stu-id="5df62-173">Add a new application to an existing virtual application package</span></span>**

1.  <span data-ttu-id="5df62-174">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**, seleccione **Microsoft Application Virtualization**y, a continuación, haga clic en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="5df62-174">On the computer that runs the sequencer, click **All Programs**, point to **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5df62-175">En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente** a &gt; **continuación**.</span><span class="sxs-lookup"><span data-stu-id="5df62-175">In the App-V Sequencer, click **Modify an Existing Virtual Application Package** &gt; **Next**.</span></span>

3.  <span data-ttu-id="5df62-176">En la página **seleccionar tarea** , haga clic en **Agregar nueva aplicación** &gt; **Next**.</span><span class="sxs-lookup"><span data-stu-id="5df62-176">On the **Select Task** page, click **Add New Application** &gt; **Next**.</span></span>

4.  <span data-ttu-id="5df62-177">En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual al que desea agregar la aplicación y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-177">On the **Select Package** page, click **Browse** to locate the virtual application package to which you will add the application, and then click **Next**.</span></span>

5.  <span data-ttu-id="5df62-178">En la página **preparar el equipo** , revise los problemas que podrían provocar errores en la creación del paquete o hacer que el paquete revisado contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="5df62-178">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or cause the revised package to contain unnecessary data.</span></span> <span data-ttu-id="5df62-179">Solucione todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="5df62-179">Resolve all potential issues before you continue.</span></span> <span data-ttu-id="5df62-180">Después de realizar correcciones y resolver todos los problemas potenciales, haga clic en **Actualizar** &gt; **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-180">After making any corrections and resolving all potential issues, click **Refresh** &gt; **Next**.</span></span>

    <span data-ttu-id="5df62-181">**Importante**  Si se le pide que deshabilite el software de detección de virus, primero examine el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni malintencionados al paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-181">**Important** If you are required to disable virus scanning software, first scan the computer that runs the sequencer to ensure that no unwanted or malicious files can be added to the package.</span></span>

6.  <span data-ttu-id="5df62-182">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5df62-182">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="5df62-183">Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-183">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

7.  <span data-ttu-id="5df62-184">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, instale la aplicación para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="5df62-184">On the **Installation** page, when the sequencer and application installer are ready, install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="5df62-185">Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**y busque y ejecute los archivos de instalación adicionales.</span><span class="sxs-lookup"><span data-stu-id="5df62-185">If additional installation files must be run as part of the installation, click **Run**, and locate and run the additional installation files.</span></span> <span data-ttu-id="5df62-186">Cuando termine la instalación, seleccione **he terminado de instalar** &gt; **Next**.</span><span class="sxs-lookup"><span data-stu-id="5df62-186">When you finish the installation, select **I am finished installing** &gt; **Next**.</span></span> <span data-ttu-id="5df62-187">En el cuadro de diálogo **Buscar carpeta** , especifique el directorio principal en el que se instalará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5df62-187">In the **Browse for Folder** dialog box, specify the primary directory where the application will be installed.</span></span> <span data-ttu-id="5df62-188">Asegúrese de que se trata de una nueva ubicación para no sobrescribir la versión existente del paquete de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="5df62-188">Ensure that this is a new location so that you don’t overwrite the existing version of the virtual application package.</span></span>

    <span data-ttu-id="5df62-189">**Nota:**  El secuenciador supervisa todos los cambios e instalaciones que se producen en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="5df62-189">**Note** The sequencer monitors all changes and installations that occur on the computer that runs the sequencer.</span></span> <span data-ttu-id="5df62-190">Esto incluye los cambios y las instalaciones que se realizan fuera del asistente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="5df62-190">This includes any changes and installations that are performed outside of the sequencing wizard.</span></span>

8.  <span data-ttu-id="5df62-191">En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-191">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="5df62-192">En este paso se completan todas las licencias o tareas de configuración asociadas que se requieren para ejecutar la aplicación antes de implementar y ejecutar el paquete en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5df62-192">This step completes any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="5df62-193">Para ejecutar todos los programas al mismo tiempo, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**.</span><span class="sxs-lookup"><span data-stu-id="5df62-193">To run all the programs at the same time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="5df62-194">Para ejecutar programas específicos, seleccione el programa o los programas que desea ejecutar y, a continuación, haga clic en **Ejecutar selección**.</span><span class="sxs-lookup"><span data-stu-id="5df62-194">To run specific programs, select the program or programs you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="5df62-195">Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5df62-195">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="5df62-196">Pueden pasar varios minutos hasta que se ejecuten todos los programas.</span><span class="sxs-lookup"><span data-stu-id="5df62-196">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="5df62-197">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-197">Click **Next**.</span></span>

9.  <span data-ttu-id="5df62-198">En la página del **Informe de instalación** , puede revisar la información sobre la aplicación virtual actualizada.</span><span class="sxs-lookup"><span data-stu-id="5df62-198">On the **Installation Report** page, you can review information about the updated virtual application.</span></span> <span data-ttu-id="5df62-199">En **información adicional**, haga doble clic en el evento para obtener información más detallada y, a continuación, haga clic en **siguiente** para abrir la página **personalizar** .</span><span class="sxs-lookup"><span data-stu-id="5df62-199">In **Additional Information**, double-click the event to obtain more detailed information, and then click **Next** to open the **Customize** page.</span></span>

10. <span data-ttu-id="5df62-200">Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 13 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5df62-200">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 13 of this procedure.</span></span> <span data-ttu-id="5df62-201">Si desea realizar las siguientes personalizaciones descritas, haga clic en **personalizar**.</span><span class="sxs-lookup"><span data-stu-id="5df62-201">If you want to perform the following described customization, click **Customize**.</span></span>

    <span data-ttu-id="5df62-202">Si está personalizando, prepare el paquete virtual para la transmisión por secuencias y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-202">If you are customizing, prepare the virtual package for streaming, and then click **Next**.</span></span> <span data-ttu-id="5df62-203">La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5df62-203">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

11. <span data-ttu-id="5df62-204">En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5df62-204">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="5df62-205">Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5df62-205">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="5df62-206">Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-206">After all applications have run, close each of the applications, and then click **Next**.</span></span>

    <span data-ttu-id="5df62-207">**Nota:**  Puede detener la carga de una aplicación durante este paso.</span><span class="sxs-lookup"><span data-stu-id="5df62-207">**Note** You can stop an application from loading during this step.</span></span> <span data-ttu-id="5df62-208">En el cuadro de diálogo **Inicio** de la aplicación, haga clic en **detener** y, a continuación, seleccione detener **todas las aplicaciones** o **detener solo esta aplicación**.</span><span class="sxs-lookup"><span data-stu-id="5df62-208">In the **Application Launch** dialog box, click **Stop** and then select either **Stop all applications** or **Stop this application only**.</span></span>

12. <span data-ttu-id="5df62-209">En la página **crear paquete** , para modificar el paquete sin guardarlo, active la casilla **continuar con la modificación de paquetes sin guardar con el editor de paquetes** .</span><span class="sxs-lookup"><span data-stu-id="5df62-209">On the **Create Package** page, to modify the package without saving it, select the **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="5df62-210">Al seleccionar esta opción, se abre el paquete en la consola del secuenciador de App-V, donde puede modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="5df62-210">Selecting this option opens the package in the App-V Sequencer console, where you can modify the package before saving it.</span></span> <span data-ttu-id="5df62-211">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5df62-211">Click **Next**.</span></span>

    <span data-ttu-id="5df62-212">Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora.</span><span class="sxs-lookup"><span data-stu-id="5df62-212">To save the package immediately, select the default **Save the package now**.</span></span> <span data-ttu-id="5df62-213">Agregue **comentarios** opcionales para asociarlos con el paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-213">Add optional **Comments** to associate with the package.</span></span> <span data-ttu-id="5df62-214">Los comentarios son útiles para proporcionar versiones de la aplicación y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="5df62-214">Comments are useful for providing application versions and other information about the package.</span></span> <span data-ttu-id="5df62-215">También se muestra la **Ubicación de almacenamiento** predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5df62-215">The default **Save Location** is also displayed.</span></span> <span data-ttu-id="5df62-216">Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="5df62-216">To change the default location, click **Browse** and specify the new location.</span></span> <span data-ttu-id="5df62-217">Se muestra el tamaño del paquete sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="5df62-217">The uncompressed package size is displayed.</span></span> <span data-ttu-id="5df62-218">Haga clic en **Crear**.</span><span class="sxs-lookup"><span data-stu-id="5df62-218">Click **Create**.</span></span>

13. <span data-ttu-id="5df62-219">En la página **Finalización**, haz clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="5df62-219">On the **Completion** page, click **Close**.</span></span> <span data-ttu-id="5df62-220">El paquete está ahora disponible en el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="5df62-220">The package is now available in the sequencer.</span></span>

    <span data-ttu-id="5df62-221">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="5df62-221">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5df62-222">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5df62-222">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5df62-223">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="5df62-223">Got an App-V issue?</span></span>** <span data-ttu-id="5df62-224">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5df62-224">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5df62-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5df62-225">Related topics</span></span>

[<span data-ttu-id="5df62-226">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5df62-226">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 




