---
title: Notas de la versión de App-V 5.0 SP2
description: Notas de la versión de App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813327"
---
# <span data-ttu-id="b7c50-103">Notas de la versión de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="b7c50-103">Release Notes for App-V 5.0 SP2</span></span>


**<span data-ttu-id="b7c50-104">Para buscar un problema específico en estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="b7c50-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="b7c50-105">Lea estas notas de la versión minuciosamente antes de instalar App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b7c50-105">Read these release notes thoroughly before you install App-V 5.0 SP2.</span></span>

<span data-ttu-id="b7c50-106">Estas notas de la versión contienen información necesaria para instalar correctamente App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b7c50-106">These release notes contain information that is required to successfully install App-V 5.0 SP2.</span></span> <span data-ttu-id="b7c50-107">Las notas de la versión también contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="b7c50-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="b7c50-108">Si hay diferencias entre estas notas de la versión y otra documentación de App-V 5,0, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="b7c50-108">If there are differences between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="b7c50-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="b7c50-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="b7c50-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="b7c50-110">About the Product Documentation</span></span>


<span data-ttu-id="b7c50-111">Para obtener información sobre la documentación de App-V 5,0, consulte la página de inicio de App-V 5,0 en Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="b7c50-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="b7c50-112">Enviar comentarios</span><span class="sxs-lookup"><span data-stu-id="b7c50-112">Provide Feedback</span></span>


<span data-ttu-id="b7c50-113">Nos interesan tus comentarios en App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b7c50-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="b7c50-114">Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="b7c50-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="b7c50-115">**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios en nuestra documentación y versiones de productos.</span><span class="sxs-lookup"><span data-stu-id="b7c50-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="b7c50-116">Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="b7c50-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="b7c50-117">Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="b7c50-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="b7c50-118">Problemas conocidos con el paquete de revisiones 4 para Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="b7c50-118">Known Issues with Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>


### <span data-ttu-id="b7c50-119">Los paquetes dejan de funcionar después de desinstalar el paquete de revisiones 4 para Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="b7c50-119">Packages stop working after you uninstall Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>

<span data-ttu-id="b7c50-120">Paquetes publicados cuando se aplica el paquete de revisiones 4 para Application Virtualization 5,0 SP2 deje de funcionar cuando se quita el paquete de revisiones 4 para Application Virtualization 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b7c50-120">Packages published when Hotfix Package 4 for Application Virtualization 5.0 SP2 is applied stop working when Hotfix Package 4 for Application Virtualization 5.0 SP2 is removed.</span></span>

<span data-ttu-id="b7c50-121">SOLUCIÓN alternativa</span><span class="sxs-lookup"><span data-stu-id="b7c50-121">WORKAROUND:</span></span>

<span data-ttu-id="b7c50-122">Si la siguiente carpeta existe, debe eliminarla:</span><span class="sxs-lookup"><span data-stu-id="b7c50-122">If the following folder exists, then you must delete it:</span></span>

<span data-ttu-id="b7c50-123">**% LocalAppData%**  \\  **Microsoft**  \\  **AppV**  \\  **Cliente**  \\  **VFS**  \\  \*\* &lt; identificador &gt; del paquete\*\* para cada paquete publicado.</span><span class="sxs-lookup"><span data-stu-id="b7c50-123">**%localappdata%** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **VFS** \\ **&lt;package ID&gt;** for each package that was published.</span></span>

<span data-ttu-id="b7c50-124">**Nota:**  Debe tener privilegios elevados para eliminar esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="b7c50-124">**Note** You must have elevated privileges to delete this folder.</span></span>

 

<span data-ttu-id="b7c50-125">Para usar un script, para cada cuenta de usuario en el equipo y para cada identificador de paquete que se publicó después de instalar el paquete de revisiones 4 para Application Virtualization 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="b7c50-125">To use a script, for each user account on the computer and for each package id that was published after installing Hotfix Package 4 for Application Virtualization 5.0 SP2:</span></span>

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   <span data-ttu-id="b7c50-126">Los accesos directos permanecerán con las sesiones de usuario incluso después de eliminar la carpeta del directorio de la sección anterior, de modo que pueda hacer clic en el acceso directo para volver a ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7c50-126">The shortcuts will remain with the user sessions even after deleting the folder from the directory in the previous section, so you can click on the shortcut to run the application again.</span></span> <span data-ttu-id="b7c50-127">No es necesario volver a publicar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7c50-127">There is no need to re-publish the application.</span></span>

