---
title: Notas de la versión de App-V 5.1
description: Notas de la versión de App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813310"
---
# <span data-ttu-id="ea4e6-103">Notas de la versión de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ea4e6-103">Release Notes for App-V 5.1</span></span>


<span data-ttu-id="ea4e6-104">A continuación se muestran algunos problemas conocidos de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.1.</span></span>

## <span data-ttu-id="ea4e6-105">Se produce un error durante la actualización de publicación entre el servidor de administración de App-V 5,0 SP3 y el cliente de App-V 5,1 en Windows 10</span><span class="sxs-lookup"><span data-stu-id="ea4e6-105">Error occurs during publishing refresh between App-V 5.0 SP3 Management Server and App-V 5.1 Client on Windows 10</span></span>


<span data-ttu-id="ea4e6-106">Se genera un error durante la actualización de publicación al sincronizar paquetes desde el servidor de administración de App-V 5,0 SP3 a un cliente de App-V 5,1 en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-106">An error is generated during publishing refresh when synchronizing packages from the App-V 5.0 SP3 management server to an App-V 5.1 client on Windows 10 .</span></span> <span data-ttu-id="ea4e6-107">Este error se produce porque el servidor de App-V 5,0 SP3 no comprende el sistema operativo Windows 10 que se especifica en la dirección URL de publicación.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-107">This error occurs because the App-V 5.0 SP3 server does not understand the Windows 10 operating system that is specified in the publishing URL.</span></span> <span data-ttu-id="ea4e6-108">El problema se ha corregido en el servidor de publicación de App-V 5,1, pero no se ha importado a las versiones de App-V 5,0 SP3 o anterior.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-108">The issue is fixed for App-V 5.1 publishing server, but is not backported to versions of App-V 5.0 SP3 or earlier.</span></span>

<span data-ttu-id="ea4e6-109">**Solución**: actualice el servidor de administración de App-v 5,0 al servidor de administración de App-v 5,1 para clientes de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-109">**Workaround**: Upgrade the App-V 5.0 Management server to the App-V 5.1 Management server for Windows 10 Clients.</span></span>

## <span data-ttu-id="ea4e6-110">Las configuraciones personalizadas no se aplican a los paquetes que se publicarán globalmente si se configuran con el servidor de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="ea4e6-110">Custom configurations do not get applied for packages that will be published globally if they are set using the App-V 5.1 Server</span></span>


<span data-ttu-id="ea4e6-111">Si asigna un paquete a un grupo de AD que contiene cuentas de equipo y aplica una configuración personalizada a ese grupo con el servidor de App-V, la configuración personalizada no se aplicará a esos equipos.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-111">If you assign a package to an AD group that contains machine accounts and apply a custom configuration to that group using the App-V Server, the custom configuration will not be applied to those machines.</span></span> <span data-ttu-id="ea4e6-112">El cliente de App-V 5,1 publicará paquetes asignados a una cuenta de equipo en todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-112">The App-V 5.1 Client will publish packages assigned to a machine account globally.</span></span> <span data-ttu-id="ea4e6-113">Sin embargo, almacena los archivos de configuración personalizados por usuario en el perfil de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-113">However, it stores custom configuration files per user in each user’s profile.</span></span> <span data-ttu-id="ea4e6-114">Los paquetes publicados globalmente no tendrán acceso a esta configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-114">Globally published packages will not have access to this custom configuration.</span></span>

<span data-ttu-id="ea4e6-115">**Solución alternativa**: realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="ea4e6-115">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="ea4e6-116">Asigne el paquete a grupos que contengan solo cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-116">Assign the package to groups containing only user accounts.</span></span> <span data-ttu-id="ea4e6-117">Esto asegurará que la configuración personalizada del paquete se almacenará en el perfil de cada usuario y se aplicará correctamente.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-117">This will ensure that the package’s custom configuration will be stored in each user’s profile and will be applied correctly.</span></span>

