---
title: Cómo instalar el secuenciador (App-V 4,6 SP1)
description: Cómo instalar el secuenciador (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817271"
---
# <span data-ttu-id="26f40-103">Cómo instalar el secuenciador (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="26f40-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="26f40-104">El secuenciador de Microsoft Application Virtualization (App-V) supervisa y registra el proceso de instalación y configuración de las aplicaciones para que la aplicación se pueda ejecutar como una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="26f40-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="26f40-105">Debe instalar el secuenciador de App-V en un equipo que solo tenga instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="26f40-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="26f40-106">Como alternativa, puede instalar el secuenciador en un equipo que se ejecute en un entorno virtual, por ejemplo, un equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="26f40-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="26f40-107">Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que puede reutilizar con una configuración adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="26f40-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="26f40-108">Debe tener credenciales administrativas en el equipo que está usando para secuenciar la aplicación, y el equipo no debe estar ejecutando ninguna versión de cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="26f40-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="26f40-109">La creación de una aplicación virtual mediante el secuenciador de App-V requiere varias operaciones, por lo que es importante que instale el secuenciador en un equipo que cumpla o supere los [requisitos de software y hardware](application-virtualization-sequencer-hardware-and-software-requirements.md)del transformador de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="26f40-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="26f40-110">Nota</span><span class="sxs-lookup"><span data-stu-id="26f40-110">Note</span></span>**  
<span data-ttu-id="26f40-111">No se admite la ejecución del secuenciador de App-V en el modo seguro.</span><span class="sxs-lookup"><span data-stu-id="26f40-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="26f40-112">Para instalar Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="26f40-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="26f40-113">Copie los archivos de instalación de Microsoft Application Virtualization Sequencer en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="26f40-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="26f40-114">Para iniciar el Asistente para la instalación de Microsoft Application Virtualization Sequencer, haga doble clic en **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="26f40-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="26f40-115">Si el **paquete redistribuible de Microsoft Visual C++ SP1 (x86)** no se detecta antes de la instalación, haga clic en **instalar** para instalar el requisito previo requerido.</span><span class="sxs-lookup"><span data-stu-id="26f40-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="26f40-116">Para continuar con la instalación, en la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="26f40-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="26f40-117">En la página **contrato de licencia** , para aceptar las condiciones del contrato de licencia, haga clic en Acepto **las condiciones del contrato de licencia**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="26f40-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="26f40-118">En la página **carpeta de destino** , para aceptar la carpeta de instalación predeterminada, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="26f40-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="26f40-119">Para especificar otra carpeta de destino, haga clic en **cambiar** y especifique la carpeta de instalación que se usará para la instalación.</span><span class="sxs-lookup"><span data-stu-id="26f40-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="26f40-120">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="26f40-120">Click **Next**.</span></span>

6.  <span data-ttu-id="26f40-121">En la página **unidad virtual** , para configurar la unidad predeterminada de Application Virtualization **Q:\\** (predeterminada) como la unidad desde la que se ejecutarán todas las aplicaciones secuenciadas, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="26f40-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="26f40-122">Si desea especificar una letra de unidad diferente, use la lista y seleccione la letra de unidad que desea usar seleccionando la letra de unidad correspondiente y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="26f40-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="26f40-123">Importante</span><span class="sxs-lookup"><span data-stu-id="26f40-123">Important</span></span>**  
    <span data-ttu-id="26f40-124">La letra de unidad de virtualización de aplicaciones especificada en este paso es la letra de unidad desde la que se ejecutarán las aplicaciones virtuales en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="26f40-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="26f40-125">La letra de unidad especificada debe estar disponible y no está en uso en los equipos que ejecutan el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="26f40-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="26f40-126">Si la unidad especificada ya está en uso, la aplicación virtual falla en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="26f40-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="26f40-127">En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="26f40-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="26f40-128">En la página **completado del asistente InstallShield** , para cerrar el Asistente de instalación y abrir el secuenciador de App-V, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="26f40-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="26f40-129">Para cerrar el Asistente de instalación sin abrir el secuenciador, desactive **iniciar el programa**y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="26f40-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="26f40-130">Nota</span><span class="sxs-lookup"><span data-stu-id="26f40-130">Note</span></span>**  
    <span data-ttu-id="26f40-131">Si instaló el secuenciador de App-V en un equipo que ejecuta un entorno virtual, por ejemplo, una máquina virtual, debe tomar una instantánea.</span><span class="sxs-lookup"><span data-stu-id="26f40-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="26f40-132">Después de secuenciar una aplicación, puede volver a esta imagen, de modo que pueda secuenciar la siguiente aplicación.</span><span class="sxs-lookup"><span data-stu-id="26f40-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="26f40-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26f40-133">Related topics</span></span>


[<span data-ttu-id="26f40-134">Configuración del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="26f40-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









