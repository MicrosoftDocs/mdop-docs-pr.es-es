---
title: Planeación de la implementación de MBAM con Administrador de configuración
description: Planeación de la implementación de MBAM con Administrador de configuración
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825630"
---
# Planeación de la implementación de MBAM con Administrador de configuración


Para implementar MBAM con la topología de Configuration Manager, se recomienda una arquitectura de tres servidores, que admite clientes de 200.000. Use un servidor independiente para ejecutar Configuration Manager e instale las características básicas de administración y supervisión en dos servidores, tal y como se muestra en la imagen arquitectura de [Introducción-uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).

**Importante**  
Windows to go no se admite al instalar la topología integrada de MBAM con Configuration Manager 2007.



## Requisitos previos de implementación para la instalación de MBAM con Configuration Manager


Asegúrese de cumplir los siguientes requisitos previos antes de instalar MBAM con Configuration Manager:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Información adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Asegúrese de que el servidor de Configuration Manager es un sitio principal en el sistema del administrador de configuración.</p></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="even">
<td align="left"><p>Habilite el agente cliente de inventario de hardware en el servidor de Configuration Manager.</p></td>
<td align="left"><p>Para el administrador de configuración 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Cómo configurar el inventario de hardware para un sitio </a> .</p>
<p>Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Cómo configurar el inventario de hardware en Configuration Manager </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Habilite el agente de administración de configuración deseada (DCM) o la configuración de cumplimiento, en función de la versión del administrador de configuración que esté usando.</p></td>
<td align="left"><p>Para el administrador de configuración 2007, habilite las <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> propiedades de agente del cliente de administración de configuración deseada </a> .</p>
<p>Para System Center 2012 Configuration Manager, vea configuración <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> de las opciones de cumplimiento en Configuration Manager </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Defina un punto de servicios de informes en Configuration Manager. Necesario para SQL Reporting Services.</p></td>
<td align="left"><p>Para Configuration Manager 2007, vea <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Cómo crear un punto de servicios de informes para SQL Reporting Services </a> .</p>
<p>Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requisitos previos para informes en Configuration Manager </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Versiones compatibles con Configuration Manager


MBAM admite las siguientes versiones de Configuration Manager:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión compatible</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 o posterior</p></td>
<td align="left"><p>64 bits</p>
<div class="alert">
<strong>Nota</strong><br/><p>Aunque Configuration Manager 2007 es de 32 bits, debe instalarlo y SQL Server en un sistema operativo de 64 bits para que coincida con el software de MBAM de 64 bits.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Administrador de configuración de Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



Para obtener una lista de las configuraciones admitidas para el servidor de Configuration Manager, consulte la página web correspondiente a la versión de Configuration Manager que está usando. MBAM no tiene requisitos de sistema adicionales para el servidor de Configuration Manager.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> Requisitos del sistema de MBAM y SQL Server


Las configuraciones compatibles y los requisitos del sistema para los servidores de MBAM y SQL Server para la topología del administrador de configuración son iguales a los de la topología independiente. Para conocer los requisitos del sistema independientes, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Para el servidor de MBAM y los requisitos de espacio en el procesador, la RAM y el espacio de disco de SQL Server para la topología de Configuration Manager, consulte las secciones siguientes.

## Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server para MBAM


En la siguiente tabla se enumeran los requisitos de procesador, RAM y espacio de disco del servidor para los servidores de MBAM cuando se usa la topología de integración de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Encargado del tratamiento de datos</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o más</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espacio libre en el disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



## Requisitos de procesador, memoria RAM y espacio en disco de SQL Server


En la tabla siguiente se enumeran los requisitos de procesador, RAM y espacio de disco del servidor de SQL Server cuando se usa la topología de integración de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de hardware</th>
<th align="left">Requisito mínimo</th>
<th align="left">Requisito recomendado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Encargado del tratamiento de datos</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o más</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espacio libre en el disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB o más</p></td>
</tr>
</tbody>
</table>



## Permisos necesarios para instalar el servidor de MBAM


Para instalar MBAM con Configuration Manager, debe disponer de un usuario administrativo en Configuration Manager que tenga un rol de seguridad con los permisos mínimos que se indican en la tabla siguiente. En la tabla también se muestran los derechos que debe tener, además de los derechos de administrador de equipo básicos, para instalar el servidor MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permisos</th>
<th align="left">Característica de MBAM Server</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Roles de servidor de inicio de sesión de instancias de SQL:-dbcreator-processadmin</p></td>
<td align="left"><p>- Base de datos de recuperación: base de datos de auditoría</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de instancia de SQL Server Reporting Services:-crear carpetas-publicar informes</p></td>
<td align="left"><p>- Integración de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**System Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permisos</th>
<th align="left">Característica servidor de Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Derechos de sitio de Configuration Manager:-leer</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de recopilación de Configuration Manager:-crear, eliminar-leer-modificar-implementar elementos de configuración</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Derechos de elemento de configuración de Configuration Manager:-crear-eliminar-leer</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Configuration Manager2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permisos</th>
<th align="left">Característica servidor de Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Derechos de sitio de Configuration Manager:-leer</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de recopilación de Configuration Manager:-Create-Delete-Read-ReadResource</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Derechos del elemento de configuración del administrador de configuración:-crear-eliminar-lectura-distribuir</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Orden de implementación de características de MBAM para la topología del administrador de configuración


Al implementar MBAM en el servidor de Configuration Manager, debe completar las tareas de implementación en el siguiente orden:

1.  Edite el archivo Configuration. mof en el servidor de Configuration Manager.

2.  Cree o edite el servidor de administración de archivos SMS \ _def. mof.

3.  Instale MBAM en el servidor de Configuration Manager.

4.  Instale la base de datos de recuperación y la base de datos de auditoría en el servidor de bases de datos.

5.  Instale las características de MBAM en el servidor de administración y supervisión.

## Lista de comprobación de la planificación para instalar MBAM con Configuration Manager


En esta lista de comprobación se describen los pasos recomendados y una lista de nivel superior de elementos que se deben tener en cuenta al planear una implementación de administración y supervisión de Microsoft BitLocker con Configuration Manager. Se recomienda copiar esta lista de comprobación en un programa de hoja de cálculo y personalizarla para su uso.

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
<td align="left"><p>Revise la información de introducción, que describe cómo Configuration Manager funciona con MBAM y muestra la arquitectura de alto nivel recomendada.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">Tareas iniciales: Uso de MBAM con Administrador de configuración</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la información de planeación, que describe los requisitos previos de implementación, las configuraciones admitidas, los permisos necesarios y el orden de implementación de cada característica.</p></td>
<td align="left"><p>Planeación de la implementación de MBAM con Administrador de configuración</p></td>
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
<td align="left"><p>Planee y cree los grupos de seguridad necesarios de los servicios de dominio de Active Directory y plan para MBAM requisitos de pertenencia a grupos de seguridad local.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planificación de roles de administrador de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear la implementación de la implementación de cliente de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planeación para la implementación de clientes de MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Uso de MBAM con Administrador de configuración](using-mbam-with-configuration-manager.md)









