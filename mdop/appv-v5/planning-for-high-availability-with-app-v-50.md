---
title: Planeación para la alta disponibilidad con App-V 5.0
description: Planeación para la alta disponibilidad con App-V 5.0
author: dansimp
ms.assetid: 6d9a6492-23f8-465c-82e5-49c863594156
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebf586de7cae19d40d76c9c0c845f93e7bd9021b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813494"
---
# <span data-ttu-id="85726-103">Planeación para la alta disponibilidad con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="85726-103">Planning for High Availability with App-V 5.0</span></span>


<span data-ttu-id="85726-104">Microsoft Application Virtualization 5,0 (App-V 5,0) las configuraciones del sistema pueden aprovechar las opciones que mantienen un alto nivel de servicio disponible.</span><span class="sxs-lookup"><span data-stu-id="85726-104">Microsoft Application Virtualization 5.0 (App-V 5.0) system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="85726-105">Use la información de las siguientes secciones como ayuda para comprender las opciones para implementar App-V 5,0 en una configuración de alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="85726-105">Use the information in the following sections to help you understand the options to deploy App-V 5.0 in a highly available configuration.</span></span>

-   [<span data-ttu-id="85726-106">Compatibilidad con clústeres de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="85726-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="85726-107">Compatibilidad con el equilibrio de carga de red de IIS</span><span class="sxs-lookup"><span data-stu-id="85726-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="85726-108">Compatibilidad con servidores de archivos agrupados en el modo de ejecución (SCS)</span><span class="sxs-lookup"><span data-stu-id="85726-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="85726-109">Compatibilidad con el reflejo de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="85726-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="85726-110">Compatibilidad con Microsoft SQL Server siempre activada</span><span class="sxs-lookup"><span data-stu-id="85726-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="85726-111">Compatibilidad con clústeres de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="85726-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="85726-112">Puede ejecutar la base de datos de administración de App-V y la base de datos de informes en equipos que ejecutan clústeres de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85726-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="85726-113">Sin embargo, debe instalar las bases de datos con scripts.</span><span class="sxs-lookup"><span data-stu-id="85726-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="85726-114">Para obtener instrucciones, vea [cómo implementar las bases de datos de App-V con scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="85726-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="85726-115">Compatibilidad con el equilibrio de carga de red de IIS</span><span class="sxs-lookup"><span data-stu-id="85726-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="85726-116">Puede usar el equilibrio de carga de red de Internet Information Services (IIS) para configurar un entorno de alta disponibilidad para equipos que ejecuten los servicios de administración de App-V 5. x, publicación y creación de informes implementados mediante IIS.</span><span class="sxs-lookup"><span data-stu-id="85726-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="85726-117">Revise lo siguiente para obtener más información sobre la configuración de IIS y el equilibrio de carga de red en equipos que ejecutan sistemas operativos de Windows Server:</span><span class="sxs-lookup"><span data-stu-id="85726-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="85726-118">Proporciona información sobre cómo configurar servicios de Internet Information Server (IIS) 7,0.</span><span class="sxs-lookup"><span data-stu-id="85726-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="85726-119">[Obtención de alta disponibilidad y escalabilidad: arr y NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="85726-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="85726-120">Configuración de Microsoft Windows Server</span><span class="sxs-lookup"><span data-stu-id="85726-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="85726-121">[Equilibrio de carga de red](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="85726-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="85726-122">Esta información también se aplica a los clústeres de equilibrio de carga de red (NLB) de IIS en Windows Server2008, Windows Server2008R2 o Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="85726-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="85726-123">**Nota:**  La funcionalidad de equilibrio de carga de red de IIS en Windows Server2012 es generalmente la misma que en Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="85726-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="85726-124">Sin embargo, algunos detalles de las tareas se modifican en Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="85726-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="85726-125">Para obtener información sobre las nuevas formas de realizar tareas, consulte [navegación y tareas de administración comunes en Windows server 2012 R2 Preview y Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="85726-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="85726-126">Compatibilidad con servidores de archivos agrupados en el modo de ejecución (SCS)</span><span class="sxs-lookup"><span data-stu-id="85726-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="85726-127">La ejecución de App-V 5,0 en el modo compartir almacén de contenido (SCS) con servidores de archivos agrupados es compatible.</span><span class="sxs-lookup"><span data-stu-id="85726-127">Running App-V 5.0 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="85726-128">Puede usar los siguientes pasos para habilitar esta configuración:</span><span class="sxs-lookup"><span data-stu-id="85726-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="85726-129">Configure App-V 5,0 para que se ejecute en el modo de SCS de cliente.</span><span class="sxs-lookup"><span data-stu-id="85726-129">Configure App-V 5.0 to run in client SCS mode.</span></span> <span data-ttu-id="85726-130">Para obtener más información sobre la configuración de App-V 5,0 SCS, consulte [Cómo instalar el cliente de App-v 5,0 para el modo de almacenamiento de contenido compartido](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span><span class="sxs-lookup"><span data-stu-id="85726-130">For more information about configuring App-V 5.0 SCS mode, see [How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="85726-131">Configure el clúster de servidores de archivos configurado tanto en el modo de escalado horizontal de Microsoft Server2012 como en el modo pre **2012** con una San virtual.</span><span class="sxs-lookup"><span data-stu-id="85726-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="85726-132">Puede usar los siguientes pasos para validar la configuración:</span><span class="sxs-lookup"><span data-stu-id="85726-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="85726-133">Agregue un paquete en el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="85726-133">Add a package on the publishing server.</span></span> <span data-ttu-id="85726-134">Para obtener más información sobre cómo agregar un paquete, consulte [Cómo agregar o actualizar paquetes mediante la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="85726-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="85726-135">Realice una actualización de publicación en el equipo que ejecuta el cliente de App-V 5,0 y abra una aplicación.</span><span class="sxs-lookup"><span data-stu-id="85726-135">Perform a publishing refresh on the computer running the App-V 5.0 client and open an application.</span></span>

3.  <span data-ttu-id="85726-136">Cambiar de nodo de clúster la actualización de publicación en Mid y la transmisión por secuencias para asegurar que la conmutación por error funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="85726-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="85726-137">Revise lo siguiente para obtener más información sobre cómo configurar los clústeres de conmutación por error de Windows Server:</span><span class="sxs-lookup"><span data-stu-id="85726-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="85726-138">[Lista de comprobación: crear un servidor de archivos agrupado](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="85726-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="85726-139">[Usar volúmenes compartidos de clúster en un clúster de conmutación por error de Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="85726-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="85726-140">Compatibilidad con el reflejo de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="85726-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="85726-141">Con el reflejo de Microsoft SQL Server, donde la base de datos del servidor de administración de App-V 5,0 se refleja con dos instancias de SQL Server, se admiten las bases de datos de servidor de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="85726-141">Using Microsoft SQL Server mirroring, where the App-V 5.0 management server database is mirrored utilizing two SQL Server instances, for App-V 5.0 management server databases is supported.</span></span>

<span data-ttu-id="85726-142">Revise lo siguiente para obtener más información sobre cómo configurar el reflejo de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="85726-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="85726-143">[Cómo: preparar una base de datos de reflejo para la creación de reflejos (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="85726-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="85726-144">[Establecer una sesión de creación de reflejo de base de datos con la autenticación de Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="85726-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="85726-145">Puede usar los siguientes pasos para validar la configuración:</span><span class="sxs-lookup"><span data-stu-id="85726-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="85726-146">Inicie una sesión de creación de reflejos de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85726-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="85726-147">Seleccione **conmutación por error** para designar una nueva instancia maestra de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85726-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="85726-148">Compruebe que el servidor de administración de App-V 5,0 siga funcionando según lo esperado después de la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="85726-148">Verify that the App-V 5.0 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="85726-149">La cadena de conexión en el servidor de administración se puede modificar para que incluya \*\*failover Partner = &lt; server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="85726-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="85726-150">Esto solo es útil cuando el principal en el reflejo conmuta por error al secundario y el equipo que ejecuta el cliente de App-V 5,0 está haciendo una conexión nueva (por ejemplo, después de reiniciar).</span><span class="sxs-lookup"><span data-stu-id="85726-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.0 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="85726-151">Siga estos pasos para modificar la cadena de conexión para que incluya **failover Partner &lt; = &gt; server2**:</span><span class="sxs-lookup"><span data-stu-id="85726-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="85726-152">**Importante**  En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="85726-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="85726-153">Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="85726-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="85726-154">Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro.</span><span class="sxs-lookup"><span data-stu-id="85726-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="85726-155">Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver.</span><span class="sxs-lookup"><span data-stu-id="85726-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="85726-156">Cambie el registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="85726-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="85726-157">Inicie sesión en el servidor de administración y Abra **regedit**.</span><span class="sxs-lookup"><span data-stu-id="85726-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="85726-158">Vaya a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.</span><span class="sxs-lookup"><span data-stu-id="85726-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="85726-159">Modifique el valor de **Administración \ _SQL \ _CONNECTION \ _STRING** valor con el \*\*asociado de conmutación por error = &lt; servidor2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="85726-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="85726-160">Reinicie el servicio de administración mediante la consola de IIS.</span><span class="sxs-lookup"><span data-stu-id="85726-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="85726-161">**Nota:**  El reflejo de la base de datos está en la lista de características del motor de base de datos obsoletas para Microsoft SQL Server2012 a causa de la característica **AlwaysOn** disponible en Microsoft sql server 2012.</span><span class="sxs-lookup"><span data-stu-id="85726-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="85726-162">Para obtener más información, haga clic en cualquiera de los siguientes vínculos:</span><span class="sxs-lookup"><span data-stu-id="85726-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="85726-163">[Cómo: preparar una base de datos de reflejo para la creación de reflejos (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="85726-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="85726-164">[Cómo: configurar una sesión de creación de reflejo de base de datos (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="85726-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="85726-165">[Establecer una sesión de creación de reflejo de base de datos con la autenticación de Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .</span><span class="sxs-lookup"><span data-stu-id="85726-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="85726-166">[Características del motor de base de datos obsoletas en SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .</span><span class="sxs-lookup"><span data-stu-id="85726-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="85726-167">Compatibilidad con Microsoft SQL Server siempre en la configuración</span><span class="sxs-lookup"><span data-stu-id="85726-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="85726-168">La base de datos de App-V 5,0 Management Server admite implementaciones en equipos que ejecutan Microsoft SQL Server con la configuración **Always on** .</span><span class="sxs-lookup"><span data-stu-id="85726-168">The App-V 5.0 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>

## <span data-ttu-id="85726-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85726-169">Related topics</span></span>


[<span data-ttu-id="85726-170">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="85726-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





