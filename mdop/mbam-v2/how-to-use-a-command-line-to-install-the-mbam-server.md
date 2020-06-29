---
title: Cómo usar una línea de comandos para instalar el servidor MBAM.
description: Cómo usar una línea de comandos para instalar el servidor MBAM.
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825641"
---
# Cómo usar una línea de comandos para instalar el servidor MBAM.


Puede usar una línea de comandos para instalar el servidor de MBAM con una topología independiente o de configuración del administrador. El siguiente ejemplo de la línea de comandos es para implementar MBAM en un único servidor, que es una arquitectura que solo debe usarse en un entorno de prueba. Tendrá que cambiar la línea de comandos según corresponda al implementar MBAM en un entorno de producción, que debe tener varios servidores.

## Línea de comandos para implementar el servidor de MBAM 2.0 con la topología independiente


Puede usar una línea de comandos similar a la siguiente para instalar el servidor de MBAM con la topología independiente.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

En la siguiente tabla se describen los parámetros de la línea de comandos para implementar el servidor de MBAM con la topología independiente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Valor del parámetro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGÍA</p></td>
<td align="left"><p>,0</p></td>
<td align="left"><p>0: topología independiente</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>Agosto</p></td>
<td align="left"><p>0: no acepte el agreement1 de licencia: acepte el contrato de licencia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Características que se instalarán en el servidor</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>KeyDatabase</p></td>
<td align="left"><p>Base de datos de recuperación</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>Base de datos de informes de cumplimiento y cumplimiento</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Informes</p></td>
<td align="left"><p>Informes de cumplimiento y cumplimiento</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>Sitio web de administración y supervisión</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>Portal de autoservicio</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>PolicyTemplate</p></td>
<td align="left"><p>MBAM plantilla de directiva de grupo</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>Dominio y cuenta de usuario de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y cumplimiento</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Contraseña de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y comprobación</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>NombreDeEquipo</p></td>
<td align="left"><p>Nombre de instancia de SQL Server para la base de datos de cumplimiento y auditoría: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>NombreDeEquipo</p></td>
<td align="left"><p>Nombre de instancia de SQL Server para la base de datos de recuperación: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>NombreDeEquipo</p></td>
<td align="left"><p>Instancia de SQL Server Reporting Server donde se instalarán los informes de cumplimiento y comprobación: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Puerto para el sitio web de administración y supervisión; "83" es solo un ejemplo</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Puerto para el sitio web del portal de autoservicio; "83" es solo un ejemplo</p></td>
</tr>
</tbody>
</table>

 

## Línea de comandos para implementar el servidor de MBAM 2.0 con la topología del administrador de configuración


Puede usar una línea de comandos similar a la siguiente para instalar el servidor de MBAM con la topología de Configuration Manager.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

En la siguiente tabla se describen los parámetros de la línea de comandos para instalar el servidor de MBAM 2.0 con la topología de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Valor del parámetro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGÍA</p></td>
<td align="left"><p>uno</p></td>
<td align="left"><p>1: topología del administrador de configuración</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>Agosto</p></td>
<td align="left"><p>0: no acepte el agreement1 de licencia: acepte el contrato de licencia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>NombreDeEquipo</p></td>
<td align="left"><p>Nombre de instancia de SQL Server para la base de datos de auditoría: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>NombreDeEquipo</p></td>
<td align="left"><p>Nombre de instancia de SQL Server para la base de datos de recuperación: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>NombreDeEquipo</p></td>
<td align="left"><p>Instancia de SQL Server Reporting Server donde se instalarán los informes de auditoría; Reemplace% COMPUTERNAME% por el nombre del equipo</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>[UserDomain] [UserName1]</p></td>
<td align="left"><p>Dominio y cuenta de usuario de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y cumplimiento</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Contraseña de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y comprobación</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Puerto para el sitio web de administración y supervisión; "83" es solo un ejemplo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Puerto para el sitio web del portal de autoservicio; "83" es solo un ejemplo</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





