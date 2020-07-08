---
title: Requisitos de sistema de virtualización de aplicaciones
description: Requisitos de sistema de virtualización de aplicaciones
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819520"
---
# Requisitos de sistema de virtualización de aplicaciones


En este tema se describen los requisitos mínimos de hardware y software para el servidor de administración de Microsoft Application Virtualization (App-V) y el servidor de transmisión.

## Administración de virtualización de aplicaciones y servidores de streaming


En la siguiente lista se incluyen los requisitos mínimos de hardware y software recomendados para el servidor de administración de App-V y el servidor de streaming de App-V.

### Requisitos de hardware

-   Procesador: Intel Pentium III, 1 GHz

-   RAM: 512 MB

-   Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido

### Requisitos de software

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
<td align="left"><p>Edición estándar</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edición Enterprise o Datacenter</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edición estándar</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edición Enterprise o Datacenter</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ solo se aplica a App-V 4,5 SP1 y SP2.

## Almacén de datos


En la siguiente lista se incluyen los requisitos mínimos de hardware y software recomendados para el equipo que se usa cuando se instala el almacén de datos en un servidor independiente. El almacén de datos solo es necesario para el servidor de administración de virtualización de aplicaciones.

### Requisitos de hardware

-   Procesador: Intel Pentium III, 850 MHz

-   RAM: 512 MB

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

### Requisitos de software

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
<td align="left"><p>Edición estándar</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edición Enterprise o Datacenter</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edición estándar</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edición Enterprise o Datacenter</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ solo se aplica a App-V 4,5 SP1 y SP2.

-   Base de datos: Microsoft SQL Server2000 SP3a o SP4, SQL Server2005 SP1, SP2 o SP3, o SQL Server2008, sin Service Pack o SP1 ni SQL Server2008 R2 (32 bits o 64 bits)

-   Microsoft Data Access Components: MDAC 2,7

-   Controlador de dominio: servicios de dominio de Active Directory o controlador principal de dominio (PDC) basado en Windows NT 4.0 como autoridad de autenticación central

## Servicio Web de administración


En la siguiente lista se incluyen los requisitos mínimos de hardware y software recomendados para el servicio Web de administración de virtualización de aplicaciones cuando se instala en un equipo independiente.

### Requisitos de hardware

-   Procesador: Intel Pentium III, 800 MHz

-   RAM: 256 MB

-   Espacio en disco: 50 MB de espacio disponible en el disco duro

### Requisitos de software

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
<td align="left"><p>Edición estándar</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edición Enterprise o Datacenter</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edición estándar</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edición Enterprise o Datacenter</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ solo se aplica a App-V 4,5 SP1 y SP2.

-   Servicios de Internet Information Server: servicios de Internet Information Server (IIS) 6,0 configurados con Microsoft ASP.NET, IIS 7

-   Microsoft .NET Framework 2.0

## Consola de administración


La siguiente lista incluye los requisitos mínimos de hardware y software recomendados para la consola de administración de virtualización de aplicaciones cuando se instala en un equipo independiente.

### Requisitos de hardware

-   Procesador: Intel Pentium III, 450 MHz

-   RAM: 256 MB

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

### Requisitos de software

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
<td align="left"><p>Edición profesional</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edición para empresas, empresas o Ultimate</p></td>
<td align="left"><p>Sin Service Pack, SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ solo se aplica a App-V 4,5 SP1 y SP2.

-   Microsoft Management Console: MMC 3.0 o posterior

-   Microsoft .NET Framework 2.0 SP2 (mínimo)

    **Importante**  El requisito mínimo es .NET Framework 2,0 SP2 si debe instalar App-V Hotfix KB980850 o posteriores Hotfix de App-V en el equipo que está ejecutando la consola de administración de App-V.

     

## Temas relacionados


[Requisitos de hardware y software de cliente de virtualización de aplicaciones](application-virtualization-client-hardware-and-software-requirements.md)

[Requisitos de hardware y software del secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Cómo configurar servidores para implementación basada en servidor](how-to-configure-servers-for-server-based-deployment.md)

[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)

[Cómo actualizar los servidores y componentes del sistema](how-to-upgrade-the-servers-and-system-components.md)

 

 





