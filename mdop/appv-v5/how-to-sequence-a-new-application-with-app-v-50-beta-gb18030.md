---
title: Cómo secuenciar una nueva aplicación con App-V 5.0
description: Cómo secuenciar una nueva aplicación con App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813719"
---
# <span data-ttu-id="13645-103">Cómo secuenciar una nueva aplicación con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="13645-103">How to Sequence a New Application with App-V 5.0</span></span>


**<span data-ttu-id="13645-104">Para revisar o hacer antes de iniciar la secuencia</span><span class="sxs-lookup"><span data-stu-id="13645-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="13645-105">Determine el tipo de paquete de aplicación virtualizado que desea crear:</span><span class="sxs-lookup"><span data-stu-id="13645-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="13645-106">Tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="13645-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="13645-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="13645-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="13645-108">Standard</span><span class="sxs-lookup"><span data-stu-id="13645-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="13645-109">Crea un paquete que contiene una aplicación o un conjunto de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="13645-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="13645-110">Esta es la opción preferida para la mayoría de los tipos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="13645-111">Complemento o complemento</span><span class="sxs-lookup"><span data-stu-id="13645-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="13645-112">Crea un paquete que extiende la funcionalidad de una aplicación estándar, por ejemplo, un complemento para Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="13645-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="13645-113">Además, puede usar complementos para aplicaciones instaladas de forma nativa o para otro paquete vinculado mediante grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="13645-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="13645-114">Cabe</span><span class="sxs-lookup"><span data-stu-id="13645-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="13645-115">Crea un paquete necesario para una aplicación estándar, por ejemplo, Java.</span><span class="sxs-lookup"><span data-stu-id="13645-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="13645-116">Los paquetes de middleware se usan para vincular a otros paquetes mediante grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="13645-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="13645-117">Copie todos los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="13645-118">Haga una imagen de copia de seguridad de su entorno virtual antes de la secuenciar una aplicación y, a continuación, vuelva a la imagen cada vez que termine de secuenciar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="13645-119">Revise los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="13645-119">Review the following items:</span></span>

    -   <span data-ttu-id="13645-120">Si un instalador de aplicaciones cambia el acceso de seguridad a un archivo o directorio nuevo o existente, esos cambios no se capturan en el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="13645-121">Si se han deshabilitado las rutas cortas para el volumen de destino del paquete virtualizado, también debe secuenciar el paquete en un volumen que se haya creado y tenga las rutas cortas deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="13645-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="13645-122">No puede ser el volumen del sistema.</span><span class="sxs-lookup"><span data-stu-id="13645-122">It cannot be the system volume.</span></span>

    -   <span data-ttu-id="13645-123">A partir de App-V 5,0 SP3, el directorio principal de la aplicación virtual (PVAD) está oculto, pero puede volver a activarlo.</span><span class="sxs-lookup"><span data-stu-id="13645-123">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="13645-124">Consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="13645-124">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>

