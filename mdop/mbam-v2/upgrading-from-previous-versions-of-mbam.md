---
title: Actualización desde versiones anteriores de MBAM
description: Actualización desde versiones anteriores de MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823810"
---
# <span data-ttu-id="a7578-103">Actualización desde versiones anteriores de MBAM</span><span class="sxs-lookup"><span data-stu-id="a7578-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="a7578-104">Puede actualizar la administración y supervisión de Microsoft BitLocker (MBAM) a MBAM 2.0, con la topología independiente o la topología del administrador de configuración, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a7578-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="a7578-105">**Sustitución de servidor manual local** : para actualizar el servidor de MBAM, desinstale manualmente MBAM con el instalador o el panel de control y, a continuación, instale la infraestructura de MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="a7578-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="a7578-106">No es necesario quitar las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a7578-106">You do not have to remove the databases.</span></span> <span data-ttu-id="a7578-107">La desinstalación de MBAM 1,0 Server deja intacta las bases de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7578-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="a7578-108">Si especifica las mismas bases de datos que MBAM 1,0, la instalación de MBAM 2.0 conserva los datos de MBAM 1,0 en las bases de datos y convierte las bases de datos para que funcionen con MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="a7578-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="a7578-109">**Actualización de cliente distribuido** : Si usa la topología de MBAM independiente, puede actualizar los clientes de MBAM gradualmente después de instalar la infraestructura de servidor de MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="a7578-110">El servidor de MBAM 2,0 detecta la versión del cliente existente y realiza los pasos necesarios para actualizar al cliente de 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="a7578-111">Después de actualizar la infraestructura de servidor de MBAM 2,0, los clientes de MBAM 1,0 continúan reportando correctamente al servidor de MBAM 2,0, depósito de garantía de datos de recuperación, pero el cumplimiento se basará en las políticas de MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="a7578-112">Debe actualizar los clientes a MBAM 2,0 para que los equipos cliente notifiquen de forma precisa el cumplimiento de las directivas de MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="a7578-113">Puede actualizar los clientes al cliente de MBAM 2,0 sin desinstalar el cliente anterior y el cliente comenzará a aplicar y notificará las directivas de MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="a7578-114">Si está usando MBAM con Configuration Manager, debe actualizar los clientes de MBAM 1,0 a MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="a7578-115">Actualización de MBAM desde una arquitectura de dos servidores</span><span class="sxs-lookup"><span data-stu-id="a7578-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="a7578-116">Use las siguientes instrucciones para actualizar una versión anterior de MBAM cuando esté usando una arquitectura de dos servidores, donde un servidor está hospedando los componentes de Microsoft SQL Server y el otro servidor hospeda los sitios web y los servicios.</span><span class="sxs-lookup"><span data-stu-id="a7578-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="a7578-117">Para actualizar MBAM de una arquitectura de dos servidores</span><span class="sxs-lookup"><span data-stu-id="a7578-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="a7578-118">En el servidor con las características de SQL Server, en el panel de control, seleccione **programas y características**y, a continuación, desinstale **Administración y administración de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a7578-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="a7578-119">La base de datos de recuperación y la base de datos de auditoría y cumplimiento permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="a7578-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="a7578-120">Ejecute **MBAMSetup.exe** para la versión MBAM 2,0, seleccione, opcionalmente, el programa para la mejora de la **experiencia del usuario**y, a continuación, haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="a7578-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="a7578-121">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="a7578-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="a7578-122">En la **Página selección de topología** , seleccione la topología de integración independiente o **de** **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="a7578-123">En la página **seleccionar características para instalar** , desactive las características servidor de **autoservicio** , **Administración y supervisión** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="a7578-124">Espere a que finalicen las comprobaciones de requisitos previos y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="a7578-125">Si se detecta un requisito previo que falta, resuelva los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="a7578-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="a7578-126">En la página **proporcionar la cuenta usada para acceder a las bases de datos de MBAM** , proporcione el nombre del equipo del servidor que hospedará los sitios y servicios y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="a7578-127">En la página **configurar la base** de datos de recuperación, especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a7578-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="a7578-128">También debe especificar dónde se ubicarán los archivos de base de datos y la información de registro.</span><span class="sxs-lookup"><span data-stu-id="a7578-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="a7578-129">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a7578-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="a7578-130">En la página **Configure the Compliance and Audit Database** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="a7578-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="a7578-131">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a7578-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="a7578-132">En la página **configurar los informes de cumplimiento y cumplimiento** , especifique la instancia de SQL Server Reporting Services en la que se instalarán los informes de cumplimiento y cumplimiento, y proporcione una cuenta de usuario y contraseña de dominio para obtener acceso a la base de datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="a7578-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="a7578-133">Configure la contraseña de esta cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="a7578-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="a7578-134">La cuenta de usuario puede tener acceso a todos los datos disponibles para el grupo de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7578-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="a7578-135">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a7578-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="a7578-136">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="a7578-137">Esto no activa las actualizaciones automáticas en Windows.</span><span class="sxs-lookup"><span data-stu-id="a7578-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="a7578-138">Si anteriormente decidió usar Microsoft Update para este producto o para otro producto, la página de Microsoft Update no aparece.</span><span class="sxs-lookup"><span data-stu-id="a7578-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="a7578-139">En la página Resumen de la **instalación** , revise las características que se instalarán y, a continuación, haga clic en **instalar** para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a7578-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="a7578-140">Para desinstalar las características del servidor de administración y supervisión y para completar la actualización</span><span class="sxs-lookup"><span data-stu-id="a7578-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="a7578-141">En el equipo que hospeda las características de servidor de administración y supervisión, en el panel de control, seleccione **programas y características**y, después, desinstale MBAM para quitar los sitios web y servicios previamente instalados.</span><span class="sxs-lookup"><span data-stu-id="a7578-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="a7578-142">Ejecute el **MBAMSetup.exe** para la versión 2,0, opcionalmente, seleccione el programa para la mejora de la **experiencia del usuario**y, a continuación, haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="a7578-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="a7578-143">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="a7578-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="a7578-144">En la **Página selección de topología** , seleccione la topología de integración independiente o **de** **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="a7578-145">En la **página seleccionar las características que desea instalar** , desactive las características base de **datos de recuperación** , **base** de datos de recuperación y cumplimiento de **normas y auditoría** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="a7578-146">Espere a que finalicen las comprobaciones de requisitos previos y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="a7578-147">Si se detecta un requisito previo que falta, resuelva primero los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="a7578-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="a7578-148">En la página **configurar la seguridad de comunicaciones de red** , elija si desea usar el cifrado de nivel de socket seguro (SSL) para los sitios web y los servicios.</span><span class="sxs-lookup"><span data-stu-id="a7578-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="a7578-149">Si decide cifrar la comunicación, seleccione el certificado de la entidad de certificación (CA) que quiere usar para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="a7578-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="a7578-150">**Nota:**  El certificado debe crearse antes de este paso para poder seleccionarlo en esta página.</span><span class="sxs-lookup"><span data-stu-id="a7578-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="a7578-151">En la página **configurar la ubicación de la base de datos de estado de cumplimiento** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacena los datos de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="a7578-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="a7578-152">También debe especificar dónde se ubicarán los archivos de base de datos y la información de registro.</span><span class="sxs-lookup"><span data-stu-id="a7578-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="a7578-153">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a7578-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="a7578-154">En la página **configurar la ubicación de la base de datos de recuperación** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacena los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a7578-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="a7578-155">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a7578-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="a7578-156">En la página **configurar los informes de cumplimiento y cumplimiento** , escriba la dirección URL de la instancia de informes que ha configurado en el otro servidor.</span><span class="sxs-lookup"><span data-stu-id="a7578-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="a7578-157">Use el botón **prueba** para comprobar que puede comunicarse con el sitio.</span><span class="sxs-lookup"><span data-stu-id="a7578-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="a7578-158">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a7578-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="a7578-159">En la página **configurar el portal de autoservicio** , escriba el número de puerto, el nombre de host, el nombre del directorio virtual y la ruta de instalación para el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="a7578-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="a7578-160">**Nota:**  El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host.</span><span class="sxs-lookup"><span data-stu-id="a7578-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="a7578-161">En la página **configurar el servidor de administración y supervisión** , especifique el directorio virtual que desee para el sitio web del Departamento de soporte.</span><span class="sxs-lookup"><span data-stu-id="a7578-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="a7578-162">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a7578-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="a7578-163">Este paso no activa las actualizaciones automáticas en Windows.</span><span class="sxs-lookup"><span data-stu-id="a7578-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="a7578-164">Si anteriormente decidió usar Microsoft Update para este producto o para otro producto, la página de Microsoft Update no aparece.</span><span class="sxs-lookup"><span data-stu-id="a7578-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="a7578-165">En la página Resumen de la **instalación** , revise las características que se instalarán y, a continuación, haga clic en **instalar** para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a7578-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="a7578-166">Para validar que la actualización se ha realizado correctamente, compruebe que puede comunicarse con cada sitio desde otro equipo del dominio.</span><span class="sxs-lookup"><span data-stu-id="a7578-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="a7578-167">Actualización del cliente de MBAM en equipos de usuario final</span><span class="sxs-lookup"><span data-stu-id="a7578-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="a7578-168">Para actualizar los equipos de los usuarios finales al cliente de MBAM 2,0, ejecute **MbamClientSetup.exe** en cada equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="a7578-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="a7578-169">El instalador actualiza automáticamente el cliente al cliente de MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7578-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="a7578-170">Puede instalar el cliente de MBAM a través de un sistema electrónico de distribución de software, herramientas como Active Directory Domain Services o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7578-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="a7578-171">Para validar la actualización del cliente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a7578-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="a7578-172">Espere hasta que el ciclo de informes configurado haya finalizado y, a continuación, inicie **SQL Server Management Studio** en el equipo con SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a7578-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="a7578-173">En el equipo con SQL Server, inicie **SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="a7578-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="a7578-174">Compruebe que la tabla **RecoveryAndHardwareCore. Machines** contiene una fila que muestra el nombre del equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="a7578-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="a7578-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7578-175">Related topics</span></span>


[<span data-ttu-id="a7578-176">Implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a7578-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





