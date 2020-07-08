---
title: Configuraciones admitidas de MED-V 1.0 SP1
description: Configuraciones admitidas de MED-V 1.0 SP1
author: dansimp
ms.assetid: 4dcf37c4-a061-43d2-878c-28efc87c3cdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5a707e8a3d59a423308f9f735ff38df9e235fbf5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824170"
---
# Configuraciones admitidas de MED-V 1.0 SP1


En este tema se especifican los requisitos necesarios para instalar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 Service Pack 1 (SP1) en su entorno.

## Requisitos del sistema para clientes de MED-V 1,0 SP1


### Requisitos del sistema operativo de cliente MED-V

En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación del cliente MED-V 1,0 SP1.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte el ciclo de vida de los [Service Pack compatibles](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva Microsoft support Lifecycle support](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



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
<td align="left"><p>Empresa, empresa o Ultimate</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
</tbody>
</table>



**Nota**  
El cliente MED-V no se ejecuta en modo x64 nativo. En su lugar, MED-V se ejecuta en modo Windows en Windows 64-bit (WOW64) en equipos de 64 bits.



En la siguiente tabla se enumeran las RAM mínimas necesarias para cada sistema operativo compatible con MED-V 1,0 SP1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">RAM mínima requerida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows XP Professional</p></td>
<td align="left"><p>1 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 x86</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7 x64</p></td>
<td align="left"><p>3 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-client-configuration-"></a>Configuración de cliente de MED-V 1,0 SP1

**Versión de .NET Framework**

Las siguientes versiones de Microsoft .NET Framework son compatibles con la instalación del cliente MED-V 1,0 SP1:

-   .NET Framework 2,0 o .NET Framework 2,0 SP1

-   .NET Framework 3,0 o .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Motor de virtualización**

Microsoft Virtual PC 2007 SP1 con la revisión que se describe en el artículo 974918 de Microsoft Knowledge base es compatible con la instalación del cliente MED-V 1,0 SP1 en las siguientes configuraciones:

-   Archivo de disco duro virtual estático (VHD)

-   Varios archivos VHD ubicados en el mismo directorio

-   Archivo VHD dinámico

**Explorador de Internet**

Windows Internet Explorer 7 y Windows Internet Explorer 8 son compatibles con la instalación del cliente MED-V 1,0 SP1.

**Microsoft Hyper-V Server**

El cliente de MED-V no es compatible en un entorno de Microsoft Hyper-V Server.

## Requisitos del sistema del área de trabajo de MED-V 1,0 SP1


MED-V 1,0 SP1 introduce los cambios en los requisitos del sistema de los de MED-V 1,0.

### Requisitos del sistema operativo de área de trabajo MED-V

En la siguiente tabla se enumeran los sistemas operativos compatibles con las áreas de trabajo de MED-V 1,0 SP1.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte el ciclo de vida de los [Service Pack compatibles](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva Microsoft support Lifecycle support](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



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



### <a href="" id="med-v-1-0-sp1-workspace-configuration-"></a>Configuración del área de trabajo de MED-V 1,0 SP1

**Versión de .NET Framework**

MED-V necesita una de las siguientes versiones compatibles de la instalación del área de trabajo de Microsoft .NET Framework para MED-V 1,0 SP1:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Nota**  
Recomendamos .NET Framework 3,5 SP1 para garantizar que el área de trabajo de MED-V sea compatible con las versiones futuras de MED-V.



**Explorador de Internet**

Windows Internet Explorer 6 SP2 y Windows Internet Explorer 7 son compatibles con la instalación del área de trabajo MED-V 1,0 SP1.

### <a href="" id="med-v-workspace-images-"></a>Imágenes del área de trabajo de MED-V

Las imágenes del área de trabajo de MED-V deben crearse con Virtual PC 2007 SP1.

## Requisitos del sistema para el servidor MED-V 1,0 SP1


MED-V 1,0 SP1 introduce los cambios en los requisitos del sistema de los de MED-V 1,0.

### Requisitos del sistema operativo de servidor MED-V 1,0

En la siguiente tabla se enumeran los sistemas operativos compatibles con las instalaciones de servidor MED-V 1,0 SP1.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte el ciclo de vida de los [Service Pack compatibles](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva Microsoft support Lifecycle support](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



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
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>X86 o x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard o Enterprise</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-server-configuration-"></a>Configuración del servidor MED-V 1,0 SP1

**Versión de .NET Framework**

MED-V necesita una de las siguientes versiones compatibles de la instalación del área de trabajo de Microsoft .NET Framework para MED-V 1,0 SP1:

-   .NET Framework 2,0 o .NET Framework 2,0 SP1

-   .NET Framework 3,0 o .NET Framework 3,0 SP1

-   .NET Framework 3,5 o .NET Framework 3,5 SP1

**Versión de Microsoft SQL Server**

Las siguientes versiones de Microsoft SQL Server son compatibles con MED-V 1,0 SP1 cuando SQL Server se instala de forma local o remota desde el servidor MED-V 1,0 SP1:

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

## Información de globalización de MED-V 1,0 SP1


Si bien MED-V no se ha publicado en idiomas que no sean el inglés, las versiones de idioma del sistema operativo Windows son compatibles con las instalaciones del cliente, el área de trabajo y el servidor MED-V 1,0:

-   Inglés

-   Francés

-   Alemán

-   Italiano

-   Español

-   Portugués (Brasil)

-   Neerlandés (Países Bajos)

-   Japonés









