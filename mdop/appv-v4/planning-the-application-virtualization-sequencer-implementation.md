---
title: Planificación de la implementación del secuenciador de virtualización de aplicaciones
description: Planificación de la implementación del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815891"
---
# <span data-ttu-id="97398-103">Planificación de la implementación del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="97398-103">Planning the Application Virtualization Sequencer Implementation</span></span>


<span data-ttu-id="97398-104">Secuenciación, el proceso que usa la virtualización de aplicaciones para crear aplicaciones virtuales y paquetes de aplicaciones, requiere el uso de un equipo con el software Application Virtualization Sequencer instalado.</span><span class="sxs-lookup"><span data-stu-id="97398-104">Sequencing, the process used by Application Virtualization to create virtual applications and application packages, requires the use of a computer with the Application Virtualization Sequencer software installed.</span></span>

<span data-ttu-id="97398-105">Durante el proceso de secuenciación, el secuenciador se coloca en el modo de monitor y la aplicación que se va a secuenciar se instala en el equipo de secuencias.</span><span class="sxs-lookup"><span data-stu-id="97398-105">During the sequencing process, the Sequencer is placed in monitor mode, and the application to be sequenced is installed on the sequencing computer.</span></span> <span data-ttu-id="97398-106">A continuación, se inicia la aplicación de secuencia y las funciones más importantes y más usadas se ejecutan para que el proceso de supervisión pueda configurar el bloque de características principal, que contiene el contenido mínimo de un paquete de aplicación que es necesario para que se ejecute una aplicación.</span><span class="sxs-lookup"><span data-stu-id="97398-106">Next, the sequenced application is started, and its most important and commonly used functions are exercised so that the monitoring process can configure the primary feature block, which contains the minimum content in an application package that is necessary for an application to run.</span></span> <span data-ttu-id="97398-107">Cuando se completan estos pasos, se detiene el modo de supervisión y la aplicación de secuencia se guarda y se prueba para comprobar que la operación es correcta.</span><span class="sxs-lookup"><span data-stu-id="97398-107">When these steps are complete, monitoring mode is stopped and the sequenced application is saved and tested to verify correct operation.</span></span>

<span data-ttu-id="97398-108">Cuando decida qué aplicaciones elegir para la secuenciación, recuerde que determinadas aplicaciones no se pueden secuenciar.</span><span class="sxs-lookup"><span data-stu-id="97398-108">When deciding which applications to choose for sequencing, remember that certain applications cannot be sequenced.</span></span> <span data-ttu-id="97398-109">Estas incluyen determinadas partes del sistema operativo Windows, como Internet Explorer, controladores de dispositivos y aplicaciones que inician servicios en el momento del inicio.</span><span class="sxs-lookup"><span data-stu-id="97398-109">These include certain parts of the Windows operating system, such as Internet Explorer, device drivers, and applications that start services at boot time.</span></span>

