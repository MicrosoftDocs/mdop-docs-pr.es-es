---
title: Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos
description: Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814014"
---
# <span data-ttu-id="2bb66-103">Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="2bb66-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="2bb66-104">Use el siguiente procedimiento para instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="2bb66-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="2bb66-105">Para instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="2bb66-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="2bb66-106">Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="2bb66-106">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="2bb66-107">Para iniciar la instalación de servidor de App-V 5,1, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="2bb66-107">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="2bb66-108">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-108">Click **Install**.</span></span>

2.  <span data-ttu-id="2bb66-109">En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="2bb66-110">En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="2bb66-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="2bb66-111">Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="2bb66-112">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-112">Click **Next**.</span></span>

4.  <span data-ttu-id="2bb66-113">En la página **selección de características** , seleccione la casilla servidor de **Administración** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="2bb66-114">En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="2bb66-115">En la página **configurar una base de datos de administración existente** , seleccione **usar un servidor SQL Server remoto**y escriba el nombre del equipo que ejecuta Microsoft SQL SQL, por ejemplo, **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="2bb66-116">Nota</span><span class="sxs-lookup"><span data-stu-id="2bb66-116">Note</span></span>**  
    <span data-ttu-id="2bb66-117">Si Microsoft SQL Server está implementado en el mismo servidor, seleccione **usar SQL Server local**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="2bb66-118">En la página **configurar el servidor de administración** , especifique el grupo de ad o la cuenta que se conectará a la consola de administración por razones administrativas, por ejemplo, **MyDomain\\MyUser** o **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="2bb66-119">La cuenta o el grupo de AD que especifique se habilitarán para administrar el servidor a través de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="2bb66-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="2bb66-120">Puede Agregar usuarios o grupos adicionales con la consola de administración después de la instalación</span><span class="sxs-lookup"><span data-stu-id="2bb66-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="2bb66-121">Especifique el **nombre del sitio web** que desea usar para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="2bb66-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="2bb66-122">Acepte el valor predeterminado si no tiene un nombre personalizado.</span><span class="sxs-lookup"><span data-stu-id="2bb66-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="2bb66-123">Para el **enlace de puertos**, especifique el número de puerto que se va a usar, por ejemplo **12345**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="2bb66-124">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="2bb66-124">Click **Install**.</span></span>

9. <span data-ttu-id="2bb66-125">Para confirmar que la configuración se ha completado correctamente, abra un explorador Web y escriba la siguiente dirección URL: http://managementserver:portnumber/Console .</span><span class="sxs-lookup"><span data-stu-id="2bb66-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.</span></span> <span data-ttu-id="2bb66-126">Si la instalación se realizó correctamente, debería ver que la **consola de administración** aparece sin ningún mensaje de error ni advertencia en pantalla.</span><span class="sxs-lookup"><span data-stu-id="2bb66-126">If the installation was successful, you should see the **Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="2bb66-127">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="2bb66-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2bb66-128">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="2bb66-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2bb66-129">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="2bb66-129">Got an App-V issue?</span></span>** <span data-ttu-id="2bb66-130">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2bb66-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2bb66-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bb66-131">Related topics</span></span>


[<span data-ttu-id="2bb66-132">Implementación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2bb66-132">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









