---
title: Consideraciones de seguridad de UE-V 1.0
description: Consideraciones de seguridad de UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824000"
---
# <span data-ttu-id="fc32f-103">Consideraciones de seguridad de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fc32f-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="fc32f-104">Este tema contiene una breve introducción a las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad de la virtualización de la experiencia del usuario de Microsoft (UE-V).</span><span class="sxs-lookup"><span data-stu-id="fc32f-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="fc32f-105">Para obtener más información, siga los vínculos que se proporcionan aquí.</span><span class="sxs-lookup"><span data-stu-id="fc32f-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="fc32f-106">Consideraciones de seguridad para la configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="fc32f-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="fc32f-107">Cuando cree el recurso compartido de almacenamiento de configuración, limite el acceso compartido a los usuarios que necesitan acceso.</span><span class="sxs-lookup"><span data-stu-id="fc32f-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="fc32f-108">Como los paquetes de configuración pueden contener información personal, debe tener cuidado para protegerlos de la mejor manera posible.</span><span class="sxs-lookup"><span data-stu-id="fc32f-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="fc32f-109">En general, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc32f-109">In general, do the following:</span></span>

-   <span data-ttu-id="fc32f-110">Restringir el uso compartido solo a los usuarios que lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="fc32f-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="fc32f-111">Cree un grupo de seguridad para los usuarios que tengan carpetas redirigidas en un determinado recurso compartido y limite el acceso a solo esos usuarios.</span><span class="sxs-lookup"><span data-stu-id="fc32f-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="fc32f-112">Cuando crees el uso compartido, oculta el uso compartido colocando un $ después del nombre compartido.</span><span class="sxs-lookup"><span data-stu-id="fc32f-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="fc32f-113">Esto ocultará el uso compartido de los exploradores ocasionales y el uso compartido no se verá en mis sitios de red.</span><span class="sxs-lookup"><span data-stu-id="fc32f-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="fc32f-114">Otorgue a los usuarios la cantidad mínima de permisos necesarios.</span><span class="sxs-lookup"><span data-stu-id="fc32f-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="fc32f-115">Los permisos necesarios se muestran en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="fc32f-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="fc32f-116">Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de ubicación de almacenamiento de configuración:</span><span class="sxs-lookup"><span data-stu-id="fc32f-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="fc32f-117">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="fc32f-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="fc32f-118">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="fc32f-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="fc32f-119">Todos</span><span class="sxs-lookup"><span data-stu-id="fc32f-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="fc32f-120">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="fc32f-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="fc32f-121">Grupo de seguridad de UE-V</span><span class="sxs-lookup"><span data-stu-id="fc32f-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="fc32f-122">Control total</span><span class="sxs-lookup"><span data-stu-id="fc32f-122">Full Control</span></span></p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### <span data-ttu-id="fc32f-123">Usar servidores de Windows Server 2003 o versiones posteriores para hospedar recursos compartidos de archivos redirigidos</span><span class="sxs-lookup"><span data-stu-id="fc32f-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="fc32f-124">Los archivos del paquete de configuración de usuario contienen información personal que se transfiere entre el equipo cliente y el servidor que almacena los paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc32f-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="fc32f-125">Por ello, debe asegurarse de que los datos estén protegidos mientras viajan por la red.</span><span class="sxs-lookup"><span data-stu-id="fc32f-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="fc32f-126">Los datos de configuración de usuario son vulnerables a estas amenazas potenciales: interceptar los datos a medida que pasan por la red; manipulación de los datos a medida que pasan por la red; y imitación del servidor que hospeda los datos.</span><span class="sxs-lookup"><span data-stu-id="fc32f-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="fc32f-127">Varias características de Windows Server 2003 y versiones posteriores pueden ayudar a proteger los datos de usuario:</span><span class="sxs-lookup"><span data-stu-id="fc32f-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="fc32f-128">**Kerberos** : Kerberos es estándar en todas las versiones de Windows 2000 y windows Server 2003 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="fc32f-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="fc32f-129">Kerberos garantiza el nivel más alto de seguridad para los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="fc32f-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="fc32f-130">NTLM autentica solo al cliente; Kerberos autentica al servidor y al cliente.</span><span class="sxs-lookup"><span data-stu-id="fc32f-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="fc32f-131">Cuando se usa NTLM, el cliente no sabe si el servidor es válido.</span><span class="sxs-lookup"><span data-stu-id="fc32f-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="fc32f-132">Esto es especialmente importante si el cliente intercambia archivos personales con el servidor, como es el caso de los perfiles móviles.</span><span class="sxs-lookup"><span data-stu-id="fc32f-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="fc32f-133">Kerberos proporciona mayor seguridad que NTLM.</span><span class="sxs-lookup"><span data-stu-id="fc32f-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="fc32f-134">Kerberos no está disponible en Windows NT versión 4,0 o en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="fc32f-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="fc32f-135">**IPSec** : el protocolo de seguridad IP (IPSec) proporciona autenticación de nivel de red, integridad de datos y cifrado.</span><span class="sxs-lookup"><span data-stu-id="fc32f-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="fc32f-136">IPsec garantiza lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc32f-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="fc32f-137">Los datos móviles son seguros para la modificación de datos mientras se encuentra en tránsito.</span><span class="sxs-lookup"><span data-stu-id="fc32f-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="fc32f-138">Los datos móviles son seguros para interceptar, ver o copiar.</span><span class="sxs-lookup"><span data-stu-id="fc32f-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="fc32f-139">Es seguro que las personas sin autenticación acceden a los datos móviles.</span><span class="sxs-lookup"><span data-stu-id="fc32f-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="fc32f-140">**Firma SMB** : el protocolo de autenticación de bloque de mensajes de servidor (SMB) admite la autenticación de mensajes que evita los ataques de mensajes activos y "hombre en el medio".</span><span class="sxs-lookup"><span data-stu-id="fc32f-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="fc32f-141">La firma SMB proporciona esta autenticación al colocar una firma digital en cada SMB.</span><span class="sxs-lookup"><span data-stu-id="fc32f-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="fc32f-142">Después, el cliente y el servidor comprueban la firma digital.</span><span class="sxs-lookup"><span data-stu-id="fc32f-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="fc32f-143">Para poder usar la firma SMB, primero debe habilitarla o requerirla en el cliente SMB y en el servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="fc32f-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="fc32f-144">Tenga en cuenta que la firma SMB impone una disminución del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fc32f-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="fc32f-145">No consume más ancho de banda de la red, pero usa más ciclos de CPU en el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fc32f-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="fc32f-146">Usar siempre el sistema de archivos NTFS para los volúmenes que contienen datos de los usuarios</span><span class="sxs-lookup"><span data-stu-id="fc32f-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="fc32f-147">Para obtener la configuración más segura, configure los servidores que hospedan los archivos de configuración de UE-V para que usen el sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="fc32f-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="fc32f-148">A diferencia de FAT, NTFS admite las listas de control de acceso discrecional (DACL) y las listas de control de acceso del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="fc32f-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="fc32f-149">Las DACL y las SACL controlan quién puede realizar operaciones en un archivo y qué eventos desencadenarán el registro de las acciones realizadas en un archivo.</span><span class="sxs-lookup"><span data-stu-id="fc32f-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="fc32f-150">No confíe en EFS para cifrar los archivos de los usuarios cuando se transmitan a través de la red.</span><span class="sxs-lookup"><span data-stu-id="fc32f-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="fc32f-151">Al usar el sistema de archivos cifrados (EFS) para cifrar archivos en un servidor remoto, los datos cifrados no se cifran durante el tránsito a través de la red; Solo se cifrará cuando se almacene en disco.</span><span class="sxs-lookup"><span data-stu-id="fc32f-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="fc32f-152">Las excepciones para ello son cuando el sistema incluye seguridad de protocolo Internet (IPsec) o sistema distribuido de creación y control de versiones web (WebDAV).</span><span class="sxs-lookup"><span data-stu-id="fc32f-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="fc32f-153">IPsec cifra los datos mientras se transfieren a través de una red TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fc32f-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="fc32f-154">Si el archivo está cifrado antes de copiarlo o moverlo a una carpeta WebDAV de un servidor, permanecerá cifrado durante la transmisión y mientras esté almacenado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fc32f-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="fc32f-155">Cifrar la caché de archivos sin conexión</span><span class="sxs-lookup"><span data-stu-id="fc32f-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="fc32f-156">De forma predeterminada, la caché de archivos sin conexión está protegida en particiones NTFS por ACL, pero el cifrado de la caché mejora aún más la seguridad en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="fc32f-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="fc32f-157">De forma predeterminada, la caché del equipo local no está cifrada, por lo que los archivos cifrados almacenados en caché de la red no se cifrarán en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fc32f-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="fc32f-158">Esto puede suponer un riesgo de seguridad en algunos entornos.</span><span class="sxs-lookup"><span data-stu-id="fc32f-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="fc32f-159">Cuando el cifrado está habilitado, todos los archivos de la caché de archivos sin conexión están cifrados.</span><span class="sxs-lookup"><span data-stu-id="fc32f-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="fc32f-160">Esto incluye el cifrado de archivos existentes, así como los archivos que se agregan más tarde.</span><span class="sxs-lookup"><span data-stu-id="fc32f-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="fc32f-161">La copia en caché en el equipo local se ve afectada, pero no la copia de red asociada.</span><span class="sxs-lookup"><span data-stu-id="fc32f-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="fc32f-162">La caché se puede cifrar de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="fc32f-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="fc32f-163">A través de una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="fc32f-163">Via Group Policy.</span></span> <span data-ttu-id="fc32f-164">-Habilite la opción **cifrar la memoria caché de archivos sin conexión** , ubicada en archivos de Configuration\\Administrative Templates\\Network\\Offline de equipo, en el editor de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="fc32f-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="fc32f-165">Automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fc32f-165">Manually.</span></span> <span data-ttu-id="fc32f-166">-Seleccione Herramientas y, a continuación, opciones de carpeta en el menú de comandos del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc32f-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="fc32f-167">Seleccione la pestaña archivos sin conexión y, a continuación, seleccione la casilla **cifrar archivos sin conexión para proteger los datos** .</span><span class="sxs-lookup"><span data-stu-id="fc32f-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="fc32f-168">Dejar que el agente de UE-V cree carpetas para cada usuario</span><span class="sxs-lookup"><span data-stu-id="fc32f-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="fc32f-169">Para asegurarse de que UE-V funcione de manera óptima, cree solo el recurso compartido raíz en el servidor y deje que el agente de UE-V cree las carpetas para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="fc32f-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="fc32f-170">UE-V creará estas carpetas de usuario con la seguridad adecuada.</span><span class="sxs-lookup"><span data-stu-id="fc32f-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="fc32f-171">Esta configuración de permisos permite a los usuarios crear carpetas para el almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc32f-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="fc32f-172">El agente UE-V crea y protege una carpeta settingspackage mientras se ejecuta en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc32f-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="fc32f-173">El usuario recibe control total en su carpeta settingspackage.</span><span class="sxs-lookup"><span data-stu-id="fc32f-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="fc32f-174">Otros usuarios no heredan el acceso a esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc32f-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="fc32f-175">No es necesario crear ni proteger directorios de usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="fc32f-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="fc32f-176">El agente que se ejecuta en el contexto del usuario lo hará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fc32f-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="fc32f-177">Nota</span><span class="sxs-lookup"><span data-stu-id="fc32f-177">Note</span></span>**  
<span data-ttu-id="fc32f-178">Se puede configurar la seguridad adicional cuando se usa un servidor de Windows para el recurso de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc32f-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="fc32f-179">UE-V se puede configurar para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc32f-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="fc32f-180">Para habilitar la seguridad adicional, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="fc32f-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="fc32f-181">Agregue una clave del registro de REG \ _DWORD denominada "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="fc32f-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="fc32f-182">Establezca el valor de la clave del registro en 1.</span><span class="sxs-lookup"><span data-stu-id="fc32f-182">Set registry key value to 1.</span></span>

