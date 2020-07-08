---
title: Lista de comprobación para evaluar aplicaciones de línea de negocio para UE-V 1.0
description: Lista de comprobación para evaluar aplicaciones de línea de negocio para UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826460"
---
# Lista de comprobación para evaluar aplicaciones de línea de negocio para UE-V 1.0


Para evaluar qué aplicaciones de línea de negocio deben incluirse en su implementación de UE-V, tenga en cuenta lo siguiente:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Esta aplicación contiene opciones de configuración que el usuario puede personalizar?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Es importante para el usuario que esta configuración sea móvil?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Esta configuración de usuario ya está administrada por una solución de directiva de configuración o administración de aplicaciones? UE-V aplica la configuración de la aplicación en el inicio de la aplicación y en la configuración de Windows en los eventos de inicio de sesión, desbloqueo o conexión remota. Si usa UE-V con otras soluciones de directiva de configuración, es posible que los usuarios experimenten una incoherencia en la configuración de roaming.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Son las configuraciones específicas de la aplicación para el equipo? Las preferencias y personalizaciones de la aplicación que están relacionadas con el hardware o con la configuración específica de un equipo no se mueven de manera coherente entre sesiones y pueden provocar una mala experiencia de la aplicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿La configuración del almacén de aplicaciones en el directorio archivos de programa o en el directorio de archivos que se encuentra en el <strong> </strong> directorio \ [nombre de usuario] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ? Los datos de la aplicación que se almacenan en cualquiera de estas ubicaciones no suelen ser móviles con el usuario, porque estos datos son específicos del equipo o porque los datos son demasiado grandes para poder ser móviles.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿La aplicación almacena la configuración en un archivo que contiene otros datos de la aplicación que no deberían ser móviles? UE-V sincroniza los archivos como una sola unidad. Si la configuración se almacena en archivos que incluyen datos de aplicaciones distintos de la configuración, la sincronización de estos datos adicionales puede provocar una mala experiencia de la aplicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Cuál es el tamaño de los archivos que contienen la configuración? El rendimiento de la sincronización de configuración puede verse afectado por archivos grandes. La inclusión de archivos grandes puede influir en el rendimiento de la sincronización de configuración.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Planificación de métodos de configuración de UE-V](planning-for-ue-v-configuration-methods.md)

[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

 

 





