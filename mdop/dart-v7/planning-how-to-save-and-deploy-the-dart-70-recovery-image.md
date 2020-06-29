---
title: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0
description: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822800"
---
# <span data-ttu-id="ad735-103">Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ad735-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="ad735-104">Use la información de esta sección cuando planea guardar e implementar la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="ad735-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="ad735-105">Planear cómo guardar e implementar la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="ad735-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="ad735-106">Puede guardar e implementar la imagen de recuperación de DaRT mediante los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="ad735-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="ad735-107">Cuando determine el método que va a usar, tenga en cuenta las ventajas y desventajas de cada uno.</span><span class="sxs-lookup"><span data-stu-id="ad735-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="ad735-108">Además, tenga en cuenta cómo desea usar DaRT en su empresa.</span><span class="sxs-lookup"><span data-stu-id="ad735-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="ad735-109">**Nota:**  Es posible que desee usar más de un método de su organización.</span><span class="sxs-lookup"><span data-stu-id="ad735-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="ad735-110">Por ejemplo, puede arrancar en DaRT desde una partición remota para la mayoría de las situaciones y tener una unidad flash USB disponible en caso de que el equipo del usuario final no pueda conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="ad735-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="ad735-111">En la tabla siguiente se muestran algunas de las ventajas y desventajas de cada método de uso de DaRT en su organización.</span><span class="sxs-lookup"><span data-stu-id="ad735-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad735-112">Método para arrancar DaRT</span><span class="sxs-lookup"><span data-stu-id="ad735-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="ad735-113">Ventajas</span><span class="sxs-lookup"><span data-stu-id="ad735-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="ad735-114">Desventajas</span><span class="sxs-lookup"><span data-stu-id="ad735-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad735-115">Desde un CD o DVD</span><span class="sxs-lookup"><span data-stu-id="ad735-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-116">Es compatible con escenarios en los que el registro de inicio maestro (MBR) está dañado y no se puede obtener acceso al disco duro.</span><span class="sxs-lookup"><span data-stu-id="ad735-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="ad735-117">También admite casos en los que no hay conexión de red.</span><span class="sxs-lookup"><span data-stu-id="ad735-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="ad735-118">Esto está más familiarizado con los usuarios de versiones anteriores de DaRT, y se puede grabar un CD o DVD directamente desde el <strong> Asistente de imagen de recuperación de DART </strong> .</span><span class="sxs-lookup"><span data-stu-id="ad735-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-119">Requiere que la persona con acceso al CD o DVD se encuentre físicamente en el equipo del usuario final para iniciar en DaRT.</span><span class="sxs-lookup"><span data-stu-id="ad735-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad735-120">Desde una unidad flash USB (UFD)</span><span class="sxs-lookup"><span data-stu-id="ad735-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-121">Proporciona las mismas ventajas que el inicio desde un CD o DVD y también proporciona compatibilidad con equipos que no tienen unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="ad735-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-122">Requiere formatear la UFD antes de poder usarla para arrancar DaRT.</span><span class="sxs-lookup"><span data-stu-id="ad735-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="ad735-123">También requiere que alguien con acceso a la UFD esté físicamente en el equipo del usuario final para iniciar en DaRT.</span><span class="sxs-lookup"><span data-stu-id="ad735-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad735-124">Desde una partición remota (de red)</span><span class="sxs-lookup"><span data-stu-id="ad735-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-125">Le permite arrancar DaRT sin necesidad de un CD, DVD o UFD.</span><span class="sxs-lookup"><span data-stu-id="ad735-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="ad735-126">También permite actualizaciones de DaRT fácilmente, ya que solo se puede actualizar una ubicación de archivo.</span><span class="sxs-lookup"><span data-stu-id="ad735-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-127">No funciona si el equipo del usuario final no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="ad735-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="ad735-128">Ampliamente disponible para los usuarios finales y es posible que necesite otras consideraciones de seguridad al crear la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ad735-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad735-129">Desde una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="ad735-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-130">Le permite arrancar DaRT sin necesidad de un CD, DVD o UFD que incluya instancias en las que no haya conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="ad735-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="ad735-131">Además, puede implementarse y administrarse como parte del proceso estándar de la imagen de Windows mediante herramientas de distribución automatizadas, como Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ad735-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad735-132">Al actualizar DaRT, debe actualizar todos los equipos de su empresa en lugar de solo una partición (en la red) o un dispositivo (CD, DVD o UFD).</span><span class="sxs-lookup"><span data-stu-id="ad735-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ad735-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad735-133">Related topics</span></span>


[<span data-ttu-id="ad735-134">Planificación de la implementación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ad735-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





