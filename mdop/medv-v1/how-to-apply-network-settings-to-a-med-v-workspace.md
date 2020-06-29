---
title: Cómo aplicar la configuración de red en un área de trabajo de MED-V
description: Cómo aplicar la configuración de red en un área de trabajo de MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826520"
---
# <span data-ttu-id="15fc9-103">Cómo aplicar la configuración de red en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="15fc9-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="15fc9-104">Los administradores pueden definir la configuración de red para cada área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="15fc9-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="15fc9-105">Todas las opciones de configuración de red se configuran en el módulo **Directiva** , en la pestaña **red** .</span><span class="sxs-lookup"><span data-stu-id="15fc9-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="15fc9-106">Para aplicar la configuración de red a un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="15fc9-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="15fc9-107">Haga clic en el área de trabajo de MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="15fc9-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="15fc9-108">En el panel **red** , configure los valores como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="15fc9-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="15fc9-109">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="15fc9-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="15fc9-110">Propiedades de red de área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="15fc9-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15fc9-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15fc9-111">Property</span></span></th>
<th align="left"><span data-ttu-id="15fc9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="15fc9-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15fc9-113">Propiedades de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="15fc9-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15fc9-114">Usar la dirección IP del host (NAT) </strong> : el área de trabajo usará NAT para compartir la IP del host para el tráfico saliente.</span><span class="sxs-lookup"><span data-stu-id="15fc9-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="15fc9-115">Usar una dirección IP diferente a la de host (puente) </strong> : el área de trabajo de MED-V tendrá su propia dirección de red, normalmente obtenida a través de DHCP.</span><span class="sxs-lookup"><span data-stu-id="15fc9-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="15fc9-116">Active la <strong> casilla asignar varios adaptadores al área </strong> de trabajo cuando el equipo host tenga varios adaptadores.</span><span class="sxs-lookup"><span data-stu-id="15fc9-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="15fc9-117">Se recomienda usar esta configuración cuando el host se desplaza entre redes diferentes usando distintos adaptadores.</span><span class="sxs-lookup"><span data-stu-id="15fc9-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15fc9-118">Servidor DNS</span><span class="sxs-lookup"><span data-stu-id="15fc9-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15fc9-119">No cambiar </strong> : la configuración de DNS establecida en la máquina virtual del área de trabajo MED-V no se cambiará.</span><span class="sxs-lookup"><span data-stu-id="15fc9-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="15fc9-120">Usar la dirección DNS del host </strong> : la configuración DNS del área de trabajo de MED-V se sincronizará para coincidir con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="15fc9-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="15fc9-121">La sincronización DNS es dinámica.</span><span class="sxs-lookup"><span data-stu-id="15fc9-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="15fc9-122">Se sincroniza periódicamente con el host para que, si se cambia en el host, cambie de forma dinámica en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="15fc9-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="15fc9-123">Usar direcciones DNS específicas </strong> : el área de trabajo de MED-V usará un DNS específico, según se especifique.</span><span class="sxs-lookup"><span data-stu-id="15fc9-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="15fc9-124">En los <strong> </strong> campos principal y <strong> secundario </strong> , escriba las direcciones DNS principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="15fc9-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="15fc9-125">Active la <strong> casilla de verificación anexar direcciones DNS del host </strong> para anexar el host a las direcciones DNS configuradas.</span><span class="sxs-lookup"><span data-stu-id="15fc9-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15fc9-126">Asignar sufijos DNS</span><span class="sxs-lookup"><span data-stu-id="15fc9-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15fc9-127">Asignar los siguientes sufijos </strong> : Seleccione esta casilla para asignar sufijos DNS específicos; en el cuadro, escriba un sufijo o varios sufijos separados por comas.</span><span class="sxs-lookup"><span data-stu-id="15fc9-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="15fc9-128">Anexar sufijos de host </strong> : Seleccione esta casilla para anexar los sufijos de host a la dirección DNS.</span><span class="sxs-lookup"><span data-stu-id="15fc9-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="15fc9-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15fc9-129">Related topics</span></span>


[<span data-ttu-id="15fc9-130">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="15fc9-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="15fc9-131">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="15fc9-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





