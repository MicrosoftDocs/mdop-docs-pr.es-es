---
title: Solución de problemas de instalación de MBAM 2.5
description: Introducción a la solución de problemas de instalación de MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812863"
---
# <span data-ttu-id="64632-103">Solución de problemas de instalación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="64632-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="64632-104">En este artículo se presenta cómo solucionar problemas de instalación de Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 en una configuración independiente.</span><span class="sxs-lookup"><span data-stu-id="64632-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="64632-105">Referencia de los archivos de registro de MBAM para la solución de problemas</span><span class="sxs-lookup"><span data-stu-id="64632-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="64632-106">MBAM incluye el registro de instalación de servidor, instalación de cliente y eventos.</span><span class="sxs-lookup"><span data-stu-id="64632-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="64632-107">Debe hacerse referencia a este registro para la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="64632-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="64632-108">Archivos de registro de instalación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="64632-108">MBAM server installation log files</span></span>

<span data-ttu-id="64632-109">MBAMServerSetup.exe genera los siguientes archivos de registro en la carpeta% Temp% del usuario durante la instalación de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="64632-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 números>. log</span><span class="sxs-lookup"><span data-stu-id="64632-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="64632-111">MBAMServerSetup.exe registra las acciones que se llevaron a cabo durante la instalación de MBAM y MBAM Server Feature:</span><span class="sxs-lookup"><span data-stu-id="64632-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="64632-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="64632-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="64632-113">MBAMServerSetup.exe registra las acciones adicionales que se llevaron a cabo durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="64632-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="64632-114">Archivo de registro de instalación del cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-114">MBAM client installation log file</span></span>

<span data-ttu-id="64632-115">La instalación del cliente se registra en el siguiente archivo de registro en la carpeta% Temp% (o en una ubicación personalizada, según la instalación del cliente):</span><span class="sxs-lookup"><span data-stu-id="64632-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="64632-116">MSI \<five random characters\> . log</span><span class="sxs-lookup"><span data-stu-id="64632-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="64632-117">Este registro contiene las acciones que se realizan durante la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="64632-118">Canal de registro de eventos de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="64632-119">MBAM tiene canales de registro de eventos separados.</span><span class="sxs-lookup"><span data-stu-id="64632-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="64632-120">Los archivos de registro, analítico y operativo se encuentran en el visor de eventos, en **registros de aplicaciones y servicios**de  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="64632-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="64632-121">En la tabla siguiente se proporciona una breve descripción de cada registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="64632-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="64632-122">Registro de eventos</span><span class="sxs-lookup"><span data-stu-id="64632-122">Event log</span></span>| <span data-ttu-id="64632-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="64632-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="64632-124">Microsoft-Windows-MBAM/admin</span><span class="sxs-lookup"><span data-stu-id="64632-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="64632-125">Contiene mensajes de error</span><span class="sxs-lookup"><span data-stu-id="64632-125">Contains error messages</span></span>|
|<span data-ttu-id="64632-126">Microsoft-Windows-MBAM/analítico</span><span class="sxs-lookup"><span data-stu-id="64632-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="64632-127">Contiene información de registro avanzada</span><span class="sxs-lookup"><span data-stu-id="64632-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="64632-128">Microsoft-Windows-MBAM/Operational</span><span class="sxs-lookup"><span data-stu-id="64632-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="64632-129">Contiene mensajes de éxito</span><span class="sxs-lookup"><span data-stu-id="64632-129">Contains success messages</span></span>|

### <span data-ttu-id="64632-130">MBAM: canal de registro de eventos del servidor</span><span class="sxs-lookup"><span data-stu-id="64632-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="64632-131">Los archivos de registro se encuentran en el visor de eventos, en **registros de aplicaciones y servicios**de  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="64632-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="64632-132">En la tabla siguiente se incluyen los registros de eventos del servidor que se introdujeron en MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="64632-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="64632-133">Registro de eventos</span><span class="sxs-lookup"><span data-stu-id="64632-133">Event log</span></span>| <span data-ttu-id="64632-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="64632-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="64632-135">Microsoft-Windows-MBAM/admin</span><span class="sxs-lookup"><span data-stu-id="64632-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="64632-136">Contiene mensajes de error</span><span class="sxs-lookup"><span data-stu-id="64632-136">Contains error messages</span></span>|
|<span data-ttu-id="64632-137">Microsoft-Windows-MBAM/analítico</span><span class="sxs-lookup"><span data-stu-id="64632-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="64632-138">Contiene información de registro avanzada</span><span class="sxs-lookup"><span data-stu-id="64632-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="64632-139">Microsoft-Windows-MBAM/Operational</span><span class="sxs-lookup"><span data-stu-id="64632-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="64632-140">Contiene mensajes de éxito</span><span class="sxs-lookup"><span data-stu-id="64632-140">Contains success messages</span></span>|

