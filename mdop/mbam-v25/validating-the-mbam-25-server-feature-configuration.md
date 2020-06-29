---
title: Validación de la configuración de funciones de servidor de MBAM 2.5
description: Validación de la configuración de funciones de servidor de MBAM 2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827081"
---
# <span data-ttu-id="8ab0f-103">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8ab0f-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="8ab0f-104">Cuando finalice la implementación de características de administración y supervisión de Microsoft BitLocker (MBAM) 2,5, le recomendamos que valide la implementación para asegurarse de que todas las características se hayan configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="8ab0f-105">Use el procedimiento que coincida con la topología (integración independiente o de System Center Configuration Manager) que ha implementado.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="8ab0f-106">Validación de la implementación del servidor de MBAM con la topología independiente</span><span class="sxs-lookup"><span data-stu-id="8ab0f-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="8ab0f-107">Siga estos pasos para validar la implementación de su servidor de MBAM con la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="8ab0f-108">Para validar una implementación de servidor MBAM independiente</span><span class="sxs-lookup"><span data-stu-id="8ab0f-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="8ab0f-109">En cada servidor en el que se implemente una característica de MBAM, haga clic en **Panel de control** &gt; **programas** programas &gt; **y características**.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="8ab0f-110">Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .</span><span class="sxs-lookup"><span data-stu-id="8ab0f-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="8ab0f-111">Nota</span><span class="sxs-lookup"><span data-stu-id="8ab0f-111">Note</span></span>**  
    <span data-ttu-id="8ab0f-112">Para realizar la validación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="8ab0f-113">En el servidor donde está configurada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está configurada.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="8ab0f-114">En el servidor donde está configurada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la **base de datos de estado de cumplimiento de MBAM** esté configurada.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="8ab0f-115">En el servidor donde está configurada la característica informes, abra un explorador Web con credenciales administrativas y busque el "Inicio" del sitio de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="8ab0f-116">La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services es:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="8ab0f-117">http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Puerto* &gt; /Reports.aspx</span><span class="sxs-lookup"><span data-stu-id="8ab0f-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="8ab0f-118">Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que especificó durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="8ab0f-119">Confirme que una carpeta informes denominada **supervisión y administración de Microsoft BitLocker** contiene un origen de datos denominado **MaltaDataSource** , así como las carpetas de idioma.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="8ab0f-120">El origen de datos contiene carpetas con nombres que representan idiomas (por ejemplo, en-es).</span><span class="sxs-lookup"><span data-stu-id="8ab0f-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="8ab0f-121">Los informes se encuentran en las carpetas de idioma.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="8ab0f-122">Nota</span><span class="sxs-lookup"><span data-stu-id="8ab0f-122">Note</span></span>**  
    <span data-ttu-id="8ab0f-123">Si SQL Server Reporting Services (SSRs) se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="8ab0f-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="8ab0f-124">En el servidor donde está configurada la característica sitio web de supervisión y supervisión, ejecute **Administrador del servidor**, vaya a **roles**y, a continuación, seleccione **servidor Web (IIS)** &gt; **Administrador de servicios de Internet Information Server (** IIS).</span><span class="sxs-lookup"><span data-stu-id="8ab0f-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="8ab0f-125">En **conexiones**, vaya a \* &lt; &gt; nombre de equipo\* y seleccione **sitios** &gt; **Administración y administración de BitLocker de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="8ab0f-126">Compruebe que se muestran las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="8ab0f-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="8ab0f-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="8ab0f-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="8ab0f-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="8ab0f-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="8ab0f-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="8ab0f-130">En el servidor en el que se han configurado el sitio web de administración y supervisión y el portal de autoservicio, abra un explorador Web con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="8ab0f-131">Vaya a los siguientes sitios web para comprobar que se cargan correctamente:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="8ab0f-132">https (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /Helpdesk/: Confirme cada uno de los vínculos para la navegación e informes</span><span class="sxs-lookup"><span data-stu-id="8ab0f-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="8ab0f-133">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /SelfService/</span><span class="sxs-lookup"><span data-stu-id="8ab0f-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="8ab0f-134">Nota</span><span class="sxs-lookup"><span data-stu-id="8ab0f-134">Note</span></span>**  
   <span data-ttu-id="8ab0f-135">Se supone que ha configurado las características de servidor en el puerto predeterminado sin cifrado de red.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="8ab0f-136">Si ha configurado las características de servidor en un puerto o directorio virtual diferente, cambie las direcciones URL para que incluyan el puerto correspondiente, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="8ab0f-137">http (s):// &lt; *nombre de host* &gt; : &lt; *Puerto* &gt; /Helpdesk/</span><span class="sxs-lookup"><span data-stu-id="8ab0f-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="8ab0f-138">http (s):// &lt; *nombre de host* &gt; : &lt; *Puerto* &gt; / &lt; *VirtualDirectory*&gt;/</span><span class="sxs-lookup"><span data-stu-id="8ab0f-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="8ab0f-139">Si las características de servidor se han configurado con el cifrado de red, cambie http://a https://.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="8ab0f-140">Vaya a los siguientes servicios web para comprobar que se cargan correctamente.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="8ab0f-141">Se abre una página para indicar que el servicio se está ejecutando, pero la página no muestra metadatos.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="8ab0f-142">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMAdministrationService/AdministrationService.SVC</span><span class="sxs-lookup"><span data-stu-id="8ab0f-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="8ab0f-143">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMUserSupportService/UserSupportService.SVC</span><span class="sxs-lookup"><span data-stu-id="8ab0f-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="8ab0f-144">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMComplianceStatusService/StatusReportingService.SVC</span><span class="sxs-lookup"><span data-stu-id="8ab0f-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="8ab0f-145">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC</span><span class="sxs-lookup"><span data-stu-id="8ab0f-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="8ab0f-146">Validación de la implementación del servidor de MBAM con la topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ab0f-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="8ab0f-147">Siga estos pasos para validar la implementación de MBAM con la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="8ab0f-148">Complete los pasos de validación que coincidan con la versión del administrador de configuración que está usando.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="8ab0f-149">Validación de la implementación del servidor de MBAM con el administrador de configuración de System Center 2012</span><span class="sxs-lookup"><span data-stu-id="8ab0f-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="8ab0f-150">Siga estos pasos para validar la implementación de su servidor de MBAM cuando use MBAM con System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="8ab0f-151">Para validar una integración de Configuration Manager MBAM Server Deployment: System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ab0f-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="8ab0f-152">En el servidor donde se implementa System Center 2012 Configuration Manager, Abra **programas y características** en el **Panel de control**y compruebe que aparece **Administración y supervisión de Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="8ab0f-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="8ab0f-153">Nota</span><span class="sxs-lookup"><span data-stu-id="8ab0f-153">Note</span></span>**  
    <span data-ttu-id="8ab0f-154">Para validar la configuración, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="8ab0f-155">En la consola del administrador de configuración, haga clic en los conjuntos de dispositivos del área de trabajo de **activos y cumplimiento** &gt; **Device Collections**y confirme que se muestra una nueva colección denominada **MBAM equipos compatibles** .</span><span class="sxs-lookup"><span data-stu-id="8ab0f-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="8ab0f-156">En la consola del administrador de configuración, **Monitoring** haga clic en el &gt; **Reporting** &gt; **Reports** &gt; **MBAM**informes del área de trabajo supervisión.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="8ab0f-157">Compruebe que la carpeta **MBAM** contiene subcarpetas, con nombres que representan distintos idiomas y que los siguientes informes aparecen en la subcarpeta de cada idioma:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="8ab0f-158">Cumplimiento de BitLocker Computer</span><span class="sxs-lookup"><span data-stu-id="8ab0f-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="8ab0f-159">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8ab0f-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="8ab0f-160">Detalles de la compatibilidad con BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8ab0f-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="8ab0f-161">Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8ab0f-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="8ab0f-162">En la consola del administrador de configuración, haga clic en los planes de configuración de cumplimiento del área de trabajo de **activos y cumplimiento** &gt; **Compliance Settings** &gt; **Configuration Baselines**y compruebe que se muestra la configuración de la **protección de BitLocker** de línea base.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="8ab0f-163">En la consola del administrador de configuración, haga clic en los elementos de configuración de configuración de cumplimiento del área de trabajo de **activos y cumplimiento** &gt; **Compliance Settings** &gt; **Configuration Items**y compruebe que se muestran los siguientes elementos de configuración:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="8ab0f-164">Protección de las unidades de datos fijas de BitLocker</span><span class="sxs-lookup"><span data-stu-id="8ab0f-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="8ab0f-165">Protección de unidades del sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="8ab0f-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="8ab0f-166">Validación de la implementación del servidor de MBAM con Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="8ab0f-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="8ab0f-167">Siga estos pasos para validar la implementación de su servidor de MBAM cuando use MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="8ab0f-168">Para validar una integración de Configuration Manager MBAM Server Deployment: administrador de configuración 2007</span><span class="sxs-lookup"><span data-stu-id="8ab0f-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="8ab0f-169">En el servidor donde se implementa Configuration Manager 2007, Abra **programas y características** en el **Panel de control** y compruebe que aparece **Administración y supervisión de Microsoft BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="8ab0f-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="8ab0f-170">Nota</span><span class="sxs-lookup"><span data-stu-id="8ab0f-170">Note</span></span>**  
    <span data-ttu-id="8ab0f-171">Para validar la configuración, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="8ab0f-172">En la consola del administrador de configuración, haga clic en **Site Database &lt; nombresitio &gt;  -  &lt; ServerName &gt; , &lt; siteName &gt; , administración de equipos**y confirme que se muestra una nueva colección denominada **MBAM equipos compatibles** .</span><span class="sxs-lookup"><span data-stu-id="8ab0f-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="8ab0f-173">En la consola de Configuration Manager, haga clic en **Reporting** Reporting &gt; **Services** &gt; \*\* \\\\ &lt; &gt; ServerName\*\* Report &gt; **folders** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="8ab0f-174">Compruebe que la carpeta **MBAM** contiene subcarpetas, con nombres que representan distintos idiomas y que los siguientes informes aparecen en la subcarpeta de cada idioma:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="8ab0f-175">Cumplimiento de BitLocker Computer</span><span class="sxs-lookup"><span data-stu-id="8ab0f-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="8ab0f-176">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8ab0f-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="8ab0f-177">Detalles de la compatibilidad con BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8ab0f-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="8ab0f-178">Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8ab0f-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="8ab0f-179">En la consola del administrador de configuración, haga clic en líneas de base de configuración de **Administración de configuración deseada** &gt; **Configuration Baselines**y compruebe que aparece la **protección de BitLocker** de la configuración básica.</span><span class="sxs-lookup"><span data-stu-id="8ab0f-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="8ab0f-180">En la consola del administrador de configuración, haga clic en elementos de configuración de **Administración de configuración deseada** &gt; **Configuration Items**y confirme que se muestran los siguientes elementos de configuración:</span><span class="sxs-lookup"><span data-stu-id="8ab0f-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="8ab0f-181">Protección de las unidades de datos fijas de BitLocker</span><span class="sxs-lookup"><span data-stu-id="8ab0f-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="8ab0f-182">Protección de unidades del sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="8ab0f-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="8ab0f-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ab0f-183">Related topics</span></span>


[<span data-ttu-id="8ab0f-184">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8ab0f-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="8ab0f-185">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="8ab0f-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8ab0f-186">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8ab0f-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8ab0f-187">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8ab0f-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






