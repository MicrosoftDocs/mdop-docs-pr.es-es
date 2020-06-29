---
title: Cómo instalar el secuenciador
description: Cómo instalar el secuenciador
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817270"
---
# <span data-ttu-id="1f7b4-103">Cómo instalar el secuenciador</span><span class="sxs-lookup"><span data-stu-id="1f7b4-103">How to Install the Sequencer</span></span>


<span data-ttu-id="1f7b4-104">El secuenciador de Microsoft Application Virtualization (App-V) supervisa y registra el proceso de instalación y configuración de las aplicaciones para que la aplicación se pueda ejecutar como una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="1f7b4-105">Debe instalar el secuenciador en un equipo que solo tenga instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="1f7b4-106">Como alternativa, puede instalar el secuenciador en un equipo que ejecute un entorno virtual, por ejemplo, Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="1f7b4-107">Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que se puede volver a usar con una configuración adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="1f7b4-108">Debe tener derechos administrativos en el equipo que está usando para secuenciar la aplicación y el equipo debe estar conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="1f7b4-109">El equipo no debe estar ejecutando ninguna versión del cliente de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="1f7b4-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="1f7b4-110">Crear una aplicación virtual con el secuenciador es muy intensivo de recursos, por lo que es importante que instale el secuenciador en un equipo que cumpla o supere los requisitos recomendados.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="1f7b4-111">Para obtener más información sobre los requisitos del sistema, consulte [los requisitos de software y hardware del secuenciador](sequencer-hardware-and-software-requirements.md)..</span><span class="sxs-lookup"><span data-stu-id="1f7b4-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="1f7b4-112">Para instalar Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="1f7b4-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="1f7b4-113">Copie los archivos de instalación de Microsoft Application Virtualization Sequencer en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="1f7b4-114">Para iniciar el Asistente para la instalación de Microsoft Application Virtualization Sequencer, seleccione **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="1f7b4-115">Si el **paquete redistribuible de Microsoft Visual C++ SP1 (x86)** no se detecta antes de la instalación, **setup.exe** lo instalará.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="1f7b4-116">En la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="1f7b4-117">En la página **contrato de licencia** , para aceptar las condiciones del contrato de licencia, seleccione Acepto **las condiciones del contrato de licencia**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="1f7b4-118">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-118">Click **Next**.</span></span>

5.  <span data-ttu-id="1f7b4-119">En la página **carpeta de destino** , para aceptar la carpeta de instalación predeterminada, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="1f7b4-120">Para especificar otra carpeta de destino, haga clic en **cambiar** y especifique la carpeta de instalación que se usará para la instalación.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="1f7b4-121">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-121">Click **Next**.</span></span>

6.  <span data-ttu-id="1f7b4-122">En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="1f7b4-123">En la página **completado del asistente InstallShield** , para cerrar el Asistente de instalación y abrir el secuenciador, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="1f7b4-124">Para cerrar el Asistente de instalación sin abrir el secuenciador, anule la selección de **iniciar el programa** y haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="1f7b4-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="1f7b4-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f7b4-125">Related topics</span></span>


[<span data-ttu-id="1f7b4-126">Configuración del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="1f7b4-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 