-   <span data-ttu-id="ea4e6-118">Cree un archivo de configuración de implementación personalizado y aplíquelo al paquete en el cliente con el cmdlet Add-AppvClientPackage con el parámetro – DynamicDeploymentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-118">Create a custom deployment configuration file and apply it to the package on the client using the Add-AppvClientPackage cmdlet with the –DynamicDeploymentConfiguration parameter.</span></span> <span data-ttu-id="ea4e6-119">Para obtener más información [, consulta acerca de la configuración dinámica de App-V 5,1](about-app-v-51-dynamic-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4e6-119">See [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md) for more information.</span></span>

-   <span data-ttu-id="ea4e6-120">Cree un paquete nuevo con la configuración personalizada mediante el secuenciador de aplicaciones-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-120">Create a new package with the custom configuration using the App-V 5.1 Sequencer.</span></span>

## <span data-ttu-id="ea4e6-121">Archivos de servidor no eliminados después de la instalación de la nueva aplicación: V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="ea4e6-121">Server files not deleted after new App-V 5.1 Server installation</span></span>


<span data-ttu-id="ea4e6-122">Si desinstala el servidor de App-V 5,0 SP1 y luego instala el servidor de App-V 5,1, se producirá un error en la instalación, se instalará la versión incorrecta del servidor de administración y se devolverá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-122">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.1 Server, the installation fails, the wrong version of the Management server is installed, and an error message is returned.</span></span> <span data-ttu-id="ea4e6-123">El problema se produce porque los archivos del servidor no se eliminan al desinstalar App-V 5,0 SP1, por lo que el proceso de instalación realiza una actualización en lugar de una instalación nueva.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-123">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the installation process does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="ea4e6-124">**Solución alternativa**: Elimine esta clave del registro antes de empezar a instalar App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="ea4e6-124">**Workaround**: Delete this registry key before you start installing App-V 5.1:</span></span>

<span data-ttu-id="ea4e6-125">En HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, busque y elimine la clave GUID de instalación que contiene el valor DWORD "DisplayName" con datos de valor "Microsoft Application Virtualization (App-V) Server".</span><span class="sxs-lookup"><span data-stu-id="ea4e6-125">Under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, locate and delete the installation GUID key that contains the DWORD value "DisplayName" with value data "Microsoft Application Virtualization (App-V) Server".</span></span> <span data-ttu-id="ea4e6-126">Esta es la única tecla que debe eliminarse.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-126">This is the only key that should be deleted.</span></span>

## <span data-ttu-id="ea4e6-127">Las asociaciones de tipos de archivo agregadas manualmente no se guardan correctamente</span><span class="sxs-lookup"><span data-stu-id="ea4e6-127">File type associations added manually are not saved correctly</span></span>


<span data-ttu-id="ea4e6-128">Las asociaciones de tipos de archivo agregadas manualmente a un paquete de aplicación mediante los accesos directos y la ficha FTAs al final del Asistente para actualización de aplicaciones no se guardan correctamente.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-128">File type associations added to an application package manually using the Shortcuts and FTAs tab at the end of the application upgrade wizard are not saved correctly.</span></span> <span data-ttu-id="ea4e6-129">No estarán disponibles para el cliente de App-V ni para el secuenciador cuando actualice el paquete guardado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-129">They will not be available to the App-V Client or to the Sequencer when updating the saved package again.</span></span>

<span data-ttu-id="ea4e6-130">**Solución alternativa**: para agregar una asociación de tipo de archivo, abra el paquete para modificar y ejecute el Asistente para actualización.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-130">**Workaround**: To add a file type association, open the package for modification and run the update wizard.</span></span> <span data-ttu-id="ea4e6-131">Durante el paso de instalación, agregue la nueva asociación de tipo de archivo a través del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-131">During the Installation step, add the new file type association through the operating system.</span></span> <span data-ttu-id="ea4e6-132">El secuenciador detectará la nueva asociación en el registro del sistema y la agregará al registro virtual del paquete, donde estará disponible para el cliente.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-132">The sequencer will detect the new association in the system registry and add it to the package’s virtual registry, where it will be available to the client.</span></span>

