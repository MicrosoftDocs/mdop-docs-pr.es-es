---
title: Instalar y quitar una aplicación en el área de trabajo de MED-V
description: Instalar y quitar una aplicación en el área de trabajo de MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827220"
---
# <span data-ttu-id="c6582-103">Instalar y quitar una aplicación en el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c6582-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="c6582-104">Las aplicaciones que no son compatibles con el sistema operativo del host se pueden ejecutar en el área de trabajo de MED-V y se pueden abrir en el área de trabajo de MED-V de la misma manera en que se abren desde el equipo host, en el menú **Inicio** o mediante un acceso directo de localhost.</span><span class="sxs-lookup"><span data-stu-id="c6582-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="c6582-105">Después de implementar un área de trabajo de MED-V, tiene varias opciones diferentes disponibles para instalar y quitar aplicaciones en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6582-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="c6582-106">Entre estas opciones se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6582-106">These options include the following:</span></span>

-   [<span data-ttu-id="c6582-107">Uso de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="c6582-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="c6582-108">Uso de un sistema electrónico de distribución de software</span><span class="sxs-lookup"><span data-stu-id="c6582-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="c6582-109">Usar la virtualización de aplicaciones (APP-V)</span><span class="sxs-lookup"><span data-stu-id="c6582-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="c6582-110">Actualización de la imagen principal</span><span class="sxs-lookup"><span data-stu-id="c6582-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="c6582-111">**Importante**  Para asegurarse de que una aplicación instalada se publique automáticamente en el host, instale la aplicación en la máquina virtual para **todos los usuarios**.</span><span class="sxs-lookup"><span data-stu-id="c6582-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="c6582-112">Para obtener más información sobre la publicación de aplicaciones, vea [Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="c6582-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="c6582-113">**Sugerencia**  MED-V no admite el redireccionamiento de invitado a host para la administración de contenido, como, por ejemplo, hacer doble clic en un documento de Microsoft Word en Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6582-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="c6582-114">Por lo tanto, las aplicaciones necesarias, como Microsoft Word, deben instalarse en el área de trabajo de MED-V para proporcionar la funcionalidad de administración de contenido predeterminada que puede esperar un usuario final.</span><span class="sxs-lookup"><span data-stu-id="c6582-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="c6582-115">Agregar y quitar aplicaciones mediante la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="c6582-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="c6582-116">Puede usar la Directiva de grupo y los objetos de directiva de grupo para asignar o publicar aplicaciones a todas o algunas áreas de trabajo de MED-V de su empresa.</span><span class="sxs-lookup"><span data-stu-id="c6582-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="c6582-117">Para las aplicaciones asignadas, cuando un usuario final inicia sesión en su equipo, la aplicación aparece en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c6582-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="c6582-118">Cuando seleccionan la nueva aplicación por primera vez, la aplicación se instala y está lista para su uso.</span><span class="sxs-lookup"><span data-stu-id="c6582-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="c6582-119">Para las aplicaciones publicadas, la aplicación no aparece en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c6582-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="c6582-120">Solo está disponible para que el usuario final la instale mediante **Agregar o quitar programas** en el **Panel de control** o al abrir un archivo asociado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c6582-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="c6582-121">También puede usar la Directiva de grupo y los objetos de directiva de grupo de la misma manera para quitar aplicaciones del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6582-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="c6582-122">Para obtener más información acerca de cómo agregar y quitar aplicaciones con la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="c6582-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="c6582-123">Agregar y quitar aplicaciones con un sistema ESD</span><span class="sxs-lookup"><span data-stu-id="c6582-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="c6582-124">Un sistema de distribución electrónica de software (ESD) está diseñado para implementar de forma eficaz software y otra información en muchos equipos diferentes a través de conexiones de red.</span><span class="sxs-lookup"><span data-stu-id="c6582-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="c6582-125">Si su organización usa un sistema ESD para implementar software, puede usarlo para agregar y quitar aplicaciones en áreas de trabajo de MED-V, de la misma manera que agrega y quita aplicaciones en equipos físicos.</span><span class="sxs-lookup"><span data-stu-id="c6582-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="c6582-126">Agregar y quitar aplicaciones con APP-V</span><span class="sxs-lookup"><span data-stu-id="c6582-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="c6582-127">Microsoft Application Virtualization (App-V) proporciona la capacidad administrativa de poner las aplicaciones a disposición de los equipos de los usuarios finales sin tener que instalar las aplicaciones directamente en esos equipos.</span><span class="sxs-lookup"><span data-stu-id="c6582-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="c6582-128">Es posible que desee usar MED-V y App-V conjuntamente si, por ejemplo, su organización tiene aplicaciones que ha secuenciado con App-V en Windows XP y la resecuenciación retrasa la migración a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6582-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="c6582-129">Puede usar MED-V junto con App-V para agregar y quitar aplicaciones virtuales en un área de trabajo de MED-V implementada.</span><span class="sxs-lookup"><span data-stu-id="c6582-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="c6582-130">Para administrar las aplicaciones de esta manera, primero debe instalar el agente de App-V en el sistema operativo invitado MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6582-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="c6582-131">Después, puede usar App-V en el área de trabajo de MED-V para agregar y quitar las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="c6582-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="c6582-132">Para obtener más información sobre cómo instalar y usar App-V, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="c6582-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="c6582-133">**Importante**  Las aplicaciones de App-V que publique en el área de trabajo MED-V tienen asociaciones de tipo de archivo que no se pueden redirigir desde el equipo host a la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="c6582-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="c6582-134">Sin embargo, el usuario final aún puede acceder a estos tipos de archivo haciendo clic en **archivo**y, a continuación, haciendo clic en **abrir** en la aplicación de App-V publicada.</span><span class="sxs-lookup"><span data-stu-id="c6582-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="c6582-135">Para forzar el redireccionamiento de esas asociaciones de tipo de archivo, consulte App-V para las asociaciones de tipos de archivo asignados escribiendo lo siguiente en un símbolo del sistema en la máquina virtual invitada: **sftmime/Query OBJ: tipo**.</span><span class="sxs-lookup"><span data-stu-id="c6582-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="c6582-136">A continuación, asigne esas asociaciones de tipos de archivo en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="c6582-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="c6582-137">Agregar y quitar aplicaciones en la imagen principal</span><span class="sxs-lookup"><span data-stu-id="c6582-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="c6582-138">Aunque no se considere un procedimiento recomendado por MED-V, puede Agregar y quitar aplicaciones directamente en la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="c6582-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="c6582-139">Después de agregar o quitar una aplicación, puede volver a implementar el área de trabajo de MED-V en su empresa, de la misma manera en que lo implementó originalmente.</span><span class="sxs-lookup"><span data-stu-id="c6582-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="c6582-140">Para obtener más información sobre cómo agregar o quitar aplicaciones en la imagen principal, consulte [instalar aplicaciones en una imagen de Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md).</span><span class="sxs-lookup"><span data-stu-id="c6582-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="c6582-141">**Importante**  No se recomienda este método de administración de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6582-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="c6582-142">Si agrega o quita aplicaciones en la imagen principal y vuelve a implementar el área de trabajo de MED-V en su empresa, la configuración debe volver a ejecutarse y todos los datos guardados en la máquina virtual se perderán.</span><span class="sxs-lookup"><span data-stu-id="c6582-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="c6582-143">**Nota:**  Aunque una aplicación se instala en un área de trabajo de MED-V, también es posible que tenga que publicar la aplicación antes de que esté disponible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="c6582-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="c6582-144">Por ejemplo, es posible que tenga que publicar una aplicación instalada si la instalación no ha creado automáticamente un acceso directo en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c6582-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="c6582-145">Del mismo modo, para anular la publicación de una aplicación, es posible que tenga que quitar manualmente un acceso directo del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="c6582-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="c6582-146">De forma predeterminada, la mayoría de las aplicaciones se publican en el momento en que se instalan, cuando los accesos directos se crean y se habilitan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c6582-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="c6582-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6582-147">Related topics</span></span>


[<span data-ttu-id="c6582-148">Cómo probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6582-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="c6582-149">Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c6582-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





