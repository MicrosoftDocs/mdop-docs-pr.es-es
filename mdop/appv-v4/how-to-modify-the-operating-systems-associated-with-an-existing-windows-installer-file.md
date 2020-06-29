---
title: Cómo modificar los sistemas operativos asociados con un archivo de instalador de Windows existente
description: Cómo modificar los sistemas operativos asociados con un archivo de instalador de Windows existente
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816951"
---
# <span data-ttu-id="c08ab-103">Cómo modificar los sistemas operativos asociados con un archivo de instalador de Windows existente</span><span class="sxs-lookup"><span data-stu-id="c08ab-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="c08ab-104">Use el siguiente procedimiento para modificar las versiones del sistema operativo asociadas a un archivo existente de Windows Installer (**MSI**) que se creó con el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="c08ab-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="c08ab-105">Para modificar los sistemas operativos de un archivo de Windows Installer existente</span><span class="sxs-lookup"><span data-stu-id="c08ab-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="c08ab-106">Instale el secuenciador de App-V en un equipo de su entorno que solo tenga instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c08ab-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="c08ab-107">Como alternativa, puede instalar el secuenciador en un equipo que ejecute un entorno virtual, por ejemplo, Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c08ab-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="c08ab-108">Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que puede reutilizar con una configuración adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="c08ab-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="c08ab-109">Para obtener más información sobre cómo instalar el secuenciador de App-V, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="c08ab-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="c08ab-110">Copie el paquete de la aplicación virtual completo que contiene el archivo de Windows Installer que desea modificar al equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="c08ab-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="c08ab-111">Para modificar el archivo de Windows Installer, abra la consola del secuenciador, seleccione **paquete**  /  **abierto**y, a continuación, vaya a la ubicación donde se guardó el paquete de aplicación virtual asociado con el archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c08ab-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="c08ab-112">Para agregar o quitar sistemas operativos, seleccione la ficha **implementación** en la consola del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="c08ab-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="c08ab-113">Para especificar sistemas operativos adicionales que se asociarán con el archivo de Windows Installer, seleccione el sistema operativo que desee y, a continuación, haga clic en la flecha que apunta al control de lista del sistema operativo **seleccionado** .</span><span class="sxs-lookup"><span data-stu-id="c08ab-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="c08ab-114">Para quitar una asociación de sistema operativo, seleccione el sistema operativo que desee quitar y, a continuación, haga clic en la flecha que apunta al control de lista de sistema operativo **disponible** .</span><span class="sxs-lookup"><span data-stu-id="c08ab-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="c08ab-115">Para crear un nuevo Windows Installer que se asociará con el paquete de la aplicación virtual, seleccione **generar paquete de Microsoft Windows Installer (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="c08ab-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="c08ab-116">También puede seleccionar **herramientas**para  /  **crear MSI**.</span><span class="sxs-lookup"><span data-stu-id="c08ab-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="c08ab-117">**Nota:**  Si selecciona **herramientas** / **crear MSI** para crear un nuevo archivo de Windows Installer, puede omitir el **paso 6** de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c08ab-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="c08ab-118">Para guardar el paquete de aplicación virtual, **Package**seleccione  /  **Guardar**paquete.</span><span class="sxs-lookup"><span data-stu-id="c08ab-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="c08ab-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c08ab-119">Related topics</span></span>


[<span data-ttu-id="c08ab-120">Tareas del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c08ab-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