## <span data-ttu-id="ea4e6-133">Al transmitir paquetes en el modo de almacén de contenido compartido (SCS) a un cliente que también se administra con AppLocker, se escriben datos adicionales en el disco local.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-133">When streaming packages in Shared Content Store (SCS) mode to a client that is also managed with AppLocker, additional data is written to the local disk.</span></span>


<span data-ttu-id="ea4e6-134">Para reducir la cantidad de datos que se escriben en el disco local de un cliente, puede habilitar el modo SCS en el cliente de App-V 5,1 para transmitir el contenido de un paquete a petición.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-134">To decrease the amount of data written to a client’s local disk, you can enable SCS mode on the App-V 5.1 Client to stream the contents of a package on demand.</span></span> <span data-ttu-id="ea4e6-135">Sin embargo, si AppLocker administra una aplicación dentro del paquete, algunos datos podrían escribirse en el disco local del cliente que no se escribiría de otra manera.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-135">However, if AppLocker manages an application within the package, some data might be written to the client’s local disk that would not otherwise be written.</span></span>

<span data-ttu-id="ea4e6-136">**Solución alternativa**: ninguna</span><span class="sxs-lookup"><span data-stu-id="ea4e6-136">**Workaround**: None</span></span>

## <span data-ttu-id="ea4e6-137">En el cuadro de diálogo Agregar paquete de consola de administración, el botón examinar no está disponible al usar Chrome o Firefox</span><span class="sxs-lookup"><span data-stu-id="ea4e6-137">In the Management Console Add Package dialog box, the Browse button is not available when using Chrome or Firefox</span></span>


<span data-ttu-id="ea4e6-138">En la página paquetes de la consola de administración, si hace clic en **Agregar o actualizar** en la esquina inferior derecha, aparece el cuadro de diálogo **Agregar paquete** .</span><span class="sxs-lookup"><span data-stu-id="ea4e6-138">On the Packages page of the Management Console, if you click **Add or Upgrade** in the lower-right corner, the **Add Package** dialog box appears.</span></span> <span data-ttu-id="ea4e6-139">Si accede a la consola de administración con Chrome o Firefox como explorador, no podrá desplazarse hasta la ubicación del paquete.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-139">If you are accessing the Management Console using Chrome or Firefox as your browser, you will not be able to browse to the location of the package.</span></span>

<span data-ttu-id="ea4e6-140">**Solución alternativa**: escriba o copie y pegue la ruta de acceso al paquete en el campo **Agregar paquete** de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-140">**Workaround**: Type or copy and paste the path to the package into the **Add Package** input field.</span></span> <span data-ttu-id="ea4e6-141">Si la consola de administración tiene acceso a esta ruta de acceso, podrá agregar el paquete.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-141">If the Management Console has access to this path, you will be able to add the package.</span></span> <span data-ttu-id="ea4e6-142">Si el paquete está en un recurso compartido de red, puede ir a la ubicación con el explorador de archivos siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ea4e6-142">If the package is on a network share, you can browse to the location using File Explorer by doing these steps:</span></span>

1.  <span data-ttu-id="ea4e6-143">Mantenga pulsada la **tecla Mayús**y haga clic con el botón derecho en el archivo del paquete.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-143">While pressing **Shift**, right-click on the package file</span></span>

2.  <span data-ttu-id="ea4e6-144">Seleccione **Copiar como ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="ea4e6-144">Select **Copy as path**</span></span>

3.  <span data-ttu-id="ea4e6-145">Pegue la ruta de acceso en el campo de entrada del cuadro de diálogo **Agregar paquete**</span><span class="sxs-lookup"><span data-stu-id="ea4e6-145">Paste the path into the **Add Package** dialog box input field</span></span>

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a><span data-ttu-id="ea4e6-146">Al actualizar App-V Management Server a 5,1, a veces se produce un error con el mensaje "se ha producido un error de base de datos"</span><span class="sxs-lookup"><span data-stu-id="ea4e6-146">Upgrading App-V Management Server to 5.1 sometimes fails with the message “A database error occurred”</span></span>


