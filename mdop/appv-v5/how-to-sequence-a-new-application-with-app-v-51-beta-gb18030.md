---
title: Cómo secuenciar una nueva aplicación con App-V 5.1
description: Cómo secuenciar una nueva aplicación con App-V 5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813718"
---
# <span data-ttu-id="44930-103">Cómo secuenciar una nueva aplicación con App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="44930-103">How to Sequence a New Application with App-V 5.1</span></span>


**<span data-ttu-id="44930-104">Para revisar o hacer antes de iniciar la secuencia</span><span class="sxs-lookup"><span data-stu-id="44930-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="44930-105">Determine el tipo de paquete de aplicación virtualizado que desea crear:</span><span class="sxs-lookup"><span data-stu-id="44930-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="44930-106">Tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="44930-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="44930-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="44930-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="44930-108">Standard</span><span class="sxs-lookup"><span data-stu-id="44930-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="44930-109">Crea un paquete que contiene una aplicación o un conjunto de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="44930-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="44930-110">Esta es la opción preferida para la mayoría de los tipos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="44930-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="44930-111">Complemento o complemento</span><span class="sxs-lookup"><span data-stu-id="44930-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="44930-112">Crea un paquete que extiende la funcionalidad de una aplicación estándar, por ejemplo, un complemento para Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="44930-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="44930-113">Además, puede usar complementos para aplicaciones instaladas de forma nativa o para otro paquete vinculado mediante grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="44930-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="44930-114">Cabe</span><span class="sxs-lookup"><span data-stu-id="44930-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="44930-115">Crea un paquete necesario para una aplicación estándar, por ejemplo, Java.</span><span class="sxs-lookup"><span data-stu-id="44930-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="44930-116">Los paquetes de middleware se usan para vincular a otros paquetes mediante grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="44930-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="44930-117">Copie todos los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="44930-118">Haga una imagen de copia de seguridad de su entorno virtual antes de la secuenciar una aplicación y, a continuación, vuelva a la imagen cada vez que termine de secuenciar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="44930-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="44930-119">Revise los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="44930-119">Review the following items:</span></span>

    -   <span data-ttu-id="44930-120">Si un instalador de aplicaciones cambia el acceso de seguridad a un archivo o directorio nuevo o existente, esos cambios no se capturan en el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="44930-121">Si se han deshabilitado las rutas cortas para el volumen de destino del paquete virtualizado, también debe secuenciar el paquete en un volumen que se haya creado y tenga las rutas cortas deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="44930-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="44930-122">No puede ser el volumen del sistema.</span><span class="sxs-lookup"><span data-stu-id="44930-122">It cannot be the system volume.</span></span>

> [!NOTE]  
> <span data-ttu-id="44930-123">El secuenciador de App-V 5. x no puede secuenciar aplicaciones con nombres de archivo que coincidan con "CO_ &lt; x &gt; " donde x es un número.</span><span class="sxs-lookup"><span data-stu-id="44930-123">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="44930-124">Se generará el error 0x8007139F.</span><span class="sxs-lookup"><span data-stu-id="44930-124">Error 0x8007139F will be generated.</span></span>

**<span data-ttu-id="44930-125">Para secuenciar una nueva aplicación estándar</span><span class="sxs-lookup"><span data-stu-id="44930-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="44930-126">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**y, a continuación, haga clic en **Microsoft Application**Virtualization y en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="44930-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="44930-127">En el secuenciador, haga clic en **crear un nuevo paquete de aplicaciones virtual**.</span><span class="sxs-lookup"><span data-stu-id="44930-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="44930-128">Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="44930-129">En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="44930-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="44930-130">Debes resolver todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="44930-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="44930-131">Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="44930-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="44930-132">Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-132">After you have resolved all potential issues, click **Next**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="44930-133">Si se le pide que deshabilite el software de detección de virus, primero debe examinar el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni maliciosos al paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-133">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. <span data-ttu-id="44930-134">En la página **tipo de aplicación** , haga clic en la casilla de verificación **aplicación estándar (predeterminada)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-134">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5. <span data-ttu-id="44930-135">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="44930-135">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="44930-136">Si el instalador de la aplicación especificada modifica el acceso de seguridad a un archivo o directorio, ya sea existentes o nuevos, los cambios asociados no se capturarán en el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-136">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="44930-137">En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-137">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="44930-138">Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-138">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="44930-139">El nombre del paquete se muestra en la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="44930-139">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="44930-140">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-140">Click **Next**.</span></span>

