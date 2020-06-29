---
title: Información de solución de problemas del cliente de virtualización de aplicaciones
description: Información de solución de problemas del cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815191"
---
# <span data-ttu-id="168f3-103">Información de solución de problemas del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="168f3-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="168f3-104">En este tema se incluye información que puede usar para solucionar varios problemas en el cliente de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="168f3-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="168f3-105">La actualización de publicaciones es muy lenta</span><span class="sxs-lookup"><span data-stu-id="168f3-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="168f3-106">Si la actualización de publicación en un equipo específico tarda mucho más tiempo de lo esperado y si el cliente está configurado para usar la configuración de **IconSourceRoot** , determine si **IconSourceRoot** contiene una dirección URL no válida.</span><span class="sxs-lookup"><span data-stu-id="168f3-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="168f3-107">Una dirección URL no válida producirá retrasos muy largos durante la actualización de la publicación.</span><span class="sxs-lookup"><span data-stu-id="168f3-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="168f3-108">Los usuarios no pueden conectarse al servidor e ir al modo de operaciones desconectadas</span><span class="sxs-lookup"><span data-stu-id="168f3-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="168f3-109">Si está usando un servidor de administración de App-V configurado con el protocolo RTSPs, si los usuarios no pueden conectarse y entran en el modo de operaciones desconectadas, determine si el certificado que se usa en el servidor es válido.</span><span class="sxs-lookup"><span data-stu-id="168f3-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="168f3-110">Un certificado no válido evitará que los usuarios se conecten y harán que pasen al modo de operaciones desconectadas.</span><span class="sxs-lookup"><span data-stu-id="168f3-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="168f3-111">Los usuarios experimentan un bajo nivel de rendimiento cuando las aplicaciones no se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="168f3-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="168f3-112">Cuando las aplicaciones no se almacenan en la memoria caché, es posible que ocasionalmente se produzcan problemas de rendimiento lentos o intermitentes al iniciar o usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="168f3-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="168f3-113">Hay varios motivos posibles por los que esto puede ocurrir, por ejemplo, cuando el cliente de App-V se encuentra en el proceso de carga automática de una aplicación o cuando se está procesando una solicitud fuera de secuencia.</span><span class="sxs-lookup"><span data-stu-id="168f3-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="168f3-114">Cuando las aplicaciones se almacenan en la caché por completo, estos problemas ya no se producen.</span><span class="sxs-lookup"><span data-stu-id="168f3-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="168f3-115">Error que se muestra después de quitar una actualización</span><span class="sxs-lookup"><span data-stu-id="168f3-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="168f3-116">Debe usar el formato de comando correcto de Windows Installer 3,1 para quitar una actualización del cliente de App-V, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="168f3-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="168f3-117">El uso del anterior formato de comando `msiexec /package <GUID> /uninstall <GUID>` producirá el error 6003 "no se pudo iniciar el cliente de Application Virtualization".</span><span class="sxs-lookup"><span data-stu-id="168f3-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="168f3-118">Código de error 0A-0000E01E se produce cuando intenta iniciar una aplicación</span><span class="sxs-lookup"><span data-stu-id="168f3-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="168f3-119">Código de error 0A-0000E01E indica que el paquete de la aplicación secuenciada podría estar dañado.</span><span class="sxs-lookup"><span data-stu-id="168f3-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="168f3-120">La solución es reordenar el paquete.</span><span class="sxs-lookup"><span data-stu-id="168f3-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="168f3-121">Los usuarios no pueden acceder a los archivos que han creado en la unidad Q:</span><span class="sxs-lookup"><span data-stu-id="168f3-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="168f3-122">Si los usuarios guardan archivos en la unidad **Q:** , no pueden recuperarlos porque no tienen derechos de lectura en la unidad.</span><span class="sxs-lookup"><span data-stu-id="168f3-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="168f3-123">Los usuarios no deben guardar los archivos en la unidad **Q:** .</span><span class="sxs-lookup"><span data-stu-id="168f3-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="168f3-124">Se muestra un mensaje de error 1D1</span><span class="sxs-lookup"><span data-stu-id="168f3-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="168f3-125">Cuando la dirección URL de transmisión de archivos se establece incorrectamente en el archivo descriptor de software abierto (OSD), el cliente de App-V devuelve un error 1D1 en lugar de un error "no se encuentra el archivo".</span><span class="sxs-lookup"><span data-stu-id="168f3-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="168f3-126">Este error indica que se produjo un error en el inicio de la aplicación y el usuario se ha forzado al modo de operaciones desconectado.</span><span class="sxs-lookup"><span data-stu-id="168f3-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="168f3-127">Corrija la dirección URL de transmisión de archivos.</span><span class="sxs-lookup"><span data-stu-id="168f3-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="168f3-128">Iconos incorrectos asociados con algunas aplicaciones</span><span class="sxs-lookup"><span data-stu-id="168f3-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="168f3-129">Cuando se va a usar un icono en una operación de publicación, el cliente de App-V determina en primer lugar si ya tiene una copia en caché del icono, consultando la caché de iconos de un elemento cuya ruta de acceso de origen original coincide con la ruta de acceso del icono dado a la operación de publicación.</span><span class="sxs-lookup"><span data-stu-id="168f3-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="168f3-130">Si el cliente de App-V encuentra una coincidencia, usará el icono ya almacenado en caché; en caso contrario, se descargará el nuevo icono en la caché.</span><span class="sxs-lookup"><span data-stu-id="168f3-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="168f3-131">Si la ruta de acceso al icono es un directorio de borrador o si se vuelve a utilizar para nuevos iconos o paquetes, la búsqueda en la memoria caché podría mostrar un icono incorrecto de una operación anterior.</span><span class="sxs-lookup"><span data-stu-id="168f3-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="168f3-132">Se solicitan las credenciales a los usuarios al iniciar una aplicación</span><span class="sxs-lookup"><span data-stu-id="168f3-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="168f3-133">Si un usuario intenta iniciar una aplicación virtual a la que el administrador del sistema ha restringido el acceso, es posible que se le pida al usuario que escriba las credenciales.</span><span class="sxs-lookup"><span data-stu-id="168f3-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="168f3-134">El usuario debe escribir el nombre de usuario y la contraseña de una cuenta que tenga permiso para iniciar la aplicación y, a continuación, presionar entrar.</span><span class="sxs-lookup"><span data-stu-id="168f3-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="168f3-135">Se produce un error en la actualización de publicación después de actualizar el cliente de App-V a la versión 4,5</span><span class="sxs-lookup"><span data-stu-id="168f3-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="168f3-136">Si el directorio de datos de usuario se colocó anteriormente en una ubicación no estándar (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nombreusuario*%), los usuarios que no tengan privilegios de administrador en el equipo encontrarán la actualización de publicación después de que se actualice el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="168f3-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="168f3-137">Durante la actualización, el directorio de datos globales del cliente App-V y todos sus subdirectorios están configurados con derechos de acceso restringido solo para administradores.</span><span class="sxs-lookup"><span data-stu-id="168f3-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="168f3-138">Para evitar este problema, cambie el directorio de datos de usuario antes de la actualización para que no sea un subdirectorio del directorio de datos global.</span><span class="sxs-lookup"><span data-stu-id="168f3-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="168f3-139">Reinicio necesario después de un error de instalación</span><span class="sxs-lookup"><span data-stu-id="168f3-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="168f3-140">Si se produce un error en la instalación del cliente por cualquier motivo y, si los intentos posteriores de instalar el cliente también fallan, compruebe el registro de Windows Installer para ver si se muestra un error "sftplay error, error = 1072".</span><span class="sxs-lookup"><span data-stu-id="168f3-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="168f3-141">Si es así, reinicie el equipo antes de intentar instalar el cliente de nuevo.</span><span class="sxs-lookup"><span data-stu-id="168f3-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="168f3-142">Reparar una aplicación virtual dañada</span><span class="sxs-lookup"><span data-stu-id="168f3-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="168f3-143">Si, por cualquier motivo, un paquete de aplicaciones virtual instalado con un archivo de paquete de Windows Installer (MSI) se daña, vuelva a instalar el paquete.</span><span class="sxs-lookup"><span data-stu-id="168f3-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="168f3-144">La función de reparación disponible en Windows Installer no actualizará los volúmenes de usuario.</span><span class="sxs-lookup"><span data-stu-id="168f3-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="168f3-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="168f3-145">Related topics</span></span>


[<span data-ttu-id="168f3-146">Referencia del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="168f3-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





