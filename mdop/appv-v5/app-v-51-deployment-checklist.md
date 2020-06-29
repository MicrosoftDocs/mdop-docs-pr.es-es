---
title: Lista de comprobación de implementación de App-V 5.1
description: Lista de comprobación de implementación de App-V 5.1
author: dansimp
ms.assetid: 44bed85a-e4f5-49d7-a308-a2b681f76372
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0864335e505996a3ea379b09de6a1aaa7fbe1676
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814774"
---
# <span data-ttu-id="b5476-103">Lista de comprobación de implementación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b5476-103">App-V 5.1 Deployment Checklist</span></span>


<span data-ttu-id="b5476-104">Esta lista de comprobación se puede usar para ayudarle durante la implementación de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="b5476-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

**<span data-ttu-id="b5476-105">Nota</span><span class="sxs-lookup"><span data-stu-id="b5476-105">Note</span></span>**  
<span data-ttu-id="b5476-106">En esta lista de comprobación se describen los pasos recomendados y una lista de alto nivel de los elementos que se deben tener en cuenta al implementar características de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b5476-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.1 features.</span></span> <span data-ttu-id="b5476-107">Se recomienda copiar esta lista de comprobación en un programa de hoja de cálculo y personalizarla para su uso.</span><span class="sxs-lookup"><span data-stu-id="b5476-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="b5476-108">Tarea</span><span class="sxs-lookup"><span data-stu-id="b5476-108">Task</span></span></th>
<th align="left"><span data-ttu-id="b5476-109">Referencias</span><span class="sxs-lookup"><span data-stu-id="b5476-109">References</span></span></th>
<th align="left"><span data-ttu-id="b5476-110">Notas</span><span class="sxs-lookup"><span data-stu-id="b5476-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b5476-111">Complete la fase de planeación para preparar el entorno de equipos para la implementación de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b5476-111">Complete the planning phase to prepare the computing environment for App-V 5.1 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-51-planning-checklist.md" data-raw-source="[App-V 5.1 Planning Checklist](app-v-51-planning-checklist.md)"><span data-ttu-id="b5476-112">Lista de comprobación de planificación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b5476-112">App-V 5.1 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b5476-113">Revise la información de configuración admitida de la aplicación-V 5,1 para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b5476-113">Review the App-V 5.1 supported configurations information to make sure selected client and server computers are supported for App-V 5.1 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="b5476-114">Configuraciones compatibles con App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b5476-114">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="b5476-115">Ejecute el programa de instalación de App-V 5,1 para implementar las características de App-V 5,1 necesarias para su entorno.</span><span class="sxs-lookup"><span data-stu-id="b5476-115">Run App-V 5.1 Setup to deploy the required App-V 5.1 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b5476-116">Nota</span><span class="sxs-lookup"><span data-stu-id="b5476-116">Note</span></span></strong><br/><p><span data-ttu-id="b5476-117">Realice un seguimiento de los nombres de los servidores y de la dirección URL asociada durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="b5476-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="b5476-118">Esta información se utilizará durante todo el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="b5476-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-51beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)"><span data-ttu-id="b5476-119">Cómo instalar el secuenciador</span><span class="sxs-lookup"><span data-stu-id="b5476-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="b5476-120">Cómo implementar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="b5476-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="b5476-121">Cómo implementar el servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b5476-121">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="b5476-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5476-122">Related topics</span></span>


[<span data-ttu-id="b5476-123">Implementación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b5476-123">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









