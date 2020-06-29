---
title: Guía detallada de Administración avanzada de directivas de grupo de Microsoft 3.0
description: Guía detallada de Administración avanzada de directivas de grupo de Microsoft 3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818330"
---
# <span data-ttu-id="f50d6-103">Guía detallada de Administración avanzada de directivas de grupo de Microsoft 3.0</span><span class="sxs-lookup"><span data-stu-id="f50d6-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="f50d6-104">En esta guía paso a paso se muestran las técnicas avanzadas de administración de directivas de grupo con la consola de administración de directivas de grupo (GPMC) y la administración avanzada de directivas de grupo (AGPM) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f50d6-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="f50d6-105">AGPM aumenta las capacidades de la GPMC, proporcionando:</span><span class="sxs-lookup"><span data-stu-id="f50d6-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="f50d6-106">Roles estándar para delegar permisos para administrar objetos de directiva de grupo (GPO) en varios administradores de la Directiva de grupo, así como la capacidad de delegar el acceso a los GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="f50d6-107">Archivo para permitir que los administradores de directivas de grupo creen y modifiquen los GPO desconectados antes de implementarlos en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="f50d6-108">La posibilidad de volver a cualquier versión anterior de un GPO en el archivo y limitar el número de versiones almacenadas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="f50d6-109">Funcionalidad de protección/desprotección para los GPO para asegurarse de que los administradores de directivas de grupo no sobrescriban accidentalmente el trabajo de los demás.</span><span class="sxs-lookup"><span data-stu-id="f50d6-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="f50d6-110">Información general del escenario AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-110">AGPM scenario overview</span></span>


<span data-ttu-id="f50d6-111">Para este escenario, usará una cuenta de usuario independiente para cada rol en AGPM con el fin de demostrar cómo se puede administrar la Directiva de grupo en un entorno con varios administradores de directivas de grupo que tienen diferentes niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="f50d6-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="f50d6-112">En concreto, realizará las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="f50d6-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="f50d6-113">Con una cuenta que sea miembro del grupo de administradores de dominio, instale el servidor de AGPM y asigne el rol de administrador de AGPM a una cuenta o un grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="f50d6-114">Con las cuentas a las que asignará roles de AGPM, instale el cliente AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="f50d6-115">Usando una cuenta con el rol de administrador de AGPM, configure AGPM y delegue el acceso a los GPO asignando roles a otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="f50d6-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="f50d6-116">Con una cuenta que tenga la función editor, solicite la creación de un GPO, que después apruebe usando una cuenta con el rol aprobador.</span><span class="sxs-lookup"><span data-stu-id="f50d6-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="f50d6-117">Con la cuenta editor, compruebe el GPO fuera del archivo, edite el GPO, proteja el objeto en el archivo y solicite la implementación.</span><span class="sxs-lookup"><span data-stu-id="f50d6-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="f50d6-118">Con una cuenta que tenga el rol de aprobador, revise el GPO e impleméntelo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="f50d6-119">Con una cuenta que tenga la función editor, cree una plantilla de GPO y úsela como punto de partida para crear un nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="f50d6-120">Con una cuenta que tenga el rol de aprobador, elimine y restaure un GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![proceso de desarrollo de objetos de directiva de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="f50d6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f50d6-122">Requirements</span></span>


<span data-ttu-id="f50d6-123">Los equipos en los que desea instalar AGPM deben cumplir los siguientes requisitos y debe crear cuentas para usarlas en este escenario.</span><span class="sxs-lookup"><span data-stu-id="f50d6-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="f50d6-124">**Nota:**  Si tiene instalado AGPM 2,5 y está actualizando Windows Server® 2003 a Windows Server2008 o vista® sin ningún Service Pack instalado en vista con Service Pack1, debe actualizar el sistema operativo antes de poder actualizar a AGPM 3.0.</span><span class="sxs-lookup"><span data-stu-id="f50d6-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="f50d6-125">Requisitos del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-125">AGPM Server requirements</span></span>

