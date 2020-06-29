---
title: Importar un GPO desde un archivo
description: Importar un GPO desde un archivo
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820721"
---
# <span data-ttu-id="34c39-103">Importar un GPO desde un archivo</span><span class="sxs-lookup"><span data-stu-id="34c39-103">Import a GPO from a File</span></span>


<span data-ttu-id="34c39-104">En administración avanzada de directivas de grupo (AGPM), si ha exportado un objeto de directiva de grupo (GPO) a un archivo CAB, puede importar la configuración de directiva de ese GPO a un GPO existente en un dominio de otro bosque.</span><span class="sxs-lookup"><span data-stu-id="34c39-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="34c39-105">Al importar la configuración de directivas en un GPO existente, se reemplaza toda la configuración de la Directiva dentro de ese GPO.</span><span class="sxs-lookup"><span data-stu-id="34c39-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="34c39-106">Para obtener información sobre cómo exportar la configuración de GPO a un archivo CAB, consulte [exportar un GPO a un archivo](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="34c39-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="34c39-107">Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="34c39-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="34c39-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="34c39-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="34c39-109">Para importar la configuración de directivas en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="34c39-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="34c39-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el dominio al que desea importar la configuración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="34c39-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="34c39-111">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="34c39-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="34c39-112">Desproteja el GPO de destino al que desea importar la configuración de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="34c39-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="34c39-113">Haga clic con el botón derecho en el GPO de destino, seleccione **Importar desde**y, a continuación, haga clic en **archivo**.</span><span class="sxs-lookup"><span data-stu-id="34c39-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="34c39-114">Siga las instrucciones del **Asistente para importar configuración** para seleccionar una copia de seguridad de GPO, importar su configuración de directiva para reemplazar a la del GPO de destino y escribir un comentario para la pista de auditoría del GPO de destino.</span><span class="sxs-lookup"><span data-stu-id="34c39-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="34c39-115">De forma predeterminada, el GPO de destino se protege cuando el asistente ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="34c39-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="34c39-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="34c39-116">Additional considerations</span></span>

-   <span data-ttu-id="34c39-117">Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="34c39-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="34c39-118">En concreto, debe tener el contenido de la **lista**, **editar la configuración**y permisos para **importar GPO** para el dominio, y el objeto de directiva de grupo debe estar desprotegido por usted.</span><span class="sxs-lookup"><span data-stu-id="34c39-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="34c39-119">Aunque un editor no puede importar la configuración de directiva en un GPO nuevo durante su creación, un editor puede solicitar la creación de un nuevo GPO y, a continuación, importar la configuración de la Directiva en él después de crearlo.</span><span class="sxs-lookup"><span data-stu-id="34c39-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="34c39-120">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="34c39-120">Additional references</span></span>

-   [<span data-ttu-id="34c39-121">Uso de un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="34c39-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





