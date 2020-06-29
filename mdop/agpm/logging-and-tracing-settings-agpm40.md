---
title: Registro y seguimiento de configuración
description: Registro y seguimiento de configuración
author: dansimp
ms.assetid: 66d03306-80d8-4132-bf71-2827157b1fc9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c58da00e7030c5e4cb3e4d5c4e5bbffa0c754233
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820600"
---
# <span data-ttu-id="b8430-103">Registro y seguimiento de configuración</span><span class="sxs-lookup"><span data-stu-id="b8430-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="b8430-104">La configuración de la plantilla administrativa de administración de directivas de grupo (AGPM) avanzada le permite configurar de forma centralizada las opciones de registro y seguimiento para clientes y servidores AGPM a los que se aplica un objeto de directiva de grupo (GPO) con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="b8430-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="b8430-105">La siguiente opción está disponible en equipo Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM al editar un GPO.</span><span class="sxs-lookup"><span data-stu-id="b8430-105">The following setting is available under Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<span data-ttu-id="b8430-106">**Ubicaciones del archivo de seguimiento**:</span><span class="sxs-lookup"><span data-stu-id="b8430-106">**Trace file locations**:</span></span>

-   <span data-ttu-id="b8430-107">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="b8430-107">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="b8430-108">Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="b8430-108">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8430-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="b8430-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="b8430-110">Efecto</span><span class="sxs-lookup"><span data-stu-id="b8430-110">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b8430-111">AGPM: configurar el registro</span><span class="sxs-lookup"><span data-stu-id="b8430-111">AGPM: Configure logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b8430-112">Esta configuración de directiva le permite activar y configurar el registro para AGPM.</span><span class="sxs-lookup"><span data-stu-id="b8430-112">This policy setting allows you to turn on and configure logging for AGPM.</span></span> <span data-ttu-id="b8430-113">Esta configuración afecta tanto a los componentes del cliente como del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="b8430-113">This setting affects both client and server components of AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b8430-114">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="b8430-114">Additional references</span></span>

-   [<span data-ttu-id="b8430-115">Carpeta de plantillas administrativas</span><span class="sxs-lookup"><span data-stu-id="b8430-115">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

 

 





