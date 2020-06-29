---
title: Guía detallada de Administración avanzada de directivas de grupo 2.5
description: Guía detallada de Administración avanzada de directivas de grupo 2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820191"
---
# <span data-ttu-id="e7780-103">Guía detallada de Administración avanzada de directivas de grupo 2.5</span><span class="sxs-lookup"><span data-stu-id="e7780-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="e7780-104">En esta guía paso a paso se muestran las técnicas avanzadas de administración de directivas de grupo con la consola de administración de directivas de grupo (GPMC) y la administración avanzada de directivas de grupo (AGPM) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e7780-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="e7780-105">AGPM aumenta las capacidades de la GPMC, proporcionando:</span><span class="sxs-lookup"><span data-stu-id="e7780-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="e7780-106">Roles estándar para delegar permisos para administrar objetos de directiva de grupo (GPO) en varios administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="e7780-107">Archivo para permitir que los administradores de directivas de grupo creen y modifiquen los GPO desconectados antes de implementarlos en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="e7780-108">La posibilidad de volver a cualquier versión anterior de un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="e7780-109">Funcionalidad de protección/desprotección para los GPO para asegurarse de que los administradores de directivas de grupo no sobrescriban accidentalmente el trabajo de los demás.</span><span class="sxs-lookup"><span data-stu-id="e7780-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="e7780-110">Información general del escenario AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-110">AGPM scenario overview</span></span>


<span data-ttu-id="e7780-111">Para este escenario, usará una cuenta de usuario independiente para cada rol en AGPM con el fin de demostrar cómo se puede administrar la Directiva de grupo en un entorno con varios administradores de directivas de grupo que tienen diferentes niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="e7780-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="e7780-112">En concreto, realizará las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="e7780-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="e7780-113">Con una cuenta que sea miembro del grupo de administradores de dominio, instale el servidor de AGPM y asigne el rol de administrador de AGPM a una cuenta o un grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="e7780-114">Con las cuentas a las que asignará roles de AGPM, instale el cliente AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="e7780-115">Usando una cuenta con el rol de administrador de AGPM, configure AGPM y delegue el acceso a los GPO asignando roles a otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="e7780-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="e7780-116">Con una cuenta que tenga la función editor, solicite la creación de un GPO, que después apruebe usando una cuenta con el rol aprobador.</span><span class="sxs-lookup"><span data-stu-id="e7780-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="e7780-117">Con la cuenta editor, compruebe el GPO fuera del archivo, edite el GPO, proteja el objeto en el archivo y solicite la implementación.</span><span class="sxs-lookup"><span data-stu-id="e7780-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="e7780-118">Con una cuenta que tenga el rol de aprobador, revise el GPO e impleméntelo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="e7780-119">Con una cuenta que tenga la función editor, cree una plantilla de GPO y úsela como punto de partida para crear un nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="e7780-120">Con una cuenta que tenga el rol de aprobador, elimine y restaure un GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![proceso de desarrollo de objetos de directiva de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="e7780-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7780-122">Requirements</span></span>


<span data-ttu-id="e7780-123">Los equipos en los que desea instalar AGPM deben cumplir los siguientes requisitos y debe crear cuentas para usarlas en este escenario.</span><span class="sxs-lookup"><span data-stu-id="e7780-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="e7780-124">Requisitos del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-124">AGPM Server requirements</span></span>

