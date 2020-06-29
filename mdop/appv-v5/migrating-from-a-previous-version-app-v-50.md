---
title: Migrar desde una versión anterior
description: Migrar desde una versión anterior
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813558"
---
# <span data-ttu-id="767b6-103">Migrar desde una versión anterior</span><span class="sxs-lookup"><span data-stu-id="767b6-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="767b6-104">Con App-V 5,0 puede migrar la infraestructura de App-V 4,6 existente a la infraestructura más flexible, integrada y de administración de App-V 5,0 más sencilla.</span><span class="sxs-lookup"><span data-stu-id="767b6-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="767b6-105">Considere las siguientes secciones al planear la estrategia de migración:</span><span class="sxs-lookup"><span data-stu-id="767b6-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="767b6-106">**Nota:**  Para obtener más información sobre las diferencias entre App-V 4,6 y App-V 5,0, consulte las **diferencias entre App-v 4,6 y la sección App-v 5,0** de [acerca de App-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="767b6-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="767b6-107">Conversión de paquetes creados con una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="767b6-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="767b6-108">Use la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales creados con versiones anteriores de App-V.</span><span class="sxs-lookup"><span data-stu-id="767b6-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="767b6-109">El convertidor de paquetes usa PowerShell para convertir paquetes y puede ayudar a automatizar el proceso si tiene muchos paquetes que requieren conversión.</span><span class="sxs-lookup"><span data-stu-id="767b6-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="767b6-110">**Importante**  Después de convertir un paquete existente, debe probar el paquete antes de implementar el paquete para asegurarse de que el proceso de conversión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="767b6-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="767b6-111">Qué debe saber antes de convertir paquetes existentes</span><span class="sxs-lookup"><span data-stu-id="767b6-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="767b6-112">Problema</span><span class="sxs-lookup"><span data-stu-id="767b6-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="767b6-113">Solución alternativa</span><span class="sxs-lookup"><span data-stu-id="767b6-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-114">Los scripts de paquetes no se convierten.</span><span class="sxs-lookup"><span data-stu-id="767b6-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="767b6-115">Pruebe el paquete convertido.</span><span class="sxs-lookup"><span data-stu-id="767b6-115">Test the converted package.</span></span> <span data-ttu-id="767b6-116">Si es necesario, convierta el script.</span><span class="sxs-lookup"><span data-stu-id="767b6-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="767b6-117">Las invalidaciones de configuración del registro de paquetes no se convierten.</span><span class="sxs-lookup"><span data-stu-id="767b6-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="767b6-118">Pruebe el paquete convertido.</span><span class="sxs-lookup"><span data-stu-id="767b6-118">Test the converted package.</span></span> <span data-ttu-id="767b6-119">Si es necesario, vuelva a agregar las invalidaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="767b6-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-120">Los paquetes virtuales que usan DSC no se vinculan después de la conversión.</span><span class="sxs-lookup"><span data-stu-id="767b6-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="767b6-121">Vincule los paquetes usando grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="767b6-121">Link the packages using connection groups.</span></span> <span data-ttu-id="767b6-122">Consulte <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> Administración de grupos de conexión </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="767b6-123">Los conflictos de variables de entorno se detectan durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="767b6-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="767b6-124">Resuelva los conflictos en el <strong> archivo. OSD asociado </strong> .</span><span class="sxs-lookup"><span data-stu-id="767b6-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-125">Las rutas de código no modificables se detectan durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="767b6-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="767b6-126">Las rutas de código no modificables son difíciles de convertir correctamente.</span><span class="sxs-lookup"><span data-stu-id="767b6-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="767b6-127">El convertidor de paquetes detectará y devolverá paquetes con archivos que contienen rutas de código no modificables.</span><span class="sxs-lookup"><span data-stu-id="767b6-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="767b6-128">Visualice el archivo con la ruta de acceso del código y determine si el paquete necesita el archivo.</span><span class="sxs-lookup"><span data-stu-id="767b6-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="767b6-129">En ese caso, se recomienda volver a crear el paquete.</span><span class="sxs-lookup"><span data-stu-id="767b6-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="767b6-130">Al convertir un paquete, comprobar si hay errores en los archivos o en los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="767b6-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="767b6-131">Busque el elemento en el paquete de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="767b6-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="767b6-132">Es posible que se deba a una ruta de acceso no modificable.</span><span class="sxs-lookup"><span data-stu-id="767b6-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="767b6-133">Convertir la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="767b6-133">Convert the path.</span></span>

