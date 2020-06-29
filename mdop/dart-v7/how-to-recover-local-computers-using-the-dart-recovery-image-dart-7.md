---
title: Cómo recuperar los equipos locales con la imagen para recuperación de DaRT
description: Cómo recuperar los equipos locales con la imagen para recuperación de DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823761"
---
# <span data-ttu-id="1f8e1-103">Cómo recuperar los equipos locales con la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="1f8e1-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="1f8e1-104">Para recuperar un equipo local mediante Microsoft Diagnostics and Recovery Toolset (DaRT) 7, debe estar presente físicamente en el equipo del usuario final que está experimentando problemas que requieren DaRT.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="1f8e1-105">También puede ejecutar DaRT de manera remota siguiendo las instrucciones que encontrará en [Cómo recuperar equipos remotos con la imagen de recuperación de DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="1f8e1-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="1f8e1-106">Para recuperar un equipo local con DaRT</span><span class="sxs-lookup"><span data-stu-id="1f8e1-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="1f8e1-107">Mientras se inicia el equipo en la imagen de recuperación de DaRT, aparece el cuadro de diálogo **netstart** .</span><span class="sxs-lookup"><span data-stu-id="1f8e1-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="1f8e1-108">Se le pregunta si desea inicializar los servicios de red.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="1f8e1-109">Si hace clic en **sí**, se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="1f8e1-110">Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="1f8e1-111">Para omitir el proceso de inicialización de red, haga clic en **no**.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="1f8e1-112">Siguiendo el cuadro de diálogo inicialización de red, se le preguntará si desea volver a asignar las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="1f8e1-113">Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="1f8e1-114">Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="1f8e1-115">La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="1f8e1-116">Siguiendo el cuadro de diálogo reasignación, aparece un cuadro de diálogo **Opciones de recuperación del sistema** y le pide que seleccione una distribución de teclado.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="1f8e1-117">Después, se muestra el directorio raíz del sistema, el tipo de sistema operativo instalado y el tamaño de la partición.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="1f8e1-118">Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="1f8e1-119">Esto le pedirá que inserte los medios de instalación para el dispositivo y que seleccione el controlador.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="1f8e1-120">Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="1f8e1-121">Nota</span><span class="sxs-lookup"><span data-stu-id="1f8e1-121">Note</span></span>**  
    <span data-ttu-id="1f8e1-122">Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 7 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="1f8e1-123">En la ventana **Opciones de recuperación del sistema** , haga clic en **Microsoft Diagnostics and Recovery Toolset**.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="1f8e1-124">Se abrirá la ventana **conjunto de herramientas de diagnóstico y recuperación** .</span><span class="sxs-lookup"><span data-stu-id="1f8e1-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="1f8e1-125">Ahora puede ejecutar cualquiera de las herramientas o asistentes individuales que se incluyeron cuando se creó la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="1f8e1-126">Puede hacer clic en **ayuda** en la ventana **conjunto de herramientas de diagnósticos y recuperación** para abrir el archivo de ayuda del cliente que proporciona instrucciones detalladas e información necesaria para ejecutar las herramientas de DART individuales.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="1f8e1-127">También puede hacer clic en el **Asistente para soluciones** en la ventana conjunto de herramientas de **diagnóstico y recuperación** para elegir la mejor herramienta para la situación, en función de una breve entrevista que proporciona el asistente.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="1f8e1-128">Para obtener información general sobre cualquiera de las herramientas de DaRT, consulte [información general sobre las herramientas de dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="1f8e1-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="1f8e1-129">Para ejecutar DaRT en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="1f8e1-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="1f8e1-130">Puede ejecutar DaRT en el símbolo del sistema especificando el comando **netstart.exe** y utilizando cualquiera de los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="1f8e1-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1f8e1-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1f8e1-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="1f8e1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f8e1-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="1f8e1-133">-red</span><span class="sxs-lookup"><span data-stu-id="1f8e1-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1f8e1-134">Inicializa los servicios de red.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="1f8e1-135">-volver a montar</span><span class="sxs-lookup"><span data-stu-id="1f8e1-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1f8e1-136">Reasigna las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="1f8e1-137">-prompt</span><span class="sxs-lookup"><span data-stu-id="1f8e1-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1f8e1-138">Muestra mensajes que piden al usuario final que especifique si desea inicializar la red y reasignar las unidades.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1f8e1-139">Importante</span><span class="sxs-lookup"><span data-stu-id="1f8e1-139">Important</span></span></strong><br/><p><span data-ttu-id="1f8e1-140">La respuesta del usuario final a las preguntas reemplaza a los modificadores-Network y-remount.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="1f8e1-141">Puede personalizar DaRT para que un equipo que inicie en DaRT abra automáticamente la herramienta de **conexión remota** que se usa para establecer una conexión remota con el Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="1f8e1-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="1f8e1-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f8e1-142">Related topics</span></span>


[<span data-ttu-id="1f8e1-143">Equipos de recuperación que usan DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="1f8e1-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









