---
title: Cómo configurar o deshabilitar el tamaño de la base de datos
description: Cómo configurar o deshabilitar el tamaño de la base de datos
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816561"
---
# <span data-ttu-id="63832-103">Cómo configurar o deshabilitar el tamaño de la base de datos</span><span class="sxs-lookup"><span data-stu-id="63832-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="63832-104">Puede usar los procedimientos siguientes en la consola de administración de Application Virtualization Server para especificar el tamaño (en MB) del uso del sistema de virtualización de aplicaciones que desea almacenar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="63832-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="63832-105">Cuando el tamaño de los datos almacenados alcanza el 95% (la marca de agua superior) del límite especificado, el sistema elimina el 10% de los datos de uso, dejando el 85% de los datos.</span><span class="sxs-lookup"><span data-stu-id="63832-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="63832-106">Los datos de uso de aplicaciones y paquetes se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="63832-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="63832-107">Cuando la base de datos crezca lo suficiente y se aproxime el límite máximo, se enviará un mensaje de advertencia al registro de SQL Server para informarle de que se ha alcanzado el límite.</span><span class="sxs-lookup"><span data-stu-id="63832-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="63832-108">Esta advertencia es necesaria porque la acción de limpieza puede afectar al resultado de los informes.</span><span class="sxs-lookup"><span data-stu-id="63832-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="63832-109">También le ayudará a decidir si necesita aumentar el tamaño máximo de la base de datos, reducir el número de meses de datos de uso que se van a mantener o desactivar el nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="63832-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="63832-110">**Nota:**  Se proporcionan las opciones **sin límite de tamaño** y **mantener todas** las opciones de uso para que pueda deshabilitar la creación de informes de uso y la limpieza de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="63832-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="63832-111">Al seleccionar estos elementos, también se limpiará el registro de transacciones de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="63832-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="63832-112">(Todas las transacciones confirmadas de Microsoft SQL Server se eliminarán del registro de la base de datos).</span><span class="sxs-lookup"><span data-stu-id="63832-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="63832-113">Para configurar el tamaño de la base de datos</span><span class="sxs-lookup"><span data-stu-id="63832-113">To set up database size</span></span>**

1.  <span data-ttu-id="63832-114">Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel izquierdo y seleccione **Opciones del sistema**.</span><span class="sxs-lookup"><span data-stu-id="63832-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="63832-115">Seleccione la pestaña **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="63832-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="63832-116">Seleccione el botón de radio **tamaño máximo de la base de datos (MB)** o **sin límite de tamaño** .</span><span class="sxs-lookup"><span data-stu-id="63832-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="63832-117">Si elige especificar un tamaño de base de datos, se recomiendan procedimientos recomendados para escribir un número entre 512 y 4096 MB.</span><span class="sxs-lookup"><span data-stu-id="63832-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="63832-118">El tamaño predeterminado es 1024 MB y si necesita aumentar el tamaño de la base de datos, el valor máximo que puede especificar es 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="63832-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="63832-119">Si selecciona **sin límite de tamaño**, la base de datos crecerá hasta que alcance el límite de tamaño de disco.</span><span class="sxs-lookup"><span data-stu-id="63832-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="63832-120">Haga clic en **aplicar** o **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="63832-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="63832-121">Para deshabilitar los límites de tamaño de base de datos</span><span class="sxs-lookup"><span data-stu-id="63832-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="63832-122">Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel de **ámbito** y seleccione **Opciones del sistema**.</span><span class="sxs-lookup"><span data-stu-id="63832-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="63832-123">Seleccione la pestaña **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="63832-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="63832-124">Seleccione los botones de radio **sin límite de tamaño** y **mantener todos los usos** .</span><span class="sxs-lookup"><span data-stu-id="63832-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="63832-125">Haga clic en **aplicar** o **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="63832-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="63832-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63832-126">Related topics</span></span>


[<span data-ttu-id="63832-127">Cómo personalizar un sistema de virtualización de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="63832-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="63832-128">Cómo configurar o deshabilitar el informe de uso</span><span class="sxs-lookup"><span data-stu-id="63832-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 





