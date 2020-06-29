---
title: Implementación de Microsoft Office 2016 mediante el uso de App-V
description: Implementación de Microsoft Office 2016 mediante el uso de App-V
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814622"
---
# <span data-ttu-id="1cc20-103">Implementación de Microsoft Office 2016 mediante el uso de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-103">Deploying Microsoft Office 2016 by Using App-V</span></span>


<span data-ttu-id="1cc20-104">Use la información de este artículo para usar Microsoft Application Virtualization 5,0, o versiones posteriores, para ofrecer Microsoft Office 2016 como una aplicación virtualizada a los equipos de su organización.</span><span class="sxs-lookup"><span data-stu-id="1cc20-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2016 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="1cc20-105">Para obtener información sobre cómo usar App-V para ofrecer Office 2013, consulte [implementar Microsoft office 2013 mediante App-v](deploying-microsoft-office-2013-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="1cc20-105">For information about using App-V to deliver Office 2013, see [Deploying Microsoft Office 2013 by Using App-V](deploying-microsoft-office-2013-by-using-app-v.md).</span></span> <span data-ttu-id="1cc20-106">Para obtener información sobre cómo usar App-V para ofrecer Office 2010, consulte [implementar Microsoft office 2010 mediante App-v](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="1cc20-106">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span>

<span data-ttu-id="1cc20-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="1cc20-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1cc20-108">Qué debe saber antes de empezar</span><span class="sxs-lookup"><span data-stu-id="1cc20-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="1cc20-109">Crear un paquete de Office 2016 para App-V con la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-109">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="1cc20-110">Publicar el paquete de Office para App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1cc20-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="1cc20-111">Personalizar y administrar paquetes de App-V de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="1cc20-112">Qué debe saber antes de empezar</span><span class="sxs-lookup"><span data-stu-id="1cc20-112">What to know before you start</span></span>


<span data-ttu-id="1cc20-113">Antes de implementar Office 2016 mediante App-V, revise la siguiente información de planeación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-113">Before you deploy Office 2016 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="1cc20-114">Versiones de Office compatibles y coexistencia de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="1cc20-115">Use la siguiente tabla para obtener información acerca de las versiones compatibles de Office y acerca de la ejecución de versiones coexistentes de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-116">Información para revisar</span><span class="sxs-lookup"><span data-stu-id="1cc20-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="1cc20-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc20-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="1cc20-118">Versiones compatibles de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-118">Supported versions of Microsoft Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1cc20-119">Versiones compatibles de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="1cc20-120">Tipos de implementación admitidos (por ejemplo, escritorio, infraestructura de escritorio virtual personal (VDI), VDI agrupada)</span><span class="sxs-lookup"><span data-stu-id="1cc20-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="1cc20-121">Opciones de licencia de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="1cc20-122">Planificación para usar App-V con versiones coexistentes de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-122">Planning for Using App-V with coexisting versions of Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="1cc20-123">Consideraciones para instalar diferentes versiones de Office en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="1cc20-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="1cc20-124">Requisitos de empaquetado, publicación e implementación</span><span class="sxs-lookup"><span data-stu-id="1cc20-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="1cc20-125">Antes de implementar Office con App-V, revise los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cc20-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-126">Tarea</span><span class="sxs-lookup"><span data-stu-id="1cc20-126">Task</span></span></th>
<th align="left"><span data-ttu-id="1cc20-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc20-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-128">Empaquetado</span><span class="sxs-lookup"><span data-stu-id="1cc20-128">Packaging</span></span></p></td>
<td align="left">
<ul>
<li><p><span data-ttu-id="1cc20-129">Todas las aplicaciones de Office que desee implementar para los usuarios deben tener un único paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-130">En App-V 5,0 y versiones posteriores, debe usar la herramienta de implementación de Office para crear paquetes.</span><span class="sxs-lookup"><span data-stu-id="1cc20-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="1cc20-131">No puede usar el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="1cc20-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-132">Si va a implementar Microsoft Visio 2016 y Microsoft Project 2016 junto con Office, debe incluirlos en el mismo paquete que Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-132">If you are deploying Microsoft Visio 2016 and Microsoft Project 2016 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="1cc20-133">Para obtener más información, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> implementar Visio 2016 y Project 2016 con Office </a> .</span><span class="sxs-lookup"><span data-stu-id="1cc20-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2016 and Project 2016 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cc20-134">Publicación</span><span class="sxs-lookup"><span data-stu-id="1cc20-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1cc20-135">Solo puede publicar un paquete de Office en cada equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-136">Debe publicar el paquete de Office globalmente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-136">You must publish the Office package globally.</span></span> <span data-ttu-id="1cc20-137">No puede publicar para el usuario.</span><span class="sxs-lookup"><span data-stu-id="1cc20-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-138">Implementar cualquiera de los siguientes productos en un equipo compartido, por ejemplo, con servicios de escritorio remoto:</span><span class="sxs-lookup"><span data-stu-id="1cc20-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="1cc20-139">Aplicaciones de Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="1cc20-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="1cc20-140">Visio Pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="1cc20-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="1cc20-141">Project Pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="1cc20-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1cc20-142">Debe habilitar la <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> activación en equipos compartidos </a> .</span><span class="sxs-lookup"><span data-stu-id="1cc20-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
</td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1cc20-143">Excluir aplicaciones de Office de un paquete</span><span class="sxs-lookup"><span data-stu-id="1cc20-143">Excluding Office applications from a package</span></span>

