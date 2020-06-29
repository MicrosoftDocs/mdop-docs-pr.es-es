---
title: Cómo implementar al cliente MBAM como parte de una implementación de Windows
description: Cómo implementar al cliente MBAM como parte de una implementación de Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824911"
---
# <span data-ttu-id="02f40-103">Cómo implementar al cliente MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="02f40-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="02f40-104">El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="02f40-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="02f40-105">El cliente de BitLocker se puede integrar en una organización al habilitar el cifrado y la administración de BitLocker en equipos cliente durante el proceso de creación de imágenes de equipos y de Windows.</span><span class="sxs-lookup"><span data-stu-id="02f40-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="02f40-106">Nota</span><span class="sxs-lookup"><span data-stu-id="02f40-106">Note</span></span>**  
<span data-ttu-id="02f40-107">Para consultar los requisitos del sistema del cliente de MBAM, consulte [configuraciones compatibles con MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="02f40-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="02f40-108">El cifrado de equipos cliente con BitLocker durante la fase de creación de imágenes inicial de una implementación de Windows puede reducir la sobrecarga administrativa de la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02f40-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="02f40-109">Este enfoque también garantiza que todos los equipos que se implementan ya tengan BitLocker ejecutándose y que estén configurados correctamente.</span><span class="sxs-lookup"><span data-stu-id="02f40-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="02f40-110">Advertencia</span><span class="sxs-lookup"><span data-stu-id="02f40-110">Warning</span></span>**  
<span data-ttu-id="02f40-111">En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="02f40-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="02f40-112">Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="02f40-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="02f40-113">Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro.</span><span class="sxs-lookup"><span data-stu-id="02f40-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="02f40-114">Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver.</span><span class="sxs-lookup"><span data-stu-id="02f40-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="02f40-115">Cambie el registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="02f40-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="02f40-116">Para cifrar un equipo como parte de la implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="02f40-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="02f40-117">Si su organización planea usar el protector módulo de plataforma segura (TPM) o las opciones de protector de TPM + PIN en BitLocker, debe activar el chip TPM antes de la implementación inicial de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02f40-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="02f40-118">Al activar el chip de TPM, se evita el reinicio más adelante en el proceso y se asegura de que los chips de TPM se hayan configurado correctamente de acuerdo con los requisitos de la organización.</span><span class="sxs-lookup"><span data-stu-id="02f40-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="02f40-119">Debe activar el chip TPM manualmente en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="02f40-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="02f40-120">Para obtener más información sobre cómo configurar el chip de TPM, consulte la documentación del fabricante.</span><span class="sxs-lookup"><span data-stu-id="02f40-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="02f40-121">Instale el agente de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02f40-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="02f40-122">Le recomendamos que se una al equipo a un dominio...</span><span class="sxs-lookup"><span data-stu-id="02f40-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="02f40-123">Si el equipo no se ha unido a un dominio, la contraseña de recuperación no se almacena en el servicio de recuperación de claves de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02f40-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="02f40-124">De forma predeterminada, MBAM no permite que se produzca el cifrado, a menos que se pueda almacenar la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="02f40-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="02f40-125">Si un equipo se inicia en el modo de recuperación antes de que se almacene la clave de recuperación en el servidor de MBAM, el equipo tiene que recrear la imagen.</span><span class="sxs-lookup"><span data-stu-id="02f40-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="02f40-126">No hay ningún método de recuperación disponible.</span><span class="sxs-lookup"><span data-stu-id="02f40-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="02f40-127">Abra un símbolo del sistema como administrador, detenga el servicio MBAM y, a continuación, configure el servicio como **manual** o a **petición**.</span><span class="sxs-lookup"><span data-stu-id="02f40-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="02f40-128">A continuación, ejecute los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="02f40-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="02f40-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="02f40-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="02f40-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="02f40-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="02f40-131">Establezca la configuración del registro para que el agente de MBAM ignore la Directiva de grupo y ejecute el TPM para el **cifrado solo del sistema operativo** para ello, ejecute **regedit**y, a continuación, importe la plantilla de clave del registro de c:\\Archivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="02f40-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="02f40-132">En regedit, vaya a HKLM\\SOFTWARE\\Microsoft\\MBAM y configure las opciones que se indican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="02f40-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="02f40-133">Entrada del registro</span><span class="sxs-lookup"><span data-stu-id="02f40-133">Registry entry</span></span>

    <span data-ttu-id="02f40-134">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="02f40-134">Configuration settings</span></span>

    <span data-ttu-id="02f40-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="02f40-135">DeploymentTime</span></span>

    <span data-ttu-id="02f40-136">0 = DESHABILITADO</span><span class="sxs-lookup"><span data-stu-id="02f40-136">0 = OFF</span></span>

    <span data-ttu-id="02f40-137">1 = usar la configuración de directiva de tiempo de implementación (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="02f40-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="02f40-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="02f40-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="02f40-139">0 = no usar custodia de claves (en este caso, no se necesitan las dos siguientes entradas de registro).</span><span class="sxs-lookup"><span data-stu-id="02f40-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="02f40-140">1 = usar custodia de clave en el sistema de recuperación de claves (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="02f40-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="02f40-141">Recomendado: el equipo debe poder comunicarse con el servicio de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="02f40-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="02f40-142">Compruebe que el equipo puede comunicarse con el servicio antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="02f40-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="02f40-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="02f40-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="02f40-144">0 = cargar solo la clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="02f40-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="02f40-145">1 = cargar la clave de recuperación y el paquete de recuperación de claves (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="02f40-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="02f40-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="02f40-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="02f40-147">Establezca este valor en la dirección URL del servidor Web de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="02f40-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="02f40-148">Ejemplo: http:// &lt; nombre de equipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC.</span><span class="sxs-lookup"><span data-stu-id="02f40-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="02f40-149">El agente de MBAM reinicia el sistema durante la implementación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02f40-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="02f40-150">Cuando esté listo para este reinicio, ejecute el comando siguiente en un símbolo del sistema como administrador:</span><span class="sxs-lookup"><span data-stu-id="02f40-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="02f40-151">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="02f40-151">net start mbamagent</span></span>**

8. <span data-ttu-id="02f40-152">Cuando se reinicien los equipos y el BIOS le solicite que acepte un cambio de TPM, acepte el cambio.</span><span class="sxs-lookup"><span data-stu-id="02f40-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="02f40-153">Durante el proceso de creación de imágenes del sistema operativo de cliente Windows, cuando esté listo para iniciar el cifrado, reinicie el servicio agente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02f40-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="02f40-154">Después, para establecer Inicio en **automático**, abra un símbolo del sistema como administrador y ejecute los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="02f40-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="02f40-155">SC config mbamagent Start = Auto</span><span class="sxs-lookup"><span data-stu-id="02f40-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="02f40-156">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="02f40-156">net start mbamagent</span></span>**

10. <span data-ttu-id="02f40-157">Quite los valores de omisión del registro.</span><span class="sxs-lookup"><span data-stu-id="02f40-157">Remove the bypass registry values.</span></span> <span data-ttu-id="02f40-158">Para ello, ejecute regedit, vaya a la entrada del registro HKLM\\SOFTWARE\\Microsoft, haga clic con el botón secundario en el nodo **MBAM** y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="02f40-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="02f40-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02f40-159">Related topics</span></span>


[<span data-ttu-id="02f40-160">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02f40-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









