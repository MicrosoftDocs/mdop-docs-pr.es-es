---
title: Administración avanzada de directivas de grupo
description: Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: 493ca3c3-c3d6-4bb1-9430-dc1e43c86bb0
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/23/2017
ms.openlocfilehash: 457cca9db5d39466691b0bc7c41455910b4483d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795871"
---
# <span data-ttu-id="9abf8-103">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="9abf8-103">Advanced Group Policy Management</span></span>


<span data-ttu-id="9abf8-104">Administración avanzada de directivas de grupo (AGPM) de Microsoft amplía las capacidades de la consola de administración de directivas de grupo (GPMC) para proporcionar control de cambios completo y administración mejorada para objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="9abf8-104">Microsoft Advanced Group Policy Management (AGPM) extends the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span> <span data-ttu-id="9abf8-105">AGPM está disponible como parte del paquete de optimización de escritorio de Microsoft (MDOP) para software Assurance.</span><span class="sxs-lookup"><span data-stu-id="9abf8-105">AGPM is available as part of the Microsoft Desktop Optimization Pack (MDOP) for Software Assurance.</span></span>

## <span data-ttu-id="9abf8-106">Información de versión de AGPM</span><span class="sxs-lookup"><span data-stu-id="9abf8-106">AGPM Version Information</span></span>


<span data-ttu-id="9abf8-107">[AGPM 4,0 SP3](agpm-40-sp3-navengl.md) es compatible con Windows 10, windows Server 2019, windows Server 2016, windows Server 2012 R2, Windows 8,1, Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="9abf8-107">[AGPM 4.0 SP3](agpm-40-sp3-navengl.md) supports Windows 10, Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="9abf8-108">[AGPM 4,0 SP2](agpm-40-sp2-navengl.md) admite windows Server 2012 R2, Windows 8,1, windows Server 2012, windows Server 2008 R2, Windows 7, windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="9abf8-108">[AGPM 4.0 SP2](agpm-40-sp2-navengl.md) supports Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="9abf8-109">[AGPM 4,0 SP1](agpm-40-sp1-navengl.md) admite windows Server 2012, windows Server 2008 R2, Windows 7, windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="9abf8-109">[AGPM 4.0 SP1](agpm-40-sp1-navengl.md) supports Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="9abf8-110">[AGPM 4](agpm-4-navengl.md) es compatible con windows Server 2008 R2, Windows 7, windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="9abf8-110">[AGPM 4](agpm-4-navengl.md) supports Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="9abf8-111">[AGPM 3](agpm-3-navengl.md) admite windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="9abf8-111">[AGPM 3](agpm-3-navengl.md) supports Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="9abf8-112">[AGPM 2,5](agpm-25-navengl.md) admite Windows Vista (32 bits) sin Service Pack ni windows Server 2003 (32-bit).</span><span class="sxs-lookup"><span data-stu-id="9abf8-112">[AGPM 2.5](agpm-25-navengl.md) supports Windows Vista (32-bit) with no service pack and Windows Server 2003 (32-bit).</span></span>

## <span data-ttu-id="9abf8-113">Guía complementaria de producto de MDOP</span><span class="sxs-lookup"><span data-stu-id="9abf8-113">Supplemental MDOP Product Guidance</span></span>


