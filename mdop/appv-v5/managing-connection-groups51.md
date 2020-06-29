---
title: Administración de grupos de conexión
description: Administración de grupos de conexión
author: dansimp
ms.assetid: 22c9d3cb-7246-4173-9742-4ba1c24b0a6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c89fab70fa13a66c2c27b8d014a5bac034f21bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813574"
---
# <span data-ttu-id="52b13-103">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="52b13-103">Managing Connection Groups</span></span>


<span data-ttu-id="52b13-104">Los grupos de conexión permiten que las aplicaciones de un paquete interactúen entre sí en el entorno virtual, mientras que permanecen aisladas del resto del sistema.</span><span class="sxs-lookup"><span data-stu-id="52b13-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="52b13-105">Mediante los grupos de conexión, los administradores pueden administrar paquetes de forma independiente y evitar tener que agregar la misma aplicación varias veces a un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="52b13-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="52b13-106">**Nota:**  En algunas versiones anteriores de App-V, los grupos de conexión se denominaban composición de conjunto dinámico.</span><span class="sxs-lookup"><span data-stu-id="52b13-106">**Note** In some previous versions of App-V, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="52b13-107">En este tema:</span><span class="sxs-lookup"><span data-stu-id="52b13-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment51.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment51.md)"><span data-ttu-id="52b13-108">Información acerca del entorno virtual del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="52b13-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="52b13-109">Describe el entorno virtual de grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="52b13-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file51.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file51.md)"><span data-ttu-id="52b13-110">Información acerca del archivo del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="52b13-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="52b13-111">Describe el archivo de grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="52b13-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group51.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group51.md)"><span data-ttu-id="52b13-112">Cómo crear un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="52b13-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="52b13-113">Explica cómo crear un nuevo grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="52b13-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md)"><span data-ttu-id="52b13-114">Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente</span><span class="sxs-lookup"><span data-stu-id="52b13-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="52b13-115">Explica cómo crear un nuevo grupo de conexiones que contenga una combinación de paquetes que se publiquen para el usuario y que se publiquen globalmente.</span><span class="sxs-lookup"><span data-stu-id="52b13-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group51.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group51.md)"><span data-ttu-id="52b13-116">Cómo eliminar un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="52b13-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="52b13-117">Explica cómo eliminar un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="52b13-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group51.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group51.md)"><span data-ttu-id="52b13-118">Cómo publicar un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="52b13-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="52b13-119">Explica cómo publicar un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="52b13-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="52b13-120">Otros recursos para los grupos de conexión de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="52b13-120">Other resources for App-V 5.1 connection groups</span></span>


-   [<span data-ttu-id="52b13-121">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="52b13-121">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





