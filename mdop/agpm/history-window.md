---
title: Ventana de historial
description: Ventana de historial
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820790"
---
# Ventana de historial


El historial de un objeto de directiva de grupo (GPO) se puede mostrar haciendo doble clic en un GPO o haciendo clic con el botón secundario en un GPO y luego haciendo clic en **historial**. También se muestra en la **consola de administración de directivas de grupo** (GPMC) como una ficha para cada GPO.

El historial proporciona una lista de todas las versiones del GPO seleccionado guardadas en el archivo. Desde la ventana **historial** , puede obtener un informe de la configuración de un objeto de directiva de grupo, comparar varias versiones de un GPO o volver a una versión anterior de un objeto de directiva de grupo.

## Filtrar eventos en la ventana Historial


Las pestañas de la ventana **historial** filtran los eventos que se muestran.

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
<td align="left"><p><strong>Mostrar todo</strong></p></td>
<td align="left"><p>Mostrar todas las versiones del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Protegido</strong></p></td>
<td align="left"><p>Mostrar solo las versiones protegidas del GPO. La versión implementada se omite de esta lista.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Solo etiquetas</strong></p></td>
<td align="left"><p>Mostrar solo los GPO que tengan etiquetas asociadas.</p></td>
</tr>
</tbody>
</table>

 

## Información del evento


Se proporciona información para cada evento en el historial del GPO seleccionado.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica de GPO</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Ordenador</strong></p></td>
<td align="left"><p>Versión generada automáticamente de la parte de configuración del equipo del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Usuario</strong></p></td>
<td align="left"><p>Versión generada automáticamente de la parte de configuración de usuario del GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Tiempo</strong></p></td>
<td align="left"><p>Marca de fecha y hora de la versión del GPO cuando se realizó la acción en el campo de estado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>El estado de la versión seleccionada del GPO:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Implementado </strong> : esta versión del GPO está actualmente activa en el entorno de producción.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Protegido </strong> : esta versión del GPO está disponible para que los editores autorizados las desprotejan para editarla o para que la implemente un administrador de directiva de grupo.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Desprotegido </strong> : esta versión del GPO está desprotegida por un editor y no está disponible para otros editores. (El estado desprotegido no se registra en el <strong> Historial </strong> excepto para indicar si un objeto de directiva de grupo está actualmente desprotegido.</p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong>Creado </strong> : identifica la fecha y la hora de la creación inicial del GPO.</p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong>Etiquetada </strong> : identifica una versión con etiqueta del GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Estado de GPO</strong></p></td>
<td align="left"><p>La configuración del equipo y la configuración del usuario se pueden administrar por separado. Este estado muestra las partes del GPO que están habilitadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Propietario</strong></p></td>
<td align="left"><p>La persona que protegió o implementó el GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comentario</strong></p></td>
<td align="left"><p>Un comentario escrito por el propietario de un objeto de directiva de grupo en el momento en que se modificó esta versión. Es útil para identificar las características específicas de la versión en caso de que sea necesario revertir a una versión anterior.</p></td>
</tr>
</tbody>
</table>

 

## Informes


En función de si se selecciona una única versión de GPO o varias versiones de GPO, los botones **configuración** y **diferencias** muestran informes sobre la configuración de GPO. Hacer clic con el botón secundario del mouse en versiones de GPO ofrece la opción de mostrar informes basados en XML.

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

-   [Pestaña Contenido](contents-tab.md)

 

 





