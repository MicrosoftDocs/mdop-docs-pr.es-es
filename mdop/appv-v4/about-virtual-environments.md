---
title: Acerca de entornos virtuales
description: Acerca de entornos virtuales
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822391"
---
# <span data-ttu-id="0637d-103">Acerca de entornos virtuales</span><span class="sxs-lookup"><span data-stu-id="0637d-103">About Virtual Environments</span></span>


<span data-ttu-id="0637d-104">Las aplicaciones virtuales se ejecutan en entornos virtuales.</span><span class="sxs-lookup"><span data-stu-id="0637d-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="0637d-105">Los entornos virtuales permiten que cada aplicación se ejecute en un servidor de escritorio, portátil o de host de sesión de escritorio remoto (host RDSession) sin necesidad de instalar ni alterar el sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="0637d-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="0637d-106">Cada aplicación lleva su propia información de configuración en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="0637d-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="0637d-107">Como resultado, muchas aplicaciones se ejecutan en paralelo con otras aplicaciones en el mismo equipo sin ningún conflicto.</span><span class="sxs-lookup"><span data-stu-id="0637d-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="0637d-108">Las aplicaciones virtuales se ejecutan de forma local, de modo que se ejecutan con el rendimiento completo, la funcionalidad y el acceso a los servicios locales que cabría esperar de cualquier aplicación instalada de forma local.</span><span class="sxs-lookup"><span data-stu-id="0637d-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="0637d-109">Dado que cada aplicación se ejecuta en un entorno virtual, se reducen los problemas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0637d-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="0637d-110">Conflictos de aplicaciones: en entornos que no usan la virtualización de aplicaciones, debe probar minuciosamente todas las aplicaciones para asegurarse de que no interfiera con otras aplicaciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="0637d-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="0637d-111">Pruebas de regresión: como la aplicación no cambia el sistema operativo subyacente, se eliminan las pruebas largas de regresión.</span><span class="sxs-lookup"><span data-stu-id="0637d-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="0637d-112">Incompatibilidad de versiones: diferentes versiones de la misma aplicación pueden ejecutarse simultáneamente en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="0637d-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="0637d-113">Acceso multiusuario: las aplicaciones que no se ejecutan en modo multiusuario y, por lo tanto, no pueden ejecutarse en un host RDSession, ahora pueden hacerlo y funcionar correctamente para varios usuarios en un único host RDSession.</span><span class="sxs-lookup"><span data-stu-id="0637d-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="0637d-114">Problemas de multiinquilino: dos instancias de la misma aplicación que usan distintas configuraciones se pueden ejecutar en el mismo equipo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0637d-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="0637d-115">Silos de servidores: se elimina la necesidad de tener muchos conjuntos de servidores independientes.</span><span class="sxs-lookup"><span data-stu-id="0637d-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="0637d-116">Los entornos virtuales incluyen un registro virtual para cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="0637d-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="0637d-117">Otras aplicaciones o utilidades como regedit no pueden ver la configuración del registro creada por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0637d-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="0637d-118">En lugar de copiar el registro completo, el registro virtual usa un método de *superposición* .</span><span class="sxs-lookup"><span data-stu-id="0637d-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="0637d-119">La aplicación puede leer los elementos en el registro del cliente siempre que una copia virtual de ese elemento del registro no esté incluida en el registro virtual.</span><span class="sxs-lookup"><span data-stu-id="0637d-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="0637d-120">Todas las escrituras de la aplicación en el registro están incluidas en el registro virtual.</span><span class="sxs-lookup"><span data-stu-id="0637d-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="0637d-121">Los entornos virtuales también incluyen un sistema de archivos virtual y otros componentes virtuales, incluidos los servicios virtuales y COM virtual.</span><span class="sxs-lookup"><span data-stu-id="0637d-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="0637d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0637d-122">Related topics</span></span>


[<span data-ttu-id="0637d-123">Introducción a la consola de administración de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0637d-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





