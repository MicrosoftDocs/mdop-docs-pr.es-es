---
title: Determinar el método de publicación
description: Determinar el método de publicación
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821680"
---
# <span data-ttu-id="b150e-103">Determinar el método de publicación</span><span class="sxs-lookup"><span data-stu-id="b150e-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="b150e-104">Después de secuenciar una aplicación mediante Application Virtualization Sequencer, tendrá que *publicarla* para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b150e-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="b150e-105">La publicación de la aplicación consiste en ofrecer los iconos, la información de definición del paquete y la ubicación del origen de contenido en cada equipo en el que se haya instalado el cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b150e-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="b150e-106">En la siguiente tabla se describen los métodos de publicación que se admiten al implementar la virtualización de aplicaciones mediante un sistema de distribución de software electrónico (ESD).</span><span class="sxs-lookup"><span data-stu-id="b150e-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b150e-107">Método</span><span class="sxs-lookup"><span data-stu-id="b150e-107">Method</span></span></th>
<th align="left"><span data-ttu-id="b150e-108">Ventajas</span><span class="sxs-lookup"><span data-stu-id="b150e-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="b150e-109">Desventajas</span><span class="sxs-lookup"><span data-stu-id="b150e-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b150e-110">Genere un archivo de Windows Installer durante la secuenciación, como una solución independiente.</span><span class="sxs-lookup"><span data-stu-id="b150e-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b150e-111">Es muy fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="b150e-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="b150e-112">Paquete cargado en la caché de forma local en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="b150e-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="b150e-113">Iconos que se muestran al usuario.</span><span class="sxs-lookup"><span data-stu-id="b150e-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="b150e-114">Similar a la implementación de software tradicional.</span><span class="sxs-lookup"><span data-stu-id="b150e-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="b150e-115">No es necesario que los servidores de streaming sean.</span><span class="sxs-lookup"><span data-stu-id="b150e-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b150e-116">No hay flexibilidad en la ubicación del contenido del paquete en los equipos, la misma ubicación en todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="b150e-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="b150e-117">Debe usar solo agregar o quitar programas o msiexec para quitar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b150e-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="b150e-118">Eliminación y sustitución con la nueva versión necesaria para la actualización de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b150e-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b150e-119">Genera un archivo de Windows Installer durante la secuenciación, que se usa con las propiedades de línea de comandos MODE, LOAD y OVERRIDEURL y el manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="b150e-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b150e-120">Fácil de usar, pero con flexibilidad añadida.</span><span class="sxs-lookup"><span data-stu-id="b150e-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="b150e-121">Iconos que se muestran al usuario.</span><span class="sxs-lookup"><span data-stu-id="b150e-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="b150e-122">SFT el archivo que contiene las aplicaciones puede colocarse en una ubicación de origen de transmisión, con clientes configurados para usar esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="b150e-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b150e-123">Flexibilidad limitada: solo se puede controlar la ubicación del contenido del paquete en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b150e-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="b150e-124">Debe usar solo agregar o quitar programas o msiexec para quitar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b150e-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="b150e-125">Eliminación y sustitución con la nueva versión necesaria para actualizar paquetes, a menos que use el servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="b150e-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b150e-126">Ejecute los comandos de SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="b150e-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b150e-127">Flexibilidad completa: control total de todas las funciones de administración de paquetes.</span><span class="sxs-lookup"><span data-stu-id="b150e-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b150e-128">Los comandos deben incluirse en scripts para usarlos con el sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="b150e-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="b150e-129">Los comandos deben ejecutarse en cada equipo en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="b150e-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="b150e-130">Comprensión detallada del lenguaje de comandos y una planificación precisa.</span><span class="sxs-lookup"><span data-stu-id="b150e-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b150e-131">Para obtener más información sobre cómo usar estos métodos de publicación, vea [Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="b150e-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="b150e-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b150e-132">Related topics</span></span>


[<span data-ttu-id="b150e-133">Determinar el método de streaming</span><span class="sxs-lookup"><span data-stu-id="b150e-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="b150e-134">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="b150e-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="b150e-135">Introducción a escenario basado en la distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="b150e-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="b150e-136">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="b150e-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="b150e-137">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="b150e-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





