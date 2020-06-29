---
title: Generación de informes independientes de MBAM 2.5
description: Generación de informes independientes de MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823121"
---
# <span data-ttu-id="94ce7-103">Generación de informes independientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="94ce7-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="94ce7-104">Al configurar administración y supervisión de Microsoft BitLocker (MBAM) con la topología independiente, puede generar informes para supervisar el uso del cifrado de unidad BitLocker y el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="94ce7-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="94ce7-105">Este tema contiene los procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="94ce7-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="94ce7-106">Para abrir el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="94ce7-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="94ce7-107">Para generar un informe de compatibilidad empresarial</span><span class="sxs-lookup"><span data-stu-id="94ce7-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="94ce7-108">Para generar un informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="94ce7-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="94ce7-109">Para generar un informe de auditoría de clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="94ce7-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="94ce7-110">Para obtener descripciones de los informes independientes, consulte [Understanding MBAM 2,5 informes independientes](understanding-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="94ce7-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="94ce7-111">**Nota:**  Para ejecutar los informes, debe ser miembro del grupo de **usuarios de informes de MBAM** , que puede configurar en los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94ce7-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="94ce7-112">Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="94ce7-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="94ce7-113">Para abrir el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="94ce7-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="94ce7-114">Abra un explorador Web y vaya al sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="94ce7-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="94ce7-115">La dirección URL predeterminada para el sitio web de administración y supervisión es:</span><span class="sxs-lookup"><span data-stu-id="94ce7-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="94ce7-116">http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; Puerto &gt; /Helpdesk</span><span class="sxs-lookup"><span data-stu-id="94ce7-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="94ce7-117">En el panel de la izquierda, haga clic en **informes**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="94ce7-118">En la barra de menús superior, seleccione el informe que desea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="94ce7-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="94ce7-119">Los datos del cliente de MBAM se conservan en la base de datos de cumplimiento y auditoría para las referencias históricas en caso de pérdida o robo de un equipo.</span><span class="sxs-lookup"><span data-stu-id="94ce7-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="94ce7-120">Cuando se ejecutan informes empresariales, le recomendamos que use las fechas de inicio y finalización apropiadas para el ámbito de los intervalos de tiempo para los informes de una a dos semanas, lo que aumentará la precisión de los datos.</span><span class="sxs-lookup"><span data-stu-id="94ce7-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="94ce7-121">Después de generar un informe, puede guardar los resultados en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="94ce7-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="94ce7-122">**Nota:**  Configure SQL Server Reporting Services (SSRS) para usar la capa de sockets seguros (SSL) antes de configurar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="94ce7-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="94ce7-123">Si, por cualquier motivo, SSRS no está configurado para usar SSL, la dirección URL de los informes se establecerá en HTTP en lugar de en HTTPS cuando configure el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="94ce7-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="94ce7-124">Si, a continuación, visita el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro".</span><span class="sxs-lookup"><span data-stu-id="94ce7-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="94ce7-125">Para mostrar el informe, haga clic en **Mostrar todo el contenido**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="94ce7-126">Para generar un informe de compatibilidad empresarial</span><span class="sxs-lookup"><span data-stu-id="94ce7-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="94ce7-127">Desde el sitio web de administración y supervisión, seleccione el nodo **informes** en el panel de navegación izquierdo, seleccione **Informe de cumplimiento**de la empresa y seleccione los filtros que desea usar.</span><span class="sxs-lookup"><span data-stu-id="94ce7-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="94ce7-128">Los filtros disponibles para el informe de cumplimiento de la empresa son:</span><span class="sxs-lookup"><span data-stu-id="94ce7-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="94ce7-129">**Estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-129">**Compliance Status**.</span></span> <span data-ttu-id="94ce7-130">Use este filtro para especificar los tipos de estado de cumplimiento del informe (por ejemplo, compatible o no compatible).</span><span class="sxs-lookup"><span data-stu-id="94ce7-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="94ce7-131">**Estado de error**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-131">**Error State**.</span></span> <span data-ttu-id="94ce7-132">Use este filtro para especificar los tipos de estado de error del informe (por ejemplo, sin errores o errores).</span><span class="sxs-lookup"><span data-stu-id="94ce7-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="94ce7-133">Haga clic en **Ver informe** para mostrar el informe seleccionado.</span><span class="sxs-lookup"><span data-stu-id="94ce7-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="94ce7-134">Seleccione un nombre de equipo para ver información sobre el equipo en el informe de cumplimiento de equipos.</span><span class="sxs-lookup"><span data-stu-id="94ce7-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="94ce7-135">Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.</span><span class="sxs-lookup"><span data-stu-id="94ce7-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="94ce7-136">Para generar un informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="94ce7-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="94ce7-137">En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione **Informe de cumplimiento de equipos**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="94ce7-138">Use el informe de cumplimiento de equipos para buscar el **nombre de usuario** o **el nombre del equipo**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="94ce7-139">Haga clic en **Ver informe** para ver el informe de cumplimiento de equipos.</span><span class="sxs-lookup"><span data-stu-id="94ce7-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="94ce7-140">Seleccione el nombre de un equipo para mostrar más información sobre el equipo en el informe cumplimiento de equipos.</span><span class="sxs-lookup"><span data-stu-id="94ce7-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="94ce7-141">Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.</span><span class="sxs-lookup"><span data-stu-id="94ce7-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="94ce7-142">**Nota:**  Un equipo cliente de MBAM se considera conforme si el equipo cumple o supera los requisitos de la configuración de directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="94ce7-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="94ce7-143">Para generar un informe de auditoría de clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="94ce7-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="94ce7-144">En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione **Informe de auditoría de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="94ce7-145">Seleccione los filtros para el informe de auditoría de clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="94ce7-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="94ce7-146">Los filtros disponibles para auditorías de claves de recuperación son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="94ce7-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="94ce7-147">**Usuario del servicio de asistencia**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-147">**Helpdesk User**.</span></span> <span data-ttu-id="94ce7-148">Este filtro permite a los usuarios especificar el nombre de usuario del solicitante.</span><span class="sxs-lookup"><span data-stu-id="94ce7-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="94ce7-149">El solicitante es la persona del servicio de asistencia que ha tenido acceso a la clave en nombre de un usuario final.</span><span class="sxs-lookup"><span data-stu-id="94ce7-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="94ce7-150">**Usuario final**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-150">**End User**.</span></span> <span data-ttu-id="94ce7-151">Este filtro permite a los usuarios especificar el nombre de usuario del solicitante.</span><span class="sxs-lookup"><span data-stu-id="94ce7-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="94ce7-152">El solicitante es el usuario final que llamó al servicio de asistencia para obtener una clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="94ce7-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="94ce7-153">**Resultado**de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="94ce7-153">**Request Result**.</span></span> <span data-ttu-id="94ce7-154">Este filtro permite a los usuarios especificar los tipos de resultado de la solicitud (por ejemplo, éxito o error) en los que desean basar el informe.</span><span class="sxs-lookup"><span data-stu-id="94ce7-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="94ce7-155">Por ejemplo, es posible que los usuarios deseen ver los intentos fallidos de acceso clave.</span><span class="sxs-lookup"><span data-stu-id="94ce7-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="94ce7-156">**Tipo de clave**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-156">**Key Type**.</span></span> <span data-ttu-id="94ce7-157">Este filtro permite a los usuarios especificar el tipo de clave (por ejemplo, la contraseña de la clave de recuperación o el hash de contraseña de TPM) en el que desean basar el informe.</span><span class="sxs-lookup"><span data-stu-id="94ce7-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="94ce7-158">**Fecha de inicio**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-158">**Start Date**.</span></span> <span data-ttu-id="94ce7-159">Este filtro se usa para definir la parte de fecha de inicio del intervalo de fechas para el que el usuario desea informar.</span><span class="sxs-lookup"><span data-stu-id="94ce7-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="94ce7-160">**Fecha de finalización**.</span><span class="sxs-lookup"><span data-stu-id="94ce7-160">**End Date**.</span></span> <span data-ttu-id="94ce7-161">Este filtro se usa para definir la fecha de finalización del intervalo de fechas en la que los usuarios desean informar.</span><span class="sxs-lookup"><span data-stu-id="94ce7-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="94ce7-162">Haga clic en **Ver informe** para ver el informe.</span><span class="sxs-lookup"><span data-stu-id="94ce7-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="94ce7-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94ce7-163">Related topics</span></span>


[<span data-ttu-id="94ce7-164">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="94ce7-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="94ce7-165">Descripción de informes independientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="94ce7-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="94ce7-166">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="94ce7-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="94ce7-167">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="94ce7-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="94ce7-168">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="94ce7-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