<span data-ttu-id="e7780-125">El servidor AGPM 2.5 requiere vista® (versión de 32 bits) sin Service Packs instalados o Windows Server® 2003 (versión de 32 bits), así como la GPMC.</span><span class="sxs-lookup"><span data-stu-id="e7780-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="e7780-126">Además, debe ser miembro del grupo administradores de dominio para instalar el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="e7780-127">Debe instalar el servidor AGPM en un servidor miembro o controlador de dominio con la versión más reciente de la GPMC que está disponible y que es compatible con AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="e7780-128">AGPM usa la GPMC para realizar copias de seguridad y restaurar los GPO, y las versiones más recientes de la GPMC proporcionan opciones de directiva adicionales que no están disponibles en las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e7780-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="e7780-129">Si la versión de la GPMC en el servidor AGPM es anterior a la versión de los equipos que los administradores usan para administrar la Directiva de grupo, el servidor de AGPM no podrá almacenar la configuración de directivas que no está disponible en la versión anterior de la GPMC.</span><span class="sxs-lookup"><span data-stu-id="e7780-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="e7780-130">En concreto, si su servidor de AGPM ejecuta Windows Server2003 y la versión de la GPMC que lo acompaña, y los equipos de los administradores de directivas de grupo ejecutan vista y la versión de la GPMC que lo acompaña, puede administrar la mayoría de las opciones de configuración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e7780-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="e7780-131">Sin embargo, el servidor de AGPM no puede almacenar la configuración de directivas de GPMC en Windows Vista que no están disponibles en la consola GPMC en Windows Server 2003, como las relacionadas con el redireccionamiento de carpetas, las redes inalámbricas (IEEE 802,11) e impresoras implementadas, incluso si los administradores pueden configurarlas con AGPM en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="e7780-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="e7780-132">Si debe instalar el servidor AGPM en un equipo con una versión anterior de GPMC en la que se ejecutan los administradores de directivas de grupo, consulte la referencia de configuración de directiva de grupo para obtener detalles sobre qué opciones de directiva están disponibles con qué sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="e7780-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="e7780-133">Para descargar la referencia de la configuración de directiva de grupo, consulte <https://go.microsoft.com/fwlink/?LinkID=106147> .</span><span class="sxs-lookup"><span data-stu-id="e7780-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="e7780-134">**Nota:**  Los archivos no se pueden migrar desde un servidor de AGPM o un servidor de GPOVault que ejecute Windows Server 2003 a un servidor de AGPM que ejecute vista.</span><span class="sxs-lookup"><span data-stu-id="e7780-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="e7780-135">Para Windows Server2003, si GPOVault Server está instalado en el equipo en el que desea instalar el servidor AGPM, se recomienda que no desinstale GPOVault servidor antes de comenzar la instalación.</span><span class="sxs-lookup"><span data-stu-id="e7780-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="e7780-136">La instalación del servidor de AGPM desinstalará GPOVault Server y transferirá automáticamente los datos existentes del archivo GPOVault a un archivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="e7780-137">Requisitos del cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-137">AGPM Client requirements</span></span>

<span data-ttu-id="e7780-138">El cliente AGPM 2.5 requiere vista (versión de 32 bits) sin ningún Service Pack instalado o Windows Server2003 (versión de 32 bits), así como la GPMC.</span><span class="sxs-lookup"><span data-stu-id="e7780-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="e7780-139">El cliente AGPM puede instalarse en un equipo que ejecuta el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="e7780-140">Requisitos del escenario</span><span class="sxs-lookup"><span data-stu-id="e7780-140">Scenario requirements</span></span>

<span data-ttu-id="e7780-141">Antes de empezar este escenario, cree cuatro cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7780-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="e7780-142">Durante el escenario, asignará uno de los siguientes roles de AGPM a cada una de estas cuentas: administrador de AGPM (control total), aprobador, editor y revisor.</span><span class="sxs-lookup"><span data-stu-id="e7780-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="e7780-143">Estas cuentas deben poder enviar y recibir mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e7780-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="e7780-144">Asigne el permiso **vincular GPO** a las cuentas con los roles de editor administrador de AGPM, aprobador y (opcionalmente).</span><span class="sxs-lookup"><span data-stu-id="e7780-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="e7780-145">**Nota:** 
 El permiso **vincular GPO** está asignado a miembros de administradores de dominio y administradores de empresa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e7780-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="e7780-146">Para asignar el permiso **vincular GPO** a usuarios o grupos adicionales (como cuentas con los roles de administrador o aprobador de AGPM), haga clic en el nodo del dominio y, a continuación, haga clic en la pestaña **delegación** , seleccione **vincular GPO**, haga clic en **Agregar**y seleccione los usuarios o grupos a los que desea asignar el permiso.</span><span class="sxs-lookup"><span data-stu-id="e7780-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="e7780-147">Para este escenario, debe realizar acciones con cuentas diferentes.</span><span class="sxs-lookup"><span data-stu-id="e7780-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="e7780-148">Puede iniciar sesión con cada cuenta como se indica, o puede usar el comando **Ejecutar como** para iniciar la consola GPMC con la cuenta indicada.</span><span class="sxs-lookup"><span data-stu-id="e7780-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="e7780-149">**Nota:**  Para usar el comando **Ejecutar como** con GPMC en Windows Server2003, haga clic en **Inicio**, seleccione **herramientas administrativas**, haga clic con el botón secundario en **Administración de directivas de grupo**y haga clic en **Ejecutar como**.</span><span class="sxs-lookup"><span data-stu-id="e7780-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="e7780-150">Haga clic en **el siguiente usuario** y escriba las credenciales de una cuenta.</span><span class="sxs-lookup"><span data-stu-id="e7780-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="e7780-151">Para usar el comando **Ejecutar como** con GPMC en Windows Vista, haga clic en el botón **Inicio** , seleccione **Ejecutar**y escriba **runas/user:** <em> DomainName\\UserName </em> **"MMC%WINDIR%\\system32\\gpmc.msc"** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="e7780-152">Escriba la contraseña de la cuenta cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="e7780-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="e7780-153">Pasos para instalar y configurar AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="e7780-154">Debe completar los pasos siguientes para instalar y configurar AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="e7780-155">Paso 1: instalar el servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="e7780-156">Paso 2: instalar el cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="e7780-157">Paso 3: configurar una conexión de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="e7780-158">Paso 4: configurar la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e7780-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="e7780-159">Paso 5: delegar el acceso</span><span class="sxs-lookup"><span data-stu-id="e7780-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="e7780-160">Paso 1: instalar el servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="e7780-161">En este paso, instalará el servidor AGPM en el servidor miembro o el controlador de dominio que ejecutará el servicio AGPM y configurará el archivo.</span><span class="sxs-lookup"><span data-stu-id="e7780-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="e7780-162">Todas las operaciones de AGPM se administran a través de este servicio de Windows y se ejecutan con las credenciales del servicio.</span><span class="sxs-lookup"><span data-stu-id="e7780-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="e7780-163">El archivo administrado por un servidor de AGPM puede alojarse en ese servidor o en otro servidor del mismo bosque.</span><span class="sxs-lookup"><span data-stu-id="e7780-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="e7780-164">Para instalar el servidor AGPM en el equipo que hospedará el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="e7780-165">Inicie sesión con una cuenta que sea miembro del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="e7780-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="e7780-166">Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones en pantalla para seleccionar **Administración avanzada de directivas de grupo-servidor**.</span><span class="sxs-lookup"><span data-stu-id="e7780-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="e7780-167">En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="e7780-168">En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="e7780-169">En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="e7780-170">El equipo en el que está instalado el servidor de AGPM hospedará el servicio AGPM y administrará el archivo.</span><span class="sxs-lookup"><span data-stu-id="e7780-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="e7780-171">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-171">Click **Next**.</span></span>

