---
title: Cómo mover funciones de MBAM 2.0 a otro equipo
description: Cómo mover funciones de MBAM 2.0 a otro equipo
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825080"
---
# Cómo mover funciones de MBAM 2.0 a otro equipo


En este tema se describen los pasos que debe seguir para mover una o más características de administración y supervisión de Microsoft BitLocker (MBAM) a un equipo diferente. Al mover más de una característica de administración y administración de Microsoft BitLocker, debe moverlas en el siguiente orden:

1.  Base de datos de recuperación

2.  Base de datos de cumplimiento y auditoría

3.  Informes de cumplimiento y cumplimiento

4.  Administración y supervisión

## Mover la base de datos de recuperación


Para mover la base de datos de recuperación de un equipo a otro (por ejemplo, del servidor a al servidor B), use el procedimiento siguiente.

1.  Detenga todas las instancias del sitio web de administración y supervisión.

2.  Ejecute el programa de instalación de MBAM en el servidor B.

3.  Haga una copia de seguridad de la base de datos de recuperación de MBAM en el servidor A.

4.  Mueva la base de datos de recuperación de MBAM desde el servidor a a B.

5.  Restaure la base de datos de recuperación de MBAM en el servidor B.

6.  Configure el acceso a la base de datos de recuperación de MBAM en el servidor B.

7.  Actualice los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM.

8.  Resume todas las instancias del sitio web de supervisión y administración de MBAM.

**Detener todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM, que se denomina **Administración de Microsoft BitLocker y supervisión**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar la línea de comandos que es similar a la siguiente:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Para ejecutar esta línea de comandos de PowerShell, el módulo IIS para PowerShell debe agregarse a la instancia actual de PowerShell. Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.



**Ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la **base de datos de recuperación** para la instalación.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar la línea de comandos que es similar a la siguiente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia a la que se moverá la base de datos de recuperación.

    -   $DOMAIN $ \ \ $SERVERNAME $: escriba los nombres de dominio y servidor de cada MBAM de administración y supervisión que se pondrá en contacto con la base de datos de recuperación. Use punto y coma para separar cada pareja de dominio y servidor de la lista (por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $). Cada nombre de servidor debe ir seguido de un símbolo "$", como se muestra en el ejemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.



**Hacer copia de seguridad de la base de datos de recuperación del servidor A**

1.  Para hacer una copia de seguridad de la base de datos de recuperación en el servidor A, use SQL Server Management Studio y la tarea llamada copia de seguridad. De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de recuperación**.

