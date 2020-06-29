---
title: Copia de seguridad del archivo
description: Copia de seguridad del archivo
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819210"
---
# <span data-ttu-id="cc0d5-103">Copia de seguridad del archivo</span><span class="sxs-lookup"><span data-stu-id="cc0d5-103">Back Up the Archive</span></span>


<span data-ttu-id="cc0d5-104">Para ayudar en la recuperación del archivo para administración de directivas de grupo (AGPM) avanzada si se produce un desastre, un administrador de AGPM (control total) debe realizar una copia de seguridad del archivo con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="cc0d5-105">De forma predeterminada, el archivo se crea en%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="cc0d5-106">Sin embargo, puede especificar una ruta diferente durante la configuración de administración de directivas de grupo (servidor) avanzada de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="cc0d5-107">Para completar este procedimiento, se necesita una cuenta de usuario que tenga acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y a la carpeta que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="cc0d5-108">Para hacer una copia de seguridad del archivo</span><span class="sxs-lookup"><span data-stu-id="cc0d5-108">To back up the archive</span></span>**

1.  <span data-ttu-id="cc0d5-109">Detenga el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-109">Stop the AGPM Service.</span></span> <span data-ttu-id="cc0d5-110">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="cc0d5-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="cc0d5-111">Haga una copia de seguridad de la carpeta de archivo con el explorador de Windows, xcopy, Windows Server® copia de seguridad u otra herramienta de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="cc0d5-112">Asegúrese de hacer una copia de seguridad de los archivos ocultos, de sistema y de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="cc0d5-113">Almacene la copia de seguridad del archivo en un lugar seguro.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="cc0d5-114">Reinicie el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-114">Restart the AGPM Service.</span></span> <span data-ttu-id="cc0d5-115">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="cc0d5-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

<span data-ttu-id="cc0d5-116">**Nota:**  Si un administrador de AGPM realiza copias de seguridad del archivo con frecuencia, los objetos de directiva de grupo (GPO) de la copia de seguridad del archivo no estarán actualizados.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="cc0d5-117">Para asegurarse de que la copia de seguridad del archivo esté actualizada, haga una copia de seguridad del archivo como parte de la estrategia de copia de seguridad diaria de su organización.</span><span class="sxs-lookup"><span data-stu-id="cc0d5-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="cc0d5-118">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="cc0d5-118">Additional references</span></span>

-   [<span data-ttu-id="cc0d5-119">Restaurar el archivo desde una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="cc0d5-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup.md)

-   [<span data-ttu-id="cc0d5-120">Mover el servidor AGPM y el archivo</span><span class="sxs-lookup"><span data-stu-id="cc0d5-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="cc0d5-121">Administración del archivo</span><span class="sxs-lookup"><span data-stu-id="cc0d5-121">Managing the Archive</span></span>](managing-the-archive.md)

 

 





