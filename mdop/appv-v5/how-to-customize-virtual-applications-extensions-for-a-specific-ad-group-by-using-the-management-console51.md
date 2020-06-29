---
title: Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración
description: Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración
author: dansimp
ms.assetid: dd71df05-512f-4eb4-a55f-e5b93601323d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bf086da3fbb6938a4fc602af5ab63adb1621532
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814255"
---
# <span data-ttu-id="d7609-103">Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="d7609-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="d7609-104">Use el siguiente procedimiento para personalizar las extensiones de aplicación virtual para un grupo de Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="d7609-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="d7609-105">Para personalizar las extensiones de aplicaciones virtuales para un grupo de AD</span><span class="sxs-lookup"><span data-stu-id="d7609-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="d7609-106">Para ver el paquete que desea configurar, abra la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d7609-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="d7609-107">Para ver la configuración que está asignada a un grupo de usuarios determinado, seleccione el paquete y haga clic con el botón secundario en el nombre del paquete y seleccione **Editar acceso de Active**Directory.</span><span class="sxs-lookup"><span data-stu-id="d7609-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="d7609-108">Como alternativa, seleccione el paquete y haga clic en **Editar** en el panel de **acceso ad** .</span><span class="sxs-lookup"><span data-stu-id="d7609-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="d7609-109">Para personalizar un grupo de AD, puede buscar el grupo en la lista de **entidades de ad con Access**.</span><span class="sxs-lookup"><span data-stu-id="d7609-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="d7609-110">Después, con el cuadro desplegable en el panel **configuración asignada** , seleccione **personalizado**y, a continuación, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="d7609-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="d7609-111">Para deshabilitar todas las extensiones para una aplicación determinada, desactive **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="d7609-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="d7609-112">Para agregar un nuevo acceso directo para la aplicación seleccionada, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Agregar nuevo acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="d7609-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="d7609-113">Para quitar un acceso directo, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Quitar acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="d7609-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="d7609-114">Para editar un acceso directo existente, haga clic con el botón derecho en la aplicación y seleccione **Editar acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="d7609-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="d7609-115">Para ver cualquier otra extensión de la aplicación, haga clic en **avanzadas**y en **exportar configuración**.</span><span class="sxs-lookup"><span data-stu-id="d7609-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="d7609-116">Escriba un nombre de archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="d7609-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="d7609-117">Puede ver todas las extensiones de aplicaciones asociadas con el paquete mediante el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="d7609-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="d7609-118">Para editar extensiones de aplicación adicionales, modifique el archivo de configuración y haga clic en **importar y sobrescriba esta configuración**.</span><span class="sxs-lookup"><span data-stu-id="d7609-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="d7609-119">Seleccione el archivo modificado y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="d7609-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="d7609-120">En el cuadro de diálogo, haga clic en **sobrescribir** para completar el proceso.</span><span class="sxs-lookup"><span data-stu-id="d7609-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="d7609-121">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="d7609-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d7609-122">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="d7609-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d7609-123">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="d7609-123">Got an App-V issue?</span></span>** <span data-ttu-id="d7609-124">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d7609-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d7609-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7609-125">Related topics</span></span>


[<span data-ttu-id="d7609-126">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="d7609-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





