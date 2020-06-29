---
title: Cómo validar la instalación de MBAM con Administrador de configuración
description: Cómo validar la instalación de MBAM con Administrador de configuración
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822640"
---
# <span data-ttu-id="ad880-103">Cómo validar la instalación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="ad880-103">How to Validate the MBAM Installation with Configuration Manager</span></span>


<span data-ttu-id="ad880-104">Después de instalar administración y supervisión de Microsoft BitLocker (MBAM) con Configuration Manager, valide que la instalación haya configurado correctamente todas las características necesarias para MBAM completando los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="ad880-104">After installing Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, validate that the installation has successfully set up all the necessary features for MBAM by completing the following steps.</span></span>

**<span data-ttu-id="ad880-105">Para validar la instalación de características del servidor de MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ad880-105">To validate the MBAM Server feature installation with Configuration Manager</span></span>**

1.  <span data-ttu-id="ad880-106">En el servidor donde se implementa System Center Configuration Manager, abra el **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="ad880-106">On the server where System Center Configuration Manager is deployed, open **Control Panel**.</span></span> <span data-ttu-id="ad880-107">Seleccione el programa que se usa para desinstalar o cambiar un programa.</span><span class="sxs-lookup"><span data-stu-id="ad880-107">Select the program that is used to uninstall or change a program.</span></span> <span data-ttu-id="ad880-108">Compruebe que **Administración y supervisión de Microsoft BitLocker** aparece en la lista de programas y características.</span><span class="sxs-lookup"><span data-stu-id="ad880-108">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the list of programs and features.</span></span>

    <span data-ttu-id="ad880-109">**Nota:**  Para validar la instalación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="ad880-109">**Note** To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

     

2.  <span data-ttu-id="ad880-110">Use la consola del administrador de configuración para confirmar que se muestra una nueva colección denominada "MBAMs compatibles".</span><span class="sxs-lookup"><span data-stu-id="ad880-110">Use the Configuration Manager console to confirm that a new collection, called “MBAM Supported Computers,” is displayed.</span></span>

    <span data-ttu-id="ad880-111">Para ver la colección con Configuration Manager 2007: haga clic en **Site Database** ( &lt; **nombresitio** &gt;  -  &lt; **ServerName** &gt; , &lt; **siteName** &gt; ), **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="ad880-111">To view the collection with Configuration Manager 2007: Click **Site Database** (&lt;**SiteCode**&gt; - &lt;**ServerName**&gt;, &lt;**SiteName**&gt;), **Computer Management**.</span></span>

    <span data-ttu-id="ad880-112">Para ver la colección con SystemCenter2012 ConfigurationManager: haga clic en el área de trabajo de **activos fijos y cumplimiento** , **colecciones de dispositivos**.</span><span class="sxs-lookup"><span data-stu-id="ad880-112">To view the collection with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Device Collections**.</span></span>

3.  <span data-ttu-id="ad880-113">Use la consola del administrador de configuración para comprobar que los siguientes informes aparecen en la carpeta **MBAM** :</span><span class="sxs-lookup"><span data-stu-id="ad880-113">Use the Configuration Manager console to verify that the following reports are listed in the **MBAM** folder:</span></span>

    -   <span data-ttu-id="ad880-114">Cumplimiento de BitLocker Computer</span><span class="sxs-lookup"><span data-stu-id="ad880-114">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="ad880-115">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="ad880-115">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="ad880-116">Detalles de la compatibilidad con BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="ad880-116">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="ad880-117">Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="ad880-117">BitLocker Enterprise Compliance Summary</span></span>

    <span data-ttu-id="ad880-118">Para ver los informes con Configuration Manager 2007: haga clic en **informes**, **Reporting Services**, \ \ \ \ &lt; **nombreDeServidor** &gt; , **carpetas de informes**</span><span class="sxs-lookup"><span data-stu-id="ad880-118">To view the reports with Configuration Manager 2007: Click **Reporting**, **Reporting Services**, \\\\&lt;**ServerName**&gt;, **Report Folders**</span></span>

    <span data-ttu-id="ad880-119">Para ver los informes con SystemCenter2012 ConfigurationManager: haga clic en el área **de trabajo** **supervisión** , informes, **informes**.</span><span class="sxs-lookup"><span data-stu-id="ad880-119">To view the reports with SystemCenter2012 ConfigurationManager: Click the **Monitoring** workspace, **Reporting**, **Reports**.</span></span>

4.  <span data-ttu-id="ad880-120">Use la consola del administrador de configuración para confirmar que aparece la línea base de configuración "protección de BitLocker".</span><span class="sxs-lookup"><span data-stu-id="ad880-120">Use the Configuration Manager console to confirm that the configuration baseline “BitLocker Protection” is listed.</span></span>

    <span data-ttu-id="ad880-121">Para ver las líneas de base de configuración con el administrador de configuración 2007: haga clic en **Administración de configuración deseada**, **líneas base de configuración**.</span><span class="sxs-lookup"><span data-stu-id="ad880-121">To view the configuration baselines with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Baselines**.</span></span>

    <span data-ttu-id="ad880-122">Para ver las líneas de base de configuración con SystemCenter2012 ConfigurationManager: haga clic en el área de trabajo **activos y cumplimiento** , **configuración de cumplimiento**, **líneas de base de configuración**.</span><span class="sxs-lookup"><span data-stu-id="ad880-122">To view the configuration baselines with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Baselines**.</span></span>

5.  <span data-ttu-id="ad880-123">Use la consola del administrador de configuración para confirmar que se muestran los siguientes elementos de configuración nuevos:</span><span class="sxs-lookup"><span data-stu-id="ad880-123">Use the Configuration Manager console to confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="ad880-124">Protección de las unidades de datos fijas de BitLocker</span><span class="sxs-lookup"><span data-stu-id="ad880-124">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="ad880-125">Protección de unidades del sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="ad880-125">BitLocker Operating System Drive Protection</span></span>

    <span data-ttu-id="ad880-126">Para ver los elementos de configuración con Configuration Manager 2007: haga clic en administración de la **configuración deseada**, **elementos de configuración**.</span><span class="sxs-lookup"><span data-stu-id="ad880-126">To view the configuration items with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Items**.</span></span>

    <span data-ttu-id="ad880-127">Para ver los elementos de configuración con SystemCenter2012 ConfigurationManager: haga clic en el área de trabajo **activos y cumplimiento** , **configuración de cumplimiento**, **elementos de configuración**.</span><span class="sxs-lookup"><span data-stu-id="ad880-127">To view the configuration items with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Items**.</span></span>

## <span data-ttu-id="ad880-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad880-128">Related topics</span></span>


[<span data-ttu-id="ad880-129">Implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="ad880-129">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





