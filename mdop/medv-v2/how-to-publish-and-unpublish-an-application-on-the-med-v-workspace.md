---
title: Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V
description: Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826921"
---
# <span data-ttu-id="e2e29-103">Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e2e29-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="e2e29-104">Aunque una aplicación se instala en un área de trabajo de MED-V, también es posible que tenga que publicar la aplicación antes de que esté disponible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="e2e29-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="e2e29-105">De forma predeterminada, la mayoría de las aplicaciones se publican en el momento en que se instalan y se habilitan los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="e2e29-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="e2e29-106">En algunos casos, es posible que desee instalar aplicaciones en el área de trabajo de MED-V sin que estén disponibles para el usuario final, por ejemplo, software de detección de virus.</span><span class="sxs-lookup"><span data-stu-id="e2e29-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="e2e29-107">De forma similar, hay ocasiones en las que desea publicar una aplicación instalada en el área de trabajo de MED-V que antes no estaba disponible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="e2e29-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="e2e29-108">Por ejemplo, es posible que tenga que publicar una aplicación instalada si la instalación no ha creado automáticamente un acceso directo en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="e2e29-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="e2e29-109">**Importante**  Si publica una aplicación que no admite rutas de acceso UNC, le recomendamos que asigne la aplicación a una unidad.</span><span class="sxs-lookup"><span data-stu-id="e2e29-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="e2e29-110">Puede publicar o anular la publicación de aplicaciones en un área de trabajo de MED-V implementada realizando una de las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="e2e29-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="e2e29-111">Para publicar o anular la publicación de una aplicación instalada</span><span class="sxs-lookup"><span data-stu-id="e2e29-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="e2e29-112">Para publicar una aplicación en un área de trabajo de MED-V implementada, copie un acceso directo para esa aplicación en la siguiente carpeta de la máquina virtual:</span><span class="sxs-lookup"><span data-stu-id="e2e29-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="e2e29-113">Menú Users\\Start de C:\\Documents and Settings\\All</span><span class="sxs-lookup"><span data-stu-id="e2e29-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="e2e29-114">Si es necesario, use una directiva de grupo o un sistema ESD para implementar una secuencia de comandos que copie el acceso directo de esa aplicación a la carpeta del menú todos los Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="e2e29-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="e2e29-115">Para anular la publicación de una aplicación en un área de trabajo de MED-V implementada, elimine el acceso directo de la aplicación en la siguiente carpeta de la máquina virtual:</span><span class="sxs-lookup"><span data-stu-id="e2e29-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="e2e29-116">Menú Users\\Start de C:\\Documents and Settings\\All</span><span class="sxs-lookup"><span data-stu-id="e2e29-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="e2e29-117">Si es necesario, use una directiva de grupo o un sistema ESD para implementar una secuencia de comandos que elimine el acceso directo de la aplicación en la carpeta del menú todos los Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="e2e29-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="e2e29-118">**Nota:**  Con frecuencia, el acceso directo se elimina automáticamente del menú **Inicio** del equipo host al desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2e29-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="e2e29-119">Sin embargo, en algunos casos, como para un área de trabajo de MED-V que está configurada para todos los usuarios de un equipo compartido, es posible que tenga que eliminar manualmente el acceso directo en el menú **Inicio** después de desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2e29-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="e2e29-120">El usuario final puede hacerlo haciendo clic con el botón secundario del ratón en el acceso directo y seleccionando **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="e2e29-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="e2e29-121">Para comprobar que la aplicación se ha publicado o no se ha publicado, compruebe en el área de trabajo de MED-V si el método abreviado correspondiente está disponible o no.</span><span class="sxs-lookup"><span data-stu-id="e2e29-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="e2e29-122">**Nota:**  Las aplicaciones que se incluyen en Windows XP SP3 y que se encuentran en la carpeta del menú Inicio de la máquina virtual no se publican automáticamente en el host.</span><span class="sxs-lookup"><span data-stu-id="e2e29-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="e2e29-123">Se controlan mediante la configuración del registro que bloquea la publicación automática.</span><span class="sxs-lookup"><span data-stu-id="e2e29-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="e2e29-124">Para obtener más información, vea [lista de exclusión de aplicaciones de Virtual PC de Windows](windows-virtual-pc-application-exclude-list.md).</span><span class="sxs-lookup"><span data-stu-id="e2e29-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="e2e29-125">Para publicar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="e2e29-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="e2e29-126">Cree un acceso directo en la máquina virtual en la que el destino sea el nombre del elemento, como C:\\WINDOWS\\system32\\appwiz.cpl.</span><span class="sxs-lookup"><span data-stu-id="e2e29-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="e2e29-127">El acceso directo debe crearse o moverse a la carpeta "%ALLUSERSPROFILE%\\Start Menu\\" o a una de sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="e2e29-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="e2e29-128">El elemento se publicará en el equipo host, en la ubicación correspondiente, en la carpeta del menú Inicio del host.</span><span class="sxs-lookup"><span data-stu-id="e2e29-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="e2e29-129">Inicie el acceso directo para el elemento en el host.</span><span class="sxs-lookup"><span data-stu-id="e2e29-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="e2e29-130">**PRECAUCIÓN**  Cuando cree el acceso directo, no especifique% SystemRoot% \\control.exe.</span><span class="sxs-lookup"><span data-stu-id="e2e29-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="e2e29-131">Esta aplicación no se publicará porque está incluida en la configuración del registro que bloquea la publicación automática.</span><span class="sxs-lookup"><span data-stu-id="e2e29-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="e2e29-132">Cómo controla MED-V la publicación automática de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e2e29-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="e2e29-133">Durante la publicación de la aplicación, MED-V copia los accesos directos de la máquina virtual invitada en el equipo host al intentar coincidir con la jerarquía de carpetas que existe en el invitado.</span><span class="sxs-lookup"><span data-stu-id="e2e29-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="e2e29-134">Al hacerlo, MED-V copia los accesos directos del invitado en el host siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="e2e29-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="e2e29-135">MED-V intenta localizar una carpeta en Start Menu\\Programs en el equipo host que tiene el mismo nombre que la carpeta del invitado donde se encuentra el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="e2e29-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="e2e29-136">Si no hay ninguna carpeta coincidente, MED-V intenta encontrar una carpeta en la carpeta del menú Inicio del host que tiene el mismo nombre que la carpeta del invitado donde se encuentra el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="e2e29-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="e2e29-137">Si no hay ninguna carpeta coincidente, MED-V copia el acceso directo a la carpeta predeterminada del host, la carpeta Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="e2e29-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="e2e29-138">Ejemplo de proceso de publicación de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="e2e29-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="e2e29-139">Si un acceso directo de la aplicación se publica en la carpeta Start Menu\\Programs\\AppShortcuts en el invitado, MED-V busca en el equipo anfitrión una carpeta Start Menu\\Programs\\ AppShortcuts y, si la encuentra, copia el acceso directo a esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="e2e29-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="e2e29-140">Si no se encuentra la carpeta, MED-V busca en el equipo anfitrión una carpeta Start Menu\\AppShortcuts y, si la encuentra, copia el acceso directo a esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="e2e29-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="e2e29-141">Si no se encuentra la carpeta, MED-V copia el acceso directo a la carpeta Inicio de Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="e2e29-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="e2e29-142">**Nota:**  Ya debe existir una carpeta en la carpeta del menú Inicio del equipo host para MED-V para copiar el acceso directo allí.</span><span class="sxs-lookup"><span data-stu-id="e2e29-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="e2e29-143">MED-V no crea la carpeta si aún no existe.</span><span class="sxs-lookup"><span data-stu-id="e2e29-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="e2e29-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2e29-144">Related topics</span></span>


[<span data-ttu-id="e2e29-145">Instalar y quitar una aplicación en el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e2e29-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="e2e29-146">Administrar las actualizaciones de Software para áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e2e29-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="e2e29-147">Lista de exclusión de aplicación de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e2e29-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 





