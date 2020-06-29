---
title: Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control
description: Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812774"
---
# <span data-ttu-id="22ff5-103">Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="22ff5-103">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>


<span data-ttu-id="22ff5-104">En este tema se describen las **Opciones de cifrado de BitLocker** y los elementos del panel de control del **cifrado de unidad BitLocker** , y se explica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="22ff5-104">This topic describes the **BitLocker Encryption Options** and **BitLocker Drive Encryption** Control Panel items and explains the following:</span></span>

-   <span data-ttu-id="22ff5-105">Cómo se crean estos elementos</span><span class="sxs-lookup"><span data-stu-id="22ff5-105">How these items are created</span></span>

-   <span data-ttu-id="22ff5-106">Tareas que le permiten realizar</span><span class="sxs-lookup"><span data-stu-id="22ff5-106">Tasks they enable you to perform</span></span>

-   <span data-ttu-id="22ff5-107">**Administrar BitLocker** menú contextual "hacer clic con el botón secundario", cuando está visible frente a oculto y cómo configurarlo para que esté visible de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="22ff5-107">**Manage BitLocker** “right-click” shortcut menu, when it is visible versus hidden, and how to set it to be visible by default</span></span>

## <span data-ttu-id="22ff5-108">Opciones de cifrado de BitLocker y elementos del panel de control de cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="22ff5-108">BitLocker Encryption Options and BitLocker Drive Encryption Control Panel items</span></span>


<span data-ttu-id="22ff5-109">En la siguiente tabla se enumeran las tareas que puede realizar en cada elemento del panel de control y se describe cómo se crean estos elementos.</span><span class="sxs-lookup"><span data-stu-id="22ff5-109">The following table lists the tasks you can perform from each Control Panel item and describes how these items are created.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="22ff5-110">Opciones de cifrado de BitLocker (MBAM)</span><span class="sxs-lookup"><span data-stu-id="22ff5-110">BitLocker Encryption Options (MBAM)</span></span></th>
<th align="left"><span data-ttu-id="22ff5-111">Cifrado de unidad BitLocker (Windows)</span><span class="sxs-lookup"><span data-stu-id="22ff5-111">BitLocker Drive Encryption (Windows)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22ff5-112">Tareas que puede realizar</span><span class="sxs-lookup"><span data-stu-id="22ff5-112">Tasks you can do</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22ff5-113">Cambiar el PIN o la contraseña</span><span class="sxs-lookup"><span data-stu-id="22ff5-113">Change your PIN or password</span></span></p></li>
<li><p><span data-ttu-id="22ff5-114">Comprobar el estado del cifrado de una unidad</span><span class="sxs-lookup"><span data-stu-id="22ff5-114">Check encryption status for a drive</span></span></p></li>
<li><p><span data-ttu-id="22ff5-115">Abrir la consola de administración de TPM</span><span class="sxs-lookup"><span data-stu-id="22ff5-115">Open the TPM Management console</span></span></p></li>
<li><p><span data-ttu-id="22ff5-116">Activar BitLocker</span><span class="sxs-lookup"><span data-stu-id="22ff5-116">Turn on BitLocker</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22ff5-117">Suspender la protección de una unidad</span><span class="sxs-lookup"><span data-stu-id="22ff5-117">Suspend protection for a drive</span></span></p></li>
<li><p><span data-ttu-id="22ff5-118">Realizar una copia de seguridad de la clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="22ff5-118">Back up your recovery key</span></span></p></li>
<li><p><span data-ttu-id="22ff5-119">Cambiar el PIN</span><span class="sxs-lookup"><span data-stu-id="22ff5-119">Change your PIN</span></span></p></li>
<li><p><span data-ttu-id="22ff5-120">Desactivar BitLocker en una unidad</span><span class="sxs-lookup"><span data-stu-id="22ff5-120">Turn off BitLocker for a drive</span></span></p></li>
<li><p><span data-ttu-id="22ff5-121">Activar BitLocker en una unidad</span><span class="sxs-lookup"><span data-stu-id="22ff5-121">Turn on BitLocker for a drive</span></span></p></li>
<li><p><span data-ttu-id="22ff5-122">Abrir la consola de administración de TPM</span><span class="sxs-lookup"><span data-stu-id="22ff5-122">Open the TPM Management console</span></span></p></li>
<li><p><span data-ttu-id="22ff5-123">Descifrar una unidad de disco (solo aparece si el cliente de MBAM no está instalado)</span><span class="sxs-lookup"><span data-stu-id="22ff5-123">Decrypt a drive (appears only if the MBAM Client is NOT installed)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22ff5-124">Cómo se crea el elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="22ff5-124">How the Control Panel item is created</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ff5-125">Creado en el panel de control al instalar el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="22ff5-125">Created in Control Panel when you install the MBAM Client.</span></span> <span data-ttu-id="22ff5-126">Este elemento no se puede ocultar.</span><span class="sxs-lookup"><span data-stu-id="22ff5-126">This item cannot be hidden.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="22ff5-127">Nota</span><span class="sxs-lookup"><span data-stu-id="22ff5-127">Note</span></span></strong><br/><p><span data-ttu-id="22ff5-128">Este elemento aparece además de, pero no reemplaza, el elemento predeterminado del panel de control del cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="22ff5-128">This item appears in addition to, but does not replace, the default BitLocker Drive Encryption Control Panel item.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="22ff5-129">Aparece de forma predeterminada en el panel de control como parte del sistema operativo Windows, pero puede ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="22ff5-129">Appears by default in Control Panel as part of the Windows operating system, but you can hide it.</span></span></p>
<p><span data-ttu-id="22ff5-130">Para ocultarlo, vea <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> ocultar el elemento de cifrado de unidad BitLocker predeterminado en el panel de control </a> .</span><span class="sxs-lookup"><span data-stu-id="22ff5-130">To hide it, see <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)">Hiding the Default BitLocker Drive Encryption Item in Control Panel</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a><span data-ttu-id="22ff5-131">Menú contextual "Administrar BitLocker"</span><span class="sxs-lookup"><span data-stu-id="22ff5-131">“Manage BitLocker” shortcut menu</span></span>


