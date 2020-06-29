---
title: Probar un GPO en una unidad organizativa independiente
description: Probar un GPO en una unidad organizativa independiente
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818260"
---
# <span data-ttu-id="309de-103">Probar un GPO en una unidad organizativa independiente</span><span class="sxs-lookup"><span data-stu-id="309de-103">Test a GPO in a Separate Organizational Unit</span></span>


<span data-ttu-id="309de-104">Si usa una unidad organizativa (OU) Testing para probar objetos de directiva de grupo (GPO) dentro del mismo dominio antes de la implementación en el entorno de producción, debe disponer de los permisos necesarios para obtener acceso a la OU de prueba.</span><span class="sxs-lookup"><span data-stu-id="309de-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) within the same domain before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="309de-105">El uso de una OU de prueba es opcional.</span><span class="sxs-lookup"><span data-stu-id="309de-105">Using a test OU is optional.</span></span>

**<span data-ttu-id="309de-106">Para usar una OU de prueba</span><span class="sxs-lookup"><span data-stu-id="309de-106">To use a test OU</span></span>**

1.  <span data-ttu-id="309de-107">Aunque el GPO está desprotegido para editarlo, en la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que está administrando los GPO.</span><span class="sxs-lookup"><span data-stu-id="309de-107">Although you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="309de-108">Haga clic en la copia desprotegida del GPO que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="309de-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="309de-109">El nombre estará precedido por **\ [AGPM \]**.</span><span class="sxs-lookup"><span data-stu-id="309de-109">The name will be preceded by **\[AGPM\]**.</span></span> <span data-ttu-id="309de-110">(Si no aparece en la lista, haga clic en **acción**y, a continuación, en **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="309de-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="309de-111">Ordene los nombres alfabéticamente y **\ [AGPM \]** los GPO suelen aparecer en la parte superior de la lista.)</span><span class="sxs-lookup"><span data-stu-id="309de-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="309de-112">Arrastre el GPO a la OU de prueba.</span><span class="sxs-lookup"><span data-stu-id="309de-112">Drag the GPO to the test OU.</span></span>

4.  <span data-ttu-id="309de-113">Haga clic en **Aceptar** en el cuadro de diálogo que le pregunta si desea crear un vínculo al GPO en la ou de prueba.</span><span class="sxs-lookup"><span data-stu-id="309de-113">Click **OK** in the dialog box that asks whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="309de-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="309de-114">Additional considerations</span></span>

-   <span data-ttu-id="309de-115">Cuando finalice la prueba, la incorporación del GPO elimina automáticamente el vínculo a la copia desprotegida del GPO.</span><span class="sxs-lookup"><span data-stu-id="309de-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="309de-116">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="309de-116">Additional references</span></span>

-   [<span data-ttu-id="309de-117">Uso de un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="309de-117">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





