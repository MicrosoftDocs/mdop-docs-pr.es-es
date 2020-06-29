---
title: Arquitectura de alto nivel de App-V 5.1
description: Arquitectura de alto nivel de App-V 5.1
author: dansimp
ms.assetid: 90406361-55b8-40b7-85c0-449436789d4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8044c6ae9af4673ec12b47cf3b8fa73a134d9cca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814519"
---
# <span data-ttu-id="7f22d-103">Arquitectura de alto nivel de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7f22d-103">High Level Architecture for App-V 5.1</span></span>


<span data-ttu-id="7f22d-104">Use la siguiente información para que le resulte más fácil simplificar la implementación de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="7f22d-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

## <span data-ttu-id="7f22d-105">Descripción general de la arquitectura</span><span class="sxs-lookup"><span data-stu-id="7f22d-105">Architecture Overview</span></span>


<span data-ttu-id="7f22d-106">Una implementación típica de App-V 5,1 consta de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7f22d-106">A typical App-V 5.1 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7f22d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7f22d-107">Element</span></span></th>
<th align="left"><span data-ttu-id="7f22d-108">Más información</span><span class="sxs-lookup"><span data-stu-id="7f22d-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7f22d-109">Servidor de administración de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7f22d-109">App-V 5.1 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7f22d-110">El servidor de administración de App-V 5,1 proporciona una funcionalidad de administración general para la infraestructura de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7f22d-110">The App-V 5.1 Management server provides overall management functionality for the App-V 5.1 infrastructure.</span></span> <span data-ttu-id="7f22d-111">Además, puede instalar más de una instancia del servidor de administración en su entorno, lo que ofrece las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="7f22d-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="7f22d-112">Tolerancia a errores y alta disponibilidad: la instalación y la configuración del servidor de administración de App-V 5,1 en dos equipos diferentes puede ayudar en situaciones en las que uno de los servidores no está disponible o desconectado.</span><span class="sxs-lookup"><span data-stu-id="7f22d-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.1 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="7f22d-113">También puede ayudar a aumentar la disponibilidad de App-V 5,1 instalando el servidor de administración en varios equipos.</span><span class="sxs-lookup"><span data-stu-id="7f22d-113">You can also help increase App-V 5.1 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="7f22d-114">En este escenario, también se debe tener en cuenta un equilibrador de carga de red para equilibrar las solicitudes del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f22d-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="7f22d-115">Escalabilidad: puede agregar servidores de administración adicionales según sea necesario para admitir una carga elevada, por ejemplo, puede instalar varios servidores detrás de un equilibrador de carga.</span><span class="sxs-lookup"><span data-stu-id="7f22d-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7f22d-116">Servidor de publicación de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7f22d-116">App-V 5.1 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7f22d-117">El servidor de publicación de App-V 5,1 proporciona una funcionalidad para el hospedaje de aplicaciones virtuales y la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="7f22d-117">The App-V 5.1 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="7f22d-118">El servidor de publicación no requiere una conexión de base de datos y admite los siguientes protocolos:</span><span class="sxs-lookup"><span data-stu-id="7f22d-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="7f22d-119">HTTP y HTTPS</span><span class="sxs-lookup"><span data-stu-id="7f22d-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="7f22d-120">También puede mejorar la disponibilidad de App-V 5,1 instalando el servidor de publicación en varios equipos.</span><span class="sxs-lookup"><span data-stu-id="7f22d-120">You can also help increase App-V 5.1 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="7f22d-121">También se debe tener en cuenta un equilibrador de carga de red para que las solicitudes del servidor estén equilibradas.</span><span class="sxs-lookup"><span data-stu-id="7f22d-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7f22d-122">Servidor de informes de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7f22d-122">App-V 5.1 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7f22d-123">El servidor de informes de App-V 5,1 permite que los usuarios autorizados ejecuten y vean informes existentes de App-V 5,1 e informes ad hoc que pueden ayudarle a administrar la infraestructura de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7f22d-123">The App-V 5.1 Reporting server enables authorized users to run and view existing App-V 5.1 reports and ad hoc reports that can help them manage the App-V 5.1 infrastructure.</span></span> <span data-ttu-id="7f22d-124">El servidor de informes requiere una conexión a la base de datos de informes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7f22d-124">The Reporting server requires a connection to the App-V 5.1 reporting database.</span></span> <span data-ttu-id="7f22d-125">También puede mejorar la disponibilidad de App-V 5,1 instalando el servidor de informes en varios equipos.</span><span class="sxs-lookup"><span data-stu-id="7f22d-125">You can also help increase App-V 5.1 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="7f22d-126">También se debe tener en cuenta un equilibrador de carga de red para que las solicitudes del servidor estén equilibradas.</span><span class="sxs-lookup"><span data-stu-id="7f22d-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7f22d-127">Cliente de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7f22d-127">App-V 5.1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="7f22d-128">El cliente de App-V 5,1 permite que los paquetes creados con App-V 5,1 se ejecuten en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="7f22d-128">The App-V 5.1 client enables packages created using App-V 5.1 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7f22d-129">**Nota:**  Si está usando App-V 5,1 con distribución electrónica de software (ESD), no es necesario que use el servidor de administración de App-V 5,1; sin embargo, puede seguir usando la funcionalidad de creación de informes y transmisión de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7f22d-129">**Note** If you are using App-V 5.1 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.1 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.1.</span></span>

 






## <span data-ttu-id="7f22d-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f22d-130">Related topics</span></span>


[<span data-ttu-id="7f22d-131">Introducción a App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7f22d-131">Getting Started with App-V 5.1</span></span>](getting-started-with-app-v-51.md)

 

 





