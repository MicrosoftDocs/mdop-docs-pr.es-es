---
title: Importar un GPO desde un archivo
description: Importar un GPO desde un archivo
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820751"
---
# <span data-ttu-id="e6185-103">Importar un GPO desde un archivo</span><span class="sxs-lookup"><span data-stu-id="e6185-103">Import a GPO from a File</span></span>


<span data-ttu-id="e6185-104">En administración avanzada de directivas de grupo (AGPM), si es un administrador de AGPM (control total) y ha exportado un objeto de directiva de grupo (GPO) a un archivo CAB, puede importar la configuración de directiva de ese GPO a un nuevo GPO o a un GPO existente en un dominio de otro bosque.</span><span class="sxs-lookup"><span data-stu-id="e6185-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="e6185-105">Para obtener información sobre cómo exportar la configuración de GPO a un archivo CAB, consulte [exportar un GPO a un archivo](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="e6185-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="e6185-106">Es necesario disponer de una cuenta de usuario con el rol de administrador de AGPM o los permisos necesarios en AGPM para importar la configuración de la Directiva a un nuevo GPO controlado.</span><span class="sxs-lookup"><span data-stu-id="e6185-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="e6185-107">Se necesita una cuenta de usuario con la función editor o administrador de AGPM o los permisos necesarios en AGPM para importar la configuración de la Directiva a un GPO existente.</span><span class="sxs-lookup"><span data-stu-id="e6185-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="e6185-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="e6185-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="e6185-109">Importar la configuración de la directiva desde un archivo</span><span class="sxs-lookup"><span data-stu-id="e6185-109">Importing policy settings from a file</span></span>


<span data-ttu-id="e6185-110">Cuando importa la configuración de una directiva de un archivo, puede importarla a un nuevo GPO o a un GPO existente.</span><span class="sxs-lookup"><span data-stu-id="e6185-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="e6185-111">Sin embargo, si importa la configuración de una directiva en un GPO existente, se reemplazarán todas las configuraciones de directiva que contenga.</span><span class="sxs-lookup"><span data-stu-id="e6185-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="e6185-112">Importar la configuración de directiva en un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="e6185-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="e6185-113">Importar la configuración de directiva en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="e6185-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="e6185-114">Para importar la configuración de directivas en un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="e6185-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="e6185-115">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el dominio al que desea importar la configuración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e6185-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="e6185-116">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="e6185-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e6185-117">Crear un nuevo GPO controlado.</span><span class="sxs-lookup"><span data-stu-id="e6185-117">Create a new controlled GPO.</span></span> <span data-ttu-id="e6185-118">En el cuadro de diálogo **nuevo GPO controlado** , haga clic en **importar** y, a continuación, en **iniciar asistente**.</span><span class="sxs-lookup"><span data-stu-id="e6185-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="e6185-119">Para obtener más información sobre cómo crear un GPO, consulte [crear un nuevo GPO controlado](create-a-new-controlled-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e6185-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="e6185-120">Siga las instrucciones del **Asistente para importar configuración** para seleccionar una copia de seguridad de GPO, importar la configuración de la Directiva para el nuevo GPO y escriba un comentario para la pista de auditoría del nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="e6185-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="e6185-121">Para importar la configuración de directivas en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="e6185-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="e6185-122">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el dominio al que desea importar la configuración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e6185-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="e6185-123">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="e6185-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e6185-124">Desproteja el GPO de destino al que desea importar la configuración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e6185-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="e6185-125">Haga clic con el botón derecho en el GPO de destino, seleccione **Importar desde**y, a continuación, haga clic en **archivo**.</span><span class="sxs-lookup"><span data-stu-id="e6185-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="e6185-126">Siga las instrucciones del **Asistente para importar configuración** para seleccionar una copia de seguridad de GPO, importar su configuración de directiva para reemplazar a la del GPO de destino y escribir un comentario para la pista de auditoría del GPO de destino.</span><span class="sxs-lookup"><span data-stu-id="e6185-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="e6185-127">De forma predeterminada, el GPO de destino se protege cuando el asistente ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e6185-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="e6185-128">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="e6185-128">Additional considerations</span></span>

-   <span data-ttu-id="e6185-129">Para importar la configuración de directivas en un nuevo GPO controlado, debe tener permisos de **listar contenido**, **importar GPO**y **crear GPO** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="e6185-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="e6185-130">Para realizar este procedimiento, debe ser administrador de AGPM de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e6185-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="e6185-131">Para importar la configuración de directivas en un GPO existente, debe tener el contenido de la **lista**, **editar la configuración**y permisos para **importar GPO** para el dominio, y el GPO debe estar desprotegido por usted.</span><span class="sxs-lookup"><span data-stu-id="e6185-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="e6185-132">Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e6185-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="e6185-133">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="e6185-133">Additional references</span></span>

-   [<span data-ttu-id="e6185-134">Administración del archivo</span><span class="sxs-lookup"><span data-stu-id="e6185-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





