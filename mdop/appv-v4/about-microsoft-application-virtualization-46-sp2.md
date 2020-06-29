---
title: Acerca de Microsoft Application Virtualization4.6SP2
description: Acerca de Microsoft Application Virtualization4.6SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820020"
---
# <span data-ttu-id="60db0-103">Acerca de Microsoft Application Virtualization4.6SP2</span><span class="sxs-lookup"><span data-stu-id="60db0-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="60db0-104">Microsoft Application Virtualization (App-V) 4.6 SP2 proporciona varias mejoras y nuevas características, que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="60db0-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="60db0-105">**PRECAUCIÓN**  En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="60db0-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="60db0-106">Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="60db0-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="60db0-107">Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro.</span><span class="sxs-lookup"><span data-stu-id="60db0-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="60db0-108">Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver.</span><span class="sxs-lookup"><span data-stu-id="60db0-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="60db0-109">Cambie el registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="60db0-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="60db0-110">Compatibilidad con Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60db0-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="60db0-111">App-V 4.6 SP2 agrega compatibilidad con servicios de escritorio remoto de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="60db0-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="60db0-112">Compatibilidad con la coexistencia con el cliente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="60db0-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="60db0-113">App-V 4.6 SP2 proporciona compatibilidad para la coexistencia con el cliente de Microsoft Application Virtualization 5,0.</span><span class="sxs-lookup"><span data-stu-id="60db0-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="60db0-114">Revise la documentación de App-V 5,0 para obtener instrucciones sobre cómo configurar el cliente de App-V 5,0 para la coexistencia con el cliente de App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="60db0-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="60db0-115">Para obtener más información sobre App-V 5,0, vea [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) en TechNet.</span><span class="sxs-lookup"><span data-stu-id="60db0-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="60db0-116">Posibilidad de virtualizar Adobe Reader X con el modo protegido</span><span class="sxs-lookup"><span data-stu-id="60db0-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="60db0-117">Puede virtualizar Adobe Reader X con la característica de modo protegido activada mediante los procedimientos siguientes.</span><span class="sxs-lookup"><span data-stu-id="60db0-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="60db0-118">Anteriormente, tenía que deshabilitar el modo protegido para virtualizar Adobe Reader X.</span><span class="sxs-lookup"><span data-stu-id="60db0-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="60db0-119">Antes de iniciar el secuenciador de App-V, cree el valor de registro siguiente en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span><span class="sxs-lookup"><span data-stu-id="60db0-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="60db0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="60db0-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="60db0-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="60db0-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="60db0-122">Datos</span><span class="sxs-lookup"><span data-stu-id="60db0-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="60db0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="60db0-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="60db0-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="60db0-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="60db0-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="60db0-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="60db0-126">uno</span><span class="sxs-lookup"><span data-stu-id="60db0-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="60db0-127">Establezca este valor en <strong> 1 para </strong> iniciar Adobe Reader X en modo protegido durante la fase de inicio.</span><span class="sxs-lookup"><span data-stu-id="60db0-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="60db0-128">**Nota:**  En un equipo que ejecute un sistema operativo de 64 bits, cree el valor del registro en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span><span class="sxs-lookup"><span data-stu-id="60db0-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="60db0-129">Para cada archivo OSD de su paquete de Adobe Reader X, agregue los siguientes elementos en el &lt; elemento Policies &gt; :</span><span class="sxs-lookup"><span data-stu-id="60db0-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="60db0-130">Nuevo parámetro de línea de comandos de secuenciador</span><span class="sxs-lookup"><span data-stu-id="60db0-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="60db0-131">Al crear un acelerador de paquetes (PA) a través de la GUI secuenciador, puede seleccionar un archivo RTF o TXT que proporcione instrucciones de empaquetado e implementación a los administradores que aplicarán el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="60db0-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="60db0-132">Esta funcionalidad ahora está disponible con la CLI SPRJ.</span><span class="sxs-lookup"><span data-stu-id="60db0-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="60db0-133">Especifique una ruta de acceso a un archivo RTF o TXT que proporcione instrucciones de empaquetado e implementación al crear un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="60db0-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="60db0-134">Los informes de errores de aplicaciones de Microsoft ya no necesitan instalarse</span><span class="sxs-lookup"><span data-stu-id="60db0-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="60db0-135">Al instalar el cliente de App-V 4.6 SP2 con setup.msi, ya no necesita instalar informes de errores de aplicaciones de Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="60db0-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="60db0-136">App-V 4.6 SP2 ahora usa informe de errores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60db0-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="60db0-137">Para obtener más información, vea [Cómo instalar el cliente de App-V con Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span><span class="sxs-lookup"><span data-stu-id="60db0-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="60db0-138">Comentarios de los clientes y Resumen de revisiones</span><span class="sxs-lookup"><span data-stu-id="60db0-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="60db0-139">App-V 4.6 SP2 incluye un resumen de las correcciones para resolver los problemas encontrados desde el lanzamiento de App-V 4,6 SP1.</span><span class="sxs-lookup"><span data-stu-id="60db0-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="60db0-140">App-V 4.6 SP2 contiene las últimas revisiones hasta el Hotfix 6 de Microsoft Application Virtualization 4,6 SP1.</span><span class="sxs-lookup"><span data-stu-id="60db0-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="60db0-141">En esta sección</span><span class="sxs-lookup"><span data-stu-id="60db0-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="60db0-142">Notas de la versión de App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="60db0-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="60db0-143">Proporciona la información más actualizada sobre problemas conocidos con App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="60db0-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





