---
title: Lista de exclusión de aplicación de Windows Virtual PC
description: Lista de exclusión de aplicación de Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823691"
---
# <span data-ttu-id="3edc7-103">Lista de exclusión de aplicación de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3edc7-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="3edc7-104">En algunos casos, es posible que no desee que las aplicaciones instaladas en el área de trabajo de MED-V se publiquen en el menú **Inicio** del equipo host.</span><span class="sxs-lookup"><span data-stu-id="3edc7-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="3edc7-105">Puede anular la publicación de estas aplicaciones siguiendo las instrucciones [que encontrará en cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="3edc7-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="3edc7-106">Sin embargo, si el programa se actualiza de forma automática, también puede volver a publicarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3edc7-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="3edc7-107">Esto hace que tenga que volver a publicar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3edc7-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="3edc7-108">Windows Virtual PC incluye una característica que se denomina "lista de exclusión" que le permite especificar determinadas aplicaciones instaladas que no desea que se publiquen en el menú **Inicio** del host.</span><span class="sxs-lookup"><span data-stu-id="3edc7-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="3edc7-109">La "lista de exclusión" se encuentra en el registro de invitados de la clave HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList y enumera las aplicaciones que no se han publicado en el menú **Inicio** de host.</span><span class="sxs-lookup"><span data-stu-id="3edc7-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="3edc7-110">Puede pensar en la "lista de exclusión" como en el que se cancela la publicación de las aplicaciones especificadas de forma permanente porque todas las actualizaciones automáticas de las aplicaciones que aparecen en la lista no provocarán que se vuelvan a publicar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3edc7-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="3edc7-111">Administración de aplicaciones con la lista de exclusión en Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3edc7-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="3edc7-112">Abra el área de trabajo de MED-V en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="3edc7-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="3edc7-113">Para obtener información sobre cómo abrir el área de trabajo de MED-V en el modo de pantalla completa con el kit de herramientas de administración de MED-V, vea [Ver configuraciones de áreas de trabajo de Med-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span><span class="sxs-lookup"><span data-stu-id="3edc7-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="3edc7-114">O bien, puede abrirlo manualmente en pantalla completa haciendo clic en **Inicio**, haga clic en **todos los programas**, en **Windows Virtual PC**, en **Windows Virtual PC**y, a continuación, haga doble clic en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3edc7-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="3edc7-115">En la ventana del área de trabajo virtual de Windows, abra el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="3edc7-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="3edc7-116">Haga clic en **Inicio**, haga clic en **Ejecutar**y, a continuación, escriba regedit.</span><span class="sxs-lookup"><span data-stu-id="3edc7-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="3edc7-117">A continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3edc7-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="3edc7-118">En el editor del registro, busque la clave del registro HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="3edc7-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="3edc7-119">Cree un nuevo valor de registro para la aplicación instalada que no desea que se publique en el menú **Inicio** del equipo host.</span><span class="sxs-lookup"><span data-stu-id="3edc7-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="3edc7-120">Por ejemplo, si desea anular la publicación del programa publicado automáticamente, Microsoft Silverlight, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3edc7-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="3edc7-121">Con la clave de registro VPCVAppExcludeList resaltada, haga clic en **Editar**, en **nuevo**y, a continuación, en **valor de cadena**.</span><span class="sxs-lookup"><span data-stu-id="3edc7-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="3edc7-122">Escriba el nombre del nuevo valor del registro.</span><span class="sxs-lookup"><span data-stu-id="3edc7-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="3edc7-123">Por ejemplo, para Microsoft Silverlight, puede escribir sllauncher.exe.</span><span class="sxs-lookup"><span data-stu-id="3edc7-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="3edc7-124">Haga doble clic en el nuevo valor del registro y escriba los datos del valor.</span><span class="sxs-lookup"><span data-stu-id="3edc7-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="3edc7-125">Los datos del valor son la ruta de acceso completa del comando cuya publicación desea anular.</span><span class="sxs-lookup"><span data-stu-id="3edc7-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="3edc7-126">Puede encontrar la ruta completa haciendo clic con el botón secundario del mouse en el acceso directo en el menú **Inicio** de la aplicación que no desea publicar y, después, haciendo clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="3edc7-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="3edc7-127">La ruta completa se muestra en la pestaña **acceso directo** en **destino**.</span><span class="sxs-lookup"><span data-stu-id="3edc7-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="3edc7-128">Por ejemplo, para el programa Microsoft Silverlight, la ruta de acceso completa puede ser "C:\\Archivos de Programa\\microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe".</span><span class="sxs-lookup"><span data-stu-id="3edc7-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="3edc7-129">**Importante**  Si procede, quite las comillas de la ruta de acceso completa al introducirla en el campo valor de datos.</span><span class="sxs-lookup"><span data-stu-id="3edc7-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="3edc7-130">Cierre el editor del registro y reinicie la máquina virtual del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="3edc7-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="3edc7-131">La aplicación aún se instala en el área de trabajo de MED-V, pero ahora se ha quitado del menú **Inicio** del equipo host.</span><span class="sxs-lookup"><span data-stu-id="3edc7-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="3edc7-132">También puede volver a publicar una aplicación excluida en el menú de **Inicio** de host eliminando el valor correspondiente de la clave VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="3edc7-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="3edc7-133">Por ejemplo, para volver a publicar Microsoft Silverlight, haga clic con el botón derecho en el valor del registro sllauncher.exe y seleccione **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="3edc7-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="3edc7-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3edc7-134">Related topics</span></span>


[<span data-ttu-id="3edc7-135">Referencia técnica de MED-V</span><span class="sxs-lookup"><span data-stu-id="3edc7-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="3edc7-136">Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="3edc7-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





