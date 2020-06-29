---
title: Cómo agregar o actualizar paquetes mediante el uso de la consola de administración
description: Cómo agregar o actualizar paquetes mediante el uso de la consola de administración
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814470"
---
# <span data-ttu-id="a4dbe-103">Cómo agregar o actualizar paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="a4dbe-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="a4dbe-104">Puede realizar el procedimiento siguiente para agregar o actualizar un paquete a la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-104">You can the following procedure to add or upgrade a package to the App-V 5.0 Management Console.</span></span> <span data-ttu-id="a4dbe-105">Para actualizar un paquete que ya existe en la consola de administración, siga estos pasos e importe el paquete actualizado con el mismo **nombre**de paquete.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="a4dbe-106">Para agregar un paquete a la consola de administración</span><span class="sxs-lookup"><span data-stu-id="a4dbe-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="a4dbe-107">Haga clic en la ficha **paquetes** en el panel de navegación de la pantalla de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="a4dbe-108">La consola muestra la lista de paquetes que se han agregado al servidor junto con la información de estado de cada paquete.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="a4dbe-109">Cuando se selecciona un paquete, se muestra información detallada sobre el paquete en el panel **paquetes** .</span><span class="sxs-lookup"><span data-stu-id="a4dbe-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="a4dbe-110">Haga clic en el cuadro de lista desplegable **desagrupado** y especifique cómo se mostrarán los paquetes en la consola.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="a4dbe-111">También puede hacer clic en el encabezado de la columna asociada para ordenar los paquetes.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="a4dbe-112">Para especificar el paquete que desea agregar, haga clic en **Agregar o actualizar paquetes**.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="a4dbe-113">Escriba la ruta de acceso completa del paquete que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="a4dbe-114">Use el formato de ruta UNC o HTTP, por ejemplo **\\\\servername\\sharename\\foldername\\packagename.appv** o **http://server.1234/file.appv** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="a4dbe-115">**Importante**  Debe seleccionar un paquete con la extensión de nombre de archivo **. appv** .</span><span class="sxs-lookup"><span data-stu-id="a4dbe-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="a4dbe-116">La página muestra el mensaje de estado \*\*agregando &lt; packagename &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="a4dbe-117">Haga clic en **importar estado** para comprobar el estado de un paquete que ha importado.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="a4dbe-118">Haga clic en **Aceptar** para agregar el paquete y cerrar la página **Agregar paquete** .</span><span class="sxs-lookup"><span data-stu-id="a4dbe-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="a4dbe-119">Si se produjo un error durante la importación, haga clic en **detalles** en la página de **importación de paquetes** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="a4dbe-120">El paquete recién agregado está ahora disponible en el panel **paquetes** .</span><span class="sxs-lookup"><span data-stu-id="a4dbe-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="a4dbe-121">Haga clic en **cerrar** para cerrar la página **Agregar o actualizar paquetes** .</span><span class="sxs-lookup"><span data-stu-id="a4dbe-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="a4dbe-122">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="a4dbe-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a4dbe-123">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a4dbe-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a4dbe-124">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="a4dbe-124">Got an App-V issue?</span></span>** <span data-ttu-id="a4dbe-125">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a4dbe-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a4dbe-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4dbe-126">Related topics</span></span>


[<span data-ttu-id="a4dbe-127">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a4dbe-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





