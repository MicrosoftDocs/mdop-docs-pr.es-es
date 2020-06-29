---
title: Implementación de Microsoft Office 2013 mediante el uso de App-V
description: Implementación de Microsoft Office 2013 mediante el uso de App-V
author: dansimp
ms.assetid: 02df5dc8-79e2-4c5c-8398-dbfb23344ab3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: c57227d531c61949f9160c27fc249db72dbc6523
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814631"
---
# <span data-ttu-id="ff59a-103">Implementación de Microsoft Office 2013 mediante el uso de App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="ff59a-104">Use la información de este artículo para usar Microsoft Application Virtualization 5,0, o versiones posteriores, para ofrecer Microsoft Office 2013 como una aplicación virtualizada a los equipos de su organización.</span><span class="sxs-lookup"><span data-stu-id="ff59a-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="ff59a-105">Para obtener información sobre cómo usar App-V para ofrecer Office 2010, consulte [implementar Microsoft office 2010 mediante App-v](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="ff59a-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span> <span data-ttu-id="ff59a-106">Para implementar correctamente Office 2013 con App-V, debe estar familiarizado con Office 2013 y PP-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and pp-V.</span></span>

<span data-ttu-id="ff59a-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="ff59a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="ff59a-108">Qué debe saber antes de empezar</span><span class="sxs-lookup"><span data-stu-id="ff59a-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="ff59a-109">Crear un paquete de Office 2013 para App-V con la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="ff59a-110">Publicar el paquete de Office para App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ff59a-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="ff59a-111">Personalizar y administrar paquetes de App-V de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="ff59a-112">Qué debe saber antes de empezar</span><span class="sxs-lookup"><span data-stu-id="ff59a-112">What to know before you start</span></span>


<span data-ttu-id="ff59a-113">Antes de implementar Office 2013 mediante App-V, revise la siguiente información de planeación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="ff59a-114">Versiones de Office compatibles y coexistencia de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="ff59a-115">Use la siguiente tabla para obtener información acerca de las versiones compatibles de Office y acerca de la ejecución de versiones coexistentes de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-116">Información para revisar</span><span class="sxs-lookup"><span data-stu-id="ff59a-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="ff59a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff59a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="ff59a-118">Planificación para el uso de App-V con Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ff59a-119">Versiones compatibles de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="ff59a-120">Tipos de implementación admitidos (por ejemplo, escritorio, infraestructura de escritorio virtual personal (VDI), VDI agrupada)</span><span class="sxs-lookup"><span data-stu-id="ff59a-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="ff59a-121">Opciones de licencia de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="ff59a-122">Planificación para el uso de App-V con Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ff59a-123">Consideraciones para instalar diferentes versiones de Office en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="ff59a-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="ff59a-124">Requisitos de empaquetado, publicación e implementación</span><span class="sxs-lookup"><span data-stu-id="ff59a-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="ff59a-125">Antes de implementar Office con App-V, revise los siguientes requisitos.</span><span class="sxs-lookup"><span data-stu-id="ff59a-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-126">Tarea</span><span class="sxs-lookup"><span data-stu-id="ff59a-126">Task</span></span></th>
<th align="left"><span data-ttu-id="ff59a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff59a-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-128">Empaquetado</span><span class="sxs-lookup"><span data-stu-id="ff59a-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ff59a-129">Todas las aplicaciones de Office que desee implementar para los usuarios deben tener un único paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-130">En App-V 5,0 y versiones posteriores, debe usar la herramienta de implementación de Office para crear paquetes.</span><span class="sxs-lookup"><span data-stu-id="ff59a-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="ff59a-131">No puede usar el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="ff59a-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-132">Si va a implementar Microsoft Visio 2013 y Microsoft Project 2013 junto con Office, debe incluirlos en el mismo paquete que Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="ff59a-133">Para obtener más información, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> implementar Visio 2013 y Project 2013 con Office </a> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff59a-134">Publicación</span><span class="sxs-lookup"><span data-stu-id="ff59a-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ff59a-135">Solo puede publicar un paquete de Office en cada equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-136">Debe publicar el paquete de Office globalmente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-136">You must publish the Office package globally.</span></span> <span data-ttu-id="ff59a-137">No puede publicar para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ff59a-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-138">Implementar cualquiera de los siguientes productos en un equipo compartido, por ejemplo, con servicios de escritorio remoto:</span><span class="sxs-lookup"><span data-stu-id="ff59a-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff59a-139">Aplicaciones de Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="ff59a-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="ff59a-140">Visio Pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="ff59a-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="ff59a-141">Project Pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="ff59a-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="ff59a-142">Debe habilitar la <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> activación en equipos compartidos </a> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="ff59a-143">No se usa la activación en equipos compartidos si está implementando un producto con licencia por volumen, como:</span><span class="sxs-lookup"><span data-stu-id="ff59a-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff59a-144">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="ff59a-145">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="ff59a-146">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="ff59a-147">Excluir aplicaciones de Office de un paquete</span><span class="sxs-lookup"><span data-stu-id="ff59a-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="ff59a-148">En la siguiente tabla se describen los métodos recomendados para excluir aplicaciones específicas de Office de un paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-149">Tarea</span><span class="sxs-lookup"><span data-stu-id="ff59a-149">Task</span></span></th>
<th align="left"><span data-ttu-id="ff59a-150">Detalles</span><span class="sxs-lookup"><span data-stu-id="ff59a-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-151">Use la <strong> </strong> configuración ExcludeApp al crear el paquete con la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ff59a-152">Permite excluir determinadas aplicaciones de Office del paquete cuando la herramienta de implementación de Office crea el paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="ff59a-153">Por ejemplo, puede usar esta opción para crear un paquete que solo contenga Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="ff59a-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-154">Para obtener más información, consulta <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff59a-155">Modificar el archivo de DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="ff59a-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ff59a-156">Modifique el archivo DeploymentConfig.xml después de que se haya creado el paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="ff59a-157">Este archivo contiene la configuración de paquete predeterminada para todos los usuarios de un equipo que ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-158">Para obtener más información, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> deshabilitar aplicaciones de Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="ff59a-159">Crear un paquete de Office 2013 para App-V con la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="ff59a-160">Complete los pasos siguientes para crear un paquete de Office 2013 para App-V 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ff59a-160">Complete the following steps to create an Office 2013 package for App-V 5.0 or later.</span></span>

