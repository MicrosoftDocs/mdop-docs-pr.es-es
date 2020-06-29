---
title: Cómo configurar o deshabilitar el informe de uso
description: Cómo configurar o deshabilitar el informe de uso
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816550"
---
# <span data-ttu-id="daacb-103">Cómo configurar o deshabilitar el informe de uso</span><span class="sxs-lookup"><span data-stu-id="daacb-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="daacb-104">Puede usar los procedimientos siguientes en la consola de administración de Application Virtualization Server para especificar la duración (en meses) de la información de uso del sistema de virtualización de aplicaciones que desea almacenar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="daacb-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="daacb-105">**Nota:**  Para almacenar información de uso, debe seleccionar la casilla **registrar información de uso** en la pestaña **canalización del proveedor** . Para mostrar esta pestaña, haga clic con el botón secundario en la Directiva de proveedor en el panel de **resultados de directivas del proveedor** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="daacb-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="daacb-106">Para configurar los informes de uso</span><span class="sxs-lookup"><span data-stu-id="daacb-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="daacb-107">Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel izquierdo y seleccione **Opciones del sistema**.</span><span class="sxs-lookup"><span data-stu-id="daacb-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="daacb-108">Seleccione la pestaña **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="daacb-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="daacb-109">Seleccione el botón **de radio mantener uso para (meses)** o **mantener todo el uso** .</span><span class="sxs-lookup"><span data-stu-id="daacb-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="daacb-110">Si decide especificar la duración del uso en meses, escriba un número entre 1 y 120 (el valor predeterminado es de 6 meses).</span><span class="sxs-lookup"><span data-stu-id="daacb-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="daacb-111">Si selecciona **mantener todo el uso**, la base de datos crecerá hasta que alcance el límite de tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="daacb-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="daacb-112">Haga clic en **aplicar** o **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="daacb-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="daacb-113">Para deshabilitar los informes de uso</span><span class="sxs-lookup"><span data-stu-id="daacb-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="daacb-114">Haga clic en el nodo **directivas de proveedor** .</span><span class="sxs-lookup"><span data-stu-id="daacb-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="daacb-115">Haga clic con el botón secundario en **Directiva de proveedor** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="daacb-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="daacb-116">Seleccione la ficha **canalización del proveedor** .</span><span class="sxs-lookup"><span data-stu-id="daacb-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="daacb-117">Desactive la casilla **registrar información de uso** .</span><span class="sxs-lookup"><span data-stu-id="daacb-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="daacb-118">Haga clic en **aplicar** o **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="daacb-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="daacb-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="daacb-119">Related topics</span></span>


[<span data-ttu-id="daacb-120">Cómo personalizar un sistema de virtualización de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="daacb-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="daacb-121">Cómo configurar o deshabilitar el tamaño de la base de datos</span><span class="sxs-lookup"><span data-stu-id="daacb-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 





