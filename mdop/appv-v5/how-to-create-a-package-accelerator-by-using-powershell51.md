---
title: Cómo crear un acelerador de paquetes mediante el uso de PowerShell
description: Cómo crear un acelerador de paquetes mediante el uso de PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814279"
---
# <span data-ttu-id="5ee4b-103">Cómo crear un acelerador de paquetes mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ee4b-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="5ee4b-104">Los aceleradores de paquetes de App-V 5,1 automáticamente ordenan aplicaciones grandes y complejas.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-104">App-V 5.1 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="5ee4b-105">Además, cuando aplica un acelerador de paquetes de App-V 5,1, no siempre es necesario instalar manualmente una aplicación para crear el paquete virtualizado.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-105">Additionally, when you apply an App-V 5.1 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="5ee4b-106">Para crear un acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="5ee4b-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="5ee4b-107">Instale el secuenciador de 5,1 de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="5ee4b-108">Para obtener más información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="5ee4b-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="5ee4b-109">Para abrir una consola de PowerShell, haga clic en **iniciar** y escriba **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="5ee4b-110">Haga clic con el botón derecho en **Windows PowerShell** y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="5ee4b-111">Use el cmdlet **New-AppvPackageAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="5ee4b-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="5ee4b-112">Para crear un acelerador de paquetes, asegúrese de tener el paquete. appv para crear un acelerador desde, los archivos de instalación o los medios de instalación, y, opcionalmente, un archivo Léame para que los usuarios del acelerador usen.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="5ee4b-113">Los siguientes parámetros son necesarios para usar el cmdlet del acelerador de paquetes:</span><span class="sxs-lookup"><span data-stu-id="5ee4b-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="5ee4b-114">**InstalledFilesPath** : especifica la ruta de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="5ee4b-115">**Instalador** : especifica la ruta de acceso a los medios del instalador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5ee4b-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="5ee4b-116">**InputPackagePath** : especifica la ruta de acceso al paquete. appv</span><span class="sxs-lookup"><span data-stu-id="5ee4b-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="5ee4b-117">**Path** : especifica el directorio de salida del paquete.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="5ee4b-118">En el ejemplo siguiente se muestra cómo se puede crear un acelerador de paquetes con un paquete. appv y los medios de instalación:</span><span class="sxs-lookup"><span data-stu-id="5ee4b-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="5ee4b-119">New-AppvPackageAccelerator-InputPackagePath &lt; path al archivo. appv &gt; : ruta de acceso &lt; del instalador al archivo ejecutable de instalación &gt; -ruta &lt; de acceso de la ruta de acceso de salida&gt;</span><span class="sxs-lookup"><span data-stu-id="5ee4b-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="5ee4b-120">En la siguiente lista se muestran parámetros opcionales adicionales que se pueden usar con el cmdlet **New-AppvPackageAccelerator** :</span><span class="sxs-lookup"><span data-stu-id="5ee4b-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="5ee4b-121">**AcceleratorDescriptionFile** : especifica la ruta de acceso a las instrucciones del acelerador de paquetes creado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="5ee4b-122">Las instrucciones del acelerador de paquetes son archivos de Descripción **. txt** o **. rtf** que se empaquetarán con el paquete creado con el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="5ee4b-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="5ee4b-123">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="5ee4b-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5ee4b-124">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5ee4b-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5ee4b-125">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="5ee4b-125">Got an App-V issue?</span></span>** <span data-ttu-id="5ee4b-126">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5ee4b-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5ee4b-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ee4b-127">Related topics</span></span>


[<span data-ttu-id="5ee4b-128">Administrar 5.1 de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ee4b-128">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





