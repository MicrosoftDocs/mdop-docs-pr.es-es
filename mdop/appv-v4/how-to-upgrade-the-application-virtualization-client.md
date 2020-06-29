---
title: Cómo actualizar el cliente de virtualización de aplicaciones
description: Cómo actualizar el cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816451"
---
# <span data-ttu-id="866f0-103">Cómo actualizar el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="866f0-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="866f0-104">Puede usar los procedimientos siguientes para actualizar el cliente de escritorio de Application Virtualization (App-V) o el cliente App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="866f0-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="866f0-105">Para actualizar el cliente, instale una nueva versión sobre la versión anterior instalada previamente.</span><span class="sxs-lookup"><span data-stu-id="866f0-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="866f0-106">Al actualizar los clientes, el software del instalador automáticamente conserva y migra la configuración del usuario para las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="866f0-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="866f0-107">Los derechos administrativos son necesarios para ejecutar el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="866f0-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="866f0-108">**Nota:**  Durante la actualización a Application Virtualization (App-V) 4.5 o versiones posteriores, los permisos para la clave del registro HKCU cambian.</span><span class="sxs-lookup"><span data-stu-id="866f0-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="866f0-109">Por ello, los usuarios perderán las configuraciones de usuario que se establecieron anteriormente, como la configuración del modo desconectado configurado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="866f0-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="866f0-110">Si el usuario no tiene permisos de forma activa para configurar el comportamiento de la interfaz de usuario del cliente mediante un bloqueo de permisos, el usuario puede restablecer estas preferencias después de una actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="866f0-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="866f0-111">**Importante**  Al actualizar a la versión 4.6 o a una versión posterior del cliente de App-V, debe usar el instalador correcto para el sistema operativo del equipo, 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="866f0-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="866f0-112">La instalación no se realizará y aparecerá un mensaje de error si usa el instalador equivocado.</span><span class="sxs-lookup"><span data-stu-id="866f0-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="866f0-113">Para actualizar el cliente de escritorio de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="866f0-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="866f0-114">Cierre todas las aplicaciones virtuales, haga clic con el botón derecho en el icono del cliente de escritorio de App-V que aparece en el área de notificación del escritorio de Windows y seleccione **salir** para cerrar el cliente existente.</span><span class="sxs-lookup"><span data-stu-id="866f0-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="866f0-115">Una vez que haya obtenido el archivo de instalación de instalador correcto y lo haya guardado en el equipo, haga doble clic en él para expandir el archivo.</span><span class="sxs-lookup"><span data-stu-id="866f0-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="866f0-116">Busque el archivo de setup.exe y haga doble clic en setup.exe para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="866f0-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="866f0-117">El asistente comprueba el sistema para asegurarse de que haya instalado todo el software necesario y le pedirá que instale cualquiera de las siguientes opciones, si no la encuentra:</span><span class="sxs-lookup"><span data-stu-id="866f0-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="866f0-118">Paquete redistribuible Microsoft VisualC + + 2005SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="866f0-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="866f0-119">Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="866f0-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="866f0-120">Informes de errores de aplicaciones de Microsoft</span><span class="sxs-lookup"><span data-stu-id="866f0-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="866f0-121">**Nota:**  Para la versión 4.6 o superior, el Asistente también instalará el siguiente requisito previo de software:</span><span class="sxs-lookup"><span data-stu-id="866f0-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="866f0-122">Paquete redistribuible Microsoft VisualC + + 2008SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="866f0-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="866f0-123">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="866f0-123">Click **Install**.</span></span> <span data-ttu-id="866f0-124">Se muestra el progreso de instalación y el estado cambia de **pendiente** a **instalación**.</span><span class="sxs-lookup"><span data-stu-id="866f0-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="866f0-125">El estado de la instalación cambiará a **correcto** , ya que cada paso se completa correctamente.</span><span class="sxs-lookup"><span data-stu-id="866f0-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="866f0-126">Cuando aparezca el cuadro de diálogo de **cliente de escritorio de Application Virtualization** y se muestre un mensaje que indica que se ha encontrado una versión anterior del cliente en el equipo, haga clic en **siguiente** para actualizar a la nueva versión.</span><span class="sxs-lookup"><span data-stu-id="866f0-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="866f0-127">Cuando aparezca la pantalla **contrato de licencia** , lea el contrato de licencia y, si está de acuerdo, haga clic en Acepto **las condiciones del contrato de licencia**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="866f0-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="866f0-128">Cuando el asistente InstallShield muestra la pantalla de diálogo **listo para actualizar el programa** , haga clic en **Actualizar** para iniciar la actualización.</span><span class="sxs-lookup"><span data-stu-id="866f0-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="866f0-129">La siguiente pantalla indica que el cliente se está instalando.</span><span class="sxs-lookup"><span data-stu-id="866f0-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="866f0-130">**ADVERTENCIA**  Si no ha cerrado el programa cliente en el paso 1, es posible que aparezca la advertencia **archivos en uso** .</span><span class="sxs-lookup"><span data-stu-id="866f0-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="866f0-131">Si esto sucede, haga clic con el botón derecho en el icono del cliente de App-V que se muestra en el área de notificación del escritorio y seleccione **salir** para cerrar el cliente existente.</span><span class="sxs-lookup"><span data-stu-id="866f0-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="866f0-132">A continuación, haga clic en **Reintentar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="866f0-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="866f0-133">Cuando la instalación se complete correctamente, se le pedirá que reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="866f0-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="866f0-134">Debe reiniciar el equipo para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="866f0-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="866f0-135">**PRECAUCIÓN**  Si la actualización no se realiza por algún motivo, tendrá que reiniciar el equipo antes de volver a intentar la actualización.</span><span class="sxs-lookup"><span data-stu-id="866f0-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="866f0-136">Para actualizar el cliente de virtualización de aplicaciones mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="866f0-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="866f0-137">Si actualiza el cliente de App-V con el programa setup.msi, asegúrese de que se haya instalado todo el software necesario.</span><span class="sxs-lookup"><span data-stu-id="866f0-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="866f0-138">Importante</span><span class="sxs-lookup"><span data-stu-id="866f0-138">Important</span></span>**  
    -   <span data-ttu-id="866f0-139">Para la versión 4.6 y posteriores del cliente de App-V, el programa de setup.msi comprueba el sistema y generará un mensaje de error que indica que la instalación no puede continuar si el software necesario no está instalado.</span><span class="sxs-lookup"><span data-stu-id="866f0-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="866f0-140">Para la versión 4.6 de App-V, los parámetros de la línea de comandos no se pueden usar durante una actualización y se omitirán.</span><span class="sxs-lookup"><span data-stu-id="866f0-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="866f0-141">En el siguiente ejemplo de línea de comandos se usa el archivo setup.msi para actualizar el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="866f0-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="866f0-142">Tendrá que usar el programa de instalación de cliente correcto, en función de si está actualizando el cliente de escritorio de App-V o el cliente App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="866f0-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="866f0-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="866f0-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="866f0-144">**Importante**  Las comillas solo son necesarias cuando el valor contiene un espacio.</span><span class="sxs-lookup"><span data-stu-id="866f0-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="866f0-145">Por coherencia, todas las instancias del ejemplo anterior se muestran con comillas.</span><span class="sxs-lookup"><span data-stu-id="866f0-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="866f0-146">Para actualizar el cliente de virtualización de aplicaciones para servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="866f0-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="866f0-147">Siga las directivas estándar de su organización para instalar o actualizar aplicaciones en el servidor de host de sesión de escritorio remoto (host RDSession).</span><span class="sxs-lookup"><span data-stu-id="866f0-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="866f0-148">Si el sistema forma parte de un conjunto de servidores, quite el host RDSession del conjunto de servidores.</span><span class="sxs-lookup"><span data-stu-id="866f0-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="866f0-149">Para actualizar el cliente de App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server), debe usar la línea de comandos porque no puede actualizar el cliente manualmente en el host de RDSession.</span><span class="sxs-lookup"><span data-stu-id="866f0-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="866f0-150">**Nota:**  En la versión 4,6 y posteriores de App-V, además de usar la línea de comandos para actualizar el cliente, también puede usar una sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="866f0-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="866f0-151">No se necesitan parámetros especiales para iniciar la sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="866f0-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="866f0-152">Una vez completada la actualización del cliente para servicios de escritorio remoto, reinicie e inicie sesión en el host RDSession.</span><span class="sxs-lookup"><span data-stu-id="866f0-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="866f0-153">Después de reiniciar el sistema, agregue el servidor a la granja de servidores.</span><span class="sxs-lookup"><span data-stu-id="866f0-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="866f0-154">**PRECAUCIÓN**  Si la actualización no se realiza por algún motivo, tendrá que reiniciar el equipo antes de volver a intentar la actualización.</span><span class="sxs-lookup"><span data-stu-id="866f0-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="866f0-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="866f0-155">Related topics</span></span>


[<span data-ttu-id="866f0-156">Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="866f0-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





