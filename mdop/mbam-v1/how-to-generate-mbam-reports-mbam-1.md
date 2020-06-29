---
title: Cómo generar informes MBAM.
description: Cómo generar informes MBAM.
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824530"
---
# <span data-ttu-id="4a58a-103">Cómo generar informes MBAM.</span><span class="sxs-lookup"><span data-stu-id="4a58a-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="4a58a-104">Administración y supervisión de Microsoft BitLocker (MBAM) genera varios informes para supervisar el uso del cifrado de BitLocker y el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="4a58a-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="4a58a-105">En este tema se describe cómo abrir el sitio web de administración de MBAM y cómo generar informes de MBAM sobre cumplimiento de normas para empresas, equipos individuales, compatibilidad de hardware y actividad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="4a58a-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="4a58a-106">Para obtener más información sobre los informes de MBAM, vea Descripción de los [informes de MBAM](understanding-mbam-reports-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="4a58a-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="4a58a-107">**Nota:**  Para ejecutar los informes, debe ser miembro de la función de **usuarios de informes** en los equipos en los que haya instalado las características del servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y los informes de auditoría y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="4a58a-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="4a58a-108">Para abrir el sitio web de administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="4a58a-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="4a58a-109">Abra un explorador Web y vaya al sitio web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="4a58a-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="4a58a-110">La dirección URL predeterminada del sitio Web *es &lt; http:// &gt; NombreDeEquipo* del servidor de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4a58a-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="4a58a-111">**Nota:**  Si el sitio web de MBAMadministration se instaló en un puerto que no es 80, debe especificar ese número de puerto en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="4a58a-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="4a58a-112">Por ejemplo, \*http:// &lt; nombreEquipo &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="4a58a-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="4a58a-113">Si especificó un nombre de host para el sitio web de MBAMadministration durante la instalación, la dirección URL sería \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="4a58a-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="4a58a-114">En el panel de navegación, haga clic en **informes**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="4a58a-115">En el panel principal, haga clic en la pestaña de su tipo de informe: **Informe de cumplimiento**de la empresa, informe de **cumplimiento de equipos**, informe de auditoría de **hardware**o informe de **Auditoría de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="4a58a-116">**Nota:**  Los datos históricos de los clientes de MBAM se conservan en la base de datos de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="4a58a-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="4a58a-117">Es posible que se necesiten datos retenidos en caso de pérdida o robo de un equipo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="4a58a-118">Cuando se ejecutan informes empresariales, debe usar fechas de inicio y finalización apropiadas para el ámbito de los intervalos de tiempo para los informes de una a dos semanas, con el fin de aumentar la precisión de los datos de informes.</span><span class="sxs-lookup"><span data-stu-id="4a58a-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="4a58a-119">Para generar un informe de compatibilidad empresarial</span><span class="sxs-lookup"><span data-stu-id="4a58a-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="4a58a-120">En el sitio web de MBAMadministration, haga clic en **informes** en el panel de navegación y, a continuación, haga clic en la pestaña **Informe de cumplimiento corporativo** y seleccione los filtros adecuados para el informe.</span><span class="sxs-lookup"><span data-stu-id="4a58a-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="4a58a-121">Para el informe de cumplimiento de la empresa, puede configurar los siguientes filtros.</span><span class="sxs-lookup"><span data-stu-id="4a58a-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="4a58a-122">**Estado de cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-122">**Compliance Status**.</span></span> <span data-ttu-id="4a58a-123">Use este filtro para especificar los tipos de estado de cumplimiento (por ejemplo, conformes o no conformes) para incluirlos en el informe.</span><span class="sxs-lookup"><span data-stu-id="4a58a-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="4a58a-124">**Estado de error**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-124">**Error State**.</span></span> <span data-ttu-id="4a58a-125">Use este filtro para especificar los tipos de estado de error, como sin error o error, para incluirlos en el informe.</span><span class="sxs-lookup"><span data-stu-id="4a58a-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="4a58a-126">Haga clic en **Ver informe** para mostrar el informe especificado.</span><span class="sxs-lookup"><span data-stu-id="4a58a-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="4a58a-127">Los resultados del informe se pueden guardar en cualquiera de los formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4a58a-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="4a58a-128">**Nota:**  El informe de cumplimiento de la empresa se genera a partir de un trabajo de SQL que se ejecuta cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="4a58a-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="4a58a-129">Por lo tanto, la primera vez que intente ver el informe, puede encontrarse con algunos datos que faltan.</span><span class="sxs-lookup"><span data-stu-id="4a58a-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="4a58a-130">Para ver la información de un equipo en el informe cumplimiento de equipos, seleccione el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="4a58a-131">Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="4a58a-132">Para generar el informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="4a58a-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="4a58a-133">En el sitio web de MBAMadministration, seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de cumplimiento de equipos**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="4a58a-134">Use el informe de cumplimiento de equipos para buscar el **nombre de usuario** o **el nombre del equipo**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="4a58a-135">Haga clic en **Ver informe** para ver el informe del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="4a58a-136">Los resultados se pueden guardar en cualquiera de los formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4a58a-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="4a58a-137">Para mostrar más información sobre un equipo en el informe cumplimiento de equipos, seleccione el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="4a58a-138">Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="4a58a-139">**Nota:**  Un equipo cliente de MBAM se considera conforme si el equipo cumple con los requisitos de la configuración de la Directiva MBAM o el modelo de hardware del equipo se establece en incompatible.</span><span class="sxs-lookup"><span data-stu-id="4a58a-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="4a58a-140">Por lo tanto, al ver información detallada sobre los volúmenes de disco asociados con el equipo, los equipos que están exentos de cifrado de BitLocker debido a la compatibilidad de hardware se pueden mostrar como compatibles aunque el estado de cifrado del volumen de la unidad se muestre como no conforme.</span><span class="sxs-lookup"><span data-stu-id="4a58a-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="4a58a-141">Para generar el informe de auditoría de compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="4a58a-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="4a58a-142">En el sitio web de MBAMadministration, seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de auditoría de hardware**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="4a58a-143">Seleccione los filtros adecuados para su informe de auditoría de hardware.</span><span class="sxs-lookup"><span data-stu-id="4a58a-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="4a58a-144">El informe de auditoría de hardware ofrece los siguientes filtros disponibles:</span><span class="sxs-lookup"><span data-stu-id="4a58a-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="4a58a-145">**Usuario (dominio\\usuario)**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="4a58a-146">Especifica el nombre del usuario que realizó un cambio.</span><span class="sxs-lookup"><span data-stu-id="4a58a-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="4a58a-147">**Cambiar tipo**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-147">**Change Type**.</span></span> <span data-ttu-id="4a58a-148">Especifica el tipo de cambios que está buscando.</span><span class="sxs-lookup"><span data-stu-id="4a58a-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="4a58a-149">**Fecha de inicio**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-149">**Start Date**.</span></span> <span data-ttu-id="4a58a-150">Especifica la parte de la fecha de inicio del intervalo de fechas en el que desea informar.</span><span class="sxs-lookup"><span data-stu-id="4a58a-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="4a58a-151">**Fecha de finalización**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-151">**End Date**.</span></span> <span data-ttu-id="4a58a-152">Especifica la parte de la fecha de finalización del intervalo de fechas en el que desea informar.</span><span class="sxs-lookup"><span data-stu-id="4a58a-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="4a58a-153">Haga clic en **Ver informe** para ver el informe.</span><span class="sxs-lookup"><span data-stu-id="4a58a-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="4a58a-154">Los resultados se pueden guardar en varios formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4a58a-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="4a58a-155">Para generar el informe de auditoría de clave de recuperación</span><span class="sxs-lookup"><span data-stu-id="4a58a-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="4a58a-156">En el sitio web de MBAMadministration, seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de auditoría de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="4a58a-157">Seleccione los filtros para el informe de auditoría de clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4a58a-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="4a58a-158">Los filtros disponibles para auditorías de claves de recuperación son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a58a-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="4a58a-159">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-159">**Requestor**.</span></span> <span data-ttu-id="4a58a-160">Especifica el nombre de usuario del solicitante.</span><span class="sxs-lookup"><span data-stu-id="4a58a-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="4a58a-161">El solicitante es la persona del Departamento de soporte que ha tenido acceso a la clave en nombre de un usuario.</span><span class="sxs-lookup"><span data-stu-id="4a58a-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="4a58a-162">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-162">**Requestee**.</span></span> <span data-ttu-id="4a58a-163">Especifica el nombre de usuario del solicitante.</span><span class="sxs-lookup"><span data-stu-id="4a58a-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="4a58a-164">El solicitante es la persona que llamó al servicio de asistencia para obtener una clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4a58a-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="4a58a-165">**Resultado** de la solicitud Especifica los tipos de resultado de la solicitud, como: correcto o erróneo.</span><span class="sxs-lookup"><span data-stu-id="4a58a-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="4a58a-166">Por ejemplo, es posible que desee ver los intentos fallidos de acceso clave.</span><span class="sxs-lookup"><span data-stu-id="4a58a-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="4a58a-167">**Tipo de clave**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-167">**Key Type**.</span></span> <span data-ttu-id="4a58a-168">Especifica el tipo de clave, como por ejemplo: contraseña de clave de recuperación o hash de contraseña de TPM.</span><span class="sxs-lookup"><span data-stu-id="4a58a-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="4a58a-169">**Fecha de inicio**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-169">**Start Date**.</span></span> <span data-ttu-id="4a58a-170">Especifica la fecha de inicio del intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="4a58a-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="4a58a-171">**Fecha de finalización**.</span><span class="sxs-lookup"><span data-stu-id="4a58a-171">**End Date**.</span></span> <span data-ttu-id="4a58a-172">Especifica la parte de la fecha de finalización del intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="4a58a-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="4a58a-173">Haga clic en **Ver informe** para mostrar el informe.</span><span class="sxs-lookup"><span data-stu-id="4a58a-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="4a58a-174">Los resultados se pueden guardar en varios formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4a58a-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="4a58a-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a58a-175">Related topics</span></span>


[<span data-ttu-id="4a58a-176">Supervisión e informes de cumplimiento de BitLocker con MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4a58a-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





