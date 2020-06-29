---
title: Cómo configurar el equilibrio de carga de red para MBAM
description: Cómo configurar el equilibrio de carga de red para MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825511"
---
# <span data-ttu-id="7bf29-103">Cómo configurar el equilibrio de carga de red para MBAM</span><span class="sxs-lookup"><span data-stu-id="7bf29-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="7bf29-104">Para comprobar que cumple los requisitos previos y los requisitos de hardware y software para instalar la característica servidor de administración y supervisión, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7bf29-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="7bf29-105">**Nota:**  Para obtener los archivos de registro de configuración, debe instalar Microsoft BitLocker Administration and Monitoring (MBAM) mediante el paquete **msiexec** y la opción **/l** de la &lt; Ubicación &gt; .</span><span class="sxs-lookup"><span data-stu-id="7bf29-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="7bf29-106">Los archivos de registro se crean en la ubicación que especifique.</span><span class="sxs-lookup"><span data-stu-id="7bf29-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="7bf29-107">Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% del usuario que instala MBAM.</span><span class="sxs-lookup"><span data-stu-id="7bf29-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="7bf29-108">Los clústeres de equilibrio de carga de red (NLB) de la característica servidor de administración y supervisión proporcionan escalabilidad en MBAM y deben admitir más de 55.000 MBAM de equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="7bf29-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="7bf29-109">**Nota:**  El equilibrio de carga de red de Windows Server distribuye las solicitudes de cliente a través de un conjunto de servidores que están configurados en un clúster de servidor único.</span><span class="sxs-lookup"><span data-stu-id="7bf29-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="7bf29-110">Cuando el equilibrio de carga de red está instalado en cada uno de los servidores (hosts) de un clúster, el clúster presenta una dirección IP virtual o un nombre de dominio completo (FQDN) a las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="7bf29-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="7bf29-111">Las solicitudes de cliente iniciales van a todos los hosts del clúster, pero solo un anfitrión acepta y controla la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7bf29-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="7bf29-112">Todos los equipos que formarán parte de un clúster NLB tienen los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="7bf29-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="7bf29-113">Todos los equipos del clúster NLB deben estar en el mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="7bf29-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="7bf29-114">Cada equipo del clúster NLB debe usar una dirección IP estática.</span><span class="sxs-lookup"><span data-stu-id="7bf29-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="7bf29-115">Cada equipo del clúster NLB debe tener habilitado el equilibrio de carga de red.</span><span class="sxs-lookup"><span data-stu-id="7bf29-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="7bf29-116">El clúster NLB requiere una dirección IP estática y se debe crear un registro de host manualmente en el sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="7bf29-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="7bf29-117">Configuración del equilibrio de carga de red para los servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="7bf29-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="7bf29-118">Los pasos siguientes describen cómo configurar un nombre virtual de clúster NLB y una dirección IP para dos servidores de supervisión y administración de MBAM, y cómo configurar los clientes de MBAM para que usen el clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="7bf29-119">Antes de empezar los procedimientos que se describen en este tema, debe tener la característica del servidor de administración y supervisión de MBAM instalada correctamente mediante el mismo enlace de puerto de IIS en dos equipos de servidor independientes que cumplan los requisitos previos para la instalación de características de servidor MBAM y la configuración de clúster de NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="7bf29-120">**Nota:**  En este tema se describe el proceso básico de uso del administrador de equilibrio de carga de red para crear un clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="7bf29-121">Los pasos exactos para configurar un servidor Windows como parte de un clúster NLB dependen de la versión de Windows Server en uso..</span><span class="sxs-lookup"><span data-stu-id="7bf29-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="7bf29-122">Para obtener más información sobre cómo crear NLBs en WindowsServer2008, consulte [creación de clústeres de equilibrio de carga de red](https://go.microsoft.com/fwlink/?LinkId=197176) en la biblioteca de TechNet de Server2008 de Windows.</span><span class="sxs-lookup"><span data-stu-id="7bf29-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="7bf29-123">Para configurar un nombre virtual de clúster NLB y una dirección IP para dos servidores de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="7bf29-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="7bf29-124">Haga clic en **Inicio**, en **todos los programas**, en **herramientas administrativas**y, por último, en **Administrador de equilibrio de carga de red**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="7bf29-125">**Nota:**  Si el administrador de NLB no está presente, puede instalarlo como una característica de WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="7bf29-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="7bf29-126">Debe instalar esta característica en los servidores de supervisión y administración de MBAM si desea configurarlo en el clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="7bf29-127">En la barra de menús, haga clic en **cluster**y, a continuación, haga clic en **nuevo** para abrir el cuadro de diálogo **parámetros de clúster** .</span><span class="sxs-lookup"><span data-stu-id="7bf29-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="7bf29-128">En el cuadro de diálogo **parámetros de clúster** , escriba la información para la configuración IP del clúster de NLB:</span><span class="sxs-lookup"><span data-stu-id="7bf29-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="7bf29-129">**Dirección IP:** Dirección IP del clúster NLB registrada en DNS</span><span class="sxs-lookup"><span data-stu-id="7bf29-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="7bf29-130">**Máscara de subred:** Máscara de subred de la dirección IP del clúster NLB registrada en DNS</span><span class="sxs-lookup"><span data-stu-id="7bf29-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="7bf29-131">**Nombre completo de Internet:** FQDN del nombre de clúster NLB registrado en DNS</span><span class="sxs-lookup"><span data-stu-id="7bf29-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="7bf29-132">Asegúrese de que **unidifusión** está seleccionado en el **modo de operación de clúster**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="7bf29-133">En la página **direcciones IP del clúster** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="7bf29-134">En la página **reglas de Puerto** , haga clic en **Editar** para definir los puertos a los que responderá el clúster NLB y configure los puertos que se usan para la comunicación del sistema entre el cliente y la definición del sitio, o haga clic en **siguiente** para habilitar la dirección IP del clúster NLB para responder a todos los puertos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7bf29-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="7bf29-135">**Nota:**  Asegúrese de que **affinity** es **Single**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="7bf29-136">En la página **Connect** , escriba un nombre de host de instancia de servidor de supervisión y administración de MBAM que formará parte del clúster NLB en **host**y, a continuación, haga clic en **conectar**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="7bf29-137">En las **interfaces disponibles para configurar un nuevo clúster**, seleccione la interfaz de red que se configurará para responder a la comunicación del clúster NLB y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="7bf29-138">En la página **parámetros de host** , revise la información que se muestra para asegurarse de que la configuración de **IP dedicada** muestra la configuración de IP de host dedicada para el host de clúster NLB correcto, compruebe que el estado **predeterminado** del host es **iniciado**y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="7bf29-139">**Nota:**  La página de **parámetros de host** también muestra la prioridad de host de clúster de NLB, que es de 1 a 32.</span><span class="sxs-lookup"><span data-stu-id="7bf29-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="7bf29-140">A medida que se agregan nuevos hosts al clúster NLB, la prioridad del host debe ser diferente de la de los hosts agregados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7bf29-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="7bf29-141">La prioridad se incrementa automáticamente al usar el administrador de equilibrio de carga de red.</span><span class="sxs-lookup"><span data-stu-id="7bf29-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="7bf29-142">Haga clic en \*\* &lt; nombre &gt; del clúster NLB\*\* y asegúrese de que el **Estado** de la interfaz del host NLB está **convergido** antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="7bf29-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="7bf29-143">Es posible que este paso requiera que actualice la pantalla del clúster NLB como la configuración TCP/IP del host modificada por el administrador de NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="7bf29-144">Para agregar hosts adicionales al clúster NLB, haga clic con el botón secundario en \*\* &lt; &gt; nombre del clúster NLB\*\*, haga clic en **Agregar host al clúster** y, a continuación, repita los pasos del 7 al 10 para cada sistema de sitio que formará parte del clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="7bf29-145">En un equipo que tenga instalada una plantilla de directiva de grupo de MBAM, modifique la configuración de directiva de grupo de MBAM para configurar los puntos de conexión de servicios de MBAM para usar el nombre de clúster NLB y el enlace de Puerto IIS adecuado para acceder a las características de servidor de administración y supervisión de MBAM que se instalan en los equipos del clúster de NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="7bf29-146">Para obtener más información sobre cómo editar la configuración de GPO de MBAM, vea [Cómo editar la configuración de GPO de MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7bf29-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="7bf29-147">Si los servidores de administración y supervisión de MBAM son nuevos en su entorno, asegúrese de que las pertenencias a grupos de seguridad local obligatorias se hayan configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7bf29-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="7bf29-148">Para obtener más información sobre los requisitos de los grupos de seguridad, consulte [roles de planificación de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7bf29-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="7bf29-149">Cuando se complete la configuración del clúster NLB, le recomendamos que valide que el clúster NLB de administración y supervisión de MBAM es funcional.</span><span class="sxs-lookup"><span data-stu-id="7bf29-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="7bf29-150">Para ello, abra un explorador Web en un equipo distinto de los servidores que están configurados en el NLB y asegúrese de que puede obtener acceso al sitio web de supervisión y administración de MBAM con el FQDN de NLB.</span><span class="sxs-lookup"><span data-stu-id="7bf29-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="7bf29-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bf29-151">Related topics</span></span>


[<span data-ttu-id="7bf29-152">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7bf29-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





