---
title: Cómo mover las bases de datos de MBAM 2.5
description: Cómo mover las bases de datos de MBAM 2.5
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812399"
---
# <span data-ttu-id="60bbb-103">Cómo mover las bases de datos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="60bbb-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="60bbb-104">Use estos procedimientos para mover las siguientes bases de datos de un equipo a otro; del servidor a al servidor B, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="60bbb-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="60bbb-105">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="60bbb-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="60bbb-106">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="60bbb-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="60bbb-107">Es importante restaurar las bases de datos en la máquina B antes de ejecutar el Asistente para la configuración de MBAM para actualizarlas o configurarlas.</span><span class="sxs-lookup"><span data-stu-id="60bbb-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="60bbb-108">Si las bases de datos no están presentes, el Asistente para configuración crea bases de datos nuevas y vacías.</span><span class="sxs-lookup"><span data-stu-id="60bbb-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="60bbb-109">Cuando se restauren las bases de datos existentes, este proceso interrumpirá la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="60bbb-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="60bbb-110">Restaure primero las bases de datos y, a continuación, ejecute el Asistente para la configuración de MBAM, elija la opción de base de datos y el Asistente para la configuración se "conectará" a las bases de datos que haya restaurado. se actualizan si es necesario como parte del proceso.</span><span class="sxs-lookup"><span data-stu-id="60bbb-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="60bbb-111">Si va a mover varias características, muévala en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="60bbb-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="60bbb-112">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="60bbb-112">Recovery Database</span></span>

2.  <span data-ttu-id="60bbb-113">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="60bbb-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="60bbb-114">Informes</span><span class="sxs-lookup"><span data-stu-id="60bbb-114">Reports</span></span>

4.  <span data-ttu-id="60bbb-115">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="60bbb-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="60bbb-116">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="60bbb-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="60bbb-117">Para ejecutar los scripts de ejemplo de Windows PowerShell que se proporcionan en este tema, debe actualizar la Directiva de ejecución de Windows PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="60bbb-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="60bbb-118">Consulte [ejecución de scripts de Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="60bbb-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="60bbb-119">Mover la base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="60bbb-119">Move the Recovery Database</span></span>

<span data-ttu-id="60bbb-120">A continuación, se resumen los pasos para mover la base de datos de recuperación:</span><span class="sxs-lookup"><span data-stu-id="60bbb-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="60bbb-121">Detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="60bbb-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="60bbb-122">Hacer copia de seguridad de la base de datos de recuperación del servidor A</span><span class="sxs-lookup"><span data-stu-id="60bbb-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="60bbb-123">Mover la base de datos de recuperación desde el servidor a al servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="60bbb-124">Restaurar la base de datos de recuperación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="60bbb-125">Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión</span><span class="sxs-lookup"><span data-stu-id="60bbb-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="60bbb-126">Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="60bbb-127">Reanudar la instancia del sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="60bbb-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="60bbb-128">Cómo mover la base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="60bbb-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="60bbb-129">Detenga todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="60bbb-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="60bbb-130">En cada servidor que ejecute el sitio web del servidor de supervisión y administración de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="60bbb-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="60bbb-131">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="60bbb-132">Para ejecutar este comando, debe agregar el módulo servicios de Internet Information Server (IIS) para Windows PowerShell a la instancia actual de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60bbb-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="60bbb-133">Hacer copia de seguridad de la base de datos de recuperación del servidor A</span><span class="sxs-lookup"><span data-stu-id="60bbb-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="60bbb-134">Use la tarea de **copia de seguridad** en SQL Server Management Studio para realizar una copia de seguridad de la base de datos de recuperación del servidor a.  De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="60bbb-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="60bbb-135">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL y cambie la base de datos de recuperación de MBAM para que use el modo de recuperación completa:</span><span class="sxs-lookup"><span data-stu-id="60bbb-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