<span data-ttu-id="f50d6-126">AGPM Server 3.0 requiere que Windows Server2008 o vista con Service Pack1 y la GPMC de las herramientas de administración de servidor remoto (RSAT) estén instaladas.</span><span class="sxs-lookup"><span data-stu-id="f50d6-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="f50d6-127">Se admiten las versiones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f50d6-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="f50d6-128">Antes de instalar el servidor AGPM, debe ser miembro del grupo administradores de dominio y las siguientes características de Windows deben estar presentes, a menos que se indique lo contrario:</span><span class="sxs-lookup"><span data-stu-id="f50d6-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="f50d6-129">GPMC</span><span class="sxs-lookup"><span data-stu-id="f50d6-129">GPMC</span></span>

    -   <span data-ttu-id="f50d6-130">Windows Server 2008: AGPM instala automáticamente la consola GPMC si no está presente.</span><span class="sxs-lookup"><span data-stu-id="f50d6-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="f50d6-131">Windows Vista: debe instalar la consola GPMC desde RSAT antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="f50d6-132">Para obtener más información, consulte <https://go.microsoft.com/fwlink/?LinkID=116179> .</span><span class="sxs-lookup"><span data-stu-id="f50d6-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="f50d6-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="f50d6-133">.NET Framework 3.5</span></span>

<span data-ttu-id="f50d6-134">El servidor de AGPM requiere las siguientes características de Windows, que se instalarán automáticamente si no están presentes:</span><span class="sxs-lookup"><span data-stu-id="f50d6-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="f50d6-135">Activación de WCF; Activación no HTTP</span><span class="sxs-lookup"><span data-stu-id="f50d6-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="f50d6-136">Servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="f50d6-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="f50d6-137">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="f50d6-137">Process Model</span></span>

    -   <span data-ttu-id="f50d6-138">Entorno .NET</span><span class="sxs-lookup"><span data-stu-id="f50d6-138">.NET Environment</span></span>

    -   <span data-ttu-id="f50d6-139">API de configuración</span><span class="sxs-lookup"><span data-stu-id="f50d6-139">Configuration APIs</span></span>

### <span data-ttu-id="f50d6-140">Requisitos del cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-140">AGPM Client requirements</span></span>

<span data-ttu-id="f50d6-141">Para el cliente de AGPM 3.0 se necesita Windows Server2008 o vista con Service Pack 1 y la GPMC de las herramientas de administración de servidor remoto (RSAT) instaladas.</span><span class="sxs-lookup"><span data-stu-id="f50d6-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="f50d6-142">Se admiten las versiones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f50d6-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="f50d6-143">El cliente AGPM puede instalarse en un equipo que ejecuta el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="f50d6-144">Las siguientes características de Windows son obligatorias para el cliente de AGPM y se instalarán automáticamente si no están presentes, a menos que se indique lo contrario:</span><span class="sxs-lookup"><span data-stu-id="f50d6-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="f50d6-145">GPMC</span><span class="sxs-lookup"><span data-stu-id="f50d6-145">GPMC</span></span>

    -   <span data-ttu-id="f50d6-146">Windows Server 2008: AGPM instala automáticamente la consola GPMC si no está presente.</span><span class="sxs-lookup"><span data-stu-id="f50d6-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="f50d6-147">Windows Vista: debe instalar la consola GPMC desde RSAT antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="f50d6-148">Para obtener más información, consulte <https://go.microsoft.com/fwlink/?LinkID=116179> .</span><span class="sxs-lookup"><span data-stu-id="f50d6-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="f50d6-149">3,0 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f50d6-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="f50d6-150">Requisitos del escenario</span><span class="sxs-lookup"><span data-stu-id="f50d6-150">Scenario requirements</span></span>

