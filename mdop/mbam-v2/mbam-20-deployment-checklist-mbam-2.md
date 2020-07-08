---
title: Lista de comprobación de implementación de MBAM 2.0
description: Lista de comprobación de implementación de MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826440"
---
# Lista de comprobación de implementación de MBAM 2.0


Esta lista de comprobación se puede usar para ayudarle durante la implementación de administración y supervisión de Microsoft BitLocker (MBAM) con una topología independiente.

**Nota**  
En esta lista de comprobación se describen los pasos recomendados y una lista de nivel superior de elementos que se deben tener en cuenta al implementar las características de administración y supervisión de Microsoft BitLocker. Se recomienda copiar esta lista de comprobación en un programa de hoja de cálculo y personalizarla para su uso.



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
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)">Lista de comprobación de planificación de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la información de configuración admitida de MBAM para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configuraciones admitidas de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en el siguiente orden:</p>
<ol>
<li><p>Base de datos de recuperación</p></li>
<li><p>Base de datos de cumplimiento y auditoría</p></li>
<li><p>Auditoría y informes de cumplimiento</p></li>
<li><p>Servidor de autoservicio</p></li>
<li><p>Servidor de administración y supervisión</p></li>
<li><p>MBAM plantilla de directiva de grupo</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Realice un seguimiento de los nombres de los servidores en los que está instalado cada característica. Esta información se utilizará durante todo el proceso de instalación.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)">Implementación de la infraestructura de servidor de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Agregue los grupos de seguridad de los servicios de dominio de Active Directory creados durante la fase de planeación al servidor de MBAM local adecuado los administradores de características se agrupan en servidores apropiados.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planificación de los roles de administrador de MBAM 2,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Cómo administrar los roles de administrador de MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Cree e implemente objetos de directiva de grupo MBAM obligatorios.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Implementación de objetos de directiva de grupo de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implemente el software de cliente de MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Implementación de cliente de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Implementación de MBAM 2.0](deploying-mbam-20-mbam-2.md)









