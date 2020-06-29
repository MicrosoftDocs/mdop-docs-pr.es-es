---
title: Cambiar la frecuencia de las tareas programadas de UE-V
description: Cambiar la frecuencia de las tareas programadas de UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822690"
---
# <span data-ttu-id="d5ab0-103">Cambiar la frecuencia de las tareas programadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="d5ab0-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="d5ab0-104">El instalador del agente de Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, crea dos tareas programadas durante la instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="d5ab0-105">Las dos tareas son la tarea de **actualización automática** de la plantilla y la tarea configuración de la **Ubicación de almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="d5ab0-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="d5ab0-106">Estas tareas programadas no se pueden configurar con las herramientas de UE-V.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="d5ab0-107">Los administradores que deseen cambiar la tarea programada para estos elementos pueden crear un script que use las opciones de la línea de comandos de Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="d5ab0-108">Para obtener más información sobre Schtasks.exe, consulte [Cómo usar Schtasks, exe para programar tareas en Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="d5ab0-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="d5ab0-109">Actualización automática de plantillas</span><span class="sxs-lookup"><span data-stu-id="d5ab0-109">Template Auto-Update</span></span>


<span data-ttu-id="d5ab0-110">La tarea de **actualización automática** de la plantilla comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o eliminadas.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="d5ab0-111">Esta tarea solo se ejecuta si el SettingsTemplateCatalog está configurado.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="d5ab0-112">La tarea **actualización automática** de la plantilla ejecuta el archivo de ApplySettingsCatalog.exe, que se encuentra en el directorio de instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d5ab0-113">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="d5ab0-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="d5ab0-114">Desencadenador predeterminado</span><span class="sxs-lookup"><span data-stu-id="d5ab0-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5ab0-115">Actualización automática de \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="d5ab0-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5ab0-116">3:30 AM todos los días</span><span class="sxs-lookup"><span data-stu-id="d5ab0-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d5ab0-117">**Ejemplo:** El siguiente comando configura el agente para comprobar el almacén del catálogo de plantillas de configuración cada hora.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="d5ab0-118">Estado de ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="d5ab0-118">Settings Storage Location Status</span></span>


<span data-ttu-id="d5ab0-119">La tarea de **configuración de estado de ubicación de almacenamiento** ejecuta las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="d5ab0-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="d5ab0-120">Comprueba que las carpetas UE-V estén fijas o registradas con la característica archivos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="d5ab0-121">Comprueba si la ubicación de almacenamiento de configuración está desconectada o conectada.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="d5ab0-122">Fuerza una sincronización en el intervalo especificado en lugar del intervalo predeterminado para archivos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="d5ab0-123">Sincroniza los paquetes de configuración que están configurados para su búsqueda anticipada.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="d5ab0-124">Comprueba si la ruta del directorio principal de Active Directory ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="d5ab0-125">Escribe la configuración de almacenamiento de la configuración actual en la siguiente ubicación</span><span class="sxs-lookup"><span data-stu-id="d5ab0-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="d5ab0-126">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="d5ab0-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="d5ab0-127">Desencadenador predeterminado</span><span class="sxs-lookup"><span data-stu-id="d5ab0-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d5ab0-128">Estado de la ubicación de almacenamiento de \Microsoft\UE-V\Settings</span><span class="sxs-lookup"><span data-stu-id="d5ab0-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d5ab0-129">Al iniciar sesión en cualquier usuario: después de su activación, repita cada 30 minutos indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="d5ab0-130">**Ejemplo:** El siguiente comando configura el agente para que ejecute la acción por encima de cada hora.</span><span class="sxs-lookup"><span data-stu-id="d5ab0-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="d5ab0-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5ab0-131">Related topics</span></span>


[<span data-ttu-id="d5ab0-132">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d5ab0-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="d5ab0-133">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d5ab0-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





