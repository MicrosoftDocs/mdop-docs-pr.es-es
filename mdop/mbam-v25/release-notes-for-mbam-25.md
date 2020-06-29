---
title: Notas de la versión de MBAM 2.5
description: Notas de la versión de MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824981"
---
# <span data-ttu-id="012d9-103">Notas de la versión de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="012d9-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="012d9-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="012d9-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="012d9-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="012d9-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="012d9-106">Estas notas de la versión contienen información necesaria para instalar MBAM correctamente y pueden contener información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="012d9-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="012d9-107">Si estas notas de la versión difieren de otra documentación de MBAM 2,5, considere el cambio más reciente para que sea autoritativo.</span><span class="sxs-lookup"><span data-stu-id="012d9-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="012d9-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="012d9-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="012d9-109">Problemas conocidos de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="012d9-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="012d9-110">Esta sección contiene notas de la versión para MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="012d9-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="012d9-111">Explorador Web ejecutándose como administrador de forma involuntaria</span><span class="sxs-lookup"><span data-stu-id="012d9-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="012d9-112">Los vínculos de ayuda de la herramienta de configuración del servidor de MBAM pueden hacer que las ventanas del explorador se abran con derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="012d9-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="012d9-113">**Solución alternativa:** Habilite la configuración de seguridad mejorada de Internet Explorer (IESC) o cierre el explorador Web antes de navegar a otros sitios.</span><span class="sxs-lookup"><span data-stu-id="012d9-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="012d9-114">**Nota:**  Esto se ha corregido en MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="012d9-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="012d9-115">MBAM informa de que no es compatible un cliente cifrado con las claves de cifrado y el difusor de AES 256 bits</span><span class="sxs-lookup"><span data-stu-id="012d9-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="012d9-116">Si un equipo tiene el cliente MBAM 2,5 instalado y se cifra mediante la norma AES 256 bits con cifrado de difusor, el cliente de MBAM se notifica como no conforme en los informes de cumplimiento de MBAM.</span><span class="sxs-lookup"><span data-stu-id="012d9-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="012d9-117">**Solución alternativa:** Instale el Hotfix en [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span><span class="sxs-lookup"><span data-stu-id="012d9-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="012d9-118">MBAM no cifra un volumen e informa de un error Si estableces un protector de TPM + PIN en un dispositivo de tableta</span><span class="sxs-lookup"><span data-stu-id="012d9-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="012d9-119">Si los usuarios finales intentan establecer un protector de anclaje + PIN en un dispositivo de tableta, MBAM no se cifrará y notificará un error.</span><span class="sxs-lookup"><span data-stu-id="012d9-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="012d9-120">Este problema se produce porque los dispositivos de tableta no tienen un teclado de entorno de preinicialización.</span><span class="sxs-lookup"><span data-stu-id="012d9-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="012d9-121">**Solución alternativa:** Habilite la configuración **Habilitar el uso de la autenticación de BitLocker que requiera la entrada del teclado de prearranque en tabletas** .</span><span class="sxs-lookup"><span data-stu-id="012d9-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="012d9-122">Esta opción es una configuración de directiva de grupo de BitLocker y no está disponible en las plantillas de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="012d9-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="012d9-123">El nombre principal de usuario es necesario para todas las cuentas de servicio</span><span class="sxs-lookup"><span data-stu-id="012d9-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="012d9-124">Debe establecerse un nombre principal de usuario (UPN) para todas las cuentas de servicio en MBAM.</span><span class="sxs-lookup"><span data-stu-id="012d9-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="012d9-125">Si no puede crear un UPN para una cuenta, aparecerá un mensaje de error durante el proceso de configuración para indicar que el usuario o grupo no se pudo encontrar en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="012d9-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="012d9-126">**Solución alternativa:** Agregue el UPN a la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="012d9-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="012d9-127">El portal de autoservicio requiere una configuración adicional si los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft Ajax</span><span class="sxs-lookup"><span data-stu-id="012d9-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="012d9-128">Si los equipos cliente no tienen acceso a la red de entrega de contenido (CDN) de Microsoft Ajax, lo que proporciona al portal de autoservicio el acceso que necesita a determinados archivos JavaScript, debe configurar el portal de autoservicio para hacer referencia a los archivos de JavaScript desde un origen accesible.</span><span class="sxs-lookup"><span data-stu-id="012d9-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="012d9-129">Si no configura el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red CDN, solo se mostrará el nombre de la compañía y la cuenta con la que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="012d9-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="012d9-130">No aparece ningún mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="012d9-130">No error message appears.</span></span>

