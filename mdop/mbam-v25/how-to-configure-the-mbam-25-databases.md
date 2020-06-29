---
title: Cómo configurar las bases de datos de MBAM 2.5
description: Cómo configurar las bases de datos de MBAM 2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826621"
---
# Cómo configurar las bases de datos de MBAM 2.5


En este tema se explica cómo configurar la base de datos de cumplimiento y la supervisión de administración de Microsoft BitLocker (MBAM) 2,5 y la base de datos de recuperación mediante:

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
<td align="left"><p>Instale el software de servidor MBAM en cada servidor en el que vaya a configurar una característica de MBAM Server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Puede instalar las bases de datos en un equipo SQL Server remoto mediante Windows PowerShell o un paquete de aplicación de capa de datos (DAC) exportado. Para obtener más información sobre los paquetes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicaciones de capa de datos </a> .</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar cmdlets de Windows PowerShell para configurar las características del servidor de MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar las bases de datos mediante Windows PowerShell**

1.  Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.

2.  Use el cmdlet **enable-MbamDatabase de** Windows PowerShell para configurar las bases de datos. Para obtener información sobre este cmdlet de Windows PowerShell, escriba **Get-Help enable-MbamDatabase**.

**Para configurar la base de datos de cumplimiento y comprobación mediante el asistente**

1. En el servidor en el que desea configurar las bases de datos, inicie el Asistente para la **configuración del servidor de MBAM** . Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.

2. Haga clic en **Agregar nuevas características**, seleccione **cumplimiento y** base de datos de auditoría y **base de datos de recuperación**y, a continuación, haga clic en **siguiente**. El asistente comprueba que se cumplen todos los requisitos previos de las bases de datos.

3. Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar. De lo contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.

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
   <td align="left"><p><strong>Nombre del servidor SQL Server</strong></p></td>
   <td align="left"><p>Nombre del servidor en el que está configurando la base de datos de cumplimiento y comprobación.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Debe agregar una excepción en el equipo de base de datos de cumplimiento y auditoría para habilitar el tráfico entrante en el puerto de Microsoft SQL Server. El número de puerto predeterminado es 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instancia de base de datos de SQL Server</strong></p></td>
   <td align="left"><p>Nombre de la instancia de la base de datos en la que se almacenarán los datos de cumplimiento y auditoría. También debe especificar dónde se ubicará la información de la base de datos.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nombre de la base de datos</strong></p></td>
   <td align="left"><p>Nombre de la base de datos que almacenará los datos de cumplimiento.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Si está actualizando desde una versión anterior de MBAM, debe usar el mismo nombre de base de datos que el que se usó en la implementación anterior.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Acceso de lectura y escritura a un usuario o grupo de dominio</strong></p></td>
   <td align="left"><p>Grupo o usuario de dominio que tiene permiso de lectura y escritura para esta base de datos para permitir que las aplicaciones web tengan acceso a los datos y los informes de esta base de datos.</p>
   <p>Si especifica un usuario en este campo, debe ser el mismo valor que el valor del <strong> campo cuenta de dominio del grupo de aplicaciones de servicio Web </strong> en la <strong> Página configurar aplicaciones Web </strong> .</p>
   <p>Si especifica un grupo en este campo, el valor del <strong> campo cuenta de dominio del grupo de aplicaciones </strong> de servicio Web en la <strong> Página configurar aplicaciones Web </strong> debe ser miembro del grupo que especifique en este campo.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Acceso de solo lectura a un usuario o grupo de dominio</strong></p></td>
   <td align="left"><p>Nombre del usuario o grupo que tendrá permiso de solo lectura para esta base de datos para permitir que los informes tengan acceso a los datos de cumplimiento de esta base de datos.</p>
   <p>Si especifica un usuario en este campo, debe ser el mismo usuario que el que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> .</p>
   <p>Si especifica un grupo en este campo, el valor que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> debe ser miembro del grupo que especifique en este campo.</p></td>
   </tr>
   </tbody>
   </table>



5. Continúe con la siguiente sección para configurar la base de datos de recuperación.

**Para configurar la base de datos de recuperación mediante el asistente**

1. Con las siguientes descripciones, escriba los valores de campo en el asistente:

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
   <td align="left"><p><strong>Nombre del servidor SQL Server</strong></p></td>
   <td align="left"><p>Nombre del servidor en el que está configurando la base de datos de recuperación.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Debe agregar una excepción en el equipo de la base de datos de recuperación para habilitar el tráfico entrante en el puerto de Microsoft SQL Server. El número de puerto predeterminado es 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instancia de base de datos de SQL Server</strong></p></td>
   <td align="left"><p>Nombre de la instancia de la base de datos en la que se almacenarán los datos de recuperación. También debe especificar dónde se ubicará la información de la base de datos.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nombre de la base de datos</strong></p></td>
   <td align="left"><p>Nombre de la base de datos que almacenará los datos de recuperación.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Si está actualizando desde una versión anterior de MBAM, debe usar el mismo nombre de base de datos que el que se usó en la implementación anterior.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Acceso de lectura y escritura a un usuario o grupo de dominio</strong></p></td>
   <td align="left"><p>Grupo o usuario de dominio que tiene permiso de lectura y escritura para esta base de datos para permitir que las aplicaciones web tengan acceso a los datos y los informes de esta base de datos.</p>
   <p>Si especifica un usuario en este campo, debe ser el mismo valor que el valor del <strong> campo cuenta de dominio del grupo de aplicaciones de servicio Web </strong> en la <strong> Página configurar aplicaciones Web </strong> .</p>
   <p>Si especifica un grupo en este campo, el valor del <strong> campo cuenta de dominio del grupo de aplicaciones </strong> de servicio Web en la <strong> Página configurar aplicaciones Web </strong> debe ser miembro del grupo que especifique en este campo.</p></td>
   </tr>
   </tbody>
   </table>



2. Cuando termine las entradas, haga clic en **siguiente**.

   El asistente comprueba que se cumplen todos los requisitos previos de las bases de datos.

3. Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar. En caso contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **siguiente** .

4. En la página **Resumen** , revise las características que se agregarán.

   **Nota**  
   Para crear un script de Windows PowerShell de las entradas que acaba de realizar, haga clic en **Exportar script de PowerShell**y, a continuación, guarde el script.



5. Haga clic en **Agregar** para agregar las bases de datos de MBAM en el servidor y, a continuación, haga clic en **cerrar**.



## Temas relacionados


[Registros de eventos de servidor](server-event-logs.md)

[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Cómo configurar los informes de MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Cómo configurar las aplicaciones web de MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Validación de la configuración de funciones de servidor de MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





