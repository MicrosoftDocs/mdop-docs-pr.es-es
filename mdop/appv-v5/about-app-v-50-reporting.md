---
title: Acerca de la generación de informes de App-V5.0
description: Acerca de la generación de informes de App-V5.0
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815021"
---
# <span data-ttu-id="a8bbb-103">Acerca de la generación de informes de App-V5.0</span><span class="sxs-lookup"><span data-stu-id="a8bbb-103">About App-V 5.0 Reporting</span></span>


<span data-ttu-id="a8bbb-104">Microsoft Application Virtualization (App-V) 5,0 incluye una característica de creación de informes integrada que le ayuda a recopilar información sobre los equipos que ejecutan el cliente de App-V 5,0, así como información sobre el uso de paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-104">Microsoft Application Virtualization (App-V) 5.0 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.0 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="a8bbb-105">Puede usar esta información para generar informes desde una base de datos centralizada.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-0-reporting-overview"></a> <span data-ttu-id="a8bbb-106">Información general de informes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a8bbb-106">App-V 5.0 Reporting Overview</span></span>


<span data-ttu-id="a8bbb-107">En la siguiente lista se muestra el flujo de trabajo de alto nivel end-to-end para informes en App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.0.</span></span>

1.  <span data-ttu-id="a8bbb-108">El servidor de informes de Microsoft Application Virtualization (App-V) 5,0 tiene los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-108">The Microsoft Application Virtualization (App-V) 5.0 Reporting server has the following prerequisites:</span></span>

    -   <span data-ttu-id="a8bbb-109">Rol de servidor Web de Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="a8bbb-109">Internet Information Service (IIS) web server role</span></span>

    -   <span data-ttu-id="a8bbb-110">Rol de autenticación de Windows (en **IIS/seguridad**)</span><span class="sxs-lookup"><span data-stu-id="a8bbb-110">Windows Authentication role (under **IIS / Security**)</span></span>

    -   <span data-ttu-id="a8bbb-111">SQL Server instalado y ejecutándose con SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="a8bbb-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="a8bbb-112">Para confirmar que SQL Server Reporting Services está en ejecución, vea `http://localhost/Reports` en un explorador Web como administrador en el servidor que hospedará informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.0 Reporting.</span></span> <span data-ttu-id="a8bbb-113">Aparecerá la Página principal de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-113">The SQL Server Reporting Services Home page should display.</span></span>

2.  <span data-ttu-id="a8bbb-114">Instale el servidor de informes de App-V 5,0 y la base de datos asociada.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-114">Install the App-V 5.0 reporting server and associated database.</span></span> <span data-ttu-id="a8bbb-115">Para obtener más información sobre cómo instalar el servidor de informes [, vea Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md).</span><span class="sxs-lookup"><span data-stu-id="a8bbb-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md).</span></span> <span data-ttu-id="a8bbb-116">Configure la hora en la que el equipo que ejecuta el cliente de App-V 5,0 debe enviar datos al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-116">Configure the time when the computer running the App-V 5.0 client should send data to the reporting server.</span></span>

3.  <span data-ttu-id="a8bbb-117">Si no usa un sistema electrónico de distribución de software, como Configuration Manager, para ver los informes, puede definir informes en SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="a8bbb-118">Descargue los informes predefinidos de appvshort desde el centro de descarga en <https://go.microsoft.com/fwlink/?LinkId=397255> .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-118">Download predefined appvshort Reports from the Download Center at <https://go.microsoft.com/fwlink/?LinkId=397255>.</span></span>

    <span data-ttu-id="a8bbb-119">**Nota:**  Si está usando la integración de Configuration Manager con App-V 5,0, la mayoría de los informes se generan desde Configuration Manager en lugar de desde App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-119">**Note** If you are using the Configuration Manager integration with App-V 5.0, most reports are generated from Configuration Manager rather than from App-V 5.0.</span></span>

     

