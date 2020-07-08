---
title: Funciones de la pestaña Contenido
description: Funciones de la pestaña Contenido
author: dansimp
ms.assetid: 725f025a-c30a-4d07-add1-4e0ed9a1a5fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f64aad16a3335d78641812121692f6d5f6436ee1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818910"
---
# Funciones de la pestaña Contenido


Cada pestaña secundaria de la pestaña **contenido** tiene dos secciones:**objetos de directiva de grupo** y **grupos y usuarios**.

## Sección objetos de directiva de grupo


En la sección **objetos de directiva de grupo** se muestra una lista filtrada de objetos de directiva de grupo (GPO) y se identifican los siguientes atributos de cada GPO:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Atributo GPO</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nombre del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>El estado del GPO seleccionado</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cambiado por</strong></p></td>
<td align="left"><p>El editor que protegió o el aprobador que implementó el GPO seleccionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Fecha de modificación</strong></p></td>
<td align="left"><p>Para un GPO controlado, la fecha más reciente en la que se protegió después de modificarlo o desprotegerlo para modificarlo. Para un GPO no controled, la fecha en la que se modificó por última vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comentario</strong></p></td>
<td align="left"><p>Un comentario escrito por la persona que protegió o implementó un GPO en el momento en que se modificó. Es útil para identificar las características específicas de la versión en caso de que sea necesario revertir a una versión anterior.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versión del equipo</strong></p></td>
<td align="left"><p>Versión generada automáticamente de la parte de configuración del equipo del GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Versión de usuario</strong></p></td>
<td align="left"><p>Versión generada automáticamente de la parte de configuración de usuario del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado de GPO</strong></p></td>
<td align="left"><p>La configuración del equipo y la configuración del usuario se pueden administrar por separado. El estado del GPO indica qué partes del GPO están habilitadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Mostrar todos los filtros WMI que se aplican a este GPO. Los filtros WMI se administran en la <strong> carpeta WMI filters </strong> del dominio en el árbol de consola de la GPMC.</p></td>
</tr>
</tbody>
</table>

 

## Sección grupos y usuarios


Cuando se selecciona un GPO, la sección **grupos y usuarios** muestra una lista de los grupos y usuarios con acceso a ese GPO. Los permisos y la herencia permitidos se muestran para cada grupo o usuario. Un administrador de AGPM puede configurar permisos con roles de AGPM estándar (editor, aprobador, revisor y administrador de AGPM) o una combinación personalizada de permisos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Botón</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Agregar</strong></p></td>
<td align="left"><p>Agregue una nueva entrada al descriptor de seguridad. Se puede Agregar a cualquier usuario o grupo de Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eliminar</strong></p></td>
<td align="left"><p>Quitar la entrada seleccionada de la lista de control de acceso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propiedades</strong></p></td>
<td align="left"><p>Mostrar las propiedades del objeto seleccionado. La página de propiedades es la misma que se muestra para un objeto en <strong> usuarios y equipos de Active Directory </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avanzado</strong></p></td>
<td align="left"><p>Abra el <strong> Editor de la lista de control de acceso </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Consideraciones adicionales

-   Para obtener información sobre los roles y los permisos relacionados con tareas específicas, consulte las tareas de realizar tareas de [Administrador de AGPM](performing-agpm-administrator-tasks-agpm30ops.md), [realizar tareas de editor](performing-editor-tasks-agpm30ops.md), [realizar tareas de aprobador](performing-approver-tasks-agpm30ops.md)y [realizar tareas de revisor](performing-reviewer-tasks-agpm30ops.md).

### Referencias adicionales

-   [Pestaña Contenido](contents-tab-agpm30ops.md)

 

 





