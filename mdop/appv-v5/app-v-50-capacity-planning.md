---
title: Planificación de la capacidad de App-V 5.0
description: Planificación de la capacidad de App-V 5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814854"
---
# <span data-ttu-id="e076c-103">Planificación de la capacidad de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e076c-103">App-V 5.0 Capacity Planning</span></span>


<span data-ttu-id="e076c-104">Las siguientes recomendaciones se pueden usar como una línea de base para ayudar a determinar la información de planeación de capacidad adecuada para la infraestructura de App-V 5,0 de su organización.</span><span class="sxs-lookup"><span data-stu-id="e076c-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="e076c-105">**Importante**  Use la información de esta sección solo como guía general para planear la implementación de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.0 deployment.</span></span> <span data-ttu-id="e076c-106">Los requisitos de capacidad del sistema dependerán de los detalles específicos de su entorno de hardware y de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="e076c-107">Además, los números de rendimiento que se muestran en este documento son ejemplos y los resultados pueden variar.</span><span class="sxs-lookup"><span data-stu-id="e076c-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="e076c-108">Determinar el ámbito del proyecto</span><span class="sxs-lookup"><span data-stu-id="e076c-108">Determine the Project Scope</span></span>


<span data-ttu-id="e076c-109">Antes de diseñar la infraestructura de App-V 5,0, debe determinar el ámbito del proyecto.</span><span class="sxs-lookup"><span data-stu-id="e076c-109">Before you design the App-V 5.0 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="e076c-110">El ámbito consiste en determinar qué aplicaciones estarán disponibles de forma virtual e identificar los usuarios de destino y sus ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="e076c-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="e076c-111">Esta información le ayudará a determinar qué tipo de infraestructura de App-V 5,0 debe implementarse.</span><span class="sxs-lookup"><span data-stu-id="e076c-111">This information will help determine what type of App-V 5.0 infrastructure should be implemented.</span></span> <span data-ttu-id="e076c-112">Las decisiones sobre el ámbito del proyecto deben basarse en las necesidades específicas de su organización.</span><span class="sxs-lookup"><span data-stu-id="e076c-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-113">Tarea</span><span class="sxs-lookup"><span data-stu-id="e076c-113">Task</span></span></th>
<th align="left"><span data-ttu-id="e076c-114">Más información</span><span class="sxs-lookup"><span data-stu-id="e076c-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-115">Determinar el ámbito de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e076c-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-116">En función de las aplicaciones que se vayan a virtualizar, la infraestructura de App-V 5,0 se puede configurar de diferentes maneras.</span><span class="sxs-lookup"><span data-stu-id="e076c-116">Depending on the applications to be virtualized, the App-V 5.0 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="e076c-117">La primera tarea es definir qué aplicaciones desea virtualizar.</span><span class="sxs-lookup"><span data-stu-id="e076c-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-118">Determinar el ámbito de ubicación</span><span class="sxs-lookup"><span data-stu-id="e076c-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-119">El ámbito de ubicación hace referencia a las ubicaciones físicas (por ejemplo, en toda la empresa o en una ubicación geográfica específica) donde tiene previsto ejecutar las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="e076c-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="e076c-120">También puede hacer referencia a la población de usuarios (por ejemplo, un único departamento) que ejecutará las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="e076c-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="e076c-121">Debe obtener un mapa de red que incluya las rutas de conexión, así como el ancho de banda disponible para cada ubicación y el número de usuarios que usan aplicaciones virtualizadas y la velocidad de vínculo de WAN.</span><span class="sxs-lookup"><span data-stu-id="e076c-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e076c-122">Determinar qué infraestructura de App-V 5,0 es necesaria</span><span class="sxs-lookup"><span data-stu-id="e076c-122">Determine Which App-V 5.0 Infrastructure is Required</span></span>