<span data-ttu-id="f50d6-151">Antes de empezar este escenario, cree cuatro cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="f50d6-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="f50d6-152">Durante el escenario, asignará uno de los siguientes roles de AGPM a cada una de estas cuentas: administrador de AGPM (control total), aprobador, editor y revisor.</span><span class="sxs-lookup"><span data-stu-id="f50d6-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="f50d6-153">Estas cuentas deben poder enviar y recibir mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f50d6-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="f50d6-154">Asigne el permiso **vincular GPO** a las cuentas con los roles de editor administrador de AGPM, aprobador y (opcionalmente).</span><span class="sxs-lookup"><span data-stu-id="f50d6-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="f50d6-155">**Nota:** 
 El permiso **vincular GPO** está asignado a miembros de administradores de dominio y administradores de empresa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f50d6-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="f50d6-156">Para asignar el permiso **vincular GPO** a usuarios o grupos adicionales (como cuentas con los roles de administrador o aprobador de AGPM), haga clic en el nodo del dominio y, a continuación, haga clic en la pestaña **delegación** , seleccione **vincular GPO**, haga clic en **Agregar**y seleccione los usuarios o grupos a los que desea asignar el permiso.</span><span class="sxs-lookup"><span data-stu-id="f50d6-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="f50d6-157">Pasos para instalar y configurar AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="f50d6-158">Debe completar los pasos siguientes para instalar y configurar AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="f50d6-159">Paso 1: instalar el servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="f50d6-160">Paso 2: instalar el cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="f50d6-161">Paso 3: configurar una conexión de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="f50d6-162">Paso 4: configurar la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="f50d6-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="f50d6-163">Paso 5: delegar el acceso</span><span class="sxs-lookup"><span data-stu-id="f50d6-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="f50d6-164">Paso 1: instalar el servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="f50d6-165">En este paso, instalará el servidor AGPM en el servidor miembro o el controlador de dominio que ejecutará el servicio AGPM y configurará el archivo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="f50d6-166">Todas las operaciones de AGPM se administran a través de este servicio de Windows y se ejecutan con las credenciales del servicio.</span><span class="sxs-lookup"><span data-stu-id="f50d6-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="f50d6-167">El archivo administrado por un servidor de AGPM puede alojarse en ese servidor o en otro servidor del mismo bosque.</span><span class="sxs-lookup"><span data-stu-id="f50d6-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="f50d6-168">Para instalar el servidor AGPM en el equipo que hospedará el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="f50d6-169">Inicie sesión con una cuenta que sea miembro del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="f50d6-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="f50d6-170">Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones en pantalla para seleccionar **Administración avanzada de directivas de grupo-servidor**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="f50d6-171">En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="f50d6-172">En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="f50d6-173">En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="f50d6-174">El equipo en el que está instalado el servidor de AGPM hospedará el servicio AGPM y administrará el archivo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="f50d6-175">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-175">Click **Next**.</span></span>

6.  <span data-ttu-id="f50d6-176">En el cuadro de diálogo **ruta de acceso del archivo** , seleccione una ubicación para el archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="f50d6-177">La ruta de acceso al archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero debe seleccionar una ubicación con suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="f50d6-178">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-178">Click **Next**.</span></span>

7.  <span data-ttu-id="f50d6-179">En el cuadro de diálogo **cuenta de servicio AGPM** , seleccione una cuenta de servicio en la que se ejecutará el servicio AGPM y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="f50d6-180">En el cuadro de diálogo **propietario del archivo** , seleccione una cuenta o un grupo al que inicialmente desee asignar el rol de administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="f50d6-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="f50d6-181">Este administrador de AGPM puede asignar roles y permisos de AGPM a otros administradores de directivas de grupo (incluido el rol de administrador de AGPM).</span><span class="sxs-lookup"><span data-stu-id="f50d6-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="f50d6-182">Para este escenario, seleccione la cuenta que se va a usar en el rol de administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="f50d6-183">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-183">Click **Next**.</span></span>

9.  <span data-ttu-id="f50d6-184">En el cuadro de diálogo **configuración del puerto** , escriba un puerto en el que deba escuchar el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="f50d6-185">No desactive la casilla **Agregar excepción de puerto al firewall** , a menos que configure manualmente las excepciones de puerto o use reglas para configurar las excepciones de puerto.</span><span class="sxs-lookup"><span data-stu-id="f50d6-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="f50d6-186">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-186">Click **Next**.</span></span>

10. <span data-ttu-id="f50d6-187">En el cuadro de diálogo **idiomas** , seleccione uno o más idiomas para mostrar que se instalarán en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="f50d6-188">Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="f50d6-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="f50d6-189">**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="f50d6-190">Esto puede impedir que el servicio AGPM se inicie.</span><span class="sxs-lookup"><span data-stu-id="f50d6-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="f50d6-191">Para obtener información sobre cómo modificar la configuración del servicio, consulte la ayuda para la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="f50d6-192">Paso 2: instalar el cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="f50d6-193">Cada administrador de directivas de grupo (cualquier persona que cree, edite, implemente, revise o elimine GPO) debe tener instalado un cliente AGPM en los equipos que usen para administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="f50d6-194">Para este escenario, debe instalar el cliente de AGPM en un equipo como mínimo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="f50d6-195">No es necesario instalar el cliente de AGPM en los equipos de los usuarios finales que no realizan la administración de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="f50d6-196">Para instalar el cliente de AGPM en el equipo de un administrador de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="f50d6-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="f50d6-197">Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones de la pantalla para seleccionar **Advanced Group Policy Management-Client**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="f50d6-198">En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="f50d6-199">En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="f50d6-200">En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el cliente AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="f50d6-201">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-201">Click **Next**.</span></span>

