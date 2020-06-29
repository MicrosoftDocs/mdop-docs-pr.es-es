---
title: Configurar aplicaciones y extensiones de aplicaciones virtuales predeterminadas en la consola de administración
description: Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814703"
---
#   <span data-ttu-id="66a3a-103">Configurar aplicaciones y extensiones de aplicaciones virtuales predeterminadas en la consola de administración</span><span class="sxs-lookup"><span data-stu-id="66a3a-103">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>

<span data-ttu-id="66a3a-104">Use el procedimiento siguiente para *Ver* y *configurar* las extensiones de paquete predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="66a3a-104">Use the following procedure to *view* and *configure* default package extensions.</span></span>

**<span data-ttu-id="66a3a-105">Para ver y configurar extensiones de aplicaciones virtuales predeterminadas</span><span class="sxs-lookup"><span data-stu-id="66a3a-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="66a3a-106">Para ver el paquete que desea configurar, abra la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="66a3a-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="66a3a-107">Seleccione el paquete que desea configurar, haga clic con el botón secundario en el nombre del paquete y seleccione **Editar configuración predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="66a3a-108">Para ver las aplicaciones contenidas en el paquete especificado, en el panel **configuración predeterminado** , haga clic en **aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="66a3a-109">Para ver los accesos directos de ese paquete, haga clic en **accesos directos**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="66a3a-110">Para ver las asociaciones de los tipos de archivo de ese paquete, haga clic en **tipos de archivo**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="66a3a-111">Para habilitar las extensiones de la aplicación, seleccione **Habilitar**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="66a3a-112">Para habilitar los métodos abreviados, seleccione **Habilitar métodos abreviados**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="66a3a-113">Para agregar un nuevo acceso directo para la aplicación seleccionada, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Agregar nuevo acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="66a3a-114">Para quitar un acceso directo, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Quitar acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="66a3a-115">Para editar un acceso directo existente, haga clic con el botón derecho en la aplicación y seleccione **Editar acceso directo**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="66a3a-116">Para ver cualquier otra extensión de la aplicación, haga clic en **avanzadas** y en **exportar configuración**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="66a3a-117">Escriba un nombre de archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="66a3a-118">Puede ver todas las extensiones de aplicaciones asociadas con el paquete mediante el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="66a3a-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="66a3a-119">Para editar otras extensiones de aplicaciones, modifique el archivo de configuración y haga clic en **importar y sobrescriba esta configuración**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="66a3a-120">Seleccione el archivo modificado y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="66a3a-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="66a3a-121">En el cuadro de diálogo, haga clic en **sobrescribir** para completar el proceso.</span><span class="sxs-lookup"><span data-stu-id="66a3a-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

><span data-ttu-id="66a3a-122">**Nota:** Si se produce un error en la carga y el tamaño del archivo de configuración es superior a 4 MB, tendrá que aumentar el tamaño de archivo máximo permitido por el servidor.</span><span class="sxs-lookup"><span data-stu-id="66a3a-122">**Note** If the upload fails and the size of your configuration file is above 4MB, you will need to increase the maximum file size allowed by the server.</span></span> <span data-ttu-id="66a3a-123">Esto puede hacerse agregando el atributo maxRequestLength con un valor mayor que el tamaño del archivo de configuración (en KB) al elemento httpRuntime de la línea 26 de `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .</span><span class="sxs-lookup"><span data-stu-id="66a3a-123">This can be done by adding the maxRequestLength attribute with a value greater than the size of your configuration file (in KB) to the httpRuntime element on line 26 of `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config`.</span></span>  
<span data-ttu-id="66a3a-124">Por ejemplo, si cambia `<httpRuntime targetFramework="4.5"/>` para `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` aumentar el tamaño máximo a 8 MB</span><span class="sxs-lookup"><span data-stu-id="66a3a-124">For example, changing `<httpRuntime targetFramework="4.5"/>` to `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` will increase the maximum size to 8MB</span></span>


<span data-ttu-id="66a3a-125">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="66a3a-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="66a3a-126">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="66a3a-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="66a3a-127">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="66a3a-127">Got an App-V issue?</span></span>** <span data-ttu-id="66a3a-128">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="66a3a-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="66a3a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66a3a-129">Related topics</span></span>


[<span data-ttu-id="66a3a-130">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="66a3a-130">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





