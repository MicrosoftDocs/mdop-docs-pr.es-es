---
title: Cómo hacer que un grupo de conexión ignore la versión del paquete
description: Cómo hacer que un grupo de conexión ignore la versión del paquete
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813959"
---
# <span data-ttu-id="b23d5-103">Cómo hacer que un grupo de conexión ignore la versión del paquete</span><span class="sxs-lookup"><span data-stu-id="b23d5-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="b23d5-104">Microsoft Application Virtualization (App-V) 5,0 SP3 le permite configurar un grupo de conexiones para usar cualquier versión de un paquete, lo que simplifica las actualizaciones de los paquetes y reduce el número de grupos de conexión que necesita crear.</span><span class="sxs-lookup"><span data-stu-id="b23d5-104">Microsoft Application Virtualization (App-V) 5.0 SP3 enables you to configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="b23d5-105">Para actualizar un paquete en versiones anteriores de App-V, tenía que realizar varios pasos, como deshabilitar el grupo de conexión y modificar el archivo de definición XML del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="b23d5-105">To upgrade a package in earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b23d5-106">Descripción de la tarea con App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="b23d5-106">Task description with App-V 5.0 SP3</span></span></th>
<th align="left"><span data-ttu-id="b23d5-107">Cómo realizar la tarea con App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="b23d5-107">How to perform the task with App-V 5.0 SP3</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b23d5-108">Puede configurar un grupo de conexiones para que acepte cualquier versión de un paquete, lo que le permite actualizar el paquete sin tener que deshabilitar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="b23d5-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="b23d5-109">Cómo funciona la característica:</span><span class="sxs-lookup"><span data-stu-id="b23d5-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="b23d5-110">Si el grupo de conexión tiene acceso a varias versiones de un paquete, se usa la última versión.</span><span class="sxs-lookup"><span data-stu-id="b23d5-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="b23d5-111">Si el grupo de conexiones contiene un paquete opcional con una versión incorrecta, el paquete se pasa por alto y no bloqueará la creación del entorno virtual del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="b23d5-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="b23d5-112">Si el grupo de conexiones contiene un paquete no opcional con una versión incorrecta, no se puede crear el entorno virtual del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="b23d5-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b23d5-113">Método</span><span class="sxs-lookup"><span data-stu-id="b23d5-113">Method</span></span></th>
<th align="left"><span data-ttu-id="b23d5-114">Pasos</span><span class="sxs-lookup"><span data-stu-id="b23d5-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b23d5-115">Servidor de App-V: consola de administración</span><span class="sxs-lookup"><span data-stu-id="b23d5-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="b23d5-116">En la consola de administración, seleccione <strong> paquetes de conexión de paquetes </strong> &gt; <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="b23d5-116">In the Management Console, select <strong>PACKAGES</strong> &gt; <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b23d5-117">Seleccione el grupo de conexiones correcto en la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="b23d5-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="b23d5-118">Haga clic en <strong> Editar </strong> en el panel de paquetes conectados.</span><span class="sxs-lookup"><span data-stu-id="b23d5-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="b23d5-119">Seleccione <strong> usar cualquier versión </strong> junto al nombre del paquete y haga clic en <strong> aplicar </strong> .</span><span class="sxs-lookup"><span data-stu-id="b23d5-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="b23d5-120">Para obtener más información sobre cómo agregar o actualizar paquetes, consulte <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> Cómo agregar o actualizar paquetes mediante la consola de administración </a> .</span><span class="sxs-lookup"><span data-stu-id="b23d5-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b23d5-121">Cliente de App-V en un equipo independiente</span><span class="sxs-lookup"><span data-stu-id="b23d5-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="b23d5-122">Cree el documento XML del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="b23d5-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="b23d5-123">Para que se actualice el paquete, establezca el <strong> atributo VersionID de la etiqueta del paquete </strong> <strong> </strong> en un asterisco ( <strong>\*</strong> ).</span><span class="sxs-lookup"><span data-stu-id="b23d5-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="b23d5-124">Use el siguiente cmdlet para agregar el grupo de conexión e incluya la ruta de acceso al documento XML del grupo de conexiones:</span><span class="sxs-lookup"><span data-stu-id="b23d5-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="b23d5-125">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="b23d5-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="b23d5-126">Cuando actualice un paquete, use los siguientes cmdlets para quitar el paquete anterior, agregar el paquete actualizado y publicar el paquete actualizado:</span><span class="sxs-lookup"><span data-stu-id="b23d5-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="b23d5-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b23d5-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="b23d5-128">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b23d5-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="b23d5-129">Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b23d5-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="b23d5-130">Para más información, consulta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b23d5-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="b23d5-131">El archivo XML de ejemplo, <strong> archivo XML del grupo de conexiones con paquetes opcionales </strong> , en esta sección: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> Cómo usar paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="b23d5-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="b23d5-132">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="b23d5-132">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="b23d5-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b23d5-133">Related topics</span></span>


[<span data-ttu-id="b23d5-134">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="b23d5-134">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





