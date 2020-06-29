---
title: Restaurar el archivo desde una copia de seguridad
description: Restaurar el archivo desde una copia de seguridad
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818400"
---
# <span data-ttu-id="275c5-103">Restaurar el archivo desde una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="275c5-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="275c5-104">Si se produce un desastre y el archivo de administración de directivas de grupo (AGPM) avanzada está dañado o destruido, un administrador AGPM (control total) puede restaurar el archivo desde una copia de seguridad preparada por adelantado y, a continuación, importar desde el entorno de producción del dominio cualquier objeto de directiva de grupo (GPO) que no esté en el archivo o cuya versión en producción sea más actual</span><span class="sxs-lookup"><span data-stu-id="275c5-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment of the domain any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="275c5-105">Para obtener información sobre cómo restaurar una copia de seguridad de archivo en un servidor diferente, vea [mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="275c5-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

<span data-ttu-id="275c5-106">Para completar este procedimiento, se necesita una cuenta de usuario que tenga acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y a la carpeta que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="275c5-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="275c5-107">Para restaurar el archivo a partir de una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="275c5-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="275c5-108">Detenga el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="275c5-108">Stop the AGPM Service.</span></span> <span data-ttu-id="275c5-109">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="275c5-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="275c5-110">Quitar el archivo existente.</span><span class="sxs-lookup"><span data-stu-id="275c5-110">Remove the existing archive.</span></span> <span data-ttu-id="275c5-111">De forma predeterminada, la carpeta de archivo es%ProgramData%\\Microsoft\\AGPM, pero es posible que el administrador AGPM que instaló Microsoft Advanced Group Policy Management-Server haya introducido una ubicación diferente durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="275c5-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="275c5-112">Vuelva a crear la carpeta de archivo mediante la configuración de la ruta de archivo, la cuenta del servicio AGPM, el propietario del archivo y el puerto de escucha.</span><span class="sxs-lookup"><span data-stu-id="275c5-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="275c5-113">No es necesario usar los mismos valores que se usan en la instalación original.</span><span class="sxs-lookup"><span data-stu-id="275c5-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="275c5-114">Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="275c5-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

4.  <span data-ttu-id="275c5-115">Copie el contenido de la copia de seguridad archivada en la carpeta archivo, copie las subcarpetas y archivos para asegurarse de que cada subcarpeta y archivo heredan los permisos de la carpeta archivo.</span><span class="sxs-lookup"><span data-stu-id="275c5-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="275c5-116">Tenga cuidado de no sobrescribir la carpeta de archivo.</span><span class="sxs-lookup"><span data-stu-id="275c5-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="275c5-117">Si no está seguro de si un GPO en la copia de seguridad de archivo es más reciente que la copia de ese GPO en producción, genere un informe de diferencias y compare su configuración.</span><span class="sxs-lookup"><span data-stu-id="275c5-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="275c5-118">Para obtener más información, consulte [identificar diferencias entre objetos de directiva de grupo, versiones de GPO o plantillas](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="275c5-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).</span></span>

6.  <span data-ttu-id="275c5-119">Reinicie el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="275c5-119">Restart the AGPM Service.</span></span> <span data-ttu-id="275c5-120">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="275c5-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

### <span data-ttu-id="275c5-121">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="275c5-121">Additional references</span></span>

-   [<span data-ttu-id="275c5-122">Copia de seguridad del archivo</span><span class="sxs-lookup"><span data-stu-id="275c5-122">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="275c5-123">Mover el servidor AGPM y el archivo</span><span class="sxs-lookup"><span data-stu-id="275c5-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="275c5-124">Administración del archivo</span><span class="sxs-lookup"><span data-stu-id="275c5-124">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





