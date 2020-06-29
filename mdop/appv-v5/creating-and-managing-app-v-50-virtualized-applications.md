---
title: Creación y administración de aplicaciones virtualizadas de App-V 5.0
description: Creación y administración de aplicaciones virtualizadas de App-V 5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814702"
---
# <span data-ttu-id="5cb8e-103">Creación y administración de aplicaciones virtualizadas de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5cb8e-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="5cb8e-104">Después de implementar correctamente el secuenciador de Microsoft Application Virtualization (App-V) 5,0, puede usarlo para supervisar y registrar el proceso de instalación y configuración para que una aplicación se ejecute como una aplicación virtualizada.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="5cb8e-105">**Nota:**  Para obtener más información sobre cómo configurar Microsoft Application Virtualization (App-V) 5,0 secuenciador, procedimientos recomendados de secuencias y un ejemplo de creación y actualización de una aplicación virtual, consulte la [Guía de secuenciación de Microsoft Application virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 secuencias Guide.docx).</span><span class="sxs-lookup"><span data-stu-id="5cb8e-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="5cb8e-106">Secuenciar una aplicación</span><span class="sxs-lookup"><span data-stu-id="5cb8e-106">Sequencing an application</span></span>


<span data-ttu-id="5cb8e-107">Puede usar el secuenciador de aplicaciones-V 5,0 para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="5cb8e-108">Cree paquetes virtuales que se puedan implementar en equipos que ejecuten el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="5cb8e-109">Actualizar paquetes existentes.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-109">Upgrade existing packages.</span></span> <span data-ttu-id="5cb8e-110">Puede expandir un paquete existente en el equipo que ejecuta el secuenciador y, a continuación, actualizar la aplicación para crear una versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="5cb8e-111">Editar la información de configuración asociada a un paquete existente.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="5cb8e-112">Por ejemplo, puede Agregar un acceso directo o modificar una asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="5cb8e-113">**Nota:**  Debe crear accesos directos y guardarlos en una ubicación de red disponible para permitir la itinerancia.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="5cb8e-114">Si se crea un acceso directo y se guarda en una ubicación privada, el paquete debe publicarse localmente en el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="5cb8e-115">Convertir paquetes virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="5cb8e-116">El secuenciador utiliza **% TMP% \ \ Scratch** o **% temp% \ \ Scratch** Directory y el directorio **temp** para almacenar los archivos temporales durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="5cb8e-117">En el equipo que ejecuta el secuenciador, debe configurar estos directorios con espacio libre en disco equivalente a los requisitos estimados de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="5cb8e-118">La configuración de los directorios temporales y el directorio Temp en distintas particiones del disco duro puede ayudar a mejorar el rendimiento durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="5cb8e-119">Al usar el secuenciador para crear una nueva aplicación virtual, se crean los siguientes archivos de la lista.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="5cb8e-120">Estos archivos constituyen el paquete de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="5cb8e-121">archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-121">.msi file.</span></span> <span data-ttu-id="5cb8e-122">El secuenciador crea este archivo de Windows Installer (. msi) y se usa para instalar el paquete virtual en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="5cb8e-123">Archivo de Report.xml.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-123">Report.xml file.</span></span> <span data-ttu-id="5cb8e-124">En este archivo, el secuenciador guarda todos los problemas, advertencias y errores detectados durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="5cb8e-125">Muestra la información después de que se haya creado el paquete.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="5cb8e-126">Puede obtener este informe para diagnosticar y solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="5cb8e-127">archivo. appv.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-127">.appv file.</span></span> <span data-ttu-id="5cb8e-128">Este es el archivo de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="5cb8e-129">Archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-129">Deployment configuration file.</span></span> <span data-ttu-id="5cb8e-130">El archivo de configuración de implementación determina cómo se implementará la aplicación virtual en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="5cb8e-131">Archivo de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-131">User configuration file.</span></span> <span data-ttu-id="5cb8e-132">El archivo de configuración de usuario determina cómo se ejecutará la aplicación virtual en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="5cb8e-133">**Importante**  Debe configurar las carpetas% TMP% y% TEMP% que el convertidor de paquetes usa para ser una ubicación y un directorio seguros.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="5cb8e-134">Un administrador solo puede tener acceso a una ubicación segura.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="5cb8e-135">Además, cuando ordene el paquete, debe guardar el paquete en una ubicación segura o asegurarse de que ningún otro usuario pueda iniciar sesión durante el proceso de conversión y supervisión.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="5cb8e-136">El cuadro de diálogo **Opciones** en la consola del secuenciador contiene las siguientes pestañas:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="5cb8e-137">**General**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-137">**General**.</span></span> <span data-ttu-id="5cb8e-138">Use esta pestaña para habilitar la ejecución de actualizaciones de Microsoft durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="5cb8e-139">Seleccione **anexar la versión del paquete al nombre del archivo** para configurar la secuencia para agregar un número de versión al paquete virtualizado que se secuencia.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="5cb8e-140">Seleccione **confiar siempre en la fuente de aceleradores de paquetes** para crear paquetes virtuales con un acelerador de paquetes sin que se le pida autorización.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="5cb8e-141">**Importante**  Los aceleradores de paquetes creados con App-V 4.6 no son compatibles con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="5cb8e-142">**Elementos de análisis**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-142">**Parse Items**.</span></span> <span data-ttu-id="5cb8e-143">Esta pestaña muestra las ubicaciones de la ruta de acceso de los archivos asociada que se analizarán o se convertirán en token en en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="5cb8e-144">Los tokens son útiles para agregar archivos mediante la pestaña **archivos del paquete** en la **Edición avanzada**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="5cb8e-145">**Elementos de exclusión**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-145">**Exclusion Items**.</span></span> <span data-ttu-id="5cb8e-146">Use esta pestaña para especificar qué carpetas y directorios no se deben supervisar durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="5cb8e-147">Para agregar datos de la aplicación local que se guardan en la carpeta de datos de la aplicación local en el paquete, haga clic en **nuevo** y especifique la ubicación y el **tipo de asignación**asociada.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="5cb8e-148">Esta opción es necesaria para algunos paquetes.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-148">This option is required for some packages.</span></span>

