---
title: Administración de grupos de conexión
description: Administración de grupos de conexión
author: dansimp
ms.assetid: 1a9c8f26-f421-4b70-b7e2-da8118e8198c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2e57b9dbe56072e6049e8fabef5705c374d022c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813582"
---
# <span data-ttu-id="0295f-103">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="0295f-103">Managing Connection Groups</span></span>


<span data-ttu-id="0295f-104">Los grupos de conexión permiten que las aplicaciones de un paquete interactúen entre sí en el entorno virtual, mientras que permanecen aisladas del resto del sistema.</span><span class="sxs-lookup"><span data-stu-id="0295f-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="0295f-105">Mediante los grupos de conexión, los administradores pueden administrar paquetes de forma independiente y evitar tener que agregar la misma aplicación varias veces a un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="0295f-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="0295f-106">**Nota:**  En versiones anteriores de App-V 5,0, los grupos de conexión se denominaban composición de conjunto dinámico.</span><span class="sxs-lookup"><span data-stu-id="0295f-106">**Note** In previous versions of App-V 5.0, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="0295f-107">En este tema:</span><span class="sxs-lookup"><span data-stu-id="0295f-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md)"><span data-ttu-id="0295f-108">Información acerca del entorno virtual del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="0295f-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0295f-109">Describe el entorno virtual de grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="0295f-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file.md)"><span data-ttu-id="0295f-110">Información acerca del archivo del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="0295f-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0295f-111">Describe el archivo de grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="0295f-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group.md)"><span data-ttu-id="0295f-112">Cómo crear un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="0295f-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0295f-113">Explica cómo crear un nuevo grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="0295f-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="0295f-114">Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente</span><span class="sxs-lookup"><span data-stu-id="0295f-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0295f-115">Explica cómo crear un nuevo grupo de conexiones que contenga una combinación de paquetes que se publiquen para el usuario y que se publiquen globalmente.</span><span class="sxs-lookup"><span data-stu-id="0295f-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group.md)"><span data-ttu-id="0295f-116">Cómo eliminar un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="0295f-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0295f-117">Explica cómo eliminar un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="0295f-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group.md)"><span data-ttu-id="0295f-118">Cómo publicar un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="0295f-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0295f-119">Explica cómo publicar un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="0295f-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="0295f-120">Otros recursos para los grupos de conexión de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0295f-120">Other resources for App-V 5.0 connection groups</span></span>


-   [<span data-ttu-id="0295f-121">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0295f-121">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





