---
title: Publicación de aplicaciones e interacción de clientes
description: Publicación de aplicaciones e interacción de clientes
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814735"
---
# <span data-ttu-id="b3a4d-103">Publicación de aplicaciones e interacción de clientes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="b3a4d-104">Este artículo ofrece información técnica sobre las operaciones de cliente de App-V comunes y su integración con el sistema operativo local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="b3a4d-105">Archivos de paquete de App-V creados por el secuenciador</span><span class="sxs-lookup"><span data-stu-id="b3a4d-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="b3a4d-106">¿Qué hay en el archivo de appv?</span><span class="sxs-lookup"><span data-stu-id="b3a4d-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="b3a4d-107">Ubicaciones de almacenamiento de datos de cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="b3a4d-108">Registro del paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="b3a4d-109">Comportamiento del almacén de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="b3a4d-110">Datos y registro de itinerancia</span><span class="sxs-lookup"><span data-stu-id="b3a4d-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="b3a4d-111">Administración del ciclo de vida de aplicaciones de cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="b3a4d-112">Integración de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="b3a4d-113">Procesamiento de configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="b3a4d-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="b3a4d-114">Ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="b3a4d-115">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="b3a4d-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="b3a4d-116">Para obtener información de referencia adicional, consulte [Página de descarga de recursos de documentación de Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="b3a4d-117">Archivos de paquete de App-V creados por el secuenciador</span><span class="sxs-lookup"><span data-stu-id="b3a4d-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="b3a4d-118">El secuenciador crea paquetes de App-V y genera una aplicación virtualizada.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="b3a4d-119">El proceso de secuencia crea los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-120">Archivo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-120">File</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-122">. appv</span><span class="sxs-lookup"><span data-stu-id="b3a4d-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-123">El archivo de paquete principal, que contiene los activos y la información de estado capturados del proceso de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-124">Arquitectura del archivo de paquete, información de publicación y registro en un formulario con token que se puede volver a aplicar a un equipo y a un usuario específico después de su entrega.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-125">. MS</span><span class="sxs-lookup"><span data-stu-id="b3a4d-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-126">Contenedor de implementación ejecutable que puede usar para implementar archivos. appv de forma manual o mediante una plataforma de implementación de terceros.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-128">Archivo que se usa para personalizar los parámetros de publicación predeterminados de todas las aplicaciones de un paquete que se implementa globalmente para todos los usuarios de un equipo que ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-130">Archivo que se usa para personalizar los parámetros de publicación de todas las aplicaciones en un paquete que se ha implementado en un usuario específico en un equipo que ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-132">Resumen de los mensajes resultantes del proceso de secuenciación, incluidos los drivers omitidos, los archivos y las ubicaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-133">. CAB</span><span class="sxs-lookup"><span data-stu-id="b3a4d-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="b3a4d-134">Opcional: </em> archivo de acelerador de paquetes que se usa para volver a crear automáticamente un paquete de aplicación virtual secuenciado previamente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-135">.appvt</span><span class="sxs-lookup"><span data-stu-id="b3a4d-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="b3a4d-136">Opcional: </em> archivo de plantilla de secuenciador que se usa para conservar la configuración del secuenciador reutilizada.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b3a4d-137">Para obtener información sobre la secuenciación, consulte [Guía de secuenciación de Application virtualization 5,0](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-137">For information about sequencing, see [Application Virtualization 5.0 Sequencing Guide](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="b3a4d-138">¿Qué hay en el archivo de appv?</span><span class="sxs-lookup"><span data-stu-id="b3a4d-138">What’s in the appv file?</span></span>


<span data-ttu-id="b3a4d-139">El archivo de appv es un contenedor que almacena archivos XML y no XML juntos en una sola entidad.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="b3a4d-140">Este archivo se crea a partir del formato AppX, que se basa en el estándar convenciones de empaquetado abierto (OPC).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="b3a4d-141">Para ver el contenido del archivo de appv, haga una copia del paquete y, a continuación, cambie el nombre del archivo copiado a una extensión ZIP.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="b3a4d-142">El archivo de appv contiene la carpeta y los archivos siguientes, que se usan al crear y publicar una aplicación virtual:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="b3a4d-143">Name</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-144">Type</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-146">Raíz</span><span class="sxs-lookup"><span data-stu-id="b3a4d-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-147">Carpeta de archivos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-148">Directorio que contiene el sistema de archivos de la aplicación virtualizada que se captura durante la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-149">[Content_Types]. XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-150">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-151">Lista de los tipos de contenido principales en el archivo de appv (por ejemplo, DLL, EXE, BIN).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-153">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-154">Diseño del archivo de appv, que usa los elementos archivo, bloque y BlockMap que permiten la ubicación y validación de archivos en el paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-156">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-157">Metadatos del paquete que contiene la información necesaria para agregar, publicar e iniciar el paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="b3a4d-158">Incluye puntos de extensión (asociaciones de tipo de archivo y accesos directos), así como los nombres y GUID asociados con el paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-160">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-161">Lista de los archivos capturados durante la secuenciación, incluidos los atributos (por ejemplo, directorios, archivos, directorios opacos, directorios vacíos y nombres largos y cortos).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-163">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-164">Información sobre el equipo de secuencia (versión del sistema operativo, versión de Internet Explorer, versión de .NET Framework) y proceso (actualización, versión de paquete).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-165">Registry. dat</span><span class="sxs-lookup"><span data-stu-id="b3a4d-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-166">Archivo DAT</span><span class="sxs-lookup"><span data-stu-id="b3a4d-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-167">Claves y valores de registro capturados durante el proceso de secuenciación para el paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-169">Archivo XML</span><span class="sxs-lookup"><span data-stu-id="b3a4d-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-170">Lista de archivos para el bloque de características principal y de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="b3a4d-171">El bloque de características de publicación contiene los archivos ICO y las partes necesarias de los archivos (EXE y DLL) para publicar el paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="b3a4d-172">Cuando está presente, el bloque de características principal incluye los archivos que se han optimizado para la transmisión por secuencias durante el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="b3a4d-173">Ubicaciones de almacenamiento de datos de cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-173">App-V client data storage locations</span></span>


<span data-ttu-id="b3a4d-174">El cliente de App-V realiza tareas para garantizar que las aplicaciones virtuales se ejecuten correctamente y funcionen como aplicaciones instaladas de forma local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="b3a4d-175">El proceso de apertura y ejecución de aplicaciones virtuales requiere la asignación desde el sistema de archivos virtual y el registro para garantizar que la aplicación tenga los componentes necesarios de una aplicación tradicional prevista por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="b3a4d-176">En esta sección se describen los activos necesarios para ejecutar aplicaciones virtuales y se muestra una lista de la ubicación en la que App-V almacena los activos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-177">Nombre</span><span class="sxs-lookup"><span data-stu-id="b3a4d-177">Name</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-178">Ubicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-178">Location</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-180">Tienda de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-182">Ubicación predeterminada de los archivos de paquete de solo lectura</span><span class="sxs-lookup"><span data-stu-id="b3a4d-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-183">Catálogo de máquina</span><span class="sxs-lookup"><span data-stu-id="b3a4d-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="b3a4d-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-185">Contiene documentos de configuración por máquina</span><span class="sxs-lookup"><span data-stu-id="b3a4d-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-186">Catálogo de usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="b3a4d-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-188">Contiene documentos de configuración por usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-189">Copias de seguridad de accesos directos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="b3a4d-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-191">Almacena los puntos de integración anteriores que permiten la restauración al volver a publicar el paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-192">Itinerancia de copia en escritura (vaca)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="b3a4d-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-194">Ubicación de itinerancia grabable para la modificación de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-195">Copiar en escritura (COW) local</span><span class="sxs-lookup"><span data-stu-id="b3a4d-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="b3a4d-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-197">Ubicación de no movilidad grabable para la modificación de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-198">Registro del equipo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="b3a4d-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-200">Contiene información de estado del paquete, incluyendo VReg para equipos o paquetes publicados globalmente (sección equipo)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-201">Registro de usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="b3a4d-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-203">Contiene información de estado del paquete de usuario, incluido VReg</span><span class="sxs-lookup"><span data-stu-id="b3a4d-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-204">Clases de registro de usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="b3a4d-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-206">Contiene información adicional sobre el estado de un paquete de usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b3a4d-207">Los detalles adicionales de la tabla se muestran en la sección siguiente y en todo el documento.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="b3a4d-208">Tienda de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-208">Package store</span></span>

