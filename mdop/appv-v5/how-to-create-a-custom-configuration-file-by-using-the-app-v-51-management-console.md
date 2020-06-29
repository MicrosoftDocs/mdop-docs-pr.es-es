---
title: Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1
description: Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814326"
---
# <span data-ttu-id="82457-103">Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82457-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="82457-104">Puede usar una configuración dinámica para personalizar un paquete de App-V 5,1 para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="82457-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="82457-105">Sin embargo, primero debe crear el archivo de configuración de usuario dinámica (. xml) o el archivo de configuración de implementación dinámica antes de poder usar los archivos.</span><span class="sxs-lookup"><span data-stu-id="82457-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="82457-106">La creación del archivo es una operación manual avanzada.</span><span class="sxs-lookup"><span data-stu-id="82457-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="82457-107">Para obtener información general sobre los archivos de configuración de usuario dinámicos, consulte [configuración dinámica de App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="82457-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="82457-108">Use el siguiente procedimiento para crear un archivo de configuración de usuario dinámico con la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82457-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="82457-109">Para crear un archivo de configuración de usuario dinámico</span><span class="sxs-lookup"><span data-stu-id="82457-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="82457-110">Haga clic con el botón secundario en el nombre del paquete que desea ver y seleccione **Editar acceso de Active Directory** para ver la configuración asignada a un grupo de usuarios determinado.</span><span class="sxs-lookup"><span data-stu-id="82457-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="82457-111">Como alternativa, seleccione el paquete y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="82457-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="82457-112">Con la lista de **entidades de ad con Access**, seleccione el grupo de ad que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="82457-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="82457-113">Seleccione **personalizado** en la lista desplegable, si aún no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="82457-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="82457-114">Aparecerá un vínculo con el nombre **Editar** .</span><span class="sxs-lookup"><span data-stu-id="82457-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="82457-115">Haz clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="82457-115">Click **Edit**.</span></span> <span data-ttu-id="82457-116">Se mostrará la configuración de usuario dinámica que está asignada al grupo de AD.</span><span class="sxs-lookup"><span data-stu-id="82457-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="82457-117">Haga clic en **avanzadas**y, a continuación, en **exportar configuración**.</span><span class="sxs-lookup"><span data-stu-id="82457-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="82457-118">Escriba un nombre de archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="82457-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="82457-119">Ahora puede editar el archivo para configurar un paquete para un usuario.</span><span class="sxs-lookup"><span data-stu-id="82457-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="82457-120">Nota</span><span class="sxs-lookup"><span data-stu-id="82457-120">Note</span></span>**  
    <span data-ttu-id="82457-121">Para exportar una configuración mientras se ejecuta en Windows Server, debe deshabilitar la "configuración de seguridad mejorada de Internet".</span><span class="sxs-lookup"><span data-stu-id="82457-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="82457-122">Si esta opción está habilitada y está configurada para bloquear las descargas, no podrás descargar nada desde el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="82457-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="82457-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82457-123">Related topics</span></span>


[<span data-ttu-id="82457-124">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82457-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









