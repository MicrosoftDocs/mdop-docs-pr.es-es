---
title: Acerca de App-V 5.0 SP3
description: Acerca de App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814971"
---
# <span data-ttu-id="56c5f-103">Acerca de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="56c5f-104">Use las siguientes secciones para revisar la información sobre los cambios significativos que se aplican a Microsoft Application Virtualization (App-V) 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="56c5f-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="56c5f-105">Requisitos previos de software de App-V 5,0 SP3 y configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="56c5f-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="56c5f-106">Migrar a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="56c5f-107">El archivo XML del grupo de conexiones creado manualmente requiere actualizar al esquema</span><span class="sxs-lookup"><span data-stu-id="56c5f-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="56c5f-108">Mejoras en los grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="56c5f-109">Los administradores pueden publicar y anular la publicación de paquetes para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="56c5f-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="56c5f-110">Habilitar solo los administradores para publicar y anular la publicación de paquetes</span><span class="sxs-lookup"><span data-stu-id="56c5f-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="56c5f-111">La clave de registro RunVirtual admite paquetes que se publican para el usuario</span><span class="sxs-lookup"><span data-stu-id="56c5f-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="56c5f-112">Nuevos cmdlets de PowerShell y ayuda para cmdlet actualizable</span><span class="sxs-lookup"><span data-stu-id="56c5f-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="56c5f-113">El directorio principal de la aplicación virtual (PVAD) está oculto pero puede activarse</span><span class="sxs-lookup"><span data-stu-id="56c5f-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="56c5f-114">ClientVersion es necesario para ver los metadatos de publicación de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="56c5f-115">Los registros de eventos de App-V se han consolidado</span><span class="sxs-lookup"><span data-stu-id="56c5f-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="56c5f-116">Requisitos previos de software de App-V 5,0 SP3 y configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="56c5f-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="56c5f-117">Consulte los siguientes vínculos para los requisitos previos del software de App-V 5,0 SP3 y las configuraciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="56c5f-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-118">Vínculos a requisitos previos y configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="56c5f-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="56c5f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="56c5f-120">Requisitos previos de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="56c5f-121">Requisitos previos de software que debe instalar antes de iniciar la instalación de App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="56c5f-122">Configuraciones admitidas de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="56c5f-123">Requisitos de hardware y sistemas operativos compatibles con el servidor de App-V, el secuenciador y los componentes de cliente</span><span class="sxs-lookup"><span data-stu-id="56c5f-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="56c5f-124">Migrar a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="56c5f-125">Use la siguiente información para actualizar a App-V 5,0 SP3 desde versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="56c5f-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="56c5f-126">Antes de iniciar la actualización</span><span class="sxs-lookup"><span data-stu-id="56c5f-126">Before you start the upgrade</span></span>

