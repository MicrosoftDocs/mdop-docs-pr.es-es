---
title: Cómo instalar y configurar MBAM en servidores distribuidos
description: Cómo instalar y configurar MBAM en servidores distribuidos
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824060"
---
# <span data-ttu-id="34455-103">Cómo instalar y configurar MBAM en servidores distribuidos</span><span class="sxs-lookup"><span data-stu-id="34455-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="34455-104">Los procedimientos de este tema describen cómo instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 en la topología independiente en servidores distribuidos.</span><span class="sxs-lookup"><span data-stu-id="34455-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="34455-105">Para ver un diagrama de la arquitectura recomendada, junto con una descripción de las bases de datos y las características, consulte [implementación de la infraestructura de servidor de MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="34455-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="34455-106">Para instalar administración y supervisión de Microsoft BitLocker con la topología de Configuration Manager, consulte [implementación de MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="34455-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="34455-107">Cada característica de servidor tiene ciertos requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="34455-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="34455-108">Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) y [MBAM 2,0 compatibles](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="34455-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="34455-109">Además, algunas características requieren que proporcione cierta información durante el proceso de instalación para implementar la característica correctamente.</span><span class="sxs-lookup"><span data-stu-id="34455-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="34455-110">También debe revisar la [planificación de la implementación de MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md) antes de iniciar la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="34455-111">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-111">Note</span></span>**  
<span data-ttu-id="34455-112">Para obtener los archivos de registro de instalación, tiene que usar el paquete msiexec y la opción de ubicación **/l** &lt; &gt; para instalar MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="34455-113">Los archivos de registro se crean en la ubicación que especifique.</span><span class="sxs-lookup"><span data-stu-id="34455-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="34455-114">Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% en el servidor del usuario que instala MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="34455-115">Implementar las características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="34455-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="34455-116">Los pasos siguientes describen cómo instalar características generales de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="34455-117">Para iniciar el Asistente para la instalación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="34455-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="34455-118">En el servidor en el que desea instalar la supervisión y administración de Microsoft BitLocker, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="34455-119">En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="34455-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="34455-120">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="34455-121">En la página **selección de topología** , seleccione la topología **independiente** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="34455-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="34455-122">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-122">Note</span></span>**  
    <span data-ttu-id="34455-123">Si desea instalar MBAM con la topología integrada de Configuration Manager, consulte [implementación de MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="34455-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="34455-124">Seleccione las características que desea instalar.</span><span class="sxs-lookup"><span data-stu-id="34455-124">Select the features that you want to install.</span></span> <span data-ttu-id="34455-125">De forma predeterminada, se seleccionan todas las características de MBAM para la instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="34455-126">Borre las características que desee instalar en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="34455-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="34455-127">Las características que se instalarán en el mismo equipo deben instalarse juntas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="34455-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="34455-128">Debe instalar las características de MBAM en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="34455-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="34455-129">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="34455-129">Recovery Database</span></span>

    -   <span data-ttu-id="34455-130">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="34455-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="34455-131">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="34455-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="34455-132">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="34455-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="34455-133">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="34455-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="34455-134">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="34455-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="34455-135">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-135">Note</span></span>**  
    <span data-ttu-id="34455-136">El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="34455-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="34455-137">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="34455-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="34455-138">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="34455-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="34455-139">Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="34455-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="34455-140">Para instalar la base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="34455-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="34455-141">En la página **configurar la base de datos de recuperación** , especifique los nombres de los equipos que ejecutarán la característica de servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="34455-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="34455-142">Después de implementar la característica de servidor de administración y supervisión, se usa su cuenta de dominio para conectarse a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="34455-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="34455-143">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="34455-144">Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="34455-145">También debe especificar dónde se ubicará la base de datos y dónde se ubicará la información de registro.</span><span class="sxs-lookup"><span data-stu-id="34455-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="34455-146">Haga clic en **siguiente** para continuar con el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="34455-147">Para instalar la base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="34455-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="34455-148">En la página **configurar la base de datos de cumplimiento y auditoría** , especifique la cuenta de usuario que se usará para obtener acceso a la base de datos para los informes.</span><span class="sxs-lookup"><span data-stu-id="34455-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="34455-149">Especifique los nombres de los equipos que ejecutarán el servidor de administración y supervisión, así como los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="34455-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="34455-150">Después de implementar el servidor de administración, supervisión y cumplimiento e informes de auditoría, usan sus cuentas de dominio para conectarse a las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="34455-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="34455-151">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-151">Note</span></span>**  
    <span data-ttu-id="34455-152">Si va a instalar la base de datos de cumplimiento y auditoría sin la característica informes de cumplimiento y auditoría, debe agregar una excepción en el equipo de base de datos de cumplimiento y auditoría para habilitar el tráfico entrante en el puerto de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="34455-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="34455-153">El número de puerto predeterminado es 1433.</span><span class="sxs-lookup"><span data-stu-id="34455-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="34455-154">Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="34455-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="34455-155">También debe especificar dónde se ubicarán la información de la base de datos y del registro.</span><span class="sxs-lookup"><span data-stu-id="34455-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="34455-156">Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34455-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="34455-157">Para instalar los informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="34455-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="34455-158">En la página **configurar los informes de cumplimiento y cumplimiento** , especifique el nombre de instancia de SQL Server remoto (por ejemplo, &lt; nombreServidor &gt; ) donde se instaló la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="34455-159">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-159">Note</span></span>**  
    <span data-ttu-id="34455-160">Si va a instalar los informes de cumplimiento y cumplimiento sin el servidor de administración y supervisión, debe agregar una excepción en el equipo de informe de cumplimiento y auditoría para habilitar el tráfico entrante en el puerto del servidor de informes (el puerto predeterminado es 80).</span><span class="sxs-lookup"><span data-stu-id="34455-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="34455-161">Especificar el nombre de la base de datos de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="34455-162">De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento, aunque puede cambiar el nombre al instalar la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="34455-163">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="34455-164">Seleccione la instancia de SQL Server Reporting Services donde se instalarán los informes de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="34455-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="34455-165">Proporcione una cuenta de usuario y una contraseña de dominio para acceder a la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="34455-166">Configure la contraseña de esta cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="34455-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="34455-167">La cuenta de usuario debería poder acceder a todos los datos que están disponibles para el grupo de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="34455-168">Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34455-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="34455-169">Para instalar el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="34455-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="34455-170">En la página **configurar el portal de autoservicio** , puede cifrar de forma opcional la comunicación entre el portal de autoservicio y los servidores de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="34455-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="34455-171">Si elige la opción para cifrar la comunicación, se le pedirá que seleccione la entidad emisora de certificados que se usará para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="34455-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="34455-172">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="34455-173">Especifique la instancia remota de SQL Server (por ejemplo, \* &lt; ServerName &gt; \*) donde se instaló la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="34455-174">Especificar el nombre de la base de datos de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="34455-175">De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="34455-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="34455-176">Sin embargo, puede cambiar el nombre cuando instale la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="34455-177">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="34455-178">Especifique la instancia remota de SQL Server (por ejemplo, \* &lt; ServerName &gt; \*) donde se instaló la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="34455-179">Especifique el nombre de la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="34455-180">De forma predeterminada, el nombre de la base de datos es **recuperación y hardware de MBAM**.</span><span class="sxs-lookup"><span data-stu-id="34455-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="34455-181">Sin embargo, puede cambiar el nombre al instalar la característica de base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="34455-182">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="34455-183">Escriba el **número de Puerto**, el **nombre de host** (opcional) y la ruta de **instalación** para el servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="34455-184">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-184">Note</span></span>**  
    <span data-ttu-id="34455-185">El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host.</span><span class="sxs-lookup"><span data-stu-id="34455-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="34455-186">Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.</span><span class="sxs-lookup"><span data-stu-id="34455-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="34455-187">Para registrar opcionalmente un nombre principal de servicio (SPN) para el portal de autoservicio, seleccione **registrar los nombres principales de servicio (SPN) de este equipo con Active Directory (necesario para la autenticación de Windows)**.</span><span class="sxs-lookup"><span data-stu-id="34455-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="34455-188">Si activa esta casilla, el programa de instalación de MBAM no intentará registrar los SPN existentes y puede registrar manualmente el SPN antes o después de la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="34455-189">Para obtener instrucciones sobre cómo registrar el SPN manualmente, consulte [manual registration SPN](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="34455-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="34455-190">Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34455-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="34455-191">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="34455-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="34455-192">Cuando se complete la información de la característica de MBAM seleccionada, estará listo para iniciar la instalación de MBAM con el Asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="34455-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="34455-193">Haga clic en **atrás** para desplazarse por el asistente si tiene que revisar o cambiar la configuración de instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="34455-194">Haga clic en **instalar** para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="34455-195">Haga clic en **Cancelar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="34455-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="34455-196">El programa de instalación instala las características de MBAM que ha seleccionado y le notifica que ha finalizado la instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="34455-197">Haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="34455-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="34455-198">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-198">Note</span></span>**  
    <span data-ttu-id="34455-199">Para configurar el portal de autoservicio después de instalarlo, marca el portal de autoservicio con el nombre de su empresa y otra información específica de la empresa, consulte [Cómo personalizar el portal de autoservicio](how-to-brand-the-self-service-portal.md) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="34455-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="34455-200">Si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft, lo que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript, finalizará la instalación del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="34455-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="34455-201">Si los equipos cliente no tienen acceso a la red CDN de Microsoft, complete los pasos de la siguiente sección para configurar el portal de autoservicio para hacer referencia a los archivos de JavaScript desde un origen accesible.</span><span class="sxs-lookup"><span data-stu-id="34455-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="34455-202">Para configurar el portal de autoservicio cuando los usuarios finales no pueden obtener acceso a la red de entrega de contenido de Microsoft</span><span class="sxs-lookup"><span data-stu-id="34455-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="34455-203">Si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft, lo que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript, se completa la instalación del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="34455-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="34455-204">Si los equipos cliente no tienen acceso a la CDN de Microsoft, complete los pasos restantes de esta sección para configurar el portal de autoservicio para hacer referencia a los archivos de JavaScript desde un origen accesible.</span><span class="sxs-lookup"><span data-stu-id="34455-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="34455-205">Descargue los cuatro archivos de JavaScript desde la CDN de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="34455-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="34455-206">jQuery-1.7.2.min.js[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="34455-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="34455-207">MicrosoftAjax.js:[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="34455-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="34455-208">MicrosoftMvcAjax.js[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="34455-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="34455-209">MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="34455-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="34455-210">Copie los archivos de JavaScript en el directorio **scripts** del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="34455-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="34455-211">Este directorio se encuentra en <em> &lt; MBAM de autoservicio de directorio de instalación de autoservicio &gt; \\ </em> Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="34455-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="34455-212">Abra el **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="34455-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="34455-213">Expanda **sitios** &gt; **Microsoft BitLocker administración y supervisión**, y resalte **SelfService**.</span><span class="sxs-lookup"><span data-stu-id="34455-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="34455-214">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-214">Note</span></span>**  
   <span data-ttu-id="34455-215">*SelfService* es el nombre del directorio virtual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="34455-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="34455-216">Si ha elegido un nombre diferente para este directorio durante la instalación, no olvide reemplazar *SelfService* en el resto de estas instrucciones por el nombre que ha elegido.</span><span class="sxs-lookup"><span data-stu-id="34455-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="34455-217">En el panel central, haga doble clic en configuración de la **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="34455-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="34455-218">Para cada elemento de la siguiente lista, modifique la configuración de la aplicación para que haga referencia a la nueva ubicación reemplazando el &lt; directorio virtual &gt; con/SelfService/(o el nombre que haya elegido durante la instalación).</span><span class="sxs-lookup"><span data-stu-id="34455-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="34455-219">Por ejemplo, la ruta de acceso del directorio virtual será similar a/SelfService/scripts/jquery-1.7.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="34455-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="34455-220">jQueryPath:/ &lt; directorio virtual &gt; /scripts/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="34455-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="34455-221">MicrosoftAjaxPath:/ &lt; directorio virtual &gt; /scripts/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="34455-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="34455-222">MicrosoftMvcAjaxPath:/ &lt; directorio virtual &gt; /scripts/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="34455-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="34455-223">MicrosoftMvcValidationPath:/ &lt; directorio virtual &gt; /scripts/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="34455-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="34455-224">Para instalar la característica servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="34455-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="34455-225">MBAM puede cifrar la comunicación entre los servicios web y los servidores de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="34455-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="34455-226">Si elige la opción para cifrar la comunicación, se le pedirá que seleccione la entidad emisora de certificados que se usará para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="34455-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="34455-227">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="34455-228">Especifique la instancia remota de SQL Server (por ejemplo: \* &lt; ServerName &gt; \*) donde se instaló la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="34455-229">Especificar el nombre de la base de datos de cumplimiento y de auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="34455-230">De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="34455-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="34455-231">Sin embargo, puede cambiar el nombre cuando instale la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="34455-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="34455-232">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="34455-233">Especifique la instancia remota de SQL Server (por ejemplo: \* &lt; ServerName &gt; \*) donde se instaló la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="34455-234">Especifique el nombre de la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="34455-235">De forma predeterminada, el nombre de la base de datos es **recuperación y hardware de MBAM**.</span><span class="sxs-lookup"><span data-stu-id="34455-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="34455-236">Sin embargo, puede cambiar el nombre al instalar la característica de base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="34455-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="34455-237">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="34455-238">Especifique la dirección URL de la "página de inicio" del sitio de SQL Server Reporting Services (SRS).</span><span class="sxs-lookup"><span data-stu-id="34455-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="34455-239">La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services es:</span><span class="sxs-lookup"><span data-stu-id="34455-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="34455-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer</span><span class="sxs-lookup"><span data-stu-id="34455-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="34455-241">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-241">Note</span></span>**  
   <span data-ttu-id="34455-242">Si SQL Server Reporting Services se ha configurado como una instancia con nombre, la dirección URL es similar a la siguiente: http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="34455-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="34455-243">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="34455-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="34455-244">Escriba el **número de Puerto**, el **nombre de host** (opcional) y la ruta de **instalación** para el servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="34455-245">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-245">Note</span></span>**  
    <span data-ttu-id="34455-246">El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host.</span><span class="sxs-lookup"><span data-stu-id="34455-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="34455-247">Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.</span><span class="sxs-lookup"><span data-stu-id="34455-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="34455-248">Para registrar opcionalmente un nombre principal de servicio (SPN) para el portal de autoservicio, seleccione **registrar los nombres principales de servicio (SPN) de este equipo con Active Directory (necesario para la autenticación de Windows)**.</span><span class="sxs-lookup"><span data-stu-id="34455-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="34455-249">Si activa esta casilla, el programa de instalación de MBAM no intentará registrar los SPN existentes y puede registrar manualmente el SPN antes o después de la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="34455-250">Para obtener instrucciones sobre cómo registrar el SPN manualmente, consulte [manual registration SPN](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="34455-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="34455-251">Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="34455-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="34455-252">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="34455-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="34455-253">Cuando se complete la información de la característica de MBAM seleccionada, estará listo para iniciar la instalación de MBAM con el Asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="34455-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="34455-254">Haga clic en **atrás** para desplazarse por el asistente si tiene que revisar o cambiar la configuración de instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="34455-255">Haga clic en **instalar** para ser la instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="34455-256">Haga clic en **Cancelar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="34455-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="34455-257">El programa de instalación instala las características de MBAM que ha seleccionado y le notifica que ha finalizado la instalación.</span><span class="sxs-lookup"><span data-stu-id="34455-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="34455-258">Haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="34455-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="34455-259">Para realizar la configuración posterior a la instalación</span><span class="sxs-lookup"><span data-stu-id="34455-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="34455-260">En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales para proporcionarles acceso a las características del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="34455-261">**Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a las características de recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="34455-262">Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="34455-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="34455-263">**Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="34455-264">Para los usuarios avanzados, solo se requiere el campo de identificador de clave en la recuperación de unidades.</span><span class="sxs-lookup"><span data-stu-id="34455-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="34455-265">En **administrar TPM**, solo se necesitan el campo **dominio del equipo** y el campo **nombre del equipo** .</span><span class="sxs-lookup"><span data-stu-id="34455-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="34455-266">En el servidor que hospeda administración y supervisión de servidor y la base de datos de cumplimiento y auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento, agregue usuarios al siguiente grupo local para darles acceso a la característica informes del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="34455-267">**Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a los informes en el sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="34455-268">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-268">Note</span></span>**  
    <span data-ttu-id="34455-269">La pertenencia a grupos o usuarios idénticos del grupo local de **usuarios de informes de MBAM** debe mantenerse en todos los equipos en los que estén instaladas las características de servidor de administración y supervisión de MBAM, la base de datos de cumplimiento y comprobación, y los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="34455-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="34455-270">Validar la instalación de características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="34455-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="34455-271">Cuando se complete la instalación de características de administración y supervisión de Microsoft BitLocker, le recomendamos que valide que la instalación ha configurado correctamente todas las características necesarias para MBAM.</span><span class="sxs-lookup"><span data-stu-id="34455-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="34455-272">Use el procedimiento siguiente para confirmar que el servicio de administración y supervisión de Microsoft BitLocker es funcional.</span><span class="sxs-lookup"><span data-stu-id="34455-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="34455-273">Para validar una instalación de servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="34455-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="34455-274">En cada servidor en el que se implemente una característica de MBAM, abra el **Panel de control**, seleccione **programas**y, después, seleccione **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="34455-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="34455-275">Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .</span><span class="sxs-lookup"><span data-stu-id="34455-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="34455-276">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-276">Note</span></span>**  
   <span data-ttu-id="34455-277">Para validar la instalación de MBAM, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="34455-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="34455-278">En el servidor donde está instalada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.</span><span class="sxs-lookup"><span data-stu-id="34455-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="34455-279">En el servidor en el que está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la **base de datos de estado de cumplimiento de MBAM** esté instalada.</span><span class="sxs-lookup"><span data-stu-id="34455-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="34455-280">En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con credenciales administrativas y busque el "Inicio" del sitio de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="34455-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="34455-281">Se puede encontrar la ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="34455-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="34455-282">Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que se especificaron durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="34455-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="34455-283">Confirme que una carpeta de informes denominada **supervisión y administración de Microsoft BitLocker** contiene un origen de datos denominado **MaltaDataSource** y que una carpeta **de en-EE.UU.** contiene cuatro informes.</span><span class="sxs-lookup"><span data-stu-id="34455-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="34455-284">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-284">Note</span></span>**  
   <span data-ttu-id="34455-285">Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="34455-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="34455-286">En el servidor donde está instalada la característica de administración y supervisión, ejecute el **Administrador del servidor** y desplácese hasta **roles**.</span><span class="sxs-lookup"><span data-stu-id="34455-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="34455-287">Seleccione **servidor Web (IIS)** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="34455-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="34455-288">En **conexiones**, vaya a \* &lt; NombreDeEquipo &gt; \*, seleccione **sitios**y, a continuación, **Administración y supervisión de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="34455-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="34455-289">Compruebe que **MBAMAdministrationService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** aparezcan en la lista.</span><span class="sxs-lookup"><span data-stu-id="34455-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="34455-290">En el servidor donde se instalan las características de administración y supervisión y el portal de autoservicio, abra un explorador Web con credenciales administrativas y busque las siguientes ubicaciones para comprobar que se cargan correctamente.</span><span class="sxs-lookup"><span data-stu-id="34455-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="34455-291">Nota</span><span class="sxs-lookup"><span data-stu-id="34455-291">Note</span></span>**  
   <span data-ttu-id="34455-292">Las direcciones URL que terminan en ". SVC" no muestran un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="34455-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="34455-293">El éxito viene indicado por el mensaje "la publicación de metadatos para este servicio está deshabilitada" o por información similar a código.</span><span class="sxs-lookup"><span data-stu-id="34455-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="34455-294">Si aparece otro mensaje de error o si no se puede encontrar la página, la página no se ha cargado correctamente.</span><span class="sxs-lookup"><span data-stu-id="34455-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="34455-295">Compruebe que cada página web se carga correctamente.</span><span class="sxs-lookup"><span data-stu-id="34455-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="34455-296">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34455-296">Related topics</span></span>


[<span data-ttu-id="34455-297">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="34455-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