<span data-ttu-id="9abf8-114">Además de la documentación del producto disponible en línea, se pueden obtener instrucciones de producto adicionales, como vídeos informativos y laboratorios virtuales, para la mayoría de los productos de MDOP.</span><span class="sxs-lookup"><span data-stu-id="9abf8-114">In addition to the product documentation available online, supplemental product guidance such as informational videos and virtual labs are available for most MDOP products.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9abf8-115">Laboratorios virtuales de MDOP</span><span class="sxs-lookup"><span data-stu-id="9abf8-115">MDOP Virtual Labs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9abf8-116">Para obtener una lista de los laboratorios virtuales de MDOP disponibles, vaya a <a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="[Microsoft Desktop Optimization Pack (MDOP) Virtual Labs](https://go.microsoft.com/fwlink/?LinkId=234276)"> Microsoft Desktop Optimization Pack (MDOP) virtual Labs </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=234276"> https://go.microsoft.com/fwlink/?LinkId=234276 </a> ).</span><span class="sxs-lookup"><span data-stu-id="9abf8-116">For a list of available MDOP virtual labs, go to <a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="[Microsoft Desktop Optimization Pack (MDOP) Virtual Labs](https://go.microsoft.com/fwlink/?LinkId=234276)">Microsoft Desktop Optimization Pack (MDOP) Virtual Labs</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=234276">https://go.microsoft.com/fwlink/?LinkId=234276</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9abf8-117">TechCenter de MDOP</span><span class="sxs-lookup"><span data-stu-id="9abf8-117">MDOP TechCenter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9abf8-118">Para obtener informes técnicos, materiales de evaluación, blogs y recursos adicionales de MDOP, vaya a la <a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="[MDOP TechCenter](https://go.microsoft.com/fwlink/?LinkId=225286)"> TechCenter de MDOP </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=225286"> https://go.microsoft.com/fwlink/?LinkId=225286 </a> ).</span><span class="sxs-lookup"><span data-stu-id="9abf8-118">For technical whitepapers, evaluation materials, blogs, and additional MDOP resources, go to <a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="[MDOP TechCenter](https://go.microsoft.com/fwlink/?LinkId=225286)">MDOP TechCenter</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=225286">https://go.microsoft.com/fwlink/?LinkId=225286</a>)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-getmdop"></a><span data-ttu-id="9abf8-119">Cómo obtener MDOP</span><span class="sxs-lookup"><span data-stu-id="9abf8-119">How to Get MDOP</span></span>


<span data-ttu-id="9abf8-120">MDOP es un conjunto de productos que pueden ayudar a simplificar la implementación, la administración y el soporte técnico de escritorio en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="9abf8-120">MDOP is a suite of products that can help streamline desktop deployment, management, and support across the enterprise.</span></span> <span data-ttu-id="9abf8-121">MDOP está disponible como una suscripción adicional para los clientes de garantía de software.</span><span class="sxs-lookup"><span data-stu-id="9abf8-121">MDOP is available as an additional subscription for Software Assurance customers.</span></span>

<a href="" id="evaluate-mdop"></a><span data-ttu-id="9abf8-122">**Evaluar MDOP** MDOP también está disponible para pruebas y evaluaciones para los suscriptores de [MSDN](https://msdn.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) y [technet](https://technet.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) conforme a los acuerdos de MSDN y technet.</span><span class="sxs-lookup"><span data-stu-id="9abf8-122">**Evaluate MDOP** MDOP is also available for test and evaluation to [MSDN](https://msdn.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) and [TechNet](https://technet.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) subscribers in accordance with MSDN and TechNet agreements.</span></span>

<a href="" id="download-mdop"></a><span data-ttu-id="9abf8-123">**Descargar MDOP** Los suscriptores de MDOP pueden descargar el software en el [sitio web de licencias por volumen de Microsoft (MVLS)](https://go.microsoft.com/fwlink/?LinkId=166331).</span><span class="sxs-lookup"><span data-stu-id="9abf8-123">**Download MDOP** MDOP subscribers can download the software at the [Microsoft Volume Licensing website (MVLS)](https://go.microsoft.com/fwlink/?LinkId=166331).</span></span>

<a href="" id="purchase-mdop"></a><span data-ttu-id="9abf8-124">**Comprar MDOP** Visite el sitio web de licencias de empresa de [compras de Windows](https://www.microsoft.com/windows/enterprise/how-to-buy.aspx) para averiguar cómo comprar MDOP para su empresa.</span><span class="sxs-lookup"><span data-stu-id="9abf8-124">**Purchase MDOP** Visit the enterprise [Purchase Windows Enterprise Licensing](https://www.microsoft.com/windows/enterprise/how-to-buy.aspx) website to find out how to purchase MDOP for your business.</span></span>

 

 





