---
title: Consideraciones de seguridad de App-V 5.0
description: Consideraciones de seguridad de App-V 5.0
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814807"
---
# <span data-ttu-id="86a55-103">Consideraciones de seguridad de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="86a55-103">App-V 5.0 Security Considerations</span></span>


<span data-ttu-id="86a55-104">Este tema contiene una breve descripción general de las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for App-V 5.0.</span></span>

**<span data-ttu-id="86a55-105">Importante</span><span class="sxs-lookup"><span data-stu-id="86a55-105">Important</span></span>**  
<span data-ttu-id="86a55-106">App-V 5,0 no es un producto de seguridad y no proporciona ninguna garantía para un entorno seguro.</span><span class="sxs-lookup"><span data-stu-id="86a55-106">App-V 5.0 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="86a55-107">La característica PackageStoreAccessControl (PSAC) ha quedado obsoleta</span><span class="sxs-lookup"><span data-stu-id="86a55-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="86a55-108">Desde el 2014 de junio de, la característica PackageStoreAccessControl (PSAC) que se introdujo en Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) ha quedado obsoleta en entornos con un único usuario y varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="86a55-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="86a55-109">Consideraciones generales de seguridad</span><span class="sxs-lookup"><span data-stu-id="86a55-109">General security considerations</span></span>


**<span data-ttu-id="86a55-110">Comprender los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="86a55-110">Understand the security risks.</span></span>** <span data-ttu-id="86a55-111">El riesgo más serio para App-V 5,0 es que un usuario no autorizado pudiera secuestrar su funcionalidad, que podría volver a configurar los datos clave en los clientes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-111">The most serious risk to App-V 5.0 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.0 clients.</span></span> <span data-ttu-id="86a55-112">La pérdida de la funcionalidad de App-V 5,0 durante un breve período de tiempo debido a un ataque de denegación de servicio generalmente no tendría un impacto catastrófico.</span><span class="sxs-lookup"><span data-stu-id="86a55-112">The loss of App-V 5.0 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="86a55-113">**Proteja físicamente sus equipos**.</span><span class="sxs-lookup"><span data-stu-id="86a55-113">**Physically secure your computers**.</span></span> <span data-ttu-id="86a55-114">La seguridad está incompleta sin seguridad física.</span><span class="sxs-lookup"><span data-stu-id="86a55-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="86a55-115">Cualquier persona que tenga acceso físico a un servidor de App-V 5,0 podría atacar toda la base de clientes.</span><span class="sxs-lookup"><span data-stu-id="86a55-115">Anyone with physical access to an App-V 5.0 server could potentially attack the entire client base.</span></span> <span data-ttu-id="86a55-116">Cualquier posible ataque físico debe considerarse de alto riesgo y mitigarse de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="86a55-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="86a55-117">Los servidores de App-V 5,0 deben almacenarse en una sala de servidores físicamente segura con acceso controlado.</span><span class="sxs-lookup"><span data-stu-id="86a55-117">App-V 5.0 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="86a55-118">Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.</span><span class="sxs-lookup"><span data-stu-id="86a55-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="86a55-119">**Aplique las actualizaciones de seguridad más recientes a todos los equipos**.</span><span class="sxs-lookup"><span data-stu-id="86a55-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="86a55-120">Para mantenerse informado acerca de las actualizaciones más recientes para sistemas operativos, Microsoft SQL Server y App-V 5,0, suscríbase al servicio de notificación de seguridad ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="86a55-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.0, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="86a55-121">**Use contraseñas seguras o frases**.</span><span class="sxs-lookup"><span data-stu-id="86a55-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="86a55-122">Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de App-V 5,0 y de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-122">Always use strong passwords with 15 or more characters for all App-V 5.0 and App-V 5.0 administrator accounts.</span></span> <span data-ttu-id="86a55-123">Nunca use contraseñas en blanco.</span><span class="sxs-lookup"><span data-stu-id="86a55-123">Never use blank passwords.</span></span> <span data-ttu-id="86a55-124">Para obtener más información sobre los conceptos de contraseñas, consulte las notas del producto "directivas y contraseñas de la cuenta" en TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="86a55-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="86a55-125">Cuentas y grupos en App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="86a55-125">Accounts and groups in App-V 5.0</span></span>


<span data-ttu-id="86a55-126">Un procedimiento recomendado para la administración de cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="86a55-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="86a55-127">Después, agregue las cuentas globales de dominio a los grupos locales App-V 5,0 en los servidores App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-127">Then, add the domain global accounts to the necessary App-V 5.0 local groups on the App-V 5.0 servers.</span></span>

**<span data-ttu-id="86a55-128">Nota</span><span class="sxs-lookup"><span data-stu-id="86a55-128">Note</span></span>**  
<span data-ttu-id="86a55-129">Las cuentas de equipos cliente de App-V que necesitan conectarse al servidor de publicación deben formar parte del grupo local de **usuarios** del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="86a55-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="86a55-130">De forma predeterminada, todos los equipos del dominio forman parte del grupo **usuarios autorizados** , que forma parte del grupo local **usuarios** .</span><span class="sxs-lookup"><span data-stu-id="86a55-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-0-server-security"></a> <span data-ttu-id="86a55-131">Seguridad del servidor de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="86a55-131">App-V 5.0 server security</span></span>

