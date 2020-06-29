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
# Cómo mover las bases de datos de MBAM 2.5

Use estos procedimientos para mover las siguientes bases de datos de un equipo a otro; del servidor a al servidor B, por ejemplo:

-   Base de datos de cumplimiento y auditoría

-   Base de datos de recuperación

>[!NOTE]
>Es importante restaurar las bases de datos en la máquina B antes de ejecutar el Asistente para la configuración de MBAM para actualizarlas o configurarlas.

Si las bases de datos no están presentes, el Asistente para configuración crea bases de datos nuevas y vacías. Cuando se restauren las bases de datos existentes, este proceso interrumpirá la configuración de MBAM.

Restaure primero las bases de datos y, a continuación, ejecute el Asistente para la configuración de MBAM, elija la opción de base de datos y el Asistente para la configuración se "conectará" a las bases de datos que haya restaurado. se actualizan si es necesario como parte del proceso.

**Si va a mover varias características, muévala en el siguiente orden:**

1.  Base de datos de recuperación

2.  Base de datos de cumplimiento y auditoría

3.  Informes

4.  Sitio web de administración y supervisión

5.  Portal de autoservicio

>[!Note]
>Para ejecutar los scripts de ejemplo de Windows PowerShell que se proporcionan en este tema, debe actualizar la Directiva de ejecución de Windows PowerShell para habilitar la ejecución de scripts. Consulte [ejecución de scripts de Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obtener instrucciones.

## Mover la base de datos de recuperación

A continuación, se resumen los pasos para mover la base de datos de recuperación:

1.  Detener todas las instancias del sitio web de supervisión y administración de MBAM

2.  Hacer copia de seguridad de la base de datos de recuperación del servidor A

3.  Mover la base de datos de recuperación desde el servidor a al servidor B

4.  Restaurar la base de datos de recuperación en el servidor B

5.  Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión

6.  Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B

7.  Reanudar la instancia del sitio web de administración y supervisión

### Cómo mover la base de datos de recuperación

**Detenga todas las instancias del sitio web de supervisión y administración de MBAM.** En cada servidor que ejecute el sitio web del servidor de supervisión y administración de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de administración y supervisión.

Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para ejecutar este comando, debe agregar el módulo servicios de Internet Information Server (IIS) para Windows PowerShell a la instancia actual de Windows PowerShell.

### Hacer copia de seguridad de la base de datos de recuperación del servidor A

1.  Use la tarea de **copia de seguridad** en SQL Server Management Studio para realizar una copia de seguridad de la base de datos de recuperación del servidor a.  De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de recuperación**.

2.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL y cambie la base de datos de recuperación de MBAM para que use el modo de recuperación completa:

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

3.  Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno:

    **$Password $** -contraseña que usa para cifrar el archivo de clave privada.

4.  En Windows PowerShell, ejecute el script almacenado en el archivo y de forma similar a la siguiente:

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno:

    **$ServerName $ \ $SQLINSTANCENAME $** : nombre del servidor e instancia de la que se hará la copia de seguridad de la base de datos de recuperación.

### Mover la base de datos de recuperación desde el servidor a al servidor B

Use el explorador de Windows para mover el archivo data de la **base de datos de recuperación MBAM. bak** del servidor a al servidor B.

Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
Use la información de la tabla siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.

| **Parámetro**        | **Descripción**  |
|----------------------|------------------|
| $SERVERNAME $       | Nombre del servidor en el que se van a copiar los archivos. |
| $DESTINATIONSHARE $ | Nombre del recurso compartido y la ruta de acceso en la que se copiarán los archivos. |


### Restaurar la base de datos de recuperación en el servidor B

1.  Restaure la base de datos de recuperación en el servidor B mediante la tarea **restaurar base de datos** de SQL Server Management Studio.

2.  Cuando finalice la tarea anterior, seleccione **desde el dispositivo**y, a continuación, seleccione el archivo de copia de seguridad de la base de datos.

3.  Use el comando **Agregar** para seleccionar el archivo datos de la **base de datos de recuperación de MBAM** y haga clic en **Aceptar** para completar el proceso de restauración.

4.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

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

5.  Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.

    **$Password $** -contraseña que usó para cifrar el archivo de clave privada.

6.  En Windows PowerShell, ejecute el script almacenado en el archivo y de forma similar a la siguiente:

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  Use el valor siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.

    **$ServerName $ \ $SQLINSTANCENAME $** : nombre del servidor y instancia en el que se restaurará la base de datos de recuperación.

### Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión

1. Compruebe que el inicio de sesión de usuario de Microsoft SQL Server que habilita el acceso a la base de datos restaurada se asigne a la cuenta de acceso que proporcionó durante el proceso de configuración.

   >[!NOTE]
   >Si el inicio de sesión no es el mismo, cree un inicio de sesión con SQL Server Management Studio y asígnela al usuario de la base de datos existente.

2. En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión de los sitios web de MBAM.

3. Edite la siguiente clave de registro:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. Actualice el valor del **origen de datos** con el nombre del servidor y de la instancia (por ejemplo, \ $ServerName \ $ \ \ \ $SQLINSTANCENAME) a la que se movió la base de datos de recuperación.

5. Actualice el valor del **catálogo inicial** con el nombre de la base de datos recuperada.

6. Para automatizar este proceso, puede usar el símbolo del sistema de Windows PowerShell para especificar una línea de comandos en el servidor de administración y supervisión que es similar a la siguiente:

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
   >Todas las aplicaciones web locales MBAM comparten esta cadena de conexión. Por lo tanto, debe actualizarse solo una vez por servidor.


7. Use la tabla siguiente para reemplazar los valores en el ejemplo de código por valores que coincidan con su entorno.

   |Parámetro|Descripción|
   |---------|-----------|
   |$SERVERNAME $/\ $SQLINSTANCENAME $|Nombre del servidor y instancia de SQL Server donde se encuentra la base de datos de recuperación.|
   |$DATABASE $|Nombre de la base de datos de recuperación.|


### Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B

1.  Instale el software de servidor MBAM 2,5 en el servidor B. Para obtener más información, consulte [Installing the MBAM 2,5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica de **base de datos de recuperación** . Para obtener más información sobre cómo configurar las bases de datos, consulte [Cómo configurar las bases de datos de MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Como alternativa, puede usar el cmdlet **enable-MbamDatabase** de Windows PowerShell para configurar la base de datos de recuperación.


### Reanudar la instancia del sitio web de administración y supervisión

En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de administración y supervisión.

Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para ejecutar este comando, debe agregar el módulo IIS para Windows PowerShell a la instancia actual de Windows PowerShell.

## Mover la base de datos de cumplimiento y auditoría

A continuación, se resumen los pasos para mover la base de datos de cumplimiento y auditoría:

1.  Detener todas las instancias del sitio web de supervisión y administración de MBAM

2.  Realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A

3.  Mover la base de datos de cumplimiento y comprobación del servidor a al servidor B

4.  Restaurar la base de datos de cumplimiento y comprobación en el servidor B

5.  Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión

6.  Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B

7.  Reanudar la instancia del sitio web de administración y supervisión

### Cómo mover la base de datos de cumplimiento y auditoría

**Detenga todas las instancias del sitio web de supervisión y administración de MBAM.**  En cada servidor que ejecute el sitio web del servidor de supervisión y administración de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de administración y supervisión.

Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para ejecutar este comando, debe agregar el módulo servicios de Internet Information Server (IIS) para Windows PowerShell a la instancia actual de Windows PowerShell.

### Realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A

1.  Use la tarea de **copia de seguridad** de SQL Server Management Studio para realizar una copia de seguridad de la base de datos de cumplimiento y auditoría en el servidor A. De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de estado de cumplimiento**.

2.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

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

3.  Ejecute el script almacenado en el archivo. SQL con un comando de Windows PowerShell similar al siguiente:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  Con el siguiente valor, reemplace los valores en el ejemplo de código por valores que coincidan con su entorno:

    **$ServerName $ \ $SQLINSTANCENAME $** : nombre e instancia de servidor de la que se hará la copia de seguridad de la base de datos de cumplimiento y auditoría.

### Mover la base de datos de cumplimiento y comprobación del servidor a al servidor B * *

1.  Use el explorador de Windows para mover el archivo de la **base de datos de estado de cumplimiento de MBAM** en el servidor a al servidor B.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  En la tabla siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.

    | **Parámetro**        | **Descripción**                                               |
    |----------------------|---------------------------------------------------------------|
    | $SERVERNAME $       | Nombre del servidor en el que se van a copiar los archivos.         |
    | $DESTINATIONSHARE $ | Nombre del recurso compartido y la ruta de acceso en la que se copiarán los archivos. |


### Restaurar la base de datos de cumplimiento y comprobación en el servidor B

1.  Restaure la base de datos de comprobación y cumplimiento en el servidor B mediante la tarea **restaurar base de datos** de SQL Server Management Studio.

2.  Cuando finalice la tarea anterior, seleccione **desde el dispositivo**y, a continuación, seleccione el archivo de copia de seguridad de la base de datos.

3.  Use el comando **Agregar** para seleccionar el archivo de **base de datos de estado de cumplimiento de MBAM** y haga clic en **Aceptar** para completar el proceso de restauración.

4.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  En Windows PowerShell, ejecute el script almacenado en el archivo y de forma similar a la siguiente:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  Con el valor siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.

    **$ServerName $ \ $SQLINSTANCENAME $** : nombre del servidor y instancia en el que se restaurará la base de datos de cumplimiento y auditoría.

### Configurar el acceso a la base de datos en el servidor B y actualizar los datos de conexión

1. Compruebe que el inicio de sesión de usuario de Microsoft SQL Server que permite el acceso a la base de datos restaurada de cumplimiento y auditoría se asigna a la cuenta de acceso que proporcionó durante el proceso de configuración.

   >[!NOTE]
   >Si el inicio de sesión no es el mismo, cree un inicio de sesión con SQL Server Management Studio y asígnela al usuario de la base de datos existente.

2. En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para el sitio Web.

3. Edite la siguiente clave de registro:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. Actualice el valor del **origen de datos** con el nombre del servidor y de la instancia (por ejemplo, \ $ServerName \ $ \ \ \ $SQLINSTANCENAME) a la que se movió la base de datos de recuperación.

5. Actualice el valor del **catálogo inicial** con el nombre de la base de datos recuperada.

6. Para automatizar este proceso, puede usar el símbolo del sistema de Windows PowerShell para especificar una línea de comandos en el servidor de administración y supervisión que es similar a la siguiente:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >Todas las aplicaciones web locales MBAM comparten esta cadena de conexión. Por lo tanto, debe actualizarse solo una vez por servidor.


7. En la tabla siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.

   |Parámetro | Descripción |
   |---------|------------|
   |$SERVERNAME $ \ $SQLINSTANCENAME $ | Nombre del servidor y instancia de SQL Server donde se encuentra la base de datos de recuperación.|
   |$DATABASE $|Nombre de la base de datos recuperada.|

### Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B

1.  Instale el software de servidor MBAM 2,5 en el servidor B. Para obtener más información, consulte [Installing the MBAM 2,5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica de **base de datos cumplimiento y auditoría** . Para obtener más información sobre cómo configurar las bases de datos, consulte [Cómo configurar las bases de datos de MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Como alternativa, puede usar el cmdlet **enable-MbamDatabase de** Windows PowerShell para configurar la base de datos de cumplimiento y auditoría.


### Reanudar la instancia del sitio web de administración y supervisión

En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de administración y supervisión.

Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Para ejecutar este comando, debe agregar el módulo IIS para Windows PowerShell a la instancia actual de Windows PowerShell.
