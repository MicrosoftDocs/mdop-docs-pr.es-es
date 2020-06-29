---
title: Información acerca del archivo del grupo de conexión
description: Información acerca del archivo del grupo de conexión
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814927"
---
# <span data-ttu-id="ab5be-103">Información acerca del archivo del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-103">About the Connection Group File</span></span>


**<span data-ttu-id="ab5be-104">En este tema:</span><span class="sxs-lookup"><span data-stu-id="ab5be-104">In this topic:</span></span>**

-   [<span data-ttu-id="ab5be-105">Ubicación y propósito del archivo de grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="ab5be-106">Estructura del archivo XML del grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="ab5be-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="ab5be-107">Configuración de la prioridad de paquetes en un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="ab5be-108">Configuraciones de conexión de aplicaciones virtuales compatibles</span><span class="sxs-lookup"><span data-stu-id="ab5be-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="ab5be-109">Ubicación y propósito del archivo de grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-110">Propósito de grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-111">Un grupo de conexión es una característica de App-V que le permite agrupar paquetes para crear un entorno virtual en el que las aplicaciones de esos paquetes puedan interactuar entre sí.</span><span class="sxs-lookup"><span data-stu-id="ab5be-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="ab5be-112">Ejemplo: desea usar complementos con Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="ab5be-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="ab5be-113">Puede crear un paquete que contenga los complementos, crear otro paquete que contenga Office y, a continuación, agregar ambos paquetes a un grupo de conexión para que Office pueda usar esos complementos.</span><span class="sxs-lookup"><span data-stu-id="ab5be-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab5be-114">Cómo funciona el archivo de grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-115">Cuando se aplica un archivo de grupo de conexión de App-V 5,1, los paquetes que se enumeran en el archivo se combinan en tiempo de ejecución en un solo entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="ab5be-115">When you apply an App-V 5.1 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="ab5be-116">Use el archivo de grupo de conexión de Microsoft Application Virtualization (App-V) 5,1 para configurar grupos de conexión existentes de la versión 5,1 de App-V.</span><span class="sxs-lookup"><span data-stu-id="ab5be-116">Use the Microsoft Application Virtualization (App-V) 5.1 connection group file to configure existing App-V 5.1 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-117">Ejemplo de ruta de archivo</span><span class="sxs-lookup"><span data-stu-id="ab5be-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="ab5be-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="ab5be-119">Estructura del archivo XML del grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="ab5be-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="ab5be-120">En esta sección:</span><span class="sxs-lookup"><span data-stu-id="ab5be-120">In this section:</span></span>**

-   [<span data-ttu-id="ab5be-121">Parámetros que definen el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="ab5be-122">Parámetros que definen los paquetes en el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="ab5be-123">Archivo XML de grupo de conexión de ejemplo de App-V</span><span class="sxs-lookup"><span data-stu-id="ab5be-123">App-V example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="ab5be-124">Archivo XML de grupo de conexión de aplicación-V 5,0 a través de App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="ab5be-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="ab5be-125">Parámetros que definen el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-125">Parameters that define the connection group</span></span>

<span data-ttu-id="ab5be-126">En la siguiente tabla se describen los parámetros del archivo XML que definen el grupo de conexiones en sí, no los paquetes.</span><span class="sxs-lookup"><span data-stu-id="ab5be-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab5be-127">Campo</span><span class="sxs-lookup"><span data-stu-id="ab5be-127">Field</span></span></th>
<th align="left"><span data-ttu-id="ab5be-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab5be-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-129">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="ab5be-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-130">Nombre del esquema.</span><span class="sxs-lookup"><span data-stu-id="ab5be-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="ab5be-131">Aplicable a partir de App-V 5,0 SP3 </strong> : Si desea usar las nuevas características "paquetes opcionales" y "usar cualquier versión" que se describen en esta tabla, debe especificar el siguiente esquema en el archivo XML:</span><span class="sxs-lookup"><span data-stu-id="ab5be-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab5be-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="ab5be-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-133">Identificador GUID único para este grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ab5be-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="ab5be-134">El estado del grupo de conexiones está asociado con este identificador.</span><span class="sxs-lookup"><span data-stu-id="ab5be-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="ab5be-135">Especifique este identificador solo cuando cree el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="ab5be-136">Puede crear un nuevo GUID escribiendo: <strong>[Guid]::NewGuid()</strong> .</span><span class="sxs-lookup"><span data-stu-id="ab5be-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-137">VersionId</span><span class="sxs-lookup"><span data-stu-id="ab5be-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-138">Identificador GUID de versión de esta versión del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ab5be-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="ab5be-139">Cuando actualice un grupo de conexión (por ejemplo, agregando o actualizando un paquete nuevo), debe actualizar el GUID de versión para que refleje la nueva versión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab5be-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ab5be-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-141">Nombre para mostrar del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ab5be-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-142">Prioridad</span><span class="sxs-lookup"><span data-stu-id="ab5be-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-143">Campo de prioridad opcional para el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="ab5be-144">"0" </strong> - indica la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="ab5be-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="ab5be-145">Si se requiere una prioridad, pero no se ha configurado, el paquete fallará porque no se puede determinar el grupo de conexión correcto.</span><span class="sxs-lookup"><span data-stu-id="ab5be-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="ab5be-146">Parámetros que definen los paquetes en el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="ab5be-147">En la &lt; sección Packages &gt; del archivo XML del grupo de conexión, enumere los paquetes miembro del grupo de conexión especificando el identificador de paquete único de cada paquete y el identificador de versión, tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab5be-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="ab5be-148">El primer paquete de la lista tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="ab5be-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab5be-149">Campo</span><span class="sxs-lookup"><span data-stu-id="ab5be-149">Field</span></span></th>
<th align="left"><span data-ttu-id="ab5be-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab5be-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-151">PackageId</span><span class="sxs-lookup"><span data-stu-id="ab5be-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-152">Identificador GUID único para este paquete.</span><span class="sxs-lookup"><span data-stu-id="ab5be-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="ab5be-153">Este GUID no cambia cuando se publican versiones más recientes del paquete.</span><span class="sxs-lookup"><span data-stu-id="ab5be-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab5be-154">VersionId</span><span class="sxs-lookup"><span data-stu-id="ab5be-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-155">Identificador GUID único de la versión del paquete.</span><span class="sxs-lookup"><span data-stu-id="ab5be-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="ab5be-156">Aplicable a partir de App-V 5,0 SP3 </strong> : Si especifica <strong> "\*" </strong> para la versión del paquete, se insertará dinámicamente el GUID de la última versión del paquete disponible.</span><span class="sxs-lookup"><span data-stu-id="ab5be-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-157">IsOptional</span><span class="sxs-lookup"><span data-stu-id="ab5be-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="ab5be-158">Aplicable a partir de App-V 5,0 SP3 </strong> : parámetro que le permite hacer un paquete opcional dentro del grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ab5be-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="ab5be-159">Las entradas válidas son:</span><span class="sxs-lookup"><span data-stu-id="ab5be-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="ab5be-160">"true" </strong> : el paquete es opcional en el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="ab5be-161">"falso" </strong> : el paquete es obligatorio en el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="ab5be-162">Consulte <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> Cómo usar paquetes opcionales en grupos de conexión </a> .</span><span class="sxs-lookup"><span data-stu-id="ab5be-162">See <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="ab5be-163">Archivo XML de grupo de conexión de ejemplo de App-V</span><span class="sxs-lookup"><span data-stu-id="ab5be-163">App-V example connection group XML file</span></span>

<span data-ttu-id="ab5be-164">En el siguiente ejemplo de archivo XML de grupo de conexiones se muestran ejemplos de los campos de las tablas anteriores y se resaltan los elementos que son nuevos desde App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="ab5be-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new starting in App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="ab5be-165">Archivo XML de grupo de conexión de aplicación-V 5,0 a través de App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="ab5be-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="ab5be-166">El siguiente ejemplo de archivo XML de grupo de conexión se aplica a App-V 5,0 mediante App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="ab5be-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="ab5be-167">Muestra ejemplos de los campos de la tabla anterior, pero excluye los cambios descritos anteriormente para App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="ab5be-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="ab5be-168">Configuración de la prioridad de paquetes en un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="ab5be-169">La prioridad del paquete se configura con el orden de la lista de paquetes.</span><span class="sxs-lookup"><span data-stu-id="ab5be-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="ab5be-170">El primer paquete del documento tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="ab5be-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="ab5be-171">Los paquetes siguientes de la lista tienen prioridad descendente.</span><span class="sxs-lookup"><span data-stu-id="ab5be-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="ab5be-172">Prioridad de los paquetes es la resolución de conflictos de recursos, por lo demás, inevitables durante la inicialización del entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="ab5be-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="ab5be-173">Por ejemplo, si dos paquetes que se abren en el mismo entorno virtual definen el mismo valor DWORD del registro, el paquete con la prioridad más alta determina el valor que se establece.</span><span class="sxs-lookup"><span data-stu-id="ab5be-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="ab5be-174">Puede usar el archivo de grupo de conexión para configurar cada grupo de conexiones con los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab5be-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="ab5be-175">Especificar prioridades en tiempo de ejecución para grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-175">Specify runtime priorities for connection groups.</span></span> <span data-ttu-id="ab5be-176">Para editar la prioridad mediante la consola de administración de App-V, haga clic en el grupo de conexiones y, a continuación, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ab5be-176">To edit priority by using the App-V Management Console, click the connection group and then click **Edit**.</span></span>

    <span data-ttu-id="ab5be-177">**Nota:**  La prioridad solo es necesaria si el paquete está asociado a más de un grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-177">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="ab5be-178">Especifique la prioridad de los paquetes en el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-178">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="ab5be-179">El campo Priority es obligatorio cuando una aplicación virtual en ejecución se inicia desde una solicitud de aplicación nativa, por ejemplo, el explorador de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ab5be-179">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="ab5be-180">El cliente de App-V usa la prioridad para determinar qué entorno virtual de grupo de conexiones debe ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab5be-180">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="ab5be-181">Esta situación se produce si una aplicación virtual forma parte de varios grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-181">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="ab5be-182">Si se abre una aplicación virtual con otra aplicación virtual, se usará el entorno virtual de la aplicación virtual original.</span><span class="sxs-lookup"><span data-stu-id="ab5be-182">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="ab5be-183">El campo Priority no se usa en este caso.</span><span class="sxs-lookup"><span data-stu-id="ab5be-183">The priority field is not used in this case.</span></span>

**<span data-ttu-id="ab5be-184">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ab5be-184">Example:</span></span>**

<span data-ttu-id="ab5be-185">La aplicación virtual Microsoft Outlook se está ejecutando en el entorno virtual **XYZ**.</span><span class="sxs-lookup"><span data-stu-id="ab5be-185">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="ab5be-186">Al abrir un documento de Microsoft Word adjunto, se abrirá una versión virtualizada de Microsoft Word en el entorno virtual **XYZ**, independientemente de los grupos de conexiones o las prioridades de tiempo de ejecución asociados con Microsoft Word virtualizado.</span><span class="sxs-lookup"><span data-stu-id="ab5be-186">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="ab5be-187">Configuraciones de conexión de aplicaciones virtuales compatibles</span><span class="sxs-lookup"><span data-stu-id="ab5be-187">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab5be-188">Configuración</span><span class="sxs-lookup"><span data-stu-id="ab5be-188">Configuration</span></span></th>
<th align="left"><span data-ttu-id="ab5be-189">Escenario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab5be-189">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-190">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab5be-190">An.</span></span> <span data-ttu-id="ab5be-191">archivo exe y complemento (. dll)</span><span class="sxs-lookup"><span data-stu-id="ab5be-191">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ab5be-192">Desea distribuir Microsoft Office a todos los usuarios, pero distribuir un complemento de Microsoft Excel solo a un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="ab5be-192">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="ab5be-193">Habilitar el grupo de conexión para los usuarios adecuados.</span><span class="sxs-lookup"><span data-stu-id="ab5be-193">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="ab5be-194">Actualice cada paquete individualmente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ab5be-194">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab5be-195">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab5be-195">An.</span></span> <span data-ttu-id="ab5be-196">exe y una aplicación de middleware</span><span class="sxs-lookup"><span data-stu-id="ab5be-196">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ab5be-197">Tiene una aplicación que requiere una aplicación de middleware o varias aplicaciones que dependen de la misma versión de tiempo de ejecución de middleware.</span><span class="sxs-lookup"><span data-stu-id="ab5be-197">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="ab5be-198">Todos los equipos que requieren una o más de las aplicaciones reciben los grupos de conexión con la aplicación y el motor en tiempo de ejecución de aplicaciones middleware.</span><span class="sxs-lookup"><span data-stu-id="ab5be-198">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="ab5be-199">De manera opcional, puede combinar varias aplicaciones middleware en un único grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ab5be-199">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab5be-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab5be-200">Example</span></span></th>
<th align="left"><span data-ttu-id="ab5be-201">Descripción del ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab5be-201">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-202">Grupo de conexión de aplicación virtual para la división financiera</span><span class="sxs-lookup"><span data-stu-id="ab5be-202">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ab5be-203">Aplicación de middleware 1</span><span class="sxs-lookup"><span data-stu-id="ab5be-203">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="ab5be-204">Aplicación de middleware 2</span><span class="sxs-lookup"><span data-stu-id="ab5be-204">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="ab5be-205">Aplicación de middleware 3</span><span class="sxs-lookup"><span data-stu-id="ab5be-205">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="ab5be-206">Tiempo de ejecución de aplicaciones middleware</span><span class="sxs-lookup"><span data-stu-id="ab5be-206">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab5be-207">Grupo de conexión de aplicación virtual para división de RRHH</span><span class="sxs-lookup"><span data-stu-id="ab5be-207">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ab5be-208">Aplicación de middleware 5</span><span class="sxs-lookup"><span data-stu-id="ab5be-208">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="ab5be-209">Aplicación de middleware 6</span><span class="sxs-lookup"><span data-stu-id="ab5be-209">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="ab5be-210">Tiempo de ejecución de aplicaciones middleware</span><span class="sxs-lookup"><span data-stu-id="ab5be-210">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab5be-211">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab5be-211">An.</span></span> <span data-ttu-id="ab5be-212">exe y un archivo. exe</span><span class="sxs-lookup"><span data-stu-id="ab5be-212">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab5be-213">Tiene una aplicación que se basa en otra aplicación y desea mantener los paquetes separados en cuanto a eficacia operativa, restricciones de licencias o escalas de tiempo de implementación.</span><span class="sxs-lookup"><span data-stu-id="ab5be-213">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="ab5be-214">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ab5be-214">Example:</span></span></strong></p>
<p><span data-ttu-id="ab5be-215">Si va a implementar Microsoft Lync 2010, puede usar tres paquetes:</span><span class="sxs-lookup"><span data-stu-id="ab5be-215">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="ab5be-216">Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="ab5be-216">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="ab5be-217">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="ab5be-217">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="ab5be-218">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="ab5be-218">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="ab5be-219">Puede administrar la implementación con los siguientes grupos de conexión:</span><span class="sxs-lookup"><span data-stu-id="ab5be-219">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="ab5be-220">Microsoft Office2010 y Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="ab5be-220">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="ab5be-221">Microsoft Office2010 y Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="ab5be-221">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="ab5be-222">Una vez completada la implementación, puede crear un nuevo paquete de Microsoft Office2010 + Microsoft Lync2010, o bien, conservarlos y mantenerlos como paquetes independientes e implementarlos con un grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="ab5be-222">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="ab5be-223">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab5be-223">Related topics</span></span>


[<span data-ttu-id="ab5be-224">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="ab5be-224">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





