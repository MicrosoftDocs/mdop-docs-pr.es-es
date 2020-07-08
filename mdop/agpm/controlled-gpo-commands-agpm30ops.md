---
title: Comandos de GPO controlado
description: Comandos de GPO controlado
author: dansimp
ms.assetid: 82db4772-154a-4a8d-99cd-2c69e1738698
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8e537751107a2796727e5ed71511649b6bce953a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818880"
---
# Comandos de GPO controlado


La ficha **controlada** :

-   Muestra una lista de objetos de directiva de grupo (GPO) administrados por la administración avanzada de directivas de grupo (AGPM).

-   Proporciona un menú contextual con comandos para administrar objetos de directiva de grupo y mostrar el historial y los informes de los GPO.

-   Muestra una lista de los grupos y los usuarios que tienen permiso para obtener acceso a un objeto de directiva de grupo seleccionado.

Al hacer clic con el botón secundario en la lista **objetos de directiva de grupo** de esta pestaña se muestra un menú contextual, incluyendo cualquiera de las opciones siguientes.

## Control e historial


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
<td align="left"><p>Cree un nuevo GPO con control de cambios administrado mediante AGPM y impleméntelo en el entorno de producción. Si no tiene permiso para crear un GPO, se le pedirá que envíe una solicitud. (Esta opción aparece si no se selecciona ningún GPO al hacer clic con el botón secundario del ratón en el <strong> Lista de objetos de directiva de grupo </strong> ).</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Historial</strong></p></td>
<td align="left"><p>Abrir una ventana en la que se muestran todas las versiones del GPO seleccionado guardadas en el archivo. Desde el historial, puede obtener un informe de la configuración de un objeto de directiva de grupo, comparar dos versiones de un GPO, comparar un GPO con una plantilla o volver a una versión anterior de un objeto de directiva de grupo.</p></td>
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
<td align="left"><p>Generar un informe basado en HTML o basado en XML que muestre la configuración dentro del GPO seleccionado o mostrar los vínculos a los GPO seleccionados de unidades organizativas en el momento en que los GPO se hayan controlado, importado o protegido más recientemente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Temporaria</strong></p></td>
<td align="left"><p>Generar un informe basado en HTML o en XML comparando la configuración en dos GPO seleccionados o dentro del GPO seleccionado y una plantilla.</p></td>
</tr>
</tbody>
</table>

 

## Edición


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
<td align="left"><p><strong>Editar</strong></p></td>
<td align="left"><p>Abra la <strong> ventana del editor </strong> de administración de directivas de grupo para realizar cambios en el GPO seleccionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Check-out</strong></p></td>
<td align="left"><p>Obtenga una copia del objeto de directiva de grupo seleccionado del archivo para editarlo sin conexión y prohíba a cualquier otra persona que lo edite hasta que se vuelva a registrar en el archivo. (El administrador de AGPM puede reemplazarlo por un administrador de AGPM (control total))).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Check-in</strong></p></td>
<td align="left"><p>Compruebe la versión editada del GPO seleccionado en el archivo, para que otros editores autorizados puedan realizar cambios o un aprobador pueda implementarlo en el entorno de producción.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Deshacer la desprotección</strong></p></td>
<td align="left"><p>Devolver un GPO desprotegido al archivo sin cambios.</p></td>
</tr>
</tbody>
</table>

 

## Administración de versiones


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
<td align="left"><p><strong>Importar desde producción</strong></p></td>
<td align="left"><p>Para el GPO seleccionado, copie la versión del entorno de producción en el archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eliminar</strong></p></td>
<td align="left"><p>Mover el GPO seleccionado a la papelera de reciclaje e indicar si se debe abandonar la versión implementada (si existe) en la producción o eliminarla, así como la versión en el archivo. Si no tiene permiso para eliminar un GPO, se le pedirá que envíe una solicitud.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Implementar</strong></p></td>
<td align="left"><p>Mover el GPO seleccionado que está protegido en el archivo al entorno de producción. Esta acción la activa en la red y sobrescribe la versión previamente activa del GPO, si existe alguna. Si no tiene permiso para implementar un GPO, se le pedirá que envíe una solicitud.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Etiqueta</strong></p></td>
<td align="left"><p>Marcar el GPO seleccionado con una etiqueta descriptiva (como &quot; bueno conocido &quot; ) y el comentario para la conservación de registros. Las etiquetas aparecen en <strong> la </strong> columna Estado y los comentarios en la <strong> </strong> columna Comentario de la ventana del historial, lo que le <strong> </strong> permite identificar fácilmente versiones anteriores de un GPO identificado con una etiqueta en particular, de modo que pueda revertir si se produce un problema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cambiar nombre</strong></p></td>
<td align="left"><p>Cambiar el nombre del GPO seleccionado. Si el GPO ya se ha implementado, el nombre se actualizará en el entorno de producción cuando se vuelva a implementar el GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Guardar como plantilla</strong></p></td>
<td align="left"><p>Crear una nueva plantilla basada en la configuración del objeto de directiva de grupo seleccionado.</p></td>
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
<td align="left"><p>Actualice la visualización de la consola de administración de directivas de grupo (GPMC) para incorporar los cambios. Algunos cambios no son visibles hasta que se actualiza la pantalla.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ayuda</strong></p></td>
<td align="left"><p>Mostrar la ayuda para AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Pestaña Contenido](contents-tab-agpm30ops.md)

-   [Realización de tareas de editor](performing-editor-tasks-agpm30ops.md)

-   [Realización de tareas del Aprobador](performing-approver-tasks-agpm30ops.md)

-   [Realización de tareas de revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





