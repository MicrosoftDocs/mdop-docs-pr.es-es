---
title: Cómo implementar paquetes de App-V 5.0 con la distribución electrónica de software
description: Cómo implementar paquetes de App-V 5.0 con la distribución electrónica de software
author: dansimp
ms.assetid: 08e5e05b-dbb8-4be7-b2d8-721ef627da81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 33af02c5e9fad7408f9719ecd1a7fa90eacfeb29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814190"
---
# <span data-ttu-id="27373-103">Cómo implementar paquetes de App-V 5.0 con la distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="27373-103">How to deploy App-V 5.0 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="27373-104">Puede usar un sistema de distribución electrónica de software (ESD) para implementar aplicaciones virtuales de App-V 5,0 en clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="27373-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.0 virtual applications to App-V clients.</span></span> <span data-ttu-id="27373-105">Para obtener más información, consulte la documentación disponible con el ESD que está usando.</span><span class="sxs-lookup"><span data-stu-id="27373-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="27373-106">Para conocer los requisitos de componente y las opciones para usar un ESD para implementar paquetes de App-V, consulte [planificación para implementar App-v 5,0 con un sistema electrónico de distribución de software](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="27373-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.0 with an Electronic Software Distribution System](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="27373-107">Use uno de los siguientes métodos para publicar paquetes en equipos cliente de App-V con un ESD:</span><span class="sxs-lookup"><span data-stu-id="27373-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27373-108">Método</span><span class="sxs-lookup"><span data-stu-id="27373-108">Method</span></span></th>
<th align="left"><span data-ttu-id="27373-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="27373-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27373-110">Funcionalidad proporcionada por una tercera parte ESD</span><span class="sxs-lookup"><span data-stu-id="27373-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="27373-111">Usar la funcionalidad en un ESD de terceros.</span><span class="sxs-lookup"><span data-stu-id="27373-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27373-112">Windows Installer independiente</span><span class="sxs-lookup"><span data-stu-id="27373-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="27373-113">Instale la aplicación en el equipo cliente de destino con el archivo de Windows Installer (. msi) asociado que se crea al momento de la secuencia de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="27373-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="27373-114">El archivo de Windows Installer contiene la información del archivo de paquete de App-V 5,0 asociada para configurar un paquete y copiar los archivos de paquete necesarios en el cliente.</span><span class="sxs-lookup"><span data-stu-id="27373-114">The Windows Installer file contains the associated App-V 5.0 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27373-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="27373-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="27373-116">Use los cmdlets de PowerShell para implementar aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="27373-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="27373-117">Para obtener más información sobre cómo usar PowerShell y App-V 5,0, consulte <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)"> administrar App-v con PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="27373-117">For more information about using PowerShell and App-V 5.0, see <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)">Administering App-V by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="27373-118">Para implementar paquetes de App-V 5,0 con un ESD</span><span class="sxs-lookup"><span data-stu-id="27373-118">To deploy App-V 5.0 packages by using an ESD</span></span>**

1.  <span data-ttu-id="27373-119">Instale el secuenciador de 5,0 de App-V en un equipo de su entorno.</span><span class="sxs-lookup"><span data-stu-id="27373-119">Install the App-V 5.0 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="27373-120">Para obtener más información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="27373-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="27373-121">Use el secuenciador de aplicaciones-V 5,0 para crear una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="27373-121">Use the App-V 5.0 Sequencer to create virtual application.</span></span> <span data-ttu-id="27373-122">Para obtener información sobre la creación de una aplicación virtual, vea [crear y administrar aplicaciones virtualizadas de App-V 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="27373-122">For information about creating a virtual application, see [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="27373-123">Después de crear la aplicación virtual, implemente el paquete con la solución de ESD.</span><span class="sxs-lookup"><span data-stu-id="27373-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="27373-124">Si está usando System Center Configuration Manager, empiece por revisar la [Introducción a administración de aplicaciones en Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) para obtener información sobre el uso de App-V 5,0 y System Center2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="27373-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.0 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="27373-125">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="27373-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="27373-126">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="27373-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="27373-127">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="27373-127">Got an App-V issue?</span></span>** <span data-ttu-id="27373-128">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="27373-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="27373-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27373-129">Related topics</span></span>


[<span data-ttu-id="27373-130">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="27373-130">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





