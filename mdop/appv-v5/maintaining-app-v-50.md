---
title: Mantenimiento de App-V 5.0
description: Mantenimiento de App-V 5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813615"
---
# <span data-ttu-id="02b8c-103">Mantenimiento de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="02b8c-103">Maintaining App-V 5.0</span></span>


<span data-ttu-id="02b8c-104">Después de completar todos los planes necesarios y después la implementación de la 5,0 de App-V, puede usar la siguiente información para mantener la infraestructura de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="02b8c-104">After you have completed all the necessary planning, and then deployment of App-V 5.0, you can use the following information to maintain the App-V 5.0 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-0-server-"></a><span data-ttu-id="02b8c-105">Mover el servidor de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="02b8c-105">Move the App-V 5.0 Server</span></span>


<span data-ttu-id="02b8c-106">El servidor de App-V 5,0 se conecta a la base de datos de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="02b8c-106">The App-V 5.0 server connects to the App-V 5.0 database.</span></span> <span data-ttu-id="02b8c-107">Por lo tanto, puede instalar el componente de administración en cualquier equipo de la red y, a continuación, conectarlo a la base de datos de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="02b8c-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.0 database.</span></span>

[<span data-ttu-id="02b8c-108">Cómo mover el servidor de App-V a otro equipo</span><span class="sxs-lookup"><span data-stu-id="02b8c-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a><span data-ttu-id="02b8c-109">Determinar si una aplicación de App-V 5,0 se está ejecutando virtualizada</span><span class="sxs-lookup"><span data-stu-id="02b8c-109">Determine if an App-V 5.0 Application is Running Virtualized</span></span>


<span data-ttu-id="02b8c-110">Los proveedores de software independientes (ISV) que deseen determinar si una aplicación se ejecuta virtualizada con App-V 5,0 o una versión posterior, deben abrir un objeto con nombre denominado \*\*AppVVirtual- &lt; PID &gt; \*\* en el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02b8c-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.0 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="02b8c-111">Por ejemplo, la API de Windows **GetCurrentProcessId ()** se puede usar para obtener el identificador del proceso actual, por ejemplo 4052, y, después, si un objeto de evento con nombre denominado **AppVVirtual-4052** se puede abrir correctamente con **OpenEvent ()** en el espacio de nombres predeterminado para acceso de lectura, entonces la aplicación es virtual.</span><span class="sxs-lookup"><span data-stu-id="02b8c-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="02b8c-112">Si la llamada a **OpenEvent ()** falla, la aplicación no es virtual.</span><span class="sxs-lookup"><span data-stu-id="02b8c-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="02b8c-113">Además, los ISV que deseen virtualizar explícitamente o no las llamadas en API específicas con App-V 5,0 y versiones posteriores pueden usar las funciones **VirtualizeCurrentThread ()** y **CurrentThreadIsVirtualized ()** implementadas en el módulo AppEntSubsystems32.dll.</span><span class="sxs-lookup"><span data-stu-id="02b8c-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.0 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="02b8c-114">Proporcionan una forma de hacer sugerencias en un componente descendente que la llamada debe o no se debe virtualizar.</span><span class="sxs-lookup"><span data-stu-id="02b8c-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="02b8c-115">Otros recursos para mantener la aplicación-V 5,0</span><span class="sxs-lookup"><span data-stu-id="02b8c-115">Other resources for maintaining App-V 5.0</span></span>


[<span data-ttu-id="02b8c-116">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="02b8c-116">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





