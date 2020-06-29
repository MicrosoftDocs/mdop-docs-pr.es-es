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
# <span data-ttu-id="07906-103">Cómo mover funciones de MBAM 1.0 a otro equipo</span><span class="sxs-lookup"><span data-stu-id="07906-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="07906-104">En este tema se describen los pasos que debe seguir para mover una o más características de administración y supervisión de Microsoft BitLocker (MBAM) a un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="07906-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="07906-105">Al mover más de una característica de MBAM a otro equipo, debe moverlas en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="07906-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="07906-106">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="07906-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="07906-107">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="07906-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="07906-108">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="07906-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="07906-109">Administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="07906-109">Administration and Monitoring</span></span>

## <span data-ttu-id="07906-110">Para mover la base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="07906-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="07906-111">Puede usar el siguiente procedimiento para mover la base de datos de hardware y recuperación de MBAM de un equipo a otro (puede mover esta característica de MBAM Server del servidor a al servidor B):</span><span class="sxs-lookup"><span data-stu-id="07906-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="07906-112">Detenga todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="07906-113">Ejecute el programa de instalación de MBAM en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="07906-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="07906-114">Haga una copia de seguridad de la base de datos de recuperación y hardware de MBAM en el servidor A.</span><span class="sxs-lookup"><span data-stu-id="07906-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="07906-115">Base de datos de recuperación y hardware de MBAM del servidor a a B</span><span class="sxs-lookup"><span data-stu-id="07906-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="07906-116">Restaurar la base de datos de recuperación y hardware de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="07906-117">Configurar el acceso a la base de datos de recuperación y hardware de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="07906-118">Actualizar los datos de conexión de la base de datos en los servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="07906-119">Reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="07906-120">Para detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="07906-121">Use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM en cada uno de los servidores que ejecutan la característica de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="07906-122">El sitio web de MBAM se denomina **Administración y supervisión de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="07906-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="07906-123">Para automatizar este procedimiento, puede usar Windows PowerShell para usar un comando en el símbolo del sistema similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="07906-124">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-124">Note</span></span>**  
    <span data-ttu-id="07906-125">Para ejecutar este símbolo del sistema de PowerShell, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07906-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="07906-126">Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="07906-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="07906-127">Para ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="07906-128">Ejecute el programa de instalación de MBAM en el servidor B y seleccione la base de datos de recuperación y hardware para la instalación.</span><span class="sxs-lookup"><span data-stu-id="07906-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="07906-129">Para automatizar este procedimiento, puede usar Windows PowerShell para usar un comando en el símbolo del sistema similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="07906-130">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-130">Note</span></span>**  
    <span data-ttu-id="07906-131">Reemplace los siguientes valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-132">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia a la que se moverá la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="07906-133">$DOMAIN $ \ \ $SERVERNAME $: escriba los nombres de dominio y servidor de cada aplicación de MBAM y servidor de supervisión que se pondrá en contacto con la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="07906-134">Si hay varios nombres de dominio y de servidor, use un punto y coma para separar cada uno de ellos en la lista.</span><span class="sxs-lookup"><span data-stu-id="07906-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="07906-135">Por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="07906-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="07906-136">Además, cada nombre de servidor debe ir seguido de un **$** .</span><span class="sxs-lookup"><span data-stu-id="07906-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="07906-137">Por ejemplo, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="07906-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="07906-138">Para hacer una copia de seguridad de la base de datos en el servidor A</span><span class="sxs-lookup"><span data-stu-id="07906-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="07906-139">Para realizar una copia de seguridad de la base de datos de recuperación y de hardware en el servidor A, use SQL Server Management Studio y la tarea llamada **copia de seguridad...**.</span><span class="sxs-lookup"><span data-stu-id="07906-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="07906-140">De forma predeterminada, el nombre de la base de datos es **MBAM recuperación y base de datos de hardware**.</span><span class="sxs-lookup"><span data-stu-id="07906-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="07906-141">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="07906-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="07906-142">Modifique la base de datos de recuperación y hardware de MBAM para usar el modo de recuperación completa.</span><span class="sxs-lookup"><span data-stu-id="07906-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="07906-143">Crear datos de bases de datos de hardware y recuperación de MBAM y MBAM dispositivos de copia de seguridad lógicos.</span><span class="sxs-lookup"><span data-stu-id="07906-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="07906-144">Haga una copia de seguridad de la base de datos de hardware y la recuperación de MBAM completa.</span><span class="sxs-lookup"><span data-stu-id="07906-144">Back up the full MBAM Recovery and Hardware database.</span></span>

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

    **<span data-ttu-id="07906-145">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-145">Note</span></span>**  
    <span data-ttu-id="07906-146">Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-147">$PASSWORD $: escriba una contraseña que usará para cifrar el archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="07906-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="07906-148">Ejecute el archivo SQL con SQL Server PowerShell y use un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="07906-149">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-149">Note</span></span>**  
    <span data-ttu-id="07906-150">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-151">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia desde la que realiza la copia de seguridad de la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="07906-152">Para mover la base de datos y el certificado del servidor a a B</span><span class="sxs-lookup"><span data-stu-id="07906-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="07906-153">Mueva la base de datos de recuperación y de hardware de MBAM. bak del servidor a al servidor B con el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="07906-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="07906-154">Para mover el certificado de la base de datos cifrada, tendrá que usar los siguientes pasos de automatización.</span><span class="sxs-lookup"><span data-stu-id="07906-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="07906-155">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="07906-156">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-156">Note</span></span>**  
    <span data-ttu-id="07906-157">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-158">$SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="07906-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="07906-159">$DESTINATIONSHARE $: escriba el nombre del uso compartido y la ruta de acceso en la que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="07906-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="07906-160">Para restaurar la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="07906-161">Restaure la base de datos de recuperación y hardware en el servidor B con SQL Server Management Studio y la tarea denominada **restore database**.</span><span class="sxs-lookup"><span data-stu-id="07906-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="07906-162">Una vez ejecutada la tarea, elija el archivo de copia de seguridad de la base de datos seleccionando la opción **de dispositivo** y, a continuación, use el comando **Agregar** para elegir el archivo MBAM de la base de datos de recuperación y hardware **. bak** .</span><span class="sxs-lookup"><span data-stu-id="07906-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="07906-163">Seleccione **Aceptar** para completar el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="07906-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="07906-164">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="07906-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="07906-165">Coloque el certificado creado por el programa de instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="07906-166">Agregar certificado</span><span class="sxs-lookup"><span data-stu-id="07906-166">Add certificate</span></span>

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

    <span data-ttu-id="07906-167">Restaure los datos de la base de datos de recuperación y de hardware de MBAM y los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="07906-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="07906-168">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-168">Note</span></span>**  
    <span data-ttu-id="07906-169">Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-170">$PASSWORD $: escriba la contraseña que usó para cifrar el archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="07906-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="07906-171">Use Windows PowerShell para escribir una línea de comandos similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="07906-172">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-172">Note</span></span>**  
    <span data-ttu-id="07906-173">Reemplace el valor del ejemplo siguiente por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-174">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia a la que se restaurará la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="07906-175">Configurar el acceso a la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="07906-176">En el servidor B, use el complemento usuarios locales y grupos en el administrador de servidores para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM Recovery and hardware dB Access**.</span><span class="sxs-lookup"><span data-stu-id="07906-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="07906-177">Para automatizar este procedimiento, puede usar Windows PowerShell en el servidor B para especificar un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="07906-178">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-178">Note</span></span>**  
    <span data-ttu-id="07906-179">Reemplace los valores del ejemplo anterior por los valores aplicables para su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="07906-180">$DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre de dominio y el nombre del equipo del servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="07906-181">El nombre del servidor debe ir seguido de a **$** , por ejemplo, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="07906-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="07906-182">Para actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores</span><span class="sxs-lookup"><span data-stu-id="07906-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="07906-183">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de supervisión y administración de Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="07906-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="07906-184">Servicio de administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="07906-185">Servicio de hardware y recuperación de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="07906-186">Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.</span><span class="sxs-lookup"><span data-stu-id="07906-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="07906-187">Seleccione la opción **configurationStrings** en el control de lista de secciones.</span><span class="sxs-lookup"><span data-stu-id="07906-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="07906-188">Elija la fila denominada **(colección)** y abra el editor de la **colección** seleccionando el botón situado en el lado derecho de la fila.</span><span class="sxs-lookup"><span data-stu-id="07906-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="07906-189">En el **Editor de colecciones**, elija la fila denominada **KeyRecoveryConnectionString** cuando actualizó la configuración de la aplicación ' MBAMAdministrationService ' o elija la fila llamada <strong> Microsoft. Mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString, al actualizar la configuración de ' MBAMRecoveryAndHardwareService '.</span><span class="sxs-lookup"><span data-stu-id="07906-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="07906-190">Actualice el **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y la instancia a la que se movió la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="07906-191">Por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME $.</span><span class="sxs-lookup"><span data-stu-id="07906-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="07906-192">Para automatizar este procedimiento, puede usar un comando similar al siguiente, usando Windows PowerShell en cada servidor de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="07906-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="07906-193">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-193">Note</span></span>**  
   <span data-ttu-id="07906-194">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="07906-195">$SERVERNAME $ \ \ $SQLINSTANCENAME $-escriba el nombre del servidor y la instancia en la que se encuentra la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="07906-196">Para reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="07906-197">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM, que se denomina **Administración de Microsoft BitLocker y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="07906-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="07906-198">Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="07906-199">Para mover la característica de base de datos de estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="07906-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="07906-200">Si elige mover la característica de base de datos de estado de cumplimiento de MBAM de un equipo a otro, como del servidor a al servidor B, debe seguir este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="07906-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="07906-201">Detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="07906-202">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="07906-203">Hacer copia de seguridad de la base de datos en el servidor A</span><span class="sxs-lookup"><span data-stu-id="07906-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="07906-204">Mover la base de datos del servidor a a B</span><span class="sxs-lookup"><span data-stu-id="07906-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="07906-205">Restaurar la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="07906-206">Configurar el acceso a la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="07906-207">Actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores</span><span class="sxs-lookup"><span data-stu-id="07906-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="07906-208">Reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="07906-209">Para detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="07906-210">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM, que se denomina **Administración de Microsoft BitLocker y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="07906-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="07906-211">Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="07906-212">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-212">Note</span></span>**  
    <span data-ttu-id="07906-213">Para ejecutar este comando, debe agregar el módulo IIS para PowerShell a la instancia actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07906-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="07906-214">Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="07906-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="07906-215">Para ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="07906-216">Ejecute el programa de instalación de MBAM en el servidor B y seleccione la característica de base de datos de estado de cumplimiento para la instalación.</span><span class="sxs-lookup"><span data-stu-id="07906-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="07906-217">Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="07906-218">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-218">Note</span></span>**  
    <span data-ttu-id="07906-219">Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-220">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia a la que se moverá la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="07906-221">$DOMAIN $ \ \ $SERVERNAME $: escriba los nombres de dominio y los nombres de servidor de cada aplicación de MBAM y servidor de supervisión que se pondrá en contacto con la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="07906-222">Si hay varios nombres de dominio y nombres de servidor, use un punto y coma para separar cada uno de ellos en la lista.</span><span class="sxs-lookup"><span data-stu-id="07906-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="07906-223">Por ejemplo, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="07906-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="07906-224">Cada nombre de servidor debe ir seguido **$** de una, como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="07906-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="07906-225">Por ejemplo, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="07906-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="07906-226">$DOMAIN $ \ \ $USERNAME $-escriba el nombre de dominio y de usuario que usará la característica informes de cumplimiento y de auditoría para conectarse a la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="07906-227">Para hacer una copia de seguridad de la base de datos de cumplimiento en el servidor A</span><span class="sxs-lookup"><span data-stu-id="07906-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="07906-228">Para realizar una copia de seguridad de la base de datos de cumplimiento en el servidor A, use SQL Server Management Studio y la tarea llamada **copia de seguridad...**.</span><span class="sxs-lookup"><span data-stu-id="07906-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="07906-229">De forma predeterminada, el nombre de la base de datos es **MBAM base de datos de estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="07906-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="07906-230">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="07906-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="07906-231">Ejecute el archivo SQL con un comando similar al siguiente, usando SQL Server PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="07906-232">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-232">Note</span></span>**  
    <span data-ttu-id="07906-233">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-234">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia desde donde se hará la copia de seguridad de la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="07906-235">Para mover la base de datos del servidor a a B</span><span class="sxs-lookup"><span data-stu-id="07906-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="07906-236">Mueva los siguientes archivos del servidor a al servidor B con el explorador de Windows:</span><span class="sxs-lookup"><span data-stu-id="07906-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="07906-237">Base de datos de estado de cumplimiento de MBAM Data. bak</span><span class="sxs-lookup"><span data-stu-id="07906-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="07906-238">Para automatizar este procedimiento, puede usar un comando similar al siguiente con Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="07906-239">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-239">Note</span></span>**  
    <span data-ttu-id="07906-240">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-241">$SERVERNAME $: escriba el nombre del servidor en el que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="07906-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="07906-242">$DESTINATIONSHARE $: escriba el nombre del recurso compartido y la ruta en la que se copiarán los archivos.</span><span class="sxs-lookup"><span data-stu-id="07906-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="07906-243">Para restaurar la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="07906-244">Restaure la base de datos del estado de cumplimiento en el servidor B con SQL Server Management Studio y la tarea llamada **restore database...**.</span><span class="sxs-lookup"><span data-stu-id="07906-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="07906-245">Una vez ejecutada la tarea, seleccione el archivo de copia de seguridad de la base de datos, seleccionando la opción de dispositivo y, a continuación, use el comando Agregar para elegir el archivo. bak de la base de datos del estado de cumplimiento de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="07906-246">Haga clic en Aceptar para completar el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="07906-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="07906-247">Para automatizar este procedimiento, cree un archivo SQL (. SQL) que contenga la siguiente secuencia de comandos SQL:</span><span class="sxs-lookup"><span data-stu-id="07906-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="07906-248">Ejecute el archivo SQL con un comando similar al siguiente, usando SQL Server PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="07906-249">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-249">Note</span></span>**  
    <span data-ttu-id="07906-250">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-251">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia en la que se restaurará la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="07906-252">Para configurar el acceso a la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="07906-253">En el servidor B, use el complemento de usuarios y grupos locales del administrador del servidor para agregar las cuentas de equipo de cada servidor que ejecuta la característica de supervisión y administración de MBAM al grupo local denominado **MBAM acceso de BD del estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="07906-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="07906-254">Para automatizar este procedimiento, puede usar un comando similar al siguiente, usando Windows PowerShell en el servidor B:</span><span class="sxs-lookup"><span data-stu-id="07906-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="07906-255">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-255">Note</span></span>**  
    <span data-ttu-id="07906-256">Reemplace el valor del ejemplo anterior por los valores correspondientes de su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="07906-257">$DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="07906-258">El nombre del servidor debe ir seguido de una **$** . Por ejemplo, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="07906-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="07906-259">$DOMAIN $ \ \ $REPORTSUSERNAME $-escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="07906-260">Para actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores</span><span class="sxs-lookup"><span data-stu-id="07906-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="07906-261">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la información de la cadena de conexión para las siguientes aplicaciones, que se hospedan en el sitio web de supervisión y administración de Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="07906-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="07906-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="07906-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="07906-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="07906-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="07906-264">Seleccione cada aplicación y use la característica **Editor de configuración** , que se encuentra en la sección **Administración** de la vista de **características**.</span><span class="sxs-lookup"><span data-stu-id="07906-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="07906-265">Seleccione la opción **configurationStrings** en el control de lista de secciones.</span><span class="sxs-lookup"><span data-stu-id="07906-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="07906-266">Seleccione la fila con el nombre **(colección)** y abra el editor de la colección seleccionando el botón situado en el lado derecho de la fila.</span><span class="sxs-lookup"><span data-stu-id="07906-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="07906-267">En el **Editor de colecciones**, seleccione la fila denominada **ComplianceStatusConnectionString**, cuando actualice la configuración de la aplicación MBAMAdministrationService, o la fila denominada **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, cuando actualice la configuración de la MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="07906-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="07906-268">Actualice el valor del **origen de datos =** valor de la propiedad **configurationStrings** para mostrar el nombre del servidor y el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="07906-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="07906-269">Por ejemplo, $SERVERNAME $ \ \ $SQLINSTANCENAME, a la que se movió la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="07906-270">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar un comando similar al siguiente en cada servidor de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="07906-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="07906-271">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-271">Note</span></span>**  
    <span data-ttu-id="07906-272">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-273">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y el nombre de la instancia donde se encuentra la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="07906-274">Para reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="07906-275">En cada uno de los servidores que ejecuta la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y supervisión de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="07906-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="07906-276">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="07906-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="07906-277">&gt;Inicio de PS C:\\-sitio web "administración y administración de BitLocker de Microsoft"</span><span class="sxs-lookup"><span data-stu-id="07906-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="07906-278">Para mover los informes de cumplimiento y de auditoría</span><span class="sxs-lookup"><span data-stu-id="07906-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="07906-279">Si decide mover los informes de auditoría y cumplimiento normativo de MBAM de un equipo a otro (en concreto, si mueve la característica del servidor a al servidor B), debe seguir estos pasos y pasos:</span><span class="sxs-lookup"><span data-stu-id="07906-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="07906-280">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="07906-281">Configurar el acceso a los informes de cumplimiento y de auditoría en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="07906-282">Detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="07906-283">Actualizar los datos de conexión de los informes en los servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="07906-284">Reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="07906-285">Para ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="07906-286">Ejecute el programa de instalación de MBAM en el servidor B y seleccione la característica de cumplimiento y auditoría para la instalación.</span><span class="sxs-lookup"><span data-stu-id="07906-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="07906-287">Para automatizar este procedimiento, puede usar un comando similar al siguiente mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="07906-288">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-288">Note</span></span>**  
    <span data-ttu-id="07906-289">Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-290">$SERVERNAME $ \ \ $SQLINSTANCENAME $: escriba el nombre del servidor y la instancia donde se encuentra la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="07906-291">$DOMAIN $ \ \ $USERNAME $-escriba el nombre de dominio y el nombre de usuario que usará la característica informes de cumplimiento y auditoría para conectarse a la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="07906-292">$PASSWORD $: escriba la contraseña de la cuenta de usuario que se usará para conectarse a la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="07906-293">Para configurar el acceso a los informes de cumplimiento y cumplimiento en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="07906-294">En el servidor B, use el complemento usuario local y grupos en el administrador del servidor para agregar las cuentas de usuario que tendrán acceso a los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="07906-295">Agregue las cuentas de usuario al grupo local denominado "MBAM Report users".</span><span class="sxs-lookup"><span data-stu-id="07906-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="07906-296">Para automatizar este procedimiento, puede usar un comando similar al siguiente mediante Windows PowerShell en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="07906-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="07906-297">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-297">Note</span></span>**  
    <span data-ttu-id="07906-298">Reemplace el siguiente valor del ejemplo anterior con los valores aplicables para su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="07906-299">$DOMAIN $ \ \ $REPORTSUSERNAME $-escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="07906-300">Para detener todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="07906-301">En cada uno de los servidores que ejecutan la característica de supervisión y administración de MBAM, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="07906-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="07906-302">Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="07906-303">Para actualizar los datos de conexión de la base de datos en MBAM administración y supervisión de servidores</span><span class="sxs-lookup"><span data-stu-id="07906-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="07906-304">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para actualizar la dirección URL de los informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="07906-305">Seleccione el sitio web de **Administración y administración de Microsoft BitLocker** y use la característica **Editor de configuración** que se encuentra en la sección **Administración** de la **vista de características**.</span><span class="sxs-lookup"><span data-stu-id="07906-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="07906-306">Seleccione la opción **appSettings** en el control de lista de secciones.</span><span class="sxs-lookup"><span data-stu-id="07906-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="07906-307">Desde aquí, seleccione la fila denominada **(colección)** y, a continuación, abra el editor de la **colección** seleccionando el botón situado en el lado derecho de la fila.</span><span class="sxs-lookup"><span data-stu-id="07906-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="07906-308">En el **Editor de colecciones**, seleccione la fila denominada "Microsoft. Mbam. Reports. URL".</span><span class="sxs-lookup"><span data-stu-id="07906-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="07906-309">Actualice el valor de Microsoft. Mbam. Reports. URL para reflejar el nombre del servidor para el servidor B. Si la característica informes de cumplimiento y comprobación se ha instalado en una instancia de SQL Reporting Services con nombre, asegúrese de agregar o actualizar el nombre de la instancia a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="07906-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="07906-310">Por ejemplo, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....</span><span class="sxs-lookup"><span data-stu-id="07906-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="07906-311">Para automatizar este procedimiento, puede usar Windows PowerShell para especificar un comando similar al siguiente en cada servidor de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="07906-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="07906-312">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-312">Note</span></span>**  
   <span data-ttu-id="07906-313">Reemplace el valor del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="07906-314">$SERVERNAME $: escriba el nombre del servidor en el que se instalaron los informes de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="07906-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="07906-315">$SRSINSTANCENAME $: escriba el nombre de la instancia de SQL Reporting Services en la que se instalaron los informes de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="07906-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="07906-316">Para reanudar todas las instancias del sitio web de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="07906-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="07906-317">En cada uno de los servidores que ejecutan la característica de administración y supervisión de MBAM, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de MBAM denominado **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="07906-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="07906-318">Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="07906-319">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-319">Note</span></span>**  
    <span data-ttu-id="07906-320">Para ejecutar este comando, el módulo IIS para PowerShell debe agregarse a la instancia actual de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07906-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="07906-321">Además, debe actualizar la Directiva de ejecución de PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="07906-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="07906-322">Para mover la característica de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="07906-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="07906-323">Si opta por mover la característica informes de administración y supervisión de MBAM de un equipo a otro, (si mueve la característica del servidor a al servidor B), debe seguir este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="07906-324">El proceso incluye los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="07906-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="07906-325">Ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="07906-326">Configurar el acceso a la base de datos en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="07906-327">Para ejecutar el programa de instalación de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="07906-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="07906-328">Ejecute el programa de instalación de MBAM en el servidor B y seleccione la característica de administración para la instalación.</span><span class="sxs-lookup"><span data-stu-id="07906-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="07906-329">Para automatizar este procedimiento, puede usar un comando similar al siguiente, mediante Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07906-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="07906-330">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-330">Note</span></span>**  
    <span data-ttu-id="07906-331">Reemplace los valores del ejemplo anterior por los que coincidan con su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="07906-332">$SERVERNAME $ \ \ $SQLINSTANCENAME $-para el parámetro COMPLIDB \ _SQLINSTANCE, introduzca el nombre del servidor y la instancia donde se encuentra la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="07906-333">Para el parámetro RECOVERYANDHWDB \ _SQLINSTANCE, escriba el nombre del servidor y la instancia donde se encuentra la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="07906-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="07906-334">$DOMAIN $ \ \ $USERNAME $-escriba el nombre de dominio y de usuario que usará la característica informes de cumplimiento y de auditoría para conectarse a la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="07906-335">$ REPORTSSERVERURL $: escriba la dirección URL de la ubicación particular del sitio web de SQL Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="07906-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="07906-336">Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="07906-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="07906-337">Si los informes se instalaron en una instancia predeterminada de SRS, el formato de la dirección URL tendrá el formato "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $".</span><span class="sxs-lookup"><span data-stu-id="07906-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="07906-338">Para configurar el acceso a las bases de datos</span><span class="sxs-lookup"><span data-stu-id="07906-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="07906-339">En servidores o servidores donde se encuentran la recuperación y el hardware, y se implementan las bases de datos de auditoría y cumplimiento, use el complemento de usuarios y grupos locales desde el administrador del servidor para agregar las cuentas de los equipos de cada servidor que ejecuta la característica de supervisión y administración de MBAM a los grupos locales denominados "acceso de base de datos de recuperación y hardware de MBAM" (servidor de base de datos de recuperación y hardware).</span><span class="sxs-lookup"><span data-stu-id="07906-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="07906-340">Para automatizar este procedimiento, puede usar un comando similar al siguiente, usando Windows PowerShell en el servidor donde se implementaron las bases de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="07906-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="07906-341">En el servidor donde se han implementado las bases de datos de recuperación y hardware, ejecute un comando similar al siguiente usando Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07906-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="07906-342">Nota</span><span class="sxs-lookup"><span data-stu-id="07906-342">Note</span></span>**  
    <span data-ttu-id="07906-343">Reemplace el valor del ejemplo anterior por los valores correspondientes de su entorno:</span><span class="sxs-lookup"><span data-stu-id="07906-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="07906-344">$DOMAIN $ \ \ $SERVERNAME $ $-escriba el nombre del dominio y del equipo del servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07906-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="07906-345">El nombre del servidor debe ir seguido de una **$** .</span><span class="sxs-lookup"><span data-stu-id="07906-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="07906-346">Por ejemplo, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="07906-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="07906-347">$DOMAIN $ \ \ $REPORTSUSERNAME $: escriba el nombre de la cuenta de usuario que se usó para configurar el origen de datos para los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="07906-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="07906-348">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07906-348">Related topics</span></span>


[<span data-ttu-id="07906-349">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="07906-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









