---
title: Cómo configurar los informes de MBAM 2.5
description: Cómo configurar los informes de MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826620"
---
# Cómo configurar los informes de MBAM 2.5


En este tema se explica cómo configurar la característica de informes de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 mediante:

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
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager </a> (si corresponde)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Instale el software de servidor MBAM en cada servidor en el que vaya a configurar una característica de MBAM Server.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar cmdlets de Windows PowerShell para configurar las características del servidor de MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar los informes mediante Windows PowerShell**

1.  Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.

2.  Use el cmdlet **enable-MbamReport de** Windows PowerShell para configurar los informes. Para obtener información sobre este cmdlet de Windows PowerShell, escriba **Get-Help enable-MbamReport**.

**Para configurar los informes mediante el asistente**

1. En el servidor en el que desea configurar los informes, inicie el Asistente para la **configuración del servidor de MBAM** . Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.

2. Haga clic en **Agregar nuevas características**, seleccione **informes**y, a continuación, haga clic en **siguiente**. El asistente comprueba que se cumplen todos los requisitos previos para los informes.

3. Haz clic en **Siguiente** para continuar.

4. Con las siguientes descripciones, escriba los valores de campo en el asistente:

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
   <td align="left"><p><strong>Instancia de SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>Instancia de SQL Server Reporting Services en la que se configurarán los informes.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Grupo de dominio de rol de informes</strong></p></td>
   <td align="left"><p>Nombre del grupo usuarios del dominio cuyos miembros tienen derechos de acceso a los informes en el servidor de administración y supervisión.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nombre del servidor SQL Server</strong></p></td>
   <td align="left"><p>Nombre del servidor en el que está configurada la base de datos de cumplimiento y auditoría.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instancia de base de datos de SQL Server</strong></p></td>
   <td align="left"><p>Nombre de la instancia de SQL Server (por ejemplo, <em> MSSQLSERVER </em> ) donde está configurada la base de datos de cumplimiento y auditoría.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Debe agregar una excepción en el equipo de informes para habilitar el tráfico entrante en el puerto del servidor de creación de informes (el puerto predeterminado es 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nombre de la base de datos</strong></p></td>
   <td align="left"><p>Nombre de la base de datos de cumplimiento y auditoría. De forma predeterminada, el nombre de la base de datos es <strong> MBAM estado de cumplimiento </strong> , aunque puede cambiar el nombre al configurar la base de datos de cumplimiento y auditoría.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Si está actualizando desde una versión anterior de MBAM, debe usar el mismo nombre de base de datos que el nombre usado en la implementación anterior.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Cuenta de dominio de base de datos de auditoría y cumplimiento</strong></p></td>
   <td align="left"><p>Cuenta de usuario y contraseña de dominio para acceder a la base de datos de cumplimiento y comprobación.</p>
   <p>Si el valor que escribe en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> de la <strong> Página configurar bases de datos </strong> es un usuario, debe escribir el mismo valor en este campo.</p>
   <p>Si el valor que especifica en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> de la <strong> Página configurar bases de datos </strong> es un grupo, el valor que especifique en este campo debe ser miembro de ese grupo.</p>
   <p>Configure la contraseña de esta cuenta para que nunca expire. La cuenta de usuario debería poder acceder a todos los datos que están disponibles para el grupo de usuarios de informes de MBAM.</p></td>
   </tr>
   </tbody>
   </table>



5. Cuando termine las entradas, haga clic en **siguiente**.

   El asistente comprueba que se cumplen todos los requisitos previos para la característica de informes.

6. Haz clic en **Siguiente** para continuar.

7. En la página **Resumen** , revise las características que se agregarán.

   **Nota**  
   Para crear un script de Windows PowerShell de las entradas que acaba de realizar, haga clic en **Exportar script de PowerShell**y, a continuación, guarde el script.



8. Haga clic en **Agregar** para agregar los informes en el servidor y, a continuación, haga clic en **cerrar**.



## Temas relacionados


[Registros de eventos de servidor](server-event-logs.md)

[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Cómo configurar las aplicaciones web de MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Validación de la configuración de funciones de servidor de MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






