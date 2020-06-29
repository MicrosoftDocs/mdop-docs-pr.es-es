---
title: Autenticación de los usuarios finales de MED-V
description: Autenticación de los usuarios finales de MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824890"
---
# <span data-ttu-id="31f7e-103">Autenticación de los usuarios finales de MED-V</span><span class="sxs-lookup"><span data-stu-id="31f7e-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="31f7e-104">La autenticación de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 usuarios finales es un problema de seguridad muy importante.</span><span class="sxs-lookup"><span data-stu-id="31f7e-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="31f7e-105">En este contexto, la autenticación hace referencia a comprobar la identidad del usuario final de MED-V.</span><span class="sxs-lookup"><span data-stu-id="31f7e-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="31f7e-106">En la sección siguiente se proporciona información y orientación sobre la autenticación de usuario final en MED-V.</span><span class="sxs-lookup"><span data-stu-id="31f7e-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="31f7e-107">Autenticación de usuario en MED-V</span><span class="sxs-lookup"><span data-stu-id="31f7e-107">User Authentication in MED-V</span></span>


<span data-ttu-id="31f7e-108">Normalmente, la autenticación en MED-V se produce en dos niveles: cuando un usuario accede por primera vez a MED-V y cada vez que cambian su contraseña.</span><span class="sxs-lookup"><span data-stu-id="31f7e-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="31f7e-109">En función de cómo haya configurado la configuración de MED-V para la autenticación, normalmente se le solicitará al usuario final que escriba su contraseña, ya sea la primera vez que se inicie MED-V o la primera vez que intenten abrir una aplicación publicada.</span><span class="sxs-lookup"><span data-stu-id="31f7e-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="31f7e-110">Existen varios aspectos de la autenticación de usuario final que puede controlar, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="31f7e-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="31f7e-111">Si las credenciales que escribe el usuario final se almacenan en el administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="31f7e-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="31f7e-112">En qué forma se presenta al usuario final la opción de escribir y guardar su contraseña</span><span class="sxs-lookup"><span data-stu-id="31f7e-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="31f7e-113">Según el proceso preferido de su empresa para administrar la autenticación de usuario final, puede especificar si el almacenamiento en caché de las credenciales se produce para un área de trabajo de MED-V en particular.</span><span class="sxs-lookup"><span data-stu-id="31f7e-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="31f7e-114">El almacenamiento en caché de las credenciales de un usuario final es útil porque solo se le solicitan una vez para su contraseña.</span><span class="sxs-lookup"><span data-stu-id="31f7e-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="31f7e-115">Si el usuario final no tiene permiso para guardar su contraseña o decide no hacerlo, cada vez que inicie una nueva sesión de MED-V, debe escribirla de nuevo.</span><span class="sxs-lookup"><span data-stu-id="31f7e-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="31f7e-116">Por ejemplo, si MED-V está configurado para iniciarse cuando el usuario final inicia sesión en el host pero la autenticación está deshabilitada, el usuario final solo se le solicita una vez durante el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="31f7e-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="31f7e-117">En este caso, las credenciales son válidas hasta que el usuario final cierra la sesión en el host.</span><span class="sxs-lookup"><span data-stu-id="31f7e-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="31f7e-118">Si es necesario, puede usar el administrador de credenciales para quitar todas las credenciales de usuario final almacenadas.</span><span class="sxs-lookup"><span data-stu-id="31f7e-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="31f7e-119">De forma predeterminada, el almacenamiento de credenciales está deshabilitado, pero puede cambiar esta configuración mediante uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="31f7e-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="31f7e-120">**Mientras crea el paquete de área de trabajo MED-V**.</span><span class="sxs-lookup"><span data-stu-id="31f7e-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="31f7e-121">Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="31f7e-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="31f7e-122">**Después de implementar el área de trabajo de MED-V**.</span><span class="sxs-lookup"><span data-stu-id="31f7e-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="31f7e-123">Edite el parámetro del cmdlet MED-V UxCredentialCacheEnabled para establecer la clave del registro de servicios de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="31f7e-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="31f7e-124">Para obtener más información, vea la ayuda de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31f7e-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="31f7e-125">Después de la implementación del área de trabajo de MED-V, puede establecer su preferencia para la autenticación de usuarios finales modificando la Directiva de servicios de Terminal Server denominada DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="31f7e-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="31f7e-126">DisablePasswordSaving controla si la casilla de verificación de contraseñas se ve en la ventana del cuadro de diálogo del cliente RDP y si se muestra el símbolo del sistema de credenciales MED-V.</span><span class="sxs-lookup"><span data-stu-id="31f7e-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="31f7e-127">A continuación se encuentra la ruta de directiva para la Directiva de servicios de Terminal Server denominada DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="31f7e-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="31f7e-128">Regedit</span><span class="sxs-lookup"><span data-stu-id="31f7e-128">Regedit:</span></span>**

