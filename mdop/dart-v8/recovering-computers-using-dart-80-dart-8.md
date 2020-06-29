---
title: Equipos de recuperación que usan DaRT 8.0
description: Equipos de recuperación que usan DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824870"
---
# <span data-ttu-id="655be-103">Equipos de recuperación que usan DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="655be-103">Recovering Computers Using DaRT 8.0</span></span>


<span data-ttu-id="655be-104">Después de implementar la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, puede usar DaRT 8,0 para recuperar equipos.</span><span class="sxs-lookup"><span data-stu-id="655be-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can use DaRT 8.0 to recover computers.</span></span> <span data-ttu-id="655be-105">En la información de esta sección se describen las tareas de recuperación que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="655be-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="655be-106">Puede elegir entre varios métodos diferentes para iniciar en DaRT, en función de cómo implemente la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="655be-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="655be-107">Inserte un CD, DVD o una unidad flash USB de la imagen de recuperación de DaRT en el equipo problemático y utilícelo para arrancar en el equipo.</span><span class="sxs-lookup"><span data-stu-id="655be-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="655be-108">Inicie DaRT desde una partición de recuperación en el equipo con problemas.</span><span class="sxs-lookup"><span data-stu-id="655be-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="655be-109">Inicie en DaRT desde una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="655be-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="655be-110">Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="655be-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="655be-111">Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="655be-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="655be-112">**Nota:**  La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.</span><span class="sxs-lookup"><span data-stu-id="655be-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="655be-113">Recuperar un equipo local con la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="655be-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="655be-114">Para recuperar un equipo local con DaRT, debe estar físicamente presente en el equipo del usuario final que está experimentando problemas que requieren DaRT.</span><span class="sxs-lookup"><span data-stu-id="655be-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="655be-115">Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="655be-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="655be-116">Recuperar un equipo remoto con la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="655be-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="655be-117">La característica de conexión remota de DaRT permite que un administrador de TI ejecute las herramientas de DaRT de manera remota en un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="655be-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="655be-118">Una vez que el usuario final proporcione cierta información (o un profesional del Departamento de soporte técnico trabajando en el equipo del usuario final), el administrador de ti o el trabajador del Departamento de soporte puede tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.</span><span class="sxs-lookup"><span data-stu-id="655be-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="655be-119">**Importante**  Los dos equipos que establecen una conexión remota deben formar parte de la misma red.</span><span class="sxs-lookup"><span data-stu-id="655be-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="655be-120">La ventana del **conjunto de herramientas de diagnóstico y recuperación** incluye la opción de ejecutar DART en un equipo del usuario final de forma remota desde un equipo de administrador.</span><span class="sxs-lookup"><span data-stu-id="655be-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="655be-121">El usuario final abre las herramientas de DaRT en el equipo problemático e inicia la sesión remota haciendo clic en **conexión remota**.</span><span class="sxs-lookup"><span data-stu-id="655be-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="655be-122">La característica de conexión remota en el equipo del usuario final crea la siguiente información de conexión: un número de vale, un puerto y una lista de todas las direcciones IP disponibles.</span><span class="sxs-lookup"><span data-stu-id="655be-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="655be-123">El número y el puerto del vale se generan de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="655be-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="655be-124">El administrador de ti o el trabajador del Departamento de soporte introduce esta información en el **visor de conexión remota de DART** para establecer la conexión de servicios de Terminal Server con el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="655be-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="655be-125">La conexión de servicios de Terminal Server que se establece permite que un administrador de ti interactúe de forma remota con las herramientas de DaRT en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="655be-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="655be-126">Después, el equipo del usuario final procesa la información de conexión, comparte su pantalla y responde a las instrucciones del PC administrador de ti.</span><span class="sxs-lookup"><span data-stu-id="655be-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="655be-127">Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="655be-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="655be-128">Otros recursos para recuperar equipos con DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="655be-128">Other resources for recovering computers using DaRT 8.0</span></span>


[<span data-ttu-id="655be-129">Operaciones para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="655be-129">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





