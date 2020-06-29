---
title: Planificación para la implementación de servidores de MBAM 2.5
description: Planificación para la implementación de servidores de MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826211"
---
# Planificación para la implementación de servidores de MBAM 2.5


En este tema, se enumeran las características que se implementan en las topologías independientes del administrador de configuración y MBAM, y se indica el orden en el que es necesario implementarlas. Hay una configuración recomendada para cada topología. Sin embargo, puede configurar las bases de datos y características de MBAM Server en diferentes configuraciones y en varios servidores, en función de los requisitos de escalabilidad.

## Consideraciones de planeación importantes para ambas topologías


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Razones</th>
<th align="left">Detalles o propósito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Revise lo siguiente antes de iniciar la implementación:</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></li>
</ul></td>
<td align="left"><p>Cada característica de MBAM tiene requisitos previos específicos que deben cumplirse antes de iniciar la instalación de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Las claves de recuperación de BitLocker de MBAM expiran después de un solo uso.</p></td>
<td align="left"><p>Un solo uso significa que la clave de recuperación se ha recuperado a través del sitio web de administración y supervisión (también conocido como servicio de asistencia), portal de autoservicio o mediante el cmdlet Get- <strong> MbamBitLockerRecoveryKey de </strong> Windows PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Realice un seguimiento de los nombres de los equipos en los que va a configurar cada característica. Usará esta información durante el proceso de configuración.</p></td>
<td align="left"><p>Es posible que desee usar la <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> lista de comprobación de implementación de MBAM 2,5 </a> para este propósito.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure solo la configuración de directiva de grupo en el nodo MDOP MBAM (administración de BitLocker). No cambie la configuración de directiva de grupo en el nodo cifrado de unidad BitLocker.</p></td>
<td align="left"><p>Si cambia la configuración de directiva de grupo en el nodo cifrado de unidad BitLocker, MBAM no funcionará.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>Planificación de la implementación de MBAM Server: topología independiente


En el caso de una topología independiente, se recomienda una configuración de dos servidores para entornos de producción, aunque se pueden usar configuraciones de tres a cuatro servidores.

La infraestructura de servidor de la topología independiente MBAM contiene las siguientes características, que se deben configurar en el orden indicado:

1.  Bases de datos (base de datos de cumplimiento y de auditoría y base de datos de recuperación)

2.  Informes

3.  Aplicaciones web (y sus correspondientes servicios web)

    -   Sitio web de administración y supervisión

    -   Portal de autoservicio

Para obtener una descripción de estas características, consulte [arquitectura de alto nivel de MBAM 2,5 con topología independiente](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>Planificación de la implementación de MBAM Server: topología del administrador de configuración


Para la topología de integración de Configuration Manager, se recomienda una configuración de tres servidores para entornos de producción, aunque se puede usar la configuración de servidores adicionales.

La infraestructura de servidor de la topología del administrador de configuración de MBAM contiene las siguientes características, que se deben configurar o realizar en el orden indicado:

1.  Bases de datos (base de datos de cumplimiento y de auditoría y base de datos de recuperación)

2.  Informes

3.  Aplicaciones web (y sus correspondientes servicios web)

    -   Sitio web de administración y supervisión

    -   Portal de autoservicio

4.  Integración de System Center Configuration Manager

Para obtener una descripción de estas características, consulte [arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).



## Temas relacionados


[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

[Implementación de la infraestructura de servidor de MBAM 2.5](deploying-the-mbam-25-server-infrastructure.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





