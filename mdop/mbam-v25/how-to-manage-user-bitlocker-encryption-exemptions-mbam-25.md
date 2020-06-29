---
title: Cómo administrar exenciones de cifrado de BitLocker de usuario
description: Cómo administrar exenciones de cifrado de BitLocker de usuario
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826791"
---
# <span data-ttu-id="c6f44-103">Cómo administrar exenciones de cifrado de BitLocker de usuario</span><span class="sxs-lookup"><span data-stu-id="c6f44-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="c6f44-104">Administración y supervisión de Microsoft BitLocker (MBAM) le permite excluir a los usuarios de los requisitos de cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="c6f44-105">Para excluir a los usuarios de la protección de BitLocker, tiene que:</span><span class="sxs-lookup"><span data-stu-id="c6f44-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6f44-106">Tarea</span><span class="sxs-lookup"><span data-stu-id="c6f44-106">Task</span></span></th>
<th align="left"><span data-ttu-id="c6f44-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="c6f44-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6f44-108">Crear una infraestructura para admitir usuarios excluidos.</span><span class="sxs-lookup"><span data-stu-id="c6f44-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6f44-109">Algunos ejemplos de esta infraestructura son proporcionar a los usuarios un número de teléfono de contacto, una página web o una dirección de correo que puedan usar para solicitar una exención.</span><span class="sxs-lookup"><span data-stu-id="c6f44-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6f44-110">Agregue el usuario excluido a un grupo de seguridad para un objeto de directiva de grupo que está configurado específicamente para los usuarios excluidos.</span><span class="sxs-lookup"><span data-stu-id="c6f44-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6f44-111">Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la configuración de directiva de grupo del usuario exime al usuario de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="c6f44-112">La configuración de directiva de grupo del usuario sobrescribe la Directiva de equipo, y el equipo permanecerá exento del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c6f44-113">Nota</span><span class="sxs-lookup"><span data-stu-id="c6f44-113">Note</span></span></strong><br/><p><span data-ttu-id="c6f44-114">MBAM no establece la Directiva de cifrado si el equipo ya está protegido por BitLocker y el usuario está exento.</span><span class="sxs-lookup"><span data-stu-id="c6f44-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="c6f44-115">Sin embargo, si otro usuario no está exento de la Directiva de cifrado inicia sesión en el equipo, tendrá lugar el cifrado.</span><span class="sxs-lookup"><span data-stu-id="c6f44-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c6f44-116">Los pasos siguientes describen lo que ocurre cuando los usuarios finales solicitan una exención del proceso de exención del cifrado de unidad BitLocker a través del cliente MBAM o de cualquier proceso que use su organización.</span><span class="sxs-lookup"><span data-stu-id="c6f44-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="c6f44-117">Debe configurar la configuración de directiva de grupo de MBAM para permitir que los usuarios finales soliciten una exención del cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="c6f44-118">Cuando los usuarios finales inician sesión en un equipo que debe estar cifrado, reciben una notificación de que el equipo se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="c6f44-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="c6f44-119">Pueden seleccionar **exención de solicitud** y posponer el cifrado seleccionando **posponer**o pueden seleccionar **iniciar cifrado** para aceptar el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="c6f44-120">Nota</span><span class="sxs-lookup"><span data-stu-id="c6f44-120">Note</span></span>**  
    <span data-ttu-id="c6f44-121">Al seleccionar **exención de solicitud** , se pospone la protección de BitLocker hasta el tiempo máximo establecido en la Directiva de exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6f44-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="c6f44-122">Si los usuarios finales seleccionan **exención de solicitud**, recibirán una notificación que les indicará que se pongan en contacto con el grupo de administración de BitLocker de la organización.</span><span class="sxs-lookup"><span data-stu-id="c6f44-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="c6f44-123">En función de la configuración de la **directiva configurar excepciones de usuario** , los usuarios disponen de uno o varios de los siguientes métodos de contacto:</span><span class="sxs-lookup"><span data-stu-id="c6f44-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="c6f44-124">Número de teléfono</span><span class="sxs-lookup"><span data-stu-id="c6f44-124">Phone number</span></span>

    -   <span data-ttu-id="c6f44-125">Dirección URL de la página web</span><span class="sxs-lookup"><span data-stu-id="c6f44-125">Webpage URL</span></span>

    -   <span data-ttu-id="c6f44-126">Dirección de correo</span><span class="sxs-lookup"><span data-stu-id="c6f44-126">Mailing address</span></span>

