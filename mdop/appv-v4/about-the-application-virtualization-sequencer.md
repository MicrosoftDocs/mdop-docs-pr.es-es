---
title: Acerca del secuenciador de virtualización de aplicaciones
description: Acerca del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820000"
---
# <span data-ttu-id="b0566-103">Acerca del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b0566-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="b0566-104">El secuenciador de Microsoft Application Virtualization (App-V) supervisa y registra todos los procesos de instalación y configuración de una aplicación y crea los siguientes archivos: **ICO**, **OSD**, **SFT**y **SPRJ**.</span><span class="sxs-lookup"><span data-stu-id="b0566-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="b0566-105">Estos archivos contienen toda la información necesaria sobre una aplicación para que la aplicación pueda ejecutarse en un entorno virtual en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="b0566-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="b0566-106">Puede usar el secuenciador de Microsoft Application Virtualization (App-V) para crear aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b0566-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="b0566-107">Después de la secuencia de una aplicación, se puede transmitir a los equipos de destino, o bien los equipos de destino pueden ejecutar la aplicación virtual descargando el contenido del paquete de aplicación virtual y ejecutando la aplicación de forma local.</span><span class="sxs-lookup"><span data-stu-id="b0566-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="b0566-108">**Importante**  Para ejecutar un paquete de aplicación virtual, el equipo de destino debe ejecutar la versión adecuada del cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="b0566-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="b0566-109">Los paquetes de aplicaciones virtuales se ejecutan en equipos de destino sin interactuar con el sistema operativo subyacente en el equipo de destino, ya que cada aplicación se ejecuta en un entorno virtual y se aísla de otras aplicaciones que se instalan o se ejecutan en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="b0566-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="b0566-110">Este aislamiento puede reducir los conflictos de aplicaciones y puede ayudar a reducir la cantidad requerida de pruebas previas a la implementación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b0566-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="b0566-111">Terminología del secuenciador</span><span class="sxs-lookup"><span data-stu-id="b0566-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="b0566-112">Unidad de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b0566-112">Application Virtualization drive</span></span>  
<span data-ttu-id="b0566-113">La unidad de virtualización de aplicaciones es la unidad predeterminada (Q:\) en el equipo de destino desde el que se ejecutan las aplicaciones con secuencias.</span><span class="sxs-lookup"><span data-stu-id="b0566-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="b0566-114">Archivo ICO</span><span class="sxs-lookup"><span data-stu-id="b0566-114">ICO file</span></span>  
<span data-ttu-id="b0566-115">El archivo de icono en el escritorio del cliente, que se usa para iniciar una aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0566-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="b0566-116">Directorio de instalación</span><span class="sxs-lookup"><span data-stu-id="b0566-116">Installation directory</span></span>  
<span data-ttu-id="b0566-117">El directorio usado por el secuenciador para colocar los archivos de instalación durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="b0566-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="b0566-118">Archivo descriptor de software (OSD) abierto</span><span class="sxs-lookup"><span data-stu-id="b0566-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="b0566-119">Un archivo basado en XML que indica al cliente de App-V cómo recuperar la aplicación secuenciada del servidor de streaming de App-V y cómo ejecutar la aplicación secuenciada en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b0566-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="b0566-120">Directorio raíz del paquete</span><span class="sxs-lookup"><span data-stu-id="b0566-120">Package root directory</span></span>  
<span data-ttu-id="b0566-121">El directorio en el equipo de secuencia en el que se instalan los archivos para el paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0566-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="b0566-122">Este directorio también existe prácticamente en el equipo al que se transmitirá una aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0566-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="b0566-123">Aplicación de secuencia</span><span class="sxs-lookup"><span data-stu-id="b0566-123">Sequenced application</span></span>  
<span data-ttu-id="b0566-124">Una aplicación que ha sido supervisada por el secuenciador, dividida en bloques de características principales y secundarios, transmitida a un equipo de destino que ejecuta el cliente de App-V y ejecuta un entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="b0566-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="b0566-125">Paquete de aplicación de secuencia</span><span class="sxs-lookup"><span data-stu-id="b0566-125">Sequenced application package</span></span>  
<span data-ttu-id="b0566-126">Los archivos que componen una aplicación virtual y permiten que se ejecute una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="b0566-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="b0566-127">Estos archivos se crean después de la secuenciación e incluyen específicamente los archivos **. OSD**, **. SFT**, **. SPRJ**y **. ico** .</span><span class="sxs-lookup"><span data-stu-id="b0566-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="b0566-128">128</span><span class="sxs-lookup"><span data-stu-id="b0566-128">Sequencing</span></span>  
<span data-ttu-id="b0566-129">El proceso de creación de un paquete de aplicación con el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="b0566-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="b0566-130">En este proceso, se supervisa una aplicación, se configuran los métodos abreviados y se crea un paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0566-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="b0566-131">Equipo de secuencias</span><span class="sxs-lookup"><span data-stu-id="b0566-131">Sequencing computer</span></span>  
<span data-ttu-id="b0566-132">El equipo utilizado para secuenciar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0566-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="b0566-133">Aplicación virtual</span><span class="sxs-lookup"><span data-stu-id="b0566-133">Virtual application</span></span>  
<span data-ttu-id="b0566-134">Una aplicación empaquetada por el secuenciador para que se ejecute en un entorno virtual independiente.</span><span class="sxs-lookup"><span data-stu-id="b0566-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="b0566-135">El entorno virtual contiene la información necesaria para ejecutar la aplicación en el cliente sin instalar la aplicación de forma local.</span><span class="sxs-lookup"><span data-stu-id="b0566-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="b0566-136">Bloque de características principal</span><span class="sxs-lookup"><span data-stu-id="b0566-136">Primary feature block</span></span>  
<span data-ttu-id="b0566-137">El contenido mínimo en un paquete de aplicación virtual que es necesario para que una aplicación se ejecute en un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="b0566-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="b0566-138">El contenido del bloque de características principal se identifica durante la fase de aplicación de las secuencias y generalmente consta del contenido de las características de aplicación más usadas.</span><span class="sxs-lookup"><span data-stu-id="b0566-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="b0566-139">Aplicaciones de secuencias</span><span class="sxs-lookup"><span data-stu-id="b0566-139">Sequencing Applications</span></span>


