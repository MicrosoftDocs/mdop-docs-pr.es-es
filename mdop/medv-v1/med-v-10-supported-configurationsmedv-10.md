---
title: Configuraciones admitidas de MED-V 1.0
description: Configuraciones admitidas de MED-V 1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812607"
---
# Configuraciones admitidas de MED-V 1.0


En este tema se especifican los requisitos necesarios para instalar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 en su entorno.

## Requisitos del sistema para el cliente de MED-V 1,0


### Requisitos del sistema operativo de cliente MED-V

En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación del cliente MED-V 1,0.

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
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Edición profesional</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edición para empresas, empresas o Ultimate</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



**Nota**  
El cliente MED-V no se ejecuta en modo x64 nativo. En su lugar, MED-V se ejecuta en modo Windows en Windows 64-bit (WOW64) en equipos de 64 bits.



### <a href="" id="med-v-1-0-client-configuration-"></a>Configuración de cliente MED-V 1,0

**Versión de .NET Framework**

Las siguientes versiones de Microsoft .NET Framework son compatibles con la instalación del cliente MED-V 1,0:

-   .NET Framework 2,0 o .NET Framework 2,0 SP1

-   .NET Framework 3,0 o .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Motor de virtualización**

Microsoft Virtual PC 2007 SP1 con la revisión que se describe en el artículo 974918 de Microsoft Knowledge base es compatible con la instalación del cliente MED-V 1,0 en las siguientes configuraciones:

-   Archivo de disco duro virtual estático (VHD)

-   Varios archivos VHD ubicados en el mismo directorio

-   Archivo VHD dinámico

**Explorador de Internet**

Windows Internet Explorer 7 y Windows Internet Explorer 8 son compatibles con la instalación del cliente MED-V 1,0.

**Microsoft Hyper-V Server**

El cliente de MED-V no es compatible en un entorno de Microsoft Hyper-V Server.

## Requisitos del sistema del área de trabajo MED-V 1,0


### Requisitos del sistema operativo de área de trabajo MED-V

En la siguiente tabla se enumeran los sistemas operativos compatibles con las áreas de trabajo de MED-V 1,0.

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
<td align="left"><p>Windows 2000</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>Pack</p></td>
<td align="left"><p>Microprocesador</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Edición profesional</p></td>
<td align="left"><p>SP2 o SP3</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se recomienda usar SP3 para garantizar que el área de trabajo de MED-V sea compatible con versiones futuras de MED-V.</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a>Configuración del área de trabajo MED-V 1,0

**Versión de .NET Framework**

MED-V necesita una de las siguientes versiones compatibles de la instalación del área de trabajo de Microsoft .NET Framework para MED-V 1,0:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Nota**  
Se recomienda .NET Framework 3,5 SP1 para asegurarse de que el área de trabajo MED-V sea compatible con versiones futuras de MED-V.



**Explorador de Internet**

Windows Internet Explorer 6 SP2 y Windows Internet Explorer 7 son compatibles con la instalación del área de trabajo MED-V 1,0.

### <a href="" id="med-v-workspace-images-"></a>Imágenes del área de trabajo de MED-V

Las imágenes del área de trabajo de MED-V deben crearse con Virtual PC 2007 SP1.

## Requisitos del sistema para el servidor MED-V 1,0


### Requisitos del sistema operativo de servidor MED-V 1,0

En la siguiente tabla se enumeran los sistemas operativos compatibles con las instalaciones de servidor MED-V 1,0.

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
<td align="left"><p>WindowsServer2008</p></td>
<td align="left"><p>Standard o Enterprise</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a>Configuración del servidor MED-V 1,0

**Versión de .NET Framework**

MED-V necesita una de las siguientes versiones compatibles de la instalación del área de trabajo de Microsoft .NET Framework para MED-V 1,0:

-   .NET Framework 2,0 o .NET Framework 2,0 SP1

-   .NET Framework 3,0 o .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Versión de Microsoft SQL Server**

Las siguientes versiones de Microsoft SQL Server son compatibles con MED-V 1,0 cuando SQL Server se instala de forma local o remota desde el servidor MED-V 1,0:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de SQL Server</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2005 de SQL Server</p></td>
<td align="left"><p>Express, Standard o Enterprise Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>2008 de SQL Server</p></td>
<td align="left"><p>Express, Standard o Enterprise</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

El servidor MED-V es compatible con un entorno de Microsoft Hyper-V Server.

## Información de globalización de MED-V 1,0


Aunque MED-V no se ha publicado en idiomas que no sean el inglés, las instalaciones del cliente, el área de trabajo y los servidores de Windows MED-V 1,0 son compatibles con las siguientes versiones de idioma del sistema operativo Windows:

-   Inglés

-   Francés

-   Alemán

-   Italiano

-   Español

-   Portugués (Brasil)









