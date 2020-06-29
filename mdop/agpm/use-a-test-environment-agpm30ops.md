---
title: Usar un entorno de prueba
description: Usar un entorno de prueba
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818240"
---
# <span data-ttu-id="a88e3-103">Usar un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="a88e3-103">Use a Test Environment</span></span>


<span data-ttu-id="a88e3-104">Si usa una unidad organizativa (OU) Testing para probar objetos de directiva de grupo (GPO) antes de la implementación en el entorno de producción, debe disponer de los permisos necesarios para obtener acceso a la OU de prueba.</span><span class="sxs-lookup"><span data-stu-id="a88e3-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="a88e3-105">El uso de una OU de prueba es opcional.</span><span class="sxs-lookup"><span data-stu-id="a88e3-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="a88e3-106">Para usar una OU de prueba</span><span class="sxs-lookup"><span data-stu-id="a88e3-106">To use a test OU</span></span>**

1.  <span data-ttu-id="a88e3-107">Mientras el GPO está desprotegido para editarlo, en la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que está administrando los GPO.</span><span class="sxs-lookup"><span data-stu-id="a88e3-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="a88e3-108">Haga clic en la copia desprotegida del GPO que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="a88e3-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="a88e3-109">El nombre estará precedido por **\ [desprotegido \]**.</span><span class="sxs-lookup"><span data-stu-id="a88e3-109">The name will be preceded with **\[Checked Out\]**.</span></span> <span data-ttu-id="a88e3-110">(Si no aparece en la lista, haga clic en **acción**y, a continuación, en **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a88e3-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="a88e3-111">Ordenar los nombres alfabéticamente y **\ [desprotegido \]** los objetos de directiva de grupo normalmente aparecerán en la parte superior de la lista.)</span><span class="sxs-lookup"><span data-stu-id="a88e3-111">Sort the names alphabetically, and **\[Checked Out\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="a88e3-112">Arrastre y coloque el GPO en la OU de prueba.</span><span class="sxs-lookup"><span data-stu-id="a88e3-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="a88e3-113">Haga clic en **Aceptar** en el cuadro de diálogo que le pregunta si desea crear un vínculo al GPO en la ou de prueba.</span><span class="sxs-lookup"><span data-stu-id="a88e3-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="a88e3-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="a88e3-114">Additional considerations</span></span>

-   <span data-ttu-id="a88e3-115">Cuando finalice la prueba, la incorporación del GPO elimina automáticamente el vínculo a la copia desprotegida del GPO.</span><span class="sxs-lookup"><span data-stu-id="a88e3-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="a88e3-116">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a88e3-116">Additional references</span></span>

-   [<span data-ttu-id="a88e3-117">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="a88e3-117">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