<span data-ttu-id="012d9-131">**Solución alternativa:** Instale MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="012d9-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="012d9-132">o configurar el portal de autoservicio siguiendo estas instrucciones: [Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="012d9-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="012d9-133">El portal de autoservicio y el sitio web de administración y supervisión no se abren después de actualizar IIS a .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="012d9-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="012d9-134">Al actualizar Internet Information Services (IIS) a Microsoft .NET Framework 4,5, el portal de autoservicio y el sitio web de administración y supervisión no se abren.</span><span class="sxs-lookup"><span data-stu-id="012d9-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="012d9-135">**Solución alternativa:** Vea el artículo [mensaje de error después de instalar .NET Framework 4,0: "no se pudo cargar el tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="012d9-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="012d9-136">Sitio web de supervisión y administración muestra el mensaje de error "no se puede encontrar el informe" cuando no se han configurado los informes</span><span class="sxs-lookup"><span data-stu-id="012d9-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="012d9-137">Si configura el sitio web de administración y supervisión y, a continuación, intenta ver un informe sin configurar la característica informes en primer lugar, un mensaje de error indica que no se puede encontrar el informe.</span><span class="sxs-lookup"><span data-stu-id="012d9-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="012d9-138">**Solución alternativa:** Configure la característica informes antes de configurar las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="012d9-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="012d9-139">Los informes del sitio web de administración y supervisión muestran una advertencia si SSL no está configurado en SSRS</span><span class="sxs-lookup"><span data-stu-id="012d9-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="012d9-140">Si SQL Server Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de la característica de informes se establecerá en HTTP en lugar de en HTTPS al configurar el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="012d9-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="012d9-141">Si abre el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje de error: "solo se muestra el contenido seguro".</span><span class="sxs-lookup"><span data-stu-id="012d9-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="012d9-142">**Solución alternativa:** Para mostrar el informe, haga clic en **Mostrar todo el contenido**.</span><span class="sxs-lookup"><span data-stu-id="012d9-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="012d9-143">Para corregir este problema, vaya al equipo MBAM donde está instalado SQL Server Reporting Services, ejecute el **Administrador de configuración de Reporting Services**y, a continuación, haga clic en **URL de servicio Web**.</span><span class="sxs-lookup"><span data-stu-id="012d9-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="012d9-144">Seleccione el certificado SSL adecuado para el servidor, escriba el puerto SSL adecuado (el puerto predeterminado es 443) y, a continuación, haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="012d9-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="012d9-145">Al hacer clic en "atrás" en el informe Resumen de compatibilidad de BitLocker, se puede producir un error</span><span class="sxs-lookup"><span data-stu-id="012d9-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="012d9-146">Si explora en profundidad un informe de Resumen de cumplimiento de BitLocker y luego hace clic en el vínculo **atrás** en el informe de SSRS, se puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="012d9-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="012d9-147">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="012d9-147">**Workaround:** None.</span></span>

### <span data-ttu-id="012d9-148">El cifrado de espacio usado no funciona correctamente</span><span class="sxs-lookup"><span data-stu-id="012d9-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="012d9-149">Si cifra un equipo por primera vez después de instalar el cliente de MBAM y ha configurado una opción de directiva de grupo para implementar el cifrado solo de espacio usado, MBAM cifra todo el disco erróneamente en lugar de cifrar solo el espacio usado por el disco.</span><span class="sxs-lookup"><span data-stu-id="012d9-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="012d9-150">Si un equipo ya está cifrado con el espacio usado solo cuando instala el cliente MBAM y ha configurado la misma configuración de directiva de grupo, MBAM informa que la unidad está cifrada correctamente y no intenta volver a cifrar la unidad.</span><span class="sxs-lookup"><span data-stu-id="012d9-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="012d9-151">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="012d9-151">**Workaround:** None.</span></span>

### <span data-ttu-id="012d9-152">La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos con BitLocker</span><span class="sxs-lookup"><span data-stu-id="012d9-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="012d9-153">Si no establece una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado, el informe de cumplimiento de BitLocker Computer en la topología de integración del administrador de configuración siempre muestra "desconocido" para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="012d9-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="012d9-154">El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="012d9-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="012d9-155">**Solución alternativa:** Establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.</span><span class="sxs-lookup"><span data-stu-id="012d9-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="012d9-156">La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="012d9-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="012d9-157">Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.</span><span class="sxs-lookup"><span data-stu-id="012d9-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="012d9-158">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="012d9-158">**Workaround:** None.</span></span> <span data-ttu-id="012d9-159">No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="012d9-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="012d9-160">La configuración de seguridad mejorada puede provocar que los informes muestren un mensaje de error incorrectamente</span><span class="sxs-lookup"><span data-stu-id="012d9-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="012d9-161">Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca un mensaje de error "acceso denegado" cuando intente ver informes en el servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="012d9-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="012d9-162">De forma predeterminada, ESC se activa para proteger el servidor disminuyendo la exposición del servidor ante posibles ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="012d9-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="012d9-163">**Solución alternativa:** Si aparece el mensaje de error "acceso denegado" al intentar ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada.</span><span class="sxs-lookup"><span data-stu-id="012d9-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="012d9-164">También puede ver los informes desde otro equipo en el que la ESC no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="012d9-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="012d9-165">Revisiones y artículos de Knowledge base para MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="012d9-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="012d9-166">En esta tabla se enumeran los Hotfix y los artículos de KB para MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="012d9-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="012d9-167">Artículo de KB</span><span class="sxs-lookup"><span data-stu-id="012d9-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="012d9-168">Title</span><span class="sxs-lookup"><span data-stu-id="012d9-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="012d9-169">Link</span><span class="sxs-lookup"><span data-stu-id="012d9-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="012d9-170">2975636</span><span class="sxs-lookup"><span data-stu-id="012d9-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-171">Paquete de Hotfix 1 para administración y supervisión de Microsoft BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="012d9-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="012d9-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="012d9-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="012d9-173">3015477</span><span class="sxs-lookup"><span data-stu-id="012d9-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-174">Paquete de revisiones 2 para administración y supervisión de BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="012d9-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="012d9-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="012d9-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="012d9-176">3011022</span><span class="sxs-lookup"><span data-stu-id="012d9-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-177">Se produce un error en la instalación de MBAM 2,5 o en los informes de Configuration Manager si el nombre de la instancia SSRS contiene un guión bajo</span><span class="sxs-lookup"><span data-stu-id="012d9-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="012d9-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="012d9-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="012d9-179">2756402</span><span class="sxs-lookup"><span data-stu-id="012d9-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-180">El cliente de MBAM no funcionaba con el identificador de evento 4 y el código de error 0x8004100E en la descripción del evento</span><span class="sxs-lookup"><span data-stu-id="012d9-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="012d9-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="012d9-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="012d9-182">2639518</span><span class="sxs-lookup"><span data-stu-id="012d9-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-183">Error al abrir informes de cumplimiento de los equipos o de la empresa en MBAM</span><span class="sxs-lookup"><span data-stu-id="012d9-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="012d9-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="012d9-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="012d9-185">2870842</span><span class="sxs-lookup"><span data-stu-id="012d9-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-186">Error de instalación de MBAM 2,0 durante el escenario de integración de Configuration Manager con SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="012d9-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="012d9-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="012d9-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="012d9-188">2975472</span><span class="sxs-lookup"><span data-stu-id="012d9-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="012d9-189">Interbloqueos de SQL cuando muchos clientes de MBAM se conectan a la base de datos de recuperación de MBAM</span><span class="sxs-lookup"><span data-stu-id="012d9-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="012d9-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="012d9-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="012d9-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="012d9-191">Related topics</span></span>


[<span data-ttu-id="012d9-192">Acerca de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="012d9-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="012d9-193">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="012d9-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="012d9-194">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="012d9-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="012d9-195">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="012d9-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





