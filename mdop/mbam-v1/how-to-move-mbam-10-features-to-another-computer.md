---
title: Cómo mover funciones de MBAM 1.0 a otro equipo
description: Cómo mover funciones de MBAM 1.0 a otro equipo
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812950"
---
# Cómo mover funciones de MBAM 1.0 a otro equipo


En este tema se describen los pasos que debe seguir para mover una o más características de administración y supervisión de Microsoft BitLocker (MBAM) a un equipo diferente. Al mover más de una característica de MBAM a otro equipo, debe moverlas en el siguiente orden:

1.  Base de datos de recuperación y hardware

2.  Base de datos de cumplimiento y auditoría

3.  Informes de cumplimiento y cumplimiento

4.  Administración y supervisión

## Para mover la base de datos de recuperación y hardware


Puede usar el siguiente procedimiento para mover la base de datos de hardware y recuperación de MBAM de un equipo a otro (puede mover esta característica de MBAM Server del servidor a al servidor B):

****

1.  Detenga todas las instancias del sitio web de supervisión y administración de MBAM.

2.  Ejecute el programa de instalación de MBAM en el servidor B.

3.  Haga una copia de seguridad de la base de datos de recuperación y hardware de MBAM en el servidor A.

4.  Base de datos de recuperación y hardware de MBAM del servidor a a B

5.  Restaurar la base de datos de recuperación y hardware de MBAM en el servidor B

6.  Configurar el acceso a la base de datos de recuperación y hardware de MBAM en el servidor B

7.  Actualizar los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM

8.  Reanudar todas las instancias del sitio web de supervisión y administración de MBAM

**Para detener todas las instancias del sitio web de supervisión y administración de MBAM**

1.  Use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM en cada uno de los servidores que ejecutan la característica de supervisión y administración de MBAM. El sitio web de MBAM se denomina **Administración y supervisión de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para usar un comando en el símbolo del sistema similar al siguiente:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Para ejecutar este símbolo del sistema de PowerShell, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell. Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.



**Para ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione la base de datos de recuperación y hardware para la instalación.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para usar un comando en el símbolo del sistema similar al siguiente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia a la que se moverá la base de datos de recuperación y hardware.

    -   $DOMAIN $ \ \ $SERVERNAME $: escriba los nombres de dominio y servidor de cada aplicación de MBAM y servidor de supervisión que se pondrá en contacto con la base de datos de recuperación y hardware. Si hay varios nombres de dominio y de servidor, use un punto y coma para separar cada uno de ellos en la lista. Por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $. Además, cada nombre de servidor debe ir seguido de un **$** . Por ejemplo, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.



**Para hacer una copia de seguridad de la base de datos en el servidor A**

1.  Para realizar una copia de seguridad de la base de datos de recuperación y de hardware en el servidor A, use SQL Server Management Studio y la tarea llamada **copia de seguridad...**. De forma predeterminada, el nombre de la base de datos es **MBAM recuperación y base de datos de hardware**.

