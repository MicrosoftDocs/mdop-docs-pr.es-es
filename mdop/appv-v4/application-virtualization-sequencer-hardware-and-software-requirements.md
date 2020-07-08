---
title: Requisitos de hardware y software del secuenciador de virtualización de aplicaciones
description: Requisitos de hardware y software del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819621"
---
# Requisitos de hardware y software del secuenciador de virtualización de aplicaciones


En este tema se describen los requisitos mínimos de hardware y software recomendados para el equipo que ejecuta el secuenciador de Microsoft Application Virtualization (App-V).

**Importante**  Debe ejecutar el secuenciador de App-V (**SFTSequencer.exe**) con una cuenta que tenga privilegios de administrador debido a los cambios que realiza el secuenciante en el sistema local. Estos cambios pueden incluir la escritura de archivos en el directorio **c:\\Archivos de programa** , la realización de cambios en el registro, el inicio y la detención de servicios, la actualización de los descriptores de seguridad para archivos y el cambio de permisos.

 

Antes de instalar el secuenciador y después de la secuencia de cada aplicación, debe restaurar una imagen de sistema operativo limpia en el equipo de secuenciación. Puede usar uno de los siguientes métodos para restaurar el equipo que ejecuta el secuenciador:

-   Vuelva a formatear el disco duro y reinstale el sistema operativo.

-   Restaure el disco duro en el equipo que ejecuta la imagen del secuenciador mediante otro software de creación de imágenes de disco.

-   Revertir una imagen de sistema operativo virtual, como una imagen de Microsoft Virtual PC. El uso de una máquina virtual permite reutilizar fácilmente los entornos de secuencias limpias con la administración mínima.

En la siguiente lista se describen los requisitos de hardware recomendados para ejecutar el secuenciador de App-V.

Los requisitos se enumeran en primer lugar para Microsoft Application Virtualization (App-V) 4.6 SP2, seguido de los requisitos de las versiones precedidas de App-V 4.6 SP2.

### <a href="" id="hardware-requirements-"></a>Requisitos de hardware

-   Procesador: Intel Pentium III, 1 GHz (32 bits o 64 bits). El proceso de secuenciación es un proceso de subproceso único y no aprovecha los procesadores dobles.

-   Memoria: se recomienda 1 GB o más de 2 GB.

-   Disco duro: 40 gigabytes (GB) de espacio en el disco duro con un mínimo de 15 GB de espacio disponible en el disco duro. Le recomendamos que tenga al menos tres veces el espacio en el disco duro que la aplicación que está secuenciando requiere.

    **Nota:**  La secuenciación requiere mucho uso de disco. Una velocidad de disco rápida puede disminuir el tiempo de secuencia.

     

### Requisitos de software para App-V 4,6 SP2

En la siguiente lista se describen los sistemas operativos compatibles para ejecutar el secuenciador de App-V 4,6 SP2.

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
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Empresa, empresa o Ultimate</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate</p></td>
<td align="left"><p>Sin Service Pack ni SP1</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro o Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Application Virtualization (App-V) 4,6 SP2 Sequencer es compatible con las versiones de 32 y 64 bits de estos sistemas operativos.

 

Debe configurar los equipos que ejecutan el secuenciador con las mismas aplicaciones que están instaladas en los equipos de destino.

### Requisitos de software para las versiones anteriores a App-V 4,6 SP2

En la lista siguiente se describen los sistemas operativos compatibles para ejecutar el secuenciador para las versiones anteriores a la aplicación-V 4,6 SP2.

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

### Requisitos de software para servicios de escritorio remoto para App-V 4,6 SP2

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
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Sin Service Pack ni SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Virtualización de aplicaciones (App-V) 4,6 SP2 para servicios de escritorio remoto admite las versiones de 32 bits y 64 bits de estos sistemas operativos.

 

### Requisitos de software para servicios de escritorio remoto para versiones anteriores a App-V 4,6 SP2

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
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Sin Service Pack ni SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Virtualización de aplicaciones (App-V) 4,6 SP2 para servicios de escritorio remoto admite las versiones de 32 bits y 64 bits de estos sistemas operativos.

 

## Temas relacionados


[Requisitos de hardware y software de cliente de virtualización de aplicaciones](application-virtualization-client-hardware-and-software-requirements.md)

[Requisitos de sistema de virtualización de aplicaciones](application-virtualization-system-requirements.md)

[Cómo instalar el secuenciador de virtualización de aplicaciones](how-to-install-the-application-virtualization-sequencer.md)

[Cómo actualizar el cliente secuenciador de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





