---
title: Referencia de línea de comandos de instalación de cliente
description: Referencia de línea de comandos de instalación de cliente
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826730"
---
# <span data-ttu-id="fad22-103">Referencia de línea de comandos de instalación de cliente</span><span class="sxs-lookup"><span data-stu-id="fad22-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="fad22-104">Para instalar MED-V desde la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="fad22-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="fad22-105">Desde la línea de comandos, ejecute el paquete MED-V. msi seguido de cualquiera de los parámetros opcionales que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fad22-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="fad22-106">El paquete MED-V. msi se llama *MED-V\_x.msi*, donde *x* es el número de versión.</span><span class="sxs-lookup"><span data-stu-id="fad22-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="fad22-107">Por ejemplo, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="fad22-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fad22-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fad22-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="fad22-109">Valor</span><span class="sxs-lookup"><span data-stu-id="fad22-109">Value</span></span></th>
<th align="left"><span data-ttu-id="fad22-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fad22-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-111">/Quiet</span><span class="sxs-lookup"><span data-stu-id="fad22-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fad22-112">Instalación silenciosa</span><span class="sxs-lookup"><span data-stu-id="fad22-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fad22-113">/log &lt; ruta completa del archivo de registro&gt;</span><span class="sxs-lookup"><span data-stu-id="fad22-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-114">La ruta de acceso completa del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="fad22-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="fad22-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-116">La ruta de acceso completa del directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="fad22-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fad22-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="fad22-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-118">La ruta de acceso completa a la carpeta de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad22-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="fad22-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fad22-120">1,0</span><span class="sxs-lookup"><span data-stu-id="fad22-120">1,0</span></span></strong></p>
<p><span data-ttu-id="fad22-121">Valor predeterminado: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="fad22-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fad22-122">Instala las herramientas de administración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fad22-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fad22-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="fad22-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fad22-124">1,0</span><span class="sxs-lookup"><span data-stu-id="fad22-124">1,0</span></span></strong></p>
<p><span data-ttu-id="fad22-125">Valor predeterminado: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="fad22-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fad22-126">Inicia automáticamente el cliente de MED-V cada vez que el usuario inicia sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="fad22-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="fad22-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-128">nombre de host o IP</span><span class="sxs-lookup"><span data-stu-id="fad22-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fad22-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="fad22-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-130">puerto</span><span class="sxs-lookup"><span data-stu-id="fad22-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="fad22-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fad22-132">1,0</span><span class="sxs-lookup"><span data-stu-id="fad22-132">1,0</span></span></strong></p>
<p><span data-ttu-id="fad22-133">para <strong> https </strong> o <strong> http</span><span class="sxs-lookup"><span data-stu-id="fad22-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fad22-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="fad22-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fad22-135">1,0</span><span class="sxs-lookup"><span data-stu-id="fad22-135">1,0</span></span></strong></p>
<p><span data-ttu-id="fad22-136">Valor predeterminado: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="fad22-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fad22-137">Inicia MED-V al finalizar la instalación de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fad22-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fad22-138">Nota</span><span class="sxs-lookup"><span data-stu-id="fad22-138">Note</span></span></strong><br/><p><span data-ttu-id="fad22-139">Se recomienda establecer START_MEDV = 0 en caso de que el sistema Instale MED-V.</span><span class="sxs-lookup"><span data-stu-id="fad22-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="fad22-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fad22-141">1,0</span><span class="sxs-lookup"><span data-stu-id="fad22-141">1,0</span></span></strong></p>
<p><span data-ttu-id="fad22-142">Valor predeterminado: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="fad22-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fad22-143">Crea un acceso directo en el escritorio, que inicia el cliente de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fad22-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fad22-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="fad22-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-145">RAM en MB</span><span class="sxs-lookup"><span data-stu-id="fad22-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fad22-146">Al instalar MED-V, comprueba si el equipo tiene la cantidad mínima de RAM especificada.</span><span class="sxs-lookup"><span data-stu-id="fad22-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="fad22-147">Si no es así, la instalación se cancela.</span><span class="sxs-lookup"><span data-stu-id="fad22-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fad22-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="fad22-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fad22-149">1,0</span><span class="sxs-lookup"><span data-stu-id="fad22-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fad22-150">Omite la validación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fad22-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