-   <span data-ttu-id="b7c50-128">Este problema se produce para paquetes publicados de forma global y empaquetadas por el usuario, por ejemplo, Microsoft Office2013.</span><span class="sxs-lookup"><span data-stu-id="b7c50-128">This issue happens for both user published packaged and globally published packages for example, Microsoft Office2013.</span></span> <span data-ttu-id="b7c50-129">Para ambos tipos de paquetes, debe eliminarse la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b7c50-129">The folder must be deleted for both types of packages.</span></span>

-   <span data-ttu-id="b7c50-130">No es necesario eliminar la carpeta VFS en los datos de la aplicación de itinerancia (**% AppData%**).</span><span class="sxs-lookup"><span data-stu-id="b7c50-130">You do not need to delete the VFS folder in the Roaming app data (**%appdata%**).</span></span> <span data-ttu-id="b7c50-131">Solo se debe eliminar el **% LocalAppData%** .</span><span class="sxs-lookup"><span data-stu-id="b7c50-131">Only the **%localappdata%** must be deleted.</span></span>

### <span data-ttu-id="b7c50-132">La integración de Microsoft Office apunta a una ubicación incorrecta del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="b7c50-132">Microsoft Office integration points to wrong file system location</span></span>

<span data-ttu-id="b7c50-133">La integración de Microsoft Office apunta a una ubicación incorrecta del sistema de archivos (mensaje de error Groove.exe).</span><span class="sxs-lookup"><span data-stu-id="b7c50-133">Microsoft Office integration points to wrong file system location (Groove.exe error message).</span></span>

<span data-ttu-id="b7c50-134">SOLUCIÓN alternativa</span><span class="sxs-lookup"><span data-stu-id="b7c50-134">WORKAROUND:</span></span>

<span data-ttu-id="b7c50-135">Use uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7c50-135">Use one of the following methods:</span></span>

1.  <span data-ttu-id="b7c50-136">Elimine el acceso directo en la carpeta de inicio después de la actualización.</span><span class="sxs-lookup"><span data-stu-id="b7c50-136">Delete the shortcut in the start-up folder after upgrade.</span></span>

2.  <span data-ttu-id="b7c50-137">Cambie el método abreviado en la carpeta de inicio con un script.</span><span class="sxs-lookup"><span data-stu-id="b7c50-137">Change the shortcut in the start-up folder using a script.</span></span>

3.  <span data-ttu-id="b7c50-138">Use el archivo de configuración de implementación para especificar el destino de acceso directo a la raíz de integración.</span><span class="sxs-lookup"><span data-stu-id="b7c50-138">Use the deployment configuration file to specify the shortcut target to the integration root.</span></span>

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> <span data-ttu-id="b7c50-139">El paquete de Hotfix 4 para el instalador de Application Virtualization 5,0 SP2 puede tardar mucho tiempo</span><span class="sxs-lookup"><span data-stu-id="b7c50-139">Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can take a long time</span></span>

<span data-ttu-id="b7c50-140">El paquete de revisiones 4 para el instalador de Application Virtualization 5,0 SP2 puede tardar mucho tiempo en función de cuántos archivos se almacenan en la memoria caché del paquete existente.</span><span class="sxs-lookup"><span data-stu-id="b7c50-140">The Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can potentially take a long time depending on how many files are stored in the existing package cache.</span></span>

