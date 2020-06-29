---
title: Cómo administrar grupos de aplicaciones en la consola de administración de servidor
description: Cómo administrar grupos de aplicaciones en la consola de administración de servidor
author: dansimp
ms.assetid: 46997971-bdc8-4565-aefd-f47e90d6d7a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 59a357d93ea63cc728f59a0633b7a5b9953aad14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817201"
---
# <span data-ttu-id="55d04-103">Cómo administrar grupos de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="55d04-103">How to Manage Application Groups in the Server Management Console</span></span>


<span data-ttu-id="55d04-104">Puede mostrar y administrar una o más aplicaciones en grupos de aplicaciones en la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="55d04-104">You can display and manage one or more applications in application groups in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="55d04-105">Esto puede ser útil cuando desee hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55d04-105">This can be useful when you want to do the following:</span></span>

-   <span data-ttu-id="55d04-106">Organice muchas aplicaciones en subgrupos más manejables.</span><span class="sxs-lookup"><span data-stu-id="55d04-106">Organize many applications into more manageable subgroups.</span></span>

-   <span data-ttu-id="55d04-107">Crear grupos de aplicaciones específicas para un departamento u otra división de compañía.</span><span class="sxs-lookup"><span data-stu-id="55d04-107">Create groups of applications specific to a department or other company division.</span></span>

-   <span data-ttu-id="55d04-108">Agrupar tipos similares de aplicaciones, como software financiero.</span><span class="sxs-lookup"><span data-stu-id="55d04-108">Group similar types of applications, such as financial software.</span></span>

-   <span data-ttu-id="55d04-109">Simplificar los permisos de acceso o la administración de licencias por grupo.</span><span class="sxs-lookup"><span data-stu-id="55d04-109">Simplify access permissions or license management by group.</span></span>

-   <span data-ttu-id="55d04-110">Cambie las propiedades de las aplicaciones y los grupos de aplicaciones de un grupo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="55d04-110">Change the properties of applications and application groups within a group simultaneously.</span></span>

<span data-ttu-id="55d04-111">Puede crear un grupo, ubicarlo en el árbol de **aplicaciones** de la consola e importar aplicaciones al grupo.</span><span class="sxs-lookup"><span data-stu-id="55d04-111">You can create a group, place it where you would like in the console's **Applications** tree, and import applications to the group.</span></span> <span data-ttu-id="55d04-112">A continuación, puede configurar y administrar las propiedades del grupo para que afecten a todas sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="55d04-112">Then you can configure and manage the group's properties to affect all of its applications.</span></span> <span data-ttu-id="55d04-113">También puede mover aplicaciones entre grupos.</span><span class="sxs-lookup"><span data-stu-id="55d04-113">You can also move applications among groups.</span></span>

<span data-ttu-id="55d04-114">**Nota:**  El traslado de aplicaciones a grupos no afecta a la ubicación de sus archivos (SFT, OSD o SPRJ) en el sistema de archivos del servidor.</span><span class="sxs-lookup"><span data-stu-id="55d04-114">**Note** Moving applications into groups does not affect the locations of their files (SFT, OSD, or SPRJ) on the server's file system.</span></span>

 

## <span data-ttu-id="55d04-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="55d04-115">In This Section</span></span>


<a href="" id="how-to-create-an-application-group"></a>[<span data-ttu-id="55d04-116">Cómo crear un grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="55d04-116">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)  
<span data-ttu-id="55d04-117">Proporciona instrucciones paso a paso para crear un grupo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="55d04-117">Provides step-by-step instructions for creating an application group.</span></span>

<a href="" id="how-to-move-an-application-group"></a>[<span data-ttu-id="55d04-118">Cómo mover un grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="55d04-118">How to Move an Application Group</span></span>](how-to-move-an-application-group.md)  
<span data-ttu-id="55d04-119">Proporciona instrucciones paso a paso para mover un grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="55d04-119">Provides step-by-step instructions for moving an application group.</span></span>

<a href="" id="how-to-rename-an-application-group"></a>[<span data-ttu-id="55d04-120">Cómo cambiar el nombre de un grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="55d04-120">How to Rename an Application Group</span></span>](how-to-rename-an-application-group.md)  
<span data-ttu-id="55d04-121">Proporciona instrucciones paso a paso para cambiar el nombre de un grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="55d04-121">Provides step-by-step instructions for renaming an application group.</span></span>

<a href="" id="how-to-remove-an-application-group"></a>[<span data-ttu-id="55d04-122">Cómo eliminar un grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="55d04-122">How to Remove an Application Group</span></span>](how-to-remove-an-application-group.md)  
<span data-ttu-id="55d04-123">Proporciona instrucciones paso a paso para quitar o eliminar un grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="55d04-123">Provides step-by-step instructions for removing or deleting an application group.</span></span>

## <span data-ttu-id="55d04-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55d04-124">Related topics</span></span>


[<span data-ttu-id="55d04-125">Cómo administrar aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="55d04-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="55d04-126">Cómo realizar tareas administrativas en la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="55d04-126">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





