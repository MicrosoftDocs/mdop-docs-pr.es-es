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
# Copia de plantillas de directiva de grupo de MBAM 2.5


Antes de implementar la instalación del cliente MBAM, debe descargar las plantillas de directiva de grupo MBAM, que contienen la configuración de la Directiva de grupo que define MBAM configuración de implementación para cifrado de unidad BitLocker. Después de descargar las plantillas, establezca la configuración de directiva de grupo para implementarla en toda la empresa.

## Descargar e implementar las plantillas de directiva de grupo de MDOP


Las plantillas de directiva de grupo de MDOP están disponibles para su descarga en un archivo comprimido autoextraíble, agrupado por tecnología y versión.

**Cómo descargar e implementar las plantillas de directiva de grupo de MDOP**

1. Descargue las plantillas administrativas de la Directiva de grupo MDOP de [Microsoft Desktop Optimization Pack](https://www.microsoft.com/download/details.aspx?id=55531).

2. Ejecute el archivo descargado para extraer las carpetas de plantillas.

   **Advertencia**  
   No extraiga las plantillas directamente en el directorio de implementación de la Directiva de grupo. En este archivo se incluyen varias tecnologías y versiones.



3. En la carpeta extraída, busque el archivo. ADMX de la versión Technology. Algunas tecnologías de MDOP tienen varios conjuntos de objetos de directiva de grupo (GPO). Por ejemplo, MBAM incluye configuración de administración de MBAM y MBAM configuración de usuario.

4. Busque el archivo. ADML correspondiente por idioma-referencia cultural (es decir, *en* para inglés, Estados Unidos).

5. Copie los archivos. ADMX y. ADML en una carpeta de definición de directiva. Según dónde almacene las plantillas, puede configurar opciones de directiva de grupo desde el dispositivo local o desde cualquier equipo del dominio.

   **Archivos locales.** Para configurar las opciones de directiva de grupo desde el dispositivo local, copie los archivos de plantilla en las siguientes ubicaciones:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo de archivo</th>
   <th align="left">Ubicación del archivo</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Plantilla de directiva de grupo (. admx)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;policyDefinitions fuerte</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Archivo de idioma de directiva de grupo (. ADML)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;policyDefinitions fuerte</strong><code>[MUIculture]</code></p></td>
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



6. Edite la configuración de directiva de grupo mediante la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) para configurar la configuración de directiva de grupo para la tecnología de MDOP. Para obtener más información, consulte [editar la configuración de la Directiva de grupo de MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) .

   Para obtener descripciones de la configuración de directiva de grupo, consulte requisitos de la [Directiva de grupo planificación de MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).


## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 2.5](deploying-mbam-25-group-policy-objects.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






