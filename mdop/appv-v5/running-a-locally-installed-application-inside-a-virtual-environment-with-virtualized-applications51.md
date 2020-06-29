---
title: Ejecución de una aplicación instalada localmente dentro de un entorno virtual con aplicaciones virtualizadas
description: Ejecución de una aplicación instalada localmente dentro de un entorno virtual con aplicaciones virtualizadas
author: dansimp
ms.assetid: 71baf193-a9e8-4ffa-aa7f-e0bffed2e4b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 384a1325b2f363595971f70f25fe0a25cade448d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813295"
---
# <span data-ttu-id="6f9b9-103">Ejecución de una aplicación instalada localmente dentro de un entorno virtual con aplicaciones virtualizadas</span><span class="sxs-lookup"><span data-stu-id="6f9b9-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="6f9b9-104">Puede ejecutar una aplicación instalada de forma local en un entorno virtual, junto con las aplicaciones que se han virtualizado mediante Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="6f9b9-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="6f9b9-105">Si lo desea, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="6f9b9-106">Desea instalar y ejecutar una aplicación de forma local en los equipos cliente, pero desea virtualizar y ejecutar complementos específicos que funcionen con esa aplicación local.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="6f9b9-107">Está solucionando problemas de un paquete de cliente de App-V y desea abrir una aplicación local dentro del entorno virtual de App-V.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="6f9b9-108">Use cualquiera de los métodos siguientes para abrir una aplicación local dentro del entorno virtual de App-V:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="6f9b9-109">Clave de registro RunVirtual</span><span class="sxs-lookup"><span data-stu-id="6f9b9-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="6f9b9-110">Cmdlet Get-AppvClientPackage de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9b9-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="6f9b9-111">/Appvpid de modificador de la línea de comandos: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="6f9b9-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="6f9b9-112">Modificador de enlace de la línea de comandos/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="6f9b9-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="6f9b9-113">Cada método realiza esencialmente la misma tarea, pero algunos métodos pueden ser más adecuados para algunas aplicaciones que otros, en función de si la aplicación virtualizada ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="6f9b9-114">Clave de registro RunVirtual</span><span class="sxs-lookup"><span data-stu-id="6f9b9-114">RunVirtual registry key</span></span>


