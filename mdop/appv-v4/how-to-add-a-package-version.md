---
title: Cómo agregar una versión de paquete
description: Cómo agregar una versión de paquete
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821401"
---
# <span data-ttu-id="7f6a6-103">Cómo agregar una versión de paquete</span><span class="sxs-lookup"><span data-stu-id="7f6a6-103">How to Add a Package Version</span></span>


<span data-ttu-id="7f6a6-104">En la consola de administración de Application Virtualization Server, cuando reordene un paquete, puede usar el siguiente procedimiento para agregar la nueva versión a los servidores para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-104">In the Application Virtualization Server Management Console, when you resequence a package, you can use the following procedure to add the new version to your servers for streaming.</span></span>

<span data-ttu-id="7f6a6-105">**Nota:**  Cuando actualiza un paquete con una nueva versión, puede dejar la versión existente en contexto o eliminarla y dejar solo la más reciente.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-105">**Note** When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="7f6a6-106">Es posible que desee dejar la versión anterior vigente para la compatibilidad con documentos heredados o bien, puede probar la nueva versión antes de ponerla a disposición de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-106">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

 

**<span data-ttu-id="7f6a6-107">Para agregar una versión de paquete</span><span class="sxs-lookup"><span data-stu-id="7f6a6-107">To add a package version</span></span>**

1.  <span data-ttu-id="7f6a6-108">Copie el nuevo archivo SFT a la carpeta de contenido del servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-108">Copy the new SFT file to the application server's content folder.</span></span> <span data-ttu-id="7f6a6-109">Si la resecuenciación no ha agregado los cambios en los archivos del descriptor de software abierto (OSD), de icono (ICO) o del SPRJ (SPRJ), no es necesario que los copie.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-109">If resequencing did not add changes to the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="7f6a6-110">Puede incluir esos archivos si quiere que todos los archivos muestren la misma fecha.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-110">You can include those files if you want all the files to display the same date.</span></span>

2.  <span data-ttu-id="7f6a6-111">En el panel izquierdo de la consola de administración de Application Virtualization Server, expanda el nodo **paquetes** .</span><span class="sxs-lookup"><span data-stu-id="7f6a6-111">In left pane of the Application Virtualization Server Management Console, expand the **Packages** node.</span></span>

3.  <span data-ttu-id="7f6a6-112">Haga clic con el botón derecho en el paquete que quiera actualizar y elija **Agregar versión**.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-112">Right-click the package you want to upgrade, and choose **Add Version**.</span></span>

4.  <span data-ttu-id="7f6a6-113">En el cuadro de diálogo **Agregar versión del paquete** , busque o escriba el nombre de la ruta de acceso del nuevo archivo de aplicación en el campo **ruta de acceso completa del archivo de paquete** .</span><span class="sxs-lookup"><span data-stu-id="7f6a6-113">In the **Add Package Version** dialog box, browse for or type the path name for the new application file in the **Full path for package file** field.</span></span> <span data-ttu-id="7f6a6-114">Debe ser un archivo de SFT.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-114">This must be an SFT file.</span></span>

5.  <span data-ttu-id="7f6a6-115">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-115">Click **Next**.</span></span>

6.  <span data-ttu-id="7f6a6-116">El cuadro de diálogo **Resumen** muestra la ubicación del archivo y le pide que copie el archivo allí si aún no lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-116">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="7f6a6-117">Haga clic en **Finalizar** una vez que haya verificado la información.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-117">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="7f6a6-118">La nueva versión ya está completa y lista para transmitirse.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-118">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="7f6a6-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f6a6-119">Related topics</span></span>


[<span data-ttu-id="7f6a6-120">Cómo eliminar un paquete</span><span class="sxs-lookup"><span data-stu-id="7f6a6-120">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="7f6a6-121">Cómo administrar paquetes en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="7f6a6-121">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





