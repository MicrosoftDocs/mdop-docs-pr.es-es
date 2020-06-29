---
title: Acerca de las aplicaciones de virtualización de aplicaciones
description: Acerca de las aplicaciones de virtualización de aplicaciones
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820090"
---
# <span data-ttu-id="8409c-103">Acerca de las aplicaciones de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8409c-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="8409c-104">En la virtualización de aplicaciones, una *aplicación* es un programa ejecutable, como Microsoft Visio, que se transmite al cliente o cliente de escritorio de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server) desde un servidor de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8409c-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="8409c-105">Antes de que se pueda transmitir una aplicación a un cliente, la aplicación debe estar preparada para la transmisión por secuencias al procesarla con el secuenciador de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="8409c-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="8409c-106">Administración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8409c-106">Managing Applications</span></span>


<span data-ttu-id="8409c-107">Para que los usuarios puedan disponer de las aplicaciones, debe agregar las aplicaciones al sistema.</span><span class="sxs-lookup"><span data-stu-id="8409c-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="8409c-108">El método más común para agregar aplicaciones al sistema es importarlas.</span><span class="sxs-lookup"><span data-stu-id="8409c-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="8409c-109">Para obtener acceso a esta característica, haga clic con el botón derecho en el nodo **aplicaciones** en la consola de administración del servidor de virtualización de aplicaciones y elija **importar aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="8409c-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="8409c-110">Puede importar más de un archivo descriptor de software abierto (OSD) al mismo tiempo o importar un archivo SPRJ (SPRJ) que pueda contener varios archivos OSD.</span><span class="sxs-lookup"><span data-stu-id="8409c-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="8409c-111">Esta funcionalidad le permite configurar aplicaciones relacionadas de forma similar.</span><span class="sxs-lookup"><span data-stu-id="8409c-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="8409c-112">También puede usar las siguientes características para ayudarle a administrar sus aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="8409c-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="8409c-113">**Grupos de aplicaciones**: le permite crear grupos lógicos de aplicaciones para simplificar la administración.</span><span class="sxs-lookup"><span data-stu-id="8409c-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="8409c-114">Cuando se realizan cambios en un grupo (por ejemplo, permisos de acceso), los cambios se aplican a todas las aplicaciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="8409c-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="8409c-115">Las aplicaciones de un grupo pueden provenir de diferentes paquetes.</span><span class="sxs-lookup"><span data-stu-id="8409c-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="8409c-116">**Selección múltiple**: permite seleccionar varias aplicaciones al mismo tiempo manteniendo presionada la tecla Ctrl al hacer clic en una aplicación para modificar las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8409c-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="8409c-117">Sin embargo, si desea mantener una relación entre las aplicaciones, debe crear un grupo de aplicaciones para que contenga las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8409c-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="8409c-118">**Copia entre sistemas**: le permite copiar aplicaciones de un entorno a otro entorno que ejecute la misma versión de App-V en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="8409c-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="8409c-119">Por ejemplo, es posible que tenga un entorno de prueba de aceptación de usuario en el que inicialmente implemente y configure las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8409c-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="8409c-120">Después de finalizar la fase de prueba, es posible que desee replicar el mismo conjunto de aplicaciones (incluidos los permisos) en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="8409c-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="8409c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8409c-121">Related topics</span></span>


[<span data-ttu-id="8409c-122">Acerca de los paquetes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8409c-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="8409c-123">Acerca de la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8409c-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="8409c-124">Cómo administrar grupos de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="8409c-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="8409c-125">Cómo administrar aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="8409c-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





