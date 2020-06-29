---
title: Notas de la versión de MBAM 2.5 SP1
description: Notas de la versión de MBAM 2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824990"
---
# <span data-ttu-id="070c9-103">Notas de la versión de MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="070c9-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="070c9-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="070c9-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="070c9-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="070c9-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="070c9-106">Estas notas de la versión contienen información necesaria para instalar MBAM correctamente y pueden contener información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="070c9-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="070c9-107">Si estas notas de la versión difieren de otra documentación de MBAM 2,5 SP1, considere el cambio más reciente para que sea autoritativo.</span><span class="sxs-lookup"><span data-stu-id="070c9-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="070c9-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="070c9-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="070c9-109">Problemas conocidos de MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="070c9-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="070c9-110">Esta sección contiene notas de la versión para MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="070c9-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="070c9-111">Los cmdlets de lectura de AD \ \* de PowerShell no proporcionan comentarios si el usuario no tiene derechos suficientes</span><span class="sxs-lookup"><span data-stu-id="070c9-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="070c9-112">Si un usuario que intenta usar los cmdlets de lectura-AD \ \* de PowerShell para el servidor de MBAM no tiene derechos de usuario para leer la información de recuperación de Active Directory o para leer la información de TPM, los cmdlets no proporcionarán al usuario ningún error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="070c9-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="070c9-113">**Solución alternativa:** Use solo los cmdlets de lectura de AD \ \* de PowerShell si tiene los derechos de usuario requeridos.</span><span class="sxs-lookup"><span data-stu-id="070c9-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="070c9-114">MBAM cmdlets de migración de Active Directory (AD) no recuperan información de recuperación de volúmenes</span><span class="sxs-lookup"><span data-stu-id="070c9-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="070c9-115">MBAM cmdlets de migración de Active Directory (AD) no pueden recuperar información de recuperación de volúmenes de equipos en unidades organizativas (OU) si el carácter de barra diagonal (/) forma parte del nombre de la uo.</span><span class="sxs-lookup"><span data-stu-id="070c9-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="070c9-116">Las extracciones de anuncios repetidas fallarán con un error de terminación de canalización cuando se detecte este error.</span><span class="sxs-lookup"><span data-stu-id="070c9-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="070c9-117">**Detalles técnicos:** Verá este error al ejecutar el comando:</span><span class="sxs-lookup"><span data-stu-id="070c9-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="070c9-118">Además, el seguimiento de pila de excepción tendrá el siguiente `Error[0].Exception.StackTrace` aspecto:</span><span class="sxs-lookup"><span data-stu-id="070c9-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="070c9-119">**Solución alternativa:** Realice una de estas tareas para resolver esta situación:</span><span class="sxs-lookup"><span data-stu-id="070c9-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="070c9-120">Cambie el nombre de la OU para quitar el carácter de barra diagonal y, a continuación, ejecute el script.</span><span class="sxs-lookup"><span data-stu-id="070c9-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="070c9-121">Para excluir cualquier unidad organizativa problemática del proceso de copia de seguridad, busque una lista de unidades organizativas cuyos nombres no contengan el carácter de barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="070c9-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="070c9-122">Ejecute la secuencia de comandos en estas unidades organizativas, una por una.</span><span class="sxs-lookup"><span data-stu-id="070c9-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="070c9-123">MBAM no cifra un volumen e informa de un error Si estableces un protector de TPM + PIN en un dispositivo de tableta</span><span class="sxs-lookup"><span data-stu-id="070c9-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="070c9-124">Si los usuarios finales intentan establecer un protector de anclaje + PIN en un dispositivo de tableta, MBAM no se cifrará y notificará un error.</span><span class="sxs-lookup"><span data-stu-id="070c9-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="070c9-125">Este problema se produce porque los dispositivos de tableta no tienen un teclado de entorno de preinicialización.</span><span class="sxs-lookup"><span data-stu-id="070c9-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="070c9-126">**Solución alternativa:** Habilite la configuración **Habilitar el uso de la autenticación de BitLocker que requiera la entrada del teclado de prearranque en tabletas** .</span><span class="sxs-lookup"><span data-stu-id="070c9-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="070c9-127">Esta opción es una configuración de directiva de grupo de BitLocker y no está disponible en las plantillas de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="070c9-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="070c9-128">El nombre principal de usuario es necesario para todas las cuentas de servicio</span><span class="sxs-lookup"><span data-stu-id="070c9-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="070c9-129">Debe establecerse un nombre principal de usuario (UPN) para todas las cuentas de servicio en MBAM.</span><span class="sxs-lookup"><span data-stu-id="070c9-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="070c9-130">Si no puede crear un UPN para una cuenta, aparecerá un mensaje de error durante el proceso de configuración para indicar que el usuario o grupo no se pudo encontrar en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="070c9-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="070c9-131">**Solución alternativa:** Agregue el UPN a la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="070c9-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="070c9-132">El portal de autoservicio y el sitio web de administración y supervisión no se abren después de actualizar IIS a .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="070c9-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="070c9-133">Al actualizar Internet Information Services (IIS) a Microsoft .NET Framework 4,5, el portal de autoservicio y el sitio web de administración y supervisión no se abren.</span><span class="sxs-lookup"><span data-stu-id="070c9-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="070c9-134">**Solución alternativa:** Vea el artículo [mensaje de error después de instalar .NET Framework 4,0: "no se pudo cargar el tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="070c9-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="070c9-135">Sitio web de supervisión y administración muestra el mensaje de error "no se puede encontrar el informe" cuando no se han configurado los informes</span><span class="sxs-lookup"><span data-stu-id="070c9-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="070c9-136">Si configura el sitio web de administración y supervisión y, a continuación, intenta ver un informe sin configurar la característica informes en primer lugar, un mensaje de error indica que no se puede encontrar el informe.</span><span class="sxs-lookup"><span data-stu-id="070c9-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="070c9-137">**Solución alternativa:** Configure la característica informes antes de configurar las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="070c9-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="070c9-138">Los informes del sitio web de administración y supervisión muestran una advertencia si SSL no está configurado en SSRS</span><span class="sxs-lookup"><span data-stu-id="070c9-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="070c9-139">Si SQL Server Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de la característica de informes se establecerá en HTTP en lugar de en HTTPS al configurar el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="070c9-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="070c9-140">Si abre el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje de error: "solo se muestra el contenido seguro".</span><span class="sxs-lookup"><span data-stu-id="070c9-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="070c9-141">**Solución alternativa:** Para mostrar el informe, haga clic en **Mostrar todo el contenido**.</span><span class="sxs-lookup"><span data-stu-id="070c9-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="070c9-142">Para corregir este problema, vaya al equipo MBAM donde está instalado SQL Server Reporting Services, ejecute el **Administrador de configuración de Reporting Services**y, a continuación, haga clic en **URL de servicio Web**.</span><span class="sxs-lookup"><span data-stu-id="070c9-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="070c9-143">Seleccione el certificado SSL adecuado para el servidor, escriba el puerto SSL adecuado (el puerto predeterminado es 443) y, a continuación, haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="070c9-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="070c9-144">Al hacer clic en "atrás" en el informe Resumen de compatibilidad de BitLocker, se puede producir un error</span><span class="sxs-lookup"><span data-stu-id="070c9-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="070c9-145">Si explora en profundidad un informe de Resumen de cumplimiento de BitLocker y luego hace clic en el vínculo **atrás** en el informe de SSRS, se puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="070c9-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="070c9-146">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="070c9-146">**Workaround:** None.</span></span>