6.  <span data-ttu-id="e7780-172">En el cuadro de diálogo **ruta de acceso del archivo** , seleccione una ubicación para el archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="e7780-173">La ruta de acceso al archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero debe seleccionar una ubicación con suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="e7780-174">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-174">Click **Next**.</span></span>

7.  <span data-ttu-id="e7780-175">En el cuadro de diálogo **cuenta de servicio AGPM** , seleccione una cuenta de servicio en la que se ejecutará el servicio AGPM y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="e7780-176">En el cuadro de diálogo **propietario del archivo** , seleccione una cuenta o un grupo al que inicialmente desee asignar el rol de administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="e7780-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="e7780-177">Este administrador de AGPM puede asignar roles y permisos de AGPM a otros administradores de directivas de grupo (incluido el rol de administrador de AGPM).</span><span class="sxs-lookup"><span data-stu-id="e7780-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="e7780-178">Para este escenario, seleccione la cuenta que se va a usar en el rol de administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="e7780-179">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-179">Click **Next**.</span></span>

9.  <span data-ttu-id="e7780-180">Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="e7780-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="e7780-181">**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e7780-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="e7780-182">Esto puede impedir que el servicio AGPM se inicie.</span><span class="sxs-lookup"><span data-stu-id="e7780-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="e7780-183">Para obtener información sobre cómo modificar la configuración del servicio, consulte la ayuda para la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="e7780-184">Paso 2: instalar el cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="e7780-185">Cada administrador de directivas de grupo (cualquier persona que cree, edite, implemente, revise o elimine GPO) debe tener instalado un cliente AGPM en los equipos que usen para administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="e7780-186">Para este escenario, debe instalar el cliente de AGPM en un equipo como mínimo.</span><span class="sxs-lookup"><span data-stu-id="e7780-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="e7780-187">No es necesario instalar el cliente de AGPM en los equipos de los usuarios finales que no realizan la administración de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="e7780-188">Para instalar el cliente de AGPM en el equipo de un administrador de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="e7780-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="e7780-189">Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones de la pantalla para seleccionar **Advanced Group Policy Management-Client**.</span><span class="sxs-lookup"><span data-stu-id="e7780-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="e7780-190">En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="e7780-191">En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="e7780-192">En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el cliente AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="e7780-193">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-193">Click **Next**.</span></span>

5.  <span data-ttu-id="e7780-194">En el cuadro de diálogo **servidor de AGPM** , escriba el nombre de equipo completo y el puerto para el servidor de AGPM al que se conectará.</span><span class="sxs-lookup"><span data-stu-id="e7780-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="e7780-195">El puerto predeterminado para el servicio AGPM es 4600.</span><span class="sxs-lookup"><span data-stu-id="e7780-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="e7780-196">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-196">Click **Next**.</span></span>

