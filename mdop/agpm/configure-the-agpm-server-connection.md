---
title: Configurar la conexión del servidor AGPM
description: Configurar la conexión del servidor AGPM
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818911"
---
# <span data-ttu-id="0d6a0-103">Configurar la conexión del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="0d6a0-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="0d6a0-104">Administración avanzada de directivas de grupo (AGPM) almacena todas las versiones de cada objeto de directiva de grupo (GPO) controlado en un archivo central, de modo que los administradores de directivas de grupo pueden ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="0d6a0-105">Una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO usado en estos procedimientos o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo es necesaria para completar estos procedimientos para configurar ubicaciones de archivo de forma centralizada para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="0d6a0-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="0d6a0-107">Configurar la conexión del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0d6a0-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="0d6a0-108">Como administrador de AGPM (control total), puede asegurarse de que todos los administradores de directivas de grupo se conecten con el mismo servidor de AGPM mediante la configuración centralizada de la configuración.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="0d6a0-109">Si su entorno requiere servidores AGPM independientes para algunos o todos los dominios, configure esos servidores de AGPM adicionales como excepciones a la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="0d6a0-110">Si no configura de forma centralizada las conexiones de servidor de AGPM, cada administrador de directivas de grupo debe configurar manualmente el servidor de AGPM para que se muestre en cada dominio.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="0d6a0-111">Configurar un servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0d6a0-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="0d6a0-112">Configurar servidores AGPM adicionales para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0d6a0-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="0d6a0-113">Configurar manualmente un servidor de AGPM para su cuenta</span><span class="sxs-lookup"><span data-stu-id="0d6a0-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="0d6a0-114">Para configurar un servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0d6a0-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="0d6a0-115">En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="0d6a0-116">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo.md)).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="0d6a0-117">En el **Editor de objetos de directiva de grupo**, haga clic en **configuración de usuario**, **plantillas administrativas**y **componentes de Windows**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="0d6a0-118">Si **AGPM** no aparece en **componentes de Windows**:</span><span class="sxs-lookup"><span data-stu-id="0d6a0-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="0d6a0-119">Haga clic con el botón secundario en **plantillas administrativas** y haga clic en **Agregar o quitar plantillas**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="0d6a0-120">Haga clic en **Agregar**, seleccione **AGPM. ADMX** o **AGPM. adm**, haga clic en **abrir**y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="0d6a0-121">En **componentes de Windows**, haga doble clic en **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="0d6a0-122">En el panel de detalles, haga doble clic en **servidor de AGPM (todos los dominios)**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="0d6a0-123">En la ventana de **propiedades del servidor de AGPM (todos los dominios)** , seleccione la casilla de verificación **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="0d6a0-124">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-124">Click **OK**.</span></span> <span data-ttu-id="0d6a0-125">A menos que desee configurar conexiones de servidores AGPM adicionales, cierre el **Editor de objetos de directiva de grupo** e implemente el GPO.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="0d6a0-126">(Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md)). Cuando se actualiza la Directiva de grupo, la conexión del servidor de AGPM está configurada para todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="0d6a0-127">Para configurar servidores AGPM adicionales para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0d6a0-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="0d6a0-128">Si no se ha configurado ninguna conexión de servidor de AGPM, siga el procedimiento anterior para configurar un servidor de AGPM predeterminado para todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="0d6a0-129">Para configurar servidores de AGPM independientes para algunos o todos los dominios (invalidando el servidor de AGPM predeterminado), edite un GPO que se aplica a todos los administradores de directiva de grupo en el árbol de **consola de administración de directivas** de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="0d6a0-130">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo.md)).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="0d6a0-131">En **configuración de usuario** en **el editor de objetos de directiva de grupo**, haga doble clic en **plantillas administrativas**, **componentes de Windows**y, a continuación, **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="0d6a0-132">En el panel de detalles, haga doble clic en **servidor de AGPM**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="0d6a0-133">En la ventana de **propiedades del servidor de AGPM** , seleccione la casilla **habilitado** y haga clic en **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="0d6a0-134">En la ventana **Mostrar contenido** :</span><span class="sxs-lookup"><span data-stu-id="0d6a0-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="0d6a0-135">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="0d6a0-136">En **nombre del valor**, escriba el nombre de dominio (por ejemplo, server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="0d6a0-137">En **valor**, escriba el nombre del servidor de AGPM y el puerto que se usarán para este dominio (por ejemplo, server2.contoso.com:4600) y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="0d6a0-138">(De forma predeterminada, el servicio AGPM escucha en el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="0d6a0-139">Para usar un puerto diferente, vea [modificar el puerto en el que el servicio AGPM escucha](modify-the-port-on-which-the-agpm-service-listens.md).)</span><span class="sxs-lookup"><span data-stu-id="0d6a0-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="0d6a0-140">Repita el procedimiento para cada dominio que no use el servidor de AGPM predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="0d6a0-141">Haga clic en **Aceptar** para cerrar las ventanas **Mostrar contenido** y **propiedades del servidor de AGPM** .</span><span class="sxs-lookup"><span data-stu-id="0d6a0-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="0d6a0-142">Cierre el **Editor de objetos de directiva de grupo**.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="0d6a0-143">(Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md)). Cuando se actualiza la Directiva de grupo, las nuevas conexiones de servidor de AGPM se configuran para todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="0d6a0-144">Si ha configurado de manera centralizada la conexión de servidor de AGPM, la opción de hacerlo manualmente no está disponible para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="0d6a0-145">Para configurar manualmente el servidor de AGPM para que se muestre en su cuenta</span><span class="sxs-lookup"><span data-stu-id="0d6a0-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="0d6a0-146">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="0d6a0-147">En el panel de detalles, haga clic en la pestaña **servidor de AGPM** .</span><span class="sxs-lookup"><span data-stu-id="0d6a0-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="0d6a0-148">Escriba el nombre de equipo completo para el servidor AGPM que administra el archivo usado para este dominio (por ejemplo, server.contoso.com) y el puerto en el que el servicio AGPM escucha (de forma predeterminada, el puerto 4600).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="0d6a0-149">Haga clic en **aplicar**y, a continuación, en **sí** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="0d6a0-150">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="0d6a0-150">Additional considerations</span></span>

-   <span data-ttu-id="0d6a0-151">Debe poder editar e implementar un GPO para realizar los procedimientos para configurar conexiones de servidor de AGPM de forma centralizada para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="0d6a0-152">Consulte [editar un GPO](editing-a-gpo.md) e [implementar un GPO](deploy-a-gpo.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="0d6a0-153">El servidor de AGPM seleccionado determina los GPO que se muestran en la pestaña **contenido** y la ubicación en la que se aplica la configuración de la pestaña de **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="0d6a0-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="0d6a0-154">Si no se administra de forma centralizada a través de la plantilla administrativa, cada administrador de directivas de grupo debe configurar esta opción para que apunte al servidor de AGPM para el dominio.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="0d6a0-155">La pertenencia al grupo propietarios del creador de directivas de grupo se debe restringir para que no se use para eludir la administración de acceso a los GPO por AGPM.</span><span class="sxs-lookup"><span data-stu-id="0d6a0-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="0d6a0-156">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="0d6a0-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="0d6a0-157">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="0d6a0-157">Additional references</span></span>

-   [<span data-ttu-id="0d6a0-158">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="0d6a0-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





