---
title: Cómo instalar la consola de administración
description: Cómo instalar la consola de administración
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817301"
---
# <span data-ttu-id="76e96-103">Cómo instalar la consola de administración</span><span class="sxs-lookup"><span data-stu-id="76e96-103">How to Install the Management Console</span></span>


<span data-ttu-id="76e96-104">Puede usar el siguiente procedimiento para instalar la consola de administración de virtualización de aplicaciones en un equipo de destino de la red.</span><span class="sxs-lookup"><span data-stu-id="76e96-104">You can use the following procedure to install the Application Virtualization Management Console on a target computer on the network.</span></span> <span data-ttu-id="76e96-105">Debe usar una cuenta de red que tenga privilegios de administrador en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="76e96-105">You must use a network account that has administrator privileges on the target computer.</span></span> <span data-ttu-id="76e96-106">Puede usar la consola para configurar y administrar la plataforma del sistema de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="76e96-106">You can use the console to configure and manage the Application Virtualization System Platform.</span></span>

<span data-ttu-id="76e96-107">Para poder completar este procedimiento, debe instalar el servicio Web de administración de virtualización de aplicaciones en este equipo o en otro.</span><span class="sxs-lookup"><span data-stu-id="76e96-107">Before you can complete this procedure, you must install the Application Virtualization Management Web Service on this or a different computer.</span></span> <span data-ttu-id="76e96-108">El servicio Web de administración le permite obtener acceso al almacén de datos y al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="76e96-108">The Management Web Service allows you to access the data store and the domain controller.</span></span> <span data-ttu-id="76e96-109">Para obtener más información sobre cómo instalar el servicio Web, vea [Cómo instalar el servicio Web de administración](how-to-install-the-management-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="76e96-109">For more information about installing the Web service, see [How to Install the Management Web Service](how-to-install-the-management-web-service.md).</span></span>

**<span data-ttu-id="76e96-110">Para instalar la consola de administración</span><span class="sxs-lookup"><span data-stu-id="76e96-110">To install the Management Console</span></span>**

1.  <span data-ttu-id="76e96-111">Compruebe que ninguna de las versiones anteriores de la consola de administración estén instaladas en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="76e96-111">Verify that no previous versions of the Management Console are installed on the target computer.</span></span>

2.  <span data-ttu-id="76e96-112">Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="76e96-112">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="76e96-113">En la **Página principal**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="76e96-113">On the **Welcome Page**, click **Next**.</span></span>

4.  <span data-ttu-id="76e96-114">En la página **contrato de licencia** , para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de licencia**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="76e96-114">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="76e96-115">En la página **información de registro** , especifique el nombre de **usuario** y la información de la **organización** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="76e96-115">On the **Registration Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

6.  <span data-ttu-id="76e96-116">En la página **tipo de configuración** , haga clic en **personalizar** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="76e96-116">On the **Setup Type** page, click **Custom** and then click **Next**.</span></span>

7.  <span data-ttu-id="76e96-117">En la página **Configuración personalizada** , anule la selección de todos los componentes del sistema de Application Virtualization, excepto la **consola de administración**y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="76e96-117">On the **Custom Setup** page, deselect all Application Virtualization System components except **Management Console**, and then click **Next**.</span></span>

    <span data-ttu-id="76e96-118">**Nota:**  Si un componente ya está instalado en el equipo, anulando la selección en la pantalla de instalación personalizada, se desinstalará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="76e96-118">**Note** If a component is already installed on the computer, by deselecting it on the Custom Setup screen, it will automatically be uninstalled.</span></span>

     

8.  <span data-ttu-id="76e96-119">En la pantalla **listo para modificar el programa** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="76e96-119">On the **Ready to Modify the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="76e96-120">**Nota:**  Si este es el primer componente que instala, se muestra la página **preparado para instalar el programa** .</span><span class="sxs-lookup"><span data-stu-id="76e96-120">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="76e96-121">Para iniciar la instalación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="76e96-121">To start the installation, click **Install**.</span></span>

     

9.  <span data-ttu-id="76e96-122">En la pantalla **Asistente para la instalación completada** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="76e96-122">On the **Installation Wizard Completed** screen, click **Finish**.</span></span> <span data-ttu-id="76e96-123">Haga clic en **Aceptar** para reiniciar el equipo y completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="76e96-123">Click **Okay** to restart the computer and complete the installation.</span></span>

10. <span data-ttu-id="76e96-124">En el panel de control de Windows, haga doble clic en **herramientas administrativas** y, a continuación, en **consola de administración de Application Virtualization** para mostrar la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="76e96-124">In the Windows Control Panel, double-click **Administrative Tools** and then click **Application Virtualization Management Console** to display the Management Console.</span></span>

11. <span data-ttu-id="76e96-125">Haga clic en el icono **conectar** , o haga clic con el botón secundario en el contenedor **sistemas de virtualización de aplicaciones** y luego haga clic en **conectar con el sistema de virtualización de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="76e96-125">Click the **Connect** icon, or right-click the **Application Virtualization Systems** container, and then click **Connect to Application Virtualization System**.</span></span>

12. <span data-ttu-id="76e96-126">En la pantalla **conectar a Application Virtualization System** , escriba el nombre de host y el puerto del equipo de servicio Web de administración, cambie la información de seguridad y las credenciales de inicio de sesión si es necesario, y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="76e96-126">On the **Connect to Application Virtualization System** screen, enter the host name and port of the Management Web Service computer, change the security information and login credentials if necessary, and then click **OK**.</span></span>

13. <span data-ttu-id="76e96-127">Después de conectar con el equipo del servicio Web de administración, haga clic en **archivo** en el menú de **consola** y, a continuación, haga clic en **salir**.</span><span class="sxs-lookup"><span data-stu-id="76e96-127">After connecting to the Management Web Service computer, click **File** on the **Console** menu, and then click **Exit**.</span></span> <span data-ttu-id="76e96-128">Haga clic en **sí** para guardar la configuración de la consola.</span><span class="sxs-lookup"><span data-stu-id="76e96-128">Click **Yes** to save console settings.</span></span>

## <span data-ttu-id="76e96-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76e96-129">Related topics</span></span>


[<span data-ttu-id="76e96-130">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="76e96-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





