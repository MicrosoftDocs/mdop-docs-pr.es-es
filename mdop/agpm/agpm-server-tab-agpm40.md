---
title: Pestaña Servidor AGPM
description: Pestaña Servidor AGPM
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819281"
---
# <span data-ttu-id="723db-103">Pestaña Servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="723db-103">AGPM Server Tab</span></span>


<span data-ttu-id="723db-104">La pestaña **servidor de AGPM** del panel control de **cambios** le permite seleccionar un servidor de AGPM escribiendo un nombre de equipo y un puerto completos, y para eliminar versiones anteriores de objetos de directiva de grupo (GPO) del archivo para conservar espacio en el disco en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="723db-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="723db-105">Especificar el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="723db-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="723db-106">El servidor de AGPM seleccionado determina el archivo que se muestra en la pestaña **contenido** y en qué ubicación se aplica la configuración de **delegación del dominio** .</span><span class="sxs-lookup"><span data-stu-id="723db-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="723db-107">El puerto predeterminado para administración avanzada de directivas de grupo (AGPM) es el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="723db-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="723db-108">Si la conexión del servidor de AGPM está configurada de forma centralizada con la configuración de plantillas administrativas, las opciones de esta pestaña para configurar la conexión no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="723db-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="723db-109">Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="723db-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

## <span data-ttu-id="723db-110">Eliminar versiones anteriores de GPO</span><span class="sxs-lookup"><span data-stu-id="723db-110">Deleting old GPO versions</span></span>


<span data-ttu-id="723db-111">De forma predeterminada, todas las versiones de cada GPO controlado se conservan en el archivo.</span><span class="sxs-lookup"><span data-stu-id="723db-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="723db-112">Sin embargo, puede configurar el servicio AGPM para limitar el número de versiones que se conservan para cada GPO y eliminar automáticamente la versión más antigua cuando se supere ese límite.</span><span class="sxs-lookup"><span data-stu-id="723db-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="723db-113">Solo las versiones de GPO mostradas en la pestaña **versiones únicas** de la ventana **historial** recuenton el límite.</span><span class="sxs-lookup"><span data-stu-id="723db-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="723db-114">**Nota:**  El número máximo de versiones únicas para almacenar para cada objeto de directiva de grupo no incluye la versión actual, por lo que la especificación de 0 solo retiene la versión actual.</span><span class="sxs-lookup"><span data-stu-id="723db-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="723db-115">El límite no debe ser mayor que las versiones de 999.</span><span class="sxs-lookup"><span data-stu-id="723db-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="723db-116">Cuando se elimina una versión de GPO, se mantiene un registro de esa versión en el historial del GPO, pero la versión de GPO en sí se elimina del archivo.</span><span class="sxs-lookup"><span data-stu-id="723db-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="723db-117">Para evitar que se elimine una versión de GPO, márquelo en el historial como no eliminable.</span><span class="sxs-lookup"><span data-stu-id="723db-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="723db-118">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="723db-118">Additional references</span></span>

-   [<span data-ttu-id="723db-119">Interfaz de usuario: Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="723db-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="723db-120">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="723db-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="723db-121">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="723db-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





