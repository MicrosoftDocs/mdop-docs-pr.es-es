---
title: Instalación de la plantilla de directiva de grupo de MBAM 2.0
description: Instalación de la plantilla de directiva de grupo de MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826251"
---
# <span data-ttu-id="80c8c-103">Instalación de la plantilla de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="80c8c-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="80c8c-104">Además de las características de administración y supervisión de Microsoft BitLocker relacionadas con el servidor (MBAM), la aplicación de configuración del servidor incluye una plantilla de directiva de grupo supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="80c8c-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="80c8c-105">Esta plantilla se puede instalar en cualquier equipo capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="80c8c-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="80c8c-106">Los pasos siguientes describen cómo instalar la plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="80c8c-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="80c8c-107">**Nota:**  Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="80c8c-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="80c8c-108">Para instalar la plantilla de directiva de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="80c8c-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="80c8c-109">En el servidor en el que desea instalar MBAM, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="80c8c-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="80c8c-110">En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="80c8c-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="80c8c-111">Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="80c8c-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="80c8c-112">De forma predeterminada, se seleccionan todas las características de supervisión y administración de Microsoft BitLocker para la instalación.</span><span class="sxs-lookup"><span data-stu-id="80c8c-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="80c8c-113">Desactive todas las opciones de característica excepto **plantilla de directiva**y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="80c8c-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="80c8c-114">**Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="80c8c-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="80c8c-115">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="80c8c-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="80c8c-116">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="80c8c-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="80c8c-117">Una vez cumplidos todos los requisitos previos, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="80c8c-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="80c8c-118">Para conocer los pasos específicos sobre cómo y dónde instalar las plantillas, consulte [Cómo descargar e implementar plantillas de directiva de grupo de MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="80c8c-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="80c8c-119">Después de que el Asistente para la configuración de administración y supervisión de Microsoft BitLocker muestre páginas de instalación para las características seleccionadas, haga clic en **Finalizar** para cerrar la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="80c8c-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="80c8c-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80c8c-120">Related topics</span></span>


[<span data-ttu-id="80c8c-121">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="80c8c-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





