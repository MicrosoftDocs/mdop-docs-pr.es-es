---
title: Implementación del servidor de App-V 5.0
description: Implementación del servidor de App-V 5.0
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814574"
---
# <span data-ttu-id="a6cbf-103">Implementación del servidor de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-103">Deploying the App-V 5.0 Server</span></span>


<span data-ttu-id="a6cbf-104">Puede instalar las características de servidor de App-V 5,0 con diferentes configuraciones de implementación, que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-104">You can install the App-V 5.0 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="a6cbf-105">Antes de instalar las características de servidor, revise la sección servidor de [consideraciones de seguridad de App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="a6cbf-105">Before you install the server features, review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

<span data-ttu-id="a6cbf-106">Para obtener información sobre cómo implementar el servidor de App-V 5,0 SP3, consulte [acerca de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="a6cbf-106">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

<span data-ttu-id="a6cbf-107">**Importante**  Antes de instalar y configurar los servidores de App-V 5,0, debe especificar un puerto en el que se hospedará cada componente.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-107">**Important** Before you install and configure the App-V 5.0 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="a6cbf-108">También debe agregar las reglas de Firewall asociadas para permitir que las solicitudes entrantes tengan acceso a los puertos especificados.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="a6cbf-109">El instalador no modifica la configuración del firewall.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-109">The installer does not modify firewall settings.</span></span>

 

## <a href="" id="---------app-v-5-0-server-overview"></a> <span data-ttu-id="a6cbf-110">Información general de App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="a6cbf-110">App-V 5.0 Server overview</span></span>


<span data-ttu-id="a6cbf-111">El servidor de App-V 5,0 está formado por cinco componentes.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-111">The App-V 5.0 Server is made up of five components.</span></span> <span data-ttu-id="a6cbf-112">Cada componente tiene un propósito diferente dentro del entorno de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-112">Each component serves a different purpose within the App-V 5.0 environment.</span></span> <span data-ttu-id="a6cbf-113">Cada uno de los cinco componentes se describe brevemente aquí:</span><span class="sxs-lookup"><span data-stu-id="a6cbf-113">Each of the five components is briefly described here:</span></span>

-   <span data-ttu-id="a6cbf-114">Servidor de administración: proporciona funcionalidad de administración general para la infraestructura de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-114">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="a6cbf-115">Base de datos de administración: facilita las preimplementaciones de base de datos para la administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-115">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="a6cbf-116">Publishing Server: proporciona funcionalidad de hospedaje y transmisión por secuencias para aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="a6cbf-117">Servidor de informes: proporciona App-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-117">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="a6cbf-118">Base de datos de informes: facilita las preimplementaciones de base de datos para informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-118">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> <span data-ttu-id="a6cbf-119">Implementación independiente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-119">App-V 5.0 stand-alone deployment</span></span>


<span data-ttu-id="a6cbf-120">La implementación de App-V 5,0 independiente proporciona una topología adecuada para una implementación pequeña o un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-120">The App-V 5.0 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="a6cbf-121">Al usar este tipo de implementación, todos los componentes de servidor se implementan en un solo equipo.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="a6cbf-122">Los servicios y las bases de datos asociadas competirán por los recursos en el equipo que ejecuta los componentes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.0 components.</span></span> <span data-ttu-id="a6cbf-123">Por lo tanto, no debe usar esta topología para implementaciones más grandes.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="a6cbf-124">Cómo implementar el servidor de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-124">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)

