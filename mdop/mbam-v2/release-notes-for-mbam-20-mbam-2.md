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
# <span data-ttu-id="5968a-103">Notas de la versión de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5968a-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="5968a-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="5968a-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="5968a-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLockerAdministration y Monitoring (MBAM) 2.0.</span><span class="sxs-lookup"><span data-stu-id="5968a-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="5968a-106">Estas notas de la versión contienen información que se necesita para instalar correctamente BitLockerAdministration y monitor 2.0 y contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="5968a-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="5968a-107">Si hay una diferencia entre estas notas de la versión y otra documentación de MBAM 2.0, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="5968a-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="5968a-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="5968a-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="5968a-109">Problemas conocidos de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5968a-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="5968a-110">Esta sección contiene notas de la versión para MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="5968a-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="5968a-111">El campo Nombre del equipo no puede aparecer en los informes de cumplimiento de los equipos con BitLocker y de la conformidad de BitLocker Enterprise al ejecutar MBAM con Microsoft System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="5968a-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="5968a-112">El campo Nombre del equipo puede estar en blanco en los informes de cumplimiento de los equipos con BitLocker y de la compatibilidad de la empresa de BitLocker al usar MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="5968a-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="5968a-113">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="5968a-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="5968a-114">El informe de cumplimiento empresarial no se actualiza después de actualizar la infraestructura de servidor de MBAM independiente</span><span class="sxs-lookup"><span data-stu-id="5968a-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="5968a-115">Si está usando la topología independiente MBAM y actualiza la infraestructura de servidor de la versión 1,0 a la 2,0, el informe de cumplimiento de la empresa no se actualizará.</span><span class="sxs-lookup"><span data-stu-id="5968a-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="5968a-116">SOLUCIÓN: después de la actualización, ejecute el siguiente script en la base de datos de cumplimiento y auditoría:</span><span class="sxs-lookup"><span data-stu-id="5968a-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

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

