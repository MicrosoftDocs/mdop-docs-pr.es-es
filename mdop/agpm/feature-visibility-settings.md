---
title: Configuración de visibilidad de funciones
description: Configuración de visibilidad de funciones
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820810"
---
# <span data-ttu-id="4c2af-103">Configuración de visibilidad de funciones</span><span class="sxs-lookup"><span data-stu-id="4c2af-103">Feature Visibility Settings</span></span>


<span data-ttu-id="4c2af-104">La configuración de la plantilla administrativa de administración de directivas de grupo (AGPM) avanzada le permite configurar de forma centralizada la visibilidad del nodo **control de cambios** y la pestaña **historial** para los administradores de directiva de grupo a los que se aplica un objeto de directiva de grupo (GPO) con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="4c2af-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="4c2af-105">La siguiente configuración está disponible en la consola de administración de Configuration\\Administrative Templates\\Windows de usuario de Components\\Microsoft \ \ restricciones/permitidos Snap-ins\\Extension en el **Editor de objetos de directiva de grupo** al editar un GPO en la consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="4c2af-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="4c2af-106">Si esta ruta de acceso no está visible, haga clic con el botón secundario en **plantillas administrativas**y agregue la plantilla AGPM. ADMX o AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="4c2af-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c2af-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="4c2af-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="4c2af-108">Efecto</span><span class="sxs-lookup"><span data-stu-id="4c2af-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c2af-109">Control de cambios de AGPM</span><span class="sxs-lookup"><span data-stu-id="4c2af-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c2af-110">Si se habilita o no se configura, el <strong> </strong> nodo de control de cambios estará visible en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="4c2af-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="4c2af-111">Si se deshabilita, el <strong> </strong> nodo de control de cambios no es visible en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="4c2af-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c2af-112">Extensión de vínculo de AGPM</span><span class="sxs-lookup"><span data-stu-id="4c2af-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c2af-113">Si se habilita o no se configura <strong> , </strong> aparece una ficha historial en la GPMC para cada GPO vinculado.</span><span class="sxs-lookup"><span data-stu-id="4c2af-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="4c2af-114">Si está deshabilitada, la <strong> </strong> ficha historial no está visible para los GPO vinculados.</span><span class="sxs-lookup"><span data-stu-id="4c2af-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c2af-115">Extensión de GPO de AGPM</span><span class="sxs-lookup"><span data-stu-id="4c2af-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c2af-116">Si se habilita o no se configura <strong> , </strong> aparece una ficha historial en la GPMC para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="4c2af-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="4c2af-117">Si se deshabilita, <strong> la </strong> ficha historial no está visible para los GPO.</span><span class="sxs-lookup"><span data-stu-id="4c2af-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4c2af-118">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="4c2af-118">Additional references</span></span>

-   [<span data-ttu-id="4c2af-119">Configuración de plantilla administrativa</span><span class="sxs-lookup"><span data-stu-id="4c2af-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





