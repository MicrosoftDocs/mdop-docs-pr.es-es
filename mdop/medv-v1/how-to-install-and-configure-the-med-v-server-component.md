---
title: Cómo instalar y configurar el componente de servidor MED-V
description: Cómo instalar y configurar el componente de servidor MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826980"
---
# <span data-ttu-id="b7f9a-103">Cómo instalar y configurar el componente de servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="b7f9a-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="b7f9a-104">En esta sección se explica cómo [instalar](#bkmk-howtoinstallthemedvserver) y [configurar](#bkmk-howtoconfigurethemedvserver) el servidor de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="b7f9a-105">Cómo instalar el servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="b7f9a-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="b7f9a-106">Para instalar el servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="b7f9a-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="b7f9a-107">Instale el paquete MED-V Server. msi.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="b7f9a-108">El paquete MED-V Server. msi se llama *MED-V\_Server\_x.msi*, donde x es el número de versión.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="b7f9a-109">Por ejemplo, *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="b7f9a-110">Cuando aparezca la pantalla de **bienvenida del asistente de InstallShield** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="b7f9a-111">En la pantalla **contrato de licencia** , lea el contrato de licencia, haga clic en Acepto **las condiciones del contrato de licencia**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="b7f9a-112">Aparece la pantalla **carpeta de destino** , donde se muestra la carpeta de instalación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="b7f9a-113">La carpeta de instalación predeterminada es *%SystemDrive%\\Program de escritorio de Programa\\microsoft Enterprise Virtualization\\*.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="b7f9a-114">Para cambiar la carpeta donde se debe instalar MED-V, haga clic en **cambiar** y vaya a una carpeta existente.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="b7f9a-115">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-115">Click **Next**.</span></span>

5.  <span data-ttu-id="b7f9a-116">En la pantalla **preparado para instalar el programa** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="b7f9a-117">Se iniciará la instalación del servidor de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-117">The MED-V server installation starts.</span></span> <span data-ttu-id="b7f9a-118">Esto puede demorar varios minutos y es posible que no se muestre el texto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="b7f9a-119">Durante la instalación, aparecen varias pantallas de progreso.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="b7f9a-120">Si aparece un mensaje, siga las instrucciones proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="b7f9a-121">Cuando aparezca la pantalla **Asistente InstallShield completado** , haga clic en **Finalizar** para completar el asistente.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="b7f9a-122">Nota</span><span class="sxs-lookup"><span data-stu-id="b7f9a-122">Note</span></span>**  
<span data-ttu-id="b7f9a-123">Si va a instalar el servidor MED-V a través de Microsoft Remote Desktop, use la siguiente sintaxis: **mstsc/admin**. Asegúrese de que la sesión RDP se dirija a la consola.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="b7f9a-124">Cómo configurar el servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="b7f9a-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="b7f9a-125">Puede configurar las siguientes opciones del servidor:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="b7f9a-126">Conexiones</span><span class="sxs-lookup"><span data-stu-id="b7f9a-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="b7f9a-127">Imágenes</span><span class="sxs-lookup"><span data-stu-id="b7f9a-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="b7f9a-128">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7f9a-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="b7f9a-129">Informes</span><span class="sxs-lookup"><span data-stu-id="b7f9a-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="b7f9a-130">Configurar conexiones</span><span class="sxs-lookup"><span data-stu-id="b7f9a-130">Configuring Connections</span></span>

**<span data-ttu-id="b7f9a-131">Para configurar conexiones</span><span class="sxs-lookup"><span data-stu-id="b7f9a-131">To configure connections</span></span>**

1.  <span data-ttu-id="b7f9a-132">En el menú Inicio de Windows, seleccione **todos los programas &gt; Med-v &gt; Med-v Server Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="b7f9a-133">Nota</span><span class="sxs-lookup"><span data-stu-id="b7f9a-133">Note</span></span>**  
    <span data-ttu-id="b7f9a-134">Nota: Si ha activado la casilla de verificación **iniciar administrador de configuración del servidor Med-v** durante la instalación del servidor, el administrador de configuración del servidor Med-v se inicia automáticamente después de que se complete la instalación del servidor.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="b7f9a-135">En la pestaña **conexiones** , configure las siguientes opciones de conexión de cliente:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="b7f9a-136">**Habilitar conexiones no cifradas (http), mediante puerto**: Seleccione esta casilla para habilitar las conexiones sin cifrar con un puerto específico.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="b7f9a-137">En el cuadro puerto, escriba el puerto de servidor en el que se aceptarán las conexiones no cifradas (http).</span><span class="sxs-lookup"><span data-stu-id="b7f9a-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="b7f9a-138">**Habilitar conexiones cifradas (https), usando puerto**: Seleccione esta casilla para habilitar conexiones cifradas que usen un puerto específico.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="b7f9a-139">En el cuadro puerto, escriba el puerto de servidor en el que desea aceptar las conexiones cifradas (https).</span><span class="sxs-lookup"><span data-stu-id="b7f9a-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="b7f9a-140">Https es una configuración opcional que se puede establecer para garantizar transacciones seguras entre los clientes de MED-V Server y MED-V.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="b7f9a-141">Para configurar https, debe realizar los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="b7f9a-142">Configurar un certificado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="b7f9a-143">Asociar el certificado de servidor con el puerto especificado mediante netsh.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="b7f9a-144">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="b7f9a-145">Comandos Netsh para el protocolo de transferencia de hipertexto (HTTP)</span><span class="sxs-lookup"><span data-stu-id="b7f9a-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="b7f9a-146">Cómo configurar un puerto con un certificado SSL</span><span class="sxs-lookup"><span data-stu-id="b7f9a-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="b7f9a-147">Cómo configurar un puerto con un certificado SSL</span><span class="sxs-lookup"><span data-stu-id="b7f9a-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="b7f9a-148">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="b7f9a-149">Configurar imágenes</span><span class="sxs-lookup"><span data-stu-id="b7f9a-149">Configuring Images</span></span>

