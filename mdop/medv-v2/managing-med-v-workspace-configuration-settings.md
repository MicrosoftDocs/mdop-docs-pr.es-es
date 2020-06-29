---
title: Administrar opciones de configuración de área de trabajo de MED-V
description: Administrar opciones de configuración de área de trabajo de MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826160"
---
# <span data-ttu-id="18fa4-103">Administrar opciones de configuración de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="18fa4-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="18fa4-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 almacena su configuración de configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="18fa4-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="18fa4-105">La información que incluimos aquí sobre el registro puede ayudarte a administrar mejor tus servicios de MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="18fa4-106">MED-V usa la siguiente ruta de búsqueda al buscar los valores de configuración resultantes:</span><span class="sxs-lookup"><span data-stu-id="18fa4-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="18fa4-107">MED-V busca primero en la Directiva de equipo.</span><span class="sxs-lookup"><span data-stu-id="18fa4-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="18fa4-108">Si no se encuentra el valor, MED-V busca en la Directiva de usuario.</span><span class="sxs-lookup"><span data-stu-id="18fa4-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="18fa4-109">Si no se encuentra el valor, MED-V busca en la sección HKEY \ _LOCAL \ _MACHINE \\System.</span><span class="sxs-lookup"><span data-stu-id="18fa4-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="18fa4-110">Si no se encuentra el valor, MED-V busca en la sección HKEY \ _CURRENT USER del registro.</span><span class="sxs-lookup"><span data-stu-id="18fa4-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="18fa4-111">Si aún no se encuentra el valor, MED-V usa el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="18fa4-112">Una práctica recomendada general es establecer el valor en el subárbol HKEY \ _LOCAL \ _MACHINE \\System o en la Directiva de equipo.</span><span class="sxs-lookup"><span data-stu-id="18fa4-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="18fa4-113">Pero si desea que el usuario final pueda configurar una configuración determinada, debe dejarla.</span><span class="sxs-lookup"><span data-stu-id="18fa4-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="18fa4-114">Nota</span><span class="sxs-lookup"><span data-stu-id="18fa4-114">Note</span></span>**  
<span data-ttu-id="18fa4-115">Antes de implementar sus áreas de trabajo de MED-V, puede usar un editor de scripts para cambiar el script de Windows PowerShell (archivo. PS1) que ha creado el paquete de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="18fa4-116">Para obtener más información, vea [Configuración avanzada mediante Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="18fa4-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="18fa4-117">Después de implementar sus áreas de trabajo de MED-V, puede cambiar determinadas opciones de configuración de MED-V modificando las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="18fa4-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="18fa4-118">En esta sección se enumeran todas las claves del registro MED-V configurables y se explican sus usos.</span><span class="sxs-lookup"><span data-stu-id="18fa4-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="18fa4-119">Clave de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="18fa4-119">Diagnostics Key</span></span>


<span data-ttu-id="18fa4-120">En la tabla siguiente se proporciona información acerca de los valores del registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="18fa4-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18fa4-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="18fa4-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="18fa4-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="18fa4-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="18fa4-123">Datos/valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="18fa4-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="18fa4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="18fa4-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="18fa4-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-127">Valor predeterminado = 3</span><span class="sxs-lookup"><span data-stu-id="18fa4-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-128">El tipo de información que se registra en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="18fa4-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="18fa4-129">Entre los niveles se incluyen los siguientes: 0 (ninguno), 1 (error), 2 (ADVERTENCIA), 3 (información), 4 (depurar).</span><span class="sxs-lookup"><span data-stu-id="18fa4-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="18fa4-130">Tecla FTS</span><span class="sxs-lookup"><span data-stu-id="18fa4-130">Fts Key</span></span>


<span data-ttu-id="18fa4-131">En la tabla siguiente se proporciona información acerca de los valores del registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.</span><span class="sxs-lookup"><span data-stu-id="18fa4-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18fa4-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="18fa4-132">Name</span></span></th>
<th align="left"><span data-ttu-id="18fa4-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="18fa4-133">Type</span></span></th>
<th align="left"><span data-ttu-id="18fa4-134">Datos/valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="18fa4-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="18fa4-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="18fa4-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-138">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-139">Configura la primera vez que el programa de instalación agrega automáticamente el usuario final al grupo&#39;s de administrador.</span><span class="sxs-lookup"><span data-stu-id="18fa4-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="18fa4-140">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-141">0 = falso: la configuración de la primera vez no agrega automáticamente el usuario final al grupo&#39;s del administrador.</span><span class="sxs-lookup"><span data-stu-id="18fa4-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-142">1 = verdadero: el programa de instalación agrega automáticamente el usuario final al grupo&#39;s de administrador.</span><span class="sxs-lookup"><span data-stu-id="18fa4-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="18fa4-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-144">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-145">MEDV\*</span><span class="sxs-lookup"><span data-stu-id="18fa4-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-146">La máscara de nombre de equipo que se usa para crear la máquina virtual invitada&#39;el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="18fa4-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-147">La máscara puede contener una etiqueta% username% para insertar el nombre de usuario como parte del nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="18fa4-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="18fa4-148">Del mismo modo, la etiqueta% hostname% inserta el nombre del equipo host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="18fa4-149">Cada &quot; # &quot; carácter de la máscara se reemplaza por un dígito aleatorio.</span><span class="sxs-lookup"><span data-stu-id="18fa4-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="18fa4-150">Un carácter de asterisco (\*) al final de la máscara se reemplaza por caracteres alfanuméricos aleatorios.</span><span class="sxs-lookup"><span data-stu-id="18fa4-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="18fa4-151">Se puede capturar un número específico de caracteres de% hostname% y% username% con corchetes.</span><span class="sxs-lookup"><span data-stu-id="18fa4-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="18fa4-152">Por ejemplo, &quot; % username% [3] &quot; usaría los primeros tres caracteres del nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="18fa4-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-155">Valor predeterminado = 90</span><span class="sxs-lookup"><span data-stu-id="18fa4-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-156">El valor de tiempo de espera, en segundos, la primera vez que la configuración intenta eliminar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="18fa4-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="18fa4-157">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-160">Valor predeterminado = 120</span><span class="sxs-lookup"><span data-stu-id="18fa4-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-161">El valor de tiempo de espera, en segundos, la primera vez que la instalación intenta desasociar el disquete virtual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="18fa4-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="18fa4-162">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="18fa4-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-164">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-165">Dirección URL personalizable que se vincula a la página web interna y se muestra en los mensajes de diálogo de configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-168">Valor predeterminado = 900</span><span class="sxs-lookup"><span data-stu-id="18fa4-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-169">El valor de tiempo de espera, en segundos, que la primera vez de la configuración espera el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="18fa4-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="18fa4-170">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="18fa4-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-173">El mensaje se encuentra en el archivo de recursos</span><span class="sxs-lookup"><span data-stu-id="18fa4-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-174">Mensaje personalizable que se muestra al usuario final cuando no se puede completar la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="18fa4-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-177">Valor predeterminado = 3</span><span class="sxs-lookup"><span data-stu-id="18fa4-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-178">Número máximo de veces que MED-V intenta proporcionar derechos de grupo de usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="18fa4-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="18fa4-179">Si se supera el valor de reintentos especificado sin que sea posible conceder correctamente a un usuario final los derechos de grupo es probable que el error de preparación de la máquina virtual se someta al valor MaxRetryCount.</span><span class="sxs-lookup"><span data-stu-id="18fa4-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="18fa4-180">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-183">Valor predeterminado = 300</span><span class="sxs-lookup"><span data-stu-id="18fa4-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-184">El valor de tiempo de espera, en segundos, al otorgar derechos de grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="18fa4-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="18fa4-185">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="18fa4-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-188">Una lista de las rutas de los archivos de registro que MED-V recopila durante la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="18fa4-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-191">Valor predeterminado = 120</span><span class="sxs-lookup"><span data-stu-id="18fa4-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-192">El número máximo de horas que el usuario final puede posponer la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="18fa4-193">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="18fa4-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-196">Valor predeterminado = 3</span><span class="sxs-lookup"><span data-stu-id="18fa4-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-197">El número máximo de veces que MED-V intenta preparar una máquina virtual si cada intento finaliza en un error que no es de software.</span><span class="sxs-lookup"><span data-stu-id="18fa4-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="18fa4-198">Cuando se produce un error en la preparación de la máquina virtual y se supera el número de reintentos de configuración por primera vez, MED-V informa al usuario final sobre el error y no le da la opción de reintentar.</span><span class="sxs-lookup"><span data-stu-id="18fa4-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="18fa4-199">El recuento se vuelve a establecer cada vez que se inicia MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="18fa4-200">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-201">Modo</span><span class="sxs-lookup"><span data-stu-id="18fa4-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-202">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-203">Valor predeterminado = desatendida</span><span class="sxs-lookup"><span data-stu-id="18fa4-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-204">Configura la manera en que la configuración interactúa por primera vez con el usuario.</span><span class="sxs-lookup"><span data-stu-id="18fa4-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="18fa4-205">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="18fa4-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-206">Asistida.</span><span class="sxs-lookup"><span data-stu-id="18fa4-206">Attended.</span></span></strong> <span data-ttu-id="18fa4-207">El usuario final debe escribir la información durante la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="18fa4-208">Nota</span><span class="sxs-lookup"><span data-stu-id="18fa4-208">Note</span></span></strong><br/><p><span data-ttu-id="18fa4-209">Si creó el archivo Sysprep. inf para que la instalación mínima requiera que se complete la entrada del usuario, debe seleccionar el <strong> </strong> modo atendido o los problemas pueden ocurrir durante la primera configuración.</span><span class="sxs-lookup"><span data-stu-id="18fa4-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-210">Desatendida </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-210">Unattended</strong>.</span></span> <span data-ttu-id="18fa4-211">La máquina virtual no se muestra al usuario final durante la configuración de la primera vez, pero se solicita al usuario final antes de que se inicie la instalación por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-212">Silencioso </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-212">Silent</strong>.</span></span> <span data-ttu-id="18fa4-213">La máquina virtual no se muestra al usuario final en ningún momento durante la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="18fa4-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-216">Valor predeterminado = 15</span><span class="sxs-lookup"><span data-stu-id="18fa4-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-217">El valor de tiempo de espera, en minutos, que debe completarse la primera configuración en el modo interactivo de configuración por primera vez al volver a intentar la instalación.</span><span class="sxs-lookup"><span data-stu-id="18fa4-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="18fa4-218">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-221">Valor predeterminado = 45</span><span class="sxs-lookup"><span data-stu-id="18fa4-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-222">El valor de tiempo de espera, en minutos, que la primera vez debe completarse la configuración en el modo interactivo de primera configuración.</span><span class="sxs-lookup"><span data-stu-id="18fa4-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="18fa4-223">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="18fa4-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-225">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-226">La fecha y hora, en formato de fecha UTC, que se puede posponer la primera configuración.</span><span class="sxs-lookup"><span data-stu-id="18fa4-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="18fa4-227">Escriba en el formato &quot; AAAA-MM-DD HH: mm &quot; con las horas especificadas usando el estándar de reloj de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="18fa4-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="18fa4-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-230">El mensaje se encuentra en el archivo de recursos</span><span class="sxs-lookup"><span data-stu-id="18fa4-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-231">Mensaje personalizable que se muestra al usuario final cuando la primera vez la configuración debe volver a intentar la instalación.</span><span class="sxs-lookup"><span data-stu-id="18fa4-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-234">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-235">Configura si la entrada ComputerName de la sección [UserData] del archivo Sysprep. inf en el invitado debe actualizarse de acuerdo con el ComputerNameMask especificado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="18fa4-236">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-237">0 = falso: la entrada ComputerName del archivo Sysprep. inf no se actualiza según el ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="18fa4-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-238">1 = verdadero: la entrada ComputerName en el archivo Sysprep. inf se actualiza según el ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="18fa4-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-241">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-242">Configura si la configuración de JoinDomain de la sección [Identification] del archivo Sysprep. inf del invitado debe actualizarse para que coincida con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="18fa4-243">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-244">0 = falso: la configuración de JoinDomain del archivo Sysprep. inf no se actualiza para coincidir con la del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-245">1 = verdadero: la configuración de JoinDomain del archivo Sysprep. inf se actualiza para coincidir con la del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-248">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-249">Configura si la configuración MachineObjectOU de la sección [Identification] del archivo Sysprep. inf en el invitado se actualiza para coincidir con el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="18fa4-250">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-251">0 = falso: el valor de MachineObjectOU en el archivo Sysprep. inf no se actualiza para coincidir con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-252">1 = true: el valor MachineObjectOU en el archivo Sysprep. inf se actualiza para coincidir con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-253">SetRegionalSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-255">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-256">Configura si la configuración de la sección [RegionalSettings] del archivo Sysprep. inf en el invitado se actualiza para coincidir con el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="18fa4-257">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="18fa4-258">Nota</span><span class="sxs-lookup"><span data-stu-id="18fa4-258">Note</span></span></strong><br/><p><span data-ttu-id="18fa4-259">De forma predeterminada, la configuración de TimeZone en el invitado siempre se sincroniza con la configuración de la zona horaria en el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-260">0 = falso: la configuración de la sección [RegionalSettings] del archivo Sysprep. inf del invitado no se actualiza para coincidir con el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-261">1 = verdadero: la configuración de la sección [RegionalSettings] del archivo Sysprep. inf en el invitado se actualiza para coincidir con el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-264">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-265">Configura si la configuración FullName y OrgName de la sección [UserData] del archivo Sysprep. inf en el invitado se actualiza para coincidir con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="18fa4-266">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-267">0 = falso: la configuración FullName y OrgName del archivo Sysprep. inf no se actualiza para coincidir con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-268">1 = true: la configuración FullName y OrgName en el archivo Sysprep. inf se actualiza para coincidir con la configuración del host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="18fa4-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-271">El mensaje se encuentra en el archivo de recursos</span><span class="sxs-lookup"><span data-stu-id="18fa4-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-272">Mensaje personalizable que se muestra al usuario final cuando está listo para iniciar la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="18fa4-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-275">Valor predeterminado = 30</span><span class="sxs-lookup"><span data-stu-id="18fa4-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-276">El valor de tiempo de espera, en segundos, que la primera vez de la configuración espera una respuesta de la máquina virtual para una operación de cancelación.</span><span class="sxs-lookup"><span data-stu-id="18fa4-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="18fa4-277">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-280">Valor predeterminado = 60</span><span class="sxs-lookup"><span data-stu-id="18fa4-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-281">El valor de tiempo de espera, en segundos, que la primera vez la configuración espera a que se cierre la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="18fa4-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="18fa4-282">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-285">Valor predeterminado = 600</span><span class="sxs-lookup"><span data-stu-id="18fa4-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-286">El tiempo, en segundos, antes de que se agote el tiempo de espera de la actualización del software de agente invitado de MED-V. Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="18fa4-287">Tecla UserExperience</span><span class="sxs-lookup"><span data-stu-id="18fa4-287">UserExperience Key</span></span>


<span data-ttu-id="18fa4-288">En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience y la clave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.</span><span class="sxs-lookup"><span data-stu-id="18fa4-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18fa4-289">Nombre</span><span class="sxs-lookup"><span data-stu-id="18fa4-289">Name</span></span></th>
<th align="left"><span data-ttu-id="18fa4-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="18fa4-290">Type</span></span></th>
<th align="left"><span data-ttu-id="18fa4-291">Datos/valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="18fa4-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="18fa4-292">Descripción</span><span class="sxs-lookup"><span data-stu-id="18fa4-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-295">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-296">Configura si la publicación de la aplicación del invitado en el host está habilitada.</span><span class="sxs-lookup"><span data-stu-id="18fa4-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="18fa4-297">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-298">0 = falso: deshabilita la publicación de aplicaciones del invitado en el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-299">1 = true: habilita la publicación de aplicaciones desde el invitado al host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-302">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-303">Configura si el uso compartido del dispositivo de audio e/s entre el invitado y el host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="18fa4-304">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-305">0 = falso: deshabilita el uso compartido del dispositivo de e/s de audio entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-306">1 = true: permite compartir el dispositivo de audio e/s entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-309">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-310">Configura si el uso compartido del portapapeles entre el invitado y el host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="18fa4-311">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-312">0 = falso: deshabilita el uso compartido del portapapeles entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-313">1 = verdadero: permite compartir el portapapeles entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-316">Valor predeterminado = 300</span><span class="sxs-lookup"><span data-stu-id="18fa4-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-317">El tiempo, en segundos, antes de que el cuadro de diálogo iniciar por primera vez se agote el tiempo de espera. Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-318">HideVmTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-320">Valor predeterminado = 30</span><span class="sxs-lookup"><span data-stu-id="18fa4-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-321">El valor de tiempo de espera, en minutos, que la ventana del equipo virtual de pantalla completa está oculta para el usuario final durante un largo intento de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="18fa4-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-324">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-325">Configura si el invitado debe iniciarse cuando el usuario final inicia sesión en el escritorio o cuando se inicia la primera aplicación invitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="18fa4-326">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-327">0 = falso: el invitado se inicia cuando se inicia la primera aplicación invitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-328">1 = verdadero: el invitado se inicia cuando el usuario final inicia sesión en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="18fa4-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-331">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-332">Configura si el uso compartido de las impresoras entre el invitado y el host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="18fa4-333">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-334">0 = falso: deshabilita el uso compartido de impresoras entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-335">1 = true: permite el uso compartido de impresoras entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-338">Valor predeterminado = 1440</span><span class="sxs-lookup"><span data-stu-id="18fa4-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-339">El valor de tiempo de espera, en minutos, que la primera vez de la configuración espera un reinicio.</span><span class="sxs-lookup"><span data-stu-id="18fa4-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="18fa4-340">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="18fa4-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-343">Lista de direcciones URL especificada</span><span class="sxs-lookup"><span data-stu-id="18fa4-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-344">Especifica una lista de direcciones URL que el host debe redirigir al invitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-345">SmartCardLogonEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-347">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-348">Configura si las tarjetas inteligentes se pueden usar para autenticar usuarios en MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="18fa4-349">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-350">0 = falso: no permite que las tarjetas inteligentes autentiquen a los usuarios finales en MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-351">1 = verdadero: permite que las tarjetas inteligentes autentiquen a los usuarios finales en MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="18fa4-352">Importante</span><span class="sxs-lookup"><span data-stu-id="18fa4-352">Important</span></span></strong><br/><p><span data-ttu-id="18fa4-353">Si SmartCardLogonEnabled y CredentialCacheEnabled están habilitados, SmartCardLogonEnabled invalida CredentialCacheEnabled.</span><span class="sxs-lookup"><span data-stu-id="18fa4-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-356">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-357">Configura si el uso compartido de tarjetas inteligentes entre el invitado y el host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="18fa4-358">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-359">0 = falso: deshabilita el uso compartido de tarjetas inteligentes entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-360">1 = true: permite el uso compartido de tarjetas inteligentes entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-363">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-364">Configura si el uso compartido de dispositivos USB entre el invitado y el host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="18fa4-365">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-366">0 = falso: deshabilita el uso compartido de dispositivos USB entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-367">1 = true: permite el uso compartido de dispositivos USB entre el invitado y el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="18fa4-368">Clave de VM</span><span class="sxs-lookup"><span data-stu-id="18fa4-368">VM Key</span></span>


<span data-ttu-id="18fa4-369">En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM y la clave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="18fa4-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18fa4-370">Nombre</span><span class="sxs-lookup"><span data-stu-id="18fa4-370">Name</span></span></th>
<th align="left"><span data-ttu-id="18fa4-371">Tipo</span><span class="sxs-lookup"><span data-stu-id="18fa4-371">Type</span></span></th>
<th align="left"><span data-ttu-id="18fa4-372">Datos/valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="18fa4-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="18fa4-373">Descripción</span><span class="sxs-lookup"><span data-stu-id="18fa4-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-374">CloseAction</span><span class="sxs-lookup"><span data-stu-id="18fa4-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-375">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-376">Predeterminado = HIBERNAr</span><span class="sxs-lookup"><span data-stu-id="18fa4-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-377">La acción que realiza la máquina virtual después de que se cierre la última aplicación que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="18fa4-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="18fa4-378">Este valor se pasa por alto si el valor LogonStartEnabled está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="18fa4-379">Las opciones posibles son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="18fa4-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-380">HIBERNAr </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="18fa4-381">Esta opción libera todos los recursos físicos que usa la máquina virtual, como la memoria y la CPU, y guarda el estado de todas las aplicaciones y operaciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="18fa4-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-382">SHUTDOWN </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="18fa4-383">Esta opción cierra el sistema operativo invitado de manera segura y luego libera todos los recursos físicos que usa la máquina virtual, como la memoria y la CPU.</span><span class="sxs-lookup"><span data-stu-id="18fa4-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-384">DESACTIVAR </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="18fa4-385">Esta opción puede provocar pérdida de datos porque es lo mismo que desactivar el botón de encendido o extraer el cable de alimentación en un equipo físico.</span><span class="sxs-lookup"><span data-stu-id="18fa4-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="18fa4-386">Use esta opción solo si no puede usar una de las otras dos opciones.</span><span class="sxs-lookup"><span data-stu-id="18fa4-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="18fa4-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="18fa4-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-390">Una lista de los valores de memoria (MB) del invitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="18fa4-391">Este valor se usa para determinar cuánta RAM está disponible para el invitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="18fa4-392">En combinación con HostMemToGuestMem, se crea una tabla de búsqueda para determinar cuánta RAM se debe asignar en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="18fa4-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="18fa4-393">Los valores posibles pueden estar comprendidos entre 128 y 3712.</span><span class="sxs-lookup"><span data-stu-id="18fa4-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="18fa4-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-396">Valor predeterminado = 240</span><span class="sxs-lookup"><span data-stu-id="18fa4-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-397">Número de minutos que MED-V debe mantener al invitado activo para su actualización automática, a partir de la hora especificada en el valor GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="18fa4-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="18fa4-398">Intervalo = 0 a 1440.</span><span class="sxs-lookup"><span data-stu-id="18fa4-398">Range = 0 to 1440.</span></span> <span data-ttu-id="18fa4-399">Al establecer este valor en cero (0), se deshabilita la funcionalidad de corrección de invitados.</span><span class="sxs-lookup"><span data-stu-id="18fa4-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="18fa4-400">Para obtener más información sobre las revisiones de invitado para las actualizaciones automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Administración de actualizaciones automáticas para áreas de trabajo de MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="18fa4-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-402">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-403">Valor predeterminado = 00:00</span><span class="sxs-lookup"><span data-stu-id="18fa4-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-404">La hora y el minuto cada día en que MED-V debe reactivar al invitado para su actualización automática, mediante el estándar de reloj de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="18fa4-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="18fa4-405">Especificar la hora en el formato HH: MM</span><span class="sxs-lookup"><span data-stu-id="18fa4-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="18fa4-406">Para obtener más información sobre las revisiones de invitado para las actualizaciones automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Administración de actualizaciones automáticas para áreas de trabajo de MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="18fa4-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="18fa4-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-410">Una lista de los valores de memoria (MB) para el invitado, determinado por la RAM disponible en el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="18fa4-411">En combinación con GuestMemFromHostMem, se crea una tabla de búsqueda para determinar cuánta RAM se debe asignar en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="18fa4-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="18fa4-412">Los valores posibles pueden estar comprendidos entre 1024 y 16384.</span><span class="sxs-lookup"><span data-stu-id="18fa4-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-415">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-416">Configura si la memoria asignada al invitado se calcula a partir de la memoria presente en el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="18fa4-417">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-418">0 = falso: la memoria asignada al invitado no se calcula a partir de la memoria presente en el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-419">1 = true: la memoria asignada al invitado se calcula a partir de la memoria presente en el host.</span><span class="sxs-lookup"><span data-stu-id="18fa4-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-420">Memoria</span><span class="sxs-lookup"><span data-stu-id="18fa4-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-422">Valor predeterminado = 512</span><span class="sxs-lookup"><span data-stu-id="18fa4-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-423">La RAM (MB) que se debe asignar a la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="18fa4-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="18fa4-424">Esta configuración se pasa por alto si la configuración HostMemToGuestMemEnabled está habilitada.</span><span class="sxs-lookup"><span data-stu-id="18fa4-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="18fa4-425">Intervalo = 128 a 2048.</span><span class="sxs-lookup"><span data-stu-id="18fa4-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="18fa4-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-428">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="18fa4-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-429">Configura si varios usuarios comparten el mismo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="18fa4-430">0 = falso; 1 = true.</span><span class="sxs-lookup"><span data-stu-id="18fa4-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-431">0 = falso: varios usuarios no comparten el mismo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-432">1 = true: varios usuarios comparten el mismo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="18fa4-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18fa4-433">NetworkingMode</span><span class="sxs-lookup"><span data-stu-id="18fa4-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-434">SZ</span><span class="sxs-lookup"><span data-stu-id="18fa4-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-435">Predeterminado = NAT</span><span class="sxs-lookup"><span data-stu-id="18fa4-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-436">El tipo de conexión de red que se usa en el invitado.</span><span class="sxs-lookup"><span data-stu-id="18fa4-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="18fa4-437">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="18fa4-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-438">Con puente </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-438">Bridged</strong>.</span></span> <span data-ttu-id="18fa4-439">MED-V tiene su propia dirección de red, que normalmente se obtiene a través de DHCP.</span><span class="sxs-lookup"><span data-stu-id="18fa4-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="18fa4-440">NAT </strong> .</span><span class="sxs-lookup"><span data-stu-id="18fa4-440">NAT</strong>.</span></span> <span data-ttu-id="18fa4-441">MED-V usa la traducción de direcciones de red (NAT) para compartir el host&#39;s IP para el tráfico saliente.</span><span class="sxs-lookup"><span data-stu-id="18fa4-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="18fa4-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-444">Valor predeterminado = 600</span><span class="sxs-lookup"><span data-stu-id="18fa4-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-445">Un valor de tiempo de espera general, en segundos, que MED-V espera a que se complete una tarea, como reiniciar y apagar.</span><span class="sxs-lookup"><span data-stu-id="18fa4-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="18fa4-446">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="18fa4-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="18fa4-447">Configuración del registro de invitados</span><span class="sxs-lookup"><span data-stu-id="18fa4-447">Guest Registry Settings</span></span>


<span data-ttu-id="18fa4-448">En esta sección se enumeran las claves del registro de invitado de MED-V configurables y se explican sus usos.</span><span class="sxs-lookup"><span data-stu-id="18fa4-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="18fa4-449">2</span><span class="sxs-lookup"><span data-stu-id="18fa4-449">v2</span></span>

<span data-ttu-id="18fa4-450">En la tabla siguiente se proporciona información sobre el valor del registro invitado asociado a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.</span><span class="sxs-lookup"><span data-stu-id="18fa4-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18fa4-451">Nombre</span><span class="sxs-lookup"><span data-stu-id="18fa4-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="18fa4-452">Tipo</span><span class="sxs-lookup"><span data-stu-id="18fa4-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="18fa4-453">Datos/valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="18fa4-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="18fa4-454">Descripción</span><span class="sxs-lookup"><span data-stu-id="18fa4-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18fa4-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="18fa4-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="18fa4-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="18fa4-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-457">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="18fa4-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="18fa4-458">Configura la forma en que MED-V controla las claves BufferPolicyReads y GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="18fa4-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="18fa4-459">De forma predeterminada, MED-V establece estas claves de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="18fa4-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="18fa4-460">BufferPolicyReads = 1 y GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="18fa4-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="18fa4-461">Cree la clave EnableGPWorkarounds, si es necesario, y establezca la clave en cero si no quiere que MED-V cambie la configuración predeterminada de BufferPolicyReads y GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="18fa4-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="18fa4-462">Nota</span><span class="sxs-lookup"><span data-stu-id="18fa4-462">Note</span></span></strong><br/><p><span data-ttu-id="18fa4-463">Si el área de trabajo de MED-V se ejecuta en modo NAT, EnableGPWorkarounds afecta a las claves del registro BufferPolicyReads y GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="18fa4-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="18fa4-464">Si el área de trabajo de MED-V se ejecuta en modo puente, EnableGPWorkarounds solo afectará a la clave del registro BufferPolicyReads.</span><span class="sxs-lookup"><span data-stu-id="18fa4-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="18fa4-465">1 = verdadero: MED-V establece las claves BufferPolicyReads = 1 y GroupPolicyMinTransferRate = 0 (si se ejecuta en modo NAT) o simplemente BufferPolicyReads = 1 (si se ejecuta en modo BRIDGEd).</span><span class="sxs-lookup"><span data-stu-id="18fa4-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="18fa4-466">0 = falso: MED-V no realiza cambios en las claves BufferPolicyReads y GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="18fa4-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="18fa4-467">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18fa4-467">Related topics</span></span>


[<span data-ttu-id="18fa4-468">Administrar aplicaciones de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="18fa4-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="18fa4-469">Administrar la redirección de la dirección URL de MED-V</span><span class="sxs-lookup"><span data-stu-id="18fa4-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="18fa4-470">Administrar la configuración del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="18fa4-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









