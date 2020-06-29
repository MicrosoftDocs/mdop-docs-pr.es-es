---
title: Uso de un entorno de prueba
description: Uso de un entorno de prueba
author: dansimp
ms.assetid: fc5fcc7c-1ac8-483a-a6bd-2279ae2ee3fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc3ad91747c755efe0576cc62473848094b72ed1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818171"
---
# <span data-ttu-id="b2982-103">Uso de un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="b2982-103">Using a Test Environment</span></span>


<span data-ttu-id="b2982-104">Antes de solicitar que se implemente un objeto de directiva de grupo (GPO) en el entorno de producción, debe probar el GPO en un entorno de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="b2982-104">Before you request that a Group Policy Object (GPO) be deployed to the production environment, you should test the GPO in a lab environment.</span></span> <span data-ttu-id="b2982-105">Si desarrolla el GPO en un dominio de un bosque de prueba, puede exportar el GPO a un archivo e importarlo a un dominio del bosque de producción.</span><span class="sxs-lookup"><span data-stu-id="b2982-105">If you develop the GPO in a domain in a test forest, you can export the GPO to a file and import the file to a domain in the production forest.</span></span> <span data-ttu-id="b2982-106">Después, puede probar el GPO vinculándolos a una unidad organizativa (OU) que contenga equipos de prueba y usuarios.</span><span class="sxs-lookup"><span data-stu-id="b2982-106">You can then test the GPO by linking it to an organizational unit (OU) that contains test computers and users.</span></span>

-   [<span data-ttu-id="b2982-107">Exportar un GPO a un archivo</span><span class="sxs-lookup"><span data-stu-id="b2982-107">Export a GPO to a File</span></span>](export-a-gpo-to-a-file.md)

-   [<span data-ttu-id="b2982-108">Importar un GPO desde un archivo</span><span class="sxs-lookup"><span data-stu-id="b2982-108">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-ed.md)

-   [<span data-ttu-id="b2982-109">Probar un GPO en una unidad organizativa independiente</span><span class="sxs-lookup"><span data-stu-id="b2982-109">Test a GPO in a Separate Organizational Unit</span></span>](test-a-gpo-in-a-separate-organizational-unit-agpm40.md)

<span data-ttu-id="b2982-110">**Nota:**  También puede importar un objeto de directiva de grupo desde el entorno de producción del dominio.</span><span class="sxs-lookup"><span data-stu-id="b2982-110">**Note** You can also import a GPO from the production environment of the domain.</span></span> <span data-ttu-id="b2982-111">Para obtener más información, vea [importar un GPO desde la producción](import-a-gpo-from-production-agpm40-ed.md).</span><span class="sxs-lookup"><span data-stu-id="b2982-111">For more information, see [Import a GPO from Production](import-a-gpo-from-production-agpm40-ed.md).</span></span>

 

 

 





