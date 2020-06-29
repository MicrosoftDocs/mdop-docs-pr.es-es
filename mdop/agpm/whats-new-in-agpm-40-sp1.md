---
title: Novedades de AGPM 4.0 SP1
description: Novedades de AGPM 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818151"
---
# <span data-ttu-id="c447e-103">Novedades de AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="c447e-104">Este contenido de "Novedades" describe las mejoras y las configuraciones admitidas para la administración avanzada de directivas de grupo (AGPM) 4,0 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c447e-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="c447e-105">Si hay una diferencia entre este contenido y otra documentación de AGPM, este contenido debe considerarse autoritario y debe reemplazar el contenido incluido en este producto.</span><span class="sxs-lookup"><span data-stu-id="c447e-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="c447e-106">Novedades</span><span class="sxs-lookup"><span data-stu-id="c447e-106">What’s new</span></span>


<span data-ttu-id="c447e-107">AGPM 4,0 SP1 admite las siguientes mejoras:</span><span class="sxs-lookup"><span data-stu-id="c447e-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="c447e-108">Extensiones de cliente nuevas y modificadas</span><span class="sxs-lookup"><span data-stu-id="c447e-108">New and changed client-side extensions</span></span>

<span data-ttu-id="c447e-109">Se han agregado o cambiado extensiones de cliente de la Directiva de grupo (CSE) para que AGPM admita las nuevas directivas de grupo en Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c447e-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="c447e-110">Estas directivas de Grupo permiten a los administradores de directivas de grupo administrar y realizar un seguimiento de la configuración específica de la Directiva de grupo de Windows 8 que cambian entre dos objetos de directiva de grupo (GPO) o plantillas.</span><span class="sxs-lookup"><span data-stu-id="c447e-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="c447e-111">También puede crear GPO personalizados, con la configuración específica de Windows 8, y configurar y guardar los GPO como una plantilla.</span><span class="sxs-lookup"><span data-stu-id="c447e-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="c447e-112">Para ver las CSE, use los informes de configuración y de diferencias que están disponibles en el cliente AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c447e-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="c447e-113">Las extensiones del cliente de directiva de grupo nuevas y modificadas son:</span><span class="sxs-lookup"><span data-stu-id="c447e-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="c447e-114">**Directiva de acceso central:** Permite a los administradores de la Directiva de grupo especificar directivas de acceso central en servidores de directivas de grupo, por ejemplo, servidores de archivos.</span><span class="sxs-lookup"><span data-stu-id="c447e-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="c447e-115">La Directiva de acceso central es una directiva de autorización que se especifica mediante un elemento de GPO y que se aplica a los destinos de directiva para facilitar el acceso centralizado y el control de los recursos.</span><span class="sxs-lookup"><span data-stu-id="c447e-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="c447e-116">Estas directivas de acceso centralizado se deben configurar en un equipo cliente de directiva de grupo desde Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c447e-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="c447e-117">Una directiva de grupo distribuye el conocimiento de una directiva de acceso central aplicable a los equipos que deben exigirlo.</span><span class="sxs-lookup"><span data-stu-id="c447e-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="c447e-118">**Cambios en la Directiva de resolución de nombres:** Permite a los administradores de la Directiva de grupo establecer la configuración de la seguridad DNS y DirectAccess en equipos cliente DNS.</span><span class="sxs-lookup"><span data-stu-id="c447e-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="c447e-119">Se han agregado nuevas pestañas para configurar la configuración del servidor DNS genérico y la configuración de la codificación.</span><span class="sxs-lookup"><span data-stu-id="c447e-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="c447e-120">**Cambios de preferencias de directiva de Grupo:** Agrega compatibilidad para la configuración y administración de la configuración de Internet Explorer 10 que se agregó para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c447e-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="c447e-121">**Conexiones de escritorio y aplicaciones remotas:** Permite a los administradores de directivas de grupo especificar la dirección URL de conexión predeterminada que se usa para las conexiones de escritorio y de aplicaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="c447e-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="c447e-122">**Opciones de inicio de Windows to Go:** Permite a los administradores de directivas de grupo configurar si el equipo arrancará en Windows to go si un dispositivo USB que contiene un área de trabajo de Windows to go está conectado.</span><span class="sxs-lookup"><span data-stu-id="c447e-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="c447e-123">**Opciones de hibernación de Windows to Go:** Permite a los administradores de directivas de grupo configurar si un equipo puede usar el estado de suspensión de hibernación (S4) cuando el equipo se inicia desde un área de trabajo de Windows to go.</span><span class="sxs-lookup"><span data-stu-id="c447e-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="c447e-124">Comentarios de los clientes y Resumen de revisiones</span><span class="sxs-lookup"><span data-stu-id="c447e-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="c447e-125">AGPM 4,0 SP1 incluye un resumen de correcciones para resolver los problemas encontrados desde la versión de AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="c447e-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="c447e-126">AGPM 4,0 SP1 contiene las últimas revisiones hasta el Hotfix 1 de 4,0 administración avanzada de directivas de grupo de Microsoft (incluido).</span><span class="sxs-lookup"><span data-stu-id="c447e-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="c447e-127">La configuración y los informes de diferencias muestran las nuevas extensiones de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="c447e-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="c447e-128">Las nuevas extensiones de directiva de grupo se han agregado a los informes de diferencias y configuración.</span><span class="sxs-lookup"><span data-stu-id="c447e-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="c447e-129">Cambios de instalación y soporte técnico</span><span class="sxs-lookup"><span data-stu-id="c447e-129">Installer changes and support</span></span>

