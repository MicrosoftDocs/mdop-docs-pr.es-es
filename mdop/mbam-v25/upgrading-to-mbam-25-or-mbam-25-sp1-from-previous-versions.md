---
title: Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores
description: Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812751"
---
# Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores


En este tema se describe el proceso de actualización del servidor de administración y supervisión de Microsoft BitLocker (MBAM) y el cliente de MBAM de versiones anteriores de MBAM.

**Nota:**  Puede actualizar directamente a MBAM 2,5 o MBAM 2,5 SP1 desde cualquier versión anterior de MBAM.

 

## Antes de iniciar la actualización


Revise la siguiente información antes de iniciar la actualización.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Qué debe saber antes de empezar</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Si va a instalar los sitios web de MBAM en un servidor y los servicios web en otro servidor, tiene que usar los cmdlets de Windows PowerShell para configurarlos.</p></td>
<td align="left"><p>El Asistente para la configuración del servidor de MBAM no admite la configuración de los sitios web en un servidor y los servicios web en otro servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Si está actualizando a MBAM 2.5 o 2,5 SP1 desde MBAM 2.0 o 2,0 SP1 en Windows Server2008 R2:</p>
<p>El sitio web de administración y supervisión y el portal de autoservicio no funcionan si instala el software de .NET Framework 4.5 requerido después de que los servicios de Internet Information Server (IIS) ya estén instalados.</p>
<p>Este problema se produce porque ASP.NET no se puede registrar correctamente con IIS si .NET Framework está instalado después de haber instalado IIS.</p></td>
<td align="left"><p><strong>Para resolver este problema:</strong></p>
<p>Ejecute <strong> Aspnet_regiis – i </strong> desde la siguiente ubicación:</p>
<p>C:\windows\microsoft.net\Framework\v4.0.30319</p>
<p>Para obtener más información, vea: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> herramienta de registro de IIS de ASP.net </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registre un SPN en la cuenta del grupo de aplicaciones si se cumplen todas las condiciones siguientes:</p>
<ul>
<li><p>Está actualizando desde una versión anterior de MBAM.</p></li>
<li><p>Por el momento, no está ejecutando los sitios web de MBAM en una configuración distribuida o con equilibrio de carga, pero le gustaría hacerlo al actualizar a MBAM 2.5 o 2,5 SP1.</p></li>
</ul></td>
<td align="left"><p>Para obtener instrucciones, consulte <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> planear cómo proteger los sitios web de MBAM </a> .</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>¿Qué recomendamos?</strong></p></td>
<td align="left"><p>Registre un nombre principal de servicio (SPN) para la cuenta del grupo de aplicaciones, aunque es posible que ya tenga SPN registrados para la cuenta de la máquina.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>¿Por qué lo recomendamos?</strong></p></td>
<td align="left"><p>Es necesario registrar un SPN en la cuenta del grupo de aplicaciones para configurar los sitios web en una configuración distribuida o con equilibrio de carga.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>¿Qué sucede si los SPN ya están configurados en una cuenta de equipo?</strong></p></td>
<td align="left"><p>MBAM usará los SPN que ya ha registrado y no necesita configurar SPN adicionales, pero no podrá configurar los sitios web en una configuración distribuida o con equilibrio de carga.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## Pasos para actualizar la infraestructura del servidor de MBAM


Siga los pasos que se indican en las siguientes secciones para actualizar MBAM para la topología independiente o la topología de integración de System Center Configuration Manager.

**Para actualizar la infraestructura de servidor de MBAM para una topología independiente**

