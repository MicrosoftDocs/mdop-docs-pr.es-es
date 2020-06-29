---
title: Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5
description: Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812446"
---
# Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5


En este tema se explica cómo configurar administración y supervisión de Microsoft BitLocker (MBAM) para usar la topología de integración de System Center Configuration Manager, que integra MBAM con Configuration Manager.

En las instrucciones se explica cómo configurar la integración de Configuration Manager mediante:

-   Un cmdlet de Windows PowerShell

-   El Asistente para la configuración del servidor de MBAM

Las instrucciones se basan en la arquitectura recomendada en [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Antes de comenzar con la configuración:**

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
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración</a></p></td>
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
<td align="left"><p>Instale el software de servidor MBAM en cada servidor donde configurará una característica de MBAM Server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Para esta topología, debe instalar la consola de Configuration Manager en el equipo en el que está instalando el software de servidor MBAM.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revise los requisitos previos de Windows PowerShell (solo es aplicable si va a usar cmdlets de Windows PowerShell para configurar MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar la integración de Configuration Manager mediante Windows PowerShell**

1.  Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.

2.  Use el cmdlet **enable-MbamCMIntegration de** Windows PowerShell para configurar los informes. Para obtener información sobre este cmdlet, escriba **Get-Help enable-MbamCMIntegration**.

**Para configurar la integración de System Center Configuration Manager mediante el asistente**

1.  En el servidor en el que desea configurar la característica de integración de System Center Configuration Manager, inicie el Asistente para la configuración del servidor de MBAM. Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.

2.  Haga clic en **Agregar nuevas características**, seleccione **integración de System Center Configuration Manager**y, a continuación, haga clic en **siguiente**.

    El asistente comprueba que se hayan cumplido todos los requisitos previos para la integración de Configuration Manager.

3.  Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar. De lo contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.

4.  Use las siguientes descripciones para especificar los valores de campo en el asistente:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Servidor de SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nombre de dominio completo (FQDN) del servidor con el rol de punto de servicio de informes. Este es el servidor al que se implementan los informes de MBAM Configuration Manager.</p>
    <p>Si no especifica un servidor, los informes de Configuration Manager se implementarán en el servidor local.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instancia de SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nombre de la instancia de SQL Server Reporting Services (SSRS) en la que se implementan los informes de Configuration Manager.</p>
    <p>Si no especifica una instancia, los informes de Configuration Manager se implementarán en el nombre de instancia de SSRS predeterminado. El valor que escriba se ignorará si el servidor tiene System Center 2012 Configuration Manager instalado.</p></td>
    </tr>
    </tbody>
    </table>



5.  En la página **Resumen** , revise las características que se agregarán.

    **Nota**  
    Para crear un script de Windows PowerShell de las entradas que acaba de realizar, haga clic en **Exportar script de PowerShell** y guarde el script.



6.  Haga clic en **Agregar** para agregar la característica de integración del administrador de configuración al servidor y, a continuación, haga clic en **cerrar**.



## Temas relacionados


[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Validación de la configuración de funciones de servidor de MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






