---
title: Lista de comprobación de planificación de MBAM 2.5
description: Lista de comprobación de planificación de MBAM 2.5
author: dansimp
ms.assetid: ffe11eb8-44db-4886-8300-6dffec8bcfa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 505f2890d67f36056ab5bb87df2a894473cd3306
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826541"
---
# Lista de comprobación de planificación de MBAM 2.5


Puede usar las siguientes listas de comprobación como ayuda para preparar el entorno de equipos para la implementación de administración y supervisión de Microsoft BitLocker (MBAM). Las listas de comprobación proporcionan una lista de alto nivel de los elementos que se deben tener en cuenta al planear la implementación. Hay listas de comprobación independientes para la topología independiente y la topología de integración de Configuration Manager. Es posible que desee copiar la lista de comprobación deseada en una hoja de cálculo y personalizarla para su uso.

**Lista de comprobación de la planificación para una implementación de MBAM**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tarea</th>
<th align="left">Referencias</th>
<th align="left">Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la &quot; información de introducción &quot; para comprender el producto antes de comenzar el plan de implementación.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-25.md" data-raw-source="[Getting Started with MBAM 2.5](getting-started-with-mbam-25.md)">Introducción a MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la arquitectura de alto nivel recomendada para una implementación de MBAM. Es posible que también desee revisar una ilustración y una descripción de las partes individuales (bases de datos, sitios web, informes) de una implementación de MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitectura de alto nivel de MBAM 2.5</a></p>
<p><a href="illustrated-features-of-an-mbam-25-deployment.md" data-raw-source="[Illustrated Features of an MBAM 2.5 Deployment](illustrated-features-of-an-mbam-25-deployment.md)">Funciones mostradas de una implementación MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise y complete los requisitos previos para los MBAM topologías independientes y de integración del administrador de configuración.</p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Si planea usar la topología de integración de Configuration Manager, complete los requisitos previos adicionales que solo se aplican a esta topología.</p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise y cumpla con los requisitos previos de MBAM 2,5 para el cliente de MBAM.</p></td>
<td align="left"><p><a href="prerequisites-for-mbam-25-clients.md" data-raw-source="[Prerequisites for MBAM 2.5 Clients](prerequisites-for-mbam-25-clients.md)">Requisitos previos para clientes MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear y configurar los requisitos de la Directiva de grupo de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Planificación para requisitos de directiva de grupo de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear y crear los grupos de seguridad ActiveDirectoryDomainServices necesarios.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planificación para cuentas y grupos de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifique cómo protegerás los sitios web de MBAM.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planificación de cómo proteger los sitios web MBAM.</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise las configuraciones admitidas de MBAM para asegurarse de que su hardware cumpla con los requisitos del sistema de instalación.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise las consideraciones para implementar las características del servidor de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-server-deployment.md" data-raw-source="[Planning for MBAM 2.5 Server Deployment](planning-for-mbam-25-server-deployment.md)">Planificación para la implementación de servidores de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise las consideraciones para implementar el cliente de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-client-deployment.md" data-raw-source="[Planning for MBAM 2.5 Client Deployment](planning-for-mbam-25-client-deployment.md)">Planificación para la implementación de clientes de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise los requisitos y los pasos para implementar MBAM en una configuración de alta disponibilidad.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-high-availability.md" data-raw-source="[Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md)">Planificación para alta disponibilidad de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise las consideraciones de seguridad de MBAM que pertenecen al módulo de plataforma segura, los archivos de registro y el cifrado de datos transparente.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">Consideraciones sobre seguridad de MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>De manera opcional, revise los pasos para evaluar MBAM en un entorno de prueba.</p></td>
<td align="left"><p><a href="evaluating-mbam-25-in-a-test-environment.md" data-raw-source="[Evaluating MBAM 2.5 in a Test Environment](evaluating-mbam-25-in-a-test-environment.md)">Evaluación de MBAM 2.5 en un entorno de prueba</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados


[Planificación para MBAM 2.5](planning-for-mbam-25.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




