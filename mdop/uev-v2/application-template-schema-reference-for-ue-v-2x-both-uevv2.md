---
title: Referencia de esquema de plantilla de aplicación para UE-V 2. x
description: Referencia de esquema de plantilla de aplicación para UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827410"
---
# <span data-ttu-id="5f418-103">Referencia de esquema de plantilla de aplicación para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="5f418-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="5f418-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 use las plantillas de ubicación de configuración XML para definir la configuración de la aplicación de escritorio y la configuración de Windows que se capturan y aplican en UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="5f418-105">UE-V incluye un conjunto de plantillas de ubicación de configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f418-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="5f418-106">También puede crear plantillas de ubicación de configuración personalizadas con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="5f418-107">Un usuario avanzado puede personalizar el archivo XML para una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="5f418-108">En este tema se detalla la estructura XML de las plantillas de ubicación de configuración de UE-V 2,1 (SP1) y 2,0 y se proporcionan instrucciones para editar estos archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="5f418-109">Referencia de esquema de plantilla de aplicación de UE-V 2,1 y 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="5f418-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="5f418-110">En esta sección se detalla la estructura XML de la plantilla de ubicación de configuración de UE-V 2,1 y 2,1 SP1 y se proporcionan instrucciones para editar este archivo.</span><span class="sxs-lookup"><span data-stu-id="5f418-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="5f418-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5f418-111">In This Section</span></span>

