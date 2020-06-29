---
title: Cómo configurar el archivo de registro del cliente
description: Cómo configurar el archivo de registro del cliente
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817800"
---
# <span data-ttu-id="07758-103">Cómo configurar el archivo de registro del cliente</span><span class="sxs-lookup"><span data-stu-id="07758-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="07758-104">Puede usar los procedimientos siguientes para configurar el archivo de registro de cliente de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="07758-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="07758-105">Para cambiar la ubicación del archivo de registro</span><span class="sxs-lookup"><span data-stu-id="07758-105">To change the log file location</span></span>**

-   <span data-ttu-id="07758-106">Edite el siguiente valor de la clave del registro para especificar la nueva ruta de acceso del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="07758-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="07758-107">Debe reiniciar el servicio **sftlist** después de cambiar este valor.</span><span class="sxs-lookup"><span data-stu-id="07758-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="07758-108">Esta ubicación también se puede cambiar de forma interactiva después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="07758-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="07758-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span><span class="sxs-lookup"><span data-stu-id="07758-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="07758-110">Para cambiar el nivel de informes de registro</span><span class="sxs-lookup"><span data-stu-id="07758-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="07758-111">De forma predeterminada, el tipo de mensajes que se escriben en el registro incluye todos los eventos de nivel de gravedad 4 (informativo) o superior.</span><span class="sxs-lookup"><span data-stu-id="07758-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="07758-112">El nivel de gravedad se almacena en el siguiente valor de clave.</span><span class="sxs-lookup"><span data-stu-id="07758-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="07758-113">Establezca este valor de clave en 5 para habilitar el registro detallado.</span><span class="sxs-lookup"><span data-stu-id="07758-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="07758-114">Use el registro detallado solo durante breves períodos de solución de problemas, ya que generará un gran volumen de mensajes y hará que el registro se llene rápidamente.</span><span class="sxs-lookup"><span data-stu-id="07758-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="07758-115">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="07758-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="07758-116">Para cambiar el tamaño del registro</span><span class="sxs-lookup"><span data-stu-id="07758-116">To change the log size</span></span>**

-   <span data-ttu-id="07758-117">En Application Virtualization (App-V) 4,5, el tamaño del registro está controlado por el siguiente valor de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="07758-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="07758-118">Este valor se establece de forma predeterminada en 256 MB y define el tamaño máximo, en MB, que puede alcanzar el registro antes de restablecerlo.</span><span class="sxs-lookup"><span data-stu-id="07758-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="07758-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="07758-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="07758-120">**PRECAUCIÓN**  Este valor de clave del registro debe establecerse en un valor mayor que cero para garantizar que el archivo de registro se restablezca.</span><span class="sxs-lookup"><span data-stu-id="07758-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="07758-121">Para cambiar el número de copias de seguridad</span><span class="sxs-lookup"><span data-stu-id="07758-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="07758-122">Cuando el archivo de registro alcanza el tamaño máximo, se fuerza un reinicio cuando se produce la siguiente escritura en el registro.</span><span class="sxs-lookup"><span data-stu-id="07758-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="07758-123">Un restablecimiento hace que se cree un nuevo archivo de registro y el nombre del archivo antiguo es de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="07758-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="07758-124">La siguiente configuración del registro controla el número de copias de seguridad del archivo de registro que se conservan cuando se restablece el archivo.</span><span class="sxs-lookup"><span data-stu-id="07758-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="07758-125">El valor predeterminado es 4.</span><span class="sxs-lookup"><span data-stu-id="07758-125">The default value is 4.</span></span>

    <span data-ttu-id="07758-126">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="07758-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="07758-127">El formato de los nombres de archivo de registro de la copia de seguridad es: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** y se basa en el tiempo de restablecimiento, en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="07758-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="07758-128">En la tabla siguiente se enumeran los símbolos que se usan para crear los nombres de archivo y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="07758-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="07758-129">Símbolo</span><span class="sxs-lookup"><span data-stu-id="07758-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="07758-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="07758-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="07758-131">DD</span><span class="sxs-lookup"><span data-stu-id="07758-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-132">año de 4 dígitos</span><span class="sxs-lookup"><span data-stu-id="07758-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="07758-133">MM</span><span class="sxs-lookup"><span data-stu-id="07758-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-134">mes de 2 dígitos (01 a 12)</span><span class="sxs-lookup"><span data-stu-id="07758-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="07758-135">YYYY</span><span class="sxs-lookup"><span data-stu-id="07758-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-136">día del mes de 2 dígitos (01 a 31)</span><span class="sxs-lookup"><span data-stu-id="07758-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="07758-137">HH</span><span class="sxs-lookup"><span data-stu-id="07758-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-138">hora (00 a 23)</span><span class="sxs-lookup"><span data-stu-id="07758-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="07758-139">mm</span><span class="sxs-lookup"><span data-stu-id="07758-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-140">minutos (00 a 59)</span><span class="sxs-lookup"><span data-stu-id="07758-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="07758-141">ss</span><span class="sxs-lookup"><span data-stu-id="07758-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-142">segundos (00 a 59)</span><span class="sxs-lookup"><span data-stu-id="07758-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="07758-143">uuu</span><span class="sxs-lookup"><span data-stu-id="07758-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07758-144">milisegundos (000 a 999)</span><span class="sxs-lookup"><span data-stu-id="07758-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="07758-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07758-145">Related topics</span></span>


[<span data-ttu-id="07758-146">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="07758-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





