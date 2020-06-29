---
title: Pestaña Delegación de dominio
description: Pestaña Delegación de dominio
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818630"
---
# <span data-ttu-id="6920f-103">Pestaña Delegación de dominio</span><span class="sxs-lookup"><span data-stu-id="6920f-103">Domain Delegation Tab</span></span>


<span data-ttu-id="6920f-104">La pestaña **delegación de dominios** del panel control de **cambios** proporciona una lista de administradores de directivas de grupo que tienen acceso en el nivel de dominio al archivo y indican las funciones de cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="6920f-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="6920f-105">Además, esta pestaña permite a los administradores de AGPM (control total) configurar permisos de nivel de dominio para editores, aprobadores, revisores y otros administradores de AGPM.</span><span class="sxs-lookup"><span data-stu-id="6920f-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="6920f-106">Hay dos secciones en la pestaña **delegación de dominios** : configuración de notificaciones de correo electrónico y delegación basada en roles para la administración avanzada de directivas de grupo (AGPM) en el nivel de dominio.</span><span class="sxs-lookup"><span data-stu-id="6920f-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="6920f-107">Configuración de la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="6920f-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="6920f-108">En la sección notificación de correo electrónico de esta pestaña se identifican los aprobadores que recibirán una notificación cuando haya operaciones pendientes en AGPM.</span><span class="sxs-lookup"><span data-stu-id="6920f-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6920f-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="6920f-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="6920f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6920f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6920f-111">Desde</span><span class="sxs-lookup"><span data-stu-id="6920f-111">From</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-112">Alias de AGPM desde el que se envía la notificación a los aprobadores.</span><span class="sxs-lookup"><span data-stu-id="6920f-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="6920f-113">En un entorno con varios dominios, puede ser el mismo alias en todo el entorno o un alias diferente para cada dominio.</span><span class="sxs-lookup"><span data-stu-id="6920f-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6920f-114">Para</span><span class="sxs-lookup"><span data-stu-id="6920f-114">To</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-115">Una lista delimitada por comas de las direcciones de correo electrónico de los aprobadores a las que se va a enviar la notificación</span><span class="sxs-lookup"><span data-stu-id="6920f-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6920f-116">Servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="6920f-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-117">El nombre del servidor de correo electrónico, como mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6920f-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6920f-118">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="6920f-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-119">Un usuario con acceso al servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="6920f-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6920f-120">Contraseña</span><span class="sxs-lookup"><span data-stu-id="6920f-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-121">Contraseña del usuario para la autenticación en el servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="6920f-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6920f-122">Confirmar contraseña</span><span class="sxs-lookup"><span data-stu-id="6920f-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-123">Confirmar la contraseña del usuario</span><span class="sxs-lookup"><span data-stu-id="6920f-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6920f-124">Delegación basada en roles de nivel de dominio</span><span class="sxs-lookup"><span data-stu-id="6920f-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="6920f-125">La sección delegación basada en roles de esta pestaña muestra y permite a un administrador de AGPM delegar permisos permitidos, denegados y heredados para cada grupo y usuario del dominio con acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="6920f-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="6920f-126">Un administrador de AGPM puede configurar permisos para todo el dominio con roles de AGPM estándar (editor, aprobador, revisor y administrador de AGPM) o una combinación personalizada de permisos para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="6920f-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6920f-127">Botón</span><span class="sxs-lookup"><span data-stu-id="6920f-127">Button</span></span></th>
<th align="left"><span data-ttu-id="6920f-128">Efecto</span><span class="sxs-lookup"><span data-stu-id="6920f-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6920f-129">Agregar</span><span class="sxs-lookup"><span data-stu-id="6920f-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-130">Agregue una nueva entrada al descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6920f-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="6920f-131">Todos los usuarios o grupos de Active Directory se pueden agregar como administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="6920f-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6920f-132">Eliminar</span><span class="sxs-lookup"><span data-stu-id="6920f-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-133">Quitar los administradores de directivas de grupo seleccionados de la lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="6920f-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6920f-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6920f-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-135">Mostrar las propiedades de los administradores de directivas de grupo seleccionados.</span><span class="sxs-lookup"><span data-stu-id="6920f-135">Display the properties for the selected Group Policy administrators.</span></span> <span data-ttu-id="6920f-136">La página de propiedades es la misma que se muestra para un objeto en <strong> usuarios y equipos de Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="6920f-136">The properties page is the same one displayed for an object in <strong>Active Directory User and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6920f-137">Avanzado</span><span class="sxs-lookup"><span data-stu-id="6920f-137">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6920f-138">Abra el <strong> Editor de la lista de control de acceso </strong> .</span><span class="sxs-lookup"><span data-stu-id="6920f-138">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6920f-139">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="6920f-139">Additional considerations</span></span>

-   <span data-ttu-id="6920f-140">Para obtener información sobre los roles y los permisos relacionados con tareas específicas, consulte las tareas de realizar tareas de [Administrador de AGPM](performing-agpm-administrator-tasks.md), [realizar tareas de editor](performing-editor-tasks.md), [realizar tareas de aprobador](performing-approver-tasks.md)y [realizar tareas de revisor](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="6920f-140">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="6920f-141">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="6920f-141">Additional references</span></span>

-   [<span data-ttu-id="6920f-142">Interfaz de usuario: Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="6920f-142">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

-   [<span data-ttu-id="6920f-143">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="6920f-143">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





