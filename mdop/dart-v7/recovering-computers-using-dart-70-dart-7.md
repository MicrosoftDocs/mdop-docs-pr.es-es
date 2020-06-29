---
title: Equipos de recuperación que usan DaRT 7.0
description: Equipos de recuperación que usan DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822770"
---
# <span data-ttu-id="fbd9a-103">Equipos de recuperación que usan DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="fbd9a-103">Recovering Computers Using DaRT 7.0</span></span>


<span data-ttu-id="fbd9a-104">Hay dos métodos disponibles para recuperar equipos con Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-104">There are two methods available to recover computers using Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="fbd9a-105">Puede ejecutar la imagen de recuperación de DaRT7 localmente o usar la característica de conexión remota disponible en DaRT7 para recuperar un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-105">You can either run the DaRT7 recovery image locally or use The Remote Connection feature available in DaRT7 to recover a remote computer.</span></span> <span data-ttu-id="fbd9a-106">Ambos métodos se describen más detalladamente en esta sección.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-106">Both methods are described in more detail in this section.</span></span>

## <span data-ttu-id="fbd9a-107">Recuperar equipos locales con la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="fbd9a-107">Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="fbd9a-108">Para recuperar un equipo local mediante DaRT7, debe estar presente físicamente en el equipo del usuario final que está experimentando problemas que requieren DaRT.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-108">To recover a local computer by using DaRT7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

<span data-ttu-id="fbd9a-109">Puede elegir entre varios métodos diferentes para iniciar en DaRT, en función de cómo implemente la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-109">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="fbd9a-110">Inserte un CD, DVD o una unidad flash USB de la imagen de recuperación de DaRT en el equipo problemático y utilícelo para arrancar en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-110">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="fbd9a-111">Inicie DaRT desde una partición de recuperación en el equipo con problemas.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-111">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="fbd9a-112">Inicie en DaRT desde una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-112">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="fbd9a-113">Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="fbd9a-113">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

<span data-ttu-id="fbd9a-114">Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-114">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="fbd9a-115">**Nota:**  La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-115">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

[<span data-ttu-id="fbd9a-116">Cómo recuperar los equipos locales con la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="fbd9a-116">How to Recover Local Computers Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="fbd9a-117">Recuperar equipos remotos con la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="fbd9a-117">Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="fbd9a-118">La característica de conexión remota de DaRT permite que un administrador de TI ejecute las herramientas de DaRT de manera remota en un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-118">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="fbd9a-119">Después de que el usuario final proporcione determinada información (o de un profesional del Departamento de soporte técnico que trabaje en el equipo del usuario final), el administrador de ti o el agente de asistencia pueden tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-119">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="fbd9a-120">**Importante**  Los dos equipos que establecen una conexión remota deben formar parte de la misma red.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-120">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="fbd9a-121">La ventana del **conjunto de herramientas de diagnóstico y recuperación** incluye la opción de ejecutar DART en un equipo del usuario final de forma remota desde un equipo de administrador.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-121">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="fbd9a-122">El usuario final abre las herramientas de DaRT en el equipo problemático e inicia la sesión remota haciendo clic en **conexión remota**.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-122">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="fbd9a-123">La característica de conexión remota en el equipo del usuario final crea la siguiente información de conexión: un número de vale, un puerto y una lista de todas las direcciones IP disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-123">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="fbd9a-124">El número y el puerto del vale se generan de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-124">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="fbd9a-125">El administrador de ti o el agente de asistencia escribe esta información en el **visor de conexión remota de DART** para establecer la conexión de servicios de Terminal Server con el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-125">The IT administrator or helpdesk agent enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="fbd9a-126">La conexión de servicios de Terminal Server que se establece permite que un administrador de ti interactúe de forma remota con las herramientas de DaRT en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-126">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="fbd9a-127">Después, el equipo del usuario final procesa la información de conexión, comparte su pantalla y responde a las instrucciones del PC administrador de ti.</span><span class="sxs-lookup"><span data-stu-id="fbd9a-127">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="fbd9a-128">Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="fbd9a-128">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="fbd9a-129">Otros recursos para recuperar equipos mediante DaRT7</span><span class="sxs-lookup"><span data-stu-id="fbd9a-129">Other resources for recovering computers using DaRT7</span></span>


[<span data-ttu-id="fbd9a-130">Operaciones para DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="fbd9a-130">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