<span data-ttu-id="b3a4d-209">El cliente de App-V administra los activos de las aplicaciones montados en el almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="b3a4d-210">Esta ubicación de almacenamiento predeterminada es `%ProgramData%\App-V` , pero puede configurarla durante o después de la instalación mediante el `Set-AppVClientConfiguration` comando PowerShell, que modifica el registro local ( `PackageInstallationRoot` valor de la `HKLM\Software\Microsoft\AppV\Client\Streaming` clave).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="b3a4d-211">El almacén de paquetes debe estar ubicado en una ruta local en el sistema operativo del cliente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="b3a4d-212">Los paquetes individuales se almacenan en el almacén de paquetes en los subdirectorios denominados para el GUID del paquete y la GUID de versión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="b3a4d-213">Ejemplo de una ruta de acceso a una aplicación específica:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="b3a4d-214">Para cambiar la ubicación predeterminada del almacén de paquetes durante la configuración, vea [cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

### <span data-ttu-id="b3a4d-215">Almacén de contenido compartido</span><span class="sxs-lookup"><span data-stu-id="b3a4d-215">Shared Content Store</span></span>

<span data-ttu-id="b3a4d-216">Si el cliente de App-V está configurado en el modo de almacenamiento de contenido compartido, no se escribirá ningún dato en el disco cuando se produzca un error de transmisión, lo que significa que los paquetes requieren un mínimo de espacio en disco local (datos de publicación).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="b3a4d-217">El uso de menos espacio en el disco es muy conveniente en entornos de VDI, donde el almacenamiento local se puede limitar y la transmisión de las aplicaciones desde una ubicación de red de alto rendimiento (como una SAN) es preferible.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="b3a4d-218">Para obtener más información sobre el modo de almacén de contenido compartido, consulte <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="b3a4d-219">**Nota:**  El almacén de paquetes y equipos debe estar ubicado en una unidad local, incluso si usa configuraciones de almacén de contenido compartido para el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="b3a4d-220">Catálogos de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-220">Package catalogs</span></span>

<span data-ttu-id="b3a4d-221">El cliente de App-V administra las siguientes dos ubicaciones basadas en archivos:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="b3a4d-222">Catálogos (usuario y equipo).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="b3a4d-223">**Ubicaciones del registro** : depende de cómo se destinará el paquete a la publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="b3a4d-224">Hay un catálogo (almacén de datos) para el equipo y un catálogo para cada usuario individual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="b3a4d-225">El catálogo de equipos almacena información global aplicable a todos los usuarios o a cualquier usuario, y el catálogo de usuarios almacena la información aplicable a un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="b3a4d-226">El catálogo es una colección de configuraciones dinámicas y archivos de manifiesto; hay datos discretos para el archivo y el registro por versión de paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="b3a4d-227">Catálogo de máquina</span><span class="sxs-lookup"><span data-stu-id="b3a4d-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-229">Almacena los documentos de paquetes que están disponibles para los usuarios en el equipo, cuando se agregan y publican paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="b3a4d-230">Sin embargo, si un paquete es "global" en el momento de la publicación, las integraciones estarán disponibles para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="b3a4d-231">Si un paquete no es global, las integraciones se publican solo para usuarios específicos, pero todavía hay recursos globales que se han modificado y visible para cualquier persona en el equipo cliente (por ejemplo, el directorio del paquete se encuentra en una ubicación de disco compartido).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="b3a4d-232">Si hay un paquete disponible para un usuario en el equipo (global o no global), el manifiesto se almacena en el catálogo del equipo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="b3a4d-233">Cuando un paquete se publica globalmente, hay un archivo de configuración dinámica que se almacena en el catálogo del equipo; por lo tanto, la determinación de si un paquete es global se define en función de si hay un archivo de directivas (archivo UserDeploymentConfiguration) en el catálogo del equipo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-234">Ubicación de almacenamiento predeterminada</span><span class="sxs-lookup"><span data-stu-id="b3a4d-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="b3a4d-235">Esta ubicación no es la misma que la ubicación del almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="b3a4d-236">El almacén de paquetes es el oro o la copia original de los archivos del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-237">Archivos del catálogo de la máquina</span><span class="sxs-lookup"><span data-stu-id="b3a4d-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-240">UserManifest.xml (paquete publicado globalmente)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-241">UserDeploymentConfiguration.xml (paquete publicado globalmente)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-242">Ubicación adicional del catálogo de equipos, que se usa cuando el paquete forma parte de un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-243">La siguiente ubicación se agrega a la ubicación de paquete específica mencionada anteriormente:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-244">Archivos adicionales en el catálogo de equipos cuando el paquete forma parte de un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-246">UserPackageGroupDescriptor.xml (grupo de conexión publicado globalmente)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b3a4d-247">Catálogo de usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-249">Creado durante el proceso de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-249">Created during the publishing process.</span></span> <span data-ttu-id="b3a4d-250">Contiene información usada para publicar el paquete y también se usa en el lanzamiento para garantizar que se aprovisione un paquete a un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="b3a4d-251">Creado en una ubicación de itinerancia e incluye información de publicación específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="b3a4d-252">Cuando se publica un paquete para un usuario, el archivo de Directiva se almacena en el catálogo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="b3a4d-253">Al mismo tiempo, se almacena una copia del manifiesto en el catálogo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="b3a4d-254">Cuando se quita un derecho de paquete para un usuario, los archivos correspondientes del paquete se quitan del catálogo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="b3a4d-255">Si observa el catálogo de usuarios, un administrador puede ver la presencia de un archivo de configuración dinámico, lo que indica que el paquete tiene derecho a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="b3a4d-256">Para los usuarios móviles, el catálogo de usuarios debe estar en una ubicación de itinerancia o compartida para preservar el comportamiento de App-V heredado de los usuarios de destino de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="b3a4d-257">El derecho y la política están vinculadas a un usuario, no a un equipo, por lo que deben moverse con el usuario una vez que se hayan aprovisionado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-258">Ubicación de almacenamiento predeterminada</span><span class="sxs-lookup"><span data-stu-id="b3a4d-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-259">Archivos en el catálogo de usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-261">DynamicConfiguration.xml o UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-262">Ubicación adicional del catálogo de usuarios, usada cuando el paquete forma parte de un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-263">La siguiente ubicación se agrega a la ubicación de paquete específica mencionada anteriormente:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-264">Archivo adicional en el catálogo de la máquina cuando el paquete forma parte de un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b3a4d-265">Copias de seguridad de accesos directos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-265">Shortcut backups</span></span>

<span data-ttu-id="b3a4d-266">Durante el proceso de publicación, el cliente de App-V realiza una copia de seguridad de los accesos directos y los puntos de integración en `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` esta copia de seguridad permite la restauración de estos puntos de integración a las versiones anteriores cuando se cancela la publicación del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="b3a4d-267">Copiar archivos en escritura</span><span class="sxs-lookup"><span data-stu-id="b3a4d-267">Copy on Write files</span></span>

<span data-ttu-id="b3a4d-268">El almacén de paquetes contiene una copia original de los archivos del paquete que se han transmitido desde el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="b3a4d-269">Durante el funcionamiento normal de una aplicación de App-V, el usuario o el servicio pueden requerir cambios en los archivos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="b3a4d-270">Estos cambios no se realizan en el almacén de paquetes para preservar su capacidad de reparar la aplicación, lo que elimina estos cambios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="b3a4d-271">Estas ubicaciones, denominadas copia en escritura (COW), admiten tanto las ubicaciones de itinerancia como las no móviles.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="b3a4d-272">La ubicación en la que se almacenan las modificaciones depende de dónde se ha programado la aplicación para escribir cambios en una experiencia nativa.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="b3a4d-273">Itinerancia de vaca</span><span class="sxs-lookup"><span data-stu-id="b3a4d-273">COW roaming</span></span>

<span data-ttu-id="b3a4d-274">La ubicación de itinerancia de VACAntes descrita anteriormente almacena los cambios en archivos y directorios destinados a la ubicación de% AppData% típica o a la ubicación de \\Users\\{username}\\AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="b3a4d-275">A continuación, estos directorios y archivos se mueven en función de la configuración del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="b3a4d-276">Local de VACAntes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-276">COW local</span></span>

<span data-ttu-id="b3a4d-277">La ubicación local de vaca es similar a la ubicación de itinerancia, pero los directorios y los archivos no se mueven a otros equipos, incluso si se ha configurado la compatibilidad con la itinerancia.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="b3a4d-278">La ubicación local de VACAntes descritas anteriormente almacena los cambios aplicables a las ventanas típicas y no a la ubicación de% AppData%.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="b3a4d-279">Los directorios que aparecen en la lista variarán, pero habrá dos ubicaciones para las ubicaciones típicas de Windows (por ejemplo, AppData comunes y Common AppDataS).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="b3a4d-280">La **S** significa la ubicación restringida cuando el servicio virtual solicita el cambio como un usuario elevado diferente de los usuarios que han iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="b3a4d-281">La ubicación en la que no se almacenan los cambios**basados en usuarios** .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="b3a4d-282">Registro del paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-282">Package registry</span></span>


<span data-ttu-id="b3a4d-283">Antes de que una aplicación pueda acceder a los datos del registro del paquete, el cliente de App-V debe poner los datos del registro del paquete a disposición de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="b3a4d-284">El cliente de App-V usa el registro real como almacén de respaldo para todos los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="b3a4d-285">Cuando se agrega un paquete nuevo al cliente de App-V, una copia del registro. DAT del paquete se crea en `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="b3a4d-286">El nombre del archivo es el GUID de versión con el. Extensión DAT.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="b3a4d-287">El motivo por el que se realiza esta copia es asegurarse de que el archivo de subárbol real del paquete nunca se esté usando, lo que impedirá que se quite el paquete más adelante.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b3a4d-288">Registry. dat del almacén de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b3a4d-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</span><span class="sxs-lookup"><span data-stu-id="b3a4d-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b3a4d-290">Cuando la primera aplicación del paquete se inicia en el cliente, el cliente fases o copia el contenido del archivo de subárbol, volviendo a crear los datos del registro del paquete en una ubicación alternativa `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="b3a4d-291">Los datos de registro preconfigurados tienen dos tipos distintos de datos de equipo y datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="b3a4d-292">Los datos de la máquina se comparten entre todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="b3a4d-293">Los datos de los usuarios se almacenan en una ubicación userspecific `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="b3a4d-294">Los datos de la máquina se eliminan en última instancia en el tiempo de eliminación del paquete y los datos de usuario se eliminan en una operación de anulación de la publicación del usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="b3a4d-295">Paquetes de ensayo del registro de paquetes y de grupo de conexiones por fases</span><span class="sxs-lookup"><span data-stu-id="b3a4d-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="b3a4d-296">Cuando hay grupos de conexión, el proceso anterior de ensayo del registro tiene el valor true, pero en lugar de tener un subárbol para procesar, hay más de uno.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="b3a4d-297">Los archivos se procesan en el orden en que aparecen en el XML del grupo de conexión, con el primer editor que gana conflictos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="b3a4d-298">El registro preconfigurado persiste de la misma manera que en el caso de un único paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="b3a4d-299">Los datos del registro de usuario preconfigurados permanecen para el grupo de conexión hasta que se deshabilitan; los datos del registro de la máquina ensayada se quitan de la eliminación del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="b3a4d-300">Registro virtual</span><span class="sxs-lookup"><span data-stu-id="b3a4d-300">Virtual registry</span></span>

<span data-ttu-id="b3a4d-301">El propósito del registro virtual (VREG) es proporcionar una única vista combinada del registro del paquete y del registro nativo en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="b3a4d-302">También proporciona funcionalidad de copia en escritura (COW), es decir, cualquier cambio realizado en el registro desde el contexto de un proceso virtual se realiza en una ubicación de vaca distinta.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="b3a4d-303">Esto significa que el VREG debe combinar hasta tres ubicaciones de registro independientes en una sola vista basada en las ubicaciones rellenadas en el registro de COW- &gt; paquete- &gt; nativo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="b3a4d-304">Cuando se realiza una solicitud de que los datos del registro se encuentren por orden hasta que encuentre los datos que ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="b3a4d-305">Es decir, si hay un valor almacenado en una ubicación de vaca, no podrá continuar con otras ubicaciones, sin embargo, si no hay datos en la ubicación de vaca, pasará al paquete y luego a la ubicación nativa hasta que encuentre los datos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="b3a4d-306">Ubicaciones del registro</span><span class="sxs-lookup"><span data-stu-id="b3a4d-306">Registry locations</span></span>

<span data-ttu-id="b3a4d-307">Hay dos ubicaciones del registro de paquetes y dos ubicaciones de grupos de conexiones en las que el cliente de App-V almacena la información del registro, en función de si el paquete se publica de forma individual o como parte de un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="b3a4d-308">Existen tres ubicaciones de vacas para paquetes y tres para grupos de conexión, que se crean y administran mediante el VREG.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="b3a4d-309">La configuración de paquetes y grupos de conexiones no es compartida:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="b3a4d-310">Un solo paquete VReg:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b3a4d-311">Ubicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b3a4d-312">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b3a4d-313">VACA</span><span class="sxs-lookup"><span data-stu-id="b3a4d-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (solo se puede escribir en el proceso de elevación)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-315">User Registry\Client\Packages\PkgGUID\REGISTRY (usuarios que viajan por escrito en HKCU excepto Software\Classes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-316">Registro de usuario Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes escrituras y HKLM para procesos no elevados)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b3a4d-317">Paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-318">Equipo Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span><span class="sxs-lookup"><span data-stu-id="b3a4d-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-319">Registro de usuario Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span><span class="sxs-lookup"><span data-stu-id="b3a4d-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b3a4d-320">Nativa</span><span class="sxs-lookup"><span data-stu-id="b3a4d-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-321">Ubicación nativa del registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="b3a4d-322">VReg de grupo de conexión:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b3a4d-323">Ubicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b3a4d-324">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b3a4d-325">VACA</span><span class="sxs-lookup"><span data-stu-id="b3a4d-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (solo se puede escribir en el proceso de elevación)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (cualquier cosa que se escriba en HKCU excepto Software\Classes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-328">Registro de usuario Classes\Client\PackageGroups\GrpGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="b3a4d-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b3a4d-329">Paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-330">Equipo Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="b3a4d-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-331">Registro de usuario Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="b3a4d-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b3a4d-332">Nativa</span><span class="sxs-lookup"><span data-stu-id="b3a4d-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b3a4d-333">Ubicación nativa del registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="b3a4d-334">Existen dos ubicaciones de vaca para HKLM; procesos elevados y no elevados.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="b3a4d-335">Los procesos elevados siempre escriben cambios de HKLM en la seguridad de vaca en HKLM.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="b3a4d-336">Los procesos no elevados siempre escriben cambios de HKLM en la vaca no segura en HKCU\\Software\\Classes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="b3a4d-337">Cuando una aplicación Lea los cambios de HKLM, los procesos elevados leerán los cambios de la vaca segura en HKLM.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="b3a4d-338">Lecturas no elevadas de ambos, favorecer los cambios realizados en la vaca no segura en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="b3a4d-339">Teclas de acceso directo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-339">Pass-through keys</span></span>

<span data-ttu-id="b3a4d-340">Las teclas de acceso directo permiten a un administrador configurar determinadas teclas para que solo puedan leerlas desde el registro nativo, omitiendo las ubicaciones de los paquetes y las VACAntes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="b3a4d-341">Las ubicaciones de paso a través son globales para el equipo (no específicas del paquete) y se pueden configurar agregando la ruta de acceso a la clave, que debe tratarse como paso a través del valor **reg \ _MULTI \ _SZ** denominado **PassThroughPaths** de la clave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="b3a4d-342">Cualquier tecla que aparezca en este valor de cadena múltiple (y sus elementos secundarios) se tratará como paso a través.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="b3a4d-343">Las siguientes ubicaciones se configuran como ubicaciones de paso a través de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="b3a4d-344">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="b3a4d-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="b3a4d-345">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="b3a4d-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="b3a4d-346">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span><span class="sxs-lookup"><span data-stu-id="b3a4d-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="b3a4d-347">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span><span class="sxs-lookup"><span data-stu-id="b3a4d-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="b3a4d-348">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span><span class="sxs-lookup"><span data-stu-id="b3a4d-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="b3a4d-349">HKEY \ _CURRENT \ _USER configuración \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet</span><span class="sxs-lookup"><span data-stu-id="b3a4d-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="b3a4d-350">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="b3a4d-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="b3a4d-351">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="b3a4d-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="b3a4d-352">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="b3a4d-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="b3a4d-353">El propósito de las claves de paso a través es garantizar que una aplicación virtual no escribe datos del registro en el VReg que se requiere para las aplicaciones no virtuales para que funcionen o se integran correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="b3a4d-354">La clave de directivas garantiza que la configuración basada en directivas de grupo establecida por el administrador se use y no por configuración de paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="b3a4d-355">La clave AppModel es necesaria para la integración con aplicaciones basadas en la interfaz de usuario moderna de Windows.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="b3a4d-356">Es recomendable que los complementos no modifiquen ninguna de las teclas de acceso directo predeterminadas, pero en algunos casos, según el comportamiento de la aplicación, es posible que necesite agregar claves de paso a través.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="b3a4d-357">Comportamiento del almacén de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-357">App-V package store behavior</span></span>


<span data-ttu-id="b3a4d-358">App-V 5 administra el almacén de paquetes, que es la ubicación en la que se almacenan los archivos de activos expandidos del archivo de appv.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="b3a4d-359">De forma predeterminada, esta ubicación se almacena en%ProgramData%\\App-V y está limitada en cuanto a las capacidades de almacenamiento solo por espacio libre en disco.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="b3a4d-360">El almacén de paquetes está organizado por los GUID para el paquete y la versión, tal y como se menciona en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="b3a4d-361">Agregar paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-361">Add packages</span></span>

<span data-ttu-id="b3a4d-362">Los paquetes de App-V se almacenan en el equipo con el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="b3a4d-363">El cliente de App-V proporciona un almacenamiento provisional a petición.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="b3a4d-364">Durante la publicación o un complemento manual Add-AppVClientPackage, la estructura de datos se crea en el almacén de paquetes (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="b3a4d-365">Los archivos de paquetes identificados en el bloque de publicación definido en el StreamMap.xml se agregan al sistema y las carpetas de nivel superior y los archivos secundarios están preconfigurados para garantizar que los activos de la aplicación sean correctos en el inicio.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="b3a4d-366">Montar paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-366">Mounting packages</span></span>

<span data-ttu-id="b3a4d-367">Los paquetes se pueden cargar explícitamente con PowerShell `Mount-AppVClientPackage` o mediante la **interfaz de usuario del cliente de App-V** para descargar un paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="b3a4d-368">Esta operación carga completamente todo el paquete en el almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="b3a4d-369">Paquetes de streaming</span><span class="sxs-lookup"><span data-stu-id="b3a4d-369">Streaming packages</span></span>

<span data-ttu-id="b3a4d-370">El cliente de App-V puede configurarse para cambiar el comportamiento predeterminado de la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="b3a4d-371">Todas las directivas de transmisión se almacenan en la siguiente clave de registro: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="b3a4d-372">Las directivas se establecen con el cmdlet de PowerShell `Set-AppvClientConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="b3a4d-373">Las siguientes directivas se aplican a la transmisión por secuencias:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-374">Directiva</span><span class="sxs-lookup"><span data-stu-id="b3a4d-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-375">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b3a4d-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-377">En Windows 8, permite la transmisión por secuencias a través de redes móviles y 3G.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-377">On Windows 8 it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-378">Autocargar</span><span class="sxs-lookup"><span data-stu-id="b3a4d-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-379">Especifica la configuración de carga en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="b3a4d-380">0 </strong> - deshabilitado</span><span class="sxs-lookup"><span data-stu-id="b3a4d-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="b3a4d-381">1 </strong> : solo paquetes usados previamente</span><span class="sxs-lookup"><span data-stu-id="b3a4d-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="b3a4d-382">2 </strong> : todos los paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-383">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b3a4d-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-384">La carpeta raíz para el almacén de paquetes en la máquina local</span><span class="sxs-lookup"><span data-stu-id="b3a4d-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b3a4d-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-386">El reemplazo de raíz a partir del cual se transfieren los paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b3a4d-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-388">Habilita el uso del almacén de contenido compartido para escenarios de VDI</span><span class="sxs-lookup"><span data-stu-id="b3a4d-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="b3a4d-389">Esta configuración afecta al comportamiento de la transmisión de flujo de los activos del paquete App-V al cliente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="b3a4d-390">De forma predeterminada, App-V solo descarga los recursos necesarios después de descargar los bloques iniciales de publicación y de características principales.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="b3a4d-391">Hay tres comportamientos específicos en relación con los paquetes de transmisión que se deben explicar:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="b3a4d-392">Transmisión por secuencias de fondo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-392">Background Streaming</span></span>

-   <span data-ttu-id="b3a4d-393">Transmisión por secuencias optimizada</span><span class="sxs-lookup"><span data-stu-id="b3a4d-393">Optimized Streaming</span></span>

-   <span data-ttu-id="b3a4d-394">Errores de secuencia</span><span class="sxs-lookup"><span data-stu-id="b3a4d-394">Stream Faults</span></span>

### <span data-ttu-id="b3a4d-395">Transmisión por secuencias de fondo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-395">Background streaming</span></span>

<span data-ttu-id="b3a4d-396">El cmdlet de PowerShell `Get-AppvClientConfiguration` se puede usar para determinar el modo actual para la transmisión por secuencias de fondo con la configuración de autocarga y modificar el cmdlet Set-AppvClientConfiguration o desde el registro (clave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="b3a4d-397">La transmisión por secuencias de fondo es una configuración predeterminada en la que la configuración de autocargar está configurada para descargar paquetes usados previamente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="b3a4d-398">El comportamiento basado en la configuración predeterminada (valor = 1) descarga bloques de datos de App-V en segundo plano después de que se haya iniciado la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="b3a4d-399">Esta configuración se puede deshabilitar en conjunto (valor = 0) o habilitada para todos los paquetes (valor = 2), ya sea que se hayan iniciado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="b3a4d-400">Transmisión por secuencias optimizada</span><span class="sxs-lookup"><span data-stu-id="b3a4d-400">Optimized streaming</span></span>

<span data-ttu-id="b3a4d-401">Los paquetes de App-V se pueden configurar con un bloque de características principal durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="b3a4d-402">Esta configuración permite al ingeniero de secuenciación supervisar los archivos de inicio para una aplicación o aplicaciones específicas, y marcar los bloques de datos en el paquete de App-V para transmitirlos en el primer inicio de cualquier aplicación del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="b3a4d-403">Errores de secuencia</span><span class="sxs-lookup"><span data-stu-id="b3a4d-403">Stream faults</span></span>

<span data-ttu-id="b3a4d-404">Después de la secuencia inicial de cualquier tipo de datos de publicación y el bloque de características principal, las solicitudes de archivos adicionales realizan errores de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="b3a4d-405">Estos bloques de datos se descargan en el almacén de paquetes según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="b3a4d-406">Esto permite a un usuario descargar solo una pequeña parte del paquete, generalmente suficiente para iniciar el paquete y ejecutar las tareas normales.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="b3a4d-407">Todos los demás bloques se descargan cuando un usuario inicia una operación que requiere datos que no se encuentran actualmente en el almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="b3a4d-408">Para obtener más información sobre la transmisión por secuencias de paquetes de App-V, visite: <https://go.microsoft.com/fwlink/?LinkId=392770> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="b3a4d-409">La secuencia de optimización para la transmisión por secuencias está disponible en: <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="b3a4d-410">Actualizaciones de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-410">Package upgrades</span></span>

<span data-ttu-id="b3a4d-411">Los paquetes de App-V necesitan actualizarse a lo largo del ciclo de vida de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="b3a4d-412">Las actualizaciones de paquetes de App-V son similares a la operación de publicación de paquetes, ya que cada versión se creará en su propia ubicación de PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="b3a4d-413">La operación de actualización se optimiza creando vínculos fuertes a archivos idénticos y transmitidos desde otras versiones del mismo paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="b3a4d-414">Eliminación de paquetes</span><span class="sxs-lookup"><span data-stu-id="b3a4d-414">Package removal</span></span>

<span data-ttu-id="b3a4d-415">El comportamiento del cliente de App-V cuando se quitan paquetes depende del método usado para la eliminación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="b3a4d-416">Con una infraestructura completa de App-V para anular la publicación de la aplicación, los archivos de catálogo de usuarios (catálogo de equipos para aplicaciones publicadas globalmente) se quitan, pero conservan la ubicación del almacén de paquetes y las ubicaciones de los VACAntes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="b3a4d-417">Cuando se usa el cmdlet de PowerShell `Remove-AppVClientPackge` para quitar un paquete de App-V, se limpia la ubicación del almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="b3a4d-418">Recuerde que al anular la publicación de un paquete de App-V desde el servidor de administración no se realiza una operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="b3a4d-419">Ninguna de las operaciones quitará los archivos de paquete del almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="b3a4d-420">Datos y registro de itinerancia</span><span class="sxs-lookup"><span data-stu-id="b3a4d-420">Roaming registry and data</span></span>


<span data-ttu-id="b3a4d-421">App-V 5 puede ofrecer una experiencia casi nativa en el momento de la itinerancia, en función de cómo se haya escrito la aplicación que se usa.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="b3a4d-422">De forma predeterminada, App-V AppData de itinerancia que se almacena en la ubicación de itinerancia, en función de la configuración de itinerancia del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="b3a4d-423">Otras ubicaciones para el almacenamiento de datos basados en archivos no se mueven de un equipo a otro, ya que se encuentran en ubicaciones que no se transfieren.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="b3a4d-424">Requisitos de itinerancia y almacenamiento de datos de catálogo de usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="b3a4d-425">App-V almacena datos, que representan el estado del catálogo del usuario, en forma de:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="b3a4d-426">Archivos en%appdata%\\Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="b3a4d-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="b3a4d-427">Configuración del registro en</span><span class="sxs-lookup"><span data-stu-id="b3a4d-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="b3a4d-428">En conjunto, estos archivos y la configuración del registro representan el catálogo del usuario, por lo que ambos deben ser móviles o ninguno de ellos se debe mover a un usuario dado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="b3a4d-429">App-V no es compatible con la itinerancia% AppData%, pero no se mueve el perfil del usuario (registro) o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="b3a4d-430">**Nota:**  El cmdlet **repair-AppvClientPackage** no repara el estado de publicación de los paquetes, en los que falta el estado de App-V del usuario `HKEY_CURRENT_USER` o no coincide con los datos de% appdata%.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="b3a4d-431">Datos basados en el registro</span><span class="sxs-lookup"><span data-stu-id="b3a4d-431">Registry-based data</span></span>

<span data-ttu-id="b3a4d-432">La itinerancia del registro de App-V se divide en dos escenarios, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-433">Escenario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-434">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-435">Aplicaciones que se ejecutan como usuarios estándar</span><span class="sxs-lookup"><span data-stu-id="b3a4d-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-436">Cuando un usuario estándar inicia una aplicación de App-V, tanto HKLM como HKCU para aplicaciones de App-V se almacenan en el subárbol HKCU de la máquina.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="b3a4d-437">Esto presenta dos rutas distintas:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="b3a4d-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="b3a4d-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="b3a4d-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="b3a4d-440">Las ubicaciones están habilitadas para roaming en función de la configuración del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-441">Aplicaciones que se ejecutan con elevación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-442">Cuando se inicia una aplicación con elevación:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="b3a4d-443">Los datos de HKLM se almacenan en el subárbol HKLM del equipo local</span><span class="sxs-lookup"><span data-stu-id="b3a4d-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-444">Los datos HKCU se almacenan en la ubicación del registro del usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="b3a4d-445">En este escenario, estas opciones de configuración no se trasladan con las configuraciones de itinerancia del sistema operativo normal y los valores y las claves del registro resultantes se almacenan en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="b3a4d-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="b3a4d-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="b3a4d-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="b3a4d-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b3a4d-448">App-V y redirección de carpetas</span><span class="sxs-lookup"><span data-stu-id="b3a4d-448">App-V and folder redirection</span></span>

<span data-ttu-id="b3a4d-449">App-V 5.0 SP2 admite la redirección de carpetas de la carpeta de roaming (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-449">App-V 5.0SP2 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="b3a4d-450">Cuando se inicia el entorno virtual, el estado de AppData de itinerancia del directorio de AppData de roaming del usuario se copia en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="b3a4d-451">A la inversa, cuando se cierra el entorno virtual, la memoria caché local asociada a un AppData de itinerancia de usuario específico se transfiere a la ubicación real del directorio de AppData de roaming de ese usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="b3a4d-452">Un paquete típico tiene varias ubicaciones asignadas en la tienda de respaldo del usuario para la configuración tanto en AppData\\Local como en AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="b3a4d-453">Estas ubicaciones son la copia en ubicaciones de escritura que se almacenan por usuario en el perfil del usuario y que se usan para almacenar los cambios realizados en los directorios de VFS del paquete y proteger el VFS predeterminado del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="b3a4d-454">En la tabla siguiente se muestran ubicaciones locales y móviles, cuando no se ha implementado el redireccionamiento de carpetas.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-455">Directorio de VFS en el paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-456">Ubicación asignada de la tienda de respaldo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-458">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-460">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-461">Windows</span><span class="sxs-lookup"><span data-stu-id="b3a4d-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-462">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="b3a4d-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="b3a4d-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-464">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="b3a4d-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-465">AppData</span><span class="sxs-lookup"><span data-stu-id="b3a4d-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-466">C:\users\jsmith\AppData &lt; Strong &gt; roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="b3a4d-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="b3a4d-467">En la siguiente tabla se muestran ubicaciones locales y móviles, cuando se ha implementado el redireccionamiento de carpetas para% AppData%, y se ha redirigido la ubicación (normalmente a una ubicación de red).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-468">Directorio de VFS en el paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-469">Ubicación asignada de la tienda de respaldo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-471">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-473">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="b3a4d-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-474">Windows</span><span class="sxs-lookup"><span data-stu-id="b3a4d-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-475">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="b3a4d-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="b3a4d-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-477">C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="b3a4d-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-478">AppData</span><span class="sxs-lookup"><span data-stu-id="b3a4d-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="b3a4d-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="b3a4d-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="b3a4d-480">El controlador de VFS de cliente de App-V actual no puede escribir en ubicaciones de red, por lo que el cliente de App-V detecta la presencia de redireccionamiento de carpetas y copia los datos en la unidad local durante la publicación y cuando se inicia el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="b3a4d-481">Después de que el usuario cierra la aplicación de App-V y el cliente de App-V cierra el entorno virtual, el almacenamiento local de la AppData de VFS se vuelve a copiar a la red, lo que permite la itinerancia a máquinas adicionales, donde se repetirá el proceso.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="b3a4d-482">Los pasos detallados de los procesos son:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="b3a4d-483">Durante el inicio de la publicación o del entorno virtual, el cliente de App-V detecta la ubicación del directorio de AppData.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="b3a4d-484">Si la ruta de AppData de roaming es local o Ino AppData\\Roaming ubicación está asignada, no sucede nada.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="b3a4d-485">Si la ruta de AppData de AppData no es local, el directorio de VFS se asigna al directorio local de appdata.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="b3a4d-486">Este proceso resuelve el problema de un% AppData% no local que no es compatible con el controlador de dispositivo de cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="b3a4d-487">Sin embargo, los datos almacenados en esta nueva ubicación no se mueven con el redireccionamiento de carpetas.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="b3a4d-488">Todos los cambios durante la ejecución de la aplicación se producen en la ubicación local AppData y se deben copiar a la ubicación redirigida.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="b3a4d-489">Los pasos detallados de este proceso son:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="b3a4d-490">Se cierra la aplicación App-V, que cierra el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="b3a4d-491">La memoria caché local de la ubicación de AppData de roaming se comprime y se almacena en un archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="b3a4d-492">Se usa una marca de tiempo al final del proceso de empaquetado ZIP para asignarle un nombre al archivo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="b3a4d-493">La marca de hora se graba en el registro: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime como la última marca de hora de AppData conocidos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="b3a4d-494">El proceso de redireccionamiento de carpetas se llama para evaluar e iniciar el archivo ZIP cargado en el directorio AppData de roaming.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="b3a4d-495">La marca de tiempo se usa para determinar un escenario "gana el último escritor" si hay un conflicto y se usa para optimizar la descarga de los datos cuando se publica la aplicación de App-V o se inicia el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="b3a4d-496">El redireccionamiento de carpetas hará que los datos estén disponibles de cualquier otro cliente cubierto por la Directiva de soporte técnico e iniciará el proceso de almacenamiento de los datos de AppData\\Roaming en la ubicación local AppData en el cliente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="b3a4d-497">Los procesos detallados son:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="b3a4d-498">El usuario inicia el entorno virtual iniciando una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="b3a4d-499">El entorno virtual de la aplicación comprueba el archivo ZIP de marcado de hora más reciente, si está presente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="b3a4d-500">Se comprueba si el registro tiene la última marca de hora de carga conocida, si está presente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="b3a4d-501">Se descarga el archivo ZIP más reciente, a menos que la marca de hora de última carga conocida local sea mayor o igual que la marca de hora del archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="b3a4d-502">Si la marca de hora de la última carga conocida local es anterior a la del archivo ZIP más reciente en la ubicación de AppData de roaming, el archivo ZIP se extrae en el directorio temporal local del perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="b3a4d-503">Una vez que el archivo ZIP se haya extraído correctamente, se cambiará el nombre de la memoria caché local del directorio de AppData y los nuevos datos se trasladarán a su sitio.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="b3a4d-504">El directorio cuyo nombre ha cambiado se elimina y la aplicación se abre con los últimos datos de itinerancia que se han guardado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="b3a4d-505">Esto completa la itinerancia correcta de la configuración de la aplicación que está presente en las ubicaciones de AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="b3a4d-506">La única condición que debe solucionarse es una operación de reparación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="b3a4d-507">Los detalles del proceso son:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-507">The details of the process are:</span></span>

1.  <span data-ttu-id="b3a4d-508">Durante la reparación, detecte si la ruta al directorio de AppData de roaming del usuario no es local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="b3a4d-509">Los destinos de la ruta de acceso de protección contra roaming no local de AppData se recrean.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="b3a4d-510">Elimine la marca de hora almacenada en el registro, si está presente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="b3a4d-511">Este proceso volverá a crear las ubicaciones locales y de red de AppData y quitará el registro de registro de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="b3a4d-512">Administración del ciclo de vida de aplicaciones de cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="b3a4d-513">En una infraestructura completa de App-V, después de secuenciar las aplicaciones, se administran y publican en usuarios o equipos a través de los servidores de publicación y administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="b3a4d-514">En esta sección se detallan las operaciones que se producen durante las operaciones comunes del ciclo de vida de la aplicación de App-V (agregar, publicar, iniciar, actualizar y quitar), así como las ubicaciones de archivo y registro que se modifican y modifican desde la perspectiva del cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="b3a4d-515">Las operaciones de cliente de App-V se realizan como una serie de comandos de PowerShell iniciados en el equipo en el que se ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="b3a4d-516">Este documento se centra en las soluciones de infraestructura completa de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="b3a4d-517">Para obtener información específica sobre la integración de App-V con Configuration Manager 2012, visite: <https://go.microsoft.com/fwlink/?LinkId=392773> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="b3a4d-518">Las tareas de la aplicación App-V del ciclo de vida se desencadenan cuando el inicio de sesión del usuario (predeterminado), el inicio de la máquina o como operaciones de tiempo de fondo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="b3a4d-519">La configuración de las operaciones de cliente de App-V, incluidos los servidores de publicación, los intervalos de actualización, la habilitación del script de paquete y otras, se configura durante la configuración del cliente o después de la instalación con los comandos de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="b3a4d-520">Consulte la sección Cómo implementar el cliente en TechNet en: [cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md) o usar PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="b3a4d-521">Actualización de publicaciones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-521">Publishing refresh</span></span>

<span data-ttu-id="b3a4d-522">El proceso de actualización de publicaciones consta de varias operaciones más pequeñas que se realizan en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="b3a4d-523">Como App-V es una tecnología de virtualización de aplicaciones y no una tecnología de programación de tareas, el programador de tareas de Windows se usa para habilitar el proceso de inicio de sesión del usuario, el inicio del equipo y los intervalos programados.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="b3a4d-524">La configuración del cliente durante la instalación mencionada anteriormente es el método preferido al distribuir el cliente a un grupo grande de equipos con la configuración correcta.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="b3a4d-525">Estas opciones de configuración de cliente se pueden configurar con los siguientes cmdlets de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="b3a4d-526">**Add-AppVPublishingServer:** Configura el cliente con un servidor de publicación de App-V que proporciona paquetes de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="b3a4d-527">**Set-AppVPublishingServer:** Modifica la configuración actual del servidor de publicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="b3a4d-528">**Set-AppVClientConfiguration:** Modifica la configuración de los actuales para el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="b3a4d-529">**Sync-AppVPublishingServer:** Inicia manualmente un proceso de actualización de publicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="b3a4d-530">Esto también se usa en las tareas programadas creadas durante la configuración del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="b3a4d-531">El objetivo de las siguientes secciones es detallar las operaciones que se producen durante las distintas fases de una actualización de publicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="b3a4d-532">Los temas incluyen:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-532">The topics include:</span></span>

-   <span data-ttu-id="b3a4d-533">Agregar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="b3a4d-534">Publicar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="b3a4d-535">Agregar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-535">Adding an App-V package</span></span>

<span data-ttu-id="b3a4d-536">Agregar un paquete de App-V al cliente es el primer paso del proceso de actualización de la publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="b3a4d-537">El resultado final es el mismo que el `Add-AppVClientPackage` cmdlet en PowerShell, excepto durante el proceso de actualización de publicaciones, se Contacta con el servidor de publicación configurado y se devuelve una lista de aplicaciones de alto nivel al cliente para obtener información más detallada y no una sola operación de adición de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="b3a4d-538">El proceso continúa con la configuración del cliente para agregar o actualizar paquetes o de grupos de conexiones, a continuación, accede al archivo de appv.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="b3a4d-539">A continuación, el contenido del archivo de appv se expande y se coloca en el sistema operativo local en las ubicaciones adecuadas.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="b3a4d-540">A continuación se incluye un flujo de trabajo detallado del proceso, asumiendo que el paquete está configurado para la transmisión por secuencias de errores.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="b3a4d-541">Cómo agregar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="b3a4d-542">Inicio manual a través de PowerShell o la secuencia de tareas iniciada por el proceso de actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="b3a4d-543">El cliente de App-V realiza una conexión HTTP y solicita una lista de aplicaciones basada en el destino.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="b3a4d-544">El proceso de actualización de publicaciones admite equipos o usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="b3a4d-545">El servidor de publicación de App-V usa la identidad del destino de inicio, el usuario o el equipo, y consulta la base de datos para obtener una lista de las aplicaciones autorizadas.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="b3a4d-546">La lista de aplicaciones se proporciona como respuesta XML, que el cliente usa para enviar solicitudes adicionales al servidor para obtener más información sobre la base de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="b3a4d-547">El agente de publicación en el cliente de App-V realiza todas las acciones que se encuentran debajo de la serialización.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="b3a4d-548">Evalúe los grupos de conexión que estén sin publicar o deshabilitados, ya que las actualizaciones de la versión del paquete que forman parte del grupo de conexión no se pueden procesar.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="b3a4d-549">Configure los paquetes mediante la identificación de las operaciones de adición o actualización.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="b3a4d-550">El cliente de App-V usa la API de AppX de Windows y obtiene acceso al archivo de appv desde el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="b3a4d-551">El archivo de paquete se abre y los AppXManifest.xml y StreamMap.xml se descargan en el almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="b3a4d-552">Datos de bloques de publicación completamente definidos en el StreamMap.xml.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="b3a4d-553">Almacena los datos del bloque de publicación en el paquete Store\\PkgGUID\\VerGUID\\Root.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="b3a4d-554">Iconos: destinos de los puntos de extensión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="b3a4d-555">Encabezados ejecutables portables (encabezados PE): los destinos de los puntos de extensión que contienen la información base de la imagen que necesita en el disco, en el que se tiene acceso directamente o a través de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="b3a4d-556">Scripts: directorio de scripts de descarga para usar en todo el proceso de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="b3a4d-557">Rellenar el almacén de paquetes:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="b3a4d-558">Cree archivos dispersos en disco que representen el paquete extraído para cualquier directorio de la lista.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="b3a4d-559">Los directorios y archivos de nivel superior del escenario, en raíz.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="b3a4d-560">Todos los demás archivos se crean cuando el directorio se muestra como disperso en el disco y se transmite a petición.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="b3a4d-561">Cree las entradas del catálogo de equipos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-561">Create the machine catalog entries.</span></span> <span data-ttu-id="b3a4d-562">Cree el Manifest.xml y DeploymentConfiguration.xml a partir de los archivos de paquete (si no hay DeploymentConfiguration.xml archivo en el paquete creado un marcador de posición).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="b3a4d-563">Crear la ubicación del almacén de paquetes en el registro de HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span><span class="sxs-lookup"><span data-stu-id="b3a4d-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="b3a4d-564">Cree el archivo Registry. dat del almacén de paquetes en%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat</span><span class="sxs-lookup"><span data-stu-id="b3a4d-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="b3a4d-565">Registrar el paquete con el controlador de modo de núcleo de App-V HKLM\\Microsoft\\Software\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="b3a4d-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="b3a4d-566">Invoca el scripting desde el archivo AppxManifest.xml o DeploymentConfig.xml para agregar intervalos a los paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="b3a4d-567">Configure grupos de conexión agregando y habilitando o deshabilitando.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="b3a4d-568">Quitar objetos que no se publican en el destino (usuario o equipo).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="b3a4d-569">**Nota:**  Esto no hará una eliminación de paquete, sino que quitará los puntos de integración para el destino específico (usuario o equipo) y eliminará los archivos de catálogo de usuarios (archivos de catálogo de equipo para publicación global).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="b3a4d-570">Invoca el montaje de carga en segundo plano basado en la configuración del cliente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="b3a4d-571">Los paquetes que ya tienen información de publicación para el equipo o el usuario se restauran inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="b3a4d-572">**Nota:**  Esta condición se produce como un producto de desinstalación sin anular la publicación con la adición de fondo del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="b3a4d-573">Esto completa un paquete de App-V que agrega el proceso de actualización de la publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="b3a4d-574">El siguiente paso es publicar el paquete en el destino específico (equipo o usuario).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![paquete de adición de archivos y datos de registro](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="b3a4d-576">Publicar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-576">Publishing an App-V package</span></span>

<span data-ttu-id="b3a4d-577">Durante la operación de actualización de publicación, la operación de publicación específica (Publish-AppVClientPackage) agrega entradas al catálogo de usuarios, asigna derechos al usuario, identifica el almacén local y termina completando los pasos de integración.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="b3a4d-578">A continuación se muestran los pasos detallados.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="b3a4d-579">Cómo publicar y el paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="b3a4d-580">Las entradas de paquete se agregan al catálogo de usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="b3a4d-581">Paquetes dirigidos por el usuario: los UserDeploymentConfiguration.xml y UserManifest.xml se colocan en el equipo del catálogo de usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="b3a4d-582">Paquetes de destino de la máquina (global): el UserDeploymentConfiguration.xml se coloca en el catálogo de la máquina</span><span class="sxs-lookup"><span data-stu-id="b3a4d-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="b3a4d-583">Registrar el paquete con el controlador de modo de núcleo para el usuario en HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="b3a4d-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="b3a4d-584">Realizar tareas de integración.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="b3a4d-585">Crear puntos de extensión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-585">Create extension points.</span></span>

    2.  <span data-ttu-id="b3a4d-586">Almacene la información de copia de seguridad en el registro del usuario y en el perfil de itinerancia (accesos directos).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="b3a4d-587">**Nota:**  Esto habilita los puntos de extensión de restauración si el paquete no se ha publicado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="b3a4d-588">Ejecutar scripts destinados a intervalos de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="b3a4d-589">Publicar un paquete de App-V que forma parte de un grupo de conexiones es muy similar al proceso anterior.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="b3a4d-590">Para los grupos de conexión, la ruta de acceso que almacena la información de catálogo específica incluye PackageGroups como un elemento secundario del directorio del catálogo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="b3a4d-591">Revise la información del catálogo de usuarios y equipos para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-591">Review the machine and users catalog information above for details.</span></span>

![Agregar archivo y datos del registro: global](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="b3a4d-593">Inicio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-593">Application launch</span></span>

<span data-ttu-id="b3a4d-594">Después del proceso de actualización de la publicación, el usuario inicia y después vuelve a iniciar una aplicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="b3a4d-595">El proceso es muy simple y optimizado para iniciarse rápidamente con un mínimo de tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="b3a4d-596">El cliente de App-V comprueba la ruta de acceso al catálogo de usuarios para los archivos creados durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="b3a4d-597">Después de establecer los derechos para iniciar el paquete, el cliente de App-V crea un entorno virtual, comienza a transmitir los datos necesarios y aplica el manifiesto adecuado y los archivos de configuración de implementación durante la creación del entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="b3a4d-598">Con el entorno virtual creado y configurado para el paquete y la aplicación específicos, se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="b3a4d-599">Cómo iniciar aplicaciones de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="b3a4d-600">El usuario inicia la aplicación haciendo clic en un acceso directo o en una invocación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="b3a4d-601">El cliente de App-V comprueba la existencia en el catálogo de usuarios para los siguientes archivos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="b3a4d-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="b3a4d-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="b3a4d-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="b3a4d-604">Si los archivos están presentes, la aplicación tendrá derecho a ese usuario específico y la aplicación iniciará el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="b3a4d-605">No hay tráfico de red en este momento.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="b3a4d-606">A continuación, el cliente de App-V comprueba que la ruta de acceso del paquete registrada para el servicio de cliente de App-V se encuentre en el registro.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="b3a4d-607">Al encontrar la ruta de acceso al almacén de paquetes, se crea el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="b3a4d-608">Si este es el primer inicio, el bloque de características principal se descarga si está presente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="b3a4d-609">Después de la descarga, el servicio del cliente de App-V consume el manifiesto y los archivos de configuración de implementación para configurar el entorno virtual y se cargan todos los subsistemas de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="b3a4d-610">Se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-610">The Application launches.</span></span> <span data-ttu-id="b3a4d-611">Para los archivos que faltan en el almacén de paquetes (archivos dispersos), App-V enviará por error los archivos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![empaquetar Agregar archivo y datos del registro: secuencia](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="b3a4d-613">Actualización de un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-613">Upgrading an App-V package</span></span>

<span data-ttu-id="b3a4d-614">El proceso de actualización del paquete App-V 5 difiere de las versiones anteriores de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="b3a4d-615">App-V es compatible con varias versiones del mismo paquete en un equipo que tiene derecho a usuarios diferentes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="b3a4d-616">Las versiones del paquete se pueden agregar en cualquier momento, ya que el almacén y los catálogos del paquete se actualizan con los nuevos recursos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="b3a4d-617">El único proceso específico de la incorporación de nuevos recursos de versión es la optimización del almacenamiento de información.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="b3a4d-618">Durante una actualización, solo se agregan los nuevos archivos a la nueva ubicación del almacén de versiones y se crean vínculos físicos para los archivos que no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="b3a4d-619">Esto reduce el almacenamiento general al presentar el archivo en una ubicación del disco y, a continuación, proyectarlo en todas las carpetas con una entrada de ubicación del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="b3a4d-620">Los detalles específicos de la actualización de un paquete de App-V son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="b3a4d-621">Cómo actualizar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="b3a4d-622">El cliente de App-V realiza una actualización de publicación y detecta una versión más reciente de un paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="b3a4d-623">Las entradas de paquete se agregan al catálogo correspondiente para la nueva versión</span><span class="sxs-lookup"><span data-stu-id="b3a4d-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="b3a4d-624">Paquetes dirigidos por el usuario: los UserDeploymentConfiguration.xml y UserManifest.xml se colocan en el equipo del catálogo de usuarios en appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="b3a4d-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="b3a4d-625">Paquetes de destino de la máquina (global): el UserDeploymentConfiguration.xml se coloca en el catálogo de máquina en%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="b3a4d-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="b3a4d-626">Registrar el paquete con el controlador de modo de núcleo para el usuario en HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="b3a4d-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="b3a4d-627">Realizar tareas de integración.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="b3a4d-628">Integre puntos de extensión (EP) desde el manifiesto y los archivos de configuración dinámica.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="b3a4d-629">Los datos de EP basados en archivos se almacenan en la carpeta AppData con puntos de unión del almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="b3a4d-630">La versión 1 de EPs ya existe cuando hay una nueva versión disponible.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="b3a4d-631">Los puntos de extensión se cambian a la ubicación de la versión 2 en los catálogos de usuario o de equipo para los puntos de extensión nuevos o actualizados.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="b3a4d-632">Ejecutar scripts destinados a intervalos de publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="b3a4d-633">Instale los ensamblados en paralelo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="b3a4d-634">Actualización de un paquete de App-V en uso</span><span class="sxs-lookup"><span data-stu-id="b3a4d-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="b3a4d-635">A **partir de App-V 5 SP2**: Si intenta actualizar un paquete que está usando un usuario final, la tarea de actualización se coloca en un estado pendiente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="b3a4d-636">La actualización se ejecutará más tarde, de acuerdo con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-637">Tipo de tarea</span><span class="sxs-lookup"><span data-stu-id="b3a4d-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-638">Regla aplicable</span><span class="sxs-lookup"><span data-stu-id="b3a4d-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-639">Tarea basada en el usuario, por ejemplo, publicar un paquete para un usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-640">La tarea pendiente se realizará después de que el usuario cierre sesión y vuelva a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-641">Tarea basada en todo el mundo, por ejemplo, habilitar globalmente un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="b3a4d-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-642">La tarea pendiente se realizará cuando el equipo se cierre y se reinicie.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b3a4d-643">Cuando una tarea se coloca en un estado pendiente, el cliente de App-V también genera una clave del registro para la tarea pendiente de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-644">Tarea basada en usuarios o en todo el mundo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-645">Dónde se genera la clave del registro</span><span class="sxs-lookup"><span data-stu-id="b3a4d-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-646">Tareas basadas en usuarios</span><span class="sxs-lookup"><span data-stu-id="b3a4d-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-647">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="b3a4d-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-648">Tareas basadas en todo el mundo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-649">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="b3a4d-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b3a4d-650">Las siguientes operaciones deben completarse para que los usuarios puedan usar la versión más reciente del paquete:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-651">Tarea</span><span class="sxs-lookup"><span data-stu-id="b3a4d-651">Task</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-652">Detalles</span><span class="sxs-lookup"><span data-stu-id="b3a4d-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-653">Agregar el paquete al equipo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-654">Esta tarea es específica del equipo y puede realizarla en cualquier momento completando los pasos de la sección anterior Agregar paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-655">Publicar el paquete</span><span class="sxs-lookup"><span data-stu-id="b3a4d-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-656">Consulte la sección de publicación de paquetes anterior para conocer los pasos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="b3a4d-657">Este proceso requiere que se actualicen los puntos de extensión en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="b3a4d-658">Los usuarios finales no pueden estar usando la aplicación al completar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b3a4d-659">Use los siguientes escenarios de ejemplo como guía para actualizar paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-660">Escenario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-661">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-662">El paquete de App-V no se usa cuando intenta actualizar</span><span class="sxs-lookup"><span data-stu-id="b3a4d-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-663">Ninguno de los siguientes componentes del paquete puede estar en uso: aplicación virtual, servidor COM o extensiones de Shell.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="b3a4d-664">El administrador publica una versión más reciente del paquete y la actualización funciona la próxima vez que se inicie un componente o una aplicación dentro del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="b3a4d-665">La nueva versión del paquete se transmite y se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="b3a4d-666">No ha cambiado nada en este escenario en App-V 5 SP2 de las versiones anteriores de App-V 5.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-667">El paquete de App-V se está usando cuando el administrador publica una versión más reciente del paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-668">La operación de actualización se establece en pendiente por el cliente de App-V, lo que significa que está en cola y se ejecuta más tarde cuando el paquete no está en uso.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="b3a4d-669">Si la aplicación de paquete está en uso, el usuario cierra la aplicación virtual, después de la cual se puede realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="b3a4d-670">Si el paquete tiene extensiones de Shell (Office 2013), que el explorador de Windows carga permanentemente, el usuario no puede iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="b3a4d-671">Los usuarios deben cerrar sesión y volver a iniciar sesión para iniciar la actualización del paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b3a4d-672">Publicación de usuarios global vs</span><span class="sxs-lookup"><span data-stu-id="b3a4d-672">Global vs user publishing</span></span>

<span data-ttu-id="b3a4d-673">Los paquetes de App-V se pueden publicar de una de dos maneras: Usuario que da derecho a un paquete de App-V a un usuario o grupo de usuarios específico y global que da derecho al paquete de App-V a todo el equipo para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="b3a4d-674">Una vez que haya una actualización de paquete pendiente y el paquete App-V no se esté usando, considere los dos tipos de publicación:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="b3a4d-675">**Publicado globalmente**: la aplicación se publica en un equipo; todos los usuarios de ese equipo pueden usarla.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="b3a4d-676">La actualización se producirá cuando se inicie el servicio de cliente de App-V, lo que significa que el equipo se reiniciará de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="b3a4d-677">**Usuario publicado**: la aplicación se publica para un usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="b3a4d-678">Si hay varios usuarios en el equipo, la aplicación se puede publicar en un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="b3a4d-679">La actualización se producirá cuando el usuario inicie sesión o cuando se publique de nuevo (periódicamente, la actualización y evaluación de directivas de ConfigMgr, o una publicación periódica de App-V o la actualización o explícitamente a través de los comandos de PowerShell).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="b3a4d-680">Quitar un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-680">Removing an App-V package</span></span>

<span data-ttu-id="b3a4d-681">Quitar aplicaciones de App-V en una infraestructura completa es una operación de anulación de la publicación y no realiza una eliminación de paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="b3a4d-682">El proceso es el mismo que el proceso de publicación anterior, pero en lugar de agregar el proceso de eliminación, se invierten los cambios realizados para los paquetes de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="b3a4d-683">Reparación de un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-683">Repairing an App-V package</span></span>

<span data-ttu-id="b3a4d-684">La operación de reparación es muy sencilla pero puede afectar a muchas ubicaciones de la máquina.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="b3a4d-685">Las ubicaciones de copia en escritura (COW) mencionadas anteriormente se eliminan y los puntos de extensión se integran y se vuelven a integrar.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="b3a4d-686">Revise las ubicaciones de colocación de datos de la vaca revisando dónde se encuentran registradas en el registro.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="b3a4d-687">Esta operación se realiza automáticamente y no hay ningún control administrativo distinto de iniciar una operación de reparación desde la consola del cliente de App-V o mediante PowerShell (Repair-AppVClientPackage).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="b3a4d-688">Integración de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="b3a4d-688">Integration of App-V packages</span></span>


<span data-ttu-id="b3a4d-689">El cliente de App-V y la arquitectura de paquetes proporcionan una integración específica con el sistema operativo local durante la adición y publicación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="b3a4d-690">Tres archivos definen la integración o los puntos de extensión para un paquete de App-V:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="b3a4d-691">AppXManifest.xml: se almacena dentro del paquete con copias de reserva almacenadas en el almacén de paquetes y el perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="b3a4d-692">Contiene las opciones creadas durante el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="b3a4d-693">DeploymentConfig.xml: proporciona información de configuración de puntos de extensión de integración basados en equipos y usuarios.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="b3a4d-694">UserConfig.xml: un subconjunto de la Deploymentconfig.xml que solo proporciona configuraciones basadas en el usuario y solo tiene como destino puntos de extensión basados en el usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="b3a4d-695">Reglas de integración</span><span class="sxs-lookup"><span data-stu-id="b3a4d-695">Rules of integration</span></span>

<span data-ttu-id="b3a4d-696">Cuando se publican aplicaciones de App-V en un equipo con el cliente de App-V, se realizarán algunas acciones específicas, tal como se describe en la siguiente lista:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="b3a4d-697">Publicación global: los accesos directos se almacenan en la ubicación del perfil todos los usuarios y otros puntos de extensión se almacenan en el registro en el subárbol HKLM.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="b3a4d-698">Publicación de usuarios: los accesos directos se almacenan en el perfil de la cuenta de usuario actual y otros puntos de extensión se almacenan en el registro en el subárbol HKCU.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="b3a4d-699">Copia de seguridad y restauración: se realiza una copia de seguridad de los datos y el registro de la aplicación nativa (como los registros FTA) durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="b3a4d-700">Los paquetes de App-V reciben la propiedad basada en el último paquete integrado en el que la propiedad se pasa a la nueva aplicación de App-V publicada.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="b3a4d-701">La propiedad se transfiere de un paquete de App-V a otro cuando se anula la publicación del paquete App-V propietario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="b3a4d-702">Esto no iniciará una restauración de los datos o del registro.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="b3a4d-703">Restaure los datos de copia de seguridad cuando el último paquete no se haya publicado o eliminado por cada extensión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="b3a4d-704">Puntos de extensión</span><span class="sxs-lookup"><span data-stu-id="b3a4d-704">Extension points</span></span>

<span data-ttu-id="b3a4d-705">Los archivos de publicación de App-V (manifiesto y configuración dinámica) proporcionan varios puntos de extensión que permiten que la aplicación se integre con el sistema operativo local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="b3a4d-706">Estos puntos de extensión realizan tareas típicas de instalación de aplicaciones, como la colocación de accesos directos, la creación de asociaciones de tipos de archivo y el registro de componentes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="b3a4d-707">Ya que se trata de aplicaciones virtualizadas que no se instalan de la misma manera en una aplicación tradicional, existen algunas diferencias.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="b3a4d-708">A continuación se muestra una lista de los puntos de extensión descritos en esta sección:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="b3a4d-709">Abreviados</span><span class="sxs-lookup"><span data-stu-id="b3a4d-709">Shortcuts</span></span>

-   <span data-ttu-id="b3a4d-710">Asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-710">File Type Associations</span></span>

-   <span data-ttu-id="b3a4d-711">Extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="b3a4d-711">Shell Extensions</span></span>

-   <span data-ttu-id="b3a4d-712">COM</span><span class="sxs-lookup"><span data-stu-id="b3a4d-712">COM</span></span>

-   <span data-ttu-id="b3a4d-713">Clientes de software</span><span class="sxs-lookup"><span data-stu-id="b3a4d-713">Software Clients</span></span>

-   <span data-ttu-id="b3a4d-714">Capacidades de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-714">Application capabilities</span></span>

-   <span data-ttu-id="b3a4d-715">Controlador de protocolo URL</span><span class="sxs-lookup"><span data-stu-id="b3a4d-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="b3a4d-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="b3a4d-716">AppPath</span></span>

-   <span data-ttu-id="b3a4d-717">Aplicación virtual</span><span class="sxs-lookup"><span data-stu-id="b3a4d-717">Virtual Application</span></span>

### <span data-ttu-id="b3a4d-718">Abreviados</span><span class="sxs-lookup"><span data-stu-id="b3a4d-718">Shortcuts</span></span>

<span data-ttu-id="b3a4d-719">El corto corte es uno de los elementos básicos de integración con el sistema operativo y es la interfaz para iniciar directamente el usuario de una aplicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="b3a4d-720">Durante la publicación y la anulación de la publicación de aplicaciones de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="b3a4d-721">Desde el manifiesto del paquete y los archivos XML de configuración dinámica, la ruta de acceso a un ejecutable de la aplicación específica puede encontrarse en una sección similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="b3a4d-722">Como se mencionó anteriormente, los accesos directos de App-V se colocan de forma predeterminada en el perfil del usuario en función de la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="b3a4d-723">La actualización global coloca los accesos directos en el perfil todos los usuarios y la actualización de usuario los almacena en el perfil del usuario específico.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="b3a4d-724">El ejecutable real se almacena en el almacén de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="b3a4d-725">La ubicación del archivo ICO es una ubicación con tokens en el paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="b3a4d-726">Asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-726">File type associations</span></span>

<span data-ttu-id="b3a4d-727">El cliente de App-V administra las asociaciones de tipos de archivo del sistema operativo local durante la publicación, lo que permite a los usuarios usar invocaciones de tipo de archivo o abrir un archivo con una extensión registrada específicamente (. docx) para iniciar una aplicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="b3a4d-728">Las asociaciones de tipo de archivo están presentes en el manifiesto y los archivos de configuración dinámico, tal como se representa en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="b3a4d-729">**Nota:**  En este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="b3a4d-730">es la extensión</span><span class="sxs-lookup"><span data-stu-id="b3a4d-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="b3a4d-731">es el valor ProgId (que apunta al identificador de programa (ProgId) adyacente)</span><span class="sxs-lookup"><span data-stu-id="b3a4d-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="b3a4d-732">es la línea de comandos, que señala al archivo ejecutable de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="b3a4d-733">Extensiones de Shell de :</span><span class="sxs-lookup"><span data-stu-id="b3a4d-733">Shell extensions</span></span>

<span data-ttu-id="b3a4d-734">Las extensiones de Shell se incrustan automáticamente en el paquete durante el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="b3a4d-735">Cuando el paquete se publica globalmente, la extensión de Shell proporciona a los usuarios la misma funcionalidad que si la aplicación se instalara de forma local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="b3a4d-736">La aplicación no requiere ninguna configuración ni configuración adicional en el cliente para habilitar la funcionalidad de la extensión de Shell.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="b3a4d-737">Requisitos para usar extensiones de Shell:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="b3a4d-738">Los paquetes que contienen extensiones de Shell insertadas deben publicarse globalmente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="b3a4d-739">El "bits" de la aplicación, el secuenciador y el cliente de App-V deben coincidir, o las extensiones de Shell no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="b3a4d-740">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-740">For example:</span></span>

    -   <span data-ttu-id="b3a4d-741">La versión de la aplicación es 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="b3a4d-742">El secuenciador se está ejecutando en un equipo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="b3a4d-743">El paquete se está entregando a un equipo cliente de aplicación de 64 bits de-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="b3a4d-744">En la siguiente tabla se muestran las extensiones de Shell compatibles.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-745">Administrador</span><span class="sxs-lookup"><span data-stu-id="b3a4d-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-746">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a4d-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-747">Controlador del menú contextual</span><span class="sxs-lookup"><span data-stu-id="b3a4d-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-748">Agrega elementos de menú al menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="b3a4d-749">Se llama antes de mostrar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-750">Controlador de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="b3a4d-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-751">Controla la acción que se muestra al hacer clic con el botón secundario y modificar el menú contextual que aparece.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-752">Controlador de destino de colocación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-753">Controla la acción después de arrastrar y colocar un objeto de datos en un destino de colocación, como un archivo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-754">Controlador de objetos de datos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-755">Controla la acción después de copiar un archivo en el portapapeles o de arrastrarlo y colocarlo sobre un destino.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="b3a4d-756">Puede proporcionar formatos adicionales del portapapeles para el destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-757">Controlador de hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="b3a4d-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-758">Reemplaza o agrega páginas al cuadro de diálogo de la hoja de propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-759">Controlador de insugerencias</span><span class="sxs-lookup"><span data-stu-id="b3a4d-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-760">Permite recuperar los indicadores y la información de recuadro para un elemento y mostrarlo dentro de una información sobre herramientas emergente al mantener el mouse.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-761">Controlador de columnas</span><span class="sxs-lookup"><span data-stu-id="b3a4d-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-762">Permite crear y mostrar columnas personalizadas en la vista de detalles del explorador de Windows <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="b3a4d-763">Puede usarse para ampliar la ordenación y la agrupación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-764">Controlador de vista previa</span><span class="sxs-lookup"><span data-stu-id="b3a4d-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-765">Habilita una vista previa de un archivo para que se muestre en el panel de vista previa del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b3a4d-766">COM</span><span class="sxs-lookup"><span data-stu-id="b3a4d-766">COM</span></span>

<span data-ttu-id="b3a4d-767">El cliente de App-V admite aplicaciones de publicación compatibles con la integración COM y la virtualización.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="b3a4d-768">La integración COM permite al cliente de App-V registrar objetos COM en el sistema operativo local y en la virtualización de los objetos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="b3a4d-769">A los fines de este documento, la integración de objetos COM requiere más detalles.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="b3a4d-770">App-V admite el registro de objetos COM desde el paquete al sistema operativo local con dos tipos de proceso: fuera de proceso y en proceso.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="b3a4d-771">El registro de objetos COM se realiza con una o una combinación de varios modos de funcionamiento para un paquete de App-V específico que incluye apagado, aislamiento e integrado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="b3a4d-772">El modo integrado se configura para el tipo fuera de proceso o en proceso.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="b3a4d-773">La configuración de los tipos y modos COM se realiza con los archivos de configuración dinámica (deploymentconfig.xml o userconfig.xml).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="b3a4d-774">Los detalles de la integración de App-V están disponibles en: <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="b3a4d-775">Características de aplicaciones y clientes de software</span><span class="sxs-lookup"><span data-stu-id="b3a4d-775">Software clients and application capabilities</span></span>

<span data-ttu-id="b3a4d-776">App-V es compatible con clientes de software específicos y puntos de extensión de funciones de aplicaciones que permiten que las aplicaciones virtualizadas se registren con el cliente de software del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="b3a4d-777">Esto permite a los usuarios seleccionar programas predeterminados para operaciones como el correo electrónico, la mensajería instantánea y el reproductor multimedia.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="b3a4d-778">Esta operación se realiza en el panel de control con configurar acceso y programas predeterminados en el equipo, y configurado durante la secuenciación en el manifiesto o los archivos de configuración dinámica.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="b3a4d-779">Las funciones de la aplicación solo se admiten cuando las aplicaciones de App-V se publican globalmente.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="b3a4d-780">Ejemplo de registro de clientes de software de un cliente de correo basado en App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="b3a4d-781">**Nota:**  En este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="b3a4d-782">es la configuración general de los clientes de software para integrar clientes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="b3a4d-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="b3a4d-783">es la bandera para establecer un cliente de correo electrónico determinado como cliente de correo electrónico predeterminado</span><span class="sxs-lookup"><span data-stu-id="b3a4d-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="b3a4d-784">es el registro de dll MAPI</span><span class="sxs-lookup"><span data-stu-id="b3a4d-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="b3a4d-785">Controlador de protocolo URL</span><span class="sxs-lookup"><span data-stu-id="b3a4d-785">URL Protocol handler</span></span>

<span data-ttu-id="b3a4d-786">Las aplicaciones no siempre se denominan específicamente aplicaciones virtualizadas mediante la invocación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="b3a4d-787">Para, por ejemplo, en una aplicación que admite la incrustación de un vínculo mailto: dentro de un documento o una página web, el usuario hace clic en un vínculo mailto: y espera obtener su cliente de correo registrado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="b3a4d-788">App-V es compatible con los controladores de protocolo URL que se pueden registrar por paquete con el sistema operativo local.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="b3a4d-789">Durante la secuenciación, los controladores de protocolo URL se agregan automáticamente al paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="b3a4d-790">En situaciones en las que hay más de una aplicación que puede registrar el controlador de protocolo de dirección URL específico, los archivos de configuración dinámica se pueden usar para modificar el comportamiento y suprimir o deshabilitar esta característica para una aplicación que no debe ser la aplicación principal iniciada.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="b3a4d-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="b3a4d-791">AppPath</span></span>

<span data-ttu-id="b3a4d-792">El punto de extensión AppPath admite la llamada a aplicaciones de App-V directamente desde el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="b3a4d-793">Esto se realiza normalmente desde la pantalla de ejecución o de inicio, según el sistema operativo, lo que permite a los administradores proporcionar acceso a aplicaciones de App-V desde scripts o comandos del sistema operativo sin llamar a la ruta de acceso específica del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="b3a4d-794">Por lo tanto, evita modificar la variable de entorno PATH del sistema en todos los sistemas, ya que se realiza durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="b3a4d-795">El punto de extensión AppPath se configura en el manifiesto o en los archivos de configuración dinámica y se almacena en el registro del equipo local durante la publicación para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="b3a4d-796">Para obtener más información sobre la revisión de AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .</span><span class="sxs-lookup"><span data-stu-id="b3a4d-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="b3a4d-797">Aplicación virtual</span><span class="sxs-lookup"><span data-stu-id="b3a4d-797">Virtual application</span></span>

<span data-ttu-id="b3a4d-798">Este subsistema proporciona una lista de las aplicaciones capturadas durante la secuenciación, que suelen consumir otros componentes de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="b3a4d-799">La integración de puntos de extensión que pertenecen a una aplicación en particular se puede deshabilitar mediante archivos de configuración dinámica.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="b3a4d-800">Por ejemplo, si un paquete contiene dos aplicaciones, es posible deshabilitar todos los puntos de extensión que pertenecen a una aplicación para permitir únicamente la integración de puntos de extensión de otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="b3a4d-801">Reglas de punto de extensión</span><span class="sxs-lookup"><span data-stu-id="b3a4d-801">Extension point rules</span></span>

<span data-ttu-id="b3a4d-802">Los puntos de extensión descritos anteriormente se integran en el sistema operativo en función de la publicación de los paquetes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="b3a4d-803">La publicación global coloca puntos de extensión en ubicaciones de máquinas públicas, donde la publicación de usuarios coloca puntos de extensión en ubicaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="b3a4d-804">Por ejemplo, un acceso directo creado en el escritorio y publicado globalmente tendrá como resultado los datos de archivo del acceso directo (%Public%\\Desktop) y los datos del registro (HKLM\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="b3a4d-805">El mismo método abreviado tendría datos de archivo (%UserProfile%\\Desktop) y datos del registro (HKCU\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="b3a4d-806">Los puntos de extensión no se publican de la misma manera, ya que algunos puntos de extensión requerirán la publicación global y otros requieren una secuencia en el sistema operativo y la arquitectura específicos donde se entregan.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="b3a4d-807">A continuación se muestra una tabla que describe estas dos reglas clave.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3a4d-808">Extensión virtual</span><span class="sxs-lookup"><span data-stu-id="b3a4d-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-809">Requiere la secuencia de los SO de destino</span><span class="sxs-lookup"><span data-stu-id="b3a4d-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="b3a4d-810">Requiere publicación global</span><span class="sxs-lookup"><span data-stu-id="b3a4d-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-811">Método abreviado</span><span class="sxs-lookup"><span data-stu-id="b3a4d-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-812">Asociación de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-813">Protocolos URL</span><span class="sxs-lookup"><span data-stu-id="b3a4d-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-814">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="b3a4d-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-816">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-817">Modo COM</span><span class="sxs-lookup"><span data-stu-id="b3a4d-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-818">Cliente de software</span><span class="sxs-lookup"><span data-stu-id="b3a4d-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-819">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-820">Capacidades de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-821">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-822">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-823">Controlador del menú contextual</span><span class="sxs-lookup"><span data-stu-id="b3a4d-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-824">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-825">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-826">Controlador de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="b3a4d-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-827">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-828">Controlador de objetos de datos</span><span class="sxs-lookup"><span data-stu-id="b3a4d-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-829">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-830">Controlador de hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="b3a4d-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-831">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-832">Controlador de insugerencias</span><span class="sxs-lookup"><span data-stu-id="b3a4d-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-833">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-834">Controlador de columnas</span><span class="sxs-lookup"><span data-stu-id="b3a4d-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-835">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-836">Extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="b3a4d-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-837">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3a4d-838">Objeto auxiliar del explorador</span><span class="sxs-lookup"><span data-stu-id="b3a4d-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-839">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-840">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3a4d-841">Objeto X activo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-842">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3a4d-843">X</span><span class="sxs-lookup"><span data-stu-id="b3a4d-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="b3a4d-844">Procesamiento de configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="b3a4d-844">Dynamic configuration processing</span></span>


<span data-ttu-id="b3a4d-845">Implementar paquetes de App-V en un equipo o usuario es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="b3a4d-846">Sin embargo, a medida que las organizaciones implementan aplicaciones de AppV a través de líneas empresariales y límites políticos y geográficos, la capacidad de secuenciar una aplicación una vez con un conjunto de configuraciones es imposible.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="b3a4d-847">App-V se diseñó para este escenario, ya que captura configuraciones y configuraciones específicas durante la secuenciación en el archivo de manifiesto, pero también admite la modificación con archivos de configuración dinámica.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="b3a4d-848">La configuración dinámica de App-V permite especificar una directiva para un paquete, ya sea en el nivel de equipo o en el nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="b3a4d-849">Los archivos de configuración dinámica permiten a los ingenieros de secuenciación modificar la configuración de un paquete, postsecuenciación, para satisfacer las necesidades de grupos individuales de usuarios o equipos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="b3a4d-850">En algunos casos, puede que sea necesario realizar modificaciones en la aplicación para proporcionar la funcionalidad adecuada en el entorno de App-V.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="b3a4d-851">Por ejemplo, puede que sea necesario realizar modificaciones en los archivos \ _ \ \* config.xml para permitir que se realicen determinadas acciones en un momento determinado durante la ejecución de la aplicación, como deshabilitar una extensión mailto para evitar que una aplicación virtualizada sobrescriba esa extensión de otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="b3a4d-852">Los paquetes de App-V contienen el archivo de manifiesto dentro del archivo de paquete de appv, que es representativo de las operaciones de secuencia y es la política de elección a menos que los archivos de configuración dinámica se asignen a un paquete específico.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="b3a4d-853">Después de la secuenciación, los archivos de configuración dinámica se pueden modificar para permitir la publicación de una aplicación en diferentes escritorios o usuarios con diferentes puntos de extensión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="b3a4d-854">Los dos archivos de configuración dinámica son los archivos de configuración de implementación dinámica (DDC) y de configuración de usuario dinámica (DUC).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="b3a4d-855">Esta sección se centra en la combinación del manifiesto y los archivos de configuración dinámica.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="b3a4d-856">Ejemplo de archivos de configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="b3a4d-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="b3a4d-857">En el ejemplo siguiente se muestra la combinación del manifiesto, la configuración de implementación y los archivos de configuración de usuario después de la publicación y durante el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="b3a4d-858">Estos ejemplos son ejemplos abreviados de cada uno de los archivos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="b3a4d-859">El propósito es mostrar la combinación de los archivos únicamente y no ser una descripción completa de las categorías específicas disponibles en cada uno de los archivos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="b3a4d-860">Para obtener más información, consulte la guía de secuenciación de App-V 5 en:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="b3a4d-861">Manifiesta</span><span class="sxs-lookup"><span data-stu-id="b3a4d-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="b3a4d-862">Configuración de la implementación</span><span class="sxs-lookup"><span data-stu-id="b3a4d-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="b3a4d-863">Configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="b3a4d-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="b3a4d-864">Ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="b3a4d-864">Side-by-side assemblies</span></span>


<span data-ttu-id="b3a4d-865">App-V es compatible con el empaquetado automático de ensamblados en paralelo (SxS) durante la secuenciación y la implementación en el cliente durante la publicación de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="b3a4d-866">App-V SP2 admite la captura de ensamblados SxS durante la secuenciación para los ensamblados que no están presentes en el equipo de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="b3a4d-867">Y para los ensamblados compuestos de Visual C++ (versión 8 y posterior) o de tiempo de ejecución de MSXML, el secuenciador detectará y capturará automáticamente estas dependencias incluso si no se instalaron durante la supervisión.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="b3a4d-868">La característica de ensamblados en paralelo elimina las limitaciones de las versiones anteriores de App-V, donde el secuenciador de App-V no captura los ensamblados que ya están presentes en la estación de trabajo de secuenciación, y la protección de los ensamblados que se limita a una versión de bit por paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="b3a4d-869">Este comportamiento dio lugar a que los clientes de aplicaciones de App-V implementaran los ensamblados SxS obligatorios, lo que provocaba errores de inicio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="b3a4d-870">Esto forzó el proceso de empaquetado para documentar y, a continuación, asegurarse de que todos los ensamblados necesarios para los paquetes se instalaron de forma local en el sistema operativo cliente del usuario para asegurar la compatibilidad con las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="b3a4d-871">Según el número de ensamblados y la falta de documentación de la aplicación para las dependencias obligatorias, esta tarea era un desafío de administración e implementación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="b3a4d-872">El soporte de ensamblado en paralelo en App-V tiene las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="b3a4d-873">Capturas automáticas de ensamblado SxS durante la secuenciación, independientemente de si el ensamblado ya se ha instalado en la estación de trabajo de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="b3a4d-874">El cliente de App-V instala automáticamente los ensamblados SxS obligatorios en el equipo cliente en el momento de la publicación cuando no están presentes.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="b3a4d-875">El secuenciador informa de la dependencia en tiempo de ejecución de VC en el mecanismo de informes SPRJ.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="b3a4d-876">El secuenciador permite optar por no empaquetar los ensamblados que ya están instalados en el secuenciador y los escenarios en los que se hayan instalado previamente los ensamblados en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="b3a4d-877">Publicación automática de ensamblados SxS</span><span class="sxs-lookup"><span data-stu-id="b3a4d-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="b3a4d-878">Durante la publicación de un paquete de App-V con ensamblajes SxS, el cliente de App-V verificará la presencia del ensamblado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="b3a4d-879">Si el ensamblado no existe, el cliente implementará el ensamblado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="b3a4d-880">Los paquetes que forman parte de grupos de conexión dependerán de las instalaciones de ensamblado en paralelo que forman parte de los paquetes básicos, ya que el grupo de conexión no contiene información sobre la instalación del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="b3a4d-881">**Nota:**  Al anular la publicación o quitar un paquete con un ensamblado, no se quitan los ensamblados de ese paquete.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="b3a4d-882">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="b3a4d-882">Client logging</span></span>


<span data-ttu-id="b3a4d-883">El cliente de App-V registra información en el registro de eventos de Windows en el formato ETW estándar.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="b3a4d-884">Los eventos de App-V específicos pueden encontrarse en el visor de eventos, en aplicaciones y servicios Logs\\Microsoft\\AppV\\Client.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="b3a4d-885">**Nota:**  En App-V 5,0 SP3, se han consolidado algunos registros y se han movido a la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="b3a4d-885">**Note** In App-V 5.0 SP3, some logs have been consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="b3a4d-886">Para obtener una lista de los registros que se han movido, consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="b3a4d-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="b3a4d-887">A continuación se describen tres categorías específicas de eventos.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="b3a4d-888">**Administrador**: registra eventos de configuración que se aplican al cliente de App-V y contiene las advertencias y errores principales.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="b3a4d-889">**Operativo**: registra la ejecución general de App-v y el uso de componentes individuales creando un registro de auditoría de las operaciones de App-v que se completaron en el cliente de App-v.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="b3a4d-890">**Aplicación virtual**: registra la aplicación virtual y el uso de subsistemas de virtualización.</span><span class="sxs-lookup"><span data-stu-id="b3a4d-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 