<span data-ttu-id="6f9b9-115">Para agregar una aplicación instalada de forma local a un paquete o al entorno virtual de un grupo de conexión, agregue una subclave a la `RunVirtual` clave del registro en el editor del registro, como se describe en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="6f9b9-116">No hay ninguna opción de directiva de Grupo disponible para administrar esta clave del registro, por lo que tiene que usar System Center Configuration Manager u otro sistema de distribución electrónica de software (ESD), o editar manualmente el registro.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="6f9b9-117">Métodos admitidos para publicar paquetes al usar RunVirtual</span><span class="sxs-lookup"><span data-stu-id="6f9b9-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f9b9-118">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="6f9b9-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="6f9b9-119">Métodos de publicación admitidos</span><span class="sxs-lookup"><span data-stu-id="6f9b9-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9b9-120">App-V 5,0 SP3 y App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="6f9b9-120">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9b9-121">Publicada globalmente o al usuario</span><span class="sxs-lookup"><span data-stu-id="6f9b9-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f9b9-122">App-V 5,0 mediante App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="6f9b9-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9b9-123">Publicada globalmente solo</span><span class="sxs-lookup"><span data-stu-id="6f9b9-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6f9b9-124">Pasos para crear la subclave</span><span class="sxs-lookup"><span data-stu-id="6f9b9-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="6f9b9-125">Con la información de la tabla siguiente, cree una nueva clave del registro con el nombre del archivo ejecutable, por ejemplo, **MyApp.exe**.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6f9b9-126">Método de publicación de paquetes</span><span class="sxs-lookup"><span data-stu-id="6f9b9-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="6f9b9-127">Dónde crear la clave del registro</span><span class="sxs-lookup"><span data-stu-id="6f9b9-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6f9b9-128">Publicado globalmente</span><span class="sxs-lookup"><span data-stu-id="6f9b9-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6f9b9-129">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="6f9b9-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="6f9b9-130">Ejemplo </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="6f9b9-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6f9b9-131">Publicado para el usuario</span><span class="sxs-lookup"><span data-stu-id="6f9b9-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6f9b9-132">HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="6f9b9-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="6f9b9-133">Ejemplo </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="6f9b9-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6f9b9-134">El grupo de conexión puede contener:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6f9b9-135">Paquetes que se publican solo globalmente o solo para el usuario</span><span class="sxs-lookup"><span data-stu-id="6f9b9-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="6f9b9-136">Paquetes que se publican globalmente y al usuario</span><span class="sxs-lookup"><span data-stu-id="6f9b9-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="6f9b9-137">HKEY_LOCAL_MACHINE o HKEY_CURRENT_USER clave, pero se deben cumplir todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6f9b9-138">Si desea incluir varios paquetes en el entorno virtual, debe incluirlos en un grupo de conexión habilitado.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="6f9b9-139">Cree solo una subclave para uno de los paquetes en el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="6f9b9-140">Por ejemplo, si tiene un paquete que se publica globalmente y otro paquete publicado para el usuario, debe crear una subclave para cualquiera de estos paquetes, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="6f9b9-141">Aunque cree una subclave solo para uno de los paquetes, todos los paquetes del grupo de conexión, además de la aplicación local, estarán disponibles en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="6f9b9-142">La clave con la que se crea la subclave debe coincidir con el método de publicación que usó para el paquete.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="6f9b9-143">Por ejemplo, si ha publicado el paquete para el usuario, debe crear la subclave en <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="6f9b9-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="6f9b9-144">Establezca el valor de la nueva subclave del registro en el PackageId y la VersionId del paquete, separando los valores con un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="6f9b9-145">**Sintaxis**: &lt; PackageId &gt; \ _ &lt; VersionId&gt;</span><span class="sxs-lookup"><span data-stu-id="6f9b9-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="6f9b9-146">**Ejemplo**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="6f9b9-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="6f9b9-147">La aplicación del ejemplo anterior produciría un archivo de exportación del registro (archivo. reg) como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="6f9b9-148">Cmdlet Get-AppvClientPackage de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9b9-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="6f9b9-149">Puede usar el cmdlet **Start-AppVVirtualProcess** para recuperar el nombre del paquete y, a continuación, iniciar un proceso dentro del entorno virtual del paquete especificado.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="6f9b9-150">Este método te permite iniciar cualquier comando en el contexto de un paquete de App-V, independientemente de si el paquete se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="6f9b9-151">Use la siguiente sintaxis de ejemplo y sustituya el nombre del paquete por el \*\* &lt; paquete &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="6f9b9-152">Si no conoce el nombre exacto de su paquete, puede usar la línea de comandos **Get-AppvClientPackage \ \* executable\\** <em> , donde \*\*Executable </em> \* es el nombre de la aplicación, por ejemplo: get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="6f9b9-153">/Appvpid de modificador de la línea de comandos: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="6f9b9-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="6f9b9-154">Puede aplicar el modificador **/appvpid &lt; : &gt; PID** a cualquier comando, lo que permite que ese comando se ejecute dentro de un proceso virtual que se selecciona especificando su identificador de proceso (PID).</span><span class="sxs-lookup"><span data-stu-id="6f9b9-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="6f9b9-155">Con este método, se inicia el nuevo archivo ejecutable en el mismo entorno de App-V como un ejecutable que ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="6f9b9-156">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="6f9b9-157">Para encontrar el identificador de proceso (PID) del proceso de App-V, ejecute el comando **tasklist.exe** desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="6f9b9-158">Modificador de enlace de la línea de comandos/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="6f9b9-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="6f9b9-159">Este modificador le permite ejecutar un comando local dentro del entorno virtual de un paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="6f9b9-160">A diferencia del modificador **/appvid** , donde el entorno virtual ya debe estar ejecutándose, este modificador le permite iniciar el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="6f9b9-161">Sintáctica</span><span class="sxs-lookup"><span data-stu-id="6f9b9-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="6f9b9-162">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="6f9b9-163">Para obtener el GUID del paquete y el GUID de versión de la aplicación, ejecute el cmdlet **Get-AppvClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="6f9b9-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="6f9b9-164">Concatene el modificador **/appvve** con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6f9b9-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="6f9b9-165">Dos puntos</span><span class="sxs-lookup"><span data-stu-id="6f9b9-165">A colon</span></span>

-   <span data-ttu-id="6f9b9-166">GUID de paquete del paquete deseado</span><span class="sxs-lookup"><span data-stu-id="6f9b9-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="6f9b9-167">Un carácter de subrayado</span><span class="sxs-lookup"><span data-stu-id="6f9b9-167">An underscore</span></span>

-   <span data-ttu-id="6f9b9-168">IDENTIFICADOR de la versión del paquete deseado</span><span class="sxs-lookup"><span data-stu-id="6f9b9-168">Version ID of the desired package</span></span>

<span data-ttu-id="6f9b9-169">Si no conoce el nombre exacto de su paquete, use la línea de comandos **Get-AppvClientPackage \ \* executable\\** <em> , donde \*\*Executable </em> \* es el nombre de la aplicación, por ejemplo: get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="6f9b9-170">Este método te permite iniciar cualquier comando en el contexto de un paquete de App-V, independientemente de si el paquete se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6f9b9-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="6f9b9-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f9b9-171">Related topics</span></span>


[<span data-ttu-id="6f9b9-172">Referencia técnica de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="6f9b9-172">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)

 

 





