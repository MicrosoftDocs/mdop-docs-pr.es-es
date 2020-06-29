---
title: Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft
description: Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824491"
---
# <span data-ttu-id="c524b-103">Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c524b-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="c524b-104">Siga estas instrucciones si los equipos cliente de su organización no tienen acceso a la red de entrega de contenido (CDN) de Microsoft Ajax.</span><span class="sxs-lookup"><span data-stu-id="c524b-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="c524b-105">Por qué necesita configurar esto:</span><span class="sxs-lookup"><span data-stu-id="c524b-105">Why you need to configure this:</span></span>**

<span data-ttu-id="c524b-106">Los equipos cliente necesitan tener acceso a la red CDN, lo que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c524b-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="c524b-107">Si no configura el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red CDN, solo se mostrará el nombre de la empresa y la cuenta en la que se inicia sesión en el usuario final.</span><span class="sxs-lookup"><span data-stu-id="c524b-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="c524b-108">No se mostrará ningún mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="c524b-108">No error message will be shown.</span></span>

<span data-ttu-id="c524b-109">**Nota:**  En MBAM 2,5 SP1, los archivos JavaScript se incluyen en el producto y no es necesario que siga las instrucciones de esta sección para configurar el SSP para que admita clientes que no tienen acceso a Internet.</span><span class="sxs-lookup"><span data-stu-id="c524b-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="c524b-110">Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red CDN</span><span class="sxs-lookup"><span data-stu-id="c524b-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="c524b-111">Descargue los siguientes archivos JavaScript desde la red CDN:</span><span class="sxs-lookup"><span data-stu-id="c524b-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="c524b-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="c524b-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="c524b-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="c524b-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="c524b-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="c524b-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="c524b-115">Copie los archivos de JavaScript en el directorio **scripts** del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="c524b-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="c524b-116">Este directorio se encuentra en <em> &lt; MBAM de autoservicio de directorio de instalación de autoservicio &gt; \\ </em> Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="c524b-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="c524b-117">Abra el administrador de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="c524b-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="c524b-118">Expanda **sitios** &gt; **Microsoft BitLocker administración y supervisión**, y resalte **SelfService**.</span><span class="sxs-lookup"><span data-stu-id="c524b-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="c524b-119">Nota</span><span class="sxs-lookup"><span data-stu-id="c524b-119">Note</span></span>**  
   <span data-ttu-id="c524b-120">*SelfService* es el nombre del directorio virtual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c524b-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="c524b-121">Si ha elegido un nombre diferente para este directorio durante la configuración, recuerde reemplazar *SelfService* en estas instrucciones con el nombre que ha elegido.</span><span class="sxs-lookup"><span data-stu-id="c524b-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="c524b-122">En el panel central, haga doble clic en configuración de la **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="c524b-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="c524b-123">Para cada elemento de la siguiente lista, edite la configuración de la aplicación para que haga referencia a la nueva ubicación mediante reemplazo/ &lt; *directorio virtual* &gt; /con/SelfService/(o el nombre que haya elegido durante la configuración).</span><span class="sxs-lookup"><span data-stu-id="c524b-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="c524b-124">Por ejemplo, la ruta de acceso del directorio virtual será similar a/selfservice/Scripts/jQuery-1.10.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="c524b-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="c524b-125">jQueryPath:/ &lt; *directorio virtual* &gt; /scripts/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="c524b-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="c524b-126">jQueryValidatePath:/ &lt; *directorio virtual* &gt; /scripts/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="c524b-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="c524b-127">jQueryValidateUnobtrusivePath:/ &lt; *directorio virtual* &gt; /scripts/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="c524b-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="c524b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c524b-128">Related topics</span></span>


[<span data-ttu-id="c524b-129">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c524b-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="c524b-130">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="c524b-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c524b-131">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c524b-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c524b-132">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c524b-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





