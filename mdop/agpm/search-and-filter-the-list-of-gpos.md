---
title: Buscar y filtrar la lista de GPO
description: Buscar y filtrar la lista de GPO
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820261"
---
# Buscar y filtrar la lista de GPO


En administración avanzada de directivas de grupo (AGPM), puede buscar en la lista de objetos de directiva de grupo (GPO) y sus atributos para filtrar la lista de GPO que se muestran. Por ejemplo, puede buscar GPO con un nombre, un estado o un comentario concretos. También puede buscar los GPO que fueron modificados por última vez por un administrador de directiva de grupo o en una fecha determinada.

## Realizar una búsqueda compleja


Puede realizar una búsqueda compleja usando el formato de *atributo de GPO 1: cadena de búsqueda 1 atributo de GPO 2: cadena de búsqueda 2... cadenas de búsqueda de todas las columnas*. La búsqueda no distingue mayúsculas de minúsculas.

-   **Atributo de GPO:** Cualquier encabezado de columna de la lista de GPO en AGPM excepto la versión del **equipo** o la **versión del usuario**. Los atributos de GPO incluyen el nombre de GPO, el estado, el usuario que ha cambiado recientemente el GPO, la fecha y la hora en que el GPO ha cambiado recientemente, el comentario, el estado de GPO y el filtro WMI aplicado al GPO.

-   **Cadena de búsqueda:** Texto que se va a buscar en la columna especificada. Si una cadena incluye espacios, debe escribir la cadena entre comillas.

-   **Cadenas de búsqueda de todas las columnas:** Texto que se debe buscar en todas las columnas de la lista de GPO en AGPM excepto la versión del **equipo** y la **versión del usuario**. Puede incluir varias cadenas separadas por espacios. Si una cadena incluye espacios, debe escribir la cadena entre comillas.

Cada atributo de objeto de directiva de grupo y un par de cadena de búsqueda y de búsqueda se combinan mediante una operación lógica AND. El resultado es una lista de todos los objetos de directiva de grupo para los que cada atributo especificado incluye la cadena de búsqueda especificada y para la que todas las cadenas de búsqueda de todas las columnas aparecen en al menos una columna. La búsqueda devuelve cualquier coincidencia parcial para las cadenas, de modo que pueda introducir parte de un nombre de GPO o nombre de usuario y ver una lista de todos los GPO que incluyan ese texto en su nombre.

A continuación se muestran algunos ejemplos de búsquedas:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descripción de los resultados de búsqueda</th>
<th align="left">Consulta de búsqueda</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Todos los GPO con nombres que incluyen la <strong> seguridad de texto </strong> y Norteamérica <strong> </strong> .</p></td>
<td align="left"><p><strong>Nombre: </strong><strong> nombre de seguridad </strong><strong> : </strong> &quot; <strong> Norteamérica</strong>&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>Todos los GPO desprotegidos.</p></td>
<td align="left"><p><strong>Estado: </strong> &quot; <strong> desprotegido</strong>&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Todos los GPO modificados recientemente por el usuario denominado <strong> administrador </strong> y más recientemente en el mes anterior.</p></td>
<td align="left"><p><strong>modificado por: </strong><strong> fecha de cambio del administrador </strong><strong> : </strong><strong> lastmonth</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Todos los GPO en los que el Firewall de Word <strong> </strong> está incluido en el comentario más reciente y en el que la palabra <strong> seguridad </strong> aparece en cualquier columna.</p></td>
<td align="left"><p><strong>Comentario: </strong><strong> seguridad del Firewall </strong><strong></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Todos los GPO que tienen un estado de <strong> todos los valores deshabilitado </strong> .</p></td>
<td align="left"><p><strong>Estado de GPO: </strong><strong> todo</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Todos los GPO que tengan un filtro WMI denominado <strong> mi filtro WMI </strong> aplicado y que tengan un estado de configuración de <strong> usuario deshabilitado </strong> .</p></td>
<td align="left"><p><strong>filtro WMI: </strong> &quot; <strong> mi estado de GPO de filtro WMI </strong> &quot; <strong> : </strong><strong> usuario</strong></p></td>
</tr>
</tbody>
</table>

 

## Especificar fechas


Puede buscar objetos de directiva de grupo que hayan cambiado en una fecha específica, a una hora específica o durante un período de tiempo usando los mismos términos especiales disponibles cuando busque en Windows. Si va a introducir una fecha o una hora específicas, debe usar el formato que se usa en la columna **cambiar fecha** . A continuación se muestran algunos ejemplos de búsquedas de la columna **fecha de cambio** :

-   **fecha de modificación:****10/10/2009**

-   **fecha de modificación:****10/10/2009 9:00:00 a.m.**

-   **fecha de modificación:****thisweek**

Puede usar las siguientes condiciones especiales, que no distinguen entre mayúsculas y minúsculas, cuando busca en la columna de **fecha de cambio** :

-   **Today**

-   **Ayer**

-   **ThisWeek**

-   **LastWeek**

-   **ThisMonth**

-   **LastMonth**

-   **TwoMonths**

-   **ThreeMonths**

-   **ThisYear**

-   **LastYear**

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener permiso de **contenido de lista** para el dominio.

-   Para obtener más información sobre los atributos de GPO, consulte características de la [pestaña contenido](contents-tab-features-agpm40.md).

### Referencias adicionales

-   [Administración avanzada de directivas de grupo 4.0](advanced-group-policy-management-40.md)

 

 