<span data-ttu-id="1cc20-144">En la siguiente tabla se describen los métodos recomendados para excluir aplicaciones específicas de Office de un paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-144">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-145">Tarea</span><span class="sxs-lookup"><span data-stu-id="1cc20-145">Task</span></span></th>
<th align="left"><span data-ttu-id="1cc20-146">Detalles</span><span class="sxs-lookup"><span data-stu-id="1cc20-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-147">Use la <strong> </strong> configuración ExcludeApp al crear el paquete con la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-147">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1cc20-148">Permite excluir determinadas aplicaciones de Office del paquete cuando la herramienta de implementación de Office crea el paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-148">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="1cc20-149">Por ejemplo, puede usar esta opción para crear un paquete que solo contenga Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="1cc20-149">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-150">Para obtener más información, consulta <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</span><span class="sxs-lookup"><span data-stu-id="1cc20-150">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cc20-151">Modificar el archivo de DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="1cc20-151">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1cc20-152">Modifique el archivo DeploymentConfig.xml después de que se haya creado el paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-152">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="1cc20-153">Este archivo contiene la configuración de paquete predeterminada para todos los usuarios de un equipo que ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-153">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-154">Para obtener más información, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> deshabilitar aplicaciones de Office 2016 </a> .</span><span class="sxs-lookup"><span data-stu-id="1cc20-154">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)">Disabling Office 2016 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="1cc20-155">Crear un paquete de Office 2016 para App-V con la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-155">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="1cc20-156">Complete los pasos siguientes para crear un paquete de Office 2016 para App-V 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1cc20-156">Complete the following steps to create an Office 2016 package for App-V 5.0 or later.</span></span>

><span data-ttu-id="1cc20-157">**Important** &nbsp; Importante &nbsp; En App-V 5,0 y versiones posteriores, debe usar la herramienta de implementación de Office para crear un paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-157">**Important**&nbsp;&nbsp;In App-V 5.0 and later, you must use the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="1cc20-158">No puede usar el secuenciador para crear paquetes.</span><span class="sxs-lookup"><span data-stu-id="1cc20-158">You cannot use the Sequencer to create packages.</span></span>

### <span data-ttu-id="1cc20-159">Revisar los requisitos previos para usar la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-159">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="1cc20-160">El equipo en el que está instalando la herramienta de implementación de Office debe tener:</span><span class="sxs-lookup"><span data-stu-id="1cc20-160">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-161">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="1cc20-161">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="1cc20-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc20-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-163">Requisitos previos de software</span><span class="sxs-lookup"><span data-stu-id="1cc20-163">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-164">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="1cc20-164">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cc20-165">Sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="1cc20-165">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1cc20-166">versión de 64 bits de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1cc20-166">64-bit version of Windows 10</span></span></p></li>
<li><p><span data-ttu-id="1cc20-167">versión de 64 bits de Windows 8 o 8,1</span><span class="sxs-lookup"><span data-stu-id="1cc20-167">64-bit version of Windows 8 or 8.1</span></span></p></li>
<li><p><span data-ttu-id="1cc20-168">versión de 64 bits de Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cc20-168">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


><span data-ttu-id="1cc20-169">**Nota:**  En este tema, el término "paquete de aplicación de Office 2016" se refiere a licencias de suscripción.</span><span class="sxs-lookup"><span data-stu-id="1cc20-169">**Note**  In this topic, the term “Office 2016 App-V package” refers to subscription licensing.</span></span>


### <span data-ttu-id="1cc20-170">Crear paquetes de Office 2016 App-V con la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-170">Create Office 2016 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="1cc20-171">Para crear paquetes de Office 2016 App-V, use la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-171">You create Office 2016 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="1cc20-172">En las siguientes instrucciones se explica cómo crear un paquete de App-V de Office 2016 con licencias de suscripciones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-172">The following instructions explain how to create an Office 2016 App-V package with Subscription Licensing.</span></span>

<span data-ttu-id="1cc20-173">Crear paquetes de aplicación de Office 2016 en equipos Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1cc20-173">Create Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="1cc20-174">Una vez creado, el paquete de Office 2016 App-V se ejecutará en equipos Windows 7, Windows 8,1 y Windows 10 de 32 bits y 64</span><span class="sxs-lookup"><span data-stu-id="1cc20-174">Once created, the Office 2016 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="1cc20-175">Descargar la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-175">Download the Office Deployment Tool</span></span>

<span data-ttu-id="1cc20-176">Los paquetes de Office 2016 App-V se crean con la herramienta de implementación de Office, que genera un paquete de App-V de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-176">Office 2016 App-V Packages are created using the Office Deployment Tool, which generates an Office 2016 App-V Package.</span></span> <span data-ttu-id="1cc20-177">El paquete no se puede crear ni modificar mediante el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-177">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="1cc20-178">Para comenzar la creación del paquete:</span><span class="sxs-lookup"><span data-stu-id="1cc20-178">To begin package creation:</span></span>

