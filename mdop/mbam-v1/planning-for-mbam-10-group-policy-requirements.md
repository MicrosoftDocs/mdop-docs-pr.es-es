---
title: Planificación de los requisitos de directiva de grupo de MBAM 1.0
description: Planificación de los requisitos de directiva de grupo de MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812438"
---
# <span data-ttu-id="8578d-103">Planificación de los requisitos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8578d-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="8578d-104">Administración de clientes de Microsoft BitLocker Administration and Monitoring (MBAM) requiere que se aplique una configuración de directiva de grupo personalizada.</span><span class="sxs-lookup"><span data-stu-id="8578d-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="8578d-105">En este tema se describen las opciones de directiva disponibles para el objeto de directiva de grupo (GPO) cuando usa MBAM para administrar el cifrado de unidad BitLocker en la empresa.</span><span class="sxs-lookup"><span data-stu-id="8578d-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="8578d-106">Importante</span><span class="sxs-lookup"><span data-stu-id="8578d-106">Important</span></span>**  
<span data-ttu-id="8578d-107">MBAM no usa la configuración de GPO predeterminada para el cifrado de unidad BitLocker de Windows.</span><span class="sxs-lookup"><span data-stu-id="8578d-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="8578d-108">Si la configuración predeterminada está habilitada, se puede producir un comportamiento conflictivo.</span><span class="sxs-lookup"><span data-stu-id="8578d-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="8578d-109">Para habilitar MBAM para administrar BitLocker, debe definir la configuración de directiva de GPO después de instalar la plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="8578d-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="8578d-110">Después de instalar la plantilla de directiva de grupo MBAM, puede ver y modificar la configuración de directiva de GPO de MBAM personalizada que permite a MBAM administrar el cifrado de BitLocker de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8578d-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="8578d-111">La plantilla de directiva de grupo MBAM debe instalarse en un equipo que sea capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la tecnología de MDOP de administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="8578d-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="8578d-112">A continuación, para editar el objeto de directiva de grupo aplicable, abra la GPMC o AGPM y, a continuación, vaya al nodo GPO siguiente: **configuración del equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="8578d-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="8578d-113">El nodo de GPO MBAM de MDOP (administración de BitLocker) contiene cuatro parámetros de directiva global y cuatro nodos de configuración de GPO secundarios, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8578d-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="8578d-114">Los cuatro parámetros de configuración de directiva global de GPO son: administración de clientes, unidad fija, unidad de sistema operativo y unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="8578d-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="8578d-115">En las siguientes secciones se proporcionan definiciones de directiva y sugerencias de configuración de directivas para ayudarle a planear los requisitos de configuración de directiva de GPO MBAM.</span><span class="sxs-lookup"><span data-stu-id="8578d-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="8578d-116">Nota</span><span class="sxs-lookup"><span data-stu-id="8578d-116">Note</span></span>**  
<span data-ttu-id="8578d-117">Para obtener más información sobre cómo configurar las opciones mínimas de GPO sugeridas para habilitar MBAM para administrar el cifrado de BitLocker, consulte [Cómo editar la configuración de GPO de MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8578d-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="8578d-118">Definiciones de directiva global</span><span class="sxs-lookup"><span data-stu-id="8578d-118">Global policy definitions</span></span>


<span data-ttu-id="8578d-119">En esta sección se describen las definiciones de la directiva global MBAM, que se pueden encontrar en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="8578d-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8578d-120">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8578d-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="8578d-121">Información general y sugerencia de configuración de directivas</span><span class="sxs-lookup"><span data-stu-id="8578d-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-122">Elija el método de cifrado de unidad y la intensidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="8578d-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-123">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-124">Configure esta directiva para usar un método de cifrado específico y la intensidad de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8578d-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="8578d-125">Cuando esta Directiva no está configurada, BitLocker usa el método de cifrado predeterminado de AES 128 bits con difusor o el método de cifrado especificado por el script de configuración.</span><span class="sxs-lookup"><span data-stu-id="8578d-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-126">Evitar la sobrescritura de memoria al reiniciar</span><span class="sxs-lookup"><span data-stu-id="8578d-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-127">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-128">Configure esta directiva para mejorar el rendimiento de reinicio sin sobrescribir los secretos de BitLocker en memoria al reiniciar.</span><span class="sxs-lookup"><span data-stu-id="8578d-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="8578d-129">Cuando esta Directiva no está configurada, los secretos de BitLocker se quitan de la memoria cuando se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="8578d-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-130">Validar regla de uso de certificados de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="8578d-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-131">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-132">Configure esta directiva para usar la protección de BitLocker basada en certificados de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="8578d-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="8578d-133">Cuando esta Directiva no está configurada, se usa un identificador de objeto predeterminado 1.3.6.1.4.1.311.67.1.1 para especificar un certificado.</span><span class="sxs-lookup"><span data-stu-id="8578d-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-134">Proporcionar los identificadores únicos para la organización</span><span class="sxs-lookup"><span data-stu-id="8578d-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-135">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-136">Configure esta directiva para usar un agente de recuperación de datos basado en certificados o el lector de BitLocker To Go.</span><span class="sxs-lookup"><span data-stu-id="8578d-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="8578d-137">Cuando esta Directiva no está configurada <strong> , </strong> no se usa el campo de identificación.</span><span class="sxs-lookup"><span data-stu-id="8578d-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="8578d-138">Si su empresa requiere medidas de seguridad mayores, es posible que desee configurar el <strong> campo de identificación para asegurarse de </strong> que todos los dispositivos USB tienen este conjunto de campos y que están alineados con esta configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8578d-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8578d-139">Definiciones de directivas de administración de clientes</span><span class="sxs-lookup"><span data-stu-id="8578d-139">Client Management policy definitions</span></span>


<span data-ttu-id="8578d-140">En esta sección se describen las definiciones de directiva de administración de clientes para MBAM, que se encuentran en el siguiente nodo GPO: **configuración de equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**  \\  **Administración de clientes**.</span><span class="sxs-lookup"><span data-stu-id="8578d-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8578d-141">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8578d-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="8578d-142">Información general y sugerencias de configuración de directivas</span><span class="sxs-lookup"><span data-stu-id="8578d-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-143">Configurar servicios de MBAM</span><span class="sxs-lookup"><span data-stu-id="8578d-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-144">Configuración sugerida: <strong> habilitado</span><span class="sxs-lookup"><span data-stu-id="8578d-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="8578d-145">Extremo de servicio de hardware y recuperación de MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="8578d-146">Esta es la primera opción de directiva que debe configurar para habilitar la administración del cifrado de BitLocker en el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8578d-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="8578d-147">Para esta configuración, escriba la ubicación del extremo de forma similar al siguiente ejemplo: <strong> http:// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; Puerto el servicio web está enlazado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.SVC </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="8578d-148">Seleccione la información de recuperación de BitLocker para almacenar </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="8578d-149">Esta configuración de directiva le permite configurar el servicio de recuperación de claves para realizar una copia de seguridad de la información de recuperación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="8578d-150">También le permite configurar el servicio de informes de estado para recopilar informes de cumplimiento y cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="8578d-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="8578d-151">La Directiva proporciona un método administrativo para recuperar datos cifrados con BitLocker para ayudar a evitar la pérdida de datos a causa de la falta de información clave.</span><span class="sxs-lookup"><span data-stu-id="8578d-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="8578d-152">El informe de estado y la actividad de recuperación de claves se enviarán de forma automática y silencio a la ubicación del servidor de informes configurado.</span><span class="sxs-lookup"><span data-stu-id="8578d-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="8578d-153">Si no configura o si deshabilita esta configuración de Directiva, la información de recuperación de clave no se guardará y no se notificará al servidor la actividad de recuperación de clave y el informe de estado.</span><span class="sxs-lookup"><span data-stu-id="8578d-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="8578d-154">Cuando esta opción se establece en <strong> contraseña de recuperación y paquete de claves </strong> , la contraseña de recuperación y el paquete de claves se copian automáticamente en la ubicación del servidor de recuperación de claves configurado.</span><span class="sxs-lookup"><span data-stu-id="8578d-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="8578d-155">Escriba la frecuencia de estado de comprobación del cliente en minutos </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="8578d-156">Esta configuración de directiva administra la frecuencia con la que el cliente comprueba las directivas de protección de BitLocker y el estado en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="8578d-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="8578d-157">Esta Directiva también administra la frecuencia con la que se guarda el estado de cumplimiento del cliente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8578d-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="8578d-158">El cliente comprueba el estado y las directivas de protección de BitLocker en el equipo cliente, y también realiza una copia de seguridad de la clave de recuperación del cliente a la frecuencia configurada.</span><span class="sxs-lookup"><span data-stu-id="8578d-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="8578d-159">Establezca esta frecuencia según el requisito establecido por su empresa sobre la frecuencia con la que comprobar el estado de cumplimiento del equipo y la frecuencia con la que se realiza la copia de seguridad de la clave de recuperación del cliente.</span><span class="sxs-lookup"><span data-stu-id="8578d-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="8578d-160">Extremo del servicio de informes de estado de MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="8578d-161">Esta es la configuración de la Directiva segunda que debe configurar para habilitar la administración del cifrado de BitLocker en el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8578d-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="8578d-162">Para esta configuración, escriba la ubicación del extremo mediante el siguiente ejemplo: <strong> http:// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; Puerto al que está enlazado el servicio Web &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.</span><span class="sxs-lookup"><span data-stu-id="8578d-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="8578d-163">SVC </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-164">Permitir la comprobación de compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="8578d-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-165">Configuración sugerida: <strong> habilitado</span><span class="sxs-lookup"><span data-stu-id="8578d-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="8578d-166">Esta configuración de directiva le permite administrar la comprobación de la compatibilidad del hardware antes de habilitar la protección de BitLocker en las unidades de los equipos cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8578d-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="8578d-167">Debe habilitar esta opción de Directiva si su empresa tiene hardware o equipos antiguos que no son compatibles con el módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="8578d-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="8578d-168">Si alguno de estos criterios es verdadero, habilite la comprobación de compatibilidad de hardware para asegurarse de que MBAM se aplica solo a los modelos de equipo que son compatibles con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="8578d-169">Si todos los equipos de su organización son compatibles con BitLocker, no tiene que implementar la compatibilidad de hardware y puede establecer esta directiva en <strong> no configurado </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="8578d-170">Si habilita esta configuración de Directiva, el modelo del equipo se validará en la lista de compatibilidad de hardware una vez cada 24 horas, antes de que la Directiva habilite la protección de BitLocker en una unidad de equipo.</span><span class="sxs-lookup"><span data-stu-id="8578d-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8578d-171">Nota</span><span class="sxs-lookup"><span data-stu-id="8578d-171">Note</span></span></strong><br/><p><span data-ttu-id="8578d-172">Antes de habilitar esta configuración de Directiva, asegúrese de que ha configurado la <strong> configuración de extremo del servicio de recuperación y hardware </strong> de MBAM en las <strong> Opciones de directiva configurar servicios de MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8578d-173">Si deshabilita o no establece esta configuración de Directiva, el modelo de equipo no se validará en relación con la lista de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="8578d-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-174">Configurar la Directiva de exención de usuarios</span><span class="sxs-lookup"><span data-stu-id="8578d-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-175">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-176">Esta configuración de directiva le permite configurar la dirección de un sitio web, la dirección de correo electrónico o el número de teléfono que le indicará a un usuario que solicite una exención del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="8578d-177">Si habilita esta configuración de directiva y proporciona una dirección del sitio web, una dirección de correo electrónico o un número de teléfono, los usuarios verán un cuadro de diálogo con instrucciones sobre cómo solicitar una exención de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="8578d-178">Para obtener más información sobre cómo habilitar exenciones de cifrado de BitLocker para los usuarios, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> Cómo administrar las exenciones de cifrado de BitLocker </a> .</span><span class="sxs-lookup"><span data-stu-id="8578d-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="8578d-179">Si deshabilita o no establece esta configuración de Directiva, las instrucciones sobre cómo solicitar una solicitud de exención no se mostrarán a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8578d-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8578d-180">Nota</span><span class="sxs-lookup"><span data-stu-id="8578d-180">Note</span></span></strong><br/><p><span data-ttu-id="8578d-181">La exención de usuarios se administra por usuario, no por equipo.</span><span class="sxs-lookup"><span data-stu-id="8578d-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="8578d-182">Si varios usuarios inician sesión en el mismo equipo y un usuario no está exento, el equipo se cifrará.</span><span class="sxs-lookup"><span data-stu-id="8578d-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8578d-183">Definiciones de directivas de unidades fijas</span><span class="sxs-lookup"><span data-stu-id="8578d-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="8578d-184">En esta sección se describen las definiciones de directivas de unidades fijas para MBAM, que pueden encontrarse en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad fija**.</span><span class="sxs-lookup"><span data-stu-id="8578d-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8578d-185">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8578d-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="8578d-186">Información general y sugerencia de configuración de directivas</span><span class="sxs-lookup"><span data-stu-id="8578d-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-187">Configuración de cifrado de unidad de datos fija</span><span class="sxs-lookup"><span data-stu-id="8578d-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-188">Sugerencia de configuración: <strong> habilitada </strong> y seleccione la <strong> casilla de verificación Habilitar autobloqueo de unidad de datos fijos </strong> si es necesario cifrar el volumen del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8578d-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="8578d-189">Esta configuración de directiva te permite administrar si deseas cifrar o no las unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="8578d-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="8578d-190">Al habilitar esta Directiva, no deshabilite la <strong> directiva configurar el uso de la contraseña para las unidades de datos fijas </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="8578d-191">Si la <strong> casilla habilitar autobloqueo de unidad de datos fijos </strong> está activada, el volumen del sistema operativo se debe cifrar.</span><span class="sxs-lookup"><span data-stu-id="8578d-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="8578d-192">Si habilita esta configuración de Directiva, los usuarios tendrán que poner todas las unidades fijas en la protección de BitLocker, que cifrarán las unidades.</span><span class="sxs-lookup"><span data-stu-id="8578d-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="8578d-193">Si no configura esta Directiva o si deshabilita esta Directiva, los usuarios no tendrán que poner unidades fijas en la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="8578d-194">Si deshabilita esta Directiva, el agente de MBAM descifra cualquier unidad fija cifrada.</span><span class="sxs-lookup"><span data-stu-id="8578d-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="8578d-195">Si no es necesario cifrar el volumen del sistema operativo, desactive la <strong> casilla habilitar el bloqueo automático de la unidad de datos fijos </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-196">Denegar el permiso de "escritura" a las unidades fijas que no están protegidas con BitLocker</span><span class="sxs-lookup"><span data-stu-id="8578d-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-197">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-198">Esta configuración de directiva determina si se requiere la protección de BitLocker para las unidades fijas en un equipo para que se puedan escribir.</span><span class="sxs-lookup"><span data-stu-id="8578d-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="8578d-199">Esta configuración de Directiva se aplica al activar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="8578d-200">Cuando la Directiva no está configurada, todas las unidades fijas del equipo se montan con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8578d-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-201">Permitir el acceso a unidades fijas protegidas con BitLocker desde versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="8578d-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-202">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-203">Habilite esta directiva para desbloquear y ver las unidades fijas que se han formateado con el sistema de archivos de tabla de asignación de archivos (FAT) en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="8578d-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="8578d-204">Estos sistemas operativos tienen permisos de solo lectura para las unidades protegidas con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="8578d-205">Cuando la Directiva está deshabilitada, las unidades fijas formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="8578d-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-206">Configurar el uso de la contraseña para unidades fijas</span><span class="sxs-lookup"><span data-stu-id="8578d-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-207">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-208">Habilite esta directiva para configurar la protección con contraseña en unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="8578d-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="8578d-209">Cuando la Directiva no está configurada, las contraseñas serán compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de contraseña y solo requiere ocho caracteres.</span><span class="sxs-lookup"><span data-stu-id="8578d-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="8578d-210">Para mayor seguridad, habilite esta directiva y seleccione <strong> requerir contraseña para unidad de datos fija </strong> , seleccione <strong> requerir complejidad de la contraseña </strong> y establezca la <strong> longitud mínima de la contraseña deseada </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-211">Elegir cómo se pueden recuperar las unidades fijas protegidas con BitLocker</span><span class="sxs-lookup"><span data-stu-id="8578d-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-212">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-213">Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="8578d-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="8578d-214">Cuando esta Directiva no está configurada, se permite el agente de recuperación de datos de BitLocker y no se realiza una copia de seguridad de la información de recuperación en AD DS.</span><span class="sxs-lookup"><span data-stu-id="8578d-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="8578d-215">MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</span><span class="sxs-lookup"><span data-stu-id="8578d-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8578d-216">Definiciones de directiva de unidad de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8578d-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="8578d-217">En esta sección se describen las definiciones de directiva de unidad del sistema operativo para MBAM, que se encuentran en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas plantillas**de \\ **Windows componentes de Windows**de \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad del sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="8578d-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8578d-218">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8578d-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="8578d-219">Información general y sugerencia de configuración de directivas</span><span class="sxs-lookup"><span data-stu-id="8578d-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-220">Configuración de cifrado de unidad del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8578d-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-221">Configuración sugerida: <strong> habilitado</span><span class="sxs-lookup"><span data-stu-id="8578d-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="8578d-222">Esta configuración de directiva determina si se cifrará la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8578d-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="8578d-223">Configure esta directiva para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8578d-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="8578d-224">Exigir la protección de BitLocker para la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8578d-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="8578d-225">Configure el uso de PIN para usar un PIN de módulo de plataforma segura (TPM) para la protección del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8578d-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="8578d-226">Configure los pines de inicio mejorados para que admitan caracteres como letras mayúsculas y minúsculas, y números.</span><span class="sxs-lookup"><span data-stu-id="8578d-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="8578d-227">MBAM no admite el uso de símbolos y espacios para los bordes mejorados, aunque BitLocker admita símbolos y espacios.</span><span class="sxs-lookup"><span data-stu-id="8578d-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="8578d-228">Si habilita esta configuración de Directiva, los usuarios deberán proteger la unidad del sistema operativo con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="8578d-229">Si no configura o si deshabilita la configuración, los usuarios no tendrán que proteger la unidad del sistema operativo con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="8578d-230">Si deshabilita esta Directiva, el agente de MBAM descifra el volumen del sistema operativo Si está cifrado.</span><span class="sxs-lookup"><span data-stu-id="8578d-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="8578d-231">Cuando está habilitada, esta configuración de directiva requiere que los usuarios protejan el sistema operativo con la protección de BitLocker y la unidad está cifrada.</span><span class="sxs-lookup"><span data-stu-id="8578d-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="8578d-232">En función de los requisitos de cifrado, puede seleccionar el método de protección de la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8578d-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="8578d-233">Para los requisitos de seguridad más altos, use TPM + PIN, permita PIN mejorados y establezca la longitud mínima del PIN en ocho caracteres.</span><span class="sxs-lookup"><span data-stu-id="8578d-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="8578d-234">Cuando esta directiva está habilitada con el protector de TPM + PIN, puede considerar deshabilitar las siguientes directivas en <strong> configuración de suspensión de administración del sistema </strong>  /  <strong> </strong>  /  <strong> </strong> :</span><span class="sxs-lookup"><span data-stu-id="8578d-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="8578d-235">Permitir Estados de espera (S1-S3) cuando está en espera (conectado)</span><span class="sxs-lookup"><span data-stu-id="8578d-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="8578d-236">Permitir Estados de espera (S1-S3) cuando está en suspensión (con batería)</span><span class="sxs-lookup"><span data-stu-id="8578d-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-237">Configurar el perfil de validación de plataforma TPM</span><span class="sxs-lookup"><span data-stu-id="8578d-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-238">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-239">Esta configuración de directiva le permite configurar cómo el hardware de seguridad TPM de un equipo protege la clave de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="8578d-240">Esta configuración de Directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya tiene habilitada la protección de TPM.</span><span class="sxs-lookup"><span data-stu-id="8578d-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="8578d-241">Cuando esta Directiva no está configurada, el TPM usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de configuración.</span><span class="sxs-lookup"><span data-stu-id="8578d-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-242">Elegir cómo recuperar unidades de sistema operativo protegidas con BitLocker</span><span class="sxs-lookup"><span data-stu-id="8578d-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-243">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-244">Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="8578d-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="8578d-245">Cuando esta Directiva no está configurada, se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</span><span class="sxs-lookup"><span data-stu-id="8578d-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="8578d-246">La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</span><span class="sxs-lookup"><span data-stu-id="8578d-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8578d-247">Definiciones de directivas de unidades extraíbles</span><span class="sxs-lookup"><span data-stu-id="8578d-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="8578d-248">En esta sección se describen las definiciones de directivas de unidades extraíbles para MBAM, que se encuentran en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas plantillas**de \\ **Windows componentes de Windows**de \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad extraíble**.</span><span class="sxs-lookup"><span data-stu-id="8578d-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8578d-249">Nombre de directiva</span><span class="sxs-lookup"><span data-stu-id="8578d-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="8578d-250">Información general y sugerencia de configuración de directivas</span><span class="sxs-lookup"><span data-stu-id="8578d-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-251">Controlar el uso de BitLocker en unidades extraíbles</span><span class="sxs-lookup"><span data-stu-id="8578d-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-252">Configuración sugerida: <strong> habilitado</span><span class="sxs-lookup"><span data-stu-id="8578d-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="8578d-253">Esta directiva controla el uso de BitLocker en unidades de datos extraíbles.</span><span class="sxs-lookup"><span data-stu-id="8578d-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="8578d-254">Habilite la <strong> opción permitir que los usuarios apliquen la protección de BitLocker en unidades de datos extraíbles </strong> para permitir que los usuarios ejecuten el Asistente de configuración de BitLocker en una unidad de datos extraíble.</span><span class="sxs-lookup"><span data-stu-id="8578d-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="8578d-255">Habilite la <strong> opción permitir que los usuarios puedan suspender y descifrar BitLocker en unidades de datos extraíbles </strong> para permitir a los usuarios quitar el cifrado de unidad BitLocker de la unidad o para suspender el cifrado mientras se realiza el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="8578d-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="8578d-256">Cuando esta directiva está habilitada y la <strong> opción permitir que los usuarios apliquen protección de BitLocker en unidades de datos extraíbles </strong> está seleccionada, el cliente de MBAM guarda la información de recuperación de las unidades extraíbles en el servidor de recuperación de claves MBAM y permite a los usuarios recuperar la unidad si se pierde la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8578d-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-257">Denegar los permisos de "escritura" a unidades extraíbles que no estén protegidas por BitLocker</span><span class="sxs-lookup"><span data-stu-id="8578d-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-258">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-259">Habilite esta directiva para permitir permisos de solo escritura en unidades protegidas con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="8578d-260">Cuando esta directiva está habilitada, todas las unidades de datos extraíbles en el equipo requieren cifrar para que se permitan los permisos de escritura.</span><span class="sxs-lookup"><span data-stu-id="8578d-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-261">Permitir el acceso a unidades extraíbles protegidas con BitLocker desde versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="8578d-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-262">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-263">Habilite esta directiva para desbloquear y ver las unidades fijas formateadas con el sistema de archivos (FAT) en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="8578d-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="8578d-264">Estos sistemas operativos tienen permisos de solo lectura para las unidades protegidas con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8578d-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="8578d-265">Cuando la Directiva está deshabilitada, las unidades extraíbles formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="8578d-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8578d-266">Configurar el uso de la contraseña para unidades de datos extraíbles</span><span class="sxs-lookup"><span data-stu-id="8578d-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-267">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-268">Habilite esta directiva para configurar la protección con contraseña en unidades de datos extraíbles.</span><span class="sxs-lookup"><span data-stu-id="8578d-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="8578d-269">Cuando esta Directiva no está configurada, las contraseñas son compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de contraseña y solo requiere ocho caracteres.</span><span class="sxs-lookup"><span data-stu-id="8578d-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="8578d-270">Para una mayor seguridad, puede habilitar esta directiva y seleccionar <strong> requerir contraseña para la unidad de datos extraíbles </strong> , seleccionar <strong> requerir complejidad de </strong> la contraseña y, a continuación, establecer la <strong> longitud mínima de la contraseña </strong> .</span><span class="sxs-lookup"><span data-stu-id="8578d-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8578d-271">Elegir cómo se pueden recuperar las unidades extraíbles protegidas con BitLocker</span><span class="sxs-lookup"><span data-stu-id="8578d-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="8578d-272">Configuración sugerida: <strong> no configurada</span><span class="sxs-lookup"><span data-stu-id="8578d-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="8578d-273">Puede configurar esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="8578d-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="8578d-274">Cuando la Directiva se establece en <strong> no configurada </strong> , se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</span><span class="sxs-lookup"><span data-stu-id="8578d-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="8578d-275">La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</span><span class="sxs-lookup"><span data-stu-id="8578d-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8578d-276">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8578d-276">Related topics</span></span>


[<span data-ttu-id="8578d-277">Preparación del entorno para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8578d-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









