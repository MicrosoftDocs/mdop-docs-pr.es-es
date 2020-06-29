---
title: Instalar aplicaciones en una imagen de Windows Virtual PC
description: Instalar aplicaciones en una imagen de Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826831"
---
# <span data-ttu-id="3895b-103">Instalar aplicaciones en una imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3895b-103">Installing Applications on a Windows Virtual PC Image</span></span>


<span data-ttu-id="3895b-104">Después de crear una imagen de Windows Virtual PC para usarla con Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, puede instalar otros componentes que sean útiles al ejecutar MED-V, como un sistema de distribución electrónica de software (ESD) y software antivirus.</span><span class="sxs-lookup"><span data-stu-id="3895b-104">After you have created a Windows Virtual PC image for use with Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you can install other components that are helpful when running MED-V, such as an electronic software distribution (ESD) system and antivirus software.</span></span>

<span data-ttu-id="3895b-105">La siguiente sección proporciona información para ayudarle a instalar software en la imagen de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3895b-105">The following section provides information to help you install software on the MED-V image.</span></span>

<span data-ttu-id="3895b-106">**PRECAUCIÓN**  Para facilitar la administración de áreas de trabajo de MED-V después de la implementación, le recomendamos que limite el número de componentes que instale en la imagen de MED-V a los componentes necesarios o que sean útiles cuando use MED-V.</span><span class="sxs-lookup"><span data-stu-id="3895b-106">**Caution** For ease of MED-V workspace management after deployment, we recommend that you limit the number of components that you install on the MED-V image to those components that are required or that are helpful when using MED-V.</span></span> <span data-ttu-id="3895b-107">Por ejemplo, aunque no es necesario ejecutar MED-V, puede instalar un sistema ESD para usar más tarde para instalar aplicaciones en un área de trabajo de MED-V y software antivirus para la seguridad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3895b-107">For example, although they are not required to run MED-V, you can install an ESD system to use later for installing applications to a MED-V workspace and antivirus software for security on the image.</span></span>

 

**<span data-ttu-id="3895b-108">Instalar software en una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="3895b-108">Installing Software on a MED-V Image</span></span>**

1.  <span data-ttu-id="3895b-109">Si no se está ejecutando en este momento, abra su máquina virtual de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3895b-109">If it is not currently running, open your MED-V virtual machine.</span></span>

    1.  <span data-ttu-id="3895b-110">Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC** y, a continuación, haga clic en **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="3895b-110">Click **Start**, click **All Programs**, click **Windows Virtual PC** and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="3895b-111">Haga doble clic en su máquina virtual de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3895b-111">Double-click your MED-V virtual machine.</span></span>

2.  <span data-ttu-id="3895b-112">Desde el sistema operativo de la máquina virtual, busque los archivos de instalación del software que desea instalar.</span><span class="sxs-lookup"><span data-stu-id="3895b-112">From inside the virtual machine operating system, locate the installation files for the software that you want to install.</span></span>

3.  <span data-ttu-id="3895b-113">Siga las instrucciones de instalación proporcionadas por el proveedor del software.</span><span class="sxs-lookup"><span data-stu-id="3895b-113">Follow the installation instructions that are provided by the software vendor.</span></span>

    <span data-ttu-id="3895b-114">**Nota:**  Una vez completada la instalación, es posible que tenga que cerrar y reiniciar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3895b-114">**Note** After installation is complete, you might have to close and then restart the virtual machine.</span></span>

     

<span data-ttu-id="3895b-115">Repita estos pasos para cualquier software o aplicación que desee instalar en la imagen de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3895b-115">Repeat these steps for any software or application that you want to install on the MED-V image.</span></span> <span data-ttu-id="3895b-116">Le recomendamos que limite el número de aplicaciones que preinstale en la imagen.</span><span class="sxs-lookup"><span data-stu-id="3895b-116">We recommend that you limit the number of applications that you preinstall on the image.</span></span> <span data-ttu-id="3895b-117">El proceso recomendado para instalar aplicaciones y otro software de la imagen es preinstalar ahora un sistema ESD y usarlo más adelante para implementar el software en la imagen.</span><span class="sxs-lookup"><span data-stu-id="3895b-117">The recommended process for installing applications and other software on the image is to preinstall an ESD system now and to use it later to deploy software to the image.</span></span> <span data-ttu-id="3895b-118">Como alternativa, también puede usar la Directiva de grupo o App-V para agregar o quitar aplicaciones en un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3895b-118">Alternately, you can also use Group Policy or App-V to add or remove applications on a MED-V workspace.</span></span> <span data-ttu-id="3895b-119">Para obtener más información, vea [Administración de aplicaciones implementadas en áreas de trabajo de MED-V](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="3895b-119">For more information, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

<span data-ttu-id="3895b-120">Para obtener más información sobre cómo instalar software en una imagen virtual, consulte los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3895b-120">For more information about how to install software on a virtual image, see the following articles:</span></span>

-   <span data-ttu-id="3895b-121">[Publicar y usar aplicaciones virtuales](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .</span><span class="sxs-lookup"><span data-stu-id="3895b-121">[Publish and Use Virtual Applications](https://go.microsoft.com/fwlink/?LinkId=195926) (https://go.microsoft.com/fwlink/?LinkId=195926).</span></span>

-   <span data-ttu-id="3895b-122">[Ayuda de Virtual PC de Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="3895b-122">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="3895b-123">Una vez que haya instalado todo el software que desea en la imagen de MED-V, la imagen estará lista para empaquetarse.</span><span class="sxs-lookup"><span data-stu-id="3895b-123">After you have installed all of the software that you want on the MED-V image, your image is ready to be packaged.</span></span>

## <span data-ttu-id="3895b-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3895b-124">Related topics</span></span>


[<span data-ttu-id="3895b-125">Configurar una imagen de Windows Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="3895b-125">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="3895b-126">Preparar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="3895b-126">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)

 

 