4.  <span data-ttu-id="a8bbb-120">Después de importar el módulo de PowerShell App-V 5,0 usando `Import-Module AppvClient` como administrador, habilite el cliente de App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-120">After importing the App-V 5.0 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.0 client.</span></span> <span data-ttu-id="a8bbb-121">Este cmdlet de PowerShell de ejemplo habilita informes de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-121">This sample PowerShell cmdlet enables App-V 5.0 reporting:</span></span>

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="a8bbb-122">Para enviar inmediatamente datos del informe de App-V 5,0, ejecute `Send-AppvClientReport` en el cliente de App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-122">To immediately send App-V 5.0 report data, run `Send-AppvClientReport` on the App-V 5.0 client.</span></span>

    <span data-ttu-id="a8bbb-123">Para obtener más información sobre cómo instalar el cliente de App-V 5,0 con informes habilitados, consulte [acerca de](about-client-configuration-settings.md)la configuración del cliente.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-123">For more information about installing the App-V 5.0 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span> <span data-ttu-id="a8bbb-124">Para administrar los informes de App-V 5,0 con Windows PowerShell, vea [Cómo habilitar la creación de informes en el cliente de App-v 5,0 con PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a8bbb-124">To administer App-V 5.0 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).</span></span>

5.  <span data-ttu-id="a8bbb-125">Después de que el servidor de informes reciba los datos del cliente de App-V 5,0, envía los datos a la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-125">After the reporting server receives the data from the App-V 5.0 client it sends the data to the reporting database.</span></span> <span data-ttu-id="a8bbb-126">Cuando la base de datos recibe y procesa los datos del cliente, se envía una respuesta correcta al servidor de informes y, a continuación, se envía una notificación al cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.0 client.</span></span>

6.  <span data-ttu-id="a8bbb-127">Cuando el cliente de App-V 5,0 recibe la notificación de éxito, vacía la memoria caché de datos para ahorrar espacio.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-127">When the App-V 5.0 client receives the success notification, it empties the data cache to conserve space.</span></span>

    <span data-ttu-id="a8bbb-128">**Nota:**  De forma predeterminada, la caché se borra después de que el servidor confirme la recepción de los datos.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-128">**Note** By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="a8bbb-129">Puede configurar manualmente el cliente para guardar la caché de datos.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-129">You can manually configure the client to save the data cache.</span></span>

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="a8bbb-130">Preguntas más frecuentes sobre App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="a8bbb-130">App-V 5.0 reporting server frequently asked questions</span></span>

