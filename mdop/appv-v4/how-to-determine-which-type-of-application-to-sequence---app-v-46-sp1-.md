---
title: Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)
description: Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817490"
---
# <span data-ttu-id="53cc6-103">Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="53cc6-103">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>


<span data-ttu-id="53cc6-104">Puede hacer una secuencia de tres tipos básicos de aplicaciones con Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="53cc6-104">You can sequence three basic types of applications by using Microsoft Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="53cc6-105">Para determinar qué tipo de aplicación se va a secuenciar</span><span class="sxs-lookup"><span data-stu-id="53cc6-105">To determine which type of application to sequence</span></span>


<span data-ttu-id="53cc6-106">Use la tabla siguiente para determinar qué tipo de aplicación debe secuenciar y obtener más información sobre cómo hacer una secuencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53cc6-106">Use the following table to determine which type of application you should sequence and to obtain more information about how to sequence the application.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="53cc6-107">Tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="53cc6-107">Application Type</span></span></th>
<th align="left"><span data-ttu-id="53cc6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="53cc6-108">Description</span></span></th>
<th align="left"><span data-ttu-id="53cc6-109">Más información</span><span class="sxs-lookup"><span data-stu-id="53cc6-109">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cc6-110">Standard</span><span class="sxs-lookup"><span data-stu-id="53cc6-110">Standard</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cc6-111">Seleccione esta opción para crear un paquete que contenga una aplicación o un conjunto de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="53cc6-111">Select this option to create a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="53cc6-112">Debe seleccionar esta opción para la mayoría de las aplicaciones que planea secuenciar.</span><span class="sxs-lookup"><span data-stu-id="53cc6-112">You should select this option for most applications that you plan to sequence.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)"><span data-ttu-id="53cc6-113">Cómo secuenciar una nueva aplicación estándar (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="53cc6-113">How to Sequence a New Standard Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53cc6-114">Complemento o complemento</span><span class="sxs-lookup"><span data-stu-id="53cc6-114">Add-on or Plug-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cc6-115">Seleccione esta opción para crear un paquete que extienda la funcionalidad de una aplicación estándar, por ejemplo, un complemento de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="53cc6-115">Select this option to create a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="53cc6-116">Además, puede usar complementos para aplicaciones instaladas de forma nativa u otro paquete vinculado mediante la composición dinámica de conjuntos.</span><span class="sxs-lookup"><span data-stu-id="53cc6-116">Additionally, you can use plug-ins for natively installed applications, or another package that is linked by using Dynamic Suite Composition.</span></span> <span data-ttu-id="53cc6-117">Para obtener más información sobre la composición de conjuntos dinámicos, vea <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> Cómo usar la composición de conjunto dinámico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="53cc6-117">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)"><span data-ttu-id="53cc6-118">Cómo secuenciar un nuevo complemento o aplicación de complemento (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="53cc6-118">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53cc6-119">Cabe</span><span class="sxs-lookup"><span data-stu-id="53cc6-119">Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="53cc6-120">Seleccione esta opción para crear un paquete necesario para una aplicación estándar, por ejemplo, Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="53cc6-120">Select this option to create a package that is required by a standard application, for example, the Microsoft .NET Framework.</span></span> <span data-ttu-id="53cc6-121">Los paquetes de middleware se usan para vincular a otros paquetes mediante la composición de conjunto dinámico.</span><span class="sxs-lookup"><span data-stu-id="53cc6-121">Middleware packages are used for linking to other packages by using Dynamic Suite Composition.</span></span> <span data-ttu-id="53cc6-122">Para obtener más información sobre la composición de conjuntos dinámicos, vea <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> Cómo usar la composición de conjunto dinámico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="53cc6-122">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)"><span data-ttu-id="53cc6-123">Cómo secuenciar una nueva aplicación de software intermedio (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="53cc6-123">How to Sequence a New Middleware Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="53cc6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53cc6-124">Related topics</span></span>


[<span data-ttu-id="53cc6-125">Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="53cc6-125">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