5.  <span data-ttu-id="f50d6-202">En el cuadro de diálogo **servidor de AGPM** , escriba el nombre de equipo completo para el servidor de AGPM y el puerto al que se conectará.</span><span class="sxs-lookup"><span data-stu-id="f50d6-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="f50d6-203">El puerto predeterminado para el servicio AGPM es 4600.</span><span class="sxs-lookup"><span data-stu-id="f50d6-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="f50d6-204">No desactive la casilla **permitir la consola de administración de Microsoft a través del firewall** , a menos que configure manualmente las excepciones de puerto o use reglas para configurar las excepciones de puerto.</span><span class="sxs-lookup"><span data-stu-id="f50d6-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="f50d6-205">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-205">Click **Next**.</span></span>

6.  <span data-ttu-id="f50d6-206">En el cuadro de diálogo **idiomas** , seleccione uno o más idiomas para mostrar para instalar para el cliente de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="f50d6-207">Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="f50d6-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="f50d6-208">Paso 3: configurar una conexión de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="f50d6-209">AGPM almacena todas las versiones de cada objeto de directiva de grupo (GPO) controlado (un GPO para el cual AGPM proporciona control de cambios) en un archivo central, de modo que los administradores de directivas de grupo puedan ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="f50d6-210">En este paso, puede configurar una conexión de servidor de AGPM y asegurarse de que todos los administradores de directivas de grupo se conecten al mismo servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="f50d6-211">(Para obtener información acerca de la configuración de varios servidores de AGPM, consulte ayuda para la administración avanzada de directivas de grupo).</span><span class="sxs-lookup"><span data-stu-id="f50d6-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="f50d6-212">Para configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="f50d6-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="f50d6-213">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con la cuenta de usuario que seleccionó como propietario del archivo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="f50d6-214">Este usuario tiene el rol de administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="f50d6-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="f50d6-215">Haga clic en **Inicio**, seleccione **herramientas administrativas**y haga clic en **Administración de directivas de grupo** para abrir la GPMC.</span><span class="sxs-lookup"><span data-stu-id="f50d6-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="f50d6-216">Editar un GPO que se aplica a todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="f50d6-217">En la **ventana Editor de administración de directivas de grupo** , haga doble clic en configuración de **usuario**, **directivas**, **plantillas administrativas**, **componentes de Windows**y **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="f50d6-218">En el panel de detalles, haga doble clic en **AGPM: especificar el servidor de AGPM predeterminado (todos los dominios)**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="f50d6-219">En la ventana **propiedades** , seleccione **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, **Server.contoso.com:4600**) para el servidor que hospeda el archivo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="f50d6-220">De forma predeterminada, el servicio AGPM usa el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="f50d6-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="f50d6-221">Haga clic en **Aceptar**y, a continuación, cierre la ventana **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="f50d6-222">Cuando se actualiza la Directiva de grupo, se configura la conexión del servidor de AGPM para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="f50d6-223">Paso 4: configurar la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="f50d6-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="f50d6-224">Como administrador de AGPM (control total), usted designa las direcciones de correo electrónico de los aprobadores y administradores de AGPM a los que se envía un mensaje de correo electrónico que contiene una solicitud cuando un editor intenta crear, implementar o eliminar un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="f50d6-225">También puede determinar el alias desde el que se envían estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="f50d6-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="f50d6-226">Para configurar la notificación de correo electrónico para AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="f50d6-227">En el panel de detalles, haga clic en la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="f50d6-228">En el campo **desde dirección de correo electrónico** , escriba el alias de correo electrónico de AGPM desde el que se deben enviar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="f50d6-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="f50d6-229">En el campo **dirección de correo electrónico** , escriba la dirección de correo electrónico de la cuenta de usuario a la que desea asignar el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="f50d6-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="f50d6-230">En el campo **servidor SMTP** , escriba un servidor de correo SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="f50d6-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="f50d6-231">En los campos **nombre de usuario** y **contraseña** , escriba las credenciales de un usuario con acceso al servicio SMTP.</span><span class="sxs-lookup"><span data-stu-id="f50d6-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="f50d6-232">Haz clic en **Apply**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="f50d6-233">Paso 5: delegar el acceso</span><span class="sxs-lookup"><span data-stu-id="f50d6-233">Step 5: Delegate access</span></span>

