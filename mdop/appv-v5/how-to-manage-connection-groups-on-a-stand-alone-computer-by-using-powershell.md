---
title: Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell
description: Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell
author: dansimp
ms.assetid: b73ae74d-8a6f-4bb3-b1f2-0067c7bd5212
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 32dd4f9c5ad1ba4ae9e25246d5ec52a6363ef303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813926"
---
# <span data-ttu-id="97c18-103">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c18-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="97c18-104">Un grupo de conexión de App-V le permite ejecutar todas las aplicaciones virtuales como un conjunto definido de paquetes en un único entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="97c18-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="97c18-105">Por ejemplo, puede virtualizar una aplicación y sus complementos con paquetes independientes, pero puede ejecutarlos juntos en un solo grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="97c18-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="97c18-106">Un archivo XML de grupo de conexiones define el grupo de conexiones que se ejecuta en el equipo donde haya instalado el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="97c18-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="97c18-107">Para obtener información sobre el archivo XML del grupo de conexiones y sobre cómo configurarlo, consulte [acerca del archivo de grupo de conexión](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="97c18-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

<span data-ttu-id="97c18-108">En este tema, se explican los procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="97c18-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="97c18-109">Para agregar y publicar paquetes de App-V en el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="97c18-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="97c18-110">Para agregar y habilitar el grupo de conexión en el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="97c18-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="97c18-111">Para habilitar o deshabilitar un grupo de conexiones para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="97c18-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="97c18-112">Para permitir que solo los administradores puedan habilitar grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="97c18-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>**<span data-ttu-id="97c18-113">Para agregar y publicar paquetes de App-V en el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="97c18-113">To add and publish the App-V packages in the connection group</span></span>**

1.  <span data-ttu-id="97c18-114">Para agregar y publicar los paquetes de App-V 5,0 en el equipo que ejecuta el cliente de App-V, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="97c18-114">To add and publish the App-V 5.0 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="97c18-115">Add-AppvClientPackage – path c:\\tmpstore\\quartfin.appv | Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="97c18-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="97c18-116">Repita el **paso 1** de este procedimiento para cada paquete del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="97c18-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="97c18-117">Para agregar y habilitar el grupo de conexión en el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="97c18-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="97c18-118">Agregue el grupo de conexiones escribiendo el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="97c18-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="97c18-119">Add-AppvClientConnectionGroup – path c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="97c18-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="97c18-120">Para habilitar el grupo de conexión, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="97c18-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="97c18-121">Enable-AppvClientConnectionGroup – name "aplicaciones financieras"</span><span class="sxs-lookup"><span data-stu-id="97c18-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="97c18-122">Cuando se ejecutan en el equipo de destino cualquier aplicación virtual que se encuentre en los paquetes miembro, se ejecutarán dentro del entorno virtual del grupo de conexión y estarán disponibles para todas las aplicaciones virtuales de los demás paquetes del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="97c18-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="97c18-123">Para habilitar o deshabilitar un grupo de conexiones para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="97c18-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="97c18-124">Revise la descripción y los requisitos del parámetro:</span><span class="sxs-lookup"><span data-stu-id="97c18-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="97c18-125">El parámetro habilita a un administrador para habilitar o deshabilitar un grupo de conexiones para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="97c18-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="97c18-126">Debe usar el paquete de Hotfix 5 de App-V 5,0 SP2 o posterior para usar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="97c18-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="97c18-127">Puede ejecutar este cmdlet desde la sesión de usuario o de administrador.</span><span class="sxs-lookup"><span data-stu-id="97c18-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="97c18-128">Para usar el parámetro, debe haber iniciado sesión con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="97c18-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="97c18-129">El usuario final debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="97c18-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="97c18-130">Debe proporcionar el identificador de seguridad (SID) del usuario final.</span><span class="sxs-lookup"><span data-stu-id="97c18-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="97c18-131">Use los siguientes cmdlets y agregue el parámetro opcional **– UserSid** , donde **-UserSID** representa el identificador de seguridad (SID) del usuario final:</span><span class="sxs-lookup"><span data-stu-id="97c18-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="97c18-132">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97c18-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="97c18-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="97c18-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="97c18-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="97c18-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="97c18-135">Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="97c18-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="97c18-136">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="97c18-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="97c18-137">Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="97c18-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="97c18-138">Para permitir que solo los administradores puedan habilitar grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="97c18-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="97c18-139">Revise la descripción y el requisito para usar este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="97c18-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="97c18-140">Use este cmdlet y el parámetro para configurar el cliente de App-V para permitir que solo los administradores (no usuarios finales) puedan habilitar o deshabilitar grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="97c18-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="97c18-141">Debe usar al menos App-V 5,0 SP3 para usar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c18-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="97c18-142">Ejecute el siguiente cmdlet y parámetro:</span><span class="sxs-lookup"><span data-stu-id="97c18-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="97c18-143">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97c18-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="97c18-144">Parámetro y valores</span><span class="sxs-lookup"><span data-stu-id="97c18-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="97c18-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97c18-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="97c18-146">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c18-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="97c18-147">–RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="97c18-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="97c18-148">0-falso</span><span class="sxs-lookup"><span data-stu-id="97c18-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="97c18-149">1-verdadero</span><span class="sxs-lookup"><span data-stu-id="97c18-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="97c18-150">Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="97c18-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="97c18-151">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="97c18-151">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="97c18-152">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="97c18-152">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="97c18-153">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="97c18-153">Got an App-V issue?</span></span>** <span data-ttu-id="97c18-154">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="97c18-154">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="97c18-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97c18-155">Related topics</span></span>


[<span data-ttu-id="97c18-156">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="97c18-156">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="97c18-157">Administración de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c18-157">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





