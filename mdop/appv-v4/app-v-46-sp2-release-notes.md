---
title: Notas de la versión de App-V 4.6 SP2
description: Notas de la versión de App-V 4.6 SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822341"
---
# <span data-ttu-id="a5b5c-103">Notas de la versión de App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="a5b5c-103">App-V 4.6 SP2 Release Notes</span></span>


**<span data-ttu-id="a5b5c-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="a5b5c-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft Application Virtualization (App-V) 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-105">Read these release notes thoroughly before you install Microsoft Application Virtualization (App-V)4.6 SP2.</span></span>

<span data-ttu-id="a5b5c-106">Estas notas de la versión contienen la información necesaria para instalar correctamente Application Virtualization 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-106">These release notes contain information that is required to successfully install Application Virtualization 4.6 SP2.</span></span> <span data-ttu-id="a5b5c-107">Las notas de la versión también contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="a5b5c-108">Si hay una diferencia entre estas notas de la versión y otra documentación de App-V 4.6 SP2, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-108">If there is a difference between these release notes and other App-V4.6SP2 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="a5b5c-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="a5b5c-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="a5b5c-110">About the Product Documentation</span></span>


<span data-ttu-id="a5b5c-111">Para obtener más información sobre la documentación de App-V, consulte la página de [virtualización de aplicaciones](https://go.microsoft.com/fwlink/?LinkID=232982) en Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-111">For more information about documentation for App-V, see the [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) page on Microsoft TechNet.</span></span>

## <span data-ttu-id="a5b5c-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5b5c-112">Providing feedback</span></span>


<span data-ttu-id="a5b5c-113">Nos interesan tus comentarios en App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-113">We are interested in your feedback on App-V4.6SP2.</span></span> <span data-ttu-id="a5b5c-114">Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="a5b5c-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="a5b5c-115">**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios para la documentación y las versiones de producto.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-115">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="a5b5c-116">Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="a5b5c-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="a5b5c-117">Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="a5b5c-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a><span data-ttu-id="a5b5c-118">Problemas conocidos con App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="a5b5c-118">Known Issues with App-V4.6SP2</span></span>


### <span data-ttu-id="a5b5c-119">La compatibilidad con los nombres de archivo cortos está deshabilitada para las unidades físicas que no son del sistema cuando se secuencia</span><span class="sxs-lookup"><span data-stu-id="a5b5c-119">Short file name support is disabled for non-system physical drives when you sequence</span></span>

<span data-ttu-id="a5b5c-120">Cuando se hace una secuencia en Windows 8 o Windows Server 2012, la compatibilidad con los nombres de archivo cortos (8,3) está deshabilitada de forma predeterminada para las unidades físicas que no son del sistema.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-120">When you sequence on Windows 8 or Windows Server 2012, support for short file names (8.3) is disabled by default for non-system physical drives.</span></span>

<span data-ttu-id="a5b5c-121">La unidad física subyacente asociada al directorio de la aplicación virtual principal (por ejemplo, "Q:\\appname") en la estación de secuenciación debe proporcionar compatibilidad de nombre corto (8,3) para que el secuenciador de App-V 4.6 SP2 genere nombres de archivo cortos al crear paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-121">The underlying physical drive associated with the primary virtual application directory (for example, “Q:\\appname”) on the sequencing station must provide short file name (8.3) support in order for the App-V4.6SP2 Sequencer to generate short file names when creating virtual application packages.</span></span> <span data-ttu-id="a5b5c-122">La compatibilidad de nombre corto de archivo (8,3) está deshabilitada de forma predeterminada para las unidades físicas que no son del sistema en Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-122">Short file name (8.3) support is disabled by default for non-system physical drives on Windows 8 or Windows Server 2012.</span></span>

<span data-ttu-id="a5b5c-123">**Solución alternativa:** Habilitar la compatibilidad con nombres de archivo cortos (8,3) en unidades físicas que no son del sistema.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-123">**Workaround:** Enable short file name (8.3) support on non-system physical drives.</span></span> <span data-ttu-id="a5b5c-124">Puede usar el siguiente comando para habilitar la compatibilidad de nombre de archivo breve en Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-124">You can use the following command to enable short file name support on Windows 8 or Windows Server 2012.</span></span>

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

<span data-ttu-id="a5b5c-125">Por ejemplo, use el comando siguiente si la letra de unidad es "Q:":</span><span class="sxs-lookup"><span data-stu-id="a5b5c-125">For example, use the following command if the drive letter is “Q:”:</span></span>

``` syntax
fsutil 8dot3name set Q: 0
```

<span data-ttu-id="a5b5c-126">**Nota:**  No es necesario cambiar esta configuración en el cliente de App-V porque el sistema de archivos de App-V controla correctamente las rutas breves en Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-126">**Note** You do not need to change this setting on the App-V client because the App-V file system properly handles short paths on Windows 8 or Windows Server 2012.</span></span>

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> <span data-ttu-id="a5b5c-127">App-V no invalida el controlador predeterminado para las asociaciones de protocolo o tipo de archivo en Windows 8</span><span class="sxs-lookup"><span data-stu-id="a5b5c-127">App-V does not override the default handler for file type or protocol associations on Windows 8</span></span>

<span data-ttu-id="a5b5c-128">Si selecciona una aplicación predeterminada usando **programas predeterminados** en el **Panel de control** en Windows 8, App-V no invalidará las asociaciones de tipos de archivo asociados de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-128">If you select a default application by using **Default Programs** in **Control Panel** on Windows 8, App-V will not override the associated file type associations for that application.</span></span>

<span data-ttu-id="a5b5c-129">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-129">**Workaround:** None.</span></span>

### <span data-ttu-id="a5b5c-130">Outlook 2010 virtualizado no se ofrece como una opción para los vínculos que se puede hacer clic en correo en Windows 8</span><span class="sxs-lookup"><span data-stu-id="a5b5c-130">Virtualized Outlook 2010 is not offered as an option for mailto clickable links on Windows 8</span></span>

<span data-ttu-id="a5b5c-131">La extensión de Shell mailto no ofrece la 2010 virtualizada de Outlook en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-131">The mailto shell extension does not offer virtualized Outlook 2010 on Windows 8.</span></span> <span data-ttu-id="a5b5c-132">Por ejemplo, si hace clic en un vínculo mailto: desde la 2010 de Outlook virtualizada que se ejecuta en Windows 8, no se creará una ventana de correo electrónico nueva.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-132">For example, if you click a mailto: link from virtualized Outlook 2010 that is running on Windows 8, a new email window is not created.</span></span> <span data-ttu-id="a5b5c-133">Esta opción funciona correctamente en Windows 7 y versiones anteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-133">This option works correctly on Windows 7 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="a5b5c-134">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-134">**Workaround:** None.</span></span>

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> <span data-ttu-id="a5b5c-135">La actualización de Application Virtualization 4,6 SP2 no se ofrece en todas las configuraciones regionales que usan Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="a5b5c-135">Application Virtualization 4.6 SP2 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="a5b5c-136">Cuando usa Microsoft Update, la actualización de App-V 4.6 SP2 no está disponible para las siguientes configuraciones regionales de idioma:</span><span class="sxs-lookup"><span data-stu-id="a5b5c-136">When you use Microsoft Update, the update for App-V4.6SP2 is not available for the following language locales:</span></span>

-   <span data-ttu-id="a5b5c-137">Kazajo</span><span class="sxs-lookup"><span data-stu-id="a5b5c-137">Kazakh</span></span>

-   <span data-ttu-id="a5b5c-138">Hindi</span><span class="sxs-lookup"><span data-stu-id="a5b5c-138">Hindi</span></span>

-   <span data-ttu-id="a5b5c-139">Serbio-cirílico</span><span class="sxs-lookup"><span data-stu-id="a5b5c-139">Serbian-Cyrillic</span></span>

<span data-ttu-id="a5b5c-140">**Solución alternativa:** Si usa Microsoft Windows Server Update Services (WSUS), use la versión en Inglés de la actualización o descargue la actualización desde el catálogo de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-140">**Workaround:** If you are using Microsoft Windows Server Update Services (WSUS), use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

## <span data-ttu-id="a5b5c-141">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="a5b5c-141">Release Notes Copyright Information</span></span>


<span data-ttu-id="a5b5c-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="a5b5c-143">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="a5b5c-143">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="a5b5c-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5b5c-144">Related topics</span></span>


[<span data-ttu-id="a5b5c-145">Acerca de Microsoft Application Virtualization4.6SP2</span><span class="sxs-lookup"><span data-stu-id="a5b5c-145">About Microsoft Application Virtualization 4.6 SP2</span></span>](about-microsoft-application-virtualization-46-sp2.md)

 

 





