---
title: Cómo crear un acelerador de paquetes
description: Cómo crear un acelerador de paquetes
author: dansimp
ms.assetid: b61f3581-7933-443e-b872-a96bed9ff8d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6893f2e9bb9db473d285026015c3399fb0074015
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814263"
---
# <span data-ttu-id="127db-103">Cómo crear un acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="127db-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="127db-104">Los aceleradores de paquetes de App-V 5,1 generan automáticamente nuevos paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="127db-104">App-V 5.1 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="127db-105">Nota</span><span class="sxs-lookup"><span data-stu-id="127db-105">Note</span></span>**  
<span data-ttu-id="127db-106">Puede usar PowerShell para crear un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="127db-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="127db-107">Para obtener más información [, vea cómo crear un acelerador de paquetes con PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="127db-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).</span></span>



<span data-ttu-id="127db-108">Use el procedimiento siguiente para crear un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="127db-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="127db-109">Importante</span><span class="sxs-lookup"><span data-stu-id="127db-109">Important</span></span>**  
<span data-ttu-id="127db-110">Los aceleradores de paquetes pueden contener contraseña e información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="127db-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="127db-111">Por lo tanto, debe guardar los aceleradores de paquetes y los medios de instalación asociados en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="127db-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.1 Package Accelerator is applied.</span></span>



