---
title: Solución de problemas de Administración avanzada de directivas de grupo
description: Solución de problemas de Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818251"
---
# <span data-ttu-id="0f8b8-103">Solución de problemas de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="0f8b8-104">En esta sección se enumeran algunos problemas comunes que pueden surgir al usar la administración de directivas de grupo (AGPM) avanzada para administrar objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="0f8b8-105">¿Qué problemas tienes?</span><span class="sxs-lookup"><span data-stu-id="0f8b8-105">What problems are you having?</span></span>


-   [<span data-ttu-id="0f8b8-106">No puedo acceder a un archivo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="0f8b8-107">El estado de GPO varía según los distintos administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="0f8b8-108">No puedo modificar la conexión del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0f8b8-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="0f8b8-109">No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="0f8b8-110">No puedo usar un nombre de GPO determinado</span><span class="sxs-lookup"><span data-stu-id="0f8b8-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="0f8b8-111">No recibo notificaciones de correo electrónico de AGPM</span><span class="sxs-lookup"><span data-stu-id="0f8b8-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="0f8b8-112">No puedo usar el puerto 4600 para el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="0f8b8-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="0f8b8-113">El servicio AGPM no se iniciará</span><span class="sxs-lookup"><span data-stu-id="0f8b8-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="0f8b8-114">Instalación de software de directiva de grupo no se puede instalar el software</span><span class="sxs-lookup"><span data-stu-id="0f8b8-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="0f8b8-115">No puedo acceder a un archivo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="0f8b8-116">**Causa**: no ha seleccionado el servidor y puerto correctos para el archivo.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="0f8b8-117">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-117">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-118">Si es un administrador de AGPM: consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="0f8b8-119">Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="0f8b8-120">Consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="0f8b8-121">**Causa**: el servicio de administración de directivas de grupo avanzado no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="0f8b8-122">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-122">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-123">Si es un administrador de AGPM: inicie el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="0f8b8-124">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="0f8b8-125">Si no es administrador de AGPM: póngase en contacto con un administrador de AGPM para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="0f8b8-126">El estado de GPO varía según los distintos administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="0f8b8-127">**Causa**: los distintos administradores de la Directiva de grupo han seleccionado diferentes servidores de AGPM para el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="0f8b8-128">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-128">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-129">Si es un administrador de AGPM: consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="0f8b8-130">Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="0f8b8-131">Consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="0f8b8-132">No puedo modificar la conexión del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0f8b8-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="0f8b8-133">**Causa**: Si la configuración de la pestaña **servidor de AGPM** no está disponible, el servidor AGPM se ha configurado de forma centralizada con una plantilla administrativa.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="0f8b8-134">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-134">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-135">Si es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, vea [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="0f8b8-136">Si no es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, no necesita modificar el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="0f8b8-137">No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="0f8b8-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="0f8b8-138">**Causa**: no se le ha asignado un rol con los permisos necesarios para realizar la tarea o las tareas.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="0f8b8-139">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-139">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-140">Si es administrador de AGPM: vea [delegar el acceso a nivel de dominio](delegate-domain-level-access.md) y [delegar el acceso a un GPO individual](delegate-access-to-an-individual-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="0f8b8-141">Los permisos de AGPM se aplicarán en cascada desde el dominio a todos los GPO que se encuentran actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="0f8b8-142">A medida que se agregan nuevos administradores de directivas de grupo en el nivel de dominio, sus permisos deben configurarse para que se apliquen a **este objeto y a los objetos anidados**.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="0f8b8-143">Para obtener detalles sobre qué roles pueden realizar una tarea y qué permisos son necesarios para realizar una tarea, consulte la ayuda de esa tarea.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="0f8b8-144">Si no es administrador de AGPM y necesita roles o permisos adicionales, póngase en contacto con un administrador de AGPM para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="0f8b8-145">Tenga en cuenta que si es un editor, puede iniciar el proceso de creación de un GPO, implementar un GPO o eliminar un GPO desde el entorno de producción, pero un aprobador o administrador AGPM debe aprobar su solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="0f8b8-146">No puedo usar un nombre de GPO determinado</span><span class="sxs-lookup"><span data-stu-id="0f8b8-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="0f8b8-147">**Causa**: el nombre del GPO ya está en uso o usted carece de permiso para enumerar el GPO.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="0f8b8-148">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-148">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-149">Si el nombre del GPO aparece en la pestaña controlada, no **controlada**o en **espera** **, elija**otro nombre.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="0f8b8-150">Si se ha cambiado el nombre de un GPO que se ha implementado, pero aún no se ha reimplementado, se mostrará bajo su nombre antiguo en el entorno de producción; por lo tanto, el nombre anterior aún está en uso.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="0f8b8-151">Vuelva a implementar el GPO para actualizar su nombre en el entorno de producción y liberar ese nombre para que lo use otro objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="0f8b8-152">Si el nombre del GPO no aparece en la pestaña controlada **, no** **controlada**o **pendiente** , es posible que no tenga permiso para enumerar el GPO.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="0f8b8-153">Para solicitar permiso, póngase en contacto con un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="0f8b8-154">No recibo notificaciones de correo electrónico de AGPM</span><span class="sxs-lookup"><span data-stu-id="0f8b8-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="0f8b8-155">**Causa**: no se proporcionó un servidor de correo electrónico SMTP válido y una dirección de correo electrónico, o no se ha tomado ninguna acción que genere una notificación por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="0f8b8-156">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="0f8b8-156">**Solution**:</span></span>

    -   <span data-ttu-id="0f8b8-157">Si es administrador de AGPM: para las notificaciones de correo electrónico sobre las acciones pendientes que debe enviar AGPM, un administrador de AGPM debe proporcionar un servidor de correo electrónico SMTP y direcciones de correo electrónico válidos para los aprobadores en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="0f8b8-158">Las notificaciones por correo electrónico solo se generan cuando un editor, revisor u otro administrador de directiva de grupo que carezca del permiso necesario para crear, implementar o eliminar un GPO envía una solicitud de que se produzca una de esas acciones.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="0f8b8-159">No hay ninguna notificación automática de aprobación ni rechazo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="0f8b8-160">No puedo usar el puerto 4600 para el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="0f8b8-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="0f8b8-161">**Causa**: de forma predeterminada, el puerto en el que escucha el servicio AGPM es el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="0f8b8-162">**Solución**: Si el puerto 4600 no está disponible para el servicio AGPM, modifique cada archivo de índice de archivo para que use otro puerto y, a continuación, actualice el servidor de AGPM para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="0f8b8-163">Para obtener más información, vea [modificar el puerto en el que escucha el servicio AGPM](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="0f8b8-164">El servicio AGPM no se iniciará</span><span class="sxs-lookup"><span data-stu-id="0f8b8-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="0f8b8-165">**Causa**: ha modificado la configuración del servicio AGPM en el sistema operativo en **herramientas administrativas** y **servicios**.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="0f8b8-166">**Solución**: modifique la configuración de **Administración avanzada de directivas de grupo de Microsoft-servidor** en **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="0f8b8-167">Para obtener más información, vea [modificar la cuenta de servicio de AGPM](modify-the-agpm-service-account.md).</span><span class="sxs-lookup"><span data-stu-id="0f8b8-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="0f8b8-168">Instalación de software de directiva de grupo no se puede instalar el software</span><span class="sxs-lookup"><span data-stu-id="0f8b8-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="0f8b8-169">**Causa**: AGPM conserva la integridad de los paquetes de instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="0f8b8-170">Aunque los GPO se modifican sin conexión, se conservan los vínculos entre paquetes, así como la información de cliente en caché.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="0f8b8-171">Esto es así por diseño.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-171">This is by design.</span></span>

-   <span data-ttu-id="0f8b8-172">**Solución**: al editar un GPO sin conexión con AGPM, configure cualquier actualización de instalación de software de directiva de grupo de un paquete en otro GPO para hacer referencia al GPO implementado, no a la copia desprotegida.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="0f8b8-173">El editor debe tener permiso de **lectura** para el objeto de directiva de grupo implementado.</span><span class="sxs-lookup"><span data-stu-id="0f8b8-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 