6.  <span data-ttu-id="e7780-197">Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="e7780-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="e7780-198">Paso 3: configurar una conexión de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="e7780-199">AGPM almacena todas las versiones de cada objeto de directiva de grupo (GPO) controlado (un GPO para el cual AGPM proporciona control de cambios) en un archivo central, de modo que los administradores de directivas de grupo puedan ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="e7780-200">En este paso, puede configurar una conexión de servidor de AGPM y asegurarse de que todos los administradores de directivas de grupo se conecten al mismo servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="e7780-201">(Para obtener información acerca de la configuración de varios servidores de AGPM, consulte ayuda para la administración avanzada de directivas de grupo).</span><span class="sxs-lookup"><span data-stu-id="e7780-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="e7780-202">Para configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="e7780-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="e7780-203">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con la cuenta de usuario que seleccionó como propietario del archivo.</span><span class="sxs-lookup"><span data-stu-id="e7780-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="e7780-204">Este usuario tiene el rol de administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="e7780-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="e7780-205">Haga clic en **Inicio**, seleccione **herramientas administrativas**y haga clic en **Administración de directivas de grupo** para abrir la consola de administración de directivas de **grupo (GPMC)**.</span><span class="sxs-lookup"><span data-stu-id="e7780-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="e7780-206">En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="e7780-207">En la ventana **Editor de objetos de directiva de grupo** , haga clic en configuración de **usuario**, **plantillas administrativas**y **componentes de Windows**.</span><span class="sxs-lookup"><span data-stu-id="e7780-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="e7780-208">Si **AGPM** no aparece en **componentes de Windows**:</span><span class="sxs-lookup"><span data-stu-id="e7780-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="e7780-209">Haga clic con el botón secundario en **plantillas administrativas** y seleccione **Agregar o quitar plantillas**.</span><span class="sxs-lookup"><span data-stu-id="e7780-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="e7780-210">Haga clic en **Agregar**, seleccione **AGPM. ADMX** o **AGPM. adm**, haga clic en **abrir**y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="e7780-211">En **componentes de Windows**, haga doble clic en **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="e7780-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="e7780-212">En el panel de detalles, haga doble clic en **servidor de AGPM (todos los dominios)**.</span><span class="sxs-lookup"><span data-stu-id="e7780-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="e7780-213">En la ventana de **propiedades del servidor de AGPM (todos los dominios)** , seleccione **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, Server.contoso.com:4600) para el servidor que hospeda el archivo.</span><span class="sxs-lookup"><span data-stu-id="e7780-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="e7780-214">El puerto que usa el servicio AGPM es el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="e7780-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="e7780-215">Haga clic en **Aceptar**y, a continuación, cierre la ventana **Editor de objetos de directiva de grupo** .</span><span class="sxs-lookup"><span data-stu-id="e7780-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="e7780-216">Cuando se actualiza la Directiva de grupo, se configura la conexión del servidor de AGPM para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="e7780-217">Paso 4: configurar la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e7780-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="e7780-218">Como administrador de AGPM (control total), usted designa las direcciones de correo electrónico de los aprobadores y administradores de AGPM a los que se envía un mensaje de correo electrónico que contiene una solicitud cuando un editor intenta crear, implementar o eliminar un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="e7780-219">También puede determinar el alias desde el que se envían estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="e7780-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="e7780-220">Para configurar la notificación de correo electrónico para AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="e7780-221">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e7780-222">En el panel de detalles, haga clic en la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="e7780-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="e7780-223">En el campo **de** , escriba el alias de correo electrónico de AGPM desde el que se deben enviar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e7780-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="e7780-224">En el campo **para** , escriba la dirección de correo electrónico de la cuenta de usuario a la que desea asignar el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="e7780-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="e7780-225">En el campo **servidor SMTP** , escriba un servidor de correo SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="e7780-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="e7780-226">En los campos **nombre de usuario** y **contraseña** , escriba las credenciales de un usuario con acceso al servicio SMTP.</span><span class="sxs-lookup"><span data-stu-id="e7780-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="e7780-227">Haz clic en **Apply**.</span><span class="sxs-lookup"><span data-stu-id="e7780-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="e7780-228">Paso 5: delegar el acceso</span><span class="sxs-lookup"><span data-stu-id="e7780-228">Step 5: Delegate access</span></span>

