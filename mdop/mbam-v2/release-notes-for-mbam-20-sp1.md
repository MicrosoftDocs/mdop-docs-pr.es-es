---
title: Notas de la versión de MBAM 2.0 SP1
description: Notas de la versión de MBAM 2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825581"
---
# <span data-ttu-id="26037-103">Notas de la versión de MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="26037-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="26037-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="26037-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="26037-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="26037-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="26037-106">Estas notas de la versión contienen la información necesaria para instalar correctamente la administración de BitLocker y la supervisión de 2,0 SP1, y contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="26037-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="26037-107">Si hay una diferencia entre estas notas de la versión y otra documentación de MBAM 2,0 SP1, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="26037-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="26037-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="26037-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="26037-109">Problemas conocidos de MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="26037-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="26037-110">Esta sección contiene problemas conocidos de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="26037-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="26037-111">La actualización de MBAM con topología integrada de Configuration Manager a MBAM 2,0 SP1 requiere la eliminación manual de los objetos de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="26037-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="26037-112">Si está usando MBAM con Configuration Manager y desea actualizar a MBAM 2,0 SP1, debe quitar manualmente todos los objetos de Configuration Manager que se instalaron en Configuration Manager como parte de la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="26037-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="26037-113">Los objetos que debe quitar manualmente son los informes MBAM, la colección de MBAM equipos compatibles y la línea base de configuración de protección de BitLocker y los elementos de configuración asociados.</span><span class="sxs-lookup"><span data-stu-id="26037-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="26037-114">**Solución alternativa**: actualice los objetos de Configuration Manager completando los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="26037-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="26037-115">Haga una copia de seguridad de los datos de cumplimiento existentes en un archivo externo, como se describe en los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="26037-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="26037-116">**Nota:**  Todos los datos de cumplimiento de BitLocker existentes se eliminarán al eliminar la línea base existente en Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="26037-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="26037-117">Los datos se volverán a generar a lo largo del tiempo, pero se recomienda que guarde una copia de los datos en caso de que necesite los datos de cumplimiento de un equipo determinado antes de que se hayan regenerado los datos de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="26037-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="26037-118">Para guardar los datos de cumplimiento de BitLocker históricos, abra el informe **detalles de cumplimiento de BitLocker Enterprise** .</span><span class="sxs-lookup"><span data-stu-id="26037-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="26037-119">Haga clic en el icono **Guardar** en el informe y seleccione **Excel**.</span><span class="sxs-lookup"><span data-stu-id="26037-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="26037-120">El informe guardado contendrá datos como, por ejemplo, el nombre del equipo, el nombre de dominio, el estado de cumplimiento, la exención, los usuarios del dispositivo, los detalles del estado de cumplimiento y la fecha y hora del último contacto.</span><span class="sxs-lookup"><span data-stu-id="26037-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="26037-121">Algunos datos, como la información detallada del volumen y la intensidad de cifrado, no se guardan.</span><span class="sxs-lookup"><span data-stu-id="26037-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="26037-122">Desinstale **MBAM** del servidor con el instalador de **MBAM** .</span><span class="sxs-lookup"><span data-stu-id="26037-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="26037-123">Elimine manualmente los siguientes objetos de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="26037-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="26037-124">Colección de equipos compatibles con MBAM</span><span class="sxs-lookup"><span data-stu-id="26037-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="26037-125">Línea base de protección de BitLocker</span><span class="sxs-lookup"><span data-stu-id="26037-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="26037-126">Elemento de configuración de protección de unidad del sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="26037-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="26037-127">Elemento de configuración de protección de unidades de datos fijos de BitLocker</span><span class="sxs-lookup"><span data-stu-id="26037-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="26037-128">Elimine manualmente la carpeta de informes de MBAM en el sitio de SQL Server Reporting Services de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="26037-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="26037-129">Para ello:</span><span class="sxs-lookup"><span data-stu-id="26037-129">To do this:</span></span>

    1.  <span data-ttu-id="26037-130">Use Internet Explorer para desplazarse hasta el punto de servicios de informes, por ejemplo, http:// &lt; yourcmserver &gt; /Reports.</span><span class="sxs-lookup"><span data-stu-id="26037-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="26037-131">Haga clic en el vínculo de código de sitio de Configuration Manager adecuado.</span><span class="sxs-lookup"><span data-stu-id="26037-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="26037-132">Elimine la carpeta MBAM.</span><span class="sxs-lookup"><span data-stu-id="26037-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="26037-133">Use el instalador de MBAM Server para volver a instalar los objetos de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="26037-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="26037-134">Los equipos cliente comenzarán a cargar los datos de cumplimiento de BitLocker a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="26037-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="26037-135">El botón Enviar del portal de autoservicio no funciona en Internet Explorer10</span><span class="sxs-lookup"><span data-stu-id="26037-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="26037-136">Al usar Internet Explorer10 para acceder al sitio web de administración y supervisión, el botón **Enviar** del sitio web no funciona.</span><span class="sxs-lookup"><span data-stu-id="26037-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="26037-137">**Solución alternativa**: en el servidor donde instaló el sitio web de supervisión y administración, instale el [hotfix para ASP.net archivos de definición de explorador](https://go.microsoft.com/fwlink/?LinkId=317798).</span><span class="sxs-lookup"><span data-stu-id="26037-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="26037-138">No se admiten nombres de dominio internacionales</span><span class="sxs-lookup"><span data-stu-id="26037-138">International domain names are not supported</span></span>