**<span data-ttu-id="ff59a-161">Importante</span><span class="sxs-lookup"><span data-stu-id="ff59a-161">Important</span></span>**  
<span data-ttu-id="ff59a-162">En App-V 5,0 y versiones posteriores, debe disponer de la herramienta de implementación de Office para crear un paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-162">In App-V 5.0 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="ff59a-163">No puede usar el secuenciador para crear paquetes.</span><span class="sxs-lookup"><span data-stu-id="ff59a-163">You cannot use the Sequencer to create packages.</span></span>


### <span data-ttu-id="ff59a-164">Revisar los requisitos previos para usar la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="ff59a-165">El equipo en el que está instalando la herramienta de implementación de Office debe tener:</span><span class="sxs-lookup"><span data-stu-id="ff59a-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-166">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="ff59a-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="ff59a-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff59a-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-168">Requisitos previos de software</span><span class="sxs-lookup"><span data-stu-id="ff59a-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="ff59a-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff59a-170">Sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="ff59a-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ff59a-171">versión de 64 bits de Windows 8</span><span class="sxs-lookup"><span data-stu-id="ff59a-171">64-bit version of Windows 8</span></span></p></li>
<li><p><span data-ttu-id="ff59a-172">versión de 64 bits de Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff59a-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


**<span data-ttu-id="ff59a-173">Nota</span><span class="sxs-lookup"><span data-stu-id="ff59a-173">Note</span></span>**  
<span data-ttu-id="ff59a-174">En este tema, el término "paquete de App-V de Office 2013" se refiere a licencias de suscripción y licencias por volumen.</span><span class="sxs-lookup"><span data-stu-id="ff59a-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>


### <span data-ttu-id="ff59a-175">Crear paquetes de Office 2013 App-V con la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="ff59a-176">Para crear paquetes de Office 2013 App-V, use la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="ff59a-177">En las siguientes instrucciones se explica cómo crear un paquete de App-V de Office 2013 con licencias por volumen o licencias de suscripciones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="ff59a-178">Crear paquetes de aplicación de Office 2013 en equipos Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ff59a-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="ff59a-179">Una vez creado, el paquete de Office 2013 App-V se ejecutará en equipos Windows 7 y Windows 8 de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ff59a-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="ff59a-180">Descargar la herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="ff59a-181">Los paquetes de Office 2013 App-V se crean con la herramienta de implementación de Office, que genera un paquete de App-V de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="ff59a-182">El paquete no se puede crear ni modificar mediante el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="ff59a-183">Para comenzar la creación del paquete:</span><span class="sxs-lookup"><span data-stu-id="ff59a-183">To begin package creation:</span></span>

