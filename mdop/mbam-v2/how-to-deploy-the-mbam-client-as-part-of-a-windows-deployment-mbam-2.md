---
title: Cómo implementar al cliente MBAM como parte de una implementación de Windows
description: Cómo implementar al cliente MBAM como parte de una implementación de Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824621"
---
# <span data-ttu-id="ecf53-103">Cómo implementar al cliente MBAM como parte de una implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="ecf53-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="ecf53-104">El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ecf53-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="ecf53-105">Si los equipos tienen un chip de módulo de plataforma segura (TPM), el cliente de BitLocker se puede integrar en una organización habilitando la administración de BitLocker y el cifrado en los equipos cliente como parte del proceso de implementación de imágenes y ventanas.</span><span class="sxs-lookup"><span data-stu-id="ecf53-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="ecf53-106">Nota</span><span class="sxs-lookup"><span data-stu-id="ecf53-106">Note</span></span>**  
<span data-ttu-id="ecf53-107">Para revisar los requisitos del sistema cliente de administración y supervisión de Microsoft BitLocker, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ecf53-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="ecf53-108">El cifrado de equipos cliente con BitLocker durante la fase inicial de creación de la imagen de una implementación de Windows puede reducir el overhead administrativo necesario para implementar MBAM en una organización.</span><span class="sxs-lookup"><span data-stu-id="ecf53-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="ecf53-109">También garantiza que todos los equipos que se implementan ya tengan BitLocker ejecutándose y que estén configurados correctamente.</span><span class="sxs-lookup"><span data-stu-id="ecf53-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="ecf53-110">Nota</span><span class="sxs-lookup"><span data-stu-id="ecf53-110">Note</span></span>**  
<span data-ttu-id="ecf53-111">En el procedimiento de este tema se describe cómo modificar el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="ecf53-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="ecf53-112">El uso incorrecto del editor del registro puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="ecf53-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="ecf53-113">Microsoft no puede garantizar la solución de los problemas resultantes del uso incorrecto del editor del registro.</span><span class="sxs-lookup"><span data-stu-id="ecf53-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="ecf53-114">Use el editor del registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="ecf53-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="ecf53-115">Para cifrar un equipo como parte de la implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="ecf53-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="ecf53-116">Si su organización planea usar el protector módulo de plataforma segura (TPM) o las opciones de protector de TPM + PIN en BitLocker, debe activar el chip TPM antes de la implementación inicial de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ecf53-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="ecf53-117">Al activar el chip de TPM, se evita el reinicio más adelante en el proceso y se asegura de que los chips de TPM se hayan configurado correctamente de acuerdo con los requisitos de la organización.</span><span class="sxs-lookup"><span data-stu-id="ecf53-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="ecf53-118">Debe activar el chip TPM manualmente en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="ecf53-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="ecf53-119">Nota</span><span class="sxs-lookup"><span data-stu-id="ecf53-119">Note</span></span>**  
    <span data-ttu-id="ecf53-120">Algunos proveedores proporcionan herramientas para activar y activar el chip TPM en el BIOS desde el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ecf53-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="ecf53-121">Para obtener más información sobre cómo configurar el chip de TPM, consulte la documentación del fabricante.</span><span class="sxs-lookup"><span data-stu-id="ecf53-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="ecf53-122">Instale el agente del cliente de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ecf53-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="ecf53-123">Unir el equipo a un dominio (recomendado).</span><span class="sxs-lookup"><span data-stu-id="ecf53-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="ecf53-124">Si el equipo no se une al dominio, la contraseña de recuperación no se almacena en el servicio de recuperación de claves de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ecf53-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="ecf53-125">De forma predeterminada, MBAM no permite que se produzca el cifrado, a menos que se pueda almacenar la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ecf53-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="ecf53-126">Si un equipo se inicia en el modo de recuperación antes de que se almacene la clave de recuperación en el servidor de MBAM, el equipo tiene que recrear la imagen.</span><span class="sxs-lookup"><span data-stu-id="ecf53-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="ecf53-127">No hay ningún método de recuperación disponible.</span><span class="sxs-lookup"><span data-stu-id="ecf53-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="ecf53-128">Ejecute el símbolo del sistema como administrador, detenga el servicio MBAM y, a continuación, establezca el servicio en **manual** o a **petición**y, a continuación, empiece a escribir los comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ecf53-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="ecf53-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="ecf53-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="ecf53-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="ecf53-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="ecf53-131">Establezca la configuración del registro para que el agente de MBAM ignore la Directiva de grupo y ejecute el TPM para el **cifrado solo del sistema operativo** ejecutando **regedit**y, a continuación, importando la plantilla de clave del registro de c:\\Archivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="ecf53-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="ecf53-132">En regedit, vaya a HKLM\\SOFTWARE\\Microsoft\\MBAM y configure las opciones que se indican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ecf53-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="ecf53-133">Entrada del registro</span><span class="sxs-lookup"><span data-stu-id="ecf53-133">Registry entry</span></span>

    <span data-ttu-id="ecf53-134">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="ecf53-134">Configuration settings</span></span>

    <span data-ttu-id="ecf53-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="ecf53-135">DeploymentTime</span></span>

    <span data-ttu-id="ecf53-136">0 = DESHABILITADO</span><span class="sxs-lookup"><span data-stu-id="ecf53-136">0 = OFF</span></span>

    <span data-ttu-id="ecf53-137">1 = usar la configuración de directiva de tiempo de implementación (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="ecf53-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="ecf53-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="ecf53-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="ecf53-139">0 = no usar custodia de claves (en este caso, no se necesitan las dos siguientes entradas de registro)</span><span class="sxs-lookup"><span data-stu-id="ecf53-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="ecf53-140">1 = usar custodia de clave en el sistema de recuperación de claves (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="ecf53-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="ecf53-141">Recomendado: el equipo debe poder comunicarse con el servicio de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="ecf53-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="ecf53-142">Compruebe que el equipo puede comunicarse con el servicio antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="ecf53-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="ecf53-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="ecf53-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="ecf53-144">0 = solo carga la clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="ecf53-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="ecf53-145">1 = carga de clave de recuperación y paquete de recuperación de claves (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="ecf53-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="ecf53-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="ecf53-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="ecf53-147">Establezca este valor en la dirección URL del servidor Web de recuperación de claves, por ejemplo, http:// &lt; nombre de equipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC.</span><span class="sxs-lookup"><span data-stu-id="ecf53-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="ecf53-148">El agente de MBAM reinicia el sistema durante la implementación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ecf53-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="ecf53-149">Cuando esté listo para este reinicio, ejecute el comando siguiente en un símbolo del sistema como administrador:</span><span class="sxs-lookup"><span data-stu-id="ecf53-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="ecf53-150">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="ecf53-150">net start mbamagent</span></span>**

8. <span data-ttu-id="ecf53-151">Cuando se reinicien los equipos y el BIOS le solicite que acepte un cambio de TPM, acepte el cambio.</span><span class="sxs-lookup"><span data-stu-id="ecf53-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="ecf53-152">Durante el proceso de creación de imágenes del sistema operativo de cliente Windows, cuando esté listo para iniciar el cifrado, reinicie el servicio agente de MBAM y establezca iniciar en **automático** ejecutando un símbolo del sistema como administrador y escribiendo los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="ecf53-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="ecf53-153">SC config mbamagent Start = Auto</span><span class="sxs-lookup"><span data-stu-id="ecf53-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="ecf53-154">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="ecf53-154">net start mbamagent</span></span>**

10. <span data-ttu-id="ecf53-155">Para quitar los valores de omisión del registro, ejecute regedit y vaya a la entrada del registro HKLM\\SOFTWARE\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ecf53-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="ecf53-156">Para eliminar el nodo **MBAM** , haga clic con el botón secundario en el nodo y haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="ecf53-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="ecf53-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ecf53-157">Related topics</span></span>


[<span data-ttu-id="ecf53-158">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ecf53-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









