---
title: Cómo migrar la base de datos SQL de App-V a un servidor SQL Server diferente
description: Cómo migrar la base de datos SQL de App-V a un servidor SQL Server diferente
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817071"
---
# <span data-ttu-id="07040-103">Cómo migrar la base de datos SQL de App-V a un servidor SQL Server diferente</span><span class="sxs-lookup"><span data-stu-id="07040-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="07040-104">En los procedimientos siguientes se describe detalladamente cómo migrar la base de datos de SQL del servidor de administración de Microsoft Application Virtualization (App-V) a otro SQL Server.</span><span class="sxs-lookup"><span data-stu-id="07040-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="07040-105">**Importante**  Este procedimiento requiere que el servicio de servidor de App-V esté detenido y esto evitará que los usuarios finales puedan usar sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="07040-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="07040-106">Para realizar una copia de seguridad de la base de datos de SQL App-V</span><span class="sxs-lookup"><span data-stu-id="07040-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="07040-107">Abra el programa Services. msc y detenga el servicio de App-V Management Server en todos los servidores de administración que usen la base de datos que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="07040-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="07040-108">En el equipo en el que se encuentra la base de datos de App-V, abra SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="07040-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="07040-109">Expanda el nodo **bases** de datos y busque la base de datos de App-V (el nombre predeterminado es APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="07040-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="07040-110">Haga clic con el botón derecho en la base de datos y seleccione **tareas** y seleccione **copia de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="07040-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="07040-111">Compruebe que el **modelo de recuperación** está establecido en **simple** y el tipo de **copia de seguridad** es **completo**.</span><span class="sxs-lookup"><span data-stu-id="07040-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="07040-112">Cambie el **conjunto de copia de seguridad** y la configuración de **destino** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="07040-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="07040-113">Haga clic en **Aceptar** para hacer una copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="07040-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="07040-114">Una vez completada la copia de seguridad correctamente, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07040-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="07040-115">Abra el explorador de Windows y vaya a la carpeta que contiene el archivo de copia de seguridad de la base de datos, por ejemplo APPVIRT. Bak.</span><span class="sxs-lookup"><span data-stu-id="07040-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="07040-116">Copie el archivo de copia de seguridad de la base de datos en el equipo de destino que ejecuta SQL Server.</span><span class="sxs-lookup"><span data-stu-id="07040-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="07040-117">Para restaurar la base de datos de SQL App-V en el equipo de destino</span><span class="sxs-lookup"><span data-stu-id="07040-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="07040-118">En el equipo de destino, abra SQL Server Management Studio, haga clic con el botón derecho en el nodo **bases** de datos y seleccione **restaurar base de datos**.</span><span class="sxs-lookup"><span data-stu-id="07040-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="07040-119">En **origen para restaurar**, elija **desde el dispositivo** y, a continuación, haga clic en el "**...**"</span><span class="sxs-lookup"><span data-stu-id="07040-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="07040-120">de puntos suspensivos (...).</span><span class="sxs-lookup"><span data-stu-id="07040-120">button.</span></span>