1.  <span data-ttu-id="ff59a-184">Descargue la [herramienta de implementación de Office para hacer clic y ejecutar](https://www.microsoft.com/download/details.aspx?id=36778).</span><span class="sxs-lookup"><span data-stu-id="ff59a-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="ff59a-185">Ejecute el archivo. exe y extraiga sus características en la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="ff59a-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="ff59a-186">Para facilitar este proceso, puede crear una carpeta de red compartida donde se guardarán las características.</span><span class="sxs-lookup"><span data-stu-id="ff59a-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="ff59a-187">Ejemplo: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="ff59a-188">Compruebe que exista un setup.exe y un archivo configuration.xml y que se encuentren en la ubicación que especificó.</span><span class="sxs-lookup"><span data-stu-id="ff59a-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="ff59a-189">Descargar aplicaciones de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-189">Download Office 2013 applications</span></span>

<span data-ttu-id="ff59a-190">Después de descargar la herramienta de implementación de Office, puede usarla para obtener las aplicaciones de Office 2013 más recientes.</span><span class="sxs-lookup"><span data-stu-id="ff59a-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="ff59a-191">Después de obtener las aplicaciones de Office, cree el paquete de Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="ff59a-192">El archivo XML incluido en la herramienta de implementación de Office especifica los detalles del producto, como los idiomas y las aplicaciones de Office incluidos.</span><span class="sxs-lookup"><span data-stu-id="ff59a-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="ff59a-193">**Personalizar el archivo de configuración XML de ejemplo:** Use el archivo de configuración XML de ejemplo que haya descargado con la herramienta de implementación de Office para personalizar las aplicaciones de Office:</span><span class="sxs-lookup"><span data-stu-id="ff59a-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="ff59a-194">Abra el archivo XML de muestra en el Bloc de notas o su editor de texto preferido.</span><span class="sxs-lookup"><span data-stu-id="ff59a-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="ff59a-195">Con el archivo de configuration.xml de ejemplo abierto y listo para editar, puede especificar productos, idiomas y la ruta de acceso en la que guarda las aplicaciones de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="ff59a-196">A continuación se encuentra un ejemplo básico del archivo de configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="ff59a-196">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      **<span data-ttu-id="ff59a-197">Nota</span><span class="sxs-lookup"><span data-stu-id="ff59a-197">Note</span></span>**  
      <span data-ttu-id="ff59a-198">La configuración de XML es un archivo XML de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="ff59a-199">El archivo incluye líneas con comentarios. Puede "Quitar comentarios" estas líneas para personalizar la configuración adicional con el archivo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>

      <span data-ttu-id="ff59a-200">El archivo de configuración XML anterior especifica que Office 2013 ProPlus 32-bit Edition, incluido Visio ProPlus, se descargará en inglés al \\\\server\\Office 2013, que es la ubicación donde se guardarán las aplicaciones de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-200">The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="ff59a-201">Tenga en cuenta que el identificador de producto de las aplicaciones no afectará al final de la licencia de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-201">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="ff59a-202">Los paquetes de Office 2013 App-V con varias licencias se pueden crear a partir de las mismas aplicaciones mediante la especificación de licencias en una fase posterior.</span><span class="sxs-lookup"><span data-stu-id="ff59a-202">Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="ff59a-203">La tabla siguiente resume los atributos personalizables y los elementos del archivo XML:</span><span class="sxs-lookup"><span data-stu-id="ff59a-203">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="ff59a-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff59a-204">Input</span></span></th>
      <th align="left"><span data-ttu-id="ff59a-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff59a-205">Description</span></span></th>
      <th align="left"><span data-ttu-id="ff59a-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff59a-206">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="ff59a-207">Elemento Add</span><span class="sxs-lookup"><span data-stu-id="ff59a-207">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-208">Especifica los productos e idiomas que se van a incluir en el paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-208">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-209">N/D</span><span class="sxs-lookup"><span data-stu-id="ff59a-209">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="ff59a-210">OfficeClientEdition (atributo del elemento "Add")</span><span class="sxs-lookup"><span data-stu-id="ff59a-210">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-211">Especifica la edición de Office 2013 producto que se va a usar: 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ff59a-211">Specifies the edition of Office 2013 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="ff59a-212">Se produce un error en la operación si <strong> OfficeClientEdition </strong> no se establece en un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ff59a-212">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="ff59a-213">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="ff59a-213">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="ff59a-214">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="ff59a-214">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="ff59a-215">Elemento Product</span><span class="sxs-lookup"><span data-stu-id="ff59a-215">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-216">Especifica la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-216">Specifies the application.</span></span> <span data-ttu-id="ff59a-217">El proyecto 2013 y Visio 2013 deben especificarse aquí como un producto agregado que se incluirá en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-217">Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</span></span></p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
      <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
      <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="ff59a-218">Elemento de lenguaje</span><span class="sxs-lookup"><span data-stu-id="ff59a-218">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-219">Especifica el idioma admitido en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-219">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="ff59a-220">Version (atributo del elemento Add)</span><span class="sxs-lookup"><span data-stu-id="ff59a-220">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-221">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ff59a-221">Optional.</span></span> <span data-ttu-id="ff59a-222">Especifica la compilación que se usará para el paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-222">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="ff59a-223">De forma predeterminada, es la compilación anunciada más reciente (según se define en v32.CAB en el origen de Office).</span><span class="sxs-lookup"><span data-stu-id="ff59a-223">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>15.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="ff59a-224">SourcePath (atributo del elemento "Add")</span><span class="sxs-lookup"><span data-stu-id="ff59a-224">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ff59a-225">Especifica la ubicación en la que se guardarán las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-225">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2013”</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="ff59a-226">Después de editar el archivo configuration.xml para especificar el producto, los idiomas y la ubicación en que se guardarán las aplicaciones de Office 2013, por ejemplo, puede guardar el archivo de configuración como Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ff59a-226">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="ff59a-227">**Descargue las aplicaciones en la ubicación especificada:** Use un símbolo del sistema con privilegios elevados y un sistema operativo de 64 bits para descargar las aplicaciones de Office 2013 que se convertirán más adelante en un paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-227">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="ff59a-228">A continuación se muestra un comando de ejemplo con una descripción de los detalles:</span><span class="sxs-lookup"><span data-stu-id="ff59a-228">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="ff59a-229">En el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ff59a-229">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-230">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-230">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-231">es la ubicación del recurso compartido de red que contiene la herramienta de implementación de Office y el archivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ff59a-231">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ff59a-232">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="ff59a-232">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-233">es la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-233">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-234">/Download</span><span class="sxs-lookup"><span data-stu-id="ff59a-234">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-235">Descarga las aplicaciones de Office 2013 que especifique en el archivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ff59a-235">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="ff59a-236">Estos bits pueden convertirse más tarde en un paquete de App-V de Office 2013 con licencias por volumen.</span><span class="sxs-lookup"><span data-stu-id="ff59a-236">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ff59a-237">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ff59a-237">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-238">pasa el archivo de configuración XML necesario para completar el proceso de descarga, en este ejemplo, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ff59a-238">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="ff59a-239">Después de usar el comando de descarga, las aplicaciones de Office deberían encontrarse en la ubicación especificada en el archivo XML de configuración, en este ejemplo \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-239">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="ff59a-240">Convertir las aplicaciones de Office en un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-240">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="ff59a-241">Después de descargar las aplicaciones de Office 2013 mediante la herramienta de implementación de Office, use la herramienta de implementación de Office para convertirlas en un paquete de App-V de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-241">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="ff59a-242">Complete los pasos que correspondan al modelo de licencias.</span><span class="sxs-lookup"><span data-stu-id="ff59a-242">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="ff59a-243">Resumen de lo que debe hacer:</span><span class="sxs-lookup"><span data-stu-id="ff59a-243">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="ff59a-244">Crear los paquetes de App-V de Office 2013 en equipos Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ff59a-244">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="ff59a-245">Sin embargo, el paquete se ejecutará 32 en equipos con Windows 7 y Windows 8 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ff59a-245">However, the package will run on 32-bit and 64-bit Windows 7 and Windows 8 computers.</span></span>

-   <span data-ttu-id="ff59a-246">Cree un paquete de Office App-V para el paquete de licencias de suscripciones o para licencias por volumen con la herramienta de implementación de Office y, a continuación, modifique el CustomConfig.xml archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="ff59a-246">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="ff59a-247">En la siguiente tabla se resumen los valores que debe introducir en el archivo CustomConfig.xml del modelo de licencias que está usando.</span><span class="sxs-lookup"><span data-stu-id="ff59a-247">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="ff59a-248">Los pasos que se indican en las secciones siguientes de la tabla especificarán las entradas exactas que tiene que hacer.</span><span class="sxs-lookup"><span data-stu-id="ff59a-248">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-249">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="ff59a-249">Product ID</span></span></th>
<th align="left"><span data-ttu-id="ff59a-250">Licencias por volumen</span><span class="sxs-lookup"><span data-stu-id="ff59a-250">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="ff59a-251">Licencias de suscripciones</span><span class="sxs-lookup"><span data-stu-id="ff59a-251">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ff59a-252">Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-252">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ff59a-253">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="ff59a-253">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-254">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="ff59a-254">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ff59a-255">Office 2013 con Visio 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-255">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ff59a-256">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="ff59a-256">ProPlusVolume</span></span></p>
<p><span data-ttu-id="ff59a-257">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="ff59a-257">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-258">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="ff59a-258">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="ff59a-259">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="ff59a-259">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ff59a-260">Office 2013 con Visio 2013 y Project 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-260">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ff59a-261">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="ff59a-261">ProPlusVolume</span></span></p>
<p><span data-ttu-id="ff59a-262">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="ff59a-262">VisioProVolume</span></span></p>
<p><span data-ttu-id="ff59a-263">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="ff59a-263">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-264">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="ff59a-264">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="ff59a-265">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="ff59a-265">VisioProRetail</span></span></p>
<p><span data-ttu-id="ff59a-266">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="ff59a-266">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ff59a-267">Cómo convertir las aplicaciones de Office en un paquete de App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-267">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="ff59a-268">En el Bloc de notas, vuelva a abrir el archivo CustomConfig.xml y realice los cambios siguientes en el archivo:</span><span class="sxs-lookup"><span data-stu-id="ff59a-268">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="ff59a-269">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ff59a-269">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="ff59a-270">Qué cambiar el valor a</span><span class="sxs-lookup"><span data-stu-id="ff59a-270">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="ff59a-271">RutaOrigen</span><span class="sxs-lookup"><span data-stu-id="ff59a-271">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-272">Apunte a las aplicaciones de Office descargadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-272">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="ff59a-273">ProductID</span><span class="sxs-lookup"><span data-stu-id="ff59a-273">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-274">Especifique el tipo de licencia, como se muestra en los siguientes ejemplos:</span><span class="sxs-lookup"><span data-stu-id="ff59a-274">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="ff59a-275">Licencias de suscripciones</span><span class="sxs-lookup"><span data-stu-id="ff59a-275">Subscription Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="ff59a-276">En este ejemplo, se han realizado los cambios siguientes para crear un paquete con licencias de suscripciones:</span><span class="sxs-lookup"><span data-stu-id="ff59a-276">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-277">RutaOrigen</span><span class="sxs-lookup"><span data-stu-id="ff59a-277">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-278">es la ruta de acceso, que se cambió para que apunte a las aplicaciones de Office que se descargaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-278">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ff59a-279">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="ff59a-279">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-280">para Office se cambió a <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-280">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-281">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="ff59a-281">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-282">para Visio se cambió a <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-282">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="ff59a-283">Licencias por volumen</span><span class="sxs-lookup"><span data-stu-id="ff59a-283">Volume Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p><span data-ttu-id="ff59a-284">En este ejemplo, se han realizado los cambios siguientes para crear un paquete con licencias por volumen:</span><span class="sxs-lookup"><span data-stu-id="ff59a-284">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-285">RutaOrigen</span><span class="sxs-lookup"><span data-stu-id="ff59a-285">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-286">es la ruta de acceso, que se cambió para que apunte a las aplicaciones de Office que se descargaron anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-286">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ff59a-287">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="ff59a-287">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-288">para Office se cambió a <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-288">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-289">Id. del producto</span><span class="sxs-lookup"><span data-stu-id="ff59a-289">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-290">para Visio se cambió a <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-290">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="ff59a-291">ExcludeApp (opcional)</span><span class="sxs-lookup"><span data-stu-id="ff59a-291">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-292">Le permite especificar programas de Office que no desea incluir en el paquete de App-V que crea la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-292">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="ff59a-293">Por ejemplo, puede excluir Access e InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ff59a-293">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="ff59a-294">PACKAGEGUID (opcional)</span><span class="sxs-lookup"><span data-stu-id="ff59a-294">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-295">De forma predeterminada, todos los paquetes de App-V creados por la herramienta de implementación de Office comparten el mismo identificador de paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-295">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="ff59a-296">Puede usar PACKAGEGUID para especificar un identificador de paquete diferente para cada paquete, que le permite publicar varios paquetes de App-V, creados mediante la herramienta de implementación de Office, y administrarlos mediante el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-296">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="ff59a-297">Un ejemplo de Cuándo usar este parámetro es crear paquetes diferentes para diferentes usuarios.</span><span class="sxs-lookup"><span data-stu-id="ff59a-297">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="ff59a-298">Por ejemplo, puede crear un paquete con solo Office 2013 para algunos usuarios y crear otro paquete con Office 2013 y Visio 2013 para otro conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="ff59a-298">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="ff59a-299">Nota</span><span class="sxs-lookup"><span data-stu-id="ff59a-299">Note</span></span></strong><br/><p><span data-ttu-id="ff59a-300">Incluso si usas identificadores de paquete únicos, aún puedes implementar un solo paquete de App-V en un solo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-300">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="ff59a-301">Use el comando/Packager para convertir las aplicaciones de Office en un paquete de App-V de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-301">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="ff59a-302">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ff59a-302">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="ff59a-303">En el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ff59a-303">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-304">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-304">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-305">es la ubicación del recurso compartido de red que contiene la herramienta de implementación de Office y el archivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ff59a-305">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ff59a-306">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="ff59a-306">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-307">es la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-307">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-308">/packager</span><span class="sxs-lookup"><span data-stu-id="ff59a-308">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-309">crea el paquete de aplicación de Office 2013 con licencias por volumen, tal como se especifica en el archivo de customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ff59a-309">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ff59a-310">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ff59a-310">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-311">pasa el archivo XML de configuración (en este caso customConfig) que se ha preparado para la fase de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-311">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ff59a-312">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="ff59a-312">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ff59a-313">Especifica la ubicación del paquete de Office App-V recién creado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-313">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="ff59a-314">Compruebe que el paquete de Office 2013 App-V funciona correctamente:</span><span class="sxs-lookup"><span data-stu-id="ff59a-314">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="ff59a-315">Publique el paquete de App-V de Office 2013, creado globalmente, en un equipo de prueba y compruebe que aparecen los accesos directos de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-315">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="ff59a-316">Inicie algunas aplicaciones de Office 2013, como Excel o Word, para asegurarse de que el paquete funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="ff59a-316">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="ff59a-317">Publicar el paquete de Office para App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ff59a-317">Publishing the Office package for App-V 5.0</span></span>


<span data-ttu-id="ff59a-318">Use la siguiente información para publicar un paquete de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-318">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="ff59a-319">Métodos para publicar paquetes de Office App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-319">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="ff59a-320">Implemente el paquete de App-V para Office 2013 con los mismos métodos que usa para cualquier otro paquete:</span><span class="sxs-lookup"><span data-stu-id="ff59a-320">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="ff59a-321">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff59a-321">System Center Configuration Manager</span></span>

-   <span data-ttu-id="ff59a-322">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-322">App-V Server</span></span>

-   <span data-ttu-id="ff59a-323">Independiente a través de los comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff59a-323">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="ff59a-324">Publicar requisitos y requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ff59a-324">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-325">Requisito previo o requisito</span><span class="sxs-lookup"><span data-stu-id="ff59a-325">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="ff59a-326">Detalles</span><span class="sxs-lookup"><span data-stu-id="ff59a-326">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-327">Habilitar scripting de PowerShell en los clientes de App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-327">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-328">Para publicar paquetes de Office 2013, debe ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="ff59a-328">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="ff59a-329">Los scripts de paquetes están deshabilitados de forma predeterminada en los clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-329">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="ff59a-330">Para habilitar el scripting, ejecute el siguiente comando de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ff59a-330">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff59a-331">Publicar el paquete de Office 2013 globalmente</span><span class="sxs-lookup"><span data-stu-id="ff59a-331">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-332">Los puntos de extensión del paquete de Office App-V requieren instalación en el nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-332">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="ff59a-333">Al publicar en el nivel de un equipo, no es necesario realizar acciones previas ni redistribuibles, y el paquete de Office 2013 globalmente permite que sus aplicaciones funcionen como Office instalado de forma nativa, eliminando la necesidad de administradores para personalizar paquetes.</span><span class="sxs-lookup"><span data-stu-id="ff59a-333">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="ff59a-334">Cómo publicar un paquete de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-334">How to publish an Office package</span></span>

<span data-ttu-id="ff59a-335">Ejecute el siguiente comando para publicar un paquete de Office de forma global:</span><span class="sxs-lookup"><span data-stu-id="ff59a-335">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="ff59a-336">Desde la consola de administración web en el servidor de App-V, puede Agregar permisos a un grupo de equipos en lugar de a un grupo de usuarios para permitir que los paquetes se publiquen globalmente en los equipos del grupo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-336">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="ff59a-337">Personalizar y administrar paquetes de App-V de Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-337">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="ff59a-338">Para administrar los paquetes de App-V de Office, use las mismas operaciones que usaría para cualquier otro paquete, pero hay algunas excepciones, como se describe en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff59a-338">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="ff59a-339">Habilitar complementos de Office mediante grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="ff59a-339">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="ff59a-340">Deshabilitar aplicaciones de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-340">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="ff59a-341">Deshabilitar los métodos abreviados de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-341">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="ff59a-342">Administración de actualizaciones de paquetes de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-342">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="ff59a-343">Administración de actualizaciones de licencias de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-343">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="ff59a-344">Implementación de Visio 2013 y Project 2013 con Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-344">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="ff59a-345">Habilitar complementos de Office mediante grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="ff59a-345">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="ff59a-346">Siga los pasos de esta sección para habilitar complementos de Office con su paquete de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-346">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="ff59a-347">Para usar complementos de Office, debe usar el secuenciador de App-V para crear un paquete independiente que contenga solo los complementos. No puede usar la herramienta de implementación de Office para crear el paquete de complementos.</span><span class="sxs-lookup"><span data-stu-id="ff59a-347">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="ff59a-348">Después, cree un grupo de conexiones que contenga el paquete de Office y el paquete de complementos, tal y como se describe en los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="ff59a-348">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="ff59a-349">Para habilitar los complementos para los paquetes de Office App-V</span><span class="sxs-lookup"><span data-stu-id="ff59a-349">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="ff59a-350">Agregue un grupo de conexión a través de App-V Server, System Center Configuration Manager o un cmdlet de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff59a-350">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="ff59a-351">Ordene sus complementos con el secuenciador de aplicaciones-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ff59a-351">Sequence your plug-ins using the App-V 5.0 Sequencer.</span></span> <span data-ttu-id="ff59a-352">Asegúrese de que Office 2013 está instalado en el equipo que se usa para secuenciar el complemento.</span><span class="sxs-lookup"><span data-stu-id="ff59a-352">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="ff59a-353">Se recomienda usar las aplicaciones de Microsoft 365 para empresas (no virtuales) en el equipo de secuenciación al secuenciar los complementos de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-353">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="ff59a-354">Cree un paquete de App-V 5,0 que incluya los complementos que desee.</span><span class="sxs-lookup"><span data-stu-id="ff59a-354">Create an App-V 5.0 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="ff59a-355">Agregue un grupo de conexión a través de App-V Server, System Center Configuration Manager o un cmdlet de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff59a-355">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="ff59a-356">Agregue el paquete de aplicación de Office 2013 y el paquete de complementos que ha secuenciado al grupo de conexiones que ha creado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-356">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="ff59a-357">Importante</span><span class="sxs-lookup"><span data-stu-id="ff59a-357">Important</span></span>**  
    <span data-ttu-id="ff59a-358">El orden de los paquetes en el grupo de conexión determina el orden en el que se fusiona el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-358">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="ff59a-359">En el archivo descriptor de grupo de conexión, agregue en primer lugar el paquete de Office 2013 App-V y, a continuación, agregue el paquete de aplicación de complementos.</span><span class="sxs-lookup"><span data-stu-id="ff59a-359">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="ff59a-360">Asegúrese de que ambos paquetes se publiquen en el equipo de destino y de que el paquete de complementos se publique globalmente para coincidir con la configuración global del paquete publicado de la aplicación de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-360">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="ff59a-361">Compruebe que el archivo de configuración de implementación del paquete de complementos tiene la misma configuración que tiene el paquete de Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-361">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="ff59a-362">Dado que el paquete de Office 2013 App-V está integrado con el sistema operativo, la configuración del paquete de complementos debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="ff59a-362">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="ff59a-363">Puede buscar el archivo de configuración de implementación de "modo COM" y asegurarse de que el paquete de complementos tiene ese valor configurado como "integrado" y que tanto "InProcessEnabled" como "OutOfProcessEnabled" coinciden con la configuración del paquete de Office 2013 App-V publicado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-363">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="ff59a-364">Abra el archivo de configuración de la implementación y establezca el valor de los **objetos habilitados** en **falso**.</span><span class="sxs-lookup"><span data-stu-id="ff59a-364">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="ff59a-365">Si ha realizado cambios en el archivo de configuración de la implementación después de la secuenciación, asegúrese de que el paquete de complemento se publique con el archivo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-365">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="ff59a-366">Asegúrese de que el grupo de conexión que ha creado está habilitado en el equipo que desee.</span><span class="sxs-lookup"><span data-stu-id="ff59a-366">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="ff59a-367">Es probable que el grupo de conexiones creado sea "pendiente" si el paquete de Office 2013 App-V está en uso cuando el grupo de conexión está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-367">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="ff59a-368">Si esto sucede, debe reiniciar para habilitar correctamente el grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-368">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="ff59a-369">Después de publicar correctamente ambos paquetes y habilitar el grupo de conexión, inicie la aplicación de Office 2013 de destino y compruebe que el complemento publicado y agregado al grupo de conexiones funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="ff59a-369">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="ff59a-370">Deshabilitar aplicaciones de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-370">Disabling Office 2013 applications</span></span>

<span data-ttu-id="ff59a-371">Es posible que desee deshabilitar aplicaciones específicas en el paquete de Office App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-371">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="ff59a-372">Por ejemplo, puede deshabilitar el acceso, pero deje disponible el resto de la aplicación de Office Main.</span><span class="sxs-lookup"><span data-stu-id="ff59a-372">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="ff59a-373">Al deshabilitar una aplicación, el usuario final ya no verá el acceso directo de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-373">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="ff59a-374">No es necesario volver a realizar la secuencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-374">You do not have to re-sequence the application.</span></span> <span data-ttu-id="ff59a-375">Al cambiar el archivo de configuración de implementación una vez publicado el paquete de Office 2013 App-V, guardará los cambios, agregará el paquete de aplicación de Office 2013 y después lo volverá a publicar con el nuevo archivo de configuración de implementación para aplicar la nueva configuración a las aplicaciones de paquete de Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-375">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="ff59a-376">Nota</span><span class="sxs-lookup"><span data-stu-id="ff59a-376">Note</span></span>**  
<span data-ttu-id="ff59a-377">Para excluir determinadas aplicaciones de Office (por ejemplo, Access e InfoPath) al crear el paquete App-V con la herramienta de implementación de Office, use la configuración **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="ff59a-377">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="ff59a-378">Para obtener más información, vea [Referencia del archivo de configuration.xml de hacer clic y ejecutar](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="ff59a-378">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="ff59a-379">Para deshabilitar una aplicación de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-379">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="ff59a-380">Abra un archivo de configuración de implementación con un editor de texto como **el Bloc de notas** y busque "aplicaciones".</span><span class="sxs-lookup"><span data-stu-id="ff59a-380">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="ff59a-381">Busque la aplicación de Office que desea deshabilitar, por ejemplo, Access 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-381">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="ff59a-382">Cambie el valor de "habilitado" de "verdadero" a "falso".</span><span class="sxs-lookup"><span data-stu-id="ff59a-382">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="ff59a-383">Guarde el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-383">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="ff59a-384">Agregue el paquete Office 2013 App-V con el nuevo archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-384">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="ff59a-385">Vuelva a agregar el paquete de Office 2013 App-V y, a continuación, vuelva a publicarlo con el nuevo archivo de configuración de implementación para aplicar la nueva configuración a las aplicaciones de paquete de Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-385">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="ff59a-386">Deshabilitar los métodos abreviados de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-386">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="ff59a-387">Es posible que desee deshabilitar los métodos abreviados para determinadas aplicaciones de Office en lugar de anular la publicación o quitar el paquete.</span><span class="sxs-lookup"><span data-stu-id="ff59a-387">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="ff59a-388">En el ejemplo siguiente se muestra cómo deshabilitar los métodos abreviados de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ff59a-388">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="ff59a-389">Para deshabilitar los métodos abreviados de las aplicaciones de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-389">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="ff59a-390">Abra un archivo de configuración de implementación en el Bloc de notas y busque "métodos abreviados".</span><span class="sxs-lookup"><span data-stu-id="ff59a-390">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="ff59a-391">Para deshabilitar determinados métodos abreviados, elimine o comente los accesos directos específicos que no desee.</span><span class="sxs-lookup"><span data-stu-id="ff59a-391">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="ff59a-392">Debe mantener el subsistema presente y habilitado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-392">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="ff59a-393">Por ejemplo, en el ejemplo siguiente, elimine los métodos abreviados de Microsoft Access, manteniendo intacto el método abreviado de subsistemas &lt; &gt; &lt; &gt; para deshabilitar el acceso directo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ff59a-393">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="ff59a-394">Guarde el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-394">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="ff59a-395">Vuelva a publicar el paquete de aplicación de Office 2013 con el nuevo archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="ff59a-395">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="ff59a-396">Muchas configuraciones adicionales se pueden cambiar con la modificación de la configuración de implementación para paquetes de App-V, por ejemplo, asociaciones de tipo de archivo, sistema de archivos virtual y más.</span><span class="sxs-lookup"><span data-stu-id="ff59a-396">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="ff59a-397">Para obtener más información sobre cómo usar los archivos de configuración de implementación para cambiar la configuración de paquetes de App-V, consulte la sección recursos adicionales al final de este documento.</span><span class="sxs-lookup"><span data-stu-id="ff59a-397">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="ff59a-398">Administración de actualizaciones de paquetes de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-398">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="ff59a-399">Para actualizar un paquete de Office 2013, use la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-399">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="ff59a-400">Para actualizar un paquete de Office 2013 implementado anteriormente, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ff59a-400">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="ff59a-401">Cómo actualizar un paquete de Office 2013 implementado previamente</span><span class="sxs-lookup"><span data-stu-id="ff59a-401">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="ff59a-402">Cree un nuevo paquete de Office 2013 mediante la herramienta de implementación de Office que usa el software de la aplicación Office 2013 más reciente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-402">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="ff59a-403">Los Office 2013 bits más recientes siempre pueden obtenerse a través de la fase de descarga de la creación de un paquete de App-V de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ff59a-403">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="ff59a-404">El paquete de Office 2013 recién creado tendrá las actualizaciones más recientes y un nuevo identificador de versión.</span><span class="sxs-lookup"><span data-stu-id="ff59a-404">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="ff59a-405">Todos los paquetes creados con la herramienta de implementación de Office tienen el mismo linaje.</span><span class="sxs-lookup"><span data-stu-id="ff59a-405">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="ff59a-406">Nota</span><span class="sxs-lookup"><span data-stu-id="ff59a-406">Note</span></span>**  
    <span data-ttu-id="ff59a-407">Los paquetes de Office App-V tienen dos identificadores de versión:</span><span class="sxs-lookup"><span data-stu-id="ff59a-407">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="ff59a-408">Un identificador de versión de paquete de Office 2013 App-V que sea único en todos los paquetes creados con la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-408">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="ff59a-409">Un segundo identificador de versión de paquete de App-V, x. x. x, por ejemplo, en el manifiesto de AppX que solo cambiará si hay una nueva versión de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-409">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="ff59a-410">Por ejemplo, si hay disponible una nueva versión de Office 2013 con actualizaciones y se crea un paquete a través de la herramienta de implementación de Office para incorporar estas actualizaciones, el identificador de versión x. x. x cambiará para reflejar que la versión de Office en sí ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-410">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="ff59a-411">El servidor de App-V usará el identificador de versión x. x. x. x para diferenciar este paquete y reconoceremos que contiene nuevas actualizaciones para el paquete publicado anteriormente, y, como resultado, la publicaremos como una actualización al paquete de Office 2013 existente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-411">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="ff59a-412">Publique globalmente los paquetes de App-V de Office 2013 recién creados en equipos en los que desea aplicar las nuevas actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-412">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="ff59a-413">Puesto que el nuevo paquete tiene el mismo linaje del paquete antiguo Office 2013 App-V, publicar el nuevo paquete con las actualizaciones solo aplicará los nuevos cambios en el paquete antiguo y, por lo tanto, será rápido.</span><span class="sxs-lookup"><span data-stu-id="ff59a-413">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="ff59a-414">Las actualizaciones se aplicarán de la misma manera que cualquier paquete de App-V publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-414">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="ff59a-415">Debido a que es probable que las aplicaciones estén en uso, las actualizaciones pueden retrasarse hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-415">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="ff59a-416">Administración de actualizaciones de licencias de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-416">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="ff59a-417">Si un nuevo paquete de Office 2013 App-V tiene una licencia distinta de la del paquete de Office 2013 App-V implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ff59a-417">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="ff59a-418">Por ejemplo, el paquete de Office 2013 implementado es una suscripción basada en Office 2013 y el nuevo paquete de Office 2013 se basa en las licencias por volumen, se deben seguir las siguientes instrucciones para garantizar una actualización de licencias fluida:</span><span class="sxs-lookup"><span data-stu-id="ff59a-418">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="ff59a-419">Cómo actualizar una licencia de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff59a-419">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="ff59a-420">Vuelva a publicar el paquete de App-V de licencias de suscripción de Office 2013 ya implementado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-420">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="ff59a-421">Elimine el paquete App-V de licencias de suscripción de Office 2013 no publicado.</span><span class="sxs-lookup"><span data-stu-id="ff59a-421">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="ff59a-422">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="ff59a-422">Restart the computer.</span></span>

4.  <span data-ttu-id="ff59a-423">Agregue el nuevo paquete de licencias por volumen de Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ff59a-423">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="ff59a-424">Publique el paquete de App-V de Office 2013 agregado con licencias por volumen.</span><span class="sxs-lookup"><span data-stu-id="ff59a-424">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="ff59a-425">Se implementará correctamente un paquete de aplicación de Office 2013 con la licencia elegida.</span><span class="sxs-lookup"><span data-stu-id="ff59a-425">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="ff59a-426">Implementación de Visio 2013 y Project 2013 con Office</span><span class="sxs-lookup"><span data-stu-id="ff59a-426">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="ff59a-427">En la tabla siguiente se describen los requisitos y las opciones para implementar Visio 2013 y Project 2013 con Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-427">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-428">Tarea</span><span class="sxs-lookup"><span data-stu-id="ff59a-428">Task</span></span></th>
<th align="left"><span data-ttu-id="ff59a-429">Detalles</span><span class="sxs-lookup"><span data-stu-id="ff59a-429">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-430">¿Cómo se empaquetan y publican Visio 2013 y Project 2013 con Office?</span><span class="sxs-lookup"><span data-stu-id="ff59a-430">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-431">Debe incluir Visio 2013 y el proyecto 2013 en el mismo paquete de Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-431">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="ff59a-432">Si no está implementando Office, puede crear un paquete que contenga Visio o Project, siempre y cuando siga <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> implementando Microsoft Office 2010 con App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="ff59a-432">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff59a-433">¿Cómo puedo implementar Visio 2013 y Project 2013 en usuarios específicos?</span><span class="sxs-lookup"><span data-stu-id="ff59a-433">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-434">Use uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ff59a-434">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff59a-435">Si desea...</span><span class="sxs-lookup"><span data-stu-id="ff59a-435">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="ff59a-436">... después, use este método</span><span class="sxs-lookup"><span data-stu-id="ff59a-436">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff59a-437">Crear dos paquetes diferentes e implementar cada uno en un grupo de usuarios diferente</span><span class="sxs-lookup"><span data-stu-id="ff59a-437">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-438">Cree e implemente los siguientes paquetes:</span><span class="sxs-lookup"><span data-stu-id="ff59a-438">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="ff59a-439">Paquete que contiene solo Office-implementar en equipos cuyos usuarios solo necesitan Office.</span><span class="sxs-lookup"><span data-stu-id="ff59a-439">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-440">Un paquete que contiene Office, Visio y Project-implementar en equipos cuyos usuarios necesitan las tres aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ff59a-440">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff59a-441">Si desea solo un paquete para toda la organización o si tiene usuarios que comparten equipos:</span><span class="sxs-lookup"><span data-stu-id="ff59a-441">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff59a-442">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ff59a-442">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="ff59a-443">Cree un paquete que contenga Office, Visio y Project.</span><span class="sxs-lookup"><span data-stu-id="ff59a-443">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-444">Implementar el paquete para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ff59a-444">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="ff59a-445">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> para evitar que usuarios específicos usen Visio y Project.</span><span class="sxs-lookup"><span data-stu-id="ff59a-445">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ff59a-446">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ff59a-446">Additional resources</span></span>


**<span data-ttu-id="ff59a-447">Office 2013 App-V 5,0 paquetes 5,0 recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ff59a-447">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="ff59a-448">Herramienta de implementación de Office para hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="ff59a-448">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="ff59a-449">Escenarios admitidos para implementar Microsoft Office como un paquete de App-V con secuencia</span><span class="sxs-lookup"><span data-stu-id="ff59a-449">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="ff59a-450">Paquetes de Office 2010 App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ff59a-450">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="ff59a-451">Kit de secuenciación 2010 de Microsoft Office para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="ff59a-451">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="ff59a-452">Problemas conocidos al crear o usar un paquete de Office 2010 de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ff59a-452">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="ff59a-453">Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="ff59a-453">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="ff59a-454">Grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="ff59a-454">Connection Groups</span></span>**

[<span data-ttu-id="ff59a-455">Implementación de grupos de conexión en Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="ff59a-455">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="ff59a-456">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="ff59a-456">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="ff59a-457">Configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="ff59a-457">Dynamic Configuration</span></span>**

[<span data-ttu-id="ff59a-458">Acerca de la configuración dinámica de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ff59a-458">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)














