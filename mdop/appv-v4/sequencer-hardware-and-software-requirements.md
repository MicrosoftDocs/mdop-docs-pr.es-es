---
title: Requisitos hardware y software del secuenciador
description: Requisitos hardware y software del secuenciador
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815531"
---
# Requisitos hardware y software del secuenciador


En este tema se describen los requisitos mínimos de hardware y software recomendados para el equipo que ejecuta el secuenciador de Microsoft Application Virtualization (App-V).

Antes de instalar el secuenciador y después de la secuencia de cada aplicación, debe restaurar una imagen de sistema operativo limpia en el equipo de secuenciación. Puede usar uno de los siguientes métodos para restaurar el equipo que ejecuta el secuenciador:

-   Vuelva a formatear el disco duro y reinstale el sistema operativo.

-   Restaure el disco duro en el equipo que ejecuta la imagen del secuenciador mediante otro software de creación de imágenes de disco.

En la siguiente lista se describen los requisitos de hardware recomendados para ejecutar el secuenciador de App-V.

### <a href="" id="hardware-requirements-"></a>Requisitos de hardware

-   Procesador: Intel Pentium III, 1 GHz (32 bits o 64 bits). El proceso de secuenciación es un proceso de subproceso único y no aprovecha los procesadores dobles.

-   Memoria: 1GB o superior, se recomiendan 2 GB.

-   Disco duro: 40 gigabytes (GB) de espacio en el disco duro con un mínimo de 15 GB de espacio disponible en el disco duro. Le recomendamos que tenga al menos tres veces el espacio en el disco duro que la aplicación que está secuenciando requiere.

    **Nota:**  La secuenciación requiere mucho uso de disco. Una velocidad de disco rápida puede disminuir el tiempo de secuencia.

     

### Requisitos de software

En la siguiente lista se describen los sistemas operativos compatibles para ejecutar el secuenciador.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Empresa, empresa o Ultimate</p></td>
<td align="left"><p>Sin Service Pack, SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ compatible con App-V 4,5 con SP1 o SP2, y App-V 4,6 solo

**Nota:**  El secuenciador de Application Virtualization (App-V) 4,6 admite las versiones de 32 bits y 64 bits de estos sistemas operativos.

 

Debe configurar los equipos que ejecutan el secuenciador con las mismas aplicaciones que están instaladas en los equipos de destino.

### Requisitos de software para servicios de escritorio remoto

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Virtualización de aplicaciones (App-V) 4,6 para servicios de escritorio remoto admite las versiones de 32 y 64 bits de estos sistemas operativos.

 

## Temas relacionados


[Información general sobre el secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-overview.md)

 

 





