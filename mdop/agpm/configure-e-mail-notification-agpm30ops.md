---
title: Configurar notificaciones por correo electrónico
description: Configurar notificaciones por correo electrónico
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819001"
---
# <span data-ttu-id="feb14-103">Configurar notificaciones por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="feb14-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="feb14-104">Cuando un editor o un revisor intenta crear, implementar o eliminar un objeto de directiva de grupo (GPO), se envía una solicitud de esta acción a una o más direcciones de correo electrónico para que un aprobador pueda evaluar la solicitud e implementarla o denegarla.</span><span class="sxs-lookup"><span data-stu-id="feb14-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy Object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="feb14-105">Determine la dirección o direcciones de correo electrónico a las que se envían las notificaciones, así como el alias desde el que se envían las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="feb14-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="feb14-106">Para completar este procedimiento, debe tener una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="feb14-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="feb14-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="feb14-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="feb14-108">Para configurar la notificación de correo electrónico para AGPM</span><span class="sxs-lookup"><span data-stu-id="feb14-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="feb14-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="feb14-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="feb14-110">En el panel de detalles, haga clic en la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="feb14-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="feb14-111">En el campo **desde dirección de correo electrónico** , escriba el alias de correo electrónico de AGPM desde el que se deben enviar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="feb14-111">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="feb14-112">En el campo **dirección de correo electrónico** , escriba una lista delimitada por comas de las direcciones de correo electrónico de los aprobadores que deberían recibir solicitudes de aprobación.</span><span class="sxs-lookup"><span data-stu-id="feb14-112">In the **To e-mail address** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="feb14-113">En el campo **servidor SMTP** , escriba un servidor de correo SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="feb14-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="feb14-114">En los campos **nombre de usuario** y **contraseña** , escriba las credenciales de un usuario con acceso al servicio SMTP.</span><span class="sxs-lookup"><span data-stu-id="feb14-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="feb14-115">Haz clic en **Apply**.</span><span class="sxs-lookup"><span data-stu-id="feb14-115">Click **Apply**.</span></span>

### <span data-ttu-id="feb14-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="feb14-116">Additional considerations</span></span>

-   <span data-ttu-id="feb14-117">Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="feb14-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="feb14-118">En concreto, debe tener los permisos **Mostrar contenido** y **modificar opciones** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="feb14-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="feb14-119">La notificación por correo electrónico para AGPM es una configuración de nivel de dominio.</span><span class="sxs-lookup"><span data-stu-id="feb14-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="feb14-120">Puede proporcionar diferentes direcciones de correo electrónico de aprobadores o alias de correo electrónico AGPM en la pestaña de **delegación de dominios** de cada dominio o usar las mismas direcciones de correo electrónico en todo el entorno.</span><span class="sxs-lookup"><span data-stu-id="feb14-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

-   <span data-ttu-id="feb14-121">De forma predeterminada, los mensajes de correo electrónico enviados como resultado de acciones en administración avanzada de directivas de grupo (AGPM) no están cifradas.</span><span class="sxs-lookup"><span data-stu-id="feb14-121">By default, e-mail messages sent as a result of actions in Advanced Group Policy Management (AGPM) are not encrypted.</span></span> <span data-ttu-id="feb14-122">Sin embargo, puede configurar la seguridad del correo electrónico para AGPM usando la configuración del registro para especificar si desea usar el cifrado de capa de sockets seguros (SSL) y qué puerto SMTP debe usar.</span><span class="sxs-lookup"><span data-stu-id="feb14-122">However, you can configure e-mail security for AGPM using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span> <span data-ttu-id="feb14-123">Para obtener más información, consulte [configurar la seguridad del correo electrónico para AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="feb14-123">For more information, see [Configure E-Mail Security for AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span></span>

### <span data-ttu-id="feb14-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="feb14-124">Additional references</span></span>

-   [<span data-ttu-id="feb14-125">Configuración de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="feb14-125">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