<span data-ttu-id="5cb8e-149">App-V 5,0 admite aplicaciones que incluyen servicios de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="5cb8e-150">Si una aplicación incluye un servicio de Windows, el servicio se incluirá en el paquete virtual secuencial siempre que esté instalado mientras lo supervisa el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="5cb8e-151">Si una aplicación virtual crea un servicio de Windows cuando se ejecuta por primera vez, después de la instalación, la aplicación debe ejecutarse mientras el secuenciador está supervisando para que el servicio de Windows se agregue al paquete.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="5cb8e-152">Solo se admiten los servicios que se ejecutan en la cuenta del sistema local.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="5cb8e-153">Los servicios que están configurados para AutoStart o AutoStart retardado se inician antes de que la primera aplicación virtual de un paquete se ejecute dentro del entorno virtual del paquete.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="5cb8e-154">Los servicios de Windows que están configurados para iniciarse a petición de una aplicación se inician cuando la aplicación virtual dentro del paquete inicia el servicio mediante una llamada de API.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="5cb8e-155">Cómo secuenciar una nueva aplicación con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5cb8e-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="5cb8e-156">Compatibilidad con la extensión Shell de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="5cb8e-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="5cb8e-157">App-V 5.0 SP2 admite extensiones de Shell.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="5cb8e-158">Las extensiones de Shell se detectarán e incrustarán en el paquete durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="5cb8e-159">Las extensiones de Shell se incrustan automáticamente en el paquete durante el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="5cb8e-160">Cuando se publica el paquete, la extensión de Shell proporciona a los usuarios la misma funcionalidad que si la aplicación se instalara de forma local.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="5cb8e-161">Requisitos para usar extensiones de Shell:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="5cb8e-162">Los paquetes que contienen extensiones de Shell insertadas deben publicarse globalmente.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="5cb8e-163">La aplicación no requiere ninguna configuración ni configuración adicional en el cliente para habilitar la funcionalidad de la extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="5cb8e-164">El "bits" de la aplicación, el secuenciador y el cliente de App-V deben coincidir, o las extensiones de Shell no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="5cb8e-165">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-165">For example:</span></span>

    -   <span data-ttu-id="5cb8e-166">La versión de la aplicación es 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="5cb8e-167">El secuenciador se está ejecutando en un equipo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="5cb8e-168">El paquete se está entregando a un equipo cliente de aplicación de 64 bits de-V.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="5cb8e-169">En la siguiente tabla se enumeran las extensiones de Shell compatibles:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5cb8e-170">Administrador</span><span class="sxs-lookup"><span data-stu-id="5cb8e-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="5cb8e-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cb8e-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cb8e-172">Controlador del menú contextual</span><span class="sxs-lookup"><span data-stu-id="5cb8e-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-173">Agrega elementos de menú al menú contextual.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="5cb8e-174">Se llama antes de mostrar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cb8e-175">Controlador de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="5cb8e-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-176">Controla la acción en la que se hace clic con el botón derecho, arrastra y coloca y modifica el menú contextual que aparece.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cb8e-177">Controlador de destino de colocación</span><span class="sxs-lookup"><span data-stu-id="5cb8e-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-178">Controla la acción después de arrastrar un objeto de datos y colocarlo sobre un destino de colocación, como un archivo.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cb8e-179">Controlador de objetos de datos</span><span class="sxs-lookup"><span data-stu-id="5cb8e-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-180">Controla la acción después de copiar un archivo en el portapapeles o arrastrarlo y colocarlo sobre un destino.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="5cb8e-181">Puede proporcionar formatos adicionales del portapapeles para el destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cb8e-182">Controlador de hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="5cb8e-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-183">Reemplaza o agrega páginas al cuadro de diálogo de la hoja de propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cb8e-184">Controlador de insugerencias</span><span class="sxs-lookup"><span data-stu-id="5cb8e-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-185">Permite recuperar indicadores y información de recuadro de sugerencias para un elemento y mostrarlo dentro de una información emergente al pasar el mouse.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5cb8e-186">Controlador de columnas</span><span class="sxs-lookup"><span data-stu-id="5cb8e-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-187">Permite crear y mostrar columnas personalizadas en la <strong> vista de detalles del explorador de Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="5cb8e-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="5cb8e-188">Puede usarse para ampliar la ordenación y la agrupación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5cb8e-189">Controlador de vista previa</span><span class="sxs-lookup"><span data-stu-id="5cb8e-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5cb8e-190">Habilita una vista previa de un archivo para que se muestre en el panel de vista previa del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5cb8e-191">Compatibilidad con la extensión de archivo de copia en escritura (CoW)</span><span class="sxs-lookup"><span data-stu-id="5cb8e-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="5cb8e-192">Las extensiones de archivo de copia en escritura (CoW) permiten que App-V 5,0 se escriba dinámicamente en ubicaciones específicas del paquete virtual mientras se está usando.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="5cb8e-193">En la siguiente tabla se muestran los tipos de archivo que pueden existir en un paquete virtual en el directorio VFS, pero que no se pueden actualizar en el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="5cb8e-194">Se pueden modificar todos los demás archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="5cb8e-195">. ACM</span><span class="sxs-lookup"><span data-stu-id="5cb8e-195">.acm</span></span>