<span data-ttu-id="26037-139">MBAM 2,0 SP1 no admite nombres de dominio internacionales.</span><span class="sxs-lookup"><span data-stu-id="26037-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="26037-140">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="26037-140">**Workaround**: None.</span></span>

### <span data-ttu-id="26037-141">Los informes del sitio web de administración y supervisión muestran una advertencia si SSL no está configurado en SSRS</span><span class="sxs-lookup"><span data-stu-id="26037-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="26037-142">Si SQLServer Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de los informes se establecerá en HTTP en lugar de HTTPS cuando instale el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="26037-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="26037-143">Si, a continuación, visita el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro".</span><span class="sxs-lookup"><span data-stu-id="26037-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="26037-144">**Solución**: para corregir este problema, configure SSL en el **Administrador de configuración de Reporting Services** en el servidor de MBAM donde esté instalado SQLServer Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="26037-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="26037-145">Desinstale y vuelva a instalar el sitio web del servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="26037-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="26037-146">Al hacer clic en atrás en el informe Resumen de cumplimiento puede crear un error</span><span class="sxs-lookup"><span data-stu-id="26037-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="26037-147">Si profundiza en un informe Resumen de cumplimiento y, a continuación, hace clic en el vínculo **atrás** en el informe de SSRS, es posible que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="26037-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="26037-148">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="26037-148">**Workaround**: None.</span></span>

### <span data-ttu-id="26037-149">El cifrado de espacio usado no funciona correctamente</span><span class="sxs-lookup"><span data-stu-id="26037-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="26037-150">Si cifra un equipo por primera vez después de instalar el cliente MBAM y ha establecido un objeto de directiva de grupo para implementar el cifrado solo de espacio usado, MBAM cifra de forma errónea todo el disco en lugar de cifrar solo el espacio usado por el disco.</span><span class="sxs-lookup"><span data-stu-id="26037-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="26037-151">Si un equipo ya está cifrado con el cifrado solo de espacio usado antes de instalar el cliente MBAM y ha establecido el mismo objeto de directiva de grupo de cifrado de espacio solo usado, MBAM reconoce la configuración e informa correctamente el cifrado en los informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="26037-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="26037-152">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="26037-152">**Workaround**: None.</span></span>

