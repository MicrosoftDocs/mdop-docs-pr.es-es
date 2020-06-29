---
title: Registro y seguimiento de configuración
description: Registro y seguimiento de configuración
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820590"
---
# <span data-ttu-id="3b290-103">Registro y seguimiento de configuración</span><span class="sxs-lookup"><span data-stu-id="3b290-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="3b290-104">La configuración de la plantilla administrativa de administración de directivas de grupo (AGPM) avanzada le permite configurar de forma centralizada las opciones de registro y seguimiento para clientes y servidores AGPM a los que se aplica un objeto de directiva de grupo (GPO) con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="3b290-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="3b290-105">La siguiente opción está disponible en equipo Configuration\\Administrative Templates\\Windows Components\\AGPM en el **Editor de objetos de directiva de grupo** al editar un GPO en la consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="3b290-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="3b290-106">Si esta ruta de acceso no está visible, haga clic con el botón secundario en **plantillas administrativas**y agregue la plantilla AGPM. ADMX o AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="3b290-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="3b290-107">**Ubicaciones del archivo de seguimiento**:</span><span class="sxs-lookup"><span data-stu-id="3b290-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="3b290-108">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="3b290-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="3b290-109">Servidor:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="3b290-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3b290-110">Configuración</span><span class="sxs-lookup"><span data-stu-id="3b290-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="3b290-111">Efecto</span><span class="sxs-lookup"><span data-stu-id="3b290-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3b290-112">Registro de AGPM</span><span class="sxs-lookup"><span data-stu-id="3b290-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3b290-113">Si se habilita, este valor de configuración configura si el seguimiento está activado y el nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="3b290-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="3b290-114">Esta configuración afecta tanto a los componentes del cliente como del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="3b290-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="3b290-115">Si se deshabilita o no se configura, esta configuración no surte efecto.</span><span class="sxs-lookup"><span data-stu-id="3b290-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3b290-116">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="3b290-116">Additional references</span></span>

-   [<span data-ttu-id="3b290-117">Configuración de plantilla administrativa</span><span class="sxs-lookup"><span data-stu-id="3b290-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