<span data-ttu-id="e7780-229">Como administrador de AGPM (control total), puede delegar el acceso de nivel de dominio a los GPO, asignando roles a la cuenta de cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="e7780-230">**Nota:**  También puede delegar el acceso en el nivel de GPO en lugar del nivel de dominio.</span><span class="sxs-lookup"><span data-stu-id="e7780-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="e7780-231">Para obtener más información, consulte ayuda para la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="e7780-232">**Importante**  Debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, de modo que no pueda usarse para eludir la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="e7780-233">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="e7780-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="e7780-234">Para delegar el acceso a todos los GPO en un dominio</span><span class="sxs-lookup"><span data-stu-id="e7780-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="e7780-235">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e7780-236">En la pestaña **delegación de dominios** , haga clic en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="e7780-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="e7780-237">En el cuadro de diálogo **permisos** :</span><span class="sxs-lookup"><span data-stu-id="e7780-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="e7780-238">Haga clic en la cuenta de usuario de un administrador de directivas de grupo y, a continuación, seleccione la casilla **aprobador** para asignar ese rol a la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e7780-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="e7780-239">Desactive la casilla **Editor** .</span><span class="sxs-lookup"><span data-stu-id="e7780-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="e7780-240">(Este rol incluye el rol de revisor).</span><span class="sxs-lookup"><span data-stu-id="e7780-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="e7780-241">Haga clic en la cuenta de usuario de otro administrador de directiva de grupo y, a continuación, seleccione la casilla **Editor** para asignar ese rol a la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e7780-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="e7780-242">(Este rol incluye el rol de revisor).</span><span class="sxs-lookup"><span data-stu-id="e7780-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="e7780-243">Haga clic en una tercera cuenta y, a continuación, seleccione la casilla **Revisor** para asignar solo el rol de revisor a la cuenta de ese administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="e7780-244">Desactive la casilla **Editor** .</span><span class="sxs-lookup"><span data-stu-id="e7780-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="e7780-245">Haga clic en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="e7780-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="e7780-246">En el cuadro de diálogo **configuración de seguridad avanzada** :</span><span class="sxs-lookup"><span data-stu-id="e7780-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="e7780-247">Seleccione un administrador de directivas de grupo y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="e7780-248">En **aplicar en**, seleccione **este objeto y los objetos anidados**y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **entrada** de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="e7780-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="e7780-249">Repita el procedimiento para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="e7780-250">En el cuadro de diálogo **configuración de seguridad avanzada** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="e7780-251">En el cuadro de diálogo **permisos** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="e7780-252">Pasos para administrar GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-252">Steps for managing GPOs</span></span>


