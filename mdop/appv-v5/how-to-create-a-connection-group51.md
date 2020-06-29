---
title: Cómo crear un grupo de conexión
description: Cómo crear un grupo de conexión
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814334"
---
# <span data-ttu-id="46832-103">Cómo crear un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="46832-103">How to Create a Connection Group</span></span>


<span data-ttu-id="46832-104">Siga estos pasos para crear un grupo de conexión mediante la consola de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="46832-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="46832-105">Para usar PowerShell para crear grupos de conexión, consulte [Cómo administrar grupos de conexión en un equipo independiente con PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="46832-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span></span>

<span data-ttu-id="46832-106">Al colocar paquetes en un grupo de conexión, se fusionan sus rutas de raíz del paquete.</span><span class="sxs-lookup"><span data-stu-id="46832-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="46832-107">Si quita paquetes, solo los paquetes restantes mantienen la raíz combinada.</span><span class="sxs-lookup"><span data-stu-id="46832-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="46832-108">Para crear un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="46832-108">To create a connection group</span></span>**

1.  <span data-ttu-id="46832-109">En la consola de administración de App-V 5,1, seleccione **grupos de conexión** para mostrar la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="46832-109">In the App-V 5.1 Management Console, select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

2.  <span data-ttu-id="46832-110">Seleccione **Agregar grupo de conexiones** para crear un nuevo grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="46832-110">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

3.  <span data-ttu-id="46832-111">En el panel **nuevo grupo de conexiones** , escriba una descripción para el grupo.</span><span class="sxs-lookup"><span data-stu-id="46832-111">In the **New Connection Group** pane, type a description for the group.</span></span>

4.  <span data-ttu-id="46832-112">Haga clic en **Editar** en el panel de **paquetes conectados** para agregar una nueva aplicación al grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="46832-112">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

5.  <span data-ttu-id="46832-113">En el panel **paquetes completos** de la biblioteca, seleccione la aplicación que quiere agregar y haga clic en la flecha para agregar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46832-113">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="46832-114">Para quitar una aplicación, seleccione la aplicación que se va a quitar en el panel **paquetes en** y haga clic en la flecha.</span><span class="sxs-lookup"><span data-stu-id="46832-114">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="46832-115">Para reestablecer la prioridad de las aplicaciones en el grupo de conexión, use las flechas del panel **paquetes en** .</span><span class="sxs-lookup"><span data-stu-id="46832-115">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="46832-116">**Importante**  De forma predeterminada, las configuraciones de acceso a los servicios de dominio de Active Directory que están asociadas a una aplicación específica no se agregan al grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="46832-116">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="46832-117">Para transferir la configuración de acceso de Active Directory, seleccione **Agregar acceso de paquete a acceso de grupo**, que se encuentra en el panel **paquetes en** .</span><span class="sxs-lookup"><span data-stu-id="46832-117">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

6.  <span data-ttu-id="46832-118">Después de agregar todas las aplicaciones y configurar el acceso a Active Directory, haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="46832-118">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="46832-119">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="46832-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="46832-120">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="46832-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="46832-121">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="46832-121">Got an App-V issue?</span></span>** <span data-ttu-id="46832-122">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="46832-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="46832-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46832-123">Related topics</span></span>


[<span data-ttu-id="46832-124">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="46832-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="46832-125">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="46832-125">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





