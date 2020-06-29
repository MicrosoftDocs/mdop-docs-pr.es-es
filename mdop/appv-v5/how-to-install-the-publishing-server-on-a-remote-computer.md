---
title: Cómo instalar el servidor de publicación en un equipo remoto
description: Cómo instalar el servidor de publicación en un equipo remoto
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813998"
---
# <span data-ttu-id="36cec-103">Cómo instalar el servidor de publicación en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="36cec-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="36cec-104">Use el siguiente procedimiento para instalar el servidor de publicación en un equipo independiente.</span><span class="sxs-lookup"><span data-stu-id="36cec-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="36cec-105">Antes de llevar a cabo el siguiente procedimiento, asegúrese de que la base de datos y el servidor de administración están disponibles.</span><span class="sxs-lookup"><span data-stu-id="36cec-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="36cec-106">Para instalar el servidor de publicación en un equipo independiente</span><span class="sxs-lookup"><span data-stu-id="36cec-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="36cec-107">Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="36cec-107">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="36cec-108">Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="36cec-108">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="36cec-109">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="36cec-109">Click **Install**.</span></span>

2. <span data-ttu-id="36cec-110">En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="36cec-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="36cec-111">En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="36cec-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="36cec-112">Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="36cec-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="36cec-113">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="36cec-113">Click **Next**.</span></span>

4. <span data-ttu-id="36cec-114">En la página **selección de características** , seleccione la casilla **Publishing Server** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="36cec-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="36cec-115">En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="36cec-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="36cec-116">En la página **configurar Publishing Server** , especifique los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="36cec-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="36cec-117">La dirección URL del servicio de administración a la que se conectará el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="36cec-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="36cec-118">Por ejemplo, **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="36cec-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="36cec-119">Especifique el nombre del sitio web que desea usar para el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="36cec-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="36cec-120">Acepte el valor predeterminado si no tiene un nombre personalizado.</span><span class="sxs-lookup"><span data-stu-id="36cec-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="36cec-121">Para el **enlace de Puerto**, especifique un número de puerto único que usará App-V 5,0, por ejemplo, **54321**.</span><span class="sxs-lookup"><span data-stu-id="36cec-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.0, for example **54321**.</span></span>

7. <span data-ttu-id="36cec-122">En la página **preparado para instalar** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="36cec-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="36cec-123">Una vez completada la instalación, el servidor de publicación debe registrarse en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="36cec-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="36cec-124">En la consola de administración de App-V 5,0, realice los siguientes pasos para registrar el servidor:</span><span class="sxs-lookup"><span data-stu-id="36cec-124">In the App-V 5.0 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="36cec-125">Abra la consola de servidor de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="36cec-125">Open the App-V 5.0 management server console.</span></span>

   2.  <span data-ttu-id="36cec-126">En el panel izquierdo, seleccione **Servers**y, a continuación, **Register New Server**.</span><span class="sxs-lookup"><span data-stu-id="36cec-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="36cec-127">Escriba el nombre de este servidor y una descripción (si es necesario) y haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="36cec-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="36cec-128">Para comprobar si el servidor de publicación se está ejecutando correctamente, debe importar un paquete al servidor de administración, encontrarlo en un grupo de AD y publicar el paquete.</span><span class="sxs-lookup"><span data-stu-id="36cec-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="36cec-129">Con un explorador de Internet, abra la siguiente dirección URL: <strong> http://publishingserver:pubport </strong> .</span><span class="sxs-lookup"><span data-stu-id="36cec-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="36cec-130">Si el servidor se ejecuta correctamente, se mostrará información similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="36cec-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="36cec-131">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="36cec-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="36cec-132">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="36cec-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="36cec-133">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="36cec-133">Got an App-V issue?</span></span>** <span data-ttu-id="36cec-134">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="36cec-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="36cec-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36cec-135">Related topics</span></span>


[<span data-ttu-id="36cec-136">Implementación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="36cec-136">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

 

 





