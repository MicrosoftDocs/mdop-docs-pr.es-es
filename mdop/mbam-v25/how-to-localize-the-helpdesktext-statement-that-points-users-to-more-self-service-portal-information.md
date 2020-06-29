---
title: Cómo localizar la instrucción "HelpdeskText" que dirige a los usuarios a obtener más información del portal de autoservicio
description: Cómo localizar la instrucción "HelpdeskText" que dirige a los usuarios a obtener más información del portal de autoservicio
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823421"
---
# <span data-ttu-id="06391-103">Cómo localizar la instrucción "HelpdeskText" que dirige a los usuarios a obtener más información del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="06391-103">How to Localize the “HelpdeskText” Statement that Points Users to More Self-Service Portal Information</span></span>


<span data-ttu-id="06391-104">Puede configurar una versión localizada de la instrucción "HelpdeskText" del portal de autoservicio, que informa a los usuarios finales sobre cómo obtener ayuda adicional cuando usan el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="06391-104">You can configure a localized version of the Self-Service Portal "HelpdeskText" statement, which informs end users about how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="06391-105">Si configura el texto localizado de la instrucción, tal y como se describe en las siguientes instrucciones, MBAM muestra la versión localizada.</span><span class="sxs-lookup"><span data-stu-id="06391-105">If you configure localized text for the statement, as described in the following instructions, MBAM displays the localized version.</span></span> <span data-ttu-id="06391-106">Si MBAM no encuentra la versión localizada, muestra el valor que está en el parámetro **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="06391-106">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

<span data-ttu-id="06391-107">**Nota:**  En las siguientes instrucciones, *SelfService* es el nombre del directorio virtual predeterminado para el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="06391-107">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="06391-108">Es posible que haya usado un nombre diferente al configurar el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="06391-108">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="06391-109">Para mostrar una versión localizada de la instrucción HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="06391-109">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="06391-110">En el servidor en el que ha configurado el portal de autoservicio, vaya a **sitios** &gt; configuración de **Administración y supervisión de Microsoft BitLocker** &gt; **SelfService** &gt; **configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="06391-110">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="06391-111">En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .</span><span class="sxs-lookup"><span data-stu-id="06391-111">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="06391-112">En el campo **nombre** , escriba **HelpdeskText**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para el texto.</span><span class="sxs-lookup"><span data-stu-id="06391-112">In the **Name** field, type **HelpdeskText**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the text.</span></span>

    <span data-ttu-id="06391-113">Por ejemplo, para crear una instrucción HelpdeskText localizada en español, asigne el nombre **HelpdeskText \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="06391-113">For example, to create a localized HelpdeskText statement in Spanish, name the parameter **HelpdeskText\_es-es**.</span></span>

    <span data-ttu-id="06391-114">El nombre de la carpeta de idioma también puede ser **el nombre del** idioma neutral en lugar de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="06391-114">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="06391-115">Si el explorador del usuario final se establece en es **-es** y esa carpeta no existe, la configuración regional principal (tal como se define en .net) se recupera y se comprueba de forma recursiva, lo que permite resolver &lt; el directorio de instalación de autoservicio &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de convertirse en el archivo predeterminado Notice.txt.</span><span class="sxs-lookup"><span data-stu-id="06391-115">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="06391-116">Esta reserva recursiva imita las reglas de carga de recursos de .NET.</span><span class="sxs-lookup"><span data-stu-id="06391-116">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="06391-117">Para obtener una lista de los códigos de idioma válidos que puede usar, consulte referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="06391-117">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="06391-118">En el campo **valor** , escriba el texto localizado que desea mostrar a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="06391-118">In the **Value** field, type the localized text that you want to display to end users.</span></span>



## <span data-ttu-id="06391-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06391-119">Related topics</span></span>


[<span data-ttu-id="06391-120">Personalización del portal de autoservicio para la organización</span><span class="sxs-lookup"><span data-stu-id="06391-120">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 

## <span data-ttu-id="06391-121">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="06391-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="06391-122">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="06391-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="06391-123">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="06391-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