1.  <span data-ttu-id="1cc20-179">Descargue la [herramienta de implementación de Office 2016 para hacer clic y ejecutar](https://www.microsoft.com/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="1cc20-179">Download the [Office 2016 Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span>

> <span data-ttu-id="1cc20-180">**Importante** Debe usar la herramienta de implementación de Office 2016 para crear paquetes de App-V de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-180">**Important** You must use the Office 2016 Deployment Tool to create Office 2016 App-V Packages.</span></span>
> 2. <span data-ttu-id="1cc20-181">Ejecute el archivo. exe y extraiga sus características en la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="1cc20-181">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="1cc20-182">Para facilitar este proceso, puede crear una carpeta de red compartida donde se guardarán las características.</span><span class="sxs-lookup"><span data-stu-id="1cc20-182">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    Example: \\\\Server\\Office2016

3. <span data-ttu-id="1cc20-183">Compruebe que exista un setup.exe y un archivo configuration.xml y que se encuentren en la ubicación que especificó.</span><span class="sxs-lookup"><span data-stu-id="1cc20-183">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="1cc20-184">Descargar aplicaciones de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-184">Download Office 2016 applications</span></span>

<span data-ttu-id="1cc20-185">Después de descargar la herramienta de implementación de Office, puede usarla para obtener las aplicaciones de Office 2016 más recientes.</span><span class="sxs-lookup"><span data-stu-id="1cc20-185">After you download the Office Deployment Tool, you can use it to get the latest Office 2016 applications.</span></span> <span data-ttu-id="1cc20-186">Después de obtener las aplicaciones de Office, cree el paquete de Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-186">After getting the Office applications, you create the Office 2016 App-V package.</span></span>

<span data-ttu-id="1cc20-187">El archivo XML incluido en la herramienta de implementación de Office especifica los detalles del producto, como los idiomas y las aplicaciones de Office incluidos.</span><span class="sxs-lookup"><span data-stu-id="1cc20-187">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="1cc20-188">**Personalizar el archivo de configuración XML de ejemplo:** Use el archivo de configuración XML de ejemplo que haya descargado con la herramienta de implementación de Office para personalizar las aplicaciones de Office:</span><span class="sxs-lookup"><span data-stu-id="1cc20-188">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="1cc20-189">Abra el archivo XML de muestra en el Bloc de notas o su editor de texto preferido.</span><span class="sxs-lookup"><span data-stu-id="1cc20-189">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="1cc20-190">Con el archivo de configuration.xml de ejemplo abierto y listo para editar, puede especificar productos, idiomas y la ruta de acceso en la que guarda las aplicaciones de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-190">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2016 applications.</span></span> <span data-ttu-id="1cc20-191">A continuación se encuentra un ejemplo básico del archivo de configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="1cc20-191">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      ><span data-ttu-id="1cc20-192">**Nota:**  La configuración de XML es un archivo XML de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1cc20-192">**Note**  The configuration XML is a sample XML file.</span></span> <span data-ttu-id="1cc20-193">El archivo incluye líneas con comentarios. Puede "Quitar comentarios" estas líneas para personalizar la configuración adicional con el archivo.</span><span class="sxs-lookup"><span data-stu-id="1cc20-193">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span> <span data-ttu-id="1cc20-194">Para "Quitar comentarios" de estas líneas, quite el "<!</span><span class="sxs-lookup"><span data-stu-id="1cc20-194">To “uncomment” these lines, remove the "<!</span></span> <span data-ttu-id="1cc20-195">--"desde el principio de la línea y"--> "desde el final de la línea.</span><span class="sxs-lookup"><span data-stu-id="1cc20-195">- -" from the beginning of the line, and the "-- >" from the end of the line.</span></span>

      <span data-ttu-id="1cc20-196">El archivo de configuración XML anterior especifica que Office 2016 ProPlus 32-bit Edition, incluido Visio ProPlus, se descargará en inglés al \\\\server\\Office 2016, que es la ubicación donde se guardarán las aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-196">The above XML configuration file specifies that Office 2016 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2016, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="1cc20-197">Tenga en cuenta que el identificador de producto de las aplicaciones no afectará al final de la licencia de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-197">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="1cc20-198">Los paquetes de Office 2016 App-V con varias licencias se pueden crear a partir de las mismas aplicaciones mediante la especificación de licencias en una fase posterior.</span><span class="sxs-lookup"><span data-stu-id="1cc20-198">Office 2016 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="1cc20-199">La tabla siguiente resume los atributos personalizables y los elementos del archivo XML:</span><span class="sxs-lookup"><span data-stu-id="1cc20-199">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="1cc20-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cc20-200">Input</span></span></th>
      <th align="left"><span data-ttu-id="1cc20-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc20-201">Description</span></span></th>
      <th align="left"><span data-ttu-id="1cc20-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1cc20-202">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="1cc20-203">Elemento Add</span><span class="sxs-lookup"><span data-stu-id="1cc20-203">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-204">Especifica los productos e idiomas que se van a incluir en el paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-204">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-205">N/D</span><span class="sxs-lookup"><span data-stu-id="1cc20-205">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="1cc20-206">OfficeClientEdition (atributo del elemento "Add")</span><span class="sxs-lookup"><span data-stu-id="1cc20-206">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-207">Especifica la edición de Office 2016 producto que se va a usar: 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1cc20-207">Specifies the edition of Office 2016 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="1cc20-208">Se produce un error en la operación si <strong> OfficeClientEdition </strong> no se establece en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="1cc20-208">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="1cc20-209">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="1cc20-209">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="1cc20-210">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="1cc20-210">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="1cc20-211">Elemento Product</span><span class="sxs-lookup"><span data-stu-id="1cc20-211">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-212">Especifica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-212">Specifies the application.</span></span> <span data-ttu-id="1cc20-213">El proyecto 2016 y Visio 2016 deben especificarse aquí como un producto agregado que se incluirá en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-213">Project 2016 and Visio 2016 must be specified here as an added product to be included in the applications.</span></span>

      <span data-ttu-id="1cc20-214">Para obtener más información acerca de los identificadores de producto, consulte <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> identificadores de producto admitidos por la herramienta de implementación de Office para hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="1cc20-214">For more information about the product IDs, see <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)">Product IDs that are supported by the Office Deployment Tool for Click-to-Run</span></span></a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="1cc20-215">Elemento de lenguaje</span><span class="sxs-lookup"><span data-stu-id="1cc20-215">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-216">Especifica el idioma admitido en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-216">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="1cc20-217">Version (atributo del elemento Add)</span><span class="sxs-lookup"><span data-stu-id="1cc20-217">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-218">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1cc20-218">Optional.</span></span> <span data-ttu-id="1cc20-219">Especifica la compilación que se usará para el paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-219">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="1cc20-220">De forma predeterminada, es la compilación anunciada más reciente (según se define en v32.CAB en el origen de Office).</span><span class="sxs-lookup"><span data-stu-id="1cc20-220">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="1cc20-221">SourcePath (atributo del elemento "Add")</span><span class="sxs-lookup"><span data-stu-id="1cc20-221">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-222">Especifica la ubicación en la que se guardarán las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-222">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="1cc20-223">Canal (atributo del elemento "Add")</span><span class="sxs-lookup"><span data-stu-id="1cc20-223">Channel (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="1cc20-224">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1cc20-224">Optional.</span></span> <span data-ttu-id="1cc20-225">Especifica el canal de actualización del producto que desea descargar o instalar.</span><span class="sxs-lookup"><span data-stu-id="1cc20-225">Specifies the update channel for the product that you want to download or install.</span></span> </p><p><span data-ttu-id="1cc20-226">Para obtener más información sobre los canales de actualización, vea información general sobre los canales de actualización de las aplicaciones de Microsoft 365 para empresas.</span><span class="sxs-lookup"><span data-stu-id="1cc20-226">For more information about update channels, see Overview of update channels for Microsoft 365 Apps for enterprise.</span></span></p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="1cc20-227">Después de editar el archivo configuration.xml para especificar el producto, los idiomas y la ubicación en que se guardarán las aplicaciones de Office 2016, por ejemplo, puede guardar el archivo de configuración como Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="1cc20-227">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2016 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="1cc20-228">**Descargue las aplicaciones en la ubicación especificada:** Use un símbolo del sistema con privilegios elevados y un sistema operativo de 64 bits para descargar las aplicaciones de Office 2016 que se convertirán más adelante en un paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-228">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2016 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="1cc20-229">A continuación se muestra un comando de ejemplo con una descripción de los detalles:</span><span class="sxs-lookup"><span data-stu-id="1cc20-229">Below is an example command with a description of details:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   <span data-ttu-id="1cc20-230">En el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc20-230">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-231">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-231">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-232">es la ubicación del recurso compartido de red que contiene la herramienta de implementación de Office y el archivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="1cc20-232">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1cc20-233">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="1cc20-233">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-234">es la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-234">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-235">/Download</span><span class="sxs-lookup"><span data-stu-id="1cc20-235">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-236">Descarga las aplicaciones de Office 2016 que especifique en el archivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="1cc20-236">downloads the Office 2016 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="1cc20-237">Estos bits pueden convertirse más tarde en un paquete de App-V de Office 2016 con licencias por volumen.</span><span class="sxs-lookup"><span data-stu-id="1cc20-237">These bits can be later converted in an Office 2016 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1cc20-238">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="1cc20-238">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-239">pasa el archivo de configuración XML necesario para completar el proceso de descarga, en este ejemplo, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="1cc20-239">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="1cc20-240">Después de usar el comando de descarga, las aplicaciones de Office deberían encontrarse en la ubicación especificada en el archivo XML de configuración, en este ejemplo \Server\Office2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-240">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2016.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="1cc20-241">Convertir las aplicaciones de Office en un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-241">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="1cc20-242">Después de descargar las aplicaciones de Office 2016 mediante la herramienta de implementación de Office, use la herramienta de implementación de Office para convertirlas en un paquete de App-V de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-242">After you download the Office 2016 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2016 App-V package.</span></span> <span data-ttu-id="1cc20-243">Complete los pasos que correspondan al modelo de licencias.</span><span class="sxs-lookup"><span data-stu-id="1cc20-243">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="1cc20-244">Resumen de lo que debe hacer:</span><span class="sxs-lookup"><span data-stu-id="1cc20-244">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="1cc20-245">Crear los paquetes de App-V de Office 2016 en equipos Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1cc20-245">Create the Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="1cc20-246">Sin embargo, el paquete se ejecutará 32 en equipos con Windows 7, Windows 8 o 8,1 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1cc20-246">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8 or 8.1, and Windows 10 computers.</span></span>

-   <span data-ttu-id="1cc20-247">Cree un paquete de Office App-V para el paquete de licencias de suscripciones con la herramienta de implementación de Office y, a continuación, modifique el CustomConfig.xml archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="1cc20-247">Create an Office App-V package for Subscription Licensing package by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="1cc20-248">En la siguiente tabla se resumen los valores que debe introducir en el archivo CustomConfig.xml del modelo de licencias que está usando.</span><span class="sxs-lookup"><span data-stu-id="1cc20-248">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="1cc20-249">Los pasos que se indican en las secciones siguientes de la tabla especificarán las entradas exactas que tiene que hacer.</span><span class="sxs-lookup"><span data-stu-id="1cc20-249">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

><span data-ttu-id="1cc20-250">**Nota:** &nbsp; &nbsp; Puede usar la herramienta de implementación de Office para crear paquetes de App-V para las aplicaciones de Microsoft 365 para empresas.</span><span class="sxs-lookup"><span data-stu-id="1cc20-250">**Note**&nbsp;&nbsp;You can use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="1cc20-251">No se admite la creación de paquetes para las versiones con licencia por volumen de Office Professional Plus o Office Standard.</span><span class="sxs-lookup"><span data-stu-id="1cc20-251">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-252">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="1cc20-252">Product ID</span></span></th>
<th align="left"><span data-ttu-id="1cc20-253">Licencias de suscripciones</span><span class="sxs-lookup"><span data-stu-id="1cc20-253">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1cc20-254">Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-254">Office 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1cc20-255">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="1cc20-255">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1cc20-256">Office 2016 con Visio 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-256">Office 2016 with Visio 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1cc20-257">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="1cc20-257">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="1cc20-258">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="1cc20-258">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1cc20-259">Office 2016 con Visio 2016 y Project 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-259">Office 2016 with Visio 2016 and Project 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1cc20-260">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="1cc20-260">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="1cc20-261">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="1cc20-261">VisioProRetail</span></span></p>
<p><span data-ttu-id="1cc20-262">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="1cc20-262">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="1cc20-263">Cómo convertir las aplicaciones de Office en un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-263">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="1cc20-264">En el Bloc de notas, vuelva a abrir el archivo CustomConfig.xml y realice los cambios siguientes en el archivo:</span><span class="sxs-lookup"><span data-stu-id="1cc20-264">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1cc20-265">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1cc20-265">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="1cc20-266">Qué cambiar el valor a</span><span class="sxs-lookup"><span data-stu-id="1cc20-266">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="1cc20-267">RutaOrigen</span><span class="sxs-lookup"><span data-stu-id="1cc20-267">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-268">Apunte a las aplicaciones de Office descargadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-268">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="1cc20-269">ProductID</span><span class="sxs-lookup"><span data-stu-id="1cc20-269">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-270">Especifique la licencia de la suscripción, como se muestra en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc20-270">Specify Subscription licensing, as shown in the following example:</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="1cc20-271">En este ejemplo, se han realizado los cambios siguientes para crear un paquete con licencias de suscripciones:</span><span class="sxs-lookup"><span data-stu-id="1cc20-271">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-272">RutaOrigen</span><span class="sxs-lookup"><span data-stu-id="1cc20-272">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-273">es la ruta de acceso, que se cambió para que apunte a las aplicaciones de Office que se descargaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-273">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1cc20-274">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="1cc20-274">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-275">para Office se cambió a <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="1cc20-275">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-276">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="1cc20-276">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-277">para Visio se cambió a <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="1cc20-277">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="1cc20-278">ExcludeApp (opcional)</span><span class="sxs-lookup"><span data-stu-id="1cc20-278">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-279">Le permite especificar programas de Office que no desea incluir en el paquete de App-V que crea la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-279">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="1cc20-280">Por ejemplo, puede excluir Access e InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1cc20-280">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="1cc20-281">PACKAGEGUID (opcional)</span><span class="sxs-lookup"><span data-stu-id="1cc20-281">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-282">De forma predeterminada, todos los paquetes de App-V creados por la herramienta de implementación de Office comparten el mismo identificador de paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-282">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="1cc20-283">Puede usar PACKAGEGUID para especificar un identificador de paquete diferente para cada paquete, que le permite publicar varios paquetes de App-V, creados mediante la herramienta de implementación de Office, y administrarlos mediante el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-283">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="1cc20-284">Un ejemplo de Cuándo usar este parámetro es crear paquetes diferentes para diferentes usuarios.</span><span class="sxs-lookup"><span data-stu-id="1cc20-284">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="1cc20-285">Por ejemplo, puede crear un paquete con solo Office 2016 para algunos usuarios y crear otro paquete con Office 2016 y Visio 2016 para otro conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="1cc20-285">For example, you can create a package with just Office 2016 for some users, and create another package with Office 2016 and Visio 2016 for another set of users.</span></span></p>
<span data-ttu-id="1cc20-286">&gt;<strong>Nota </strong> aunque use identificadores de paquete únicos, aún puede implementar un solo paquete de App-V en un solo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1cc20-286">&gt;<strong>Note</strong> Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span>
   </td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="1cc20-287">Use el comando/Packager para convertir las aplicaciones de Office en un paquete de App-V de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-287">Use the /packager command to convert the Office applications to an Office 2016 App-V package.</span></span>

   <span data-ttu-id="1cc20-288">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc20-288">For example:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   <span data-ttu-id="1cc20-289">En el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc20-289">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-290">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-290">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-291">es la ubicación del recurso compartido de red que contiene la herramienta de implementación de Office y el archivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="1cc20-291">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1cc20-292">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="1cc20-292">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-293">es la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-293">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-294">/packager</span><span class="sxs-lookup"><span data-stu-id="1cc20-294">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-295">crea el paquete de Office 2016 App-V con el tipo de licencia especificado en el archivo de customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="1cc20-295">creates the Office 2016 App-V package with the type of licensing specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1cc20-296">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="1cc20-296">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-297">pasa el archivo XML de configuración (en este caso customConfig) que se ha preparado para la fase de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-297">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1cc20-298">\server\share\Office 2016AppV</span><span class="sxs-lookup"><span data-stu-id="1cc20-298">\server\share\Office 2016AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1cc20-299">Especifica la ubicación del paquete de Office App-V recién creado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-299">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="1cc20-300">Compruebe que el paquete de Office 2016 App-V funciona correctamente:</span><span class="sxs-lookup"><span data-stu-id="1cc20-300">Verify that the Office 2016 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="1cc20-301">Publique el paquete de App-V de Office 2016, creado globalmente, en un equipo de prueba y compruebe que aparecen los accesos directos de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-301">Publish the Office 2016 App-V package, which you created globally, to a test computer, and verify that the Office 2016 shortcuts appear.</span></span>

   2.  <span data-ttu-id="1cc20-302">Inicie algunas aplicaciones de Office 2016, como Excel o Word, para asegurarse de que el paquete funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="1cc20-302">Start a few Office 2016 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="1cc20-303">Publicar el paquete de Office para App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-303">Publishing the Office package for App-V</span></span>


<span data-ttu-id="1cc20-304">Use la siguiente información para publicar un paquete de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-304">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="1cc20-305">Métodos para publicar paquetes de Office App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-305">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="1cc20-306">Implemente el paquete de App-V para Office 2016 con los mismos métodos que usa para cualquier otro paquete:</span><span class="sxs-lookup"><span data-stu-id="1cc20-306">Deploy the App-V package for Office 2016 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="1cc20-307">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1cc20-307">System Center Configuration Manager</span></span>

-   <span data-ttu-id="1cc20-308">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-308">App-V Server</span></span>

-   <span data-ttu-id="1cc20-309">Independiente a través de los comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="1cc20-309">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="1cc20-310">Publicar requisitos y requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1cc20-310">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-311">Requisito previo o requisito</span><span class="sxs-lookup"><span data-stu-id="1cc20-311">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="1cc20-312">Detalles</span><span class="sxs-lookup"><span data-stu-id="1cc20-312">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-313">Habilitar scripting de PowerShell en los clientes de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-313">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-314">Para publicar paquetes de Office 2016, debe ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="1cc20-314">To publish Office 2016 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="1cc20-315">Los scripts de paquetes están deshabilitados de forma predeterminada en los clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-315">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="1cc20-316">Para habilitar el scripting, ejecute el siguiente comando de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="1cc20-316">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cc20-317">Publicar el paquete de Office 2016 globalmente</span><span class="sxs-lookup"><span data-stu-id="1cc20-317">Publish the Office 2016 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-318">Los puntos de extensión del paquete de Office App-V requieren instalación en el nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="1cc20-318">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="1cc20-319">Al publicar en el nivel de un equipo, no es necesario realizar acciones previas ni redistribuibles, y el paquete de Office 2016 globalmente permite que sus aplicaciones funcionen como Office instalado de forma nativa, eliminando la necesidad de administradores para personalizar paquetes.</span><span class="sxs-lookup"><span data-stu-id="1cc20-319">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2016 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1cc20-320">Cómo publicar un paquete de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-320">How to publish an Office package</span></span>

<span data-ttu-id="1cc20-321">Ejecute el siguiente comando para publicar un paquete de Office de forma global:</span><span class="sxs-lookup"><span data-stu-id="1cc20-321">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="1cc20-322">Desde la consola de administración web en el servidor de App-V, puede Agregar permisos a un grupo de equipos en lugar de a un grupo de usuarios para permitir que los paquetes se publiquen globalmente en los equipos del grupo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-322">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="1cc20-323">Personalizar y administrar paquetes de App-V de Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-323">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="1cc20-324">Para administrar los paquetes de App-V de Office, use las mismas operaciones que usaría para cualquier otro paquete, pero hay algunas excepciones, como se describe en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="1cc20-324">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="1cc20-325">Habilitar complementos de Office mediante grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="1cc20-325">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="1cc20-326">Deshabilitar aplicaciones de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-326">Disabling Office 2016 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="1cc20-327">Deshabilitar los métodos abreviados de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-327">Disabling Office 2016 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="1cc20-328">Administración de actualizaciones de paquetes de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-328">Managing Office 2016 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="1cc20-329">Implementación de Visio 2016 y Project 2016 con Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-329">Deploying Visio 2016 and Project 2016 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="1cc20-330">Habilitar complementos de Office mediante grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="1cc20-330">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="1cc20-331">Siga los pasos de esta sección para habilitar complementos de Office con su paquete de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-331">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="1cc20-332">Para usar complementos de Office, debe usar el secuenciador de App-V para crear un paquete independiente que contenga solo los complementos. No puede usar la herramienta de implementación de Office para crear el paquete de complementos.</span><span class="sxs-lookup"><span data-stu-id="1cc20-332">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="1cc20-333">Después, cree un grupo de conexiones que contenga el paquete de Office y el paquete de complementos, tal y como se describe en los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="1cc20-333">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="1cc20-334">Para habilitar los complementos para los paquetes de Office App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-334">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="1cc20-335">Agregue un grupo de conexión a través de App-V Server, System Center Configuration Manager o un cmdlet de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1cc20-335">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="1cc20-336">Ordene sus complementos con el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-336">Sequence your plug-ins using the App-V Sequencer.</span></span> <span data-ttu-id="1cc20-337">Asegúrese de que Office 2016 está instalado en el equipo que se usa para secuenciar el complemento.</span><span class="sxs-lookup"><span data-stu-id="1cc20-337">Ensure that Office 2016 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="1cc20-338">Se recomienda usar las aplicaciones de Microsoft 365 para empresas (no virtuales) en el equipo de secuenciación al secuenciar los complementos de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-338">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2016 plug-ins.</span></span>

3.  <span data-ttu-id="1cc20-339">Crear un paquete de App-V que incluya los complementos que desee.</span><span class="sxs-lookup"><span data-stu-id="1cc20-339">Create an App-V package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="1cc20-340">Agregue un grupo de conexión a través de App-V Server, System Center Configuration Manager o un cmdlet de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1cc20-340">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="1cc20-341">Agregue el paquete de aplicación de Office 2016 y el paquete de complementos que ha secuenciado al grupo de conexiones que ha creado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-341">Add the Office 2016 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    ><span data-ttu-id="1cc20-342">**Importante** El orden de los paquetes en el grupo de conexión determina el orden en el que se fusiona el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-342">**Important** The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="1cc20-343">En el archivo descriptor de grupo de conexión, agregue en primer lugar el paquete de Office 2016 App-V y, a continuación, agregue el paquete de aplicación de complementos.</span><span class="sxs-lookup"><span data-stu-id="1cc20-343">In your Connection group descriptor file, add the Office 2016 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="1cc20-344">Asegúrese de que ambos paquetes se publiquen en el equipo de destino y de que el paquete de complementos se publique globalmente para coincidir con la configuración global del paquete publicado de la aplicación de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-344">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2016 App-V package.</span></span>

7.  <span data-ttu-id="1cc20-345">Compruebe que el archivo de configuración de implementación del paquete de complementos tiene la misma configuración que tiene el paquete de Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-345">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2016 App-V package has.</span></span>

    <span data-ttu-id="1cc20-346">Dado que el paquete de Office 2016 App-V está integrado con el sistema operativo, la configuración del paquete de complementos debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="1cc20-346">Since the Office 2016 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="1cc20-347">Puede buscar el archivo de configuración de implementación de "modo COM" y asegurarse de que el paquete de complementos tiene ese valor configurado como "integrado" y que tanto "InProcessEnabled" como "OutOfProcessEnabled" coinciden con la configuración del paquete de Office 2016 App-V publicado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-347">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2016 App-V package you published.</span></span>

8.  <span data-ttu-id="1cc20-348">Abra el archivo de configuración de la implementación y establezca el valor de los **objetos habilitados** en **falso**.</span><span class="sxs-lookup"><span data-stu-id="1cc20-348">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="1cc20-349">Si ha realizado cambios en el archivo de configuración de la implementación después de la secuenciación, asegúrese de que el paquete de complemento se publique con el archivo.</span><span class="sxs-lookup"><span data-stu-id="1cc20-349">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="1cc20-350">Asegúrese de que el grupo de conexión que ha creado está habilitado en el equipo que desee.</span><span class="sxs-lookup"><span data-stu-id="1cc20-350">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="1cc20-351">Es probable que el grupo de conexiones creado sea "pendiente" si el paquete de Office 2016 App-V está en uso cuando el grupo de conexión está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-351">The Connection Group created will likely “pend” if the Office 2016 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="1cc20-352">Si esto sucede, debe reiniciar para habilitar correctamente el grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-352">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="1cc20-353">Después de publicar correctamente ambos paquetes y habilitar el grupo de conexión, inicie la aplicación de Office 2016 de destino y compruebe que el complemento publicado y agregado al grupo de conexiones funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="1cc20-353">After you successfully publish both packages and enable the Connection Group, start the target Office 2016 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="1cc20-354">Deshabilitar aplicaciones de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-354">Disabling Office 2016 applications</span></span>

<span data-ttu-id="1cc20-355">Es posible que desee deshabilitar aplicaciones específicas en el paquete de Office App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-355">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="1cc20-356">Por ejemplo, puede deshabilitar el acceso, pero deje disponible el resto de la aplicación de Office Main.</span><span class="sxs-lookup"><span data-stu-id="1cc20-356">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="1cc20-357">Al deshabilitar una aplicación, el usuario final ya no verá el acceso directo de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-357">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="1cc20-358">No es necesario volver a realizar la secuencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-358">You do not have to re-sequence the application.</span></span> <span data-ttu-id="1cc20-359">Al cambiar el archivo de configuración de implementación una vez publicado el paquete de Office 2016 App-V, guardará los cambios, agregará el paquete de aplicación de Office 2016 y después lo volverá a publicar con el nuevo archivo de configuración de implementación para aplicar la nueva configuración a las aplicaciones de paquete de Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-359">When you change the Deployment Configuration File after the Office 2016 App-V package has been published, you will save the changes, add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

><span data-ttu-id="1cc20-360">**Nota:** Para excluir determinadas aplicaciones de Office (por ejemplo, Access e InfoPath) al crear el paquete App-V con la herramienta de implementación de Office, use la configuración **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="1cc20-360">**Note** To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span>


**<span data-ttu-id="1cc20-361">Para deshabilitar una aplicación de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-361">To disable an Office 2016 application</span></span>**

1.  <span data-ttu-id="1cc20-362">Abra un archivo de configuración de implementación con un editor de texto como **el Bloc de notas** y busque "aplicaciones".</span><span class="sxs-lookup"><span data-stu-id="1cc20-362">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="1cc20-363">Busque la aplicación de Office que desea deshabilitar, por ejemplo, Access 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-363">Search for the Office application you want to disable, for example, Access 2016.</span></span>

3.  <span data-ttu-id="1cc20-364">Cambie el valor de "habilitado" de "verdadero" a "falso".</span><span class="sxs-lookup"><span data-stu-id="1cc20-364">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="1cc20-365">Guarde el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-365">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="1cc20-366">Agregue el paquete Office 2016 App-V con el nuevo archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-366">Add the Office 2016 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="1cc20-367">Vuelva a agregar el paquete de Office 2016 App-V y, a continuación, vuelva a publicarlo con el nuevo archivo de configuración de implementación para aplicar la nueva configuración a las aplicaciones de paquete de Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="1cc20-367">Re-add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="1cc20-368">Deshabilitar los métodos abreviados de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-368">Disabling Office 2016 shortcuts</span></span>

<span data-ttu-id="1cc20-369">Es posible que desee deshabilitar los métodos abreviados para determinadas aplicaciones de Office en lugar de anular la publicación o quitar el paquete.</span><span class="sxs-lookup"><span data-stu-id="1cc20-369">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="1cc20-370">En el ejemplo siguiente se muestra cómo deshabilitar los métodos abreviados de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1cc20-370">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="1cc20-371">Para deshabilitar los métodos abreviados de las aplicaciones de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-371">To disable shortcuts for Office 2016 applications</span></span>**

1.  <span data-ttu-id="1cc20-372">Abra un archivo de configuración de implementación en el Bloc de notas y busque "métodos abreviados".</span><span class="sxs-lookup"><span data-stu-id="1cc20-372">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="1cc20-373">Para deshabilitar determinados métodos abreviados, elimine o comente los accesos directos específicos que no desee.</span><span class="sxs-lookup"><span data-stu-id="1cc20-373">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="1cc20-374">Debe mantener el subsistema presente y habilitado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-374">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="1cc20-375">Por ejemplo, en el ejemplo siguiente, elimine los métodos abreviados de Microsoft Access, manteniendo intacto el método abreviado de subsistemas &lt; &gt; &lt; &gt; para deshabilitar el acceso directo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1cc20-375">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="1cc20-376">Guarde el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-376">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="1cc20-377">Vuelva a publicar el paquete de aplicación de Office 2016 con el nuevo archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="1cc20-377">Republish Office 2016 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="1cc20-378">Muchas configuraciones adicionales se pueden cambiar con la modificación de la configuración de implementación para paquetes de App-V, por ejemplo, asociaciones de tipo de archivo, sistema de archivos virtual y más.</span><span class="sxs-lookup"><span data-stu-id="1cc20-378">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="1cc20-379">Para obtener más información sobre cómo usar los archivos de configuración de implementación para cambiar la configuración de paquetes de App-V, consulte la sección recursos adicionales al final de este documento.</span><span class="sxs-lookup"><span data-stu-id="1cc20-379">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="1cc20-380">Administración de actualizaciones de paquetes de Office 2016</span><span class="sxs-lookup"><span data-stu-id="1cc20-380">Managing Office 2016 package upgrades</span></span>

<span data-ttu-id="1cc20-381">Para actualizar un paquete de Office 2016, use la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-381">To upgrade an Office 2016 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="1cc20-382">Para actualizar un paquete de Office 2016 implementado anteriormente, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="1cc20-382">To upgrade a previously deployed Office 2016 package, perform the following steps.</span></span>

**<span data-ttu-id="1cc20-383">Cómo actualizar un paquete de Office 2016 implementado previamente</span><span class="sxs-lookup"><span data-stu-id="1cc20-383">How to upgrade a previously deployed Office 2016 package</span></span>**

1. <span data-ttu-id="1cc20-384">Cree un nuevo paquete de Office 2016 mediante la herramienta de implementación de Office que usa el software de la aplicación Office 2016 más reciente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-384">Create a new Office 2016 package through the Office Deployment Tool that uses the most recent Office 2016 application software.</span></span> <span data-ttu-id="1cc20-385">Los Office 2016 bits más recientes siempre pueden obtenerse a través de la fase de descarga de la creación de un paquete de App-V de Office 2016.</span><span class="sxs-lookup"><span data-stu-id="1cc20-385">The most recent Office 2016 bits can always be obtained through the download stage of creating an Office 2016 App-V Package.</span></span> <span data-ttu-id="1cc20-386">El paquete de Office 2016 recién creado tendrá las actualizaciones más recientes y un nuevo identificador de versión.</span><span class="sxs-lookup"><span data-stu-id="1cc20-386">The newly created Office 2016 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="1cc20-387">Todos los paquetes creados con la herramienta de implementación de Office tienen el mismo linaje.</span><span class="sxs-lookup"><span data-stu-id="1cc20-387">All packages created using the Office Deployment Tool have the same lineage.</span></span>

   > <span data-ttu-id="1cc20-388">**Nota:** Los paquetes de Office App-V tienen dos identificadores de versión:</span><span class="sxs-lookup"><span data-stu-id="1cc20-388">**Note** Office App-V packages have two Version IDs:</span></span>
   > <ul>
   > <li><span data-ttu-id="1cc20-389">Un identificador de versión de paquete de Office 2016 App-V que sea único en todos los paquetes creados con la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-389">An Office 2016 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span></li>
   > <li><span data-ttu-id="1cc20-390">Un segundo identificador de versión de paquete de App-V, x. x. x, por ejemplo, en el manifiesto de AppX que solo cambiará si hay una nueva versión de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-390">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="1cc20-391">Por ejemplo, si hay disponible una nueva versión de Office 2016 con actualizaciones y se crea un paquete a través de la herramienta de implementación de Office para incorporar estas actualizaciones, el identificador de versión x. x. x cambiará para reflejar que la versión de Office en sí ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1cc20-391">For example, if a new Office 2016 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="1cc20-392">El servidor de App-V usará el identificador de versión x. x. x. x para diferenciar este paquete y reconoceremos que contiene nuevas actualizaciones para el paquete publicado anteriormente, y, como resultado, la publicaremos como una actualización al paquete de Office 2016 existente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-392">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2016 package.</span></span></li>
   > </ul>


2. <span data-ttu-id="1cc20-393">Publique globalmente los paquetes de App-V de Office 2016 recién creados en equipos en los que desea aplicar las nuevas actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-393">Globally publish the newly created Office 2016 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="1cc20-394">Puesto que el nuevo paquete tiene el mismo linaje del paquete antiguo Office 2016 App-V, publicar el nuevo paquete con las actualizaciones solo aplicará los nuevos cambios en el paquete antiguo y, por lo tanto, será rápido.</span><span class="sxs-lookup"><span data-stu-id="1cc20-394">Since the new package has the same lineage of the older Office 2016 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3. <span data-ttu-id="1cc20-395">Las actualizaciones se aplicarán de la misma manera que cualquier paquete de App-V publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="1cc20-395">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="1cc20-396">Debido a que es probable que las aplicaciones estén en uso, las actualizaciones pueden retrasarse hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="1cc20-396">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>


### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="1cc20-397">Implementación de Visio 2016 y Project 2016 con Office</span><span class="sxs-lookup"><span data-stu-id="1cc20-397">Deploying Visio 2016 and Project 2016 with Office</span></span>

<span data-ttu-id="1cc20-398">En la tabla siguiente se describen los requisitos y las opciones para implementar Visio 2016 y Project 2016 con Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-398">The following table describes the requirements and options for deploying Visio 2016 and Project 2016 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-399">Tarea</span><span class="sxs-lookup"><span data-stu-id="1cc20-399">Task</span></span></th>
<th align="left"><span data-ttu-id="1cc20-400">Detalles</span><span class="sxs-lookup"><span data-stu-id="1cc20-400">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-401">¿Cómo se empaquetan y publican Visio 2016 y Project 2016 con Office?</span><span class="sxs-lookup"><span data-stu-id="1cc20-401">How do I package and publish Visio 2016 and Project 2016 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-402">Debe incluir Visio 2016 y el proyecto 2016 en el mismo paquete de Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-402">You must include Visio 2016 and Project 2016 in the same package with Office.</span></span></p>
<p><span data-ttu-id="1cc20-403">Si no está implementando Office, puede crear un paquete que contenga Visio o Project, siempre y cuando siga los requisitos de empaquetado, publicación e implementación descritos en este tema.</span><span class="sxs-lookup"><span data-stu-id="1cc20-403">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow the packaging, publishing, and deployment requirements described in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cc20-404">¿Cómo puedo implementar Visio 2016 y Project 2016 en usuarios específicos?</span><span class="sxs-lookup"><span data-stu-id="1cc20-404">How can I deploy Visio 2016 and Project 2016 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-405">Use uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1cc20-405">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cc20-406">Si desea...</span><span class="sxs-lookup"><span data-stu-id="1cc20-406">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="1cc20-407">... después, use este método</span><span class="sxs-lookup"><span data-stu-id="1cc20-407">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cc20-408">Crear dos paquetes diferentes e implementar cada uno en un grupo de usuarios diferente</span><span class="sxs-lookup"><span data-stu-id="1cc20-408">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-409">Cree e implemente los siguientes paquetes:</span><span class="sxs-lookup"><span data-stu-id="1cc20-409">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="1cc20-410">Paquete que contiene solo Office-implementar en equipos cuyos usuarios solo necesitan Office.</span><span class="sxs-lookup"><span data-stu-id="1cc20-410">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-411">Un paquete que contiene Office, Visio y Project-implementar en equipos cuyos usuarios necesitan las tres aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1cc20-411">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cc20-412">Si desea solo un paquete para toda la organización o si tiene usuarios que comparten equipos:</span><span class="sxs-lookup"><span data-stu-id="1cc20-412">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cc20-413">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="1cc20-413">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="1cc20-414">Cree un paquete que contenga Office, Visio y Project.</span><span class="sxs-lookup"><span data-stu-id="1cc20-414">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-415">Implementar el paquete para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1cc20-415">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="1cc20-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> para evitar que usuarios específicos usen Visio y Project.</span><span class="sxs-lookup"><span data-stu-id="1cc20-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="1cc20-417">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1cc20-417">Additional resources</span></span>


[<span data-ttu-id="1cc20-418">Implementación de Microsoft Office 2013 mediante el uso de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-418">Deploying Microsoft Office 2013 by Using App-V</span></span>](deploying-microsoft-office-2013-by-using-app-v.md)

[<span data-ttu-id="1cc20-419">Implementación de Microsoft Office 2010 mediante el uso de App-V</span><span class="sxs-lookup"><span data-stu-id="1cc20-419">Deploying Microsoft Office 2010 by Using App-V</span></span>](deploying-microsoft-office-2010-by-using-app-v.md)

[<span data-ttu-id="1cc20-420">Herramienta de implementación de Office 2016 para hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="1cc20-420">Office 2016 Deployment Tool for Click-to-Run</span></span>](https://www.microsoft.com/download/details.aspx?id=49117)

**<span data-ttu-id="1cc20-421">Grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="1cc20-421">Connection Groups</span></span>**

[<span data-ttu-id="1cc20-422">Implementación de grupos de conexión en Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="1cc20-422">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="1cc20-423">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="1cc20-423">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="1cc20-424">Configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="1cc20-424">Dynamic Configuration</span></span>**

[<span data-ttu-id="1cc20-425">Acerca de la configuración dinámica de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="1cc20-425">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)