<span data-ttu-id="56c5f-127">Revise la siguiente información antes de iniciar la actualización:</span><span class="sxs-lookup"><span data-stu-id="56c5f-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-128">Elementos para revisar antes de actualizar</span><span class="sxs-lookup"><span data-stu-id="56c5f-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="56c5f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-130">Componentes para actualizar</span><span class="sxs-lookup"><span data-stu-id="56c5f-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="56c5f-131">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="56c5f-132">Secuenciador</span><span class="sxs-lookup"><span data-stu-id="56c5f-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="56c5f-133">Cliente de App-V o de servicios de escritorio remoto (RDS) de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="56c5f-134">Grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="56c5f-135">Nota</span><span class="sxs-lookup"><span data-stu-id="56c5f-135">Note</span></span></strong><br/><p><span data-ttu-id="56c5f-136">Para usar la interfaz de usuario del cliente de App-V, descargue la versión existente de la <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicación de UI cliente de Microsoft Application virtualization 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-137">Actualizando desde App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="56c5f-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-138">Primero debe actualizar a App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="56c5f-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="56c5f-139">No puede actualizar directamente de App-V 4. x a App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="56c5f-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="56c5f-140">Para más información, consulta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56c5f-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="56c5f-141">Acerca de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="56c5f-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="56c5f-142">Planificación para migrar desde una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-143">Actualización de App-V 5,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="56c5f-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-144">Puede actualizar a App-V 5,0 SP3 directamente desde cualquiera de las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="56c5f-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="56c5f-145">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="56c5f-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="56c5f-146">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="56c5f-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="56c5f-147">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="56c5f-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="56c5f-148">Para actualizar a App-V 5,0 SP3, siga los pasos que se indican en el resto de las secciones de este artículo.</span><span class="sxs-lookup"><span data-stu-id="56c5f-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-149">Cambios necesarios en paquetes y grupos de conexión después de la actualización</span><span class="sxs-lookup"><span data-stu-id="56c5f-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-150">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="56c5f-150">None.</span></span> <span data-ttu-id="56c5f-151">Los paquetes y los grupos de conexión seguirán funcionando tal y como están actualmente.</span><span class="sxs-lookup"><span data-stu-id="56c5f-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="56c5f-152">Pasos para actualizar la infraestructura de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="56c5f-153">Complete los siguientes pasos para actualizar cada componente de la infraestructura de App-V a App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="56c5f-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-154">Paso</span><span class="sxs-lookup"><span data-stu-id="56c5f-154">Step</span></span></th>
<th align="left"><span data-ttu-id="56c5f-155">Para más información</span><span class="sxs-lookup"><span data-stu-id="56c5f-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-156">Paso 1: actualizar el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="56c5f-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="56c5f-157">Si no usa el servidor de App-V, omita este paso y vaya al siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="56c5f-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="56c5f-158">Nota</span><span class="sxs-lookup"><span data-stu-id="56c5f-158">Note</span></span></strong><br/><p><span data-ttu-id="56c5f-159">El cliente de App-V 5,0 SP3 es compatible con el servidor de App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="56c5f-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="56c5f-160">Sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="56c5f-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="56c5f-161">Revise las <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> notas de la versión de App-v 5,0 SP3 </a> para problemas que pueden afectar a la instalación de App-v Server.</span><span class="sxs-lookup"><span data-stu-id="56c5f-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="56c5f-162">Siga uno de estos procedimientos, según el método que use para actualizar la base de datos de administración o la base de datos de informes:</span><span class="sxs-lookup"><span data-stu-id="56c5f-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-163">Método de actualización de base de datos</span><span class="sxs-lookup"><span data-stu-id="56c5f-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="56c5f-164">Paso</span><span class="sxs-lookup"><span data-stu-id="56c5f-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-165">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="56c5f-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-166">Omita este paso y vaya al paso 3, "si está actualizando el servidor de App-V..."</span><span class="sxs-lookup"><span data-stu-id="56c5f-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-167">Scripts SQL</span><span class="sxs-lookup"><span data-stu-id="56c5f-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="56c5f-168">Base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="56c5f-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-169">Para instalar o actualizar, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL para instalar o actualizar la base de datos del servidor de administración de App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="56c5f-170">Base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="56c5f-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-171">Siga los pasos <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> que se indican en cómo implementar las bases de datos de App-V con scripts SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="56c5f-172">Si está actualizando el servidor de App-V desde el paquete de revisiones 3 o posterior de App-V 5,0 SP1, complete los pasos de la sección <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> comprobar las claves del registro después de instalar el servidor de App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="56c5f-173">Siga los pasos <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> que se indican en cómo implementar el servidor de App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-174">Paso 2: actualice el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="56c5f-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-175">Vea <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Cómo instalar el secuenciador </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-176">Paso 3: actualizar el cliente de App-V o de App-V RDS.</span><span class="sxs-lookup"><span data-stu-id="56c5f-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-177">Consulta <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> cómo implementar el cliente de App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="56c5f-178">Comprobar las claves del registro antes de instalar el servidor de App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="56c5f-179">Este es el paso 3 de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="56c5f-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="56c5f-180">Cuando se requiera este paso</span><span class="sxs-lookup"><span data-stu-id="56c5f-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-181">Está actualizando desde App-V SP1 con cualquier paquete posterior de revisiones que haya instalado con un archivo. msp.</span><span class="sxs-lookup"><span data-stu-id="56c5f-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="56c5f-182">¿Qué componentes requieren que realice este paso?</span><span class="sxs-lookup"><span data-stu-id="56c5f-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-183">Solo los componentes de servidor de App-V que está actualizando.</span><span class="sxs-lookup"><span data-stu-id="56c5f-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="56c5f-184">Cuando tenga que realizar este paso</span><span class="sxs-lookup"><span data-stu-id="56c5f-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-185">Antes de actualizar el servidor de App-V a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="56c5f-186">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="56c5f-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-187">Con la información de las tablas siguientes, actualice cada valor de la clave del registro en <code>HKLM\Software\Microsoft\AppV\Server</code> con el valor que proporcionó en la instalación del servidor original.</span><span class="sxs-lookup"><span data-stu-id="56c5f-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="56c5f-188">Al completar este paso, se restauran los valores del registro que pueden haberse eliminado cuando se instalaron paquetes de Hotfix de App-V SP1.</span><span class="sxs-lookup"><span data-stu-id="56c5f-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="56c5f-189">Tecla ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="56c5f-189">ManagementDatabase key</span></span>**

