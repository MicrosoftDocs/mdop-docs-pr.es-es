---
title: Página de opciones avanzadas del Asistente para secuencias de virtualización de aplicaciones
description: Página de opciones avanzadas del Asistente para secuencias de virtualización de aplicaciones
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819600"
---
# Página de opciones avanzadas del Asistente para secuencias de virtualización de aplicaciones


Use la página de **Opciones avanzadas** del asistente de secuencias de Application Virtualization (App-V) para especificar las opciones avanzadas de instalación de la aplicación. La página contiene los elementos que se describen en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Tamaño de bloque</strong></p></td>
<td align="left"><p>Se usa para especificar el tamaño de los bloques en los que se dividirá el archivo SFT cuando se transmitan a través de una red. Todos los bloques son iguales al tamaño especificado; sin embargo, el último bloque puede ser más pequeño de lo especificado. Seleccione uno de los siguientes valores:</p>
<ul>
<li><p><strong>4 KB</strong></p></li>
<li><p><strong>16 KB</strong></p></li>
<li><p><strong>32 KB</strong></p></li>
<li><p><strong>64 KB</strong></p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Cuando seleccione un tamaño de bloque, tenga en cuenta el tamaño del archivo SFT y el ancho de banda de la red. Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda. Los archivos con tamaños de bloque mayores pueden transmitirse más rápido, pero usan más ancho de banda de la red. Mediante la experimentación, puede descubrir el tamaño de bloque óptimo para las aplicaciones de transmisión en su red.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Habilitar Microsoft Update durante la supervisión</strong></p></td>
<td align="left"><p>Habilita la instalación de actualizaciones de Microsoft durante la fase de supervisión&#39;s del asistente de secuencias.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rebase de archivos dll</strong></p></td>
<td align="left"><p>Permite reasignar las bibliotecas de vínculos dinámicos compatibles a un espacio contiguo en RAM, lo que ahorra memoria y mejora el rendimiento.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Atrás</strong></p></td>
<td align="left"><p>Obtiene acceso al Asistente para secuenciación&#39;s página anterior.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Siguiente</strong></p></td>
<td align="left"><p>Accede al Asistente para secuenciación&#39;s página siguiente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cancelar</strong></p></td>
<td align="left"><p>Finaliza el funcionamiento del asistente de secuencias.</p></td>
</tr>
</tbody>
</table>



\ [Valor del token de plantilla \]

Use la página de **Opciones avanzadas** del Asistente para secuenciación de aplicaciones-V para especificar las opciones avanzadas de la aplicación que está secuenciando. Esta página contiene los elementos que se describen en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Permitir que Microsoft Update se ejecute durante la supervisión</strong></p></td>
<td align="left"><p>Especifica si las actualizaciones de software se aplicarán a la aplicación durante la fase de supervisión de la secuencia de la aplicación. Esta opción es útil si se necesitan actualizaciones para completar correctamente la instalación de la aplicación. Esta opción no está seleccionada de forma predeterminada.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Rebase de archivos dll</strong></p></td>
<td align="left"><p>Permite reasignar bibliotecas de vínculos dinámicos compatibles a un espacio contiguo en la RAM. Seleccionar esta opción puede ayudar a administrar la memoria y mejorar el rendimiento de la aplicación. Esta opción no está seleccionada de forma predeterminada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Atrás</strong></p></td>
<td align="left"><p>Va a la página anterior del asistente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Siguiente</strong></p></td>
<td align="left"><p>Va a la siguiente página del asistente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cancelar</strong></p></td>
<td align="left"><p>Descarta la configuración y sale del asistente.</p></td>
</tr>
</tbody>
</table>



\ [Valor del token de plantilla \]

## Temas relacionados


[Asistente de secuenciamiento](sequencing-wizard.md)