<span data-ttu-id="b0566-140">Existen dos métodos para crear y modificar paquetes de aplicaciones virtuales en su entorno.</span><span class="sxs-lookup"><span data-stu-id="b0566-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="b0566-141">El primer método es mediante el Asistente para **secuenciación** .</span><span class="sxs-lookup"><span data-stu-id="b0566-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="b0566-142">El Asistente para la **secuenciación** le permite crear nuevos o modificar paquetes de aplicaciones virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="b0566-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="b0566-143">Para obtener más información sobre cómo usar el Asistente para **secuenciación** , vea [Cómo secuenciar una nueva aplicación](how-to-sequence-a-new-application.md).</span><span class="sxs-lookup"><span data-stu-id="b0566-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="b0566-144">El segundo método es usando la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b0566-144">The second method is by using the command-line.</span></span> <span data-ttu-id="b0566-145">La línea de comandos le permite crear o modificar paquetes de aplicaciones virtuales existentes mediante el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b0566-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="b0566-146">Para obtener más información sobre cómo usar la línea de comandos, consulte [Cómo administrar aplicaciones virtuales mediante la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="b0566-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="b0566-147">El Asistente para la **secuenciación** proporciona las siguientes funciones para crear paquetes de aplicaciones virtuales:</span><span class="sxs-lookup"><span data-stu-id="b0566-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="b0566-148">**Configuración del paquete**: el Asistente para **secuenciación** solicita la información de configuración del paquete necesaria para completar el archivo descriptor de software abierto (OSD), que es un archivo necesario para iniciar un paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0566-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="b0566-149">**Instalación de aplicaciones**: el Asistente para **secuenciación** recopila información sobre la instalación y la configuración de inicio de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0566-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="b0566-150">Supervisa y registra la información de instalación e inicio asociada a la aplicación para crear los archivos necesarios para un paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="b0566-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="b0566-151">**Inicio**de la aplicación: el Asistente para **secuenciación** recopila información para compilar y ordenar los bloques de código necesarios para realizar el inicio inicial del paquete de la aplicación secuenciada en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="b0566-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="b0566-152">La compilación del bloque de código se conoce como el bloque de características principal.</span><span class="sxs-lookup"><span data-stu-id="b0566-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="b0566-153">Consideraciones de seguridad del transordeno de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b0566-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="b0566-154">El secuenciador de App-V ejecuta todos los servicios detectados en el momento de la secuenciación con la cuenta del sistema local y no aplica los descriptores de seguridad en las solicitudes de control de servicio.</span><span class="sxs-lookup"><span data-stu-id="b0566-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="b0566-155">Si el servicio se instaló con una cuenta de usuario diferente o si los descriptores de seguridad están diseñados para conceder a diferentes grupos de usuarios permisos de servicio específicos, considere detenidamente si el servicio debe virtualizarse.</span><span class="sxs-lookup"><span data-stu-id="b0566-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="b0566-156">En algunos casos, debe instalar el servicio localmente para asegurarse de que se mantiene la seguridad de los servicios previstas.</span><span class="sxs-lookup"><span data-stu-id="b0566-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="b0566-157">**Importante**  Siempre debes guardar paquetes de aplicaciones virtuales en un lugar seguro.</span><span class="sxs-lookup"><span data-stu-id="b0566-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="b0566-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0566-158">Related topics</span></span>


[<span data-ttu-id="b0566-159">Información general sobre el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b0566-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





