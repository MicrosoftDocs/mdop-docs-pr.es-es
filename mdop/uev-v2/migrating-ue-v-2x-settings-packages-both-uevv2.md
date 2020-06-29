---
title: Migrar paquetes de configuración de UE-V 2. x
description: Migrar paquetes de configuración de UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825520"
---
# <span data-ttu-id="a1deb-103">Migrar paquetes de configuración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a1deb-103">Migrating UE-V 2.x Settings Packages</span></span>


<span data-ttu-id="a1deb-104">En el ciclo de vida de una implementación de Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, es posible que tenga que cambiar la ubicación de los paquetes de configuración de usuario al migrar a un nuevo servidor o al realizar copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a1deb-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 deployment, you might have to relocate the user settings packages either when you migrate to a new server or when you perform backups.</span></span> <span data-ttu-id="a1deb-105">Es posible que los paquetes de configuración deban migrarse en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="a1deb-105">Settings packages might have to be migrated in the following scenarios:</span></span>

-   <span data-ttu-id="a1deb-106">Actualizar el hardware de servidor existente a un servidor más moderno.</span><span class="sxs-lookup"><span data-stu-id="a1deb-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="a1deb-107">Migración de un recurso compartido de ubicación de almacenamiento de configuración de un servidor de prueba a un servidor de producción.</span><span class="sxs-lookup"><span data-stu-id="a1deb-107">Migration of a settings storage location share from a test server to a production server.</span></span>

<span data-ttu-id="a1deb-108">Simplemente copiando los archivos y carpetas no se conservan los permisos ni la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a1deb-108">Simply copying the files and folders does not preserve the security settings and permissions.</span></span> <span data-ttu-id="a1deb-109">Los pasos siguientes describen cómo copiar correctamente el paquete de configuración junto con los permisos del sistema de archivos NTFS en un nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="a1deb-109">The following steps describe how to correctly copy the settings package along with their NTFS file system permissions to a new share.</span></span>

**<span data-ttu-id="a1deb-110">Para conservar los paquetes de configuración de UE-V 2 al migrar a un nuevo servidor</span><span class="sxs-lookup"><span data-stu-id="a1deb-110">To preserve UE-V 2 settings packages when you migrate to a new server</span></span>**

1.  <span data-ttu-id="a1deb-111">En una nueva ubicación de un servidor diferente, cree una nueva carpeta, por ejemplo, a través de la configuración.</span><span class="sxs-lookup"><span data-stu-id="a1deb-111">In a new location on a different server, create a new folder, for example, MySettings.</span></span>

2.  <span data-ttu-id="a1deb-112">Deshabilite el uso compartido para el antiguo recurso compartido de carpetas en el servidor antiguo.</span><span class="sxs-lookup"><span data-stu-id="a1deb-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="a1deb-113">Para copiar los paquetes de configuración existentes en el nuevo servidor con Robocopy</span><span class="sxs-lookup"><span data-stu-id="a1deb-113">To copy the existing settings packages to the new server with Robocopy</span></span>

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="a1deb-114">**Nota:**  Para supervisar el progreso de la copia, abra MySettings.txt con un visor de registro como Trace32.</span><span class="sxs-lookup"><span data-stu-id="a1deb-114">**Note** To monitor the copy progress, open MySettings.txt with a log viewer such as Trace32.</span></span>

     

4.  <span data-ttu-id="a1deb-115">Otorgue permisos de nivel compartido al nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="a1deb-115">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="a1deb-116">Deje los permisos del sistema de archivos NTFS tal y como fueron establecidos por Robocopy.</span><span class="sxs-lookup"><span data-stu-id="a1deb-116">Leave the NTFS file system permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="a1deb-117">En los equipos que ejecutan el agente de UE-V, actualice la opción de configuración **SettingsStoragePath** a la ruta de acceso UNC (Convención de nomenclatura universal) del nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="a1deb-117">On computers that run the UE-V Agent, update the **SettingsStoragePath** configuration setting to the Universal Naming Convention (UNC) path of the new share.</span></span>

    <span data-ttu-id="a1deb-118">**¿Tiene una sugerencia para UE-V**?</span><span class="sxs-lookup"><span data-stu-id="a1deb-118">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="a1deb-119">Agregue o vote por sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a1deb-119">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="a1deb-120">**¿Tienes un problema de UE-V**?</span><span class="sxs-lookup"><span data-stu-id="a1deb-120">**Got a UE-V issue**?</span></span> <span data-ttu-id="a1deb-121">Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="a1deb-121">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="a1deb-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1deb-122">Related topics</span></span>


[<span data-ttu-id="a1deb-123">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a1deb-123">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





