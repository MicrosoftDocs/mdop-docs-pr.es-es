---
title: Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración
description: Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración
author: dansimp
ms.assetid: c77e6662-7a18-4da1-8da8-b58068b65fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5a8cd5c914d1ddd720ebfef318e3a094cdc6f0b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813622"
---
# <span data-ttu-id="2a740-103">Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="2a740-103">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>


<span data-ttu-id="2a740-104">Use el procedimiento siguiente para ver y configurar las extensiones de paquete predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="2a740-104">Use the following procedure to view and configure default package extensions.</span></span>

**<span data-ttu-id="2a740-105">Para ver y configurar extensiones de aplicaciones virtuales predeterminadas</span><span class="sxs-lookup"><span data-stu-id="2a740-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="2a740-106">Para ver el paquete que desea configurar, abra la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2a740-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="2a740-107">Seleccione el paquete que desea configurar, haga clic con el botón secundario en el nombre del paquete y seleccione **Editar configuración predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="2a740-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="2a740-108">Para ver las aplicaciones contenidas en el paquete especificado, en el panel **configuración predeterminado** , haga clic en **aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="2a740-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="2a740-109">Para ver los accesos directos de ese paquete, haga clic en **accesos directos**.</span><span class="sxs-lookup"><span data-stu-id="2a740-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="2a740-110">Para ver las asociaciones de los tipos de archivo de ese paquete, haga clic en **tipos de archivo**.</span><span class="sxs-lookup"><span data-stu-id="2a740-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="2a740-111">Para habilitar las extensiones de la aplicación, seleccione **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="2a740-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="2a740-112">Para habilitar los métodos abreviados, seleccione **Habilitar métodos abreviados**.</span><span class="sxs-lookup"><span data-stu-id="2a740-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="2a740-113">Para agregar un nuevo acceso directo para la aplicación seleccionada, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Agregar nuevo acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="2a740-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="2a740-114">Para quitar un acceso directo, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Quitar acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="2a740-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="2a740-115">Para editar un acceso directo existente, haga clic con el botón derecho en la aplicación y seleccione **Editar acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="2a740-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="2a740-116">Para ver cualquier otra extensión de la aplicación, haga clic en **avanzadas** y en **exportar configuración**.</span><span class="sxs-lookup"><span data-stu-id="2a740-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="2a740-117">Escriba un nombre de archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="2a740-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="2a740-118">Puede ver todas las extensiones de aplicaciones asociadas con el paquete mediante el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a740-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="2a740-119">Para editar otras extensiones de aplicaciones, modifique el archivo de configuración y haga clic en **importar y sobrescriba esta configuración**.</span><span class="sxs-lookup"><span data-stu-id="2a740-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="2a740-120">Seleccione el archivo modificado y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="2a740-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="2a740-121">En el cuadro de diálogo, haga clic en **sobrescribir** para completar el proceso.</span><span class="sxs-lookup"><span data-stu-id="2a740-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="2a740-122">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="2a740-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2a740-123">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="2a740-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2a740-124">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="2a740-124">Got an App-V issue?</span></span>** <span data-ttu-id="2a740-125">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2a740-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2a740-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a740-126">Related topics</span></span>


[<span data-ttu-id="2a740-127">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2a740-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