3.  <span data-ttu-id="c6f44-127">Una vez recibida la solicitud de exención, el administrador de MBAM decide si quiere agregar el usuario al grupo servicios de dominio de Active Directory (AD DS) de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="c6f44-128">Después de que un usuario final envía una solicitud de exención, el cliente de MBAM notifica al usuario como "se ha eximido temporalmente".</span><span class="sxs-lookup"><span data-stu-id="c6f44-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="c6f44-129">Después, el cliente espera un número determinado de días, que los administradores de TI han configurado, antes de volver a comprobar el cumplimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="c6f44-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="c6f44-130">Si el administrador de MBAM rechaza la solicitud de exención, la opción de solicitud de exención está desactivada, lo que impide que el usuario vuelva a solicitar la exención.</span><span class="sxs-lookup"><span data-stu-id="c6f44-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="c6f44-131">Administración y supervisión de Microsoft BitLocker (MBAM) le permite excluir a los usuarios de los requisitos de cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="c6f44-132">Para excluir a los usuarios de la protección de BitLocker, tiene que:</span><span class="sxs-lookup"><span data-stu-id="c6f44-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6f44-133">Tarea</span><span class="sxs-lookup"><span data-stu-id="c6f44-133">Task</span></span></th>
<th align="left"><span data-ttu-id="c6f44-134">Detalles</span><span class="sxs-lookup"><span data-stu-id="c6f44-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6f44-135">Crear una infraestructura para admitir usuarios excluidos.</span><span class="sxs-lookup"><span data-stu-id="c6f44-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6f44-136">Algunos ejemplos de esta infraestructura son proporcionar a los usuarios un número de teléfono de contacto, una página web o una dirección de correo que puedan usar para solicitar una exención.</span><span class="sxs-lookup"><span data-stu-id="c6f44-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6f44-137">Agregue el usuario excluido a un grupo de seguridad para un objeto de directiva de grupo que está configurado específicamente para los usuarios excluidos.</span><span class="sxs-lookup"><span data-stu-id="c6f44-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6f44-138">Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la configuración de directiva de grupo del usuario exime al usuario de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="c6f44-139">La configuración de directiva de grupo del usuario sobrescribe la Directiva de equipo, y el equipo permanecerá exento del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c6f44-140">Nota</span><span class="sxs-lookup"><span data-stu-id="c6f44-140">Note</span></span></strong><br/><p><span data-ttu-id="c6f44-141">Si el equipo ya está protegido por BitLocker, la Directiva de exención de usuarios no surte efecto.</span><span class="sxs-lookup"><span data-stu-id="c6f44-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="c6f44-142">Además, si otro usuario inicia sesión en un equipo que no está exento de la Directiva de cifrado, tendrá lugar el cifrado.</span><span class="sxs-lookup"><span data-stu-id="c6f44-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c6f44-143">Los pasos siguientes describen lo que ocurre cuando los usuarios finales solicitan una exención del proceso de exención del cifrado de unidad BitLocker a través del cliente MBAM o de cualquier proceso que use su organización.</span><span class="sxs-lookup"><span data-stu-id="c6f44-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="c6f44-144">Debe configurar la configuración de directiva de grupo de MBAM para permitir que los usuarios finales soliciten una exención del cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="c6f44-145">Cuando los usuarios finales inician sesión en un equipo que debe estar cifrado, reciben una notificación de que el equipo se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="c6f44-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="c6f44-146">Pueden seleccionar **exención de solicitud** y posponer el cifrado seleccionando **posponer**o pueden seleccionar **iniciar cifrado** para aceptar el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="c6f44-147">Nota</span><span class="sxs-lookup"><span data-stu-id="c6f44-147">Note</span></span>**  
    <span data-ttu-id="c6f44-148">Al seleccionar **exención de solicitud** , se pospone la protección de BitLocker hasta el tiempo máximo establecido en la Directiva de exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6f44-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="c6f44-149">Si los usuarios finales seleccionan **exención de solicitud**, recibirán una notificación que les indicará que se pongan en contacto con el grupo de administración de BitLocker de la organización.</span><span class="sxs-lookup"><span data-stu-id="c6f44-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="c6f44-150">En función de la configuración de la **directiva configurar excepciones de usuario** , los usuarios disponen de uno o varios de los siguientes métodos de contacto:</span><span class="sxs-lookup"><span data-stu-id="c6f44-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="c6f44-151">Número de teléfono</span><span class="sxs-lookup"><span data-stu-id="c6f44-151">Phone number</span></span>

    -   <span data-ttu-id="c6f44-152">Dirección URL de la página web</span><span class="sxs-lookup"><span data-stu-id="c6f44-152">Webpage URL</span></span>

    -   <span data-ttu-id="c6f44-153">Dirección de correo</span><span class="sxs-lookup"><span data-stu-id="c6f44-153">Mailing address</span></span>