<span data-ttu-id="fc32f-183">Cuando esta configuración está en vigor, UE-V Agent comprueba que el grupo del administrador local o el usuario actual es el propietario de la carpeta settingspackage.</span><span class="sxs-lookup"><span data-stu-id="fc32f-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="fc32f-184">De lo contrario, UE-V Agent no permitirá el acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc32f-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="fc32f-185">Si tiene que crear carpetas para los usuarios y asegurarse de que tiene los permisos correctos establecidos.</span><span class="sxs-lookup"><span data-stu-id="fc32f-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="fc32f-186">Le recomendamos encarecidamente que no precree carpetas y que, en su lugar, permita que UE-V Agent cree la carpeta para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fc32f-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="fc32f-187">Asegurarse de que se configuran los permisos correctos al almacenar la configuración de UE-V en el directorio principal de un usuario</span><span class="sxs-lookup"><span data-stu-id="fc32f-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="fc32f-188">Si redirige la configuración de UE-V al directorio particular de un usuario, asegúrese de que los permisos en el directorio principal del usuario están establecidos correctamente para su organización.</span><span class="sxs-lookup"><span data-stu-id="fc32f-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="fc32f-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc32f-189">Related topics</span></span>


[<span data-ttu-id="fc32f-190">Seguridad y privacidad para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fc32f-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









