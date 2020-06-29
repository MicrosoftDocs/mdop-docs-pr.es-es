---
title: Cómo implementar el cliente de App-V
description: Cómo implementar el cliente de App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814126"
---
# <span data-ttu-id="82e1f-103">Cómo implementar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="82e1f-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="82e1f-104">Use el siguiente procedimiento para instalar el cliente de Microsoft Application Virtualization (App-V) 5,1 y el cliente de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="82e1f-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="82e1f-105">Debe instalar la versión del cliente que se corresponda con el sistema operativo del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="82e1f-106">Qué hacer antes de empezar</span><span class="sxs-lookup"><span data-stu-id="82e1f-106">What to do before you start</span></span>**

1. <span data-ttu-id="82e1f-107">Revise e instale los requisitos previos de software:</span><span class="sxs-lookup"><span data-stu-id="82e1f-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="82e1f-108">Instale el software necesario que corresponde a la versión de la aplicación de App-V que está instalando:</span><span class="sxs-lookup"><span data-stu-id="82e1f-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="82e1f-109">Acerca de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82e1f-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="82e1f-110">Requisitos previos de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82e1f-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="82e1f-111">Revise la coexistencia del cliente y los escenarios no admitidos, como se aplica a la instalación:</span><span class="sxs-lookup"><span data-stu-id="82e1f-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-112">Implementación de clientes de App-V coexistentes</span><span class="sxs-lookup"><span data-stu-id="82e1f-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="82e1f-113">Planificación de la implementación del cliente y del secuenciador de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82e1f-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-114">Escenarios de instalación no compatibles o limitadas</span><span class="sxs-lookup"><span data-stu-id="82e1f-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-115">Consulte la sección cliente en las <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configuraciones admitidas de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82e1f-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="82e1f-116">Revise las ubicaciones de información del registro del cliente, registro y solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="82e1f-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82e1f-117">Información del registro del cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="82e1f-118">De forma predeterminada, después de instalar el cliente de App-V 5,1, la información del cliente se almacena en el registro, en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="82e1f-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="82e1f-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENTE</span><span class="sxs-lookup"><span data-stu-id="82e1f-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="82e1f-120">Al implementar un paquete virtualizado en un equipo que ejecuta el cliente de App-V, los datos del paquete asociado se almacenan en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="82e1f-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="82e1f-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="82e1f-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="82e1f-122">Sin embargo, puede volver a configurar esta ubicación con la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="82e1f-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="82e1f-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="82e1f-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82e1f-124">Archivos de registro de cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="82e1f-125">Para obtener información sobre el archivo de registro asociada con el cliente de App-V 5,1, busque en el siguiente registro:</span><span class="sxs-lookup"><span data-stu-id="82e1f-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="82e1f-126">Registros de eventos/aplicaciones y servicios/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="82e1f-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="82e1f-127">En App-V 5,0 SP3, algunos registros se consolidaron y se movieron a la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="82e1f-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="82e1f-128">Registros de eventos, registros de aplicaciones y servicios/Microsoft/AppV/ServiceLog</span><span class="sxs-lookup"><span data-stu-id="82e1f-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="82e1f-129">Para obtener una lista de los registros que se han movido, consulte <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> acerca de App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="82e1f-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="82e1f-130">Los paquetes que se encuentran almacenados en los equipos que ejecutan el cliente de App-V 5,1 se guardan en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="82e1f-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="82e1f-131">C:\ProgramData\App-V &amp; lt; identificador de paquete &gt; &amp; lt; identificador de versión&gt;</span><span class="sxs-lookup"><span data-stu-id="82e1f-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82e1f-132">Información para la solución de problemas de instalación del cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="82e1f-133">Consulte el registro de errores en la <strong> carpeta% Temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="82e1f-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="82e1f-134">Para revisar los archivos de registro, haga clic en <strong> Inicio </strong> , escriba <strong> % temp% </strong> y, a continuación, busque el <strong> registro de appv_ </strong> .</span><span class="sxs-lookup"><span data-stu-id="82e1f-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="82e1f-135">Para instalar el cliente de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82e1f-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="82e1f-136">Copie el archivo de instalación del cliente App-V 5,1 en el equipo en el que se instalará.</span><span class="sxs-lookup"><span data-stu-id="82e1f-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="82e1f-137">Elija entre los siguientes tipos de cliente:</span><span class="sxs-lookup"><span data-stu-id="82e1f-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="82e1f-138">Tipo de cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="82e1f-139">Archivo para usar</span><span class="sxs-lookup"><span data-stu-id="82e1f-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="82e1f-140">Versión estándar del cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="82e1f-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="82e1f-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="82e1f-142">Versión de servicios de escritorio remoto del cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="82e1f-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="82e1f-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="82e1f-144">Haga doble clic en el archivo de instalación y haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="82e1f-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="82e1f-145">Antes de comenzar la instalación, el instalador comprueba si el equipo tiene [requisitos previos de App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="82e1f-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="82e1f-146">Revise y acepte los términos de licencia del software, elija si desea usar Microsoft Update y si desea participar en el programa para la mejora de la experiencia del usuario de Microsoft, y haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="82e1f-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="82e1f-147">En la página la **configuración se completó correctamente** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="82e1f-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="82e1f-148">La instalación crea las siguientes entradas para el cliente App-V en los **programas**:</span><span class="sxs-lookup"><span data-stu-id="82e1f-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="82e1f-149">.exe</span><span class="sxs-lookup"><span data-stu-id="82e1f-149">.exe</span></span>**

    -   **<span data-ttu-id="82e1f-150">.msi</span><span class="sxs-lookup"><span data-stu-id="82e1f-150">.msi</span></span>**

    -   **<span data-ttu-id="82e1f-151">paquete de idioma</span><span class="sxs-lookup"><span data-stu-id="82e1f-151">language pack</span></span>**

        **<span data-ttu-id="82e1f-152">Nota</span><span class="sxs-lookup"><span data-stu-id="82e1f-152">Note</span></span>**  
        <span data-ttu-id="82e1f-153">Después de la instalación, solo se puede desinstalar el archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="82e1f-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="82e1f-154">Para instalar el cliente de App-V 5,1 con un script</span><span class="sxs-lookup"><span data-stu-id="82e1f-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="82e1f-155">Instale todo el software necesario necesario en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="82e1f-156">Consulte [Qué hacer antes de empezar](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="82e1f-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="82e1f-157">Si instala el cliente con un archivo. msi, se producirá un error en la instalación si falta alguno de los requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="82e1f-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="82e1f-158">Para usar un script para instalar el cliente de App-V 5,1, use los siguientes parámetros con **appv\_client\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="82e1f-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="82e1f-159">Nota</span><span class="sxs-lookup"><span data-stu-id="82e1f-159">Note</span></span>**  
   <span data-ttu-id="82e1f-160">El instalador de Windows (. msi) cliente admite el mismo conjunto de conmutadores, excepto el parámetro **/log** .</span><span class="sxs-lookup"><span data-stu-id="82e1f-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="82e1f-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-162">Especifica el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="82e1f-162">Specifies the installation directory.</span></span> <span data-ttu-id="82e1f-163">Ejemplo de uso: <strong> /INSTALLDIR = c:\Archivos de Files\AppV Client</span><span class="sxs-lookup"><span data-stu-id="82e1f-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="82e1f-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-165">Permite la participación en el programa para la mejora de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="82e1f-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="82e1f-166">Ejemplo de uso: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="82e1f-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-168">Habilita Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="82e1f-168">Enables Microsoft Update.</span></span> <span data-ttu-id="82e1f-169">Ejemplo de uso: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-170">/PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="82e1f-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-171">Especifica el directorio en el que se instalarán todas las nuevas aplicaciones y actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="82e1f-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="82e1f-172">Ejemplo de uso: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\App-V packages&#39;</span><span class="sxs-lookup"><span data-stu-id="82e1f-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="82e1f-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-174">Invalida la ubicación de origen para descargar el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="82e1f-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="82e1f-175">Ejemplo de uso: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="82e1f-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="82e1f-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-177">Especifica cómo se cargarán los nuevos paquetes por App-V 5,1 en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="82e1f-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="82e1f-178">Las siguientes opciones están habilitadas: [1]; cargar automáticamente todos los paquetes [2]; o no carga automáticamente paquetes [0]. <strong> Ejemplo de uso:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="82e1f-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="82e1f-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-180">Especifica que el contenido del paquete transmitido no se guardará en el disco duro local.</span><span class="sxs-lookup"><span data-stu-id="82e1f-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="82e1f-181">Ejemplo de uso: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="82e1f-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-183">Permite que el cliente de App-V 5,1 modifique los accesos directos y los FTAs asociados a los paquetes creados con una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="82e1f-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="82e1f-184">Ejemplo de uso: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="82e1f-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-186">Habilita los scripts que se definen en el archivo de manifiesto del paquete o los archivos de configuración que se deben ejecutar.</span><span class="sxs-lookup"><span data-stu-id="82e1f-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="82e1f-187">Ejemplo de uso: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="82e1f-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-189">Especifica las rutas de registro que no se transferirán a un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="82e1f-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="82e1f-190">Ejemplo de uso: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="82e1f-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="82e1f-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-192">Especifica las rutas de archivo relativas a% userprofile% que no se mueven con un perfil de usuario&#39;s.</span><span class="sxs-lookup"><span data-stu-id="82e1f-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="82e1f-193">Ejemplo de uso: <strong> /ROAMINGFILEEXCLUSIONS &#39;escritorio; mis imágenes&#39;</span><span class="sxs-lookup"><span data-stu-id="82e1f-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="82e1f-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-195">Muestra el nombre del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="82e1f-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="82e1f-196">Ejemplo de uso: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="82e1f-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="82e1f-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-198">Muestra la dirección URL del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="82e1f-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="82e1f-199">Ejemplo de uso: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="82e1f-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="82e1f-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-201">Habilita una actualización de publicación global.</span><span class="sxs-lookup"><span data-stu-id="82e1f-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="82e1f-202">Ejemplo de uso: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="82e1f-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-204">Inicia una actualización de publicación global cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="82e1f-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="82e1f-205">Ejemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="82e1f-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-207">Especifica el intervalo de actualización de la publicación, donde <strong> 0 </strong> indica que no se actualiza periódicamente.</span><span class="sxs-lookup"><span data-stu-id="82e1f-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="82e1f-208">Ejemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="82e1f-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="82e1f-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-210">Especifica la unidad de intervalo (horas [0], días [1]).</span><span class="sxs-lookup"><span data-stu-id="82e1f-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="82e1f-211">Ejemplo de uso: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="82e1f-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-213">Habilita la actualización de publicaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="82e1f-213">Enables user publishing refresh.</span></span> <span data-ttu-id="82e1f-214">Ejemplo de uso: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="82e1f-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-216">Inicia una actualización de publicación de usuario cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="82e1f-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="82e1f-217">Ejemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="82e1f-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-219">Especifica el intervalo de actualización de la publicación, donde <strong> 0 </strong> indica que no se actualiza periódicamente.</span><span class="sxs-lookup"><span data-stu-id="82e1f-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="82e1f-220">Ejemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="82e1f-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="82e1f-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-222">Especifica la unidad de intervalo (horas [0], días [1]).</span><span class="sxs-lookup"><span data-stu-id="82e1f-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="82e1f-223">Ejemplo de uso: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="82e1f-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-224">Log</span><span class="sxs-lookup"><span data-stu-id="82e1f-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-225">Especifica una ubicación donde se guarda la información del registro.</span><span class="sxs-lookup"><span data-stu-id="82e1f-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="82e1f-226">La ubicación predeterminada es% Temp%.</span><span class="sxs-lookup"><span data-stu-id="82e1f-226">The default location is %Temp%.</span></span> <span data-ttu-id="82e1f-227">Ejemplo de uso: <strong> /log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="82e1f-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-228">q</span><span class="sxs-lookup"><span data-stu-id="82e1f-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-229">Especifica una instalación desatendida.</span><span class="sxs-lookup"><span data-stu-id="82e1f-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-230">Pair</span><span class="sxs-lookup"><span data-stu-id="82e1f-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-231">Repara una instalación de cliente anterior.</span><span class="sxs-lookup"><span data-stu-id="82e1f-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="82e1f-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-233">Impide que el equipo se reinicie después de la instalación del cliente.</span><span class="sxs-lookup"><span data-stu-id="82e1f-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="82e1f-234">El parámetro impide que el equipo del usuario final se reinicie después de que se instalen las actualizaciones y le permite programar el reinicio cuando lo desee.</span><span class="sxs-lookup"><span data-stu-id="82e1f-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="82e1f-235">Por ejemplo, puede instalar App-V 5,1 y, a continuación, instalar el paquete de revisiones Y sin reiniciar después de la instalación del Service Pack.</span><span class="sxs-lookup"><span data-stu-id="82e1f-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="82e1f-236">Después de la instalación, debe reiniciar antes de empezar a usar App-V.</span><span class="sxs-lookup"><span data-stu-id="82e1f-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-237">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="82e1f-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-238">Desinstala el cliente.</span><span class="sxs-lookup"><span data-stu-id="82e1f-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="82e1f-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-240">Acepta el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="82e1f-240">Accepts the license agreement.</span></span> <span data-ttu-id="82e1f-241">Esto es necesario para una instalación desatendida.</span><span class="sxs-lookup"><span data-stu-id="82e1f-241">This is required for an unattended installation.</span></span> <span data-ttu-id="82e1f-242">Ejemplo de uso: <strong> /ACCEPTEULA </strong> o <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="82e1f-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="82e1f-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-244">Especifica la acción de diseño asociada.</span><span class="sxs-lookup"><span data-stu-id="82e1f-244">Specifies the associated layout action.</span></span> <span data-ttu-id="82e1f-245">También extrae los archivos de Windows Installer (. msi) y de script a una carpeta sin instalar App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82e1f-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="82e1f-246">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="82e1f-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="82e1f-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="82e1f-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-248">Especifica el directorio de diseño.</span><span class="sxs-lookup"><span data-stu-id="82e1f-248">Specifies the layout directory.</span></span> <span data-ttu-id="82e1f-249">Requiere un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="82e1f-249">Requires a string value.</span></span> <span data-ttu-id="82e1f-250">Ejemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualización de C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="82e1f-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="82e1f-251">/?,/h,/Help</span><span class="sxs-lookup"><span data-stu-id="82e1f-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="82e1f-252">Solicita ayuda acerca de los parámetros de instalación anteriores.</span><span class="sxs-lookup"><span data-stu-id="82e1f-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="82e1f-253">Para instalar el cliente de App-V 5,1 con el archivo de Windows Installer (. msi)</span><span class="sxs-lookup"><span data-stu-id="82e1f-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="82e1f-254">Instale los requisitos previos necesarios en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="82e1f-255">Consulte [Qué hacer antes de empezar](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="82e1f-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="82e1f-256">Si no se cumplen los requisitos previos, se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="82e1f-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="82e1f-257">Asegúrese de que los equipos de destino no tengan reinicios pendientes antes de instalar el cliente con los archivos App-V 5,1 Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="82e1f-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="82e1f-258">Los archivos de Windows Installer no marcan un reinicio pendiente.</span><span class="sxs-lookup"><span data-stu-id="82e1f-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="82e1f-259">Implemente uno de los siguientes archivos de Windows Installer en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="82e1f-260">El archivo que especifique debe coincidir con la configuración del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="82e1f-261">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="82e1f-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="82e1f-262">Implementar este archivo</span><span class="sxs-lookup"><span data-stu-id="82e1f-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="82e1f-263">El equipo está ejecutando un sistema operativo Microsoft Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="82e1f-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="82e1f-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="82e1f-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="82e1f-265">El equipo está ejecutando un sistema operativo Microsoft Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="82e1f-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="82e1f-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="82e1f-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="82e1f-267">Está implementando el cliente de servicios de escritorio remoto de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82e1f-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="82e1f-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="82e1f-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="82e1f-269">Con la información de la tabla siguiente, seleccione el paquete de idioma correspondiente **. msi** para instalar según el idioma que desee para el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="82e1f-270">La **xxxx** de la tabla se refiere a la configuración regional de destino del paquete de idioma.</span><span class="sxs-lookup"><span data-stu-id="82e1f-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="82e1f-271">Qué debe saber antes de empezar:</span><span class="sxs-lookup"><span data-stu-id="82e1f-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="82e1f-272">Los paquetes de idioma son comunes al cliente de App-V 5,1 estándar y a la versión de servicios de escritorio remoto del cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82e1f-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="82e1f-273">Si instala el cliente de App-V 5,1 con el **archivo. exe**, el instalador solo implementará el paquete de idioma que coincida con el sistema operativo que se ejecuta en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="82e1f-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="82e1f-274">Para implementar paquetes de idioma adicionales en un equipo de destino, use el procedimiento **para instalar el cliente de App-V 5,1 con el archivo de Windows Installer (. msi)**.</span><span class="sxs-lookup"><span data-stu-id="82e1f-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="82e1f-275">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="82e1f-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="82e1f-276">Implementar este archivo</span><span class="sxs-lookup"><span data-stu-id="82e1f-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="82e1f-277">El equipo está ejecutando un sistema operativo Microsoft Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="82e1f-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="82e1f-278">appv_client_LP_xxxx_ x86.msi</span><span class="sxs-lookup"><span data-stu-id="82e1f-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="82e1f-279">El equipo está ejecutando un sistema operativo Microsoft Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="82e1f-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="82e1f-280">appv_client_LP_xxxx_ x64.msi</span><span class="sxs-lookup"><span data-stu-id="82e1f-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="82e1f-281">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82e1f-281">Related topics</span></span>


[<span data-ttu-id="82e1f-282">Implementación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82e1f-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="82e1f-283">Información acerca de la configuración de cliente</span><span class="sxs-lookup"><span data-stu-id="82e1f-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="82e1f-284">Cómo desinstalar el cliente de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82e1f-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









