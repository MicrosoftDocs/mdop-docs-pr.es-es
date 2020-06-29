---
title: Introducción a App-V 5.0
description: Introducción a App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814551"
---
# <span data-ttu-id="b410c-103">Introducción a App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-103">Getting Started with App-V 5.0</span></span>


<span data-ttu-id="b410c-104">App-V 5,0 permite a los administradores implementar, actualizar y admitir aplicaciones como servicios en tiempo real, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b410c-104">App-V 5.0 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="b410c-105">Las aplicaciones individuales se transforman de productos instalados de forma local en servicios administrados de forma centralizada y están disponibles dondequiera que lo necesite, sin necesidad de preconfigurar equipos ni de cambiar la configuración del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b410c-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="b410c-106">App-V consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b410c-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b410c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b410c-107">Element</span></span></th>
<th align="left"><span data-ttu-id="b410c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b410c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b410c-109">Servidor de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="b410c-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b410c-110">Proporciona una ubicación central para administrar la infraestructura de App-V, que proporciona aplicaciones virtuales al cliente de escritorio de App-V y al cliente de servicios de escritorio remoto (anteriormente Terminal Services).</span><span class="sxs-lookup"><span data-stu-id="b410c-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="b410c-111">Usa Microsoft SQL Server® para su almacén de datos, en la que uno o varios servidores de administración de App-V pueden compartir un único almacén de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b410c-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="b410c-112">Autentica las solicitudes y proporciona seguridad, medición, supervisión y recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="b410c-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="b410c-113">El servidor usa Active Directory y herramientas de soporte para administrar usuarios y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b410c-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="b410c-114">Tiene un sitio de administración basado en Silverlight®, que le permite configurar la infraestructura de App-V desde cualquier equipo.</span><span class="sxs-lookup"><span data-stu-id="b410c-114">Has a Silverlight®-based management site, which enables you to configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="b410c-115">Puede Agregar y quitar aplicaciones, manipular accesos directos, asignar permisos de acceso a usuarios y grupos, y crear grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="b410c-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="b410c-116">Permite la comunicación entre la consola de administración web de App-V y la tienda de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b410c-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="b410c-117">Estos componentes se pueden instalar en un único equipo servidor o en uno o más equipos independientes, en función de la arquitectura del sistema requerida.</span><span class="sxs-lookup"><span data-stu-id="b410c-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b410c-118">Servidor de publicación de App-V</span><span class="sxs-lookup"><span data-stu-id="b410c-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b410c-119">Proporciona clientes de App-V con aplicaciones tituladas para el usuario específico.</span><span class="sxs-lookup"><span data-stu-id="b410c-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="b410c-120">Hospeda el paquete de aplicación virtual para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="b410c-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b410c-121">Cliente de escritorio de App-V</span><span class="sxs-lookup"><span data-stu-id="b410c-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b410c-122">Recupera aplicaciones virtuales</span><span class="sxs-lookup"><span data-stu-id="b410c-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="b410c-123">Publica las aplicaciones en los clientes.</span><span class="sxs-lookup"><span data-stu-id="b410c-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="b410c-124">Configura y administra automáticamente entornos virtuales en tiempo de ejecución en puntos de conexión de Windows.</span><span class="sxs-lookup"><span data-stu-id="b410c-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="b410c-125">Almacena la configuración de la aplicación virtual específica del usuario, como cambios de archivo y registro, en cada perfil de usuario&#39;s.</span><span class="sxs-lookup"><span data-stu-id="b410c-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b410c-126">Cliente de servicios de escritorio remoto (RDS) de App-V</span><span class="sxs-lookup"><span data-stu-id="b410c-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="b410c-127">Permite que los servidores host de sesión de escritorio remoto usen las funciones del cliente de escritorio de App-V para sesiones de escritorio compartidas.</span><span class="sxs-lookup"><span data-stu-id="b410c-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b410c-128">Secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="b410c-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b410c-129">Es una herramienta basada en un asistente que se usa para transformar las aplicaciones tradicionales en aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b410c-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="b410c-130">Genera la aplicación "paquete", que consta de:</span><span class="sxs-lookup"><span data-stu-id="b410c-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="b410c-131">un archivo de aplicación de secuencia (APPV)</span><span class="sxs-lookup"><span data-stu-id="b410c-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="b410c-132">un archivo de Windows Installer (MSI) que se puede implementar en clientes configurados para un funcionamiento independiente</span><span class="sxs-lookup"><span data-stu-id="b410c-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="b410c-133">Varios archivos XML, entre los que se incluyen Report.XML, PackageName_DeploymentConfig.XML y PackageName_UserConfig.XML.</span><span class="sxs-lookup"><span data-stu-id="b410c-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="b410c-134">Los archivos XML UserConfig y DeploymentConfig se usan para configurar cambios personalizados en el comportamiento predeterminado del paquete.</span><span class="sxs-lookup"><span data-stu-id="b410c-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b410c-135">Para obtener más información sobre estos elementos, consulte [arquitectura de alto nivel para App-V 5,0](high-level-architecture-for-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="b410c-135">For more information about these elements, see [High Level Architecture for App-V 5.0](high-level-architecture-for-app-v-50.md).</span></span>

<span data-ttu-id="b410c-136">Si es nuevo en este producto, le recomendamos que lea la documentación minuciosamente.</span><span class="sxs-lookup"><span data-stu-id="b410c-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="b410c-137">Antes de implementarlo en un entorno de producción, también le recomendamos que valide el plan de implementación en un entorno de red de prueba.</span><span class="sxs-lookup"><span data-stu-id="b410c-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="b410c-138">También puede considerar tomar una clase sobre tecnologías relevantes.</span><span class="sxs-lookup"><span data-stu-id="b410c-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="b410c-139">Para obtener más información sobre las oportunidades de aprendizaje de Microsoft, consulte la descripción general de aprendizaje de Microsoft en <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="b410c-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="b410c-140">**Nota:**  Una versión descargable de esta guía del administrador no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b410c-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="b410c-141">Sin embargo, puede obtener información sobre un modo especial de la biblioteca de TechNet que le permite seleccionar artículos, agruparlos en una colección e imprimirlos o exportarlos a un archivo en <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="b410c-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="b410c-142">Esta sección de la guía del administrador de la 5,0 de App-V incluye información de alto nivel sobre App-V 5,0 para proporcionarle una comprensión básica del producto antes de comenzar con el plan de implementación.</span><span class="sxs-lookup"><span data-stu-id="b410c-142">This section of the App-V 5.0 Administrator’s Guide includes high-level information about App-V 5.0 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="b410c-143">Introducción a App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b410c-143">Getting started with App-V 5.0</span></span>


-   [<span data-ttu-id="b410c-144">Acerca de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-144">About App-V 5.0</span></span>](about-app-v-50.md)

    <span data-ttu-id="b410c-145">Proporciona una descripción general de App-V 5,0 y cómo se puede usar en su organización.</span><span class="sxs-lookup"><span data-stu-id="b410c-145">Provides a high-level overview of App-V 5.0 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="b410c-146">Acerca de App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="b410c-146">About App-V 5.0 SP1</span></span>](about-app-v-50-sp1.md)

    <span data-ttu-id="b410c-147">Proporciona una descripción general de App-V 5.0 SP1 y de cómo se puede usar en su organización.</span><span class="sxs-lookup"><span data-stu-id="b410c-147">Provides a high-level overview of App-V 5.0SP1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="b410c-148">Acerca de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="b410c-148">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

    <span data-ttu-id="b410c-149">Proporciona una descripción general de App-V 5.0 SP2 y de cómo se puede usar en su organización.</span><span class="sxs-lookup"><span data-stu-id="b410c-149">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="b410c-150">Acerca de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="b410c-150">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

    <span data-ttu-id="b410c-151">Proporciona una descripción general de App-V 5.0 SP2 y de cómo se puede usar en su organización.</span><span class="sxs-lookup"><span data-stu-id="b410c-151">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="b410c-152">Evaluación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-152">Evaluating App-V 5.0</span></span>](evaluating-app-v-50.md)

    <span data-ttu-id="b410c-153">Proporciona información sobre cómo puede evaluar mejor App-V 5,0 para usarlo en su organización.</span><span class="sxs-lookup"><span data-stu-id="b410c-153">Provides information about how you can best evaluate App-V 5.0 for use in your organization.</span></span>

-   [<span data-ttu-id="b410c-154">Arquitectura de alto nivel de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-154">High Level Architecture for App-V 5.0</span></span>](high-level-architecture-for-app-v-50.md)

    <span data-ttu-id="b410c-155">Proporciona una descripción de las características de App-V 5,0 y cómo funcionan conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="b410c-155">Provides a description of the App-V 5.0 features and how they work together.</span></span>

-   [<span data-ttu-id="b410c-156">Accesibilidad para App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-156">Accessibility for App-V 5.0</span></span>](accessibility-for-app-v-50.md)

    <span data-ttu-id="b410c-157">Proporciona información sobre características y servicios que hacen que este producto y la documentación correspondiente sean más accesibles para las personas con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="b410c-157">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="b410c-158">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="b410c-158">Other resources for this product</span></span>


-   [<span data-ttu-id="b410c-159">Guía del administrador de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b410c-159">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="b410c-160">Planificación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-160">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

-   [<span data-ttu-id="b410c-161">Implementación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-161">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

-   [<span data-ttu-id="b410c-162">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-162">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

-   [<span data-ttu-id="b410c-163">Resolución de problemas de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b410c-163">Troubleshooting App-V 5.0</span></span>](troubleshooting-app-v-50.md)






 

 





