---
title: Configuración de funciones de servidor MBAM 2.5
description: Configuración de funciones de servidor MBAM 2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823060"
---
# Configuración de funciones de servidor MBAM 2.5


Use esta información como un lugar de inicio para configurar las características de servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 después de [instalar el software de servidor de MBAM 2,5](installing-the-mbam-25-server-software.md). Existen dos métodos que puede usar para configurar MBAM:

-   Asistente para la configuración del servidor de MBAM

-   Cmdlets de Windows PowerShell

## Antes de empezar a configurar las características del servidor de MBAM


Revise y complete los pasos siguientes antes de empezar a configurar las características del servidor de MBAM:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Dónde obtener instrucciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Revise la arquitectura recomendada para MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitectura de alto nivel de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Revise las configuraciones compatibles para MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complete los requisitos previos necesarios en cada servidor.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Instale el software de servidor MBAM en cada servidor donde configurará una característica de MBAM Server.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revise los requisitos previos para usar Windows PowerShell para configurar las características del servidor de MBAM (si usa este método para configurar las características de MBAM Server).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>

 

## Pasos para configurar las características de MBAM Server


Cada fila de la tabla siguiente describe las características que se configurarán en un servidor independiente, de acuerdo con la [arquitectura de alto nivel recomendada para MBAM 2,5](high-level-architecture-for-mbam-25.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Características para instalar</th>
<th align="left">Dónde obtener instrucciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configure las bases de datos.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Cómo configurar las bases de datos de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure los informes.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Cómo configurar los informes de MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configure las aplicaciones Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Cómo configurar las aplicaciones web de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar la integración de System Center Configuration Manager (si corresponde).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>

 

Para obtener una lista de eventos sobre la configuración de características del servidor de MBAM, consulte [registros de eventos del servidor](server-event-logs.md).



## Temas relacionados


Configuración de funciones de servidor MBAM 2.5
 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