<span data-ttu-id="f50d6-234">Como administrador de AGPM (control total), puede delegar el acceso de nivel de dominio a los GPO, asignando roles a la cuenta de cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="f50d6-235">**Nota:**  También puede delegar el acceso en el nivel de GPO en lugar del nivel de dominio.</span><span class="sxs-lookup"><span data-stu-id="f50d6-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="f50d6-236">Para obtener más información, consulte ayuda para la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="f50d6-237">**Importante**  Debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, de modo que no pueda usarse para eludir la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="f50d6-238">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="f50d6-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="f50d6-239">Para delegar el acceso a todos los GPO en un dominio</span><span class="sxs-lookup"><span data-stu-id="f50d6-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="f50d6-240">En la pestaña **delegación de dominios** , haga clic en el botón **Agregar** , seleccione la cuenta de usuario del administrador de directivas de grupo para que sirva como aprobador y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="f50d6-241">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione el rol **aprobador** para asignar ese rol a la cuenta y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="f50d6-242">(Este rol incluye el rol de revisor).</span><span class="sxs-lookup"><span data-stu-id="f50d6-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="f50d6-243">Haga clic en el botón **Agregar** , seleccione la cuenta de usuario del administrador de directivas de grupo para que sirva como editor y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="f50d6-244">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione la función **Editor** para asignar ese rol a la cuenta y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="f50d6-245">(Este rol incluye el rol de revisor).</span><span class="sxs-lookup"><span data-stu-id="f50d6-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="f50d6-246">Haga clic en el botón **Agregar** , seleccione la cuenta de usuario del administrador de directivas de grupo para que actúe como revisor y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="f50d6-247">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione el rol de **Revisor** para asignar solo ese rol a la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f50d6-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="f50d6-248">Pasos para administrar GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-248">Steps for managing GPOs</span></span>