<span data-ttu-id="b7c50-141">La actualización de los descriptores de seguridad de paquetes asociados durante el paquete 4 de hotfix para la instalación de Application Virtualization 5,0 SP2 tiene un impacto significativo en el tiempo que tarda la instalación.</span><span class="sxs-lookup"><span data-stu-id="b7c50-141">Updating associated package security descriptors during the Hotfix Package 4 for Application Virtualization 5.0 SP2 installation has a significant impact on how long it takes the installation will take.</span></span> <span data-ttu-id="b7c50-142">Anteriormente, la instalación de la instalación era estándar de duración.</span><span class="sxs-lookup"><span data-stu-id="b7c50-142">Previously, the installation install was standard in duration.</span></span> <span data-ttu-id="b7c50-143">Sin embargo, ahora depende de cuántos archivos haya ensayado en la caché del paquete.</span><span class="sxs-lookup"><span data-stu-id="b7c50-143">However, it now depends on how many files you have staged in the package cache.</span></span>

<span data-ttu-id="b7c50-144">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="b7c50-144">WORKAROUND: None</span></span>

### <span data-ttu-id="b7c50-145">No se puede desinstalar el paquete de Hotfix 4 para Application Virtualization 5,0 SP2 si el paquete JIT-V está en uso</span><span class="sxs-lookup"><span data-stu-id="b7c50-145">Uninstalling Hotfix Package 4 for Application Virtualization 5.0 SP2 fails if JIT-V package is in use</span></span>

<span data-ttu-id="b7c50-146">Si instala el paquete de revisiones 4 para Application Virtualization 5,0 SP2 y, a continuación, intenta desinstalar la corrección urgente cuando se usa la virtualización Just-in-Time (JIT-V), la operación se producirá un error si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7c50-146">If you install Hotfix Package 4 for Application Virtualization 5.0 SP2 and then try to uninstall the hotfix when just-in-time virtualization (JIT-V) is being used, the operation will fail if all of the following conditions are true:</span></span>

-   <span data-ttu-id="b7c50-147">Instaló con un archivo de Windows Installer (. msi) y, a continuación, aplica actualizaciones con un archivo de revisión de Microsoft Installer (. msp).</span><span class="sxs-lookup"><span data-stu-id="b7c50-147">You installed by using a Windows Installer file (.msi), and then you apply updates by using a Microsoft Installer Patch File (.msp).</span></span>

-   <span data-ttu-id="b7c50-148">Intenta desinstalar una actualización con el elemento agregar o quitar programas del panel de control.</span><span class="sxs-lookup"><span data-stu-id="b7c50-148">You try to uninstall an update by using the Add or Remove Programs item in Control Panel.</span></span>

-   <span data-ttu-id="b7c50-149">Un paquete habilitado para JIT se está ejecutando en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b7c50-149">A JIT-V-enabled package is running on the computer.</span></span>

<span data-ttu-id="b7c50-150">SOLUCIÓN alternativa: Complete los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7c50-150">WORKAROUND: Complete the following steps:</span></span>

1.  <span data-ttu-id="b7c50-151">Abra Windows PowerShell y ejecute los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="b7c50-151">Open Windows PowerShell and run the following commands:</span></span>

    -   **<span data-ttu-id="b7c50-152">Importación-módulo appvclient</span><span class="sxs-lookup"><span data-stu-id="b7c50-152">Import-module appvclient</span></span>**

    -   **<span data-ttu-id="b7c50-153">Get-AppvClientPackage | Stop-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b7c50-153">Get-AppvClientPackage | Stop-AppvClientPackage</span></span>**

2.  <span data-ttu-id="b7c50-154">Desinstale la actualización con agregar o quitar programas.</span><span class="sxs-lookup"><span data-stu-id="b7c50-154">Uninstall the update using Add or Remove Programs.</span></span>

## <span data-ttu-id="b7c50-155">Problemas conocidos con App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="b7c50-155">Known Issues with App-V 5.0 SP2</span></span>


### <a href="" id="bkmk-folderredirection"></a><span data-ttu-id="b7c50-156">En ocasiones, el redireccionamiento de carpetas de clientes de App-V no mueve los archivos de% AppData% a% LocalAppData%</span><span class="sxs-lookup"><span data-stu-id="b7c50-156">App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%</span></span>

