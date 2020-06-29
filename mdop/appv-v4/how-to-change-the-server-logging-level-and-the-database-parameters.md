---
title: Cómo cambiar el nivel de registro de servidor y los parámetros de la base de datos
description: Cómo cambiar el nivel de registro de servidor y los parámetros de la base de datos
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818031"
---
# <span data-ttu-id="ef970-103">Cómo cambiar el nivel de registro de servidor y los parámetros de la base de datos</span><span class="sxs-lookup"><span data-stu-id="ef970-103">How to Change the Server Logging Level and the Database Parameters</span></span>


<span data-ttu-id="ef970-104">Puede usar los procedimientos siguientes para cambiar el nivel de registro y los parámetros del registro de base de datos de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ef970-104">You can use the following procedures to change the logging level and the database log parameters from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="ef970-105">Los siguientes niveles de registro están disponibles:</span><span class="sxs-lookup"><span data-stu-id="ef970-105">The following logging levels are available:</span></span>

-   <span data-ttu-id="ef970-106">Solo transacción</span><span class="sxs-lookup"><span data-stu-id="ef970-106">Transaction Only</span></span>

-   <span data-ttu-id="ef970-107">Errores graves</span><span class="sxs-lookup"><span data-stu-id="ef970-107">Fatal Errors</span></span>

-   <span data-ttu-id="ef970-108">Errores</span><span class="sxs-lookup"><span data-stu-id="ef970-108">Errors</span></span>

-   <span data-ttu-id="ef970-109">Advertencias/errores</span><span class="sxs-lookup"><span data-stu-id="ef970-109">Warnings/Errors</span></span>

-   <span data-ttu-id="ef970-110">Información, advertencias o errores</span><span class="sxs-lookup"><span data-stu-id="ef970-110">Info/Warnings/Errors</span></span>

-   <span data-ttu-id="ef970-111">Detallado</span><span class="sxs-lookup"><span data-stu-id="ef970-111">Verbose</span></span>

<span data-ttu-id="ef970-112">**Nota:**  Debido al tamaño del archivo de registro producido al usar el modo **detallado** , se recomienda no ejecutar servidores de producción con este nivel de conjunto de registro.</span><span class="sxs-lookup"><span data-stu-id="ef970-112">**Note** Because of the size of the log file produced when you use **Verbose** mode, the recommendation is that you do not run production servers with this level of logging set.</span></span>

 

<span data-ttu-id="ef970-113">Los parámetros de registro de base de datos determinan el tipo de controlador de base de datos, las credenciales de acceso y la ubicación de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ef970-113">The database logging parameters determine the database driver type, access credentials, and location of the logging database.</span></span>

**<span data-ttu-id="ef970-114">Para cambiar el nivel de registro de los servidores de administración</span><span class="sxs-lookup"><span data-stu-id="ef970-114">To change the logging level for Management Servers</span></span>**

1.  <span data-ttu-id="ef970-115">Haga clic en el nodo **grupos de servidores** para mostrar los grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="ef970-115">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="ef970-116">Haga clic con el botón secundario en el grupo de servidores y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="ef970-116">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="ef970-117">En el cuadro de diálogo **propiedades** , seleccione la ficha **registro** .</span><span class="sxs-lookup"><span data-stu-id="ef970-117">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="ef970-118">En el cuadro de diálogo **propiedades del grupo de servidores** , seleccione el servidor y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ef970-118">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="ef970-119">En el cuadro de diálogo **Agregar/editar módulo de registro** , seleccione el nivel de registro en la lista desplegable **tipo de evento** .</span><span class="sxs-lookup"><span data-stu-id="ef970-119">In the **Add/Edit Log Module** dialog box, select the logging level from the **Event Type** drop-down list.</span></span>

6.  <span data-ttu-id="ef970-120">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ef970-120">Click **OK**.</span></span>

7.  <span data-ttu-id="ef970-121">En el cuadro de diálogo **propiedades del grupo de servidores** , haga clic en **Aceptar** o **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="ef970-121">In the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

**<span data-ttu-id="ef970-122">Para cambiar el nivel de registro de los servidores de streaming</span><span class="sxs-lookup"><span data-stu-id="ef970-122">To change the logging level for Streaming Servers</span></span>**