### <span data-ttu-id="64632-141">Registros de servicio Web de MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-141">MBAM web service logs</span></span>

<span data-ttu-id="64632-142">Cada registro del servicio Web de MBAM escribe la información de registro en un archivo de SVCLOG.</span><span class="sxs-lookup"><span data-stu-id="64632-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="64632-143">De forma predeterminada, cada servicio web escribe el archivo de seguimiento en una carpeta que usa su nombre en la carpeta C:\inetpub\Microsoft de administración de BitLocker de Solution\Logs.</span><span class="sxs-lookup"><span data-stu-id="64632-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="64632-144">Puede usar la herramienta Service Trace Viewer (parte de Microsoft Visual Studio) para revisar los seguimientos de svclog.</span><span class="sxs-lookup"><span data-stu-id="64632-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="64632-145">Solución de problemas de cifrado e informes</span><span class="sxs-lookup"><span data-stu-id="64632-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="64632-146">Esta sección contiene información de solución de problemas para la funcionalidad del servidor, la funcionalidad del cliente, la configuración y los problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="64632-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="64632-147">Instalación de cliente de MBAM, configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="64632-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="64632-148">Determine si el agente de MBAM está instalado en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="64632-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="64632-149">Cuando MBAM está instalado, crea un servicio que se denomina servicio de cliente de administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64632-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="64632-150">Este servicio está configurado para iniciarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="64632-150">This service is configured to start automatically.</span></span> <span data-ttu-id="64632-151">Determine si el servicio se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="64632-151">Determine whether the service is running.</span></span>

