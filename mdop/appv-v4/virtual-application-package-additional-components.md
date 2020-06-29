---
title: Componentes adicionales de paquete de aplicaciones virtuales
description: Componentes adicionales de paquete de aplicaciones virtuales
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815080"
---
# <span data-ttu-id="33260-103">Componentes adicionales de paquete de aplicaciones virtuales</span><span class="sxs-lookup"><span data-stu-id="33260-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="33260-104">El secuenciador de App-V ha detectado un directorio que contiene los ejecutables de 64 bits y 32 bits, o los archivos de biblioteca de vínculos dinámicos (. dll) que dependen del mismo ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="33260-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="33260-105">Normalmente, el secuenciador crea ensamblados simultáneos privados para todos los ensamblados públicos que usa el paquete; sin embargo, no es posible crear versiones de 32 y 64 bits de los ensamblados privados en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="33260-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="33260-106">Si el secuenciador detecta un único conflicto, realizará las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="33260-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="33260-107">Quite todos los ensamblados privados de 64 bits existentes en todo el paquete, si el directorio tiene un conflicto o no.</span><span class="sxs-lookup"><span data-stu-id="33260-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="33260-108">Cree solo las versiones de 32 bits de los ensamblados en paralelo privados.</span><span class="sxs-lookup"><span data-stu-id="33260-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="33260-109">Debe instalar de forma nativa las versiones públicas de todos los ensamblados de 64 bits necesarios en el equipo que ejecuta el secuenciador y en todos los equipos cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="33260-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="33260-110">Para encontrar los ensamblados públicos existentes necesarios, abra el directorio en el que está guardado el paquete y búsquelo en la carpeta **VFS** .</span><span class="sxs-lookup"><span data-stu-id="33260-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="33260-111">Por ejemplo, si la raíz del paquete es **Q:\\MyApp**, cuando ordene la aplicación, busque en **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** y busque todos los ensamblados públicos existentes.</span><span class="sxs-lookup"><span data-stu-id="33260-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="33260-112">Las versiones de 64 bits de estos archivos siempre comenzarán con el texto siguiente al principio del nombre del manifiesto: **AMD64...**.</span><span class="sxs-lookup"><span data-stu-id="33260-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="33260-113">El nombre exacto y la versión del ensamblado pueden encontrarse en el archivo de manifiesto asociado.</span><span class="sxs-lookup"><span data-stu-id="33260-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="33260-114">Use cualquiera de los siguientes vínculos para descargar e instalar la versión correcta de los requisitos previos necesarios:</span><span class="sxs-lookup"><span data-stu-id="33260-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="33260-115">Paquete redistribuible de Microsoft Visual C++ 2005 (x64)</span><span class="sxs-lookup"><span data-stu-id="33260-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="33260-116">Paquete redistribuible de Microsoft Visual C++ 2005 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="33260-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="33260-117">Paquete redistribuible de Microsoft Visual C++ 2008 (x64)</span><span class="sxs-lookup"><span data-stu-id="33260-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="33260-118">Paquete redistribuible de Microsoft Visual C++ 2008 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="33260-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





