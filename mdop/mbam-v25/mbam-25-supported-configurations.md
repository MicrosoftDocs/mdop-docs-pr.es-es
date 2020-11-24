---
title: Configuraciones admitidas de MBAM 2.5
description: Configuraciones admitidas de MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182932"
---
# Configuraciones admitidas de MBAM 2.5


Puede ejecutar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 en una topología independiente o en una topología de integración de Configuration Manager que integre MBAM con System Center Configuration Manager. Si usa la configuración recomendada para cualquiera de las topologías en un entorno de producción, MBAM admite hasta 500.000 clientes de MBAM. Para obtener información sobre la arquitectura y las características recomendadas que se configuran en cada servidor para cada topología, consulte [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).

Para obtener configuraciones adicionales específicas de la topología de integración de Configuration Manager, consulte [las versiones de Configuration Manager que admite MBAM](#bkmk-cm-ramreqs).

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)



## Idiomas admitidos en MBAM


En las tablas siguientes se muestran los idiomas admitidos para el cliente MBAM (incluido el Self-Service portal) y el servidor MBAM en MBAM 2,5 y MBAM 2,5 SP1.

**Idiomas admitidos en MBAM 2,5 SP1:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Idiomas de cliente</th>
<th align="left">Idiomas del servidor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Checo (República Checa) CS-CZ</p>
<p>Danés (Dinamarca) da-DK</p>
<p>Neerlandés (Países Bajos) nl-NL</p>
<p>Inglés (Estados Unidos) en-EE.UU.</p>
<p>Finés (Finlandia) fi-FI</p>
<p>Francés (Francia) fr-FR</p>
<p>Alemán (Alemania) de-DE</p>
<p>Griego (Grecia) el-GR</p>
<p>Húngaro (Hungría) Hu-HU</p>
<p>Italiano (Italia) ti</p>
<p>Japonés (Japón) ja-JP</p>
<p>Coreano ko-KR</p>
<p>Noruego, Bokmål (Noruega) NB-NO</p>
<p>Polaco (Polonia) PL: PL</p>
<p>Portugués (Brasil) pt-BR</p>
<p>Portugués (Portugal) pt-PT</p>
<p>Ruso (Rusia) ru-RU</p>
<p>República Eslovaca (Eslovaquia) SK-SK</p>
<p>Español (España) es-ES</p>
<p>Sueco (Suecia) VP-SE</p>
<p>Turco (Turquía) tr-TR</p>
<p>Esloveno (Eslovenia) SL-SI</p>
<p>Chino simplificado (PRC) zh-CN</p>
<p>Chino tradicional (Taiwán) zh-TW</p></td>
<td align="left"><ul>
<li><p>Inglés (Estados Unidos) en-EE.UU.</p></li>
<li><p>Francés (Francia) fr-FR</p></li>
<li><p>Alemán (Alemania) de-DE</p></li>
<li><p>Italiano (Italia) ti</p></li>
<li><p>Japonés (Japón) ja-JP</p></li>
<li><p>Coreano ko-KR</p></li>
<li><p>Portugués (Brasil) pt-BR</p></li>
<li><p>Ruso (Rusia) ru-RU</p></li>
<li><p>Español (España) es-ES</p></li>
<li><p>Chino simplificado (PRC) zh-CN</p></li>
<li><p>Chino tradicional (Taiwán) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Idiomas admitidos en MBAM 2,5:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Idiomas de cliente</th>
<th align="left">Idiomas del servidor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Inglés (Estados Unidos) en-EE.UU.</p></li>
<li><p>Francés (Francia) fr-FR</p></li>
<li><p>Alemán (Alemania) de-DE</p></li>
<li><p>Italiano (Italia) ti</p></li>
<li><p>Japonés (Japón) ja-JP</p></li>
<li><p>Coreano ko-KR</p></li>
<li><p>Portugués (Brasil) pt-BR</p></li>
<li><p>Ruso (Rusia) ru-RU</p></li>
<li><p>Español (España) es-ES</p></li>
<li><p>Chino simplificado (PRC) zh-CN</p></li>
<li><p>Chino tradicional (Taiwán) zh-TW</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Inglés (Estados Unidos) en-EE.UU.</p></li>
<li><p>Francés (Francia) fr-FR</p></li>
<li><p>Alemán (Alemania) de-DE</p></li>
<li><p>Italiano (Italia) ti</p></li>
<li><p>Japonés (Japón) ja-JP</p></li>
<li><p>Coreano ko-KR</p></li>
<li><p>Portugués (Brasil) pt-BR</p></li>
<li><p>Ruso (Rusia) ru-RU</p></li>
<li><p>Español (España) es-ES</p></li>
<li><p>Chino simplificado (PRC) zh-CN</p></li>
<li><p>Chino tradicional (Taiwán) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> Requisitos del sistema de MBAM Server


### Requisitos del sistema operativo del servidor de MBAM

Le recomendamos encarecidamente que ejecute el cliente MBAM y MBAM Server en la misma línea de sistemas operativos. Por ejemplo, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación del servidor MBAM.

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
<td align="left"><p>Windows Server 2019</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsServer2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



El dominio de la empresa debe contener al menos un controlador de dominio de Windows Server 2008 (o posterior).

### <a href="" id="bkmk-stand-alone-ramreqs"></a>Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server: topología independiente

