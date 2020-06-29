---
title: Configurar UE-V con objetos de directiva de grupo
description: Configurar UE-V con objetos de directiva de grupo
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826700"
---
# <span data-ttu-id="ece28-103">Configurar UE-V con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="ece28-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="ece28-104">Algunas opciones de configuración de la Directiva de grupo de virtualización de Microsoft User Experience (UE-V) se pueden definir para equipos y otros pueden definirse para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ece28-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="ece28-105">La configuración de la Directiva de configuración de UE-V Agent se puede definir para equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="ece28-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="ece28-106">Para obtener información sobre cómo instalar archivos ADMX de la Directiva de grupo de UE-V, consulte [instalar las plantillas ADMX de la Directiva de grupo de UE-v](installing-the-ue-v-group-policy-admx-templates.md).</span><span class="sxs-lookup"><span data-stu-id="ece28-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="ece28-107">Puede configurar las siguientes opciones de directiva para UE-V:</span><span class="sxs-lookup"><span data-stu-id="ece28-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ece28-108">Nombre de configuración de Directiva</span><span class="sxs-lookup"><span data-stu-id="ece28-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ece28-109">Target</span><span class="sxs-lookup"><span data-stu-id="ece28-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ece28-110">Descripción de configuración de Directiva</span><span class="sxs-lookup"><span data-stu-id="ece28-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ece28-111">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="ece28-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ece28-112">Usar la virtualización de la experiencia del usuario (UE-V)</span><span class="sxs-lookup"><span data-stu-id="ece28-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-113">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-114">Esta configuración de directiva le permite habilitar o deshabilitar la virtualización de la experiencia del usuario (UE-V).</span><span class="sxs-lookup"><span data-stu-id="ece28-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-115">Habilitar o deshabilitar esta configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="ece28-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ece28-116">Configuración ruta de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="ece28-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-117">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-118">Esta configuración de Directiva define dónde se almacenará la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ece28-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-119">Proporcionar una ruta de acceso UNC (Convención de nomenclatura universal) y variables como \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="ece28-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ece28-120">Ruta del catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="ece28-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-121">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="ece28-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-122">Esta configuración de Directiva define dónde se almacenan las plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="ece28-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="ece28-123">Esta configuración de directiva también configura si el catálogo se usará para reemplazar las plantillas de Microsoft predeterminadas que se instalan con el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="ece28-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-124">Proporcione una ruta de acceso UNC (Convención de nomenclatura universal), como \Server\TemplateShare, o una ubicación de carpeta en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ece28-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="ece28-125">Seleccione la casilla para reemplazar las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ece28-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ece28-126">No usar archivos sin conexión</span><span class="sxs-lookup"><span data-stu-id="ece28-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-127">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-128">Esta configuración de directiva le permite configurar si UE-V usará la característica archivos sin conexión de Windows.</span><span class="sxs-lookup"><span data-stu-id="ece28-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="ece28-129">Esta configuración de directiva también le permite habilitar la notificación para que se produzca cuando se retrasa la importación de la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ece28-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-130">Para configurar UE-V Agent de modo que no use archivos sin conexión, habilite esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ece28-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="ece28-131">Especificar si se deben proporcionar notificaciones cuando la importación de configuración se retrasa.</span><span class="sxs-lookup"><span data-stu-id="ece28-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="ece28-132">Especifique la cantidad de tiempo en segundos que se debe esperar antes de que aparezca la notificación.</span><span class="sxs-lookup"><span data-stu-id="ece28-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ece28-133">Tiempo de espera de sincronización</span><span class="sxs-lookup"><span data-stu-id="ece28-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-134">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-135">Esta configuración de Directiva define el número de milisegundos que el equipo esperará antes de que se agote el tiempo de espera al recuperar la configuración de usuario de la ubicación de configuración remota.</span><span class="sxs-lookup"><span data-stu-id="ece28-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="ece28-136">Si la ubicación de almacenamiento remoto no está disponible, el inicio de la aplicación se retrasará este número de milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ece28-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-137">Especifique el tiempo de espera de sincronización preferido en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ece28-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="ece28-138">El valor predeterminado de 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ece28-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ece28-139">Umbral de advertencia de tamaño de paquete</span><span class="sxs-lookup"><span data-stu-id="ece28-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-140">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-141">Esta configuración de directiva le permite configurar el agente de UE-V para que informe cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</span><span class="sxs-lookup"><span data-stu-id="ece28-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-142">Especificó el umbral preferido para los tamaños de paquete de configuración en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="ece28-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="ece28-143">De forma predeterminada, UE-V Agent no tiene un umbral de tamaño de archivo de paquete.</span><span class="sxs-lookup"><span data-stu-id="ece28-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ece28-144">Configuración de la aplicación de itinerancia</span><span class="sxs-lookup"><span data-stu-id="ece28-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-145">Solo usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-146">Esta configuración de Directiva define la itinerancia de la configuración de usuario de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ece28-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-147">Seleccione la configuración de Windows que se transferirá entre equipos.</span><span class="sxs-lookup"><span data-stu-id="ece28-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="ece28-148">De forma predeterminada, la configuración de usuario de las aplicaciones con la plantilla de configuración proporcionada por UE-V se ha desplazado entre equipos.</span><span class="sxs-lookup"><span data-stu-id="ece28-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ece28-149">Configuración de itinerancia de Windows</span><span class="sxs-lookup"><span data-stu-id="ece28-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-150">Solo usuarios</span><span class="sxs-lookup"><span data-stu-id="ece28-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-151">Esta configuración de Directiva establece la itinerancia de la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="ece28-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ece28-152">Seleccione las aplicaciones que se transferirán entre equipos.</span><span class="sxs-lookup"><span data-stu-id="ece28-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="ece28-153">De forma predeterminada, los temas de Windows se mueven entre equipos con la misma versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ece28-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="ece28-154">La configuración del escritorio de Windows y la de accesibilidad no se mueven.</span><span class="sxs-lookup"><span data-stu-id="ece28-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="ece28-155">Para configurar directivas dirigidas al equipo</span><span class="sxs-lookup"><span data-stu-id="ece28-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="ece28-156">Use la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) en el controlador de dominio que administra la Directiva de grupo para equipos UE-V.</span><span class="sxs-lookup"><span data-stu-id="ece28-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="ece28-157">Vaya a **configuración del equipo**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="ece28-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="ece28-158">Seleccione la configuración de directiva que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="ece28-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="ece28-159">Para configurar directivas dirigidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="ece28-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="ece28-160">Use la consola de administración de directivas de grupo (GPMC) o la herramienta de administración avanzada de directivas de grupo (AGPM) en Microsoft Desktop Optimization Pack (MDOP) en el equipo controlador de dominio que administra la Directiva de grupo de UE-V.</span><span class="sxs-lookup"><span data-stu-id="ece28-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="ece28-161">Vaya a **configuración de usuario**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="ece28-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="ece28-162">Seleccione la configuración de directiva editada.</span><span class="sxs-lookup"><span data-stu-id="ece28-162">Select the policy setting edited.</span></span>

<span data-ttu-id="ece28-163">El agente de UE-V usa el siguiente orden de prioridad para determinar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="ece28-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="ece28-164">Orden de prioridad para la configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="ece28-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="ece28-165">Configuración dirigida por el usuario administrada por directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="ece28-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="ece28-166">Configuración de destino del equipo administrada por directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="ece28-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="ece28-167">Opciones de configuración definidas por el usuario actual con PowerShell o WMI: el agente de UE-V almacena estas opciones de configuración en esta ubicación del registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="ece28-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="ece28-168">Opciones de configuración definidas para el equipo con PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="ece28-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="ece28-169">El agente de UE-V almacena estas opciones de configuración en el `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="ece28-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="ece28-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ece28-170">Related topics</span></span>


[<span data-ttu-id="ece28-171">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ece28-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="ece28-172">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ece28-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





