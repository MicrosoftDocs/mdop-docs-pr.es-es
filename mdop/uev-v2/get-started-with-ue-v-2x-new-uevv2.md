---
title: Introducción a UE-V 2.x
description: Introducción a UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823290"
---
# <span data-ttu-id="28da6-103">Introducción a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="28da6-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="28da6-104">Siga los pasos que se indican en esta guía para implementar rápidamente la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 o 2,1 en un entorno de prueba pequeño.</span><span class="sxs-lookup"><span data-stu-id="28da6-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="28da6-105">Esto le ayuda a determinar si UE-V es la solución adecuada para administrar la configuración de usuario en varios dispositivos de su empresa.</span><span class="sxs-lookup"><span data-stu-id="28da6-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="28da6-106">**Nota:**  La información de esta sección se repite con más detalle en el resto de la documentación.</span><span class="sxs-lookup"><span data-stu-id="28da6-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="28da6-107">Por lo tanto, si ya sabe que UE-V 2 es la solución adecuada y no necesita evaluarla, puede ir directamente a [preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="28da6-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="28da6-108">La instalación estándar de UE-V sincroniza la configuración predeterminada de Microsoft Windows y Office, así como la mayoría de las opciones de la aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="28da6-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="28da6-109">Asegúrese de que su entorno de prueba incluya dos o más equipos de usuario que compartan el acceso a la red y que va a evaluar UE-V en poco tiempo.</span><span class="sxs-lookup"><span data-stu-id="28da6-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="28da6-110">[Paso 1: confirmar los requisitos previos](#step1): Asegúrese de que su entorno puede ejecutar UE-V, incluyendo detalles sobre las configuraciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="28da6-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="28da6-111">[Paso 2: implementar la ubicación de almacenamiento de configuración de UE-V 2](#step2): todas las implementaciones de UE-v requieren una ubicación para los paquetes de configuración que contienen los valores de configuración sincronizados.</span><span class="sxs-lookup"><span data-stu-id="28da6-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="28da6-112">[Paso 3: implementar el agente de UE-v 2](#step3): para sincronizar la configuración con UE-v, los dispositivos deben tener el agente UE-v instalado y en ejecución.</span><span class="sxs-lookup"><span data-stu-id="28da6-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="28da6-113">[Paso 4: probar la implementación de evaluación de UE-v 2](#step4): ejecute algunas pruebas en dos equipos que tengan instalado UE-v Agent y vea el funcionamiento de UE-v.</span><span class="sxs-lookup"><span data-stu-id="28da6-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="28da6-114">¡ Así está!</span><span class="sxs-lookup"><span data-stu-id="28da6-114">That’s it!</span></span> <span data-ttu-id="28da6-115">Una vez que hayas seguido los pasos, podrás evaluar cómo UE-V puede funcionar en tu empresa.</span><span class="sxs-lookup"><span data-stu-id="28da6-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="28da6-116">**Evaluación adicional:** También puede realizar pasos adicionales para configurar algunas aplicaciones de línea de negocio y de terceros para sincronizar su configuración mediante UE-V, tal como se detalla en [deploy UE-v 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="28da6-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="28da6-117">Paso 1: confirmar los requisitos previos</span><span class="sxs-lookup"><span data-stu-id="28da6-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="28da6-118">Antes de continuar, asegúrese de que su entorno incluye los siguientes requisitos para la ejecución de UE-V.</span><span class="sxs-lookup"><span data-stu-id="28da6-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="28da6-119">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="28da6-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="28da6-120">Edición</span><span class="sxs-lookup"><span data-stu-id="28da6-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="28da6-121">Service Pack</span><span class="sxs-lookup"><span data-stu-id="28da6-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="28da6-122">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="28da6-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="28da6-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="28da6-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="28da6-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="28da6-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28da6-125">7</span><span class="sxs-lookup"><span data-stu-id="28da6-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-126">Ultimate, Enterprise o Professional Edition</span><span class="sxs-lookup"><span data-stu-id="28da6-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-127">SP1</span><span class="sxs-lookup"><span data-stu-id="28da6-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-128">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="28da6-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-129">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-130">.NET Framework 4 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28da6-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="28da6-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-132">Standard, Enterprise, Datacenter o Web Server</span><span class="sxs-lookup"><span data-stu-id="28da6-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-133">SP1</span><span class="sxs-lookup"><span data-stu-id="28da6-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="28da6-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-135">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-136">.NET Framework 4 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28da6-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="28da6-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-138">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="28da6-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="28da6-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-140">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="28da6-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-141">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-142">4,5 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="28da6-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28da6-143">Windows Server 2012 o Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="28da6-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-144">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="28da6-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-145">Ninguno</span><span class="sxs-lookup"><span data-stu-id="28da6-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-146">64 bits</span><span class="sxs-lookup"><span data-stu-id="28da6-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-147">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-148">4,5 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="28da6-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="28da6-149">Windows 10, pre-1607 Verison</span><span class="sxs-lookup"><span data-stu-id="28da6-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-150">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="28da6-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="28da6-151">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="28da6-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-152">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-153">4,5 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="28da6-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="28da6-154">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="28da6-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-155">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="28da6-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-156">Ninguno</span><span class="sxs-lookup"><span data-stu-id="28da6-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="28da6-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-158">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="28da6-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="28da6-159">4,5 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="28da6-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="28da6-160">**Nota:** A partir de Windows 10, versión 1607, UE-V está incluida en [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) y ya no forma parte del paquete de optimización de escritorio de Microsoft</span><span class="sxs-lookup"><span data-stu-id="28da6-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="28da6-161">También...</span><span class="sxs-lookup"><span data-stu-id="28da6-161">Also…</span></span>

