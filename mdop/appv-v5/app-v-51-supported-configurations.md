---
title: Configuraciones compatibles con App-V 5.1
description: Configuraciones compatibles con App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814726"
---
# Configuraciones compatibles con App-V 5.1

>Se aplica a: Windows 10, versión 1607; Windows Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (actualización de seguridad ampliada)

En este tema se especifican los requisitos para instalar y ejecutar Microsoft Application Virtualization (App-V) 5,1 en su entorno.

## Requisitos del sistema de App-V Server

En esta sección se enumeran los requisitos de sistema operativo y hardware de todos los componentes de servidor de App-V.

### Escenarios de servidor de App-V 5,1 no admitidos

El servidor de App-V 5,1 no admite los siguientes escenarios:

-   Implementación en un equipo que ejecute Microsoft Windows Server Core.

-   Implementación en un equipo que ejecute una versión anterior de los componentes de servidor de App-V 5,1. Puede instalar App-V 5,1 en paralelo solo con el servidor de servidor de streaming ligero (LWS) de App-V 4.5. Implementación de App-V en paralelo con el servidor de App-V 4,5 Application Virtualization Management Service (HWS) no es compatible.

-   Implementación en un equipo que ejecute Microsoft SQL Server Express Edition.

-   Implementación en un controlador de dominio.

-   Rutas cortas. Si tiene pensado usar una ruta corta, debe crear un volumen nuevo.

### Requisitos del sistema operativo del servidor de administración

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de servidor de administración de App-V 5,1.

> [!NOTE]
> Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información, consulte las [preguntas más frecuentes sobre la política de soporte del soporte técnico de Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 | Sistema operativo                 | Service Pack | Arquitectura del sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2|      SP1     |        64 bits       |
 

**Importante**  La implementación de la función del servidor de administración en un equipo con el uso compartido de escritorio remoto (RDS) no es compatible.

 

### <a href="" id="management-server-hardware-requirements-"></a>Requisitos de hardware del servidor de administración

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 1 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido

### Requisitos de la base de datos del servidor de administración

En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de la base de datos de administración de App-V 5,1.

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
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
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

Para obtener más información sobre los archivos de configuración de usuario con SQL Server 2016 o posterior, consulte el [artículo de soporte técnico](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).

### Requisitos del sistema operativo de Publishing Server

En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación del servidor de publicación de App-V 5,1.

| Sistema operativo                 | Service Pack | Arquitectura del sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### <a href="" id="publishing-server-hardware-requirements-"></a>Requisitos de hardware de Publishing Server

App-V no agrega requisitos adicionales más allá de los de Windows Server.

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido

### Requisitos del sistema operativo del servidor de informes

En la siguiente tabla se enumeran los sistemas operativos admitidos para la instalación de servidor de informes de App-V 5,1.

| Sistema operativo                 | Service Pack | Arquitectura del sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### <a href="" id="reporting-server-hardware-requirements-"></a>Requisitos de hardware del servidor de informes

App-V no agrega requisitos adicionales más allá de los de Windows Server.

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

### Requisitos de la base de datos del servidor de informes

En la siguiente tabla se enumeran las versiones de SQL Server compatibles con la instalación de la base de datos de informes de App-V 5,1.

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
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
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

En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de App-V 5,1.

> [!NOTE]
> Con la versión de aniversario de Windows 10 (también conocido como la versión 1607), el cliente de App-V está en el cuadro y bloqueará la instalación de cualquier versión anterior del cliente de App-V.

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
<td align="left"><p>Microsoft Windows10 (versión anterior a 1607)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
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

-   El cliente de servicios de escritorio remoto de App-V 5,1 solo se admite para servidores habilitados para RDS.

### <a href="" id="app-v-client-hardware-requirements-"></a>Requisitos de hardware del cliente de App-V

En la siguiente lista se muestra la configuración de hardware compatible para la instalación de cliente de App-V 5,1.

-   Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)

-   RAM: 1 GB (32 bits) o 2 GB (64 bits)

-   Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.

## Requisitos del sistema del cliente de servicios de escritorio remoto


En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de servicios de escritorio remoto (RDS) de App-V 5,1.

| Sistema operativo                 | Service Pack | Arquitectura del sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### Requisitos de hardware de los clientes de servicios de escritorio remoto

App-V no agrega requisitos adicionales más allá de los de Windows Server.

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

## Requisitos del sistema secuenciador

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de App-V 5,1 Sequencer.

| Sistema operativo                 | Service Pack | Arquitectura del sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |
| Microsoft Windows 10             |              | 32bits y 64bits   |
| Microsoft Windows 8,1            |              | 32bits y 64bits   |
| Microsoft Windows 7              |      SP1     | 32bits y 64bits   |

### Requisitos de hardware del secuenciador

Consulte la documentación de Windows o de Windows Server para conocer los requisitos de hardware. App-V no agrega requisitos de hardware adicionales.

## <a href="" id="bkmk-supp-ver-sccm"></a>Versiones compatibles de System Center Configuration Manager

El cliente de App-V es compatible con las siguientes versiones de System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

En la siguiente matriz de versiones de App-V y System Center Configuration Manager se muestran todas las combinaciones compatibles oficialmente de App-V y administrador de configuración.

> [!NOTE]
> Tanto App-V 4,5 como 4,6 han salido del soporte estándar.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de App-V</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">System Center 2012 Configuration Manager</th>
<th align="left">System Center 2012 Configuration Manager SP1</th>
<th align="left">System Center 2012 R2 Configuration Manager</th>
<th align="left">System Center 2012 R2 Configuration Manager SP1</th>
<th align="left">System Center 2012 Configuration Manager SP2</th>
<th align="left">System Center Configuration Manager versión 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Solo empaquetador MSI</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>5.1 de App-V</p></td>
<td align="left"><p>Solo empaquetador MSI</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre cómo Configuration Manager se integra con App-V, consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).

## Temas relacionados

[Planificación de la implementación de App-V](planning-to-deploy-app-v51.md)

[Requisitos previos de App-V 5.1](app-v-51-prerequisites.md)
