---
title: Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración
description: Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825761"
---
# Arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager

En este tema se describe la arquitectura recomendada para implementar Microsoft BitLocker Administration and Monitoring (MBAM) con la topología de integración de Configuration Manager. Esta topología integra MBAM con System Center Configuration Manager. Para implementar MBAM con la topología independiente, consulte [arquitectura de alto nivel de MBAM 2,5 con topología independiente](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

Para obtener una lista de las versiones compatibles del software mencionadas en este tema, consulte [MBAM 2,5 configuraciones admitidas](mbam-25-supported-configurations.md).

**Importante**  Windows to go no es compatible con la instalación de la topología de integración de Configuration Manager al usar el administrador de configuración 2007.

 

## Número recomendado de servidores y número de clientes admitidos


El número recomendado de servidores y la cantidad de clientes admitidos en un entorno de producción es el siguiente:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquitectura recomendada</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Número de servidores y otros equipos</p></td>
<td align="left"><p>Tres servidores</p>
<p>Una estación de trabajo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Número de equipos cliente admitidos</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Diferencias entre la integración de Configuration Manager y las topologías independientes


Las principales diferencias entre las topologías son las siguientes:

-   Las características de cumplimiento e informes se quitan de MBAM y se obtiene acceso a ellas desde Configuration Manager.

-   Los informes se ven desde la consola de administración de Configuration Manager, con la excepción del informe de auditoría de recuperación, que continúa viendo desde el sitio web de supervisión y administración de MBAM.

## Arquitectura de alto nivel recomendada de MBAM con la topología de integración de Configuration Manager


En el siguiente diagrama y tabla se describe la arquitectura de alto nivel recomendada para MBAM con la topología de integración de Configuration Manager. MBAM implementaciones de varios bosques requieren una confianza unidireccional o bidireccional. Las relaciones de confianza unidireccionales requieren que el dominio de servidor confíe en el dominio de cliente.

![mbam2\-5](images/mbam2-5-cmserver.png)

### Servidor de bases de datos

#### Base de datos de recuperación

Esta característica está configurada en un equipo con Windows Server y una instancia de SQL Server compatible.

La **base** de datos de recuperación almacena los datos de recuperación que se recopilan de MBAM equipos cliente.

#### Base de datos de auditoría

Esta característica está configurada en un equipo con Windows Server y una instancia de SQL Server compatible.

La **base** de datos de auditoría almacena los datos de actividad que se recopilan de los equipos cliente que han tenido acceso a datos de recuperación.

#### Informes

Esta característica está configurada en un equipo con Windows Server y una instancia de SQL Server compatible.

Los **informes** proporcionan datos de auditoría de recuperación para los equipos cliente de su empresa. Puede ver los informes desde la consola de Configuration Manager o directamente desde SQL Server Reporting Services.

### Servidor de sitio primario de Configuration Manager

Característica de integración de System Center Configuration Manager

-   Esta característica está configurada en el servidor de sitio primario de Configuration Manager, que es el servidor de nivel superior de la infraestructura de Configuration Manager.

-   El **servidor de Configuration Manager** recopila la información de inventario de hardware de los equipos cliente y se usa para notificar la compatibilidad de BitLocker de equipos cliente.

-   Al ejecutar el Asistente para la configuración de supervisión y administración de Microsoft BitLocker para instalar el software de servidor, la colección de equipos compatibles con MBAM, la línea base de configuración y los informes se configuran en el servidor de sitio primario de Configuration Manager.

-   La **consola de Configuration Manager** debe instalarse en el mismo equipo en el que se instala el software de servidor MBAM.

### Servidor de administración y supervisión

#### Sitio web de administración y supervisión

Esta característica está configurada en un equipo con Windows Server.

El **sitio web de administración y supervisión** se usa para:

-   Ayudar a los usuarios finales a recuperar el acceso a sus equipos cuando están bloqueados. (Esta área del sitio Web suele denominarse Servicio de asistencia).

-   Vea el informe de auditoría de recuperación, que muestra la actividad de recuperación de los equipos cliente. Otros informes se visualizan desde la consola de Configuration Manager.

#### Portal de autoservicio

Esta característica está configurada en un equipo con Windows Server.

El **portal de autoservicio** es un sitio web que permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker.

#### Supervisión de servicios web para este sitio web

Esta característica se instala en un equipo con Windows Server.

El cliente de MBAM y los sitios web usan los **servicios Web de supervisión** para comunicarse con la base de datos.

**Importante**<br>El servicio Web de supervisión ya no está disponible en Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 porque los sitios web de MBAM se comunican directamente con la base de datos de recuperación. 

 

### Estación de trabajo de administración

#### MBAM plantillas de directiva de grupo

-   Las **plantillas de directiva de grupo MBAM** son configuraciones de directiva de grupo que definen la configuración de implementación de MBAM, que le permiten administrar el cifrado de unidad BitLocker.

-   Antes de ejecutar MBAM, debe descargar las plantillas de directiva de grupo de [Cómo obtener las plantillas de la Directiva de grupo de MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) y copiarlas en un servidor o estación de trabajo que ejecute un sistema operativo Windows Server o Windows compatible.

    **NOTA**<br>La estación de trabajo no tiene que ser un equipo dedicado.

     

### Equipo cliente de Configuration Manager y cliente de MBAM

#### Software de cliente de MBAM

El **cliente de MBAM**:

-   Usa objetos de directiva de grupo para exigir el cifrado de unidad BitLocker en equipos cliente de la empresa.

-   Recopila la clave de recuperación de BitLocker para tres tipos de unidades de datos: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).

-   Recopila información de recuperación e información del equipo de los equipos cliente.

#### Cliente del Administrador de configuración

