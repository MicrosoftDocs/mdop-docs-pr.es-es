---
title: Cómo instalar el servidor de administración de virtualización de aplicaciones
description: Cómo instalar el servidor de administración de virtualización de aplicaciones
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817361"
---
# <span data-ttu-id="d5d76-103">Cómo instalar el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5d76-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="d5d76-104">El servidor de administración de virtualización de aplicaciones publica sus aplicaciones para los clientes.</span><span class="sxs-lookup"><span data-stu-id="d5d76-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="d5d76-105">En un entorno con equilibrio de carga, que es típico de implementaciones grandes, todos los servidores de un grupo de servidores deben transmitir las mismas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d5d76-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="d5d76-106">Si los servidores de administración de Application Virtualization van a publicar distintas aplicaciones, asigne los servidores a diferentes grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="d5d76-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="d5d76-107">En este caso, es posible que también tenga que aumentar la capacidad de un grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="d5d76-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="d5d76-108">Si ha designado un equipo de destino en la red y tiene una cuenta de inicio de sesión con privilegios de administrador local, puede usar el siguiente procedimiento para instalar el servidor de administración de virtualización de aplicaciones y asignarlo al grupo de servidores correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d5d76-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="d5d76-109">Nota</span><span class="sxs-lookup"><span data-stu-id="d5d76-109">Note</span></span>**  
<span data-ttu-id="d5d76-110">El Asistente para la instalación puede crear un registro de grupo de servidores, si no existe alguno, así como un registro de la pertenencia del servidor de virtualización de Application Virtualization en este grupo.</span><span class="sxs-lookup"><span data-stu-id="d5d76-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="d5d76-111">Después de completar el proceso de instalación, reinicie el servidor.</span><span class="sxs-lookup"><span data-stu-id="d5d76-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="d5d76-112">Para instalar un servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5d76-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="d5d76-113">Compruebe y, si es necesario, desinstale versiones anteriores del servidor de administración de virtualización de aplicaciones que estén instaladas en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="d5d76-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="d5d76-114">Para abrir el Asistente para la **instalación de Microsoft Application Virtualization Management Server** , vaya a la ubicación del sistema de virtualización de aplicaciones **setup.exe** en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en el archivo de **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="d5d76-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="d5d76-115">En la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="d5d76-116">En la página **contrato de licencia** , lea el contrato de licencia y, para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de la licencia**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="d5d76-117">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-117">Click **Next**.</span></span>

5.  <span data-ttu-id="d5d76-118">En la página **información de registro** , debe escribir el nombre de usuario y la **organización**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="d5d76-119">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-119">Click **Next**.</span></span>