3.  <span data-ttu-id="60bbb-136">Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="60bbb-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="60bbb-137">**$Password $** -contraseña que usa para cifrar el archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="60bbb-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="60bbb-138">En Windows PowerShell, ejecute el script almacenado en el archivo y de forma similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="60bbb-139">Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="60bbb-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="60bbb-140">**$ServerName $ \ $SQLINSTANCENAME $** : nombre del servidor e instancia de la que se hará la copia de seguridad de la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="60bbb-141">Mover la base de datos de recuperación desde el servidor a al servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="60bbb-142">Use el explorador de Windows para mover el archivo data de la **base de datos de recuperación MBAM. bak** del servidor a al servidor B.</span><span class="sxs-lookup"><span data-stu-id="60bbb-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="60bbb-143">Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="60bbb-144">Use la información de la tabla siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="60bbb-145">Parámetro</span><span class="sxs-lookup"><span data-stu-id="60bbb-145">Parameter</span></span>**        | **<span data-ttu-id="60bbb-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="60bbb-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="60bbb-147">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="60bbb-147">$SERVERNAME$</span></span>       | <span data-ttu-id="60bbb-148">Nombre del servidor en el que se van a copiar los archivos.</span><span class="sxs-lookup"><span data-stu-id="60bbb-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="60bbb-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="60bbb-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="60bbb-150">Nombre del recurso compartido y la ruta de acceso en la que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="60bbb-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="60bbb-151">Restaurar la base de datos de recuperación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="60bbb-152">Restaure la base de datos de recuperación en el servidor B mediante la tarea **restaurar base de datos** de SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="60bbb-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="60bbb-153">Cuando finalice la tarea anterior, seleccione **desde el dispositivo**y, a continuación, seleccione el archivo de copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="60bbb-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="60bbb-154">Use el comando **Agregar** para seleccionar el archivo datos de la **base de datos de recuperación de MBAM** y haga clic en **Aceptar** para completar el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="60bbb-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="60bbb-155">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="60bbb-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

    FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

    WITH REPLACE
    ```

5.  <span data-ttu-id="60bbb-156">Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="60bbb-157">**$Password $** -contraseña que usó para cifrar el archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="60bbb-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="60bbb-158">En Windows PowerShell, ejecute el script almacenado en el archivo y de forma similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="60bbb-159">Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="60bbb-160">**$ServerName $ \ $SQLINSTANCENAME $** : nombre del servidor y instancia en el que se restaurará la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="60bbb-161">Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión</span><span class="sxs-lookup"><span data-stu-id="60bbb-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="60bbb-162">Compruebe que el inicio de sesión de usuario de Microsoft SQL Server que habilita el acceso a la base de datos restaurada se asigne a la cuenta de acceso que proporcionó durante el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="60bbb-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="60bbb-163">Si el inicio de sesión no es el mismo, cree un inicio de sesión con SQL Server Management Studio y asígnela al usuario de la base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="60bbb-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="60bbb-164">En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión de los sitios web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="60bbb-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="60bbb-165">Edite la siguiente clave de registro:</span><span class="sxs-lookup"><span data-stu-id="60bbb-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="60bbb-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="60bbb-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="60bbb-167">Actualice el valor del **origen de datos** con el nombre del servidor y de la instancia (por ejemplo, \ $ServerName \ $ \ \ \ $SQLINSTANCENAME) a la que se movió la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="60bbb-168">Actualice el valor del **catálogo inicial** con el nombre de la base de datos recuperada.</span><span class="sxs-lookup"><span data-stu-id="60bbb-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="60bbb-169">Para automatizar este proceso, puede usar el símbolo del sistema de Windows PowerShell para especificar una línea de comandos en el servidor de administración y supervisión que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   ><span data-ttu-id="60bbb-170">Todas las aplicaciones web locales MBAM comparten esta cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="60bbb-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="60bbb-171">Por lo tanto, debe actualizarse solo una vez por servidor.</span><span class="sxs-lookup"><span data-stu-id="60bbb-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="60bbb-172">Use la tabla siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="60bbb-173">Parámetro</span><span class="sxs-lookup"><span data-stu-id="60bbb-173">Parameter</span></span>|<span data-ttu-id="60bbb-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="60bbb-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="60bbb-175">$SERVERNAME $/\ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="60bbb-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="60bbb-176">Nombre del servidor y instancia de SQL Server donde se encuentra la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="60bbb-177">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="60bbb-177">$DATABASE$</span></span>|<span data-ttu-id="60bbb-178">Nombre de la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="60bbb-179">Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="60bbb-180">Instale el software de servidor MBAM 2,5 en el servidor B. Para obtener más información, consulte [Installing the MBAM 2,5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="60bbb-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="60bbb-181">En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica de **base de datos de recuperación** .</span><span class="sxs-lookup"><span data-stu-id="60bbb-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="60bbb-182">Para obtener más información sobre cómo configurar las bases de datos, consulte [Cómo configurar las bases de datos de MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="60bbb-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="60bbb-183">Como alternativa, puede usar el cmdlet **enable-MbamDatabase** de Windows PowerShell para configurar la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="60bbb-184">Reanudar la instancia del sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="60bbb-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="60bbb-185">En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="60bbb-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="60bbb-186">Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="60bbb-187">Para ejecutar este comando, debe agregar el módulo IIS para Windows PowerShell a la instancia actual de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60bbb-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="60bbb-188">Mover la base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="60bbb-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="60bbb-189">A continuación, se resumen los pasos para mover la base de datos de cumplimiento y auditoría:</span><span class="sxs-lookup"><span data-stu-id="60bbb-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="60bbb-190">Detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="60bbb-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="60bbb-191">Realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A</span><span class="sxs-lookup"><span data-stu-id="60bbb-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="60bbb-192">Mover la base de datos de cumplimiento y comprobación del servidor a al servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="60bbb-193">Restaurar la base de datos de cumplimiento y comprobación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="60bbb-194">Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión</span><span class="sxs-lookup"><span data-stu-id="60bbb-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="60bbb-195">Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="60bbb-196">Reanudar la instancia del sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="60bbb-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="60bbb-197">Cómo mover la base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="60bbb-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="60bbb-198">Detenga todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="60bbb-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="60bbb-199">En cada servidor que ejecute el sitio web del servidor de supervisión y administración de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="60bbb-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="60bbb-200">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="60bbb-201">Para ejecutar este comando, debe agregar el módulo servicios de Internet Information Server (IIS) para Windows PowerShell a la instancia actual de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60bbb-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="60bbb-202">Realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A</span><span class="sxs-lookup"><span data-stu-id="60bbb-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="60bbb-203">Use la tarea de **copia de seguridad** de SQL Server Management Studio para realizar una copia de seguridad de la base de datos de cumplimiento y auditoría en el servidor A. De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="60bbb-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="60bbb-204">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="60bbb-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  <span data-ttu-id="60bbb-205">Ejecute el script almacenado en el archivo. SQL con un comando de Windows PowerShell similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="60bbb-206">Con el siguiente valor, reemplace los valores en el ejemplo de código por valores que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="60bbb-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="60bbb-207">**$ServerName $ \ $SQLINSTANCENAME $** : nombre e instancia de servidor de la que se hará la copia de seguridad de la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="60bbb-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="60bbb-208">Mover la base de datos de cumplimiento y comprobación del servidor a al servidor B \* \*</span><span class="sxs-lookup"><span data-stu-id="60bbb-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="60bbb-209">Use el explorador de Windows para mover el archivo de la **base de datos de estado de cumplimiento de MBAM** en el servidor a al servidor B.</span><span class="sxs-lookup"><span data-stu-id="60bbb-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="60bbb-210">Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="60bbb-211">En la tabla siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="60bbb-212">Parámetro</span><span class="sxs-lookup"><span data-stu-id="60bbb-212">Parameter</span></span>**        | **<span data-ttu-id="60bbb-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="60bbb-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="60bbb-214">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="60bbb-214">$SERVERNAME$</span></span>       | <span data-ttu-id="60bbb-215">Nombre del servidor en el que se van a copiar los archivos.</span><span class="sxs-lookup"><span data-stu-id="60bbb-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="60bbb-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="60bbb-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="60bbb-217">Nombre del recurso compartido y la ruta de acceso en la que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="60bbb-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="60bbb-218">Restaurar la base de datos de cumplimiento y comprobación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="60bbb-219">Restaure la base de datos de comprobación y cumplimiento en el servidor B mediante la tarea **restaurar base de datos** de SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="60bbb-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="60bbb-220">Cuando finalice la tarea anterior, seleccione **desde el dispositivo**y, a continuación, seleccione el archivo de copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="60bbb-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="60bbb-221">Use el comando **Agregar** para seleccionar el archivo de **base de datos de estado de cumplimiento de MBAM** y haga clic en **Aceptar** para completar el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="60bbb-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="60bbb-222">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="60bbb-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="60bbb-223">En Windows PowerShell, ejecute el script almacenado en el archivo y de forma similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="60bbb-224">Con el valor siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="60bbb-225">**$ServerName $ \ $SQLINSTANCENAME $** : nombre del servidor y instancia en el que se restaurará la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="60bbb-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="60bbb-226">Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión</span><span class="sxs-lookup"><span data-stu-id="60bbb-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="60bbb-227">Compruebe que el inicio de sesión de usuario de Microsoft SQL Server que permite el acceso a la base de datos restaurada de cumplimiento y auditoría se asigna a la cuenta de acceso que proporcionó durante el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="60bbb-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="60bbb-228">Si el inicio de sesión no es el mismo, cree un inicio de sesión con SQL Server Management Studio y asígnela al usuario de la base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="60bbb-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="60bbb-229">En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="60bbb-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="60bbb-230">Edite la siguiente clave de registro:</span><span class="sxs-lookup"><span data-stu-id="60bbb-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="60bbb-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="60bbb-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="60bbb-232">Actualice el valor del **origen de datos** con el nombre del servidor y de la instancia (por ejemplo, \ $ServerName \ $ \ \ \ $SQLINSTANCENAME) a la que se movió la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="60bbb-233">Actualice el valor del **catálogo inicial** con el nombre de la base de datos recuperada.</span><span class="sxs-lookup"><span data-stu-id="60bbb-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="60bbb-234">Para automatizar este proceso, puede usar el símbolo del sistema de Windows PowerShell para especificar una línea de comandos en el servidor de administración y supervisión que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="60bbb-235">Todas las aplicaciones web locales MBAM comparten esta cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="60bbb-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="60bbb-236">Por lo tanto, debe actualizarse solo una vez por servidor.</span><span class="sxs-lookup"><span data-stu-id="60bbb-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="60bbb-237">En la tabla siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="60bbb-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="60bbb-238">Parámetro</span><span class="sxs-lookup"><span data-stu-id="60bbb-238">Parameter</span></span> | <span data-ttu-id="60bbb-239">Descripción</span><span class="sxs-lookup"><span data-stu-id="60bbb-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="60bbb-240">$SERVERNAME $ \ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="60bbb-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="60bbb-241">Nombre del servidor y instancia de SQL Server donde se encuentra la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="60bbb-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="60bbb-242">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="60bbb-242">$DATABASE$</span></span>|<span data-ttu-id="60bbb-243">Nombre de la base de datos recuperada.</span><span class="sxs-lookup"><span data-stu-id="60bbb-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="60bbb-244">Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="60bbb-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="60bbb-245">Instale el software de servidor MBAM 2,5 en el servidor B. Para obtener más información, consulte [Installing the MBAM 2,5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="60bbb-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="60bbb-246">En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica de **base de datos cumplimiento y auditoría** .</span><span class="sxs-lookup"><span data-stu-id="60bbb-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="60bbb-247">Para obtener más información sobre cómo configurar las bases de datos, consulte [Cómo configurar las bases de datos de MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="60bbb-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="60bbb-248">Como alternativa, puede usar el cmdlet **enable-MbamDatabase de** Windows PowerShell para configurar la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="60bbb-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="60bbb-249">Reanudar la instancia del sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="60bbb-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="60bbb-250">En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="60bbb-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="60bbb-251">Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="60bbb-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="60bbb-252">Para ejecutar este comando, debe agregar el módulo IIS para Windows PowerShell a la instancia actual de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60bbb-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
