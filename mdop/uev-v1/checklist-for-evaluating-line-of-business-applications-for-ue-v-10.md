---
title: Lista de comprobación para evaluar aplicaciones de línea de negocio para UE-V 1.0
description: Lista de comprobación para evaluar aplicaciones de línea de negocio para UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826460"
---
# <span data-ttu-id="5556c-103">Lista de comprobación para evaluar aplicaciones de línea de negocio para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="5556c-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="5556c-104">Para evaluar qué aplicaciones de línea de negocio deben incluirse en su implementación de UE-V, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5556c-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="5556c-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="5556c-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-106">¿Esta aplicación contiene opciones de configuración que el usuario puede personalizar?</span><span class="sxs-lookup"><span data-stu-id="5556c-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-107">¿Es importante para el usuario que esta configuración sea móvil?</span><span class="sxs-lookup"><span data-stu-id="5556c-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-108">¿Esta configuración de usuario ya está administrada por una solución de directiva de configuración o administración de aplicaciones?</span><span class="sxs-lookup"><span data-stu-id="5556c-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="5556c-109">UE-V aplica la configuración de la aplicación en el inicio de la aplicación y en la configuración de Windows en los eventos de inicio de sesión, desbloqueo o conexión remota.</span><span class="sxs-lookup"><span data-stu-id="5556c-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="5556c-110">Si usa UE-V con otras soluciones de directiva de configuración, es posible que los usuarios experimenten una incoherencia en la configuración de roaming.</span><span class="sxs-lookup"><span data-stu-id="5556c-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-111">¿Son las configuraciones específicas de la aplicación para el equipo?</span><span class="sxs-lookup"><span data-stu-id="5556c-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="5556c-112">Las preferencias y personalizaciones de la aplicación que están relacionadas con el hardware o con la configuración específica de un equipo no se mueven de manera coherente entre sesiones y pueden provocar una mala experiencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5556c-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-113">¿La configuración del almacén de aplicaciones en el directorio archivos de programa o en el directorio de archivos que se encuentra en el <strong> </strong> directorio \ [nombre de usuario] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="5556c-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="5556c-114">Los datos de la aplicación que se almacenan en cualquiera de estas ubicaciones no suelen ser móviles con el usuario, porque estos datos son específicos del equipo o porque los datos son demasiado grandes para poder ser móviles.</span><span class="sxs-lookup"><span data-stu-id="5556c-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-115">¿La aplicación almacena la configuración en un archivo que contiene otros datos de la aplicación que no deberían ser móviles?</span><span class="sxs-lookup"><span data-stu-id="5556c-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="5556c-116">UE-V sincroniza los archivos como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="5556c-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="5556c-117">Si la configuración se almacena en archivos que incluyen datos de aplicaciones distintos de la configuración, la sincronización de estos datos adicionales puede provocar una mala experiencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5556c-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5556c-118">¿Cuál es el tamaño de los archivos que contienen la configuración?</span><span class="sxs-lookup"><span data-stu-id="5556c-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="5556c-119">El rendimiento de la sincronización de configuración puede verse afectado por archivos grandes.</span><span class="sxs-lookup"><span data-stu-id="5556c-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="5556c-120">La inclusión de archivos grandes puede influir en el rendimiento de la sincronización de configuración.</span><span class="sxs-lookup"><span data-stu-id="5556c-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5556c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5556c-121">Related topics</span></span>


[<span data-ttu-id="5556c-122">Planificación de métodos de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="5556c-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="5556c-123">Planificación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="5556c-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





