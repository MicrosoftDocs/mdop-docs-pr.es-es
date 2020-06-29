---
title: Mantenimiento de MBAM 1.0
description: Mantenimiento de MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825771"
---
# <span data-ttu-id="74196-103">Mantenimiento de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74196-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="74196-104">Después de completar todos los planes necesarios y, a continuación, implementar Microsoft BitLocker Administration and Monitoring (MBAM), puede configurar MBAM para que se ejecute de forma muy disponible mientras lo usa para administrar las operaciones de cifrado de BitLocker de la empresa.</span><span class="sxs-lookup"><span data-stu-id="74196-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="74196-105">En la información de esta sección se describen las opciones de alta disponibilidad para MBAM, así como la manera de mover MBAM características de servidor si es necesario.</span><span class="sxs-lookup"><span data-stu-id="74196-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="74196-106">Paquete de administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="74196-106">MBAM Management Pack</span></span>


<span data-ttu-id="74196-107">El MicrosoftSystemCenterOperationsManager Management Pack para MBAM está disponible para su descarga desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="74196-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="74196-108">Este módulo de administración supervisa las interacciones críticas de la infraestructura del servidor, como las conexiones entre las bases de datos y los servicios web y las llamadas operativas entre sitios web y su servicio Web de soporte.</span><span class="sxs-lookup"><span data-stu-id="74196-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="74196-109">También carga las solicitudes entre los clientes de escritorio y sus puntos de conexión de servicio Web de recepción respectivos.</span><span class="sxs-lookup"><span data-stu-id="74196-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="74196-110">Módulo de administración de supervisión y administración de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="74196-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="74196-111">Garantizar la alta disponibilidad de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="74196-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="74196-112">MBAM está diseñado para ser tolerante a errores.</span><span class="sxs-lookup"><span data-stu-id="74196-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="74196-113">Si un servidor no está disponible, los usuarios no se verán afectados de forma negativa.</span><span class="sxs-lookup"><span data-stu-id="74196-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="74196-114">La información de esta sección se puede usar para configurar una instalación MBAM de alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="74196-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="74196-115">Alta disponibilidad de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74196-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="74196-116">Mover características de MBAM 1,0 a otro servidor</span><span class="sxs-lookup"><span data-stu-id="74196-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="74196-117">Cuando tenga que mover una característica de MBAM Server de un equipo servidor a otro, existe un orden específico y obligatorios pasos que debe seguir para evitar la pérdida de productividad o datos.</span><span class="sxs-lookup"><span data-stu-id="74196-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="74196-118">En esta sección se describen los pasos que debe seguir para mover una o más características del servidor de MBAM a un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="74196-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="74196-119">Cómo mover funciones de MBAM 1.0 a otro equipo</span><span class="sxs-lookup"><span data-stu-id="74196-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="74196-120">Otros recursos para mantener MBAM</span><span class="sxs-lookup"><span data-stu-id="74196-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="74196-121">Operaciones para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74196-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





