---
title: Configuración de conexión del servidor AGPM
description: Configuración de conexión del servidor AGPM
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812831"
---
# <span data-ttu-id="6a3f2-103">Configuración de conexión del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="6a3f2-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="6a3f2-104">Puede usar la configuración de la plantilla administrativa para administración de directivas de grupo (AGPM) avanzada para configurar conexiones de servidor AGPM de forma centralizada para los administradores de directiva de grupo a quienes se aplica un objeto de directiva de grupo (GPO) con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="6a3f2-105">La siguiente configuración está disponible en Configuration\\Policies\\Administrative de usuario de Templates\\Windows Components\\AGPM al editar un GPO.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a3f2-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="6a3f2-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="6a3f2-107">Efecto</span><span class="sxs-lookup"><span data-stu-id="6a3f2-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a3f2-108">AGPM: especificar el servidor de AGPM predeterminado (todos los dominios)</span><span class="sxs-lookup"><span data-stu-id="6a3f2-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a3f2-109">Esta configuración de directiva le permite especificar un servidor de AGPM predeterminado para todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="6a3f2-110">Solo lo usan los clientes de AGPM, y restringe los administradores de la Directiva de grupo para que no se conecten a otro archivo.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="6a3f2-111">Puede invalidar este valor predeterminado para dominios individuales mediante la <strong> configuración AGPM: especificar servidores de AGPM </strong> .</span><span class="sxs-lookup"><span data-stu-id="6a3f2-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a3f2-112">AGPM: especificar servidores de AGPM</span><span class="sxs-lookup"><span data-stu-id="6a3f2-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a3f2-113">Esta configuración de directiva le permite especificar los servidores AGPM para dominios individuales.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="6a3f2-114">Solo lo usan los clientes de AGPM, y restringe los administradores de la Directiva de grupo para que no se conecten a un archivo diferente para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="6a3f2-115">Para especificar un servidor de AGPM predeterminado, use la <strong> opción AGPM: especificar el servidor de AGPM predeterminado (todos los dominios) </strong> y use esta configuración de directiva para reemplazar el valor predeterminado en cada dominio.</span><span class="sxs-lookup"><span data-stu-id="6a3f2-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6a3f2-116">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="6a3f2-116">Additional references</span></span>

-   [<span data-ttu-id="6a3f2-117">Carpeta de plantillas administrativas</span><span class="sxs-lookup"><span data-stu-id="6a3f2-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

-   [<span data-ttu-id="6a3f2-118">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="6a3f2-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