### <span data-ttu-id="5968a-117">Los informes del portal del servicio de asistencia muestran una advertencia si SSL no está configurado en SSRS</span><span class="sxs-lookup"><span data-stu-id="5968a-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="5968a-118">Si SQL Server Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de los informes se establecerá en HTTP en lugar de HTTPS cuando instale el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="5968a-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="5968a-119">Si, a continuación, busca el portal del servicio de asistencia y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro".</span><span class="sxs-lookup"><span data-stu-id="5968a-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="5968a-120">SOLUCIÓN alternativa: para mostrar el informe, haga clic en **Mostrar todo el contenido**.</span><span class="sxs-lookup"><span data-stu-id="5968a-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="5968a-121">Para solucionar este problema, vaya al equipo MBAM donde está instalado SQL Server Reporting Services, ejecute el **Administrador de configuración de Reporting Services**y, a continuación, haga clic en **URL de servicio Web**.</span><span class="sxs-lookup"><span data-stu-id="5968a-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="5968a-122">Seleccione el certificado SSL adecuado para el servidor, escriba el puerto SSL adecuado (el puerto predeterminado es 443) y, a continuación, haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="5968a-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="5968a-123">No se admiten instancias no predeterminadas de la base de datos de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5968a-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="5968a-124">MBAM busca solo la instancia predeterminada de la base de datos de Configuration Manager en Configuration Manager 2007 y SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="5968a-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="5968a-125">Si usa una instancia no predeterminada, no puede instalar MBAM.</span><span class="sxs-lookup"><span data-stu-id="5968a-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="5968a-126">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="5968a-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="5968a-127">Al hacer clic en "atrás" en el informe Resumen de cumplimiento, se puede producir un error</span><span class="sxs-lookup"><span data-stu-id="5968a-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="5968a-128">Si profundiza en un informe Resumen de cumplimiento y, a continuación, hace clic en el vínculo **atrás** en el informe de SSRS, se puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="5968a-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="5968a-129">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="5968a-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="5968a-130">El cifrado de espacio usado no funciona correctamente</span><span class="sxs-lookup"><span data-stu-id="5968a-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="5968a-131">Si cifra un equipo por primera vez después de instalar el cliente MBAM y ha establecido un objeto de directiva de grupo para implementar el cifrado solo de espacio usado, MBAM cifra de forma errónea todo el disco en lugar de cifrar solo el espacio usado por el disco.</span><span class="sxs-lookup"><span data-stu-id="5968a-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="5968a-132">Si un equipo ya está cifrado cuando instala el cliente MBAM y ha establecido el mismo objeto de directiva de grupo, el cifrado funciona correctamente y cifra solo el espacio de disco usado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5968a-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="5968a-133">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="5968a-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="5968a-134">La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="5968a-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="5968a-135">Si no establece una intensidad de cifrado específica en el objeto de directiva de grupo **elegir método de cifrado de unidad y intensidad** de cifrado, el informe de cumplimiento de equipos de la topología de integración del administrador de configuración siempre muestra "desconocido" para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="5968a-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="5968a-136">El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5968a-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="5968a-137">SOLUCIÓN alternativa: establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.</span><span class="sxs-lookup"><span data-stu-id="5968a-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="5968a-138">La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="5968a-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="5968a-139">Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.</span><span class="sxs-lookup"><span data-stu-id="5968a-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="5968a-140">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="5968a-140">WORKAROUND: None.</span></span> <span data-ttu-id="5968a-141">No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="5968a-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="5968a-142">La configuración de seguridad mejorada puede provocar que los informes no se muestren correctamente</span><span class="sxs-lookup"><span data-stu-id="5968a-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="5968a-143">Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca el mensaje "acceso denegado" cuando intente ver informes en el servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="5968a-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="5968a-144">De forma predeterminada, ESC se activa para proteger el servidor disminuyendo la exposición del servidor ante posibles ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5968a-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="5968a-145">SOLUCIÓN: Si el mensaje "acceso denegado" aparece al intentar ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada.</span><span class="sxs-lookup"><span data-stu-id="5968a-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="5968a-146">También puede ver los informes desde otro equipo en el que la ESC no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="5968a-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="5968a-147">Se produce un error en la instalación de MBAM Server al actualizar de SQL Server 2008 a SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="5968a-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="5968a-148">Si actualiza SQL Server 2008 a SQL Server 2012 e intenta instalar la base de datos de cumplimiento y auditoría o la base de datos de recuperación, se produce un error en la instalación y se deshace.</span><span class="sxs-lookup"><span data-stu-id="5968a-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="5968a-149">El error se produce porque el archivo de SQLCMD.exe necesario se quitó durante la actualización de SQL y el instalador de MBAM no lo puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="5968a-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="5968a-150">Las líneas del archivo de registro MSI pueden tener un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="5968a-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="5968a-151">RunDbInstallScript de BD de recuperación de RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exede BD dB de recuperación: dbInstance-xxxxxx\\I01RunDbInstallScript de BD Recovery: sqlScript-C:\\Archivos de Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript de BD de recuperación: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript defaultFileName-MBAM _Recovery \ I01\\MSSQL\\DATA\\RunDbInstallScript de BD de recuperación de certificados: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperación de la BD CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de BD Recovery dB: comenzando a ejecutar el complemento de base de datos de recuperación scriptRunDbInstallScript recuperación de BD de BD: el archivo de registro SQLCMD se encuentra en C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript de BD de recuperación excepción: instalar la acción personalizada de la base de datos de recuperación excepción: el sistema no puede encontrar el archivo especificado</span><span class="sxs-lookup"><span data-stu-id="5968a-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="5968a-152">El Windows Installer de MBAM Server está codificado para encontrar la ruta de acceso SQLCMD.exe en el valor de la cadena de ruta de acceso en el registro en HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="5968a-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="5968a-153">La clave sigue presente durante la migración de SQL Server 2008 a SQL Server 2012, pero la ruta de acceso a la que hace referencia el valor de los datos no contiene el archivo de SQLCMD.exe, porque el proceso de actualización de SQL ha eliminado el archivo.</span><span class="sxs-lookup"><span data-stu-id="5968a-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="5968a-154">SOLUCIÓN alternativa: Cambie temporalmente el valor de la cadena de ruta de acceso HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup a **path \ _old**y vuelva a ejecutar el Windows Installer del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="5968a-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="5968a-155">Cuando la instalación se complete correctamente y cree las bases de datos en SQL Server 2012, cambie el nombre de la **ruta de acceso \ _old** valor a **path**.</span><span class="sxs-lookup"><span data-stu-id="5968a-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="5968a-156">Revisiones y artículos de Knowledge base para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5968a-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="5968a-157">Esta sección contiene revisiones y artículos de KB para MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="5968a-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="5968a-158">Artículo de KB</span><span class="sxs-lookup"><span data-stu-id="5968a-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="5968a-159">Title</span><span class="sxs-lookup"><span data-stu-id="5968a-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="5968a-160">Link</span><span class="sxs-lookup"><span data-stu-id="5968a-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-161">2831166</span><span class="sxs-lookup"><span data-stu-id="5968a-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-162">Instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falla con los &quot; objetos de System Center cm ya instalados&quot;</span><span class="sxs-lookup"><span data-stu-id="5968a-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="5968a-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-164">2870849</span><span class="sxs-lookup"><span data-stu-id="5968a-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-165">Los usuarios no pueden recuperar la clave de recuperación de BitLocker con el portal de autoservicio de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5968a-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="5968a-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-167">2756402</span><span class="sxs-lookup"><span data-stu-id="5968a-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-168">El cliente de MBAM no funcionaba con el identificador de evento 4 y el código de error 0x8004100E en la descripción del evento</span><span class="sxs-lookup"><span data-stu-id="5968a-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="5968a-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-170">2620287</span><span class="sxs-lookup"><span data-stu-id="5968a-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-171">Mensaje de error "error de servidor en '/Reports ' aplicación" al hacer clic en la pestaña informes en MBAM</span><span class="sxs-lookup"><span data-stu-id="5968a-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="5968a-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-173">2639518</span><span class="sxs-lookup"><span data-stu-id="5968a-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-174">Error al abrir informes de cumplimiento de los equipos o de la empresa en MBAM</span><span class="sxs-lookup"><span data-stu-id="5968a-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="5968a-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-176">2620269</span><span class="sxs-lookup"><span data-stu-id="5968a-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-177">Los informes de empresa de MBAM no se actualizan</span><span class="sxs-lookup"><span data-stu-id="5968a-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="5968a-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-179">2712461</span><span class="sxs-lookup"><span data-stu-id="5968a-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-180">No se admite la instalación de MBAM en un controlador de dominio</span><span class="sxs-lookup"><span data-stu-id="5968a-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="5968a-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-182">2876732</span><span class="sxs-lookup"><span data-stu-id="5968a-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-183">Recibe el código de error 0x80071a90 durante la instalación independiente o de integración del administrador de configuración de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5968a-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="5968a-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-185">2754259</span><span class="sxs-lookup"><span data-stu-id="5968a-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-186">MBAM y comunicaciones seguras de red</span><span class="sxs-lookup"><span data-stu-id="5968a-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="5968a-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-188">2870842</span><span class="sxs-lookup"><span data-stu-id="5968a-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-189">El programa de instalación de MBAM 2.0 falla durante el escenario de integración de Configuration Manager con SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="5968a-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="5968a-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-191">2668533</span><span class="sxs-lookup"><span data-stu-id="5968a-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-192">Se produce un error en la instalación de MBAM si SQL SSRS no se ha configurado correctamente</span><span class="sxs-lookup"><span data-stu-id="5968a-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="5968a-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-194">2870847</span><span class="sxs-lookup"><span data-stu-id="5968a-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-195">La instalación de MBAM 2,0 produce un &quot; error al recuperar la configuración del rol de servidor de Configuration Manager para &#39;rol de&#39; de punto de servicios de informes&quot;</span><span class="sxs-lookup"><span data-stu-id="5968a-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="5968a-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-197">2870839</span><span class="sxs-lookup"><span data-stu-id="5968a-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-198">Los informes de MBAM 2.0 Enterprise no se actualizan en la topología de MBAM 2.0 Standalone debido a errores de CreateCache de trabajo de SQL</span><span class="sxs-lookup"><span data-stu-id="5968a-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="5968a-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-200">2620269</span><span class="sxs-lookup"><span data-stu-id="5968a-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-201">Los informes de empresa de MBAM no se actualizan</span><span class="sxs-lookup"><span data-stu-id="5968a-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="5968a-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5968a-203">2935997</span><span class="sxs-lookup"><span data-stu-id="5968a-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-204">MBAM equipos compatibles los informes de cumplimiento incluyen incorrectamente los productos no compatibles</span><span class="sxs-lookup"><span data-stu-id="5968a-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="5968a-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5968a-206">2612822</span><span class="sxs-lookup"><span data-stu-id="5968a-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="5968a-207">El registro del equipo se ha rechazado en MBAM</span><span class="sxs-lookup"><span data-stu-id="5968a-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="5968a-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="5968a-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5968a-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5968a-209">Related topics</span></span>


[<span data-ttu-id="5968a-210">Acerca de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5968a-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 