<span data-ttu-id="97398-110">Para obtener información paso a paso sobre cómo instalar el secuenciador, vea [Cómo instalar Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="97398-110">For step-by-step information about installing the Sequencer, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span>

<span data-ttu-id="97398-111">**Importante**  El equipo de seguridad de la empresa debe revisar y aprobar todo el plan de proceso de secuencia.</span><span class="sxs-lookup"><span data-stu-id="97398-111">**Important** The entire sequencing process plan should be reviewed and approved by your corporate security team.</span></span> <span data-ttu-id="97398-112">Normalmente, las operaciones de secuenciar se mantendrían separadas del entorno de producción en un laboratorio.</span><span class="sxs-lookup"><span data-stu-id="97398-112">Sequencer operations would usually be kept separate from the production environment in a lab.</span></span> <span data-ttu-id="97398-113">Esto puede ser tan simple o exhaustivo como sea necesario, en función de los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="97398-113">This can be as simple or as comprehensive as necessary, based on your business requirements.</span></span> <span data-ttu-id="97398-114">Los equipos de secuencias necesitarán conectividad con la red corporativa para copiar paquetes finalizados en los servidores de producción.</span><span class="sxs-lookup"><span data-stu-id="97398-114">The sequencing computers will need connectivity to the corporate network to copy finished packages over to the production servers.</span></span> <span data-ttu-id="97398-115">Sin embargo, dado que por lo general funcionan sin protección antivirus, no deben estar en la red corporativa desprotegida, por ejemplo, es posible que pueda trabajar detrás de un firewall o en un segmento de red aislado.</span><span class="sxs-lookup"><span data-stu-id="97398-115">However, because they are typically operated without antivirus protection, they must not be on the corporate network unprotected—for example, you might be able to operate behind a firewall or on an isolated network segment.</span></span> <span data-ttu-id="97398-116">El uso de equipos virtuales configurados para compartir una red virtual aislada también puede ser un enfoque aceptable.</span><span class="sxs-lookup"><span data-stu-id="97398-116">Using Virtual Machines configured to share an isolated virtual network might also be an acceptable approach.</span></span> <span data-ttu-id="97398-117">Siga las políticas de seguridad corporativas para resolver esta situación de manera segura.</span><span class="sxs-lookup"><span data-stu-id="97398-117">Follow your corporate security policies to safely address this situation.</span></span>

 

<span data-ttu-id="97398-118">Los pasos clave para planear el proceso de secuenciación son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="97398-118">Key steps for planning the sequencing process include the following:</span></span>

-   <span data-ttu-id="97398-119">Considere el número de aplicaciones que espera procesar cada mes, el tamaño de esas aplicaciones y agregue un límite para las futuras actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="97398-119">Consider the number of applications you expect to process each month, the size of those applications, and add an allowance for sequencing future updates.</span></span> <span data-ttu-id="97398-120">Los paquetes pueden tener hasta 4 GB de tamaño, comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="97398-120">Packages can be up to 4 GB in size, compressed or uncompressed.</span></span>

-   <span data-ttu-id="97398-121">Prepare y documente un proceso metódico y repetible para que su organización siga la secuencia de cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="97398-121">Prepare and document a methodical, repeatable process for your organization to follow when sequencing each application.</span></span> <span data-ttu-id="97398-122">Esto debe incluir el uso de una lista de comprobación para cada ejecución, así como un proceso de control de versiones.</span><span class="sxs-lookup"><span data-stu-id="97398-122">This should include the use of a checklist for each run, as well as a version control process.</span></span> <span data-ttu-id="97398-123">El uso de un registro de seguimiento para cada aplicación de secuencia también es muy útil a la hora de investigar posibles problemas técnicos con un paquete.</span><span class="sxs-lookup"><span data-stu-id="97398-123">The use of a tracking log for each sequenced application is also very helpful when investigating possible technical issues with a package.</span></span>

-   <span data-ttu-id="97398-124">Para las aplicaciones en secuencia, use equipos de alto rendimiento optimizados para procesar el rendimiento, con al menos 4 GB de RAM y una CPU rápida (3 GHz o más rápido).</span><span class="sxs-lookup"><span data-stu-id="97398-124">For sequencing applications, use high-performing computers that are optimized for processing throughput, with at least 4 GB of RAM and a fast CPU (3 GHz or faster).</span></span> <span data-ttu-id="97398-125">Los discos duros rápidos y el uso de volúmenes de disco independientes también pueden mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="97398-125">Fast hard disks and the use of separate disk volumes can also improve performance.</span></span> <span data-ttu-id="97398-126">Las máquinas virtuales son ideales para la secuenciación porque se pueden restablecer fácilmente, o bien puede usar un equipo físico con una imagen limpia en una partición local para permitir una nueva creación de imágenes después de completar cada operación de secuencia de paquetes.</span><span class="sxs-lookup"><span data-stu-id="97398-126">Virtual Machines are ideal for sequencing because they can easily be reset, or you can use a physical computer with a clean image on a local partition to enable rapid re-imaging after each package sequencing operation has been completed.</span></span>

    <span data-ttu-id="97398-127">**Importante**  No se admite la ejecución del secuenciador de App-V en el modo seguro.</span><span class="sxs-lookup"><span data-stu-id="97398-127">**Important** Running the App-V sequencer in Safe Mode is not supported.</span></span>

     

-   <span data-ttu-id="97398-128">Compruebe que comprende el entorno operativo de la aplicación secuenciada, incluidos los elementos de integración como Microsoft Office o Java Runtime Environment, porque con frecuencia determinará si se tiene que instalar algo en el equipo de secuenciación antes de realizar la secuenciación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="97398-128">Verify that you understand the sequenced application’s operating environment, including integration elements such as Microsoft Office or the Java Runtime Environment, because this will often determine whether anything has to be installed on the sequencing computer prior to sequencing the application.</span></span>

-   <span data-ttu-id="97398-129">Asegúrese de que cada nueva operación de secuenciación siempre comienza con una imagen base limpia.</span><span class="sxs-lookup"><span data-stu-id="97398-129">Ensure that each new sequencing operation always starts with a clean base image.</span></span> <span data-ttu-id="97398-130">Asegúrese de que el equipo de secuenciación se ha restablecido, ya sea mediante la restauración de la imagen guardada en un equipo físico o mediante el reinicio de una máquina virtual después de descartar todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="97398-130">Make sure that the sequencing computer has been reset, either by restoring the saved image to a physical computer or by restarting a virtual machine after discarding all changes.</span></span> <span data-ttu-id="97398-131">La imagen base debe tener las últimas actualizaciones aplicadas desde Windows Update antes de guardarlas.</span><span class="sxs-lookup"><span data-stu-id="97398-131">The base image should have the latest updates applied from Windows Update before saving.</span></span>

-   <span data-ttu-id="97398-132">Desactive cualquier cosa en el equipo de secuencias que pueda interferir con el proceso de supervisión de la instalación, tales escáneres antivirus y Windows Update, debido a que es esencial disponer de una plataforma estable durante el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="97398-132">Turn off anything on the sequencing computer that can interfere with the install monitoring process, such antivirus scanners and Windows Update, because having a stable platform during the sequencing process is essential.</span></span> <span data-ttu-id="97398-133">Dado que este paso produce riesgos de seguridad considerables, asegúrese de que se tomen las precauciones correctas para proteger el equipo y la red, así como el paquete de aplicación secuenciado.</span><span class="sxs-lookup"><span data-stu-id="97398-133">Because this step incurs significant security risks, ensure that the correct precautions are taken to protect the computer and network as well as the sequenced application package.</span></span> <span data-ttu-id="97398-134">Le recomendamos que realice un examen antivirus de paquetes de aplicaciones antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="97398-134">We recommend that you do an antivirus scan of application packages before sequencing them.</span></span>

-   <span data-ttu-id="97398-135">Incluya un proceso detallado para probar cada aplicación después de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="97398-135">Include a detailed process for testing each application after sequencing.</span></span> <span data-ttu-id="97398-136">La prueba de la aplicación secuenciada determinará si funciona correctamente y es una parte esencial del proceso antes de implementar la aplicación virtualizada para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="97398-136">Testing the sequenced application will determine whether it functions correctly and is an essential part of the process prior to deploying the virtualized application to end users.</span></span> <span data-ttu-id="97398-137">Como paso final de las pruebas antes de la implementación a escala amplia a los usuarios finales, también debe planear una implementación piloto en un grupo de pruebas.</span><span class="sxs-lookup"><span data-stu-id="97398-137">As the final step in testing prior to wide-scale deployment to end users, you should also plan for a pilot deployment to a test group.</span></span>

-   <span data-ttu-id="97398-138">Cuando pruebe aplicaciones de secuencia, elija equipos del mismo tipo y ejecute los mismos sistemas operativos que se usan en el entorno de producción de la empresa.</span><span class="sxs-lookup"><span data-stu-id="97398-138">When testing sequenced applications, choose computer equipment of the same type and running the same operating systems that are in use in the company production environment.</span></span> <span data-ttu-id="97398-139">Siempre que estén configurados correctamente, se pueden usar máquinas virtuales o máquinas físicas.</span><span class="sxs-lookup"><span data-stu-id="97398-139">As long as they are configured properly, either virtual machines or physical machines can be used.</span></span>

## <span data-ttu-id="97398-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97398-140">Related topics</span></span>


[<span data-ttu-id="97398-141">Requisitos de hardware y software del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="97398-141">Application Virtualization Sequencer Hardware and Software Requirements</span></span>](application-virtualization-sequencer-hardware-and-software-requirements.md)

[<span data-ttu-id="97398-142">Cómo instalar el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="97398-142">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="97398-143">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="97398-143">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="97398-144">Introducción a la seguridad y la protección</span><span class="sxs-lookup"><span data-stu-id="97398-144">Security and Protection Overview</span></span>](security-and-protection-overview.md)

 

 