<span data-ttu-id="5cb8e-196">. asa</span><span class="sxs-lookup"><span data-stu-id="5cb8e-196">.asa</span></span>

<span data-ttu-id="5cb8e-197">.asp</span><span class="sxs-lookup"><span data-stu-id="5cb8e-197">.asp</span></span>

<span data-ttu-id="5cb8e-198">. aspx</span><span class="sxs-lookup"><span data-stu-id="5cb8e-198">.aspx</span></span>

<span data-ttu-id="5cb8e-199">. AX</span><span class="sxs-lookup"><span data-stu-id="5cb8e-199">.ax</span></span>

<span data-ttu-id="5cb8e-200">.bat</span><span class="sxs-lookup"><span data-stu-id="5cb8e-200">.bat</span></span>

<span data-ttu-id="5cb8e-201">.cer</span><span class="sxs-lookup"><span data-stu-id="5cb8e-201">.cer</span></span>

<span data-ttu-id="5cb8e-202">.chm</span><span class="sxs-lookup"><span data-stu-id="5cb8e-202">.chm</span></span>

<span data-ttu-id="5cb8e-203">. CLB</span><span class="sxs-lookup"><span data-stu-id="5cb8e-203">.clb</span></span>

<span data-ttu-id="5cb8e-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="5cb8e-204">.cmd</span></span>