1.  Desinstale las versiones anteriores de MBAM de los **programas y las características** , así como de los servidores Web, para asegurarse de que la información no se escribe desde los clientes de MBAM a la infraestructura de MBAM. Para obtener instrucciones, consulte [quitar características o software de MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Realizar copias de seguridad de las bases de datos.

3.  Desinstalar versiones anteriores de MBAM de SQL Server mediante **programas y características**, entre los que se incluyen los servidores SQL que hospedan los informes de MBAM a través de SQL Server Reporting Services. Quite los archivos o carpetas temporales restantes de MBAM Server del servidor de base de datos y de Reporting Services.

    **Nota:**  Las bases de datos no se quitarán y todos los datos de cumplimiento y de seguridad se mantendrán en la base de datos.

     

4.  Instale y configure las bases de datos de MBAM 2.5 o 2,5 SP1, los informes y las aplicaciones Web, en ese orden. Las bases de datos se actualizan en su lugar.

5.  Actualice los objetos de directiva de grupo (GPO) con las plantillas de MBAM 2,5 para aprovechar las nuevas características de MBAM, como el cifrado obligatorio. Si no actualiza los GPO y el cliente de MBAM a MBAM 2,5, las versiones anteriores de los clientes de MBAM seguirán informando de sus GPO actuales con funciones reducidas. Consulte [Cómo obtener las plantillas](https://www.microsoft.com/download/details.aspx?id=41183) de la Directiva de grupo de MDOP para descargar las últimas plantillas ADMX.

    Después de actualizar la infraestructura del servidor de MBAM, los equipos cliente existentes continúan reportándose correctamente al servidor de MBAM 2.5 o 2,5 SP1 y los datos de recuperación continúan siendo almacenados.

6.  Instale el último cliente de MBAM 2.5 o 2,5 SP1. Los equipos cliente no necesitan reiniciarse después de la implementación.

**Para actualizar la infraestructura de MBAM para la topología de integración de System Center Configuration Manager**

1.  Desinstale las versiones anteriores de MBAM de los **programas y las características** , así como de los servidores Web, para asegurarse de que la información no se escribe desde los clientes de MBAM a la infraestructura de MBAM. Para obtener instrucciones, consulte [quitar características o software de MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Realizar copias de seguridad de las bases de datos.

3.  Desinstalar versiones anteriores de MBAM de SQL Server mediante **programas y características**, entre los que se incluyen los servidores SQL que hospedan los informes de MBAM a través de SQL Server Reporting Services. Quite los archivos o carpetas temporales restantes de MBAM Server del servidor de base de datos y de Reporting Services.

4.  Desinstale MBAM del servidor de Configuration Manager.

    **Nota:**  Las bases de datos y los objetos de Configuration Manager (línea base, MBAM la colección de equipos admitidos e informes) no se quitarán y todos los datos de cumplimiento y de cumplimiento se mantienen en la base de datos.

     

5.  Actualice los archivos. mof.

6.  Instale y configure las bases de datos de MBAM 2.5 o 2,5 SP1, los informes, las aplicaciones web y la integración de Configuration Manager, en ese orden. Los objetos de las bases de datos y del administrador de configuración se han actualizado en su lugar.

7.  De manera opcional, actualice los objetos de directiva de grupo (GPO) y edite la configuración si desea implementar nuevas características en MBAM, como el cifrado exigido. Si no actualiza los GPO, MBAM seguirá informando de sus GPO actuales. Consulte [Cómo obtener las plantillas](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) de la Directiva de grupo de MDOP para descargar las últimas plantillas ADMX.

    Después de actualizar la infraestructura del servidor de MBAM, los equipos cliente existentes continúan reportándose correctamente al servidor de MBAM 2.5 o 2,5 SP1 y los datos de recuperación continúan siendo almacenados.

8.  Instale el último cliente de MBAM 2.5 o 2,5 SP1. Los equipos cliente no necesitan reiniciarse después de la implementación.

## Compatibilidad de actualización para el cliente de MBAM


MBAM admite actualizaciones para el cliente de MBAM 2.5 desde cualquier versión anterior del cliente de MBAM.

**Formas de instalar el cliente de MBAM:**

-   Actualice los equipos que ejecutan el cliente de MBAM todos a la vez o gradualmente después de instalar la infraestructura de servidor de la versión 2.5 de MBAM.

-   Instale el cliente de MBAM a través de un sistema electrónico de distribución de software o mediante herramientas como Active Directory Domain Services o System Center Configuration Manager.



## Temas relacionados


[Implementación de MBAM 2.5](deploying-mbam-25.md)

[Implementación de cliente de MBAM 2.5](deploying-the-mbam-25-client.md)

[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





