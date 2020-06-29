---
title: Página Archivos de instalación
description: Página Archivos de instalación
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816341"
---
# <span data-ttu-id="31019-103">Página Archivos de instalación</span><span class="sxs-lookup"><span data-stu-id="31019-103">Installation Files Page</span></span>


<span data-ttu-id="31019-104">Use la página **archivos de instalación** para especificar los archivos de instalación que se usaron para crear el paquete de aplicaciones virtual especificado en la página **seleccionar paquete** de este asistente.</span><span class="sxs-lookup"><span data-stu-id="31019-104">Use the **Installation Files** page to specify the installation files that were used to create the virtual application package specified on the **Select Package** page of this wizard.</span></span> <span data-ttu-id="31019-105">Si ha creado un paquete de aplicaciones virtual que contiene varias aplicaciones, debe copiar todos los archivos de instalación necesarios en una sola carpeta del equipo que ejecuta Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="31019-105">If you created a virtual application package that contains multiple applications, you should copy all required installation files to a single folder on the computer running the Microsoft Application Virtualization Sequencer.</span></span>

<span data-ttu-id="31019-106">Esta página contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="31019-106">This page contains the following elements:</span></span>

<a href="" id="original-installation-files"></a>**<span data-ttu-id="31019-107">Archivos de instalación original</span><span class="sxs-lookup"><span data-stu-id="31019-107">Original Installation Files</span></span>**  
<span data-ttu-id="31019-108">Haga clic en **examinar** para especificar los archivos de instalación que se usaron originalmente para crear el paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="31019-108">Click **Browse** to specify the installation files that were originally used to create the virtual application package.</span></span> <span data-ttu-id="31019-109">El directorio principal que especifique debe guardarse localmente en el equipo que ejecuta el secuenciador y debe contener todos los archivos o subcarpetas necesarios para la instalación que contengan los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="31019-109">The parent directory you specify should be saved locally to the computer running the Sequencer and must contain all required installation files or subfolders that contain the installation files.</span></span> <span data-ttu-id="31019-110">Los archivos de instalación pueden estar contenidos en la carpeta principal o en cualquiera de las subcarpetas de la carpeta principal especificada.</span><span class="sxs-lookup"><span data-stu-id="31019-110">The installation files can be contained in the parent folder or in any of the subfolders of the specified parent folder.</span></span>

<a href="" id="files-installed-on-local-system"></a>**<span data-ttu-id="31019-111">Archivos instalados en el sistema local</span><span class="sxs-lookup"><span data-stu-id="31019-111">Files installed on local system</span></span>**  
<span data-ttu-id="31019-112">Haga clic en **examinar** para especificar los archivos de instalación que se han instalado localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="31019-112">Click **Browse** to specify the installation files that have been installed locally on the computer running the Sequencer.</span></span> <span data-ttu-id="31019-113">Solo puede seleccionar esta opción si los archivos de instalación de la aplicación se instalaron en la ubicación predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31019-113">You can only select this option if the application installation files have been installed to the application’s default location.</span></span>

<span data-ttu-id="31019-114">**Nota:**  La ubicación de instalación predeterminada que proporcione dependerá de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="31019-114">**Note** The default installation location you provide depends on the following conditions:</span></span>

 

-   <span data-ttu-id="31019-115">La raíz del paquete especificada cuando el paquete se creó originalmente.</span><span class="sxs-lookup"><span data-stu-id="31019-115">The package root specified when the package was originally created.</span></span>

-   <span data-ttu-id="31019-116">La ubicación de instalación especificada en Windows Installer cuando el paquete se creó originalmente.</span><span class="sxs-lookup"><span data-stu-id="31019-116">The installation location specified in the Windows Installer when the package was originally created.</span></span>

-   <span data-ttu-id="31019-117">La ruta de instalación predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31019-117">The default application installation path.</span></span>

<span data-ttu-id="31019-118">Por ejemplo, si la raíz del paquete especificada es **Q:\\Office12** y durante la instalación, la ubicación de instalación predeterminada cambia de **c:\\Archivos de Files\\Office12** a **Q:\\Office12**, la ruta especificada durante la deshidratación debe ser **c:\\Archivos de Files\\Office 12**.</span><span class="sxs-lookup"><span data-stu-id="31019-118">For example, if the package root specified is **Q:\\Office12** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Office12**, then the path specified during dehydration must be **C:\\Program Files\\Office 12**.</span></span>

<span data-ttu-id="31019-119">Si la raíz del paquete especificada es **Q:\\Microsoft** y durante la instalación, la ubicación de instalación predeterminada cambia de **c:\\Archivos de Files\\Office12** a **Q:\\Microsoft\\Office12**, la ruta de acceso especificada durante la deshidratación debe ser c:\\Archivos de **programa**.</span><span class="sxs-lookup"><span data-stu-id="31019-119">If the package root specified is **Q:\\Microsoft** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Microsoft\\Office12**, then the path specified during dehydration must be **C:\\Program Files**.</span></span>

<span data-ttu-id="31019-120">Al crear un paquete con un acelerador de paquetes, cada archivo del paquete, por ejemplo **Q:\\Office12\\file.txt** se encuentra en el equipo local reemplazando la raíz del paquete **Q:\\Office12** por la ubicación predeterminada especificada cuando se creó el acelerador de paquetes, por ejemplo, **c:\\Archivos de Files\\Office12**.</span><span class="sxs-lookup"><span data-stu-id="31019-120">When you create a package using a package accelerator, each file in the package, for example **Q:\\Office12\\file.txt** is found on the local computer by replacing the package root **Q:\\Office12** with the default location specified when the Package Accelerator was created, for example, **C:\\Program Files\\Office12**.</span></span> <span data-ttu-id="31019-121">En el ejemplo anterior, el archivo debe estar ubicado en **c:\\Archivos de Files\\Office12\\file.txt**.</span><span class="sxs-lookup"><span data-stu-id="31019-121">In the previous example, the file should be located in **C:\\Program Files\\Office12\\file.txt**.</span></span>

## <span data-ttu-id="31019-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31019-122">Related topics</span></span>


[<span data-ttu-id="31019-123">Crear asistente del acelerador de paquetes (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="31019-123">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