<span data-ttu-id="a8bbb-131">En la siguiente tabla se muestran respuestas a las preguntas más frecuentes sobre los informes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a8bbb-131">The following table displays answers to common questions about App-V 5.0 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a8bbb-132">Pregunta</span><span class="sxs-lookup"><span data-stu-id="a8bbb-132">Question</span></span></th>
<th align="left"><span data-ttu-id="a8bbb-133">Más información</span><span class="sxs-lookup"><span data-stu-id="a8bbb-133">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a8bbb-134">¿Cuál es la frecuencia con que se envía la información de informes a la base de datos de informes?</span><span class="sxs-lookup"><span data-stu-id="a8bbb-134">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-135">La frecuencia depende de la configuración de la tarea de informes en el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-135">The frequency depends on how the reporting task is configured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="a8bbb-136">Debe configurar la frecuencia o el intervalo para enviar los datos de informes.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-136">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="a8bbb-137">Los informes de App-V 5,0 no están habilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-137">App-V 5.0 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a8bbb-138">¿Qué información se almacena en la base de datos del servidor de informes?</span><span class="sxs-lookup"><span data-stu-id="a8bbb-138">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-139">En la siguiente lista se muestra lo que se almacena en la base de datos de informes:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-139">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="a8bbb-140">El sistema operativo que se ejecuta en el equipo que ejecuta el cliente de App-V 5,0: nombre de host, versión, Service Pack, tipo-cliente/servidor, arquitectura de procesador.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-140">The operating system running on the computer running the App-V 5.0 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="a8bbb-141">Información del cliente de App-V 5,0: versión.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-141">App-V 5.0 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="a8bbb-142">Lista de paquetes publicados: GUID, GUID de versión, nombre.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-142">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="a8bbb-143">Información de uso de la aplicación: nombre, versión, servidor de streaming, usuario (domain\alias), GUID de versión de paquete, estado y hora de inicio, hora de cierre.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-143">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a8bbb-144">¿Cuál es el volumen medio de información que se envía al servidor de informes?</span><span class="sxs-lookup"><span data-stu-id="a8bbb-144">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-145">Depende.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-145">It depends.</span></span> <span data-ttu-id="a8bbb-146">En la siguiente lista se muestran los tres conjuntos de datos enviados al servidor de informes:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-146">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="a8bbb-147">Sistema operativo y información del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-147">Operating system, and App-V 5.0 client information.</span></span> <span data-ttu-id="a8bbb-148">~ 150 bytes, cada vez que se envían estos datos.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-148">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="a8bbb-149">Lista de paquetes publicados.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-149">Published package list.</span></span> <span data-ttu-id="a8bbb-150">~ 7 KB para 30 paquetes.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-150">~7 KB for 30 packages.</span></span> <span data-ttu-id="a8bbb-151">Esto se envía solo cuando la lista de paquetes se actualiza con una actualización de publicación, lo cual se hace con poca frecuencia; Si no hay ningún cambio, esta información no se envía.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-151">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="a8bbb-152">Información de uso de aplicaciones virtuales: aproximadamente 0,25 KB por evento.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-152">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="a8bbb-153">El recuento de apertura y cierre como un evento si ambos ocurren antes de enviar la información.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-153">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="a8bbb-154">Al enviar mediante una tarea programada, solo se envían al servidor los datos desde la última carga correcta.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-154">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="a8bbb-155">Si se envía manualmente a través del cmdlet de PowerShell, hay un argumento opcional que controla si los datos necesitan volver a enviarse la próxima vez, ese argumento es <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-155">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="a8bbb-156">Así, por ejemplo, si se abren y cierran veinte aplicaciones y se programa que la información se envíe diariamente, el tráfico diario típico debe ser de 0,15 KB + 20 x 0,25 KB o de 5KB/usuario</span><span class="sxs-lookup"><span data-stu-id="a8bbb-156">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a8bbb-157">¿Se pueden programar informes?</span><span class="sxs-lookup"><span data-stu-id="a8bbb-157">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-158">Sí.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-158">Yes.</span></span> <span data-ttu-id="a8bbb-159">Además de enviar informes de forma manual mediante cmdlets de PowerShell ( <strong> send-AppvClientReport </strong> ), la tarea se puede programar para que se produzca de forma automática.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-159">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="a8bbb-160">Existen dos formas de programar los informes:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-160">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="a8bbb-161">Usar cmdlets de PowerShell- <strong> set-AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-161">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="a8bbb-162">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-162">For example:</span></span></p>
<p><span data-ttu-id="a8bbb-163">Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="a8bbb-163">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="a8bbb-164">Para obtener una lista completa de las opciones de configuración del cliente, consulte Acerca de la configuración del <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> cliente </a> y busque las siguientes entradas: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay, ReportingInterval </strong> <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-164">For a complete list of client configuration settings see <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="a8bbb-165">Mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-165">By using Group Policy.</span></span> <span data-ttu-id="a8bbb-166">Si se distribuye con el controlador de dominio, la configuración es la misma que la mencionada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-166">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a8bbb-167">Nota</span><span class="sxs-lookup"><span data-stu-id="a8bbb-167">Note</span></span></strong><br/><p><span data-ttu-id="a8bbb-168">La configuración de directiva de grupo invalida la configuración local establecida mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-168">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> <span data-ttu-id="a8bbb-169">Informes de cliente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a8bbb-169">App-V 5.0 Client Reporting</span></span>


<span data-ttu-id="a8bbb-170">Para usar los informes de 5,0 de App-V, debe instalar y configurar el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-170">To use App-V 5.0 reporting you must install and configure the App-V 5.0 client.</span></span> <span data-ttu-id="a8bbb-171">Una vez instalado el cliente, use el cmdlet **de PowerShell Set-AppVClientConfiguration** o la **plantilla ADMX** para configurar los informes.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-171">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="a8bbb-172">Los cmdlets de características de creación de informes están disponibles usando el siguiente vínculo y están precedidos por los **informes**.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-172">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="a8bbb-173">Para obtener una lista completa de las opciones de configuración de cliente, consulte Acerca de los [parámetros de configuración de cliente](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a8bbb-173">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span> <span data-ttu-id="a8bbb-174">En la siguiente sección se proporcionan ejemplos de la configuración de informes de cliente de App-V 5,0 con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-174">The following section provides examples of App-V 5.0 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="a8bbb-175">Configuración de informes de clientes de App-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8bbb-175">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="a8bbb-176">En los siguientes ejemplos se muestra cómo los parámetros de PowerShell pueden configurar las características de informes del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-176">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.0 client.</span></span>

