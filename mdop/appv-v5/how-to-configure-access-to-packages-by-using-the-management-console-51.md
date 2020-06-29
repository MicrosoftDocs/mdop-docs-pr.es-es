---
title: Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración
description: Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración
author: dansimp
ms.assetid: 4fd39bc2-d814-46de-a108-1c21fa404e8a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c6c8f930fb1fbd82432f6d43dae8b9bed7a563c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814415"
---
# <span data-ttu-id="015b4-103">Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="015b4-103">How to Configure Access to Packages by Using the Management Console</span></span>


<span data-ttu-id="015b4-104">Antes de implementar un paquete virtualizado de App-V 5,1, debe configurar los grupos de seguridad de servicios de dominio de Active Directory (AD DS) a los que se permitirá el acceso y la ejecución de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="015b4-104">Before you deploy an App-V 5.1 virtualized package, you must configure the Active Directory Domain Services (AD DS) security groups that will be allowed to access and run the applications.</span></span> <span data-ttu-id="015b4-105">Los grupos de seguridad pueden contener equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="015b4-105">The security groups may contain computers or users.</span></span> <span data-ttu-id="015b4-106">La titulación de un paquete a un grupo de equipos publica el paquete de forma global en todos los equipos del grupo.</span><span class="sxs-lookup"><span data-stu-id="015b4-106">Entitling a package to a computer group publishes the package globally to all computers in the group.</span></span>

<span data-ttu-id="015b4-107">Use el siguiente procedimiento para configurar el acceso a paquetes virtualizados.</span><span class="sxs-lookup"><span data-stu-id="015b4-107">Use the following procedure to configure access to virtualized packages.</span></span>

**<span data-ttu-id="015b4-108">Para conceder acceso a un paquete de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="015b4-108">To grant access to an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="015b4-109">Busque el paquete que desea configurar:</span><span class="sxs-lookup"><span data-stu-id="015b4-109">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="015b4-110">Abra la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="015b4-110">Open the App-V 5.1 Management console.</span></span>

    2.  <span data-ttu-id="015b4-111">Para mostrar la página **acceso a ad** , haga clic con el botón derecho en el paquete que desea configurar y seleccione **Editar acceso a Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="015b4-111">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="015b4-112">Como alternativa, seleccione el paquete y haga clic en **Editar** en el panel de **acceso ad** .</span><span class="sxs-lookup"><span data-stu-id="015b4-112">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="015b4-113">Aprovisionar un grupo de seguridad para el paquete:</span><span class="sxs-lookup"><span data-stu-id="015b4-113">Provision a security group for the package:</span></span>

    1.  <span data-ttu-id="015b4-114">Vaya a la página **buscar nombres de Active Directory válidos y conceder acceso** .</span><span class="sxs-lookup"><span data-stu-id="015b4-114">Go to the **FIND VALID ACTIVE DIRECTORY NAMES AND GRANT ACCESS** page.</span></span>

    2.  <span data-ttu-id="015b4-115">Con el formato **mydomain**  \\  **Nombredegrupo**, escriba el nombre o parte del nombre de un objeto de grupo de Active Directory y haga clic en **comprobar**.</span><span class="sxs-lookup"><span data-stu-id="015b4-115">Using the format **mydomain** \\ **groupname**, type the name or part of the name of an Active Directory group object, and click **Check**.</span></span>

        <span data-ttu-id="015b4-116">**Nota:**  Asegúrese de proporcionar un nombre de dominio asociado para el grupo que está buscando.</span><span class="sxs-lookup"><span data-stu-id="015b4-116">**Note** Ensure that you provide an associated domain name for the group that you are searching for.</span></span>

         

3.  <span data-ttu-id="015b4-117">Para conceder acceso al paquete, seleccione el grupo que desee y haga clic en **conceder acceso**.</span><span class="sxs-lookup"><span data-stu-id="015b4-117">To grant access to the package, select the desired group and click **Grant Access**.</span></span> <span data-ttu-id="015b4-118">El grupo que acaba de agregar se muestra en el panel **entidades de ad con Access** .</span><span class="sxs-lookup"><span data-stu-id="015b4-118">The newly added group is displayed in the **AD ENTITIES WITH ACCESS** pane.</span></span>

4.  

    <span data-ttu-id="015b4-119">Para aceptar la configuración predeterminada y cerrar la página de **acceso a ad** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="015b4-119">To accept the default configuration settings and close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="015b4-120">Para personalizar la configuración de un grupo específico, haga clic en la lista desplegable **configuraciones asignadas** y seleccione **personalizado**.</span><span class="sxs-lookup"><span data-stu-id="015b4-120">To customize configurations for a specific group, click the **ASSIGNED CONFIGURATIONS** drop-down and select **Custom**.</span></span> <span data-ttu-id="015b4-121">Para configurar las configuraciones personalizadas, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="015b4-121">To configure the custom configurations, click **EDIT**.</span></span> <span data-ttu-id="015b4-122">Después de conceder acceso, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="015b4-122">After you grant access, click **Close**.</span></span>

**<span data-ttu-id="015b4-123">Para quitar el acceso a un paquete de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="015b4-123">To remove access to an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="015b4-124">Busque el paquete que desea configurar:</span><span class="sxs-lookup"><span data-stu-id="015b4-124">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="015b4-125">Abra la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="015b4-125">Open the App-V 5.1 Management console.</span></span>

    2.  <span data-ttu-id="015b4-126">Para mostrar la página **acceso a ad** , haga clic con el botón derecho en el paquete que desea configurar y seleccione **Editar acceso a Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="015b4-126">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="015b4-127">Como alternativa, seleccione el paquete y haga clic en **Editar** en el panel de **acceso ad** .</span><span class="sxs-lookup"><span data-stu-id="015b4-127">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="015b4-128">Seleccione el grupo que desee quitar y haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="015b4-128">Select the group you want to remove, and click **DELETE**.</span></span>

3.  <span data-ttu-id="015b4-129">Para cerrar la página **acceso a ad** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="015b4-129">To close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="015b4-130">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="015b4-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="015b4-131">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="015b4-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="015b4-132">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="015b4-132">Got an App-V issue?</span></span>** <span data-ttu-id="015b4-133">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="015b4-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="015b4-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="015b4-134">Related topics</span></span>


[<span data-ttu-id="015b4-135">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="015b4-135">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





