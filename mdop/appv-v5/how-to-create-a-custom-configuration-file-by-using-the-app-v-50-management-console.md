---
title: Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.0
description: Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814327"
---
# <span data-ttu-id="ed074-103">Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ed074-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="ed074-104">Puede usar una configuración dinámica para personalizar un paquete de App-V 5,0 para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="ed074-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="ed074-105">Sin embargo, primero debe crear el archivo de configuración de usuario dinámica (. xml) o el archivo de configuración de implementación dinámica antes de poder usar los archivos.</span><span class="sxs-lookup"><span data-stu-id="ed074-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="ed074-106">La creación del archivo es una operación manual avanzada.</span><span class="sxs-lookup"><span data-stu-id="ed074-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="ed074-107">Para obtener información general sobre los archivos de configuración de usuario dinámicos, consulte [configuración dinámica de App-V 5,0](about-app-v-50-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="ed074-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="ed074-108">Use el siguiente procedimiento para crear un archivo de configuración de usuario dinámico con la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ed074-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="ed074-109">Para crear un archivo de configuración de usuario dinámico</span><span class="sxs-lookup"><span data-stu-id="ed074-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="ed074-110">Haga clic con el botón secundario en el nombre del paquete que desea ver y seleccione **Editar acceso de Active Directory** para ver la configuración asignada a un grupo de usuarios determinado.</span><span class="sxs-lookup"><span data-stu-id="ed074-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="ed074-111">Como alternativa, seleccione el paquete y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ed074-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="ed074-112">Con la lista de **entidades de ad con Access**, seleccione el grupo de ad que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="ed074-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="ed074-113">Seleccione **personalizado** en la lista desplegable, si aún no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ed074-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="ed074-114">Aparecerá un vínculo con el nombre **Editar** .</span><span class="sxs-lookup"><span data-stu-id="ed074-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="ed074-115">Haz clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ed074-115">Click **Edit**.</span></span> <span data-ttu-id="ed074-116">Se mostrará la configuración de usuario dinámica que está asignada al grupo de AD.</span><span class="sxs-lookup"><span data-stu-id="ed074-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="ed074-117">Haga clic en **avanzadas**y, a continuación, en **exportar configuración**.</span><span class="sxs-lookup"><span data-stu-id="ed074-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="ed074-118">Escriba un nombre de archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ed074-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="ed074-119">Ahora puede editar el archivo para configurar un paquete para un usuario.</span><span class="sxs-lookup"><span data-stu-id="ed074-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="ed074-120">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="ed074-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ed074-121">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="ed074-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ed074-122">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="ed074-122">Got an App-V issue?</span></span>** <span data-ttu-id="ed074-123">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ed074-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ed074-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed074-124">Related topics</span></span>


[<span data-ttu-id="ed074-125">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ed074-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





