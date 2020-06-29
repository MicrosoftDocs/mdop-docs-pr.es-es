---
title: Cómo instalar una base de datos
description: Cómo instalar una base de datos
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817380"
---
# <span data-ttu-id="6977f-103">Cómo instalar una base de datos</span><span class="sxs-lookup"><span data-stu-id="6977f-103">How to Install a Database</span></span>


<span data-ttu-id="6977f-104">Puede usar el siguiente procedimiento para instalar una base de datos para la implementación basada en servidor de la virtualización de aplicaciones si aún no está disponible una base de datos.</span><span class="sxs-lookup"><span data-stu-id="6977f-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="6977f-105">Por lo general, en un entorno de producción, se conectará a una base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="6977f-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="6977f-106">**Importante**  Para instalar la base de datos, debe usar una cuenta de red con los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="6977f-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="6977f-107">Si su organización requiere que solo los administradores de bases de datos puedan crear y llevar a cabo actualizaciones de la base de datos, están disponibles las secuencias de comandos que permiten realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="6977f-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="6977f-108">Para instalar una base de datos</span><span class="sxs-lookup"><span data-stu-id="6977f-108">To install a database</span></span>**

1.  <span data-ttu-id="6977f-109">Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="6977f-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="6977f-110">En la **Página principal**, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="6977f-111">En la página **contrato de licencia** , para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de licencia**y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="6977f-112">En la página **información de registro** , especifique el **nombre de usuario** y la información de la **organización** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="6977f-113">En la página **tipo de configuración** , seleccione **personalizado** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="6977f-114">En la página **Configuración personalizada** , anule la selección de todos los componentes del sistema de Application Virtualization, excepto **servidor de virtualización de aplicaciones**y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="6977f-115">**Nota:**  Si un componente ya está instalado en el equipo, anulando la selección en la pantalla de **instalación personalizada** , se desinstalará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6977f-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="6977f-116">En la página **servidor de base de datos** , escriba las contraseñas, asigne una ruta de instalación, guarde la información y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="6977f-117">Seleccione un nombre para la base de datos y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="6977f-118">**Nota:**  Si se muestra el error 25109 al intentar completar este paso, no ha configurado correctamente los permisos necesarios para instalar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6977f-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="6977f-119">Para obtener más información sobre cómo configurar los permisos de SQL necesarios, consulte <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="6977f-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="6977f-120">En la pantalla **servidor de directorio** , escriba un nombre de dominio y las credenciales que usarán los servidores de virtualización de aplicaciones y el servicio Web de administración para obtener acceso al controlador de dominio, guarde esta información y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="6977f-121">**Nota:**  La instalación se establecerá de forma predeterminada en el dominio del equipo actual.</span><span class="sxs-lookup"><span data-stu-id="6977f-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="6977f-122">En la página **grupo de administradores** , escriba el nombre de un grupo que tendrá privilegios de administrador, guarde esta información y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="6977f-123">**Nota:**  También puede introducir los primeros caracteres del nombre de un grupo que tendrá privilegios de administración, hacer clic en **siguiente**y, en la pantalla **Seleccionar grupo de administradores** , seleccionar el grupo de la lista resultante.</span><span class="sxs-lookup"><span data-stu-id="6977f-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="6977f-124">A continuación, guarda esta información y haz clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="6977f-125">En la página **grupo de proveedores predeterminado** , escriba el nombre completo de un grupo que controlará el acceso a las aplicaciones, guarde esta información y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="6977f-126">**Nota:**  También puede introducir los primeros caracteres del nombre de un grupo que controlará el acceso a las aplicaciones, hacer clic en **siguiente**y, en la pantalla **Seleccionar grupo de proveedores predeterminado** , seleccione el grupo en la lista.</span><span class="sxs-lookup"><span data-stu-id="6977f-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="6977f-127">A continuación, guarda esta información y haz clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="6977f-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="6977f-128">En la página Asistente para la **instalación finalizada** , haga clic en **Finalizar**para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="6977f-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="6977f-129">**Importante**  La instalación puede demorar unos minutos en finalizar.</span><span class="sxs-lookup"><span data-stu-id="6977f-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="6977f-130">Un mensaje de estado parpadeará por encima del área de notificación del escritorio de Windows, lo que indica si la instalación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6977f-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="6977f-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6977f-131">Related topics</span></span>


[<span data-ttu-id="6977f-132">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="6977f-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