-   <span data-ttu-id="28da6-162">**Licencia de MDOP:** Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="28da6-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="28da6-163">Los clientes empresariales pueden obtener MDOP con Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="28da6-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="28da6-164">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte ¿Cómo puedo obtener MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="28da6-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="28da6-165">**Credenciales administrativas** de cualquier equipo en el que vaya a instalarlo</span><span class="sxs-lookup"><span data-stu-id="28da6-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="28da6-166">Paso 2: implementar la ubicación de almacenamiento de configuración de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="28da6-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="28da6-167">Tendrá que implementar una ubicación de almacenamiento de configuración, un recurso compartido de red estándar en el que se almacena la configuración de usuario en un archivo de paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="28da6-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="28da6-168">Al crear el recurso de almacenamiento de configuración, debe limitar el acceso a los usuarios que lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="28da6-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="28da6-169">[Implementar una ubicación de almacenamiento de configuración](https://technet.microsoft.com/library/dn458891.aspx#ssl) proporciona información más detallada.</span><span class="sxs-lookup"><span data-stu-id="28da6-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="28da6-170">Crear un recurso compartido de red</span><span class="sxs-lookup"><span data-stu-id="28da6-170">Create a network share</span></span>**

1.  <span data-ttu-id="28da6-171">Cree un nuevo grupo de seguridad y agréguele a los usuarios de UE-V.</span><span class="sxs-lookup"><span data-stu-id="28da6-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="28da6-172">Cree una nueva carpeta en el equipo centralizado que almacena los paquetes de configuración de UE-V y, a continuación, conceda a los usuarios de UE-V acceso con permisos de grupo a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="28da6-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="28da6-173">El administrador que admita UE-V debe tener permisos para esta carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="28da6-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="28da6-174">Asigne permisos de usuarios de UE-V para crear un directorio cuando se conecten.</span><span class="sxs-lookup"><span data-stu-id="28da6-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="28da6-175">Conceda permiso total a todos los subdirectorios de ese directorio, pero no bloquee el acceso a nada anterior.</span><span class="sxs-lookup"><span data-stu-id="28da6-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="28da6-176">Establezca los siguientes permisos de bloque de mensajes de servidor (SMB) de nivel de recurso compartido para la carpeta de ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="28da6-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="28da6-177">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="28da6-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="28da6-178">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="28da6-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="28da6-179">Todos</span><span class="sxs-lookup"><span data-stu-id="28da6-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="28da6-180">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="28da6-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="28da6-181">Grupo de seguridad de los usuarios de UE-V</span><span class="sxs-lookup"><span data-stu-id="28da6-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="28da6-182">Control total</span><span class="sxs-lookup"><span data-stu-id="28da6-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="28da6-183">Establezca los siguientes permisos del sistema de archivos NTFS en la carpeta de ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="28da6-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="28da6-184">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="28da6-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="28da6-185">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="28da6-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="28da6-186">Carpeta</span><span class="sxs-lookup"><span data-stu-id="28da6-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="28da6-187">Creador/propietario</span><span class="sxs-lookup"><span data-stu-id="28da6-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="28da6-188">Control total</span><span class="sxs-lookup"><span data-stu-id="28da6-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="28da6-189">Solo subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="28da6-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="28da6-190">Grupo de seguridad de los usuarios de UE-V</span><span class="sxs-lookup"><span data-stu-id="28da6-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="28da6-191">Listar carpeta/leer datos, crear carpetas/anexar datos</span><span class="sxs-lookup"><span data-stu-id="28da6-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="28da6-192">Solo esta carpeta</span><span class="sxs-lookup"><span data-stu-id="28da6-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="28da6-193">Nota de seguridad:</span><span class="sxs-lookup"><span data-stu-id="28da6-193">Security Note:</span></span>**

