---
title: Limitar las versiones de GPO almacenados
description: Limitar las versiones de GPO almacenados
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820621"
---
# <span data-ttu-id="c659b-103">Limitar las versiones de GPO almacenados</span><span class="sxs-lookup"><span data-stu-id="c659b-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="c659b-104">De forma predeterminada, todas las versiones de cada objeto de directiva de grupo (GPO) controlado se conservan en el archivo en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="c659b-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="c659b-105">Sin embargo, puede limitar el número de versiones que se conservan para cada GPO y eliminar las versiones anteriores cuando se supere ese límite.</span><span class="sxs-lookup"><span data-stu-id="c659b-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="c659b-106">Cuando se eliminan versiones de GPO, un registro de la versión permanece en el historial del GPO, pero la versión de GPO en sí se elimina del archivo.</span><span class="sxs-lookup"><span data-stu-id="c659b-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="c659b-107">Para completar este procedimiento, debe tener una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="c659b-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="c659b-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="c659b-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c659b-109">Para limitar el número de versiones de GPO almacenadas</span><span class="sxs-lookup"><span data-stu-id="c659b-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="c659b-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="c659b-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c659b-111">En el panel de detalles, haga clic en la pestaña **servidor de AGPM** .</span><span class="sxs-lookup"><span data-stu-id="c659b-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="c659b-112">Active la casilla **Eliminar versiones anteriores de cada GPO del archivo** y escriba el número máximo de versiones de GPO para almacenar para cada GPO, sin incluir la versión actual.</span><span class="sxs-lookup"><span data-stu-id="c659b-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="c659b-113">Para conservar solo la versión actual, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="c659b-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="c659b-114">El máximo no debe ser mayor que 999.</span><span class="sxs-lookup"><span data-stu-id="c659b-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="c659b-115">**Importante**  Solo las versiones de GPO mostradas en la pestaña **versiones únicas** de la ventana **historial** recuenton el límite.</span><span class="sxs-lookup"><span data-stu-id="c659b-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="c659b-116">Haga clic en el botón **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="c659b-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="c659b-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="c659b-117">Additional considerations</span></span>

-   <span data-ttu-id="c659b-118">Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c659b-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c659b-119">En concreto, debe tener los permisos **Mostrar contenido** y **modificar opciones** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="c659b-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="c659b-120">Para evitar que se elimine una versión de GPO, márquelo en el historial como no apto para la eliminación.</span><span class="sxs-lookup"><span data-stu-id="c659b-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="c659b-121">Para ello, haga clic con el botón secundario en la versión del historial del GPO y haga clic en no **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="c659b-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="c659b-122">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="c659b-122">Additional references</span></span>

-   [<span data-ttu-id="c659b-123">Administración del archivo</span><span class="sxs-lookup"><span data-stu-id="c659b-123">Managing the Archive</span></span>](managing-the-archive.md)

 

 





