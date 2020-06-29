---
title: Migración de paquetes de configuración de UE-V
description: Migración de paquetes de configuración de UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823210"
---
# <span data-ttu-id="01713-103">Migración de paquetes de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="01713-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="01713-104">En el ciclo de vida de una implementación de virtualización de Microsoft User Experience (UE-V), es posible que tenga que cambiar la ubicación de los paquetes de configuración de usuario al migrar a un nuevo servidor o con fines de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="01713-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="01713-105">Es posible que se necesite la migración de paquetes de configuración en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="01713-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="01713-106">Actualizar el hardware de servidor existente a un servidor más moderno.</span><span class="sxs-lookup"><span data-stu-id="01713-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="01713-107">Migración de un recurso compartido de ubicación de almacenamiento de configuración de un laboratorio a un servidor de producción.</span><span class="sxs-lookup"><span data-stu-id="01713-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="01713-108">Simplemente copiando los archivos y carpetas no se conservarán los permisos ni la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="01713-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="01713-109">Los pasos descritos a continuación copiarán correctamente los archivos del paquete de configuración con sus permisos NTFS en un nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="01713-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="01713-110">Cómo mantener los paquetes de configuración de UE-V al migrar a un nuevo servidor</span><span class="sxs-lookup"><span data-stu-id="01713-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="01713-111">En una nueva ubicación de un servidor diferente, cree una nueva carpeta; por ejemplo, bisettings.</span><span class="sxs-lookup"><span data-stu-id="01713-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="01713-112">Deshabilite el uso compartido para el antiguo recurso compartido de carpetas en el servidor antiguo.</span><span class="sxs-lookup"><span data-stu-id="01713-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="01713-113">Mueva los paquetes de configuración existentes al nuevo servidor con Robocopy desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="01713-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="01713-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="01713-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="01713-115">**Nota:**  Para supervisar el progreso de la copia, abra MySettings.txt con un lector de archivos de registro, como Trace32.</span><span class="sxs-lookup"><span data-stu-id="01713-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="01713-116">Otorgue permisos de nivel compartido al nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="01713-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="01713-117">Deje los permisos NTFS tal y como fueron establecidos por Robocopy.</span><span class="sxs-lookup"><span data-stu-id="01713-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="01713-118">En los equipos que ejecutan el agente de UE-V, actualice la opción de configuración SettingsStoragePath a la ruta de acceso UNC del nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="01713-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="01713-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01713-119">Related topics</span></span>


[<span data-ttu-id="01713-120">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="01713-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="01713-121">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="01713-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