[<span data-ttu-id="a6cbf-125">Cómo implementar el servidor de App-V 5.0 mediante un script</span><span class="sxs-lookup"><span data-stu-id="a6cbf-125">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> <span data-ttu-id="a6cbf-126">Implementación distribuida de App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="a6cbf-126">App-V 5.0 Server distributed deployment</span></span>


<span data-ttu-id="a6cbf-127">La topología de implementación distribuida puede admitir una gran base de aplicaciones de la aplicación-V 5,0 cliente y le permite administrar y escalar el entorno más fácilmente.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-127">The distributed deployment topology can support a large App-V 5.0 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="a6cbf-128">Al usar este tipo de implementación, los componentes de servidor de App-V 5,0 se implementan en varios equipos, en función de la estructura y los requisitos de la organización.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-128">When you use this type of deployment, the App-V 5.0 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="a6cbf-129">Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración</span><span class="sxs-lookup"><span data-stu-id="a6cbf-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="a6cbf-130">Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="a6cbf-130">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[<span data-ttu-id="a6cbf-131">Cómo implementar el servidor de App-V 5.0 mediante un script</span><span class="sxs-lookup"><span data-stu-id="a6cbf-131">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="a6cbf-132">Cómo instalar el servidor de publicación en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="a6cbf-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="a6cbf-133">Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="a6cbf-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## <span data-ttu-id="a6cbf-134">Usar una solución de distribución de software para empresas (ESD) y App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.0</span></span>


<span data-ttu-id="a6cbf-135">También puede implementar los clientes y paquetes de App-V 5,0 con un ESD sin tener que implementar App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-135">You can also deploy the App-V 5.0 clients and packages by using an ESD without having to deploy App-V 5.0.</span></span> <span data-ttu-id="a6cbf-136">Las capacidades completas de integración varían según el ESD que uses.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

<span data-ttu-id="a6cbf-137">**Nota:**  El servidor de informes de App-V 5,0 y la base de datos de informes aún pueden implementarse junto con ESD para recopilar los datos de informes de los clientes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-137">**Note** The App-V 5.0 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.0 clients.</span></span> <span data-ttu-id="a6cbf-138">Sin embargo, los otros tres componentes del servidor no deben implementarse porque entrarán en conflicto con la funcionalidad de ESD.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

 

[<span data-ttu-id="a6cbf-139">Implementación de paquetes de App-V 5.0 mediante la distribución de software electrónica (ESD)</span><span class="sxs-lookup"><span data-stu-id="a6cbf-139">Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> <span data-ttu-id="a6cbf-140">Registros de servidor de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-140">App-V 5.0 Server logs</span></span>


<span data-ttu-id="a6cbf-141">Puede usar la información de registro de App-V 5,0 Server para ayudarle a solucionar problemas de instalación del servidor y los eventos operativos al usar App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-141">You can use App-V 5.0 server log information to help troubleshoot the server installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="a6cbf-142">La información de registro relacionada con el servidor puede revisarse con el **visor de eventos**.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="a6cbf-143">La siguiente línea muestra la ruta de acceso específica de los eventos relacionados con el servidor:</span><span class="sxs-lookup"><span data-stu-id="a6cbf-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="a6cbf-144">Visor de eventos \ \ aplicaciones y servicios registros \ \ Microsoft \ \ aplicación V</span><span class="sxs-lookup"><span data-stu-id="a6cbf-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="a6cbf-145">Los registros de configuración asociados se guardan en el siguiente directorio:</span><span class="sxs-lookup"><span data-stu-id="a6cbf-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="a6cbf-146">dicha</span><span class="sxs-lookup"><span data-stu-id="a6cbf-146">%temp%</span></span>**

<span data-ttu-id="a6cbf-147">En App-V 5,0 SP3, se han consolidado algunos registros y se han movido.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-147">In App-V 5.0 SP3, some logs have been consolidated and moved.</span></span> <span data-ttu-id="a6cbf-148">Consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="a6cbf-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-0-reporting"></a> <span data-ttu-id="a6cbf-149">Informes de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-149">App-V 5.0 reporting</span></span>


<span data-ttu-id="a6cbf-150">Los informes de App-V 5,0 permiten a los clientes de App-V 5,0 recopilar datos y, a continuación, enviarlos de nuevo para que se almacenen en un repositorio central.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-150">App-V 5.0 reporting allows App-V 5.0 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="a6cbf-151">Puede usar esta información para obtener una mejor vista del uso de aplicaciones virtuales dentro de su organización.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="a6cbf-152">En la siguiente lista se muestran algunos de los tipos de información que recopila el cliente de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="a6cbf-152">The following list displays some of the types of information the App-V 5.0 client collects:</span></span>

-   <span data-ttu-id="a6cbf-153">Información sobre el equipo que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-153">Information about the computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="a6cbf-154">Información sobre paquetes virtualizados en un equipo específico que ejecuta el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-154">Information about virtualized packages on a specific computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="a6cbf-155">Información sobre la apertura y el cierre de paquetes para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="a6cbf-156">La información de los informes se mantendrá hasta que se envíe correctamente a la base de datos del servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="a6cbf-157">Una vez que los datos están en la base de datos, puede usar Microsoft SQL Server Reporting Services para generar los informes necesarios.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="a6cbf-158">Si desea recuperar información de un informe, debe usar Microsoft SQL Server Reporting Services (SSRS), que está disponible con Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="a6cbf-159">SSRS no se instala al instalar el servidor de informes de App-V 5,0 y debe implementarse por separado para generar los informes asociados.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-159">SSRS is not installed when you install the App-V 5.0 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="a6cbf-160">Use el siguiente vínculo para obtener más información [sobre los informes de App-V 5,0](about-app-v-50-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="a6cbf-160">Use the following link for more information [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>

[<span data-ttu-id="a6cbf-161">Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6cbf-161">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## <span data-ttu-id="a6cbf-162">Otros recursos para el servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="a6cbf-162">Other resources for the App-V server</span></span>


[<span data-ttu-id="a6cbf-163">Implementación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a6cbf-163">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)






 

 