3.  <span data-ttu-id="07040-121">En el cuadro de diálogo **especificar copia de seguridad** , asegúrese de que el **medio de copia de seguridad** está establecido en **archivo** y, después, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="07040-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="07040-122">Seleccione el archivo de copia de seguridad que ha copiado del equipo original que está ejecutando SQL Server y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07040-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="07040-123">Haga clic en **Aceptar** y, a continuación, haga clic para seleccionar el conjunto de copia de seguridad que desea restaurar.</span><span class="sxs-lookup"><span data-stu-id="07040-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="07040-124">En **destino de la restauración**, haga clic en el menú desplegable para la **base de datos** y seleccione el nombre de la base de datos de App-V, por ejemplo APPVIRT.</span><span class="sxs-lookup"><span data-stu-id="07040-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="07040-125">Haga clic en **Aceptar** para iniciar la restauración.</span><span class="sxs-lookup"><span data-stu-id="07040-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="07040-126">Después de que la restauración se haya completado correctamente, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07040-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="07040-127">Expanda el nodo **seguridad** , haga clic con el botón derecho en **inicios de sesión** y seleccione **nuevo inicio de sesión**.</span><span class="sxs-lookup"><span data-stu-id="07040-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="07040-128">En el campo **nombre de inicio de sesión** , escriba los detalles de la cuenta servicio de red para el servidor de administración de App-V en el formato DOMAIN\\SERVERNAME $.</span><span class="sxs-lookup"><span data-stu-id="07040-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="07040-129">En la página **General** , en **base de datos predeterminada** , seleccione el nombre de la base de datos de App-V, por ejemplo, APPVIRT, y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07040-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="07040-130">En **seleccionar una página**, haga clic para seleccionar la página **asignación de usuario** .</span><span class="sxs-lookup"><span data-stu-id="07040-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="07040-131">En **usuarios asignados a este inicio de sesión**, haga clic en la casilla de la columna **map** para seleccionar la base de datos de App-V.</span><span class="sxs-lookup"><span data-stu-id="07040-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="07040-132">En **pertenencia de rol de base de datos para: &lt; &gt; appvdatabasename**, haga clic para seleccionar **SFTEveryone** y, después, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07040-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="07040-133">Asegúrese de que el Firewall de Windows en el nuevo equipo que ejecuta SQL Server está configurado para permitir que el servidor de administración de App-V acceda al sistema.</span><span class="sxs-lookup"><span data-stu-id="07040-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="07040-134">En **herramientas administrativas**, use el **firewall de Windows con seguridad avanzada** para crear una **regla de entrada** para el puerto que usa SQL Server (el puerto predeterminado es 1433).</span><span class="sxs-lookup"><span data-stu-id="07040-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="07040-135">Para migrar los trabajos de App-V del Agente SQL Server</span><span class="sxs-lookup"><span data-stu-id="07040-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="07040-136">En el equipo original que ejecuta SQL Server, en SQL Server Management Studio, expanda el nodo **Agente SQL Server** y, a continuación, expanda el nodo **tareas** .</span><span class="sxs-lookup"><span data-stu-id="07040-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="07040-137">Haga clic con el botón derecho en los siguientes cuatro trabajos de App-V y seleccione **trabajo de script como | CREAR en | Archivo**y guarde cada script en una carpeta y asigne un nombre descriptivo a cada secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="07040-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="07040-138">Base de datos de SoftGrid (appvdbname) comprobar historial de uso</span><span class="sxs-lookup"><span data-stu-id="07040-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="07040-139">Base de datos de SoftGrid (appvdbname) cerrar sesiones huérfanas</span><span class="sxs-lookup"><span data-stu-id="07040-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="07040-140">Base de datos de SoftGrid (appvdbname) exigir límite de tamaño</span><span class="sxs-lookup"><span data-stu-id="07040-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="07040-141">Base de datos de SoftGrid (appvdbname) supervisar el estado del trabajo y la alerta</span><span class="sxs-lookup"><span data-stu-id="07040-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="07040-142">Copie los cuatro archivos de script (. SQL) en el equipo de destino que ejecuta SQL Server y abra SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="07040-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="07040-143">En el explorador de Windows, haga clic con el botón secundario en cada archivo. SQL y después haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="07040-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="07040-144">Cada script se abrirá en una ventana de consulta en SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="07040-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="07040-145">Haga clic en **Ejecutar** para cada script y compruebe que cada uno se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="07040-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="07040-146">Actualice el nodo **Jobs** del nodo **Agente SQL Server** y confirme que los cuatro trabajos se han creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="07040-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="07040-147">Para actualizar la configuración del servidor de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="07040-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="07040-148">En el servidor de administración de App-V, modifique las siguientes claves del registro:</span><span class="sxs-lookup"><span data-stu-id="07040-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="07040-149">**SQLServerName**  =  SQLServerName &lt; newservername&gt;</span><span class="sxs-lookup"><span data-stu-id="07040-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="07040-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="07040-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="07040-151">Después, reinicie el servicio de servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="07040-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="07040-152">Busque el archivo SftMgmt. udl en el directorio de instalación de App-V Management Server (el valor predeterminado es C:\\Archivos de Programa\\microsoft System Center de la aplicación virt Management Server\\App virt Management Service).</span><span class="sxs-lookup"><span data-stu-id="07040-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="07040-153">Haga clic con el botón derecho en el archivo y seleccione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="07040-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="07040-154">En la pestaña **conexión** , escriba el nombre del equipo de destino que está ejecutando SQL Server y, a continuación, haga clic en **probar conexión**.</span><span class="sxs-lookup"><span data-stu-id="07040-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="07040-155">Cuando la prueba se haya realizado correctamente, haga clic en **Aceptar** y, a continuación, vuelva a hacer clic en **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="07040-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="07040-156">Para las versiones de App-V Management Server antes 4,5 SP2, debe actualizar la configuración de registro de SQL.</span><span class="sxs-lookup"><span data-stu-id="07040-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="07040-157">En **grupos de servidores**, haga clic con el botón secundario en el grupo de servidores del que es miembro el servidor y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="07040-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="07040-158">En la pestaña **registro** , haga clic para seleccionar la entrada de la **base de datos SQL** y, a continuación, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="07040-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="07040-159">Cambie el **nombre de host DNS** por el nombre de host del nuevo equipo que está ejecutando SQL Server y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="07040-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="07040-160">Haga clic en **Aceptar** dos veces más y, a continuación, reinicie el servicio de servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="07040-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="07040-161">Abra la consola de administración de App-V, haga clic con el botón derecho en el nodo **aplicaciones** y seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="07040-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="07040-162">La lista de aplicaciones debe mostrarse como antes.</span><span class="sxs-lookup"><span data-stu-id="07040-162">The list of applications should be displayed as before.</span></span>

 

 





