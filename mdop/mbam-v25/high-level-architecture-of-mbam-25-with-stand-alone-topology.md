---
title: Arquitectura de alto nivel de MBAM 2.5 con topología independiente
description: Arquitectura de alto nivel de MBAM 2.5 con topología independiente
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826560"
---
# Arquitectura de alto nivel de MBAM 2.5 con topología independiente


En este tema se describe la arquitectura recomendada para implementar Microsoft BitLocker Administration and Monitoring (MBAM) con la topología independiente de Configuration Manager. En esta topología, MBAM se implementa como un producto independiente. También puede implementar MBAM con la topología de integración de Configuration Manager, que integra MBAM con Configuration Manager. Para obtener más información, consulte [arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Para obtener una lista de las versiones compatibles del software mencionadas en este tema, consulte [MBAM 2,5 configuraciones admitidas](mbam-25-supported-configurations.md).

**Nota:**  Le recomendamos que use una arquitectura de servidor único solo en entornos de prueba.

 

## Número recomendado de servidores y número de clientes admitidos


El número recomendado de servidores y la cantidad de clientes admitidos en un entorno de producción es el siguiente:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquitectura recomendada en un entorno de producción</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Número de servidores y otros equipos</p></td>
<td align="left"><p>Dos servidores</p>
<p>Una estación de trabajo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Número de equipos cliente admitidos</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Arquitectura de alto nivel recomendada de MBAM con la topología independiente


En el siguiente diagrama y tabla se describe la arquitectura de dos servidores de alto nivel recomendada para MBAM con la topología independiente. MBAM implementaciones de varios bosques requieren una confianza unidireccional o bidireccional. Las relaciones de confianza unidireccionales requieren que el dominio de servidor confíe en el dominio de cliente.

![mbam2](images/mbam2-5-2servers.png)

Características de servidor para configurar en este servidor de base de datos de descripción de servidor

Base de datos de cumplimiento y auditoría

Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.

La base de datos de **cumplimiento y auditoría** almacena los datos de cumplimiento, que se usan principalmente para informes de hosts de SQL Server Reporting Services.

Base de datos de recuperación

Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.

La **base** de datos de recuperación almacena los datos de recuperación que se recopilan de MBAM equipos cliente.

Informes

Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.

Los **informes** proporcionan auditoría de recuperación y datos del estado de cumplimiento sobre los equipos cliente de su empresa. Puede acceder a los informes desde el sitio web de administración y supervisión o directamente desde SQL Server Reporting Services.

Servidor de administración y supervisión

Sitio web de administración y supervisión

Esta característica está configurada en un equipo con Windows Server.

El **sitio web de administración y supervisión** se usa para:

-   Ayudar a los usuarios finales a recuperar el acceso a sus equipos cuando están bloqueados. (Esta área del sitio Web suele denominarse Servicio de asistencia).

-   Ver informes que muestran el estado de cumplimiento y la actividad de recuperación de equipos cliente.

Portal de autoservicio

Esta característica está configurada en un equipo con Windows Server.

El **portal de autoservicio** es un sitio web que permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker.

Supervisión de servicios web para este sitio web

Esta característica está configurada en un equipo con Windows Server.

El cliente de MBAM y los sitios web usan los **servicios Web de supervisión** para comunicarse con la base de datos.

**Importante**  El servicio Web de supervisión ya no está disponible en Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 porque los sitios web de MBAM se comunican directamente con la base de datos de recuperación.

 

Estación de trabajo de administración

MBAM plantillas de directiva de grupo

-   Las plantillas de directiva de grupo MBAM son configuraciones de directiva de grupo que definen la configuración de implementación de MBAM, que le permiten administrar el cifrado de unidad BitLocker.

-   Antes de ejecutar MBAM, debe descargar las plantillas de directiva de grupo de [Cómo obtener las plantillas de la Directiva de grupo de MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) y copiarlas en un servidor o estación de trabajo que ejecute un sistema operativo Windows Server o Windows compatible.

-   La estación de trabajo no tiene que ser un equipo dedicado.

Equipo cliente de Configuration Manager y cliente de MBAM

Software de cliente de MBAM

El cliente de MBAM:

-   Usa objetos de directiva de grupo para exigir el cifrado de unidad BitLocker en equipos cliente de la empresa.

-   Recopila la clave de recuperación de BitLocker para tres tipos de unidades de datos: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).

-   Recopila información de recuperación e información del equipo de los equipos cliente.



## Temas relacionados


[Introducción a MBAM 2.5](getting-started-with-mbam-25.md)

[Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Funciones mostradas de una implementación MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





