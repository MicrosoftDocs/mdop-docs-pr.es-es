---
title: Alta disponibilidad de MBAM 1.0
description: Alta disponibilidad de MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825361"
---
# <span data-ttu-id="1d1ea-103">Alta disponibilidad de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1d1ea-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="1d1ea-104">En este tema se describe cómo configurar una instalación de alta disponibilidad de administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="1d1ea-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="1d1ea-105">Escenarios de alta disponibilidad para MBAM</span><span class="sxs-lookup"><span data-stu-id="1d1ea-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="1d1ea-106">Administración y supervisión de Microsoft BitLocker (MBAM) está diseñada para ser tolerante a errores.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="1d1ea-107">Si un servidor no está disponible, los usuarios no se verán afectados de forma negativa.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="1d1ea-108">Por ejemplo, si el agente de MBAM no se puede conectar al servidor Web de MBAM, no se le pedirá que lo solicite.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="1d1ea-109">Cuando planee su instalación de MBAM, tenga en cuenta las siguientes preocupaciones que pueden afectar a la disponibilidad del servicio MBAM:</span><span class="sxs-lookup"><span data-stu-id="1d1ea-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="1d1ea-110">Cifrado de unidad y contraseña de recuperación: Si no se puede enviar una contraseña de recuperación, el cifrado no se iniciará en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="1d1ea-111">Carga de datos del estado de cumplimiento: Si el servidor que hospeda el servicio informe de estado de cumplimiento no está disponible, los datos de cumplimiento no permanecerán actualizados.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="1d1ea-112">Acceso a la clave de recuperación del servicio de asistencia: Si el servicio de asistencia no puede tener acceso a la información de la base de datos MBAM, no podrá proporcionar claves de recuperación a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="1d1ea-113">Disponibilidad de informes: los informes no estarán disponibles si el servidor que hospeda los informes de cumplimiento y cumplimiento no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="1d1ea-114">La principal preocupación de MBAM alta disponibilidad es la disponibilidad de la recuperación de claves de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="1d1ea-115">Si el servicio de asistencia no puede proporcionar claves de recuperación, los usuarios que están bloqueados no pueden desbloquear sus equipos.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="1d1ea-116">Para evitar este problema, considere la posibilidad de implementar servidores web y bases de datos redundantes para garantizar una alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="1d1ea-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="1d1ea-117">Para obtener más información acerca de la escalabilidad y la alta disponibilidad de MBAM, consulte las notas del producto de la [escalabilidad MBAM](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="1d1ea-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="1d1ea-118">Para obtener instrucciones generales sobre la alta disponibilidad de Microsoft SQL Server, consulte [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="1d1ea-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="1d1ea-119">Para obtener instrucciones generales sobre la disponibilidad y escalabilidad para servidores Web, consulte [disponibilidad y escalabilidad](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="1d1ea-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="1d1ea-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d1ea-120">Related topics</span></span>


[<span data-ttu-id="1d1ea-121">Mantenimiento de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1d1ea-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 