2.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    Modifique la base de datos de recuperación de MBAM para usar el modo de recuperación completa.

    ```sql
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

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $PASSWORD $: escriba una contraseña que usará para cifrar el archivo de clave privada.



3.  Ejecute el archivo SQL mediante SQL Server PowerShell y una línea de comandos similar a la siguiente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia desde donde se hará la copia de seguridad de la base de datos de recuperación.



**Mover la base de datos y el certificado de recuperación desde el servidor a al servidor B**

1.  Mueva el archivo siguiente del servidor a al servidor B con el explorador de Windows.

    -   MBAM de base de datos de recuperación. bak

2.  Para mover el certificado de la base de datos cifrada, use los siguientes pasos de automatización. Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.

    -   $DESTINATIONSHARE $: escriba el nombre del uso compartido y la ruta de acceso en la que se copiarán los archivos.



**Restaurar la base de datos de recuperación en el servidor B**

1.  Restaure la base de datos de recuperación en el servidor B con SQL Server Management Studio y la tarea denominada **restore database**.

2.  Una vez completada la tarea, seleccione el archivo de copia de seguridad de la base de datos seleccionando la opción **de dispositivo** y, a continuación, use el comando **Agregar** para seleccionar el archivo datos de la base de datos de recuperación de MBAM **. bak** .

3.  Seleccione **Aceptar** para completar el proceso de restauración.

4.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

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

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $PASSWORD $: escriba una contraseña que usó para cifrar el archivo de clave privada.



5.  Puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia en la que se restaurará la base de datos de recuperación.



**Configurar el acceso a la base de datos de recuperación en el servidor B**

1.  En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM Recovery and hardware dB Access**.

2.  Verifique que el inicio de sesión de SQL **MBAM recuperación y el acceso a la BD de hardware** en la base de datos restaurada se asigne al nombre de inicio de sesión **$MachineName $ \\MBAM de acceso de la BD de hardware y recuperación**. Si no está asignado tal como se describe, cree otro inicio de sesión con pertenencias a grupos similares, y asígnela al nombre de inicio de sesión **$MachineName $ \\MBAM de la recuperación y el acceso a la BD de hardware**.

3.  Para automatizar este procedimiento, puede usar Windows PowerShell en el servidor B para especificar una línea de comandos similar a la siguiente:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los valores aplicables para su entorno:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM. El nombre del servidor debe ir seguido de un $, como se muestra en el ejemplo (por ejemplo, MyDomain\\MyServerName1 $).



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Actualizar los datos de conexión de la base de datos de recuperación en los servidores de supervisión y administración de MBAM**

1. En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de administración y supervisión:

   -   MBAMAdministrationService

   -   MBAMRecoveryAndHardwareService

2. Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.

3. Seleccione la opción **configurationStrings** en el control de **lista de secciones** .

4. Seleccione la fila denominada **(colección)** y abra el **Editor** de la colección seleccionando el botón situado en el lado derecho de la fila.

5. En el **Editor de colecciones**, seleccione la fila denominada **KeyRecoveryConnectionString** al actualizar la configuración de la aplicación MBAMAdministrationService o la fila denominada <strong> Microsoft. Mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString al actualizar la configuración de la MBAMRecoveryAndHardwareService.

6. Actualice el **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y la instancia (por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $) donde se movió la base de datos de recuperación.

7. Para automatizar este procedimiento, puede usar Windows para escribir una línea de comandos, que es similar a la siguiente, en cada servidor de administración y supervisión:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Nota**  
   Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación.



**Reanudar todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM, que se denomina **Administración de BitLocker de Microsoft y supervisión**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos similar a la siguiente:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Mover la característica de base de datos de cumplimiento y auditoría


Si desea mover la base de datos de auditoría y cumplimiento de MBAM de un equipo a otro (es decir, mover la base de datos del servidor a al servidor B), use el procedimiento siguiente. El proceso incluye los siguientes pasos de alto nivel:

1.  Detenga todas las instancias del sitio web de administración y supervisión.

2.  Ejecute el programa de instalación de MBAM en el servidor B.

3.  Haga una copia de seguridad de la base de datos en el servidor A.

4.  Mueva la base de datos del servidor a a B.

5.  Restaure la base de datos en el servidor B.

6.  Configure el acceso a la base de datos en el servidor B.

7.  Actualice los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM.

8.  Actualice la cadena de conexión del origen de datos SSRS Reports con la nueva ubicación de la base de datos de cumplimiento y auditoría.

9.  Reanude todas las instancias del sitio web de administración y supervisión.

**Detener todas las instancias del sitio web de supervisión y supervisión**

1.  En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Para ejecutar esta línea de comandos, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell. Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.



**Ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la **base de datos de cumplimiento y auditoría** para la instalación.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **Nota**  
    Nota: Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia a la que se moverá la base de datos de cumplimiento y de auditoría.

    -   $DOMAIN $ \ \ $SERVERNAME $-escriba los nombres de dominio y servidor de cada MBAM de administración y supervisión que se comunicarán con la base de datos de cumplimiento y auditoría. Use un punto y coma para separar cada pareja de dominio y servidor de la lista (por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $). Cada nombre de servidor debe ir seguido de un símbolo "$", como se muestra en el ejemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $DOMAIN $ \ \ $USERNAME $-escriba el nombre de usuario y de dominio que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de cumplimiento y auditoría.

    -   $X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.



**Realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A**

1.  Para realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A, use SQL Server Management Studio y la tarea llamada **copia de seguridad**. De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de estado de cumplimiento**.

2.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

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

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Ejecute el archivo SQL con una línea de comandos de Windows PowerShell similar a la siguiente:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia donde se realizará una copia de seguridad de la base de datos de cumplimiento y auditoría.



**Mover la base de datos de cumplimiento y comprobación del servidor a a B**

1.  Mueva los siguientes archivos del servidor a al servidor B con el explorador de Windows.

    -   Base de datos de estado de cumplimiento de MBAM Data. bak

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.

    -   $DESTINATIONSHARE $: escriba el nombre del recurso compartido y la ruta en la que se copiarán los archivos.



**Restaurar la base de datos de cumplimiento y comprobación en el servidor B**

1.  Restaure la base de datos de comprobación y cumplimiento en el servidor B con SQL Server Management Studio y la tarea denominada **restore database**.

2.  Una vez completada la tarea, seleccione el archivo de copia de seguridad de la base de datos seleccionando la opción **de dispositivo** y, a continuación, use el comando **Agregar** para seleccionar el archivo de base de datos de estado de cumplimiento MBAM. bak. Seleccione **Aceptar** para completar el proceso de restauración.

3.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Ejecute el archivo SQL con una línea de comandos de Windows PowerShell similar a la siguiente:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia donde se restaurará la base de datos de cumplimiento y auditoría.



**Configurar el acceso a la base de datos de cumplimiento y comprobación en el servidor B**

1.  En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM acceso a la base de cumplimiento del estado de cumplimiento**.

2.  Compruebe que el inicio de sesión de **MBAM auditoría de cumplimiento de BD Access** en la base de datos restaurada se asigne al nombre de inicio de sesión **$MachineName $ \ \ MBAM acceso a las bases**de datos de auditoría de cumplimiento. Si no está asignado tal como se describe, cree otro inicio de sesión con pertenencias a grupos similares, y asígnela al nombre de inicio de sesión **$MachineName $ \ \ MBAM acceso a las bases de verificación de auditoría de cumplimiento**.

3.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos en el servidor B que es similar a la siguiente:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los valores aplicables para su entorno:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM. El nombre del servidor debe ir seguido de un "$", tal y como se muestra en el ejemplo. (por ejemplo, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Actualizar los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM**

1.  En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de administración y supervisión:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.

3.  Seleccione la opción **configurationStrings** en el control de **lista de secciones** .

4.  Seleccione la fila con el nombre **(colección)** y abra el editor de la **colección** seleccionando el botón situado en el lado derecho de la fila.

5.  En el **Editor de colecciones**, seleccione la fila denominada **ComplianceStatusConnectionString** al actualizar la configuración de la aplicación MBAMAdministrationService, o la fila denominada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** al actualizar la configuración de la MBAMComplianceStatusService.

6.  Actualice el valor del **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y de la instancia (por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME) al que se movió la base de datos de recuperación.

7.  Para automatizar este procedimiento, puede usar Windows para especificar una línea de comandos en cada servidor de administración y supervisión que es similar a la siguiente:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación.



**Reanudar todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Mover los informes de cumplimiento y de auditoría


Si quiere mover los informes de auditoría y cumplimiento normativo de MBAM de un equipo a otro (es decir, mover los informes del servidor a al servidor B), use el procedimiento siguiente, que incluye los siguientes pasos de alto nivel:

1.  Ejecute el programa de instalación de MBAM en el servidor B.

2.  Configure el acceso a los informes de auditoría y cumplimiento en el servidor B.

3.  Detenga todas las instancias del sitio web de supervisión y administración de MBAM.

4.  Actualice los datos de conexión de los informes en los servidores de supervisión y administración de MBAM.

5.  Resume todas las instancias del sitio web de supervisión y administración de MBAM.

**Ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la característica **informes de cumplimiento y de auditoría** para la instalación.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia donde se encuentra la base de datos de cumplimiento y auditoría.

    -   $DOMAIN $ \ \ $USERNAME $-escriba el nombre de usuario y de dominio que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de cumplimiento y auditoría.

    -   $PASSWORD $: escriba la contraseña de la cuenta de usuario que se usará para conectarse a la base de datos de cumplimiento y de auditoría.

    -   $X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.



**Configurar el acceso a los informes de cumplimiento y de auditoría en el servidor B**

1.  En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de usuario que tendrán acceso a los informes de cumplimiento y cumplimiento. Agregue las cuentas de usuario al grupo local denominado MBAM Report users.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos en el servidor B que es similar a la siguiente:

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los valores aplicables para su entorno:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Detener todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada servidor que ejecute la característica servidor de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Actualizar los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM**

1. En cada servidor que ejecute la característica servidor de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la dirección URL de informes de cumplimiento y de cumplimiento.

2. Seleccione el sitio web de **Administración y administración de Microsoft BitLocker** y use la característica **Editor de configuración** que se encuentra en la sección **Administración** de la **vista de características**.

3. Seleccione la opción **appSettings** en el control de **lista de secciones** .

4. Seleccione la fila denominada **(colección)** y abra el **Editor** de la colección seleccionando el botón situado en el lado derecho de la fila.

5. En el **Editor de colecciones**, seleccione la fila denominada **Microsoft. Mbam. Reports. URL**.

6. Actualice el valor de **Microsoft. Mbam. Reports. URL** para reflejar el nombre del servidor para el servidor B. Si la característica informes de cumplimiento y comprobación se ha instalado en una instancia de SQL Reporting Services con nombre, asegúrese de agregar o actualizar el nombre de la instancia a la dirección URL (por ejemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....)

7. Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos en cada servidor de administración y supervisión que sea similar a la siguiente:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **Nota**  
   Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

   -   $SERVERNAME $: escriba el nombre del servidor al que se instalaron los informes de cumplimiento y comprobación.

   -   $SRSINSTANCENAME $: escriba el nombre de la instancia de SQL Reporting Services en la que se instalaron los informes de cumplimiento y comprobación.



**Reanudar todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada servidor que ejecute la característica servidor de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Para ejecutar esta línea de comandos, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell. Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.



## Desplazamiento de la característica de administración y supervisión


Si desea mover la característica de informes de administración y supervisión de MBAM de un equipo a otro (es decir, mover la característica del servidor a al servidor B), use el procedimiento siguiente, que incluye los siguientes pasos de alto nivel:

1.  Ejecute el programa de instalación de MBAM en el servidor B.

2.  Configure el acceso a la base de datos en el servidor B.

**Ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la característica **servidor de administración y supervisión** para la instalación.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-para el parámetro COMPLIDB \ _SQLINSTANCE, escriba el nombre del servidor y la instancia donde se encuentra la base de datos de cumplimiento y auditoría. Para el parámetro RECOVERYANDHWDB \ _SQLINSTANCE, escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación.

    -   $DOMAIN $ \ \ $USERNAME $-escriba el nombre de usuario y de dominio que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de cumplimiento y auditoría.

    -   $ REPORTSSERVERURL $: escriba la dirección URL de la ubicación particular del sitio web de SQL Reporting Services. Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer". Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".

    -   $X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.



**Configurar el acceso a las bases de datos**

1.  En el servidor o servidores donde está implementada la base de datos de recuperación y la base de datos de cumplimiento y auditoría, use el complemento de grupo y usuario local en el administrador de servidores para agregar las cuentas de equipo de cada servidor que ejecuta la característica servidor de administración y supervisión de MBAM en los grupos locales denominados acceso de base de datos de recuperación **y hardware** **, servidor de BD**

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos, que es similar a la siguiente, en el servidor donde se implementó la base de datos de cumplimiento y auditoría.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  En el servidor en el que se implementó la base de datos de recuperación, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Reemplace el siguiente valor del ejemplo anterior por los valores aplicables para su entorno:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de administración y supervisión. El nombre del servidor debe ir seguido de un símbolo "$", como se muestra en el ejemplo (por ejemplo, MyDomain\\MyServerName1 $).

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Temas relacionados


[Mantenimiento de MBAM 2.0](maintaining-mbam-20-mbam-2.md)