<span data-ttu-id="b7c50-157">Cuando% AppData% es una carpeta de red compartida que ha configurado para el redireccionamiento de carpetas, los cambios que los usuarios finales hacen a AppData (roaming) se pueden perder al cambiar de equipos o cuando se desactiva su AppData local cuando cierran sesión y luego vuelven a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="b7c50-157">When %AppData% is a shared network folder that you have configured for folder redirection, the changes that end users make to AppData (Roaming) can be lost when they switch computers or when their local AppData is cleared when they log off and then log back on.</span></span> <span data-ttu-id="b7c50-158">Este error se produce porque la clave del registro (AppDataTime), que indica la última carga conocida, no está sincronizada con AppData locales en caché.</span><span class="sxs-lookup"><span data-stu-id="b7c50-158">This error occurs because the registry key (AppDataTime), which indicates the last known upload, gets out of synchronization with the local cached AppData.</span></span>

<span data-ttu-id="b7c50-159">SOLUCIÓN: elimine manualmente la siguiente clave de registro para cada paquete relevante cuando un usuario final inicie o apague:</span><span class="sxs-lookup"><span data-stu-id="b7c50-159">WORKAROUND: Manually delete the following registry key for each relevant package when an end user logs on or off:</span></span>

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

<span data-ttu-id="b7c50-160">La primera vez que los usuarios finales inician una aplicación en el paquete después de que inicien sesión, App-V fuerza la descarga del% AppData%, incluso si% LocalAppData% ya está actualizado.</span><span class="sxs-lookup"><span data-stu-id="b7c50-160">The first time that end users start an application in the package after they log in, App-V forces a download of the zipped %AppData%, even if %LocalAppData% is already up to date.</span></span>

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> <span data-ttu-id="b7c50-161">El Service Pack 2 de App-V 5,0 (App-V 5,0 SP2) no incluye una nueva versión del servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="b7c50-161">App-V 5.0 Service Pack 2 (App-V 5.0 SP2) does not include a new version of the App-V Server</span></span>

<span data-ttu-id="b7c50-162">App-V 5.0 SP2 no incluye una nueva versión del servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="b7c50-162">App-V 5.0SP2 does not include a new version of the App-V Server.</span></span> <span data-ttu-id="b7c50-163">Si implementa los clientes de App-V 5,0 SP2 que ejecutan Windows 8,1 en su entorno y planea administrar los clientes mediante la infraestructura de App-V, debe instalar el [paquete de revisiones 2 para Microsoft Application virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span><span class="sxs-lookup"><span data-stu-id="b7c50-163">If you deploy App-V 5.0 SP2 clients running Windows 8.1 in your environment and plan to manage the clients using the App-V infrastructure, you must install [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span></span> <span data-ttu-id="b7c50-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span><span class="sxs-lookup"><span data-stu-id="b7c50-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span></span>

<span data-ttu-id="b7c50-165">Si está ejecutando y administrando los clientes de App-V 5,0 SP2 con cualquiera de los siguientes métodos, no se necesita la actualización de cliente:</span><span class="sxs-lookup"><span data-stu-id="b7c50-165">If you are running and managing App-V 5.0 SP2 clients using any of the following methods no client update is required:</span></span>

-   <span data-ttu-id="b7c50-166">Modo Independiente.</span><span class="sxs-lookup"><span data-stu-id="b7c50-166">Standalone mode.</span></span>

-   <span data-ttu-id="b7c50-167">Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b7c50-167">Configuration Manager.</span></span>

-   <span data-ttu-id="b7c50-168">ESD de terceros.</span><span class="sxs-lookup"><span data-stu-id="b7c50-168">Third party ESD.</span></span>

<span data-ttu-id="b7c50-169">El cliente de App-V 5,0 SP2 es totalmente compatible con Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="b7c50-169">The App-V 5.0 SP2 client is fully compatible with Windows 8.1</span></span>

<span data-ttu-id="b7c50-170">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="b7c50-170">WORKAROUND: None.</span></span>

## <span data-ttu-id="b7c50-171">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="b7c50-171">Release Notes Copyright Information</span></span>


<span data-ttu-id="b7c50-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7c50-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="b7c50-173">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="b7c50-173">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="b7c50-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7c50-174">Related topics</span></span>


[<span data-ttu-id="b7c50-175">Acerca de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="b7c50-175">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

 

 





