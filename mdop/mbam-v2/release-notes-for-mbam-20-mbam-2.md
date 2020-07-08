---
title: Notas de la versión de MBAM 2.0
description: Notas de la versión de MBAM 2.0
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825590"
---
# Notas de la versión de MBAM 2.0


Para buscar estas notas de la versión, presione Ctrl + F.

Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLockerAdministration y Monitoring (MBAM) 2.0. Estas notas de la versión contienen información que se necesita para instalar correctamente BitLockerAdministration y monitor 2.0 y contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de MBAM 2.0, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## <a href="" id="---------mbam-2-0-known-issues"></a> Problemas conocidos de MBAM 2.0


Esta sección contiene notas de la versión para MBAM 2.0.

### El campo Nombre del equipo no puede aparecer en los informes de cumplimiento de los equipos con BitLocker y de la conformidad de BitLocker Enterprise al ejecutar MBAM con Microsoft System Center Configuration Manager 2007

El campo Nombre del equipo puede estar en blanco en los informes de cumplimiento de los equipos con BitLocker y de la compatibilidad de la empresa de BitLocker al usar MBAM con Configuration Manager 2007.

SOLUCIÓN alternativa: ninguno.

### El informe de cumplimiento empresarial no se actualiza después de actualizar la infraestructura de servidor de MBAM independiente

Si está usando la topología independiente MBAM y actualiza la infraestructura de servidor de la versión 1,0 a la 2,0, el informe de cumplimiento de la empresa no se actualizará.

SOLUCIÓN: después de la actualización, ejecute el siguiente script en la base de datos de cumplimiento y auditoría:

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### Los informes del portal del servicio de asistencia muestran una advertencia si SSL no está configurado en SSRS

Si SQL Server Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de los informes se establecerá en HTTP en lugar de HTTPS cuando instale el servidor MBAM. Si, a continuación, busca el portal del servicio de asistencia y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro".

SOLUCIÓN alternativa: para mostrar el informe, haga clic en **Mostrar todo el contenido**. Para solucionar este problema, vaya al equipo MBAM donde está instalado SQL Server Reporting Services, ejecute el **Administrador de configuración de Reporting Services**y, a continuación, haga clic en **URL de servicio Web**. Seleccione el certificado SSL adecuado para el servidor, escriba el puerto SSL adecuado (el puerto predeterminado es 443) y, a continuación, haga clic en **aplicar**.

### No se admiten instancias no predeterminadas de la base de datos de Configuration Manager

MBAM busca solo la instancia predeterminada de la base de datos de Configuration Manager en Configuration Manager 2007 y SystemCenter2012 ConfigurationManager. Si usa una instancia no predeterminada, no puede instalar MBAM.

SOLUCIÓN alternativa: ninguno.

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>Al hacer clic en "atrás" en el informe Resumen de cumplimiento, se puede producir un error

Si profundiza en un informe Resumen de cumplimiento y, a continuación, hace clic en el vínculo **atrás** en el informe de SSRS, se puede producir un error.

SOLUCIÓN alternativa: ninguno.

### El cifrado de espacio usado no funciona correctamente

Si cifra un equipo por primera vez después de instalar el cliente MBAM y ha establecido un objeto de directiva de grupo para implementar el cifrado solo de espacio usado, MBAM cifra de forma errónea todo el disco en lugar de cifrar solo el espacio usado por el disco. Si un equipo ya está cifrado cuando instala el cliente MBAM y ha establecido el mismo objeto de directiva de grupo, el cifrado funciona correctamente y cifra solo el espacio de disco usado en el equipo.

SOLUCIÓN alternativa: ninguno.

### La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos

Si no establece una intensidad de cifrado específica en el objeto de directiva de grupo **elegir método de cifrado de unidad y intensidad** de cifrado, el informe de cumplimiento de equipos de la topología de integración del administrador de configuración siempre muestra "desconocido" para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits. El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.

SOLUCIÓN alternativa: establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.

### La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración

Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.

SOLUCIÓN alternativa: ninguno. No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.