-   [<span data-ttu-id="5f418-112">Atributo de declaración y de codificación XML</span><span class="sxs-lookup"><span data-stu-id="5f418-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="5f418-113">Espacio de nombres y elemento raíz</span><span class="sxs-lookup"><span data-stu-id="5f418-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="5f418-114">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="5f418-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="5f418-115">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="5f418-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="5f418-116">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="5f418-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="5f418-117">Elemento version</span><span class="sxs-lookup"><span data-stu-id="5f418-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="5f418-118">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="5f418-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="5f418-119">Procesos y elemento de proceso</span><span class="sxs-lookup"><span data-stu-id="5f418-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="5f418-120">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="5f418-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="5f418-121">Elemento común</span><span class="sxs-lookup"><span data-stu-id="5f418-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="5f418-122">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="5f418-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="5f418-123">Apéndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="5f418-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="5f418-124">Atributo de declaración y de codificación XML</span><span class="sxs-lookup"><span data-stu-id="5f418-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="5f418-125">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-125">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-126">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-126">Type: String</span></span>**

<span data-ttu-id="5f418-127">La declaración XML debe especificar el atributo de versión XML 1,0 ( &lt; ? XML version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="5f418-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="5f418-128">Las plantillas de ubicación de configuración creadas por el generador de UE-V se guardan en la codificación UTF-8, aunque la codificación no se especifica explícitamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="5f418-129">Le recomendamos que incluya el atributo de codificación = "UTF-8" en este elemento como procedimiento recomendado.</span><span class="sxs-lookup"><span data-stu-id="5f418-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="5f418-130">Todas las plantillas incluidas con el producto especifican también esta etiqueta (vea los documentos de la experiencia del usuario de%ProgramFiles%\\Microsoft Virtualization\\Templates por referencia).</span><span class="sxs-lookup"><span data-stu-id="5f418-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="5f418-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="5f418-132">Espacio de nombres y elemento raíz</span><span class="sxs-lookup"><span data-stu-id="5f418-132">Namespace and Root Element</span></span>

**<span data-ttu-id="5f418-133">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-133">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-134">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-134">Type: String</span></span>**

<span data-ttu-id="5f418-135">UE-V usa el https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espacio de nombres para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f418-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="5f418-136">SettingsLocationTemplate es el elemento raíz y contiene todos los demás elementos.</span><span class="sxs-lookup"><span data-stu-id="5f418-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="5f418-137">SettingsLocationTemplate de referencia en todas las plantillas que usan esta etiqueta:</span><span class="sxs-lookup"><span data-stu-id="5f418-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="5f418-138">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="5f418-138">Data types</span></span>

<span data-ttu-id="5f418-139">Estos son los tipos de datos para el esquema de la plantilla de aplicación UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="5f418-140">**GUID** GUID describe una expresión regular de identificador global único estándar con el formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="5f418-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="5f418-141">Se usa en el elemento Filesetting\\Root\\KnownFolder para comprobar el formato de las carpetas conocidas.</span><span class="sxs-lookup"><span data-stu-id="5f418-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="5f418-142">**FilenameString** FilenameString se refiere al nombre de archivo de un proceso que se va a supervisar.</span><span class="sxs-lookup"><span data-stu-id="5f418-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="5f418-143">Sus valores están restringidos por la función regex \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, (es decir, no pueden contener caracteres de barra invertida o asterisco o signo de interrogación; caracteres comodín, el carácter de canalización, el signo mayor que o menor que, la barra diagonal o los caracteres de dos puntos).</span><span class="sxs-lookup"><span data-stu-id="5f418-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="5f418-144">**IDString** IDString se refiere al valor de identificador de elementos de la aplicación, SettingsLocationTemplate y elementos comunes (se usa para describir conjuntos de aplicaciones que comparten una configuración común).</span><span class="sxs-lookup"><span data-stu-id="5f418-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="5f418-145">Está restringido por el mismo Regex que FilenameString (\ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="5f418-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="5f418-146">**TemplateVersion** TemplateVersion es un valor entero que se usa para describir la revisión de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="5f418-147">Su valor puede oscilar entre 0 y 2147483647.</span><span class="sxs-lookup"><span data-stu-id="5f418-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="5f418-148">**Vacío** Vacío hace referencia a un valor null.</span><span class="sxs-lookup"><span data-stu-id="5f418-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="5f418-149">Se usa en Process\\ShellProcess para indicar que no hay ningún proceso para supervisar.</span><span class="sxs-lookup"><span data-stu-id="5f418-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="5f418-150">Este valor no debe usarse en ninguna plantilla de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="5f418-151">**Autor** El tipo de datos autor es un tipo complejo que identifica al autor de una plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="5f418-152">Contiene dos elementos secundarios: **Name** y **email**.</span><span class="sxs-lookup"><span data-stu-id="5f418-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="5f418-153">En el tipo de datos autor, el elemento nombre es obligatorio mientras que el elemento de correo electrónico es opcional.</span><span class="sxs-lookup"><span data-stu-id="5f418-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="5f418-154">Este tipo se describe más detalladamente en el elemento SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="5f418-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="5f418-155">**Intervalo** Range define una clase Integer formada por dos elementos secundarios: **Minimum** y **Maximum**.</span><span class="sxs-lookup"><span data-stu-id="5f418-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="5f418-156">Este tipo de datos se implementa en el tipo de datos ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="5f418-157">Si se especifica, se deben incluir los valores mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="5f418-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="5f418-158">**ProcessVersion** ProcessVersion define un tipo con cuatro elementos secundarios: **principal**, **secundario**, de **compilación**y de **revisión**.</span><span class="sxs-lookup"><span data-stu-id="5f418-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="5f418-159">Este tipo de datos es utilizado por el elemento Process para rellenar sus valores ProductVersion y FileVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="5f418-160">Los datos de este tipo son un valor de rango.</span><span class="sxs-lookup"><span data-stu-id="5f418-160">The data for this type is a Range value.</span></span> <span data-ttu-id="5f418-161">El elemento secundario principal es obligatorio y el resto es opcional.</span><span class="sxs-lookup"><span data-stu-id="5f418-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="5f418-162">**Arquitectura** La arquitectura enumera dos valores posibles: **Win32** y **Win64**.</span><span class="sxs-lookup"><span data-stu-id="5f418-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="5f418-163">Estos valores se usan para especificar la arquitectura de los procesos.</span><span class="sxs-lookup"><span data-stu-id="5f418-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="5f418-164">**Proceso** El tipo de datos proceso es un contenedor que se usa para describir los procesos que va a supervisar UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="5f418-165">Contiene seis elementos secundarios: **nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="5f418-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="5f418-166">En esta tabla se detalla el tipo de datos respectivo de cada elemento:</span><span class="sxs-lookup"><span data-stu-id="5f418-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f418-167">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f418-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f418-168">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5f418-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f418-169">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5f418-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-170">NombreDeArchivo</span><span class="sxs-lookup"><span data-stu-id="5f418-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-171">FilenameString</span><span class="sxs-lookup"><span data-stu-id="5f418-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-172">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-173">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="5f418-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-174">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="5f418-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-175">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="5f418-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-178">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="5f418-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-180">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-181">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-184">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-185">FileVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-187">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="5f418-188">**Procesos** El tipo de datos processes representa un contenedor para una colección de uno o más elementos de proceso.</span><span class="sxs-lookup"><span data-stu-id="5f418-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="5f418-189">Se admiten dos elementos secundarios en el tipo de secuencia procesos: **proceso** y **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="5f418-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="5f418-190">Proceso es un elemento de tipo proceso y ShellProcess es de tipo de datos vacío.</span><span class="sxs-lookup"><span data-stu-id="5f418-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="5f418-191">Debe identificarse al menos un elemento en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5f418-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="5f418-192">**Ruta de acceso** La ruta de acceso la utiliza RegistrySetting y FileSetting para hacer referencia al registro y a las rutas de acceso de archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="5f418-193">Este elemento admite dos atributos opcionales: **recursivo** y **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="5f418-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="5f418-194">Ambos valores se establecen en default = "false".</span><span class="sxs-lookup"><span data-stu-id="5f418-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="5f418-195">Recursivo indica que la ruta de acceso y todas las subcarpetas están incluidas para la configuración del archivo o que todas las claves del registro secundarias se incluyen para la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="5f418-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="5f418-196">En ambos casos, todos los elementos del nivel actual se incluyen en los datos capturados.</span><span class="sxs-lookup"><span data-stu-id="5f418-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="5f418-197">En el caso de un objeto FileSettings, todos los archivos de la carpeta especificada se incluyen en los datos capturados por UE-V, pero no se incluyen las carpetas.</span><span class="sxs-lookup"><span data-stu-id="5f418-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="5f418-198">Para las rutas de registro, se capturan todos los valores de la ruta de acceso actual, pero no se capturan las claves de registro secundarias.</span><span class="sxs-lookup"><span data-stu-id="5f418-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="5f418-199">En ambos casos, debe tenerse cuidado para evitar capturar grandes conjuntos de datos o un gran número de elementos.</span><span class="sxs-lookup"><span data-stu-id="5f418-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="5f418-200">El atributo DeleteIfNotFound quita la configuración de los datos de la ruta de almacenamiento de configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="5f418-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="5f418-201">Esto puede ser conveniente en los casos en que la eliminación de esta configuración del paquete guardará una gran cantidad de espacio en disco en el servidor de archivos de la ruta de almacenamiento configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="5f418-202">**FileMask** FileMask especifica solo algunos tipos de archivo para la carpeta definida por la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5f418-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="5f418-203">Por ejemplo, Path puede ser `C:\users\username\files` y FileMask podría ser `*.txt` incluir solo archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="5f418-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="5f418-204">**RegistrySetting** RegistrySetting representa un contenedor de valores y claves de registro, así como el comportamiento deseado asociado en la parte de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="5f418-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="5f418-205">En este tipo se definen cuatro elementos secundarios: **path**, **Name**, **Exclude**y una secuencia de los valores **path** y **Name**.</span><span class="sxs-lookup"><span data-stu-id="5f418-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="5f418-206">**FileSetting** FileSetting contiene parámetros asociados con rutas de archivos y archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="5f418-207">Se definen cuatro elementos secundarios: **raíz**, **ruta**, **FileMask**y **excluir**.</span><span class="sxs-lookup"><span data-stu-id="5f418-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="5f418-208">La raíz es obligatoria y las demás son opcionales.</span><span class="sxs-lookup"><span data-stu-id="5f418-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="5f418-209">**Configuración** Configuración es un contenedor de todas las opciones de configuración que se aplican a una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="5f418-210">Contiene instancias de las configuraciones Registry, File, SystemParameter y CustomAction descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5f418-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="5f418-211">Además, también puede contener los siguientes elementos secundarios con comportamientos descritos:</span><span class="sxs-lookup"><span data-stu-id="5f418-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f418-212">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f418-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f418-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-214">Asincrónico</span><span class="sxs-lookup"><span data-stu-id="5f418-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-215">Los paquetes de configuración asincrónica se aplican sin bloquear el inicio de la aplicación para que se inicie la aplicación mientras se sigue aplicando la configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="5f418-216">Esto es útil para las opciones de configuración que se pueden aplicar de forma asincrónica, como las que se aplican <code>get/set</code> a través de una API, como SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="5f418-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="5f418-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-218">De forma predeterminada, UE-V solo guarda la configuración de una aplicación cuando se cierra la última instancia de una aplicación que usa la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="5f418-219">Cuando este elemento se establece en ' false ', UE-V exporta la configuración incluso si se están ejecutando otras instancias de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="5f418-220">Plantillas adaptadas: aquellas que incluyen una sección de elementos comunes, que se envían con UE-V, usan este indicador para permitir que la configuración compartida se exporte siempre al cerrarse de la aplicación, evitando la configuración específica de la aplicación para que no se exporte hasta que se cierre la última instancia.</span><span class="sxs-lookup"><span data-stu-id="5f418-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="5f418-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-222">(introducido en 2,1)</span><span class="sxs-lookup"><span data-stu-id="5f418-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="5f418-223">Este parámetro fuerza la aplicación de un paquete de configuración importado aunque no existan diferencias entre el paquete y el estado actual de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="5f418-224">Este parámetro debe usarse solo en casos especiales, ya que puede ralentizar la importación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="5f418-225">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="5f418-225">Name Element</span></span>

**<span data-ttu-id="5f418-226">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-226">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-227">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-227">Type: String</span></span>**

<span data-ttu-id="5f418-228">Name especifica un nombre único para la plantilla de ubicación Settings.</span><span class="sxs-lookup"><span data-stu-id="5f418-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-229">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-230">En general, Evite hacer referencia a la información de versión, ya que puede ser objeto del elemento ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="5f418-231">Por ejemplo, especifique `<Name>My Application</Name>` en lugar de `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="5f418-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="5f418-232">**Nota:**  UE-V no hace referencia a DTD externas, por lo que no es posible usar entidades con nombre en una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="5f418-233">Por ejemplo, no use &reg; el signo de marca comercial registrada®.</span><span class="sxs-lookup"><span data-stu-id="5f418-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="5f418-234">En su lugar, use referencias numeradas canónicas para incluir estos tipos de caracteres especiales, por ejemplo, & \ #174 para el carácter®.</span><span class="sxs-lookup"><span data-stu-id="5f418-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="5f418-235">Esta regla se aplica a todos los valores de cadena de este documento.</span><span class="sxs-lookup"><span data-stu-id="5f418-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="5f418-236">Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obtener una lista completa de las entidades de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f418-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="5f418-237">Los documentos con codificación UTF-8 pueden incluir directamente los caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="5f418-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="5f418-238">Al guardar las plantillas mediante el generador de UE-V, se convierten las entidades de caracteres en representaciones Unicode automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="5f418-239">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="5f418-239">ID Element</span></span>

**<span data-ttu-id="5f418-240">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-240">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-241">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-241">Type: String</span></span>**

<span data-ttu-id="5f418-242">ID rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-243">Esta etiqueta se convierte en el identificador principal que el agente de UE-V usa para hacer referencia a la plantilla en tiempo de ejecución (por ejemplo, consulte la salida de los cmdlets de PowerShell Get-UevTemplate y Get-UevTemplateProgram).</span><span class="sxs-lookup"><span data-stu-id="5f418-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="5f418-244">Por Convención, esta etiqueta no debe contener espacios, lo que simplifica el scripting.</span><span class="sxs-lookup"><span data-stu-id="5f418-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="5f418-245">Los números de versión de las aplicaciones deben especificarse en este elemento para permitir la identificación sencilla de la plantilla, como `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="5f418-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="5f418-246">Elemento version</span><span class="sxs-lookup"><span data-stu-id="5f418-246">Version Element</span></span>

**<span data-ttu-id="5f418-247">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-247">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-248">Tipo: entero</span><span class="sxs-lookup"><span data-stu-id="5f418-248">Type: Integer</span></span>**

**<span data-ttu-id="5f418-249">Valor mínimo: 0</span><span class="sxs-lookup"><span data-stu-id="5f418-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="5f418-250">Valor máximo: 2147483647</span><span class="sxs-lookup"><span data-stu-id="5f418-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="5f418-251">Versión identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios.</span><span class="sxs-lookup"><span data-stu-id="5f418-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="5f418-252">El generador de UE-V incrementa automáticamente este número en uno cada vez que se guarda la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="5f418-253">Observe que este campo debe ser un número entero entero; los valores fraccionarios, como, por ejemplo, `<Version>2.5</Version>` no están permitidos.</span><span class="sxs-lookup"><span data-stu-id="5f418-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="5f418-254">**Sugerencia:** Puede guardar las notas sobre los cambios de versión mediante etiquetas `<!-- -->` de comentario XML, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="5f418-255">**Importante**  Se consulta este valor para determinar si se debe aplicar una nueva versión de una plantilla a una plantilla existente en estos casos:</span><span class="sxs-lookup"><span data-stu-id="5f418-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="5f418-256">Cuando se ejecuta la tarea de actualización automática de la plantilla programada</span><span class="sxs-lookup"><span data-stu-id="5f418-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="5f418-257">Cuando se ejecuta el cmdlet Update-UevTemplate de PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f418-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="5f418-258">Cuando se llama al método Update microsoft\\uev: SettingsLocationTemplate mediante WMI</span><span class="sxs-lookup"><span data-stu-id="5f418-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="5f418-259">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="5f418-259">Author Element</span></span>

**<span data-ttu-id="5f418-260">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-260">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-261">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-261">Type: String</span></span>**

<span data-ttu-id="5f418-262">Autor identifica al creador de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="5f418-263">Se admiten dos elementos secundarios opcionales: **nombre** y **correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="5f418-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="5f418-264">Ambos atributos son opcionales, pero si se especifica el elemento secundario email, debe ir acompañado del elemento Name.</span><span class="sxs-lookup"><span data-stu-id="5f418-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="5f418-265">Autor hace referencia al nombre completo del contacto para la plantilla de ubicación de configuración y el correo electrónico debe hacer referencia a una dirección de correo electrónico del autor.</span><span class="sxs-lookup"><span data-stu-id="5f418-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="5f418-266">Le recomendamos que incluya esta información en las plantillas publicadas públicamente, por ejemplo, en la [Galería de plantillas de UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="5f418-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="5f418-267">Procesos y elemento de proceso</span><span class="sxs-lookup"><span data-stu-id="5f418-267">Processes and Process Element</span></span>

**<span data-ttu-id="5f418-268">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-268">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-269">Type: Element</span><span class="sxs-lookup"><span data-stu-id="5f418-269">Type: Element</span></span>**

<span data-ttu-id="5f418-270">Procesos contiene al menos un `<Process>` elemento, que a su vez contiene los siguientes elementos secundarios **: nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="5f418-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="5f418-271">El elemento secundario FILENAME es obligatorio y el resto es opcional.</span><span class="sxs-lookup"><span data-stu-id="5f418-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="5f418-272">Un elemento completamente rellenado contiene etiquetas similares a este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="5f418-273">NombreDeArchivo</span><span class="sxs-lookup"><span data-stu-id="5f418-273">Filename</span></span>

**<span data-ttu-id="5f418-274">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-274">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-275">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-275">Type: String</span></span>**

<span data-ttu-id="5f418-276">Nombre de archivo se refiere al nombre de archivo real del ejecutable tal como aparece en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="5f418-277">Este elemento especifica el criterio principal que UE-V usa para evaluar si una plantilla se aplica a un proceso o no.</span><span class="sxs-lookup"><span data-stu-id="5f418-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="5f418-278">Este elemento debe especificarse en el XML de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="5f418-279">Los nombres de archivo válidos no deben coincidir con la expresión regular \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, es decir, no pueden contener caracteres de barra invertida, asterisco o signo de interrogación caracteres comodín, el carácter de barra vertical, el signo mayor que o menor que, o el signo de dos puntos (\ \?</span><span class="sxs-lookup"><span data-stu-id="5f418-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="5f418-280">\* | &lt; &gt; /o: caracteres.).</span><span class="sxs-lookup"><span data-stu-id="5f418-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="5f418-281">**Sugerencia:** Para probar una cadena con este regex, use una ventana de comandos de PowerShell y sustituya el nombre de su archivo ejecutable por **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="5f418-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="5f418-282">Un valor de **true** indica que la cadena contiene caracteres ilegales.</span><span class="sxs-lookup"><span data-stu-id="5f418-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="5f418-283">A continuación se muestran algunos ejemplos de valores ilegales:</span><span class="sxs-lookup"><span data-stu-id="5f418-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="5f418-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="5f418-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="5f418-285">Programa \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="5f418-285">Program\*.exe</span></span>

-   <span data-ttu-id="5f418-286">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="5f418-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="5f418-287">Programa &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="5f418-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="5f418-288">**Nota:**  El generador de UE-V codifica los caracteres mayor que y menor que, como &gt; y &lt; respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="5f418-289">En raras ocasiones, el valor del nombre de archivo no incluirá necesariamente la extensión. exe, pero debe especificarse como parte del valor.</span><span class="sxs-lookup"><span data-stu-id="5f418-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="5f418-290">Por ejemplo, `<Filename>MyApplictication.exe</Filename>` debe especificarse en lugar de `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="5f418-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="5f418-291">En el segundo ejemplo no se aplica la plantilla al proceso si el nombre real del archivo ejecutable es "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="5f418-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="5f418-292">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="5f418-292">Architecture</span></span>

**<span data-ttu-id="5f418-293">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-293">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-294">Tipo: arquitectura (cadena)</span><span class="sxs-lookup"><span data-stu-id="5f418-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="5f418-295">Arquitectura se refiere a la arquitectura de procesador para la que se compiló el ejecutable de destino.</span><span class="sxs-lookup"><span data-stu-id="5f418-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="5f418-296">Los valores válidos son Win32 para las aplicaciones de 32 bits o Win64 para aplicaciones de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5f418-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="5f418-297">Si está presente, esta etiqueta limita la aplicabilidad de la plantilla de ubicación de configuración a una arquitectura de aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="5f418-298">Para obtener un ejemplo de esto, compare la experiencia de usuario de%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml y los archivos de MicrosoftOffice2010Win64.xml incluidos en UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="5f418-299">Esto es útil cuando las rutas relativas cambian entre diferentes versiones de un archivo ejecutable o si se han agregado o quitado parámetros de configuración al pasar de una arquitectura de procesador a otra.</span><span class="sxs-lookup"><span data-stu-id="5f418-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="5f418-300">Si este elemento está ausente, la plantilla de ubicación de configuración omite la arquitectura del proceso y se aplica a los procesos de 32 y 64 bits si se aplican el nombre de archivo y otros atributos.</span><span class="sxs-lookup"><span data-stu-id="5f418-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="5f418-301">**Nota:**  UE-V no admite procesadores ARM en esta versión.</span><span class="sxs-lookup"><span data-stu-id="5f418-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="5f418-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="5f418-302">ProductName</span></span>

**<span data-ttu-id="5f418-303">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-303">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-304">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-304">Type: String</span></span>**

<span data-ttu-id="5f418-305">ProductName es un elemento opcional que se usa para identificar un producto con fines administrativos o de generación de informes.</span><span class="sxs-lookup"><span data-stu-id="5f418-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="5f418-306">ProductName difiere de FILENAME en el que no hay restricciones de expresiones regulares en su valor.</span><span class="sxs-lookup"><span data-stu-id="5f418-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="5f418-307">Esto permite comprender más fácilmente las descripciones de un proceso donde el nombre ejecutable puede no ser obvio.</span><span class="sxs-lookup"><span data-stu-id="5f418-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="5f418-308">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="5f418-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="5f418-309">FileDescription</span></span>

**<span data-ttu-id="5f418-310">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-310">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-311">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-311">Type: String</span></span>**

<span data-ttu-id="5f418-312">FileDescription es una etiqueta opcional que permite una descripción administrativa del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="5f418-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="5f418-313">Este es un campo de texto sin formato y puede ser útil para distinguir varios ejecutables dentro de un paquete de software donde es necesario identificar la función del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="5f418-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="5f418-314">Por ejemplo, en una aplicación adecuada podría ser útil proporcionar avisos sobre la función de dos ejecutables (MyApplication.exe y MyApplicationHelper.exe), tal como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="5f418-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="5f418-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-315">ProductVersion</span></span>

**<span data-ttu-id="5f418-316">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-316">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-317">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-317">Type: String</span></span>**

<span data-ttu-id="5f418-318">ProductVersion hace referencia a las versiones principales y secundarias de los productos de un archivo, así como a un nivel de compilación y revisión.</span><span class="sxs-lookup"><span data-stu-id="5f418-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="5f418-319">ProductVersion es un elemento opcional, pero, si se especifica, debe contener al menos el elemento secundario principal.</span><span class="sxs-lookup"><span data-stu-id="5f418-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="5f418-320">El valor debe expresar un rango con el formato mínimo = "X" máximo = "Y" donde X e y son enteros.</span><span class="sxs-lookup"><span data-stu-id="5f418-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="5f418-321">Los valores mínimos y máximos pueden ser idénticos.</span><span class="sxs-lookup"><span data-stu-id="5f418-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="5f418-322">Es posible que los elementos de versión de archivo y producto no estén especificados.</span><span class="sxs-lookup"><span data-stu-id="5f418-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="5f418-323">De este modo, se convierte la plantilla "independiente de la versión", lo que significa que la plantilla se aplicará a todas las versiones del archivo ejecutable especificado.</span><span class="sxs-lookup"><span data-stu-id="5f418-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="5f418-324">Ejemplo 1:</span><span class="sxs-lookup"><span data-stu-id="5f418-324">Example 1:</span></span>**

<span data-ttu-id="5f418-325">Versión del producto: 1,0 especificada en el generador de UE-V genera el siguiente XML:</span><span class="sxs-lookup"><span data-stu-id="5f418-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="5f418-326">Ejemplo 2:</span><span class="sxs-lookup"><span data-stu-id="5f418-326">Example 2:</span></span>**

<span data-ttu-id="5f418-327">Versión del archivo: 5.0.2.1000 especificada en el generador de UE-V genera el siguiente XML:</span><span class="sxs-lookup"><span data-stu-id="5f418-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="5f418-328">Ejemplo incorrecto 1: intervalo incompleto:</span><span class="sxs-lookup"><span data-stu-id="5f418-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="5f418-329">Solo está presente el atributo Minimum.</span><span class="sxs-lookup"><span data-stu-id="5f418-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="5f418-330">El valor máximo debe incluirse también en un rango.</span><span class="sxs-lookup"><span data-stu-id="5f418-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="5f418-331">Ejemplo incorrecto 2: se especificó una menor sin el elemento principal:</span><span class="sxs-lookup"><span data-stu-id="5f418-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="5f418-332">Solo está presente el elemento menor.</span><span class="sxs-lookup"><span data-stu-id="5f418-332">Only the Minor element is present.</span></span> <span data-ttu-id="5f418-333">También se debe incluir una mayor importancia.</span><span class="sxs-lookup"><span data-stu-id="5f418-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="5f418-334">FileVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-334">FileVersion</span></span>

**<span data-ttu-id="5f418-335">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-335">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-336">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-336">Type: String</span></span>**

<span data-ttu-id="5f418-337">FileVersion distingue entre la versión de lanzamiento de una aplicación publicada y los detalles internos de la compilación de un ejecutable de componente.</span><span class="sxs-lookup"><span data-stu-id="5f418-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="5f418-338">Para la mayoría de las aplicaciones comerciales, estos números son idénticos.</span><span class="sxs-lookup"><span data-stu-id="5f418-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="5f418-339">Cuando varían, la versión de producto de un archivo indica la identificación de la versión genérica de un archivo, mientras que la versión de archivo indica una compilación específica de un archivo (como en el caso de una revisión o una actualización).</span><span class="sxs-lookup"><span data-stu-id="5f418-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="5f418-340">Esto identifica de forma única los archivos sin romper la lógica de detección.</span><span class="sxs-lookup"><span data-stu-id="5f418-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="5f418-341">Para determinar la versión del producto y la versión de archivo de un ejecutable en particular, haga clic con el botón derecho en el archivo en el explorador de Windows, seleccione Propiedades y, a continuación, haga clic en la pestaña detalles.</span><span class="sxs-lookup"><span data-stu-id="5f418-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="5f418-342">Incluir un elemento FileVersion para una aplicación permite una lógica de detección de ajuste más granular, pero no es necesario para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f418-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="5f418-343">La configuración del elemento de ProductVersion se comprueba en primer lugar y, a continuación, se comprueba la opción FileVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="5f418-344">Se aplicará la configuración más restrictiva.</span><span class="sxs-lookup"><span data-stu-id="5f418-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="5f418-345">Los elementos secundarios y las reglas de sintaxis de la FileVersion son idénticos a los de ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="5f418-346">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="5f418-346">Application Element</span></span>

<span data-ttu-id="5f418-347">Aplicación es un contenedor de la configuración que se aplica a una aplicación en particular.</span><span class="sxs-lookup"><span data-stu-id="5f418-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="5f418-348">Es una colección de los siguientes campos o tipos.</span><span class="sxs-lookup"><span data-stu-id="5f418-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f418-349">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="5f418-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f418-350">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-351">Name</span><span class="sxs-lookup"><span data-stu-id="5f418-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-352">Especifica un nombre único para la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-353">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-354">Para obtener más información, vea <a href="#name21" data-raw-source="[Name](#name21)"> nombre </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-355">ID</span><span class="sxs-lookup"><span data-stu-id="5f418-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-356">Rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-357">Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f418-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="5f418-358">Para obtener más información, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-359">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-360">Una descripción opcional de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-361">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="5f418-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-362">Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f418-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-364">Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-365">Versión</span><span class="sxs-lookup"><span data-stu-id="5f418-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-366">Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios.</span><span class="sxs-lookup"><span data-stu-id="5f418-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="5f418-367">Para obtener más información, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versión </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="5f418-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-369">Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no.</span><span class="sxs-lookup"><span data-stu-id="5f418-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="5f418-370">Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="5f418-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-372">De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365.</span><span class="sxs-lookup"><span data-stu-id="5f418-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="5f418-373">Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-374">FixedProfile (introducido en 2,1)</span><span class="sxs-lookup"><span data-stu-id="5f418-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-375">Especifica que esta plantilla solo se puede asociar con el perfil especificado dentro de este elemento y que no se puede cambiar mediante WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f418-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-376">Procesos</span><span class="sxs-lookup"><span data-stu-id="5f418-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-377">Un contenedor para una colección de uno o varios elementos de proceso.</span><span class="sxs-lookup"><span data-stu-id="5f418-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="5f418-378">Para obtener más información, consulte <a href="#processes21" data-raw-source="[Processes](#processes21)"> procesos </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-379">Configuración</span><span class="sxs-lookup"><span data-stu-id="5f418-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-380">Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="5f418-381">Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f418-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="5f418-382">Para obtener más información, vea <strong> configuración </strong> de los <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="5f418-383">Elemento común</span><span class="sxs-lookup"><span data-stu-id="5f418-383">Common Element</span></span>

<span data-ttu-id="5f418-384">Common es similar a un elemento de la aplicación, pero siempre está asociado con dos o más elementos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="5f418-385">La sección común representa el conjunto de opciones de configuración que se comparten entre las instancias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="5f418-386">Es una colección de los siguientes campos o tipos.</span><span class="sxs-lookup"><span data-stu-id="5f418-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f418-387">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="5f418-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f418-388">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-389">Name</span><span class="sxs-lookup"><span data-stu-id="5f418-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-390">Especifica un nombre único para la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-391">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-392">Para obtener más información, vea <a href="#name21" data-raw-source="[Name](#name21)"> nombre </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-393">ID</span><span class="sxs-lookup"><span data-stu-id="5f418-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-394">Rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-395">Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f418-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="5f418-396">Para obtener más información, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-397">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-398">Una descripción opcional de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-399">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="5f418-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-400">Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f418-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-402">Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-403">Versión</span><span class="sxs-lookup"><span data-stu-id="5f418-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-404">Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios.</span><span class="sxs-lookup"><span data-stu-id="5f418-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="5f418-405">Para obtener más información, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versión </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="5f418-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-407">Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no.</span><span class="sxs-lookup"><span data-stu-id="5f418-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="5f418-408">Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="5f418-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-410">De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365.</span><span class="sxs-lookup"><span data-stu-id="5f418-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="5f418-411">Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-412">FixedProfile (introducido en 2,1)</span><span class="sxs-lookup"><span data-stu-id="5f418-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-413">Especifica que esta plantilla solo se puede asociar con el perfil especificado dentro de este elemento y que no se puede cambiar mediante WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f418-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-414">Configuración</span><span class="sxs-lookup"><span data-stu-id="5f418-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-415">Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="5f418-416">Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f418-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="5f418-417">Para obtener más información, vea <strong> configuración </strong> de los <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="5f418-418">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="5f418-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="5f418-419">Este elemento define la configuración para una sola aplicación o un conjunto de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f418-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f418-420">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="5f418-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5f418-421">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-422">Name</span><span class="sxs-lookup"><span data-stu-id="5f418-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-423">Especifica un nombre único para la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-424">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-425">Para obtener más información, vea <a href="#name21" data-raw-source="[Name](#name21)"> nombre </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-426">ID</span><span class="sxs-lookup"><span data-stu-id="5f418-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-427">Rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-428">Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f418-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="5f418-429">Para obtener más información, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-430">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-431">Una descripción opcional de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-432">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="5f418-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-433">Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f418-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-435">Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="5f418-436">Apéndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="5f418-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="5f418-437">Este es el archivo SettingsLocationTemplate. xsd que muestra sus elementos, elementos secundarios, atributos y parámetros:</span><span class="sxs-lookup"><span data-stu-id="5f418-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="5f418-438">Referencia de esquema de la plantilla de aplicación UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="5f418-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="5f418-439">En esta sección se describe la estructura XML de la plantilla de ubicación de configuración de UE-V 2,0 y se proporcionan instrucciones para editar este archivo.</span><span class="sxs-lookup"><span data-stu-id="5f418-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="5f418-440">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5f418-440">In This Section</span></span>

-   [<span data-ttu-id="5f418-441">Atributo de declaración y de codificación XML</span><span class="sxs-lookup"><span data-stu-id="5f418-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="5f418-442">Espacio de nombres y elemento raíz</span><span class="sxs-lookup"><span data-stu-id="5f418-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="5f418-443">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="5f418-443">Data types</span></span>](#data)

-   [<span data-ttu-id="5f418-444">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="5f418-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="5f418-445">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="5f418-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="5f418-446">Elemento version</span><span class="sxs-lookup"><span data-stu-id="5f418-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="5f418-447">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="5f418-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="5f418-448">Procesos y elemento de proceso</span><span class="sxs-lookup"><span data-stu-id="5f418-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="5f418-449">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="5f418-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="5f418-450">Elemento común</span><span class="sxs-lookup"><span data-stu-id="5f418-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="5f418-451">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="5f418-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="5f418-452">Apéndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="5f418-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="5f418-453">Atributo de declaración y de codificación XML</span><span class="sxs-lookup"><span data-stu-id="5f418-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="5f418-454">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-454">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-455">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-455">Type: String</span></span>**

<span data-ttu-id="5f418-456">La declaración XML debe especificar el atributo de versión XML 1,0 ( &lt; ? XML version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="5f418-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="5f418-457">Las plantillas de ubicación de configuración creadas por el generador de UE-V se guardan en la codificación UTF-8, aunque la codificación no se especifica explícitamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="5f418-458">Le recomendamos que incluya el atributo de codificación = "UTF-8" en este elemento como procedimiento recomendado.</span><span class="sxs-lookup"><span data-stu-id="5f418-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="5f418-459">Todas las plantillas incluidas con el producto especifican también esta etiqueta (vea los documentos de la experiencia del usuario de%ProgramFiles%\\Microsoft Virtualization\\Templates por referencia).</span><span class="sxs-lookup"><span data-stu-id="5f418-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="5f418-460">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="5f418-461">Espacio de nombres y elemento raíz</span><span class="sxs-lookup"><span data-stu-id="5f418-461">Namespace and Root Element</span></span>

**<span data-ttu-id="5f418-462">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-462">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-463">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-463">Type: String</span></span>**

<span data-ttu-id="5f418-464">UE-V usa el https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espacio de nombres para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f418-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="5f418-465">SettingsLocationTemplate es el elemento raíz y contiene todos los demás elementos.</span><span class="sxs-lookup"><span data-stu-id="5f418-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="5f418-466">SettingsLocationTemplate de referencia en todas las plantillas que usan esta etiqueta:</span><span class="sxs-lookup"><span data-stu-id="5f418-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="5f418-467">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="5f418-467">Data types</span></span>

<span data-ttu-id="5f418-468">Estos son los tipos de datos para el esquema de la plantilla de aplicación UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="5f418-469">**GUID** GUID describe una expresión regular de identificador global único estándar con el formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="5f418-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="5f418-470">Se usa en el elemento Filesetting\\Root\\KnownFolder para comprobar el formato de las carpetas conocidas.</span><span class="sxs-lookup"><span data-stu-id="5f418-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="5f418-471">**FilenameString** FilenameString se refiere al nombre de archivo de un proceso que se va a supervisar.</span><span class="sxs-lookup"><span data-stu-id="5f418-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="5f418-472">Sus valores están restringidos por la función regex \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, (es decir, no pueden contener caracteres de barra invertida o asterisco o signo de interrogación; caracteres comodín, el carácter de canalización, el signo mayor que o menor que, la barra diagonal o los caracteres de dos puntos).</span><span class="sxs-lookup"><span data-stu-id="5f418-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="5f418-473">**IDString** IDString se refiere al valor de identificador de elementos de la aplicación, SettingsLocationTemplate y elementos comunes (se usa para describir conjuntos de aplicaciones que comparten una configuración común).</span><span class="sxs-lookup"><span data-stu-id="5f418-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="5f418-474">Está restringido por el mismo Regex que FilenameString (\ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="5f418-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="5f418-475">**TemplateVersion** TemplateVersion es un valor entero que se usa para describir la revisión de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="5f418-476">Su valor puede oscilar entre 0 y 2147483647.</span><span class="sxs-lookup"><span data-stu-id="5f418-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="5f418-477">**Vacío** Vacío hace referencia a un valor null.</span><span class="sxs-lookup"><span data-stu-id="5f418-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="5f418-478">Se usa en Process\\ShellProcess para indicar que no hay ningún proceso para supervisar.</span><span class="sxs-lookup"><span data-stu-id="5f418-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="5f418-479">Este valor no debe usarse en ninguna plantilla de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="5f418-480">**Autor** El tipo de datos autor es un tipo complejo que identifica al autor de una plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="5f418-481">Contiene dos elementos secundarios: **Name** y **email**.</span><span class="sxs-lookup"><span data-stu-id="5f418-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="5f418-482">En el tipo de datos autor, el elemento nombre es obligatorio mientras que el elemento de correo electrónico es opcional.</span><span class="sxs-lookup"><span data-stu-id="5f418-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="5f418-483">Este tipo se describe más detalladamente en el elemento SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="5f418-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="5f418-484">**Intervalo** Range define una clase Integer formada por dos elementos secundarios: **Minimum** y **Maximum**.</span><span class="sxs-lookup"><span data-stu-id="5f418-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="5f418-485">Este tipo de datos se implementa en el tipo de datos ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="5f418-486">Si se especifica, se deben incluir los valores mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="5f418-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="5f418-487">**ProcessVersion** ProcessVersion define un tipo con cuatro elementos secundarios: **principal**, **secundario**, de **compilación**y de **revisión**.</span><span class="sxs-lookup"><span data-stu-id="5f418-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="5f418-488">Este tipo de datos es utilizado por el elemento Process para rellenar sus valores ProductVersion y FileVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="5f418-489">Los datos de este tipo son un valor de rango.</span><span class="sxs-lookup"><span data-stu-id="5f418-489">The data for this type is a Range value.</span></span> <span data-ttu-id="5f418-490">El elemento secundario principal es obligatorio y el resto es opcional.</span><span class="sxs-lookup"><span data-stu-id="5f418-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="5f418-491">**Arquitectura** La arquitectura enumera dos valores posibles: **Win32** y **Win64**.</span><span class="sxs-lookup"><span data-stu-id="5f418-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="5f418-492">Estos valores se usan para especificar la arquitectura de los procesos.</span><span class="sxs-lookup"><span data-stu-id="5f418-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="5f418-493">**Proceso** El tipo de datos proceso es un contenedor que se usa para describir los procesos que va a supervisar UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="5f418-494">Contiene seis elementos secundarios: **nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="5f418-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="5f418-495">En esta tabla se detalla el tipo de datos respectivo de cada elemento:</span><span class="sxs-lookup"><span data-stu-id="5f418-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f418-496">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f418-496">Element</span></span></th>
<th align="left"><span data-ttu-id="5f418-497">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5f418-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="5f418-498">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5f418-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-499">NombreDeArchivo</span><span class="sxs-lookup"><span data-stu-id="5f418-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-500">FilenameString</span><span class="sxs-lookup"><span data-stu-id="5f418-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-501">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-502">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="5f418-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-503">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="5f418-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-504">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="5f418-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-506">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-507">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="5f418-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-509">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-510">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-513">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-514">FileVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-516">Falso</span><span class="sxs-lookup"><span data-stu-id="5f418-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="5f418-517">**Procesos** El tipo de datos processes representa un contenedor para una colección de uno o más elementos de proceso.</span><span class="sxs-lookup"><span data-stu-id="5f418-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="5f418-518">Se admiten dos elementos secundarios en el tipo de secuencia procesos: **proceso** y **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="5f418-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="5f418-519">Proceso es un elemento de tipo proceso y ShellProcess es de tipo de datos vacío.</span><span class="sxs-lookup"><span data-stu-id="5f418-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="5f418-520">Debe identificarse al menos un elemento en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5f418-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="5f418-521">**Ruta de acceso** La ruta de acceso la utiliza RegistrySetting y FileSetting para hacer referencia al registro y a las rutas de acceso de archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="5f418-522">Este elemento admite dos atributos opcionales: **recursivo** y **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="5f418-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="5f418-523">Ambos valores se establecen en default = "false".</span><span class="sxs-lookup"><span data-stu-id="5f418-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="5f418-524">Recursivo indica que la ruta de acceso y todas las subcarpetas están incluidas para la configuración del archivo o que todas las claves del registro secundarias se incluyen para la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="5f418-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="5f418-525">En ambos casos, todos los elementos del nivel actual se incluyen en los datos capturados.</span><span class="sxs-lookup"><span data-stu-id="5f418-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="5f418-526">En el caso de un objeto FileSettings, todos los archivos de la carpeta especificada se incluyen en los datos capturados por UE-V, pero no se incluyen las carpetas.</span><span class="sxs-lookup"><span data-stu-id="5f418-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="5f418-527">Para las rutas de registro, se capturan todos los valores de la ruta de acceso actual, pero no se capturan las claves de registro secundarias.</span><span class="sxs-lookup"><span data-stu-id="5f418-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="5f418-528">En ambos casos, debe tenerse cuidado para evitar capturar grandes conjuntos de datos o un gran número de elementos.</span><span class="sxs-lookup"><span data-stu-id="5f418-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="5f418-529">El atributo DeleteIfNotFound quita la configuración de los datos de la ruta de almacenamiento de configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="5f418-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="5f418-530">Esto puede ser conveniente en los casos en que la eliminación de esta configuración del paquete guardará una gran cantidad de espacio en disco en el servidor de archivos de la ruta de almacenamiento configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="5f418-531">**FileMask** FileMask especifica solo algunos tipos de archivo para la carpeta definida por la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5f418-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="5f418-532">Por ejemplo, Path puede ser `C:\users\username\files` y FileMask podría ser `*.txt` incluir solo archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="5f418-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="5f418-533">**RegistrySetting** RegistrySetting representa un contenedor de valores y claves de registro, así como el comportamiento deseado asociado en la parte de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="5f418-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="5f418-534">En este tipo se definen cuatro elementos secundarios: **path**, **Name**, **Exclude**y una secuencia de los valores **path** y **Name**.</span><span class="sxs-lookup"><span data-stu-id="5f418-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="5f418-535">**FileSetting** FileSetting contiene parámetros asociados con rutas de archivos y archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="5f418-536">Se definen cuatro elementos secundarios: **raíz**, **ruta**, **FileMask**y **excluir**.</span><span class="sxs-lookup"><span data-stu-id="5f418-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="5f418-537">La raíz es obligatoria y las demás son opcionales.</span><span class="sxs-lookup"><span data-stu-id="5f418-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="5f418-538">**Configuración** Configuración es un contenedor de todas las opciones de configuración que se aplican a una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="5f418-539">Contiene instancias de las configuraciones Registry, File, SystemParameter y CustomAction descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5f418-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="5f418-540">Además, también puede contener los siguientes elementos secundarios con comportamientos descritos:</span><span class="sxs-lookup"><span data-stu-id="5f418-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f418-541">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f418-541">Element</span></span></th>
<th align="left"><span data-ttu-id="5f418-542">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-543">Asincrónico</span><span class="sxs-lookup"><span data-stu-id="5f418-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-544">Los paquetes de configuración asincrónica se aplican sin bloquear el inicio de la aplicación para que se inicie la aplicación mientras se sigue aplicando la configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="5f418-545">Esto es útil para las opciones de configuración que se pueden aplicar de forma asincrónica, como las que se aplican <code>get/set</code> a través de una API, como SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="5f418-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="5f418-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-547">De forma predeterminada, UE-V solo guarda la configuración de una aplicación cuando se cierra la última instancia de una aplicación que usa la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="5f418-548">Cuando este elemento se establece en ' false ', UE-V exporta la configuración incluso si se están ejecutando otras instancias de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="5f418-549">Plantillas adaptadas: aquellas que incluyen una sección de elementos comunes, que se envían con UE-V, usan este indicador para permitir que la configuración compartida se exporte siempre al cerrarse de la aplicación, evitando la configuración específica de la aplicación para que no se exporte hasta que se cierre la última instancia.</span><span class="sxs-lookup"><span data-stu-id="5f418-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="5f418-550">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="5f418-550">Name Element</span></span>

**<span data-ttu-id="5f418-551">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-551">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-552">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-552">Type: String</span></span>**

<span data-ttu-id="5f418-553">Name especifica un nombre único para la plantilla de ubicación Settings.</span><span class="sxs-lookup"><span data-stu-id="5f418-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-554">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-555">En general, Evite hacer referencia a la información de versión, ya que puede ser objeto del elemento ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="5f418-556">Por ejemplo, especifique `<Name>My Application</Name>` en lugar de `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="5f418-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="5f418-557">**Nota:**  UE-V no hace referencia a DTD externas, por lo que no es posible usar entidades con nombre en una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="5f418-558">Por ejemplo, no use &reg; el signo de marca comercial registrada®.</span><span class="sxs-lookup"><span data-stu-id="5f418-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="5f418-559">En su lugar, use referencias numeradas canónicas para incluir estos tipos de caracteres especiales, por ejemplo, & \ #174 para el carácter®.</span><span class="sxs-lookup"><span data-stu-id="5f418-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="5f418-560">Esta regla se aplica a todos los valores de cadena de este documento.</span><span class="sxs-lookup"><span data-stu-id="5f418-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="5f418-561">Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obtener una lista completa de las entidades de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f418-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="5f418-562">Los documentos con codificación UTF-8 pueden incluir directamente los caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="5f418-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="5f418-563">Al guardar las plantillas mediante el generador de UE-V, se convierten las entidades de caracteres en representaciones Unicode automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="5f418-564">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="5f418-564">ID Element</span></span>

**<span data-ttu-id="5f418-565">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-565">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-566">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-566">Type: String</span></span>**

<span data-ttu-id="5f418-567">ID rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-568">Esta etiqueta se convierte en el identificador principal que el agente de UE-V usa para hacer referencia a la plantilla en tiempo de ejecución (por ejemplo, consulte la salida de los cmdlets de PowerShell Get-UevTemplate y Get-UevTemplateProgram).</span><span class="sxs-lookup"><span data-stu-id="5f418-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="5f418-569">Por Convención, esta etiqueta no debe contener espacios, lo que simplifica el scripting.</span><span class="sxs-lookup"><span data-stu-id="5f418-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="5f418-570">Los números de versión de las aplicaciones deben especificarse en este elemento para permitir la identificación sencilla de la plantilla, como `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="5f418-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="5f418-571">Elemento version</span><span class="sxs-lookup"><span data-stu-id="5f418-571">Version Element</span></span>

**<span data-ttu-id="5f418-572">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-572">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-573">Tipo: entero</span><span class="sxs-lookup"><span data-stu-id="5f418-573">Type: Integer</span></span>**

**<span data-ttu-id="5f418-574">Valor mínimo: 0</span><span class="sxs-lookup"><span data-stu-id="5f418-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="5f418-575">Valor máximo: 2147483647</span><span class="sxs-lookup"><span data-stu-id="5f418-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="5f418-576">Versión identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios.</span><span class="sxs-lookup"><span data-stu-id="5f418-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="5f418-577">El generador de UE-V incrementa automáticamente este número en uno cada vez que se guarda la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="5f418-578">Observe que este campo debe ser un número entero entero; los valores fraccionarios, como, por ejemplo, `<Version>2.5</Version>` no están permitidos.</span><span class="sxs-lookup"><span data-stu-id="5f418-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="5f418-579">**Sugerencia:** Puede guardar las notas sobre los cambios de versión mediante etiquetas `<!-- -->` de comentario XML, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="5f418-580">**Importante**  Se consulta este valor para determinar si se debe aplicar una nueva versión de una plantilla a una plantilla existente en estos casos:</span><span class="sxs-lookup"><span data-stu-id="5f418-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="5f418-581">Cuando se ejecuta la tarea de actualización automática de la plantilla programada</span><span class="sxs-lookup"><span data-stu-id="5f418-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="5f418-582">Cuando se ejecuta el cmdlet Update-UevTemplate de PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f418-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="5f418-583">Cuando se llama al método Update microsoft\\uev: SettingsLocationTemplate mediante WMI</span><span class="sxs-lookup"><span data-stu-id="5f418-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="5f418-584">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="5f418-584">Author Element</span></span>

**<span data-ttu-id="5f418-585">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-585">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-586">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-586">Type: String</span></span>**

<span data-ttu-id="5f418-587">Autor identifica al creador de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="5f418-588">Se admiten dos elementos secundarios opcionales: **nombre** y **correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="5f418-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="5f418-589">Ambos atributos son opcionales, pero si se especifica el elemento secundario email, debe ir acompañado del elemento Name.</span><span class="sxs-lookup"><span data-stu-id="5f418-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="5f418-590">Autor hace referencia al nombre completo del contacto para la plantilla de ubicación de configuración y el correo electrónico debe hacer referencia a una dirección de correo electrónico del autor.</span><span class="sxs-lookup"><span data-stu-id="5f418-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="5f418-591">Le recomendamos que incluya esta información en las plantillas publicadas públicamente, por ejemplo, en la [Galería de plantillas de UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="5f418-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="5f418-592">Procesos y elemento de proceso</span><span class="sxs-lookup"><span data-stu-id="5f418-592">Processes and Process Element</span></span>

**<span data-ttu-id="5f418-593">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-593">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-594">Type: Element</span><span class="sxs-lookup"><span data-stu-id="5f418-594">Type: Element</span></span>**

<span data-ttu-id="5f418-595">Procesos contiene al menos un `<Process>` elemento, que a su vez contiene los siguientes elementos secundarios **: nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="5f418-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="5f418-596">El elemento secundario FILENAME es obligatorio y el resto es opcional.</span><span class="sxs-lookup"><span data-stu-id="5f418-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="5f418-597">Un elemento completamente rellenado contiene etiquetas similares a este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="5f418-598">NombreDeArchivo</span><span class="sxs-lookup"><span data-stu-id="5f418-598">Filename</span></span>

**<span data-ttu-id="5f418-599">Obligatorio: verdadero</span><span class="sxs-lookup"><span data-stu-id="5f418-599">Mandatory: True</span></span>**

**<span data-ttu-id="5f418-600">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-600">Type: String</span></span>**

<span data-ttu-id="5f418-601">Nombre de archivo se refiere al nombre de archivo real del ejecutable tal como aparece en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5f418-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="5f418-602">Este elemento especifica el criterio principal que UE-V usa para evaluar si una plantilla se aplica a un proceso o no.</span><span class="sxs-lookup"><span data-stu-id="5f418-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="5f418-603">Este elemento debe especificarse en el XML de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="5f418-604">Los nombres de archivo válidos no deben coincidir con la expresión regular \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, es decir, no pueden contener caracteres de barra invertida, asterisco o signo de interrogación caracteres comodín, el carácter de barra vertical, el signo mayor que o menor que, o el signo de dos puntos (\ \?</span><span class="sxs-lookup"><span data-stu-id="5f418-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="5f418-605">\* | &lt; &gt; /o: caracteres.).</span><span class="sxs-lookup"><span data-stu-id="5f418-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="5f418-606">**Sugerencia:** Para probar una cadena con este regex, use una ventana de comandos de PowerShell y sustituya el nombre de su archivo ejecutable por **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="5f418-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="5f418-607">Un valor de **true** indica que la cadena contiene caracteres ilegales.</span><span class="sxs-lookup"><span data-stu-id="5f418-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="5f418-608">A continuación se muestran algunos ejemplos de valores ilegales:</span><span class="sxs-lookup"><span data-stu-id="5f418-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="5f418-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="5f418-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="5f418-610">Programa \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="5f418-610">Program\*.exe</span></span>

-   <span data-ttu-id="5f418-611">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="5f418-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="5f418-612">Programa &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="5f418-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="5f418-613">**Nota:**  El generador de UE-V codifica los caracteres mayor que y menor que, como &gt; y &lt; respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="5f418-614">En raras ocasiones, el valor del nombre de archivo no incluirá necesariamente la extensión. exe, pero debe especificarse como parte del valor.</span><span class="sxs-lookup"><span data-stu-id="5f418-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="5f418-615">Por ejemplo, `<Filename>MyApplictication.exe</Filename>` debe especificarse en lugar de `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="5f418-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="5f418-616">En el segundo ejemplo no se aplica la plantilla al proceso si el nombre real del archivo ejecutable es "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="5f418-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="5f418-617">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="5f418-617">Architecture</span></span>

**<span data-ttu-id="5f418-618">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-618">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-619">Tipo: arquitectura (cadena)</span><span class="sxs-lookup"><span data-stu-id="5f418-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="5f418-620">Arquitectura se refiere a la arquitectura de procesador para la que se compiló el ejecutable de destino.</span><span class="sxs-lookup"><span data-stu-id="5f418-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="5f418-621">Los valores válidos son Win32 para las aplicaciones de 32 bits o Win64 para aplicaciones de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5f418-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="5f418-622">Si está presente, esta etiqueta limita la aplicabilidad de la plantilla de ubicación de configuración a una arquitectura de aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="5f418-623">Para obtener un ejemplo de esto, compare la experiencia de usuario de%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml y los archivos de MicrosoftOffice2010Win64.xml incluidos en UE-V.</span><span class="sxs-lookup"><span data-stu-id="5f418-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="5f418-624">Esto es útil cuando las rutas relativas cambian entre diferentes versiones de un archivo ejecutable o si se han agregado o quitado parámetros de configuración al pasar de una arquitectura de procesador a otra.</span><span class="sxs-lookup"><span data-stu-id="5f418-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="5f418-625">Si este elemento está ausente, la plantilla de ubicación de configuración omite la arquitectura del proceso y se aplica a los procesos de 32 y 64 bits si se aplican el nombre de archivo y otros atributos.</span><span class="sxs-lookup"><span data-stu-id="5f418-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="5f418-626">**Nota:**  UE-V no admite procesadores ARM en esta versión.</span><span class="sxs-lookup"><span data-stu-id="5f418-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="5f418-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="5f418-627">ProductName</span></span>

**<span data-ttu-id="5f418-628">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-628">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-629">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-629">Type: String</span></span>**

<span data-ttu-id="5f418-630">ProductName es un elemento opcional que se usa para identificar un producto con fines administrativos o de generación de informes.</span><span class="sxs-lookup"><span data-stu-id="5f418-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="5f418-631">ProductName difiere de FILENAME en el que no hay restricciones de expresiones regulares en su valor.</span><span class="sxs-lookup"><span data-stu-id="5f418-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="5f418-632">Esto permite comprender más fácilmente las descripciones de un proceso donde el nombre ejecutable puede no ser obvio.</span><span class="sxs-lookup"><span data-stu-id="5f418-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="5f418-633">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f418-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="5f418-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="5f418-634">FileDescription</span></span>

**<span data-ttu-id="5f418-635">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-635">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-636">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-636">Type: String</span></span>**

<span data-ttu-id="5f418-637">FileDescription es una etiqueta opcional que permite una descripción administrativa del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="5f418-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="5f418-638">Este es un campo de texto sin formato y puede ser útil para distinguir varios ejecutables dentro de un paquete de software donde es necesario identificar la función del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="5f418-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="5f418-639">Por ejemplo, en una aplicación adecuada podría ser útil proporcionar avisos sobre la función de dos ejecutables (MyApplication.exe y MyApplicationHelper.exe), tal como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="5f418-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="5f418-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-640">ProductVersion</span></span>

**<span data-ttu-id="5f418-641">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-641">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-642">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-642">Type: String</span></span>**

<span data-ttu-id="5f418-643">ProductVersion hace referencia a las versiones principales y secundarias de los productos de un archivo, así como a un nivel de compilación y revisión.</span><span class="sxs-lookup"><span data-stu-id="5f418-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="5f418-644">ProductVersion es un elemento opcional, pero, si se especifica, debe contener al menos el elemento secundario principal.</span><span class="sxs-lookup"><span data-stu-id="5f418-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="5f418-645">El valor debe expresar un rango con el formato mínimo = "X" máximo = "Y" donde X e y son enteros.</span><span class="sxs-lookup"><span data-stu-id="5f418-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="5f418-646">Los valores mínimos y máximos pueden ser idénticos.</span><span class="sxs-lookup"><span data-stu-id="5f418-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="5f418-647">Es posible que los elementos de versión de archivo y producto no estén especificados.</span><span class="sxs-lookup"><span data-stu-id="5f418-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="5f418-648">De este modo, se convierte la plantilla "independiente de la versión", lo que significa que la plantilla se aplicará a todas las versiones del archivo ejecutable especificado.</span><span class="sxs-lookup"><span data-stu-id="5f418-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="5f418-649">Ejemplo 1:</span><span class="sxs-lookup"><span data-stu-id="5f418-649">Example 1:</span></span>**

<span data-ttu-id="5f418-650">Versión del producto: 1,0 especificada en el generador de UE-V genera el siguiente XML:</span><span class="sxs-lookup"><span data-stu-id="5f418-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="5f418-651">Ejemplo 2:</span><span class="sxs-lookup"><span data-stu-id="5f418-651">Example 2:</span></span>**

<span data-ttu-id="5f418-652">Versión del archivo: 5.0.2.1000 especificada en el generador de UE-V genera el siguiente XML:</span><span class="sxs-lookup"><span data-stu-id="5f418-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="5f418-653">Ejemplo incorrecto 1: intervalo incompleto:</span><span class="sxs-lookup"><span data-stu-id="5f418-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="5f418-654">Solo está presente el atributo Minimum.</span><span class="sxs-lookup"><span data-stu-id="5f418-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="5f418-655">El valor máximo debe incluirse también en un rango.</span><span class="sxs-lookup"><span data-stu-id="5f418-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="5f418-656">Ejemplo incorrecto 2: se especificó una menor sin el elemento principal:</span><span class="sxs-lookup"><span data-stu-id="5f418-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="5f418-657">Solo está presente el elemento menor.</span><span class="sxs-lookup"><span data-stu-id="5f418-657">Only the Minor element is present.</span></span> <span data-ttu-id="5f418-658">También se debe incluir una mayor importancia.</span><span class="sxs-lookup"><span data-stu-id="5f418-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="5f418-659">FileVersion</span><span class="sxs-lookup"><span data-stu-id="5f418-659">FileVersion</span></span>

**<span data-ttu-id="5f418-660">Obligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="5f418-660">Mandatory: False</span></span>**

**<span data-ttu-id="5f418-661">Tipo: cadena</span><span class="sxs-lookup"><span data-stu-id="5f418-661">Type: String</span></span>**

<span data-ttu-id="5f418-662">FileVersion distingue entre la versión de lanzamiento de una aplicación publicada y los detalles internos de la compilación de un ejecutable de componente.</span><span class="sxs-lookup"><span data-stu-id="5f418-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="5f418-663">Para la mayoría de las aplicaciones comerciales, estos números son idénticos.</span><span class="sxs-lookup"><span data-stu-id="5f418-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="5f418-664">Cuando varían, la versión de producto de un archivo indica la identificación de la versión genérica de un archivo, mientras que la versión de archivo indica una compilación específica de un archivo (como en el caso de una revisión o una actualización).</span><span class="sxs-lookup"><span data-stu-id="5f418-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="5f418-665">Esto identifica de forma única los archivos sin romper la lógica de detección.</span><span class="sxs-lookup"><span data-stu-id="5f418-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="5f418-666">Para determinar la versión del producto y la versión de archivo de un ejecutable en particular, haga clic con el botón derecho en el archivo en el explorador de Windows, seleccione Propiedades y, a continuación, haga clic en la pestaña detalles.</span><span class="sxs-lookup"><span data-stu-id="5f418-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="5f418-667">Incluir un elemento FileVersion para una aplicación permite una lógica de detección de ajuste más granular, pero no es necesario para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f418-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="5f418-668">La configuración del elemento de ProductVersion se comprueba en primer lugar y, a continuación, se comprueba la opción FileVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="5f418-669">Se aplicará la configuración más restrictiva.</span><span class="sxs-lookup"><span data-stu-id="5f418-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="5f418-670">Los elementos secundarios y las reglas de sintaxis de la FileVersion son idénticos a los de ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="5f418-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="5f418-671">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="5f418-671">Application Element</span></span>

<span data-ttu-id="5f418-672">Aplicación es un contenedor de la configuración que se aplica a una aplicación en particular.</span><span class="sxs-lookup"><span data-stu-id="5f418-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="5f418-673">Es una colección de los siguientes campos o tipos.</span><span class="sxs-lookup"><span data-stu-id="5f418-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f418-674">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="5f418-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="5f418-675">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-676">Name</span><span class="sxs-lookup"><span data-stu-id="5f418-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-677">Especifica un nombre único para la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-678">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-679">Para obtener más información, vea <a href="#name" data-raw-source="[Name](#name)"> nombre </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-680">ID</span><span class="sxs-lookup"><span data-stu-id="5f418-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-681">Rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-682">Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f418-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="5f418-683">Para obtener más información, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-684">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-685">Una descripción opcional de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-686">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="5f418-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-687">Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f418-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-689">Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-690">Versión</span><span class="sxs-lookup"><span data-stu-id="5f418-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-691">Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios.</span><span class="sxs-lookup"><span data-stu-id="5f418-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="5f418-692">Para obtener más información, consulte <a href="#version" data-raw-source="[Version](#version)"> versión </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="5f418-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-694">Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no.</span><span class="sxs-lookup"><span data-stu-id="5f418-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="5f418-695">Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="5f418-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-697">De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365.</span><span class="sxs-lookup"><span data-stu-id="5f418-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="5f418-698">Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-699">Procesos</span><span class="sxs-lookup"><span data-stu-id="5f418-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-700">Un contenedor para una colección de uno o varios elementos de proceso.</span><span class="sxs-lookup"><span data-stu-id="5f418-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="5f418-701">Para obtener más información, consulte <a href="#processes" data-raw-source="[Processes](#processes)"> procesos </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-702">Configuración</span><span class="sxs-lookup"><span data-stu-id="5f418-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-703">Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="5f418-704">Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f418-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="5f418-705">Para obtener más información, vea <strong> configuración </strong> de los <a href="#data" data-raw-source="[Data types](#data)"> tipos de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="5f418-706">Elemento común</span><span class="sxs-lookup"><span data-stu-id="5f418-706">Common Element</span></span>

<span data-ttu-id="5f418-707">Common es similar a un elemento de la aplicación, pero siempre está asociado con dos o más elementos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="5f418-708">La sección común representa el conjunto de opciones de configuración que se comparten entre las instancias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f418-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="5f418-709">Es una colección de los siguientes campos o tipos.</span><span class="sxs-lookup"><span data-stu-id="5f418-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f418-710">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="5f418-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="5f418-711">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-712">Name</span><span class="sxs-lookup"><span data-stu-id="5f418-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-713">Especifica un nombre único para la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-714">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-715">Para obtener más información, vea <a href="#name" data-raw-source="[Name](#name)"> nombre </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-716">ID</span><span class="sxs-lookup"><span data-stu-id="5f418-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-717">Rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-718">Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f418-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="5f418-719">Para obtener más información, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-720">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-721">Una descripción opcional de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-722">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="5f418-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-723">Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f418-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-725">Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-726">Versión</span><span class="sxs-lookup"><span data-stu-id="5f418-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-727">Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios.</span><span class="sxs-lookup"><span data-stu-id="5f418-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="5f418-728">Para obtener más información, consulte <a href="#version" data-raw-source="[Version](#version)"> versión </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="5f418-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-730">Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no.</span><span class="sxs-lookup"><span data-stu-id="5f418-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="5f418-731">Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="5f418-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-733">De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365.</span><span class="sxs-lookup"><span data-stu-id="5f418-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="5f418-734">Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5f418-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-735">Configuración</span><span class="sxs-lookup"><span data-stu-id="5f418-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-736">Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="5f418-737">Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f418-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="5f418-738">Para obtener más información, vea <strong> configuración </strong> de los <a href="#data" data-raw-source="[Data types](#data)"> tipos de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="5f418-739">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="5f418-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="5f418-740">Este elemento define la configuración para una sola aplicación o un conjunto de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f418-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f418-741">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="5f418-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="5f418-742">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-743">Name</span><span class="sxs-lookup"><span data-stu-id="5f418-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-744">Especifica un nombre único para la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="5f418-745">Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración.</span><span class="sxs-lookup"><span data-stu-id="5f418-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="5f418-746">Para obtener más información, vea <a href="#name" data-raw-source="[Name](#name)"> nombre </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-747">ID</span><span class="sxs-lookup"><span data-stu-id="5f418-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-748">Rellena un identificador único para una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="5f418-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="5f418-749">Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5f418-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="5f418-750">Para obtener más información, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="5f418-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-751">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f418-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-752">Una descripción opcional de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f418-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f418-753">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="5f418-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-754">Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f418-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f418-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f418-756">Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</span><span class="sxs-lookup"><span data-stu-id="5f418-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="5f418-757">Apéndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="5f418-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="5f418-758">Este es el archivo SettingsLocationTemplate. xsd que muestra sus elementos, elementos secundarios, atributos y parámetros:</span><span class="sxs-lookup"><span data-stu-id="5f418-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="5f418-759">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f418-759">Related topics</span></span>


[<span data-ttu-id="5f418-760">Trabajar con plantillas de UE-V 2. x personalizadas y el generador de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="5f418-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="5f418-761">Referencia técnica de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="5f418-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





