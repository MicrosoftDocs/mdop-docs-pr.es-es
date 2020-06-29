---
title: Migrar a App-V 5.1 desde una versión anterior
description: Migrar a App-V 5.1 desde una versión anterior
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813551"
---
# <span data-ttu-id="4e469-103">Migrar a App-V 5.1 desde una versión anterior</span><span class="sxs-lookup"><span data-stu-id="4e469-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="4e469-104">Con Microsoft Application Virtualization (App-V) 5,1, puede migrar la infraestructura de App-v 4,6 o App-V 5,0 existente a la infraestructura más flexible, integrada y más fácil de administrar de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="4e469-105">Sin embargo, no puede migrar directamente de App-V 4. x a App-V 5,1, debe migrar a App-V 5,0 en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="4e469-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="4e469-106">Para obtener más información sobre cómo migrar de App-V 4. x a App-V 5,0, consulte [migrar desde una versión anterior](migrating-from-a-previous-version-app-v-50.md)</span><span class="sxs-lookup"><span data-stu-id="4e469-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="4e469-107">**Nota:**  Los paquetes de App-V 5,1 son exactamente iguales a los de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="4e469-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="4e469-108">No se ha realizado ningún cambio en el formato de paquete entre las versiones y, por lo tanto, no es necesario convertir los paquetes de App-V 5,0 en paquetes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="4e469-109">Para obtener más información sobre las diferencias entre App-V 4,6 y App-V 5,1, consulte las **diferencias entre App-v 4,6 y la sección App-v 5,0** de [acerca de App-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="4e469-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="4e469-110">Mejoras en el convertidor de paquetes de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4e469-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="4e469-111">Ahora puede usar el convertidor de paquetes para convertir paquetes de App-V 4,6 que contienen scripts y la información del registro y scripts de los archivos. OSD de origen se incluyen ahora en la salida del convertidor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="4e469-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="4e469-112">También puede usar el `–OSDsToIncludeInPackage` parámetro con el `ConvertFrom-AppvLegacyPackage` cmdlet para especificar la información de los archivos. OSD que se convierte y se coloca en el nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="4e469-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e469-113">Nuevo en App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4e469-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="4e469-114">Antes de la aplicación-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4e469-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-115">Los archivos. XML nuevos se crean correspondientes a los archivos. OSD asociados a un paquete. Estos archivos incluyen la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="4e469-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="4e469-116">variables de entorno</span><span class="sxs-lookup"><span data-stu-id="4e469-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="4e469-117">abreviados</span><span class="sxs-lookup"><span data-stu-id="4e469-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="4e469-118">asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="4e469-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="4e469-119">información del registro</span><span class="sxs-lookup"><span data-stu-id="4e469-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="4e469-120">scripts</span><span class="sxs-lookup"><span data-stu-id="4e469-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="4e469-121">Ahora puede elegir agregar información de un subconjunto de los archivos. OSD en el directorio de origen al paquete mediante el <code>-OSDsToIncludeInPackage</code> parámetro.</span><span class="sxs-lookup"><span data-stu-id="4e469-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e469-122">La información del registro y los scripts incluidos en los archivos. OSD asociados a un paquete no se incluyeron en la salida del convertidor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="4e469-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="4e469-123">El convertidor de paquetes rellenará el nuevo paquete con información de todos los archivos. OSD en el directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="4e469-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4e469-124">Ejemplo de instrucción de conversión</span><span class="sxs-lookup"><span data-stu-id="4e469-124">Example conversion statement</span></span>

<span data-ttu-id="4e469-125">Para comprender el nuevo proceso, revise el siguiente ejemplo de la `ConvertFrom-AppvLegacyPackage` instrucción del convertidor de paquetes.</span><span class="sxs-lookup"><span data-stu-id="4e469-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="4e469-126">Si el directorio de origen (\\\\OldPkgStore\\ContosoApp) incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e469-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="4e469-127">ContosoApp. SFT</span><span class="sxs-lookup"><span data-stu-id="4e469-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="4e469-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="4e469-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="4e469-129">ContosoApp. SPRJ</span><span class="sxs-lookup"><span data-stu-id="4e469-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="4e469-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="4e469-131">X. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-131">X.osd</span></span>

-   <span data-ttu-id="4e469-132">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-132">Y.osd</span></span>

-   <span data-ttu-id="4e469-133">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-133">Z.osd</span></span>

**<span data-ttu-id="4e469-134">Y ejecuta este comando:</span><span class="sxs-lookup"><span data-stu-id="4e469-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="4e469-135">Se crea lo siguiente en el directorio de destino (\\\\NewPkgStore\\ContosoApp):</span><span class="sxs-lookup"><span data-stu-id="4e469-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="4e469-136">ContosoApp. appv</span><span class="sxs-lookup"><span data-stu-id="4e469-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="4e469-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="4e469-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="4e469-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="4e469-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="4e469-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-140">X\_Config.xml</span></span>

-   <span data-ttu-id="4e469-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="4e469-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-142">Z\_Config.xml</span></span>

