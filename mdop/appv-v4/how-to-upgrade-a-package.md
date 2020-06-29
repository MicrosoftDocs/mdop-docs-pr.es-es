---
title: Cómo actualizar un paquete
description: Cómo actualizar un paquete
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816501"
---
# <span data-ttu-id="b4c16-103">Cómo actualizar un paquete</span><span class="sxs-lookup"><span data-stu-id="b4c16-103">How to Upgrade a Package</span></span>


<span data-ttu-id="b4c16-104">El proceso de actualización automática es el mismo que para agregar una versión de paquete en la consola de administración de Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="b4c16-104">The process for an automatic upgrade is the same as for adding a package version in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="b4c16-105">Una actualización automática se realiza al reordenar la aplicación en un paquete existente.</span><span class="sxs-lookup"><span data-stu-id="b4c16-105">An automatic upgrade is performed when you resequence the application in an existing package.</span></span> <span data-ttu-id="b4c16-106">Después, puede Agregar esta nueva versión a los servidores para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="b4c16-106">Then you can add this new version to your servers for streaming.</span></span>

<span data-ttu-id="b4c16-107">Cuando actualiza un paquete con una nueva versión, puede dejar la versión existente en contexto o eliminarla y dejar solo la más reciente.</span><span class="sxs-lookup"><span data-stu-id="b4c16-107">When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="b4c16-108">Es posible que desee dejar la versión anterior vigente para la compatibilidad con documentos heredados o bien, puede probar la nueva versión antes de ponerla a disposición de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b4c16-108">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

**<span data-ttu-id="b4c16-109">Para actualizar un paquete automáticamente</span><span class="sxs-lookup"><span data-stu-id="b4c16-109">To upgrade a package automatically</span></span>**

1.  <span data-ttu-id="b4c16-110">Copie el nuevo archivo SFT a la carpeta de contenido del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b4c16-110">Copy the new SFT file to the Application Virtualization Server's content folder.</span></span>

    <span data-ttu-id="b4c16-111">**Nota:**  Si la resecuenciación no agrega características que hayan cambiado los archivos descriptor de software abierto (OSD), icono (ICO) o proyecto SPRJ (SPRJ), no es necesario copiarlos.</span><span class="sxs-lookup"><span data-stu-id="b4c16-111">**Note** If resequencing did not add features that changed the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="b4c16-112">Puede incluir estos archivos si desea que todos estos archivos muestren la misma fecha.</span><span class="sxs-lookup"><span data-stu-id="b4c16-112">You can include these files if you want all these files to display the same date.</span></span>

     

2.  <span data-ttu-id="b4c16-113">En el panel izquierdo de la consola de administración de Application Virtualization Server, expanda **Packages**.</span><span class="sxs-lookup"><span data-stu-id="b4c16-113">In left pane of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

3.  <span data-ttu-id="b4c16-114">Haga clic con el botón derecho en el paquete que desea actualizar y seleccione **Agregar versión**.</span><span class="sxs-lookup"><span data-stu-id="b4c16-114">Right-click the package you want to upgrade, and select **Add Version**.</span></span>

4.  <span data-ttu-id="b4c16-115">En el cuadro de diálogo **Agregar versión de paquete** , busque o escriba el nombre completo de la ruta de acceso para la nueva versión de la aplicación en la **ruta de acceso completa del campo de archivo** .</span><span class="sxs-lookup"><span data-stu-id="b4c16-115">In the **Add Package Version** dialog box, browse for or type the full path name for the new application version in the **Full Path for the file** field.</span></span> <span data-ttu-id="b4c16-116">Debe ser un archivo de SFT.</span><span class="sxs-lookup"><span data-stu-id="b4c16-116">This must be an SFT file.</span></span>

5.  <span data-ttu-id="b4c16-117">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b4c16-117">Click **Next**.</span></span>

6.  <span data-ttu-id="b4c16-118">El cuadro de diálogo **Resumen** muestra la ubicación del archivo y le pide que copie el archivo allí si aún no lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="b4c16-118">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="b4c16-119">Haga clic en **Finalizar** una vez que haya verificado la información.</span><span class="sxs-lookup"><span data-stu-id="b4c16-119">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="b4c16-120">La nueva versión ya está completa y lista para transmitirse.</span><span class="sxs-lookup"><span data-stu-id="b4c16-120">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="b4c16-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4c16-121">Related topics</span></span>


[<span data-ttu-id="b4c16-122">Cómo administrar paquetes en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="b4c16-122">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





