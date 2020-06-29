---
title: Evaluación de MBAM 2.0
description: Evaluación de MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824740"
---
# Evaluación de MBAM 2.0


Antes de implementar administración y supervisión de Microsoft BitLocker (MBAM) en un entorno de producción, debe evaluarlo en un entorno de prueba. La información de este tema se puede usar para configurar la administración y la supervisión de Microsoft BitLocker con una topología independiente en un entorno de prueba de servidor único para fines de evaluación. No se recomienda una topología de un solo servidor para entornos de producción.

Para obtener instrucciones sobre cómo implementar MBAM en un entorno de prueba, consulte [Cómo instalar y configurar MBAM en un solo servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).

## Configuración del entorno de prueba


Aunque esté configurando una instancia de no producción de MBAM para que se evalúe en un entorno de prueba, debe comprobar que cumple los requisitos previos y los requisitos de hardware y software. Antes de iniciar la instalación, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 Supported](mbam-20-supported-configurations-mbam-2.md), y [preparar su entorno para MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).

### Planear una implementación de evaluación de MBAM

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
<td align="left"><p>Revise la información de introducción sobre MBAM para obtener un conocimiento básico del producto antes de comenzar con el planeamiento de la implementación.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">Introducción a MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear los requisitos previos de implementación de MBAM 2,0 y preparar el entorno de equipos.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">Requisitos previos de implementación de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear y configurar los requisitos de la Directiva de grupo de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planificación de los requisitos de directiva de grupo de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear y crear grupos de seguridad de ActiveDirectoryDomainServices necesarios y planear los requisitos de pertenencia a grupos de seguridad local de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planificación de roles de administrador de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear la implementación de características de servidor de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">Planeación para la implementación de servidores de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear la implementación de la implementación de cliente de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planeación para la implementación de clientes de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### Realizar una implementación de evaluación de MBAM

Después de completar las instalaciones necesarias de planeación y de software necesarias para preparar el entorno informático para la instalación de MBAM, puede comenzar la implementación de evaluación de MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la información de configuraciones admitidas de MBAM para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configuraciones admitidas de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en un solo servidor con fines de evaluación.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">Cómo instalar y configurar MBAM en un único servidor</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Agregue grupos de seguridad ActiveDirectoryDomainServices, que ha creado durante la fase de planeación, a los grupos locales de la MBAM servidor local correspondiente en el nuevo MBAM Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planificación de los roles de administrador de MBAM 2,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Cómo administrar los roles de administrador de MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Cree e implemente objetos de directiva de grupo MBAM obligatorios.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Implementación de objetos de directiva de grupo de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implemente el software de cliente de MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Implementación de cliente de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Configurar los equipos de laboratorio para la evaluación de MBAM


Esta sección contiene información que puede usarse para acelerar los informes de estado del cliente de MBAM. Sin embargo, estas modificaciones deberían usarse solo con fines de prueba.

**Nota:**  En la información de la sección siguiente se describe cómo modificar el registro de Windows. El uso incorrecto del editor del registro puede causar serios problemas que le obliguen a reinstalar Windows. Microsoft no puede garantizar la solución de los problemas resultantes del uso incorrecto del editor del registro. Use el editor del registro bajo su propia responsabilidad.

 

### Modificar la configuración de frecuencia de informes de estado del cliente MBAM

Las frecuencias de los informes de estado y activación del cliente de MBAM tienen un valor mínimo de 90 minutos cuando se establecen mediante una directiva de grupo. Puede usar el registro de Windows para cambiar estas frecuencias a un valor inferior en los equipos cliente de MBAM para ayudar a acelerar las pruebas.

Para modificar la configuración de frecuencia de informes de estado del cliente MBAM:

1.  Use un editor del registro para ir a **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.

2.  Cambie los valores de **ClientWakeupFrequency** y **StatusReportingFrequency** a **1** como valor mínimo admitido por el cliente. Este cambio hace que el cliente de MBAM informe cada minuto.

3.  Reinicie el **servicio del cliente de administración de BitLocker**.

**Nota:**  Para establecer los valores que son muy bajos, debe establecerlos manualmente en el registro.

 

### Modificar el retraso de inicio del servicio cliente de MBAM

Además de las frecuencias de los informes de estado y la activación del cliente de MBAM, se produce un retraso aleatorio de hasta 90 minutos cuando el servicio agente de cliente de MBAM se inicia en los equipos cliente. Si no desea el retraso aleatorio, cree un valor **DWORD** de **NoStartupDelay** en **HKLM\\Software\\Microsoft\\MBAM**, establezca su valor en **1**y, a continuación, reinicie el servicio de cliente de **Administración de BitLocker**.

## Temas relacionados


[Introducción a MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





