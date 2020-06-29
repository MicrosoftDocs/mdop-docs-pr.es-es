---
title: Pestaña Servidor AGPM
description: Pestaña Servidor AGPM
author: dansimp
ms.assetid: fb3b0265-53ed-4bf6-88a4-c409f5f1bed4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 335cad07691f914884583636cef01be8dbaa0266
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819290"
---
# <span data-ttu-id="5a51c-103">Pestaña Servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="5a51c-103">AGPM Server Tab</span></span>


<span data-ttu-id="5a51c-104">La pestaña **servidor de AGPM** del panel control de **cambios** le permite seleccionar un servidor de AGPM escribiendo un nombre de equipo y un puerto completos, y para eliminar versiones anteriores de objetos de directiva de grupo (GPO) del archivo para conservar espacio en el disco en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="5a51c-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="5a51c-105">Especificar el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="5a51c-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="5a51c-106">El servidor de AGPM seleccionado determina el archivo que se muestra en la pestaña **contenido** y en qué ubicación se aplica la configuración de **delegación del dominio** .</span><span class="sxs-lookup"><span data-stu-id="5a51c-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="5a51c-107">El puerto predeterminado para administración avanzada de directivas de grupo (AGPM) es el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="5a51c-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="5a51c-108">Si la conexión del servidor de AGPM está configurada de forma centralizada con la configuración de plantillas administrativas, las opciones de esta pestaña para configurar la conexión no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="5a51c-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="5a51c-109">Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="5a51c-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

## <span data-ttu-id="5a51c-110">Eliminar versiones anteriores de GPO</span><span class="sxs-lookup"><span data-stu-id="5a51c-110">Deleting old GPO versions</span></span>


<span data-ttu-id="5a51c-111">De forma predeterminada, todas las versiones de cada GPO controlado se conservan en el archivo.</span><span class="sxs-lookup"><span data-stu-id="5a51c-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="5a51c-112">Sin embargo, puede configurar el servicio AGPM para limitar el número de versiones que se conservan para cada GPO y eliminar automáticamente la versión más antigua cuando se supere ese límite.</span><span class="sxs-lookup"><span data-stu-id="5a51c-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="5a51c-113">Solo las versiones de GPO mostradas en la pestaña **versiones únicas** de la ventana **historial** recuenton el límite.</span><span class="sxs-lookup"><span data-stu-id="5a51c-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="5a51c-114">**Nota:**  El número máximo de versiones únicas para almacenar para cada objeto de directiva de grupo no incluye la versión actual, por lo que la especificación de 0 solo retiene la versión actual.</span><span class="sxs-lookup"><span data-stu-id="5a51c-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="5a51c-115">El límite no debe ser mayor que las versiones de 999.</span><span class="sxs-lookup"><span data-stu-id="5a51c-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="5a51c-116">Cuando se elimina una versión de GPO, se mantiene un registro de esa versión en el historial del GPO, pero la versión de GPO en sí se elimina del archivo.</span><span class="sxs-lookup"><span data-stu-id="5a51c-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="5a51c-117">Para evitar que se elimine una versión de GPO, márquelo en el historial como no eliminable.</span><span class="sxs-lookup"><span data-stu-id="5a51c-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="5a51c-118">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="5a51c-118">Additional references</span></span>

-   [<span data-ttu-id="5a51c-119">Interfaz de usuario: Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="5a51c-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="5a51c-120">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="5a51c-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="5a51c-121">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="5a51c-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





