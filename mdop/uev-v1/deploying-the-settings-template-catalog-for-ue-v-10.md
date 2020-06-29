---
title: Implementación del catálogo de plantillas de configuración de UE-V 1.0
description: Implementación del catálogo de plantillas de configuración de UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826631"
---
# <span data-ttu-id="41ef8-103">Implementación del catálogo de plantillas de configuración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="41ef8-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="41ef8-104">Las plantillas de ubicación de configuración personalizadas se pueden almacenar en una ruta de carpeta en equipos de virtualización de Microsoft User Experience (UE-V) o en un recurso compartido de red de bloque de mensajes de servidor (SMB).</span><span class="sxs-lookup"><span data-stu-id="41ef8-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="41ef8-105">Una tarea programada en el equipo comprueba si hay plantillas nuevas o actualizadas de esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="41ef8-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="41ef8-106">La tarea comprueba esta ubicación una vez al día y actualiza su comportamiento de sincronización en función de las plantillas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="41ef8-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="41ef8-107">Las plantillas que se agregan o actualizan en esta carpeta desde la última comprobación son registradas por el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="41ef8-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="41ef8-108">UE-V Agent cancela el registro de las plantillas que se quitaron de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="41ef8-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="41ef8-109">La tarea programada se ejecuta como sistema.</span><span class="sxs-lookup"><span data-stu-id="41ef8-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="41ef8-110">Como mínimo, el recurso compartido de red debe conceder permisos para el grupo equipos del dominio.</span><span class="sxs-lookup"><span data-stu-id="41ef8-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="41ef8-111">Además, conceda permisos de acceso a la carpeta de recursos compartidos de red a los administradores que administrarán las plantillas almacenadas.</span><span class="sxs-lookup"><span data-stu-id="41ef8-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="41ef8-112">Para obtener más información sobre las plantillas de ubicación de configuración personalizadas, consulte [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="41ef8-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="41ef8-113">Para configurar el catálogo de plantillas de configuración para UE-V</span><span class="sxs-lookup"><span data-stu-id="41ef8-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="41ef8-114">Cree una nueva carpeta en el equipo en el que se guardará el catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="41ef8-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="41ef8-115">Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de catálogos de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="41ef8-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="41ef8-116">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="41ef8-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="41ef8-117">Recomendar permisos</span><span class="sxs-lookup"><span data-stu-id="41ef8-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="41ef8-118">Todos</span><span class="sxs-lookup"><span data-stu-id="41ef8-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-119">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="41ef8-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="41ef8-120">Equipos del dominio</span><span class="sxs-lookup"><span data-stu-id="41ef8-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-121">Niveles de permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="41ef8-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="41ef8-122">Administradores</span><span class="sxs-lookup"><span data-stu-id="41ef8-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-123">Niveles de permisos de lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="41ef8-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="41ef8-124">Configure los siguientes permisos NTFS para la carpeta del catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="41ef8-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="41ef8-125">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="41ef8-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="41ef8-126">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="41ef8-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="41ef8-127">Aplicar a</span><span class="sxs-lookup"><span data-stu-id="41ef8-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="41ef8-128">Creador/propietario</span><span class="sxs-lookup"><span data-stu-id="41ef8-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-129">Control total</span><span class="sxs-lookup"><span data-stu-id="41ef8-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-130">Esta carpeta, subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="41ef8-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="41ef8-131">Equipos del dominio</span><span class="sxs-lookup"><span data-stu-id="41ef8-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-132">Mostrar el contenido de la carpeta y leer</span><span class="sxs-lookup"><span data-stu-id="41ef8-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-133">Esta carpeta, subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="41ef8-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="41ef8-134">Todos</span><span class="sxs-lookup"><span data-stu-id="41ef8-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-135">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="41ef8-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-136">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="41ef8-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="41ef8-137">Administradores</span><span class="sxs-lookup"><span data-stu-id="41ef8-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-138">Control total</span><span class="sxs-lookup"><span data-stu-id="41ef8-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="41ef8-139">Esta carpeta, subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="41ef8-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="41ef8-140">Haga clic en **Aceptar** para cerrar los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41ef8-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="41ef8-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41ef8-141">Related topics</span></span>


[<span data-ttu-id="41ef8-142">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="41ef8-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="41ef8-143">Planificación de la implementación de la plantilla personalizada para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="41ef8-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





