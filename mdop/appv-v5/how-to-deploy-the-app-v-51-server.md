---
title: Cómo implementar el servidor de App-V 5.1
description: Cómo implementar el servidor de App-V 5.1
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814134"
---
# <span data-ttu-id="90c95-103">Cómo implementar el servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="90c95-103">How to Deploy the App-V 5.1 Server</span></span>


<span data-ttu-id="90c95-104">Use el siguiente procedimiento para instalar el servidor de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="90c95-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 server.</span></span> <span data-ttu-id="90c95-105">Para obtener información sobre cómo implementar el servidor de App-V 5,1, consulte [acerca de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).</span><span class="sxs-lookup"><span data-stu-id="90c95-105">For information about deploying the App-V 5.1 Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

**<span data-ttu-id="90c95-106">Antes de empezar:</span><span class="sxs-lookup"><span data-stu-id="90c95-106">Before you start:</span></span>**

-   <span data-ttu-id="90c95-107">Asegúrese de que ha instalado el software necesario.</span><span class="sxs-lookup"><span data-stu-id="90c95-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="90c95-108">Consulte [requisitos previos de App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="90c95-108">See [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

-   <span data-ttu-id="90c95-109">Revise la sección de servidor de [consideraciones de seguridad de App-V 5,1](app-v-51-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="90c95-109">Review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

-   <span data-ttu-id="90c95-110">Especifique un puerto en el que se hospedará cada componente.</span><span class="sxs-lookup"><span data-stu-id="90c95-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="90c95-111">Agregar reglas de Firewall para permitir que las solicitudes entrantes tengan acceso a los puertos especificados.</span><span class="sxs-lookup"><span data-stu-id="90c95-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="90c95-112">Si usa secuencias de comandos SQL, en lugar de Windows Installer, para configurar la base de datos de administración o la base de datos de informes, debe ejecutar las secuencias de comandos SQL antes de instalar el servidor de administración o el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="90c95-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="90c95-113">Vea [cómo implementar las bases de datos de App-V con scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="90c95-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

**<span data-ttu-id="90c95-114">Para instalar el servidor de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="90c95-114">To install the App-V 5.1 server</span></span>**

1. <span data-ttu-id="90c95-115">Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="90c95-115">Copy the App-V 5.1 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="90c95-116">Para iniciar la instalación del servidor de App-V 5,1, haga clic con el botón secundario en **appv\_server\_setup.exe** como administrador y, a continuación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="90c95-116">Start the App-V 5.1 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="90c95-117">Revise y acepte los términos de licencia y elija si desea habilitar las actualizaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="90c95-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="90c95-118">En la página **selección de características** , seleccione todos los componentes siguientes.</span><span class="sxs-lookup"><span data-stu-id="90c95-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="90c95-119">Componente</span><span class="sxs-lookup"><span data-stu-id="90c95-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="90c95-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="90c95-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="90c95-121">Servidor de administración</span><span class="sxs-lookup"><span data-stu-id="90c95-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-122">Proporciona funcionalidad de administración general para la infraestructura de App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="90c95-123">Base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="90c95-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-124">Facilita las preimplementaciones de base de datos para administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="90c95-125">Servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="90c95-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-126">Proporciona funcionalidades de hospedaje y transmisión por secuencias para aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="90c95-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="90c95-127">Servidor de informes</span><span class="sxs-lookup"><span data-stu-id="90c95-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-128">Proporciona App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="90c95-128">Provides App-V 5.1 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="90c95-129">Base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="90c95-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-130">Facilita las preimplementaciones de base de datos para informes de App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="90c95-131">En la página **Ubicación de instalación** , acepte la ubicación predeterminada en la que se instalarán los componentes seleccionados, o bien cambie la ubicación escribiendo una nueva ruta en la línea de ubicación de **instalación** .</span><span class="sxs-lookup"><span data-stu-id="90c95-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="90c95-132">En la página inicial **crear nueva base de datos de administración** , configure la instancia de **Microsoft SQL Server** y la **base de datos del servidor de administración** seleccionando la opción correspondiente a continuación.</span><span class="sxs-lookup"><span data-stu-id="90c95-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="90c95-133">Método</span><span class="sxs-lookup"><span data-stu-id="90c95-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="90c95-134">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="90c95-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="90c95-135">Está usando una instancia personalizada de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90c95-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-136">Seleccione <strong> usar la instancia personalizada </strong> y escriba el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="90c95-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="90c95-137">Use el formato <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="90c95-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="90c95-138">La ubicación de instalación asumida es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="90c95-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="90c95-139">No compatible: un nombre de servidor con el formato <strong> ServerName </strong> &lt; &gt; Instance </strong> .</span><span class="sxs-lookup"><span data-stu-id="90c95-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="90c95-140">Está usando un nombre de base de datos personalizado.</span><span class="sxs-lookup"><span data-stu-id="90c95-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-141">Seleccione <strong> Configuración personalizada </strong> y escriba el nombre de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="90c95-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="90c95-142">El nombre de la base de datos debe ser único o se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="90c95-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="90c95-143">En la página **configurar** , acepte el valor predeterminado **use este equipo local**.</span><span class="sxs-lookup"><span data-stu-id="90c95-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="90c95-144">Nota</span><span class="sxs-lookup"><span data-stu-id="90c95-144">Note</span></span>**  
   <span data-ttu-id="90c95-145">Si va a instalar el servidor de administración y la base de datos de administración en paralelo, algunas opciones de esta página no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="90c95-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="90c95-146">En este caso, las opciones adecuadas se seleccionan de forma predeterminada y no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="90c95-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="90c95-147">En la página inicial **crear nueva base de datos de informes** , configure la instancia de **Microsoft SQL Server** y la **base de datos del servidor de informes** seleccionando la opción correspondiente a continuación.</span><span class="sxs-lookup"><span data-stu-id="90c95-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="90c95-148">Método</span><span class="sxs-lookup"><span data-stu-id="90c95-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="90c95-149">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="90c95-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="90c95-150">Está usando una instancia personalizada de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90c95-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-151">Seleccione <strong> usar la instancia personalizada </strong> y escriba el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="90c95-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="90c95-152">Use el formato <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="90c95-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="90c95-153">La ubicación de instalación asumida es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="90c95-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="90c95-154">No compatible: un nombre de servidor con el formato <strong> ServerName </strong> &lt; &gt; Instance </strong> .</span><span class="sxs-lookup"><span data-stu-id="90c95-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="90c95-155">Está usando un nombre de base de datos personalizado.</span><span class="sxs-lookup"><span data-stu-id="90c95-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="90c95-156">Seleccione <strong> Configuración personalizada </strong> y escriba el nombre de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="90c95-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="90c95-157">El nombre de la base de datos debe ser único o se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="90c95-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="90c95-158">En la página **configurar** , acepte el valor predeterminado: **usar este equipo local**.</span><span class="sxs-lookup"><span data-stu-id="90c95-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="90c95-159">Nota</span><span class="sxs-lookup"><span data-stu-id="90c95-159">Note</span></span>**  
   <span data-ttu-id="90c95-160">Si va a instalar el servidor de administración y la base de datos de administración en paralelo, algunas opciones de esta página no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="90c95-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="90c95-161">En este caso, las opciones adecuadas se seleccionan de forma predeterminada y no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="90c95-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="90c95-162">En la página **configurar** (configuración del servidor de administración), especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="90c95-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="90c95-163">Elemento para configurar</span><span class="sxs-lookup"><span data-stu-id="90c95-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="90c95-164">Descripción y ejemplos</span><span class="sxs-lookup"><span data-stu-id="90c95-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="90c95-165">Escriba el grupo de AD con permisos suficientes para administrar el entorno de App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-166">Ejemplo: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="90c95-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="90c95-167">Después de la instalación, puede Agregar usuarios o grupos adicionales mediante la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="90c95-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="90c95-168">Sin embargo, los grupos de seguridad global y los grupos de distribución de servicios de dominio de Active Directory (AD DS) no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="90c95-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="90c95-169"><strong> </strong> <strong> Para realizar esta acción, es necesario usar grupos universales o locales </strong> de dominio.</span><span class="sxs-lookup"><span data-stu-id="90c95-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="90c95-170">Nombre del sitio Web </strong> : especifique el nombre personalizado que se usará para ejecutar el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="90c95-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-171">Si no tiene un nombre personalizado, no realice ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="90c95-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="90c95-172">Enlace de puerto </strong> : especifique un número de puerto único que será usado por App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-173">Ejemplo: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="90c95-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="90c95-174">Asegúrate de que el puerto especificado no esté siendo usado por otro sitio Web.</span><span class="sxs-lookup"><span data-stu-id="90c95-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="90c95-175">En la página **configurar** **Publishing Server** , especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="90c95-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="90c95-176">Elemento para configurar</span><span class="sxs-lookup"><span data-stu-id="90c95-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="90c95-177">Descripción y ejemplos</span><span class="sxs-lookup"><span data-stu-id="90c95-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="90c95-178">Especifique la dirección URL para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="90c95-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-179">Ejemplo<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="90c95-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="90c95-180">Nombre del sitio Web </strong> : especifique el nombre personalizado que se usará para ejecutar el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="90c95-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-181">Si no tiene un nombre personalizado, no realice ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="90c95-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="90c95-182">Enlace de puerto </strong> : especifique un número de puerto único que será usado por App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-183">Ejemplo: 54321</span><span class="sxs-lookup"><span data-stu-id="90c95-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="90c95-184">Asegúrate de que el puerto especificado no esté siendo usado por otro sitio Web.</span><span class="sxs-lookup"><span data-stu-id="90c95-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="90c95-185">En la página **servidor de informes** , especifique lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="90c95-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="90c95-186">Elemento para configurar</span><span class="sxs-lookup"><span data-stu-id="90c95-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="90c95-187">Descripción y ejemplos</span><span class="sxs-lookup"><span data-stu-id="90c95-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="90c95-188">Nombre del sitio Web </strong> : especifique el nombre personalizado que se usará para ejecutar el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="90c95-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-189">Si no tiene un nombre personalizado, no realice ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="90c95-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="90c95-190">Enlace de puerto </strong> : especifique un número de puerto único que será usado por App-V.</span><span class="sxs-lookup"><span data-stu-id="90c95-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="90c95-191">Ejemplo: 55555</span><span class="sxs-lookup"><span data-stu-id="90c95-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="90c95-192">Asegúrate de que el puerto especificado no esté siendo usado por otro sitio Web.</span><span class="sxs-lookup"><span data-stu-id="90c95-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="90c95-193">Para iniciar la instalación, haga clic en **instalar** en la página **listo** y, a continuación, haga clic en **cerrar** en la página **finalizada** .</span><span class="sxs-lookup"><span data-stu-id="90c95-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="90c95-194">Para comprobar que la configuración se completó correctamente, abra un explorador Web y escriba la siguiente dirección URL:</span><span class="sxs-lookup"><span data-stu-id="90c95-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="90c95-195">**http:// &lt; Nombre del equipo servidor de administración &gt; : &lt; número de puerto del servicio de administración &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="90c95-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="90c95-196">Ejemplo: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="90c95-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="90c95-197">Si la instalación se realizó correctamente, se muestra la consola de administración de App-V sin errores.</span><span class="sxs-lookup"><span data-stu-id="90c95-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="90c95-198">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="90c95-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="90c95-199">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="90c95-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="90c95-200">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="90c95-200">Got an App-V issue?</span></span>** <span data-ttu-id="90c95-201">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="90c95-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="90c95-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90c95-202">Related topics</span></span>


[<span data-ttu-id="90c95-203">Implementación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="90c95-203">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="90c95-204">Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración</span><span class="sxs-lookup"><span data-stu-id="90c95-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="90c95-205">Cómo instalar el servidor de publicación en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="90c95-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="90c95-206">Cómo implementar el servidor de App-V 5.1 mediante un script</span><span class="sxs-lookup"><span data-stu-id="90c95-206">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





