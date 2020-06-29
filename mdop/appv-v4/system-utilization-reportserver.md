---
title: Informe de utilización del sistema
description: Informe de utilización del sistema
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815251"
---
# <span data-ttu-id="83efb-103">Informe de utilización del sistema</span><span class="sxs-lookup"><span data-stu-id="83efb-103">System Utilization Report</span></span>


<span data-ttu-id="83efb-104">Use el informe de uso del sistema para representar el uso total diario del sistema.</span><span class="sxs-lookup"><span data-stu-id="83efb-104">Use the System Utilization Report to graph the total daily system usage.</span></span> <span data-ttu-id="83efb-105">Puede usar este informe para determinar la carga del sistema de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="83efb-105">You can use this report to determine the load on your Application Virtualization System.</span></span>

<span data-ttu-id="83efb-106">Este informe realiza un seguimiento del uso de tiempo durante el período de informes para el servidor especificado o para el grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="83efb-106">This report tracks the usage over time during the reporting period for the specified server or for the server group.</span></span>

<span data-ttu-id="83efb-107">El informe de uso del sistema también grafica el siguiente uso del sistema:</span><span class="sxs-lookup"><span data-stu-id="83efb-107">The System Utilization Report also graphs the following system usage:</span></span>

-   <span data-ttu-id="83efb-108">Uso por día de la semana</span><span class="sxs-lookup"><span data-stu-id="83efb-108">Usage by day of the week</span></span>

-   <span data-ttu-id="83efb-109">Uso por hora del día</span><span class="sxs-lookup"><span data-stu-id="83efb-109">Usage by hour of the day</span></span>

<span data-ttu-id="83efb-110">El informe de uso del sistema también incluye un resumen del uso total del sistema para usuarios específicos y el número total de sesiones.</span><span class="sxs-lookup"><span data-stu-id="83efb-110">The System Utilization Report also includes a summary of the total system usage for specific users and total session counts.</span></span>

<span data-ttu-id="83efb-111">Cuando se crea un informe, se especifican los parámetros que se usan para recopilar los datos cuando se ejecuta el informe.</span><span class="sxs-lookup"><span data-stu-id="83efb-111">When you create a report, you specify the parameters that are used for collecting the data when the report is run.</span></span>

<span data-ttu-id="83efb-112">Los informes no se ejecutan automáticamente; debe ejecutarlos de forma explícita para generar datos de salida.</span><span class="sxs-lookup"><span data-stu-id="83efb-112">Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="83efb-113">La cantidad de tiempo que se tarda en ejecutar este informe viene determinada por la cantidad de datos recopilados en el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="83efb-113">The length of time it takes to run this report is determined by the amount of data collected in the data store.</span></span>

<span data-ttu-id="83efb-114">Después de ejecutar un informe y el resultado se muestra en la consola de administración de Application Virtualization Server, puede exportar el informe en los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="83efb-114">After you run a report and the output is displayed in the Application Virtualization Server Management Console, you can export the report into the following formats:</span></span>

-   <span data-ttu-id="83efb-115">Adobe Acrobat (PDF)</span><span class="sxs-lookup"><span data-stu-id="83efb-115">Adobe Acrobat (PDF)</span></span>

-   <span data-ttu-id="83efb-116">Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="83efb-116">Microsoft Office Excel</span></span>

<span data-ttu-id="83efb-117">**Nota:**  El nombre del servidor de App-V notificado por los clientes debe ser parte del grupo de servidores predeterminado para que el informe de uso del sistema muestre los datos.</span><span class="sxs-lookup"><span data-stu-id="83efb-117">**Note** The App-V server name reported from the clients must be part of the Default Server Group in order for the System Utilization report to show data.</span></span> <span data-ttu-id="83efb-118">Por ejemplo, si usa varios servidores con un equilibrador de carga de red (NLB), debe agregar el nombre de clúster NLB al grupo de servidores predeterminado.</span><span class="sxs-lookup"><span data-stu-id="83efb-118">For example, if you are using multiple servers with a Network Load Balancer (NLB), you must add the NLB cluster name to the Default Server Group.</span></span>

 

## <span data-ttu-id="83efb-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83efb-119">Related topics</span></span>


[<span data-ttu-id="83efb-120">Cómo crear un informe</span><span class="sxs-lookup"><span data-stu-id="83efb-120">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="83efb-121">Cómo eliminar un informe</span><span class="sxs-lookup"><span data-stu-id="83efb-121">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="83efb-122">Cómo exportar un informe</span><span class="sxs-lookup"><span data-stu-id="83efb-122">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="83efb-123">Cómo imprimir un informe</span><span class="sxs-lookup"><span data-stu-id="83efb-123">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

[<span data-ttu-id="83efb-124">Cómo ejecutar un informe</span><span class="sxs-lookup"><span data-stu-id="83efb-124">How to Run a Report</span></span>](how-to-run-a-reportserver.md)

 

 





