---
title: Instalación de la plantilla de directiva de grupo de MBAM 1.0
description: Instalación de la plantilla de directiva de grupo de MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825340"
---
# <span data-ttu-id="304ea-103">Instalación de la plantilla de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="304ea-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="304ea-104">Además de las características relacionadas con el servidor de administración y supervisión de Microsoft BitLocker (MBAM), la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="304ea-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="304ea-105">Puede instalar esta plantilla en cualquier equipo que sea capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="304ea-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="304ea-106">Los pasos siguientes describen cómo instalar la plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="304ea-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="304ea-107">**Nota:**  Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="304ea-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="304ea-108">Para instalar la plantilla de directiva de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="304ea-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="304ea-109">Iniciar el Asistente para la instalación de MBAM. después, haga clic en **instalar** en la Página principal.</span><span class="sxs-lookup"><span data-stu-id="304ea-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="304ea-110">Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="304ea-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="304ea-111">De forma predeterminada, se seleccionan todas las características de MBAM para la instalación.</span><span class="sxs-lookup"><span data-stu-id="304ea-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="304ea-112">Desactive todas las opciones de característica excepto **plantilla de directiva**y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="304ea-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="304ea-113">**Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="304ea-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="304ea-114">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="304ea-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="304ea-115">Si se detecta un requisito previo que falta, debe resolver el requisito previo que falta y, a continuación, volver a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="304ea-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="304ea-116">Una vez cumplidos todos los requisitos previos, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="304ea-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="304ea-117">Cuando el Asistente para la instalación de MBAM muestre las páginas de instalación de las características seleccionadas, haga clic en **Finalizar** para cerrar MBAM configuración.</span><span class="sxs-lookup"><span data-stu-id="304ea-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="304ea-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="304ea-118">Related topics</span></span>


[<span data-ttu-id="304ea-119">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="304ea-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