1.  <span data-ttu-id="ef970-123">Edite el siguiente valor de la clave del registro para cambiar el nivel de registro:</span><span class="sxs-lookup"><span data-stu-id="ef970-123">Edit the following registry key value to change the logging level:</span></span>

    -   <span data-ttu-id="ef970-124">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span><span class="sxs-lookup"><span data-stu-id="ef970-124">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span></span>

2.  <span data-ttu-id="ef970-125">Seleccione uno de los siguientes valores para establecer el nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="ef970-125">Select one of the following values to set the logging level.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="ef970-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ef970-126">Value</span></span></th>
    <th align="left"><span data-ttu-id="ef970-127">Nivel de registro</span><span class="sxs-lookup"><span data-stu-id="ef970-127">Logging Level</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ef970-128">,0</span><span class="sxs-lookup"><span data-stu-id="ef970-128">0</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef970-129">Solo transacciones</span><span class="sxs-lookup"><span data-stu-id="ef970-129">Transactions Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ef970-130">uno</span><span class="sxs-lookup"><span data-stu-id="ef970-130">1</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef970-131">Errores graves</span><span class="sxs-lookup"><span data-stu-id="ef970-131">Fatal Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ef970-132">1</span><span class="sxs-lookup"><span data-stu-id="ef970-132">2</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef970-133">Errores</span><span class="sxs-lookup"><span data-stu-id="ef970-133">Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ef970-134">2</span><span class="sxs-lookup"><span data-stu-id="ef970-134">3</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef970-135">Advertencias/errores</span><span class="sxs-lookup"><span data-stu-id="ef970-135">Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ef970-136">cuatro</span><span class="sxs-lookup"><span data-stu-id="ef970-136">4</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef970-137">Información, advertencias o errores</span><span class="sxs-lookup"><span data-stu-id="ef970-137">Information/ Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ef970-138">4</span><span class="sxs-lookup"><span data-stu-id="ef970-138">5</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef970-139">Detallado</span><span class="sxs-lookup"><span data-stu-id="ef970-139">Verbose</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="ef970-140">Para cambiar los parámetros del registro de base de datos</span><span class="sxs-lookup"><span data-stu-id="ef970-140">To change database log parameters</span></span>**

1.  <span data-ttu-id="ef970-141">Haga clic en el nodo **grupos de servidores** para mostrar los grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="ef970-141">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="ef970-142">Haga clic con el botón secundario en el grupo de servidores y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="ef970-142">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="ef970-143">En el cuadro de diálogo **propiedades** , seleccione la ficha **registro** .</span><span class="sxs-lookup"><span data-stu-id="ef970-143">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="ef970-144">En el cuadro de diálogo **propiedades del grupo de servidores** , seleccione el servidor y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ef970-144">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="ef970-145">En el cuadro de diálogo **Agregar/editar módulo de registro** , seleccione un controlador de base de datos en la lista desplegable **controlador de base de datos** .</span><span class="sxs-lookup"><span data-stu-id="ef970-145">In the **Add/Edit Log Module** dialog box, select a database driver from the **Database Driver** drop-down list.</span></span>

6.  <span data-ttu-id="ef970-146">Escriba un **nombre de host DNS**.</span><span class="sxs-lookup"><span data-stu-id="ef970-146">Enter a **DNS Host Name**.</span></span>

7.  <span data-ttu-id="ef970-147">Haga clic en la casilla **determinar el puerto de forma dinámica** o escriba un número de puerto en el campo **Puerto** .</span><span class="sxs-lookup"><span data-stu-id="ef970-147">Click the **Dynamically Determine Port** check box, or enter a port number in the **Port** field.</span></span>

8.  <span data-ttu-id="ef970-148">Escriba un **nombre de servicio** en el campo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ef970-148">Enter a **Service Name** in the corresponding field.</span></span>

9.  <span data-ttu-id="ef970-149">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ef970-149">Click **OK**.</span></span>

10. <span data-ttu-id="ef970-150">En el cuadro de diálogo **propiedades del grupo de servidores** , haga clic en **Aceptar** o **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="ef970-150">On the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

## <span data-ttu-id="ef970-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef970-151">Related topics</span></span>


[<span data-ttu-id="ef970-152">Cómo personalizar un sistema de virtualización de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="ef970-152">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