<span data-ttu-id="ea4e6-147">Si instala el servidor de administración de App-V 5,0 SP1 y, a continuación, intenta actualizar a App-V 5,1 Server cuando se han configurado y habilitado varios grupos de conexión, se muestra el siguiente error: "error de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-147">If you install the App-V 5.0 SP1 Management Server, and then try to upgrade to App-V 5.1 Server when multiple connection groups are configured and enabled, the following error is displayed: “A database error occurred.</span></span> <span data-ttu-id="ea4e6-148">Motivo: ' nombre de columna no válido ' PackageOptional '.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-148">Reason: 'Invalid column name 'PackageOptional'.</span></span> <span data-ttu-id="ea4e6-149">Nombre de columna no válido ' VersionOptional '.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-149">Invalid column name 'VersionOptional'.”</span></span>

<span data-ttu-id="ea4e6-150">**Solución**: ejecute este comando en la base de datos SQL:</span><span class="sxs-lookup"><span data-stu-id="ea4e6-150">**Workaround**: Run this command on your SQL database:</span></span>

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

<span data-ttu-id="ea4e6-151">donde "AppVManagement" es el nombre de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-151">where “AppVManagement” is the name of the database.</span></span>

## <span data-ttu-id="ea4e6-152">Los usuarios no pueden abrir un paquete en un grupo de conexión publicado por el usuario si agrega o quita un paquete opcional</span><span class="sxs-lookup"><span data-stu-id="ea4e6-152">Users cannot open a package in a user-published connection group if you add or remove an optional package</span></span>


<span data-ttu-id="ea4e6-153">En los entornos en los que se ejecuta el cliente RDS o que tienen varios usuarios simultáneos por equipo, los usuarios con sesión iniciada no pueden abrir aplicaciones en paquetes que se encuentren en un grupo de conexiones publicadas por el usuario si se agrega o se quita un paquete opcional del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-153">In environments that are running the RDS Client or that have multiple concurrent users per computer, logged-in users cannot open applications in packages that are in a user-published connection group if an optional package is added to or removed from the connection group.</span></span>

<span data-ttu-id="ea4e6-154">**Solución alternativa**: haga que los usuarios cierren sesión y vuelva a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-154">**Workaround**: Have users log out and then log back in.</span></span>

## <span data-ttu-id="ea4e6-155">El mensaje de error se muestra de forma incorrecta cuando el grupo de conexión se publica solo para el usuario</span><span class="sxs-lookup"><span data-stu-id="ea4e6-155">Error message is erroneously displayed when the connection group is published only to the user</span></span>


<span data-ttu-id="ea4e6-156">Cuando ejecute repair-AppvClientConnectionGroup, se mostrará el error siguiente, incluso cuando el grupo de conexión se publique solo para el usuario: "error de integración de la aplicación interna: el paquete no está integrado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-156">When you run Repair-AppvClientConnectionGroup, the following error is displayed, even when the connection group is published only to the user: “Internal App-V Integration error: Package not integrated for the user.</span></span> <span data-ttu-id="ea4e6-157">Asegúrese de que el paquete se agregue a la máquina y se publique para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-157">Please ensure that the package is added to the machine and published to the user.”</span></span>

<span data-ttu-id="ea4e6-158">**Solución alternativa**: realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="ea4e6-158">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="ea4e6-159">Publicar todos los paquetes de un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-159">Publish all packages in a connection group.</span></span>

    <span data-ttu-id="ea4e6-160">El problema surge cuando el grupo de conexión que se repara tiene paquetes que faltan o que no están disponibles para el usuario (es decir, no se publican globalmente ni al usuario).</span><span class="sxs-lookup"><span data-stu-id="ea4e6-160">The problem arises when the connection group being repaired has packages that are missing or not available to the user (that is, not published globally or to the user).</span></span> <span data-ttu-id="ea4e6-161">Sin embargo, la reparación funcionará si todos los paquetes del grupo de conexión están disponibles, así que asegúrese de que todos los paquetes estén publicados.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-161">However, the repair will work if all of the connection group’s packages are available, so ensure that all packages are published.</span></span>

