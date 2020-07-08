---
title: Requisitos de hardware y software de cliente de virtualización de aplicaciones
description: Requisitos de hardware y software de cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819731"
---
# Requisitos de hardware y software de cliente de virtualización de aplicaciones


En este tema se describe la configuración mínima recomendada de hardware y software para la instalación del cliente de escritorio de virtualización de aplicaciones y el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server).

## Cliente de escritorio de virtualización de aplicaciones


En la siguiente lista se incluyen los requisitos mínimos de hardware y software recomendados para el cliente de escritorio de virtualización de aplicaciones. Los requisitos se enumeran en primer lugar para Microsoft Application Virtualization (App-V) 4.6 SP2, seguido de los requisitos de las versiones precedidas de App-V 4.6 SP2.

**Nota:**  El cliente de escritorio de Application Virtualization (App-V) no requiere recursos de RAM o de procesador adicionales más allá de los requisitos del sistema operativo host.

 

### Requisitos de hardware

Los requisitos de hardware son aplicables a todas las versiones.

-   Procesador: Consulte los requisitos del sistema recomendados para el sistema operativo que está usando.

-   RAM: Consulte los requisitos del sistema recomendados para el sistema operativo que está usando.

-   Disco: 30 MB para la instalación y 6 GB para la caché.

### Requisitos de software para App-V 4,6 SP2

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
<th align="left">SKU de arquitectura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edición profesional</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edición para empresas, empresas o Ultimate</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate Edition</p></td>
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

Los siguientes requisitos previos de software se instalan automáticamente si usas el método Setup.exe. Si está usando el programa de instalación de Setup.msi, primero debe instalar los siguientes productos.
- **Microsoft Visual c++ 2005 SP1 Redistributable Package (x86)**: para obtener más información sobre la instalación de Microsoft visual C++ 2005 SP1 Redistributable Package (x86), consulte [microsoft visual c++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Para la versión 4,5 SP2 del cliente de App-V, descargue Vcredist\_x86.exe de [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package Update de seguridad ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .
  -   **Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)**: para obtener más información sobre la instalación de Microsoft Core XML Services (msxml) 6,0 SP1 (x86), consulte [Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

Para el cliente de escritorio de Application Virtualization (App-V) 4,6, se instala automáticamente el siguiente requisito previo de software adicional si usa el método Setup.exe. Si está usando el programa de instalación de Setup.msi, también debe instalarlo con los otros requisitos previos que se indican.

-   **Microsoft VisualC + + 2008SP1 Redistributable Package (x86)**: para obtener más información sobre la instalación de Microsoft VisualC + + 2008 SP1 Redistributable Package (x86), consulte [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Requisitos de software para las versiones anteriores a App-V 4,6 SP2

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
<th align="left">SKU de arquitectura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edición profesional</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edición para empresas, empresas o Ultimate</p></td>
<td align="left"><p>Sin Service Pack, SP1 o SP2</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate Edition</p></td>
<td align="left"><p>Sin Service Pack ni SP1</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
</tbody>
</table>
¹ compatible con App-V 4,5 SP1 y SP2, App-V 4,6 y 4,6 SP1 solo

El cliente de escritorio de Application Virtualization (App-V) 4,6 admite SKU de x86 y x64 de estos sistemas operativos.

Los siguientes requisitos previos de software se instalan automáticamente si usas el método Setup.exe. Si está usando el programa de instalación de Setup.msi, primero debe instalar los siguientes productos.

-   <strong>Microsoft Visual C++ 2005 SP1 Redistributable Package (x86) </strong> : para obtener más información sobre la instalación de Microsoft Visual c++ 2005 SP1 Redistributable Package (x86), consulte <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> Microsoft visual C++ 2005 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> ). Para la versión 4,5 SP2 del cliente de App-V, descargue Vcredist_x86.exe de <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package Update de seguridad ATL </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> ).

-   <strong>Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </strong> : para obtener más información sobre la instalación de Microsoft Core XML Services (MSXML) 6,0 SP1 (x86), consulte <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> Microsoft Core XML Services (msxml) 6,0 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> ).