<span data-ttu-id="64632-152">Asegúrese de que la configuración de directiva de grupo MBAM se aplica en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="64632-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="64632-153">Si la configuración de directiva de grupo se aplicó en el equipo cliente, se crea la siguiente subclave del registro: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="64632-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="64632-154">Compruebe que esta clave existe y se rellena mediante valores por configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="64632-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="64632-155">Agente de MBAM en el período de demora inicial</span><span class="sxs-lookup"><span data-stu-id="64632-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="64632-156">El cliente de MBAM no inicia la operación inmediatamente después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="64632-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="64632-157">Hay un retraso aleatorio inicial de 1 a 18 minutos antes de que el agente de MBAM inicie su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="64632-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="64632-158">Además del retraso inicial, se produce un retraso de al menos 90 minutos.</span><span class="sxs-lookup"><span data-stu-id="64632-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="64632-159">(El retraso depende de la configuración de directiva de grupo que se haya configurado para la frecuencia de comprobar el estado del cliente). Por lo tanto, el retraso total antes de que se inicie un cliente es el *Inicio aleatorio*retraso de la  +  *frecuencia de comprobación del cliente*.</span><span class="sxs-lookup"><span data-stu-id="64632-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="64632-160">Si los registros de eventos operativos y de administración están en blanco, el cliente aún no ha iniciado la operación y se encuentra en el período de retraso que se mencionó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64632-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="64632-161">Si desea eludir el retraso, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="64632-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="64632-162">Detenga el servicio del cliente de administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64632-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="64632-163">En la subclave del registro **HKEY_LOCAL_MACHINE \software\microsoft\mbam** , cree el valor del registro **NoStartupDelay** , establezca su tipo en **REG_DWORD**y, a continuación, establezca su valor en **1**.</span><span class="sxs-lookup"><span data-stu-id="64632-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="64632-164">En **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**, establezca los valores de **ClientWakeupFrequency** y **StatusReportingFrequency** en **1**.</span><span class="sxs-lookup"><span data-stu-id="64632-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="64632-165">Estos valores volverán a la configuración original después de que las actualizaciones de la Directiva de grupo estén en el equipo.</span><span class="sxs-lookup"><span data-stu-id="64632-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="64632-166">Inicie el servicio del cliente de administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64632-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="64632-167">Después de iniciar el servicio, si inicia sesión de forma local en el equipo y no se producen errores, debe recibir una solicitud para cifrar el equipo en un minuto.</span><span class="sxs-lookup"><span data-stu-id="64632-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="64632-168">Si no recibe una solicitud, debe revisar los registros del administrador de MBAM para ver si hay alguna entrada de error.</span><span class="sxs-lookup"><span data-stu-id="64632-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="64632-169">El equipo no tiene un dispositivo TPM o el dispositivo TPM no está habilitado en el BIOS</span><span class="sxs-lookup"><span data-stu-id="64632-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="64632-170">Revise el registro de eventos del administrador de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="64632-171">Verá una entrada de evento similar a la siguiente en el registro de eventos de administración de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="64632-172">Abra administración de TPM (TPM. msc) y compruebe si el equipo tiene un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="64632-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="64632-173">Si TPM. msc no muestra un dispositivo, abra el administrador de dispositivos (devmgmt. msc) y compruebe si hay un módulo de plataforma de confianza en dispositivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="64632-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="64632-174">Si no ves un dispositivo módulo de plataforma segura, esto puede deberse a una de las siguientes razones:</span><span class="sxs-lookup"><span data-stu-id="64632-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="64632-175">El sistema no tiene un dispositivo de módulo de plataforma segura (TPM o seguridad).</span><span class="sxs-lookup"><span data-stu-id="64632-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="64632-176">El dispositivo TPM está deshabilitado en el BIOS.</span><span class="sxs-lookup"><span data-stu-id="64632-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="64632-177">El dispositivo TPM está habilitado en el BIOS, pero la administración del dispositivo TPM de la configuración del sistema operativo está deshabilitada en el BIOS.</span><span class="sxs-lookup"><span data-stu-id="64632-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="64632-178">No está usando un controlador de Microsoft para el dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="64632-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="64632-179">Revise los dispositivos que aparecen en el administrador de dispositivos para identificar el controlador de dispositivo TPM de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64632-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="64632-180">Si el dispositivo TPM no usa el controlador de C:\Windows\System32\tpm.sys, debe actualizar el controlador seleccionando el archivo C:\Windows\Inf\tpm.inf.</span><span class="sxs-lookup"><span data-stu-id="64632-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="64632-181">El equipo no tiene una partición de sistema válida</span><span class="sxs-lookup"><span data-stu-id="64632-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="64632-182">Revise el registro de eventos del administrador de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="64632-183">Verá una entrada de evento similar a la siguiente en el registro de eventos de administración de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="64632-184">BitLocker requiere una partición de sistema para habilitar el cifrado ([cifrado de unidad BitLocker en Windows 7: preguntas más frecuentes](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="64632-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="64632-185">MBAM no crea la partición del sistema automáticamente.</span><span class="sxs-lookup"><span data-stu-id="64632-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="64632-186">Puede usar la utilidad de preparación de unidad BitLocker (bdehdcfg.exe) para crear la partición del sistema y mover los archivos de inicio necesarios.</span><span class="sxs-lookup"><span data-stu-id="64632-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="64632-187">Por ejemplo, puede usar el comando **% WINDIR% \system32\bdeHdCfg.exe-tamaño predeterminado 300-Quiet** para preparar la unidad silenciosamente antes de implementar MBAM para cifrar las unidades.</span><span class="sxs-lookup"><span data-stu-id="64632-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="64632-188">Esto requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="64632-188">This requires a restart.</span></span> <span data-ttu-id="64632-189">También puede crear una secuencia de comandos para la acción si es necesario.</span><span class="sxs-lookup"><span data-stu-id="64632-189">You can also script the action if this is required.</span></span> <span data-ttu-id="64632-190">En el siguiente documento se describe la herramienta de preparación de unidad BitLocker:</span><span class="sxs-lookup"><span data-stu-id="64632-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="64632-191">Descripción de la herramienta de preparación de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="64632-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="64632-192">Las unidades no tienen el formato de un sistema de archivos compatible</span><span class="sxs-lookup"><span data-stu-id="64632-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="64632-193">Consulte el [artículo de TechNet para conocer los requisitos del sistema de archivos para BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span><span class="sxs-lookup"><span data-stu-id="64632-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="64632-194">Conflicto de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="64632-194">Group Policy conflict</span></span>

<span data-ttu-id="64632-195">Verá una entrada de evento similar a la siguiente en el registro de eventos de administración de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="64632-196">Compruebe la configuración de directiva de grupo para asegurarse de que no tiene una configuración conflictiva entre la configuración de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="64632-197">Debe configurar la Directiva de grupo mediante la plantilla MDOP MBAM y no la plantilla cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64632-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="64632-198">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="64632-198">For example:</span></span>

<span data-ttu-id="64632-199">En configuración de cifrado de unidad del sistema operativo, seleccionó TPM como protector y también seleccionó **permitir PIN mejorados para el inicio**.</span><span class="sxs-lookup"><span data-stu-id="64632-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="64632-200">Se trata de una configuración en conflicto porque la protección de TPM solo necesita un PIN.</span><span class="sxs-lookup"><span data-stu-id="64632-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="64632-201">Por lo tanto, debe deshabilitar la configuración de PIN mejorados.</span><span class="sxs-lookup"><span data-stu-id="64632-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="64632-202">Es posible que el usuario haya solicitado una exención</span><span class="sxs-lookup"><span data-stu-id="64632-202">User may have requested an exemption</span></span>

<span data-ttu-id="64632-203">Si habilitó la configuración de directiva configuración del Equipo\plantillas Administrativas\componentes de Components\MDOP MBAM (administración de BitLocker) \Client Management\Configure la Directiva de exención de usuarios, se le ofrecerá a los usuarios la opción de solicitar una exención.</span><span class="sxs-lookup"><span data-stu-id="64632-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="64632-204">De forma predeterminada, si el usuario solicita una exención, la exención será válida durante 7 días y el usuario no recibirá mensajes para cifrar durante este período.</span><span class="sxs-lookup"><span data-stu-id="64632-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="64632-205">(El valor predeterminado se puede aumentar o disminuir durante la configuración de la Directiva). Una vez que haya finalizado el período de exención, se le pedirá que lo Cifre el usuario.</span><span class="sxs-lookup"><span data-stu-id="64632-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="64632-206">Verá la siguiente entrada en el registro de eventos del administrador de MBAM cuando un equipo se encuentra en exención de usuario:</span><span class="sxs-lookup"><span data-stu-id="64632-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="64632-207">Si desea invalidar manualmente la exención de usuario para un equipo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="64632-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="64632-208">Establezca el valor AllowUserExemption en **0** debajo de la siguiente subclave del registro:</span><span class="sxs-lookup"><span data-stu-id="64632-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="64632-209">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="64632-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="64632-210">Elimine todos los valores del registro de la subclave del Registro siguiente, excepto para **AgentVersion**, **EncodedComputerName**e **instalado**:</span><span class="sxs-lookup"><span data-stu-id="64632-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="64632-211">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="64632-212">**Nota:** Debe reiniciar el agente de MBAM para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="64632-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="64632-213">Tenga en cuenta que después de aplicar la Directiva de grupo al equipo, estos valores pueden revertir a su configuración original.</span><span class="sxs-lookup"><span data-stu-id="64632-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="64632-214">Problema de WMI</span><span class="sxs-lookup"><span data-stu-id="64632-214">WMI issue</span></span>

<span data-ttu-id="64632-215">MBAM usa los métodos de la clase win32_encryptablevolume para administrar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64632-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="64632-216">Si este módulo no está registrado o está dañado, el cliente de MBAM no funcionará correctamente y verá la siguiente entrada de evento en el registro de eventos del administrador de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="64632-217">Además, es posible que observe que las directivas de recuperación y de hardware no se aplican con el código de error 0x8007007e.</span><span class="sxs-lookup"><span data-stu-id="64632-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="64632-218">Esto se traduce en "no se pudo encontrar el módulo especificado".</span><span class="sxs-lookup"><span data-stu-id="64632-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="64632-219">Para resolver este problema, debe volver a registrar la clase **win32_encryptablevolume** con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="64632-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="64632-220">Solución de problemas de comunicación del agente de MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="64632-221">Esta sección contiene información para la solución de problemas de los siguientes problemas relacionados con la comunicación del agente de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="64632-222">Dirección URL de servicio MBAM incorrecta</span><span class="sxs-lookup"><span data-stu-id="64632-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="64632-223">Si el valor de MBAM servicio de estado de cumplimiento o servicio de recuperación y hardware es incorrecto, verá una entrada de evento similar a la siguiente en el registro de eventos del administrador de MBAM en el equipo cliente:</span><span class="sxs-lookup"><span data-stu-id="64632-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="64632-224">Compruebe los valores de **KeyRecoveryServiceEndPoint** y **StatusReportingServiceEndpoint** bajo la siguiente subclave del registro en el equipo cliente:</span><span class="sxs-lookup"><span data-stu-id="64632-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="64632-225">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="64632-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="64632-226">De forma predeterminada, la dirección URL de KeyRecoveryServiceEndPoint (MBAM recuperación y el extremo del servicio de hardware) tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="64632-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="64632-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.SVC</span><span class="sxs-lookup"><span data-stu-id="64632-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="64632-228">De forma predeterminada, la dirección URL de StatusReportingServiceEndpoint (MBAM de servicio de informes de estado) tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="64632-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="64632-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.SVC</span><span class="sxs-lookup"><span data-stu-id="64632-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="64632-230">No debe haber espacios en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="64632-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="64632-231">Si la dirección URL del servicio es incorrecta, debe corregir la dirección URL del servicio en la siguiente configuración de directiva de Grupo:</span><span class="sxs-lookup"><span data-stu-id="64632-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="64632-232">**Configuración**  >  del equipo **Directivas**  >  **Plantillas administrativas**  >  **Componentes**  >  de Windows **MDOP MBAM (administración de BitLocker)**  >  **Administración**  >  de clientes **Configurar servicios de MBAM**</span><span class="sxs-lookup"><span data-stu-id="64632-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="64632-233">Problema de conectividad que afecta al servidor de administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="64632-234">El agente de MBAM no podrá enviar actualizaciones a la base de datos si existen problemas de conectividad entre el agente de cliente y el servidor de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="64632-235">En este caso, observará entradas de errores de conectividad en el registro de eventos del administrador de MBAM en el equipo cliente:</span><span class="sxs-lookup"><span data-stu-id="64632-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="64632-236">Comprobaciones básicas:</span><span class="sxs-lookup"><span data-stu-id="64632-236">Basic checks:</span></span>

* <span data-ttu-id="64632-237">Para comprobar la conectividad básica, haga ping al servidor de administración de MBAM por nombre y dirección IP.</span><span class="sxs-lookup"><span data-stu-id="64632-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="64632-238">Compruebe si puede conectarse al sitio web de administración de MBAM o al puerto de servicio mediante telnet o Portqry.</span><span class="sxs-lookup"><span data-stu-id="64632-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="64632-239">Compruebe que el servicio de IIS se está ejecutando en el servidor de supervisión y administración de MBAM y que el servicio Web de MBAM está escuchando en el mismo puerto que está configurado en el equipo cliente de MBAM ( `netstat –ano | find "portnumber"` ).</span><span class="sxs-lookup"><span data-stu-id="64632-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="64632-240">Compruebe que el número de puerto configurado para el sitio web de MBAM está usando IIS Manager (inetmgr).</span><span class="sxs-lookup"><span data-stu-id="64632-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="64632-241">Asegúrese de que el número de puerto es el mismo que el número de puerto en el que está escuchando el cliente.</span><span class="sxs-lookup"><span data-stu-id="64632-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="64632-242">Asegúrese de que otra aplicación no comparta el número de puerto.</span><span class="sxs-lookup"><span data-stu-id="64632-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="64632-243">Por ejemplo, otra aplicación del servidor no debe usar el mismo puerto.</span><span class="sxs-lookup"><span data-stu-id="64632-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="64632-244">Si hay un firewall, asegúrese de que el puerto está abierto en el firewall o en el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="64632-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="64632-245">Si la comunicación entre el cliente y el servidor es segura, asegúrese de que está usando un certificado SSL válido.</span><span class="sxs-lookup"><span data-stu-id="64632-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="64632-246">Compruebe la conectividad de red entre el servidor Web y el servidor de base de datos al que se envían los datos para su inserción.</span><span class="sxs-lookup"><span data-stu-id="64632-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="64632-247">Puede comprobar la conectividad de la base de datos desde el servidor Web con el servidor de base de datos mediante el administrador de orígenes de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="64632-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="64632-248">La información detallada sobre la solución de problemas de conexión de SQL Server está disponible [para solucionar problemas de conexión con el motor de base de datos de SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span><span class="sxs-lookup"><span data-stu-id="64632-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="64632-249">Solución de problemas de conectividad</span><span class="sxs-lookup"><span data-stu-id="64632-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="64632-250">Asegúrese de que la dirección URL de servicio configurada en el cliente es correcta.</span><span class="sxs-lookup"><span data-stu-id="64632-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="64632-251">Copie el valor de la dirección URL de KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) desde el registro y ábralo en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="64632-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="64632-252">De forma similar, copie el valor de la dirección URL para StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) y ábralo en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="64632-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="64632-253">Si no puede ir a la dirección URL desde el equipo cliente, debe probar la conectividad de red básica desde el cliente al servidor que ejecuta IIS.</span><span class="sxs-lookup"><span data-stu-id="64632-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="64632-254">Vea los puntos 1, 2, 3 y 4 de la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="64632-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="64632-255">Además, revise los registros de la aplicación en el servidor de supervisión y administración en busca de errores.</span><span class="sxs-lookup"><span data-stu-id="64632-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="64632-256">Puede realizar un seguimiento de red simultáneo entre el cliente y el servidor, y revisar el seguimiento para determinar la causa de un error de conexión entre el agente del cliente y el servidor de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="64632-257">Si puede ir a las direcciones URL del servicio desde el equipo cliente y se han producido errores de conectividad en los registros de eventos de administración de MBAM, esto puede deberse a un error de conectividad entre el servidor de administración y el servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="64632-258">Si puede examinar correctamente las direcciones URL del servicio y hay conectividad entre el cliente y el servidor que se está ejecutando, IIS está funcionando.</span><span class="sxs-lookup"><span data-stu-id="64632-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="64632-259">Sin embargo, es posible que haya un problema en la comunicación entre el servidor que ejecuta IIS y el servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="64632-260">Es posible que los servicios de MBAM no puedan conectarse al servidor de base de datos debido a un problema de red o a una configuración incorrecta de la cadena de conexión de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="64632-261">Revise los registros de aplicaciones en el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="64632-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="64632-262">Es posible que aparezcan entradas de errores o advertencias de ASP.NET de origen 2.0.50727.0 que se parezcan a la entrada de registro siguiente:</span><span class="sxs-lookup"><span data-stu-id="64632-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="64632-263">Posibles causas</span><span class="sxs-lookup"><span data-stu-id="64632-263">Possible causes</span></span>

##### <span data-ttu-id="64632-264">Causa 1</span><span class="sxs-lookup"><span data-stu-id="64632-264">Cause 1</span></span>

<span data-ttu-id="64632-265">El administrador puede haber especificado un nombre de instancia de base de datos o un nombre de base de datos no válidos durante la instalación de los componentes del servidor de supervisión y administración.</span><span class="sxs-lookup"><span data-stu-id="64632-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="64632-266">Puede comprobar y corregir las cadenas de conexión de la base de datos con la consola de administración de IIS.</span><span class="sxs-lookup"><span data-stu-id="64632-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="64632-267">Para ello, abra el administrador de IIS y vaya a administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64632-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="64632-268">Para cada servicio que aparece en la parte izquierda, siga estos pasos para cambiar las cadenas de conexión de la base de datos:</span><span class="sxs-lookup"><span data-stu-id="64632-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="64632-269">En la **vista características**, seleccione las **cadenas de conexión**.</span><span class="sxs-lookup"><span data-stu-id="64632-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="64632-270">En la página **cadenas de conexión** , seleccione la cadena de conexión que quiere cambiar.</span><span class="sxs-lookup"><span data-stu-id="64632-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="64632-271">En el panel **acciones** , seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="64632-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="64632-272">En el cuadro de diálogo **Editar cadena de conexión** , cambie las propiedades que desee cambiar y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="64632-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="64632-273">Causa 2</span><span class="sxs-lookup"><span data-stu-id="64632-273">Cause 2</span></span>

<span data-ttu-id="64632-274">Puerto de SQL Server bloqueado en el firewall.</span><span class="sxs-lookup"><span data-stu-id="64632-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="64632-275">Compruebe el número de puerto al que está configurado SQL Server para que escuche y asegúrese de que el puerto está abierto en el Firewall entre el servidor de administración y el servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="64632-276">Causa 3</span><span class="sxs-lookup"><span data-stu-id="64632-276">Cause 3</span></span>

<span data-ttu-id="64632-277">Enlaces TCP/IP incorrectos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64632-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="64632-278">Compruebe los enlaces TCP/IP de SQL en el administrador de configuración de SQL Server en el servidor de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="64632-279">MBAM requiere que los protocolos TCP/IP y las canalizaciones con nombre estén habilitados para conectarse a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="64632-280">Causa 4</span><span class="sxs-lookup"><span data-stu-id="64632-280">Cause 4</span></span>

<span data-ttu-id="64632-281">La cuenta de equipo del servidor NT Authority\Network Service o de la administración de MBAM no tiene los permisos necesarios para conectarse a la base de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="64632-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="64632-282">Durante la instalación de los componentes de base de datos en el servidor de base de datos, el instalador crea dos grupos locales: MBAM de cumplimiento de la auditoría de cumplimiento y MBAM recuperación y acceso de BD de hardware.</span><span class="sxs-lookup"><span data-stu-id="64632-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="64632-283">La cuenta NT Authority\Network Service, la cuenta de equipo del servidor de administración de MBAM y el usuario que instala los componentes de base de datos se agregan automáticamente a estos grupos.</span><span class="sxs-lookup"><span data-stu-id="64632-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="64632-284">A estos grupos se les conceden los permisos necesarios en la base de datos durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="64632-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="64632-285">Todos los usuarios que forman parte de este grupo reciben automáticamente los permisos necesarios en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="64632-286">El servicio Web no puede conectarse al servidor de base de datos debido a un problema de permisos si se cumplen una o varias de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="64632-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="64632-287">Los grupos mencionados anteriormente se quitan de los grupos locales en el servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="64632-288">La cuenta NT Authority\Network Service y la cuenta de equipo del servidor de administración de MBAM no son miembros de estos grupos.</span><span class="sxs-lookup"><span data-stu-id="64632-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="64632-289">Estos grupos no tienen los permisos necesarios en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="64632-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="64632-290">Observará errores relacionados con los permisos en los registros de aplicaciones en el servidor de supervisión y administración de MBAM si se cumple alguna de las condiciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="64632-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="64632-291">En ese caso, debe agregar manualmente la cuenta NT Authority\Network Service y la cuenta de equipo del servidor de administración de MBAM y concederles una función pública para todo el servidor en el servidor de bases de datos SQL que usa SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="64632-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="64632-292">Revisar los registros del servicio Web</span><span class="sxs-lookup"><span data-stu-id="64632-292">Review the web service logs</span></span>

<span data-ttu-id="64632-293">Si no hay eventos registrados en los registros de aplicaciones del servidor de administración de MBAM, es el momento de revisar los registros de servicio Web (. svclog) del servicio Web de MBAM que se hospeda en el servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="64632-294">Para ver el archivo de registro, tendrá que usar la herramienta Service Trace Viewer (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .</span><span class="sxs-lookup"><span data-stu-id="64632-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="64632-295">Debe investigar principalmente los registros de seguimiento de servicios de RecoveryandHardwareService y ComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="64632-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="64632-296">De forma predeterminada, los registros del servicio Web se encuentran en la C:\inetpub\Microsoft de administración de BitLocker de Solution\Logs.</span><span class="sxs-lookup"><span data-stu-id="64632-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="64632-297">Allí, cada servicio escribe el archivo. svclog en su propia carpeta.</span><span class="sxs-lookup"><span data-stu-id="64632-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="64632-298">Revise la actividad en el registro de seguimiento del servicio para comprobar si hay errores o advertencias.</span><span class="sxs-lookup"><span data-stu-id="64632-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="64632-299">De forma predeterminada, las entradas de error se resaltan en rojo.</span><span class="sxs-lookup"><span data-stu-id="64632-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="64632-300">Seleccione la descripción del error en el panel derecho del visor de seguimiento para ver información detallada sobre la entrada de error.</span><span class="sxs-lookup"><span data-stu-id="64632-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="64632-301">A continuación se muestra un error de la entrada del registro de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="64632-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="64632-302">Reinstalación o reconfiguración de la infraestructura de MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="64632-303">Para reinstalar o volver a configurar la infraestructura de MBAM, debe conocer las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="64632-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="64632-304">Cuenta del grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64632-304">Application Pool account</span></span>

* <span data-ttu-id="64632-305">Grupos MBAM (Departamento de soporte técnico, avanzado, grupo de usuarios de informes)</span><span class="sxs-lookup"><span data-stu-id="64632-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="64632-306">URL de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="64632-306">MBAM Reports URL</span></span>

* <span data-ttu-id="64632-307">Nombre de servidor SQL Server y nombres de bases de datos</span><span class="sxs-lookup"><span data-stu-id="64632-307">SQL Server name and database names</span></span>

* <span data-ttu-id="64632-308">Cuentas de MBAM ReadWrite y ReadOnly</span><span class="sxs-lookup"><span data-stu-id="64632-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="64632-309">Cuenta del grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64632-309">Application Pool account</span></span>

<span data-ttu-id="64632-310">Para encontrar la cuenta del grupo de aplicaciones, inicie sesión en el servidor Web de MBAM, Abra **Administrador de Internet Information Services (IIS)** y, a continuación, seleccione **grupos de aplicaciones**:</span><span class="sxs-lookup"><span data-stu-id="64632-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![grupos de aplicaciones](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="64632-312">El nombre principal de servicio (SPN) debe establecerse en esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="64632-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="64632-313">Esta configuración es muy importante para la funcionalidad de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="64632-314">Grupos MBAM (soporte, avanzado, grupo de usuarios de informes e URL de informes)</span><span class="sxs-lookup"><span data-stu-id="64632-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![Grupos de MBAM](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="64632-316">Proporciona información como, por ejemplo, grupo de soporte técnico, grupo avanzado de Helpdesk, grupo de usuarios de informes y URL de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="64632-317">La dirección URL de los informes de MBAM debe proporcionarse en la configuración de MBAM y debe ser: http (s)://servername/ReportServer.</span><span class="sxs-lookup"><span data-stu-id="64632-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="64632-318">Nombre de SQL Server y nombres de base de datos (DB)</span><span class="sxs-lookup"><span data-stu-id="64632-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="64632-319">Para encontrar los nombres e instancias de SQL Server que hospedan las DBs de MBAM, inicie sesión en el servidor Web de MBAM (IIS) y vaya a la siguiente subclave del registro:</span><span class="sxs-lookup"><span data-stu-id="64632-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="64632-320">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web</span><span class="sxs-lookup"><span data-stu-id="64632-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="64632-322">Las partes resaltadas son cadenas de conexión.</span><span class="sxs-lookup"><span data-stu-id="64632-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="64632-323">Deben tener el nombre del servidor SQL, los nombres de base de datos e instancias (si tiene nombre).</span><span class="sxs-lookup"><span data-stu-id="64632-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="64632-324">Cuentas de MBAM ReadWrite y ReadOnly</span><span class="sxs-lookup"><span data-stu-id="64632-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="64632-325">Esta información estará en la base de datos de SQL Server, en la que ya encontramos el nombre del servidor Web.</span><span class="sxs-lookup"><span data-stu-id="64632-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="64632-326">Cuenta ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64632-326">ReadWrite account</span></span>

1. <span data-ttu-id="64632-327">Inicie sesión en SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="64632-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="64632-328">Haga clic con el botón secundario en **MBAM recuperación y hardware**, seleccione **propiedades**y, a continuación, seleccione **permisos**.</span><span class="sxs-lookup"><span data-stu-id="64632-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="64632-329">Por ejemplo, el nombre de la cuenta de laboratorio es **MBAMWrite**.</span><span class="sxs-lookup"><span data-stu-id="64632-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="64632-330">El grupo de aplicaciones y las cuentas ReadWrite se configuran para ser iguales.</span><span class="sxs-lookup"><span data-stu-id="64632-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![BD DE SQL](images/troubleshooting-MBAM-installation-4.png)

![Propiedades de BD](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="64632-333">Vaya a **seguridad** y, a continuación, **inicie sesión** en SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="64632-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="64632-334">Vaya a la cuenta que se muestra en la captura de pantalla anterior.</span><span class="sxs-lookup"><span data-stu-id="64632-334">Browse to the account shown in the previous screenshot.</span></span>

![Seguridad de SQL](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="64632-336">Haga clic con el botón derecho en las cuentas, vaya a **asignación de usuarios de propiedades**y busque la base de datos de recuperación y hardware de MBAM:</span><span class="sxs-lookup"><span data-stu-id="64632-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![Asignación de usuarios](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="64632-338">Cuenta de solo lectura</span><span class="sxs-lookup"><span data-stu-id="64632-338">ReadOnly account</span></span>

<span data-ttu-id="64632-339">Abra el administrador de configuración de SQL Server Reporting Services en el servidor SSRS.</span><span class="sxs-lookup"><span data-stu-id="64632-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="64632-340">Seleccione **URL del administrador de informes**y, a continuación, examine las **direcciones URL**:</span><span class="sxs-lookup"><span data-stu-id="64632-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![Administrador de informes](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="64632-342">Seleccione **Administración y supervisión de Microsoft BitLocker**:</span><span class="sxs-lookup"><span data-stu-id="64632-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![Administración y supervisión de BitLocker](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="64632-344">Seleccione **MaltaDatasource**:</span><span class="sxs-lookup"><span data-stu-id="64632-344">Select **MaltaDatasource**:</span></span>

![Bases](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="64632-347">MaltaDataSource debe tener el nombre de cuenta ReadOnly y debe usarse en la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="64632-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="64632-348">Referencia</span><span class="sxs-lookup"><span data-stu-id="64632-348">Reference</span></span>

<span data-ttu-id="64632-349">Para obtener más información, consulta los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="64632-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="64632-350">Implementar MBAM 2,5 en una configuración independiente</span><span class="sxs-lookup"><span data-stu-id="64632-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="64632-351">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="64632-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