<span data-ttu-id="e076c-123">**Importante**  Los dos modelos siguientes requieren que el cliente de App-V 5,0 se instale en el equipo en el que se va a ejecutar aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="e076c-123">**Important** Both of the following models require the App-V 5.0 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="e076c-124">También puede administrar el entorno de App-V 5,0 mediante una solución de distribución de software electrónico (ESD) como Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e076c-124">You can also manage your App-V 5.0 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="e076c-125">Para obtener más información [, consulte implementación de paquetes de App-V 5,0 mediante distribución electrónica de software (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-125">For more information see [Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span></span>

 

-   <span data-ttu-id="e076c-126">**Modelo independiente** : el modelo independiente permite que las aplicaciones virtuales sean Windows Installer habilitadas para su distribución sin transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="e076c-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="e076c-127">App-V 5,0 en modo autónomo consiste en el secuenciador y el cliente; no se necesitan componentes adicionales.</span><span class="sxs-lookup"><span data-stu-id="e076c-127">App-V 5.0 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="e076c-128">Las aplicaciones se preparan para la virtualización mediante un proceso denominado secuencias.</span><span class="sxs-lookup"><span data-stu-id="e076c-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="e076c-129">Para obtener más información, vea [planeación del secuenciador de aplicaciones-V 5,0 e implementación de clientes](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-129">For more information see, [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="e076c-130">Se recomienda usar el modelo independiente para los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="e076c-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="e076c-131">Con usuarios remotos desconectados que no pueden conectarse a la infraestructura de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-131">With disconnected remote users who cannot connect to the App-V 5.0 infrastructure.</span></span>

    -   <span data-ttu-id="e076c-132">Cuando esté ejecutando un sistema de administración de software, como Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="e076c-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="e076c-133">Cuando las limitaciones de ancho de banda de red impiden la distribución electrónica del software.</span><span class="sxs-lookup"><span data-stu-id="e076c-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="e076c-134">**Modelo de infraestructura completa** : el modelo de infraestructura completo proporciona capacidades de distribución, administración y creación de informes de software; también incluye la transmisión de aplicaciones a través de la red.</span><span class="sxs-lookup"><span data-stu-id="e076c-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="e076c-135">El modelo de infraestructura completa de App-V 5,0 consta de uno o varios servidores de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-135">The App-V 5.0 Full Infrastructure Model consists of one or more App-V 5.0 management servers.</span></span> <span data-ttu-id="e076c-136">El servidor de administración se puede usar para publicar aplicaciones en todos los clientes.</span><span class="sxs-lookup"><span data-stu-id="e076c-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="e076c-137">El proceso de publicación coloca los iconos de la aplicación virtual y los accesos directos en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="e076c-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="e076c-138">También puede transmitir aplicaciones a usuarios locales.</span><span class="sxs-lookup"><span data-stu-id="e076c-138">It can also stream applications to local users.</span></span> <span data-ttu-id="e076c-139">Para obtener más información sobre cómo instalar el servidor de administración, consulte [planificación de la implementación del servidor de App-V 5,0](planning-for-the-app-v-50-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-139">For more information about installing the management server see, [Planning for the App-V 5.0 Server Deployment](planning-for-the-app-v-50-server-deployment.md).</span></span> <span data-ttu-id="e076c-140">Se recomienda el modelo de infraestructura completa para los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="e076c-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="e076c-141">**Importante**  El modelo de infraestructura completa de App-V 5,0 requiere que Microsoft SQL Server almacene los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="e076c-141">**Important** The App-V 5.0 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="e076c-142">Para obtener más información [, consulte Configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-142">For more information see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="e076c-143">Cuando desee usar el servidor de administración para publicar la aplicación en equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="e076c-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="e076c-144">Para provisioning rápido de aplicaciones a equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="e076c-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="e076c-145">Cuando quiera usar informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-145">When you want to use App-V 5.0 reporting.</span></span>

## <span data-ttu-id="e076c-146">Guía de tamaño de servidor de principio a fin</span><span class="sxs-lookup"><span data-stu-id="e076c-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="e076c-147">En la siguiente sección, se proporciona información sobre el tamaño y la planeación de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-147">The following section provides information about end-to-end App-V 5.0 sizing and planning.</span></span> <span data-ttu-id="e076c-148">Para obtener información más específica, consulte las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="e076c-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="e076c-149">**Nota:**  El tiempo de respuesta de ida y vuelta en el cliente es el tiempo que tarda el equipo que ejecuta el cliente de App-V 5,0 en recibir una notificación correcta del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.0 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="e076c-150">El tiempo de respuesta de ida y vuelta en el servidor de publicación es el tiempo que tarda el equipo que ejecuta el servidor de publicación para recibir una actualización de metadatos del paquete correcta del servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="e076c-151">los clientes de 20.000 pueden dirigirse a un solo servidor de publicación para obtener la actualización del paquete en un tiempo de ida y vuelta aceptable.</span><span class="sxs-lookup"><span data-stu-id="e076c-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="e076c-152">( &lt; 3 segundos)</span><span class="sxs-lookup"><span data-stu-id="e076c-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="e076c-153">Un solo servidor de administración puede admitir hasta 50 servidores de publicación para actualizaciones de metadatos del paquete en un tiempo de ida y vuelta aceptable.</span><span class="sxs-lookup"><span data-stu-id="e076c-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="e076c-154">( &lt; 5 segundos)</span><span class="sxs-lookup"><span data-stu-id="e076c-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="e076c-155">Recomendaciones de planeación de capacidad del servidor de administración de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-155">App-V 5.0 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="e076c-156">Los servidores de publicación de App-V 5,0 requieren el servidor de administración para las solicitudes de actualización de paquetes y las respuestas de actualización de paquetes.</span><span class="sxs-lookup"><span data-stu-id="e076c-156">The App-V 5.0 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="e076c-157">El servidor de Administración envía entonces la información a la base de datos de administración para recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="e076c-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="e076c-158">Para obtener más información sobre las configuraciones admitidas del servidor de administración de App-V 5,0, consulte [configuraciones admitidas de App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-158">For more information about App-V 5.0 management server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="e076c-159">**Nota:**  El tiempo de actualización predeterminado en el servidor de publicación de App-V 5,0 es de diez minutos.</span><span class="sxs-lookup"><span data-stu-id="e076c-159">**Note** The default refresh time on the App-V 5.0 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="e076c-160">Cuando varios servidores de publicación simultáneos se pongan en contacto con un único servidor de administración de actualizaciones de metadatos del paquete, los tres factores siguientes influirán en el tiempo de respuesta de ida y vuelta en el servidor de publicación:</span><span class="sxs-lookup"><span data-stu-id="e076c-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="e076c-161">Número de servidores de publicación que hacen solicitudes simultáneas.</span><span class="sxs-lookup"><span data-stu-id="e076c-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="e076c-162">Número de grupos de conexión configurados en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="e076c-163">Número de grupos de acceso configurados en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="e076c-164">La siguiente tabla muestra más información sobre cada factor que afecta al tiempo de recorrido de ida y vuelta.</span><span class="sxs-lookup"><span data-stu-id="e076c-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="e076c-165">**Nota:**  El tiempo de respuesta de ida y vuelta es el tiempo que tarda el equipo que ejecuta el servidor de publicación de App-V 5,0 para recibir una actualización de metadatos del paquete correcta del servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-166">Factores que afectan al tiempo de respuesta de ida y vuelta</span><span class="sxs-lookup"><span data-stu-id="e076c-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="e076c-167">Más información</span><span class="sxs-lookup"><span data-stu-id="e076c-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-168">El número de servidores de publicación que solicitan simultáneamente renovaciones de metadatos del paquete.</span><span class="sxs-lookup"><span data-stu-id="e076c-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-169">Un solo servidor de administración puede responder a un máximo de 320 servidores de publicación que solicitan metadatos de publicación al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e076c-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="e076c-170">El tiempo de respuesta de ida y vuelta para servidores pub 320 es de ~ 40 segundos.</span><span class="sxs-lookup"><span data-stu-id="e076c-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="e076c-171">Para &lt; los servidores de publicación de 50 que solicitan metadatos simultáneamente, el tiempo de respuesta de ida y vuelta es de &lt; 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="e076c-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="e076c-172">De 50 a 320 servidores de publicación, el tiempo de respuesta aumenta linealmente (aproximadamente 2x).</span><span class="sxs-lookup"><span data-stu-id="e076c-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-173">El número de grupos de conexión configurados en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-174">En el caso de grupos de conexión de hasta 100, no hay ningún cambio significativo en el tiempo de respuesta de la acción de ida y vuelta en el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="e076c-175">Para los grupos de conexiones 100-400, hay un aumento lineal menor en el tiempo de respuesta de la acción de ida y vuelta.</span><span class="sxs-lookup"><span data-stu-id="e076c-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-176">El número de grupos de acceso configurados en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-177">En el caso de grupos de acceso de hasta 40, hay un aumento lineal (aproximadamente 3x) en el tiempo de respuesta de ida y vuelta en el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-178">En la tabla siguiente se muestran valores de ejemplo para cada uno de los factores anteriores.</span><span class="sxs-lookup"><span data-stu-id="e076c-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="e076c-179">En cada variación, los paquetes de 120 se actualizan desde el servidor de administración de App-V 5.0.</span><span class="sxs-lookup"><span data-stu-id="e076c-179">In each variation, 120 packages are refreshed from the App-V 5.0management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-180">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-181">Variación</span><span class="sxs-lookup"><span data-stu-id="e076c-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="e076c-182">Número de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="e076c-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="e076c-183">Número de grupos de acceso</span><span class="sxs-lookup"><span data-stu-id="e076c-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="e076c-184">Número de servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="e076c-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="e076c-185">Tipo de conexión de red servidor de publicación/servidor de administración</span><span class="sxs-lookup"><span data-stu-id="e076c-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="e076c-186">Tiempo de respuesta de ida y vuelta en el servidor de publicación (en segundos)</span><span class="sxs-lookup"><span data-stu-id="e076c-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="e076c-187">Uso de la CPU en el servidor de administración</span><span class="sxs-lookup"><span data-stu-id="e076c-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-188">Publicar servidores de forma simultánea en el servidor de administración para publicar metadatos.</span><span class="sxs-lookup"><span data-stu-id="e076c-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-189">Número de servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="e076c-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-190">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-190">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-191">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-191">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-192">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-192">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-193">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-193">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-194">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-194">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-195">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-196">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-196">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-197">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-197">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-198">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-198">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-199">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-199">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-200">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-200">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-201">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-202">50</span><span class="sxs-lookup"><span data-stu-id="e076c-202">50</span></span></p></li>
<li><p><span data-ttu-id="e076c-203">100</span><span class="sxs-lookup"><span data-stu-id="e076c-203">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-204">200</span><span class="sxs-lookup"><span data-stu-id="e076c-204">200</span></span></p></li>
<li><p><span data-ttu-id="e076c-205">300</span><span class="sxs-lookup"><span data-stu-id="e076c-205">300</span></span></p></li>
<li><p><span data-ttu-id="e076c-206">315</span><span class="sxs-lookup"><span data-stu-id="e076c-206">315</span></span></p></li>
<li><p><span data-ttu-id="e076c-207">320</span><span class="sxs-lookup"><span data-stu-id="e076c-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-208">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-209">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-210">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-211">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-212">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-213">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-214">4</span><span class="sxs-lookup"><span data-stu-id="e076c-214">5</span></span></p></li>
<li><p><span data-ttu-id="e076c-215">base10</span><span class="sxs-lookup"><span data-stu-id="e076c-215">10</span></span></p></li>
<li><p><span data-ttu-id="e076c-216">19</span><span class="sxs-lookup"><span data-stu-id="e076c-216">19</span></span></p></li>
<li><p><span data-ttu-id="e076c-217">32</span><span class="sxs-lookup"><span data-stu-id="e076c-217">32</span></span></p></li>
<li><p><span data-ttu-id="e076c-218">0,30</span><span class="sxs-lookup"><span data-stu-id="e076c-218">30</span></span></p></li>
<li><p><span data-ttu-id="e076c-219">37</span><span class="sxs-lookup"><span data-stu-id="e076c-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-220">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-220">17</span></span></p></li>
<li><p><span data-ttu-id="e076c-221">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-221">17</span></span></p></li>
<li><p><span data-ttu-id="e076c-222">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-222">17</span></span></p></li>
<li><p><span data-ttu-id="e076c-223">4,5</span><span class="sxs-lookup"><span data-stu-id="e076c-223">15</span></span></p></li>
<li><p><span data-ttu-id="e076c-224">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-224">17</span></span></p></li>
<li><p><span data-ttu-id="e076c-225">4,5</span><span class="sxs-lookup"><span data-stu-id="e076c-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-226">Los metadatos de publicación contienen grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="e076c-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-227">Número de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="e076c-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-228">base10</span><span class="sxs-lookup"><span data-stu-id="e076c-228">10</span></span></p></li>
<li><p><span data-ttu-id="e076c-229">50</span><span class="sxs-lookup"><span data-stu-id="e076c-229">50</span></span></p></li>
<li><p><span data-ttu-id="e076c-230">100</span><span class="sxs-lookup"><span data-stu-id="e076c-230">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-231">150</span><span class="sxs-lookup"><span data-stu-id="e076c-231">150</span></span></p></li>
<li><p><span data-ttu-id="e076c-232">300</span><span class="sxs-lookup"><span data-stu-id="e076c-232">300</span></span></p></li>
<li><p><span data-ttu-id="e076c-233">400</span><span class="sxs-lookup"><span data-stu-id="e076c-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-234">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-234">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-235">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-235">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-236">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-236">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-237">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-237">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-238">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-238">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-239">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-240">100</span><span class="sxs-lookup"><span data-stu-id="e076c-240">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-241">100</span><span class="sxs-lookup"><span data-stu-id="e076c-241">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-242">100</span><span class="sxs-lookup"><span data-stu-id="e076c-242">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-243">100</span><span class="sxs-lookup"><span data-stu-id="e076c-243">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-244">100</span><span class="sxs-lookup"><span data-stu-id="e076c-244">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-245">100</span><span class="sxs-lookup"><span data-stu-id="e076c-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-246">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-247">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-248">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-249">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-250">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-251">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-252">base10</span><span class="sxs-lookup"><span data-stu-id="e076c-252">10</span></span></p></li>
<li><p><span data-ttu-id="e076c-253">once</span><span class="sxs-lookup"><span data-stu-id="e076c-253">11</span></span></p></li>
<li><p><span data-ttu-id="e076c-254">once</span><span class="sxs-lookup"><span data-stu-id="e076c-254">11</span></span></p></li>
<li><p><span data-ttu-id="e076c-255">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-255">16</span></span></p></li>
<li><p><span data-ttu-id="e076c-256">23</span><span class="sxs-lookup"><span data-stu-id="e076c-256">22</span></span></p></li>
<li><p><span data-ttu-id="e076c-257">veinticinco</span><span class="sxs-lookup"><span data-stu-id="e076c-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-258">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-258">17</span></span></p></li>
<li><p><span data-ttu-id="e076c-259">19</span><span class="sxs-lookup"><span data-stu-id="e076c-259">19</span></span></p></li>
<li><p><span data-ttu-id="e076c-260">23</span><span class="sxs-lookup"><span data-stu-id="e076c-260">22</span></span></p></li>
<li><p><span data-ttu-id="e076c-261">19</span><span class="sxs-lookup"><span data-stu-id="e076c-261">19</span></span></p></li>
<li><p><span data-ttu-id="e076c-262">veinte</span><span class="sxs-lookup"><span data-stu-id="e076c-262">20</span></span></p></li>
<li><p><span data-ttu-id="e076c-263">veinte</span><span class="sxs-lookup"><span data-stu-id="e076c-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-264">Los metadatos de publicación contienen grupos de acceso</span><span class="sxs-lookup"><span data-stu-id="e076c-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-265">Número de grupos de acceso</span><span class="sxs-lookup"><span data-stu-id="e076c-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-266">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-266">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-267">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-267">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-268">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-268">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-269">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-270">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-270">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-271">base10</span><span class="sxs-lookup"><span data-stu-id="e076c-271">10</span></span></p></li>
<li><p><span data-ttu-id="e076c-272">veinte</span><span class="sxs-lookup"><span data-stu-id="e076c-272">20</span></span></p></li>
<li><p><span data-ttu-id="e076c-273">40</span><span class="sxs-lookup"><span data-stu-id="e076c-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-274">100</span><span class="sxs-lookup"><span data-stu-id="e076c-274">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-275">100</span><span class="sxs-lookup"><span data-stu-id="e076c-275">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-276">100</span><span class="sxs-lookup"><span data-stu-id="e076c-276">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-277">100</span><span class="sxs-lookup"><span data-stu-id="e076c-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-278">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-279">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-280">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-281">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-282">base10</span><span class="sxs-lookup"><span data-stu-id="e076c-282">10</span></span></p></li>
<li><p><span data-ttu-id="e076c-283">43</span><span class="sxs-lookup"><span data-stu-id="e076c-283">43</span></span></p></li>
<li><p><span data-ttu-id="e076c-284">153</span><span class="sxs-lookup"><span data-stu-id="e076c-284">153</span></span></p></li>
<li><p><span data-ttu-id="e076c-285">535</span><span class="sxs-lookup"><span data-stu-id="e076c-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-286">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-286">17</span></span></p></li>
<li><p><span data-ttu-id="e076c-287">26</span><span class="sxs-lookup"><span data-stu-id="e076c-287">26</span></span></p></li>
<li><p><span data-ttu-id="e076c-288">veinticuatro</span><span class="sxs-lookup"><span data-stu-id="e076c-288">24</span></span></p></li>
<li><p><span data-ttu-id="e076c-289">veinticuatro</span><span class="sxs-lookup"><span data-stu-id="e076c-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-290">La utilización de la CPU del equipo que ejecuta el servidor de administración es de aproximadamente 25%, independientemente del número de servidores de publicación destinados a él.</span><span class="sxs-lookup"><span data-stu-id="e076c-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="e076c-291">Las transacciones de la base de datos de Microsoft SQL Server/sec, las solicitudes de lotes/s y las conexiones de usuario son idénticas independientemente del número de servidores de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="e076c-292">Por ejemplo: transacciones/seg es ~ 30, solicitudes por lotes ~ 200 y User Connect ~ 6.</span><span class="sxs-lookup"><span data-stu-id="e076c-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="e076c-293">Con una implementación geográfica distribuida, en la que el servidor de administración & los servidores de publicación utilizan una red de vínculo de baja velocidad entre ellos, el tiempo de respuesta de ida y vuelta en los servidores de publicación se encuentra dentro de los límites de tiempo aceptables ( &lt; 5 segundos), incluso para solicitudes simultáneas de 100 en un solo servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="e076c-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-294">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-295">Variación</span><span class="sxs-lookup"><span data-stu-id="e076c-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="e076c-296">Número de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="e076c-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="e076c-297">Número de grupos de acceso</span><span class="sxs-lookup"><span data-stu-id="e076c-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="e076c-298">Número de servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="e076c-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="e076c-299">Tipo de conexión de red servidor de publicación/servidor de administración</span><span class="sxs-lookup"><span data-stu-id="e076c-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="e076c-300">Tiempo de respuesta de ida y vuelta en el servidor de publicación (en segundos)</span><span class="sxs-lookup"><span data-stu-id="e076c-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="e076c-301">Uso de la CPU en el servidor de administración</span><span class="sxs-lookup"><span data-stu-id="e076c-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-302">Conexión de red entre el servidor de publicación y el servidor de administración</span><span class="sxs-lookup"><span data-stu-id="e076c-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-303">Red de vínculo lento de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="e076c-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-304">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-304">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-305">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-306">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-306">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-307">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-308">50</span><span class="sxs-lookup"><span data-stu-id="e076c-308">50</span></span></p></li>
<li><p><span data-ttu-id="e076c-309">100</span><span class="sxs-lookup"><span data-stu-id="e076c-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-310">Cable de 1,5 Mbps DSL</span><span class="sxs-lookup"><span data-stu-id="e076c-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="e076c-311">Cable de 1,5 Mbps DSL</span><span class="sxs-lookup"><span data-stu-id="e076c-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-312">cuatro</span><span class="sxs-lookup"><span data-stu-id="e076c-312">4</span></span></p></li>
<li><p><span data-ttu-id="e076c-313">4</span><span class="sxs-lookup"><span data-stu-id="e076c-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-314">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-314">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-315">1</span><span class="sxs-lookup"><span data-stu-id="e076c-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-316">Conexión de red entre el servidor de publicación y el servidor de administración</span><span class="sxs-lookup"><span data-stu-id="e076c-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-317">Red de área local o WIFI</span><span class="sxs-lookup"><span data-stu-id="e076c-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-318">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-318">0</span></span></p></li>
<li><p><span data-ttu-id="e076c-319">,0</span><span class="sxs-lookup"><span data-stu-id="e076c-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-320">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-320">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-321">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-322">100</span><span class="sxs-lookup"><span data-stu-id="e076c-322">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-323">200</span><span class="sxs-lookup"><span data-stu-id="e076c-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-324">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="e076c-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="e076c-325">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="e076c-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-326">once</span><span class="sxs-lookup"><span data-stu-id="e076c-326">11</span></span></p></li>
<li><p><span data-ttu-id="e076c-327">veinte</span><span class="sxs-lookup"><span data-stu-id="e076c-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-328">4,5</span><span class="sxs-lookup"><span data-stu-id="e076c-328">15</span></span></p></li>
<li><p><span data-ttu-id="e076c-329">apartado</span><span class="sxs-lookup"><span data-stu-id="e076c-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-330">Ya sea que el servidor de administración y los servidores de publicación estén conectados a través de una red de vínculo de baja velocidad o una red de alta velocidad, el servidor de administración puede controlar aproximadamente 15.000 solicitudes de actualización de paquetes en 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="e076c-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="e076c-331">Recomendaciones de planeación de capacidad del servidor de creación de informes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-331">App-V 5.0 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="e076c-332">Los clientes de App-V 5,0 envían datos de informes al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="e076c-332">App-V 5.0 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="e076c-333">El servidor de informes registra la información en la base de datos de Microsoft SQL Server y devuelve una notificación correcta al equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.0 client.</span></span> <span data-ttu-id="e076c-334">Para obtener más información sobre las configuraciones admitidas de App-V 5,0 Server, consulte [configuraciones admitidas de App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-334">For more information about App-V 5.0 Reporting Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="e076c-335">**Nota:**  El tiempo de respuesta de ida y vuelta es el tiempo que tarda el equipo que ejecuta el cliente de App-V 5,0 para enviar la información de informes al servidor de informes y recibir una notificación correcta desde el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="e076c-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-336">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-337">Resumen</span><span class="sxs-lookup"><span data-stu-id="e076c-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-338">Varios clientes de App-V 5,0 envían información de informes al servidor de informes de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="e076c-338">Multiple App-V 5.0 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-339">El tiempo de respuesta de ida y vuelta del servidor de informes es de 2,6 segundos para clientes de 500.</span><span class="sxs-lookup"><span data-stu-id="e076c-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="e076c-340">El tiempo de respuesta de ida y vuelta del servidor de informes es de 5,65 segundos para clientes de 1000.</span><span class="sxs-lookup"><span data-stu-id="e076c-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="e076c-341">El tiempo de respuesta de ida y vuelta aumenta de forma lineal dependiendo de la cantidad de clientes.</span><span class="sxs-lookup"><span data-stu-id="e076c-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-342">Solicitudes por segundo procesadas por el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="e076c-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-343">Un único servidor de creación de informes y una única base de datos pueden procesar un máximo de 139 solicitudes por segundo.</span><span class="sxs-lookup"><span data-stu-id="e076c-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="e076c-344">El promedio es solicitudes de 121/segundo.</span><span class="sxs-lookup"><span data-stu-id="e076c-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="e076c-345">Al usar dos servidores de informes en la misma base de datos de Microsoft SQL Server, el promedio de solicitudes/segundo es similar a un único servidor de informes = ~ 127, con un máximo de 278 solicitudes/segundo.</span><span class="sxs-lookup"><span data-stu-id="e076c-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="e076c-346">Un único servidor de informes puede procesar 500 conexiones simultáneas/activas.</span><span class="sxs-lookup"><span data-stu-id="e076c-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="e076c-347">Un único servidor de informes puede procesar un máximo de 1500 conexiones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="e076c-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-348">Base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="e076c-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-349">La contención de bloqueo en el equipo que ejecuta Microsoft SQL Server es el factor que limita la solicitud por segundo.</span><span class="sxs-lookup"><span data-stu-id="e076c-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="e076c-350">El rendimiento y el tiempo de respuesta son independientes del tamaño de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e076c-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-351">**Calculando retraso aleatorio**:</span><span class="sxs-lookup"><span data-stu-id="e076c-351">**Calculating random delay**:</span></span>

<span data-ttu-id="e076c-352">La demora aleatoria especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="e076c-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="e076c-353">Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre **0** y **ReportingRandomDelay** , y esperará la duración especificada antes de enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="e076c-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="e076c-354">Retraso aleatorio = 4 \ \* número de clientes/solicitudes promedio por segundo.</span><span class="sxs-lookup"><span data-stu-id="e076c-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="e076c-355">Ejemplo: para clientes de 500, con solicitudes de 120 por segundo, el retraso aleatorio es 4 \ \* 500/120 = ~ 17 minutos.</span><span class="sxs-lookup"><span data-stu-id="e076c-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="e076c-356">Recomendaciones de planeación de capacidad del servidor de publicación de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-356">App-V 5.0 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="e076c-357">Los equipos que ejecutan el cliente de App-V 5,0 se conectan al servidor de publicación de App-V 5,0 para enviar una solicitud de actualización de publicaciones y recibir una respuesta.</span><span class="sxs-lookup"><span data-stu-id="e076c-357">Computers running the App-V 5.0 client connect to the App-V 5.0 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="e076c-358">El tiempo de respuesta de ida y vuelta se mide en el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-358">Round trip response time is measured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="e076c-359">El tiempo de procesador se mide en el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="e076c-360">Para obtener más información sobre las configuraciones admitidas de App-V 5,0 Server, consulte [configuraciones admitidas de App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e076c-360">For more information about App-V 5.0 Publishing Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="e076c-361">**Importante**  En la siguiente lista se muestran los principales factores que se deben tener en cuenta al configurar el servidor de publicación de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="e076c-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.0 publishing server:</span></span>

-   <span data-ttu-id="e076c-362">El número de clientes que se conectan simultáneamente a un único servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="e076c-363">El número de paquetes de cada actualización.</span><span class="sxs-lookup"><span data-stu-id="e076c-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="e076c-364">El ancho de banda de red disponible en su entorno entre el cliente y el servidor de publicación de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-364">The available network bandwidth in your environment between the client and the App-V 5.0 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-365">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-366">Resumen</span><span class="sxs-lookup"><span data-stu-id="e076c-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-367">Varios clientes de App-V 5,0 se conectan a un único servidor de publicación de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="e076c-367">Multiple App-V 5.0 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-368">Un servidor de publicación que ejecute procesadores de doble núcleo puede responder a la mayoría de los clientes de 5000 que soliciten una actualización de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="e076c-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="e076c-369">Para los clientes de 5000-10000, el servidor de publicación requiere un mínimo de cuatro núcleos.</span><span class="sxs-lookup"><span data-stu-id="e076c-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="e076c-370">Para los clientes de 10000-20000, el servidor de publicación debe tener dos núcleos cuádruples para que los tiempos de respuesta sean más eficientes.</span><span class="sxs-lookup"><span data-stu-id="e076c-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="e076c-371">Un servidor de publicación con un núcleo cuádruple puede actualizar paquetes de 10000 en 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="e076c-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="e076c-372">(Compatible con 10000 clientes simultáneos)</span><span class="sxs-lookup"><span data-stu-id="e076c-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-373">Número de paquetes en cada actualización.</span><span class="sxs-lookup"><span data-stu-id="e076c-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-374">El aumento de la cantidad de paquetes incrementará el tiempo de respuesta ~ 40% (hasta 1000 paquetes).</span><span class="sxs-lookup"><span data-stu-id="e076c-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-375">Red entre el cliente de App-V 5,0 y el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="e076c-375">Network between the App-V 5.0 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-376">En una red de baja velocidad (1,5 Mbps de ancho de banda), se produce un aumento de 97% en el tiempo de respuesta en comparación con la LAN (hasta 1000 usuarios).</span><span class="sxs-lookup"><span data-stu-id="e076c-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-377">**Nota:**  El uso de la CPU de Publishing Server siempre es alto durante el intervalo de tiempo, cuando tiene que procesar solicitudes simultáneas ( &gt; 90% en la mayoría de los casos).</span><span class="sxs-lookup"><span data-stu-id="e076c-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="e076c-378">El servidor de publicación puede controlar ~ 1500 solicitudes de cliente en 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="e076c-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-379">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-380">Variación</span><span class="sxs-lookup"><span data-stu-id="e076c-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="e076c-381">Número de clientes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-381">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="e076c-382">Cantidad de paquetes</span><span class="sxs-lookup"><span data-stu-id="e076c-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="e076c-383">Configuración del procesador en el servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="e076c-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="e076c-384">Servidor de publicación de tipo de conexión de red/App-V 5,0 cliente</span><span class="sxs-lookup"><span data-stu-id="e076c-384">Network connection type publishing server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="e076c-385">Tiempo de ida y vuelta en el cliente de App-V 5,0 (en segundos)</span><span class="sxs-lookup"><span data-stu-id="e076c-385">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="e076c-386">Uso de la CPU en el servidor de publicación (en%)</span><span class="sxs-lookup"><span data-stu-id="e076c-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-387">El cliente de App-V 5,0 envía la solicitud de actualización &amp; de publicaciones y recibe una respuesta, cada solicitud con paquetes de 120</span><span class="sxs-lookup"><span data-stu-id="e076c-387">App-V 5.0 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-388">Cantidad de clientes</span><span class="sxs-lookup"><span data-stu-id="e076c-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-389">100</span><span class="sxs-lookup"><span data-stu-id="e076c-389">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-390">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-390">1000</span></span></p></li>
<li><p><span data-ttu-id="e076c-391">5000</span><span class="sxs-lookup"><span data-stu-id="e076c-391">5000</span></span></p></li>
<li><p><span data-ttu-id="e076c-392">10000</span><span class="sxs-lookup"><span data-stu-id="e076c-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-393">120</span><span class="sxs-lookup"><span data-stu-id="e076c-393">120</span></span></p></li>
<li><p><span data-ttu-id="e076c-394">120</span><span class="sxs-lookup"><span data-stu-id="e076c-394">120</span></span></p></li>
<li><p><span data-ttu-id="e076c-395">120</span><span class="sxs-lookup"><span data-stu-id="e076c-395">120</span></span></p></li>
<li><p><span data-ttu-id="e076c-396">120</span><span class="sxs-lookup"><span data-stu-id="e076c-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-397">Doble núcleo</span><span class="sxs-lookup"><span data-stu-id="e076c-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="e076c-398">Doble núcleo</span><span class="sxs-lookup"><span data-stu-id="e076c-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="e076c-399">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="e076c-400">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-401">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-402">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-403">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-404">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-405">uno</span><span class="sxs-lookup"><span data-stu-id="e076c-405">1</span></span></p></li>
<li><p><span data-ttu-id="e076c-406">1</span><span class="sxs-lookup"><span data-stu-id="e076c-406">2</span></span></p></li>
<li><p><span data-ttu-id="e076c-407">1</span><span class="sxs-lookup"><span data-stu-id="e076c-407">2</span></span></p></li>
<li><p><span data-ttu-id="e076c-408">2</span><span class="sxs-lookup"><span data-stu-id="e076c-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-409">100</span><span class="sxs-lookup"><span data-stu-id="e076c-409">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-410">99</span><span class="sxs-lookup"><span data-stu-id="e076c-410">99</span></span></p></li>
<li><p><span data-ttu-id="e076c-411">89</span><span class="sxs-lookup"><span data-stu-id="e076c-411">89</span></span></p></li>
<li><p><span data-ttu-id="e076c-412">77</span><span class="sxs-lookup"><span data-stu-id="e076c-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-413">Varios paquetes en cada actualización</span><span class="sxs-lookup"><span data-stu-id="e076c-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-414">Cantidad de paquetes</span><span class="sxs-lookup"><span data-stu-id="e076c-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-415">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-415">1000</span></span></p></li>
<li><p><span data-ttu-id="e076c-416">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-417">500</span><span class="sxs-lookup"><span data-stu-id="e076c-417">500</span></span></p></li>
<li><p><span data-ttu-id="e076c-418">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-419">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="e076c-420">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-421">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-422">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-423">1</span><span class="sxs-lookup"><span data-stu-id="e076c-423">2</span></span></p></li>
<li><p><span data-ttu-id="e076c-424">2</span><span class="sxs-lookup"><span data-stu-id="e076c-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-425">92</span><span class="sxs-lookup"><span data-stu-id="e076c-425">92</span></span></p></li>
<li><p><span data-ttu-id="e076c-426">91</span><span class="sxs-lookup"><span data-stu-id="e076c-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-427">Red entre el cliente y el servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="e076c-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-428">red de vínculo lento de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="e076c-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-429">100</span><span class="sxs-lookup"><span data-stu-id="e076c-429">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-430">500</span><span class="sxs-lookup"><span data-stu-id="e076c-430">500</span></span></p></li>
<li><p><span data-ttu-id="e076c-431">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-432">120</span><span class="sxs-lookup"><span data-stu-id="e076c-432">120</span></span></p></li>
<li><p><span data-ttu-id="e076c-433">120</span><span class="sxs-lookup"><span data-stu-id="e076c-433">120</span></span></p></li>
<li><p><span data-ttu-id="e076c-434">120</span><span class="sxs-lookup"><span data-stu-id="e076c-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-435">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="e076c-436">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="e076c-437">Núcleo cuádruple</span><span class="sxs-lookup"><span data-stu-id="e076c-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-438">Red intracontinental de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="e076c-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-439">2</span><span class="sxs-lookup"><span data-stu-id="e076c-439">3</span></span></p></li>
<li><p><span data-ttu-id="e076c-440">10 (con tasa de error de 0,2%)</span><span class="sxs-lookup"><span data-stu-id="e076c-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="e076c-441">17 (con tarifa de error de 1%)</span><span class="sxs-lookup"><span data-stu-id="e076c-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="e076c-442">Recomendaciones de planeación de capacidad de streaming de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-442">App-V 5.0 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="e076c-443">Los equipos que ejecutan el cliente de App-V 5,0 transmiten el paquete de aplicación virtual desde el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e076c-443">Computers running the App-V 5.0 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="e076c-444">El tiempo de respuesta de ida y vuelta se mide en el equipo que ejecuta el cliente de App-V 5,0 y es el tiempo que se tarda en transmitir por secuencias todo el paquete.</span><span class="sxs-lookup"><span data-stu-id="e076c-444">Round trip response time is measured on the computer running the App-V 5.0 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="e076c-445">**Importante**  En la siguiente lista se identifican los principales factores que se deben tener en cuenta al configurar el servidor de streaming de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="e076c-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.0 streaming server:</span></span>

-   <span data-ttu-id="e076c-446">El número de clientes que transmiten paquetes de aplicaciones de forma simultánea desde un único servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e076c-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="e076c-447">El tamaño del paquete que se está transmitiendo.</span><span class="sxs-lookup"><span data-stu-id="e076c-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="e076c-448">El ancho de banda de red disponible en su entorno entre el cliente y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e076c-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-449">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-450">Resumen</span><span class="sxs-lookup"><span data-stu-id="e076c-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-451">Varios clientes de App-V 5,0 transmiten aplicaciones desde un único servidor de transmisión de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="e076c-451">Multiple App-V 5.0 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-452">Si aumenta la cantidad de clientes que se transmiten simultáneamente desde el mismo servidor, existe una relación lineal con el tiempo de descarga/transmisión del paquete.</span><span class="sxs-lookup"><span data-stu-id="e076c-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-453">Tamaño del paquete que se está transmitiendo.</span><span class="sxs-lookup"><span data-stu-id="e076c-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-454">El tamaño del paquete tiene un impacto significativo en el tiempo de transmisión y transferencia para paquetes más grandes con un tamaño de aprox. de 1 GB.</span><span class="sxs-lookup"><span data-stu-id="e076c-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="e076c-455">En el caso de los tamaños de paquetes comprendidos entre 3 MB y 100 MB, los intervalos de tiempo de streaming van de 20 segundos a 100 segundos, con 100 clientes simultáneos.</span><span class="sxs-lookup"><span data-stu-id="e076c-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-456">Red entre el cliente de App-V 5,0 y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e076c-456">Network between the App-V 5.0 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-457">En una red de baja velocidad (1,5 Mbps de ancho de banda), se produce un aumento de 70-80% en el tiempo de respuesta en comparación con la LAN (hasta 100 usuarios).</span><span class="sxs-lookup"><span data-stu-id="e076c-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-458">En la siguiente tabla se muestran valores de ejemplo para cada uno de los factores de la lista anterior:</span><span class="sxs-lookup"><span data-stu-id="e076c-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e076c-459">Escenario</span><span class="sxs-lookup"><span data-stu-id="e076c-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="e076c-460">Variación</span><span class="sxs-lookup"><span data-stu-id="e076c-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="e076c-461">Número de clientes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-461">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="e076c-462">Tamaño de cada paquete</span><span class="sxs-lookup"><span data-stu-id="e076c-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="e076c-463">Tipo de conexión de red de Streaming Server/App-V 5,0 Client</span><span class="sxs-lookup"><span data-stu-id="e076c-463">Network connection type streaming server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="e076c-464">Tiempo de ida y vuelta en el cliente de App-V 5,0 (en segundos)</span><span class="sxs-lookup"><span data-stu-id="e076c-464">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-465">Varios clientes de App-V 5,0 que transmiten paquetes de aplicaciones virtuales desde un servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e076c-465">Multiple App-V 5.0 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-466">Número de clientes.</span><span class="sxs-lookup"><span data-stu-id="e076c-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-467">100</span><span class="sxs-lookup"><span data-stu-id="e076c-467">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-468">200</span><span class="sxs-lookup"><span data-stu-id="e076c-468">200</span></span></p></li>
<li><p><span data-ttu-id="e076c-469">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-470">100</span><span class="sxs-lookup"><span data-stu-id="e076c-470">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-471">200</span><span class="sxs-lookup"><span data-stu-id="e076c-471">200</span></span></p></li>
<li><p><span data-ttu-id="e076c-472">1000</span><span class="sxs-lookup"><span data-stu-id="e076c-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-473">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="e076c-474">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="e076c-475">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-476">5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="e076c-477">5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="e076c-478">5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-479">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-480">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-481">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-482">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-483">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-484">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-485">32</span><span class="sxs-lookup"><span data-stu-id="e076c-485">29</span></span></p></li>
<li><p><span data-ttu-id="e076c-486">39</span><span class="sxs-lookup"><span data-stu-id="e076c-486">39</span></span></p></li>
<li><p><span data-ttu-id="e076c-487">391</span><span class="sxs-lookup"><span data-stu-id="e076c-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-488">35</span><span class="sxs-lookup"><span data-stu-id="e076c-488">35</span></span></p></li>
<li><p><span data-ttu-id="e076c-489">68</span><span class="sxs-lookup"><span data-stu-id="e076c-489">68</span></span></p></li>
<li><p><span data-ttu-id="e076c-490">461</span><span class="sxs-lookup"><span data-stu-id="e076c-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e076c-491">Tamaño de cada paquete que se está transmitiendo.</span><span class="sxs-lookup"><span data-stu-id="e076c-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-492">Tamaño de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="e076c-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-493">100</span><span class="sxs-lookup"><span data-stu-id="e076c-493">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-494">200</span><span class="sxs-lookup"><span data-stu-id="e076c-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-495">100</span><span class="sxs-lookup"><span data-stu-id="e076c-495">100</span></span></p></li>
<li><p><span data-ttu-id="e076c-496">200</span><span class="sxs-lookup"><span data-stu-id="e076c-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-497">21 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="e076c-498">21 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-499">109</span><span class="sxs-lookup"><span data-stu-id="e076c-499">109</span></span></p></li>
<li><p><span data-ttu-id="e076c-500">109</span><span class="sxs-lookup"><span data-stu-id="e076c-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-501">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-502">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-503">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="e076c-504">LAN</span><span class="sxs-lookup"><span data-stu-id="e076c-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="e076c-505">33</span><span class="sxs-lookup"><span data-stu-id="e076c-505">33</span></span></p>
<p><span data-ttu-id="e076c-506">83</span><span class="sxs-lookup"><span data-stu-id="e076c-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="e076c-507">100</span><span class="sxs-lookup"><span data-stu-id="e076c-507">100</span></span></p>
<p><span data-ttu-id="e076c-508">160</span><span class="sxs-lookup"><span data-stu-id="e076c-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e076c-509">Conexión de red entre el cliente y el servidor de streaming de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="e076c-509">Network connection between client and App-V 5.0 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e076c-510">red de vínculo lento de 1,5 Mbps.</span><span class="sxs-lookup"><span data-stu-id="e076c-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-511">100</span><span class="sxs-lookup"><span data-stu-id="e076c-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-512">100</span><span class="sxs-lookup"><span data-stu-id="e076c-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-513">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="e076c-514">5 MB</span><span class="sxs-lookup"><span data-stu-id="e076c-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="e076c-515">Red intracontinental de 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="e076c-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="e076c-516">102</span><span class="sxs-lookup"><span data-stu-id="e076c-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="e076c-517">121</span><span class="sxs-lookup"><span data-stu-id="e076c-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e076c-518">Cada servidor de streaming de App-V 5,0 debe poder administrar un mínimo de 200 clientes que transmitan simultáneamente aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="e076c-518">Each App-V 5.0 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="e076c-519">**Nota:**  El tiempo real que se tardará en transmitirse se determina principalmente por el número de clientes que se transtransmiten simultáneamente, el número de paquetes, el tamaño del paquete, la actividad de la red del servidor y las condiciones de la red.</span><span class="sxs-lookup"><span data-stu-id="e076c-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="e076c-520">Por ejemplo, un usuario promedio puede transmitir un paquete de 100 MB en menos de 2 minutos, cuando se están transmitiendo 100 clientes simultáneos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="e076c-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="e076c-521">Sin embargo, un paquete de tamaño de 1 GB podría demorar hasta 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="e076c-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="e076c-522">En la mayoría de los entornos del mundo real, la demanda por streaming no se distribuye uniformemente, necesitará comprender los requisitos aproximados de transmisión por secuencias máximas presentes en su entorno para ajustar correctamente el número de servidores de streaming requeridos.</span><span class="sxs-lookup"><span data-stu-id="e076c-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="e076c-523">El número de clientes que un servidor de streaming puede mejorar puede aumentar significativamente y los requisitos de transmisión por secuencias máximas disminuyeron si se preguardan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e076c-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="e076c-524">También puede aumentar el número de clientes que un servidor de transmisión puede admitir mediante la entrega de flujo a petición y los paquetes optimizados por secuencias.</span><span class="sxs-lookup"><span data-stu-id="e076c-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="e076c-525">Aplicación de los roles de servidor de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="e076c-525">Combining App-V 5.0 Server Roles</span></span>


<span data-ttu-id="e076c-526">Descuentos en los requisitos de escala y tolerancia a errores, la cantidad mínima de servidores necesarios para una ubicación con conectividad a Active Directory es una.</span><span class="sxs-lookup"><span data-stu-id="e076c-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="e076c-527">Este servidor hospedará el servidor de administración, el servicio servidor de administración y los roles de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e076c-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="e076c-528">Los roles de servidor, por lo tanto, se pueden organizar en cualquier combinación deseada, ya que no entran en conflicto entre sí.</span><span class="sxs-lookup"><span data-stu-id="e076c-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="e076c-529">Si se omiten los requisitos de escala, la cantidad mínima de servidores necesarios para proporcionar una implementación tolerante a errores es de cuatro.</span><span class="sxs-lookup"><span data-stu-id="e076c-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="e076c-530">El servidor de administración y la compatibilidad con los roles de Microsoft SQL Server se colocan en configuraciones tolerantes a errores.</span><span class="sxs-lookup"><span data-stu-id="e076c-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="e076c-531">El servicio servidor de administración se puede combinar con cualquiera de los roles, pero sigue siendo un punto único de error.</span><span class="sxs-lookup"><span data-stu-id="e076c-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="e076c-532">Aunque hay varias estrategias y tecnologías de tolerancia a errores disponibles, no todas son aplicables a un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="e076c-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="e076c-533">Además, si se combinan los roles de 5,0 de App-V, es posible que determinadas opciones de tolerancia a errores dejen de aplicarse debido a incompatibilidades.</span><span class="sxs-lookup"><span data-stu-id="e076c-533">Additionally, if App-V 5.0 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="e076c-534">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e076c-534">Related topics</span></span>


[<span data-ttu-id="e076c-535">Consideraciones compatibles con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e076c-535">App-V 5.0 Supported Configurations</span></span>](app-v-50-supported-configurations.md)

[<span data-ttu-id="e076c-536">Planeación para la alta disponibilidad con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e076c-536">Planning for High Availability with App-V 5.0</span></span>](planning-for-high-availability-with-app-v-50.md)

[<span data-ttu-id="e076c-537">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="e076c-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





