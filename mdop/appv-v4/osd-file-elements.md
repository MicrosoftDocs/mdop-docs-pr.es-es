---
title: Elementos de archivo OSD
description: Elementos de archivo OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816110"
---
# <span data-ttu-id="79a67-103">Elementos de archivo OSD</span><span class="sxs-lookup"><span data-stu-id="79a67-103">OSD File Elements</span></span>


<span data-ttu-id="79a67-104">El directorio de instalación del secuenciador contiene un archivo de esquema XML, **Softricity. xsd**, que define la estructura válida de un archivo descriptor de software abierto (OSD).</span><span class="sxs-lookup"><span data-stu-id="79a67-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="79a67-105">A continuación se muestran algunos de los elementos de la OSD más usados.</span><span class="sxs-lookup"><span data-stu-id="79a67-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="79a67-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="79a67-106">SOFTPKG</span></span>  
<span data-ttu-id="79a67-107">El elemento raíz del archivo OSD que contiene todos los elementos que definen el paquete de software.</span><span class="sxs-lookup"><span data-stu-id="79a67-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="79a67-108">TE</span><span class="sxs-lookup"><span data-stu-id="79a67-108">CODEBASE</span></span>  
<span data-ttu-id="79a67-109">Información sobre el archivo. SFT de este paquete, incluidos los atributos HREF, FILENAME y GUID.</span><span class="sxs-lookup"><span data-stu-id="79a67-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="79a67-110">Puede editar el atributo HREF si cambia el punto de distribución de este paquete en particular.</span><span class="sxs-lookup"><span data-stu-id="79a67-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="79a67-111">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="79a67-111">OS</span></span>  
<span data-ttu-id="79a67-112">Define en qué sistemas operativos se puede ejecutar esta aplicación en función de los valores establecidos inicialmente en el Asistente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="79a67-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="79a67-113">Este valor solo puede contener los valores definidos en **Softricity. xsd**.</span><span class="sxs-lookup"><span data-stu-id="79a67-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="79a67-114">\ _INTERACTION \ _ALLOWED LOCAL</span><span class="sxs-lookup"><span data-stu-id="79a67-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="79a67-115">Si se establece en TRUE, se habilita la creación de objetos con nombre (eventos, exclusiones mutuas, semáforos, asignaciones de archivos y procesadores de datos) y objetos COM en el espacio de nombres global, en lugar de aislados en un entorno virtual en particular, lo que permite que las aplicaciones virtuales interactúen con las aplicaciones del sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="79a67-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="79a67-116">Ejemplo: &lt; implementación de SOFTPKG &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="79a67-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="79a67-117">&lt;directivas de VIRTUALENV &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="79a67-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="79a67-118">&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; verdadero</span><span class="sxs-lookup"><span data-stu-id="79a67-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="79a67-119">&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="79a67-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="79a67-120">&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="79a67-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="79a67-121">&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="79a67-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="79a67-122">DEPENDENCIAS</span><span class="sxs-lookup"><span data-stu-id="79a67-122">DEPENDENCIES</span></span>  
<span data-ttu-id="79a67-123">Define la composición dinámica de conjuntos (dependencias en otros paquetes) mediante una etiqueta codebase de otro paquete.</span><span class="sxs-lookup"><span data-stu-id="79a67-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="79a67-124">Ejemplo: &lt; dependencias de &gt; &lt; código base href = "rtsps://Server/package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" mandato = "false"/ &gt; &lt; /DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="79a67-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="79a67-125">NOMBRE DEL PAQUETE</span><span class="sxs-lookup"><span data-stu-id="79a67-125">PACKAGE NAME</span></span>  
<span data-ttu-id="79a67-126">Nombre común del paquete especificado en la página de información del **paquete** del asistente de secuenciación, que permite especificar un nombre único para una aplicación de secuencia que contiene varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="79a67-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="79a67-127">CORTESÍA</span><span class="sxs-lookup"><span data-stu-id="79a67-127">TITLE</span></span>  
<span data-ttu-id="79a67-128">Nombre descriptivo opcional de la aplicación que va a secuenciar.</span><span class="sxs-lookup"><span data-stu-id="79a67-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="79a67-129">EXTRACCIÓN</span><span class="sxs-lookup"><span data-stu-id="79a67-129">ABSTRACT</span></span>  
<span data-ttu-id="79a67-130">Descripción breve del paquete de software introducido en el campo **comentarios** en la página de **información** del asistente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="79a67-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="79a67-131">Un procedimiento recomendado es especificar información como el sistema operativo y el nivel de Service Pack de la estación de trabajo del secuenciador, la versión del secuenciador y el nombre del ingeniero de secuencias.</span><span class="sxs-lookup"><span data-stu-id="79a67-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="79a67-132">SECUENCIAS</span><span class="sxs-lookup"><span data-stu-id="79a67-132">SCRIPT</span></span>  
<span data-ttu-id="79a67-133">Define eventos específicos con scripts que se producirán durante el inicio, el apagado o la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="79a67-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="79a67-134">ADMIN \ _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="79a67-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="79a67-135">Lista de todos los métodos abreviados definidos en el asistente.</span><span class="sxs-lookup"><span data-stu-id="79a67-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="79a67-136">ADMIN \ _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="79a67-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="79a67-137">Lista de los tipos de archivo especificados en el asistente.</span><span class="sxs-lookup"><span data-stu-id="79a67-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="79a67-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79a67-138">Related topics</span></span>


[<span data-ttu-id="79a67-139">Acerca de la pestaña OSD</span><span class="sxs-lookup"><span data-stu-id="79a67-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





