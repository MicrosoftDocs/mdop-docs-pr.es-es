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
# <span data-ttu-id="9ddf2-103">Cómo mover funciones de MBAM 2.0 a otro equipo</span><span class="sxs-lookup"><span data-stu-id="9ddf2-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="9ddf2-104">En este tema se describen los pasos que debe seguir para mover una o más características de administración y supervisión de Microsoft BitLocker (MBAM) a un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="9ddf2-105">Al mover más de una característica de administración y administración de Microsoft BitLocker, debe moverlas en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="9ddf2-106">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="9ddf2-106">Recovery Database</span></span>

2.  <span data-ttu-id="9ddf2-107">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="9ddf2-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="9ddf2-108">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="9ddf2-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="9ddf2-109">Administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="9ddf2-109">Administration and Monitoring</span></span>

## <span data-ttu-id="9ddf2-110">Mover la base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="9ddf2-110">Moving the Recovery Database</span></span>


<span data-ttu-id="9ddf2-111">Para mover la base de datos de recuperación de un equipo a otro (por ejemplo, del servidor a al servidor B), use el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="9ddf2-112">Detenga todas las instancias del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="9ddf2-113">Ejecute el programa de instalación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="9ddf2-114">Haga una copia de seguridad de la base de datos de recuperación de MBAM en el servidor A.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="9ddf2-115">Mueva la base de datos de recuperación de MBAM desde el servidor a a B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="9ddf2-116">Restaure la base de datos de recuperación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="9ddf2-117">Configure el acceso a la base de datos de recuperación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="9ddf2-118">Actualice los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="9ddf2-119">Resume todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="9ddf2-120">Detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9ddf2-121">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM, que se denomina **Administración de Microsoft BitLocker y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9ddf2-122">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar la línea de comandos que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9ddf2-123">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-123">Note</span></span>**  
    <span data-ttu-id="9ddf2-124">Para ejecutar esta línea de comandos de PowerShell, el módulo IIS para PowerShell debe agregarse a la instancia actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="9ddf2-125">Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="9ddf2-126">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-127">Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la **base de datos de recuperación** para la instalación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="9ddf2-128">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar la línea de comandos que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="9ddf2-129">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-129">Note</span></span>**  
    <span data-ttu-id="9ddf2-130">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-131">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia a la que se moverá la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="9ddf2-132">$DOMAIN $ \ \ $SERVERNAME $: escriba los nombres de dominio y servidor de cada MBAM de administración y supervisión que se pondrá en contacto con la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="9ddf2-133">Use punto y coma para separar cada pareja de dominio y servidor de la lista (por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="9ddf2-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="9ddf2-134">Cada nombre de servidor debe ir seguido de un símbolo "$", como se muestra en el ejemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="9ddf2-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="9ddf2-135">$X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9ddf2-136">Hacer copia de seguridad de la base de datos de recuperación del servidor A</span><span class="sxs-lookup"><span data-stu-id="9ddf2-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="9ddf2-137">Para hacer una copia de seguridad de la base de datos de recuperación en el servidor A, use SQL Server Management Studio y la tarea llamada copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="9ddf2-138">De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="9ddf2-139">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="9ddf2-140">Modifique la base de datos de recuperación de MBAM para usar el modo de recuperación completa.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

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

    **<span data-ttu-id="9ddf2-141">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-141">Note</span></span>**  
    <span data-ttu-id="9ddf2-142">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-143">$PASSWORD $: escriba una contraseña que usará para cifrar el archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="9ddf2-144">Ejecute el archivo SQL mediante SQL Server PowerShell y una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9ddf2-145">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-145">Note</span></span>**  
    <span data-ttu-id="9ddf2-146">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-147">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia desde donde se hará la copia de seguridad de la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="9ddf2-148">Mover la base de datos y el certificado de recuperación desde el servidor a al servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="9ddf2-149">Mueva el archivo siguiente del servidor a al servidor B con el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="9ddf2-150">MBAM de base de datos de recuperación. bak</span><span class="sxs-lookup"><span data-stu-id="9ddf2-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="9ddf2-151">Para mover el certificado de la base de datos cifrada, use los siguientes pasos de automatización.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="9ddf2-152">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="9ddf2-153">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-153">Note</span></span>**  
    <span data-ttu-id="9ddf2-154">Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-155">$SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="9ddf2-156">$DESTINATIONSHARE $: escriba el nombre del uso compartido y la ruta de acceso en la que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="9ddf2-157">Restaurar la base de datos de recuperación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-158">Restaure la base de datos de recuperación en el servidor B con SQL Server Management Studio y la tarea denominada **restore database**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="9ddf2-159">Una vez completada la tarea, seleccione el archivo de copia de seguridad de la base de datos seleccionando la opción **de dispositivo** y, a continuación, use el comando **Agregar** para seleccionar el archivo datos de la base de datos de recuperación de MBAM **. bak** .</span><span class="sxs-lookup"><span data-stu-id="9ddf2-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="9ddf2-160">Seleccione **Aceptar** para completar el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="9ddf2-161">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    **<span data-ttu-id="9ddf2-162">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-162">Note</span></span>**  
    <span data-ttu-id="9ddf2-163">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-164">$PASSWORD $: escriba una contraseña que usó para cifrar el archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="9ddf2-165">Puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9ddf2-166">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-166">Note</span></span>**  
    <span data-ttu-id="9ddf2-167">Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-168">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia en la que se restaurará la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="9ddf2-169">Configurar el acceso a la base de datos de recuperación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-170">En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM Recovery and hardware dB Access**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="9ddf2-171">Verifique que el inicio de sesión de SQL **MBAM recuperación y el acceso a la BD de hardware** en la base de datos restaurada se asigne al nombre de inicio de sesión **$MachineName $ \\MBAM de acceso de la BD de hardware y recuperación**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="9ddf2-172">Si no está asignado tal como se describe, cree otro inicio de sesión con pertenencias a grupos similares, y asígnela al nombre de inicio de sesión **$MachineName $ \\MBAM de la recuperación y el acceso a la BD de hardware**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="9ddf2-173">Para automatizar este procedimiento, puede usar Windows PowerShell en el servidor B para especificar una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="9ddf2-174">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-174">Note</span></span>**  
    <span data-ttu-id="9ddf2-175">Reemplace los siguientes valores del ejemplo anterior por los valores aplicables para su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9ddf2-176">$DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9ddf2-177">El nombre del servidor debe ir seguido de un $, como se muestra en el ejemplo (por ejemplo, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="9ddf2-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="9ddf2-178">Actualizar los datos de conexión de la base de datos de recuperación en los servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="9ddf2-179">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="9ddf2-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="9ddf2-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="9ddf2-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="9ddf2-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="9ddf2-182">Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="9ddf2-183">Seleccione la opción **configurationStrings** en el control de **lista de secciones** .</span><span class="sxs-lookup"><span data-stu-id="9ddf2-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="9ddf2-184">Seleccione la fila denominada **(colección)** y abra el **Editor** de la colección seleccionando el botón situado en el lado derecho de la fila.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="9ddf2-185">En el **Editor de colecciones**, seleccione la fila denominada **KeyRecoveryConnectionString** al actualizar la configuración de la aplicación MBAMAdministrationService o la fila denominada <strong> Microsoft. Mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString al actualizar la configuración de la MBAMRecoveryAndHardwareService.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="9ddf2-186">Actualice el **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y la instancia (por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $) donde se movió la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="9ddf2-187">Para automatizar este procedimiento, puede usar Windows para escribir una línea de comandos, que es similar a la siguiente, en cada servidor de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="9ddf2-188">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-188">Note</span></span>**  
   <span data-ttu-id="9ddf2-189">Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="9ddf2-190">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="9ddf2-191">Reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9ddf2-192">En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM, que se denomina **Administración de BitLocker de Microsoft y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9ddf2-193">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="9ddf2-194">Mover la característica de base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="9ddf2-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="9ddf2-195">Si desea mover la base de datos de auditoría y cumplimiento de MBAM de un equipo a otro (es decir, mover la base de datos del servidor a al servidor B), use el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="9ddf2-196">El proceso incluye los siguientes pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="9ddf2-197">Detenga todas las instancias del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="9ddf2-198">Ejecute el programa de instalación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="9ddf2-199">Haga una copia de seguridad de la base de datos en el servidor A.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="9ddf2-200">Mueva la base de datos del servidor a a B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="9ddf2-201">Restaure la base de datos en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="9ddf2-202">Configure el acceso a la base de datos en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="9ddf2-203">Actualice los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="9ddf2-204">Actualice la cadena de conexión del origen de datos SSRS Reports con la nueva ubicación de la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="9ddf2-205">Reanude todas las instancias del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="9ddf2-206">Detener todas las instancias del sitio web de supervisión y supervisión</span><span class="sxs-lookup"><span data-stu-id="9ddf2-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9ddf2-207">En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9ddf2-208">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9ddf2-209">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-209">Note</span></span>**  
    <span data-ttu-id="9ddf2-210">Para ejecutar esta línea de comandos, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="9ddf2-211">Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="9ddf2-212">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-213">Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la **base de datos de cumplimiento y auditoría** para la instalación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="9ddf2-214">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="9ddf2-215">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-215">Note</span></span>**  
    <span data-ttu-id="9ddf2-216">Nota: Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-217">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia a la que se moverá la base de datos de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="9ddf2-218">$DOMAIN $ \ \ $SERVERNAME $-escriba los nombres de dominio y servidor de cada MBAM de administración y supervisión que se comunicarán con la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="9ddf2-219">Use un punto y coma para separar cada pareja de dominio y servidor de la lista (por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="9ddf2-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="9ddf2-220">Cada nombre de servidor debe ir seguido de un símbolo "$", como se muestra en el ejemplo (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="9ddf2-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="9ddf2-221">$DOMAIN $ \ \ $USERNAME $-escriba el nombre de usuario y de dominio que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9ddf2-222">$X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9ddf2-223">Realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A</span><span class="sxs-lookup"><span data-stu-id="9ddf2-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="9ddf2-224">Para realizar una copia de seguridad de la base de datos de auditoría y cumplimiento en el servidor A, use SQL Server Management Studio y la tarea llamada **copia de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="9ddf2-225">De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="9ddf2-226">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="9ddf2-227">Ejecute el archivo SQL con una línea de comandos de Windows PowerShell similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9ddf2-228">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-228">Note</span></span>**  
    <span data-ttu-id="9ddf2-229">Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-230">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia donde se realizará una copia de seguridad de la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="9ddf2-231">Mover la base de datos de cumplimiento y comprobación del servidor a a B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="9ddf2-232">Mueva los siguientes archivos del servidor a al servidor B con el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="9ddf2-233">Base de datos de estado de cumplimiento de MBAM Data. bak</span><span class="sxs-lookup"><span data-stu-id="9ddf2-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="9ddf2-234">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="9ddf2-235">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-235">Note</span></span>**  
    <span data-ttu-id="9ddf2-236">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-237">$SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="9ddf2-238">$DESTINATIONSHARE $: escriba el nombre del recurso compartido y la ruta en la que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="9ddf2-239">Restaurar la base de datos de cumplimiento y comprobación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-240">Restaure la base de datos de comprobación y cumplimiento en el servidor B con SQL Server Management Studio y la tarea denominada **restore database**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="9ddf2-241">Una vez completada la tarea, seleccione el archivo de copia de seguridad de la base de datos seleccionando la opción **de dispositivo** y, a continuación, use el comando **Agregar** para seleccionar el archivo de base de datos de estado de cumplimiento MBAM. bak.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="9ddf2-242">Seleccione **Aceptar** para completar el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="9ddf2-243">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="9ddf2-244">Ejecute el archivo SQL con una línea de comandos de Windows PowerShell similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9ddf2-245">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-245">Note</span></span>**  
    <span data-ttu-id="9ddf2-246">Reemplace el siguiente valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-247">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia donde se restaurará la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="9ddf2-248">Configurar el acceso a la base de datos de cumplimiento y comprobación en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-249">En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM acceso a la base de cumplimiento del estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="9ddf2-250">Compruebe que el inicio de sesión de **MBAM auditoría de cumplimiento de BD Access** en la base de datos restaurada se asigne al nombre de inicio de sesión **$MachineName $ \ \ MBAM acceso a las bases**de datos de auditoría de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="9ddf2-251">Si no está asignado tal como se describe, cree otro inicio de sesión con pertenencias a grupos similares, y asígnela al nombre de inicio de sesión **$MachineName $ \ \ MBAM acceso a las bases de verificación de auditoría de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="9ddf2-252">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos en el servidor B que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="9ddf2-253">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-253">Note</span></span>**  
    <span data-ttu-id="9ddf2-254">Reemplace los siguientes valores del ejemplo anterior por los valores aplicables para su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9ddf2-255">$DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9ddf2-256">El nombre del servidor debe ir seguido de un "$", tal y como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="9ddf2-257">(por ejemplo, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="9ddf2-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="9ddf2-258">$DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="9ddf2-259">Actualizar los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="9ddf2-260">En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="9ddf2-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="9ddf2-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="9ddf2-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="9ddf2-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="9ddf2-263">Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="9ddf2-264">Seleccione la opción **configurationStrings** en el control de **lista de secciones** .</span><span class="sxs-lookup"><span data-stu-id="9ddf2-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="9ddf2-265">Seleccione la fila con el nombre **(colección)** y abra el editor de la **colección** seleccionando el botón situado en el lado derecho de la fila.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="9ddf2-266">En el **Editor de colecciones**, seleccione la fila denominada **ComplianceStatusConnectionString** al actualizar la configuración de la aplicación MBAMAdministrationService, o la fila denominada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** al actualizar la configuración de la MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="9ddf2-267">Actualice el valor del **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y de la instancia (por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME) al que se movió la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="9ddf2-268">Para automatizar este procedimiento, puede usar Windows para especificar una línea de comandos en cada servidor de administración y supervisión que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="9ddf2-269">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-269">Note</span></span>**  
    <span data-ttu-id="9ddf2-270">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-271">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="9ddf2-272">Reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9ddf2-273">En cada servidor que ejecute la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9ddf2-274">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="9ddf2-275">Mover los informes de cumplimiento y de auditoría</span><span class="sxs-lookup"><span data-stu-id="9ddf2-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="9ddf2-276">Si quiere mover los informes de auditoría y cumplimiento normativo de MBAM de un equipo a otro (es decir, mover los informes del servidor a al servidor B), use el procedimiento siguiente, que incluye los siguientes pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="9ddf2-277">Ejecute el programa de instalación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="9ddf2-278">Configure el acceso a los informes de auditoría y cumplimiento en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="9ddf2-279">Detenga todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="9ddf2-280">Actualice los datos de conexión de los informes en los servidores de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="9ddf2-281">Resume todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="9ddf2-282">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-283">Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la característica **informes de cumplimiento y de auditoría** para la instalación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="9ddf2-284">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="9ddf2-285">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-285">Note</span></span>**  
    <span data-ttu-id="9ddf2-286">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-287">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia donde se encuentra la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="9ddf2-288">$DOMAIN $ \ \ $USERNAME $-escriba el nombre de usuario y de dominio que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9ddf2-289">$PASSWORD $: escriba la contraseña de la cuenta de usuario que se usará para conectarse a la base de datos de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9ddf2-290">$X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9ddf2-291">Configurar el acceso a los informes de cumplimiento y de auditoría en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-292">En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de usuario que tendrán acceso a los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="9ddf2-293">Agregue las cuentas de usuario al grupo local denominado MBAM Report users.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="9ddf2-294">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos en el servidor B que es similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="9ddf2-295">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-295">Note</span></span>**  
    <span data-ttu-id="9ddf2-296">Reemplace los siguientes valores del ejemplo anterior por los valores aplicables para su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9ddf2-297">$DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="9ddf2-298">Detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9ddf2-299">En cada servidor que ejecute la característica servidor de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9ddf2-300">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="9ddf2-301">Actualizar los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="9ddf2-302">En cada servidor que ejecute la característica servidor de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la dirección URL de informes de cumplimiento y de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="9ddf2-303">Seleccione el sitio web de **Administración y administración de Microsoft BitLocker** y use la característica **Editor de configuración** que se encuentra en la sección **Administración** de la **vista de características**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="9ddf2-304">Seleccione la opción **appSettings** en el control de **lista de secciones** .</span><span class="sxs-lookup"><span data-stu-id="9ddf2-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="9ddf2-305">Seleccione la fila denominada **(colección)** y abra el **Editor** de la colección seleccionando el botón situado en el lado derecho de la fila.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="9ddf2-306">En el **Editor de colecciones**, seleccione la fila denominada **Microsoft. Mbam. Reports. URL**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="9ddf2-307">Actualice el valor de **Microsoft. Mbam. Reports. URL** para reflejar el nombre del servidor para el servidor B. Si la característica informes de cumplimiento y comprobación se ha instalado en una instancia de SQL Reporting Services con nombre, asegúrese de agregar o actualizar el nombre de la instancia a la dirección URL (por ejemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....)</span><span class="sxs-lookup"><span data-stu-id="9ddf2-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="9ddf2-308">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos en cada servidor de administración y supervisión que sea similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="9ddf2-309">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-309">Note</span></span>**  
   <span data-ttu-id="9ddf2-310">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="9ddf2-311">$SERVERNAME $: escriba el nombre del servidor al que se instalaron los informes de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="9ddf2-312">$SRSINSTANCENAME $: escriba el nombre de la instancia de SQL Reporting Services en la que se instalaron los informes de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="9ddf2-313">Reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ddf2-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9ddf2-314">En cada servidor que ejecute la característica servidor de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9ddf2-315">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9ddf2-316">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-316">Note</span></span>**  
    <span data-ttu-id="9ddf2-317">Para ejecutar esta línea de comandos, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="9ddf2-318">Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="9ddf2-319">Desplazamiento de la característica de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="9ddf2-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="9ddf2-320">Si desea mover la característica de informes de administración y supervisión de MBAM de un equipo a otro (es decir, mover la característica del servidor a al servidor B), use el procedimiento siguiente, que incluye los siguientes pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="9ddf2-321">Ejecute el programa de instalación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="9ddf2-322">Configure el acceso a la base de datos en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="9ddf2-323">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="9ddf2-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9ddf2-324">Ejecute el programa de instalación de MBAM en el servidor B y seleccione solo la característica **servidor de administración y supervisión** para la instalación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="9ddf2-325">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="9ddf2-326">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-326">Note</span></span>**  
    <span data-ttu-id="9ddf2-327">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9ddf2-328">$SERVERNAME $ \ \ $SQLINSTANCENAME $-para el parámetro COMPLIDB \ _SQLINSTANCE, escriba el nombre del servidor y la instancia donde se encuentra la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="9ddf2-329">Para el parámetro RECOVERYANDHWDB \ _SQLINSTANCE, escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="9ddf2-330">$DOMAIN $ \ \ $USERNAME $-escriba el nombre de usuario y de dominio que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9ddf2-331">$ REPORTSSERVERURL $: escriba la dirección URL de la ubicación particular del sitio web de SQL Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="9ddf2-332">Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="9ddf2-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="9ddf2-333">Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".</span><span class="sxs-lookup"><span data-stu-id="9ddf2-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="9ddf2-334">$X $-escriba **0** si está instalando la topología independiente MBAM, o **1** si está instalando la topología MBAM de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9ddf2-335">Configurar el acceso a las bases de datos</span><span class="sxs-lookup"><span data-stu-id="9ddf2-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="9ddf2-336">En el servidor o servidores donde está implementada la base de datos de recuperación y la base de datos de cumplimiento y auditoría, use el complemento de grupo y usuario local en el administrador de servidores para agregar las cuentas de equipo de cada servidor que ejecuta la característica servidor de administración y supervisión de MBAM en los grupos locales denominados acceso de base de datos de recuperación **y hardware** **, servidor de BD**</span><span class="sxs-lookup"><span data-stu-id="9ddf2-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="9ddf2-337">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar una línea de comandos, que es similar a la siguiente, en el servidor donde se implementó la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="9ddf2-338">En el servidor en el que se implementó la base de datos de recuperación, puede usar Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="9ddf2-339">Nota</span><span class="sxs-lookup"><span data-stu-id="9ddf2-339">Note</span></span>**  
    <span data-ttu-id="9ddf2-340">Reemplace el siguiente valor del ejemplo anterior por los valores aplicables para su entorno:</span><span class="sxs-lookup"><span data-stu-id="9ddf2-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9ddf2-341">$DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="9ddf2-342">El nombre del servidor debe ir seguido de un símbolo "$", como se muestra en el ejemplo (por ejemplo, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="9ddf2-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="9ddf2-343">$DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9ddf2-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="9ddf2-344">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ddf2-344">Related topics</span></span>


[<span data-ttu-id="9ddf2-345">Mantenimiento de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9ddf2-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









