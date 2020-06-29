---
title: Cómo localizar el portal de autoservicio "HelpdeskURL"
description: Cómo localizar el portal de autoservicio "HelpdeskURL"
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826710"
---
# <span data-ttu-id="f89cb-103">Cómo localizar el portal de autoservicio "HelpdeskURL"</span><span class="sxs-lookup"><span data-stu-id="f89cb-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="f89cb-104">Puede configurar una versión localizada de la dirección URL del portal de autoservicio para que se muestre a los usuarios finales de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f89cb-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="f89cb-105">La dirección URL del portal de autoservicio se representa mediante el parámetro **HelpdeskURL**.</span><span class="sxs-lookup"><span data-stu-id="f89cb-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="f89cb-106">Si crea una versión localizada, tal y como se describe en las siguientes instrucciones, Microsoft BitLocker Administration and Monitoring (MBAM) busca y muestra la versión localizada.</span><span class="sxs-lookup"><span data-stu-id="f89cb-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="f89cb-107">Si MBAM no encuentra una versión localizada, muestra la dirección URL que está configurada para el parámetro **HelpDeskURL**.</span><span class="sxs-lookup"><span data-stu-id="f89cb-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="f89cb-108">**Nota:**  En las siguientes instrucciones, *SelfService* es el nombre del directorio virtual predeterminado para el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="f89cb-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="f89cb-109">Es posible que haya usado un nombre diferente al configurar el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="f89cb-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="f89cb-110">Para localizar la dirección URL del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="f89cb-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="f89cb-111">En el servidor en el que ha configurado el portal de autoservicio, vaya a **sitios** &gt; configuración de **Administración y supervisión de Microsoft BitLocker** &gt; **SelfService** &gt; **configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f89cb-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="f89cb-112">En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .</span><span class="sxs-lookup"><span data-stu-id="f89cb-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="f89cb-113">En el campo **nombre** , escriba **HelpdeskURL**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f89cb-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="f89cb-114">Por ejemplo, para crear una versión localizada del `HelpdeskURL` valor en español, asigne el nombre **HelpdeskURL \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="f89cb-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="f89cb-115">El nombre de la carpeta de idioma también puede ser **el nombre del** idioma neutral en lugar de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="f89cb-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="f89cb-116">Si el explorador del usuario final se establece en es **-es** y esa carpeta no existe, la configuración regional principal (tal como se define en .net) se recupera y se comprueba de forma recursiva, lo que permite resolver &lt; el directorio de instalación de autoservicio &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de convertirse en el archivo predeterminado Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="f89cb-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="f89cb-117">Esta reserva recursiva imita las reglas de carga de recursos de .NET.</span><span class="sxs-lookup"><span data-stu-id="f89cb-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="f89cb-118">Para obtener una lista de los códigos de idioma válidos que puede usar, consulte referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="f89cb-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="f89cb-119">En el campo **valor** , escriba la versión localizada del `HelpdeskURL` valor que desea mostrar a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="f89cb-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="f89cb-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f89cb-120">Related topics</span></span>


[<span data-ttu-id="f89cb-121">Personalización del portal de autoservicio para la organización</span><span class="sxs-lookup"><span data-stu-id="f89cb-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="f89cb-122">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="f89cb-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f89cb-123">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f89cb-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f89cb-124">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f89cb-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