<span data-ttu-id="c447e-130">Los cambios y la compatibilidad con el instalador de AGPM 4,0 SP1 son:</span><span class="sxs-lookup"><span data-stu-id="c447e-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="c447e-131">Si instala AGPM 4,0 SP1 en Windows 8 o Windows Server 2012, el instalador de AGPM verifica que se instale el software previo requerido (consola de administración de directivas de grupo y .NET 3,5 Framework).</span><span class="sxs-lookup"><span data-stu-id="c447e-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="c447e-132">Si estos requisitos previos no están instalados, la instalación de AGPM 4,0 SP1 está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c447e-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="c447e-133">Al instalar AGPM 4,0 SP1, la activación de WCF, la activación no HTTP y el servicio de activación de procesos de Windows se habilitan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c447e-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="c447e-134">En los sistemas operativos Windows Vista, Windows 7 y Windows 8, descargue la versión adecuada del kit de herramientas de administración de sistemas remoto para su sistema operativo antes de instalar AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c447e-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="c447e-135">Se admite la compatibilidad con versiones anteriores de sistemas operativos compatibles.</span><span class="sxs-lookup"><span data-stu-id="c447e-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="c447e-136">Capacidad de actualizar o actualizar a AGPM 4,0 SP1 sin volver a especificar parámetros de configuración</span><span class="sxs-lookup"><span data-stu-id="c447e-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="c447e-137">Puede actualizar el cliente o servidor de AGPM a AGPM 4,0 SP1 solo de AGPM 4,0 sin que se le pida que vuelva a escribir los parámetros de configuración (denominado "actualización inteligente"), como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c447e-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="c447e-138">Si va a actualizar a AGPM 4,0 SP1 desde otras versiones de AGPM, como se muestra en la tabla, debe usar la "actualización clásica", que requiere volver a introducir los parámetros de configuración.</span><span class="sxs-lookup"><span data-stu-id="c447e-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="c447e-139">Como cada versión de AGPM está asociada a un sistema operativo en particular, consulte [elegir la versión de AGPM que se instalará](https://go.microsoft.com/fwlink/?LinkId=254350)y asegúrese de actualizar el sistema operativo según corresponda antes de realizar una actualización.</span><span class="sxs-lookup"><span data-stu-id="c447e-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

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
<td align="left"><p><strong><span data-ttu-id="c447e-140">Versión de AGPM desde la que se puede actualizar</span><span class="sxs-lookup"><span data-stu-id="c447e-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c447e-141">2,5</span><span class="sxs-lookup"><span data-stu-id="c447e-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c447e-142">3,0</span><span class="sxs-lookup"><span data-stu-id="c447e-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c447e-143">4,0</span><span class="sxs-lookup"><span data-stu-id="c447e-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c447e-144">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c447e-145">2,5</span><span class="sxs-lookup"><span data-stu-id="c447e-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-146">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c447e-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-147">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="c447e-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-148">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="c447e-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-149">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="c447e-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c447e-150">3,0</span><span class="sxs-lookup"><span data-stu-id="c447e-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-151">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c447e-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-152">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c447e-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-153">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="c447e-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-154">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="c447e-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c447e-155">4,0</span><span class="sxs-lookup"><span data-stu-id="c447e-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-156">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c447e-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-157">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c447e-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-158">No aplicable</span><span class="sxs-lookup"><span data-stu-id="c447e-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-159">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="c447e-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c447e-160">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="c447e-160">Supported configurations</span></span>


