---
title: Comandos de plantilla
description: Comandos de plantilla
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820181"
---
# Comandos de plantilla


La ficha **plantillas** :

-   Muestra una lista de las plantillas disponibles que puede usar para crear nuevos objetos de directiva de grupo (GPO).

-   Proporciona un menú contextual con comandos para crear un GPO basado en una plantilla seleccionada, administrar plantillas y mostrar informes de plantillas.

-   Muestra una lista de los grupos y los usuarios que tienen permiso para obtener acceso a una plantilla seleccionada.

Debido a que no se puede modificar una plantilla, las plantillas no tienen historial. Sin embargo, como cualquier versión de GPO, la configuración de una plantilla se puede mostrar con un informe de configuración o compararse con otro GPO con un informe de diferencias.

**Nota:**  Una plantilla es una versión estática y no modificable de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo editables.

 

Al hacer clic con el botón secundario en la lista **objetos de directiva de grupo** de esta pestaña se muestra un menú contextual, incluyendo cualquiera de las opciones siguientes.

## Control


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nuevo GPO controlado</strong></p></td>
<td align="left"><p>Cree un GPO basado en la plantilla seleccionada. Se proporciona la opción de implementar el nuevo GPO en el entorno de producción. Si no tiene permiso para crear un GPO, se le pedirá que envíe una solicitud. (Esta opción aparece si no se selecciona ningún GPO al hacer clic con el botón secundario del ratón en el <strong> Lista de objetos de directiva de grupo </strong> ).</p></td>
</tr>
</tbody>
</table>

 

## Informes


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configuración</strong></p></td>
<td align="left"><p>Generar un informe basado en HTML o en XML en el que se muestre la configuración dentro del objeto de directiva de grupo seleccionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Temporaria</strong></p></td>
<td align="left"><p>Generar un informe basado en HTML o en XML comparando la configuración en dos plantillas de GPO seleccionadas.</p></td>
</tr>
</tbody>
</table>

 

## Administración de plantillas


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Establecer como predeterminado</strong></p></td>
<td align="left"><p>Establezca la plantilla seleccionada como predeterminada para usarla automáticamente al crear un nuevo GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eliminar</strong></p></td>
<td align="left"><p>Mover la plantilla seleccionada a la <strong> papelera de reciclaje </strong> . Si no tiene permiso para eliminar un GPO, se le pedirá que envíe una solicitud.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cambiar nombre</strong></p></td>
<td align="left"><p>Cambiar el nombre de la plantilla seleccionada.</p></td>
</tr>
</tbody>
</table>

 

## Varios


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Actualizar</strong></p></td>
<td align="left"><p>Actualice la visualización de la consola de administración de directivas de grupo para incorporar los cambios. Algunos cambios no son visibles hasta que se actualiza la pantalla.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ayuda</strong></p></td>
<td align="left"><p>Mostrar la ayuda para la administración de directivas de grupo (AGPM) avanzada.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Pestaña Contenido](contents-tab-agpm30ops.md)

-   [Realización de tareas de editor](performing-editor-tasks-agpm30ops.md)

-   [Realización de tareas de revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





