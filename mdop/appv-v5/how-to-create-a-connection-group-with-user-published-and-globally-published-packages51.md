---
title: Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente
description: Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente
author: dansimp
ms.assetid: 851b8742-0283-4aa6-b3a3-f7f6289824c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 230e687360920c05a214624750eba54dc84b5731
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814366"
---
# <span data-ttu-id="23ac8-103">Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente</span><span class="sxs-lookup"><span data-stu-id="23ac8-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>


<span data-ttu-id="23ac8-104">Puede crear grupos de conexión con el usuario titulado que contengan paquetes publicados por el usuario y de forma global, mediante uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="23ac8-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="23ac8-105">Cómo usar los cmdlets de PowerShell para crear grupos de conexión con el título del usuario</span><span class="sxs-lookup"><span data-stu-id="23ac8-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="23ac8-106">Cómo usar el servidor de App-V para crear grupos de conexión con el titular del usuario</span><span class="sxs-lookup"><span data-stu-id="23ac8-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="23ac8-107">Qué debe saber antes de empezar:</span><span class="sxs-lookup"><span data-stu-id="23ac8-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="23ac8-108">Escenarios no compatibles y posibles problemas</span><span class="sxs-lookup"><span data-stu-id="23ac8-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="23ac8-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="23ac8-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23ac8-110">No puede incluir paquetes publicados por el usuario en grupos de conexión con derecho global.</span><span class="sxs-lookup"><span data-stu-id="23ac8-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="23ac8-111">Se producirá un error en el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="23ac8-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23ac8-112">Si publica un paquete globalmente y, a continuación, crea un grupo de conexión publicado por el usuario en el que lo ha hecho no es opcional, aún puede ejecutar <strong> la anulación de publicación: &lt; paquete AppvClientPackage &gt; -global </strong> para anular la publicación del paquete, incluso cuando ese paquete se está usando en otro grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="23ac8-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="23ac8-113">Si cualquier otro grupo de conexión está usando ese paquete, el paquete no se ejecutará en esos grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="23ac8-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="23ac8-114">Para evitar la eliminación inadvertida de la publicación de un paquete no opcional que se está usando en otro grupo de conexión, le recomendamos que realice un seguimiento de los grupos de conexión en los que ha usado un paquete no opcional.</span><span class="sxs-lookup"><span data-stu-id="23ac8-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="23ac8-115">Cómo usar los cmdlets de PowerShell para crear grupos de conexión titulados por el usuario</span><span class="sxs-lookup"><span data-stu-id="23ac8-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="23ac8-116">Agregue y publique paquetes con los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="23ac8-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="23ac8-117">Add-AppvClientPackage package1 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="23ac8-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="23ac8-118">Add-AppvClientPackage package2 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="23ac8-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="23ac8-119">Publish-AppvClientPackage-PackageId package1 \ _ID-VersionId package1 \ _Version ID: global</span><span class="sxs-lookup"><span data-stu-id="23ac8-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="23ac8-120">Publish-AppvClientPackage-PackageId package2 \ _ID-VersionIdPackage2 \ _ID</span><span class="sxs-lookup"><span data-stu-id="23ac8-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="23ac8-121">Cree el archivo XML del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="23ac8-121">Create the connection group XML file.</span></span> <span data-ttu-id="23ac8-122">Para obtener más información, consulte [acerca del archivo de grupo de conexión](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="23ac8-122">For more information, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

3.  <span data-ttu-id="23ac8-123">Agregue y publique el grupo de conexión con los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="23ac8-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="23ac8-124">Add-AppvClientConnectionGroup conexión \ _Group \ _XML \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="23ac8-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="23ac8-125">Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="23ac8-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="23ac8-126">Cómo usar el servidor de App-V para crear grupos de conexión titulados por el usuario</span><span class="sxs-lookup"><span data-stu-id="23ac8-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="23ac8-127">Abra la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="23ac8-127">Open the App-V 5.1 Management Console.</span></span>

2.  <span data-ttu-id="23ac8-128">Siga las instrucciones que encontrará en [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-51.md) para publicar paquetes de forma global y para el usuario.</span><span class="sxs-lookup"><span data-stu-id="23ac8-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="23ac8-129">Siga las instrucciones que encontrará en [Cómo crear un grupo de conexiones](how-to-create-a-connection-group51.md) para crear el grupo de conexiones y agregue los paquetes publicados por el usuario y los que se hayan publicado de forma global.</span><span class="sxs-lookup"><span data-stu-id="23ac8-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group51.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="23ac8-130">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="23ac8-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="23ac8-131">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="23ac8-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="23ac8-132">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="23ac8-132">Got an App-V issue?</span></span>** <span data-ttu-id="23ac8-133">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="23ac8-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="23ac8-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23ac8-134">Related topics</span></span>


[<span data-ttu-id="23ac8-135">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="23ac8-135">Managing Connection Groups</span></span>](managing-connection-groups51.md)

[<span data-ttu-id="23ac8-136">Cómo usar los paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="23ac8-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups51.md)

 

 