<span data-ttu-id="c447e-161">AGPM admite las configuraciones de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c447e-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="c447e-162">Aunque AGPM admite configuraciones mixtas, se recomienda encarecidamente que ejecute el servidor y el cliente de AGPM en la misma familia de sistemas operativos, por ejemplo, Windows 8 con Windows Server 2012, Windows 7 con Windows Server 2008 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="c447e-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c447e-163">Configuraciones admitidas para el servidor AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c447e-164">Configuraciones compatibles para clientes AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c447e-165">Soporte técnico de AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c447e-166">Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c447e-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-167">Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c447e-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-168">Se admite</span><span class="sxs-lookup"><span data-stu-id="c447e-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c447e-169">Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="c447e-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-170">Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="c447e-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-171">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8</span><span class="sxs-lookup"><span data-stu-id="c447e-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c447e-172">Windows Server 2008 R2, Windows 7 o Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c447e-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-173">Windows Server 2008 o Windows Vista con Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="c447e-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-174">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server 2008 R2, Windows 7 o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c447e-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c447e-175">Windows Server 2008 o Windows Vista con Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="c447e-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-176">Windows Server 2008 R2, Windows 7 o Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c447e-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-177">Se admite</span><span class="sxs-lookup"><span data-stu-id="c447e-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c447e-178">Windows Server 2008 o Windows Vista con Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="c447e-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-179">Windows Server 2008 o Windows Vista con Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="c447e-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c447e-180">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server 2008 R2 o Windows 7 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="c447e-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c447e-181">Requisitos previos para instalar AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="c447e-182">La siguiente tabla describe el comportamiento en Windows 8 de los instaladores de cliente y de servidor de AGPM 4,0 SP1 cuando falta .NET 3,5 o la consola de administración de directivas de grupo en las herramientas de administración de servidor remoto (RSAT).</span><span class="sxs-lookup"><span data-stu-id="c447e-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="c447e-183">Cliente AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="c447e-184">Servidor AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="c447e-185">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c447e-185">Operating System</span></span>**

**<span data-ttu-id="c447e-186">.NET</span><span class="sxs-lookup"><span data-stu-id="c447e-186">.NET</span></span>**

**<span data-ttu-id="c447e-187">RSAT</span><span class="sxs-lookup"><span data-stu-id="c447e-187">RSAT</span></span>**

**<span data-ttu-id="c447e-188">.NET</span><span class="sxs-lookup"><span data-stu-id="c447e-188">.NET</span></span>**

**<span data-ttu-id="c447e-189">RSAT</span><span class="sxs-lookup"><span data-stu-id="c447e-189">RSAT</span></span>**

**<span data-ttu-id="c447e-190">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c447e-190">Windows 8</span></span>**

<span data-ttu-id="c447e-191">Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="c447e-192">Si GPMC no está habilitado ni instalado en el sistema, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="c447e-193">Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="c447e-194">Si GPMC no está habilitado ni instalado en el sistema, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="c447e-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c447e-195">Windows Server 2012</span></span>**

<span data-ttu-id="c447e-196">Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="c447e-197">Si la consola GPMC no está habilitada, el instalador la habilita durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="c447e-198">Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="c447e-199">Si la consola GPMC no está habilitada, el instalador la habilita durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c447e-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="c447e-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c447e-200">Related topics</span></span>


[<span data-ttu-id="c447e-201">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="c447e-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="c447e-202">Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c447e-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





