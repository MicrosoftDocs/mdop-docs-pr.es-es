---
title: Quitar las funciones o software de servidor MBAM
description: Quitar las funciones o software de servidor MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824980"
---
# <span data-ttu-id="206ab-103">Quitar las funciones o software de servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="206ab-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="206ab-104">Estas instrucciones explican cómo quitar el software y las características de administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="206ab-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="206ab-105">Si quita las características de MBAM Server, solo se quitan del servidor las características configuradas, no el software de servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="206ab-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="206ab-106">Si quita el software de servidor MBAM, se eliminarán el software y las características de MBAM Server que haya configurado en ese servidor.</span><span class="sxs-lookup"><span data-stu-id="206ab-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="206ab-107">**Nota:**  Para evitar la eliminación accidental de datos, MBAM no proporciona ningún mecanismo para quitar las bases de datos; debe hacerlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="206ab-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="206ab-108">Quitar las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="206ab-108">Removing MBAM Server features</span></span>


<span data-ttu-id="206ab-109">Puede usar cualquiera de los métodos siguientes para quitar las características de MBAM Server que haya configurado:</span><span class="sxs-lookup"><span data-stu-id="206ab-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="206ab-110">Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="206ab-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="206ab-111">Cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="206ab-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="206ab-112">Usar el Asistente para la configuración del servidor de MBAM para quitar características</span><span class="sxs-lookup"><span data-stu-id="206ab-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="206ab-113">Siga estas instrucciones para usar el Asistente para la configuración del servidor de MBAM para quitar las características de servidor de MBAM configuradas de un servidor.</span><span class="sxs-lookup"><span data-stu-id="206ab-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="206ab-114">Para quitar características de MBAM mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="206ab-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="206ab-115">En el servidor en el que desea quitar las características, seleccione **configuración del servidor de MBAM** para abrir el Asistente para la configuración.</span><span class="sxs-lookup"><span data-stu-id="206ab-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="206ab-116">Haga clic en **quitar características**, seleccione las características que desee quitar y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="206ab-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="206ab-117">Una página de **Resumen** muestra las características que seleccionó para la eliminación.</span><span class="sxs-lookup"><span data-stu-id="206ab-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="206ab-118">Haga clic en **quitar** para empezar a quitar las características y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="206ab-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="206ab-119">Usar Windows PowerShell para quitar características</span><span class="sxs-lookup"><span data-stu-id="206ab-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="206ab-120">Use los pasos siguientes como guía general para quitar características de MBAM Server mediante los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="206ab-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="206ab-121">Para quitar características de MBAM mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="206ab-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="206ab-122">Antes de quitar las características, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="206ab-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="206ab-123">Use los siguientes cmdlets para quitar las características del servidor de MBAM:</span><span class="sxs-lookup"><span data-stu-id="206ab-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="206ab-124">Disable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="206ab-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="206ab-125">Disable-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="206ab-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="206ab-126">Disable-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="206ab-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="206ab-127">Para obtener ayuda con los cmdlets de Windows PowerShell, escriba cmdlet **Get-Help** &lt; *cmdlet* &gt; o consulte la página de [automatización de Microsoft Desktop Optimization Pack con Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) para los cmdlets de Windows PowerShell de MBAM.</span><span class="sxs-lookup"><span data-stu-id="206ab-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="206ab-128">Quitar el software de servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="206ab-128">Removing MBAM Server software</span></span>


<span data-ttu-id="206ab-129">Siga estos pasos para quitar el software de servidor de MBAM y cualquier característica de MBAM Server que haya configurado en ese servidor.</span><span class="sxs-lookup"><span data-stu-id="206ab-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="206ab-130">Para quitar el software de servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="206ab-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="206ab-131">En el servidor en el que desea desinstalar el software de servidor MBAM, ejecute **MBAMserversetup.exe** para iniciar el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="206ab-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="206ab-132">Seleccione **desinstalar**y siga las indicaciones restantes para completar el proceso de desinstalación del software de servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="206ab-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="206ab-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="206ab-133">Related topics</span></span>


[<span data-ttu-id="206ab-134">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="206ab-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="206ab-135">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="206ab-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="206ab-136">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="206ab-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="206ab-137">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="206ab-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



