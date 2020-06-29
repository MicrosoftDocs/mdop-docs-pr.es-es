---
title: Referencia de comandos de SFTMIME
description: Referencia de comandos de SFTMIME
author: dansimp
ms.assetid: a4a69228-9dd3-4623-b773-899d03c0cf10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47aac9110febaf3f349461d74fef840326b1c6e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815350"
---
# <span data-ttu-id="341f3-103">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="341f3-103">SFTMIME Command Reference</span></span>


<span data-ttu-id="341f3-104">SFTMIME es una interfaz de línea de comandos usada por Application Virtualization (App-V) que le permite administrar muchos detalles de configuración de clientes.</span><span class="sxs-lookup"><span data-stu-id="341f3-104">SFTMIME is a command-line interface used by Application Virtualization (App-V) that enables you to manage many client configuration details.</span></span> <span data-ttu-id="341f3-105">Esta sección contiene todos los comandos y sus parámetros, con una breve descripción de cada uno.</span><span class="sxs-lookup"><span data-stu-id="341f3-105">This section contains all the commands and their parameters, with a brief description of each.</span></span>

**<span data-ttu-id="341f3-106">Importante</span><span class="sxs-lookup"><span data-stu-id="341f3-106">Important</span></span>**  
-   <span data-ttu-id="341f3-107">Todas las barras diagonales inversas deben estar con una barra diagonal inversa anterior, o bien, la ruta de acceso no se analizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="341f3-107">All backslash characters must be escaped using a preceding backslash, or the path will not be parsed correctly.</span></span>

-   <span data-ttu-id="341f3-108">Si está usando un programa de llamada para invocar SFTMIME con **CreateProcess**, debe asegurarse de que el primer parámetro es la ruta de acceso a sftmime.exe.</span><span class="sxs-lookup"><span data-stu-id="341f3-108">If you are using a calling program to invoke SFTMIME with **CreateProcess**, you must ensure that the first parameter is the path to sftmime.exe.</span></span>

-   <span data-ttu-id="341f3-109">El resultado del comando OBJ de la **consulta** SFTMIME no se puede canalizar al comando **Findstr** para buscar una cadena.</span><span class="sxs-lookup"><span data-stu-id="341f3-109">The output of the SFTMIME **QUERY OBJ** command cannot be piped to the **findstr** command to search for a string.</span></span>

-   <span data-ttu-id="341f3-110">El uso del modificador **global** requiere derechos de administrador local.</span><span class="sxs-lookup"><span data-stu-id="341f3-110">Use of the **GLOBAL** switch requires local administrator rights.</span></span>

-   <span data-ttu-id="341f3-111">El uso de rutas de rutas cortas y relativas puede provocar resultados inesperados y debe evitarse.</span><span class="sxs-lookup"><span data-stu-id="341f3-111">Use of short paths and relative paths can lead to unexpected results and should be avoided.</span></span> <span data-ttu-id="341f3-112">Usar siempre rutas completas.</span><span class="sxs-lookup"><span data-stu-id="341f3-112">Always use full paths.</span></span>

 

## <span data-ttu-id="341f3-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="341f3-113">In This Section</span></span>


[<span data-ttu-id="341f3-114">ADD APP</span><span class="sxs-lookup"><span data-stu-id="341f3-114">ADD APP</span></span>](add-app.md)

[<span data-ttu-id="341f3-115">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-115">ADD PACKAGE</span></span>](add-package.md)

[<span data-ttu-id="341f3-116">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="341f3-116">ADD SERVER</span></span>](add-server.md)

[<span data-ttu-id="341f3-117">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="341f3-117">ADD TYPE</span></span>](add-type.md)

[<span data-ttu-id="341f3-118">CLEAR APP</span><span class="sxs-lookup"><span data-stu-id="341f3-118">CLEAR APP</span></span>](clear-app.md)

[<span data-ttu-id="341f3-119">CLEAR OBJ</span><span class="sxs-lookup"><span data-stu-id="341f3-119">CLEAR OBJ</span></span>](clear-obj.md)

[<span data-ttu-id="341f3-120">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="341f3-120">CONFIGURE APP</span></span>](configure-app.md)

[<span data-ttu-id="341f3-121">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-121">CONFIGURE PACKAGE</span></span>](configure-package.md)

[<span data-ttu-id="341f3-122">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="341f3-122">CONFIGURE SERVER</span></span>](configure-server.md)

[<span data-ttu-id="341f3-123">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="341f3-123">CONFIGURE TYPE</span></span>](configure-type.md)

[<span data-ttu-id="341f3-124">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="341f3-124">DELETE APP</span></span>](delete-app.md)

[<span data-ttu-id="341f3-125">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="341f3-125">DELETE OBJ</span></span>](delete-obj.md)

[<span data-ttu-id="341f3-126">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-126">DELETE PACKAGE</span></span>](delete-package.md)

[<span data-ttu-id="341f3-127">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="341f3-127">DELETE SERVER</span></span>](delete-server.md)

[<span data-ttu-id="341f3-128">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="341f3-128">DELETE TYPE</span></span>](delete-type.md)

[<span data-ttu-id="341f3-129">HELP</span><span class="sxs-lookup"><span data-stu-id="341f3-129">HELP</span></span>](help.md)

[<span data-ttu-id="341f3-130">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="341f3-130">LOAD APP</span></span>](load-app.md)

[<span data-ttu-id="341f3-131">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-131">LOAD PACKAGE</span></span>](load-package.md)

[<span data-ttu-id="341f3-132">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="341f3-132">LOCK APP</span></span>](lock-app.md)

[<span data-ttu-id="341f3-133">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="341f3-133">PUBLISH APP</span></span>](publish-app.md)

[<span data-ttu-id="341f3-134">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-134">PUBLISH PACKAGE</span></span>](publish-package.md)

[<span data-ttu-id="341f3-135">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="341f3-135">QUERY OBJ</span></span>](query-obj.md)

[<span data-ttu-id="341f3-136">REFRESH SERVER</span><span class="sxs-lookup"><span data-stu-id="341f3-136">REFRESH SERVER</span></span>](refresh-server.md)

[<span data-ttu-id="341f3-137">REPAIR APP</span><span class="sxs-lookup"><span data-stu-id="341f3-137">REPAIR APP</span></span>](repair-app.md)

[<span data-ttu-id="341f3-138">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="341f3-138">UNLOAD APP</span></span>](unload-app.md)

[<span data-ttu-id="341f3-139">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-139">UNLOAD PACKAGE</span></span>](unload-package.md)

[<span data-ttu-id="341f3-140">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="341f3-140">UNLOCK APP</span></span>](unlock-app.md)

[<span data-ttu-id="341f3-141">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="341f3-141">UNPUBLISH PACKAGE</span></span>](unpublish-package.md)

 

 





