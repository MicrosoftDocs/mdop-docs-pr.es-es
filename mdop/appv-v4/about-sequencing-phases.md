---
title: Acerca de las fases de secuenciación
description: Acerca de las fases de secuenciación
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820001"
---
# <span data-ttu-id="02056-103">Acerca de las fases de secuenciación</span><span class="sxs-lookup"><span data-stu-id="02056-103">About Sequencing Phases</span></span>


<span data-ttu-id="02056-104">La secuencia es el proceso mediante el cual se crea un paquete de aplicación secuencial mediante el secuenciador Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="02056-104">Sequencing is the process by which you create a sequenced application package by using the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="02056-105">Durante la secuenciación, el secuenciador supervisa y registra todos los procesos de instalación y configuración de una aplicación y crea los siguientes archivos: ICO, OSD, SFT y SPRJ.</span><span class="sxs-lookup"><span data-stu-id="02056-105">During sequencing, the Sequencer monitors and records all installation and setup processes for an application and creates the following files: ICO, OSD, SFT, and SPRJ.</span></span> <span data-ttu-id="02056-106">Estos archivos contienen toda la información necesaria sobre una aplicación y permiten que esa aplicación se ejecute en un entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="02056-106">These files contain all the necessary information about an application, and they allow that application to run in a virtual environment.</span></span>

<span data-ttu-id="02056-107">Las cuatro fases para secuenciar una aplicación y crear un paquete de aplicación virtual son: instalación, Inicio, personalización y almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="02056-107">The four phases to sequencing an application and creating a virtual application package are installation, launch, customization, and save.</span></span> <span data-ttu-id="02056-108">En la siguiente lista se proporciona información acerca de cada una de las fases:</span><span class="sxs-lookup"><span data-stu-id="02056-108">The following list provides information about each of the phases:</span></span>

1.  <span data-ttu-id="02056-109">**Fase de instalación**: durante la fase de instalación, especifique el nombre del paquete y un comentario asociado opcional que se asociará con el paquete.</span><span class="sxs-lookup"><span data-stu-id="02056-109">**Installation phase**—During the installation phase, you specify the package name and an optional associated comment that will be associated with the package.</span></span> <span data-ttu-id="02056-110">También puede configurar opciones de supervisión avanzadas durante esta fase.</span><span class="sxs-lookup"><span data-stu-id="02056-110">You can also configure advanced monitoring options during this phase.</span></span> <span data-ttu-id="02056-111">Las opciones de supervisión avanzadas incluyen especificar el tamaño del bloque y si se instalarán actualizaciones automáticas durante la supervisión.</span><span class="sxs-lookup"><span data-stu-id="02056-111">Advanced monitoring options include specifying the block size and whether you will install automatic updates during monitoring.</span></span> <span data-ttu-id="02056-112">El secuenciador registra toda la información y todas las configuraciones necesarias para crear un paquete de aplicación virtual, así como el archivo asociado y la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="02056-112">The sequencer records all necessary information and configurations required to create a virtual application package and the associated file and registry settings.</span></span>

    <span data-ttu-id="02056-113">**Importante**  Para ver las opciones avanzadas, seleccione **Mostrar opciones de supervisión avanzadas** en la página **información del paquete** .</span><span class="sxs-lookup"><span data-stu-id="02056-113">**Important** To view the advanced options select **Show Advanced Monitoring Options** on the **Package Information** page.</span></span>

     

2.  <span data-ttu-id="02056-114">**Fase de inicio**: durante la fase de inicio, puede especificar cualquier asociación de archivos necesaria y los descriptores de seguridad que se deben configurar con el paquete.</span><span class="sxs-lookup"><span data-stu-id="02056-114">**Launch phase**—During the launch phase, you can specify any required file associations and security descriptors that should be configured with the package.</span></span> <span data-ttu-id="02056-115">Debe abrir la aplicación tantas veces como sea necesario para garantizar la funcionalidad y la estabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02056-115">You should open the application as many times as necessary to ensure application functionality and stability.</span></span>

3.  <span data-ttu-id="02056-116">**Fase de personalización**: durante la fase de personalización, puede configurar el paquete mediante los archivos. OSD asociados.</span><span class="sxs-lookup"><span data-stu-id="02056-116">**Customization phase**—During the customization phase, you can configure your package by using the associated .osd files.</span></span> <span data-ttu-id="02056-117">Puede especificar si desea que los scripts asociados se ejecuten dentro o fuera del entorno virtual, especificar acciones adicionales que se deben realizar, especificar cómo se ejecutan las secuencias de comandos asociadas (sincrónicamente o asincrónicamente), y especificar cualquier script adicional que deba ejecutarse en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="02056-117">You can specify whether any associated scripts should run inside or outside of the virtual environment, specify additional actions that should be performed, specify how associated scripts run (synchronously or asynchronously), and specify any additional scripts that should be run under the user context.</span></span>

4.  <span data-ttu-id="02056-118">**Guardar fase**: durante la fase de guardado, se crean todos los archivos necesarios para el paquete de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="02056-118">**Save phase**—During the save phase, all required files for the virtual application package are created.</span></span> <span data-ttu-id="02056-119">Los archivos creados son. SPRJ,. SFT,. OSD,. ico,. XML y el archivo de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="02056-119">The files created are .sprj, .sft, .osd, .ico, .xml manifest, and the Windows installer (.msi) file.</span></span>

## <span data-ttu-id="02056-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02056-120">Related topics</span></span>


[<span data-ttu-id="02056-121">Secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="02056-121">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