**<span data-ttu-id="b7f9a-150">Para configurar imágenes</span><span class="sxs-lookup"><span data-stu-id="b7f9a-150">To configure images</span></span>**

1.  <span data-ttu-id="b7f9a-151">Haga clic en la pestaña **imágenes** .</span><span class="sxs-lookup"><span data-stu-id="b7f9a-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="b7f9a-152">Configure las siguientes opciones de administración de imágenes:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="b7f9a-153">**Directorio VMS**: el directorio de la máquina virtual (el directorio donde se almacenan las imágenes).</span><span class="sxs-lookup"><span data-stu-id="b7f9a-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="b7f9a-154">Este campo contiene una ruta de acceso UNC al directorio de la imagen en el servidor de distribución de imágenes al que se debería obtener acceso desde el servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="b7f9a-155">**Dirección URL de MV**: la ubicación del servidor donde se almacenan las imágenes.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="b7f9a-156">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="b7f9a-157">Configurar permisos</span><span class="sxs-lookup"><span data-stu-id="b7f9a-157">Configuring Permissions</span></span>

**<span data-ttu-id="b7f9a-158">Para configurar permisos</span><span class="sxs-lookup"><span data-stu-id="b7f9a-158">To configure permissions</span></span>**

1.  <span data-ttu-id="b7f9a-159">Haga clic en la pestaña **permisos** .</span><span class="sxs-lookup"><span data-stu-id="b7f9a-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="b7f9a-160">Se proporciona una lista de todos los usuarios que pueden iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="b7f9a-161">Para aplicar permisos de lectura y escritura a un usuario, active la casilla situada junto al usuario.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="b7f9a-162">Para aplicar permisos de solo lectura a un usuario, desactive la casilla.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="b7f9a-163">Para agregar usuarios o grupos del dominio, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="b7f9a-164">Aparece el cuadro de diálogo **Escriba los nombres de los usuarios o grupos** .</span><span class="sxs-lookup"><span data-stu-id="b7f9a-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="b7f9a-165">Seleccione usuarios del dominio o grupos mediante una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="b7f9a-166">En el campo **introducir nombre de usuario o grupo** , escriba un usuario o grupo que exista en el dominio o exista como usuario o grupo local en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="b7f9a-167">A continuación, haga clic en **Comprobar nombres** para resolver el nombre completo.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="b7f9a-168">Haga clic en **Buscar** para abrir el cuadro de diálogo **Seleccionar usuarios o grupos** estándar.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="b7f9a-169">Después, seleccione usuarios o grupos del dominio.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="b7f9a-170">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-170">Click **OK**.</span></span>

4.  <span data-ttu-id="b7f9a-171">Para quitar usuarios o grupos del dominio, seleccione un usuario o grupo y haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="b7f9a-172">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="b7f9a-173">Configuración de informes</span><span class="sxs-lookup"><span data-stu-id="b7f9a-173">Configuring Reports</span></span>

**<span data-ttu-id="b7f9a-174">Para configurar informes</span><span class="sxs-lookup"><span data-stu-id="b7f9a-174">To configure reports</span></span>**

1.  <span data-ttu-id="b7f9a-175">Haga clic en la pestaña **informes** .</span><span class="sxs-lookup"><span data-stu-id="b7f9a-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="b7f9a-176">Para admitir los informes, seleccione **Habilitar informes**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="b7f9a-177">En el cuadro **cadena de conexión** , escriba una cadena de conexión para la base de datos MSSQL.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="b7f9a-178">Cuando SQL Server está instalado en un servidor remoto, use la siguiente cadena de conexión:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="b7f9a-179">Nota</span><span class="sxs-lookup"><span data-stu-id="b7f9a-179">Note</span></span>**  
        <span data-ttu-id="b7f9a-180">Nota: para conectarse a SQL Express, use:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="b7f9a-181">Para crear la base de datos, haga clic en **crear base de datos**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="b7f9a-182">Para comprobar la conexión, haga clic en **probar conexión**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="b7f9a-183">Para configurar las opciones de borrado de la base de datos, haga clic en **Borrar opciones**.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="b7f9a-184">Aparece el cuadro de diálogo **Borrar opciones de base de datos** .</span><span class="sxs-lookup"><span data-stu-id="b7f9a-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="b7f9a-185">Elija una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="b7f9a-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="b7f9a-186">**Borrar datos anteriores a**: borre todos los datos anteriores al número de días especificado; en el cuadro número, escriba un número de días.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="b7f9a-187">**Borrar todos los datos de la base de**datos: borrar todos los datos existentes en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="b7f9a-188">**Drop Database**: Elimine la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="b7f9a-189">Haga clic en **Aceptar** para aplicar los cambios y cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="b7f9a-190">Haga clic en **Aceptar** para guardar los cambios, o haga clic en **Cancelar** para cerrar el cuadro de diálogo sin guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="b7f9a-191">Si se le solicita, reinicie el servicio de servidor de MED-V para aplicar los cambios en la configuración de red.</span><span class="sxs-lookup"><span data-stu-id="b7f9a-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="b7f9a-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7f9a-192">Related topics</span></span>


[<span data-ttu-id="b7f9a-193">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="b7f9a-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="b7f9a-194">Diseñar la infraestructura de servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="b7f9a-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