Estos requisitos son para la topología independiente MBAM. Para conocer los requisitos de la topología de integración de Configuration Manager, consulte [requisitos del procesador de servidor de MBAM, RAM y espacio en disco: topología de integración de Configuration Manager](#bkmk-cm-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Procesador</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o más</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espacio libre en el disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a>Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server: topología de integración de Configuration Manager

En la siguiente tabla se enumeran los requisitos de procesador, RAM y espacio de disco del servidor para los servidores de MBAM cuando se usa la topología de integración de Configuration Manager. Para conocer los requisitos de la topología independiente, consulte requisitos del [procesador, la memoria RAM y el espacio de disco de MBAM Server: topología independiente](#bkmk-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Procesador</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o más</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espacio libre en el disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>Versiones de Configuration Manager compatibles con MBAM

MBAM es compatible con las siguientes versiones de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión compatible</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (rama actual), versiones de hasta 1902</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (LTSB-versión 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrador de configuración de Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 o posterior</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p>

&gt;<strong>Nota </strong> aunque Configuration Manager 2007 R2 es de 32 bits, debe instalarlo y SQL Server en un sistema operativo de 64 bits para que coincida con el software de MBAM de 64 bits.
</td>
</tr>
</tbody>
</table>



Para obtener una lista de las configuraciones admitidas para el servidor de Configuration Manager, consulte la documentación de TechNet correspondiente a la versión de Configuration Manager que está usando. MBAM no tiene requisitos de sistema adicionales para el servidor de Configuration Manager.

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de bases de datos de SQL Server

En la siguiente tabla se enumeran las versiones de Microsoft SQL Server que son compatibles con las características de servidor de MBAM, que incluyen la base de datos de recuperación, la base de datos de cumplimiento y auditoría, y la característica de informes. Las versiones necesarias se aplican a las topologías independientes o de integración de Configuration Manager.

Debe instalar SQL Server con la \ **_Latin1 \ _General \ _CP1 \ _CI \ _AS** intercalación.

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
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64 bits</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bits</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64 bits</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard o Enterprise</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

**Nota**  
MBAM tiene un nivel de compatibilidad máximo admitido de 140. El nivel de compatibilidad predeterminado para las nuevas bases de datos creadas en SQL Server 2019 es 150, que se debe modificar a 140 o inferior, mediante el comando ALTER DATABASE, después de crear la base de datos. Las bases de datos existentes migradas de SQL Server 2017 o versiones anteriores se conservarán en el nivel de compatibilidad anterior y no es necesario modificarlas.

Para admitir SQL 2016 debe instalar la versión de servicio de marzo de 2017 para MDOP https://www.microsoft.com/download/details.aspx?id=54967  y para admitir sql 2017 debe instalar la versión de lanzamiento de julio de 2018 para MDOP https://www.microsoft.com/download/details.aspx?id=57157 . En general, mantente al día siempre con la actualización de servicio más reciente, ya que también incluye todas las características de soluciones y las nuevas.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>Requisitos de procesador, memoria RAM y espacio en disco de SQL Server: topología independiente

En la tabla siguiente se enumeran los requisitos de procesador de servidor, RAM y espacio de disco recomendados para el equipo con SQL Server cuando está usando la topología independiente. Use estos requisitos como guía. Sus requisitos específicos variarán en función de la cantidad de equipos cliente que sean compatibles con su empresa. Para ver los requisitos de la topología de integración de Configuration Manager, consulte [requisitos de procesador, RAM y espacio en disco de SQL Server: topología de integración de Configuration Manager](#bkmk-cm-sql-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Procesador</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o más</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espacio libre en el disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB o más</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a>Requisitos de procesador, RAM y espacio en disco de SQL Server: topología de integración de Configuration Manager

En la tabla siguiente se enumeran los requisitos de procesador, RAM y espacio de disco del servidor de Microsoft SQL Server cuando se usa la topología de integración de Configuration Manager, consulte [requisitos de procesador, memoria RAM y espacio en disco de SQL Server: topología independiente](#bkmk-sql-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Procesador</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o más</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espacio libre en el disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Requisitos del sistema para el cliente de MBAM


### Requisitos del sistema operativo del cliente

Le recomendamos encarecidamente que ejecute el cliente MBAM y MBAM Server en la misma línea de sistemas operativos. Por ejemplo, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de cliente de MBAM. Los mismos requisitos se aplican a las topologías independientes y de integración de Configuration Manager.

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
<tr class="even">
    <td align="left"><p>Windows 10 IoT</p></td>
    <td align="left"><p>Empresas</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32 o 64 bits</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Empresas</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Empresas</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Empresa o Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8,1 y Windows 10 Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Requisitos de RAM de cliente

No hay requisitos de RAM específicos para la instalación del cliente de MBAM.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Requisitos del sistema de la Directiva de grupo MBAM


En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de plantillas de directiva de grupo de MBAM.

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
 <tr class="even">
      <td align="left"><p>Windows 10 IoT</p></td>
      <td align="left"><p>Empresas</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32 o 64 bits</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Empresas</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Empresas</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise o Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

## MBAM en IaaS de Azure

El servidor de MBAM se puede implementar en la infraestructura de Azure como servicio (IaaS) en cualquiera de las versiones de sistema operativo compatibles enumeradas anteriormente, conectándose a un Active Directory hospedado en una ubicación local o a un Active Directory hospedado también en IaaS de Azure.  [Aquí](https://msdn.microsoft.com/library/azure/jj156090.aspx)está la documentación para configurar y configurar Active Directory en IaaS de Azure.

El cliente MBAM no es compatible con las máquinas virtuales y tampoco se admite en IaaS de Azure.


## Versiones de servicio 

- [Hotfix 2016 de abril](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [2016 de septiembre](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [Diciembre de 2016](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [Marzo de 2017](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [Junio de 2017](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [Septiembre de 2017](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [Marzo de 2018](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2018 de julio](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2019 de mayo](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## Temas relacionados


[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

[Preparación del entorno para MBAM 2.5](preparing-your-environment-for-mbam-25.md)




## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




