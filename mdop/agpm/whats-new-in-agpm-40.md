---
title: Novedades de AGPM 4.0
description: Novedades de AGPM 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820101"
---
# Novedades de AGPM 4.0


Administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft incluye nuevas características que le permiten buscar objetos de directiva de grupo (GPO), filtrar la lista de GPO visualizados, exportar e importar un GPO a un bosque diferente e instalar AGPM en equipos que ejecuten Windows7 y Windows Server2008R2.

## Buscar y filtrar GPO


En AGPM 4,0, puede buscar atributos específicos en la lista de GPO para filtrar la lista de GPO que se muestran. Por ejemplo, puede buscar GPO con un nombre, un estado o un comentario concretos. También puede buscar los GPO que fueron modificados por última vez por un administrador de directiva de grupo o en una fecha determinada.

Puede crear una cadena de búsqueda compleja con el formato *atributo 1 de GPO: texto de búsqueda 1, atributo 2: buscar texto 2...*, donde un atributo de GPO es cualquier encabezado de columna de la lista de GPO en AGPM. Por ejemplo, para buscar todos los GPO con nombres incluyendo el texto "MyGPO" que se han protegido y modificado por última vez por la Editor03 de usuario, escriba lo siguiente en el cuadro de búsqueda: **nombre: MyGPO estado:** se ha modificado la**protección de****: Editor03**. La búsqueda devuelve coincidencias parciales para que pueda introducir parte de un nombre de GPO o nombre de usuario y ver una lista de todos los GPO que incluyan ese texto en su nombre.

Además, puede usar los mismos términos especiales disponibles cuando realiza una búsqueda en Windows para buscar objetos de directiva de grupo que hayan cambiado en una fecha específica o en un intervalo de fechas. Por ejemplo, **cambie fecha:****lastmonth** o **cambiar fecha:****thisweek**.

## Exportar e importar GPO a distintos bosques


Con AGPM 4,0, puede copiar un GPO controlado de un dominio de un bosque a un dominio en un segundo bosque. Por ejemplo, puede exportar un GPO de un dominio de un bosque a un archivo CAB mediante AGPM, copiar ese archivo CAB en una unidad USB, conectar la unidad USB a un equipo de un dominio de un segundo bosque e importar el GPO a AGPM en un dominio del segundo bosque. Puede importar el GPO como un nuevo GPO controlado o importarlo para reemplazar la configuración de un GPO existente que está desprotegido.

## Compatibilidad con Windows Server 2008 R2 y Windows 7


AGPM 4,0 admite Windows Server2008R2 y Windows7, pero todavía es compatible con Windows Server2008 y vista® con Service Pack1 (SP1). Sin embargo, existen limitaciones en un entorno mixto que incluye los sistemas operativos más nuevos y antiguos, como se indica en la tabla siguiente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo en el que se ejecuta el servidor de AGPM 4,0</th>
<th align="left">Sistema operativo en el que se ejecuta el cliente de AGPM 4,0</th>
<th align="left">Estado de la compatibilidad con AGPM 4,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>No compatible</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o Windows7</p></td>
</tr>
</tbody>
</table>

 

 

 





