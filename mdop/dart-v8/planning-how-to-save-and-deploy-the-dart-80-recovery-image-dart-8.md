---
title: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 8.0
description: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 8.0
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821241"
---
# <span data-ttu-id="62903-103">Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="62903-103">Planning How to Save and Deploy the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="62903-104">Puede guardar e implementar la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 mediante los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="62903-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image by using the following methods.</span></span> <span data-ttu-id="62903-105">Cuando determine el método que va a usar, tenga en cuenta las ventajas y desventajas de cada uno.</span><span class="sxs-lookup"><span data-stu-id="62903-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="62903-106">También debe tener en cuenta la infraestructura y el personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="62903-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="62903-107">Si tiene una infraestructura pequeña, es posible que desee implementar DaRT 8,0 mediante medios extraíbles, ya que la imagen de recuperación siempre estará disponible si la instala en el disco duro local.</span><span class="sxs-lookup"><span data-stu-id="62903-107">If you have a small infrastructure, you might want to deploy DaRT 8.0 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="62903-108">Si su organización usa servicios de dominio de Active Directory (AD DS), es posible que desee implementar imágenes de recuperación como servicio de red con Windows DS.</span><span class="sxs-lookup"><span data-stu-id="62903-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="62903-109">Las imágenes de recuperación siempre están disponibles para cualquier equipo conectado.</span><span class="sxs-lookup"><span data-stu-id="62903-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="62903-110">Puede implementar varias imágenes desde Windows DS y mantenerlas en un solo lugar.</span><span class="sxs-lookup"><span data-stu-id="62903-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="62903-111">**Nota:**  Es posible que desee usar más de un método de su organización.</span><span class="sxs-lookup"><span data-stu-id="62903-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="62903-112">Por ejemplo, puede arrancar en DaRT desde una partición remota para la mayoría de las situaciones y tener una unidad flash USB disponible en caso de que el equipo del usuario final no pueda conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="62903-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="62903-113">En la tabla siguiente se muestran algunas de las ventajas y desventajas de cada método de uso de DaRT en su organización.</span><span class="sxs-lookup"><span data-stu-id="62903-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="62903-114">Método para arrancar DaRT</span><span class="sxs-lookup"><span data-stu-id="62903-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="62903-115">Ventajas</span><span class="sxs-lookup"><span data-stu-id="62903-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="62903-116">Desventajas</span><span class="sxs-lookup"><span data-stu-id="62903-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="62903-117">Medios extraíbles</span><span class="sxs-lookup"><span data-stu-id="62903-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="62903-118">La imagen de recuperación se escribe en un CD, DVD o unidad USB para que el personal de soporte técnico pueda tomar las herramientas de recuperación con ellas en el equipo inestable.</span><span class="sxs-lookup"><span data-stu-id="62903-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="62903-119">Admite escenarios en los que el registro de inicio maestro (MBR) está dañado y no puede tener acceso al disco duro y admite casos en los que no hay conexión de red.</span><span class="sxs-lookup"><span data-stu-id="62903-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="62903-120">Le permite crear varias imágenes de recuperación con diferentes herramientas para proporcionar diferentes niveles de soporte.</span><span class="sxs-lookup"><span data-stu-id="62903-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="62903-121">Proporciona una herramienta integrada para grabar imágenes de recuperación en medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="62903-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="62903-122">Requiere que el personal de soporte técnico esté físicamente en el equipo del usuario final para iniciar en DaRT.</span><span class="sxs-lookup"><span data-stu-id="62903-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="62903-123">Requiere tiempo y mantenimiento para crear varios medios con diferentes configuraciones para los equipos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="62903-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="62903-124">Desde una partición remota (de red)</span><span class="sxs-lookup"><span data-stu-id="62903-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="62903-125">La imagen de recuperación está hospedada en un servidor de arranque de red como servicios de implementación de Windows (Windows DS), que permite a los usuarios o al personal de soporte técnico transmitirlos a equipos a petición.</span><span class="sxs-lookup"><span data-stu-id="62903-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="62903-126">Disponible para todos los equipos que tengan acceso al servidor de arranque de red.</span><span class="sxs-lookup"><span data-stu-id="62903-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="62903-127">Las imágenes de recuperación se hospedan en un servidor central, lo que permite actualizaciones centralizadas.</span><span class="sxs-lookup"><span data-stu-id="62903-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="62903-128">El personal de soporte técnico centralizado puede proporcionar reparaciones mediante conectividad remota.</span><span class="sxs-lookup"><span data-stu-id="62903-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="62903-129">No hay ningún requisito de almacenamiento local en los clientes.</span><span class="sxs-lookup"><span data-stu-id="62903-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="62903-130">Capacidad de crear varias imágenes de recuperación con diferentes herramientas para niveles de asistencia específicos.</span><span class="sxs-lookup"><span data-stu-id="62903-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="62903-131">La necesidad de proteger la infraestructura de Windows DS para garantizar que los usuarios habituales puedan iniciar solo la imagen de recuperación de DaRT y no con el proceso de creación de imágenes de sistema operativo completo.</span><span class="sxs-lookup"><span data-stu-id="62903-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="62903-132">Requiere que el equipo del usuario final esté conectado a la red en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="62903-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="62903-133">Requiere que la imagen de recuperación se conecte a través de la red.</span><span class="sxs-lookup"><span data-stu-id="62903-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="62903-134">Desde una partición de recuperación de la unidad de disco duro local</span><span class="sxs-lookup"><span data-stu-id="62903-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="62903-135">La imagen de recuperación se instala en una unidad de disco duro local, ya sea de forma manual o mediante sistemas electrónicos de distribución de software, como System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="62903-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="62903-136">La imagen de recuperación siempre está disponible porque está preconfigurada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="62903-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="62903-137">El personal de soporte técnico centralizado puede proporcionar asistencia a través de la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="62903-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="62903-138">La imagen de recuperación se administra y se implementa de forma centralizada.</span><span class="sxs-lookup"><span data-stu-id="62903-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="62903-139">Se eliminan las solicitudes de clave de recuperación adicionales en equipos protegidos por el cifrado de unidad BitLocker de Windows.</span><span class="sxs-lookup"><span data-stu-id="62903-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="62903-140">Se necesita almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="62903-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="62903-141">Se recomienda una partición dedicada y sin cifrar para la ubicación de la imagen de recuperación con el fin de reducir el riesgo de una partición de inicio con error.</span><span class="sxs-lookup"><span data-stu-id="62903-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="62903-142">Al actualizar DaRT, debe actualizar todos los equipos de su empresa en lugar de solo una partición (en la red) o un dispositivo extraíble.</span><span class="sxs-lookup"><span data-stu-id="62903-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="62903-143">Se requiere una mayor consideración si implementa la imagen de recuperación después de que se haya habilitado BitLocker.</span><span class="sxs-lookup"><span data-stu-id="62903-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="62903-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62903-144">Related topics</span></span>


[<span data-ttu-id="62903-145">Planificación de la implementación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="62903-145">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