<span data-ttu-id="56c5f-190">Si está instalando la base de datos de administración, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="56c5f-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-191">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="56c5f-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="56c5f-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="56c5f-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-194">Describe si se necesita una cuenta de acceso público para obtener acceso a bases de datos de administración no locales.</span><span class="sxs-lookup"><span data-stu-id="56c5f-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="56c5f-195">El valor se establece en "1" si es necesario.</span><span class="sxs-lookup"><span data-stu-id="56c5f-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="56c5f-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-197">Nombre de la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-199">Cuenta usada para el acceso de lectura (público) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="56c5f-200">Se usa cuando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="56c5f-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="56c5f-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-202">Identificador seguro (SID) de la cuenta usada para el acceso de lectura (público) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="56c5f-203">Se usa cuando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="56c5f-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="56c5f-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-205">Instancia de SQL Server para la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="56c5f-206">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="56c5f-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-208">Cuenta usada para el acceso de escritura (Administrador) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="56c5f-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-210">Identificador seguro (SID) de la cuenta usada para el acceso de escritura (Administrador) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-212">Cuenta de equipo remoto de Management Server (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="56c5f-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-214">Inicio de sesión del administrador de instalación del servidor de administración (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="56c5f-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="56c5f-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-216">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="56c5f-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="56c5f-217">1 </strong> : el servicio de administración está en el equipo local, es decir, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está en blanco.</span><span class="sxs-lookup"><span data-stu-id="56c5f-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="56c5f-218">0 </strong> - el servicio de administración está en un equipo diferente del equipo local.</span><span class="sxs-lookup"><span data-stu-id="56c5f-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="56c5f-219">Tecla ManagementService</span><span class="sxs-lookup"><span data-stu-id="56c5f-219">ManagementService key</span></span>**

<span data-ttu-id="56c5f-220">Si va a instalar el servidor de administración, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="56c5f-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-221">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="56c5f-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="56c5f-222">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-224">Grupo o cuenta de servicios de dominio de Active Directory (AD DS) que tiene autorización para administrar App-V (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="56c5f-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="56c5f-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-226">Instancia de SQL Server que contiene la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="56c5f-227">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="56c5f-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="56c5f-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-229">Nombre del servidor SQL Server remoto con la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="56c5f-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="56c5f-230">Si el valor está en blanco, se usa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="56c5f-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="56c5f-231">Tecla ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="56c5f-231">ReportingDatabase key</span></span>**

<span data-ttu-id="56c5f-232">Si va a instalar la base de datos de informes, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="56c5f-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-233">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="56c5f-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="56c5f-234">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="56c5f-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-236">Describe si se necesita una cuenta de acceso público para acceder a bases de datos de informes no locales.</span><span class="sxs-lookup"><span data-stu-id="56c5f-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="56c5f-237">El valor se establece en "1" si es necesario.</span><span class="sxs-lookup"><span data-stu-id="56c5f-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="56c5f-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-239">Nombre de la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="56c5f-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-241">Cuenta usada para el acceso de lectura (público) a la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="56c5f-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="56c5f-242">Se usa cuando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="56c5f-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="56c5f-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-244">Identificador seguro (SID) de la cuenta usada para el acceso de lectura (público) a la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="56c5f-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="56c5f-245">Se usa cuando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="56c5f-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="56c5f-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-247">Instancia de SQL Server para la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="56c5f-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="56c5f-248">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="56c5f-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="56c5f-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-252">Cuenta de servidor de informes remoto (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="56c5f-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="56c5f-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-254">Inicio de sesión del administrador de instalación para el servidor de informes (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="56c5f-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="56c5f-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-256">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="56c5f-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="56c5f-257">1 </strong> : el servicio de informes está en el equipo local, es decir, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está en blanco.</span><span class="sxs-lookup"><span data-stu-id="56c5f-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="56c5f-258">0 </strong> - el servicio de informes está en un equipo diferente del equipo local.</span><span class="sxs-lookup"><span data-stu-id="56c5f-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="56c5f-259">Tecla ReportingService</span><span class="sxs-lookup"><span data-stu-id="56c5f-259">ReportingService key</span></span>**

<span data-ttu-id="56c5f-260">Si va a instalar el servidor de informes, establezca estas claves del registro en `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="56c5f-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-261">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="56c5f-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="56c5f-262">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="56c5f-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-264">Instancia de SQL Server para la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="56c5f-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="56c5f-265">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="56c5f-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="56c5f-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-267">Nombre del servidor SQL Server remoto con la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="56c5f-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="56c5f-268">Si el valor está en blanco, se usa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="56c5f-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="56c5f-269">El archivo XML del grupo de conexiones creado manualmente requiere actualizar al esquema</span><span class="sxs-lookup"><span data-stu-id="56c5f-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="56c5f-270">Si va a crear manualmente el archivo XML del grupo de conexión y desea usar las nuevas características "paquetes opcionales" y "usar cualquier versión" que se describen en [mejoras en los grupos de conexión](#bkmk-cg-improvements), debe especificar el esquema siguiente en el archivo XML:</span><span class="sxs-lookup"><span data-stu-id="56c5f-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="56c5f-271">Para obtener ejemplos y más información, consulte [acerca del archivo de grupo de conexión](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="56c5f-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="56c5f-272">Mejoras en los grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-272">Improvements to connection groups</span></span>


<span data-ttu-id="56c5f-273">Puede administrar grupos de conexión más fácilmente mediante paquetes opcionales y otras mejoras que se hayan agregado en App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="56c5f-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="56c5f-274">En la tabla siguiente se resumen las tareas que puede realizar con las nuevas características del grupo de conexiones, así como vínculos a información más detallada sobre cada tarea.</span><span class="sxs-lookup"><span data-stu-id="56c5f-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-275">Tarea/característica</span><span class="sxs-lookup"><span data-stu-id="56c5f-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="56c5f-276">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-276">Description</span></span></th>
<th align="left"><span data-ttu-id="56c5f-277">Vínculos a más información</span><span class="sxs-lookup"><span data-stu-id="56c5f-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-278">Habilitar un grupo de conexiones para incluir paquetes opcionales</span><span class="sxs-lookup"><span data-stu-id="56c5f-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-279">Incluir paquetes opcionales en un grupo de conexión le permite determinar de forma dinámica qué aplicaciones se incluirán en el entorno virtual del grupo de conexión, en función de las aplicaciones a las que tengan derecho los usuarios.</span><span class="sxs-lookup"><span data-stu-id="56c5f-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="56c5f-280">No es necesario administrar tantos grupos de conexión porque se pueden mezclar paquetes opcionales y no opcionales en el mismo grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="56c5f-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="56c5f-281">La combinación de paquetes permite que diferentes grupos de usuarios utilicen el mismo grupo de conexiones, aunque los usuarios solo tengan un paquete en común.</span><span class="sxs-lookup"><span data-stu-id="56c5f-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="56c5f-282">Ejemplo </strong> : puede habilitar un paquete con Microsoft Office para todos los usuarios, pero habilitar diferentes paquetes opcionales, que contienen distintos complementos de Office, a distintos subconjuntos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="56c5f-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="56c5f-283">Cómo usar los paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-284">Anular la publicación o la eliminación de un paquete opcional sin cambiar el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-285">Puede anular la publicación o la eliminación o la anulación de la publicación de un paquete opcional, que se encuentra en un grupo de conexión, sin tener que deshabilitar o volver a habilitar el grupo de conexión en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="56c5f-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="56c5f-286">Cómo usar los paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-287">Publicar grupos de conexión que contengan paquetes publicados de forma global y publicados por el usuario</span><span class="sxs-lookup"><span data-stu-id="56c5f-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-288">Cree un grupo de conexiones publicado por el usuario que contenga paquetes publicados de forma global y publicadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="56c5f-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="56c5f-289">Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente</span><span class="sxs-lookup"><span data-stu-id="56c5f-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-290">Hacer que un grupo de conexiones omita la versión del paquete</span><span class="sxs-lookup"><span data-stu-id="56c5f-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-291">Configure un grupo de conexión para que acepte cualquier versión de un paquete, lo que le permite actualizar un paquete sin tener que deshabilitar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="56c5f-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="56c5f-292">Además, si hay un paquete opcional con una versión incorrecta en el grupo de conexión, el paquete se pasa por alto y no bloqueará el entorno virtual del grupo de conexión para que no se cree.</span><span class="sxs-lookup"><span data-stu-id="56c5f-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="56c5f-293">Cómo hacer que un grupo de conexión ignore la versión del paquete</span><span class="sxs-lookup"><span data-stu-id="56c5f-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-294">Limitar las capacidades de publicación de los usuarios finales</span><span class="sxs-lookup"><span data-stu-id="56c5f-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-295">Habilite solo administradores (no usuarios finales) para publicar paquetes y para habilitar grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="56c5f-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-296">Para obtener información acerca de los grupos de conexión, consulte <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> Cómo permitir que solo los administradores puedan habilitar grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="56c5f-297">Para obtener información sobre los paquetes, consulte los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="56c5f-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-298">Método</span><span class="sxs-lookup"><span data-stu-id="56c5f-298">Method</span></span></th>
<th align="left"><span data-ttu-id="56c5f-299">Vínculo a más información</span><span class="sxs-lookup"><span data-stu-id="56c5f-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-300">Consola de administración</span><span class="sxs-lookup"><span data-stu-id="56c5f-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="56c5f-301">Cómo publicar un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="56c5f-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="56c5f-303">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-304">Sistema de entrega electrónica de software de terceros</span><span class="sxs-lookup"><span data-stu-id="56c5f-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="56c5f-305">Cómo habilitar solo a los administradores para publicar paquetes mediante una ESD</span><span class="sxs-lookup"><span data-stu-id="56c5f-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-306">Habilitar o deshabilitar un grupo de conexiones para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="56c5f-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-307">Los administradores pueden habilitar o deshabilitar un grupo de conexiones para un usuario específico mediante el <strong> parámetro opcional-UserSID </strong> con los siguientes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="56c5f-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="56c5f-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="56c5f-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="56c5f-309">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="56c5f-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="56c5f-310">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-311">Combinación de rutas de paquetes idénticas en un directorio virtual de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-312">Si dos o más paquetes de un grupo de conexiones contienen rutas de directorio idénticas, las rutas se combinan en un único directorio virtual dentro del entorno virtual del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="56c5f-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="56c5f-313">Esta combinación de rutas permite que una aplicación de un paquete tenga acceso a los archivos de un paquete diferente.</span><span class="sxs-lookup"><span data-stu-id="56c5f-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="56c5f-314">Información acerca del entorno virtual del grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="56c5f-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="56c5f-315">Los administradores pueden publicar y anular la publicación de paquetes para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="56c5f-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="56c5f-316">Los administradores pueden usar los siguientes cmdlets para publicar o anular la publicación de paquetes para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="56c5f-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="56c5f-317">Para usar los cmdlets, escriba el parámetro **– UserSID** seguido del identificador de seguridad (SID) del usuario.</span><span class="sxs-lookup"><span data-stu-id="56c5f-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="56c5f-318">Para más información, consulta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56c5f-318">For more information, see:</span></span>

-   [<span data-ttu-id="56c5f-319">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="56c5f-320">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-321">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="56c5f-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="56c5f-322">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56c5f-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-323">Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="56c5f-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-324">Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="56c5f-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-325">Anulación de la publicación-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="56c5f-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-326">Unpublishing-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="56c5f-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="56c5f-327">Habilitar solo los administradores para publicar y anular la publicación de paquetes</span><span class="sxs-lookup"><span data-stu-id="56c5f-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="56c5f-328">Puede habilitar solo administradores (no usuarios finales) para publicar y anular la publicación de paquetes mediante uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="56c5f-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-329">Método</span><span class="sxs-lookup"><span data-stu-id="56c5f-329">Method</span></span></th>
<th align="left"><span data-ttu-id="56c5f-330">Más información</span><span class="sxs-lookup"><span data-stu-id="56c5f-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-331">Configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="56c5f-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-332">Desplácese hasta el nodo de objeto de directiva de grupo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56c5f-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="56c5f-333">&gt;Directivas de configuración &gt; del equipo Plantillas administrativas &gt; del sistema &gt; App-V &gt; Publishing </strong> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="56c5f-334">Habilite la <strong> configuración de directiva de grupo requerir publicación como administrador </strong> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="56c5f-336">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="56c5f-337">La clave de registro RunVirtual admite paquetes que se publican para el usuario</span><span class="sxs-lookup"><span data-stu-id="56c5f-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="56c5f-338">App-V 5,0 SP3 agrega compatibilidad con el uso de la clave de registro **RunVirtual** con aplicaciones virtualizadas que se encuentran en paquetes publicados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="56c5f-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="56c5f-339">La clave de registro **RunVirtual** le permite ejecutar una aplicación instalada de forma local en un entorno virtual, junto con las aplicaciones que se han virtualizado mediante App-V.</span><span class="sxs-lookup"><span data-stu-id="56c5f-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="56c5f-340">Anteriormente, las aplicaciones virtualizadas de los paquetes de App-V tenían que publicarse globalmente.</span><span class="sxs-lookup"><span data-stu-id="56c5f-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="56c5f-341">Para obtener más información sobre **RunVirtual** y sobre otros métodos de ejecución de aplicaciones instaladas localmente en un entorno virtual con aplicaciones virtualizadas, vea [ejecutar una aplicación instalada de forma local dentro de un entorno virtual con aplicaciones virtualizadas](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="56c5f-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="56c5f-342">Nuevos cmdlets de PowerShell y ayuda para cmdlet actualizable</span><span class="sxs-lookup"><span data-stu-id="56c5f-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="56c5f-343">Los nuevos cmdlets de PowerShell y la ayuda actualizable del cmdlet se incluyen en App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="56c5f-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="56c5f-344">Para descargar los módulos del cmdlet, vea [Cómo cargar los cmdlets de PowerShell y obtener ayuda para el cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span><span class="sxs-lookup"><span data-stu-id="56c5f-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="56c5f-345">Nuevos cmdlets de PowerShell de App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="56c5f-346">Se han agregado nuevos cmdlets de Windows PowerShell para el servidor de App-V para ayudarle a administrar los grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="56c5f-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-347">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="56c5f-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="56c5f-348">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-349">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="56c5f-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-350">Anexa un paquete al final de un grupo de conexiones&#39;s lista de paquetes y le permite configurar el paquete como opcional o sin ninguna versión dentro del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="56c5f-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-351">Set-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="56c5f-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-352">Permite modificar los detalles sobre el paquete de grupo de conexión, por ejemplo, si es opcional.</span><span class="sxs-lookup"><span data-stu-id="56c5f-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-353">Remove-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="56c5f-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-354">Quita un paquete de un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="56c5f-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="56c5f-355">Obtener ayuda para los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="56c5f-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="56c5f-356">La ayuda de cmdlet está disponible en los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="56c5f-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-357">Formato</span><span class="sxs-lookup"><span data-stu-id="56c5f-357">Format</span></span></th>
<th align="left"><span data-ttu-id="56c5f-358">Descripción</span><span class="sxs-lookup"><span data-stu-id="56c5f-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-359">Como módulo descargable</span><span class="sxs-lookup"><span data-stu-id="56c5f-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-360">Para obtener la ayuda más reciente, después de descargar el módulo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56c5f-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="56c5f-361">Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="56c5f-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="56c5f-362">Escriba uno de los siguientes comandos para cargar los cmdlets para el módulo que desee:</span><span class="sxs-lookup"><span data-stu-id="56c5f-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-363">Componente de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="56c5f-364">Comando para escribir</span><span class="sxs-lookup"><span data-stu-id="56c5f-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-365">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-366">Update-Help-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="56c5f-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-367">Secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-368">Update-Help-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="56c5f-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-369">Cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-370">Update-Help-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="56c5f-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-371">En TechNet como páginas web</span><span class="sxs-lookup"><span data-stu-id="56c5f-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-372">Consulte el nodo App-V en la <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automatización de Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="56c5f-373">Para obtener más información, vea [Cómo cargar los cmdlets de PowerShell y obtener ayuda para el cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span><span class="sxs-lookup"><span data-stu-id="56c5f-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="56c5f-374">El directorio principal de la aplicación virtual (PVAD) está oculto pero puede activarse</span><span class="sxs-lookup"><span data-stu-id="56c5f-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="56c5f-375">El directorio principal de la aplicación virtual (PVAD) está oculto en App-V 5,0 SP3, pero puede volver a activarlo y hacerlo visible mediante uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="56c5f-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-376">Método</span><span class="sxs-lookup"><span data-stu-id="56c5f-376">Method</span></span></th>
<th align="left"><span data-ttu-id="56c5f-377">Pasos</span><span class="sxs-lookup"><span data-stu-id="56c5f-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56c5f-378">Usar un parámetro de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="56c5f-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="56c5f-379">Pase el <strong> parámetro-EnablePVADControl </strong> al <strong>Sequencer.exe</strong> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56c5f-380">Crear una subclave del registro</span><span class="sxs-lookup"><span data-stu-id="56c5f-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="56c5f-381">En el editor del registro, vaya a:</span><span class="sxs-lookup"><span data-stu-id="56c5f-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="56c5f-382">Nota</span><span class="sxs-lookup"><span data-stu-id="56c5f-382">Note</span></span></strong><br/><p><span data-ttu-id="56c5f-383">Si la <code>Compatibility</code> subclave no existe, debe crearla.</span><span class="sxs-lookup"><span data-stu-id="56c5f-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="56c5f-384">Cree un valor DWORD denominado <strong> EnablePVADControl </strong> y establezca el valor en <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="56c5f-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="56c5f-385">Un valor de <strong> 0 </strong> significa que PVAD está oculto.</span><span class="sxs-lookup"><span data-stu-id="56c5f-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="56c5f-386">**Más información sobre PVAD:** Al usar el secuenciador para crear un paquete, puede especificar cualquier ruta de instalación para el paquete.</span><span class="sxs-lookup"><span data-stu-id="56c5f-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="56c5f-387">En versiones anteriores de App-V, se necesitaba especificar el directorio principal de la aplicación virtual (PVAD) de la aplicación como la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="56c5f-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="56c5f-388">PVAD es el directorio en el que normalmente instalaría una aplicación en el equipo local si no estaba usando App-V.</span><span class="sxs-lookup"><span data-stu-id="56c5f-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="56c5f-389">Por ejemplo, si está instalando Office en un equipo, el PVAD normalmente sería C:\\Archivos de Programa\\microsoft Office\\.</span><span class="sxs-lookup"><span data-stu-id="56c5f-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="56c5f-390">ClientVersion es necesario para ver los metadatos de publicación de App-V</span><span class="sxs-lookup"><span data-stu-id="56c5f-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="56c5f-391">En App-V 5,0 SP3, debe proporcionar los siguientes valores en la dirección al consultar el servidor de publicación de App-V para obtener metadatos:</span><span class="sxs-lookup"><span data-stu-id="56c5f-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56c5f-392">Valor</span><span class="sxs-lookup"><span data-stu-id="56c5f-392">Value</span></span></th>
<th align="left"><span data-ttu-id="56c5f-393">Detalles adicionales</span><span class="sxs-lookup"><span data-stu-id="56c5f-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="56c5f-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="56c5f-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-395">Si omite el <strong> parámetro ClientVersion </strong> de la consulta, los metadatos excluyen las nuevas características de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="56c5f-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="56c5f-396">Clientes</span><span class="sxs-lookup"><span data-stu-id="56c5f-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="56c5f-397">Solo tiene que proporcionar este valor si selecciona sistemas operativos cliente específicos al realizar la secuencia del paquete.</span><span class="sxs-lookup"><span data-stu-id="56c5f-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="56c5f-398">Si selecciona el valor predeterminado (todos los sistemas operativos), no especifique este valor en la consulta.</span><span class="sxs-lookup"><span data-stu-id="56c5f-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="56c5f-399">Si omite el <strong> </strong> parámetro de los clientes de la consulta, solo los paquetes que se secuenciaron para admitir cualquier sistema operativo aparecerán en los metadatos.</span><span class="sxs-lookup"><span data-stu-id="56c5f-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="56c5f-400">En la sintaxis y los ejemplos de esta consulta, consulte [visualización de metadatos de publicación de servidor de App-V](viewing-app-v-server-publishing-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="56c5f-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="56c5f-401">Los registros de eventos de App-V se han consolidado</span><span class="sxs-lookup"><span data-stu-id="56c5f-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="56c5f-402">Los siguientes registros de eventos, que se han ubicado anteriormente en \*\*registros de aplicaciones y servicios/Microsoft/appv/ &lt; App-V &gt; \*\*, se han movido a registros de **aplicaciones y servicios/Microsoft/appv/ServiceLog**.</span><span class="sxs-lookup"><span data-stu-id="56c5f-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="56c5f-403">Para ver los registros, seleccione **Ver** los &gt; **registros analíticos y de depuración** en la aplicación Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="56c5f-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="56c5f-404">Cliente-cliente de catálogo: cliente de integración-cliente de orquestación-cliente de PackageConfig-scripting Client-cliente de servicio-Vemgr cliente-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-subsistemas de ActiveX-AppPath Subsystems-FTA</span><span class="sxs-lookup"><span data-stu-id="56c5f-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="56c5f-405">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="56c5f-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="56c5f-406">App-V es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="56c5f-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="56c5f-407">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="56c5f-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="56c5f-408">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049)</span><span class="sxs-lookup"><span data-stu-id="56c5f-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="56c5f-409">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56c5f-409">Related topics</span></span>


[<span data-ttu-id="56c5f-410">Notas de la versión de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="56c5f-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)