### <span data-ttu-id="26037-153">La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="26037-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="26037-154">Si no establece una intensidad de cifrado específica en el objeto de directiva de grupo **elegir método de cifrado de unidad y intensidad** de cifrado, el informe de cumplimiento de equipos de la topología integrada de Configuration Manager siempre muestra **desconocido** para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="26037-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="26037-155">El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="26037-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="26037-156">**Solución alternativa**: establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.</span><span class="sxs-lookup"><span data-stu-id="26037-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="26037-157">La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="26037-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="26037-158">Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.</span><span class="sxs-lookup"><span data-stu-id="26037-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="26037-159">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="26037-159">**Workaround**: None.</span></span> <span data-ttu-id="26037-160">No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="26037-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="26037-161">La configuración de seguridad mejorada puede provocar que los informes no se muestren correctamente</span><span class="sxs-lookup"><span data-stu-id="26037-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="26037-162">Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca un mensaje de **acceso denegado** cuando intente ver informes en el servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="26037-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="26037-163">De forma predeterminada, la configuración de seguridad mejorada está activada para proteger el servidor al disminuir la exposición del servidor a potenciales ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="26037-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="26037-164">**Solución**: Si el mensaje **acceso denegado** aparece cuando intenta ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada.</span><span class="sxs-lookup"><span data-stu-id="26037-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="26037-165">También puede ver los informes desde otro equipo en el que la configuración de seguridad mejorada no esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="26037-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="26037-166">Se produce un error en la instalación de MBAM Server al actualizar de SQLServer2008 a SQLServer2012</span><span class="sxs-lookup"><span data-stu-id="26037-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="26037-167">Si actualiza de SQLServer2008 a SQLServer2012 y, a continuación, intenta instalar la base de datos de cumplimiento y auditoría o la base de datos de recuperación, se produce un error en la instalación y se deshace.</span><span class="sxs-lookup"><span data-stu-id="26037-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="26037-168">El error se produce porque el archivo de SQLCMD.exe necesario se quitó durante la actualización de SQLServer y el instalador de MBAM no lo puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="26037-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="26037-169">Las líneas del archivo de registro MSI pueden tener un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="26037-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="26037-170">RunDbInstallScript de BD de recuperación de RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exede BD dB de recuperación: dbInstance-xxxxxx\\I01RunDbInstallScript de BD Recovery: sqlScript-C:\\Archivos de Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript de BD de recuperación: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript defaultFileName-MBAM _Recovery \ I01\\MSSQL\\DATA\\RunDbInstallScript de BD de recuperación de certificados: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperación de la BD CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de BD Recovery dB: comenzando a ejecutar el complemento de base de datos de recuperación scriptRunDbInstallScript recuperación de BD de BD: el archivo de registro SQLCMD se encuentra en C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript de BD de recuperación excepción: instalar la acción personalizada de la base de datos de recuperación excepción: el sistema no puede encontrar el archivo especificado</span><span class="sxs-lookup"><span data-stu-id="26037-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="26037-171">El Windows Installer de MBAM Server está codificado para encontrar la ruta de acceso SQLCMD.exe mirando en el valor de la cadena de la ruta de acceso en el registro en HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="26037-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="26037-172">La clave sigue presente durante la migración de SQLServer2008 a SQLServer2012, pero la ruta de acceso a la que hace referencia el valor de los datos no contiene el archivo SQLCMD.exe, porque el proceso de SQLupgrade quitó el archivo.</span><span class="sxs-lookup"><span data-stu-id="26037-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="26037-173">**Solución alternativa**: Cambie temporalmente el valor de la cadena de ruta de acceso de HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup a **path \ _old**y, a continuación, vuelva a ejecutar Windows Installer en el servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="26037-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="26037-174">Cuando la instalación se complete correctamente y cree las bases de datos en SQLServer2012, cambie el nombre de **path \ _old** a **path**.</span><span class="sxs-lookup"><span data-stu-id="26037-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="26037-175">Revisiones y artículos de Knowledge base para MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="26037-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="26037-176">Esta sección contiene revisiones y artículos de KB para MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="26037-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="26037-177">Artículo de KB</span><span class="sxs-lookup"><span data-stu-id="26037-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="26037-178">Title</span><span class="sxs-lookup"><span data-stu-id="26037-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="26037-179">Link</span><span class="sxs-lookup"><span data-stu-id="26037-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-180">2831166</span><span class="sxs-lookup"><span data-stu-id="26037-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-181">Instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falla con los &quot; objetos de System Center cm ya instalados&quot;</span><span class="sxs-lookup"><span data-stu-id="26037-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="26037-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-183">2870849</span><span class="sxs-lookup"><span data-stu-id="26037-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-184">Los usuarios no pueden recuperar la clave de recuperación de BitLocker con el portal de autoservicio de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="26037-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="26037-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-186">2756402</span><span class="sxs-lookup"><span data-stu-id="26037-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-187">El cliente de MBAM no funcionaba con el identificador de evento 4 y el código de error 0x8004100E en la descripción del evento</span><span class="sxs-lookup"><span data-stu-id="26037-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="26037-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-189">2620287</span><span class="sxs-lookup"><span data-stu-id="26037-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-190">Mensaje de error "error de servidor en '/Reports ' aplicación" al hacer clic en la pestaña informes en MBAM</span><span class="sxs-lookup"><span data-stu-id="26037-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="26037-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-192">2639518</span><span class="sxs-lookup"><span data-stu-id="26037-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-193">Error al abrir informes de cumplimiento de los equipos o de la empresa en MBAM</span><span class="sxs-lookup"><span data-stu-id="26037-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="26037-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-195">2620269</span><span class="sxs-lookup"><span data-stu-id="26037-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-196">Los informes de empresa de MBAM no se actualizan</span><span class="sxs-lookup"><span data-stu-id="26037-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="26037-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-198">2712461</span><span class="sxs-lookup"><span data-stu-id="26037-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-199">No se admite la instalación de MBAM en un controlador de dominio</span><span class="sxs-lookup"><span data-stu-id="26037-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="26037-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-201">2876732</span><span class="sxs-lookup"><span data-stu-id="26037-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-202">Recibe el código de error 0x80071a90 durante la instalación independiente o de integración del administrador de configuración de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="26037-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="26037-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-204">2754259</span><span class="sxs-lookup"><span data-stu-id="26037-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-205">MBAM y comunicaciones seguras de red</span><span class="sxs-lookup"><span data-stu-id="26037-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="26037-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-207">2870842</span><span class="sxs-lookup"><span data-stu-id="26037-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-208">El programa de instalación de MBAM 2.0 falla durante el escenario de integración de Configuration Manager con SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="26037-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="26037-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-210">2668533</span><span class="sxs-lookup"><span data-stu-id="26037-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-211">Se produce un error en la instalación de MBAM si SQL SSRS no se ha configurado correctamente</span><span class="sxs-lookup"><span data-stu-id="26037-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="26037-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-213">2870847</span><span class="sxs-lookup"><span data-stu-id="26037-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-214">La instalación de MBAM 2,0 produce un &quot; error al recuperar la configuración del rol de servidor de Configuration Manager para &#39;rol de&#39; de punto de servicios de informes&quot;</span><span class="sxs-lookup"><span data-stu-id="26037-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="26037-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-216">2870839</span><span class="sxs-lookup"><span data-stu-id="26037-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-217">Los informes de MBAM 2.0 Enterprise no se actualizan en la topología de MBAM 2.0 Standalone debido a errores de CreateCache de trabajo de SQL</span><span class="sxs-lookup"><span data-stu-id="26037-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="26037-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-219">2620269</span><span class="sxs-lookup"><span data-stu-id="26037-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-220">Los informes de empresa de MBAM no se actualizan</span><span class="sxs-lookup"><span data-stu-id="26037-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="26037-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26037-222">2935997</span><span class="sxs-lookup"><span data-stu-id="26037-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-223">MBAM equipos compatibles los informes de cumplimiento incluyen incorrectamente los productos no compatibles</span><span class="sxs-lookup"><span data-stu-id="26037-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="26037-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26037-225">2612822</span><span class="sxs-lookup"><span data-stu-id="26037-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="26037-226">El registro del equipo se ha rechazado en MBAM</span><span class="sxs-lookup"><span data-stu-id="26037-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="26037-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="26037-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="26037-228">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26037-228">Related topics</span></span>


[<span data-ttu-id="26037-229">Acerca de MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="26037-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 





