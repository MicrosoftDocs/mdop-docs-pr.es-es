---
title: Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell
description: Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814071"
---
# <span data-ttu-id="40b4b-103">Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="40b4b-103">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>


<span data-ttu-id="40b4b-104">Use el siguiente procedimiento para configurar el 5,1 de App-V para informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-104">Use the following procedure to configure the App-V 5.1 for reporting.</span></span>

**<span data-ttu-id="40b4b-105">Para configurar el equipo que ejecuta el cliente de App-V 5,1 para informes</span><span class="sxs-lookup"><span data-stu-id="40b4b-105">To configure the computer running the App-V 5.1 client for reporting</span></span>**

1. <span data-ttu-id="40b4b-106">Instale el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="40b4b-106">Install the App-V 5.1 client.</span></span> <span data-ttu-id="40b4b-107">Para obtener más información sobre la instalación del cliente [, consulte Cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="40b4b-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

2. <span data-ttu-id="40b4b-108">Después de instalar el cliente de App-V 5,1, use el PowerShell **set-AppvClientConfiguration** para configurar las opciones de configuración de informes apropiadas:</span><span class="sxs-lookup"><span data-stu-id="40b4b-108">After you have installed the App-V 5.1 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="40b4b-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="40b4b-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="40b4b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40b4b-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="40b4b-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="40b4b-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-112">Permite al cliente devolver información a un servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="40b4b-113">Esta configuración es necesaria para que el cliente recopile los datos de informes en el cliente.</span><span class="sxs-lookup"><span data-stu-id="40b4b-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="40b4b-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="40b4b-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-115">Especifica la ubicación en el servidor de informes donde se guarda la información del cliente.</span><span class="sxs-lookup"><span data-stu-id="40b4b-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="40b4b-116">Por ejemplo, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="40b4b-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="40b4b-117">Nota</span><span class="sxs-lookup"><span data-stu-id="40b4b-117">Note</span></span></strong><br/><p><span data-ttu-id="40b4b-118">Este es el número de puerto que se asignó durante la configuración del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="40b4b-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="40b4b-119">Hora de inicio de informes</span><span class="sxs-lookup"><span data-stu-id="40b4b-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-120">Se establece para programar el cliente para que envíe los datos al servidor automáticamente.</span><span class="sxs-lookup"><span data-stu-id="40b4b-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="40b4b-121">Esta configuración indicará la hora a la que los datos de informes comenzarán a enviarse.</span><span class="sxs-lookup"><span data-stu-id="40b4b-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="40b4b-122">Se encuentra en el formato de 24 horas y tomará un número entre 0-23.</span><span class="sxs-lookup"><span data-stu-id="40b4b-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="40b4b-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="40b4b-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-124">Especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="40b4b-125">Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre 0 y ReportingRandomDelay, y esperará la duración especificada antes de enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="40b4b-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="40b4b-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="40b4b-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-127">Especifica el intervalo de reintento que usará el cliente para volver a enviar datos al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="40b4b-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="40b4b-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-129">Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="40b4b-130">El tamaño se aplica a la memoria caché en memoria.</span><span class="sxs-lookup"><span data-stu-id="40b4b-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="40b4b-131">Cuando se alcance el límite, el archivo de registro se retirará.</span><span class="sxs-lookup"><span data-stu-id="40b4b-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="40b4b-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="40b4b-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="40b4b-133">Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="40b4b-134">El tamaño se aplica a la memoria caché en memoria.</span><span class="sxs-lookup"><span data-stu-id="40b4b-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="40b4b-135">Cuando se alcance el límite, el archivo de registro se retirará.</span><span class="sxs-lookup"><span data-stu-id="40b4b-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="40b4b-136">Una vez que se haya configurado la configuración adecuada, el equipo que ejecuta el cliente de App-V 5,1 recopilará los datos automáticamente y los enviará de vuelta al servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="40b4b-136">After the appropriate settings have been configured, the computer running the App-V 5.1 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="40b4b-137">Además, los administradores pueden volver a enviar los datos de forma manual mediante el cmdlet de PowerShell **send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="40b4b-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="40b4b-138">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="40b4b-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="40b4b-139">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="40b4b-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="40b4b-140">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="40b4b-140">Got an App-V issue?</span></span>** <span data-ttu-id="40b4b-141">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="40b4b-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="40b4b-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40b4b-142">Related topics</span></span>


[<span data-ttu-id="40b4b-143">Administrar 5.1 de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="40b4b-143">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









