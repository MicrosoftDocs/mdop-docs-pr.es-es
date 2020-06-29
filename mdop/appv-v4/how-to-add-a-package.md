---
title: Cómo agregar un paquete
description: Cómo agregar un paquete
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821400"
---
# <span data-ttu-id="32062-103">Cómo agregar un paquete</span><span class="sxs-lookup"><span data-stu-id="32062-103">How to Add a Package</span></span>


<span data-ttu-id="32062-104">Puede Agregar un paquete desde la consola de administración de Application Virtualization Server de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="32062-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="32062-105">Importar una aplicación, que crea el paquete automáticamente en el proceso.</span><span class="sxs-lookup"><span data-stu-id="32062-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="32062-106">Agregar un paquete de forma manual.</span><span class="sxs-lookup"><span data-stu-id="32062-106">Add a package manually.</span></span>

<span data-ttu-id="32062-107">Se recomienda importar aplicaciones en lugar de agregarlas manualmente.</span><span class="sxs-lookup"><span data-stu-id="32062-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="32062-108">Para obtener más información sobre cómo importar aplicaciones, vea [Cómo importar una aplicación](how-to-import-an-applicationserver.md).</span><span class="sxs-lookup"><span data-stu-id="32062-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="32062-109">Para agregar un paquete de forma manual</span><span class="sxs-lookup"><span data-stu-id="32062-109">To add a package manually</span></span>**

1.  <span data-ttu-id="32062-110">En la consola de administración de Application Virtualization Server, haga clic con el botón derecho en el nodo **paquetes** en el panel izquierdo y elija **nuevo paquete**.</span><span class="sxs-lookup"><span data-stu-id="32062-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="32062-111">En el cuadro de diálogo **nuevo paquete** , escriba un nombre en el campo **nombre del paquete** .</span><span class="sxs-lookup"><span data-stu-id="32062-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="32062-112">Busque o escriba un nombre de ruta en el campo **ruta de acceso completa del archivo de paquete** .</span><span class="sxs-lookup"><span data-stu-id="32062-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="32062-113">Debe ser un archivo de SFT.</span><span class="sxs-lookup"><span data-stu-id="32062-113">This must be an SFT file.</span></span>

    <span data-ttu-id="32062-114">**Nota:**  Si busca el archivo SFT, reemplace la ruta de acceso local (como C:\\Archivos de Files\\User\ _Apps \\Virtual\ _App \ _Server \\content) con el nombre de host estático o la dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="32062-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="32062-115">El uso de la variable *% SFT \ _SOFTGRIDSERVER%* requiere la configuración del equipo por cliente.</span><span class="sxs-lookup"><span data-stu-id="32062-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="32062-116">En los cuadros de diálogo que hacen referencia a servidores de aplicaciones virtuales, debe usar una ubicación de red, como el nombre de host estático del servidor o la dirección IP a la que los usuarios pueden tener acceso.</span><span class="sxs-lookup"><span data-stu-id="32062-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="32062-117">El archivo descriptor de software abierto (OSD) de la aplicación puede reemplazar la variable de marcador de posición *% SFT \ _SOFTGRIDSERER%* por la dirección IP o el nombre de host estático del servidor.</span><span class="sxs-lookup"><span data-stu-id="32062-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="32062-118">Si deja la variable de marcador de posición, debe establecer esta variable en cada equipo cliente que tenga acceso a ese servidor.</span><span class="sxs-lookup"><span data-stu-id="32062-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="32062-119">Establezca una variable de usuario o de sistema en cada equipo para SFT \ _SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="32062-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="32062-120">El valor de la variable debe ser el nombre de host estático o la dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="32062-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="32062-121">Si establece una variable, salga de la sesión del cliente, cierre la sesión y vuelva a usar Microsoft Windows y, a continuación, reinicie la sesión en cada equipo en el que se haya realizado una sesión y que haya establecido la variable.</span><span class="sxs-lookup"><span data-stu-id="32062-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="32062-122">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="32062-122">Click **Next**.</span></span>

5.  <span data-ttu-id="32062-123">El cuadro de diálogo **Resumen** muestra la ubicación del archivo y le pide que copie el archivo en la ubicación si todavía no lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="32062-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="32062-124">Haga clic en **Finalizar** una vez que haya verificado la información.</span><span class="sxs-lookup"><span data-stu-id="32062-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="32062-125">**Nota:**  Si está administrando aplicaciones en un servidor remoto, en el siguiente cuadro de diálogo, escriba solo la ruta de acceso del archivo relativa a la raíz de contenido del servidor.</span><span class="sxs-lookup"><span data-stu-id="32062-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="32062-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32062-126">Related topics</span></span>


[<span data-ttu-id="32062-127">Cómo importar una aplicación</span><span class="sxs-lookup"><span data-stu-id="32062-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="32062-128">Cómo administrar paquetes en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="32062-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