<span data-ttu-id="28da6-194">Si crea el recurso de almacenamiento de configuración en un equipo que ejecuta un sistema operativo Windows Server, configure UE-V para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="28da6-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="28da6-195">Para habilitar esta seguridad adicional, especifique esta configuración en el editor del registro de Windows Server:</span><span class="sxs-lookup"><span data-stu-id="28da6-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="28da6-196">Agregue una clave del registro **reg \ _DWORD** denominada **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="28da6-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="28da6-197">Establezca el valor de la clave del registro en *1*.</span><span class="sxs-lookup"><span data-stu-id="28da6-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="28da6-198">Paso 3: implementar el agente de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="28da6-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="28da6-199">El agente UE-V sincroniza la configuración de las aplicaciones y de Windows entre los equipos y los dispositivos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="28da6-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="28da6-200">Para fines de evaluación, instale el agente en al menos dos equipos del entorno de prueba que pertenezcan al mismo usuario.</span><span class="sxs-lookup"><span data-stu-id="28da6-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="28da6-201">Ejecute el archivo AgentSetup.exe desde la línea de comandos para instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="28da6-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="28da6-202">Se instala en sistemas operativos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="28da6-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="28da6-203">Debe especificar el parámetro de la línea de comandos SettingsStoragePath como el recurso compartido de red del paso 2.</span><span class="sxs-lookup"><span data-stu-id="28da6-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="28da6-204">[Implementar un agente de UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) proporciona información más detallada.</span><span class="sxs-lookup"><span data-stu-id="28da6-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="28da6-205">Paso 4: probar la implementación de la evaluación de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="28da6-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="28da6-206">Ahora puede ejecutar algunas pruebas en la implementación de evaluación de UE-V para ver cómo funciona UE-V.</span><span class="sxs-lookup"><span data-stu-id="28da6-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="28da6-207">En el primer equipo (equipo A), realice uno o varios de estos cambios:</span><span class="sxs-lookup"><span data-stu-id="28da6-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="28da6-208">Abra el escritorio de Windows y mueva la barra de tareas a otra ubicación en la ventana.</span><span class="sxs-lookup"><span data-stu-id="28da6-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="28da6-209">Cambie las fuentes predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="28da6-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="28da6-210">Abra Calculator y establezca el valor en **científico**.</span><span class="sxs-lookup"><span data-stu-id="28da6-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="28da6-211">Cambie el comportamiento de cualquier aplicación de Windows, como se detalla en [administrar las plantillas de ubicación de configuración de UE-V 2. x con Windows PowerShell y WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="28da6-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="28da6-212">Deshabilitar la sincronización y los perfiles de itinerancia de configuración de la cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28da6-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="28da6-213">Cierre la sesión en el equipo A. la configuración se guarda en un paquete de configuración de UE-V cuando los usuarios bloquean, cierran sesión, salen de una aplicación o cuando se ejecuta el proveedor de sincronización (cada 30 minutos de forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="28da6-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="28da6-214">Inicie sesión en el segundo equipo (el equipo B) como el mismo usuario que el equipo A.</span><span class="sxs-lookup"><span data-stu-id="28da6-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="28da6-215">Abra el escritorio de Windows y compruebe que la ubicación de la barra de tareas coincide con la del equipo A. Compruebe que las fuentes predeterminadas coinciden y que esa calculadora se establece en **científica**.</span><span class="sxs-lookup"><span data-stu-id="28da6-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="28da6-216">Además, verifica el cambio que realizaste en cualquier aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="28da6-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="28da6-217">Puede cambiar la configuración del equipo B a la configuración del equipo original.</span><span class="sxs-lookup"><span data-stu-id="28da6-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="28da6-218">Cierre la sesión con el equipo B e inicie sesión en el equipo a para comprobar los cambios.</span><span class="sxs-lookup"><span data-stu-id="28da6-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="28da6-219">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="28da6-219">Other resources for this product</span></span>


-   [<span data-ttu-id="28da6-220">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="28da6-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="28da6-221">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="28da6-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="28da6-222">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="28da6-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="28da6-223">Solución de problemas de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="28da6-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="28da6-224">Referencia técnica de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="28da6-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





