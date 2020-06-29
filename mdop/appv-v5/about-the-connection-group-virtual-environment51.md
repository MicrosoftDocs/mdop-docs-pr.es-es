---
title: Información acerca del entorno virtual del grupo de conexión
description: Información acerca del entorno virtual del grupo de conexión
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814886"
---
# <span data-ttu-id="0bdd8-103">Información acerca del entorno virtual del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="0bdd8-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="0bdd8-104">En este tema:</span><span class="sxs-lookup"><span data-stu-id="0bdd8-104">In this topic:</span></span>**

-   [<span data-ttu-id="0bdd8-105">Cómo se determina la prioridad del paquete</span><span class="sxs-lookup"><span data-stu-id="0bdd8-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="0bdd8-106">Combinación de rutas de paquetes idénticas en un directorio virtual de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="0bdd8-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="0bdd8-107">Cómo se determina la prioridad del paquete</span><span class="sxs-lookup"><span data-stu-id="0bdd8-107">How package priority is determined</span></span>


<span data-ttu-id="0bdd8-108">El entorno virtual y su estado actual están asociados con el grupo de conexión, no con los paquetes individuales.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="0bdd8-109">Si se quita un paquete de App-V del grupo de conexiones, el estado que existía como parte del grupo de conexión no se migrará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="0bdd8-110">Si el mismo paquete forma parte de dos grupos de conexión diferentes, debe indicar qué aplicación de grupo de conexión debe usar.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="0bdd8-111">Por ejemplo, es posible que tenga dos paquetes en un grupo de conexión para que cada uno de ellos defina el mismo valor DWORD del registro.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="0bdd8-112">El grupo de conexión que se usa se basa en el orden en que un paquete aparece dentro del documento XML **AppConnectionGroup** :</span><span class="sxs-lookup"><span data-stu-id="0bdd8-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="0bdd8-113">El primer paquete tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="0bdd8-114">El segundo paquete tiene la segunda prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="0bdd8-115">Considere la siguiente sección de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0bdd8-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="0bdd8-116">Supongamos que el mismo valor DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) se define en el primer y tercer paquete, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0bdd8-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="0bdd8-117">Paquete 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="0bdd8-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="0bdd8-118">Paquete 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="0bdd8-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="0bdd8-119">Como el paquete 1 aparece primero, el entorno virtual de AppConnectionGroup tendrá el valor DWORD único de 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5).</span><span class="sxs-lookup"><span data-stu-id="0bdd8-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="0bdd8-120">Esto significa que las aplicaciones virtuales del paquete 1, package 2 y Package 3 verán el valor 5 cuando hacen una consulta para HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="0bdd8-121">Otros recursos de entorno virtual se resuelven de forma similar, pero el caso habitual es que las colisiones se producen en el registro.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="0bdd8-122">Combinación de rutas de paquetes idénticas en un directorio virtual de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="0bdd8-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="0bdd8-123">Si dos o más paquetes de un grupo de conexiones contienen rutas de directorio idénticas, las rutas se combinan en un único directorio virtual dentro del entorno virtual del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="0bdd8-124">Esta combinación de rutas permite que una aplicación de un paquete tenga acceso a los archivos de un paquete diferente.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="0bdd8-125">Al quitar un paquete de un grupo de conexiones, las aplicaciones de ese paquete eliminado ya no podrán obtener acceso a los archivos del grupo de conexiones que quede en los demás paquetes.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="0bdd8-126">El orden en el que App-V busca el nombre de un archivo en el grupo de conexión se especifica mediante el orden en el que se muestran los paquetes de App-V en el archivo de manifiesto del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="0bdd8-127">En el ejemplo siguiente se muestra el orden y la relación de una búsqueda de nombres de archivo en un grupo de conexión para el **paquete a** y el **paquete B**.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0bdd8-128">Empaquetar una</span><span class="sxs-lookup"><span data-stu-id="0bdd8-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="0bdd8-129">Paquete B</span><span class="sxs-lookup"><span data-stu-id="0bdd8-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0bdd8-130">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="0bdd8-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="0bdd8-131">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="0bdd8-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0bdd8-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="0bdd8-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="0bdd8-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="0bdd8-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0bdd8-134">En el ejemplo anterior, cuando una aplicación virtualizada intenta encontrar un archivo específico, se busca en primer lugar una ruta de acceso de archivo coincidente.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="0bdd8-135">Si no se encuentra una ruta de acceso coincidente, se busca en el paquete B con las siguientes reglas de asignación:</span><span class="sxs-lookup"><span data-stu-id="0bdd8-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="0bdd8-136">Si hay un archivo denominado **test.txt** en la misma jerarquía de carpetas virtuales de ambos paquetes de la aplicación, se usa el primero.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="0bdd8-137">Si un archivo denominado **bar.txt** existe en la jerarquía de carpetas virtuales de un paquete de la aplicación, pero no en el otro, se usa el primer archivo coincidente.</span><span class="sxs-lookup"><span data-stu-id="0bdd8-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="0bdd8-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bdd8-138">Related topics</span></span>


[<span data-ttu-id="0bdd8-139">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="0bdd8-139">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





