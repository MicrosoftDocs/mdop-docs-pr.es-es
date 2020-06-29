---
title: Copia de plantillas de directiva de grupo de MBAM 2.5
description: Copia de plantillas de directiva de grupo de MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825221"
---
# <span data-ttu-id="00854-103">Copia de plantillas de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00854-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="00854-104">Antes de implementar la instalación del cliente MBAM, debe descargar las plantillas de directiva de grupo MBAM, que contienen la configuración de la Directiva de grupo que define MBAM configuración de implementación para cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="00854-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="00854-105">Después de descargar las plantillas, establezca la configuración de directiva de grupo para implementarla en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="00854-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="00854-106">Descargar e implementar las plantillas de directiva de grupo de MDOP</span><span class="sxs-lookup"><span data-stu-id="00854-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="00854-107">Las plantillas de directiva de grupo de MDOP están disponibles para su descarga en un archivo comprimido autoextraíble, agrupado por tecnología y versión.</span><span class="sxs-lookup"><span data-stu-id="00854-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="00854-108">Cómo descargar e implementar las plantillas de directiva de grupo de MDOP</span><span class="sxs-lookup"><span data-stu-id="00854-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="00854-109">Descargue las plantillas administrativas de la Directiva de grupo MDOP de [Microsoft Desktop Optimization Pack](https://www.microsoft.com/download/details.aspx?id=55531).</span><span class="sxs-lookup"><span data-stu-id="00854-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="00854-110">Ejecute el archivo descargado para extraer las carpetas de plantillas.</span><span class="sxs-lookup"><span data-stu-id="00854-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="00854-111">Advertencia</span><span class="sxs-lookup"><span data-stu-id="00854-111">Warning</span></span>**  
   <span data-ttu-id="00854-112">No extraiga las plantillas directamente en el directorio de implementación de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="00854-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="00854-113">En este archivo se incluyen varias tecnologías y versiones.</span><span class="sxs-lookup"><span data-stu-id="00854-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="00854-114">En la carpeta extraída, busque el archivo. ADMX de la versión Technology.</span><span class="sxs-lookup"><span data-stu-id="00854-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="00854-115">Algunas tecnologías de MDOP tienen varios conjuntos de objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="00854-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="00854-116">Por ejemplo, MBAM incluye configuración de administración de MBAM y MBAM configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="00854-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="00854-117">Busque el archivo. ADML correspondiente por idioma-referencia cultural (es decir, *en* para inglés, Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="00854-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="00854-118">Copie los archivos. ADMX y. ADML en una carpeta de definición de directiva.</span><span class="sxs-lookup"><span data-stu-id="00854-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="00854-119">Según dónde almacene las plantillas, puede configurar opciones de directiva de grupo desde el dispositivo local o desde cualquier equipo del dominio.</span><span class="sxs-lookup"><span data-stu-id="00854-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="00854-120">Archivos locales.</span><span class="sxs-lookup"><span data-stu-id="00854-120">Local files.</span></span>** <span data-ttu-id="00854-121">Para configurar las opciones de directiva de grupo desde el dispositivo local, copie los archivos de plantilla en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="00854-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="00854-122">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="00854-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="00854-123">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="00854-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="00854-124">Plantilla de directiva de grupo (. admx)</span><span class="sxs-lookup"><span data-stu-id="00854-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="00854-125">&lt;&gt;policyDefinitions fuerte</span><span class="sxs-lookup"><span data-stu-id="00854-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="00854-126">Archivo de idioma de directiva de grupo (. ADML)</span><span class="sxs-lookup"><span data-stu-id="00854-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="00854-127">&lt;&gt;policyDefinitions fuerte</span><span class="sxs-lookup"><span data-stu-id="00854-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="00854-128">Edite la configuración de directiva de grupo mediante la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) para configurar la configuración de directiva de grupo para la tecnología de MDOP.</span><span class="sxs-lookup"><span data-stu-id="00854-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="00854-129">Para obtener más información, consulte [editar la configuración de la Directiva de grupo de MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="00854-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="00854-130">Para obtener descripciones de la configuración de directiva de grupo, consulte requisitos de la [Directiva de grupo planificación de MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00854-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="00854-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00854-131">Related topics</span></span>


[<span data-ttu-id="00854-132">Implementación de objetos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00854-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="00854-133">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="00854-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="00854-134">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="00854-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="00854-135">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="00854-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






