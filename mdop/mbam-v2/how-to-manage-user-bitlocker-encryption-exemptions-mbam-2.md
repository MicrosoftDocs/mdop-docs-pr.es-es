---
title: Cómo administrar exenciones de cifrado de BitLocker de usuario
description: Cómo administrar exenciones de cifrado de BitLocker de usuario
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825071"
---
# <span data-ttu-id="518bc-103">Cómo administrar exenciones de cifrado de BitLocker de usuario</span><span class="sxs-lookup"><span data-stu-id="518bc-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="518bc-104">La administración y supervisión de Microsoft BitLocker (MBAM) se puede usar para administrar la protección de BitLocker al eximir a los usuarios si hay usuarios que no necesitan o quieren que sus unidades estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="518bc-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="518bc-105">Para excluir a los usuarios de la protección de BitLocker, una organización tendrá que crear una infraestructura para admitir usuarios excluidos, como asignar al usuario un número de teléfono de contacto, una página web o una dirección de correo para solicitar una exención.</span><span class="sxs-lookup"><span data-stu-id="518bc-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="518bc-106">Además, será necesario agregar un usuario exento a un grupo de seguridad para un objeto de directiva de grupo creado específicamente para los usuarios excluidos.</span><span class="sxs-lookup"><span data-stu-id="518bc-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="518bc-107">Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la configuración de directiva de grupo del usuario muestra que el usuario está exento de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="518bc-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="518bc-108">La configuración de directiva de grupo del usuario sobrescribe la Directiva de equipo, y el equipo permanecerá exento del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="518bc-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="518bc-109">**Nota:**  Si el equipo ya está protegido por BitLocker, la Directiva de exención de usuarios no surte efecto.</span><span class="sxs-lookup"><span data-stu-id="518bc-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="518bc-110">En la tabla siguiente se muestra cómo se aplica la protección de BitLocker en función de la configuración de las exenciones.</span><span class="sxs-lookup"><span data-stu-id="518bc-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="518bc-111">Estado de usuario</span><span class="sxs-lookup"><span data-stu-id="518bc-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="518bc-112">Equipo no exento</span><span class="sxs-lookup"><span data-stu-id="518bc-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="518bc-113">Exención de equipo</span><span class="sxs-lookup"><span data-stu-id="518bc-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="518bc-114">El usuario no está exento</span><span class="sxs-lookup"><span data-stu-id="518bc-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="518bc-115">Se exige la protección de BitLocker en el equipo</span><span class="sxs-lookup"><span data-stu-id="518bc-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="518bc-116">No se exige la protección de BitLocker en el equipo</span><span class="sxs-lookup"><span data-stu-id="518bc-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="518bc-117">Exención de usuarios</span><span class="sxs-lookup"><span data-stu-id="518bc-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="518bc-118">No se exige la protección de BitLocker en el equipo</span><span class="sxs-lookup"><span data-stu-id="518bc-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="518bc-119">No se exige la protección de BitLocker en el equipo</span><span class="sxs-lookup"><span data-stu-id="518bc-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="518bc-120">Para eximir a un usuario del cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="518bc-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="518bc-121">Cree un grupo de seguridad ActiveDirectoryDomainServices que se usará para administrar las exenciones de usuario de los requisitos de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="518bc-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="518bc-122">Cree una configuración de objeto de directiva de grupo con la plantilla de directiva de grupo supervisión y administración de BitLocker de Microsoft y asóciela al grupo de Active Directory que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="518bc-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="518bc-123">La configuración de directiva para excluir a los usuarios puede encontrarse en **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (administración de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="518bc-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="518bc-124">Después de crear un grupo de seguridad para los usuarios exentos de BitLocker, agregue a este grupo los nombres de los usuarios que solicitan una exención.</span><span class="sxs-lookup"><span data-stu-id="518bc-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="518bc-125">Cuando los usuarios inicien sesión en un equipo controlado por BitLocker, el cliente de MBAM verificará la configuración de la Directiva de exención de usuarios y se suspenderá la protección en función de si el usuario forma parte del grupo de seguridad de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="518bc-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="518bc-126">**Importante**  Los escenarios de equipos compartidos requieren una consideración especial al usar exenciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="518bc-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="518bc-127">Si un usuario no exento inicia sesión en un equipo compartido con un usuario exento, el equipo se puede cifrar.</span><span class="sxs-lookup"><span data-stu-id="518bc-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="518bc-128">Para permitir a los usuarios solicitar una exención del cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="518bc-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="518bc-129">Si ha configurado directivas de exención de usuarios mediante la plantilla de directiva MBAM, un usuario puede solicitar una exención de la protección de BitLocker a través del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="518bc-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="518bc-130">Cuando los usuarios inician sesión en un equipo que debe estar cifrado, reciben una notificación de que se va a cifrar su equipo.</span><span class="sxs-lookup"><span data-stu-id="518bc-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="518bc-131">Pueden seleccionar **solicitar exención** y posponer el cifrado seleccionando **más tarde**, o bien seleccionar **iniciar** para aceptar el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="518bc-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="518bc-132">**Nota:**  Al seleccionar **exención de solicitud** , se pospone la protección de BitLocker hasta el tiempo máximo establecido en la Directiva de exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="518bc-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="518bc-133">Si los usuarios seleccionan la **solicitud de exención**, recibirán una notificación para indicarles que se pongan en contacto con el grupo de administración de BitLocker de su organización.</span><span class="sxs-lookup"><span data-stu-id="518bc-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="518bc-134">En función de la configuración de la directiva configurar excepciones de usuario, los usuarios disponen de uno o varios de los siguientes métodos de contacto:</span><span class="sxs-lookup"><span data-stu-id="518bc-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="518bc-135">Número de teléfono</span><span class="sxs-lookup"><span data-stu-id="518bc-135">Phone Number</span></span>

    -   <span data-ttu-id="518bc-136">Dirección URL de la página web</span><span class="sxs-lookup"><span data-stu-id="518bc-136">Webpage URL</span></span>

    -   <span data-ttu-id="518bc-137">Dirección de correo</span><span class="sxs-lookup"><span data-stu-id="518bc-137">Mailing Address</span></span>

    <span data-ttu-id="518bc-138">Una vez recibida la solicitud de exención, el administrador de MBAM puede decidir si es adecuado agregar el usuario al grupo de Active Directory de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="518bc-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="518bc-139">**Nota:**  Una vez que un usuario envía una solicitud de exención, el agente de MBAM notifica al usuario como "no disponible temporalmente" y, a continuación, espera un número configurable de días antes de comprobar de nuevo la conformidad del equipo.</span><span class="sxs-lookup"><span data-stu-id="518bc-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="518bc-140">Si el administrador de MBAM rechaza la solicitud de exención, la opción de solicitud de exención está desactivada, lo que evita que el usuario pueda volver a solicitar la exención.</span><span class="sxs-lookup"><span data-stu-id="518bc-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="518bc-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="518bc-141">Related topics</span></span>


[<span data-ttu-id="518bc-142">Administración de funciones de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="518bc-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





