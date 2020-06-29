---
title: Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos
description: Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813974"
---
# <span data-ttu-id="d0fcb-103">Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="d0fcb-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="d0fcb-104">Use el siguiente procedimiento para instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="d0fcb-105">**Importante** Antes de realizar el siguiente procedimiento, debe leer y comprender [acerca de los informes de App-V 5,1](about-app-v-51-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="d0fcb-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="d0fcb-106">Para instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos</span><span class="sxs-lookup"><span data-stu-id="d0fcb-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="d0fcb-107">Copie los archivos de instalación de App-V 5,1 Server en el equipo en el que desea instalarlo.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="d0fcb-108">Para iniciar la instalación de servidor de App-V 5,1, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="d0fcb-109">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-109">Click **Install**.</span></span>

2. <span data-ttu-id="d0fcb-110">En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="d0fcb-111">En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="d0fcb-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="d0fcb-112">Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="d0fcb-113">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-113">Click **Next**.</span></span>

4. <span data-ttu-id="d0fcb-114">En la página **selección de características** , seleccione la casilla servidor de **informes** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="d0fcb-115">En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="d0fcb-116">En la página **configurar una base de datos de informes existente** , seleccione **usar un servidor SQL Server remoto**y escriba el nombre del equipo que ejecuta Microsoft SQL Server, por ejemplo, **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d0fcb-117">Si Microsoft SQL Server está implementado en el mismo servidor, seleccione **usar SQL Server local**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="d0fcb-118">Para la instancia de SQL Server, seleccione **usar la instancia predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="d0fcb-119">Si está usando una instancia personalizada de Microsoft SQL Server, debe seleccionar **usar una instancia personalizada** y, a continuación, escribir el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="d0fcb-120">Especifique el **nombre de la base de datos de SQL Server** que usará este servidor de informes, por ejemplo **AppvReporting**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="d0fcb-121">En la página **configurar el servidor de informes** .</span><span class="sxs-lookup"><span data-stu-id="d0fcb-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="d0fcb-122">Especifique el nombre del sitio web que desea usar para el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="d0fcb-123">Deje el valor predeterminado sin modificar si no tiene un nombre personalizado.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="d0fcb-124">Para el **enlace de Puerto**, especifique un número de puerto único que usará App-V 5,1, por ejemplo, **55555**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="d0fcb-125">También debe asegurarse de que el puerto especificado no esté siendo usado por otro sitio Web.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="d0fcb-126">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="d0fcb-126">Click **Install**.</span></span>

**<span data-ttu-id="d0fcb-127">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="d0fcb-127">Got an App-V issue?</span></span>** <span data-ttu-id="d0fcb-128">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d0fcb-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d0fcb-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0fcb-129">Related topics</span></span>

[<span data-ttu-id="d0fcb-130">Acerca de la generación de informes de App-V5.1</span><span class="sxs-lookup"><span data-stu-id="d0fcb-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="d0fcb-131">Implementación de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="d0fcb-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="d0fcb-132">Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="d0fcb-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
