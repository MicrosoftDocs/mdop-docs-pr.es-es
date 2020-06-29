---
title: Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)
description: Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817640"
---
# <span data-ttu-id="66fb9-103">Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="66fb9-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="66fb9-104">Puede usar los aceleradores de paquetes de App-V para generar automáticamente un nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="66fb9-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="66fb9-105">Después de crear correctamente un acelerador de paquetes, puede volver a usar y compartir el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="66fb9-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="66fb9-106">Para obtener más información sobre los aceleradores de paquetes, consulte Acerca de los [aceleradores de paquetes de App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="66fb9-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="66fb9-107">La creación de aceleradores de paquetes de App-V es una tarea avanzada.</span><span class="sxs-lookup"><span data-stu-id="66fb9-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="66fb9-108">Los aceleradores de paquetes pueden contener contraseña e información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="66fb9-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="66fb9-109">Por lo tanto, debe guardar los aceleradores de paquetes y los medios de instalación asociados en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes de App-V.</span><span class="sxs-lookup"><span data-stu-id="66fb9-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="66fb9-110">En algunas situaciones, para crear el acelerador de paquetes es posible que tenga que instalar la aplicación de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="66fb9-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="66fb9-111">En primer lugar, intente crear el acelerador de paquetes usando los medios de instalación y, si hay una cantidad de archivos que faltan, instálelo localmente en el equipo que ejecuta el secuenciador y, a continuación, cree el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="66fb9-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="66fb9-112">Importante</span><span class="sxs-lookup"><span data-stu-id="66fb9-112">Important</span></span>**  
<span data-ttu-id="66fb9-113">Antes de empezar con el procedimiento siguiente, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="66fb9-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="66fb9-114">Copie el paquete de la aplicación virtual que debe usar para crear el acelerador de paquetes de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="66fb9-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="66fb9-115">Copie todos los archivos de instalación necesarios asociados con el paquete de la aplicación virtual en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="66fb9-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="66fb9-116">Importante</span><span class="sxs-lookup"><span data-stu-id="66fb9-116">Important</span></span>**  
<span data-ttu-id="66fb9-117">Renuncia de responsabilidad: Microsoft Application Virtualization Sequencer no le otorga derechos de licencia a la aplicación de software que está usando para crear un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="66fb9-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="66fb9-118">Debe cumplir todos los términos de licencia de usuario final para dicha aplicación.</span><span class="sxs-lookup"><span data-stu-id="66fb9-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="66fb9-119">Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="66fb9-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="66fb9-120">Para crear un acelerador de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="66fb9-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="66fb9-121">Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="66fb9-122">Para iniciar el Asistente para la **creación de aceleradores de paquetes** de App-v, en el secuenciador de App-v, haga clic en **herramientas**  /  **crear paquete acelerador**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="66fb9-123">En la página **seleccionar paquete** , para especificar que un paquete de aplicación virtual existente se use para crear el acelerador de paquetes, haga clic en **examinar**y busque el paquete de aplicación virtual existente (archivo. SPRJ).</span><span class="sxs-lookup"><span data-stu-id="66fb9-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="66fb9-124">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="66fb9-124">Tip</span></span>**  
    <span data-ttu-id="66fb9-125">Copie los archivos asociados con el paquete de aplicación virtual que planea usar localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="66fb9-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="66fb9-126">En la página **archivos de instalación** , para especificar la carpeta que contiene los archivos de instalación que usó para crear el paquete de aplicación virtual original, haga clic en **examinar**y, a continuación, seleccione el directorio que contiene los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="66fb9-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="66fb9-127">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="66fb9-127">Tip</span></span>**  
   <span data-ttu-id="66fb9-128">Copie la carpeta que contiene los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="66fb9-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="66fb9-129">En la página **recopilando información** , revise los archivos que no se encontraron en la ubicación especificada en la página **archivos de instalación** de este asistente.</span><span class="sxs-lookup"><span data-stu-id="66fb9-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="66fb9-130">Si los archivos que se muestran no son obligatorios, seleccione **quitar estos archivos**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="66fb9-131">Si los archivos son obligatorios, haga clic en **anterior** y copie los archivos necesarios en el directorio especificado en la página **archivos de instalación** .</span><span class="sxs-lookup"><span data-stu-id="66fb9-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="66fb9-132">Nota</span><span class="sxs-lookup"><span data-stu-id="66fb9-132">Note</span></span>**  
   <span data-ttu-id="66fb9-133">Debe quitar los archivos no necesarios o hacer clic en **anterior** y ubicar los archivos necesarios para avanzar a la siguiente página de este asistente.</span><span class="sxs-lookup"><span data-stu-id="66fb9-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="66fb9-134">En la página **seleccionar archivos** , revise cuidadosamente los archivos detectados y borre cualquier archivo que deba quitarse del acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="66fb9-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="66fb9-135">Seleccione solo los archivos necesarios para que la aplicación se ejecute correctamente y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="66fb9-136">En la página **comprobar aplicaciones** , confirme que se muestran todos los archivos de instalación necesarios para compilar el paquete.</span><span class="sxs-lookup"><span data-stu-id="66fb9-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="66fb9-137">Cuando se usa el acelerador de paquetes para crear un nuevo paquete, todos los archivos de instalación que se muestran en el panel **aplicaciones** son necesarios para crear el paquete.</span><span class="sxs-lookup"><span data-stu-id="66fb9-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="66fb9-138">Si es necesario, para agregar archivos de instalador adicionales, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="66fb9-139">Para quitar los archivos de instalación innecesarios, seleccione el archivo instalador y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="66fb9-140">Para editar las propiedades asociadas con un instalador, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="66fb9-141">Los archivos de instalación especificados en este paso se requerirán cuando se use el acelerador de paquetes para crear un nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="66fb9-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="66fb9-142">Una vez que haya confirmado la información que se muestra, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="66fb9-143">En la página **seleccionar guía** , para especificar un archivo que contiene información sobre el acelerador de paquetes, haga clic en **examinar**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="66fb9-144">Por ejemplo, este archivo puede contener información sobre cómo debe configurarse el equipo que ejecuta el secuenciador, información de requisitos previos de la aplicación para equipos de destino y notas generales.</span><span class="sxs-lookup"><span data-stu-id="66fb9-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="66fb9-145">Debes proporcionar toda la información necesaria para que el acelerador de paquetes se aplique correctamente.</span><span class="sxs-lookup"><span data-stu-id="66fb9-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="66fb9-146">El archivo que seleccione debe tener formato de texto enriquecido (. rtf) o de archivo de texto (. txt).</span><span class="sxs-lookup"><span data-stu-id="66fb9-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="66fb9-147">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-147">Click **Next**.</span></span>

9. <span data-ttu-id="66fb9-148">En la página **crear acelerador de paquetes** , para especificar dónde desea guardar el acelerador de paquetes, haga clic en **examinar** y seleccione el directorio.</span><span class="sxs-lookup"><span data-stu-id="66fb9-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="66fb9-149">En la página **finalización** , para cerrar el Asistente para **crear aceleradores de paquetes** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="66fb9-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="66fb9-150">Importante</span><span class="sxs-lookup"><span data-stu-id="66fb9-150">Important</span></span>**  
   <span data-ttu-id="66fb9-151">Para garantizar que el acelerador de paquetes sea lo más seguro posible, y para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes, siempre debe firmar digitalmente el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="66fb9-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="66fb9-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66fb9-152">Related topics</span></span>


<span data-ttu-id="66fb9-153">Configuración del Application Virtualization Sequencer (App-V 4,6 SP1) [Cómo aplicar un acelerador de paquetes para crear un paquete de aplicaciones virtual (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="66fb9-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>