6.  <span data-ttu-id="d5d76-120">En la página **tipo de configuración** , seleccione **personalizado**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="d5d76-121">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-121">Click **Next**.</span></span> <span data-ttu-id="d5d76-122">En la página **Configuración personalizada** , anule la selección de todos los componentes del sistema de Application Virtualization, excepto **servidor de virtualización de aplicaciones**y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="d5d76-123">Actúe</span><span class="sxs-lookup"><span data-stu-id="d5d76-123">Caution</span></span>**  
    <span data-ttu-id="d5d76-124">Si un componente ya está instalado en el equipo, cuando lo anule en la ventana de **instalación personalizada** , el componente se desinstalará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d5d76-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="d5d76-125">En la **página base de datos de configuración** , seleccione un servidor de base de datos de la lista de servidores disponibles o agregar un servidor seleccionando **usar el siguiente nombre de host** y especificando los datos de nombre del **servidor** y **número de Puerto** .</span><span class="sxs-lookup"><span data-stu-id="d5d76-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="d5d76-126">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-126">Click **Next**.</span></span>

    **<span data-ttu-id="d5d76-127">Nota</span><span class="sxs-lookup"><span data-stu-id="d5d76-127">Note</span></span>**  
    <span data-ttu-id="d5d76-128">El servidor de administración de virtualización de aplicaciones no admite SQL con distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d5d76-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="d5d76-129">En la página **modo de seguridad de conexión** , seleccione el certificado deseado de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="d5d76-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="d5d76-130">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-130">Click **Next**.</span></span>

   **<span data-ttu-id="d5d76-131">Nota</span><span class="sxs-lookup"><span data-stu-id="d5d76-131">Note</span></span>**  
   <span data-ttu-id="d5d76-132">La configuración del **modo de conexión segura** requiere que el servidor tenga un certificado de servidor provisto de una infraestructura de clave pública.</span><span class="sxs-lookup"><span data-stu-id="d5d76-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="d5d76-133">Si un certificado de servidor no está instalado en el servidor, esta opción no está disponible y no se puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="d5d76-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="d5d76-134">Debe conceder acceso de lectura a la cuenta de servicio de red al certificado que se está usando.</span><span class="sxs-lookup"><span data-stu-id="d5d76-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="d5d76-135">En la página **configuración del puerto TCP** , para usar el puerto predeterminado (554), seleccione **usar puerto predeterminado (554)**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="d5d76-136">Para especificar un puerto personalizado, seleccione **usar puerto personalizado** y especifique el número de puerto que se usará.</span><span class="sxs-lookup"><span data-stu-id="d5d76-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="d5d76-137">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-137">Click **Next**.</span></span>

   **<span data-ttu-id="d5d76-138">Nota</span><span class="sxs-lookup"><span data-stu-id="d5d76-138">Note</span></span>**  
   <span data-ttu-id="d5d76-139">Al instalar el servidor en un entorno no seguro, puede usar el puerto predeterminado (554) o puede definir un puerto personalizado.</span><span class="sxs-lookup"><span data-stu-id="d5d76-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="d5d76-140">En la página **grupo de administradores** , especifique el nombre del grupo de seguridad autorizado para administrar este servidor en nombre de **Grupo**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="d5d76-141">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-141">Click **Next**.</span></span> <span data-ttu-id="d5d76-142">Confirme el grupo especificado y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="d5d76-143">En la página **grupo de proveedores predeterminado** , especifique el nombre del grupo de proveedores predeterminado y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="d5d76-144">En la página **ruta de contenido** , especifique la ubicación en el equipo de destino donde se guardarán los archivos de SFT y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="d5d76-145">Nota</span><span class="sxs-lookup"><span data-stu-id="d5d76-145">Note</span></span>**  
   <span data-ttu-id="d5d76-146">Si el puerto HTTP o RTSP del servidor de administración ya está asignado, se le pedirá que elija un nuevo puerto.</span><span class="sxs-lookup"><span data-stu-id="d5d76-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="d5d76-147">Seleccione el puerto que desee y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="d5d76-148">En la página **listo para instalar el programa** , para instalar el servidor de administración de virtualización de aplicaciones, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="d5d76-149">Nota</span><span class="sxs-lookup"><span data-stu-id="d5d76-149">Note</span></span>**  
   <span data-ttu-id="d5d76-150">Si se muestra el error 25120 al intentar completar este paso, debe habilitar **las herramientas de administración y los scripts de administración de**IIS.</span><span class="sxs-lookup"><span data-stu-id="d5d76-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="d5d76-151">Para habilitar esta característica de Windows, abra el panel de control **programas y características** , seleccione **activar o desactivar las características de Windows**y vaya a **servicios de información de Internet.**</span><span class="sxs-lookup"><span data-stu-id="d5d76-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="d5d76-152">En **herramientas de administración web**, habilite **scripts y herramientas de administración de IIS**.</span><span class="sxs-lookup"><span data-stu-id="d5d76-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="d5d76-153">En la pantalla Asistente para la **instalación finalizada** , haga clic en **Finalizar**para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="d5d76-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="d5d76-154">Importante</span><span class="sxs-lookup"><span data-stu-id="d5d76-154">Important</span></span>**  
   <span data-ttu-id="d5d76-155">La instalación puede demorar unos minutos en finalizar.</span><span class="sxs-lookup"><span data-stu-id="d5d76-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="d5d76-156">Un mensaje de estado parpadeará por encima del área de notificación del escritorio de Windows, lo que indica que la instalación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5d76-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="d5d76-157">No es necesario reiniciar el equipo cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="d5d76-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="d5d76-158">Sin embargo, para optimizar el rendimiento del sistema, se recomienda un reinicio.</span><span class="sxs-lookup"><span data-stu-id="d5d76-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="d5d76-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5d76-159">Related topics</span></span>


[<span data-ttu-id="d5d76-160">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="d5d76-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)









