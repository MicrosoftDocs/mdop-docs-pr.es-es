---
title: Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración
description: Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814023"
---
# <span data-ttu-id="27dbc-103">Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración</span><span class="sxs-lookup"><span data-stu-id="27dbc-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="27dbc-104">Use el siguiente procedimiento para instalar el servidor de base de datos y el servidor de administración en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="27dbc-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="27dbc-105">El equipo en el que va a instalar el servidor de base de datos debe estar ejecutando una versión compatible de Microsoft SQL o se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="27dbc-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="27dbc-106">Nota</span><span class="sxs-lookup"><span data-stu-id="27dbc-106">Note</span></span>**  
<span data-ttu-id="27dbc-107">Una vez completada la implementación, el administrador que instala el servicio necesitará el nombre de **Microsoft SQL Server**, el nombre de la **instancia** y el nombre de la **base de datos** instalando el servicio para poder conectarse a estas bases de datos.</span><span class="sxs-lookup"><span data-stu-id="27dbc-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="27dbc-108">Para instalar la base de datos de administración y el servidor de administración en equipos independientes</span><span class="sxs-lookup"><span data-stu-id="27dbc-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="27dbc-109">Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="27dbc-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="27dbc-110">Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="27dbc-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="27dbc-111">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-111">Click **Install**.</span></span>

2.  <span data-ttu-id="27dbc-112">En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="27dbc-113">En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="27dbc-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="27dbc-114">Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="27dbc-115">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-115">Click **Next**.</span></span>

4.  <span data-ttu-id="27dbc-116">En la página **selección de características** , seleccione los componentes que desea instalar seleccionando la casilla de la base de datos del servidor de **Administración** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="27dbc-117">En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="27dbc-118">En la **Página inicial crear nueva base de datos del servidor de administración**, acepte las selecciones predeterminadas, si corresponde, y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="27dbc-119">Si está usando una instancia de SQL Server personalizada, seleccione **usar una instancia personalizada** y escriba el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="27dbc-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="27dbc-120">Si está usando un nombre de base de datos personalizado, seleccione **Configuración personalizada** y escriba el nombre de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="27dbc-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="27dbc-121">En la siguiente página **crear nueva base de datos del servidor de administración** , seleccione **usar un equipo remoto**y escriba la cuenta de la máquina remota con el siguiente formato: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="27dbc-122">Nota</span><span class="sxs-lookup"><span data-stu-id="27dbc-122">Note</span></span>**  
    <span data-ttu-id="27dbc-123">Si planea implementar el servidor de administración en el mismo equipo, debe seleccionar **usar este equipo local**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="27dbc-124">Para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="27dbc-125">Para instalar la base de datos de informes y el servidor de informes en equipos independientes</span><span class="sxs-lookup"><span data-stu-id="27dbc-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="27dbc-126">Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="27dbc-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="27dbc-127">Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="27dbc-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="27dbc-128">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-128">Click **Install**.</span></span>

2.  <span data-ttu-id="27dbc-129">En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="27dbc-130">En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="27dbc-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="27dbc-131">Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="27dbc-132">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-132">Click **Next**.</span></span>

4.  <span data-ttu-id="27dbc-133">En la página **selección de características** , seleccione los componentes que desea instalar seleccionando la casilla de la base de datos del servidor de **informes** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="27dbc-134">En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="27dbc-135">En la página **crear nueva base de datos del servidor de informes** , acepte las selecciones predeterminadas, si es necesario, y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="27dbc-136">Si está usando una instancia de SQL Server personalizada, seleccione **usar una instancia personalizada** y escriba el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="27dbc-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="27dbc-137">Si está usando un nombre de base de datos personalizado, seleccione **Configuración personalizada** y escriba el nombre de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="27dbc-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="27dbc-138">En la página **crear nueva base de datos del servidor de informes** , seleccione **usar un equipo remoto**y escriba la cuenta de la máquina remota con el siguiente formato: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="27dbc-139">Nota</span><span class="sxs-lookup"><span data-stu-id="27dbc-139">Note</span></span>**  
    <span data-ttu-id="27dbc-140">Si planea implementar el servidor de informes en el mismo equipo, debe seleccionar **usar este equipo local**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="27dbc-141">Para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="27dbc-142">Para instalar las bases de datos de administración y informes con scripts de base de datos de 5,0 de App-V</span><span class="sxs-lookup"><span data-stu-id="27dbc-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="27dbc-143">Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="27dbc-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="27dbc-144">Para extraer las secuencias de comandos de la base de datos de App-V 5,0, abra un símbolo del sistema y especifique la ubicación donde se guardan los archivos de instalación y ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="27dbc-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="27dbc-145">**appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="27dbc-146">Una vez completada la extracción, para acceder a los scripts de base de datos de App-V 5,0 y al archivo Léame:</span><span class="sxs-lookup"><span data-stu-id="27dbc-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="27dbc-147">El Léame de las secuencias de comandos e instrucciones de la base de datos de administración de APP **InstallationExtractionLocation**-V 5,0 se encuentra en la siguiente carpeta: base de datos de administración de  \\  **scripts**de InstallationExtractionLocation  \\  **Management Database**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="27dbc-148">Los scripts e instrucciones README de la base de datos de App-V 5,0 se encuentran en la siguiente carpeta: **InstallationExtractionLocation**base de datos de informes de  \\  **scripts de base de datos**  \\  **Reporting Database**.</span><span class="sxs-lookup"><span data-stu-id="27dbc-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="27dbc-149">Para cada base de datos, copie las secuencias de comandos en un recurso compartido y modifíquelas siguiendo las instrucciones del archivo README (Léame).</span><span class="sxs-lookup"><span data-stu-id="27dbc-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="27dbc-150">Nota</span><span class="sxs-lookup"><span data-stu-id="27dbc-150">Note</span></span>**  
    <span data-ttu-id="27dbc-151">Para obtener más información sobre cómo modificar los SID necesarios que se incluyen en los scripts, vea [Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="27dbc-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="27dbc-152">Ejecute los scripts en el equipo que ejecuta Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="27dbc-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="27dbc-153">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="27dbc-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="27dbc-154">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="27dbc-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="27dbc-155">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="27dbc-155">Got an App-V issue?</span></span>** <span data-ttu-id="27dbc-156">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="27dbc-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="27dbc-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27dbc-157">Related topics</span></span>


[<span data-ttu-id="27dbc-158">Implementación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="27dbc-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