-   <span data-ttu-id="ea4e6-162">Para reparar paquetes de forma individual, use el comando repair-AppvClientPackage en lugar del comando repair-AppvClientConnectionGroup.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-162">Repair packages individually using the Repair-AppvClientPackage command rather than the Repair-AppvClientConnectionGroup command.</span></span>

    <span data-ttu-id="ea4e6-163">Determine qué paquetes estarán disponibles para los usuarios y, a continuación, ejecute el comando repair-AppvClientPackage una vez para cada paquete.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-163">Determine which packages are available to users and then run the Repair-AppvClientPackage command once for each package.</span></span> <span data-ttu-id="ea4e6-164">Use los cmdlets de PowerShell para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ea4e6-164">Use PowerShell cmdlets to do the following:</span></span>

    1.  <span data-ttu-id="ea4e6-165">Obtener todos los paquetes de un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-165">Get all the packages in a connection group.</span></span>

    2.  <span data-ttu-id="ea4e6-166">Compruebe si cada paquete está publicado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-166">Check to see if each package is currently published.</span></span>

    3.  <span data-ttu-id="ea4e6-167">Si el paquete está publicado actualmente, ejecute repair-AppvClientPackage en ese paquete.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-167">If the package is currently published, run Repair-AppvClientPackage on that package.</span></span>

## <span data-ttu-id="ea4e6-168">Los iconos no se muestran correctamente en el secuenciador</span><span class="sxs-lookup"><span data-stu-id="ea4e6-168">Icons not displayed properly in Sequencer</span></span>


<span data-ttu-id="ea4e6-169">Los iconos de las pestañas accesos directos y asociaciones de tipos de archivo no se muestran correctamente al modificar un paquete en el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-169">Icons in the Shortcuts and File Type Associations tab are not displayed correctly when modifying a package in the App-V Sequencer.</span></span> <span data-ttu-id="ea4e6-170">Este problema se produce cuando el tamaño de los iconos no es 16x16 ni de 32x32.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-170">This problem occurs when the size of the icons are not 16x16 or 32x32.</span></span>

<span data-ttu-id="ea4e6-171">**Solución alternativa**: Use iconos que sean 16x16 o 32x32.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-171">**Workaround**: Only use icons that are 16x16 or 32x32.</span></span>

## <span data-ttu-id="ea4e6-172">La secuencia de comandos InsertVersionInfo. SQL ya no es necesaria para la base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="ea4e6-172">InsertVersionInfo.sql script no longer required for the Management Database</span></span>


<span data-ttu-id="ea4e6-173">La secuencia de comandos InsertVersionInfo. SQL no es necesaria para las versiones de la base de datos de administración de App-V 5,0 SP3 más tarde que App-V SP3.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-173">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="ea4e6-174">La secuencia de comandos Permissions. SQL debe actualizarse de acuerdo con el **paso 2** del [artículo 3031340 de KB](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="ea4e6-174">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span>

<span data-ttu-id="ea4e6-175">**Importante** 
 El **paso 1** no es necesario para las versiones de App-v posteriores a App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-175">**Important**
**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

 

## <span data-ttu-id="ea4e6-176">Microsoft Visual Studio 2012 no es compatible</span><span class="sxs-lookup"><span data-stu-id="ea4e6-176">Microsoft Visual Studio 2012 not supported</span></span>


<span data-ttu-id="ea4e6-177">App-V 5,1 no admite Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-177">App-V 5.1 does not support Visual Studio 2012.</span></span>

<span data-ttu-id="ea4e6-178">**Solución alternativa**: ninguna</span><span class="sxs-lookup"><span data-stu-id="ea4e6-178">**Workaround**: None</span></span>

## <span data-ttu-id="ea4e6-179">Restricciones del nombre de archivo de la aplicación para el secuenciador de App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="ea4e6-179">Application filename restrictions for App-V 5.x Sequencer</span></span>


