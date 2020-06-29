---
title: Planificación de la implementación de App-V 5.1 con un sistema de distribución electrónica de software
description: Planificación de la implementación de App-V 5.1 con un sistema de distribución electrónica de software
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813399"
---
# <span data-ttu-id="5aa04-103">Planificación de la implementación de App-V 5.1 con un sistema de distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="5aa04-103">Planning to Deploy App-V 5.1 with an Electronic Software Distribution System</span></span>


<span data-ttu-id="5aa04-104">Si está usando un sistema de distribución de software electrónico para implementar paquetes de App-V, revise las siguientes consideraciones de planeación.</span><span class="sxs-lookup"><span data-stu-id="5aa04-104">If you are using an electronic software distribution system to deploy App-V packages, review the following planning considerations.</span></span> <span data-ttu-id="5aa04-105">Para obtener información sobre el uso de System Center Configuration Manager para implementar App-V, consulte [Introducción a la administración de aplicaciones en Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span><span class="sxs-lookup"><span data-stu-id="5aa04-105">For information about using System Center Configuration Manager to deploy App-V, see [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span></span>

<span data-ttu-id="5aa04-106">Revise las siguientes opciones de requisitos de componentes y arquitectura que se aplican al usar un ESD para implementar paquetes de App-V:</span><span class="sxs-lookup"><span data-stu-id="5aa04-106">Review the following component and architecture requirements options that apply when you use an ESD to deploy App-V packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5aa04-107">Opción o requisito de implementación</span><span class="sxs-lookup"><span data-stu-id="5aa04-107">Deployment requirement or option</span></span></th>
<th align="left"><span data-ttu-id="5aa04-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa04-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5aa04-109">El servidor de administración de App-V, la base de datos de administración y el servidor de publicación no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="5aa04-109">The App-V Management server, Management database, and Publishing server are not required.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5aa04-110">Estas funciones son controladas por la solución ESD implementada.</span><span class="sxs-lookup"><span data-stu-id="5aa04-110">These functions are handled by the implemented ESD solution.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5aa04-111">Puede implementar el servidor de informes de App-V y la base de datos de informes en paralelo con el ESD.</span><span class="sxs-lookup"><span data-stu-id="5aa04-111">You can deploy the App-V Reporting server and Reporting database side by side with the ESD.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5aa04-112">La implementación en paralelo le permite recopilar datos y generar informes.</span><span class="sxs-lookup"><span data-stu-id="5aa04-112">The side-by-side deployment lets you to collect data and generate reports.</span></span></p>
<p><span data-ttu-id="5aa04-113">Si habilita el cliente de App-V para enviar información de informes y no usa el servidor de informes de App-V, los datos de informes se almacenan en archivos. XML asociados.</span><span class="sxs-lookup"><span data-stu-id="5aa04-113">If you enable the App-V client to send report information, and you are not using the App-V Reporting server, the reporting data is stored in associated .xml files.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="5aa04-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5aa04-114">Related topics</span></span>


[<span data-ttu-id="5aa04-115">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="5aa04-115">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





