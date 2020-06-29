---
title: Permisos de acceso de usuario en el cliente de virtualización de aplicaciones
description: Permisos de acceso de usuario en el cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815120"
---
# <span data-ttu-id="e709c-103">Permisos de acceso de usuario en el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e709c-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="e709c-104">En la pestaña **permisos** en el cuadro de diálogo **propiedades** , accesible haciendo clic con el botón secundario en el nodo de **virtualización de aplicaciones** en la consola de administración del cliente de virtualización de aplicaciones, los administradores pueden conceder permisos a los usuarios para que usen las distintas funciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="e709c-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="e709c-105">**Nota:**  Antes de cambiar los permisos de los usuarios, asegúrese de que los cambios de permisos son coherentes con las pautas de la organización para conceder permisos de usuario.</span><span class="sxs-lookup"><span data-stu-id="e709c-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="e709c-106">En la tabla siguiente se enumeran y describen los permisos que se pueden conceder a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e709c-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e709c-107">Nombre del permiso</span><span class="sxs-lookup"><span data-stu-id="e709c-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="e709c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e709c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-109">Agregar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e709c-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-110">Registre nuevas aplicaciones pasando un nuevo archivo OSD al cliente mediante sfttray.exe, sftmime.exe o MMC.</span><span class="sxs-lookup"><span data-stu-id="e709c-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-111">Cambiar el tamaño de la caché del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="e709c-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-112">Aumente el tamaño de la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e709c-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-113">Cambiar la unidad del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="e709c-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-114">Seleccione otra letra de unidad preferida para el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e709c-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-115">Cambiar la configuración del registro</span><span class="sxs-lookup"><span data-stu-id="e709c-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-116">Cambie el nivel de registro o la ruta de acceso al registro del archivo de registro del cliente.</span><span class="sxs-lookup"><span data-stu-id="e709c-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-117">Cambiar archivos OSD</span><span class="sxs-lookup"><span data-stu-id="e709c-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-118">Modifique los archivos OSD para las aplicaciones registradas y paselos al cliente.</span><span class="sxs-lookup"><span data-stu-id="e709c-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="e709c-119">Esto no afecta a la actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="e709c-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-120">Borrar la configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e709c-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-121">Elimine los tipos de archivo, los accesos directos y cualquier configuración del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e709c-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-122">Eliminar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e709c-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-123">Quite todas las referencias a una aplicación del sistema de archivos y la caché OSD para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="e709c-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-124">Importar aplicaciones a la caché</span><span class="sxs-lookup"><span data-stu-id="e709c-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-125">Cargue los datos de la aplicación directamente desde un archivo SFT especificado en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e709c-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="e709c-126">Esto afecta a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e709c-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-127">Cargar aplicaciones en la caché</span><span class="sxs-lookup"><span data-stu-id="e709c-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-128">Inicie una carga del archivo SFT de una aplicación desde el origen configurado, como un servidor de streaming de App-V.</span><span class="sxs-lookup"><span data-stu-id="e709c-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="e709c-129">Esto carga la aplicación para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="e709c-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-130">Bloquear y desbloquear aplicaciones en la caché</span><span class="sxs-lookup"><span data-stu-id="e709c-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-131">Impedir o permitir que se descarguen aplicaciones de la memoria caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e709c-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="e709c-132">Esto afecta a todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="e709c-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-133">Administrar asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="e709c-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-134">Agregar, modificar o eliminar asociaciones de tipo de archivo solo para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e709c-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-135">Administrar la configuración de actualización de publicaciones</span><span class="sxs-lookup"><span data-stu-id="e709c-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-136">Cambie la configuración que controla la temporización de las actualizaciones de publicación para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="e709c-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-137">Administrar servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="e709c-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-138">Agregue, modifique o elimine servidores de publicación para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="e709c-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="e709c-139">Este permiso incluye implícitamente permisos para administrar la configuración de actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="e709c-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-140">Publicar accesos directos</span><span class="sxs-lookup"><span data-stu-id="e709c-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-141">Crear nuevos accesos directos a las aplicaciones registradas.</span><span class="sxs-lookup"><span data-stu-id="e709c-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="e709c-142">El usuario también debe tener permiso para crear archivos en el sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="e709c-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-143">Reparar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e709c-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-144">Quitar configuraciones específicas de la aplicación para el usuario actual sin eliminar accesos directos ni asociaciones de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e709c-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-145">Iniciar una actualización de publicación</span><span class="sxs-lookup"><span data-stu-id="e709c-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-146">Iniciar una actualización de publicación no programada para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e709c-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-147">Activar o desactivar el modo sin conexión</span><span class="sxs-lookup"><span data-stu-id="e709c-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-148">Cambie el cliente completo del modo en línea a sin conexión para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e709c-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e709c-149">Descargar aplicaciones de la caché</span><span class="sxs-lookup"><span data-stu-id="e709c-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-150">Borrar los datos de la aplicación de la caché del sistema de archivos para todos los usuarios sin quitar la configuración, los accesos directos ni las asociaciones de tipos de archivo específicos del usuario.</span><span class="sxs-lookup"><span data-stu-id="e709c-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e709c-151">Ver todas las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e709c-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="e709c-152">Permite al usuario ver las aplicaciones virtuales de todos los usuarios registrados en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e709c-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e709c-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e709c-153">Related topics</span></span>


[<span data-ttu-id="e709c-154">Cómo cambiar los permisos de acceso de usuario</span><span class="sxs-lookup"><span data-stu-id="e709c-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 