**<span data-ttu-id="127db-112">Importante</span><span class="sxs-lookup"><span data-stu-id="127db-112">Important</span></span>**  
<span data-ttu-id="127db-113">Antes de comenzar con el procedimiento siguiente, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="127db-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="127db-114">Copie el paquete de la aplicación virtual que usará para crear el acelerador de paquetes localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="127db-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="127db-115">Copie todos los archivos de instalación necesarios asociados con el paquete de la aplicación virtual en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="127db-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="127db-116">Para crear un acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="127db-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="127db-117">Importante</span><span class="sxs-lookup"><span data-stu-id="127db-117">Important</span></span>**  
    <span data-ttu-id="127db-118">El secuenciador de 5,1 de App-V no concede derechos de licencia a la aplicación de software que usas para crear el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="127db-118">The App-V 5.1 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="127db-119">Debe cumplir todos los términos de licencia de usuario final de la aplicación que esté usando.</span><span class="sxs-lookup"><span data-stu-id="127db-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="127db-120">Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con App-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="127db-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.1 Sequencer.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="127db-121">Para iniciar el Asistente para **crear acelerador de paquetes** de App-v 5,1, en la consola de App-v 5,1 Sequencer, haga clic en **herramientas**  /  **crear acelerador**.</span><span class="sxs-lookup"><span data-stu-id="127db-121">To start the App-V 5.1 **Create Package Accelerator** wizard, in the App-V 5.1 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="127db-122">En la página **seleccionar paquete** , para especificar que un paquete de aplicación virtual existente se use para crear el acelerador de paquetes, haga clic en **examinar**y busque el paquete de aplicación virtual existente (archivo. appv).</span><span class="sxs-lookup"><span data-stu-id="127db-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="127db-123">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="127db-123">Tip</span></span>**  
   <span data-ttu-id="127db-124">Copie los archivos asociados con el paquete de aplicación virtual que planea usar localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="127db-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="127db-125">En la página **archivos de instalación** , para especificar la carpeta que contiene los archivos de instalación que usó para crear el paquete de aplicación virtual original, haga clic en **examinar**y, a continuación, seleccione el directorio que contiene los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="127db-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="127db-126">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="127db-126">Tip</span></span>**  
   <span data-ttu-id="127db-127">Copie la carpeta que contiene los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="127db-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="127db-128">Si la aplicación ya está instalada en el equipo que ejecuta el secuenciador, para especificar el archivo de instalación, seleccione **archivos instalados en el sistema local**.</span><span class="sxs-lookup"><span data-stu-id="127db-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="127db-129">Para usar esta opción, la aplicación debe estar instalada en la ubicación de instalación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="127db-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="127db-130">En la página **recopilando información** , revise los archivos que no se encontraron en la ubicación especificada en la página **archivos de instalación** de este asistente.</span><span class="sxs-lookup"><span data-stu-id="127db-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="127db-131">Si los archivos que se muestran no son obligatorios, seleccione **quitar estos archivos**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="127db-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="127db-132">Si los archivos son obligatorios, haga clic en **anterior** y copie los archivos necesarios en el directorio especificado en la página **archivos de instalación** .</span><span class="sxs-lookup"><span data-stu-id="127db-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="127db-133">Nota</span><span class="sxs-lookup"><span data-stu-id="127db-133">Note</span></span>**  
   <span data-ttu-id="127db-134">Debe quitar los archivos no necesarios o hacer clic en **anterior** y ubicar los archivos necesarios para avanzar a la siguiente página de este asistente.</span><span class="sxs-lookup"><span data-stu-id="127db-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="127db-135">En la página **seleccionar archivos** , revise cuidadosamente los archivos detectados y borre cualquier archivo que deba quitarse del acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="127db-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="127db-136">Seleccione solo los archivos necesarios para que la aplicación se ejecute correctamente y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="127db-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="127db-137">En la página **comprobar aplicaciones** , confirme que se muestran todos los archivos de instalación necesarios para compilar el paquete.</span><span class="sxs-lookup"><span data-stu-id="127db-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="127db-138">Cuando se usa el acelerador de paquetes para crear un nuevo paquete, todos los archivos de instalación que se muestran en el panel **aplicaciones** son necesarios para crear el paquete.</span><span class="sxs-lookup"><span data-stu-id="127db-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="127db-139">Si es necesario, para agregar archivos de instalador adicionales, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="127db-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="127db-140">Para quitar los archivos de instalación innecesarios, seleccione el archivo instalador y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="127db-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="127db-141">Para editar las propiedades asociadas con un instalador, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="127db-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="127db-142">Los archivos de instalación especificados en este paso se requerirán cuando se use el acelerador de paquetes para crear un nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="127db-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="127db-143">Una vez que haya confirmado la información que se muestra, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="127db-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="127db-144">En la página **seleccionar guía** , para especificar un archivo que contiene información sobre el acelerador de paquetes, haga clic en **examinar**.</span><span class="sxs-lookup"><span data-stu-id="127db-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="127db-145">Por ejemplo, este archivo puede contener información sobre cómo debe configurarse el equipo que ejecuta el secuenciador, información de requisitos previos de la aplicación para equipos de destino y notas generales.</span><span class="sxs-lookup"><span data-stu-id="127db-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="127db-146">Debes proporcionar toda la información necesaria para que el acelerador de paquetes se aplique correctamente.</span><span class="sxs-lookup"><span data-stu-id="127db-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="127db-147">El archivo que seleccione debe tener formato de texto enriquecido (. rtf) o de archivo de texto (. txt).</span><span class="sxs-lookup"><span data-stu-id="127db-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="127db-148">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="127db-148">Click **Next**.</span></span>

10. <span data-ttu-id="127db-149">En la página **crear acelerador de paquetes** , para especificar dónde desea guardar el acelerador de paquetes, haga clic en **examinar** y seleccione el directorio.</span><span class="sxs-lookup"><span data-stu-id="127db-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="127db-150">En la página **finalización** , para cerrar el Asistente para **crear aceleradores de paquetes** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="127db-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="127db-151">Importante</span><span class="sxs-lookup"><span data-stu-id="127db-151">Important</span></span>**  
   <span data-ttu-id="127db-152">Para garantizar que el acelerador de paquetes sea lo más seguro posible, y para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes, siempre debe firmar digitalmente el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="127db-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="127db-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="127db-153">Related topics</span></span>


[<span data-ttu-id="127db-154">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="127db-154">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="127db-155">Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="127db-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)