**<span data-ttu-id="13645-125">Para secuenciar una nueva aplicación estándar</span><span class="sxs-lookup"><span data-stu-id="13645-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="13645-126">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**y, a continuación, haga clic en **Microsoft Application**Virtualization y en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="13645-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="13645-127">En el secuenciador, haga clic en **crear un nuevo paquete de aplicaciones virtual**.</span><span class="sxs-lookup"><span data-stu-id="13645-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="13645-128">Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="13645-129">En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="13645-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="13645-130">Debes resolver todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="13645-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="13645-131">Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="13645-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="13645-132">Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-132">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="13645-133">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-133">Important</span></span>**  
    <span data-ttu-id="13645-134">Si se le pide que deshabilite el software de detección de virus, primero debe examinar el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni maliciosos al paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-134">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="13645-135">En la página **tipo de aplicación** , haga clic en la casilla de verificación **aplicación estándar (predeterminada)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-135">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5.  <span data-ttu-id="13645-136">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-136">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

    **<span data-ttu-id="13645-137">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-137">Note</span></span>**  
    <span data-ttu-id="13645-138">Si el instalador de la aplicación especificada modifica el acceso de seguridad a un archivo o directorio, ya sea existentes o nuevos, los cambios asociados no se capturarán en el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-138">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="13645-139">En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-139">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="13645-140">Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-140">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="13645-141">El nombre del paquete se muestra en la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="13645-141">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="13645-142">El **directorio principal de la aplicación virtual** muestra la ruta en la que se instalará la aplicación en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="13645-142">The **Primary Virtual Application Directory** displays the path where the application will be installed on target computers.</span></span> <span data-ttu-id="13645-143">Para especificar esta ubicación, seleccione **examinar**.</span><span class="sxs-lookup"><span data-stu-id="13645-143">To specify this location, select **Browse**.</span></span>

   **<span data-ttu-id="13645-144">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-144">Note</span></span>**  
   <span data-ttu-id="13645-145">A partir de App-V 5,0 SP3, el directorio principal de la aplicación virtual (PVAD) está oculto, pero puede volver a activarlo.</span><span class="sxs-lookup"><span data-stu-id="13645-145">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="13645-146">Consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="13645-146">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. <span data-ttu-id="13645-147">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede continuar con la instalación de la aplicación para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="13645-147">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   **<span data-ttu-id="13645-148">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-148">Important</span></span>**  
   <span data-ttu-id="13645-149">Siempre debe instalar aplicaciones en una ubicación segura y asegurarse de que ningún otro usuario ha iniciado sesión en el equipo que ejecuta el secuenciador durante la supervisión.</span><span class="sxs-lookup"><span data-stu-id="13645-149">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="13645-150">En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtualizado.</span><span class="sxs-lookup"><span data-stu-id="13645-150">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="13645-151">En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-151">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="13645-152">Este paso le permite completar cualquier tarea de configuración o licencia necesaria antes de implementar y ejecutar el paquete en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="13645-152">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="13645-153">Para ejecutar todos los programas a la vez, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**.</span><span class="sxs-lookup"><span data-stu-id="13645-153">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="13645-154">Para ejecutar programas específicos, seleccione el programa o programas y, a continuación, haga clic en **Ejecutar selección**.</span><span class="sxs-lookup"><span data-stu-id="13645-154">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="13645-155">Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="13645-155">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="13645-156">Es posible que tenga que esperar varios minutos para que se ejecuten todos los programas.</span><span class="sxs-lookup"><span data-stu-id="13645-156">You may need to wait several minutes for all programs to run.</span></span>

   **<span data-ttu-id="13645-157">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-157">Note</span></span>**  
   <span data-ttu-id="13645-158">Para ejecutar las tareas de primer uso para cualquier aplicación que no esté disponible en la lista, abra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-158">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="13645-159">La información asociada se capturará durante este paso.</span><span class="sxs-lookup"><span data-stu-id="13645-159">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="13645-160">En la página del **Informe de instalación** , puede revisar la información sobre el paquete de la aplicación virtualizada que acaba de secuenciar.</span><span class="sxs-lookup"><span data-stu-id="13645-160">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="13645-161">En **información adicional**, haga doble clic en un evento para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="13645-161">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="13645-162">Para continuar, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-162">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="13645-163">Se muestra la página **personalizar** .</span><span class="sxs-lookup"><span data-stu-id="13645-163">The **Customize** page is displayed.</span></span> <span data-ttu-id="13645-164">Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 14 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="13645-164">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="13645-165">Para realizar una de las siguientes personalizaciones, seleccione **personalizar**.</span><span class="sxs-lookup"><span data-stu-id="13645-165">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="13645-166">Preparar el paquete virtual para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="13645-166">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="13645-167">La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="13645-167">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="13645-168">Especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-168">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="13645-169">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-169">Click **Next**.</span></span>

