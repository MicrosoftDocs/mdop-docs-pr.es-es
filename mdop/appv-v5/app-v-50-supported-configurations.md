---
title: Consideraciones compatibles con App-V 5.0
description: Consideraciones compatibles con App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814790"
---
# Consideraciones compatibles con App-V 5.0


En este tema se especifican los requisitos necesarios para instalar y ejecutar Microsoft Application Virtualization (App-V) 5,0 en su entorno.

**Importante**  
**Las configuraciones admitidas en este artículo solo se aplican a App-V 5,0**. Para obtener las configuraciones compatibles que se aplican a los Service Pack de App-V 5,0, consulte las siguientes páginas web:

-   [Novedades de App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Acerca de App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Configuraciones admitidas de App-V 5.0 SP3](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> Requisitos del sistema para el servidor de App-V 5,0


**Importante**  
El servidor de App-V 5,0 no admite los siguientes escenarios:



-   Implementación en un equipo que ejecute Microsoft Windows Server Core.

-   Implementación en un equipo que ejecute una versión anterior de los componentes de servidor de App-V 5,0.

    **Nota**  
    Puede instalar App-V 5,0 en paralelo con el servidor de servidor de transmisión ligero de App-V 4,5 (LWS). Implementación de App-V 5,0 en paralelo con el servidor de App-V 4,5 Application Virtualization Management Service (HWS) no es compatible.



-   Implementación en un equipo que ejecute Microsoft SQL Server Express Edition.

-   Implementación remota de la base de datos del servidor de administración o de la base de datos de informes. El instalador debe ejecutarse directamente en el equipo que ejecuta Microsoft SQL para que la instalación de la base de datos se realice correctamente.

-   Implementación en un controlador de dominio.

-   No se admiten las rutas cortas. Si va a usar una trayectoria corta, debe crear un volumen nuevo.

### Requisitos del sistema operativo del servidor de administración

En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de servidor de administración de App-V 5,0.

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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter o Web Server)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1 o superior</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



**Importante**  
La implementación de la función del servidor de administración en un equipo con el uso compartido de escritorio remoto (RDS) no es compatible.



### <a href="" id="management-server-hardware-requirements-"></a>Requisitos de hardware del servidor de administración

-   Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)

-   RAM: 1 GB de RAM (64 bits)

-   Espacio en disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido.

### Requisitos del sistema operativo de Publishing Server

En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación del servidor de publicación de App-V 5,0.

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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter o Web Server)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>Requisitos de hardware de Publishing Server

-   Procesador: 1,4 GHz o más rápido. procesador de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro. no incluye el directorio de contenido

### Requisitos del sistema operativo del servidor de informes

En la siguiente tabla se enumeran los sistemas operativos admitidos para la instalación de servidor de informes de App-V 5,0.

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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter o Web Server)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>Requisitos de hardware del servidor de informes

-   Procesador: 1,4 GHz o más rápido. procesador de 64 bits (x64)

-   RAM: 2 GB de RAM (64 bits)

-   Espacio en el disco: 200 MB de espacio libre en el disco duro

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de bases de datos de SQL Server

En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de la base de datos App-V 5,0 y del servidor.

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
<th align="left">Tipo de servidor de App-V 5,0</th>
<th align="left">Versión de SQL Server</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Administración/informes</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(Standard, Enterprise, Datacenter o Developer Edition con la siguiente característica: <strong> Servicios de motor de base de datos </strong> ).</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administración/informes</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(Standard, Enterprise, Datacenter o Developer Edition con la siguiente característica: <strong> Servicios de motor de base de datos </strong> ).</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administración/informes</p></td>
<td align="left"><p>Microsoft SQL Server 2012</p>
<p>(Standard, Enterprise, Datacenter o Developer Edition con la siguiente característica: <strong> Servicios de motor de base de datos </strong> ).</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> Requisitos del sistema para el cliente de App-V 5,0


En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de App-V 5,0.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Windows 8,1 solo es compatible con App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
</tbody>
</table>



Los siguientes escenarios de instalación de cliente de App-V no son compatibles, excepto como se indica:

-   Equipos que ejecutan Windows Server

-   Equipos que ejecutan App-V 4,6 SP1 o versiones anteriores

-   El cliente de servicios de escritorio remoto de App-V 5,0 solo se admite para servidores habilitados para RDS.

### <a href="" id="client-hardware-requirements-"></a>Requisitos de hardware del cliente

En la siguiente lista se muestra la configuración de hardware compatible para la instalación de cliente de App-V 5,0.

-   Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)

-   RAM: 1 GB (32 bits) o 2 GB (64 bits)

-   Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> Requisitos del sistema del cliente de escritorio remoto de App-V 5,0


En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de escritorio remoto de App-V 5,0.

**Nota**  
Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)



Operating System Edition Service Pack para Microsoft Windows Server 2008

R2

SP1

Microsoft Windows Server 2012

**Importante**  
Windows Server 2012 R2 solo es compatible con App-V 5,0 SP2



Microsoft Windows Server 2012 (Standard, Datacenter)

R2

64 bits



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>Requisitos de hardware de los clientes de escritorio remoto

En la siguiente lista se muestra la configuración de hardware compatible para la instalación de cliente de App-V 5,0.

-   Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)

-   RAM: 1 GB (32 bits) o 2 GB (64 bits)

-   Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> Requisitos del sistema de App-V 5,0 Sequencer


En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de App-V 5,0 Sequencer.

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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Windows 8,1 solo es compatible con App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits y 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Windows Server 2012 R2 solo es compatible con App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>Versiones compatibles de System Center Configuration Manager


Puede usar Microsoft System Center 2012 Configuration Manager o System Center 2012 R2 Configuration Manager para administrar aplicaciones virtuales de App-V, informes y otras funciones. En la siguiente tabla se enumeran las versiones compatibles de Configuration Manager para cada versión aplicable de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de Configuration Manager compatible</th>
<th align="left">Versión de App-V</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Administrador de configuración de Microsoft System Center 2012</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Para obtener más información sobre cómo Configuration Manager se integra con App-V, consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v.md)

[Requisitos previos de App-V 5.0](app-v-50-prerequisites.md)