3.  <span data-ttu-id="c6f44-154">Una vez recibida la solicitud de exención, el administrador de MBAM decide si quiere agregar el usuario al grupo servicios de dominio de Active Directory (AD DS) de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="c6f44-155">Después de que un usuario final envía una solicitud de exención, el cliente de MBAM notifica al usuario como "se ha eximido temporalmente".</span><span class="sxs-lookup"><span data-stu-id="c6f44-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="c6f44-156">Después, el cliente espera un número determinado de días, que los administradores de TI han configurado, antes de volver a comprobar el cumplimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="c6f44-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="c6f44-157">Si el administrador de MBAM rechaza la solicitud de exención, la opción de solicitud de exención está desactivada, lo que impide que el usuario vuelva a solicitar la exención.</span><span class="sxs-lookup"><span data-stu-id="c6f44-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="c6f44-158">Para eximir a un usuario del cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="c6f44-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="c6f44-159">Cree un grupo de seguridad de AD DS que se usará para administrar las exenciones de usuario de los requisitos de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="c6f44-160">Crear un objeto de directiva de grupo mediante las plantillas de directiva de Grupo administración y supervisión de BitLocker de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6f44-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="c6f44-161">Asocie el objeto de directiva de grupo con el grupo de AD DS que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="c6f44-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="c6f44-162">La configuración de directiva para excluir a los usuarios se encuentra en: **UserConfiguration** &gt; **Administrative templates** &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="c6f44-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="c6f44-163">Para el grupo de seguridad que ha creado para usuarios exentos de BitLocker, agregue los nombres de los usuarios que solicitan una exención.</span><span class="sxs-lookup"><span data-stu-id="c6f44-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="c6f44-164">Cuando un usuario inicia sesión en un equipo controlado por BitLocker, el cliente de MBAM comprueba la configuración de la Directiva de exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6f44-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="c6f44-165">Si el equipo ya está cifrado, la protección de BitLocker no se suspende.</span><span class="sxs-lookup"><span data-stu-id="c6f44-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="c6f44-166">Si el equipo no está cifrado, MBAM no le pide al usuario que lo cifre.</span><span class="sxs-lookup"><span data-stu-id="c6f44-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="c6f44-167">Importante</span><span class="sxs-lookup"><span data-stu-id="c6f44-167">Important</span></span>**  
    <span data-ttu-id="c6f44-168">Los escenarios de equipos compartidos requieren una consideración especial cuando se usan exenciones de usuario de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6f44-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="c6f44-169">Si un usuario no exento inicia sesión en un equipo que está compartido con un usuario exento, el equipo puede estar cifrado.</span><span class="sxs-lookup"><span data-stu-id="c6f44-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="c6f44-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6f44-170">Related topics</span></span>


[<span data-ttu-id="c6f44-171">Administración de funciones de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c6f44-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="c6f44-172">Planificación para requisitos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c6f44-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="c6f44-173">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="c6f44-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c6f44-174">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c6f44-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c6f44-175">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c6f44-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