<span data-ttu-id="e7780-253">Debe completar los pasos siguientes para crear, editar, revisar e implementar GPO con AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="e7780-254">Además, creará una plantilla, eliminará un objeto de directiva de grupo y restaurará un objeto de directiva de grupo eliminado.</span><span class="sxs-lookup"><span data-stu-id="e7780-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="e7780-255">Paso 1: crear un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="e7780-256">Paso 2: editar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="e7780-257">Paso 3: revisar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="e7780-258">Paso 4: usar una plantilla para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="e7780-259">Paso 5: eliminar y restaurar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="e7780-260">Paso 1: crear un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="e7780-261">En un entorno con varios administradores de directivas de grupo, los usuarios con el rol Editor tienen la capacidad de solicitar la creación de nuevos GPO, pero dicha solicitud debe ser aprobada por alguien con el rol de aprobador, ya que la creación de un nuevo objeto de directiva de grupo afecta al entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="e7780-262">En este paso, usará una cuenta con la función editor para solicitar la creación de un nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="e7780-263">Con una cuenta que tenga el rol de aprobador, apruebe esta solicitud y complete la creación de un GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="e7780-264">Para solicitar la creación de un GPO nuevo administrado a través de AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="e7780-265">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado la función editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="e7780-266">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e7780-267">Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="e7780-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="e7780-268">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="e7780-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="e7780-269">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="e7780-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="e7780-270">Escriba **MyGPO** como nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="e7780-271">Escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="e7780-272">Haga clic en **crear en vivo** para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="e7780-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="e7780-273">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="e7780-274">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-275">El nuevo GPO se muestra en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="e7780-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="e7780-276">Para aprobar la solicitud pendiente para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="e7780-277">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="e7780-278">Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud del editor para crear un GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="e7780-279">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="e7780-280">En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.</span><span class="sxs-lookup"><span data-stu-id="e7780-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="e7780-281">Haga clic con el botón derecho en **MyGPO**y luego en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="e7780-282">Haga clic en **sí** para confirmar la aprobación de la creación del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="e7780-283">El objeto de directiva de grupo se mueve a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="e7780-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="e7780-284">Paso 2: editar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="e7780-285">Puede usar los GPO para configurar las opciones de usuario o de equipo e implementarlas en muchos equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="e7780-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="e7780-286">En este paso, se usa una cuenta con el rol Editor para desproteger un GPO desde el archivo, editar el GPO sin conexión, comprobar el GPO editado en el archivo y solicitar la implementación del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="e7780-287">Para este escenario, debe configurar una opción de configuración en el GPO para requerir que la contraseña tenga al menos ocho caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="e7780-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="e7780-288">Para comprobar el GPO fuera del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="e7780-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="e7780-289">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="e7780-290">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e7780-291">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="e7780-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="e7780-292">Haga clic con el botón derecho en **MyGPO**y, después, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="e7780-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="e7780-293">Escriba un comentario para que aparezca en el **historial** del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="e7780-294">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-295">En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="e7780-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="e7780-296">Para modificar el GPO sin conexión y configurar la longitud mínima de la contraseña</span><span class="sxs-lookup"><span data-stu-id="e7780-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="e7780-297">En la pestaña **controlado** , haga clic con el botón secundario en **MyGPO**y, a continuación, haga clic en **Editar** para abrir la ventana Editor de objetos de **Directiva de grupo** y realizar cambios en una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="e7780-298">Para este escenario, configure la longitud mínima de la contraseña:</span><span class="sxs-lookup"><span data-stu-id="e7780-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="e7780-299">En **configuración del equipo**, haga doble clic en **configuración de Windows**, haga doble clic en **configuración de seguridad**, haga doble clic en directivas de **cuenta**y haga doble clic en **Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="e7780-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="e7780-300">En el panel de detalles, haga doble clic en **longitud mínima**de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e7780-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="e7780-301">En la ventana Propiedades, active la casilla **definir esta configuración de directiva** , establezca el número de caracteres en **8**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="e7780-302">Cierre la ventana **Editor de objetos de directiva de grupo** .</span><span class="sxs-lookup"><span data-stu-id="e7780-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="e7780-303">Para comprobar el objeto de directiva de grupo en el archivo</span><span class="sxs-lookup"><span data-stu-id="e7780-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="e7780-304">En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **proteger**.</span><span class="sxs-lookup"><span data-stu-id="e7780-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="e7780-305">Escriba un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="e7780-306">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-307">En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.</span><span class="sxs-lookup"><span data-stu-id="e7780-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="e7780-308">Para solicitar la implementación del GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="e7780-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="e7780-309">En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **implementar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="e7780-310">Como esta cuenta no es aprobador o administrador AGPM, debe enviar una solicitud de implementación.</span><span class="sxs-lookup"><span data-stu-id="e7780-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="e7780-311">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="e7780-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="e7780-312">Escriba un comentario para que aparezca en el **historial** del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="e7780-313">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-314">**MyGPO** se muestra en la lista de GPO en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="e7780-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="e7780-315">Paso 3: revisar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="e7780-316">En este paso, usted actúa como aprobador, creando informes y analizando la configuración y los cambios en la configuración del GPO para determinar si debe aprobarlos.</span><span class="sxs-lookup"><span data-stu-id="e7780-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="e7780-317">Después de evaluar el GPO, impleméntelo en el entorno de producción y vincúlelo a un dominio o una unidad organizativa (OU) para que tenga efecto cuando se actualice la Directiva de grupo de los equipos de ese dominio o unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="e7780-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="e7780-318">Para revisar la configuración en el GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="e7780-319">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="e7780-320">(Cualquier administrador de directiva de grupo con el rol de revisor, que se incluye en todos los demás roles, puede revisar la configuración de un GPO).</span><span class="sxs-lookup"><span data-stu-id="e7780-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="e7780-321">Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud de un editor para implementar un GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="e7780-322">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="e7780-323">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="e7780-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="e7780-324">Haga doble clic en **MyGPO** para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="e7780-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="e7780-325">Revise la configuración de la versión más reciente de MyGPO:</span><span class="sxs-lookup"><span data-stu-id="e7780-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="e7780-326">En la ventana **historial** , haga clic con el botón secundario en la versión de GPO con la marca de tiempo más reciente, haga clic en **configuración**y, después, haga clic en **Informe HTML** para mostrar un resumen de la configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="e7780-327">En el explorador Web, haga clic en **Mostrar todo** para ver todas las opciones de configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="e7780-328">Cierra el explorador.</span><span class="sxs-lookup"><span data-stu-id="e7780-328">Close the browser.</span></span>

7.  <span data-ttu-id="e7780-329">Compare la versión más reciente de MyGPO con la primera versión protegida en el archivo:</span><span class="sxs-lookup"><span data-stu-id="e7780-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="e7780-330">En la ventana **historial** , haga clic en la versión de GPO con la marca de hora más reciente.</span><span class="sxs-lookup"><span data-stu-id="e7780-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="e7780-331">Presione **Ctrl** y haga clic en la versión de GPO más antigua que tenga el estado **protegido**.</span><span class="sxs-lookup"><span data-stu-id="e7780-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="e7780-332">Haga clic en el botón **diferencias** .</span><span class="sxs-lookup"><span data-stu-id="e7780-332">Click the **Differences** button.</span></span> <span data-ttu-id="e7780-333">La sección **directivas de cuenta/Directiva de contraseña** está resaltada en verde y precedida de **\ [+ \]**, lo que indica que esta configuración está configurada únicamente en la última versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="e7780-334">Haga clic en **directivas de cuenta/Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="e7780-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="e7780-335">La configuración de **longitud mínima** de la contraseña también está resaltada en verde y precedida de **\ [+ \]**, lo que indica que está configurada solo en la última versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="e7780-336">Cierre el explorador Web.</span><span class="sxs-lookup"><span data-stu-id="e7780-336">Close the Web browser.</span></span>

