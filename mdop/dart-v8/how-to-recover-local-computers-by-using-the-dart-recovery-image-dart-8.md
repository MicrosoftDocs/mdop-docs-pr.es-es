---
title: Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT
description: Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT
author: dansimp
ms.assetid: f679d522-49ab-429c-93d0-294c3f3e5639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1b5faa0eb9ac24b33c66f1d5262a050b92e11e52
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824310"
---
# <span data-ttu-id="a3732-103">Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="a3732-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="a3732-104">Siga estas instrucciones para recuperar un equipo cuando esté físicamente presente en el equipo del usuario final que tiene problemas.</span><span class="sxs-lookup"><span data-stu-id="a3732-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="a3732-105">Cómo recuperar un equipo local mediante la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="a3732-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="a3732-106">Inicie el equipo del usuario final con la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="a3732-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

    <span data-ttu-id="a3732-107">A medida que el equipo se inicia en la imagen de recuperación de DaRT 8,0, aparece el cuadro de diálogo **netstart** .</span><span class="sxs-lookup"><span data-stu-id="a3732-107">As the computer is booting into the DaRT 8.0 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="a3732-108">Cuando se le pregunte si desea inicializar los servicios de red, seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3732-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="a3732-109">**Sí** : se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="a3732-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="a3732-110">Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.</span><span class="sxs-lookup"><span data-stu-id="a3732-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="a3732-111">**No** , omitir el proceso de inicialización de red.</span><span class="sxs-lookup"><span data-stu-id="a3732-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="a3732-112">Indique si desea volver a asignar las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="a3732-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="a3732-113">Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión.</span><span class="sxs-lookup"><span data-stu-id="a3732-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="a3732-114">Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea.</span><span class="sxs-lookup"><span data-stu-id="a3732-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="a3732-115">La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.</span><span class="sxs-lookup"><span data-stu-id="a3732-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="a3732-116">En el cuadro de diálogo **Opciones de recuperación del sistema** , seleccione una distribución de teclado.</span><span class="sxs-lookup"><span data-stu-id="a3732-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="a3732-117">Compruebe el directorio raíz del sistema que se muestra, el tipo de sistema operativo instalado y el tamaño de la partición.</span><span class="sxs-lookup"><span data-stu-id="a3732-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="a3732-118">Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos y, a continuación, inserte los medios de instalación para el dispositivo y seleccione el controlador.</span><span class="sxs-lookup"><span data-stu-id="a3732-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="a3732-119">Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a3732-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="a3732-120">Nota</span><span class="sxs-lookup"><span data-stu-id="a3732-120">Note</span></span>**  
    <span data-ttu-id="a3732-121">Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 8 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a3732-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 8 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="a3732-122">En la ventana **Opciones de recuperación del sistema** , haga clic en **Microsoft Diagnostics and Recovery Toolset**.</span><span class="sxs-lookup"><span data-stu-id="a3732-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="a3732-123">Se abrirá la ventana **conjunto de herramientas de diagnóstico y recuperación** .</span><span class="sxs-lookup"><span data-stu-id="a3732-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="a3732-124">Ahora puede ejecutar cualquiera de las herramientas o asistentes individuales que se incluyeron cuando se creó la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="a3732-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="a3732-125">Puede hacer clic en **ayuda** en la ventana **conjunto de herramientas de diagnósticos y recuperación** para abrir el archivo de ayuda del cliente que proporciona instrucciones detalladas e información necesaria para ejecutar las herramientas de DART individuales.</span><span class="sxs-lookup"><span data-stu-id="a3732-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="a3732-126">También puede hacer clic en el **Asistente para soluciones** en la ventana conjunto de herramientas de **diagnóstico y recuperación** para elegir la mejor herramienta para la situación, en función de una breve entrevista que proporciona el asistente.</span><span class="sxs-lookup"><span data-stu-id="a3732-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="a3732-127">Para obtener información general sobre cualquiera de las herramientas de DaRT, consulte [información general sobre las herramientas de dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="a3732-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

**<span data-ttu-id="a3732-128">Cómo ejecutar DaRT en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="a3732-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="a3732-129">Para ejecutar DaRT en el símbolo del sistema, especifique el comando **netstart.exe** y, a continuación, use cualquiera de los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="a3732-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="a3732-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a3732-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="a3732-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3732-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="a3732-132">-red</span><span class="sxs-lookup"><span data-stu-id="a3732-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="a3732-133">Inicializa los servicios de red.</span><span class="sxs-lookup"><span data-stu-id="a3732-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="a3732-134">-volver a montar</span><span class="sxs-lookup"><span data-stu-id="a3732-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="a3732-135">Reasigna las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="a3732-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="a3732-136">-prompt</span><span class="sxs-lookup"><span data-stu-id="a3732-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="a3732-137">Muestra mensajes que piden al usuario final que especifique si desea inicializar la red y reasignar las unidades.</span><span class="sxs-lookup"><span data-stu-id="a3732-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="a3732-138">Advertencia</span><span class="sxs-lookup"><span data-stu-id="a3732-138">Warning</span></span></strong><br/><p><span data-ttu-id="a3732-139">La respuesta del usuario final a la solicitud reemplaza los modificadores – Network y-Mount.</span><span class="sxs-lookup"><span data-stu-id="a3732-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="a3732-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3732-140">Related topics</span></span>


[<span data-ttu-id="a3732-141">Operaciones para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a3732-141">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="a3732-142">Equipos de recuperación que usan DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a3732-142">Recovering Computers Using DaRT 8.0</span></span>](recovering-computers-using-dart-80-dart-8.md)









