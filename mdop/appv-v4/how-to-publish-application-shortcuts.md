---
title: Cómo publicar accesos directos de aplicación
description: Cómo publicar accesos directos de aplicación
author: dansimp
ms.assetid: fc5efe86-1bbe-438b-b7d8-4f9b815cc58e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eafdb85414a1a6cf3e1072fdc5532bcd04699653
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816841"
---
# <span data-ttu-id="fc58a-103">Cómo publicar accesos directos de aplicación</span><span class="sxs-lookup"><span data-stu-id="fc58a-103">How to Publish Application Shortcuts</span></span>


<span data-ttu-id="fc58a-104">Puede usar el procedimiento siguiente para publicar accesos directos a una aplicación directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fc58a-104">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="fc58a-105">Para publicar accesos directos a aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fc58a-105">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="fc58a-106">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **nuevo acceso directo** en el menú emergente para mostrar el Asistente para nuevo acceso directo.</span><span class="sxs-lookup"><span data-stu-id="fc58a-106">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="fc58a-107">En la primera página del Asistente para crear accesos directos, seleccione un icono y especifique un nombre para el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="fc58a-107">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="fc58a-108">**Cambiar icono**: muestra un explorador de iconos estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc58a-108">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="fc58a-109">Busque y seleccione el icono que quiera.</span><span class="sxs-lookup"><span data-stu-id="fc58a-109">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="fc58a-110">**Título del acceso directo**: escriba el nombre que desea asignar al acceso directo.</span><span class="sxs-lookup"><span data-stu-id="fc58a-110">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="fc58a-111">El valor predeterminado de este campo es el nombre y la versión existentes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc58a-111">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="fc58a-112">En la segunda página del asistente, determine la ubicación del acceso directo publicado.</span><span class="sxs-lookup"><span data-stu-id="fc58a-112">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="fc58a-113">**El escritorio**: Seleccione esta casilla para publicar el acceso directo en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="fc58a-113">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="fc58a-114">**La barra de herramientas de inicio rápido**: Seleccione esta casilla para publicar el acceso directo en la barra de herramientas Inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="fc58a-114">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="fc58a-115">**El menú enviar a**: Seleccione esta casilla para publicar el acceso directo en el menú **Enviar a** .</span><span class="sxs-lookup"><span data-stu-id="fc58a-115">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="fc58a-116">**Programas en el menú Inicio**: cuando se activa la casilla de verificación **menú Inicio** , este campo se activa.</span><span class="sxs-lookup"><span data-stu-id="fc58a-116">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="fc58a-117">Deje este campo en blanco para publicar el acceso directo directamente en la raíz de la carpeta programas o escriba un nombre de carpeta o jerarquía, por ejemplo, "My \ _Computer aplicaciones \\Office".</span><span class="sxs-lookup"><span data-stu-id="fc58a-117">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="fc58a-118">Los accesos directos creados de esta manera solo están disponibles para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="fc58a-118">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="fc58a-119">**Otra ubicación** y botón **examinar** : al seleccionar la casilla **otra ubicación** , este campo se activa.</span><span class="sxs-lookup"><span data-stu-id="fc58a-119">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="fc58a-120">Escriba cualquier ubicación válida en el equipo o cualquier ruta UNC disponible (archivo o directorio compartido en una red).</span><span class="sxs-lookup"><span data-stu-id="fc58a-120">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="fc58a-121">El botón **examinar** muestra un cuadro de diálogo estándar de **apertura de archivo** de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc58a-121">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="fc58a-122">En la tercera página del asistente, escriba los parámetros de la línea de comandos que desee.</span><span class="sxs-lookup"><span data-stu-id="fc58a-122">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="fc58a-123">Haga clic en **Finalizar** para publicar los métodos abreviados y salir en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="fc58a-123">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="fc58a-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc58a-124">Related topics</span></span>


[<span data-ttu-id="fc58a-125">Cómo agregar una asociación de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="fc58a-125">How to Add a File Type Association</span></span>](how-to-add-a-file-type-association.md)

[<span data-ttu-id="fc58a-126">Cómo agregar una aplicación</span><span class="sxs-lookup"><span data-stu-id="fc58a-126">How to Add an Application</span></span>](how-to-add-an-application.md)

[<span data-ttu-id="fc58a-127">Cómo eliminar una asociación de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="fc58a-127">How to Delete a File Type Association</span></span>](how-to-delete-a-file-type-association.md)

 

 