**<span data-ttu-id="e7780-337">Para implementar el GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="e7780-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="e7780-338">En la pestaña **pendiente** , haga clic con el botón derecho en **MyGPO** y, a continuación, haga clic en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="e7780-339">Escriba un comentario para incluirlo en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="e7780-340">Haz clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="e7780-340">Click **Yes**.</span></span> <span data-ttu-id="e7780-341">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-342">El objeto de directiva de grupo se implementa en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="e7780-343">Para vincular el GPO a un dominio o unidad de organización</span><span class="sxs-lookup"><span data-stu-id="e7780-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="e7780-344">En la GPMC, haga clic con el botón secundario en el dominio o en una unidad organizativa a la que desee aplicar el GPO que ha configurado y, a continuación, haga clic en **vincular un GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="e7780-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="e7780-345">En el cuadro de diálogo **seleccionar GPO** , haga clic en **MyGPO**y, después, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="e7780-346">Paso 4: usar una plantilla para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="e7780-347">En este paso, se usa una cuenta con la función editor para crear una plantilla (una versión no modificable y estática de un GPO para usarla como punto de partida para crear nuevos GPO) y, a continuación, crear un GPO nuevo basado en esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="e7780-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="e7780-348">Las plantillas son útiles para crear rápidamente varios GPO que incluyan muchos de los ajustes de configuración.</span><span class="sxs-lookup"><span data-stu-id="e7780-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="e7780-349">Para crear una plantilla basada en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="e7780-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="e7780-350">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="e7780-351">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e7780-352">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="e7780-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="e7780-353">Haga clic con el botón derecho en **MyGPO**y, a continuación, haga clic en **Guardar como plantilla** para crear una plantilla que incorpore toda la configuración que se encuentra en MyGPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="e7780-354">Escriba **MyTemplate** como el nombre de la plantilla y un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="e7780-355">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-356">La nueva plantilla aparecerá en la ficha **plantillas** .</span><span class="sxs-lookup"><span data-stu-id="e7780-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="e7780-357">Para solicitar la creación de un GPO nuevo administrado a través de AGPM</span><span class="sxs-lookup"><span data-stu-id="e7780-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="e7780-358">Haga clic en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="e7780-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="e7780-359">Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="e7780-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="e7780-360">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="e7780-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="e7780-361">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="e7780-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="e7780-362">Escriba **MyOtherGPO** como nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="e7780-363">Escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="e7780-364">Haga clic en **crear en vivo**para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="e7780-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="e7780-365">En **plantilla de GPO de**para **, seleccione MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="e7780-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="e7780-366">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="e7780-367">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-368">El nuevo GPO se muestra en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="e7780-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="e7780-369">Use una cuenta a la que se le haya asignado el rol de aprobador para aprobar la solicitud pendiente para crear el GPO como hizo en el [paso 1: crear un GPO](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="e7780-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="e7780-370">MyTemplate incorpora toda la configuración que ha configurado en MyGPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="e7780-371">Como MyOtherGPO se creó con MyTemplate, inicialmente contiene toda la configuración que MyGPO en el momento en que se creó MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="e7780-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="e7780-372">Puede confirmarlo generando un informe de diferencias para comparar MyOtherGPO con MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="e7780-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="e7780-373">Para comprobar el GPO fuera del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="e7780-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="e7780-374">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e7780-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="e7780-375">Haga clic con el botón derecho en **MyOtherGPO**y, después, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="e7780-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="e7780-376">Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="e7780-377">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-378">En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="e7780-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="e7780-379">Para editar el GPO sin conexión y configurar la duración del bloqueo de cuenta</span><span class="sxs-lookup"><span data-stu-id="e7780-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="e7780-380">En la pestaña **controlado** , haga clic con el botón secundario en **MyOtherGPO**y, a continuación, haga clic en **Editar** para abrir la ventana Editor de objetos de **Directiva de grupo** y realizar cambios en una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="e7780-381">Para este escenario, configure la longitud mínima de la contraseña:</span><span class="sxs-lookup"><span data-stu-id="e7780-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="e7780-382">En **configuración del equipo**, haga doble clic en **configuración de Windows**, haga doble clic en **configuración de seguridad**, haga doble clic en directivas de **cuenta**y haga doble clic en Directiva de **bloqueo de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="e7780-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="e7780-383">En el panel de detalles, haga doble clic en **duración del bloqueo de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="e7780-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="e7780-384">En la ventana Propiedades, seleccione **definir esta configuración de directiva**, establezca la duración en **30** minutos y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="e7780-385">Cierre la ventana **Editor de objetos de directiva de grupo** .</span><span class="sxs-lookup"><span data-stu-id="e7780-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="e7780-386">Visite MyOtherGPO en el archivo y solicite la implementación como hizo para MyGPO en el [paso 2: editar un GPO](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="e7780-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="e7780-387">Puede comparar MyOtherGPO con MyGPO o con MyTemplate mediante informes de diferencias.</span><span class="sxs-lookup"><span data-stu-id="e7780-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="e7780-388">Cualquier cuenta que incluya el rol de revisor (Administrador AGPM \ [control total \], aprobador, editor o revisor) puede generar informes.</span><span class="sxs-lookup"><span data-stu-id="e7780-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="e7780-389">Para comparar un GPO con otro GPO y con una plantilla</span><span class="sxs-lookup"><span data-stu-id="e7780-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="e7780-390">Para comparar MyGPO y MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="e7780-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="e7780-391">En la pestaña **controlado** , haga clic en **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="e7780-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="e7780-392">Presione **Ctrl** y, a continuación, haga clic en **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="e7780-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="e7780-393">Haga clic con el botón derecho en **MyOtherGPO**, apunte a **diferencias**y haga clic en **Informe HTML**.</span><span class="sxs-lookup"><span data-stu-id="e7780-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="e7780-394">Para comparar MyOtherGPO y MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="e7780-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="e7780-395">En la pestaña **controlado** , haga clic en **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="e7780-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="e7780-396">Haga clic con el botón derecho en **MyOtherGPO**, apunte a **diferencias**y haga clic en **plantilla**.</span><span class="sxs-lookup"><span data-stu-id="e7780-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="e7780-397">Seleccione **MyTemplate** y **Informe html**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="e7780-398">Paso 5: eliminar y restaurar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="e7780-399">En este paso, actuará como aprobador para eliminar un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e7780-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="e7780-400">Para eliminar un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="e7780-401">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="e7780-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="e7780-402">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e7780-403">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="e7780-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="e7780-404">Haga clic con el botón derecho en **MyGPO**y luego haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="e7780-405">Haga clic en **eliminar GPO de archivo y producción** para eliminar la versión del archivo, así como la versión implementada del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="e7780-406">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="e7780-407">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-408">El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.</span><span class="sxs-lookup"><span data-stu-id="e7780-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="e7780-409">En ocasiones, es posible que desconozcas después de eliminar un objeto de directiva de grupo que aún es necesario.</span><span class="sxs-lookup"><span data-stu-id="e7780-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="e7780-410">En este paso, usted actúa como aprobador para restaurar un GPO que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="e7780-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="e7780-411">Para restaurar un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="e7780-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="e7780-412">En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.</span><span class="sxs-lookup"><span data-stu-id="e7780-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="e7780-413">Haga clic con el botón derecho en **MyGPO**y luego haga clic en **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="e7780-414">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="e7780-415">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-416">El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="e7780-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="e7780-417">**Nota:**  Al restaurar un GPO en el archivo, no se vuelve a implementar automáticamente en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e7780-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="e7780-418">Para devolver el GPO al entorno de producción, implemente el GPO como en el [paso 3: revisar e implementar un GPO](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="e7780-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="e7780-419">Después de editar e implementar un GPO, es posible que descubra que los cambios recientes en el GPO están causando el problema.</span><span class="sxs-lookup"><span data-stu-id="e7780-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="e7780-420">En este paso, actuará como aprobador para volver a una versión anterior del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="e7780-421">Puede revertir a cualquier versión en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="e7780-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="e7780-422">Puede usar los comentarios y las etiquetas para identificar las versiones correctas y cuando se han realizado cambios específicos.</span><span class="sxs-lookup"><span data-stu-id="e7780-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="e7780-423">Para volver a una versión anterior de un GPO</span><span class="sxs-lookup"><span data-stu-id="e7780-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="e7780-424">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="e7780-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="e7780-425">Haga doble clic en **MyGPO** para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="e7780-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="e7780-426">Haga clic con el botón secundario en la versión que se va a implementar, haga clic en **implementar**y luego haga clic en **sí**.</span><span class="sxs-lookup"><span data-stu-id="e7780-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="e7780-427">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e7780-428">En la ventana **historial** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e7780-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="e7780-429">**Nota:**  Para comprobar que la versión reimplementada es la versión prevista, examine un informe de diferencias para las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="e7780-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="e7780-430">En la ventana **historial** del GPO, seleccione las dos versiones, haga clic con el botón secundario, seleccione **diferencia**y, a continuación, haga clic en **Informe HTML** o **Informe XML**.</span><span class="sxs-lookup"><span data-stu-id="e7780-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





