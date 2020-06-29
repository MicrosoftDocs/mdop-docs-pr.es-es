---
title: Configurar conexiones de servidor AGPM
description: Configurar conexiones de servidor AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819071"
---
# <span data-ttu-id="45899-103">Configurar conexiones de servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="45899-103">Configure AGPM Server Connections</span></span>


<span data-ttu-id="45899-104">Todas las versiones de cada objeto de directiva de grupo (GPO) controlado se almacenan en un archivo central para que los administradores de directivas de grupo puedan ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="45899-104">All versions of each controlled Group Policy Object (GPO) are stored in a central archive so that Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="45899-105">Una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO usado en estos procedimientos o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM) para completar estos procedimientos para la configuración centralizada de las ubicaciones de archivo para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="45899-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="45899-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="45899-107">Configurar conexiones de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="45899-107">Configuring AGPM Server connections</span></span>


<span data-ttu-id="45899-108">Como administrador de AGPM, puede asegurarse de que todos los administradores de directivas de grupo se conecten al mismo servidor de AGPM mediante la configuración centralizada de la configuración asociada.</span><span class="sxs-lookup"><span data-stu-id="45899-108">As an AGPM Administrator, you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the associated setting.</span></span> <span data-ttu-id="45899-109">Si su entorno requiere servidores AGPM independientes para algunos o todos los dominios, configure esos servidores de AGPM adicionales como excepciones a la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="45899-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="45899-110">Si no configura de forma centralizada las conexiones de servidor de AGPM, cada administrador de directivas de grupo debe configurar manualmente el servidor de AGPM para que se muestre en cada dominio.</span><span class="sxs-lookup"><span data-stu-id="45899-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="45899-111">Configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="45899-111">Configure an AGPM Server connection for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="45899-112">Configurar conexiones de servidores AGPM adicionales para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="45899-112">Configure additional AGPM Server connections for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="45899-113">Configurar manualmente una conexión de servidor de AGPM para su cuenta</span><span class="sxs-lookup"><span data-stu-id="45899-113">Manually configure an AGPM Server connection for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="45899-114">Para configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="45899-114">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="45899-115">En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="45899-116">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm40.md)).</span><span class="sxs-lookup"><span data-stu-id="45899-116">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="45899-117">En la **ventana Editor de administración de directivas de grupo** , haga clic en configuración de **usuario**, **directivas**, **plantillas administrativas**, **componentes de Windows**y **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="45899-117">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="45899-118">En el panel de detalles, haga doble clic en **AGPM: especificar el servidor de AGPM predeterminado (todos los dominios)**.</span><span class="sxs-lookup"><span data-stu-id="45899-118">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

4.  <span data-ttu-id="45899-119">En la ventana **propiedades** , active la casilla de verificación **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="45899-119">In the **Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

5.  <span data-ttu-id="45899-120">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="45899-120">Click **OK**.</span></span> <span data-ttu-id="45899-121">A menos que desee configurar conexiones de servidor AGPM adicionales, cierre la ventana **Editor de administración de directivas de grupo** e implemente el GPO.</span><span class="sxs-lookup"><span data-stu-id="45899-121">Unless you want to configure additional AGPM Server connections, close the **Group Policy Management Editor** window and deploy the GPO.</span></span> <span data-ttu-id="45899-122">(Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm40.md)). Cuando se actualiza la Directiva de grupo, la conexión del servidor de AGPM está configurada para todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-122">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="45899-123">Para configurar conexiones de servidores AGPM adicionales para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="45899-123">To configure additional AGPM Server connections for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="45899-124">Si no se ha configurado ninguna conexión de servidor de AGPM, siga el procedimiento anterior para configurar un servidor de AGPM predeterminado para todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="45899-124">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="45899-125">Para configurar servidores de AGPM independientes para algunos o todos los dominios (invalidando el servidor de AGPM predeterminado), edite un GPO que se aplica a todos los administradores de directiva de grupo en el árbol de **consola de administración de directivas** de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-125">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="45899-126">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm40.md)).</span><span class="sxs-lookup"><span data-stu-id="45899-126">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

