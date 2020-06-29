---
title: Planificación para alta disponibilidad de MBAM 2.5
description: Planificación para alta disponibilidad de MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826941"
---
# Planificación para alta disponibilidad de MBAM 2.5


Administración y supervisión de Microsoft BitLocker (MBAM) puede mantener una alta disponibilidad mediante el uso de una o más de las siguientes tecnologías, que se describen en las siguientes secciones:

-   [Grupos de disponibilidad AlwaysOn de SQL Server](#bkmk-alwayson)

-   [Clustering de Microsoft SQL Server](#bkmk-sql-clustering)

-   [Equilibrio de carga de red de IIS](#bkmk-load-balance)

-   [Reflejo de base de datos en SQL Server](#bkmk-db-mirroring)

-   [Copia de seguridad de las bases de datos de MBAM mediante el servicio de instantáneas de volumen (VSS)](#bkmk-vss)

Use la información de las siguientes secciones como ayuda para comprender las opciones para implementar MBAM en una configuración de alta disponibilidad.

## <a href="" id="bkmk-alwayson"></a>Compatibilidad con los grupos de disponibilidad AlwaysOn de SQL Server


MBAM le permite configurar y administrar los grupos de disponibilidad de las bases de datos de Microsoft SQL Server. Un grupo de disponibilidad para MBAM admite un entorno de conmutación por error en el que la base de datos de cumplimiento y auditoría y la base de datos de recuperación conmutan por error en lugar de por separado.

Un grupo de disponibilidad admite un conjunto de bases de datos primarias de lectura y escritura y de una a cuatro conjuntos de bases de datos secundarias correspondientes. De manera opcional, las bases de datos secundarias pueden estar disponibles para permisos de solo lectura, algunas operaciones de copia de seguridad o ambas.

Para obtener más información sobre cómo configurar grupos de disponibilidad, consulte [grupos de disponibilidad AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).

## <a href="" id="bkmk-sql-clustering"></a>Clustering de Microsoft SQL Server


Puede ejecutar la base de datos de cumplimiento y cumplimiento de MBAM 2,5 y la base de datos de recuperación en equipos que ejecutan clústeres de SQL Server.

## <a href="" id="bkmk-load-balance"></a>Equilibrio de carga de red de IIS


Puede usar el equilibrio de carga de red para configurar un entorno de alta disponibilidad para equipos que ejecuten el sitio web de administración y supervisión (también conocido como servicio de asistencia), el portal de autoservicio y los servicios web que se implementan a través de los servicios de Internet Information Server (IIS).

### Requisitos previos

Antes de configurar el equilibrio de carga, asegúrese de cumplir los siguientes requisitos previos:

-   Debe haber un equilibrador de carga disponible. Puede usar equilibradores de carga de Microsoft o de otra empresa. Para más información sobre la tecnología de equilibrador de carga de Microsoft, vea [crear una granja de servidores web con servidores IIS](https://go.microsoft.com/fwlink/?LinkId=393326).

-   Al menos dos servidores ejecutan IIS y cumplen todos los requisitos previos de MBAM para admitir sus características Web, entre las que se incluyen ASP.NET MVC 4.

-   Las bases de datos y los informes de MBAM se ejecutan en un servidor.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> Cambios específicos de MBAM necesarios para habilitar el equilibrio de carga

Complete las siguientes tareas:

1.  Registre un nombre principal de servicio (SPN) para el nombre de host virtual en la cuenta de dominio que está usando para los grupos de aplicaciones Web. Por ejemplo, si el nombre de host virtual es mbamvirtual.contoso.com y la cuenta de dominio que se usa para los grupos de aplicaciones web es contoso\\mbamapppooluser, el comando siguiente registra el SPN correctamente.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  Configure las siguientes características Web de MBAM:

    -   En cada servidor que hospede las características Web de MBAM, use la misma cuenta de dominio para las credenciales administrativas del grupo de aplicaciones.

    -   Especifique un nombre de host que coincida con el nombre de host virtual (nombre DNS) del clúster de equilibrio de carga. Por ejemplo, al instalar MBAM en un servidor denominado "NLB1" con un nombre de host virtual de **mbamvirtual.contoso.com**, asegúrese de que el nombre de host que especifique en el cmdlet de Windows PowerShell sea **mbamvirtual.contoso.com**.

3.  Si va a configurar los sitios web en una granja de servidores web con un equilibrador de carga, debe configurar los sitios web para que usen la misma clave de equipo.

    Para obtener más información, vea las secciones siguientes del [elemento machineKey (esquema de configuración de ASP.net)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):

    -   Explicación de la clave de equipo

    -   Consideraciones de implementación de granjas de servidores Web

    Para obtener instrucciones sobre cómo generar una clave automáticamente, vea [generar una clave de máquina (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).

La información sobre el equilibrio de carga también se aplica a los clústeres de equilibrio de carga de red (NLB) de IIS en Windows Server 2012 o Windows Server2008R2. La funcionalidad de equilibrio de carga de red de IIS en Windows Server 2012 generalmente es la misma que en Windows Server2008R2. Sin embargo, algunos detalles de las tareas son diferentes en Windows Server 2012. Para obtener información sobre las nuevas formas de realizar tareas, consulte [navegación y tareas de administración comunes en Windows server 2012 R2 Preview y Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).

## <a href="" id="bkmk-db-mirroring"></a>Reflejo de base de datos en SQL Server


MBAM admite el uso de reflejos de SQL Server, en el que la base de datos de cumplimiento y de comprobación y la base de datos de recuperación se reflejan utilizando dos instancias de SQL Server para cada base de datos. Antes de implementar la creación de reflejos, ten en cuenta que el reflejo se retirará lentamente, en favor de los grupos de disponibilidad, que se describen anteriormente en este tema.

Para implementar el reflejo de MBAM, debe especificar las cadenas de conexión apropiadas para la configuración de la base de datos reflejada mediante el cmdlet **enable-MbamWebApplication de** Windows PowerShell. Para obtener más información sobre los cmdlets de Windows PowerShell de MBAM 2,5, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

### Ejemplos de implementación del reflejo de SQL Server mediante Windows PowerShell

En los siguientes ejemplos se muestra cómo puede implementar el reflejo de SQL Server mediante cmdlets de Windows PowerShell.

**Ejemplo 1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**Ejemplo 2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### Más información sobre el reflejo de SQL Server

Los vínculos siguientes proporcionan más información sobre cómo configurar el reflejo de SQL Server:

-   [Cómo: preparar una base de datos de reflejo para la creación de reflejos (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Establecer una sesión de creación de reflejo de base de datos con la autenticación de Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>Copia de seguridad de las bases de datos de MBAM mediante el servicio de instantáneas de volumen (VSS)


MBAM ofrece un escritor de servicio de instantáneas de volumen (VSS), denominado escritor de administración y administración de Microsoft BitLocker. Este VSS Writer facilita la copia de seguridad de la base de datos de cumplimiento y comprobación y la base de datos de recuperación.

El VSS Writer se registra en todos los servidores en los que se habilita una aplicación web MBAM. El MBAM VSS Writer depende del Escritor VSS de SQL Server, que está registrado como parte de la instalación de Microsoft SQL Server. Cualquier tecnología de copia de seguridad que use escritores de VSS para realizar copias de seguridad puede descubrir el MBAM VSS Writer.



## Temas relacionados


[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




