---
title: Instalación de software de servidor MBAM 2.5
description: Instalación de software de servidor MBAM 2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823391"
---
# <span data-ttu-id="caf28-103">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="caf28-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="caf28-104">En este tema se describe cómo instalar el software de servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 mediante el Asistente de configuración de administración y supervisión de Microsoft BitLocker o mediante parámetros de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="caf28-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="caf28-105">Repita el proceso de instalación del servidor para cada servidor en el que esté configurando las características de servidor de MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="caf28-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="caf28-106">Una vez finalizada la instalación, consulte Configuración de las [características de servidor de MBAM 2,5](configuring-the-mbam-25-server-features.md) para conocer los pasos para configurar las características de servidor.</span><span class="sxs-lookup"><span data-stu-id="caf28-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="caf28-107">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="caf28-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="caf28-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="caf28-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="caf28-109">Revisar la información de planificación de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="caf28-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="caf28-110">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="caf28-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="caf28-111">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="caf28-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="caf28-112">Arquitectura de alto nivel de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="caf28-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="caf28-113">Leer cómo obtener archivos de registro</span><span class="sxs-lookup"><span data-stu-id="caf28-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-114">De forma predeterminada, los archivos de registro se crean en la carpeta% Temp% del equipo local.</span><span class="sxs-lookup"><span data-stu-id="caf28-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="caf28-115">Para escribir los archivos de registro en una ubicación específica en lugar de en la <strong> carpeta% Temp </strong> %, use el <strong> </strong> &lt; <em> argumento/log ubicación </em> &gt; .</span><span class="sxs-lookup"><span data-stu-id="caf28-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="caf28-116">Es posible que se registren eventos adicionales en el visor de eventos de los <strong> nodos MBAM-Setup </strong> o <strong> MBAM-Web </strong> en <strong> las aplicaciones y servicios de &gt; Microsoft &gt; Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="caf28-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="caf28-117">Por ejemplo, Si desinstala MBAM, el desinstalador también desinstalará los registros MBAM-setup y MBAM-Web en EventViewer.</span><span class="sxs-lookup"><span data-stu-id="caf28-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="caf28-118">Instalar el software de servidor MBAM 2,5 con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="caf28-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="caf28-119">Siga estos pasos para instalar el software de servidor MBAM mediante el Asistente para la configuración de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="caf28-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="caf28-120">Para instalar el software de servidor MBAM 2,5 con el asistente</span><span class="sxs-lookup"><span data-stu-id="caf28-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="caf28-121">En el servidor en el que desea instalar MBAM, ejecute **MBAMserversetup.exe** para iniciar el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="caf28-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="caf28-122">En la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="caf28-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="caf28-123">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="caf28-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="caf28-124">Elija si desea usar Microsoft Update cuando busque actualizaciones y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="caf28-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="caf28-125">Elija si desea participar en el programa para la mejora de la experiencia del usuario y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="caf28-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="caf28-126">Para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="caf28-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="caf28-127">Para configurar las características de servidor cuando termine de instalarse el software del servidor MBAM, seleccione la casilla **ejecutar la configuración del servidor después de que se cierre el asistente** .</span><span class="sxs-lookup"><span data-stu-id="caf28-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="caf28-128">Como alternativa, puede configurar MBAM más adelante con el método abreviado de **configuración del servidor de MBAM** que la instalación del servidor crea en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="caf28-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="caf28-129">Haz clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="caf28-129">Click **Finish**.</span></span>

## <span data-ttu-id="caf28-130">Instalar el software de servidor MBAM 2,5 mediante una ventana de símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="caf28-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="caf28-131">En un símbolo del sistema, escriba un comando similar al siguiente para instalar el software de servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="caf28-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="caf28-132">En la siguiente tabla se describen los parámetros de la línea de comandos para instalar el software de servidor MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="caf28-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="caf28-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="caf28-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="caf28-134">Valor del parámetro</span><span class="sxs-lookup"><span data-stu-id="caf28-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="caf28-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="caf28-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="caf28-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="caf28-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-137">Verdadero falso</span><span class="sxs-lookup"><span data-stu-id="caf28-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-138">Participe en el programa de mejora de la experiencia del cliente, que ayuda a que Microsoft Identifique qué características de MBAM mejorar.</span><span class="sxs-lookup"><span data-stu-id="caf28-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="caf28-139">Falso: no participe en el programa de mejora de la experiencia del cliente.</span><span class="sxs-lookup"><span data-stu-id="caf28-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="caf28-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="caf28-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-141">Verdadero falso</span><span class="sxs-lookup"><span data-stu-id="caf28-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-142">True: Use Microsoft Update para mantener su equipo seguro y actualizado para Windows y otros productos de Microsoft, incluido MBAM.</span><span class="sxs-lookup"><span data-stu-id="caf28-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="caf28-143">Falso: no use Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="caf28-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="caf28-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="caf28-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-145">&lt;Ruta de acceso&gt;</span><span class="sxs-lookup"><span data-stu-id="caf28-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-146">Ubicación en la que desea instalar MBAM.</span><span class="sxs-lookup"><span data-stu-id="caf28-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="caf28-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="caf28-147">Example:</span></span></p>
<p><span data-ttu-id="caf28-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="caf28-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="caf28-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="caf28-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-150">Verdadero falso</span><span class="sxs-lookup"><span data-stu-id="caf28-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="caf28-151">True: continúa con el proceso de desinstalación de MBAM, incluso si no se pueden quitar las características.</span><span class="sxs-lookup"><span data-stu-id="caf28-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="caf28-152">Falso (valor predeterminado) si la acción personalizada de desinstalación no puede quitar una característica de servidor de MBAM agregada, se produce un error en la desinstalación y MBAM permanece instalado.</span><span class="sxs-lookup"><span data-stu-id="caf28-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="caf28-153">En ambos casos, cualquier característica que se haya eliminado correctamente durante el intento de desinstalar MBAM se mantendrá eliminada.</span><span class="sxs-lookup"><span data-stu-id="caf28-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="caf28-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="caf28-154">Related topics</span></span>


[<span data-ttu-id="caf28-155">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="caf28-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="caf28-156">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="caf28-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="caf28-157">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="caf28-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="caf28-158">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="caf28-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="caf28-159">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="caf28-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