<span data-ttu-id="31f7e-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="31f7e-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="31f7e-130">Nota</span><span class="sxs-lookup"><span data-stu-id="31f7e-130">Note</span></span>**  
<span data-ttu-id="31f7e-131">Los cambios que realice en DisablePasswordSaving solo afectan al símbolo del sistema de RDP a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="31f7e-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="31f7e-132">En la tabla siguiente se enumeran las diferentes maneras en las que puede configurar las opciones de almacenamiento de credenciales y los efectos de las distintas configuraciones:</span><span class="sxs-lookup"><span data-stu-id="31f7e-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="31f7e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="31f7e-133">Value</span></span></th>
<th align="left"><span data-ttu-id="31f7e-134">Configuración</span><span class="sxs-lookup"><span data-stu-id="31f7e-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="31f7e-135">Resultado</span><span class="sxs-lookup"><span data-stu-id="31f7e-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31f7e-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="31f7e-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="31f7e-137">Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="31f7e-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31f7e-138">Se presenta el símbolo del sistema MED-V y la casilla para aceptar está disponible y desactivada.</span><span class="sxs-lookup"><span data-stu-id="31f7e-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="31f7e-139">Si el usuario final activa la casilla, las credenciales se almacenan en caché para usarlas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="31f7e-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="31f7e-140">El usuario final también tiene la ventaja de que solo se le pregunte cuando la contraseña venza.</span><span class="sxs-lookup"><span data-stu-id="31f7e-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="31f7e-141">Si el usuario final no activa la casilla, se muestra el mensaje de cliente de conexión a escritorio remoto (RDC) en lugar del símbolo de MED-V y la casilla de verificación aceptar está desactivada.</span><span class="sxs-lookup"><span data-stu-id="31f7e-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="31f7e-142">Si el usuario final activa la casilla, la credencial del cliente RDC se almacena para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="31f7e-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="31f7e-143">Importante</span><span class="sxs-lookup"><span data-stu-id="31f7e-143">Important</span></span></strong><br/><p><span data-ttu-id="31f7e-144">RDC no valida las credenciales cuando el usuario final las especifica.</span><span class="sxs-lookup"><span data-stu-id="31f7e-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="31f7e-145">Si el usuario final almacena en caché las credenciales a través del símbolo de línea RDC, hay un riesgo de que se almacenen Credenciales incorrectas.</span><span class="sxs-lookup"><span data-stu-id="31f7e-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="31f7e-146">En este caso, se deben eliminar las credenciales incorrectas en el administrador de credenciales de Windows.</span><span class="sxs-lookup"><span data-stu-id="31f7e-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31f7e-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="31f7e-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="31f7e-148">Habilitado</span><span class="sxs-lookup"><span data-stu-id="31f7e-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="31f7e-149">Nota</span><span class="sxs-lookup"><span data-stu-id="31f7e-149">Note</span></span></strong><br/><p><span data-ttu-id="31f7e-150">Esta configuración es más segura porque no permite almacenar las credenciales de usuario final.</span><span class="sxs-lookup"><span data-stu-id="31f7e-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="31f7e-151">De forma predeterminada, la instalación de MED-V configura una clave del registro en el invitado para suprimir el mensaje "la contraseña está a punto de expirar".</span><span class="sxs-lookup"><span data-stu-id="31f7e-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="31f7e-152">El usuario final solo tiene que cambiar la contraseña en el host.</span><span class="sxs-lookup"><span data-stu-id="31f7e-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="31f7e-153">Las credenciales que se actualizan en el host se pasan al invitado.</span><span class="sxs-lookup"><span data-stu-id="31f7e-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="31f7e-154">Actúe</span><span class="sxs-lookup"><span data-stu-id="31f7e-154">Caution</span></span>**  
<span data-ttu-id="31f7e-155">Si usa una directiva de grupo en su entorno, sabrá que puede invalidar la clave del registro, lo que provocará que las solicitudes de contraseña del invitado vuelvan a aparecer.</span><span class="sxs-lookup"><span data-stu-id="31f7e-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="31f7e-156">Problemas de seguridad con la autenticación</span><span class="sxs-lookup"><span data-stu-id="31f7e-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="31f7e-157">Aunque el almacenamiento en caché de las credenciales del usuario final proporcione la mejor experiencia de usuario, debe tener en cuenta los riesgos implicados.</span><span class="sxs-lookup"><span data-stu-id="31f7e-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="31f7e-158">Cuando el almacenamiento en caché de credenciales está habilitado, la credencial de dominio del usuario final se almacena en un formato reversible dentro del administrador de credenciales de Windows.</span><span class="sxs-lookup"><span data-stu-id="31f7e-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="31f7e-159">Como resultado, un atacante podría escribir una herramienta que se ejecute como un proceso de nivel de sistema o un proceso de usuario final y que recupere las credenciales del usuario final.</span><span class="sxs-lookup"><span data-stu-id="31f7e-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="31f7e-160">Solo puede reducir este riesgo si establece DisablePasswordSaving en **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="31f7e-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="31f7e-161">Esta misma preocupación se produce cuando la autenticación de MED-V está deshabilitada, pero la configuración de directiva de servicios de Terminal Server está habilitada.</span><span class="sxs-lookup"><span data-stu-id="31f7e-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="31f7e-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31f7e-162">Related topics</span></span>


[<span data-ttu-id="31f7e-163">Procedimientos recomendados de seguridad para las operaciones de MED-V</span><span class="sxs-lookup"><span data-stu-id="31f7e-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









