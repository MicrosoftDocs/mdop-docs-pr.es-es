---
title: Cómo actualizar los servidores y componentes del sistema
description: Cómo actualizar los servidores y componentes del sistema
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816421"
---
# <span data-ttu-id="1f25f-103">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="1f25f-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="1f25f-104">Use el siguiente procedimiento para actualizar los componentes de software instalados en todos los equipos del sistema de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1f25f-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="1f25f-105">Los servicios del sistema de Application Virtualization se reiniciarán automáticamente en cada equipo después de que se haya actualizado.</span><span class="sxs-lookup"><span data-stu-id="1f25f-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="1f25f-106">Nota</span><span class="sxs-lookup"><span data-stu-id="1f25f-106">Note</span></span>**  
-   <span data-ttu-id="1f25f-107">El proceso de actualización detiene todos los servicios del sistema de virtualización de aplicaciones, por lo que el sistema queda fuera de servicio.</span><span class="sxs-lookup"><span data-stu-id="1f25f-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="1f25f-108">Las sesiones de usuario deben cerrarse antes de comenzar el proceso de actualización y debe detener todos los servicios del servidor de virtualización de aplicaciones en su entorno.</span><span class="sxs-lookup"><span data-stu-id="1f25f-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="1f25f-109">Si tiene más de un servidor que comparte el acceso a la base de datos de virtualización de la aplicación, todos esos servidores deben estar desconectados mientras se actualiza la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f25f-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="1f25f-110">Debe seguir las prácticas normales de negocios para la actualización de la base de datos, pero es muy aconsejable que pruebe la actualización de la base de datos con una copia de seguridad de la base de datos en primer lugar en un servidor de prueba.</span><span class="sxs-lookup"><span data-stu-id="1f25f-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="1f25f-111">Después, seleccione uno de los servidores para la primera actualización, que actualizará el esquema de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f25f-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="1f25f-112">Una vez que la base de datos de producción se ha actualizado correctamente, puede actualizar los otros servidores.</span><span class="sxs-lookup"><span data-stu-id="1f25f-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="1f25f-113">Solo puede actualizar a Microsoft Application Virtualization (App-V) 4.5 desde Microsoft Application Virtualization (App-V) 4.1 ó 4.1 SP1.</span><span class="sxs-lookup"><span data-stu-id="1f25f-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="1f25f-114">Es necesario que App-V 4.0 y versiones anteriores se desinstalen o actualicen a 4.1 ó 4.1 SP1 antes de actualizar a App-V 4.5.</span><span class="sxs-lookup"><span data-stu-id="1f25f-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="1f25f-115">Para actualizar los componentes de software en Application Virtualization System Computers</span><span class="sxs-lookup"><span data-stu-id="1f25f-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="1f25f-116">Vaya a la ubicación del programa de instalación en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en el archivo Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="1f25f-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="1f25f-117">En la página **principal** del asistente de instalación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="1f25f-118">En la página **contrato de licencia** , lea el contrato de licencia, seleccione Acepto **las condiciones del contrato de licencia**y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="1f25f-119">Cuando se abra la página **software instalado** y se muestre una lista de los componentes del sistema de virtualización de aplicaciones instalados y la versión de cada componente, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="1f25f-120">En la página **Advertencia de pérdida de sesión** , lea el mensaje que se muestra y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="1f25f-121">En la página **conectar con la base de datos de configuración** , revise el contenido de la página y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="1f25f-122">Si se muestra la página actualización de la **base de datos requerida** , es necesaria una actualización de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f25f-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="1f25f-123">Escriba las credenciales administrativas de la base de datos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="1f25f-124">Si no se muestra esta página, vaya al paso 9.</span><span class="sxs-lookup"><span data-stu-id="1f25f-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="1f25f-125">En la página **configuración de copia de seguridad** de la base de datos, active las casillas correspondientes para realizar la copia de seguridad y exportarla a una ubicación existente, y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="1f25f-126">**Importante**  Si desea poder revertir a la versión anterior en el caso de que se produzca un error de actualización, asegúrese de que activa la casilla **realizar una copia de seguridad de la base de datos de configuración** o perderá los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="1f25f-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="1f25f-127">Cuando desee restaurar una base de datos con VSS, primero debe detener el servicio de servidor de App-V en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="1f25f-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="1f25f-128">Debe hacerse en todos los servidores de administración si hay más de un servidor conectado a la misma base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f25f-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="1f25f-129">En la primera página de **validación del paquete** , lea el contenido y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="1f25f-130">En la segunda página de **validación del paquete** , tiene la opción de mostrar los detalles de la validación del paquete en una ventana del Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="1f25f-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="1f25f-131">Para ver los detalles, haga clic en **detalles**; en caso contrario, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="1f25f-132">En la página **listo para actualizar el programa** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="1f25f-133">En la página **Asistente para la instalación completada** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="1f25f-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="1f25f-134">Repita los pasos 1 a 12 en todos los demás equipos en los que instaló la consola de administración de virtualización de aplicaciones o el componente de software del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1f25f-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="1f25f-135">Después de actualizar el almacén de datos, puede reanudar el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="1f25f-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="1f25f-136">(El almacén de datos se actualiza cuando actualiza cualquier servidor o el servicio Web de administración de App-V).</span><span class="sxs-lookup"><span data-stu-id="1f25f-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="1f25f-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f25f-137">Related topics</span></span>


[<span data-ttu-id="1f25f-138">Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="1f25f-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





