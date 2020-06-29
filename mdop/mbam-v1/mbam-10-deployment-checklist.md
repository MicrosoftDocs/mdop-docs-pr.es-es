---
title: Lista de comprobación de implementación de MBAM 1.0
description: Lista de comprobación de implementación de MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812535"
---
# Lista de comprobación de implementación de MBAM 1.0


Esta lista de comprobación está diseñada para facilitar la implementación de la supervisión y administración de Microsoft BitLocker (MBAM).

**Nota**  
En esta lista de comprobación se describen los pasos recomendados y se proporciona una lista de nivel superior de los elementos que se deben tener en cuenta al implementar las características de MBAM. Le recomendamos que copie esta lista de comprobación en un programa de hoja de cálculo y la Personalice según sus necesidades específicas.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tarea</th>
<th align="left">Referencias</th>
<th align="left">Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Complete la fase de planeamiento para preparar el entorno informático para la implementación de MBAM.</p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">Lista de comprobación de planificación de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la información de MBAM configuraciones compatibles para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configuraciones admitidas de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en el siguiente orden:</p>
<ol>
<li><p>Base de datos de recuperación y hardware</p></li>
<li><p>Base de datos de estado de cumplimiento</p></li>
<li><p>Auditoría y informes de cumplimiento</p></li>
<li><p>Servidor de administración y supervisión</p></li>
<li><p>MBAM plantilla de directiva de grupo</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Realice un seguimiento de los nombres de los servidores en los que está instalado cada característica. Usará esta información durante el proceso de instalación.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">Implementación de la infraestructura de servidor de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Agregue los grupos de seguridad de los servicios de dominio de Active Directory creados durante la fase de planeación al grupo de administradores de características del servidor de MBAM local adecuado en los servidores correspondientes.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planificación de los roles de administrador de MBAM 1,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Cómo administrar los roles de administrador de MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Cree e implemente los objetos de directiva de grupo MBAM obligatorios.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Implementación de objetos de directiva de grupo de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implemente el software de cliente de MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Implementación de cliente de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Implementación de MBAM 1.0](deploying-mbam-10.md)