<span data-ttu-id="f50d6-249">Debe completar los pasos siguientes para crear, editar, revisar e implementar GPO con AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="f50d6-250">Además, creará una plantilla, eliminará un objeto de directiva de grupo y restaurará un objeto de directiva de grupo eliminado.</span><span class="sxs-lookup"><span data-stu-id="f50d6-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="f50d6-251">Paso 1: crear un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="f50d6-252">Paso 2: editar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="f50d6-253">Paso 3: revisar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="f50d6-254">Paso 4: usar una plantilla para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="f50d6-255">Paso 5: eliminar y restaurar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="f50d6-256">Paso 1: crear un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="f50d6-257">En un entorno con varios administradores de directivas de grupo, los usuarios con el rol Editor tienen la capacidad de solicitar la creación de nuevos GPO, pero dicha solicitud debe ser aprobada por alguien con el rol de aprobador, ya que la creación de un nuevo objeto de directiva de grupo afecta al entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="f50d6-258">En este paso, usará una cuenta con la función editor para solicitar la creación de un nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="f50d6-259">Con una cuenta que tenga el rol de aprobador, apruebe esta solicitud y complete la creación de un GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="f50d6-260">Para solicitar la creación de un GPO nuevo administrado a través de AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="f50d6-261">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado la función editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="f50d6-262">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="f50d6-263">Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="f50d6-264">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="f50d6-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="f50d6-265">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="f50d6-266">Escriba **MyGPO** como nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="f50d6-267">Escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="f50d6-268">Haga clic en **crear en vivo** para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="f50d6-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="f50d6-269">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="f50d6-270">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-271">El nuevo GPO se muestra en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="f50d6-272">Para aprobar la solicitud pendiente para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="f50d6-273">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador en AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="f50d6-274">Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud del editor para crear un GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="f50d6-275">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="f50d6-276">En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.</span><span class="sxs-lookup"><span data-stu-id="f50d6-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="f50d6-277">Haga clic con el botón derecho en **MyGPO**y luego en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="f50d6-278">Haga clic en **sí** para confirmar la aprobación de la creación del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="f50d6-279">El objeto de directiva de grupo se mueve a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="f50d6-280">Paso 2: editar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="f50d6-281">Puede usar los GPO para configurar las opciones de usuario o de equipo e implementarlas en muchos equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="f50d6-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="f50d6-282">En este paso, se usa una cuenta con el rol Editor para desproteger un GPO desde el archivo, editar el GPO sin conexión, comprobar el GPO editado en el archivo y solicitar la implementación del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="f50d6-283">Para este escenario, debe configurar una opción de configuración en el GPO para requerir que la contraseña tenga al menos ocho caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="f50d6-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="f50d6-284">Para comprobar el GPO fuera del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="f50d6-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="f50d6-285">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="f50d6-286">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="f50d6-287">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="f50d6-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="f50d6-288">Haga clic con el botón derecho en **MyGPO**y, después, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="f50d6-289">Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="f50d6-290">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-291">En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="f50d6-292">Para modificar el GPO sin conexión y configurar la longitud mínima de la contraseña</span><span class="sxs-lookup"><span data-stu-id="f50d6-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="f50d6-293">En la pestaña **controlado** , haga clic con el botón secundario en **MyGPO**y, a continuación, haga clic en **Editar** para abrir la ventana del editor de administración de **directivas de grupo** y realizar cambios en una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="f50d6-294">Para este escenario, configure la longitud mínima de la contraseña:</span><span class="sxs-lookup"><span data-stu-id="f50d6-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="f50d6-295">En **configuración del equipo**, haga doble clic en **directivas**, **configuración de Windows**, **configuración de seguridad**, directivas de **cuenta**y **Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="f50d6-296">En el panel de detalles, haga doble clic en **longitud mínima**de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f50d6-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="f50d6-297">En la ventana Propiedades, active la casilla **definir esta configuración de directiva** , establezca el número de caracteres en **8**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="f50d6-298">Cierre la ventana del **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="f50d6-299">Para comprobar el objeto de directiva de grupo en el archivo</span><span class="sxs-lookup"><span data-stu-id="f50d6-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="f50d6-300">En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **proteger**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="f50d6-301">Escriba un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="f50d6-302">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-303">En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="f50d6-304">Para solicitar la implementación del GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="f50d6-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="f50d6-305">En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **implementar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="f50d6-306">Como esta cuenta no es aprobador o administrador AGPM, debe enviar una solicitud de implementación.</span><span class="sxs-lookup"><span data-stu-id="f50d6-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="f50d6-307">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="f50d6-308">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="f50d6-309">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-310">**MyGPO** se muestra en la lista de GPO en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="f50d6-311">Paso 3: revisar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="f50d6-312">En este paso, usted actúa como aprobador, creando informes y analizando la configuración y los cambios en la configuración del GPO para determinar si debe aprobarlos.</span><span class="sxs-lookup"><span data-stu-id="f50d6-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="f50d6-313">Después de evaluar el GPO, impleméntelo en el entorno de producción y vincúlelo a un dominio o una unidad organizativa (OU) para que tenga efecto cuando se actualice la Directiva de grupo de los equipos de ese dominio o unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="f50d6-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="f50d6-314">Para revisar la configuración en el GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="f50d6-315">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador en AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="f50d6-316">(Cualquier administrador de directiva de grupo con el rol de revisor, que se incluye en todos los demás roles, puede revisar la configuración de un GPO).</span><span class="sxs-lookup"><span data-stu-id="f50d6-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="f50d6-317">Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud de un editor para implementar un GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="f50d6-318">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="f50d6-319">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="f50d6-320">Haga doble clic en **MyGPO** para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="f50d6-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="f50d6-321">Revise la configuración de la versión más reciente de MyGPO:</span><span class="sxs-lookup"><span data-stu-id="f50d6-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="f50d6-322">En la ventana **historial** , haga clic con el botón secundario en la versión de GPO con la marca de tiempo más reciente, haga clic en **configuración**y, después, haga clic en **Informe HTML** para mostrar un resumen de la configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="f50d6-323">En el explorador Web, haga clic en **Mostrar todo** para ver todas las opciones de configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="f50d6-324">Cierra el explorador.</span><span class="sxs-lookup"><span data-stu-id="f50d6-324">Close the browser.</span></span>

7. <span data-ttu-id="f50d6-325">Compare la versión más reciente de MyGPO con la primera versión protegida en el archivo:</span><span class="sxs-lookup"><span data-stu-id="f50d6-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="f50d6-326">En la ventana **historial** , haga clic en la versión de GPO con la más reciente.</span><span class="sxs-lookup"><span data-stu-id="f50d6-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="f50d6-327">Presione CTRL y haga clic en la versión de GPO más antigua cuya **versión del equipo** no sea \* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="f50d6-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="f50d6-328">Haga clic en el botón **diferencias** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-328">Click the **Differences** button.</span></span> <span data-ttu-id="f50d6-329">La sección **directivas de cuenta/Directiva de contraseña** está resaltada en verde y precedida de **\ [+ \]**, lo que indica que esta configuración está configurada únicamente en la última versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="f50d6-330">Haga clic en **directivas de cuenta/Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="f50d6-331">La configuración de **longitud mínima** de la contraseña también está resaltada en verde y precedida de **\ [+ \]**, lo que indica que está configurada solo en la última versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="f50d6-332">Cierre el explorador Web.</span><span class="sxs-lookup"><span data-stu-id="f50d6-332">Close the Web browser.</span></span>

