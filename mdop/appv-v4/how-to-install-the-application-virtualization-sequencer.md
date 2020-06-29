---
title: Cómo instalar el secuenciador de virtualización de aplicaciones
description: Cómo instalar el secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817310"
---
# <span data-ttu-id="f7efb-103">Cómo instalar el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f7efb-103">How to Install the Application Virtualization Sequencer</span></span>


<span data-ttu-id="f7efb-104">Microsoft Application Virtualization SPRJ supervisa y registra el proceso de instalación y configuración de las aplicaciones para que la aplicación se pueda ejecutar como una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="f7efb-104">The Microsoft Application Virtualization Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="f7efb-105">Debe instalar el secuenciador en un equipo que solo tenga instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f7efb-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="f7efb-106">Como alternativa, puede instalar el secuenciador en un equipo que ejecute un entorno virtual, por ejemplo, Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f7efb-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="f7efb-107">Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que se puede volver a usar con una configuración adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="f7efb-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="f7efb-108">Debe tener derechos administrativos en el equipo que está usando para secuenciar la aplicación y el equipo no debe estar ejecutando ninguna versión del cliente de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="f7efb-108">You must have administrative rights on the computer you are using to sequence the application and the computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="f7efb-109">Crear una aplicación virtual mediante el secuenciador es muy intensivo de recursos, por lo que es importante que instale el secuenciador en un equipo que cumpla o supere los requisitos recomendados.</span><span class="sxs-lookup"><span data-stu-id="f7efb-109">Creating a virtual application by using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="f7efb-110">No se admite la ejecución del secuenciador de App-V en el modo seguro.</span><span class="sxs-lookup"><span data-stu-id="f7efb-110">Running the App-V sequencer in Safe Mode is not supported.</span></span> <span data-ttu-id="f7efb-111">Para obtener más información sobre los requisitos del sistema, consulte [requisitos del sistema de Application Virtualization](application-virtualization-system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f7efb-111">For more information about the system requirements, see [Application Virtualization System Requirements](application-virtualization-system-requirements.md).</span></span>

<span data-ttu-id="f7efb-112">**Importante**  Una vez que haya realizado la secuencia de una aplicación, antes de que pueda secuenciar correctamente una nueva aplicación, debe reinstalar el sistema operativo y el secuenciador en el equipo que está usando para secuenciar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f7efb-112">**Important** After you have sequenced an application, before you can properly sequence a new application you must reinstall the operating system and the Sequencer on the computer you are using to sequence applications.</span></span>

 

**<span data-ttu-id="f7efb-113">Para instalar Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7efb-113">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="f7efb-114">Copie los archivos de instalación de Microsoft Application Virtualization Sequencer en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="f7efb-114">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="f7efb-115">Para iniciar el Asistente para la instalación de Microsoft Application Virtualization Sequencer, seleccione **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-115">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="f7efb-116">Si el **paquete redistribuible de Microsoft Visual C++ SP1 (x86)** no se detecta antes de la instalación, **setup.exe** lo instalará.</span><span class="sxs-lookup"><span data-stu-id="f7efb-116">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="f7efb-117">En la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-117">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="f7efb-118">En la página **contrato de licencia** , para aceptar las condiciones del contrato de licencia, seleccione Acepto **las condiciones del contrato de licencia**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-118">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="f7efb-119">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-119">Click **Next**.</span></span>

5.  <span data-ttu-id="f7efb-120">En la página **carpeta de destino** , para aceptar la carpeta de instalación predeterminada, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-120">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="f7efb-121">Para especificar otra carpeta de destino, haga clic en **cambiar** y especifique la carpeta de instalación que se usará para la instalación.</span><span class="sxs-lookup"><span data-stu-id="f7efb-121">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="f7efb-122">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-122">Click **Next**.</span></span>

6.  <span data-ttu-id="f7efb-123">En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-123">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="f7efb-124">En la página **completado del asistente InstallShield** , para cerrar el Asistente de instalación y abrir el secuenciador, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-124">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="f7efb-125">Para cerrar el Asistente de instalación sin abrir el secuenciador, anule la selección de **iniciar el programa** y haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="f7efb-125">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="f7efb-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7efb-126">Related topics</span></span>


[<span data-ttu-id="f7efb-127">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f7efb-127">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="f7efb-128">Requisitos de implementación de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f7efb-128">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

 

 





