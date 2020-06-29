---
title: Métodos de sincronización para UE-V 2.x
description: Métodos de sincronización para UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823580"
---
# <span data-ttu-id="a0580-103">Métodos de sincronización para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="a0580-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="a0580-104">El agente de Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 y 2,1 SP1 le permite sincronizar la configuración de Windows y de la aplicación de los usuarios con la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="a0580-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="a0580-105">La configuración del *método de sincronización* define cómo UE-V Agent carga y descarga esa configuración en la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="a0580-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="a0580-106">UE-V 2. x introduce una nueva SyncMethod denominada *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="a0580-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="a0580-107">Para obtener más información sobre los eventos desencadenadores que inician la sincronización de la configuración de la aplicación y de Windows, consulte [sincronizar eventos desencadenadores para UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="a0580-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="a0580-108">Configuración de SyncMethod</span><span class="sxs-lookup"><span data-stu-id="a0580-108">SyncMethod Configuration</span></span>


<span data-ttu-id="a0580-109">En esta tabla se explican los cambios de SyncMethod de UE-V v 1.0 a v 2.0 a v 2.1, así como la configuración de cada configuración:</span><span class="sxs-lookup"><span data-stu-id="a0580-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0580-110">Configuración de SyncMethod</span><span class="sxs-lookup"><span data-stu-id="a0580-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a0580-111">V 1.0</span><span class="sxs-lookup"><span data-stu-id="a0580-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a0580-112">V 2.0</span><span class="sxs-lookup"><span data-stu-id="a0580-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a0580-113">V 2.1 y V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="a0580-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a0580-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0580-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0580-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="a0580-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-116">n/d</span><span class="sxs-lookup"><span data-stu-id="a0580-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-117">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a0580-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-118">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a0580-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-119">Los cambios de configuración para una aplicación específica o para la configuración de escritorio global de Windows se guardan de forma local en una carpeta de caché.</span><span class="sxs-lookup"><span data-stu-id="a0580-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="a0580-120">Estos cambios se sincronizan con la ubicación de almacenamiento de configuración cuando tiene lugar un evento de activación de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a0580-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="a0580-121">Al presionar los cambios se guardarán los cambios locales en la ruta de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="a0580-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="a0580-122">Esta configuración predeterminada es la norma Gold para equipos.</span><span class="sxs-lookup"><span data-stu-id="a0580-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="a0580-123">Esta opción intenta sincronizar la configuración y se agota el tiempo de espera después de un breve retraso para garantizar que el inicio de la aplicación o del sistema operativo no se retrase durante un período de tiempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="a0580-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="a0580-124">Esta funcionalidad también está vinculada a la tarea programada: aplicación de controlador de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a0580-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="a0580-125">El administrador controla la frecuencia de la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="a0580-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="a0580-126">De forma predeterminada, los equipos sincronizan su configuración cada 30 minutos después de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="a0580-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0580-127">OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="a0580-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-128">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a0580-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-129">En desuso</span><span class="sxs-lookup"><span data-stu-id="a0580-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-130">En desuso</span><span class="sxs-lookup"><span data-stu-id="a0580-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-131">Se comporta de la misma manera que SyncProvider en V 2.0.</span><span class="sxs-lookup"><span data-stu-id="a0580-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="a0580-132">Si los archivos sin conexión están habilitados y la carpeta está anclada, UE-V desanclará esta carpeta y se sincronizará directamente con el directorio central SMB.</span><span class="sxs-lookup"><span data-stu-id="a0580-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="a0580-133">Nota: </strong> en V 1.0 si desea usar UE-V en una sociedad corporativa desconectada (también conocido como un viaje con un equipo portátil), la guía consiste en usar archivos sin conexión para asegurarse de que la configuración se ha movido.</span><span class="sxs-lookup"><span data-stu-id="a0580-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="a0580-134">Hemos recibido suficientes comentarios de los clientes para que la activación de archivos sin conexión sea un bloqueo empresarial no trivial.</span><span class="sxs-lookup"><span data-stu-id="a0580-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="a0580-135">Por tanto, en UE-V 2, hemos creado un motor de sincronización estrechamente acoplado para almacenar los datos de forma local y sincronizar la configuración con el servidor central.</span><span class="sxs-lookup"><span data-stu-id="a0580-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="a0580-136">Este área de características no reemplaza los archivos sin conexión ni el redireccionamiento de carpetas.</span><span class="sxs-lookup"><span data-stu-id="a0580-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="a0580-137">UE-V 2 no funciona bien con las carpetas sin conexión, de modo que la orientación no es establecer la ruta de almacenamiento de configuración en una carpeta anclada sin conexión o CSC.</span><span class="sxs-lookup"><span data-stu-id="a0580-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0580-138">External</span><span class="sxs-lookup"><span data-stu-id="a0580-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-139">n/d</span><span class="sxs-lookup"><span data-stu-id="a0580-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-140">n/d</span><span class="sxs-lookup"><span data-stu-id="a0580-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-141">Se admite</span><span class="sxs-lookup"><span data-stu-id="a0580-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-142">Nuevo en UE-V 2,1, este método de configuración especifica que si la configuración de UE-V se escribe en una carpeta local en el equipo del usuario, cualquier motor de sincronización externo (como OneDrive para la empresa, carpetas de trabajo, SharePoint o Dropbox) se puede usar para aplicar esta configuración a los diferentes equipos a los que los usuarios tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="a0580-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0580-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a0580-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-144">Sí</span><span class="sxs-lookup"><span data-stu-id="a0580-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-145">Sí</span><span class="sxs-lookup"><span data-stu-id="a0580-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-146">Sí</span><span class="sxs-lookup"><span data-stu-id="a0580-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0580-147">Esta configuración está diseñada para la experiencia de infraestructura de escritorio virtual (VDI) y la de aplicaciones transmitidas principalmente.</span><span class="sxs-lookup"><span data-stu-id="a0580-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="a0580-148">Esta configuración debe usarse en los cuadros de Windows Server que se usan en un centro de recursos, donde la conexión siempre estará disponible.</span><span class="sxs-lookup"><span data-stu-id="a0580-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="a0580-149">Los cambios de configuración se guardan directamente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a0580-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="a0580-150">Si la conexión de red a la ruta de almacenamiento de configuración no está disponible, los cambios de configuración se almacenarán en caché en el dispositivo y se sincronizarán la próxima vez que se ejecute el proveedor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a0580-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="a0580-151">Si no se encuentra la ruta de almacenamiento de configuración y el perfil de usuario se quita de un entorno de VDI agrupado al cerrar sesión, se perderán estos cambios de configuración y el usuario deberá volver a aplicar el cambio cuando el equipo pueda volver a la ruta de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="a0580-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="a0580-152">Las aplicaciones y el sistema operativo esperarán indefinidamente a que la ubicación esté presente.</span><span class="sxs-lookup"><span data-stu-id="a0580-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="a0580-153">Esto podría provocar que el tiempo de inicio de sesión de un sistema operativo o la carga de la aplicación aumente significativamente si no se encuentra la ubicación.</span><span class="sxs-lookup"><span data-stu-id="a0580-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a0580-154">Puede configurar el método de sincronización de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="a0580-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="a0580-155">Al [implementar el agente de UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) con un parámetro de línea de comandos o en un script de proceso por lotes</span><span class="sxs-lookup"><span data-stu-id="a0580-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="a0580-156">Mediante la configuración de [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0580-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="a0580-157">Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) para UE-V</span><span class="sxs-lookup"><span data-stu-id="a0580-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="a0580-158">Después de la instalación de UE-V Agent, mediante [Windows PowerShell o el instrumental de administración de Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0580-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="a0580-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0580-159">Related topics</span></span>


[<span data-ttu-id="a0580-160">Implementar funciones necesarias para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="a0580-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="a0580-161">Implementar funciones necesarias para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="a0580-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="a0580-162">Referencia técnica de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="a0580-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