**<span data-ttu-id="a8bbb-177">Nota</span><span class="sxs-lookup"><span data-stu-id="a8bbb-177">Note</span></span>**  
<span data-ttu-id="a8bbb-178">La siguiente tarea de configuración también se puede configurar con la configuración de directiva de grupo de la plantilla App-V 5,0 ADMX.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-178">The following configuration task can also be configured using Group Policy settings in the App-V 5.0 ADMX template.</span></span> <span data-ttu-id="a8bbb-179">Para obtener más información sobre el uso de la plantilla ADMX, consulte [Cómo modificar la configuración de cliente de App-V 5,0 con la plantilla ADMX y la Directiva de grupo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="a8bbb-179">For more information about using the ADMX template, see [How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>
 


<span data-ttu-id="a8bbb-180">**Para habilitar los informes e iniciar la recopilación de datos en el equipo que ejecuta el cliente de App-V 5,0**:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-180">**To enable reporting and to initiate data collection on the computer running the App-V 5.0 client**:</span></span>

`Set-AppVClientConfiguration –ReportingEnabled 1`

<span data-ttu-id="a8bbb-181">**Para configurar el cliente para que envíe datos automáticamente a un servidor de informes específico**:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-181">**To configure the client to automatically send data to a specific reporting server**:</span></span>

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

<span data-ttu-id="a8bbb-182">En este ejemplo se configura el cliente para que envíe automáticamente los datos de informes a la dirección URL del servidor de informes <strong> http://MyReportingServer:MyPort/ </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-182">This example configures the client to automatically send the reporting data to the reporting server URL <strong>http://MyReportingServer:MyPort/</strong>.</span></span> <span data-ttu-id="a8bbb-183">Además, los datos de informes se enviarán todos los días entre 8:00 y 8:30 PM, según el retraso aleatorio generado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-183">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="a8bbb-184">**Para limitar el tamaño de la caché de datos en el cliente**, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-184">**To limit the size of the data cache on the client**:</span></span>

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

<span data-ttu-id="a8bbb-185">Configura el tamaño máximo de la caché de informes en el equipo que ejecuta el cliente de App-V 5,0 en 100 MB.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-185">Configures the maximum size of the reporting cache on the computer running the App-V 5.0 client to 100 MB.</span></span> <span data-ttu-id="a8bbb-186">Si se alcanza el límite de la caché antes de que los datos se envíen al servidor, el inicio de sesión y los datos se sobrescribirán según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-186">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="a8bbb-187">**Para configurar el tamaño del bloque de datos transmitido a través de la red entre el cliente y el servidor**:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-187">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

<span data-ttu-id="a8bbb-188">Especifica el bloque de datos máximo que el cliente envía a 10240 MB.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-188">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="a8bbb-189">Tipos de datos recopilados</span><span class="sxs-lookup"><span data-stu-id="a8bbb-189">Types of data collected</span></span>