<span data-ttu-id="ea4e6-180">El secuenciador de App-V 5. x no puede secuenciar aplicaciones con nombres de archivo que coincidan con "CO_ &lt; x &gt; " donde x es un número.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-180">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="ea4e6-181">Se generará el error 0x8007139F.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-181">Error 0x8007139F will be generated.</span></span>

<span data-ttu-id="ea4e6-182">**Solución alternativa**: use otro nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="ea4e6-182">**Workaround**: Use a different filename</span></span>

## <span data-ttu-id="ea4e6-183">Error intermitente "archivo no encontrado" al montar un paquete</span><span class="sxs-lookup"><span data-stu-id="ea4e6-183">Intermittent "File Not Found" error when Mounting a Package</span></span>


<span data-ttu-id="ea4e6-184">En ocasiones, al montar un paquete, se genera un error "archivo no encontrado" (0x80070002).</span><span class="sxs-lookup"><span data-stu-id="ea4e6-184">Occasionally when mounting a package, a "File Not Found" (0x80070002) error is generated.</span></span> <span data-ttu-id="ea4e6-185">Esto suele ocurrir cuando una carpeta en un paquete de App-V contiene muchos archivos (es decir, 20.000 o más).</span><span class="sxs-lookup"><span data-stu-id="ea4e6-185">Typically, this occurs when a folder in an App-V package contains many files ( i.e. 20K or more).</span></span> <span data-ttu-id="ea4e6-186">Esto puede provocar que la transmisión tarde más de lo esperado y que se agote el tiempo de espera, lo que genera el error "no se encuentra el archivo".</span><span class="sxs-lookup"><span data-stu-id="ea4e6-186">This can cause streaming to take longer than expected and to time out which generates the "File Not Found" error.</span></span>

<span data-ttu-id="ea4e6-187">**Solución alternativa**: a partir de HF06, se ha introducido una nueva clave del registro para habilitar la extensión de este período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-187">**Workaround**: Starting with HF06, a new registry key has been introduced to enable extending this time-out period.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left"><span data-ttu-id="ea4e6-188">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="ea4e6-188">Path</span></span></td>
<td align="left"><span data-ttu-id="ea4e6-189">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</span><span class="sxs-lookup"><span data-stu-id="ea4e6-189">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Streaming</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="ea4e6-190">Configuración</span><span class="sxs-lookup"><span data-stu-id="ea4e6-190">Setting</span></span></td>
<td align="left"><span data-ttu-id="ea4e6-191">StreamResponseWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="ea4e6-191">StreamResponseWaitTimeout</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="ea4e6-192">Tipo de de</span><span class="sxs-lookup"><span data-stu-id="ea4e6-192">DataType</span></span></td>
<td align="left"><span data-ttu-id="ea4e6-193">DWORD</span><span class="sxs-lookup"><span data-stu-id="ea4e6-193">DWORD</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="ea4e6-194">Unit</span><span class="sxs-lookup"><span data-stu-id="ea4e6-194">Units</span></span></td>
<td align="left"><span data-ttu-id="ea4e6-195">Segundos</span><span class="sxs-lookup"><span data-stu-id="ea4e6-195">Seconds</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="ea4e6-196">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="ea4e6-196">Default</span></span></td>
<td align="left"><span data-ttu-id="ea4e6-197">4</span><span class="sxs-lookup"><span data-stu-id="ea4e6-197">5</span></span><br />
<strong><span data-ttu-id="ea4e6-198">Nota </strong> : este valor es el predeterminado si la clave del registro no está definida o se &lt; especifica un valor = 5.</span><span class="sxs-lookup"><span data-stu-id="ea4e6-198">Note</strong>: this value is the default if the registry key is not defined or a value &lt;=5 is specified.</span></span>
</td>
</tr>
</tbody>
</table>






## <span data-ttu-id="ea4e6-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea4e6-199">Related topics</span></span>


[<span data-ttu-id="ea4e6-200">Acerca de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ea4e6-200">About App-V 5.1</span></span>](about-app-v-51.md)

 

 





