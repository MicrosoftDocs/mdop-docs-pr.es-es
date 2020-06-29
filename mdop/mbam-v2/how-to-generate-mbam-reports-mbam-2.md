---
title: Cómo generar informes MBAM.
description: Cómo generar informes MBAM.
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824091"
---
# <span data-ttu-id="b2101-103">Cómo generar informes MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2101-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="b2101-104">Al instalar la administración y supervisión de Microsoft BitLocker (MBAM) con la topología independiente, puede generar diferentes informes para supervisar el uso y el cumplimiento del cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b2101-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="b2101-105">Los procedimientos de este tema describen cómo abrir el sitio web de administración y supervisión, así como los pasos necesarios para generar informes de administración y supervisión de Microsoft BitLocker sobre el cumplimiento de la norma empresarial, los equipos individuales y la actividad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="b2101-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="b2101-106">Para obtener información detallada que ayude a comprender los informes de MBAM, consulte [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="b2101-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="b2101-107">**Nota:**  Para ejecutar los informes, debe ser miembro del **rol de usuarios de informes** en los equipos en los que se instalan las características de servidor administración y supervisión, la base de datos de cumplimiento y la base de datos y los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b2101-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="b2101-108">Para abrir el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="b2101-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="b2101-109">Abra un explorador Web y vaya al sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="b2101-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="b2101-110">La dirección URL predeterminada para el sitio web de administración y supervisión es \*http:// &lt; NombreDeEquipo &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="b2101-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="b2101-111">**Nota:**  Si el sitio web de administración y supervisión se instaló en un puerto que no es 80, tiene que especificar el puerto en la dirección URL (por ejemplo, \*http:// &lt; NombreDeEquipo &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="b2101-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="b2101-112">Si especificó un nombre de host para el sitio web de administración y supervisión durante la instalación, la dirección URL es \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="b2101-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="b2101-113">En el panel izquierdo, haga clic en **informes** y, a continuación, seleccione el informe que desea ejecutar en la barra de menús superior.</span><span class="sxs-lookup"><span data-stu-id="b2101-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="b2101-114">Los datos históricos de los clientes de MBAM se conservan en la base de datos de cumplimiento para referencia histórica en caso de pérdida o robo de un equipo.</span><span class="sxs-lookup"><span data-stu-id="b2101-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="b2101-115">Cuando se ejecutan informes empresariales, le recomendamos que use las fechas de inicio y finalización apropiadas para el ámbito de los intervalos de tiempo para los informes de una a dos semanas, lo que aumentará la precisión de los datos.</span><span class="sxs-lookup"><span data-stu-id="b2101-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="b2101-116">**Nota:**  Si SSRS no se configuró para usar el nivel de socket seguro, la dirección URL de los informes se establecerá en HTTP en lugar de en HTTPS cuando instale el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2101-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="b2101-117">Si, a continuación, va al portal del servicio de asistencia y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro".</span><span class="sxs-lookup"><span data-stu-id="b2101-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="b2101-118">Para mostrar el informe, haga clic en **Mostrar todo el contenido**.</span><span class="sxs-lookup"><span data-stu-id="b2101-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="b2101-119">Para generar un informe de compatibilidad empresarial</span><span class="sxs-lookup"><span data-stu-id="b2101-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="b2101-120">Desde el sitio web de administración y supervisión, seleccione el nodo **informes** en el panel de navegación izquierdo, seleccione **Informe de cumplimiento**de la empresa y seleccione los filtros que desea usar.</span><span class="sxs-lookup"><span data-stu-id="b2101-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="b2101-121">Los filtros disponibles para el informe de cumplimiento de la empresa son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2101-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="b2101-122">**Estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="b2101-122">**Compliance Status**.</span></span> <span data-ttu-id="b2101-123">Use este filtro para especificar los tipos de estado de cumplimiento (por ejemplo, conformes o no conformes) del informe.</span><span class="sxs-lookup"><span data-stu-id="b2101-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="b2101-124">**Estado de error**.</span><span class="sxs-lookup"><span data-stu-id="b2101-124">**Error State**.</span></span> <span data-ttu-id="b2101-125">Use este filtro para especificar los tipos de estado de error (por ejemplo, ningún error o error) del informe.</span><span class="sxs-lookup"><span data-stu-id="b2101-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="b2101-126">Haga clic en **Ver informe** para mostrar el informe seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b2101-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="b2101-127">Los resultados se pueden guardar en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b2101-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="b2101-128">**Nota:**  El informe de cumplimiento de la empresa se genera a partir de un trabajo de SQL que se ejecuta cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="b2101-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="b2101-129">Por lo tanto, la primera vez que vea el informe, puede encontrarse con algunos datos que faltan.</span><span class="sxs-lookup"><span data-stu-id="b2101-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="b2101-130">Puede generar datos de informes actualizados de forma manual mediante SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b2101-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="b2101-131">En la ventana **Explorador de objetos** , expanda el **Agente SQL Server**, expanda **trabajos**, haga clic con el botón derecho en el trabajo **CreateCache** y seleccione **Iniciar tarea en el paso....**</span><span class="sxs-lookup"><span data-stu-id="b2101-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="b2101-132">Seleccione un nombre de equipo para ver información sobre el equipo en el informe de cumplimiento de equipos.</span><span class="sxs-lookup"><span data-stu-id="b2101-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="b2101-133">Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.</span><span class="sxs-lookup"><span data-stu-id="b2101-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="b2101-134">Para generar el informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="b2101-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="b2101-135">En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione el **Informe de cumplimiento de equipos**.</span><span class="sxs-lookup"><span data-stu-id="b2101-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="b2101-136">Use el informe de cumplimiento de equipos para buscar el **nombre de usuario** o **el nombre del equipo**.</span><span class="sxs-lookup"><span data-stu-id="b2101-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="b2101-137">Haga clic en **Ver informe** para ver el informe del equipo.</span><span class="sxs-lookup"><span data-stu-id="b2101-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="b2101-138">Los resultados se pueden guardar en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b2101-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="b2101-139">Seleccione el nombre de un equipo para mostrar más información sobre el equipo en el informe cumplimiento de equipos.</span><span class="sxs-lookup"><span data-stu-id="b2101-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="b2101-140">Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.</span><span class="sxs-lookup"><span data-stu-id="b2101-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="b2101-141">**Nota:**  Un equipo cliente de MBAM se considera conforme si el equipo cumple con los requisitos de la configuración de directiva de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2101-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="b2101-142">Para generar el informe de auditoría de clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="b2101-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="b2101-143">En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione el **Informe de auditoría de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="b2101-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="b2101-144">Seleccione los filtros para el informe de auditoría de clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="b2101-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="b2101-145">Los filtros disponibles para auditorías de claves de recuperación son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2101-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="b2101-146">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="b2101-146">**Requestor**.</span></span> <span data-ttu-id="b2101-147">Este filtro permite a los usuarios especificar el nombre de usuario del solicitante.</span><span class="sxs-lookup"><span data-stu-id="b2101-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="b2101-148">El solicitante es la persona del Departamento de soporte que ha tenido acceso a la clave en nombre de un usuario.</span><span class="sxs-lookup"><span data-stu-id="b2101-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="b2101-149">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="b2101-149">**Requestee**.</span></span> <span data-ttu-id="b2101-150">Este filtro permite a los usuarios especificar el nombre de usuario del solicitante.</span><span class="sxs-lookup"><span data-stu-id="b2101-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="b2101-151">El solicitante es la persona que llamó al servicio de asistencia para obtener una clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="b2101-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="b2101-152">**Resultado**de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2101-152">**Request Result**.</span></span> <span data-ttu-id="b2101-153">Este filtro permite a los usuarios especificar los tipos de resultado de la solicitud (por ejemplo, éxito o error) en los que desean basar el informe.</span><span class="sxs-lookup"><span data-stu-id="b2101-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="b2101-154">Por ejemplo, es posible que los usuarios deseen ver los intentos fallidos de acceso clave.</span><span class="sxs-lookup"><span data-stu-id="b2101-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="b2101-155">**Tipo de clave**.</span><span class="sxs-lookup"><span data-stu-id="b2101-155">**Key Type**.</span></span> <span data-ttu-id="b2101-156">Este filtro permite a los usuarios especificar el tipo de clave (por ejemplo: contraseña de la clave de recuperación o hash de contraseña de TPM) en la que desee basar el informe.</span><span class="sxs-lookup"><span data-stu-id="b2101-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="b2101-157">**Fecha de inicio**.</span><span class="sxs-lookup"><span data-stu-id="b2101-157">**Start Date**.</span></span> <span data-ttu-id="b2101-158">Este filtro se usa para definir la parte de fecha de inicio del intervalo de fechas para el que el usuario desea informar.</span><span class="sxs-lookup"><span data-stu-id="b2101-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="b2101-159">**Fecha de finalización**.</span><span class="sxs-lookup"><span data-stu-id="b2101-159">**End Date**.</span></span> <span data-ttu-id="b2101-160">Este filtro se usa para definir la fecha de finalización del intervalo de fechas en la que los usuarios desean informar.</span><span class="sxs-lookup"><span data-stu-id="b2101-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="b2101-161">Haga clic en **Ver informe** para ver el informe.</span><span class="sxs-lookup"><span data-stu-id="b2101-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="b2101-162">Los resultados se pueden guardar en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b2101-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="b2101-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2101-163">Related topics</span></span>


[<span data-ttu-id="b2101-164">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b2101-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





