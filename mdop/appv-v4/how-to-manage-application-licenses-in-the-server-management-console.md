---
title: Cómo administrar licencias de aplicaciones en la consola de administración de servidor
description: Cómo administrar licencias de aplicaciones en la consola de administración de servidor
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817221"
---
# <span data-ttu-id="84035-103">Cómo administrar licencias de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="84035-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="84035-104">La consola de administración de Application Virtualization Server es la interfaz que se usa para administrar la plataforma de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="84035-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="84035-105">Puede Agregar, quitar, configurar y controlar los grupos de licencias de aplicación.</span><span class="sxs-lookup"><span data-stu-id="84035-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="84035-106">**Importante**  Si la configuración raíz de origen de la aplicación cliente de App-V (ASR) se ha configurado para usar cualquier tipo de origen de transmisión que no sea el servidor de administración, por ejemplo, un servidor de transmisión, un servidor IIS o un servidor de archivos, el servidor de administración no puede aplicar su Directiva de licencias.</span><span class="sxs-lookup"><span data-stu-id="84035-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="84035-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="84035-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="84035-108">Cómo crear un grupo de licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="84035-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="84035-109">Proporciona un procedimiento para crear una nueva aplicación en un grupo de licencias.</span><span class="sxs-lookup"><span data-stu-id="84035-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="84035-110">Cómo asociar una aplicación a un grupo de licencias</span><span class="sxs-lookup"><span data-stu-id="84035-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="84035-111">Proporciona un procedimiento para agregar una aplicación a un grupo de licencias.</span><span class="sxs-lookup"><span data-stu-id="84035-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="84035-112">Cómo quitar una aplicación de un grupo de licencias</span><span class="sxs-lookup"><span data-stu-id="84035-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="84035-113">Proporciona un procedimiento para quitar una aplicación de un grupo de licencias.</span><span class="sxs-lookup"><span data-stu-id="84035-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="84035-114">Cómo eliminar un grupo de licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="84035-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="84035-115">En esta sección se incluyen los pasos necesarios para eliminar un grupo de licencias de aplicación.</span><span class="sxs-lookup"><span data-stu-id="84035-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="84035-116">Cómo configurar un grupo de licencias ilimitado</span><span class="sxs-lookup"><span data-stu-id="84035-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="84035-117">Proporciona un procedimiento para crear un nuevo grupo de licencias ilimitadas, lo que permite que un número ilimitado de usuarios acceda a las aplicaciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="84035-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="84035-118">Cómo configurar un grupo de licencias simultáneas</span><span class="sxs-lookup"><span data-stu-id="84035-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="84035-119">Proporciona un procedimiento para crear un nuevo grupo de licencias simultáneas, lo que permite que un número específico de usuarios simultáneos tenga acceso a las aplicaciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="84035-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="84035-120">Cómo configurar un grupo de licencias designadas</span><span class="sxs-lookup"><span data-stu-id="84035-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="84035-121">Proporciona un procedimiento para crear un nuevo grupo de licencias ilimitadas, lo que permite que usuarios específicos tengan acceso a las aplicaciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="84035-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="84035-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84035-122">Related topics</span></span>


[<span data-ttu-id="84035-123">Cómo realizar tareas administrativas en la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="84035-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