7. <span data-ttu-id="44930-141">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede continuar con la instalación de la aplicación para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="44930-141">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-142">Siempre debe instalar aplicaciones en una ubicación segura y asegurarse de que ningún otro usuario ha iniciado sesión en el equipo que ejecuta el secuenciador durante la supervisión.</span><span class="sxs-lookup"><span data-stu-id="44930-142">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="44930-143">En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtualizado.</span><span class="sxs-lookup"><span data-stu-id="44930-143">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="44930-144">En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-144">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="44930-145">Este paso le permite completar cualquier tarea de configuración o licencia necesaria antes de implementar y ejecutar el paquete en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="44930-145">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="44930-146">Para ejecutar todos los programas a la vez, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**.</span><span class="sxs-lookup"><span data-stu-id="44930-146">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="44930-147">Para ejecutar programas específicos, seleccione el programa o programas y, a continuación, haga clic en **Ejecutar selección**.</span><span class="sxs-lookup"><span data-stu-id="44930-147">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="44930-148">Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="44930-148">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="44930-149">Es posible que tenga que esperar varios minutos para que se ejecuten todos los programas.</span><span class="sxs-lookup"><span data-stu-id="44930-149">You may need to wait several minutes for all programs to run.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="44930-150">Para ejecutar las tareas de primer uso para cualquier aplicación que no esté disponible en la lista, abra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="44930-150">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="44930-151">La información asociada se capturará durante este paso.</span><span class="sxs-lookup"><span data-stu-id="44930-151">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="44930-152">En la página del **Informe de instalación** , puede revisar la información sobre el paquete de la aplicación virtualizada que acaba de secuenciar.</span><span class="sxs-lookup"><span data-stu-id="44930-152">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="44930-153">En **información adicional**, haga doble clic en un evento para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="44930-153">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="44930-154">Para continuar, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-154">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="44930-155">Se muestra la página **personalizar** .</span><span class="sxs-lookup"><span data-stu-id="44930-155">The **Customize** page is displayed.</span></span> <span data-ttu-id="44930-156">Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 14 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="44930-156">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="44930-157">Para realizar una de las siguientes personalizaciones, seleccione **personalizar**.</span><span class="sxs-lookup"><span data-stu-id="44930-157">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="44930-158">Preparar el paquete virtual para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="44930-158">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="44930-159">La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="44930-159">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="44930-160">Especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-160">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="44930-161">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-161">Click **Next**.</span></span>

