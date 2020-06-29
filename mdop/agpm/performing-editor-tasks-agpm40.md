---
title: Realización de tareas de editor
description: Realización de tareas de editor
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820410"
---
# <span data-ttu-id="2c292-103">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="2c292-103">Performing Editor Tasks</span></span>


<span data-ttu-id="2c292-104">En administración avanzada de directivas de grupo (AGPM), un editor es una persona autorizada por un administrador de AGPM (control total) para cambiar objetos de directiva de grupo (GPO) y crear plantillas de GPO.</span><span class="sxs-lookup"><span data-stu-id="2c292-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="2c292-105">Además, un editor puede solicitar que se cree, elimine o restaure un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2c292-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="2c292-106">Un aprobador debe aprobar la solicitud para que se implemente.</span><span class="sxs-lookup"><span data-stu-id="2c292-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="2c292-107">Un editor puede exportar un GPO a un archivo para que se pueda copiar a un dominio de otro bosque e importar un GPO que se haya copiado de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="2c292-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="2c292-108">**Importante**  Asegúrese de estar conectando con el archivo central de los GPO.</span><span class="sxs-lookup"><span data-stu-id="2c292-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="2c292-109">Para obtener más información, vea [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="2c292-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="2c292-110">Creación o control de un GPO</span><span class="sxs-lookup"><span data-stu-id="2c292-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="2c292-111">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="2c292-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="2c292-112">Uso de un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="2c292-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="2c292-113">Solicitar la implementación de un GPO</span><span class="sxs-lookup"><span data-stu-id="2c292-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="2c292-114">Crear una plantilla y establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="2c292-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="2c292-115">Eliminación o restauración de un GPO</span><span class="sxs-lookup"><span data-stu-id="2c292-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="2c292-116">**Nota:**  Puesto que la función editor incluye los permisos para el rol de revisor, un editor también puede revisar la configuración y comparar los GPO.</span><span class="sxs-lookup"><span data-stu-id="2c292-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="2c292-117">Para obtener más información, consulte [realización de tareas de revisor](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="2c292-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="2c292-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="2c292-118">Additional considerations</span></span>

<span data-ttu-id="2c292-119">De forma predeterminada, se proporcionan los siguientes permisos para la función editor:</span><span class="sxs-lookup"><span data-stu-id="2c292-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="2c292-120">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="2c292-120">List Contents</span></span>

-   <span data-ttu-id="2c292-121">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="2c292-121">Read Settings</span></span>

-   <span data-ttu-id="2c292-122">Editar configuración</span><span class="sxs-lookup"><span data-stu-id="2c292-122">Edit Settings</span></span>

-   <span data-ttu-id="2c292-123">Exportar GPO</span><span class="sxs-lookup"><span data-stu-id="2c292-123">Export GPO</span></span>

-   <span data-ttu-id="2c292-124">Importar GPO</span><span class="sxs-lookup"><span data-stu-id="2c292-124">Import GPO</span></span>

-   <span data-ttu-id="2c292-125">Crear plantilla</span><span class="sxs-lookup"><span data-stu-id="2c292-125">Create Template</span></span>

 

 