3.  <span data-ttu-id="45899-127">En la **ventana Editor de administración de directivas de grupo** , haga clic en configuración de **usuario**, **directivas**, **plantillas administrativas**, **componentes de Windows**y, a continuación, **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="45899-127">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="45899-128">En el panel de detalles, haga doble clic en **AGPM: especifique los servidores de AGPM**.</span><span class="sxs-lookup"><span data-stu-id="45899-128">In the details pane, double-click **AGPM: Specify AGPM Servers**.</span></span>

5.  <span data-ttu-id="45899-129">En la ventana **propiedades** , seleccione la casilla de verificación **habilitado** y haga clic en **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="45899-129">In the **Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="45899-130">En la ventana **Mostrar contenido** :</span><span class="sxs-lookup"><span data-stu-id="45899-130">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="45899-131">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="45899-131">Click **Add**.</span></span>

    2.  <span data-ttu-id="45899-132">En **nombre del valor**, escriba el nombre de dominio (por ejemplo, server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="45899-132">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="45899-133">En **valor**, escriba el nombre del servidor de AGPM y el puerto que se usarán para este dominio (por ejemplo, server2.contoso.com:4600) y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="45899-133">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="45899-134">(De forma predeterminada, el servicio AGPM escucha en el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="45899-134">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="45899-135">Para usar un puerto diferente, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="45899-135">To use a different port, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).)</span></span>

    4.  <span data-ttu-id="45899-136">Repita el procedimiento para cada dominio que no use el servidor de AGPM predeterminado.</span><span class="sxs-lookup"><span data-stu-id="45899-136">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="45899-137">Haga clic en **Aceptar** para cerrar las ventanas **Mostrar contenido** y **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="45899-137">Click **OK** to close the **Show Contents** and **Properties** windows.</span></span>

8.  <span data-ttu-id="45899-138">Cierre la ventana del **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="45899-138">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="45899-139">(Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm40.md)). Cuando se actualiza la Directiva de grupo, las nuevas conexiones de servidor de AGPM se configuran para todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-139">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="45899-140">Si ha configurado de forma centralizada la conexión de servidor de AGPM, la opción para configurarla manualmente no está disponible para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-140">If you have centrally configured the AGPM Server connection, the option to manually configure it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="45899-141">Para configurar manualmente qué servidor de AGPM Mostrar para su cuenta</span><span class="sxs-lookup"><span data-stu-id="45899-141">To manually configure which AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="45899-142">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="45899-142">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="45899-143">En el panel de detalles, haga clic en la pestaña **servidor de AGPM** .</span><span class="sxs-lookup"><span data-stu-id="45899-143">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="45899-144">Escriba el nombre de equipo completo para el servidor AGPM que administra el archivo usado para este dominio (por ejemplo, server.contoso.com) y el puerto en el que el servicio AGPM escucha (de forma predeterminada, el puerto 4600).</span><span class="sxs-lookup"><span data-stu-id="45899-144">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="45899-145">Haga clic en **aplicar**y, a continuación, en **sí** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="45899-145">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="45899-146">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="45899-146">Additional considerations</span></span>

-   <span data-ttu-id="45899-147">Debe poder editar e implementar un GPO para realizar los procedimientos para configurar conexiones de servidor de AGPM de forma centralizada para todos los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="45899-147">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="45899-148">Consulte [editar un GPO](editing-a-gpo-agpm40.md) e [implementar un GPO](deploy-a-gpo-agpm40.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="45899-148">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

-   <span data-ttu-id="45899-149">El servidor de AGPM seleccionado determina los GPO que se muestran en la pestaña **contenido** y la ubicación en la que se aplica la configuración de la pestaña de **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="45899-149">The selected AGPM Server determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="45899-150">Si no se administra de forma centralizada a través de la plantilla administrativa, cada administrador de directivas de grupo debe configurar esta opción para que apunte al servidor de AGPM para el dominio.</span><span class="sxs-lookup"><span data-stu-id="45899-150">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="45899-151">Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="45899-151">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="45899-152">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="45899-152">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="45899-153">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="45899-153">Additional references</span></span>

-   [<span data-ttu-id="45899-154">Configuración de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="45899-154">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