El **cliente de Configuration Manager** permite a Configuration Manager recopilar datos de compatibilidad de hardware sobre los equipos cliente y notificar información de cumplimiento.

 

## Diferencias en la implementación de MBAM para las versiones compatibles de Configuration Manager


Al implementar MBAM con la topología de integración de Configuration Manager, puede instalar MBAM en un servidor de sitio primario. Sin embargo, la instalación de MBAM funciona de manera diferente para el administrador de configuración de Center2012 de configuración y Manager2007 de configuración.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de Configuration Manager</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Administrador de configuración del sistema Center2012 R2</p>
<p>Administrador de configuración de Center2012 del sistema</p></td>
<td align="left"><p>Si instala MBAM en un servidor de sitio principal o en un servidor de administración central, MBAM realiza todas las acciones de instalación en ese servidor de sitio.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración Manager2007 R2</p>
<p>Configuración Manager2007</p></td>
<td align="left"><p>Si instala MBAM en un servidor de sitio principal que forma parte de una jerarquía de administrador de configuración superior con un servidor principal de sitio central, MBAM identifica el servidor principal del sitio central y realiza todas las acciones de instalación en ese servidor principal. La instalación incluye la comprobación de los requisitos previos y la instalación de los objetos e informes de Configuration Manager.</p>
<p>Por ejemplo, si instala MBAM en un servidor de sitio principal que es un elemento secundario de un servidor principal del sitio central, MBAM instala todos los objetos e informes de Configuration Manager en el servidor principal. Si instala MBAM en el servidor principal, MBAM realiza todas las acciones de instalación en ese servidor principal.</p></td>
</tr>
</tbody>
</table>

 

## Cómo funciona MBAM con Configuration Manager


La integración de MBAM con Configuration Manager se basa en un paquete de configuración que instala los elementos que se describen en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementos instalados en Configuration Manager</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Datos de configuración</p></td>
<td align="left"><p>Los datos de configuración instalan una línea base de configuración, denominada "protección de BitLocker", que contiene dos elementos de configuración:</p>
<ul>
<li><p>Protección de unidades del sistema operativo BitLocker</p></li>
<li><p>Protección de las unidades de datos fijas de BitLocker</p></li>
</ul>
<p>La línea base de configuración se implementa en la colección de equipos MBAM compatibles, que también se crea cuando se instala MBAM.</p>
<p>Los dos elementos de configuración proporcionan la base para evaluar el estado de cumplimiento de los equipos cliente. Esta información es capturada, almacenada y evaluada en Configuration Manager.</p>
<p>Los elementos de configuración se basan en los requisitos de cumplimiento para las unidades de sistema operativo y las unidades de datos fijas. La información necesaria para los equipos implementados se recopila para que se pueda evaluar la conformidad de esos tipos de unidades.</p>
<p>De forma predeterminada, la línea base de configuración evalúa el estado de cumplimiento every12 horas y envía los datos de cumplimiento a Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Colección de equipos compatibles con MBAM</p></td>
<td align="left"><p>MBAM crea una colección que se denomina MBAM equipos compatibles. La línea base de configuración está destinada a los equipos cliente de esta colección.</p>
<p>Esta es una colección dinámica. De forma predeterminada, ejecuta every12 horas y evalúa la pertenencia según tres criterios:</p>
<ul>
<li><p>El equipo es una versión compatible del sistema operativo Windows.</p></li>
<li><p>El equipo es un equipo físico. No se admiten máquinas virtuales.</p></li>
<li><p>El equipo tiene un módulo de plataforma segura (TPM) que está disponible. Se necesita una versión compatible de TPM 1.2 o posterior para Windows7. Windows10, Windows 8.1, Windows8 y Windows to go no requieren TPM.</p></li>
</ul>
<p>La colección se evalúa en todos los equipos y se crea un subconjunto de equipos compatibles, lo que proporciona la base para la evaluación de cumplimiento y los informes para la integración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Informes</p></td>
<td align="left"><p>Al configurar MBAM con la topología de integración de Configuration Manager, verá todos los informes en Configuration Manager, excepto el informe de auditoría de recuperación, el último de los cuales continúa en el sitio web de administración y supervisión de MBAM. Los informes disponibles en Configuration Manager son:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Informe</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Panel de cumplimiento de BitLocker Enterprise</p></td>
<td align="left"><p>Proporciona a los administradores de ti tres vistas de información en un solo informe: distribución del estado de cumplimiento, no conforme a la distribución de errores y distribución del estado de cumplimiento según el tipo de unidad. Las opciones de desglose en el informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado seleccionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles de la compatibilidad con BitLocker Enterprise</p></td>
<td align="left"><p>Permite a los administradores de ti ver información sobre el estado de compatibilidad con el cifrado de BitLocker de la empresa e incluye el estado de cumplimiento de cada equipo. Las opciones de desglose en el informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado seleccionado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cumplimiento de BitLocker Computer</p></td>
<td align="left"><p>Permite a los administradores de ti ver un equipo individual y determinar por qué se ha notificado con un estado de conforme o no compatible. El informe también muestra el estado de cifrado de las unidades de sistema operativo y las unidades de datos fijas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Resumen de cumplimiento de BitLocker Enterprise</p></td>
<td align="left"><p>Permite a los administradores de ti ver el estado del cumplimiento de la Directiva de MBAM en la empresa. El estado de cada equipo es evaluado y el informe muestra un resumen de la compatibilidad de todos los equipos de la empresa con la Directiva. Las opciones de desglose en el informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado seleccionado.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados


[Introducción a MBAM 2.5](getting-started-with-mbam-25.md)

[Arquitectura de alto nivel de MBAM 2.5 con topología independiente](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Funciones mostradas de una implementación MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




