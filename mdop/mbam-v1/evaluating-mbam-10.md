---
title: Evaluación de MBAM 1.0
description: Evaluación de MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825251"
---
# <span data-ttu-id="e4645-103">Evaluación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="e4645-104">Antes de implementar administración y supervisión de Microsoft BitLocker (MBAM) en un entorno de producción, debe evaluarlo en un entorno de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="e4645-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="e4645-105">Puede usar la información de este tema para configurar MBAM en un solo entorno de laboratorio de servidor con fines de evaluación.</span><span class="sxs-lookup"><span data-stu-id="e4645-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="e4645-106">Aunque los pasos de implementación reales son muy similares al escenario que se describe en [Cómo instalar y configurar MBAM en un solo servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), este tema contiene información adicional que le permite configurar un entorno de evaluación de MBAM en el mínimo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e4645-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="e4645-107">Configurar el entorno de laboratorio</span><span class="sxs-lookup"><span data-stu-id="e4645-107">Set up the Lab Environment</span></span>


<span data-ttu-id="e4645-108">Incluso cuando configure una instancia de MBAM que no sea de producción para que se evalúe en un entorno de laboratorio, debe comprobar que cumple los requisitos previos de implementación y los requisitos de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="e4645-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="e4645-109">Para obtener más información, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e4645-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="e4645-110">También debe revisar la [preparación del entorno para MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de comenzar la implementación de evaluación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="e4645-111">Planear una implementación de evaluación de MBAM</span><span class="sxs-lookup"><span data-stu-id="e4645-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="e4645-112">Tarea</span><span class="sxs-lookup"><span data-stu-id="e4645-112">Task</span></span></th>
<th align="left"><span data-ttu-id="e4645-113">Referencias</span><span class="sxs-lookup"><span data-stu-id="e4645-113">References</span></span></th>
<th align="left"><span data-ttu-id="e4645-114">Notas</span><span class="sxs-lookup"><span data-stu-id="e4645-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-115">Revise la información de introducción sobre MBAM para obtener un conocimiento básico del producto antes de empezar con el plan de implementación.</span><span class="sxs-lookup"><span data-stu-id="e4645-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="e4645-116">Introducción a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="e4645-117">Prepare su entorno informático para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="e4645-118">Para ello, debe habilitar el cifrado de datos transparente (TDE) en las instancias de SQL Server que hospedarán las bases de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="e4645-119">Para habilitar TDE en su entorno de laboratorio, puede crear un archivo. SQL para ejecutarlo en la base de datos Master que se hospeda en la instancia de SQL Server que usará MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e4645-120">Nota</span><span class="sxs-lookup"><span data-stu-id="e4645-120">Note</span></span></strong><br/><p><span data-ttu-id="e4645-121">Puede usar el ejemplo siguiente para crear un archivo. SQL para su entorno de laboratorio con el fin de habilitar rápidamente TDE en la instancia de SQL Server que hospedará las bases de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="e4645-122">Estos comandos de SQL Server habilitarán TDE mediante el uso de un certificado de SQL Server firmado localmente.</span><span class="sxs-lookup"><span data-stu-id="e4645-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="e4645-123">Asegúrese de realizar una copia de seguridad del certificado TDE y de su clave de cifrado asociada al ejemplo de la ruta de copia de seguridad local de <em> C:\backup </em> .</span><span class="sxs-lookup"><span data-stu-id="e4645-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="e4645-124">El certificado TDE y la clave son obligatorios al recuperar la base de datos o al mover el certificado y la clave a otro servidor que tenga el cifrado de TDE.</span><span class="sxs-lookup"><span data-stu-id="e4645-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="e4645-125">Requisitos previos de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="e4645-126">Cifrado de base de datos en SQL Server 2008 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="e4645-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-127">Planear y configurar los requisitos de la Directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="e4645-128">Planificación de los requisitos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-129">Planee y cree los grupos de seguridad necesarios de los servicios de dominio de Active Directory y plan para MBAM requisitos de pertenencia a grupos de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="e4645-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="e4645-130">Planificación de roles de administrador de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-131">Planear la implementación de características de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="e4645-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="e4645-132">Planificación para la implementación de servidores de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-133">Planear la implementación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="e4645-134">Planificación para la implementación de clientes de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e4645-135">Realizar una implementación de evaluación de MBAM</span><span class="sxs-lookup"><span data-stu-id="e4645-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="e4645-136">Después de completar las instalaciones necesarias de planeación y de software necesarias para preparar el entorno informático para una instalación MBAM, puede iniciar la implementación de evaluación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-137">Revise la información de configuraciones admitidas de MBAM para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="e4645-138">Configuraciones admitidas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-139">Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en un solo servidor con fines de evaluación.</span><span class="sxs-lookup"><span data-stu-id="e4645-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="e4645-140">Cómo instalar y configurar MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="e4645-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-141">Agregue los grupos de seguridad de los servicios de dominio de Active Directory que creó durante la fase de planeación a los grupos locales de la MBAM de servidor local correspondiente en el nuevo servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="e4645-142">Planificación de los roles de administrador de MBAM 1,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="e4645-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-143">Cree e implemente los objetos de directiva de grupo MBAM obligatorios.</span><span class="sxs-lookup"><span data-stu-id="e4645-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="e4645-144">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e4645-145">Implemente el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e4645-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="e4645-146">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e4645-147">Configurar los equipos de laboratorio para la evaluación de MBAM</span><span class="sxs-lookup"><span data-stu-id="e4645-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="e4645-148">Puede cambiar la configuración de frecuencia en los informes de estado del cliente de MBAM mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="e4645-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="e4645-149">Sin embargo, estas modificaciones deberían usarse solo con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="e4645-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="e4645-150">Advertencia</span><span class="sxs-lookup"><span data-stu-id="e4645-150">Warning</span></span>**  
<span data-ttu-id="e4645-151">En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="e4645-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="e4645-152">Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="e4645-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="e4645-153">Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro.</span><span class="sxs-lookup"><span data-stu-id="e4645-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="e4645-154">Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver.</span><span class="sxs-lookup"><span data-stu-id="e4645-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="e4645-155">Cambie el registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="e4645-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="e4645-156">Modificar la configuración de frecuencia de los informes de estado de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="e4645-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="e4645-157">Las frecuencias de los informes de estado y la activación del cliente de MBAM tienen un valor mínimo de 90 minutos cuando se establecen para usar una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e4645-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="e4645-158">Puede cambiar estas frecuencias en MBAM equipos cliente editando el registro de Windows con valores más bajos, que le ayudarán a acelerar las pruebas.</span><span class="sxs-lookup"><span data-stu-id="e4645-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="e4645-159">Para modificar la configuración de frecuencia en la creación de informes de estado de cliente de MBAM, use un editor del registro para ir a **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, cambie los valores de **ClientWakeupFrequency** y **StatusReportingFrequency** a **1** como valor mínimo admitido por el cliente y, a continuación, reinicie el servicio cliente de administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e4645-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="e4645-160">Cuando realices este cambio, el cliente de MBAM se informará cada minuto.</span><span class="sxs-lookup"><span data-stu-id="e4645-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="e4645-161">Puede configurar los valores como bajo solo cuando lo haga de forma manual en el registro.</span><span class="sxs-lookup"><span data-stu-id="e4645-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="e4645-162">Modificar el retraso de inicio en el servicio de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="e4645-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="e4645-163">Además de las frecuencias de los informes de estado y la activación del cliente de MBAM, se produce un retraso aleatorio de hasta 90 minutos cuando el servicio agente de cliente de MBAM se inicia en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="e4645-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="e4645-164">Si no desea el retraso aleatorio, cree un valor **DWORD** de **NoStartupDelay** en **HKLM\\Software\\Microsoft\\MBAM**, establezca su valor en **1**y, a continuación, reinicie el servicio de cliente de administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e4645-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="e4645-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4645-165">Related topics</span></span>


[<span data-ttu-id="e4645-166">Introducción a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e4645-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)









