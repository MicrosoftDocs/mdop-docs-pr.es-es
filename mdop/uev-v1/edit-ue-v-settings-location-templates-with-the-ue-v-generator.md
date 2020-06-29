---
title: Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V
description: Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827111"
---
# <span data-ttu-id="5fa91-103">Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="5fa91-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="5fa91-104">Use el generador de virtualización de la experiencia del usuario de Microsoft (UE-V) para editar las plantillas de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="5fa91-105">Cuando se agregue la configuración revisada a las plantillas mediante el generador de UE-V, la información de versión de la plantilla se actualizará automáticamente para asegurarse de que las plantillas existentes implementadas en la empresa se actualicen correctamente.</span><span class="sxs-lookup"><span data-stu-id="5fa91-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="5fa91-106">Cómo modificar una plantilla de ubicación de configuración de UE-V con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="5fa91-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="5fa91-107">Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.</span><span class="sxs-lookup"><span data-stu-id="5fa91-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="5fa91-108">Haga clic en **editar una plantilla de ubicación de configuración**.</span><span class="sxs-lookup"><span data-stu-id="5fa91-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="5fa91-109">En la lista de plantillas usadas recientemente, seleccione la plantilla que desea editar.</span><span class="sxs-lookup"><span data-stu-id="5fa91-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="5fa91-110">Como alternativa, **vaya** al archivo de la plantilla de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="5fa91-111">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="5fa91-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="5fa91-112">Revise las ubicaciones **propiedades**, ubicaciones **del registro** y **archivos** de la plantilla de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="5fa91-113">Edite según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5fa91-113">Edit as needed.</span></span>

    -   <span data-ttu-id="5fa91-114">La pestaña **propiedades** le permite ver y editar las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="5fa91-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="5fa91-115">**Nombre**de la aplicación: el nombre de la aplicación escrito en la descripción de las propiedades del archivo del programa.</span><span class="sxs-lookup"><span data-stu-id="5fa91-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="5fa91-116">**Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa.</span><span class="sxs-lookup"><span data-stu-id="5fa91-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="5fa91-117">Este nombre suele tener la extensión. exe.</span><span class="sxs-lookup"><span data-stu-id="5fa91-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="5fa91-118">**Versión del producto**: número de versión del producto del archivo. exe de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fa91-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="5fa91-119">Esta propiedad, junto con la **versión del archivo**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="5fa91-120">Esta propiedad acepta un número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="5fa91-120">This property accepts a major version number.</span></span> <span data-ttu-id="5fa91-121">Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del producto.</span><span class="sxs-lookup"><span data-stu-id="5fa91-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="5fa91-122">**Versión**del archivo: el número de versión del archivo the.exe archivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fa91-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="5fa91-123">Esta propiedad, junto con la **versión del producto**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="5fa91-124">Esta propiedad acepta un número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="5fa91-124">This property accepts a major version number.</span></span> <span data-ttu-id="5fa91-125">Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del programa.</span><span class="sxs-lookup"><span data-stu-id="5fa91-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="5fa91-126">**Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="5fa91-127">**Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="5fa91-128">La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="5fa91-129">Puede editar las ubicaciones del registro mediante el menú desplegable **tareas** .</span><span class="sxs-lookup"><span data-stu-id="5fa91-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="5fa91-130">Las tareas incluyen agregar nuevas claves, editar el nombre o el ámbito de las claves existentes, eliminar claves y examinar el registro en el que se encuentran las teclas.</span><span class="sxs-lookup"><span data-stu-id="5fa91-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="5fa91-131">Al definir el ámbito del registro, puede usar el ámbito de **todas las opciones de configuración** para incluir todas las opciones de configuración del registro en la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="5fa91-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="5fa91-132">Use **todas las configuraciones** y **subclaves** para incluir todas las opciones de configuración del registro en la clave, las subclaves y la configuración de la subclave especificadas.</span><span class="sxs-lookup"><span data-stu-id="5fa91-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="5fa91-133">La pestaña **archivos** muestra la ruta de acceso del archivo y la máscara de archivo de las ubicaciones de archivo incluidas en la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="5fa91-134">Puede editar las ubicaciones de los archivos mediante el menú desplegable **tareas** .</span><span class="sxs-lookup"><span data-stu-id="5fa91-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="5fa91-135">Las tareas para ubicaciones de archivos incluyen la adición de nuevos archivos o ubicaciones de carpetas, la edición del ámbito de archivos o carpetas existentes, la eliminación de archivos o carpetas y la apertura de la ubicación seleccionada en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="5fa91-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="5fa91-136">Para incluir todos los archivos en la carpeta especificada, deje la máscara de archivo vacía.</span><span class="sxs-lookup"><span data-stu-id="5fa91-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="5fa91-137">Haga clic en **Guardar** para guardar los cambios en la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="5fa91-138">Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="5fa91-139">Salga de la aplicación de generación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5fa91-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="5fa91-140">Después de editar la plantilla de ubicación de configuración de una aplicación, debe probarla.</span><span class="sxs-lookup"><span data-stu-id="5fa91-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="5fa91-141">Implemente la plantilla de ubicación de configuración revisada en un entorno de laboratorio antes de ponerlo en producción en la empresa.</span><span class="sxs-lookup"><span data-stu-id="5fa91-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="5fa91-142">Cómo modificar manualmente una plantilla de ubicación de configuración</span><span class="sxs-lookup"><span data-stu-id="5fa91-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="5fa91-143">Crear una copia local de la plantilla de ubicación de configuración (archivo. xml).</span><span class="sxs-lookup"><span data-stu-id="5fa91-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="5fa91-144">Configuración de UE-V las plantillas de ubicación son archivos. XML que identifican las ubicaciones en las que los valores de la aplicación almacén.</span><span class="sxs-lookup"><span data-stu-id="5fa91-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="5fa91-145">Abra el archivo de plantilla de la ubicación de configuración con un editor XML.</span><span class="sxs-lookup"><span data-stu-id="5fa91-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="5fa91-146">Edite el archivo de plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5fa91-146">Edit the settings location template file.</span></span> <span data-ttu-id="5fa91-147">Todos los cambios deben cumplir con el archivo de esquema UE-V definido en SettingsLocationTempate. xsd.</span><span class="sxs-lookup"><span data-stu-id="5fa91-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="5fa91-148">De forma predeterminada, se encuentra una copia del archivo. xsd `\ProgramData\Microsoft\UEV\Templates` .</span><span class="sxs-lookup"><span data-stu-id="5fa91-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="5fa91-149">Guarde el archivo de plantilla de ubicación de configuración y cierre el editor XML.</span><span class="sxs-lookup"><span data-stu-id="5fa91-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="5fa91-150">Valide el archivo de plantilla de ubicación de configuración modificado con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5fa91-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="5fa91-151">Para obtener más información sobre cómo validar con el generador de UE-V, consulte [validar plantillas de ubicación de configuración de UE-v con el generador de UE-v](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span><span class="sxs-lookup"><span data-stu-id="5fa91-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="5fa91-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5fa91-152">Related topics</span></span>


[<span data-ttu-id="5fa91-153">Trabajo con plantillas personalizadas de UE-V y el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="5fa91-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="5fa91-154">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="5fa91-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





