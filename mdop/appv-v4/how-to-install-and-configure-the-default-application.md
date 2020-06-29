---
title: Cómo instalar y configurar la aplicación predeterminada
description: Cómo instalar y configurar la aplicación predeterminada
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817370"
---
# <span data-ttu-id="d44f2-103">Cómo instalar y configurar la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="d44f2-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="d44f2-104">La aplicación predeterminada se proporciona como parte de la instalación y se copia automáticamente en el servidor de administración de Microsoft Application Virtualization (App-V) durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="d44f2-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="d44f2-105">Se usa para comprobar que el servidor de administración se ha instalado y configurado correctamente, pero debe publicarse en el cliente de Microsoft Application Virtualization (App-V) para que el usuario pueda obtener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="d44f2-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="d44f2-106">Use los procedimientos siguientes para publicar la aplicación predeterminada y para transmitirla.</span><span class="sxs-lookup"><span data-stu-id="d44f2-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="d44f2-107">Para publicar la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="d44f2-107">To publish the default application</span></span>**

1.  <span data-ttu-id="d44f2-108">Inicie sesión en el servidor de administración de App-V con una cuenta que sea miembro del grupo de administradores de App-V especificado durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="d44f2-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="d44f2-109">En el servidor de administración de App-V, haga clic en **Inicio**, haga clic en **herramientas administrativas**y, a continuación, en **consola de administración de virtualización de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="d44f2-110">En la consola de administración de App-V, haga clic en **acciones**y, a continuación, haga clic en **conectar con el sistema de virtualización de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="d44f2-111">En la página **Configurar conexión** , desactive la casilla **Usar conexión segura** .</span><span class="sxs-lookup"><span data-stu-id="d44f2-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="d44f2-112">En el cuadro **nombre de host de servicio Web** , escriba el nombre de dominio completo (FQDN) del servidor de administración de App-V y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="d44f2-113">**Nota:**  También puede usar **localhost** para el nombre de host de servicio Web si está instalado en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="d44f2-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="d44f2-114">En la consola de administración de App-V, haga clic con el botón secundario en el nodo de **servidor** y haga clic en **Opciones del sistema**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="d44f2-115">En la pestaña **General** , en el cuadro **ruta de contenido predeterminada** , escriba la ruta de acceso UNC (Convención de nomenclatura universal) a la carpeta de contenido que creó en el servidor durante la instalación; por ejemplo, \ \ \ \ &lt; nombre de servidor &gt; \\Content y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="d44f2-116">**Importante**  Use el FQDN para el nombre del servidor para que el cliente pueda resolver el nombre correctamente.</span><span class="sxs-lookup"><span data-stu-id="d44f2-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="d44f2-117">En la consola de administración de App-V, en el panel de navegación, expanda el nodo **servidor** y, a continuación, haga clic en **aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="d44f2-118">En el panel de temas, haga clic en **aplicación predeterminada**y, a continuación, en el panel **acciones** , haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="d44f2-119">En el cuadro de diálogo **propiedades** , junto al cuadro Ruta de la **OSD** , haga clic en **examinar**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="d44f2-120">En el cuadro de diálogo **abrir** , escriba la ruta de acceso UNC a la carpeta de contenido que creó en el servidor durante la instalación; por ejemplo, \ \ \ \ &lt; nombre de servidor &gt; \\Content y presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="d44f2-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="d44f2-121">Debe usar el nombre de servidor real y no puede usar el **localhost** aquí.</span><span class="sxs-lookup"><span data-stu-id="d44f2-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="d44f2-122">**Importante**  Asegúrese de que los valores de los cuadros **ruta de acceso** de la OSD e ruta de acceso al **icono** estén en formato UNC (por ejemplo, \ \ \ \ &lt; nombre de servidor &gt; \\Content\\DefaultApp.ico) y seleccione la carpeta de contenido que ha creado al instalar el servidor.</span><span class="sxs-lookup"><span data-stu-id="d44f2-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="d44f2-123">No use **localhost** o una ruta de acceso de archivo que contenga una letra de unidad, como C:\\Archivos de Files\\.. \\.. Objetos.</span><span class="sxs-lookup"><span data-stu-id="d44f2-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="d44f2-124">Seleccione el archivo DefaultApp. OSD y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="d44f2-125">Repita los pasos anteriores para configurar la ruta de acceso del icono.</span><span class="sxs-lookup"><span data-stu-id="d44f2-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="d44f2-126">Haga clic en la pestaña **permisos de acceso** y confirme que el grupo de usuarios de App-V tiene permisos de acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d44f2-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="d44f2-127">Haga clic en la pestaña **métodos abreviados** y luego en **publicar en el escritorio del usuario**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="d44f2-128">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d44f2-128">Click **OK**.</span></span>

16. <span data-ttu-id="d44f2-129">Abra el explorador de Windows y busque el directorio de contenido.</span><span class="sxs-lookup"><span data-stu-id="d44f2-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="d44f2-130">Haga doble clic en el archivo DefaultApp. OSD y ábralo con el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="d44f2-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="d44f2-131">Busque la línea que contiene la etiqueta **href** y cámbiela por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="d44f2-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="d44f2-132">O bien, si usa RTSPs:</span><span class="sxs-lookup"><span data-stu-id="d44f2-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="d44f2-133">Cierre el archivo DefaultApp. OSD y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="d44f2-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="d44f2-134">Para transmitir la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="d44f2-134">To stream the default application</span></span>**

1.  <span data-ttu-id="d44f2-135">En el equipo que tiene instalado el cliente de App-V, inicie sesión como un usuario que sea miembro del grupo de usuarios de Application Virtualization especificado durante la instalación del servidor.</span><span class="sxs-lookup"><span data-stu-id="d44f2-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="d44f2-136">En el escritorio, aparece el método abreviado de **aplicaciones predeterminado aplicación de virtualización** .</span><span class="sxs-lookup"><span data-stu-id="d44f2-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="d44f2-137">Haga doble clic en el acceso directo para iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d44f2-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="d44f2-138">Una barra de estado, que aparece sobre el área de notificación de Windows, informa que la aplicación se está iniciando.</span><span class="sxs-lookup"><span data-stu-id="d44f2-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="d44f2-139">Si el inicio de la aplicación se realiza correctamente, se muestra la pantalla de título de la aplicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d44f2-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="d44f2-140">Haga clic en **Aceptar** para cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d44f2-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="d44f2-141">Ya ha confirmado que el sistema de App-V se está ejecutando correctamente.</span><span class="sxs-lookup"><span data-stu-id="d44f2-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="d44f2-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d44f2-142">Related topics</span></span>


[<span data-ttu-id="d44f2-143">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="d44f2-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