<span data-ttu-id="22ff5-132">En la siguiente tabla se describe cómo difiere el menú de acceso directo **Administrar BitLocker** en función de si el cliente MBAM está instalado.</span><span class="sxs-lookup"><span data-stu-id="22ff5-132">The following table describes how the **Manage BitLocker** shortcut menu differs depending on whether the MBAM Client is installed.</span></span> <span data-ttu-id="22ff5-133">El término "menú contextual" se refiere a las opciones que aparecen al hacer clic con el botón secundario en una unidad en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="22ff5-133">The term “shortcut menu” refers to options that appear when you right-click a drive in Windows Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="22ff5-134">Cuando está instalado MBAM cliente</span><span class="sxs-lookup"><span data-stu-id="22ff5-134">When MBAM Client is installed</span></span></th>
<th align="left"><span data-ttu-id="22ff5-135">Cuando el cliente de MBAM no está instalado</span><span class="sxs-lookup"><span data-stu-id="22ff5-135">When MBAM Client is not installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22ff5-136">Visibilidad del menú contextual</span><span class="sxs-lookup"><span data-stu-id="22ff5-136">Visibility of shortcut menu</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ff5-137">La opción Administrar BitLocker está oculta.</span><span class="sxs-lookup"><span data-stu-id="22ff5-137">The Manage BitLocker option is hidden.</span></span></p>
<p><span data-ttu-id="22ff5-138">Para que la opción Administrar BitLocker esté visible en el menú contextual, que muestra la opción para descifrar una unidad, elimine la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="22ff5-138">To make the Manage BitLocker option visible on the shortcut menu, which displays the option to decrypt a drive, delete the following registry key:</span></span></p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p><span data-ttu-id="22ff5-139">La opción Administrar BitLocker aparece en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="22ff5-139">The Manage BitLocker option appears on the shortcut menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22ff5-140">Lo que pueden hacer los usuarios</span><span class="sxs-lookup"><span data-stu-id="22ff5-140">What users can do</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ff5-141">Con el acceso directo oculto, los usuarios pueden abrir el elemento del panel de control del cifrado de unidad BitLocker, pero la opción para descifrar una unidad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="22ff5-141">With the shortcut hidden, users can open the BitLocker Drive Encryption Control Panel item, but the option to decrypt a drive is not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="22ff5-142">Con el acceso directo visible, al seleccionar la <strong> opción Administrar BitLocker </strong> se abre el elemento panel de control del cifrado de unidad BitLocker, que muestra la opción de descifrar una unidad.</span><span class="sxs-lookup"><span data-stu-id="22ff5-142">With the shortcut visible, selecting the <strong>Manage BitLocker</strong> option opens the BitLocker Drive Encryption Control Panel item, which displays the option to decrypt a drive.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="22ff5-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22ff5-143">Related topics</span></span>


[<span data-ttu-id="22ff5-144">Administración de funciones de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22ff5-144">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)



## <span data-ttu-id="22ff5-145">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="22ff5-145">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="22ff5-146">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="22ff5-146">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="22ff5-147">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="22ff5-147">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