<span data-ttu-id="5cb8e-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="5cb8e-205">.cnt</span></span>

<span data-ttu-id="5cb8e-206">. CNV</span><span class="sxs-lookup"><span data-stu-id="5cb8e-206">.cnv</span></span>

<span data-ttu-id="5cb8e-207">.com</span><span class="sxs-lookup"><span data-stu-id="5cb8e-207">.com</span></span>

<span data-ttu-id="5cb8e-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="5cb8e-208">.cpl</span></span>

<span data-ttu-id="5cb8e-209">.cpx</span><span class="sxs-lookup"><span data-stu-id="5cb8e-209">.cpx</span></span>

<span data-ttu-id="5cb8e-210">.crt</span><span class="sxs-lookup"><span data-stu-id="5cb8e-210">.crt</span></span>

<span data-ttu-id="5cb8e-211">.dll</span><span class="sxs-lookup"><span data-stu-id="5cb8e-211">.dll</span></span>

<span data-ttu-id="5cb8e-212">.drv</span><span class="sxs-lookup"><span data-stu-id="5cb8e-212">.drv</span></span>

<span data-ttu-id="5cb8e-213">.exe</span><span class="sxs-lookup"><span data-stu-id="5cb8e-213">.exe</span></span>

<span data-ttu-id="5cb8e-214">.fon</span><span class="sxs-lookup"><span data-stu-id="5cb8e-214">.fon</span></span>

<span data-ttu-id="5cb8e-215">.grp</span><span class="sxs-lookup"><span data-stu-id="5cb8e-215">.grp</span></span>

<span data-ttu-id="5cb8e-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="5cb8e-216">.hlp</span></span>

<span data-ttu-id="5cb8e-217">.hta</span><span class="sxs-lookup"><span data-stu-id="5cb8e-217">.hta</span></span>

<span data-ttu-id="5cb8e-218">. IME</span><span class="sxs-lookup"><span data-stu-id="5cb8e-218">.ime</span></span>

<span data-ttu-id="5cb8e-219">.inf</span><span class="sxs-lookup"><span data-stu-id="5cb8e-219">.inf</span></span>

<span data-ttu-id="5cb8e-220">.ins</span><span class="sxs-lookup"><span data-stu-id="5cb8e-220">.ins</span></span>

<span data-ttu-id="5cb8e-221">.isp</span><span class="sxs-lookup"><span data-stu-id="5cb8e-221">.isp</span></span>

<span data-ttu-id="5cb8e-222">. su</span><span class="sxs-lookup"><span data-stu-id="5cb8e-222">.its</span></span>

<span data-ttu-id="5cb8e-223">.js</span><span class="sxs-lookup"><span data-stu-id="5cb8e-223">.js</span></span>

<span data-ttu-id="5cb8e-224">.jse</span><span class="sxs-lookup"><span data-stu-id="5cb8e-224">.jse</span></span>

<span data-ttu-id="5cb8e-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="5cb8e-225">.lnk</span></span>

<span data-ttu-id="5cb8e-226">.msc</span><span class="sxs-lookup"><span data-stu-id="5cb8e-226">.msc</span></span>

<span data-ttu-id="5cb8e-227">.msi</span><span class="sxs-lookup"><span data-stu-id="5cb8e-227">.msi</span></span>