12. <span data-ttu-id="13645-170">En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="13645-170">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="13645-171">Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="13645-171">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="13645-172">Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-172">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="13645-173">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-173">Note</span></span>**  
   <span data-ttu-id="13645-174">Si no abre ninguna aplicación durante este paso, el método de transmisión por secuencias predeterminado es la entrega por secuencias a petición.</span><span class="sxs-lookup"><span data-stu-id="13645-174">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="13645-175">Esto significa que las aplicaciones se descargarán bit a bit hasta que se puedan abrir y, en función de cómo esté configurada la carga del fondo, cargarán el resto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-175">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="13645-176">En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-176">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="13645-177">Para permitir que todos los sistemas operativos compatibles en su entorno ejecuten este paquete, seleccione **permitir la ejecución de este paquete en cualquier sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="13645-177">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="13645-178">Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, seleccione **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-178">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="13645-179">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-179">Click **Next**.</span></span>

   **<span data-ttu-id="13645-180">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-180">Important</span></span>**  
   <span data-ttu-id="13645-181">Asegúrese de que los sistemas operativos que especifica aquí son compatibles con la aplicación que está transformando.</span><span class="sxs-lookup"><span data-stu-id="13645-181">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="13645-182">Aparece la página **crear paquete** .</span><span class="sxs-lookup"><span data-stu-id="13645-182">The **Create Package** page is displayed.</span></span> <span data-ttu-id="13645-183">Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="13645-183">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="13645-184">Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="13645-184">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="13645-185">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-185">Click **Next**.</span></span>

   <span data-ttu-id="13645-186">Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora** (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="13645-186">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="13645-187">Agregue **comentarios** opcionales para asociarlos con el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-187">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="13645-188">Los comentarios son útiles para identificar la versión del programa y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-188">Comments are useful for identifying the program version and other information about the package.</span></span>

   **<span data-ttu-id="13645-189">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-189">Important</span></span>**  
   <span data-ttu-id="13645-190">El sistema no admite caracteres no imprimibles en **comentarios** y **descripciones**.</span><span class="sxs-lookup"><span data-stu-id="13645-190">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="13645-191">Se muestra la página **finalización** .</span><span class="sxs-lookup"><span data-stu-id="13645-191">The **Completion** page is displayed.</span></span> <span data-ttu-id="13645-192">Revise la información del panel **Informe de paquete de aplicación virtual** según sea necesario y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="13645-192">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="13645-193">Esta información también está disponible en el archivo de **Report.xml** que se encuentra en el directorio en el que se creó el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-193">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="13645-194">El paquete está ahora disponible en el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-194">The package is now available in the sequencer.</span></span>

   **<span data-ttu-id="13645-195">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-195">Important</span></span>**  
   <span data-ttu-id="13645-196">Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-196">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="13645-197">Para secuenciar un complemento o una aplicación de complemento</span><span class="sxs-lookup"><span data-stu-id="13645-197">To sequence an add-on or plug-in application</span></span>**

1.  

    **<span data-ttu-id="13645-198">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-198">Note</span></span>**  
    <span data-ttu-id="13645-199">Antes de realizar el procedimiento siguiente, instale la aplicación principal de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-199">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="13645-200">O bien, si tiene la aplicación principal virtualizada, puede seguir los pasos que se indican en el flujo de trabajo de complementos o complementos para desempaquetar la aplicación principal en el equipo.</span><span class="sxs-lookup"><span data-stu-id="13645-200">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>

    <span data-ttu-id="13645-201">Por ejemplo, si va a secuenciar un complemento para Microsoft Excel, instale Microsoft Excel de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-201">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="13645-202">También Instale la aplicación principal en el mismo directorio en el que se instala la aplicación en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="13645-202">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="13645-203">Si el complemento o complemento se va a usar con un paquete de aplicación virtual existente, instale la aplicación en la misma unidad de aplicación virtual que se usó cuando creó el paquete de la aplicación virtual principal.</span><span class="sxs-lookup"><span data-stu-id="13645-203">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="13645-204">\*<strong><em>En el secuenciador, haga clic en \* </em> crear un nuevo paquete de aplicaciones virtual </strong> .</span><span class="sxs-lookup"><span data-stu-id="13645-204">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="13645-205">Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-205">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="13645-206">En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="13645-206">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="13645-207">Debes resolver todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="13645-207">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="13645-208">Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="13645-208">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="13645-209">Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-209">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="13645-210">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-210">Important</span></span>**  
   <span data-ttu-id="13645-211">Si se le pide que deshabilite el software de detección de virus, primero debe examinar el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni maliciosos al paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-211">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="13645-212">En la página **tipo de aplicación** , seleccione **complementos o complementos**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-212">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="13645-213">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación del complemento o complemento.</span><span class="sxs-lookup"><span data-stu-id="13645-213">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="13645-214">Si el complemento o complemento no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-214">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="13645-215">En la página de **instalación principal** , asegúrese de que la aplicación principal está instalada en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-215">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="13645-216">Como alternativa, puede expandir un paquete existente guardado localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-216">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="13645-217">Para ello, haga clic en **expandir paquete**y, a continuación, seleccione el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-217">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="13645-218">Después de expandir o instalar el programa principal, seleccione **he instalado el programa**principal principal.</span><span class="sxs-lookup"><span data-stu-id="13645-218">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="13645-219">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-219">Click **Next**.</span></span>

7. <span data-ttu-id="13645-220">En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-220">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="13645-221">Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-221">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="13645-222">El nombre del paquete aparecerá en la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="13645-222">The package name will be displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="13645-223">El **directorio principal de la aplicación virtual** muestra la ruta en la que se instalará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-223">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="13645-224">Para especificar esta ubicación, escriba la ruta de acceso o haga clic en **examinar**.</span><span class="sxs-lookup"><span data-stu-id="13645-224">To specify this location, type the path, or click **Browse**.</span></span>

   **<span data-ttu-id="13645-225">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-225">Note</span></span>**  
   <span data-ttu-id="13645-226">A partir de App-V 5,0 SP3, el directorio principal de la aplicación virtual (PVAD) está oculto, pero puede volver a activarlo.</span><span class="sxs-lookup"><span data-stu-id="13645-226">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="13645-227">Consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="13645-227">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="13645-228">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede continuar con la instalación de la aplicación de complemento o complemento para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="13645-228">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="13645-229">Use el proceso de instalación de la aplicación para realizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="13645-229">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="13645-230">Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar** y busque y ejecute los archivos de instalación adicionales.</span><span class="sxs-lookup"><span data-stu-id="13645-230">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="13645-231">Cuando haya finalizado la instalación, seleccione **he terminado de instalar**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-231">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="13645-232">En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicaciones virtual que acaba de secuenciar.</span><span class="sxs-lookup"><span data-stu-id="13645-232">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="13645-233">Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento.</span><span class="sxs-lookup"><span data-stu-id="13645-233">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="13645-234">Después de revisar la información, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-234">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="13645-235">Se muestra la página **personalizar** .</span><span class="sxs-lookup"><span data-stu-id="13645-235">The **Customize** page is displayed.</span></span> <span data-ttu-id="13645-236">Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 12 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="13645-236">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="13645-237">Para realizar una de las siguientes personalizaciones, seleccione **personalizar**.</span><span class="sxs-lookup"><span data-stu-id="13645-237">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="13645-238">Optimizar la forma en que el paquete se ejecutará a través de una red lenta o no confiable.</span><span class="sxs-lookup"><span data-stu-id="13645-238">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="13645-239">Especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-239">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="13645-240">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-240">Click **Next**.</span></span>

11. <span data-ttu-id="13645-241">En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="13645-241">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="13645-242">La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino en redes de alta latencia.</span><span class="sxs-lookup"><span data-stu-id="13645-242">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="13645-243">Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="13645-243">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="13645-244">Una vez ejecutadas todas las aplicaciones, cierre cada una de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="13645-244">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="13645-245">También puede configurar el paquete para que se descargue completamente antes de la apertura seleccionando la casilla **obligar a que se descarguen las aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="13645-245">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="13645-246">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-246">Click **Next**.</span></span>

   **<span data-ttu-id="13645-247">Nota</span><span class="sxs-lookup"><span data-stu-id="13645-247">Note</span></span>**  
   <span data-ttu-id="13645-248">Si es necesario, puede detener la carga de una aplicación durante este paso.</span><span class="sxs-lookup"><span data-stu-id="13645-248">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="13645-249">En el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener** y seleccione una de las casillas de verificación: **detener todas las aplicaciones** o **detener solo esta aplicación**.</span><span class="sxs-lookup"><span data-stu-id="13645-249">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="13645-250">En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-250">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="13645-251">Para permitir que todos los sistemas operativos compatibles en su entorno ejecuten este paquete, active la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="13645-251">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="13645-252">Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y, a continuación, seleccione los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-252">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="13645-253">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-253">Click **Next**.</span></span>

13. <span data-ttu-id="13645-254">Aparece la página **crear paquete** .</span><span class="sxs-lookup"><span data-stu-id="13645-254">The **Create Package** page is displayed.</span></span> <span data-ttu-id="13645-255">Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con la casilla de verificación editor de paquetes** .</span><span class="sxs-lookup"><span data-stu-id="13645-255">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="13645-256">Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="13645-256">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="13645-257">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-257">Click **Next**.</span></span>

   <span data-ttu-id="13645-258">Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora**.</span><span class="sxs-lookup"><span data-stu-id="13645-258">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="13645-259">De manera opcional, agregue una **Descripción** que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-259">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="13645-260">Las descripciones son útiles para identificar la versión y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-260">Descriptions are useful for identifying the version and other information about the package.</span></span>

   **<span data-ttu-id="13645-261">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-261">Important</span></span>**  
   <span data-ttu-id="13645-262">El sistema no admite caracteres no imprimibles en comentarios y descripciones.</span><span class="sxs-lookup"><span data-stu-id="13645-262">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="13645-263">Para secuenciar una aplicación de middleware</span><span class="sxs-lookup"><span data-stu-id="13645-263">To sequence a middleware application</span></span>**

1. <span data-ttu-id="13645-264">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**y, a continuación, haga clic en **Microsoft Application**Virtualization y en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="13645-264">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="13645-265">\*<strong><em>En el secuenciador, haga clic en \* </em> crear un nuevo paquete de aplicaciones virtual </strong> .</span><span class="sxs-lookup"><span data-stu-id="13645-265">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="13645-266">Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-266">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="13645-267">En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="13645-267">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="13645-268">Debes resolver todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="13645-268">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="13645-269">Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="13645-269">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="13645-270">Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-270">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="13645-271">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-271">Important</span></span>**  
   <span data-ttu-id="13645-272">Si se le pide que deshabilite el software de detección de virus, primero debe analizar el equipo que ejecuta el secuenciador de App-V 5,0 para asegurarse de que no se pueda agregar archivos no deseados o maliciosos al paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-272">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="13645-273">En la página **tipo de aplicación** , seleccione **middleware**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-273">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="13645-274">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-274">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="13645-275">Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-275">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="13645-276">En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-276">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="13645-277">Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-277">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="13645-278">El nombre del paquete se muestra en la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="13645-278">The package name is displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="13645-279">El **directorio principal de la aplicación virtual** muestra la ruta en la que se instalará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13645-279">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="13645-280">Para especificar esta ubicación, escriba la ruta de acceso o haga clic en **examinar**.</span><span class="sxs-lookup"><span data-stu-id="13645-280">To specify this location, type the path or click **Browse**.</span></span>

   <span data-ttu-id="13645-281">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-281">Click **Next**.</span></span>

7. <span data-ttu-id="13645-282">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación de middleware estén listos, puede continuar con la instalación de la aplicación para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="13645-282">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="13645-283">Use el proceso de instalación de la aplicación para realizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="13645-283">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="13645-284">Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**para ubicar y ejecutar los archivos de instalación adicionales.</span><span class="sxs-lookup"><span data-stu-id="13645-284">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="13645-285">Cuando haya terminado con la instalación, active la casilla de verificación **he finalizado la instalación** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-285">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="13645-286">En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="13645-286">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="13645-287">En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicación virtual que acaba de secuenciar.</span><span class="sxs-lookup"><span data-stu-id="13645-287">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="13645-288">En **información adicional**, haga doble clic en un evento para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="13645-288">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="13645-289">Para continuar, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-289">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="13645-290">En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-290">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="13645-291">Para habilitar todos los sistemas operativos compatibles de su entorno para que ejecuten este paquete, seleccione la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="13645-291">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="13645-292">Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-292">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="13645-293">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-293">Click **Next**.</span></span>

11. <span data-ttu-id="13645-294">Aparece la página **crear paquete** .</span><span class="sxs-lookup"><span data-stu-id="13645-294">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="13645-295">Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="13645-295">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="13645-296">Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="13645-296">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="13645-297">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13645-297">Click **Next**.</span></span>

    <span data-ttu-id="13645-298">Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora**.</span><span class="sxs-lookup"><span data-stu-id="13645-298">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="13645-299">De manera opcional, agregue una **Descripción** que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-299">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="13645-300">Las descripciones son útiles para identificar la versión del programa y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="13645-300">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    **<span data-ttu-id="13645-301">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-301">Important</span></span>**  
    <span data-ttu-id="13645-302">El sistema no admite caracteres no imprimibles en comentarios y descripciones.</span><span class="sxs-lookup"><span data-stu-id="13645-302">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="13645-303">Se muestra la página **finalización** .</span><span class="sxs-lookup"><span data-stu-id="13645-303">The **Completion** page is displayed.</span></span> <span data-ttu-id="13645-304">Revise la información del panel **Informe de paquete de aplicación virtual** según sea necesario y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="13645-304">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="13645-305">Esta información también está disponible en el archivo de **Report.xml** que se encuentra en el directorio especificado en el paso 11 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="13645-305">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="13645-306">El paquete está ahora disponible en el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-306">The package is now available in the sequencer.</span></span> <span data-ttu-id="13645-307">Para editar las propiedades del paquete, haga clic en **Editar \ [nombre del paquete \]**.</span><span class="sxs-lookup"><span data-stu-id="13645-307">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   **<span data-ttu-id="13645-308">Importante</span><span class="sxs-lookup"><span data-stu-id="13645-308">Important</span></span>**  
   <span data-ttu-id="13645-309">Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="13645-309">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="13645-310">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13645-310">Related topics</span></span>


[<span data-ttu-id="13645-311">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="13645-311">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