<span data-ttu-id="767b6-134">**Nota:**  Se recomienda usar el secuenciador App-V 5,0 para convertir aplicaciones críticas o aplicaciones que necesiten aprovechar las características.</span><span class="sxs-lookup"><span data-stu-id="767b6-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="767b6-135">Vea [Cómo secuenciar una nueva aplicación con App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="767b6-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="767b6-136">Si un paquete convertido no se abre después de convertirlo, también se recomienda que vuelva a realizar la secuencia de la aplicación con el secuenciador de aplicaciones-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="767b6-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="767b6-137">Cómo convertir un paquete creado en una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="767b6-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="767b6-138">Migrar clientes</span><span class="sxs-lookup"><span data-stu-id="767b6-138">Migrating Clients</span></span>


<span data-ttu-id="767b6-139">En la tabla siguiente se muestra el método recomendado para actualizar clientes.</span><span class="sxs-lookup"><span data-stu-id="767b6-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="767b6-140">Tarea</span><span class="sxs-lookup"><span data-stu-id="767b6-140">Task</span></span></th>
<th align="left"><span data-ttu-id="767b6-141">Más información</span><span class="sxs-lookup"><span data-stu-id="767b6-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-142">Actualizar el entorno a App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="767b6-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="767b6-143">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="767b6-144">Instale el cliente de App-V 5,0 con la coexistencia habilitada.</span><span class="sxs-lookup"><span data-stu-id="767b6-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="767b6-145">Cómo implementar el cliente de App-V 4,6 y App-V 5,0 en el mismo equipo </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-146">Secuencia y lanzamiento de paquetes de aplicaciones-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="767b6-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="767b6-147">Según sea necesario, vuelva a publicar los paquetes de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="767b6-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="767b6-148">Cómo secuencia una nueva aplicación con App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="767b6-149">**Importante**  Para poder usar el modo de coexistencia, debe estar ejecutando App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="767b6-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="767b6-150">Además, al secuenciar un paquete, debe configurar la configuración de la autoridad de administración, que se encuentra en la **configuración del usuario** , en la sección **configuración de usuario** .</span><span class="sxs-lookup"><span data-stu-id="767b6-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="767b6-151">Migrar la infraestructura completa de App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="767b6-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="767b6-152">No hay ningún método directo para actualizar a una infraestructura completa de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="767b6-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="767b6-153">Use la información de la siguiente sección para obtener información sobre cómo actualizar el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="767b6-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="767b6-154">Tarea</span><span class="sxs-lookup"><span data-stu-id="767b6-154">Task</span></span></th>
<th align="left"><span data-ttu-id="767b6-155">Más información</span><span class="sxs-lookup"><span data-stu-id="767b6-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-156">Actualice su entorno a App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="767b6-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="767b6-157">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="767b6-158">Implemente la versión de App-V 5,0 del cliente.</span><span class="sxs-lookup"><span data-stu-id="767b6-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="767b6-159">Cómo implementar el cliente de App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="767b6-160">Instale App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="767b6-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="767b6-161">Cómo implementar el servidor de App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="767b6-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="767b6-162">Migrar paquetes existentes.</span><span class="sxs-lookup"><span data-stu-id="767b6-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="767b6-163">Consulte la <strong> sección convertir paquetes creados con una versión anterior de App-V </strong> de este artículo.</span><span class="sxs-lookup"><span data-stu-id="767b6-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="767b6-164">Tareas adicionales de migración</span><span class="sxs-lookup"><span data-stu-id="767b6-164">Additional Migration tasks</span></span>


<span data-ttu-id="767b6-165">También puede realizar tareas adicionales de migración, como cambiar la configuración de los extremos, así como abrir un paquete creado con una versión anterior en un equipo que ejecute el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="767b6-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="767b6-166">Los vínculos siguientes proporcionan más información sobre cómo realizar estas tareas.</span><span class="sxs-lookup"><span data-stu-id="767b6-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="767b6-167">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="767b6-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="767b6-168">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.0 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="767b6-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="767b6-169">Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="767b6-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="767b6-170">Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="767b6-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="767b6-171">Otros recursos para realizar tareas de migración de App-V</span><span class="sxs-lookup"><span data-stu-id="767b6-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="767b6-172">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="767b6-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="767b6-173">Un procedimiento simplificado para la actualización del servidor de administración de Microsoft App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="767b6-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





