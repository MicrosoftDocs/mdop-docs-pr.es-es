---
title: Cómo actualizar un paquete mediante el comando Abrir paquete
description: Cómo actualizar un paquete mediante el comando Abrir paquete
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816520"
---
# <span data-ttu-id="5ac92-103">Cómo actualizar un paquete mediante el comando Abrir paquete</span><span class="sxs-lookup"><span data-stu-id="5ac92-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="5ac92-104">Use el comando abrir paquete para actualizar o aplicar una actualización a un paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5ac92-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="5ac92-105">Al actualizar un paquete de aplicaciones virtual existente mediante la línea de comandos, se elimina la versión original del archivo. SFT.</span><span class="sxs-lookup"><span data-stu-id="5ac92-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="5ac92-106">Debe realizar una copia de seguridad del archivo. SFT asociado antes de actualizar el paquete mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ac92-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="5ac92-107">Para actualizar un paquete con el comando abrir paquete</span><span class="sxs-lookup"><span data-stu-id="5ac92-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="5ac92-108">Para abrir el paquete que se actualizará, en la consola de Application Virtualization (App-V), seleccione **archivo**, **abrir paquete para la actualización**.</span><span class="sxs-lookup"><span data-stu-id="5ac92-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="5ac92-109">En el cuadro de diálogo **abrir** , seleccione el paquete que se actualizará.</span><span class="sxs-lookup"><span data-stu-id="5ac92-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="5ac92-110">Para iniciar el Asistente para **secuenciación** , seleccione **herramientas**, **Asistente para secuencias**.</span><span class="sxs-lookup"><span data-stu-id="5ac92-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="5ac92-111">Complete el asistente que aplica los cambios de configuración para guardar la nueva aplicación de secuencia, seleccione **archivo**, **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5ac92-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="5ac92-112">Para anexar el número de versión al nombre del paquete, en la consola del secuenciador, seleccione **herramientas**, **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="5ac92-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="5ac92-113">Seleccione **anexar versión del paquete al nombre de archivo**.</span><span class="sxs-lookup"><span data-stu-id="5ac92-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="5ac92-114">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5ac92-114">Click **OK**.</span></span>

    <span data-ttu-id="5ac92-115">**Importante**  La actualización del nombre de archivo con la versión del paquete es esencial para que la actualización se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ac92-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="5ac92-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ac92-116">Related topics</span></span>


[<span data-ttu-id="5ac92-117">Cómo administrar aplicaciones virtuales con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="5ac92-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





