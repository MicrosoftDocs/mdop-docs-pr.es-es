---
title: Configuraciones admitidas de App-V 5.0 SP3
description: Configuraciones admitidas de App-V 5.0 SP3
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814791"
---
# Configuraciones admitidas de App-V 5.0 SP3


En este tema se especifican los requisitos para instalar y ejecutar Microsoft Application Virtualization (App-V) 5,0 SP3 en su entorno.

## Requisitos del sistema de App-V Server


En esta sección se enumeran los requisitos de sistema operativo y hardware de todos los componentes de servidor de App-V.

### Escenarios de servidor de App-V 5,0 SP3 no admitidos

El servidor de App-V 5,0 SP3 no admite los siguientes escenarios:

-   Implementación en un equipo que ejecute Microsoft Windows Server Core.

-   Implementación en un equipo que ejecute una versión anterior de los componentes del servidor de App-V 5,0 SP3. Puede instalar App-V 5,0 SP3 en paralelo solo con el servidor de servidor de transmisión ligero de App-V 4.5 (LWS). Implementación de App-V en paralelo con el servidor de App-V 4,5 Application Virtualization Management Service (HWS) no es compatible.

-   Implementación en un equipo que ejecute Microsoft SQL Server Express Edition.

-   Implementación remota de la base de datos del servidor de administración o de la base de datos de informes. Debe ejecutar el instalador directamente en el equipo que ejecuta Microsoft SQL Server.

-   Implementación en un controlador de dominio.

-   Rutas cortas. Si tiene pensado usar una ruta corta, debe crear un volumen nuevo.

### Requisitos del sistema operativo del servidor de administración

En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación del servidor de administración de App-V 5,0 SP3.

**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información, consulte las [preguntas más frecuentes sobre la política de soporte del soporte técnico de Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

**Importante**  La implementación de la función del servidor de administración en un equipo con el uso compartido de escritorio remoto (RDS) no es compatible.

 

### <a href="" id="management-server-hardware-requirements-"></a>Requisitos de hardware del servidor de administración

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 1 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido

### Requisitos de la base de datos del servidor de administración

En la siguiente tabla se enumeran las versiones de SQL Server compatibles con la instalación de la base de datos de administración de App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>

 

### Requisitos del sistema operativo de Publishing Server

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación del servidor de publicación de App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a>Requisitos de hardware de Publishing Server

App-V no agrega requisitos adicionales más allá de los de Windows Server.

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido

### Requisitos del sistema operativo del servidor de informes

En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del servidor de informes de App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a>Requisitos de hardware del servidor de informes

App-V no agrega requisitos adicionales más allá de los de Windows Server.

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

### Requisitos de la base de datos del servidor de informes

En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de la base de datos de informes de App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>Requisitos del sistema para el cliente de App-V


En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación del cliente de App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>

 

Los siguientes escenarios de instalación de cliente de App-V no son compatibles, excepto como se indica:

-   Equipos que ejecutan Windows Server

-   Equipos que ejecutan App-V 4.6 SP1 o versiones anteriores

-   El cliente de servicios de escritorio remoto de App-V 5,0 SP3 solo es compatible con servidores habilitados para RDS.

### <a href="" id="app-v-client-hardware-requirements-"></a>Requisitos de hardware del cliente de App-V

La siguiente lista muestra la configuración de hardware compatible para la instalación del cliente de App-V 5,0 SP3.

-   Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)

-   RAM: 1 GB (32 bits) o 2 GB (64 bits)

-   Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.

## Requisitos del sistema del cliente de servicios de escritorio remoto


En la siguiente tabla, se enumeran los sistemas operativos que son compatibles con la instalación del cliente de servicios de escritorio remoto (RDS) de App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

### Requisitos de hardware de los clientes de servicios de escritorio remoto

App-V no agrega requisitos adicionales más allá de los de Windows Server.

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

## Requisitos del sistema secuenciador


En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de App-V 5,0 SP3 Sequencer.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2012 R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
</tbody>
</table>

 

### Requisitos de hardware del secuenciador

Consulte la documentación de Windows o de Windows Server para conocer los requisitos de hardware. App-V no agrega requisitos de hardware adicionales.

## <a href="" id="bkmk-supp-ver-sccm"></a>Versiones compatibles de System Center Configuration Manager


El cliente de App-V es compatible con las siguientes versiones de System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

Para obtener más información sobre cómo Configuration Manager se integra con App-V, consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v.md)

[Requisitos previos de App-V 5.0 SP3](app-v-50-sp3-prerequisites.md)

 

 