**<span data-ttu-id="4e469-143">En el ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="4e469-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e469-144">Estos archivos de directorio de origen...</span><span class="sxs-lookup"><span data-stu-id="4e469-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="4e469-145">... se convierten en estos archivos de directorio de destino...</span><span class="sxs-lookup"><span data-stu-id="4e469-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="4e469-146">... y contendrá estos elementos</span><span class="sxs-lookup"><span data-stu-id="4e469-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="4e469-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e469-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="4e469-148">X. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="4e469-149">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="4e469-150">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4e469-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="4e469-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="4e469-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4e469-154">Variables de entorno</span><span class="sxs-lookup"><span data-stu-id="4e469-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="4e469-155">Abreviados</span><span class="sxs-lookup"><span data-stu-id="4e469-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="4e469-156">Asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="4e469-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="4e469-157">Información del registro</span><span class="sxs-lookup"><span data-stu-id="4e469-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="4e469-158">Scripts</span><span class="sxs-lookup"><span data-stu-id="4e469-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="4e469-159">Cada archivo. OSD se convierte en un archivo. xml independiente y correspondiente que contiene los elementos que se enumeran aquí en el formato de configuración de implementación de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="4e469-160">Estos elementos se pueden copiar desde estos archivos. XML y colocarlos en la configuración de implementación o los archivos de configuración de usuario según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4e469-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="4e469-161">En este ejemplo, hay tres archivos. XML, que corresponden a los tres archivos. OSD del directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="4e469-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="4e469-162">Cada archivo. xml contiene las variables de entorno, los accesos directos, las asociaciones de tipos de archivo, la información del registro y las secuencias de comandos en su archivo. OSD correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4e469-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="4e469-163">X. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="4e469-164">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="4e469-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4e469-165">ContosoApp. appv</span><span class="sxs-lookup"><span data-stu-id="4e469-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="4e469-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="4e469-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="4e469-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4e469-168">Variables de entorno</span><span class="sxs-lookup"><span data-stu-id="4e469-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="4e469-169">Abreviados</span><span class="sxs-lookup"><span data-stu-id="4e469-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="4e469-170">Asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="4e469-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="4e469-171">La información de los archivos. OSD especificados en el <code>-OSDsToIncludeInPackage</code> parámetro se convierten y se colocan dentro del paquete.</span><span class="sxs-lookup"><span data-stu-id="4e469-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="4e469-172">A continuación, el convertidor rellena el archivo de configuración de implementación y el archivo de configuración de usuario con el contenido del paquete, del mismo modo que el secuenciador de App-V realiza al secuenciar un nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="4e469-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="4e469-173">En este ejemplo, las variables de entorno, los accesos directos y las asociaciones de tipo de archivo incluidos en X. OSD e y. OSD se han convertido y colocado en el paquete de App-V, y parte de esta información también se incluyó en la configuración de implementación y en los archivos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="4e469-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="4e469-174">X. OSD e y. OSD se usaron porque se incluyeron como argumentos para el <code>-OSDsToIncludeInPackage</code> parámetro.</span><span class="sxs-lookup"><span data-stu-id="4e469-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="4e469-175">No se incluyó información de Z. OSD en el paquete porque no se incluyó como uno de estos argumentos.</span><span class="sxs-lookup"><span data-stu-id="4e469-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4e469-176">Conversión de paquetes creados con una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="4e469-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="4e469-177">Use la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales creados con versiones de App-V anteriores a App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="4e469-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="4e469-178">El convertidor de paquetes usa PowerShell para convertir paquetes y puede ayudar a automatizar el proceso si tiene muchos paquetes que requieren conversión.</span><span class="sxs-lookup"><span data-stu-id="4e469-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="4e469-179">**Importante**  Después de convertir un paquete existente, debe probar el paquete antes de implementar el paquete para asegurarse de que el proceso de conversión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e469-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="4e469-180">Qué debe saber antes de convertir paquetes existentes</span><span class="sxs-lookup"><span data-stu-id="4e469-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e469-181">Problema</span><span class="sxs-lookup"><span data-stu-id="4e469-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="4e469-182">Solución alternativa</span><span class="sxs-lookup"><span data-stu-id="4e469-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-183">Los paquetes virtuales que usan DSC no se vinculan después de la conversión.</span><span class="sxs-lookup"><span data-stu-id="4e469-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e469-184">Vincule los paquetes usando grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="4e469-184">Link the packages using connection groups.</span></span> <span data-ttu-id="4e469-185">Consulte <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> Administración de grupos de conexión </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e469-186">Los conflictos de variables de entorno se detectan durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="4e469-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e469-187">Resuelva los conflictos en el <strong> archivo. OSD asociado </strong> .</span><span class="sxs-lookup"><span data-stu-id="4e469-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-188">Las rutas de código no modificables se detectan durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="4e469-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e469-189">Las rutas de código no modificables son difíciles de convertir correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e469-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="4e469-190">El convertidor de paquetes detectará y devolverá paquetes con archivos que contienen rutas de código no modificables.</span><span class="sxs-lookup"><span data-stu-id="4e469-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="4e469-191">Visualice el archivo con la ruta de acceso del código y determine si el paquete necesita el archivo.</span><span class="sxs-lookup"><span data-stu-id="4e469-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="4e469-192">En ese caso, se recomienda volver a crear el paquete.</span><span class="sxs-lookup"><span data-stu-id="4e469-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4e469-193">Al convertir un paquete, comprobar si hay errores en los archivos o en los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="4e469-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="4e469-194">Busque el elemento en el paquete de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="4e469-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="4e469-195">Puede ser una ruta de acceso no modificable.</span><span class="sxs-lookup"><span data-stu-id="4e469-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="4e469-196">Convertir la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4e469-196">Convert the path.</span></span>