<span data-ttu-id="5cb8e-228">.msp</span><span class="sxs-lookup"><span data-stu-id="5cb8e-228">.msp</span></span>

<span data-ttu-id="5cb8e-229">.mst</span><span class="sxs-lookup"><span data-stu-id="5cb8e-229">.mst</span></span>

<span data-ttu-id="5cb8e-230">. MUI</span><span class="sxs-lookup"><span data-stu-id="5cb8e-230">.mui</span></span>

<span data-ttu-id="5cb8e-231">. NLS</span><span class="sxs-lookup"><span data-stu-id="5cb8e-231">.nls</span></span>

<span data-ttu-id="5cb8e-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="5cb8e-232">.ocx</span></span>

<span data-ttu-id="5cb8e-233">. PAL</span><span class="sxs-lookup"><span data-stu-id="5cb8e-233">.pal</span></span>

<span data-ttu-id="5cb8e-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="5cb8e-234">.pcd</span></span>

<span data-ttu-id="5cb8e-235">.pif</span><span class="sxs-lookup"><span data-stu-id="5cb8e-235">.pif</span></span>

<span data-ttu-id="5cb8e-236">.reg</span><span class="sxs-lookup"><span data-stu-id="5cb8e-236">.reg</span></span>

<span data-ttu-id="5cb8e-237">.scf</span><span class="sxs-lookup"><span data-stu-id="5cb8e-237">.scf</span></span>

<span data-ttu-id="5cb8e-238">.scr</span><span class="sxs-lookup"><span data-stu-id="5cb8e-238">.scr</span></span>

<span data-ttu-id="5cb8e-239">. SCT</span><span class="sxs-lookup"><span data-stu-id="5cb8e-239">.sct</span></span>

<span data-ttu-id="5cb8e-240">.shb</span><span class="sxs-lookup"><span data-stu-id="5cb8e-240">.shb</span></span>

<span data-ttu-id="5cb8e-241">.shs</span><span class="sxs-lookup"><span data-stu-id="5cb8e-241">.shs</span></span>

<span data-ttu-id="5cb8e-242">.sys</span><span class="sxs-lookup"><span data-stu-id="5cb8e-242">.sys</span></span>

<span data-ttu-id="5cb8e-243">. tlb</span><span class="sxs-lookup"><span data-stu-id="5cb8e-243">.tlb</span></span>

<span data-ttu-id="5cb8e-244">. TSP</span><span class="sxs-lookup"><span data-stu-id="5cb8e-244">.tsp</span></span>

<span data-ttu-id="5cb8e-245">.url</span><span class="sxs-lookup"><span data-stu-id="5cb8e-245">.url</span></span>

<span data-ttu-id="5cb8e-246">.vb</span><span class="sxs-lookup"><span data-stu-id="5cb8e-246">.vb</span></span>

<span data-ttu-id="5cb8e-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="5cb8e-247">.vbe</span></span>

<span data-ttu-id="5cb8e-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="5cb8e-248">.vbs</span></span>

<span data-ttu-id="5cb8e-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="5cb8e-249">.vsmacros</span></span>

<span data-ttu-id="5cb8e-250">.ws</span><span class="sxs-lookup"><span data-stu-id="5cb8e-250">.ws</span></span>

<span data-ttu-id="5cb8e-251">. ESC</span><span class="sxs-lookup"><span data-stu-id="5cb8e-251">.esc</span></span>

<span data-ttu-id="5cb8e-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="5cb8e-252">.wsf</span></span>

<span data-ttu-id="5cb8e-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="5cb8e-253">.wsh</span></span>

 

## <span data-ttu-id="5cb8e-254">Modificar un paquete de aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="5cb8e-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="5cb8e-255">Puede usar el secuenciador para modificar un paquete existente.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="5cb8e-256">El equipo en el que realiza esta acción debe coincidir con la arquitectura de chip del equipo que usó para crear la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="5cb8e-257">Por ejemplo, si inicialmente ha secuenciado un paquete con un equipo que ejecuta un sistema operativo de 64 bits, debe modificar el paquete con un equipo que ejecute un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="5cb8e-258">Cómo modificar un paquete de aplicaciones virtuales existentes</span><span class="sxs-lookup"><span data-stu-id="5cb8e-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="5cb8e-259">Crear una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="5cb8e-259">Creating a project template</span></span>


