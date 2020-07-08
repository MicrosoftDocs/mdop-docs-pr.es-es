---
title: Cómo determinar si se va a editar o actualizar un paquete de aplicaciones virtuales
description: Cómo determinar si se va a editar o actualizar un paquete de aplicaciones virtuales
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817501"
---
# Cómo determinar si se va a editar o actualizar un paquete de aplicaciones virtuales


Use la siguiente tabla para determinar si se puede abrir un paquete de aplicaciones virtual para su edición, si es necesario crear una nueva versión del paquete o si una de las opciones está disponible, mediante el secuenciador de App-V.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Acción</th>
<th align="left">Abrir para editar</th>
<th align="left">Abrir para actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ver las propiedades del paquete.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ver el historial de cambios del paquete.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ver archivos de paquetes asociados.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Edite la configuración del registro.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revise la configuración adicional del paquete (excepto las propiedades del archivo del sistema operativo).</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Crear un instalador de Windows (MSI) asociado.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modificar archivo OSD.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Comprimir y descomprimir el paquete.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Agregue asociaciones de tipos de archivo.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cambiar el nombre de los accesos directos.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Establezca el estado de la clave del registro virtualizado (override/Merge).</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Establecer el estado de carpeta virtualizado.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Editar asignaciones del sistema de archivos virtual.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Revise todas las propiedades del archivo del sistema operativo asociado de un paquete.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Agregar servicios adicionales.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agregar archivos adicionales.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recopilar y configurar los descriptores de seguridad relacionados.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicar actualizaciones de seguridad o actualizar a una nueva versión.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Agregue una aplicación adicional.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplique actualizaciones que requieran que se abra la aplicación.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aplique actualizaciones que requieran que el equipo se reinicie.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Cómo modificar una aplicación virtual existente](how-to-edit-an-existing-virtual-application.md)

[Cómo actualizar una aplicación Virtual existente](how-to-upgrade-an-existing-virtual-application.md)

 

 