<span data-ttu-id="a8bbb-190">En la siguiente tabla se muestran los tipos de información que puede recopilar mediante el uso de informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-190">The following table displays the types of information you can collect by using App-V 5.0 reporting.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a8bbb-191">Información del cliente</span><span class="sxs-lookup"><span data-stu-id="a8bbb-191">Client Information</span></span></th>
<th align="left"><span data-ttu-id="a8bbb-192">Información de paquete</span><span class="sxs-lookup"><span data-stu-id="a8bbb-192">Package Information</span></span></th>
<th align="left"><span data-ttu-id="a8bbb-193">Uso de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a8bbb-193">Application Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a8bbb-194">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="a8bbb-194">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-195">Nombre del paquete</span><span class="sxs-lookup"><span data-stu-id="a8bbb-195">Package Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-196">Horas de inicio y finalización</span><span class="sxs-lookup"><span data-stu-id="a8bbb-196">Start and End Times</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a8bbb-197">Versión de cliente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a8bbb-197">App-V 5.0 Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-198">Versión del paquete</span><span class="sxs-lookup"><span data-stu-id="a8bbb-198">Package Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-199">Estado de ejecución</span><span class="sxs-lookup"><span data-stu-id="a8bbb-199">Run Status</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a8bbb-200">Arquitectura del procesador</span><span class="sxs-lookup"><span data-stu-id="a8bbb-200">Processor Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-201">Origen del paquete</span><span class="sxs-lookup"><span data-stu-id="a8bbb-201">Package Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-202">Estado de apagado</span><span class="sxs-lookup"><span data-stu-id="a8bbb-202">Shutdown State</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a8bbb-203">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a8bbb-203">Operating System Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-204">Porcentaje en caché</span><span class="sxs-lookup"><span data-stu-id="a8bbb-204">Percent Cached</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-205">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a8bbb-205">Application Name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a8bbb-206">Nivel de Service Pack</span><span class="sxs-lookup"><span data-stu-id="a8bbb-206">Service Pack Level</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-207">Versión de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a8bbb-207">Application Version</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a8bbb-208">Tipo de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a8bbb-208">Operating System Type</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-209">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="a8bbb-209">Username</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-210">Grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="a8bbb-210">Connection Group</span></span></p></td>
</tr>
</tbody>
</table>
 


<span data-ttu-id="a8bbb-211">El cliente recopila y guarda estos datos en un formato **. XML** .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-211">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="a8bbb-212">La caché de datos está oculta de forma predeterminada y requiere derechos de administrador para abrir el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-212">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="a8bbb-213">Enviar datos al servidor</span><span class="sxs-lookup"><span data-stu-id="a8bbb-213">Sending data to the server</span></span>

<span data-ttu-id="a8bbb-214">Puede configurar el equipo que ejecuta el cliente de App-V 5,0 para que envíe datos automáticamente al servidor de informes especificado.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-214">You can configure the computer that is running the App-V 5.0 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="a8bbb-215">Para especificar el servidor, use el cmdlet **set-AppvClientConfiguration** con la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-215">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

-   <span data-ttu-id="a8bbb-216">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8bbb-216">ReportingEnabled</span></span>

-   <span data-ttu-id="a8bbb-217">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="a8bbb-217">ReportingServerURL</span></span>

-   <span data-ttu-id="a8bbb-218">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="a8bbb-218">ReportingStartTime</span></span>

-   <span data-ttu-id="a8bbb-219">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="a8bbb-219">ReportingInterval</span></span>

-   <span data-ttu-id="a8bbb-220">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="a8bbb-220">ReportingRandomDelay</span></span>

<span data-ttu-id="a8bbb-221">Una vez configurada la configuración anterior, debe crear una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-221">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="a8bbb-222">La tarea programada se pondrá en contacto con el servidor especificado por la configuración de **ReportingServerURL** y iniciará la transferencia.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-222">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="a8bbb-223">Si desea enviar datos de forma manual fuera de las horas programadas, use el siguiente cmdlet de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-223">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

<span data-ttu-id="a8bbb-224">Si el servidor de informes se ha configurado previamente, se puede omitir el parámetro **– URL** .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-224">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="a8bbb-225">Como alternativa, si los datos se deben enviar a una ubicación alternativa, especifique una dirección URL diferente para invalidar el **ReportingServerURL** configurado para esta recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-225">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="a8bbb-226">El parámetro **-DeleteOnSuccess** indica que si la transferencia se realiza correctamente, la caché de datos se borrará.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-226">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="a8bbb-227">Si no se especifica, la caché no se borrará.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-227">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="a8bbb-228">Recopilación de datos manual</span><span class="sxs-lookup"><span data-stu-id="a8bbb-228">Manual Data Collection</span></span>

