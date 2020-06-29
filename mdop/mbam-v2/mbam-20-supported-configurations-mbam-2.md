---
title: Configuraciones admitidas de MBAM 2.0
description: Configuraciones admitidas de MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823910"
---
# Configuraciones admitidas de MBAM 2.0


En este tema se especifican los requisitos para instalar y ejecutar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 en su entorno mediante la topología independiente. Para obtener información sobre las configuraciones compatibles que se aplican a versiones posteriores, consulte la documentación de la versión correspondiente.

Si tiene previsto instalar MBAM 2,0 mediante la topología del administrador de configuración y desea revisar una lista de los requisitos del sistema, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

La configuración recomendada para ejecutar MBAM en un entorno de producción es con dos servidores, en función de los requisitos de escalabilidad. Esta configuración admite hasta 200.000 clientes MBAM. Para obtener una imagen y descripciones de la infraestructura de servidor de MBAM independiente, consulte [arquitectura de alto nivel para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

## <a href="" id="---------mbam-server-system-requirements"></a> Requisitos del sistema de MBAM Server


### Requisitos del sistema operativo del servidor

En la tabla siguiente se enumeran los sistemas operativos que se admiten en la instalación del servidor de administración y supervisión de Microsoft BitLocker.

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
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Standard o Datacenter Edition</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  No se admite la instalación de servicios de MBAM, informes o bases de datos en un equipo controlador de dominio.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>Requisitos de procesador de servidor, RAM y espacio en disco

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Encargado del tratamiento de datos</p></td>
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

 

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de la base de datos de SQLServer

En la tabla siguiente se enumeran las versiones de SQLServer admitidas para la instalación de características de servidor de administración y supervisión, que incluye la base de datos de recuperación, la base de datos de cumplimiento y auditoría, y los informes de auditoría y cumplimiento. Además, las bases de datos requieren la instalación de las herramientas de administración de SQL Server.

**Nota:**  MBAM no es compatible de forma nativa con los grupos de clústeres, reflejos o disponibilidad de SQL. Para instalar las bases de datos, debe ejecutar la instalación del servidor de MBAM en un servidor SQL Server independiente.

 

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
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Encargado del tratamiento de datos</p></td>
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

 

## <a href="" id="---------mbam-client-system-requirements"></a> Requisitos del sistema para el cliente de MBAM


### Requisitos del sistema operativo del cliente

En la tabla siguiente se enumeran los sistemas operativos compatibles con la instalación del cliente de supervisión y administración de Microsoft BitLocker.

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
<td align="left"><p>7</p></td>
<td align="left"><p>Edición Enterprise o Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Edición Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8 Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>Requisitos de RAM de cliente

No hay requisitos de RAM específicos de la instalación del cliente de supervisión y administración de Microsoft BitLocker.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Requisitos del sistema de la Directiva de grupo MBAM


En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de la plantilla Directiva de Grupo administración y supervisión de Microsoft BitLocker.

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
<td align="left"><p>7</p></td>
<td align="left"><p>Enterprise o Ultimate Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Edición Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Planificación de la implementación de MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Requisitos previos de implementación de MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