2.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    Modifique la base de datos de recuperación y hardware de MBAM para usar el modo de recuperación completa.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    Crear datos de bases de datos de hardware y recuperación de MBAM y MBAM dispositivos de copia de seguridad lógicos.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    Haga una copia de seguridad de la base de datos de hardware y la recuperación de MBAM completa.

    ```sql
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
    Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:

    -   $PASSWORD $: escriba una contraseña que usará para cifrar el archivo de clave privada.



3.  Ejecute el archivo SQL con SQL Server PowerShell y use un comando similar al siguiente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia desde la que realiza la copia de seguridad de la base de datos de recuperación y hardware.



**Para mover la base de datos y el certificado del servidor a a B**

1.  Mueva la base de datos de recuperación y de hardware de MBAM. bak del servidor a al servidor B con el explorador de Windows.

2.  Para mover el certificado de la base de datos cifrada, tendrá que usar los siguientes pasos de automatización. Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.

    -   $DESTINATIONSHARE $: escriba el nombre del uso compartido y la ruta de acceso en la que se copiarán los archivos.



**Para restaurar la base de datos en el servidor B**

1.  Restaure la base de datos de recuperación y hardware en el servidor B con SQL Server Management Studio y la tarea denominada **restore database**.

2.  Una vez ejecutada la tarea, elija el archivo de copia de seguridad de la base de datos seleccionando la opción **de dispositivo** y, a continuación, use el comando **Agregar** para elegir el archivo MBAM de la base de datos de recuperación y hardware **. bak** .

3.  Seleccione **Aceptar** para completar el proceso de restauración.

4.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    Coloque el certificado creado por el programa de instalación de MBAM.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    Agregar certificado

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    Restaure los datos de la base de datos de recuperación y de hardware de MBAM y los archivos de registro.

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **Nota**  
    Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:

    -   $PASSWORD $: escriba la contraseña que usó para cifrar el archivo de clave privada.



5.  Use Windows PowerShell para escribir una línea de comandos similar a la siguiente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el valor del ejemplo siguiente por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia a la que se restaurará la base de datos de recuperación y hardware.



**Configurar el acceso a la base de datos en el servidor B**

1.  En el servidor B, use el complemento usuarios locales y grupos en el administrador de servidores para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM Recovery and hardware dB Access**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell en el servidor B para especificar un comando similar al siguiente:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Reemplace los valores del ejemplo anterior por los valores aplicables para su entorno:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre de dominio y el nombre del equipo del servidor de supervisión y administración de MBAM. El nombre del servidor debe ir seguido de a **$** , por ejemplo, MyDomain\\MyServerName1 $.



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Para actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores**

1. En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de supervisión y administración de Microsoft BitLocker:

   -   Servicio de administración de MBAM

   -   Servicio de hardware y recuperación de MBAM

2. Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.

3. Seleccione la opción **configurationStrings** en el control de lista de secciones.

4. Elija la fila denominada **(colección)** y abra el editor de la **colección** seleccionando el botón situado en el lado derecho de la fila.

5. En el **Editor de colecciones**, elija la fila denominada **KeyRecoveryConnectionString** cuando actualizó la configuración de la aplicación ' MBAMAdministrationService ' o elija la fila llamada <strong> Microsoft. Mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString, al actualizar la configuración de ' MBAMRecoveryAndHardwareService '.

6. Actualice el **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y la instancia a la que se movió la base de datos de recuperación y hardware. Por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $.

7. Para automatizar este procedimiento, puede usar un comando similar al siguiente, usando Windows PowerShell en cada servidor de administración y supervisión:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Nota**  
   Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia en la que se encuentra la base de datos de recuperación y hardware.



**Para reanudar todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM, que se denomina **Administración de Microsoft BitLocker y supervisión**.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Para mover la característica de base de datos de estado de cumplimiento


Si elige mover la característica de base de datos de estado de cumplimiento de MBAM de un equipo a otro, como del servidor a al servidor B, debe seguir este procedimiento:

1.  Detener todas las instancias del sitio web de supervisión y administración de MBAM

2.  Ejecutar el programa de instalación de MBAM en el servidor B

3.  Hacer copia de seguridad de la base de datos en el servidor A

4.  Mover la base de datos del servidor a a B

5.  Restaurar la base de datos en el servidor B

6.  Configurar el acceso a la base de datos en el servidor B

7.  Actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores

8.  Reanudar todas las instancias del sitio web de supervisión y administración de MBAM

**Para detener todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM, que se denomina **Administración de Microsoft BitLocker y supervisión**.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Para ejecutar este comando, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell. Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.



**Para ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione la característica de base de datos de estado de cumplimiento para la instalación.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **Nota**  
    Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia a la que se moverá la base de datos de estado de cumplimiento.

    -   $DOMAIN $ \ \ $SERVERNAME $: escriba los nombres de dominio y los nombres de servidor de cada aplicación de MBAM y servidor de supervisión que se pondrá en contacto con la base de datos de estado de cumplimiento. Si hay varios nombres de dominio y nombres de servidor, use un punto y coma para separar cada uno de ellos en la lista. Por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $. Cada nombre de servidor debe ir seguido **$** de una, como se muestra en el ejemplo. Por ejemplo, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.

    -   $DOMAIN $ \ \ $USERNAME $-escriba el nombre de dominio y de usuario que usará la característica informes de cumplimiento y de auditoría para conectarse a la base de datos de estado de cumplimiento.



**Para hacer una copia de seguridad de la base de datos de cumplimiento en el servidor A**

1.  Para realizar una copia de seguridad de la base de datos de cumplimiento en el servidor A, use SQL Server Management Studio y la tarea llamada **copia de seguridad...**. De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de estado de cumplimiento**.

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Ejecute el archivo SQL con un comando similar al siguiente, usando SQL Server PowerShell:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia desde donde se hará la copia de seguridad de la base de datos de estado de cumplimiento.



**Para mover la base de datos del servidor a a B**

1.  Mueva los siguientes archivos del servidor a al servidor B con el explorador de Windows:

    -   Base de datos de estado de cumplimiento de MBAM Data. bak

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente con Windows PowerShell:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.

    -   $DESTINATIONSHARE $: escriba el nombre del recurso compartido y la ruta en la que se copiarán los archivos.



**Para restaurar la base de datos en el servidor B**

1.  Restaure la base de datos del estado de cumplimiento en el servidor B con SQL Server Management Studio y la tarea llamada **restore database...**.

2.  Una vez ejecutada la tarea, seleccione el archivo de copia de seguridad de la base de datos, seleccionando la opción de dispositivo y, a continuación, use el comando Agregar para elegir el archivo. bak de la base de datos del estado de cumplimiento de MBAM. Haga clic en Aceptar para completar el proceso de restauración.

3.  Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Ejecute el archivo SQL con un comando similar al siguiente, usando SQL Server PowerShell:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia en la que se restaurará la base de datos de estado de cumplimiento.



**Para configurar el acceso a la base de datos en el servidor B**

1.  En el servidor B, use el complemento de usuarios y grupos locales del administrador del servidor para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM acceso de BD del estado de cumplimiento**.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, usando Windows PowerShell en el servidor B:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los valores correspondientes de su entorno:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM. El nombre del servidor debe ir seguido de una **$** . Por ejemplo, MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**Para actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores**

1.  En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de supervisión y administración de Microsoft BitLocker:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.

3.  Seleccione la opción **configurationStrings** en el control de lista de secciones.

4.  Seleccione la fila con el nombre **(colección)** y abra el editor de la colección seleccionando el botón situado en el lado derecho de la fila.

5.  En el **Editor de colecciones**, seleccione la fila denominada **ComplianceStatusConnectionString**, cuando actualice la configuración de la aplicación MBAMAdministrationService, o la fila denominada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, cuando actualice la configuración de la MBAMComplianceStatusService.

6.  Actualice el valor del **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y el nombre de la instancia. Por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME, a la que se movió la base de datos de recuperación y hardware.

7.  Para automatizar este procedimiento, puede usar Windows PowerShell para especificar un comando similar al siguiente en cada servidor de administración y supervisión:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y el nombre de la instancia donde se encuentra la base de datos de recuperación y hardware.



**Para reanudar todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada uno de los servidores que ejecuta la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y supervisión de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:

    **&gt;Inicio de PS C:\\-sitio web "administración y administración de BitLocker de Microsoft"**

## Para mover los informes de cumplimiento y de auditoría


Si decide mover los informes de auditoría y cumplimiento normativo de MBAM de un equipo a otro (en concreto, si mueve la característica del servidor a al servidor B), debe seguir estos pasos y pasos:

1.  Ejecutar el programa de instalación de MBAM en el servidor B

2.  Configurar el acceso a los informes de cumplimiento y de auditoría en el servidor B

3.  Detener todas las instancias del sitio web de supervisión y administración de MBAM

4.  Actualizar los datos de conexión de los informes en los servidores de supervisión y administración de MBAM

5.  Reanudar todas las instancias del sitio web de supervisión y administración de MBAM

**Para ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione la característica de cumplimiento y auditoría para la instalación.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente mediante Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **Nota**  
    Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia donde se encuentra la base de datos de estado de cumplimiento.

    -   $DOMAIN $ \ \ $USERNAME $-escriba el nombre de dominio y el nombre de usuario que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de estado de cumplimiento.

    -   $PASSWORD $: escriba la contraseña de la cuenta de usuario que se usará para conectarse a la base de datos de estado de cumplimiento.



**Para configurar el acceso a los informes de cumplimiento y cumplimiento en el servidor B**

1.  En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de usuario que tendrán acceso a los informes de cumplimiento y cumplimiento. Agregue las cuentas de usuario al grupo local denominado "MBAM Report users".

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente mediante Windows PowerShell en el servidor B.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Reemplace el siguiente valor del ejemplo anterior con los valores aplicables para su entorno:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Para detener todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada uno de los servidores que ejecutan la característica de supervisión y administración de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Para actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores**

1. En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la dirección URL de los informes de cumplimiento.

2. Seleccione el sitio web de **Administración y administración de Microsoft BitLocker** y use la característica **Editor de configuración** que se encuentra en la sección **Administración** de la **vista de características**.

3. Seleccione la opción **appSettings** en el control de lista de secciones.

4. Desde aquí, seleccione la fila denominada **(colección)** y, a continuación, abra el editor de la **colección** seleccionando el botón situado en el lado derecho de la fila.

5. En el **Editor de colecciones**, seleccione la fila denominada "Microsoft. Mbam. Reports. URL".

6. Actualice el valor de Microsoft. Mbam. Reports. URL para reflejar el nombre del servidor para el servidor B. Si la característica informes de cumplimiento y comprobación se ha instalado en una instancia de SQL Reporting Services con nombre, asegúrese de agregar o actualizar el nombre de la instancia a la dirección URL. Por ejemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....

7. Para automatizar este procedimiento, puede usar Windows PowerShell para especificar un comando similar al siguiente en cada servidor de administración y supervisión:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **Nota**  
   Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:

   -   $SERVERNAME $: escriba el nombre del servidor en el que se instalaron los informes de cumplimiento y de auditoría.

   -   $SRSINSTANCENAME $: escriba el nombre de la instancia de SQL Reporting Services en la que se instalaron los informes de cumplimiento y comprobación.



**Para reanudar todas las instancias del sitio web de supervisión y administración de MBAM**

1.  En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Para ejecutar este comando, el módulo IIS para PowerShell debe agregarse a la instancia actual de PowerShell. Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.



## Para mover la característica de administración y supervisión


Si opta por mover la característica informes de administración y supervisión de MBAM de un equipo a otro, (si mueve la característica del servidor a al servidor B), debe seguir este procedimiento. El proceso incluye los siguientes pasos:

1.  Ejecutar el programa de instalación de MBAM en el servidor B

2.  Configurar el acceso a la base de datos en el servidor B

**Para ejecutar el programa de instalación de MBAM en el servidor B**

1.  Ejecute el programa de instalación de MBAM en el servidor B y seleccione la característica de administración para la instalación.

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **Nota**  
    Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-para el parámetro COMPLIDB \ _SQLINSTANCE, introduzca el nombre del servidor y la instancia donde se encuentra la base de datos de estado de cumplimiento. Para el parámetro RECOVERYANDHWDB \ _SQLINSTANCE, escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación y hardware.

    -   $DOMAIN $ \ \ $USERNAME $-escriba el nombre de dominio y de usuario que usará la característica informes de cumplimiento y de auditoría para conectarse a la base de datos de estado de cumplimiento.

    -   $ REPORTSSERVERURL $: escriba la dirección URL de la ubicación particular del sitio web de SQL Reporting Services. Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer". Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".



**Para configurar el acceso a las bases de datos**

1.  En servidores o servidores donde se encuentran la recuperación y el hardware, y se implementan las bases de datos de auditoría y cumplimiento, use el complemento de usuarios y grupos locales desde el administrador del servidor para agregar las cuentas de los equipos de cada servidor que ejecuta la característica de supervisión y administración de MBAM a los grupos locales denominados "acceso de base de datos de recuperación y hardware de MBAM" (servidor de base de datos de recuperación y hardware).

2.  Para automatizar este procedimiento, puede usar un comando similar al siguiente, usando Windows PowerShell en el servidor donde se implementaron las bases de datos de cumplimiento y auditoría.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  En el servidor donde se han implementado las bases de datos de recuperación y hardware, ejecute un comando similar al siguiente usando Windows PowerShell.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Reemplace el valor del ejemplo anterior por los valores correspondientes de su entorno:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM. El nombre del servidor debe ir seguido de una **$** . Por ejemplo, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Temas relacionados


[Administración de funciones de MBAM 1.0](administering-mbam-10-features.md)









