---
title: LOAD APP
description: LOAD APP
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816250"
---
# <span data-ttu-id="246c6-103">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="246c6-103">LOAD APP</span></span>


<span data-ttu-id="246c6-104">Carga la aplicación especificada y todas las demás aplicaciones del paquete en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="246c6-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="246c6-105">**Nota:**  El comando **cargar aplicación** inicia el proceso de carga y se muestra una barra de progreso en el área de notificación del escritorio.</span><span class="sxs-lookup"><span data-stu-id="246c6-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="246c6-106">El comando se cierra inmediatamente después de iniciar este proceso, de modo que cualquier error de carga se muestra en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="246c6-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="246c6-107">Use el comando **cargar paquete** si desea iniciar el proceso de carga desde la línea de comandos sin usar el área de notificación del escritorio.</span><span class="sxs-lookup"><span data-stu-id="246c6-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="246c6-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="246c6-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="246c6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="246c6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="246c6-110">Aplicación: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="246c6-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="246c6-111">El nombre y la versión (opcional) de la aplicación que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="246c6-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="246c6-112">Log</span><span class="sxs-lookup"><span data-stu-id="246c6-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="246c6-113">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="246c6-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="246c6-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="246c6-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="246c6-115">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="246c6-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="246c6-116">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="246c6-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="246c6-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="246c6-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="246c6-118">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="246c6-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="246c6-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="246c6-119">Related topics</span></span>


[<span data-ttu-id="246c6-120">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="246c6-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