<span data-ttu-id="5cb8e-260">Un archivo. appvt es una plantilla de proyecto que se puede usar para guardar la configuración personalizada más frecuentemente.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="5cb8e-261">Puede usar esta configuración más fácilmente para futuras secuencias.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="5cb8e-262">Las plantillas de proyecto de App-V 5,0 difieren de los aceleradores de aplicaciones de App-V 5,0 porque los aceleradores de aplicaciones de App-V 5,0 son específicos de la aplicación y las plantillas de proyecto de App-V 5,0 se pueden aplicar a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="5cb8e-263">Además, no puede usar una plantilla de proyecto cuando usa un acelerador de paquetes para crear un paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="5cb8e-264">La siguiente configuración general se guarda con una plantilla de proyecto de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="5cb8e-265">Una plantilla puede especificar y almacenar varias opciones de configuración de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5cb8e-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="5cb8e-266">**Opciones de supervisión avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="5cb8e-267">Permite que Microsoft Update se ejecute durante la supervisión.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="5cb8e-268">Guarda la configuración de la opción permitir interacción local</span><span class="sxs-lookup"><span data-stu-id="5cb8e-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="5cb8e-269">**Opciones generales**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-269">**General Options**.</span></span> <span data-ttu-id="5cb8e-270">Permite usar **Windows Installer**, **anexar la versión del paquete al nombre de archivo**.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="5cb8e-271">Elementos de exclusión.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-271">Exclusion Items.</span></span>** <span data-ttu-id="5cb8e-272">Contiene la lista de patrones de exclusión.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="5cb8e-273">Cómo crear y usar una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="5cb8e-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="5cb8e-274">Crear un acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="5cb8e-274">Creating a package accelerator</span></span>


<span data-ttu-id="5cb8e-275">**Nota:**  Los aceleradores de paquetes creados con una versión anterior de App-V deben volver a crearse con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="5cb8e-276">Puede usar los aceleradores de paquetes de App-V 5,0 para generar automáticamente nuevos paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="5cb8e-277">Después de crear correctamente un acelerador de paquetes, puede volver a usar y compartir el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="5cb8e-278">En algunas situaciones, para crear el acelerador de paquetes es posible que tenga que instalar la aplicación de forma local en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="5cb8e-279">En tal caso, primero debe intentar crear el acelerador de paquetes con los medios de instalación.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="5cb8e-280">Si se necesitan varios archivos que faltan, debe instalar la aplicación localmente en el equipo que ejecuta el secuenciador y, a continuación, crear el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="5cb8e-281">Después de crear correctamente un acelerador de paquetes, puede volver a usar y compartir el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="5cb8e-282">La creación de aceleradores de paquetes de App-V 5,0 es una tarea avanzada.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="5cb8e-283">Los aceleradores de paquetes pueden contener contraseña e información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="5cb8e-284">Por lo tanto, debe guardar los aceleradores de paquetes y los medios de instalación asociados en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="5cb8e-285">Cómo crear un acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="5cb8e-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="5cb8e-286">Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="5cb8e-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="5cb8e-287">Informe de errores de secuenciador</span><span class="sxs-lookup"><span data-stu-id="5cb8e-287">Sequencer error reporting</span></span>


<span data-ttu-id="5cb8e-288">El secuenciador de 5,0 de App-V puede detectar problemas de secuencia comunes durante la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="5cb8e-289">La página del **Informe de instalación** al final del asistente de secuenciación muestra mensajes de diagnóstico clasificados en **errores**, **advertencias**e **información** , según la gravedad del problema.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="5cb8e-290">También puede encontrar información adicional sobre errores de secuenciación con el visor de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="5cb8e-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="5cb8e-291">Otros recursos para el secuenciador de aplicaciones-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5cb8e-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="5cb8e-292">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5cb8e-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