### <span data-ttu-id="070c9-147">La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos con BitLocker</span><span class="sxs-lookup"><span data-stu-id="070c9-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="070c9-148">Si no establece una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado, el informe de cumplimiento de BitLocker Computer en la topología de integración del administrador de configuración siempre muestra "desconocido" para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="070c9-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="070c9-149">El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="070c9-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="070c9-150">**Solución alternativa:** Establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.</span><span class="sxs-lookup"><span data-stu-id="070c9-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="070c9-151">La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="070c9-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="070c9-152">Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.</span><span class="sxs-lookup"><span data-stu-id="070c9-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="070c9-153">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="070c9-153">**Workaround:** None.</span></span> <span data-ttu-id="070c9-154">No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="070c9-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="070c9-155">La configuración de seguridad mejorada puede provocar que los informes muestren un mensaje de error incorrectamente</span><span class="sxs-lookup"><span data-stu-id="070c9-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="070c9-156">Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca un mensaje de error "acceso denegado" cuando intente ver informes en el servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="070c9-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="070c9-157">De forma predeterminada, ESC se activa para proteger el servidor disminuyendo la exposición del servidor ante posibles ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="070c9-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="070c9-158">**Solución alternativa:** Si aparece el mensaje de error "acceso denegado" al intentar ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada.</span><span class="sxs-lookup"><span data-stu-id="070c9-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="070c9-159">También puede ver los informes desde otro equipo en el que la ESC no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="070c9-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="070c9-160">Compatibilidad con el algoritmo de cifrado XTS-AES de BitLocker</span><span class="sxs-lookup"><span data-stu-id="070c9-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="070c9-161">BitLocker agregó compatibilidad para el algoritmo de cifrado XTS-AES en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="070c9-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="070c9-162">Con HF02, MBAM agregó compatibilidad de cliente para esta opción de BitLocker y en HF04, agregó la compatibilidad del lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="070c9-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="070c9-163">Sin embargo, hay una limitación conocida:</span><span class="sxs-lookup"><span data-stu-id="070c9-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="070c9-164">Los clientes deben usar la misma intensidad de cifrado para el sistema operativo y los volúmenes de datos en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="070c9-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="070c9-165">Si se usan diferentes niveles de cifrado, MBAM notificará el equipo como **no conforme**.</span><span class="sxs-lookup"><span data-stu-id="070c9-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="070c9-166">El portal de autoservicio agrega automáticamente "-" en la entrada del identificador de clave</span><span class="sxs-lookup"><span data-stu-id="070c9-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="070c9-167">A partir de la HF02, el portal de autoservicio de MBAM agrega automáticamente la "-" en la entrada del identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="070c9-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="070c9-168">**Nota:** El servidor debe reconfigurarse para que el JavaScript surta efecto.</span><span class="sxs-lookup"><span data-stu-id="070c9-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="070c9-169">Los informes de MBAM 2,5 SP1 no funcionan o se representan correctamente</span><span class="sxs-lookup"><span data-stu-id="070c9-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="070c9-170">La página de informes no se representa correctamente cuando SSRS se hospeda en SQL Server 2016 Edition.</span><span class="sxs-lookup"><span data-stu-id="070c9-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="070c9-171">Por ejemplo, para navegar al servicio de asistencia al usuario (haciendo clic en informes) (la parte resaltada tiene "x"), lo que hace que sea más de Fiddler; parece que una vez que hacemos clic en los informes, se llama a la página de SSRS con el formato de representación HTML 4,0.</span><span class="sxs-lookup"><span data-stu-id="070c9-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="070c9-172">**Solución alternativa:** Mirar el código de site. Master e observado que el modo X-UA se dictó como IE8.</span><span class="sxs-lookup"><span data-stu-id="070c9-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="070c9-173">Como IE8 se retrasó al final de la vida útil y el cliente usa IE11.</span><span class="sxs-lookup"><span data-stu-id="070c9-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="070c9-174">Actualice la configuración al código que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="070c9-174">Update the setting to the below code.</span></span> <span data-ttu-id="070c9-175">Esto permite al sitio usar tecnologías de representación de IE11</span><span class="sxs-lookup"><span data-stu-id="070c9-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="070c9-176">La configuración original es:</span><span class="sxs-lookup"><span data-stu-id="070c9-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="070c9-177">Este es el motivo por el que el problema no se ha visto con otros exploradores como Chrome, Firefox, etc.</span><span class="sxs-lookup"><span data-stu-id="070c9-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="070c9-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="070c9-178">Related topics</span></span>


[<span data-ttu-id="070c9-179">Acerca de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="070c9-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="070c9-180">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="070c9-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="070c9-181">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="070c9-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="070c9-182">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="070c9-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





