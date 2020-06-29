---
title: Cómo administrar exenciones de cifrado de BitLocker de usuario
description: Cómo administrar exenciones de cifrado de BitLocker de usuario
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812966"
---
# <span data-ttu-id="d218f-103">Cómo administrar exenciones de cifrado de BitLocker de usuario</span><span class="sxs-lookup"><span data-stu-id="d218f-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="d218f-104">La administración y supervisión de Microsoft BitLocker (MBAM) se puede usar para administrar la protección de BitLocker al eximir a los usuarios que no necesitan o quieren que sus unidades estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="d218f-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="d218f-105">Para eximir a los usuarios de la protección de BitLocker, una organización debe crear primero una infraestructura que admita estas exenciones.</span><span class="sxs-lookup"><span data-stu-id="d218f-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="d218f-106">La infraestructura auxiliar puede incluir un número de teléfono de contacto, una página web o una dirección de correo para solicitar la exención.</span><span class="sxs-lookup"><span data-stu-id="d218f-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="d218f-107">Además, se deberá agregar a cualquier usuario exento a un grupo de seguridad para la Directiva de grupo creada específicamente para los usuarios excluidos.</span><span class="sxs-lookup"><span data-stu-id="d218f-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="d218f-108">Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la Directiva de grupo de usuarios muestra que el usuario está exento de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="d218f-109">La Directiva de usuario sobrescribe la Directiva de equipo y el equipo permanecerá exento del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="d218f-110">**Nota:**  Si el equipo ya está protegido por BitLocker, la Directiva de exención de usuarios no surte efecto.</span><span class="sxs-lookup"><span data-stu-id="d218f-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="d218f-111">En la tabla siguiente se muestra cómo se aplica la protección de BitLocker en función de la configuración de las exenciones.</span><span class="sxs-lookup"><span data-stu-id="d218f-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d218f-112">Estado de usuario</span><span class="sxs-lookup"><span data-stu-id="d218f-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="d218f-113">Equipo no exento</span><span class="sxs-lookup"><span data-stu-id="d218f-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="d218f-114">Exención de equipo</span><span class="sxs-lookup"><span data-stu-id="d218f-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d218f-115">El usuario no está exento</span><span class="sxs-lookup"><span data-stu-id="d218f-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d218f-116">La protección de BitLocker se aplica en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d218f-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d218f-117">La protección de BitLocker no se exige en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d218f-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d218f-118">Exención de usuarios</span><span class="sxs-lookup"><span data-stu-id="d218f-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d218f-119">La protección de BitLocker no se exige en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d218f-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d218f-120">La protección de BitLocker no se exige en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d218f-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d218f-121">Para eximir a un usuario del cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="d218f-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="d218f-122">Cree un grupo de seguridad ActiveDirectoryDomainServices que se usará para administrar las exenciones de usuario del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="d218f-123">Cree una configuración de objeto de directiva de grupo con la plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d218f-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="d218f-124">Asocie el objeto de directiva de grupo con el grupo de Active Directory que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="d218f-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="d218f-125">Para obtener más información sobre las opciones de directiva necesarias para permitir a los usuarios solicitar la exención del cifrado de BitLocker, consulte la sección configurar directivas de exención de usuarios en [planeamiento de los requisitos de la Directiva de grupo de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d218f-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="d218f-126">Después de crear un grupo de seguridad para los usuarios exentos de BitLocker, agregue a este grupo los nombres de los usuarios que solicitan exención.</span><span class="sxs-lookup"><span data-stu-id="d218f-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="d218f-127">Cuando un usuario inicia sesión en un equipo controlado por BitLocker, el cliente de MBAM verificará la configuración de la Directiva de exención de usuarios y se suspenderá en función de si el usuario forma parte del grupo de seguridad de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="d218f-128">**Nota:**  Los escenarios de equipos compartidos requieren consideraciones especiales sobre la exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="d218f-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="d218f-129">Si un usuario no exento inicia sesión en un equipo compartido con un usuario exento, el equipo se puede cifrar.</span><span class="sxs-lookup"><span data-stu-id="d218f-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="d218f-130">Para permitir a los usuarios solicitar la exención del cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="d218f-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="d218f-131">Una vez que haya configurado las directivas de exención de usuarios mediante la usingwith de la plantilla de directiva de MBAM, un usuario puede solicitar la exención de la protección de BitLocker a través del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d218f-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="d218f-132">Cuando un usuario inicia sesión en un equipo que está marcado como **compatible** en la lista de compatibilidad de hardware de MBAM, el sistema presenta al usuario una notificación que indica que el equipo se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="d218f-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="d218f-133">El usuario puede seleccionar **solicitar exención** y posponer el cifrado seleccionando **más tarde**o seleccionar **iniciar** para aceptar el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="d218f-134">**Nota:**  La selección de la **exención de solicitud** pospondrá la protección de BitLocker hasta el límite máximo establecido en la Directiva de exención de usuarios.</span><span class="sxs-lookup"><span data-stu-id="d218f-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="d218f-135">Cuando un usuario selecciona **solicitar exención**, el usuario recibe una notificación para que se comunique con el grupo de administración de BitLocker de la organización.</span><span class="sxs-lookup"><span data-stu-id="d218f-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="d218f-136">En función de la configuración de la directiva configurar excepciones de usuario, los usuarios disponen de uno o varios de los siguientes métodos de contacto:</span><span class="sxs-lookup"><span data-stu-id="d218f-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="d218f-137">Número de teléfono</span><span class="sxs-lookup"><span data-stu-id="d218f-137">Phone Number</span></span>

    -   <span data-ttu-id="d218f-138">Dirección URL de la página web</span><span class="sxs-lookup"><span data-stu-id="d218f-138">Webpage URL</span></span>

    -   <span data-ttu-id="d218f-139">Dirección de correo</span><span class="sxs-lookup"><span data-stu-id="d218f-139">Mailing Address</span></span>

    <span data-ttu-id="d218f-140">Después de enviar la solicitud, el administrador de MBAM puede decidir si es adecuado agregar el usuario al grupo de Active Directory de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="d218f-141">**Nota:**  Una vez que haya expirado el límite de tiempo de la Directiva de exención de usuarios, los usuarios no verán la opción de solicitar exención a la Directiva de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d218f-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="d218f-142">En este momento, los usuarios deben ponerse en contacto con el administrador de MBAM directamente para recibir exención de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d218f-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="d218f-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d218f-143">Related topics</span></span>


[<span data-ttu-id="d218f-144">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d218f-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





