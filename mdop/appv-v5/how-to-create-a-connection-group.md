---
title: Cómo crear un grupo de conexión
description: Cómo crear un grupo de conexión
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814342"
---
# <span data-ttu-id="307e5-103">Cómo crear un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="307e5-103">How to Create a Connection Group</span></span>


<span data-ttu-id="307e5-104">Siga estos pasos para crear un grupo de conexión mediante la consola de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="307e5-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="307e5-105">Para usar PowerShell para crear grupos de conexión, consulte [Cómo administrar grupos de conexión en un equipo independiente con PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="307e5-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span></span>

<span data-ttu-id="307e5-106">Al colocar paquetes en un grupo de conexión, se fusionan sus rutas de raíz del paquete.</span><span class="sxs-lookup"><span data-stu-id="307e5-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="307e5-107">Si quita paquetes, solo los paquetes restantes mantienen la raíz combinada.</span><span class="sxs-lookup"><span data-stu-id="307e5-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="307e5-108">Para crear un grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="307e5-108">To create a connection group</span></span>**

1.  <span data-ttu-id="307e5-109">En la consola de administración de App-V 5,0, seleccione **packages (paquetes**).</span><span class="sxs-lookup"><span data-stu-id="307e5-109">In the App-V 5.0 Management Console, select **Packages**.</span></span>

2.  <span data-ttu-id="307e5-110">Seleccione **grupos de conexión** para mostrar la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="307e5-110">Select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

3.  <span data-ttu-id="307e5-111">Seleccione **Agregar grupo de conexiones** para crear un nuevo grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="307e5-111">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

4.  <span data-ttu-id="307e5-112">En el panel **nuevo grupo de conexiones** , escriba una descripción para el grupo.</span><span class="sxs-lookup"><span data-stu-id="307e5-112">In the **New Connection Group** pane, type a description for the group.</span></span>

5.  <span data-ttu-id="307e5-113">Haga clic en **Editar** en el panel de **paquetes conectados** para agregar una nueva aplicación al grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="307e5-113">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

6.  <span data-ttu-id="307e5-114">En el panel **paquetes completos** de la biblioteca, seleccione la aplicación que quiere agregar y haga clic en la flecha para agregar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="307e5-114">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="307e5-115">Para quitar una aplicación, seleccione la aplicación que se va a quitar en el panel **paquetes en** y haga clic en la flecha.</span><span class="sxs-lookup"><span data-stu-id="307e5-115">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="307e5-116">Para reestablecer la prioridad de las aplicaciones en el grupo de conexión, use las flechas del panel **paquetes en** .</span><span class="sxs-lookup"><span data-stu-id="307e5-116">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="307e5-117">**Importante**  De forma predeterminada, las configuraciones de acceso a los servicios de dominio de Active Directory que están asociadas a una aplicación específica no se agregan al grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="307e5-117">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="307e5-118">Para transferir la configuración de acceso de Active Directory, seleccione **Agregar acceso de paquete a acceso de grupo**, que se encuentra en el panel **paquetes en** .</span><span class="sxs-lookup"><span data-stu-id="307e5-118">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

7.  <span data-ttu-id="307e5-119">Después de agregar todas las aplicaciones y configurar el acceso a Active Directory, haga clic en **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="307e5-119">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="307e5-120">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="307e5-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="307e5-121">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="307e5-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="307e5-122">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="307e5-122">Got an App-V issue?</span></span>** <span data-ttu-id="307e5-123">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="307e5-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="307e5-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="307e5-124">Related topics</span></span>


[<span data-ttu-id="307e5-125">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="307e5-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="307e5-126">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="307e5-126">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





