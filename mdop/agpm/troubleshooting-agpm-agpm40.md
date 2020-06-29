---
title: Solución de problemas de AGPM
description: Solución de problemas de AGPM
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820151"
---
# <span data-ttu-id="8c605-103">Solución de problemas de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-103">Troubleshooting AGPM</span></span>


<span data-ttu-id="8c605-104">En esta sección se enumeran los problemas comunes que pueden surgir al usar la administración de directivas de grupo (AGPM) avanzada para administrar objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="8c605-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="8c605-105">Para diagnosticar problemas que no se encuentran aquí, puede ser útil que un administrador de AGPM (control total) Use el registro y el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="8c605-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="8c605-106">Para obtener más información, vea [configurar el registro y el seguimiento](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

**<span data-ttu-id="8c605-107">Nota</span><span class="sxs-lookup"><span data-stu-id="8c605-107">Note</span></span>**  
-   <span data-ttu-id="8c605-108">Para obtener información sobre cómo revertir a una versión anterior de un GPO si hay problemas, consulte volver [a una versión anterior de un GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

-   <span data-ttu-id="8c605-109">Para obtener información sobre cómo recuperarse de un desastre restaurando el archivo completo desde una copia de seguridad, consulte [restaurar el archivo a partir de una copia de seguridad](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

 

## <span data-ttu-id="8c605-110">¿Qué problemas tienes?</span><span class="sxs-lookup"><span data-stu-id="8c605-110">What problems are you having?</span></span>


-   [<span data-ttu-id="8c605-111">No puedo acceder a un archivo</span><span class="sxs-lookup"><span data-stu-id="8c605-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="8c605-112">El estado de GPO varía según los distintos administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="8c605-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="8c605-113">No puedo modificar la conexión del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="8c605-114">No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8c605-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="8c605-115">No puedo usar un nombre de GPO determinado</span><span class="sxs-lookup"><span data-stu-id="8c605-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="8c605-116">No recibo notificaciones de correo electrónico de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="8c605-117">No puedo usar el puerto 4600 para el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="8c605-118">El servicio AGPM no se iniciará</span><span class="sxs-lookup"><span data-stu-id="8c605-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="8c605-119">Instalación de software de directiva de grupo no se puede instalar el software</span><span class="sxs-lookup"><span data-stu-id="8c605-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="8c605-120">Error al restaurar el archivo en un nuevo servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="8c605-121">No puedo acceder a un archivo</span><span class="sxs-lookup"><span data-stu-id="8c605-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="8c605-122">**Causa**: no ha seleccionado el servidor y puerto correctos para el archivo.</span><span class="sxs-lookup"><span data-stu-id="8c605-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="8c605-123">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-123">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-124">Si es un administrador de AGPM: consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="8c605-125">Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="8c605-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="8c605-126">Consulte [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

-   <span data-ttu-id="8c605-127">**Causa**: el servicio AGPM no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8c605-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="8c605-128">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-128">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-129">Si es un administrador de AGPM: inicie el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="8c605-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="8c605-130">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    -   <span data-ttu-id="8c605-131">Si no es administrador de AGPM: póngase en contacto con un administrador de AGPM para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="8c605-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="8c605-132">El estado de GPO varía según los distintos administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="8c605-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="8c605-133">**Causa**: los distintos administradores de la Directiva de grupo han seleccionado diferentes servidores de AGPM para el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="8c605-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="8c605-134">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-134">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-135">Si es un administrador de AGPM: consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="8c605-136">Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="8c605-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="8c605-137">Consulte [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="8c605-138">No puedo modificar la conexión del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="8c605-139">**Causa**: Si la configuración de la pestaña **servidor de AGPM** no está disponible, el servidor AGPM se ha configurado de forma centralizada con una plantilla administrativa.</span><span class="sxs-lookup"><span data-stu-id="8c605-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="8c605-140">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-140">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-141">Si es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="8c605-142">Si no es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, no necesita modificar el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="8c605-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="8c605-143">No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8c605-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="8c605-144">**Causa**: no se le ha asignado un rol con los permisos necesarios para realizar la tarea o las tareas.</span><span class="sxs-lookup"><span data-stu-id="8c605-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="8c605-145">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-145">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-146">Si es administrador de AGPM: consulte [delegar el acceso a nivel de dominio en el archivo](delegate-domain-level-access-to-the-archive-agpm40.md) y [delegar el acceso a un GPO individual en el archivo](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span></span> <span data-ttu-id="8c605-147">Los permisos de AGPM se aplicarán en cascada desde el dominio a todos los GPO que se encuentran actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="8c605-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="8c605-148">Para obtener más información sobre qué roles pueden realizar una tarea y cuáles son los permisos necesarios para realizar una tarea, consulte la ayuda de esa tarea.</span><span class="sxs-lookup"><span data-stu-id="8c605-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="8c605-149">Si no es administrador de AGPM y necesita roles o permisos adicionales, póngase en contacto con un administrador de AGPM para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="8c605-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="8c605-150">Tenga en cuenta que si es un editor, puede iniciar el proceso de creación de un GPO, implementar un GPO o eliminar un objeto de directiva de grupo del entorno de producción del dominio, pero un aprobador o administrador AGPM debe aprobar su solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c605-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment of the domain, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="8c605-151">No puedo usar un nombre de GPO determinado</span><span class="sxs-lookup"><span data-stu-id="8c605-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="8c605-152">**Causa**: el nombre del GPO ya está en uso o usted carece de permiso para enumerar el GPO.</span><span class="sxs-lookup"><span data-stu-id="8c605-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="8c605-153">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-153">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-154">Si el nombre del GPO aparece en la pestaña controlada, no **controlada**o en **espera** **, elija**otro nombre.</span><span class="sxs-lookup"><span data-stu-id="8c605-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="8c605-155">Si se ha cambiado el nombre de un GPO que se ha implementado pero aún no se ha reimplementado, se mostrará con su nombre antiguo en el entorno de producción del dominio.</span><span class="sxs-lookup"><span data-stu-id="8c605-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment of the domain.</span></span> <span data-ttu-id="8c605-156">Por lo tanto, el nombre antiguo aún se está usando.</span><span class="sxs-lookup"><span data-stu-id="8c605-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="8c605-157">Vuelva a implementar el GPO para actualizar su nombre en el entorno de producción y liberar ese nombre para que lo use otro objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8c605-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="8c605-158">Si el nombre del GPO no aparece en la pestaña controlada **, no** **controlada**o **pendiente** , es posible que no tenga permiso para enumerar el GPO.</span><span class="sxs-lookup"><span data-stu-id="8c605-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="8c605-159">Para solicitar permiso, póngase en contacto con un administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="8c605-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="8c605-160">No recibo notificaciones de correo electrónico de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="8c605-161">**Causa**: no se proporcionó un servidor de correo electrónico SMTP válido y una dirección de correo electrónico, o no se ha tomado ninguna acción que genere una notificación por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="8c605-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="8c605-162">**Solución**:</span><span class="sxs-lookup"><span data-stu-id="8c605-162">**Solution**:</span></span>

    -   <span data-ttu-id="8c605-163">Si es administrador de AGPM: para las notificaciones de correo electrónico sobre las acciones pendientes que debe enviar AGPM, un administrador de AGPM debe proporcionar un servidor de correo electrónico SMTP y direcciones de correo electrónico válidos para los aprobadores en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

    -   <span data-ttu-id="8c605-164">Las notificaciones por correo electrónico solo se generan cuando un editor, revisor u otro administrador de directiva de grupo que carezca del permiso necesario para crear, implementar o eliminar un GPO envía una solicitud de que se produzca una de esas acciones.</span><span class="sxs-lookup"><span data-stu-id="8c605-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="8c605-165">No hay ninguna notificación automática de aprobación ni rechazo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c605-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="8c605-166">No puedo usar el puerto 4600 para el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="8c605-167">**Causa**: de forma predeterminada, el puerto en el que escucha el servicio AGPM es el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="8c605-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="8c605-168">**Solución**: Si el puerto 4600 no está disponible para el servicio AGPM, modifique la configuración del puerto en el servidor de AGPM para usar otro puerto y, a continuación, actualice el puerto en la conexión del servidor de AGPM para clientes AGPM.</span><span class="sxs-lookup"><span data-stu-id="8c605-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="8c605-169">Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="8c605-170">El servicio AGPM no se iniciará</span><span class="sxs-lookup"><span data-stu-id="8c605-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="8c605-171">**Causa**: ha modificado la configuración del servicio AGPM en el sistema operativo en **herramientas administrativas** y **servicios**.</span><span class="sxs-lookup"><span data-stu-id="8c605-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="8c605-172">**Solución**: modifique la configuración de **Administración avanzada de directivas de grupo de Microsoft-servidor** en **programas y características** en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="8c605-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="8c605-173">Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="8c605-174">Instalación de software de directiva de grupo no se puede instalar el software</span><span class="sxs-lookup"><span data-stu-id="8c605-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="8c605-175">**Causa**: AGPM conserva la integridad de los paquetes de instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8c605-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="8c605-176">Aunque los GPO se modifican sin conexión, se conservan los vínculos entre paquetes además de la información de cliente en caché.</span><span class="sxs-lookup"><span data-stu-id="8c605-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="8c605-177">Esto es así por diseño.</span><span class="sxs-lookup"><span data-stu-id="8c605-177">This is by design.</span></span>

-   <span data-ttu-id="8c605-178">**Solución**: al editar un GPO sin conexión con AGPM, configure cualquier actualización de instalación de software de directiva de grupo de un paquete en otro GPO para hacer referencia al GPO implementado, no a la copia desprotegida.</span><span class="sxs-lookup"><span data-stu-id="8c605-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="8c605-179">El editor debe tener permiso de **lectura** para el objeto de directiva de grupo implementado.</span><span class="sxs-lookup"><span data-stu-id="8c605-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="8c605-180">Error al restaurar el archivo en un nuevo servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="8c605-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="8c605-181">**Causa**: por razones de seguridad, el cifrado que protege la contraseña especificada en la pestaña **delegación de dominios** provoca que se produzcan errores en la contraseña si el archivo se mueve a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="8c605-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="8c605-182">**Solución**: vuelva a escribir y confirme la contraseña en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8c605-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

 

 





