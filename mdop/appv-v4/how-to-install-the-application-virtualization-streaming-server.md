---
title: Cómo instalar el servidor de streaming de virtualización de aplicaciones
description: Cómo instalar el servidor de streaming de virtualización de aplicaciones
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817330"
---
# <span data-ttu-id="6b854-103">Cómo instalar el servidor de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6b854-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="6b854-104">El servidor de streaming de Application Virtualization publica sus aplicaciones para los clientes.</span><span class="sxs-lookup"><span data-stu-id="6b854-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="6b854-105">En un entorno con equilibrio de carga, que es típico de implementaciones grandes, todos los servidores de un grupo de servidores deben transmitir las mismas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6b854-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="6b854-106">Si los servidores de streaming de Application Virtualization van a transmitir aplicaciones distintas, asigne los servidores a diferentes grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="6b854-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="6b854-107">En este caso, es posible que también tenga que aumentar la capacidad de un grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="6b854-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="6b854-108">Si ha designado un equipo de destino en la red, con una cuenta de inicio de sesión con privilegios administrativos locales, puede usar el siguiente procedimiento para instalar el servidor de streaming de virtualización de aplicaciones y asignarlo al grupo de servidores correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6b854-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="6b854-109">**Nota:**  El Asistente para la instalación puede crear un registro de grupo de servidores, si no existe alguno, y un registro de la pertenencia a un servidor de streaming de Application Virtualization en este grupo.</span><span class="sxs-lookup"><span data-stu-id="6b854-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="6b854-110">Después de completar el proceso de instalación, reinicie el servidor.</span><span class="sxs-lookup"><span data-stu-id="6b854-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="6b854-111">Para instalar un servidor de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6b854-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="6b854-112">Compruebe que ninguna de las versiones anteriores del servidor de streaming de Application Virtualization están instaladas en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="6b854-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="6b854-113">**Importante**  Asegúrese de que el servidor de administración de App-V no esté instalado en este equipo.</span><span class="sxs-lookup"><span data-stu-id="6b854-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="6b854-114">Los dos productos no se pueden instalar en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="6b854-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="6b854-115">Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en el archivo **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="6b854-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="6b854-116">En la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="6b854-117">En la página **contrato de licencia** , para aceptar los términos de licencia, seleccione Acepto **los términos y condiciones de la**licencia y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="6b854-118">En la página **información del cliente** , especifique el nombre de **usuario** y la organización y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="6b854-119">En la página **ruta de instalación** , haga clic en **examinar**, especifique la ubicación en la que desea instalar el servidor de streaming y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="6b854-120">En la página **modo de seguridad de conexión** , seleccione el certificado que desee de la lista desplegable y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="6b854-121">**Nota:**  La configuración del **modo de conexión segura** requiere que el servidor tenga un certificado de servidor provisto de una infraestructura de clave pública.</span><span class="sxs-lookup"><span data-stu-id="6b854-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="6b854-122">Si un certificado de servidor no está instalado en el servidor, esta opción no está disponible y no se puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="6b854-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="6b854-123">Debe conceder acceso de lectura a la cuenta de servicio de red al certificado que se está usando.</span><span class="sxs-lookup"><span data-stu-id="6b854-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="6b854-124">En la página **configuración del puerto TCP** , para usar el puerto estándar (554), seleccione **usar puerto predeterminado (554)**.</span><span class="sxs-lookup"><span data-stu-id="6b854-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="6b854-125">Para especificar un puerto personalizado, seleccione **usar puerto personalizado**, especifique el número de puerto en el campo correspondiente y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="6b854-126">**Nota:**  Al instalar el servidor en un escenario no seguro, puede usar el puerto predeterminado (554) o puede definir un puerto personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b854-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="6b854-127">En la página **raíz de contenido** , especifique la ubicación en el equipo de destino donde se guardarán los archivos de SFT y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="6b854-128">**Nota:**  Si el puerto HTTP o RTSP del servidor de streaming de aplicaciones virtuales ya está asignado, se le pedirá que seleccione un nuevo puerto.</span><span class="sxs-lookup"><span data-stu-id="6b854-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="6b854-129">Especifique el puerto que desee y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6b854-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="6b854-130">En la pantalla **Configuración avanzada** , escriba la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b854-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="6b854-131">Número máximo de conexiones de cliente</span><span class="sxs-lookup"><span data-stu-id="6b854-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="6b854-132">Tiempo de espera de conexión (s)</span><span class="sxs-lookup"><span data-stu-id="6b854-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="6b854-133">Tamaño del grupo de subprocesos RTSP</span><span class="sxs-lookup"><span data-stu-id="6b854-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="6b854-134">Tiempo de espera de RTSP (SEC)</span><span class="sxs-lookup"><span data-stu-id="6b854-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="6b854-135">Número de procesos principales</span><span class="sxs-lookup"><span data-stu-id="6b854-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="6b854-136">Tiempo de espera del núcleo (SEC)</span><span class="sxs-lookup"><span data-stu-id="6b854-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="6b854-137">Habilitar autenticación de usuario</span><span class="sxs-lookup"><span data-stu-id="6b854-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="6b854-138">Habilitar autorización de usuario</span><span class="sxs-lookup"><span data-stu-id="6b854-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="6b854-139">Tamaño de bloque de caché (KB)</span><span class="sxs-lookup"><span data-stu-id="6b854-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="6b854-140">Tamaño máximo de la caché (MB)</span><span class="sxs-lookup"><span data-stu-id="6b854-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="6b854-141">**Nota:**  El servidor de streaming de App-V usa permisos de sistema de archivos NTFS para controlar el acceso a las aplicaciones en el recurso compartido de contenido.</span><span class="sxs-lookup"><span data-stu-id="6b854-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="6b854-142">Use **Habilitar autenticación de usuario** y **Habilitar autorización de usuario** para controlar si el servidor comprueba y aplica esas listas de control de acceso (ACL) o no.</span><span class="sxs-lookup"><span data-stu-id="6b854-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="6b854-143">En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="6b854-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="6b854-144">En la pantalla Asistente para la **instalación finalizada** , haga clic en **Finalizar**para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="6b854-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="6b854-145">**Importante**  La instalación puede demorar varios minutos en finalizar.</span><span class="sxs-lookup"><span data-stu-id="6b854-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="6b854-146">Un mensaje de estado parpadeará por encima del área de notificación del escritorio de Windows, lo que indica que la instalación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b854-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="6b854-147">No es necesario que reinicie el equipo cuando se le pida.</span><span class="sxs-lookup"><span data-stu-id="6b854-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="6b854-148">Sin embargo, para optimizar el rendimiento del sistema, recomendamos un reinicio.</span><span class="sxs-lookup"><span data-stu-id="6b854-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="6b854-149">Repita los pasos 1 a 12 para cada servidor de aplicaciones virtual que tenga que instalar.</span><span class="sxs-lookup"><span data-stu-id="6b854-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="6b854-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b854-150">Related topics</span></span>


[<span data-ttu-id="6b854-151">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="6b854-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





