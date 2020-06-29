---
title: Cómo abrir una aplicación secuenciada mediante la línea de comandos
description: Cómo abrir una aplicación secuenciada mediante la línea de comandos
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816920"
---
# <span data-ttu-id="ab498-103">Cómo abrir una aplicación secuenciada mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ab498-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="ab498-104">Puede abrir paquetes de aplicaciones virtuales desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="ab498-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="ab498-105">Debe ejecutar el símbolo del sistema de **cmd** como administrador.</span><span class="sxs-lookup"><span data-stu-id="ab498-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="ab498-106">Use el procedimiento siguiente para abrir paquetes de aplicaciones secuenciales con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ab498-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="ab498-107">Para abrir una aplicación con secuencia mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ab498-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="ab498-108">Para abrir el símbolo del sistema, haga clic en **Inicio**, seleccione **Ejecutar**, escriba **cmd**y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ab498-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="ab498-109">En un símbolo del sistema, escriba **cd\\** y especifique la ruta de acceso al directorio donde está instalado el secuenciador y, a continuación, presione **entrar.**</span><span class="sxs-lookup"><span data-stu-id="ab498-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="ab498-110">En el símbolo del sistema, escriba el siguiente comando y reemplace el texto en cursiva con sus valores:</span><span class="sxs-lookup"><span data-stu-id="ab498-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="ab498-111">SFTSequencer/OPEN:*"especifica el archivo. SPRJ que se abrirá"*</span><span class="sxs-lookup"><span data-stu-id="ab498-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="ab498-112">Presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="ab498-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="ab498-113">También puede especificar los siguientes parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="ab498-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="ab498-114">En el símbolo del sistema, escriba los siguientes comandos y reemplace el texto en cursiva con sus valores:</span><span class="sxs-lookup"><span data-stu-id="ab498-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="ab498-115">/PACKAGENAME: "*especifica el nombre del paquete"*</span><span class="sxs-lookup"><span data-stu-id="ab498-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="ab498-116">/MSI: especifica la creación de un Microsoft Windows Installer asociado.</span><span class="sxs-lookup"><span data-stu-id="ab498-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="ab498-117">/COMPRESS: especifica si se comprimirá el paquete.</span><span class="sxs-lookup"><span data-stu-id="ab498-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="ab498-118">De forma predeterminada, los paquetes no se comprimen.</span><span class="sxs-lookup"><span data-stu-id="ab498-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="ab498-119">Presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="ab498-119">Press **Enter**.</span></span>

    <span data-ttu-id="ab498-120">**Nota:**  Si el instalador o el paquete de Windows Installer tiene una interfaz de usuario gráfica, se mostrará después de especificar los parámetros de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="ab498-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="ab498-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab498-121">Related topics</span></span>


[<span data-ttu-id="ab498-122">Cómo administrar aplicaciones virtuales con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ab498-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





