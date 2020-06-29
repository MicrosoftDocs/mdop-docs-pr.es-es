---
title: Ficha General de propiedades de virtualización de aplicaciones
description: Ficha General de propiedades de virtualización de aplicaciones
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819690"
---
# <span data-ttu-id="a7c54-103">Propiedades de virtualización de aplicaciones: Pestaña General</span><span class="sxs-lookup"><span data-stu-id="a7c54-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="a7c54-104">Use la pestaña **General** del cuadro de diálogo **propiedades de Application Virtualization** para modificar la configuración de registro y las ubicaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="a7c54-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="a7c54-105">Esta pestaña contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="a7c54-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="a7c54-106">Nivel de registro</span><span class="sxs-lookup"><span data-stu-id="a7c54-106">Log Level</span></span>**  
<span data-ttu-id="a7c54-107">Seleccione el nivel de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="a7c54-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="a7c54-108">El nivel predeterminado es **información**.</span><span class="sxs-lookup"><span data-stu-id="a7c54-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="a7c54-109">Restablecer registro</span><span class="sxs-lookup"><span data-stu-id="a7c54-109">Reset Log</span></span>**  
<span data-ttu-id="a7c54-110">Haga clic en este botón para realizar una copia de seguridad del archivo de registro actual e iniciar inmediatamente un nuevo archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="a7c54-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="a7c54-111">Ubicación</span><span class="sxs-lookup"><span data-stu-id="a7c54-111">Location</span></span>**  
<span data-ttu-id="a7c54-112">Escriba o busque la ubicación en la que desea guardar el archivo de registro sftlog.txt.</span><span class="sxs-lookup"><span data-stu-id="a7c54-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="a7c54-113">Las ubicaciones predeterminadas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7c54-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="a7c54-114">Para WindowsXP, Windows Server2003:*C:\\Documents and Settings\\All Users\\Application cliente de virtualización de Data\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="a7c54-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="a7c54-115">Para Windows Vista, Windows 7, Windows Server2008:*C:\\ProgramData\\Microsoft\\Application cliente de virtualización*</span><span class="sxs-lookup"><span data-stu-id="a7c54-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="a7c54-116">Nivel de registro del sistema</span><span class="sxs-lookup"><span data-stu-id="a7c54-116">System Log Level</span></span>**  
<span data-ttu-id="a7c54-117">Seleccione el nivel de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="a7c54-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="a7c54-118">El nivel predeterminado es **ADVERTENCIA**.</span><span class="sxs-lookup"><span data-stu-id="a7c54-118">The default level is **Warning**.</span></span>

<span data-ttu-id="a7c54-119">**Nota:**  La configuración del **nivel de registro del sistema** controla el nivel de los mensajes enviados al registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="a7c54-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="a7c54-120">Los mensajes registrados son idénticos a los mensajes que se registran en el registro de eventos del cliente, pero se almacenan en una ubicación diferente que no tiene las limitaciones de espacio del registro de eventos del cliente.</span><span class="sxs-lookup"><span data-stu-id="a7c54-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="a7c54-121">Dado que el registro de eventos del sistema no tiene limitaciones de espacio, es ideal para situaciones en las que es necesario realizar registros detallados.</span><span class="sxs-lookup"><span data-stu-id="a7c54-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="a7c54-122">Directorio de datos global</span><span class="sxs-lookup"><span data-stu-id="a7c54-122">Global Data Directory</span></span>**  
<span data-ttu-id="a7c54-123">Escriba o busque la ubicación del directorio del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="a7c54-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="a7c54-124">Las ubicaciones predeterminadas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7c54-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="a7c54-125">Para WindowsXP, Windows Server2003:*C:\\Documents and Settings\\All Users\\Application cliente de virtualización de Data\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="a7c54-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="a7c54-126">Para Windows Vista, Windows 7, Windows Server2008:*C:\\ProgramData\\Microsoft\\Application cliente de virtualización*</span><span class="sxs-lookup"><span data-stu-id="a7c54-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="a7c54-127">Directorio de datos de usuario</span><span class="sxs-lookup"><span data-stu-id="a7c54-127">User Data Directory</span></span>**  
<span data-ttu-id="a7c54-128">Escriba o busque la ubicación del directorio donde se almacenan los datos específicos del usuario.</span><span class="sxs-lookup"><span data-stu-id="a7c54-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="a7c54-129">El valor predeterminado es% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="a7c54-129">The default is %APPDATA%.</span></span> <span data-ttu-id="a7c54-130">Esta ruta debe ser una variable de entorno válida en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="a7c54-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="a7c54-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7c54-131">Related topics</span></span>


[<span data-ttu-id="a7c54-132">Consola de administración de cliente: Propiedades de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a7c54-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