<span data-ttu-id="86a55-132">Durante la instalación de App-V 5,0 no se crean grupos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="86a55-132">No groups are created automatically during App-V 5.0 Setup.</span></span> <span data-ttu-id="86a55-133">Debe crear los siguientes grupos globales de servicios de dominio de Active Directory para administrar las operaciones del servidor de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.0 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86a55-134">Nombre de grupo</span><span class="sxs-lookup"><span data-stu-id="86a55-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="86a55-135">Detalles</span><span class="sxs-lookup"><span data-stu-id="86a55-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86a55-136">Grupo de administradores de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="86a55-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="86a55-137">Se usa para administrar el servidor de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-137">Used to manage the App-V 5.0 management server.</span></span> <span data-ttu-id="86a55-138">Este grupo se crea durante la instalación de servidor de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-138">This group is created during the App-V 5.0 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86a55-139">Importante</span><span class="sxs-lookup"><span data-stu-id="86a55-139">Important</span></span></strong><br/><p><span data-ttu-id="86a55-140">No hay ningún método para crear el grupo con la consola de administración una vez completada la instalación.</span><span class="sxs-lookup"><span data-stu-id="86a55-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86a55-141">Base de datos de lectura/escritura para la cuenta del servicio de administración</span><span class="sxs-lookup"><span data-stu-id="86a55-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="86a55-142">Proporciona acceso de lectura y escritura a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="86a55-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="86a55-143">Esta cuenta debe crearse durante la instalación de la base de datos de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-143">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86a55-144">Instalación de la cuenta de administrador del servicio de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="86a55-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86a55-145">Nota</span><span class="sxs-lookup"><span data-stu-id="86a55-145">Note</span></span></strong><br/><p><span data-ttu-id="86a55-146">Esto solo es necesario si la base de datos de administración se instala por separado del servicio.</span><span class="sxs-lookup"><span data-stu-id="86a55-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="86a55-147">Proporciona acceso público a la tabla de versión de esquema de la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="86a55-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="86a55-148">Esta cuenta debe crearse durante la instalación de la base de datos de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-148">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86a55-149">Instalación de la cuenta de administrador de App-V Reporting Service</span><span class="sxs-lookup"><span data-stu-id="86a55-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86a55-150">Nota</span><span class="sxs-lookup"><span data-stu-id="86a55-150">Note</span></span></strong><br/><p><span data-ttu-id="86a55-151">Esto solo es necesario si la base de datos de informes se instala por separado del servicio.</span><span class="sxs-lookup"><span data-stu-id="86a55-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="86a55-152">Acceso público a la tabla de versión de esquema de la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="86a55-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="86a55-153">Esta cuenta debe crearse durante la instalación de la base de datos de informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="86a55-153">This account should be created during the App-V 5.0 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="86a55-154">Considere la siguiente información adicional:</span><span class="sxs-lookup"><span data-stu-id="86a55-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="86a55-155">Acceso a los recursos compartidos del paquete: Si un recurso compartido se encuentra en el mismo equipo que el servidor de administración, el servicio de **red** requiere acceso de lectura al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="86a55-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="86a55-156">Además, cada equipo cliente de App-V debe tener acceso de lectura al recurso compartido de paquete.</span><span class="sxs-lookup"><span data-stu-id="86a55-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="86a55-157">Nota</span><span class="sxs-lookup"><span data-stu-id="86a55-157">Note</span></span>**  
    <span data-ttu-id="86a55-158">En versiones anteriores de App-V, el recurso compartido de paquetes se denominaba recurso compartido de contenido.</span><span class="sxs-lookup"><span data-stu-id="86a55-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="86a55-159">Registrar servidores de publicación con el servidor de administración: un servidor de publicación debe estar registrado en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="86a55-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="86a55-160">Por ejemplo, debe agregarse a la base de datos para que las cuentas del equipo del servidor de publicación puedan llamar a la API del servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="86a55-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-0-package-security"></a> <span data-ttu-id="86a55-161">Seguridad del paquete de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="86a55-161">App-V 5.0 package security</span></span>

<span data-ttu-id="86a55-162">Lo siguiente le ayudará a planear cómo asegurarse de que los paquetes virtualizados sean seguros.</span><span class="sxs-lookup"><span data-stu-id="86a55-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="86a55-163">Si un instalador de aplicaciones aplica una lista de control de acceso (ACL) a un archivo o directorio, esa ACL no se conserva en el paquete.</span><span class="sxs-lookup"><span data-stu-id="86a55-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="86a55-164">Cuando se implementa el paquete, si un usuario modifica el archivo o el directorio, este heredará la ACL en **% userprofile%** o heredará la ACL del directorio del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="86a55-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="86a55-165">El primer caso se da si el archivo o directorio no existe en una ubicación de un sistema de archivos virtual; el último caso se produce si el archivo o el directorio existe en una ubicación del sistema de archivos virtual, por ejemplo, **% WINDIR%**.</span><span class="sxs-lookup"><span data-stu-id="86a55-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-0-log-files"></a> <span data-ttu-id="86a55-166">Archivos de registro de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="86a55-166">App-V 5.0 log files</span></span>


<span data-ttu-id="86a55-167">Durante la instalación de App-V 5,0, los archivos de registro de configuración se crean en la carpeta **% temp%** del usuario de instalación.</span><span class="sxs-lookup"><span data-stu-id="86a55-167">During App-V 5.0 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>
