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
# Cómo descargar e implementar plantillas (.admx) de la directiva de grupo de MDOP


Puede administrar la configuración de características de ciertas tecnologías de Microsoft Desktop Optimization Pack (MDOP) (por ejemplo, App-V, UE-V o MBAM) mediante plantillas de directiva de grupo, los archivos. ADMX y. ADML. Las plantillas de directiva de grupo de MDOP están disponibles para su descarga en un archivo comprimido autoextraíble, agrupado por tecnología y versión.

## Plantillas de directiva de grupo de MDOP

**Cómo descargar e implementar las plantillas de directiva de grupo de MDOP**

1. Descargar las [plantillas de directiva de grupo de MDOP](https://www.microsoft.com/download/details.aspx?id=55531) más recientes 

2. Expanda el archivo. cab descargado ejecutando `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Advertencia**  
   No extraiga las plantillas directamente en el directorio de implementación de la Directiva de grupo. En este archivo se incluyen varias tecnologías y versiones.

3. En la carpeta extraída, busque el archivo. ADMX de la versión Technology. Algunas tecnologías de MDOP tienen varios conjuntos de objetos de directiva de grupo (GPO). Por ejemplo, MBAM incluye configuración de administración de MBAM y MBAM configuración de usuario.

4. Busque el archivo. ADML correspondiente por idioma-referencia cultural (es decir, *en-* es para inglés-Estados Unidos).

5. Copie los archivos. ADMX y. ADML en una carpeta de definición de directiva. Según dónde almacene las plantillas, puede configurar opciones de directiva de grupo desde el dispositivo local o desde cualquier equipo del dominio.

   - **Archivos locales:** Para configurar las opciones de directiva de grupo desde el dispositivo local, copie los archivos de plantilla en las siguientes ubicaciones:

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

   - **Almacén central del dominio:** Para habilitar la configuración de directiva de grupo de un administrador de directivas de grupo desde cualquier equipo del dominio, copie los archivos a las siguientes ubicaciones del controlador de dominio:

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
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;sysvol\domain\policies\PolicyDefinitions fuerte</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Archivo de idioma de directiva de grupo (. ADML)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;Strong &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>Por ejemplo, el archivo específico de idioma (ADML) de Inglés de Estados Unidos se almacenará en%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
   </tr>
   </tbody>
   </table>

6. Edite la configuración de directiva de grupo mediante la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) para configurar la configuración de directiva de grupo para la tecnología de MDOP.

### La Directiva de grupo de MDOP por tecnología

Para obtener más información sobre la Directiva de grupo de MDOP admitida, consulte la documentación específica de la tecnología.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tecnología de MDOP</th>
<th align="left">Paquetes de versiones</th>
<th align="left">Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Virtualización de la aplicación (App-V)</strong></p></td>
<td align="left"><p>Service Packs de App-V 5,0 y App-V 5,0</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Virtualización de la experiencia de usuario (UE-V)</strong></p></td>
<td align="left"><p>UE-V 2,0 y UE-V 2,1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">Configuración de UE-V 2. x con objetos de directiva de grupo</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1,0 incluyendo 1,0 SP1</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">Configurar UE-V con objetos de directiva de grupo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Microsoft BitLocker Administration and Monitoring (MBAM)</strong></p></td>
<td align="left"><p>MBAM 2,5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">Planificación para requisitos de directiva de grupo de MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2,0 incluido el Service Pack 1 de 2,0</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planificación de los requisitos de directiva de grupo de MBAM 2.0</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">Implementación de objetos de directiva de grupo de MBAM 2.0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1,0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">Cambiar la configuración del GPO de MBAM 1.0</a></p></td>
</tr>
</tbody>
</table>

 

 

 





