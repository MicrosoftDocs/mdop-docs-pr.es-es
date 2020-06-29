---
title: Consideraciones sobre seguridad de MBAM 2.5
description: Consideraciones sobre seguridad de MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826840"
---
# <span data-ttu-id="3f804-103">Consideraciones sobre seguridad de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3f804-103">MBAM 2.5 Security Considerations</span></span>


<span data-ttu-id="3f804-104">Este tema contiene la siguiente información sobre cómo proteger la administración y supervisión de Microsoft BitLocker (MBAM):</span><span class="sxs-lookup"><span data-stu-id="3f804-104">This topic contains the following information about how to secure Microsoft BitLocker Administration and Monitoring (MBAM):</span></span>

-   [<span data-ttu-id="3f804-105">Configurar MBAM para custodiar TPM y almacenar OwnerAuth contraseñas</span><span class="sxs-lookup"><span data-stu-id="3f804-105">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>](#bkmk-tpm)

-   [<span data-ttu-id="3f804-106">Configurar MBAM para que desbloquee TPM automáticamente después de un bloqueo</span><span class="sxs-lookup"><span data-stu-id="3f804-106">Configure MBAM to automatically unlock the TPM after a lockout</span></span>](#bkmk-autounlock)

-   [<span data-ttu-id="3f804-107">Conexiones seguras a SQL Server</span><span class="sxs-lookup"><span data-stu-id="3f804-107">Secure connections to SQL Server</span></span>](#bkmk-secure-databases)

-   [<span data-ttu-id="3f804-108">Crear cuentas y grupos</span><span class="sxs-lookup"><span data-stu-id="3f804-108">Create accounts and groups</span></span>](#bkmk-accts-groups)

-   [<span data-ttu-id="3f804-109">Usar archivos de registro de MBAM</span><span class="sxs-lookup"><span data-stu-id="3f804-109">Use MBAM log files</span></span>](#bkmk-logfiles)

-   [<span data-ttu-id="3f804-110">Revisar las consideraciones de la base de datos de MBAM TDE</span><span class="sxs-lookup"><span data-stu-id="3f804-110">Review MBAM database TDE considerations</span></span>](#bkmk-tde)

-   [<span data-ttu-id="3f804-111">Comprender las consideraciones generales de seguridad</span><span class="sxs-lookup"><span data-stu-id="3f804-111">Understand general security considerations</span></span>](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a><span data-ttu-id="3f804-112">Configurar MBAM para custodiar TPM y almacenar OwnerAuth contraseñas</span><span class="sxs-lookup"><span data-stu-id="3f804-112">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>

<span data-ttu-id="3f804-113">**Nota:** Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-113">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="3f804-114">Además, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-114">In addition, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="3f804-115">Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="3f804-115">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="3f804-116">En función de su configuración, el módulo de plataforma segura (TPM) se bloqueará en determinadas situaciones: como cuando se escriben demasiadas contraseñas incorrectas: y puede permanecer bloqueada durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f804-116">Depending on its configuration, the Trusted Platform Module (TPM) will lock itself in certain situations ─ such as when too many incorrect passwords are entered ─ and can remain locked for a period of time.</span></span> <span data-ttu-id="3f804-117">Durante el bloqueo de TPM, BitLocker no puede obtener acceso a las claves de cifrado para realizar operaciones de desbloqueo o descifrado, lo que requiere que el usuario escriba su clave de recuperación de BitLocker para obtener acceso a la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3f804-117">During TPM lockout, BitLocker cannot access the encryption keys to perform unlock or decryption operations, requiring the user to enter their BitLocker recovery key to access the operating system drive.</span></span> <span data-ttu-id="3f804-118">Para restablecer el bloqueo de TPM, debe proporcionar la contraseña del TPM OwnerAuth.</span><span class="sxs-lookup"><span data-stu-id="3f804-118">To reset TPM lockout, you must provide the TPM OwnerAuth password.</span></span>

<span data-ttu-id="3f804-119">MBAM puede almacenar la contraseña de OwnerAuth de TPM en la base de datos de MBAM si es propietaria de TPM o si la contraseña se custodia.</span><span class="sxs-lookup"><span data-stu-id="3f804-119">MBAM can store the TPM OwnerAuth password in the MBAM database if it owns the TPM or if it escrows the password.</span></span> <span data-ttu-id="3f804-120">Las contraseñas de OwnerAuth son fácilmente accesibles en el sitio web de administración y supervisión cuando debe recuperarse desde un bloqueo de TPM, lo que elimina la necesidad de esperar a que el bloqueo se resuelva por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="3f804-120">OwnerAuth passwords are then easily accessible on the Administration and Monitoring Website when you must recover from a TPM lockout, eliminating the need to wait for the lockout to resolve on its own.</span></span>

### <span data-ttu-id="3f804-121">Custodia de OwnerAuth TPM en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="3f804-121">Escrowing TPM OwnerAuth in Windows 8 and higher</span></span>

<span data-ttu-id="3f804-122">**Nota:** Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-122">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="3f804-123">En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-123">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="3f804-124">Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="3f804-124">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="3f804-125">En Windows 8 o versiones posteriores, MBAM ya no debe poseer el TPM para almacenar la contraseña de OwnerAuth, siempre que la OwnerAuth esté disponible en la máquina local.</span><span class="sxs-lookup"><span data-stu-id="3f804-125">In Windows 8 or higher, MBAM no longer must own the TPM to store the OwnerAuth password, as long as the OwnerAuth is available on the local machine.</span></span>

<span data-ttu-id="3f804-126">Para habilitar MBAM para el depósito de garantía y, a continuación, almacenar las contraseñas de OwnerAuth de TPM, debe configurar estas opciones de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3f804-126">To enable MBAM to escrow and then store TPM OwnerAuth passwords, you must configure these Group Policy settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f804-127">Configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="3f804-127">Group Policy Setting</span></span></th>
<th align="left"><span data-ttu-id="3f804-128">Configuración</span><span class="sxs-lookup"><span data-stu-id="3f804-128">Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f804-129">Activar la copia de seguridad de TPM en servicios de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f804-129">Turn on TPM backup to Active Directory Domain Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f804-130">Deshabilitado o no configurado</span><span class="sxs-lookup"><span data-stu-id="3f804-130">Disabled or Not Configured</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f804-131">Configurar el nivel de información de autorización de propietario de TPM disponible para el sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3f804-131">Configure the level of TPM owner authorization information available to the operating system</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f804-132">Delegado/ninguno o no configurado</span><span class="sxs-lookup"><span data-stu-id="3f804-132">Delegated/None or Not Configured</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3f804-133">La ubicación de esta configuración de directiva de grupo es **configuración de equipo** &gt; **plantillas administrativas** &gt; **System** &gt; **servicios de módulo de plataforma segura**.</span><span class="sxs-lookup"><span data-stu-id="3f804-133">The location of these Group Policy settings is **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="3f804-134">**Nota:**  Windows elimina el OwnerAuth de forma local después de que MBAM lo logró correctamente con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="3f804-134">**Note** Windows removes the OwnerAuth locally after MBAM successfully escrows it with these settings.</span></span>

 

### <span data-ttu-id="3f804-135">Custodia de OwnerAuth TPM en Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f804-135">Escrowing TPM OwnerAuth in Windows 7</span></span>

<span data-ttu-id="3f804-136">En Windows 7, MBAM debe poseer el TPM para custodiar automáticamente la información de OwnerAuth de TPM en la base de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-136">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="3f804-137">Si MBAM no posee el TPM, debe usar los cmdlets de importación de datos de Active Directory (AD) MBAM para copiar OwnerAuth de TPM de Active Directory a la base de datos MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-137">If MBAM does not own the TPM, you must use the MBAM Active Directory (AD) Data Import cmdlets to copy TPM OwnerAuth from Active Directory into the MBAM database.</span></span>

### <span data-ttu-id="3f804-138">MBAM cmdlets de importación de datos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f804-138">MBAM Active Directory Data Import cmdlets</span></span>

<span data-ttu-id="3f804-139">Los cmdlets de importación de datos de Active Directory de MBAM le permiten recuperar paquetes de claves de recuperación y OwnerAuth contraseñas almacenadas en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3f804-139">The MBAM Active Directory Data Import cmdlets let you retrieve recovery key packages and OwnerAuth passwords that are stored in Active Directory.</span></span>

<span data-ttu-id="3f804-140">El servidor MBAM 2,5 SP1 se suministra con cuatro cmdlets de PowerShell que previamente rellenan las bases de datos de MBAM con la información de recuperación por volumen y de propietario de TPM almacenada en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3f804-140">The MBAM 2.5 SP1 server ships with four PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="3f804-141">Para claves de recuperación de volumen y paquetes:</span><span class="sxs-lookup"><span data-stu-id="3f804-141">For Volume Recovery keys and packages:</span></span>

-   <span data-ttu-id="3f804-142">Lectura-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="3f804-142">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="3f804-143">Escritura MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="3f804-143">Write-MbamRecoveryInformation</span></span>

<span data-ttu-id="3f804-144">Para información de propietario de TPM:</span><span class="sxs-lookup"><span data-stu-id="3f804-144">For TPM Owner Information:</span></span>

-   <span data-ttu-id="3f804-145">Lectura-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="3f804-145">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="3f804-146">Escritura MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="3f804-146">Write-MbamTpmInformation</span></span>

<span data-ttu-id="3f804-147">Para asociar usuarios a equipos:</span><span class="sxs-lookup"><span data-stu-id="3f804-147">For Associating Users to Computers:</span></span>

-   <span data-ttu-id="3f804-148">Escritura MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="3f804-148">Write-MbamComputerUser</span></span>

<span data-ttu-id="3f804-149">Los cmdlets de lectura de AD \ \* leen la información de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3f804-149">The Read-AD\* cmdlets read information from Active Directory.</span></span> <span data-ttu-id="3f804-150">El cmdlet Write-Mbam \ \* inserta los datos en las bases de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-150">The Write-Mbam\* cmdlets push the data into the MBAM databases.</span></span> <span data-ttu-id="3f804-151">Consulte [Referencia del cmdlet de administración y 2,5 supervisión de Microsoft BitLocker](https://technet.microsoft.com/library/dn459018.aspx) para obtener información detallada sobre estos cmdlets, incluida la sintaxis, los parámetros y los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="3f804-151">See [Cmdlet Reference for Microsoft Bitlocker Administration and Monitoring 2.5](https://technet.microsoft.com/library/dn459018.aspx) for detailed information about these cmdlets, including syntax, parameters, and examples.</span></span>

<span data-ttu-id="3f804-152">**Crear asociaciones entre usuarios:** Los cmdlets de importación de datos de Active Directory MBAM recopilan información de Active Directory e insertan los datos en MBAM base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f804-152">**Create user-to-computer associations:** The MBAM Active Directory Data Import cmdlets gather information from Active Directory and insert the data into MBAM database.</span></span> <span data-ttu-id="3f804-153">Sin embargo, no asocian usuarios a los volúmenes.</span><span class="sxs-lookup"><span data-stu-id="3f804-153">However, they do not associate users to volumes.</span></span> <span data-ttu-id="3f804-154">Puede descargar el script de PowerShell Add-ComputerUser.ps1 para crear asociaciones entre equipos, lo que permite a los usuarios recuperar el acceso a un equipo a través del sitio web de administración y supervisión o mediante el portal de autoservicio para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="3f804-154">You can download the Add-ComputerUser.ps1 PowerShell script to create user-to-machine associations, which let users regain access to a computer through the Administration and Monitoring Website or by using the Self-Service Portal for recovery.</span></span> <span data-ttu-id="3f804-155">El script de Add-ComputerUser.ps1 recopila los datos del atributo **administrado por** en Active Directory (ad), el propietario del objeto en ad o un archivo CSV personalizado.</span><span class="sxs-lookup"><span data-stu-id="3f804-155">The Add-ComputerUser.ps1 script gathers data from the **Managed By** attribute in Active Directory (AD), the object owner in AD, or from a custom CSV file.</span></span> <span data-ttu-id="3f804-156">La secuencia de comandos agrega los usuarios detectados al objeto de canal información de recuperación, que se debe pasar a write-MbamRecoveryInformation para insertar los datos en la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="3f804-156">The script then adds the discovered users to the recovery information pipeline object, which must be passed to Write-MbamRecoveryInformation to insert the data into the recovery database.</span></span>

<span data-ttu-id="3f804-157">Descargue el Add-ComputerUser.ps1 script de PowerShell desde el [centro de descarga de Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).</span><span class="sxs-lookup"><span data-stu-id="3f804-157">Download the Add-ComputerUser.ps1 PowerShell script from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122).</span></span>

<span data-ttu-id="3f804-158">Puede especificar la **ayuda Add-ComputerUser.ps1** para obtener ayuda sobre el script, incluidos ejemplos de uso de los cmdlets y el script.</span><span class="sxs-lookup"><span data-stu-id="3f804-158">You can specify **help Add-ComputerUser.ps1** to get help for the script, including examples of how to use the cmdlets and the script.</span></span>

<span data-ttu-id="3f804-159">Para crear asociaciones entre usuarios después de haber instalado el servidor MBAM, use el cmdlet de PowerShell Write-MbamComputerUser.</span><span class="sxs-lookup"><span data-stu-id="3f804-159">To create user-to-computer associations after you have installed the MBAM server, use the Write-MbamComputerUser PowerShell cmdlet.</span></span> <span data-ttu-id="3f804-160">Al igual que el script de PowerShell de Add-ComputerUser.ps1, este cmdlet le permite especificar los usuarios que pueden usar el portal de autoservicio para obtener información de OwnerAuth de TPM o contraseñas de recuperación de volúmenes para el equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="3f804-160">Similar to the Add-ComputerUser.ps1 PowerShell script, this cmdlet lets you specify users that can use the Self-Service Portal to get TPM OwnerAuth information or volume recovery passwords for the specified computer.</span></span>

<span data-ttu-id="3f804-161">**Nota:**  El agente de MBAM invalidará las asociaciones entre usuarios cuando el equipo comienza a notificar al servidor.</span><span class="sxs-lookup"><span data-stu-id="3f804-161">**Note** The MBAM agent will override user-to-computer associations when that computer begins reporting up to the server.</span></span>

 

<span data-ttu-id="3f804-162">**Requisitos previos:** Los cmdlets de lectura-AD \ \* solo pueden recuperar información de AD si se ejecutan como una cuenta de usuario con privilegios elevados, como un administrador de dominio, o como una cuenta en un grupo de seguridad personalizado con acceso de lectura a la información (recomendado).</span><span class="sxs-lookup"><span data-stu-id="3f804-162">**Prerequisites:** The Read-AD\* cmdlets can retrieve information from AD only if they are either run as a highly privileged user account, such as a Domain Administrator, or run as an account in a custom security group granted read access to the information (recommended).</span></span>

<span data-ttu-id="3f804-163">[Guía de operaciones de cifrado de unidad BitLocker: recuperar volúmenes cifrados con AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) proporciona detalles sobre cómo crear un grupo de seguridad personalizado (o varios grupos) con acceso de lectura a la información del anuncio.</span><span class="sxs-lookup"><span data-stu-id="3f804-163">[BitLocker Drive Encryption Operations Guide: Recovering Encrypted Volumes with AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) provides details about creating a custom security group (or multiple groups) with read access to the AD information.</span></span>

<span data-ttu-id="3f804-164">**Permisos de escritura de los servicios Web de recuperación y hardware de MBAM:** Los cmdlets \ \* de escritura Mbam aceptan la dirección URL del servicio de recuperación y hardware de MBAM, que se usa para publicar la información del TPM o la recuperación.</span><span class="sxs-lookup"><span data-stu-id="3f804-164">**MBAM Recovery and Hardware Web Service Write Permissions:** The Write-Mbam\* cmdlets accept the URL of the MBAM Recovery and Hardware Service, used to publish the recovery or TPM information.</span></span> <span data-ttu-id="3f804-165">Normalmente, solo una cuenta de servicio de equipo de dominio puede comunicarse con el servicio de hardware y recuperación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-165">Typically, only a domain computer service account can communicate with the MBAM Recovery and Hardware Service.</span></span> <span data-ttu-id="3f804-166">En MBAM 2,5 SP1, puede configurar el servicio de hardware y recuperación de MBAM con un grupo de seguridad denominado DataMigrationAccessGroup cuyos miembros pueden omitir la comprobación de la cuenta de servicio de equipo del dominio.</span><span class="sxs-lookup"><span data-stu-id="3f804-166">In MBAM 2.5 SP1, you can configure the MBAM Recovery and Hardware Service with a security group called DataMigrationAccessGroup whose members are allowed to bypass the domain computer service account check.</span></span> <span data-ttu-id="3f804-167">Los cmdlets \ \* de escritura Mbam deben ejecutarse como un usuario que pertenece a este grupo configurado.</span><span class="sxs-lookup"><span data-stu-id="3f804-167">The Write-Mbam\* cmdlets must be run as a user belonging to this configured group.</span></span> <span data-ttu-id="3f804-168">(También, las credenciales de un usuario individual en el grupo configurado se pueden especificar con el parámetro – credential en los cmdlets \ \* de escritura Mbam.)</span><span class="sxs-lookup"><span data-stu-id="3f804-168">(Alternatively, the credentials of an individual user in the configured group can be specified by using the –Credential parameter in the Write-Mbam\* cmdlets.)</span></span>

<span data-ttu-id="3f804-169">Puede configurar el servicio de hardware y recuperación de MBAM con el nombre de este grupo de seguridad de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="3f804-169">You can configure the MBAM Recovery and Hardware Service with the name of this security group in one of these ways:</span></span>

-   <span data-ttu-id="3f804-170">Proporcione el nombre del grupo de seguridad (o individual) en el parámetro-DataMigrationAccessGroup del cmdlet enable-MbamWebApplication – AgentService de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3f804-170">Provide the name of the security group (or individual) in the -DataMigrationAccessGroup parameter of the Enable-MbamWebApplication –AgentService Powershell cmdlet.</span></span>

-   <span data-ttu-id="3f804-171">Configure el grupo después de instalar el servicio de hardware y recuperación de MBAM editando el archivo web.config de la &lt; carpeta de administración de BitLocker de Inetpub &gt; \\Microsoft Solution\\Recovery y de hardware Service\\.</span><span class="sxs-lookup"><span data-stu-id="3f804-171">Configure the group after the MBAM Recovery and Hardware Service has been installed by editing the web.config file in the &lt;inetpub&gt;\\Microsoft Bitlocker Management Solution\\Recovery and Hardware Service\\ folder.</span></span>

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    <span data-ttu-id="3f804-172">donde &lt; GroupName &gt; se reemplaza con el dominio y el nombre del grupo (o el usuario individual) que se usará para permitir la migración de datos desde Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3f804-172">where &lt;groupName&gt; is replaced with the domain and the group name (or the individual user) that will be used to allow data migration from Active Directory.</span></span>

-   <span data-ttu-id="3f804-173">Use el editor de configuración del administrador de IIS para modificar esta appSetting.</span><span class="sxs-lookup"><span data-stu-id="3f804-173">Use the Configuration Editor in IIS Manager to edit this appSetting.</span></span>

<span data-ttu-id="3f804-174">En el siguiente ejemplo, el comando, cuando se ejecuta como miembro del grupo ADRecoveryInformation y del grupo usuarios de migración de datos, extrae la información de recuperación de volumen de los equipos de la unidad organizativa (Uo) estaciones de trabajo del dominio contoso.com y la escribe en MBAM con el servicio de hardware y recuperación MBAM que se ejecuta en el servidor mbam.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="3f804-174">In the following example, the command, when run as a member of both the ADRecoveryInformation group and the Data Migration Users group, will pull the volume recovery information from computers in the WORKSTATIONS organizational unit (OU) in the contoso.com domain and write them to MBAM by using the MBAM Recovery and Hardware Service running on the mbam.contoso.com server.</span></span>

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

<span data-ttu-id="3f804-175">Los \*\*cmdlets de lectura-ad \ \*\*\* aceptan el nombre o la dirección IP de un equipo de servidor de hospedaje de Active Directory para consultar información de recuperación o de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-175">**Read-AD\* cmdlets** accept the name or IP address of an Active Directory hosting server machine to query for recovery or TPM information.</span></span> <span data-ttu-id="3f804-176">Le recomendamos que proporcione los nombres distintivos de los contenedores de AD en los que el objeto de equipo reside como valor del parámetro SearchBase.</span><span class="sxs-lookup"><span data-stu-id="3f804-176">We recommend providing the distinguished names of the AD containers in which the computer object resides as the value of the SearchBase parameter.</span></span> <span data-ttu-id="3f804-177">Si los equipos se almacenan en varias unidades organizativas, los cmdlets pueden aceptar la entrada de canalización una vez para cada contenedor.</span><span class="sxs-lookup"><span data-stu-id="3f804-177">If computers are stored across several OUs, the cmdlets can accept pipeline input to run once for each container.</span></span> <span data-ttu-id="3f804-178">El nombre distintivo de un contenedor de AD tendrá un aspecto similar a OU = máquinas, DC = Contoso, DC = com.</span><span class="sxs-lookup"><span data-stu-id="3f804-178">The distinguished name of an AD container will look similar to OU=Machines,DC=contoso,DC=com.</span></span> <span data-ttu-id="3f804-179">Realizar una búsqueda dirigida a contenedores específicos ofrece las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="3f804-179">Performing a search targeted to specific containers provides the following benefits:</span></span>

-   <span data-ttu-id="3f804-180">Reduce el riesgo de tiempo de espera al consultar un conjunto de objetos de AD grande para objetos de equipo.</span><span class="sxs-lookup"><span data-stu-id="3f804-180">Reduces the risk of timeout while querying a large AD dataset for computer objects.</span></span>

-   <span data-ttu-id="3f804-181">Puede omitir las unidades organizativas que contienen servidores de centro de datos u otras clases de equipos para los que es posible que la copia de seguridad no se desee o sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="3f804-181">Can omit OUs containing datacenter servers or other classes of computers for which the backup might not be desired or necessary.</span></span>

<span data-ttu-id="3f804-182">Otra opción es proporcionar la marca de recursividad con o sin el SearchBase opcional para buscar objetos de equipo en todos los contenedores en la SearchBase especificada o en todo el dominio, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3f804-182">Another option is to provide the –Recurse flag with or without the optional SearchBase to search for computer objects across all containers under the specified SearchBase or the entire domain respectively.</span></span> <span data-ttu-id="3f804-183">Al usar la bandera-recurse, también puede usar el parámetro-MaxPageSize para controlar la cantidad de memoria local y remota necesaria para atender la consulta.</span><span class="sxs-lookup"><span data-stu-id="3f804-183">When you use the -Recurse flag, you can also use the -MaxPageSize parameter to control the amount of local and remote memory required to service the query.</span></span>

<span data-ttu-id="3f804-184">Estos cmdlets escriben en los objetos de canalización de tipo PsObject.</span><span class="sxs-lookup"><span data-stu-id="3f804-184">These cmdlets write to the pipeline objects of type PsObject.</span></span> <span data-ttu-id="3f804-185">Cada instancia de PsObject contiene una única clave de recuperación de volumen o una cadena de propietario de TPM con el nombre de equipo asociado, la marca de hora y otra información necesaria para publicarla en el almacén de datos MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-185">Each PsObject instance contains a single volume recovery key or TPM owner string with its associated computer name, timestamp, and other information required to publish it to the MBAM data store.</span></span>

<span data-ttu-id="3f804-186">\*\*Cmdlets de Write-Mbam \ \*\*\* aceptan valores de parámetros de información de recuperación de la canalización por nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f804-186">**Write-Mbam\* cmdlets** accept recovery information parameter values from the pipeline by property name.</span></span> <span data-ttu-id="3f804-187">Esto permite que los cmdlets \ \* de escritura Mbam acepten la salida de la canalización de los cmdlets de lectura-AD \ \* (por ejemplo, Read-ADRecoveryInformation-Server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="3f804-187">This allows the Write-Mbam\* cmdlets to accept the pipeline output of the Read-AD\* cmdlets (for example, Read-ADRecoveryInformation –Server contoso.com –Recurse | Write-MbamRecoveryInformation –RecoveryServiceEndpoint mbam.contoso.com).</span></span>

<span data-ttu-id="3f804-188">El \*\*cmdlet Write-Mbam \ \*\*\* incluye parámetros opcionales que proporcionan opciones para la tolerancia a errores, registro detallado y preferencias para Whatif y confirm.</span><span class="sxs-lookup"><span data-stu-id="3f804-188">The **Write-Mbam\* cmdlets** include optional parameters that provide options for fault tolerance, verbose logging, and preferences for WhatIf and Confirm.</span></span>

<span data-ttu-id="3f804-189">Los **cmdlets \ \* de escritura Mbam** también incluyen un parámetro de *hora* opcional cuyo valor es un objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="3f804-189">The **Write-Mbam\* cmdlets** also include an optional *Time* parameter whose value is a **DateTime** object.</span></span> <span data-ttu-id="3f804-190">Este objeto incluye un atributo *Kind* que puede establecerse en `Local` , `UTC` o `Unspecified` .</span><span class="sxs-lookup"><span data-stu-id="3f804-190">This object includes a *Kind* attribute that can be set to `Local`, `UTC`, or `Unspecified`.</span></span> <span data-ttu-id="3f804-191">Cuando se rellena el parámetro de *hora* a partir de los datos tomados de Active Directory, la hora se convierte en UTC y este atributo de *tipo* se establece automáticamente en `UTC` .</span><span class="sxs-lookup"><span data-stu-id="3f804-191">When the *Time* parameter is populated from data taken from the Active Directory, the time is converted to UTC and this *Kind* attribute is set automatically to `UTC`.</span></span> <span data-ttu-id="3f804-192">Sin embargo, al rellenar el parámetro de *hora* con otro origen, como un archivo de texto, debe establecer explícitamente el atributo *Kind* en el valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="3f804-192">However, when populating the *Time* parameter using another source, such as a text file, you must explicitly set the *Kind* attribute to its appropriate value.</span></span>

<span data-ttu-id="3f804-193">**Nota:**  Los cmdlets de lectura AD \ \* no tienen la capacidad de descubrir las cuentas de usuario que representan a los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="3f804-193">**Note** The Read-AD\* cmdlets do not have the ability to discover the user accounts that represent the computer users.</span></span> <span data-ttu-id="3f804-194">Las asociaciones de cuenta de usuario son necesarias para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3f804-194">User account associations are needed for the following:</span></span>

-   <span data-ttu-id="3f804-195">A los usuarios recuperar las contraseñas y paquetes de volumen mediante el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="3f804-195">Users to recover volume passwords/packages by using the Self-Service portal</span></span>

-   <span data-ttu-id="3f804-196">Usuarios que no se encuentran en el MBAM grupo de seguridad avanzado de los usuarios del servicio de asistencia, como se definieron durante la instalación, recuperar en nombre de otros usuarios</span><span class="sxs-lookup"><span data-stu-id="3f804-196">Users who are not in the MBAM Advanced Helpdesk Users security group as defined during installation, recovering on behalf of other users</span></span>

 

## <a href="" id="bkmk-autounlock"></a><span data-ttu-id="3f804-197">Configurar MBAM para que desbloquee TPM automáticamente después de un bloqueo</span><span class="sxs-lookup"><span data-stu-id="3f804-197">Configure MBAM to automatically unlock the TPM after a lockout</span></span>


<span data-ttu-id="3f804-198">Puede configurar MBAM 2,5 SP1 para que desbloquee automáticamente el TPM en caso de que se bloquee.</span><span class="sxs-lookup"><span data-stu-id="3f804-198">You can configure MBAM 2.5 SP1 to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="3f804-199">Si el restablecimiento automático de bloqueo de TPM está habilitado, MBAM puede detectar que un usuario está bloqueado y, a continuación, obtener la contraseña de OwnerAuth de la base de datos de MBAM para desbloquear automáticamente el TPM para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3f804-199">If TPM lockout auto reset is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span> <span data-ttu-id="3f804-200">El bloqueo automático de bloqueo de TPM solo está disponible si la clave de recuperación del sistema operativo para ese equipo se recuperó usando el portal de autoservicio o el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="3f804-200">TPM lockout auto reset is only available if the OS recovery key for that computer was retrieved by using the Self Service Portal or the Administration and Monitoring Website.</span></span>

<span data-ttu-id="3f804-201">**Importante**  Para habilitar el restablecimiento automático del bloqueo de TPM, debe configurar esta característica en el lado del servidor y en la Directiva de grupo del cliente.</span><span class="sxs-lookup"><span data-stu-id="3f804-201">**Important** To enable TPM lockout auto reset, you must configure this feature on both the server side and in Group Policy on the client side.</span></span>

 

-   <span data-ttu-id="3f804-202">Para habilitar el restablecimiento automático del bloqueo de TPM en el cliente, establezca la configuración de directiva de grupo "configurar el bloqueo automático de bloqueo de TPM", que se encuentra en **configuración de equipo** &gt; **plantillas administrativas** de &gt; **Windows componentes** de &gt; **MDOP MBAM** &gt; **Client Management**.</span><span class="sxs-lookup"><span data-stu-id="3f804-202">To enable TPM lockout auto reset on the client side, configure the Group Policy setting "Configure TPM lockout auto reset" located at **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM** &gt; **Client Management**.</span></span>

-   <span data-ttu-id="3f804-203">Para habilitar el restablecimiento automático del bloqueo de TPM en el servidor, puede activar "habilitar el bloqueo automático de bloqueo de TPM" en el Asistente para la configuración del servidor de MBAM durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="3f804-203">To enable TPM lockout auto reset on the server side, you can check "Enable TPM lockout auto reset" in the MBAM Server Configuration wizard during setup.</span></span>

    <span data-ttu-id="3f804-204">También puede habilitar el restablecimiento automático del bloqueo de TPM en PowerShell especificando el modificador "-TPM bloqueo automático" al habilitar el componente web del servicio agente.</span><span class="sxs-lookup"><span data-stu-id="3f804-204">You can also enable TPM lockout auto reset in PowerShell by specifying the "-TPM lockout auto reset" switch while enabling the agent service web component.</span></span>

<span data-ttu-id="3f804-205">Después de que un usuario haya introducido la clave de recuperación de BitLocker que obtuvo del portal de autoservicio o del sitio web de administración y supervisión, el agente de MBAM determinará si el TPM está bloqueado. Si está bloqueado, intentará recuperar el OwnerAuth de TPM para el equipo de la base de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-205">After a user enters the BitLocker recovery key they obtained from the Self Service Portal or the Administration and Monitoring Website, the MBAM agent will determine if the TPM is locked out. If it is locked out, it will attempt to retrieve the TPM OwnerAuth for the computer from the MBAM database.</span></span> <span data-ttu-id="3f804-206">Si el TPM OwnerAuth se recupera correctamente, se usará para desbloquear el TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-206">If the TPM OwnerAuth is successfully retrieved, it will be used to unlock the TPM.</span></span> <span data-ttu-id="3f804-207">Desbloquear el TPM hace que el TPM sea completamente funcional y el usuario no se verá obligado a escribir la contraseña de recuperación durante el resto de los reinicios desde un bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-207">Unlocking the TPM makes the TPM fully functional and the user will not be forced to enter the recovery password during subsequent reboots from a TPM lockout.</span></span>

<span data-ttu-id="3f804-208">El restablecimiento automático del bloqueo de TPM está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f804-208">TPM lockout auto reset is disabled by default.</span></span>

<span data-ttu-id="3f804-209">**Nota:**  El bloqueo automático de bloqueo de TPM solo se admite en equipos que ejecutan la versión 1,2 de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-209">**Note** TPM lockout auto reset is only supported on computers running TPM version 1.2.</span></span> <span data-ttu-id="3f804-210">El TPM 2,0 proporciona funciones de bloqueo automático de bloqueo integrado.</span><span class="sxs-lookup"><span data-stu-id="3f804-210">TPM 2.0 provides built-in lockout auto reset functionality.</span></span>

 

<span data-ttu-id="3f804-211">**El informe de auditoría de recuperación** incluye eventos relacionados con el restablecimiento automático del bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f804-211">**The Recovery Audit Report** includes events related to TPM lockout auto reset.</span></span> <span data-ttu-id="3f804-212">Si una solicitud se realiza desde el cliente de MBAM para recuperar una contraseña de OwnerAuth de TPM, se registra un evento para indicar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="3f804-212">If a request is made from the MBAM client to retrieve a TPM OwnerAuth password, an event is logged to indicate recovery.</span></span> <span data-ttu-id="3f804-213">Las entradas de auditoría incluirán los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="3f804-213">Audit entries will include the following events:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f804-214">MOV</span><span class="sxs-lookup"><span data-stu-id="3f804-214">Entry</span></span></th>
<th align="left"><span data-ttu-id="3f804-215">Valor</span><span class="sxs-lookup"><span data-stu-id="3f804-215">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f804-216">Origen de solicitud de auditoría</span><span class="sxs-lookup"><span data-stu-id="3f804-216">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f804-217">Desbloquear TPM del agente</span><span class="sxs-lookup"><span data-stu-id="3f804-217">Agent TPM unlock</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f804-218">Tipo de clave</span><span class="sxs-lookup"><span data-stu-id="3f804-218">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f804-219">Hash de contraseña de TPM</span><span class="sxs-lookup"><span data-stu-id="3f804-219">TPM Password Hash</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f804-220">Descripción del motivo</span><span class="sxs-lookup"><span data-stu-id="3f804-220">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f804-221">Reinicio de TPM</span><span class="sxs-lookup"><span data-stu-id="3f804-221">TPM Reset</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a><span data-ttu-id="3f804-222">Conexiones seguras a SQL Server</span><span class="sxs-lookup"><span data-stu-id="3f804-222">Secure connections to SQL Server</span></span>


<span data-ttu-id="3f804-223">En MBAM, SQL Server se comunica con SQL Server Reporting Services y con los servicios web para el sitio web de administración y supervisión y el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="3f804-223">In MBAM, SQL Server communicates with SQL Server Reporting Services and with the web services for the Administration and Monitoring Website and Self-Service Portal.</span></span> <span data-ttu-id="3f804-224">Le recomendamos que proteja la comunicación con SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3f804-224">We recommend that you secure the communication with SQL Server.</span></span> <span data-ttu-id="3f804-225">Para obtener más información, consulte [cifrar conexiones a SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f804-225">For more information, see [Encrypting Connections to SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span></span>

<span data-ttu-id="3f804-226">Para obtener más información sobre cómo proteger los sitios web de MBAM, consulte [planificación de la seguridad de los sitios web de MBAM](planning-how-to-secure-the-mbam-websites.md).</span><span class="sxs-lookup"><span data-stu-id="3f804-226">For more information about securing the MBAM websites, see [Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md).</span></span>

## <a href="" id="bkmk-accts-groups"></a><span data-ttu-id="3f804-227">Crear cuentas y grupos</span><span class="sxs-lookup"><span data-stu-id="3f804-227">Create accounts and groups</span></span>


<span data-ttu-id="3f804-228">El procedimiento recomendado para administrar cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f804-228">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="3f804-229">Para obtener una descripción de las cuentas y grupos recomendados, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="3f804-229">For a description of the recommended accounts and groups, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

## <a href="" id="bkmk-logfiles"></a><span data-ttu-id="3f804-230">Usar archivos de registro de MBAM</span><span class="sxs-lookup"><span data-stu-id="3f804-230">Use MBAM log files</span></span>


<span data-ttu-id="3f804-231">En esta sección se describen los archivos de registro de MBAM Server y MBAM Client.</span><span class="sxs-lookup"><span data-stu-id="3f804-231">This section describes the MBAM Server and MBAM Client log files.</span></span>

**<span data-ttu-id="3f804-232">Archivos de registro de instalación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="3f804-232">MBAM Server Setup log files</span></span>**

<span data-ttu-id="3f804-233">El archivo de **MBAMServerSetup.exe** genera los siguientes archivos de registro en la carpeta **% temp%** del usuario durante la instalación de MBAM:</span><span class="sxs-lookup"><span data-stu-id="3f804-233">The **MBAMServerSetup.exe** file generates the following log files in the user’s **%temp%** folder during the MBAM installation:</span></span>

-   **<span data-ttu-id="3f804-234">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log</span><span class="sxs-lookup"><span data-stu-id="3f804-234">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14 numbers&gt;.log</span></span>**

    <span data-ttu-id="3f804-235">Registra las acciones realizadas durante el programa de instalación de MBAM y la configuración de características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-235">Logs the actions taken during the MBAM setup and the MBAM Server feature configuration.</span></span>

-   **<span data-ttu-id="3f804-236">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="3f804-236">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14\_numbers&gt;\_0\_MBAMServer.msi.log</span></span>**

    <span data-ttu-id="3f804-237">Registra las acciones adicionales tomadas durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="3f804-237">Logs additional action taken during installation.</span></span>

**<span data-ttu-id="3f804-238">Archivos de registro de configuración de servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="3f804-238">MBAM Server Configuration log files</span></span>**

-   **<span data-ttu-id="3f804-239">Registros de aplicaciones y servicios/Microsoft Windows/MBAM-configuración</span><span class="sxs-lookup"><span data-stu-id="3f804-239">Applications and Services Logs/Microsoft Windows/MBAM-Setup</span></span>**

    <span data-ttu-id="3f804-240">Registra los errores que se producen al usar cmdlets de Windows PowerShell o el Asistente para la configuración del servidor de MBAM para configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-240">Logs the errors that occur when you are using Windows Powershell cmdlets or the MBAM Server Configuration wizard to configure the MBAM Server features.</span></span>

**<span data-ttu-id="3f804-241">Archivos de registro de configuración de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="3f804-241">MBAM Client setup log files</span></span>**

-   **<span data-ttu-id="3f804-242">MSI &lt; cinco caracteres aleatorios &gt; . log</span><span class="sxs-lookup"><span data-stu-id="3f804-242">MSI&lt;five random characters&gt;.log</span></span>**

    <span data-ttu-id="3f804-243">Registra las acciones tomadas durante la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-243">Logs the actions taken during the MBAM Client installation.</span></span>

**<span data-ttu-id="3f804-244">MBAM: archivos de registro web</span><span class="sxs-lookup"><span data-stu-id="3f804-244">MBAM-Web log files</span></span>**

-   <span data-ttu-id="3f804-245">Muestra la actividad de los servicios y los portales web.</span><span class="sxs-lookup"><span data-stu-id="3f804-245">Shows activity from the web portals and services.</span></span>

## <a href="" id="bkmk-tde"></a><span data-ttu-id="3f804-246">Revisar las consideraciones de la base de datos de MBAM TDE</span><span class="sxs-lookup"><span data-stu-id="3f804-246">Review MBAM database TDE considerations</span></span>


<span data-ttu-id="3f804-247">La característica de cifrado de datos transparente (TDE) que está disponible en SQL Server es una instalación opcional para las instancias de base de datos que hospedarán las características de base de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-247">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host the MBAM database features.</span></span>

<span data-ttu-id="3f804-248">Con TDE, puede realizar un cifrado de nivel de base de datos completo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3f804-248">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="3f804-249">TDE es la mejor opción para el cifrado en masa para cumplir con los estándares de seguridad de datos corporativos o de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="3f804-249">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="3f804-250">TDE funciona en el nivel de archivo, que es similar a dos características de Windows: el sistema de archivos de cifrado (EFS) y el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3f804-250">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption.</span></span> <span data-ttu-id="3f804-251">Ambas características también cifran los datos del disco duro.</span><span class="sxs-lookup"><span data-stu-id="3f804-251">Both features also encrypt data on the hard drive.</span></span> <span data-ttu-id="3f804-252">TDE no reemplaza el cifrado de nivel de celda, EFS ni BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3f804-252">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="3f804-253">Cuando TDE está habilitado en una base de datos, se cifran todas las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3f804-253">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="3f804-254">Por lo tanto, se debe tener especial cuidado para asegurarse de que se realice una copia de seguridad del certificado que se usó para proteger la clave de cifrado de la base de datos con la copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f804-254">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="3f804-255">Si este certificado (o certificados) se pierde, no se podrán leer los datos.</span><span class="sxs-lookup"><span data-stu-id="3f804-255">If this certificate (or certificates) is lost, the data will be unreadable.</span></span>

<span data-ttu-id="3f804-256">Haga una copia de seguridad del certificado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f804-256">Back up the certificate with the database.</span></span> <span data-ttu-id="3f804-257">Cada copia de seguridad de certificado debe tener dos archivos.</span><span class="sxs-lookup"><span data-stu-id="3f804-257">Each certificate backup should have two files.</span></span> <span data-ttu-id="3f804-258">Ambos archivos deben archivarse.</span><span class="sxs-lookup"><span data-stu-id="3f804-258">Both of these files should be archived.</span></span> <span data-ttu-id="3f804-259">Lo ideal es que se haga una copia de seguridad de ellos por separado del archivo de copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f804-259">Ideally for security, they should be backed up separately from the database backup file.</span></span> <span data-ttu-id="3f804-260">También puede considerar la posibilidad de usar la característica Administración de claves extensible (EKM) (consulte Administración de claves extensible) para almacenar y mantener las claves que se usan para TDE.</span><span class="sxs-lookup"><span data-stu-id="3f804-260">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys that are used for TDE.</span></span>

<span data-ttu-id="3f804-261">Para obtener un ejemplo de cómo habilitar TDE para MBAM instancias de base de [datos, vea comprender el cifrado de datos transparente (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f804-261">For an example of how to enable TDE for MBAM database instances, see [Understanding Transparent Data Encryption (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span></span>

## <a href="" id="bkmk-general-security"></a><span data-ttu-id="3f804-262">Comprender las consideraciones generales de seguridad</span><span class="sxs-lookup"><span data-stu-id="3f804-262">Understand general security considerations</span></span>


**<span data-ttu-id="3f804-263">Comprender los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3f804-263">Understand the security risks.</span></span>** <span data-ttu-id="3f804-264">El riesgo más grave cuando use la administración y la supervisión de Microsoft BitLocker es que un usuario no autorizado podría comprometerse con su funcionalidad, que podría volver a configurar el cifrado de unidad BitLocker y obtener los datos de la clave de cifrado BitLocker en clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-264">The most serious risk when you use Microsoft BitLocker Administration and Monitoring is that its functionality could be compromised by an unauthorized user who could then reconfigure BitLocker Drive Encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="3f804-265">Sin embargo, la pérdida de la funcionalidad de MBAM por un breve período de tiempo, debido a un ataque de denegación de servicio, generalmente no tiene un impacto catastrófico, a diferencia de, por ejemplo, la pérdida de mensajes de correo electrónico o comunicaciones de red o la energía.</span><span class="sxs-lookup"><span data-stu-id="3f804-265">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, losing e-mail or network communications, or power.</span></span>

<span data-ttu-id="3f804-266">**Proteja físicamente sus equipos**.</span><span class="sxs-lookup"><span data-stu-id="3f804-266">**Physically secure your computers**.</span></span> <span data-ttu-id="3f804-267">No hay seguridad sin seguridad física.</span><span class="sxs-lookup"><span data-stu-id="3f804-267">There is no security without physical security.</span></span> <span data-ttu-id="3f804-268">Un atacante que obtiene acceso físico a un servidor de MBAM puede utilizarlo para atacar a toda la base de clientes.</span><span class="sxs-lookup"><span data-stu-id="3f804-268">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="3f804-269">Todos los posibles ataques físicos se deben considerar de alto riesgo y se pueden mitigar correctamente.</span><span class="sxs-lookup"><span data-stu-id="3f804-269">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="3f804-270">Los servidores de MBAM deben almacenarse en una sala de servidores segura con acceso controlado.</span><span class="sxs-lookup"><span data-stu-id="3f804-270">MBAM Servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="3f804-271">Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.</span><span class="sxs-lookup"><span data-stu-id="3f804-271">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="3f804-272">**Aplique las actualizaciones de seguridad más recientes a todos los equipos**.</span><span class="sxs-lookup"><span data-stu-id="3f804-272">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="3f804-273">Manténgase informado acerca de las nuevas actualizaciones de sistemas operativos de Windows, SQL Server y MBAM al suscribirse al servicio de notificaciones de seguridad en el [TechCenter de seguridad](https://go.microsoft.com/fwlink/?LinkId=28819).</span><span class="sxs-lookup"><span data-stu-id="3f804-273">Stay informed about new updates for Windows operating systems, SQL Server, and MBAM by subscribing to the Security Notification service at the [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819).</span></span>

<span data-ttu-id="3f804-274">**Use contraseñas seguras o frases**.</span><span class="sxs-lookup"><span data-stu-id="3f804-274">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="3f804-275">Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f804-275">Always use strong passwords with 15 or more characters for all MBAM administrator accounts.</span></span> <span data-ttu-id="3f804-276">Nunca use contraseñas en blanco.</span><span class="sxs-lookup"><span data-stu-id="3f804-276">Never use blank passwords.</span></span> <span data-ttu-id="3f804-277">Para obtener más información sobre los conceptos de contraseñas, consulte [Directiva de contraseñas](https://technet.microsoft.com/library/hh994572.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f804-277">For more information about password concepts, see [Password Policy](https://technet.microsoft.com/library/hh994572.aspx).</span></span>



## <span data-ttu-id="3f804-278">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f804-278">Related topics</span></span>


[<span data-ttu-id="3f804-279">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3f804-279">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 
## <span data-ttu-id="3f804-280">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="3f804-280">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3f804-281">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3f804-281">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="3f804-282">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3f804-282">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





