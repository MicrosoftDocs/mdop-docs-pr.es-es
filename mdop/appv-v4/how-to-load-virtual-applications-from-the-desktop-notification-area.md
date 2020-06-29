---
title: Cómo cargar aplicaciones virtuales desde el área de notificación de escritorio
description: Cómo cargar aplicaciones virtuales desde el área de notificación de escritorio
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817220"
---
# <span data-ttu-id="9cff4-103">Cómo cargar aplicaciones virtuales desde el área de notificación de escritorio</span><span class="sxs-lookup"><span data-stu-id="9cff4-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="9cff4-104">Si es un usuario móvil, es posible que desee cargar completamente las aplicaciones en la caché para usarlas durante la operación de desconexión o el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9cff4-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="9cff4-105">Para transmitir aplicaciones desde el servidor de Application Virtualization (App-V) o el servidor de streaming de Application Virtualization (App-V), debe estar conectado a un servidor para cargar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9cff4-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="9cff4-106">Si no está conectado al servidor cuando intenta cargar aplicaciones, el sistema generará un mensaje de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="9cff4-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="9cff4-107">También puede transmitir aplicaciones al cliente desde un archivo o un disco.</span><span class="sxs-lookup"><span data-stu-id="9cff4-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="9cff4-108">Las aplicaciones se cargan en una aplicación cada vez.</span><span class="sxs-lookup"><span data-stu-id="9cff4-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="9cff4-109">La barra de progreso muestra el nombre de la aplicación, el porcentaje de aplicación cargada y el número de aplicaciones ya procesadas comparada con el número total de aplicaciones puestas en cola.</span><span class="sxs-lookup"><span data-stu-id="9cff4-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="9cff4-110">Puede omitir cualquier aplicación en curso antes de que se cargue el 100%.</span><span class="sxs-lookup"><span data-stu-id="9cff4-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="9cff4-111">También puede omitir la carga de todas las aplicaciones restantes.</span><span class="sxs-lookup"><span data-stu-id="9cff4-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="9cff4-112">**Nota:**  Si el sistema encuentra un error al cargar una aplicación, se le informa del error.</span><span class="sxs-lookup"><span data-stu-id="9cff4-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="9cff4-113">Debe cerrar el cuadro de diálogo de error antes de cargar la siguiente aplicación.</span><span class="sxs-lookup"><span data-stu-id="9cff4-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="9cff4-114">Para cargar todas las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cff4-114">To load all applications</span></span>**

1.  <span data-ttu-id="9cff4-115">Haga clic con el botón derecho en el icono del sistema de virtualización de aplicaciones en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="9cff4-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="9cff4-116">Seleccione **cargar aplicaciones** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="9cff4-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="9cff4-117">Para omitir aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cff4-117">To skip applications</span></span>**

1.  <span data-ttu-id="9cff4-118">Haga clic en la barra de progreso para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9cff4-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="9cff4-119">Seleccione uno de los siguientes botones para obtener los resultados deseados:</span><span class="sxs-lookup"><span data-stu-id="9cff4-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="9cff4-120">**Omitir**: para omitir la aplicación que se está cargando en ese momento.</span><span class="sxs-lookup"><span data-stu-id="9cff4-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="9cff4-121">**Omitir todas**: para omitir todas las aplicaciones restantes.</span><span class="sxs-lookup"><span data-stu-id="9cff4-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="9cff4-122">**Continuar**: para cancelar el cuadro de diálogo y continuar con la carga de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9cff4-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="9cff4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9cff4-123">Related topics</span></span>


[<span data-ttu-id="9cff4-124">Cómo usar el área de notificación de escritorio para la administración del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cff4-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





