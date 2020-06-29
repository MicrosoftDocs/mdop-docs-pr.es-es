---
title: Archivos de registro del secuenciador de virtualización de aplicaciones
description: Archivos de registro del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816220"
---
# <span data-ttu-id="559e3-103">Archivos de registro del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="559e3-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="559e3-104">Los archivos de registro del secuenciador Application Virtualization (App-V) proporcionan información detallada sobre las aplicaciones de secuencias, y pueden resultarle útiles para comprobar la funcionalidad o para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="559e3-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="559e3-105">En la tabla siguiente se proporciona información sobre los archivos de registro y sus ubicaciones predeterminadas, que se crean al utilizar el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="559e3-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="559e3-106">Nombre de archivo de registro</span><span class="sxs-lookup"><span data-stu-id="559e3-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="559e3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="559e3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="559e3-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="559e3-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="559e3-109">Proporciona información general acerca de la secuenciación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="559e3-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="559e3-110">Use este registro como punto de partida para solucionar errores de secuenciador.</span><span class="sxs-lookup"><span data-stu-id="559e3-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="559e3-111">Ubicación del archivo de registro: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="559e3-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="559e3-112">[Valor del token de plantilla] Ubicación del archivo de registro de App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valor del token de plantilla]</span><span class="sxs-lookup"><span data-stu-id="559e3-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="559e3-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="559e3-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="559e3-114">Proporciona información sobre las tareas de reinicio del equipo que se producen durante el reinicio simulado del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="559e3-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="559e3-115">Ubicación del archivo de registro: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="559e3-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="559e3-116">[Valor del token de plantilla] Ubicación del archivo de registro de App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valor del token de plantilla]</span><span class="sxs-lookup"><span data-stu-id="559e3-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="559e3-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="559e3-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="559e3-118">Proporciona información general acerca de los procesos que se usan durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="559e3-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="559e3-119">Ubicación del archivo de registro: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="559e3-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="559e3-120">[Valor del token de plantilla] Ubicación del archivo de registro de App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valor del token de plantilla]</span><span class="sxs-lookup"><span data-stu-id="559e3-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="559e3-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="559e3-121">Related topics</span></span>


[<span data-ttu-id="559e3-122">Referencia del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="559e3-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





