---
title: Cómo implantar DaRT 7.0
description: Cómo implantar DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813047"
---
# <span data-ttu-id="f3fbf-103">Cómo implantar DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="f3fbf-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="f3fbf-104">Este tema proporciona instrucciones para implementar Microsoft Diagnostics and Recovery Toolset (DaRT) 7 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="f3fbf-105">En el primer procedimiento de este tema se supone que está instalando toda la funcionalidad en un equipo de administrador.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="f3fbf-106">Cuando necesite implementar o desinstalar DaRT en varios equipos, mediante un sistema electrónico de distribución de software, por ejemplo, puede que sea más fácil usar las opciones de instalación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="f3fbf-107">Estas opciones se definen en el segundo procedimiento de este tema, que proporciona el uso de ejemplo para las opciones de línea de comandos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="f3fbf-108">**Importante**  Antes de instalar DaRT, asegúrese de que el equipo cumpla con los requisitos mínimos de sistema enumerados en [DaRT 7,0 configuraciones admitidas](dart-70-supported-configurations-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="f3fbf-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="f3fbf-109">Para instalar DaRT en un PC administrador</span><span class="sxs-lookup"><span data-stu-id="f3fbf-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="f3fbf-110">Ubique los archivos de instalación de DaRT que recibió como parte de la descarga de software.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="f3fbf-111">Haga doble clic en el archivo de instalación de DaRT que corresponde a los requisitos del sistema: 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="f3fbf-112">El archivo de instalación de DaRT se denomina **MSDaRT70.msi**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="f3fbf-113">Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="f3fbf-114">Seleccione la carpeta de destino para instalar DaRT, seleccione si DaRT debe instalarse para todos los usuarios o solo para el usuario actual y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="f3fbf-115">Seleccione si la instalación debe ser **típica**, **personalizada**o **completa**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="f3fbf-116">**Típica** instala las herramientas que se usan con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="f3fbf-117">Se recomienda usar este método para la mayoría de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="f3fbf-118">**Personalizado** le permite seleccionar las herramientas que se instalan y dónde se instalarán.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="f3fbf-119">Esto es recomendable para usuarios avanzados, especialmente si está instalando diferentes herramientas de DaRT en diferentes equipos del servicio de asistencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="f3fbf-120">**Completa** : instala todas las herramientas de DART y requiere la mayor parte del espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="f3fbf-121">Una vez que haya seleccionado el método de instalación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="f3fbf-122">Para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="f3fbf-123">Una vez completada la instalación correctamente, haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="f3fbf-124">Para instalar DaRT en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="f3fbf-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="f3fbf-125">En el ejemplo siguiente se muestra cómo instalar todas las funcionalidades de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="f3fbf-126">En el siguiente ejemplo se muestra cómo instalar solo el **Asistente de imagen de recuperación de DART**.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="f3fbf-127">En el ejemplo siguiente se muestra cómo instalar solo el analizador de bloqueo y el visor de conexión remota de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="f3fbf-128">En el ejemplo siguiente se crea un registro de instalación para Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="f3fbf-129">Esto es útil para la depuración.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="f3fbf-130">**Nota:**  Puede Agregar/QN o/QB a cualquiera de las opciones del símbolo del sistema de la instalación de DaRT para realizar una instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="f3fbf-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="f3fbf-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3fbf-131">Related topics</span></span>


[<span data-ttu-id="f3fbf-132">Implementación de DaRT 7.0 en equipos de administrador</span><span class="sxs-lookup"><span data-stu-id="f3fbf-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