**<span data-ttu-id="f50d6-333">Para implementar el GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="f50d6-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="f50d6-334">En la pestaña **pendiente** , haga clic con el botón derecho en **MyGPO** y, a continuación, haga clic en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="f50d6-335">Escriba un comentario para incluirlo en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="f50d6-336">Haz clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-336">Click **Yes**.</span></span> <span data-ttu-id="f50d6-337">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-338">El objeto de directiva de grupo se implementa en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="f50d6-339">Para vincular el GPO a un dominio o unidad de organización</span><span class="sxs-lookup"><span data-stu-id="f50d6-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="f50d6-340">En la GPMC, haga clic con el botón secundario en el dominio o en una unidad organizativa a la que desee aplicar el GPO que ha configurado y, a continuación, haga clic en **vincular un GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="f50d6-341">En el cuadro de diálogo **seleccionar GPO** , haga clic en **MyGPO**y, después, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="f50d6-342">Paso 4: usar una plantilla para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="f50d6-343">En este paso, se usa una cuenta con la función editor para crear una plantilla (una versión no modificable y estática de un GPO para usarla como punto de partida para crear nuevos GPO) y, a continuación, crear un GPO nuevo basado en esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="f50d6-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="f50d6-344">Las plantillas son útiles para crear rápidamente varios GPO que incluyan muchos de los ajustes de configuración.</span><span class="sxs-lookup"><span data-stu-id="f50d6-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="f50d6-345">Para crear una plantilla basada en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="f50d6-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="f50d6-346">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="f50d6-347">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="f50d6-348">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="f50d6-349">Haga clic con el botón derecho en **MyGPO**y, a continuación, haga clic en **Guardar como plantilla** para crear una plantilla que incorpore toda la configuración que se encuentra en MyGPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="f50d6-350">Escriba **MyTemplate** como el nombre de la plantilla y un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="f50d6-351">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-352">La nueva plantilla aparecerá en la ficha **plantillas** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="f50d6-353">Para solicitar la creación de un GPO nuevo administrado a través de AGPM</span><span class="sxs-lookup"><span data-stu-id="f50d6-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="f50d6-354">Haga clic en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="f50d6-355">Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="f50d6-356">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="f50d6-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="f50d6-357">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="f50d6-358">Escriba **MyOtherGPO** como nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="f50d6-359">Escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="f50d6-360">Haga clic en **crear en vivo**para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="f50d6-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="f50d6-361">En **plantilla de GPO de**para **, seleccione MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="f50d6-362">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="f50d6-363">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-364">El nuevo GPO se muestra en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="f50d6-365">Use una cuenta a la que se le haya asignado el rol de aprobador para aprobar la solicitud pendiente para crear el GPO como hizo en el [paso 1: crear un GPO](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="f50d6-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="f50d6-366">MyTemplate incorpora toda la configuración que ha configurado en MyGPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="f50d6-367">Como MyOtherGPO se creó con MyTemplate, inicialmente contiene toda la configuración que MyGPO en el momento en que se creó MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="f50d6-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="f50d6-368">Puede confirmarlo generando un informe de diferencias para comparar MyOtherGPO con MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="f50d6-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="f50d6-369">Para comprobar el GPO fuera del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="f50d6-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="f50d6-370">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="f50d6-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="f50d6-371">Haga clic con el botón derecho en **MyOtherGPO**y, después, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="f50d6-372">Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="f50d6-373">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-374">En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="f50d6-375">Para editar el GPO sin conexión y configurar la duración del bloqueo de cuenta</span><span class="sxs-lookup"><span data-stu-id="f50d6-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="f50d6-376">En la pestaña **controlado** , haga clic con el botón secundario en **MyOtherGPO**y, a continuación, haga clic en **Editar** para abrir la ventana del editor de administración de **directivas de grupo** y realizar cambios en una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="f50d6-377">Para este escenario, configure la longitud mínima de la contraseña:</span><span class="sxs-lookup"><span data-stu-id="f50d6-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="f50d6-378">En **configuración del equipo**, haga doble clic en **directivas**, **configuración de Windows**, **configuración de seguridad**, directivas de **cuenta**y Directiva de **bloqueo de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="f50d6-379">En el panel de detalles, haga doble clic en **duración del bloqueo de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="f50d6-380">En la ventana Propiedades, seleccione **definir esta configuración de directiva**, establezca la duración en **30** minutos y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="f50d6-381">Cierre la ventana del **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="f50d6-382">Visite MyOtherGPO en el archivo y solicite la implementación como hizo para MyGPO en el [paso 2: editar un GPO](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="f50d6-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="f50d6-383">Puede comparar MyOtherGPO con MyGPO o con MyTemplate mediante informes de diferencias.</span><span class="sxs-lookup"><span data-stu-id="f50d6-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="f50d6-384">Cualquier cuenta que incluya el rol de revisor (Administrador AGPM \ [control total \], aprobador, editor o revisor) puede generar informes.</span><span class="sxs-lookup"><span data-stu-id="f50d6-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="f50d6-385">Para comparar un GPO con otro GPO y con una plantilla</span><span class="sxs-lookup"><span data-stu-id="f50d6-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="f50d6-386">Para comparar MyGPO y MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="f50d6-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="f50d6-387">En la pestaña **controlado** , haga clic en **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="f50d6-388">Presione CTRL y, a continuación, haga clic en **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="f50d6-389">Haga clic con el botón derecho en **MyOtherGPO**, apunte a **diferencias**y haga clic en **Informe HTML**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="f50d6-390">Para comparar MyOtherGPO y MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="f50d6-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="f50d6-391">En la pestaña **controlado** , haga clic en **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="f50d6-392">Haga clic con el botón derecho en **MyOtherGPO**, apunte a **diferencias**y haga clic en **plantilla**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="f50d6-393">Seleccione **MyTemplate** y **Informe html**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="f50d6-394">Paso 5: eliminar y restaurar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="f50d6-395">En este paso, actuará como aprobador para eliminar un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f50d6-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="f50d6-396">Para eliminar un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="f50d6-397">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="f50d6-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="f50d6-398">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="f50d6-399">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="f50d6-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="f50d6-400">Haga clic con el botón derecho en **MyGPO**y luego haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="f50d6-401">Haga clic en **eliminar GPO de archivo y producción** para eliminar la versión del archivo, así como la versión implementada del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="f50d6-402">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="f50d6-403">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-404">El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.</span><span class="sxs-lookup"><span data-stu-id="f50d6-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="f50d6-405">En ocasiones, es posible que desconozcas después de eliminar un objeto de directiva de grupo que aún es necesario.</span><span class="sxs-lookup"><span data-stu-id="f50d6-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="f50d6-406">En este paso, usted actúa como aprobador para restaurar un GPO que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="f50d6-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="f50d6-407">Para restaurar un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="f50d6-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="f50d6-408">En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.</span><span class="sxs-lookup"><span data-stu-id="f50d6-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="f50d6-409">Haga clic con el botón derecho en **MyGPO**y luego haga clic en **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="f50d6-410">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="f50d6-411">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-412">El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="f50d6-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="f50d6-413">**Nota:**  Al restaurar un GPO en el archivo, no se vuelve a implementar automáticamente en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="f50d6-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="f50d6-414">Para devolver el GPO al entorno de producción, implemente el GPO como en el [paso 3: revisar e implementar un GPO](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="f50d6-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="f50d6-415">Después de editar e implementar un GPO, es posible que descubra que los cambios recientes en el GPO están causando el problema.</span><span class="sxs-lookup"><span data-stu-id="f50d6-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="f50d6-416">En este paso, actuará como aprobador para volver a una versión anterior del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="f50d6-417">Puede revertir a cualquier versión en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="f50d6-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="f50d6-418">Puede usar los comentarios y las etiquetas para identificar las versiones correctas y cuando se han realizado cambios específicos.</span><span class="sxs-lookup"><span data-stu-id="f50d6-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="f50d6-419">Para volver a una versión anterior de un GPO</span><span class="sxs-lookup"><span data-stu-id="f50d6-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="f50d6-420">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="f50d6-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="f50d6-421">Haga doble clic en **MyGPO** para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="f50d6-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="f50d6-422">Haga clic con el botón secundario en la versión que se va a implementar, haga clic en **implementar**y luego haga clic en **sí**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="f50d6-423">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f50d6-424">En la ventana **historial** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="f50d6-425">**Nota:**  Para comprobar que la versión reimplementada es la versión prevista, examine un informe de diferencias para las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="f50d6-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="f50d6-426">En la ventana **historial** del GPO, seleccione las dos versiones, haga clic con el botón secundario, seleccione **diferencia**y, a continuación, haga clic en **Informe HTML** o **Informe XML**.</span><span class="sxs-lookup"><span data-stu-id="f50d6-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





