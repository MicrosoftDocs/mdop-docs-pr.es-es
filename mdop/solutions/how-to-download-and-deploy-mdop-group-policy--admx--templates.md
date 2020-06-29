---
title: Cómo descargar e implementar plantillas (.admx) de la directiva de grupo de MDOP
description: Cómo descargar e implementar plantillas (.admx) de la directiva de grupo de MDOP
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826920"
---
# <span data-ttu-id="80b1d-103">Cómo descargar e implementar plantillas (.admx) de la directiva de grupo de MDOP</span><span class="sxs-lookup"><span data-stu-id="80b1d-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="80b1d-104">Puede administrar la configuración de características de ciertas tecnologías de Microsoft Desktop Optimization Pack (MDOP) (por ejemplo, App-V, UE-V o MBAM) mediante plantillas de directiva de grupo, los archivos. ADMX y. ADML.</span><span class="sxs-lookup"><span data-stu-id="80b1d-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="80b1d-105">Las plantillas de directiva de grupo de MDOP están disponibles para su descarga en un archivo comprimido autoextraíble, agrupado por tecnología y versión.</span><span class="sxs-lookup"><span data-stu-id="80b1d-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="80b1d-106">Plantillas de directiva de grupo de MDOP</span><span class="sxs-lookup"><span data-stu-id="80b1d-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="80b1d-107">Cómo descargar e implementar las plantillas de directiva de grupo de MDOP</span><span class="sxs-lookup"><span data-stu-id="80b1d-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="80b1d-108">Descargar las [plantillas de directiva de grupo de MDOP](https://www.microsoft.com/download/details.aspx?id=55531) más recientes</span><span class="sxs-lookup"><span data-stu-id="80b1d-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="80b1d-109">Expanda el archivo. cab descargado ejecutando</span><span class="sxs-lookup"><span data-stu-id="80b1d-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="80b1d-110">Advertencia</span><span class="sxs-lookup"><span data-stu-id="80b1d-110">Warning</span></span>**  
   <span data-ttu-id="80b1d-111">No extraiga las plantillas directamente en el directorio de implementación de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="80b1d-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="80b1d-112">En este archivo se incluyen varias tecnologías y versiones.</span><span class="sxs-lookup"><span data-stu-id="80b1d-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="80b1d-113">En la carpeta extraída, busque el archivo. ADMX de la versión Technology.</span><span class="sxs-lookup"><span data-stu-id="80b1d-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="80b1d-114">Algunas tecnologías de MDOP tienen varios conjuntos de objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="80b1d-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="80b1d-115">Por ejemplo, MBAM incluye configuración de administración de MBAM y MBAM configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="80b1d-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="80b1d-116">Busque el archivo. ADML correspondiente por idioma-referencia cultural (es decir, *en-* es para inglés-Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="80b1d-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="80b1d-117">Copie los archivos. ADMX y. ADML en una carpeta de definición de directiva.</span><span class="sxs-lookup"><span data-stu-id="80b1d-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="80b1d-118">Según dónde almacene las plantillas, puede configurar opciones de directiva de grupo desde el dispositivo local o desde cualquier equipo del dominio.</span><span class="sxs-lookup"><span data-stu-id="80b1d-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="80b1d-119">**Archivos locales:** Para configurar las opciones de directiva de grupo desde el dispositivo local, copie los archivos de plantilla en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="80b1d-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="80b1d-120">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="80b1d-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="80b1d-121">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="80b1d-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="80b1d-122">Plantilla de directiva de grupo (. admx)</span><span class="sxs-lookup"><span data-stu-id="80b1d-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="80b1d-123">&lt;&gt;policyDefinitions fuerte</span><span class="sxs-lookup"><span data-stu-id="80b1d-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="80b1d-124">Archivo de idioma de directiva de grupo (. ADML)</span><span class="sxs-lookup"><span data-stu-id="80b1d-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="80b1d-125">&lt;&gt;policyDefinitions fuerte</span><span class="sxs-lookup"><span data-stu-id="80b1d-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="80b1d-126">**Almacén central del dominio:** Para habilitar la configuración de directiva de grupo de un administrador de directivas de grupo desde cualquier equipo del dominio, copie los archivos a las siguientes ubicaciones del controlador de dominio:</span><span class="sxs-lookup"><span data-stu-id="80b1d-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="80b1d-127">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="80b1d-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="80b1d-128">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="80b1d-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="80b1d-129">Plantilla de directiva de grupo (. admx)</span><span class="sxs-lookup"><span data-stu-id="80b1d-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="80b1d-130">&lt;&gt;sysvol\domain\policies\PolicyDefinitions fuerte</span><span class="sxs-lookup"><span data-stu-id="80b1d-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="80b1d-131">Archivo de idioma de directiva de grupo (. ADML)</span><span class="sxs-lookup"><span data-stu-id="80b1d-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="80b1d-132">&lt;Strong &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="80b1d-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="80b1d-133">Por ejemplo, el archivo específico de idioma (ADML) de Inglés de Estados Unidos se almacenará en%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span><span class="sxs-lookup"><span data-stu-id="80b1d-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="80b1d-134">Edite la configuración de directiva de grupo mediante la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) para configurar la configuración de directiva de grupo para la tecnología de MDOP.</span><span class="sxs-lookup"><span data-stu-id="80b1d-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="80b1d-135">La Directiva de grupo de MDOP por tecnología</span><span class="sxs-lookup"><span data-stu-id="80b1d-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="80b1d-136">Para obtener más información sobre la Directiva de grupo de MDOP admitida, consulte la documentación específica de la tecnología.</span><span class="sxs-lookup"><span data-stu-id="80b1d-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80b1d-137">Tecnología de MDOP</span><span class="sxs-lookup"><span data-stu-id="80b1d-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="80b1d-138">Paquetes de versiones</span><span class="sxs-lookup"><span data-stu-id="80b1d-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="80b1d-139">Notas</span><span class="sxs-lookup"><span data-stu-id="80b1d-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="80b1d-140">Virtualización de la aplicación (App-V)</span><span class="sxs-lookup"><span data-stu-id="80b1d-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="80b1d-141">Service Packs de App-V 5,0 y App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="80b1d-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="80b1d-142">Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="80b1d-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="80b1d-143">Virtualización de la experiencia de usuario (UE-V)</span><span class="sxs-lookup"><span data-stu-id="80b1d-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="80b1d-144">UE-V 2,0 y UE-V 2,1</span><span class="sxs-lookup"><span data-stu-id="80b1d-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="80b1d-145">Configuración de UE-V 2. x con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="80b1d-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="80b1d-146">UE-V 1,0 incluyendo 1,0 SP1</span><span class="sxs-lookup"><span data-stu-id="80b1d-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="80b1d-147">Configurar UE-V con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="80b1d-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="80b1d-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span><span class="sxs-lookup"><span data-stu-id="80b1d-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="80b1d-149">MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="80b1d-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="80b1d-150">Planificación para requisitos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="80b1d-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="80b1d-151">MBAM 2,0 incluido el Service Pack 1 de 2,0</span><span class="sxs-lookup"><span data-stu-id="80b1d-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="80b1d-152">Planificación de los requisitos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="80b1d-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="80b1d-153">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="80b1d-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="80b1d-154">MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="80b1d-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="80b1d-155">Cambiar la configuración del GPO de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="80b1d-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





