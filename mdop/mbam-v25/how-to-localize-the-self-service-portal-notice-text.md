---
title: Cómo localizar el texto de aviso del portal de autoservicio
description: Cómo localizar el texto de aviso del portal de autoservicio
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826711"
---
# <span data-ttu-id="661bd-103">Cómo localizar el texto de aviso del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="661bd-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="661bd-104">Puede configurar el texto del aviso localizado para que se muestre a los usuarios finales de forma predeterminada en el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="661bd-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="661bd-105">El archivo de Notice.txt que muestra el texto del aviso se encuentra en el siguiente directorio raíz:</span><span class="sxs-lookup"><span data-stu-id="661bd-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="661bd-106">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="661bd-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="661bd-107">Para mostrar texto de aviso localizado, cree un archivo de Notice.txt localizado y, a continuación, guárdelo en una carpeta de idioma específico en el siguiente directorio de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="661bd-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="661bd-108">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="661bd-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="661bd-109">**Nota:**  Puede configurar la ruta de acceso con el elemento **NoticeTextPath** en **configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="661bd-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="661bd-110">MBAM muestra el texto del aviso, en función de las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="661bd-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="661bd-111">Si crea un archivo de **Notice.txt** localizado en la carpeta de idioma correspondiente, MBAM muestra el texto del aviso localizado si el archivo de **Notice.txt** predeterminado ya existe.</span><span class="sxs-lookup"><span data-stu-id="661bd-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="661bd-112">Si falta el archivo predeterminado **Notice.txt** , aparecerá un mensaje indicando que falta el archivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="661bd-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="661bd-113">Si MBAM no encuentra una versión localizada del archivo Notice.txt, muestra el texto en el archivo predeterminado Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="661bd-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="661bd-114">Si MBAM no encuentra un archivo Notice.txt predeterminado, muestra el texto predeterminado en el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="661bd-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="661bd-115">**Nota:**  Si el explorador de un usuario final se establece en un idioma que no tiene una subcarpeta de idioma correspondiente o Notice.txt, se muestra el texto del archivo de Notice.txt en el siguiente directorio raíz:</span><span class="sxs-lookup"><span data-stu-id="661bd-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="661bd-116">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="661bd-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

 

**<span data-ttu-id="661bd-117">Para crear un archivo de Notice.txt localizado</span><span class="sxs-lookup"><span data-stu-id="661bd-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="661bd-118">En el servidor en el que ha configurado el portal de autoservicio, cree una &lt; *Language* &gt; carpeta de idioma en el siguiente directorio de ejemplo, donde &lt; *idioma* &gt; representa el nombre del idioma localizado:</span><span class="sxs-lookup"><span data-stu-id="661bd-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="661bd-119">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="661bd-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

    <span data-ttu-id="661bd-120">**Nota:**  Algunas carpetas de idioma ya existen, por lo que es posible que no tenga que crear una carpeta.</span><span class="sxs-lookup"><span data-stu-id="661bd-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="661bd-121">Si tiene que crear una carpeta de idioma, vea referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947) para obtener una lista de los nombres válidos que puede usar para la carpeta de &lt; *idioma* &gt; .</span><span class="sxs-lookup"><span data-stu-id="661bd-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="661bd-122">Cree un archivo de Notice.txt que contenga el texto del aviso localizado.</span><span class="sxs-lookup"><span data-stu-id="661bd-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="661bd-123">Guarde el archivo de Notice.txt en la carpeta de &lt; *idioma* &gt; .</span><span class="sxs-lookup"><span data-stu-id="661bd-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="661bd-124">Por ejemplo, para crear un archivo de Notice.txt localizado en español, guarde el archivo de Notice.txt localizado en el siguiente directorio de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="661bd-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="661bd-125">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\Es-es de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="661bd-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="661bd-126">El nombre de la carpeta de idioma también puede ser **el nombre del** idioma neutral en lugar de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="661bd-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="661bd-127">Si el explorador del usuario final se establece en es **-es** y esa carpeta no existe, la configuración regional principal (tal como se define en .net) se recupera y se comprueba de forma recursiva, lo que permite resolver &lt; el directorio de instalación de autoservicio &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de convertirse en el archivo predeterminado Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="661bd-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="661bd-128">Esta reserva recursiva imita las reglas de carga de recursos de .NET.</span><span class="sxs-lookup"><span data-stu-id="661bd-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="661bd-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="661bd-129">Related topics</span></span>


[<span data-ttu-id="661bd-130">Personalización del portal de autoservicio para la organización</span><span class="sxs-lookup"><span data-stu-id="661bd-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="661bd-131">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="661bd-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="661bd-132">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="661bd-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="661bd-133">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="661bd-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