<span data-ttu-id="4e469-197">**Nota:**  Se recomienda usar el secuenciador App-V 5,1 para convertir aplicaciones críticas o aplicaciones que necesiten aprovechar las características.</span><span class="sxs-lookup"><span data-stu-id="4e469-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="4e469-198">Vea [Cómo secuenciar una nueva aplicación con App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="4e469-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="4e469-199">Si un paquete convertido no se abre después de convertirlo, también se recomienda que vuelva a realizar la secuencia de la aplicación con el secuenciador de aplicaciones-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="4e469-200">Cómo convertir un paquete creado en una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="4e469-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="4e469-201">Migrar clientes</span><span class="sxs-lookup"><span data-stu-id="4e469-201">Migrating Clients</span></span>


<span data-ttu-id="4e469-202">En la tabla siguiente se muestra el método recomendado para actualizar clientes.</span><span class="sxs-lookup"><span data-stu-id="4e469-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e469-203">Tarea</span><span class="sxs-lookup"><span data-stu-id="4e469-203">Task</span></span></th>
<th align="left"><span data-ttu-id="4e469-204">Más información</span><span class="sxs-lookup"><span data-stu-id="4e469-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-205">Actualizar el entorno a la versión más reciente de App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="4e469-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="4e469-206">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e469-207">Instale el cliente de App-V 5,1 con la coexistencia habilitada.</span><span class="sxs-lookup"><span data-stu-id="4e469-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="4e469-208">Cómo implementar el cliente de App-V 4,6 y App-V 5,1 en el mismo equipo </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-209">Secuencia y lanzamiento de paquetes de aplicaciones-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="4e469-210">Según sea necesario, vuelva a publicar los paquetes de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="4e469-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="4e469-211">Cómo secuencia una nueva aplicación con App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4e469-212">**Importante**  Debe estar ejecutando la última versión de App-V 4.6 para usar el modo de coexistencia.</span><span class="sxs-lookup"><span data-stu-id="4e469-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="4e469-213">Además, al secuenciar un paquete, debe configurar la configuración de la autoridad de administración, que se encuentra en la **configuración del usuario** , en la sección **configuración de usuario** .</span><span class="sxs-lookup"><span data-stu-id="4e469-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="4e469-214">Migrar la infraestructura completa de App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="4e469-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="4e469-215">No hay ningún método directo para actualizar a una infraestructura completa de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="4e469-216">Use la información de la siguiente sección para obtener información sobre cómo actualizar el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="4e469-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e469-217">Tarea</span><span class="sxs-lookup"><span data-stu-id="4e469-217">Task</span></span></th>
<th align="left"><span data-ttu-id="4e469-218">Más información</span><span class="sxs-lookup"><span data-stu-id="4e469-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-219">Actualiza tu entorno a la versión más reciente de App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="4e469-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="4e469-220">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e469-221">Implemente la versión de App-V 5,1 del cliente.</span><span class="sxs-lookup"><span data-stu-id="4e469-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="4e469-222">Cómo implementar el cliente de App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e469-223">Instale App-V 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="4e469-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="4e469-224">Cómo implementar el servidor de App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="4e469-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e469-225">Migrar paquetes existentes.</span><span class="sxs-lookup"><span data-stu-id="4e469-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e469-226">Consulte la <strong> sección convertir paquetes creados con una versión anterior de App-V </strong> de este artículo.</span><span class="sxs-lookup"><span data-stu-id="4e469-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4e469-227">Tareas adicionales de migración</span><span class="sxs-lookup"><span data-stu-id="4e469-227">Additional Migration tasks</span></span>


<span data-ttu-id="4e469-228">También puede realizar tareas adicionales de migración, como cambiar la configuración de los extremos, así como abrir un paquete creado con una versión anterior en un equipo que ejecute el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4e469-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="4e469-229">Los vínculos siguientes proporcionan más información sobre cómo realizar estas tareas.</span><span class="sxs-lookup"><span data-stu-id="4e469-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="4e469-230">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="4e469-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="4e469-231">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="4e469-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="4e469-232">Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="4e469-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="4e469-233">Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="4e469-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="4e469-234">Otros recursos para realizar tareas de migración de App-V</span><span class="sxs-lookup"><span data-stu-id="4e469-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="4e469-235">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4e469-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="4e469-236">Un procedimiento simplificado para la actualización del servidor de administración de Microsoft App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4e469-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





