---
title: Configuraciones admitidas de MBAM 1.0
description: Configuraciones admitidas de MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825940"
---
# Configuraciones admitidas de MBAM 1.0


En este tema se especifican los requisitos necesarios para instalar y ejecutar la administración y supervisión de Microsoft BitLocker (MBAM) en su entorno.

## <a href="" id="---------mbam-server-system-requirements"></a> Requisitos del sistema de MBAM Server


### Requisitos del sistema operativo del servidor

En la tabla siguiente se enumeran los sistemas operativos que se admiten en la instalación del servidor de administración y supervisión de Microsoft BitLocker.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Standard, Enterprise, Datacenter o Web Server</p></td>
<td align="left"><p>Solo SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o Web Server</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



**Advertencia**  
No se admite la instalación de servicios de MBAM, informes o bases de datos en un equipo controlador de dominio.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>Requisitos de memoria de acceso aleatorio (RAM) del servidor

No hay requisitos de RAM específicos para la instalación de MBAM Server.

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de bases de datos de SQL Server

En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de características de servidor de MBAM.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica de MBAM Server</th>
<th align="left">Versión de SQL Server</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Informes de cumplimiento y cumplimiento</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter o Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Base de datos de recuperación y hardware</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Enterprise, Datacenter o Developer Edition</p>
<div class="alert">
<strong>Importante</strong><br/><p>Las ediciones de SQL Server Standard no son compatibles con la instalación de características de servidor de bases de datos de recuperación y hardware de MBAM.</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Base de datos de cumplimiento y auditoría</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter o Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Requisitos del sistema para el cliente de MBAM


### Requisitos del sistema operativo del cliente

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de cliente de MBAM.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Edición Enterprise</p></td>
<td align="left"><p>Ninguno, SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate Edition</p></td>
<td align="left"><p>Ninguno, SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Requisitos de RAM de cliente

No hay requisitos de RAM específicos para la instalación del cliente de MBAM.

## Temas relacionados


[Planificar la implementación de MBAM 1.0](planning-to-deploy-mbam-10.md)

[Requisitos previos de implementación de MBAM 1.0](mbam-10-deployment-prerequisites.md)









