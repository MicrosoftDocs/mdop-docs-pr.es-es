---
title: Acerca del uso compartido de la página de aceleradores de paquetes
description: Acerca del uso compartido de la página de aceleradores de paquetes
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819991"
---
# <span data-ttu-id="526e9-103">Acerca del uso compartido de la página de aceleradores de paquetes</span><span class="sxs-lookup"><span data-stu-id="526e9-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="526e9-104">Esta información proporciona la información de procedimientos recomendados sobre cómo compartir aceleradores de paquetes.</span><span class="sxs-lookup"><span data-stu-id="526e9-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="526e9-105">Si planea compartir archivos de aceleradores de paquetes, es posible que la información, como los nombres de los equipos, la información de la cuenta de usuario y la información sobre las aplicaciones incluidas en las transformaciones, se incluyan en el archivo de aceleradores de paquetes.</span><span class="sxs-lookup"><span data-stu-id="526e9-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="526e9-106">Debe revisar cualquier configuración o archivos de configuración asociados con el paquete de aplicación virtual para asegurarse de que las aplicaciones no contienen información personal. Esta página contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="526e9-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="526e9-107">**Nombre de usuario**.</span><span class="sxs-lookup"><span data-stu-id="526e9-107">**Username**.</span></span> <span data-ttu-id="526e9-108">Al iniciar sesión en el equipo que ejecuta el secuenciador de Microsoft App-V, debe usar una cuenta de usuario genérica, como la cuenta de **Administrador** integrada.</span><span class="sxs-lookup"><span data-stu-id="526e9-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="526e9-109">No debe usar una cuenta basada en un nombre de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="526e9-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="526e9-110">**Nombre del equipo**.</span><span class="sxs-lookup"><span data-stu-id="526e9-110">**Computer Name**.</span></span> <span data-ttu-id="526e9-111">Especifique un nombre general, no Identificativo, del equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="526e9-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="526e9-112">**Dirección URL del servidor**.</span><span class="sxs-lookup"><span data-stu-id="526e9-112">**Server URL**.</span></span> <span data-ttu-id="526e9-113">En la consola del secuenciador de App-V, en la pestaña **implementación** , use la configuración predeterminada para la información de configuración de la dirección URL del servidor.</span><span class="sxs-lookup"><span data-stu-id="526e9-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="526e9-114">**Las aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="526e9-114">**Applications**.</span></span> <span data-ttu-id="526e9-115">Si no desea compartir la lista de aplicaciones que se instalaron en el equipo que ejecuta el secuenciador cuando creó el acelerador de paquetes, debe eliminar el archivo de **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="526e9-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="526e9-116">Este archivo se encuentra en el directorio raíz del paquete de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="526e9-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="526e9-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="526e9-117">Related topics</span></span>


[<span data-ttu-id="526e9-118">Crear asistente del acelerador de paquetes (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="526e9-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="526e9-119">Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="526e9-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





