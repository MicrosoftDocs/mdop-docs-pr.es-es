---
title: Cómo implantar DaRT 10
description: Cómo implantar DaRT 10
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813071"
---
# <span data-ttu-id="4cd6a-103">Cómo implantar DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4cd6a-103">How to Deploy DaRT 10</span></span>


<span data-ttu-id="4cd6a-104">En las siguientes instrucciones se explica cómo implementar Microsoft Diagnostics and Recovery Toolset (DaRT) 10 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="4cd6a-105">Para obtener el software de DaRT, consulte [Cómo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="4cd6a-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="4cd6a-106">Se supone que está instalando toda la funcionalidad en un equipo de administrador.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="4cd6a-107">Si necesita implementar o desinstalar DaRT 10 en varios equipos, mediante un sistema electrónico de distribución de software, por ejemplo, puede que sea más fácil usar las opciones de instalación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-107">If you need to deploy or uninstall DaRT 10 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="4cd6a-108">En esta sección se proporcionan descripciones y ejemplos de las opciones de línea de comandos disponibles.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="4cd6a-109">**Importante**  Antes de instalar DaRT, consulte [configuraciones admitidas de DART 10](dart-10-supported-configurations.md) para asegurarse de que ha instalado todo el software necesario y de que el equipo cumple con los requisitos mínimos del sistema.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-109">**Important** Before you install DaRT, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="4cd6a-110">El equipo en el que instale DaRT debe estar ejecutando Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-110">The computer onto which you install DaRT must be running Windows 10.</span></span>

 

<span data-ttu-id="4cd6a-111">Puede instalar DaRT usando una de dos configuraciones distintas:</span><span class="sxs-lookup"><span data-stu-id="4cd6a-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="4cd6a-112">Instale DaRT y todas las herramientas de DaRT en el PC del administrador.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="4cd6a-113">Instale en el equipo del administrador solo las herramientas que necesita para crear la imagen de recuperación de DaRT y, a continuación, instale el **visor de conexión remota** y, opcionalmente, **Crash Analyzer** en un equipo de asistencia.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="4cd6a-114">El archivo de instalación de DaRT está disponible en las versiones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="4cd6a-115">Instale la versión que coincida con la arquitectura del equipo en el que está ejecutando el Asistente para imágenes de recuperación de DaRT, no la arquitectura del equipo de la imagen de recuperación que está creando.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="4cd6a-116">Puede usar cualquiera de las versiones del archivo de instalación de DaRT para crear una imagen de recuperación para equipos de 32 o 64 bits, pero no puede crear una imagen de recuperación para equipos de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="4cd6a-117">Para instalar DaRT y todas las herramientas de DaRT en un PC administrador</span><span class="sxs-lookup"><span data-stu-id="4cd6a-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="4cd6a-118">Descargue la versión de 32 bits o 64 bits del archivo de instalación de DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-118">Download the 32-bit or 64-bit version of the DaRT 10 installer file.</span></span> <span data-ttu-id="4cd6a-119">Elija la arquitectura que se corresponda con el equipo en el que está instalando DaRT y ejecute el Asistente para imágenes de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="4cd6a-120">En la carpeta en la que descargó DaRT 10, ejecute el archivo de instalación **MSDaRT.msi** correspondiente a los requisitos del sistema.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-120">From the folder into which you downloaded DaRT 10, run the **MSDaRT.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="4cd6a-121">En la página **Asistente para la instalación de DART 10 de Microsoft** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-121">On the **Welcome to the Microsoft DaRT 10 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="4cd6a-122">Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="4cd6a-123">En la página **Microsoft Update** , seleccione **usar Microsoft Update al buscar actualizaciones**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="4cd6a-124">En la página **Seleccionar carpeta de instalación** , seleccione una carpeta o haga clic en **siguiente** para instalar DART en la ubicación de instalación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="4cd6a-125">En la página **Opciones de configuración** , seleccione las características de DART que desee instalar o haga clic en **siguiente** para instalar DART con todas las características.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="4cd6a-126">Para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="4cd6a-127">Una vez completada la instalación correctamente, haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="4cd6a-128">Para instalar DaRT y todas las herramientas de DaRT en un equipo administrador mediante el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="4cd6a-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="4cd6a-129">Al instalar o desinstalar DaRT, tiene la opción de ejecutar los archivos de instalación en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="4cd6a-130">En esta sección se describen algunos ejemplos de las diferentes opciones que puede especificar al instalar o desinstalar DaRT en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="4cd6a-131">En el ejemplo siguiente se muestra cómo instalar todas las funcionalidades de DaRT.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="4cd6a-132">En el siguiente ejemplo se muestra cómo instalar solo el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="4cd6a-133">En el ejemplo siguiente se muestra cómo instalar solo el analizador de bloqueo y el visor de conexión remota de DaRT.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="4cd6a-134">En el ejemplo siguiente se crea un registro de instalación para Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="4cd6a-135">Esto es útil para la depuración.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

<span data-ttu-id="4cd6a-136">**Nota:**  Puede Agregar/QN o/QB para realizar una instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="4cd6a-137">Para validar la instalación de DaRT</span><span class="sxs-lookup"><span data-stu-id="4cd6a-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="4cd6a-138">Haga clic en **Inicio**y seleccione **diagnóstico y conjunto de herramientas de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="4cd6a-139">Se abrirá la ventana **conjunto de herramientas de diagnóstico y recuperación** .</span><span class="sxs-lookup"><span data-stu-id="4cd6a-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="4cd6a-140">Verifique que todas las herramientas de DaRT que seleccionó para la instalación se instalaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="4cd6a-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="4cd6a-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4cd6a-141">Related topics</span></span>


[<span data-ttu-id="4cd6a-142">Implementación de DaRT 10 en equipos de administrador</span><span class="sxs-lookup"><span data-stu-id="4cd6a-142">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

 

 





