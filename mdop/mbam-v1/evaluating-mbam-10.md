---
title: Evaluación de MBAM 1.0
description: Evaluación de MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825251"
---
# Evaluación de MBAM 1.0


Antes de implementar administración y supervisión de Microsoft BitLocker (MBAM) en un entorno de producción, debe evaluarlo en un entorno de laboratorio. Puede usar la información de este tema para configurar MBAM en un solo entorno de laboratorio de servidor con fines de evaluación.

Aunque los pasos de implementación reales son muy similares al escenario que se describe en [Cómo instalar y configurar MBAM en un solo servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), este tema contiene información adicional que le permite configurar un entorno de evaluación de MBAM en el mínimo tiempo.

## Configurar el entorno de laboratorio


Incluso cuando configure una instancia de MBAM que no sea de producción para que se evalúe en un entorno de laboratorio, debe comprobar que cumple los requisitos previos de implementación y los requisitos de hardware y software. Para obtener más información, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md). También debe revisar la [preparación del entorno para MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de comenzar la implementación de evaluación de MBAM.

### Planear una implementación de evaluación de MBAM

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
<td align="left"><p>Revise la información de introducción sobre MBAM para obtener un conocimiento básico del producto antes de empezar con el plan de implementación.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">Introducción a MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>Prepare su entorno informático para la instalación de MBAM. Para ello, debe habilitar el cifrado de datos transparente (TDE) en las instancias de SQL Server que hospedarán las bases de datos de MBAM. Para habilitar TDE en su entorno de laboratorio, puede crear un archivo. SQL para ejecutarlo en la base de datos Master que se hospeda en la instancia de SQL Server que usará MBAM.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Puede usar el ejemplo siguiente para crear un archivo. SQL para su entorno de laboratorio con el fin de habilitar rápidamente TDE en la instancia de SQL Server que hospedará las bases de datos de MBAM. Estos comandos de SQL Server habilitarán TDE mediante el uso de un certificado de SQL Server firmado localmente. Asegúrese de realizar una copia de seguridad del certificado TDE y de su clave de cifrado asociada al ejemplo de la ruta de copia de seguridad local de <em> C:\backup </em> . El certificado TDE y la clave son obligatorios al recuperar la base de datos o al mover el certificado y la clave a otro servidor que tenga el cifrado de TDE.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">Requisitos previos de implementación de MBAM 1.0</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">Cifrado de base de datos en SQL Server 2008 Enterprise Edition</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear y configurar los requisitos de la Directiva de grupo de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">Planificación de los requisitos de directiva de grupo de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planee y cree los grupos de seguridad necesarios de los servicios de dominio de Active Directory y plan para MBAM requisitos de pertenencia a grupos de seguridad local.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planificación de roles de administrador de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear la implementación de características de MBAM Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">Planificación para la implementación de servidores de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planear la implementación de cliente de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">Planificación para la implementación de clientes de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Realizar una implementación de evaluación de MBAM

Después de completar las instalaciones necesarias de planeación y de software necesarias para preparar el entorno informático para una instalación MBAM, puede iniciar la implementación de evaluación de MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise la información de configuraciones admitidas de MBAM para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configuraciones admitidas de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en un solo servidor con fines de evaluación.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">Cómo instalar y configurar MBAM en un único servidor</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Agregue los grupos de seguridad de los servicios de dominio de Active Directory que creó durante la fase de planeación a los grupos locales de la MBAM de servidor local correspondiente en el nuevo servidor de MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planificación de los roles de administrador de MBAM 1,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Cómo administrar los roles de administrador de MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Cree e implemente los objetos de directiva de grupo MBAM obligatorios.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Implementación de objetos de directiva de grupo de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implemente el software de cliente de MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Implementación de cliente de MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Configurar los equipos de laboratorio para la evaluación de MBAM


Puede cambiar la configuración de frecuencia en los informes de estado del cliente de MBAM mediante el editor del registro. Sin embargo, estas modificaciones deberían usarse solo con fines de prueba.

**Advertencia**  
En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro. Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows. Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro. Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver. Cambie el registro bajo su propia responsabilidad.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>Modificar la configuración de frecuencia de los informes de estado de cliente de MBAM

Las frecuencias de los informes de estado y la activación del cliente de MBAM tienen un valor mínimo de 90 minutos cuando se establecen para usar una directiva de grupo. Puede cambiar estas frecuencias en MBAM equipos cliente editando el registro de Windows con valores más bajos, que le ayudarán a acelerar las pruebas. Para modificar la configuración de frecuencia en la creación de informes de estado de cliente de MBAM, use un editor del registro para ir a **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, cambie los valores de **ClientWakeupFrequency** y **StatusReportingFrequency** a **1** como valor mínimo admitido por el cliente y, a continuación, reinicie el servicio cliente de administración de BitLocker. Cuando realices este cambio, el cliente de MBAM se informará cada minuto. Puede configurar los valores como bajo solo cuando lo haga de forma manual en el registro.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>Modificar el retraso de inicio en el servicio de cliente de MBAM

Además de las frecuencias de los informes de estado y la activación del cliente de MBAM, se produce un retraso aleatorio de hasta 90 minutos cuando el servicio agente de cliente de MBAM se inicia en los equipos cliente. Si no desea el retraso aleatorio, cree un valor **DWORD** de **NoStartupDelay** en **HKLM\\Software\\Microsoft\\MBAM**, establezca su valor en **1**y, a continuación, reinicie el servicio de cliente de administración de BitLocker.

## Temas relacionados


[Introducción a MBAM 1.0](getting-started-with-mbam-10.md)