### La configuración de seguridad mejorada puede provocar que los informes no se muestren correctamente

Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca el mensaje "acceso denegado" cuando intente ver informes en el servidor de MBAM. De forma predeterminada, ESC se activa para proteger el servidor disminuyendo la exposición del servidor ante posibles ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.

SOLUCIÓN: Si el mensaje "acceso denegado" aparece al intentar ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada. También puede ver los informes desde otro equipo en el que la ESC no está habilitada.

### Se produce un error en la instalación de MBAM Server al actualizar de SQL Server 2008 a SQL Server 2012

Si actualiza SQL Server 2008 a SQL Server 2012 e intenta instalar la base de datos de cumplimiento y auditoría o la base de datos de recuperación, se produce un error en la instalación y se deshace. El error se produce porque el archivo de SQLCMD.exe necesario se quitó durante la actualización de SQL y el instalador de MBAM no lo puede encontrar. Las líneas del archivo de registro MSI pueden tener un aspecto similar al siguiente:

RunDbInstallScript de BD de recuperación de RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exede BD dB de recuperación: dbInstance-xxxxxx\\I01RunDbInstallScript de BD Recovery: sqlScript-C:\\Archivos de Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript de BD de recuperación: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript defaultFileName-MBAM _Recovery \ I01\\MSSQL\\DATA\\RunDbInstallScript de BD de recuperación de certificados: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperación de la BD CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de BD Recovery dB: comenzando a ejecutar el complemento de base de datos de recuperación scriptRunDbInstallScript recuperación de BD de BD: el archivo de registro SQLCMD se encuentra en C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript de BD de recuperación excepción: instalar la acción personalizada de la base de datos de recuperación excepción: el sistema no puede encontrar el archivo especificado

El Windows Installer de MBAM Server está codificado para encontrar la ruta de acceso SQLCMD.exe en el valor de la cadena de ruta de acceso en el registro en HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. La clave sigue presente durante la migración de SQL Server 2008 a SQL Server 2012, pero la ruta de acceso a la que hace referencia el valor de los datos no contiene el archivo de SQLCMD.exe, porque el proceso de actualización de SQL ha eliminado el archivo.

SOLUCIÓN alternativa: Cambie temporalmente el valor de la cadena de ruta de acceso HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup a **path \ _old**y vuelva a ejecutar el Windows Installer del servidor de MBAM. Cuando la instalación se complete correctamente y cree las bases de datos en SQL Server 2012, cambie el nombre de la **ruta de acceso \ _old** valor a **path**.

## Revisiones y artículos de Knowledge base para MBAM 2.0


Esta sección contiene revisiones y artículos de KB para MBAM 2.0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artículo de KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>Instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falla con los &quot; objetos de System Center cm ya instalados&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Los usuarios no pueden recuperar la clave de recuperación de BitLocker con el portal de autoservicio de MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>El cliente de MBAM no funcionaba con el identificador de evento 4 y el código de error 0x8004100E en la descripción del evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Mensaje de error "error de servidor en '/Reports ' aplicación" al hacer clic en la pestaña informes en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Error al abrir informes de cumplimiento de los equipos o de la empresa en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Los informes de empresa de MBAM no se actualizan</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>No se admite la instalación de MBAM en un controlador de dominio</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Recibe el código de error 0x80071a90 durante la instalación independiente o de integración del administrador de configuración de MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM y comunicaciones seguras de red</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>El programa de instalación de MBAM 2.0 falla durante el escenario de integración de Configuration Manager con SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>Se produce un error en la instalación de MBAM si SQL SSRS no se ha configurado correctamente</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>La instalación de MBAM 2,0 produce un &quot; error al recuperar la configuración del rol de servidor de Configuration Manager para &#39;rol de&#39; de punto de servicios de informes&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Los informes de MBAM 2.0 Enterprise no se actualizan en la topología de MBAM 2.0 Standalone debido a errores de CreateCache de trabajo de SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Los informes de empresa de MBAM no se actualizan</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM equipos compatibles los informes de cumplimiento incluyen incorrectamente los productos no compatibles</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>El registro del equipo se ha rechazado en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Acerca de MBAM 2.0](about-mbam-20-mbam-2.md)

 

 





