---
title: Cómo administrar informes en la consola de administración de servidor
description: Cómo administrar informes en la consola de administración de servidor
author: dansimp
ms.assetid: 28d99620-6339-43f6-9288-4aa958607c59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3d70734be04df380e6ce3f4ee8de126503e482e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817141"
---
# <span data-ttu-id="ee5cc-103">Cómo administrar informes en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="ee5cc-103">How to Manage Reports in the Server Management Console</span></span>


<span data-ttu-id="ee5cc-104">Para administrar de forma eficaz el sistema de virtualización de aplicaciones, puede usar la consola de administración del servidor de virtualización de aplicaciones para generar una variedad de informes que proporcionen información sobre el sistema.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-104">To effectively manage the Application Virtualization System, you can use the Application Virtualization Server Management Console to generate a variety of reports that provide information about the system.</span></span> <span data-ttu-id="ee5cc-105">Esta información incluye información de uso diario para una aplicación específica o todas las aplicaciones, y seguimiento de errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-105">This information includes daily usage information for a specific application or all applications, and system error tracking.</span></span>

**<span data-ttu-id="ee5cc-106">Nota</span><span class="sxs-lookup"><span data-stu-id="ee5cc-106">Note</span></span>**  
-   <span data-ttu-id="ee5cc-107">Durante la instalación, el script de instalación instala solo la versión en inglés del visor de informes.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-107">During installation, the installation script installs only the English language version of report viewer.</span></span> <span data-ttu-id="ee5cc-108">Para que el visor de informes muestre la información correcta en otros idiomas, es necesario instalar un paquete de idioma desde la siguiente ubicación: <https://go.microsoft.com/fwlink/?LinkId=131645> .</span><span class="sxs-lookup"><span data-stu-id="ee5cc-108">For the report viewer to display the correct information in other languages, it is necessary to install a language pack from the following location: <https://go.microsoft.com/fwlink/?LinkId=131645>.</span></span>

-   <span data-ttu-id="ee5cc-109">Al agregar o editar una aplicación en la consola de administración de servidores, debe asegurarse de que los nombres y las versiones de la aplicación coincidan exactamente con los de los archivos OSD.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-109">When you add or edit an application in the Server Management Console, you must make sure that the application names and versions exactly match those in the OSD files.</span></span> <span data-ttu-id="ee5cc-110">La característica de informes usa los campos de datos nombres de aplicación y versiones cuando identifica los datos de uso de la aplicación en los que se va a notificar.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-110">The reporting feature uses the application names and versions data fields when it identifies application usage data on which to report.</span></span> <span data-ttu-id="ee5cc-111">Si los campos de datos no coinciden, se omitirán los registros de uso.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-111">If the data fields do not match, the usage records will be skipped.</span></span>

 

## <span data-ttu-id="ee5cc-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ee5cc-112">In This Section</span></span>


<a href="" id="application-virtualization-report-types"></a>[<span data-ttu-id="ee5cc-113">Tipos de informe de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee5cc-113">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)  
<span data-ttu-id="ee5cc-114">Contiene información sobre los tipos de informes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-114">Contains information about the available report types.</span></span>

<a href="" id="how-to-create-a-report"></a>[<span data-ttu-id="ee5cc-115">Cómo crear un informe</span><span class="sxs-lookup"><span data-stu-id="ee5cc-115">How to Create a Report</span></span>](how-to-create-a-reportserver.md)  
<span data-ttu-id="ee5cc-116">Proporciona un proceso paso a paso para crear un informe.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-116">Provides a step-by-step process for creating a report.</span></span>

<a href="" id="how-to-run-a-report"></a>[<span data-ttu-id="ee5cc-117">Cómo ejecutar un informe</span><span class="sxs-lookup"><span data-stu-id="ee5cc-117">How to Run a Report</span></span>](how-to-run-a-reportserver.md)  
<span data-ttu-id="ee5cc-118">Proporciona un proceso paso a paso para ejecutar un informe.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-118">Provides a step-by-step process for running a report.</span></span>

<a href="" id="how-to-print-a-report"></a>[<span data-ttu-id="ee5cc-119">Cómo imprimir un informe</span><span class="sxs-lookup"><span data-stu-id="ee5cc-119">How to Print a Report</span></span>](how-to-print-a-reportserver.md)  
<span data-ttu-id="ee5cc-120">Proporciona un proceso paso a paso para imprimir un informe.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-120">Provides a step-by-step process for printing a report.</span></span>

<a href="" id="how-to-export-a-report"></a>[<span data-ttu-id="ee5cc-121">Cómo exportar un informe</span><span class="sxs-lookup"><span data-stu-id="ee5cc-121">How to Export a Report</span></span>](how-to-export-a-reportserver.md)  
<span data-ttu-id="ee5cc-122">Proporciona un proceso paso a paso para exportar un informe.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-122">Provides a step-by-step process for exporting a report.</span></span>

<a href="" id="how-to-delete-a-report"></a>[<span data-ttu-id="ee5cc-123">Cómo eliminar un informe</span><span class="sxs-lookup"><span data-stu-id="ee5cc-123">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)  
<span data-ttu-id="ee5cc-124">Proporciona un proceso paso a paso para eliminar un informe.</span><span class="sxs-lookup"><span data-stu-id="ee5cc-124">Provides a step-by-step process for deleting a report.</span></span>

## <span data-ttu-id="ee5cc-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee5cc-125">Related topics</span></span>


[<span data-ttu-id="ee5cc-126">Informe de uso de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee5cc-126">Application Utilization Report</span></span>](application-utilization-reportserver.md)

[<span data-ttu-id="ee5cc-127">Cómo realizar tareas administrativas en la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee5cc-127">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="ee5cc-128">Informe de auditoría de software</span><span class="sxs-lookup"><span data-stu-id="ee5cc-128">Software Audit Report</span></span>](software-audit-reportserver.md)

[<span data-ttu-id="ee5cc-129">Informe de errores del sistema</span><span class="sxs-lookup"><span data-stu-id="ee5cc-129">System Error Report</span></span>](system-error-reportserver.md)

[<span data-ttu-id="ee5cc-130">Informe de utilización del sistema</span><span class="sxs-lookup"><span data-stu-id="ee5cc-130">System Utilization Report</span></span>](system-utilization-reportserver.md)

 

 