<span data-ttu-id="a8bbb-229">También puede usar el cmdlet **send-AppVClientReport** para recopilar datos de forma manual.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-229">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="a8bbb-230">Esta solución es útil con o sin un servidor de informes existente.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-230">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="a8bbb-231">En la siguiente lista se muestra información sobre la recopilación de datos con o sin un servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-231">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a8bbb-232">Con un servidor de informes</span><span class="sxs-lookup"><span data-stu-id="a8bbb-232">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="a8bbb-233">Sin un servidor de informes</span><span class="sxs-lookup"><span data-stu-id="a8bbb-233">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a8bbb-234">Si ya tiene un servidor de informes de App-V 5,0, cree una tarea o una secuencia de comandos personalizada.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-234">If you have an existing App-V 5.0 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="a8bbb-235">Especificar que el cliente envíe los datos a la ubicación especificada con la frecuencia que desee.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-235">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a8bbb-236">Si no tiene un servidor de informes de App-V 5,0, use el <strong> parámetro – URL </strong> para enviar los datos a un recurso compartido especificado.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-236">If you do not have an existing App-V 5.0 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="a8bbb-237">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-237">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="a8bbb-238">El ejemplo anterior enviará los datos de informes a la <strong> &lt; &gt; Ubicación de \MyShare\MyData/Strong indicada por el <strong> parámetro-URL </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8bbb-238">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="a8bbb-239">Una vez enviados los datos, la caché se borra.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-239">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a8bbb-240">Nota</span><span class="sxs-lookup"><span data-stu-id="a8bbb-240">Note</span></span></strong><br/><p><span data-ttu-id="a8bbb-241">Si se especifica una ubicación que no sea el servidor de informes, los datos se envían con el <strong> formato. XML </strong> sin ningún procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-241">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a8bbb-242">Creación de informes</span><span class="sxs-lookup"><span data-stu-id="a8bbb-242">Creating Reports</span></span>

<span data-ttu-id="a8bbb-243">Para recuperar información del informe y crear informes con App-V 5,0, debe usar uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-243">To retrieve report information and create reports using App-V 5.0 you must use one of the following methods:</span></span>

-   <span data-ttu-id="a8bbb-244">**Microsoft SQL Server Reporting Services (SSRs)** : Microsoft SQL Server Reporting Services está disponible con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-244">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="a8bbb-245">SSRS no se instala al instalar el servidor de informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-245">SSRS is not installed when you install the App-V 5.0 reporting server.</span></span> <span data-ttu-id="a8bbb-246">Debe implementarse por separado para generar los informes asociados.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-246">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="a8bbb-247">Use el siguiente vínculo para obtener más información sobre cómo usar [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span><span class="sxs-lookup"><span data-stu-id="a8bbb-247">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

-   <span data-ttu-id="a8bbb-248">**Scripting** : puede generar informes mediante scripting directamente con la base de datos de informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-248">**Scripting** – You can generate reports by scripting directly against the App-V 5.0 reporting database.</span></span> <span data-ttu-id="a8bbb-249">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-249">For example:</span></span>

    **<span data-ttu-id="a8bbb-250">Procedimiento almacenado:</span><span class="sxs-lookup"><span data-stu-id="a8bbb-250">Stored Procedure:</span></span>**

    <span data-ttu-id="a8bbb-251">**spProcessClientReport** se ha programado para ejecutarse a medianoche o 12:00 a.m.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-251">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="a8bbb-252">Para ejecutar el procedimiento almacenado programado Microsoft SQL Server, debe estar ejecutándose el Agente SQL Server de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-252">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="a8bbb-253">Debe asegurarse de que el Agente SQL Server de Microsoft esté configurado para **iniciar automáticamente**.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-253">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="a8bbb-254">Para obtener más información [, consulte AUTOSTART SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="a8bbb-254">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="a8bbb-255">El procedimiento almacenado también se crea al usar los scripts de base de datos de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-255">The stored procedure is also created when using the App-V 5.0 database scripts.</span></span>

<span data-ttu-id="a8bbb-256">También debe asegurarse de que el **número máximo de conexiones simultáneas** del servicio Web del servidor de informes esté establecido como un valor que el servidor podrá administrar sin afectar a la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-256">You should also ensure that the reporting server web service’s **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="a8bbb-257">El número recomendado de **conexiones simultáneas máximas** para el **servicio Web de informes** es **10.000**.</span><span class="sxs-lookup"><span data-stu-id="a8bbb-257">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>






## <span data-ttu-id="a8bbb-258">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8bbb-258">Related topics</span></span>


[<span data-ttu-id="a8bbb-259">Implementación del servidor de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a8bbb-259">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="a8bbb-260">Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="a8bbb-260">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





