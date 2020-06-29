---
title: Planificación de la implementación de DaRT 7.0
description: Planificación de la implementación de DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821320"
---
# <span data-ttu-id="72a2a-103">Planificación de la implementación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="72a2a-103">Planning to Deploy DaRT 7.0</span></span>


<span data-ttu-id="72a2a-104">Hay varias configuraciones de implementación y requisitos previos diferentes que debe tener en cuenta antes de crear el plan de implementación.</span><span class="sxs-lookup"><span data-stu-id="72a2a-104">There are a number of different deployment configurations and prerequisites that you must consider before you create your deployment plan.</span></span> <span data-ttu-id="72a2a-105">Esta sección incluye información que puede ayudarle a recopilar la información que necesita para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="72a2a-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

<span data-ttu-id="72a2a-106">Tenga en cuenta lo siguiente cuando planee su instalación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7:</span><span class="sxs-lookup"><span data-stu-id="72a2a-106">Consider the following when you plan your Microsoft Diagnostics and Recovery Toolset (DaRT)7 installation:</span></span>

-   <span data-ttu-id="72a2a-107">Al instalar DaRT, puede instalar toda la funcionalidad en un equipo de administrador de ti donde realizará todas las tareas asociadas con la ejecución de DaRT.</span><span class="sxs-lookup"><span data-stu-id="72a2a-107">When you install DaRT, you can either install all functionality on an IT administrator computer where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="72a2a-108">También puede instalar la funcionalidad de DaRT que crea la imagen de recuperación en el PC administrador de ti.</span><span class="sxs-lookup"><span data-stu-id="72a2a-108">Or you can install only the DaRT functionality that creates the recovery image on the IT administrator computer.</span></span> <span data-ttu-id="72a2a-109">Después, instale la funcionalidad que se usa para ejecutar DaRT, como el **visor de conexión remota DART** y **Crash Analyzer**, en un equipo agente de asistencia.</span><span class="sxs-lookup"><span data-stu-id="72a2a-109">Then, install the functionality used to run DaRT, such as the **DaRT Remote Connection Viewer** and **Crash Analyzer**, on a helpdesk agent computer.</span></span>

-   <span data-ttu-id="72a2a-110">Para poder ejecutar DaRT de forma remota, asegúrese de que el equipo del agente de asistencia y todos los equipos de los que pueda estar solucionando problemas estén en la misma red.</span><span class="sxs-lookup"><span data-stu-id="72a2a-110">To be able to run DaRT remotely, make sure that the helpdesk agent computer and all computers that you might be troubleshooting remotely are on the same network.</span></span>

-   <span data-ttu-id="72a2a-111">Antes de implementar DaRT en producción, puede crear primero un entorno de laboratorio para pruebas.</span><span class="sxs-lookup"><span data-stu-id="72a2a-111">Before you roll out DaRT into production, you can first build a lab environment for testing.</span></span> <span data-ttu-id="72a2a-112">Un laboratorio de pruebas debe incluir un mínimo de dos equipos, uno para actuar como el equipo del agente de soporte técnico y administrador de ti y otro para actuar como un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="72a2a-112">A test lab should include a minimum of two computers, one to act as the IT administrator/helpdesk agent computer and one to act as an end-user computer.</span></span> <span data-ttu-id="72a2a-113">O bien, puede usar tres equipos en el laboratorio si desea separar las responsabilidades de administrador de TI de las del agente de asistencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="72a2a-113">Or, you can use three computers in your lab if you want to separate the IT administrator responsibilities from those of the helpdesk agent.</span></span>

## <span data-ttu-id="72a2a-114">Revisar las configuraciones compatibles</span><span class="sxs-lookup"><span data-stu-id="72a2a-114">Review the supported configurations</span></span>


<span data-ttu-id="72a2a-115">Debe revisar la información de configuración admitida de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 para confirmar que los equipos que ha seleccionado para la instalación de cliente o de características cumplen con los requisitos mínimos de hardware y sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="72a2a-115">You should review the Microsoft Diagnostics and Recovery Toolset (DaRT)7 Supported Configurations information to confirm that the computers you have selected for client or feature installation meet the minimum hardware and operating system requirements.</span></span>

[<span data-ttu-id="72a2a-116">Configuraciones admitidas de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="72a2a-116">DaRT 7.0 Supported Configurations</span></span>](dart-70-supported-configurations-dart-7.md)

## <span data-ttu-id="72a2a-117">Plan para crear la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="72a2a-117">Plan for creating the DaRT recovery image</span></span>


<span data-ttu-id="72a2a-118">Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen.</span><span class="sxs-lookup"><span data-stu-id="72a2a-118">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="72a2a-119">Cuando tome esta decisión, recuerde que es posible que los usuarios finales tengan acceso ocasionalmente a las diversas herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="72a2a-119">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="72a2a-120">Cuando cree la imagen de recuperación, también deberá especificar si desea incluir controladores o archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="72a2a-120">When you create the recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="72a2a-121">Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="72a2a-121">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="72a2a-122">Debe tener en cuenta los requisitos previos y otras recomendaciones de planificación adicionales para crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="72a2a-122">You should be aware of the prerequisites and other additional planning recommendations for creating the DaRT recovery image.</span></span>

[<span data-ttu-id="72a2a-123">Planificación de creación de imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="72a2a-123">Planning to Create the DaRT 7.0 Recovery Image</span></span>](planning-to-create-the-dart-70-recovery-image.md)

## <span data-ttu-id="72a2a-124">Plan para guardar e implementar la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="72a2a-124">Plan for saving and deploying the DaRT recovery image</span></span>


<span data-ttu-id="72a2a-125">Se pueden usar varios métodos para guardar e implementar la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="72a2a-125">Several methods can be used to save and deploy the DaRT recovery image.</span></span> <span data-ttu-id="72a2a-126">Cuando determine el método que va a usar, tenga en cuenta las ventajas y desventajas de cada uno.</span><span class="sxs-lookup"><span data-stu-id="72a2a-126">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="72a2a-127">Además, tenga en cuenta cómo desea usar DaRT en su empresa.</span><span class="sxs-lookup"><span data-stu-id="72a2a-127">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="72a2a-128">**Nota:**  Es posible que desee usar más de un método de su organización.</span><span class="sxs-lookup"><span data-stu-id="72a2a-128">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="72a2a-129">Por ejemplo, puede arrancar en DaRT desde una partición remota para la mayoría de las situaciones y tener una unidad flash USB disponible en caso de que el equipo del usuario final no pueda conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="72a2a-129">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

[<span data-ttu-id="72a2a-130">Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="72a2a-130">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## <span data-ttu-id="72a2a-131">Otros recursos para planificar la implementación de DaRT</span><span class="sxs-lookup"><span data-stu-id="72a2a-131">Other resources for Planning to Deploy DaRT</span></span>


[<span data-ttu-id="72a2a-132">Planificación para DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="72a2a-132">Planning for DaRT 7.0</span></span>](planning-for-dart-70-new-ia.md)

 

 





