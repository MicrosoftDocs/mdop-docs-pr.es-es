---
title: Requisitos previos de implementación de MBAM 1.0
description: Requisitos previos de implementación de MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822661"
---
# Requisitos previos de implementación de MBAM 1.0


Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), asegúrese de cumplir los requisitos previos necesarios para instalar el producto. Esta sección contiene información que le ayudará a preparar correctamente su entorno de equipos antes de implementar los clientes y las características de servidor de MBAM.

## Requisitos previos de instalación de las características de MBAM Server


Cada una de las características del servidor de MBAM tiene requisitos previos específicos que deben cumplirse para poder instalarse correctamente. El programa de instalación de MBAM verifica si se cumplen todos los requisitos previos antes de que se inicie la instalación.

### Requisitos previos de instalación para el servidor de administración y supervisión

La tabla siguiente contiene los requisitos previos de instalación para el servidor de supervisión y administración de MBAM:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Rol de servidor de Windows ServerWeb</strong></p></td>
<td align="left"><p>Este rol debe agregarse a un sistema operativo de servidor compatible con la característica servidor de administración y supervisión de Mbam.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Herramientas de administración de servidor Web (IIS)</strong></p></td>
<td align="left"><p><strong>Scripts y herramientas de administración de IIS</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Servicios de rol de servidor Web</strong></p></td>
<td align="left"><p><strong>Características HTTP comunes:</strong></p>
<ul>
<li><p>Contenido estático</p></li>
<li><p>Documento predeterminado</p></li>
</ul>
<p><strong>Desarrollo de aplicaciones:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidad de .NET</p></li>
<li><p>Extensiones ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Seguridad</strong></p>
<ul>
<li><p>Autenticación de Windows</p></li>
<li><p>Filtrado de solicitudes</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Características de Windows Server</strong></p></td>
<td align="left"><p><strong>Características de Microsoft .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Activación de WCF</p>
<ul>
<li><p>Activación HTTP</p></li>
<li><p>Activación no HTTP</p></li>
</ul></li>
</ul>
<p><strong>Servicio de activación de procesos de Windows</strong></p>
<ul>
<li><p>Modelo de proceso</p></li>
<li><p>Entorno .NET</p></li>
<li><p>API de configuración</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Nota:**  Para obtener una lista de los sistemas operativos compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).

 

### Requisitos previos de instalación para los informes de cumplimiento y cumplimiento

Los informes de cumplimiento y cumplimiento deben instalarse en una versión compatible de SQLServer. Los requisitos previos de instalación de esta característica incluyen SQL Server Reporting Services (SSRS).

SSRS debe instalarse y ejecutarse durante la instalación de MBAM Server. Los informes también deben configurarse en modo "nativo", no en el modo "no configurado" o "SharePoint".

**Nota:**  Para obtener una lista de los sistemas operativos y las versiones de SQLServer compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).

 

### Requisitos previos de instalación para la base de datos de recuperación y hardware

La base de datos de recuperación y de hardware debe instalarse en una versión compatible de SQLServer.

SQL Server debe tener servicios del motor de base de datos instalados y ejecutándose durante la instalación del servidor MBAM. La característica cifrado de datos transparente (TDE) debe estar habilitada.

**Nota:**  Para obtener una lista de los sistemas operativos y las versiones de SQLServer compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).

 

La característica TDE SQLServer realiza el cifrado de entrada/salida (e/s) en tiempo real y el descifrado de los archivos de datos y de registro. TDE protege los datos que están "en reposo", que incluyen los datos y los archivos de registro. Proporciona la capacidad de cumplir con muchas leyes, normativas y directrices establecidas en varias industrias.

**Nota:**  Como TDE realiza el descifrado en tiempo real de la información de la base de datos, la información de la clave de recuperación estará visible si la cuenta con la que ha iniciado sesión tiene permisos para la base de datos al ver las tablas de SQL de información de claves de recuperación.

 

### Requisitos previos de instalación para la base de datos de cumplimiento y auditoría

La base de datos de cumplimiento y auditoría debe instalarse en una versión compatible de SQLServer.

SQL Server debe tener servicios del motor de base de datos instalados y ejecutándose durante la instalación de MBAM Server.

**Nota:**  Para obtener una lista de los sistemas operativos y las versiones de SQLServer compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).

 

## Requisitos previos de instalación para clientes de MBAM


Los requisitos previos necesarios que debe cumplir antes de iniciar la instalación del cliente de MBAM son los siguientes:

-   Módulo de plataforma segura (TPM) versión 1.2

-   El chip TPM debe estar activado en el BIOS y debe reestablecerse desde el sistema operativo. Para obtener más información, consulte la documentación de BIOS.

**ADVERTENCIA**  Asegúrese de que el teclado, el mouse y el vídeo estén directamente conectados al equipo, en lugar de a un conmutador de teclado, vídeo, ratón (KVM). Un conmutador KVM puede interferir con la capacidad del equipo de detectar la presencia física del hardware.

 

## Temas relacionados


[Planificar la implementación de MBAM 1.0](planning-to-deploy-mbam-10.md)

[Configuraciones admitidas de MBAM 1.0](mbam-10-supported-configurations.md)

 

 





