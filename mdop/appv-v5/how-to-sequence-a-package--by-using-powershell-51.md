---
title: Cómo hacer una secuencia de un paquete con PowerShell
description: Cómo hacer una secuencia de un paquete con PowerShell
author: dansimp
ms.assetid: 6134c6be-937d-4609-a516-92d49154b290
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1bc2933fdb64080dab3b514784e7f68b0236df9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813694"
---
# <span data-ttu-id="cc3bb-103">Cómo hacer una secuencia de un paquete con PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc3bb-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="cc3bb-104">Use el siguiente procedimiento para crear un nuevo paquete de App-V 5,1 con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-104">Use the following procedure to create a new App-V 5.1 package using PowerShell.</span></span>

<span data-ttu-id="cc3bb-105">**Nota:**  Antes de usar este procedimiento, debe copiar los archivos de instalador asociados en el equipo que ejecuta el secuenciador y leer y comprender la sección Sequencer de [la planificación de la aplicación-V 5,1 secuenciador y la implementación de cliente](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="cc3bb-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="cc3bb-106">Para crear una nueva aplicación virtual con PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc3bb-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="cc3bb-107">Instale el secuenciador de 5,1 de App-V.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="cc3bb-108">Para obtener más información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="cc3bb-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="cc3bb-109">Para abrir una consola de PowerShell, haga clic en **iniciar** y escriba **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="cc3bb-110">Haga clic con el botón derecho en **Windows PowerShell** y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="cc3bb-111">Con la consola de PowerShell, escriba lo siguiente: **Import-Module appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="cc3bb-112">Para crear un paquete, use el cmdlet **New-AppvSequencerPackage** .</span><span class="sxs-lookup"><span data-stu-id="cc3bb-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="cc3bb-113">Los siguientes parámetros son necesarios para crear un paquete:</span><span class="sxs-lookup"><span data-stu-id="cc3bb-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="cc3bb-114">**Name** : especifica el nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="cc3bb-115">**PrimaryVirtualApplicationDirectory** : especifica la ruta de acceso al directorio que se usará para instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="cc3bb-116">Esta ruta debe existir.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-116">This path must exist.</span></span>

    -   <span data-ttu-id="cc3bb-117">**Instalador** : especifica la ruta de acceso al instalador de la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="cc3bb-118">**RutaDeAcceso** : especifica el directorio de salida del paquete.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="cc3bb-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cc3bb-119">For example:</span></span>

    **<span data-ttu-id="cc3bb-120">New-AppvSequencerPackage: nombre &lt; del nombre de la ruta de acceso del paquete &gt; PrimaryVirtualApplicationDirectory &lt; a la raíz del paquete &gt; -ruta de acceso del instalador &lt; para el ejecutable del instalador &gt; -OutputPath &lt; Directorio de la ruta de acceso de salida&gt;</span><span class="sxs-lookup"><span data-stu-id="cc3bb-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="cc3bb-121">Espere a que el secuenciador cree el paquete.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="cc3bb-122">Crear un paquete con PowerShell puede tardar un tiempo.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="cc3bb-123">Si el paquete no se creó correctamente, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="cc3bb-124">En la siguiente lista se muestran parámetros opcionales adicionales que se pueden usar con **el cmdlet New-AppvSequencerPackage** :</span><span class="sxs-lookup"><span data-stu-id="cc3bb-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="cc3bb-125">AcceleratorFilePath: especifica la ruta de acceso al archivo. cab de acelerador para generar un paquete.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="cc3bb-126">InstalledFilesPath: especifica la ruta en la que se guardan los archivos locales instalados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="cc3bb-127">InstallMediaPath: especifica la ruta de acceso en la que se encuentran los medios de instalación</span><span class="sxs-lookup"><span data-stu-id="cc3bb-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="cc3bb-128">TemplateFilePath: especifica la ruta de acceso a un archivo de plantilla si desea personalizar el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="cc3bb-129">FullLoad: especifica que el paquete debe descargarse completamente en el equipo que ejecuta la aplicación-V 5,1 para que pueda abrirse.</span><span class="sxs-lookup"><span data-stu-id="cc3bb-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.1 before it can be opened.</span></span>

    <span data-ttu-id="cc3bb-130">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="cc3bb-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cc3bb-131">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="cc3bb-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cc3bb-132">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="cc3bb-132">Got an App-V issue?</span></span>** <span data-ttu-id="cc3bb-133">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cc3bb-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cc3bb-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc3bb-134">Related topics</span></span>


[<span data-ttu-id="cc3bb-135">Administrar 5.1 de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc3bb-135">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





