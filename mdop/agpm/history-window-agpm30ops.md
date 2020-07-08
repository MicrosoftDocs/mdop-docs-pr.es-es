---
title: Ventana de historial
description: Ventana de historial
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820800"
---
# Ventana de historial


El historial de un objeto de directiva de grupo (GPO) se puede mostrar haciendo doble clic en un GPO o haciendo clic con el botón secundario en un GPO y luego haciendo clic en **historial**. También se muestra en la **consola de administración de directivas de grupo** (GPMC) como una ficha para cada GPO.

El historial proporciona un registro de eventos en la duración del objeto de directiva de grupo seleccionado. Desde la ventana **historial** , puede obtener un informe de la configuración de una versión del objeto de directiva de grupo, comparar varias versiones de un GPO o volver a una versión anterior de un objeto de directiva de grupo.

## Filtrar eventos en la ventana Historial


Las pestañas de la ventana **historial** filtran los Estados en el historial del GPO.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pestañas</th>
<th align="left">Filtros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Todos los Estados</strong></p></td>
<td align="left"><p>Mostrar todos los Estados en el historial del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versiones únicas</strong></p></td>
<td align="left"><p>Mostrar solo las versiones exclusivas del GPO protegido en el archivo. En esta lista se omite la versión implementada en el entorno de producción, los accesos directos a versiones únicas y Estados informativos.</p></td>
</tr>
</tbody>
</table>



## Información del evento


Se proporciona información para cada estado del historial del GPO.

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
<td align="left"><p><strong>Fecha de modificación</strong></p></td>
<td align="left"><p>Marca de tiempo del momento en que se realizó la acción en la <strong> </strong> columna Estado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>Un estado en el historial del GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cambiado por</strong></p></td>
<td align="left"><p>La persona que protegió o implementó el GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Comentario</strong></p></td>
<td align="left"><p>Un comentario escrito por la persona que protegió o implementó un GPO en el momento en que se modificó esta versión. Es útil para identificar las características específicas de la versión en caso de que sea necesario revertir a una versión anterior.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Eliminable</strong></p></td>
<td align="left"><p>Si esta versión del GPO se puede eliminar si el número de versiones únicas de cada GPO retenidos en el archivo es limitado.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Puede modificar si una versión de un GPO se puede eliminar haciendo clic en él con el botón secundario del ratón y, a continuación, haciendo clic en no <strong> permitir eliminación </strong> o <strong> permitir eliminación </strong> .</p>
</div>
<div>

</div></td>
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
<td align="left"><p>La configuración del equipo y la configuración del usuario se pueden administrar por separado. Este estado muestra las partes del GPO que están habilitadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Mostrar todos los filtros WMI que se aplican a este GPO. Los filtros WMI se administran en la <strong> carpeta WMI filters </strong> del dominio en el árbol de consola de la GPMC.</p></td>
</tr>
</tbody>
</table>



## Informes


Los botones **configuración** y **diferencias** muestran informes sobre la configuración de GPO para la versión o versiones de GPO seleccionadas. Hacer clic con el botón secundario del mouse en versiones de GPO ofrece la opción de mostrar informes basados en XML.

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
<td align="left"><p><strong>Configuración</strong></p></td>
<td align="left"><p>Generar un informe basado en HTML que muestre la configuración dentro de la versión seleccionada del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Temporaria</strong></p></td>
<td align="left"><p>Generar un informe basado en HTML comparando la configuración con varias versiones seleccionadas del GPO.</p></td>
</tr>
</tbody>
</table>



### Clave para los informes de diferencias

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Símbolo</th>
<th align="left">Significado</th>
<th align="left">Color</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>El elemento tiene una configuración idéntica en ambos GPO</p></td>
<td align="left"><p>Varía según el nivel</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>El elemento se encuentra en los dos GPO, pero con la configuración cambiada</p></td>
<td align="left"><p>Azulado</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>El elemento solo existe en el primer GPO</p></td>
<td align="left"><p>Rojo</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>El elemento solo existe en el segundo GPO</p></td>
<td align="left"><p>Verde</p></td>
</tr>
</tbody>
</table>



-   En el caso de los elementos con la configuración cambiada, la configuración cambiada se identifica cuando se expande el elemento. El valor del atributo de cada objeto de directiva de grupo se muestra en el mismo orden en que se muestran en el informe.

-   Algunos cambios en la configuración pueden hacer que un elemento se notifique como dos elementos diferentes (uno presente solo en el primer GPO, uno solo presente en el segundo), en lugar de como un elemento que ha cambiado.

### Referencias adicionales

-   [Pestaña Contenido](contents-tab-agpm30ops.md)









