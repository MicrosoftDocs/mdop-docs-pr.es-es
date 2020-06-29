---
title: Novedades de AGPM 4.0 SP2
description: Novedades de AGPM 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818150"
---
# <span data-ttu-id="0cbb6-103">Novedades de AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="0cbb6-104">Este contenido describe las mejoras y las configuraciones admitidas para el Service Pack 2 de administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="0cbb6-105">Si hay una diferencia entre este contenido y otra documentación de AGPM, tenga en cuenta que este contenido es autoritativo y asuma que reemplaza a la otra documentación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="0cbb6-106">Novedades</span><span class="sxs-lookup"><span data-stu-id="0cbb6-106">What’s new</span></span>


<span data-ttu-id="0cbb6-107">AGPM 4.0 SP2 admite las siguientes características y funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="0cbb6-108">Compatibilidad con Windows 8.1 y Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="0cbb6-109">AGPM 4.0 SP2 agrega compatibilidad para los sistemas operativos Windows 8.1 y Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="0cbb6-110">Extensiones de cliente nuevas y modificadas</span><span class="sxs-lookup"><span data-stu-id="0cbb6-110">New and changed client-side extensions</span></span>

<span data-ttu-id="0cbb6-111">Las extensiones de cliente de la Directiva de grupo se han agregado o cambiado para que AGPM admita la nueva configuración de directiva en Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="0cbb6-112">Esta configuración de directiva permite que los administradores de directivas de grupo administren y realicen un seguimiento de configuraciones de directiva específicas de Windows 8.1 que cambian entre dos objetos de directiva de grupo (GPO) o plantillas.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="0cbb6-113">Para ver las extensiones de cliente, use la configuración y los informes de diferencias que están disponibles en el cliente de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="0cbb6-114">Las extensiones del cliente de directiva de grupo nuevas y modificadas son:</span><span class="sxs-lookup"><span data-stu-id="0cbb6-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="0cbb6-115">**Especificar la configuración de las carpetas de trabajo**</span><span class="sxs-lookup"><span data-stu-id="0cbb6-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="0cbb6-116">Si habilita esta configuración de Directiva, los administradores de TI podrán configurar las carpetas de trabajo para que se creen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="0cbb6-117">La característica carpetas de trabajo permite a los usuarios finales sincronizar los archivos de sus dispositivos de escritorio de Windows con los otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="0cbb6-118">Use esta configuración de directiva para crear la relación de sincronización en los dispositivos de un usuario final y para configurar cómo identificar el servidor de archivos que almacena las carpetas de trabajo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="0cbb6-119">Si selecciona la casilla de verificación **sincronización de provisionamiento automático** , se creará el perfil de sincronización sin la intervención del usuario y los datos comenzarán automáticamente la sincronización con el dispositivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="0cbb6-120">Si no activa la casilla de verificación **sincronización automática** , los usuarios deben proporcionar una entrada para iniciar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="0cbb6-121">**Forzar la configuración automática para todos los usuarios**.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="0cbb6-122">Si habilita esta configuración de Directiva, los administradores de TI podrán determinar si deben crear la Asociación de carpetas de trabajo automáticamente en los dispositivos de usuario final sin la entrada de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="0cbb6-123">Si habilita esta configuración de Directiva, la sincronización se establecerá de acuerdo con la forma en que configure la configuración de directiva **especificar carpetas de trabajo** .</span><span class="sxs-lookup"><span data-stu-id="0cbb6-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="0cbb6-124">Si establece la configuración de directiva **forzar la configuración automática de todos los usuarios** como **deshabilitada** o **no configurada**, la relación de las carpetas de trabajo se configurará según cómo establezca la opción de **aprovisionamiento automático** en la opción **especificar la configuración de las carpetas de trabajo** .</span><span class="sxs-lookup"><span data-stu-id="0cbb6-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="0cbb6-125">Para obtener más información sobre la característica carpetas de trabajo, consulte [Introducción a carpetas de trabajo](https://go.microsoft.com/fwlink/?LinkId=330444).</span><span class="sxs-lookup"><span data-stu-id="0cbb6-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="0cbb6-126">Comentarios de los clientes y Resumen de revisiones</span><span class="sxs-lookup"><span data-stu-id="0cbb6-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="0cbb6-127">AGPM 4.0 SP2 incluye un resumen de las revisiones para solucionar los problemas encontrados desde la versión de AGPM 4.0 Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0cbb6-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="0cbb6-128">AGPM 4.0 SP2 contiene las últimas revisiones hasta el Service Pack 1 de Microsoft Advanced Group Management 4.0 Hotfix1.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="0cbb6-129">Para obtener más información, consulte el artículo [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)de Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="0cbb6-130">Nuevas extensiones de directiva de grupo en la configuración y los informes de diferencias</span><span class="sxs-lookup"><span data-stu-id="0cbb6-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="0cbb6-131">Las nuevas extensiones de directiva de grupo se han agregado a los informes de diferencias y configuración.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="0cbb6-132">Cambios de instalación y soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0cbb6-132">Installer changes and support</span></span>

<span data-ttu-id="0cbb6-133">Los cambios y la compatibilidad con el instalador de AGPM 4.0 SP2 son:</span><span class="sxs-lookup"><span data-stu-id="0cbb6-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="0cbb6-134">Si instala AGPM 4.0 SP2 en el sistema operativo Windows 8 o Windows Server 2012 o en sistemas operativos posteriores, el instalador de AGPM verifica que se instale el software previo necesario (la consola de administración de directivas de grupo (GPMC) y Microsoft .NET Framework 3.5).</span><span class="sxs-lookup"><span data-stu-id="0cbb6-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="0cbb6-135">Si no se instala este software necesario, la instalación de AGPM 4.0 SP2 está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="0cbb6-136">Al instalar el servidor de AGPM, la activación de WCF, la activación no HTTP y el servicio de activación de procesos de Windows se habilitan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="0cbb6-137">En el sistema operativo cliente vista y versiones posteriores, descargue la versión adecuada de las herramientas de administración remota del sistema para su sistema operativo antes de instalar AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="0cbb6-138">AGPM 4.0 SP2 admite compatibilidad con versiones anteriores de sistemas operativos compatibles.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="0cbb6-139">Posibilidad de actualizar a AGPM 4.0 SP2 sin volver a escribir los parámetros de configuración</span><span class="sxs-lookup"><span data-stu-id="0cbb6-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="0cbb6-140">Puede actualizar el cliente de AGPM o el servidor AGPM a el SP2 de AGPM 4.0 sin que se le pida que vuelva a escribir los parámetros de configuración (denominado actualización inteligente) solo de AGPM 4.0 en adelante, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="0cbb6-141">Si va a actualizar a AGPM 4.0 SP2 desde otras versiones de AGPM, como se muestra en la tabla, debe usar la actualización clásica, que requiere volver a introducir los parámetros de configuración.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="0cbb6-142">Como cada versión de AGPM está asociada a un sistema operativo en particular, consulte [elegir qué versión de AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) y asegurarse de que actualiza el sistema operativo según corresponda antes de actualizar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="0cbb6-143">Actualizaciones admitidas por AGPM 4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-143">AGPM 4.0 SP2 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0cbb6-144">Versión de AGPM desde la que se puede actualizar</span><span class="sxs-lookup"><span data-stu-id="0cbb6-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0cbb6-145">2,5</span><span class="sxs-lookup"><span data-stu-id="0cbb6-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0cbb6-146">3,0</span><span class="sxs-lookup"><span data-stu-id="0cbb6-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0cbb6-147">4,0</span><span class="sxs-lookup"><span data-stu-id="0cbb6-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0cbb6-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0cbb6-149">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cbb6-150">2,5</span><span class="sxs-lookup"><span data-stu-id="0cbb6-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-151">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-152">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="0cbb6-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-153">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="0cbb6-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-154">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="0cbb6-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-155">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="0cbb6-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cbb6-156">3,0</span><span class="sxs-lookup"><span data-stu-id="0cbb6-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-157">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-158">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-159">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="0cbb6-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-160">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="0cbb6-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-161">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="0cbb6-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cbb6-162">4,0</span><span class="sxs-lookup"><span data-stu-id="0cbb6-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-163">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-164">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-165">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-166">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="0cbb6-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-167">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="0cbb6-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cbb6-168">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-169">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-170">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-171">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-172">No disponible</span><span class="sxs-lookup"><span data-stu-id="0cbb6-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-173">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="0cbb6-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0cbb6-174">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="0cbb6-174">Supported configurations</span></span>


<span data-ttu-id="0cbb6-175">AGPM 4.0 SP2 admite las configuraciones de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="0cbb6-176">Aunque AGPM admite configuraciones mixtas, le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea del sistema operativo, por ejemplo, Windows 8.1 con Windows Server2012 R2, Windows 8 con Windows Server 2012, etc.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="0cbb6-177">Configuración de directiva y sistemas operativos compatibles con el SP2 de AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="0cbb6-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0cbb6-178">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0cbb6-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0cbb6-179">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="0cbb6-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0cbb6-180">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="0cbb6-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cbb6-181">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-182">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-183">Se admite</span><span class="sxs-lookup"><span data-stu-id="0cbb6-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cbb6-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="0cbb6-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-185">Windows Server 2012 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="0cbb6-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-186">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cbb6-187">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0cbb6-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-188">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0cbb6-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-189">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="0cbb6-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cbb6-190">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0cbb6-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-191">Windows Server2008 o vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="0cbb6-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-192">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0cbb6-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cbb6-193">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-194">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0cbb6-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-195">No se admite</span><span class="sxs-lookup"><span data-stu-id="0cbb6-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cbb6-196">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-197">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cbb6-198">Compatible pero no puede editar o modificar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0cbb6-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0cbb6-199">Requisitos previos para instalar AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="0cbb6-200">En la siguiente tabla se describe el comportamiento de los instaladores de cliente y de servidor de AGPM 4.0 SP2 en Windows 8.1 cuando falta la versión 3.5 de .NET Framework o la GPMC en las herramientas de administración remota del servidor.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="0cbb6-201">Cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="0cbb6-201">AGPM Client</span></span>**

**<span data-ttu-id="0cbb6-202">Servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0cbb6-202">AGPM Server</span></span>**

**<span data-ttu-id="0cbb6-203">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0cbb6-203">Operating system</span></span>**

**<span data-ttu-id="0cbb6-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="0cbb6-204">.NET Framework</span></span>**

**<span data-ttu-id="0cbb6-205">Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="0cbb6-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="0cbb6-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="0cbb6-206">.NET Framework</span></span>**

**<span data-ttu-id="0cbb6-207">Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="0cbb6-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="0cbb6-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0cbb6-208">Windows8.1</span></span>**

<span data-ttu-id="0cbb6-209">Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="0cbb6-210">Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="0cbb6-211">Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="0cbb6-212">Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="0cbb6-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="0cbb6-214">Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="0cbb6-215">Si la GPMC no está habilitada, el instalador la habilita durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="0cbb6-216">Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="0cbb6-217">Si la GPMC no está habilitada, el instalador la habilita durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="0cbb6-218">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="0cbb6-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="0cbb6-219">AGPM 4,0 SP2 forma parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="0cbb6-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="0cbb6-220">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="0cbb6-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="0cbb6-221">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="0cbb6-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="0cbb6-222">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cbb6-222">Related topics</span></span>


[<span data-ttu-id="0cbb6-223">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0cbb6-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="0cbb6-224">Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0cbb6-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="0cbb6-225">Elección de qué versión de AGPM ha de instalarse</span><span class="sxs-lookup"><span data-stu-id="0cbb6-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