12. <span data-ttu-id="44930-162">En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="44930-162">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="44930-163">Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="44930-163">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="44930-164">Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-164">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="44930-165">Si no abre ninguna aplicación durante este paso, el método de transmisión por secuencias predeterminado es la entrega por secuencias a petición.</span><span class="sxs-lookup"><span data-stu-id="44930-165">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="44930-166">Esto significa que las aplicaciones se descargarán bit a bit hasta que se puedan abrir y, en función de cómo esté configurada la carga del fondo, cargarán el resto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="44930-166">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="44930-167">En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-167">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="44930-168">Para permitir que todos los sistemas operativos compatibles en su entorno ejecuten este paquete, seleccione **permitir la ejecución de este paquete en cualquier sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="44930-168">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="44930-169">Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, seleccione **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-169">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="44930-170">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-170">Click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-171">Asegúrese de que los sistemas operativos que especifica aquí son compatibles con la aplicación que está transformando.</span><span class="sxs-lookup"><span data-stu-id="44930-171">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="44930-172">Aparece la página **crear paquete** .</span><span class="sxs-lookup"><span data-stu-id="44930-172">The **Create Package** page is displayed.</span></span> <span data-ttu-id="44930-173">Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="44930-173">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="44930-174">Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="44930-174">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="44930-175">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-175">Click **Next**.</span></span>

   <span data-ttu-id="44930-176">Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora** (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="44930-176">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="44930-177">Agregue **comentarios** opcionales para asociarlos con el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-177">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="44930-178">Los comentarios son útiles para identificar la versión del programa y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-178">Comments are useful for identifying the program version and other information about the package.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-179">El sistema no admite caracteres no imprimibles en **comentarios** y **descripciones**.</span><span class="sxs-lookup"><span data-stu-id="44930-179">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="44930-180">Se muestra la página **finalización** .</span><span class="sxs-lookup"><span data-stu-id="44930-180">The **Completion** page is displayed.</span></span> <span data-ttu-id="44930-181">Revise la información del panel **Informe de paquete de aplicación virtual** según sea necesario y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="44930-181">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="44930-182">Esta información también está disponible en el archivo de **Report.xml** que se encuentra en el directorio en el que se creó el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-182">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="44930-183">El paquete está ahora disponible en el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-183">The package is now available in the sequencer.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-184">Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-184">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="44930-185">Para secuenciar un complemento o una aplicación de complemento</span><span class="sxs-lookup"><span data-stu-id="44930-185">To sequence an add-on or plug-in application</span></span>**

1. > [!NOTE]  
   > <span data-ttu-id="44930-186">Antes de realizar el procedimiento siguiente, instale la aplicación principal de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-186">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="44930-187">O bien, si tiene la aplicación principal virtualizada, puede seguir los pasos que se indican en el flujo de trabajo de complementos o complementos para desempaquetar la aplicación principal en el equipo.</span><span class="sxs-lookup"><span data-stu-id="44930-187">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>
   >
   > <span data-ttu-id="44930-188">Por ejemplo, si va a secuenciar un complemento para Microsoft Excel, instale Microsoft Excel de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-188">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="44930-189">También Instale la aplicación principal en el mismo directorio en el que se instala la aplicación en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="44930-189">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="44930-190">Si el complemento o complemento se va a usar con un paquete de aplicación virtual existente, instale la aplicación en la misma unidad de aplicación virtual que se usó cuando creó el paquete de la aplicación virtual principal.</span><span class="sxs-lookup"><span data-stu-id="44930-190">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="44930-191">\*<strong><em>En el secuenciador, haga clic en \* </em> crear un nuevo paquete de aplicaciones virtual </strong> .</span><span class="sxs-lookup"><span data-stu-id="44930-191">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="44930-192">Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-192">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="44930-193">En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="44930-193">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="44930-194">Debes resolver todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="44930-194">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="44930-195">Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="44930-195">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="44930-196">Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-196">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-197">Si se le pide que deshabilite el software de detección de virus, primero debe examinar el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni maliciosos al paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-197">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="44930-198">En la página **tipo de aplicación** , seleccione **complementos o complementos**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-198">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="44930-199">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación del complemento o complemento.</span><span class="sxs-lookup"><span data-stu-id="44930-199">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="44930-200">Si el complemento o complemento no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-200">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="44930-201">En la página de **instalación principal** , asegúrese de que la aplicación principal está instalada en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-201">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="44930-202">Como alternativa, puede expandir un paquete existente guardado localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-202">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="44930-203">Para ello, haga clic en **expandir paquete**y, a continuación, seleccione el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-203">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="44930-204">Después de expandir o instalar el programa principal, seleccione **he instalado el programa**principal principal.</span><span class="sxs-lookup"><span data-stu-id="44930-204">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="44930-205">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-205">Click **Next**.</span></span>

7. <span data-ttu-id="44930-206">En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-206">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="44930-207">Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-207">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="44930-208">El nombre del paquete aparecerá en la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="44930-208">The package name will be displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="44930-209">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-209">Click **Next**.</span></span>

8. <span data-ttu-id="44930-210">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede continuar con la instalación de la aplicación de complemento o complemento para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="44930-210">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="44930-211">Use el proceso de instalación de la aplicación para realizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="44930-211">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="44930-212">Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar** y busque y ejecute los archivos de instalación adicionales.</span><span class="sxs-lookup"><span data-stu-id="44930-212">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="44930-213">Cuando haya finalizado la instalación, seleccione **he terminado de instalar**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-213">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="44930-214">En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicaciones virtual que acaba de secuenciar.</span><span class="sxs-lookup"><span data-stu-id="44930-214">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="44930-215">Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento.</span><span class="sxs-lookup"><span data-stu-id="44930-215">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="44930-216">Después de revisar la información, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-216">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="44930-217">Se muestra la página **personalizar** .</span><span class="sxs-lookup"><span data-stu-id="44930-217">The **Customize** page is displayed.</span></span> <span data-ttu-id="44930-218">Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 12 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="44930-218">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="44930-219">Para realizar una de las siguientes personalizaciones, seleccione **personalizar**.</span><span class="sxs-lookup"><span data-stu-id="44930-219">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="44930-220">Optimizar la forma en que el paquete se ejecutará a través de una red lenta o no confiable.</span><span class="sxs-lookup"><span data-stu-id="44930-220">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="44930-221">Especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-221">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="44930-222">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-222">Click **Next**.</span></span>

11. <span data-ttu-id="44930-223">En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="44930-223">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="44930-224">La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino en redes de alta latencia.</span><span class="sxs-lookup"><span data-stu-id="44930-224">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="44930-225">Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="44930-225">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="44930-226">Una vez ejecutadas todas las aplicaciones, cierre cada una de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="44930-226">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="44930-227">También puede configurar el paquete para que se descargue completamente antes de la apertura seleccionando la casilla **obligar a que se descarguen las aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="44930-227">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="44930-228">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-228">Click **Next**.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="44930-229">Si es necesario, puede detener la carga de una aplicación durante este paso.</span><span class="sxs-lookup"><span data-stu-id="44930-229">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="44930-230">En el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener** y seleccione una de las casillas de verificación: **detener todas las aplicaciones** o **detener solo esta aplicación**.</span><span class="sxs-lookup"><span data-stu-id="44930-230">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="44930-231">En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-231">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="44930-232">Para permitir que todos los sistemas operativos compatibles en su entorno ejecuten este paquete, active la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="44930-232">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="44930-233">Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y, a continuación, seleccione los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-233">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="44930-234">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-234">Click **Next**.</span></span>

13. <span data-ttu-id="44930-235">Aparece la página **crear paquete** .</span><span class="sxs-lookup"><span data-stu-id="44930-235">The **Create Package** page is displayed.</span></span> <span data-ttu-id="44930-236">Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con la casilla de verificación editor de paquetes** .</span><span class="sxs-lookup"><span data-stu-id="44930-236">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="44930-237">Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="44930-237">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="44930-238">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-238">Click **Next**.</span></span>

    <span data-ttu-id="44930-239">Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora**.</span><span class="sxs-lookup"><span data-stu-id="44930-239">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="44930-240">De manera opcional, agregue una **Descripción** que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-240">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="44930-241">Las descripciones son útiles para identificar la versión y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-241">Descriptions are useful for identifying the version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="44930-242">El sistema no admite caracteres no imprimibles en comentarios y descripciones.</span><span class="sxs-lookup"><span data-stu-id="44930-242">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="44930-243">Para secuenciar una aplicación de middleware</span><span class="sxs-lookup"><span data-stu-id="44930-243">To sequence a middleware application</span></span>**

1. <span data-ttu-id="44930-244">En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**y, a continuación, haga clic en **Microsoft Application**Virtualization y en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="44930-244">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="44930-245">\*<strong><em>En el secuenciador, haga clic en \* </em> crear un nuevo paquete de aplicaciones virtual </strong> .</span><span class="sxs-lookup"><span data-stu-id="44930-245">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="44930-246">Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-246">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="44930-247">En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="44930-247">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="44930-248">Debes resolver todos los problemas potenciales antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="44930-248">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="44930-249">Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="44930-249">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="44930-250">Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-250">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-251">Si se le pide que deshabilite el software de detección de virus, primero debe analizar el equipo que ejecuta el secuenciador de App-V 5,0 para asegurarse de que no se pueda agregar archivos no deseados o maliciosos al paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-251">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="44930-252">En la página **tipo de aplicación** , seleccione **middleware**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-252">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="44930-253">En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="44930-253">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="44930-254">Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-254">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="44930-255">En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-255">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="44930-256">Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-256">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="44930-257">El nombre del paquete se muestra en la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="44930-257">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="44930-258">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-258">Click **Next**.</span></span>

7. <span data-ttu-id="44930-259">En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación de middleware estén listos, puede continuar con la instalación de la aplicación para que el secuenciador pueda supervisar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="44930-259">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="44930-260">Use el proceso de instalación de la aplicación para realizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="44930-260">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="44930-261">Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**para ubicar y ejecutar los archivos de instalación adicionales.</span><span class="sxs-lookup"><span data-stu-id="44930-261">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="44930-262">Cuando haya terminado con la instalación, active la casilla de verificación **he finalizado la instalación** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-262">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="44930-263">En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="44930-263">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="44930-264">En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicación virtual que acaba de secuenciar.</span><span class="sxs-lookup"><span data-stu-id="44930-264">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="44930-265">En **información adicional**, haga doble clic en un evento para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="44930-265">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="44930-266">Para continuar, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-266">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="44930-267">En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-267">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="44930-268">Para habilitar todos los sistemas operativos compatibles de su entorno para que ejecuten este paquete, seleccione la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="44930-268">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="44930-269">Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-269">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="44930-270">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-270">Click **Next**.</span></span>

11. <span data-ttu-id="44930-271">Aparece la página **crear paquete** .</span><span class="sxs-lookup"><span data-stu-id="44930-271">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="44930-272">Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="44930-272">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="44930-273">Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo.</span><span class="sxs-lookup"><span data-stu-id="44930-273">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="44930-274">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="44930-274">Click **Next**.</span></span>

    <span data-ttu-id="44930-275">Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora**.</span><span class="sxs-lookup"><span data-stu-id="44930-275">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="44930-276">De manera opcional, agregue una **Descripción** que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-276">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="44930-277">Las descripciones son útiles para identificar la versión del programa y otra información sobre el paquete.</span><span class="sxs-lookup"><span data-stu-id="44930-277">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="44930-278">El sistema no admite caracteres no imprimibles en comentarios y descripciones.</span><span class="sxs-lookup"><span data-stu-id="44930-278">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="44930-279">Se muestra la página **finalización** .</span><span class="sxs-lookup"><span data-stu-id="44930-279">The **Completion** page is displayed.</span></span> <span data-ttu-id="44930-280">Revise la información del panel **Informe de paquete de aplicación virtual** según sea necesario y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="44930-280">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="44930-281">Esta información también está disponible en el archivo de **Report.xml** que se encuentra en el directorio especificado en el paso 11 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="44930-281">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="44930-282">El paquete está ahora disponible en el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-282">The package is now available in the sequencer.</span></span> <span data-ttu-id="44930-283">Para editar las propiedades del paquete, haga clic en **Editar \ [nombre del paquete \]**.</span><span class="sxs-lookup"><span data-stu-id="44930-283">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="44930-284">Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="44930-284">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="44930-285">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44930-285">Related topics</span></span>


[<span data-ttu-id="44930-286">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="44930-286">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