-   <strong>Informes de errores de aplicaciones de Microsoft </strong> : el programa de instalación para este software está incluido en la <strong> </strong> carpeta Support\Watson en el archivo de extracción automática.

Para el cliente de escritorio de Application Virtualization (App-V) 4,6, se instala automáticamente el siguiente requisito previo de software adicional si usa el método Setup.exe. Si está usando el programa de instalación de Setup.msi, también debe instalarlo con los otros requisitos previos que se indican.

-   <strong>Microsoft Visual C++ 2008 SP1 Redistributable Package (x86) </strong> : para obtener más información sobre la instalación de Microsoft Visual c++ 2008 SP1 Redistributable Package (x86), consulte <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> Microsoft visual C++ 2008 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> ).

## Cliente de virtualización de aplicaciones para servicios de escritorio remoto

Estos son los requisitos de hardware y software recomendados para el cliente de virtualización de aplicaciones para servicios de escritorio remoto. Los requisitos se enumeran en primer lugar para appv461_3, seguidos de los requisitos de las versiones precedidas de App-V 4,6 SP2.

El cliente de Application Virtualization (App-V) para servicios de escritorio remoto no requiere más recursos de procesador o RAM más allá de los requisitos del sistema operativo host.

### Requisitos de hardware

Los requisitos de hardware son aplicables a todas las versiones.

-   Procesador: Consulte los requisitos del sistema recomendados para el sistema operativo que está usando.

-   RAM: Consulte los requisitos del sistema recomendados para el sistema operativo que está usando. Estos requisitos también dependen del número de usuarios y aplicaciones.

-   Disco: 30 MB para la instalación y 6 GB para la caché.

### Requisitos de software para App-V 4,6 SP2

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
<th align="left">SKU de arquitectura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 y x64</p></td>
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
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Los siguientes requisitos previos de software se instalan automáticamente si usas el método Setup.exe. Si está usando el programa de instalación de Setup.msi, primero debe instalar los siguientes productos.

-   **Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**: para obtener más información sobre la instalación de Microsoft VisualC + + 2005 SP1 Redistributable Package (x86), consulte [Microsoft VisualC + + 2005 SP1](https://go.microsoft.com/fwlink/?LinkId=119961) Redistributable Package (x86) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Para la versión 4.5 SP2 del cliente de App-V, descargue Vcredist\_x86.exe de [Microsoft Visual C++ 2005 Service Pack 1 paquete redistribuible Update de seguridad ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .

-   **Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)**: para obtener más información sobre la instalación de Microsoft Core XML Services (MSXML) 6.0 SP1 (x86), consulte [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Informes de errores de aplicaciones de Microsoft**: el programa de instalación para este software está incluido en la carpeta **Support\\Watson** en el archivo de extracción automática.

Para el cliente de escritorio de Application Virtualization (App-V) 4,6, se instala automáticamente el siguiente requisito previo de software adicional si usa el método Setup.exe. Si está usando el programa de instalación de Setup.msi, también debe instalarlo con los otros requisitos previos que se indican.

-   **Microsoft VisualC + + 2008SP1 Redistributable Package (x86)**: para obtener más información sobre la instalación de Microsoft VisualC + + 2008 SP1 Redistributable Package (x86), consulte [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Requisitos de software para las versiones anteriores a App-V 4,6 SP2

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
<th align="left">SKU de arquitectura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Sin Service Pack ni SP2</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 y x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Sin Service Pack ni SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

El cliente de Application Virtualization (App-V) 4,6 para servicios de escritorio remoto es compatible con SKU de x86 y x64 de estos sistemas operativos.

## Temas relacionados
- [Requisitos de hardware y software del secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Requisitos de sistema de virtualización de aplicaciones](application-virtualization-system-requirements.md)
- [Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)
- [Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)
- [Cómo actualizar el cliente de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-client.md)
