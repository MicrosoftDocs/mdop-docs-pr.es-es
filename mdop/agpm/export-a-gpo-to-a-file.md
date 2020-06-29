---
title: Exportar un GPO a un archivo
description: Exportar un GPO a un archivo
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820851"
---
# <span data-ttu-id="532d5-103">Exportar un GPO a un archivo</span><span class="sxs-lookup"><span data-stu-id="532d5-103">Export a GPO to a File</span></span>


<span data-ttu-id="532d5-104">Puede exportar un objeto de directiva de grupo (GPO) controlado a un archivo CAB para poder copiarlo en un dominio de otro bosque e importar el GPO a administración de directivas de grupo (AGPM) avanzada en ese dominio.</span><span class="sxs-lookup"><span data-stu-id="532d5-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="532d5-105">Para obtener información sobre cómo importar la configuración de GPO a un GPO nuevo o existente, consulte [importar un GPO desde un archivo](import-a-gpo-from-a-file-ed.md).</span><span class="sxs-lookup"><span data-stu-id="532d5-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="532d5-106">Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="532d5-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="532d5-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="532d5-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="532d5-108">Para exportar un GPO a un archivo</span><span class="sxs-lookup"><span data-stu-id="532d5-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="532d5-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="532d5-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="532d5-110">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="532d5-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="532d5-111">Haga clic con el botón secundario en el GPO y luego haga clic en **exportar a**.</span><span class="sxs-lookup"><span data-stu-id="532d5-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="532d5-112">Escriba un nombre de archivo para el archivo al que desea exportar el GPO y, a continuación, haga clic en **exportar**.</span><span class="sxs-lookup"><span data-stu-id="532d5-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="532d5-113">Si el archivo no existe, se crea.</span><span class="sxs-lookup"><span data-stu-id="532d5-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="532d5-114">Si ya existe, se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="532d5-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="532d5-115">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="532d5-115">Additional considerations</span></span>

-   <span data-ttu-id="532d5-116">Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="532d5-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="532d5-117">En concreto, debe tener permisos de **lista**, **Leer configuración**y **exportar GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="532d5-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="532d5-118">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="532d5-118">Additional references</span></span>

-   [<span data-ttu-id="532d5-119">Uso de un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="532d5-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





