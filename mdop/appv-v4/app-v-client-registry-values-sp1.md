---
title: Valores del registro de cliente de App-V
description: Valores del registro de cliente de App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819810"
---
# <span data-ttu-id="5ad88-103">Valores del registro de cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="5ad88-103">App-V Client Registry Values</span></span>


<span data-ttu-id="5ad88-104">El cliente de Microsoft Application Virtualization (App-V) almacena su configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="5ad88-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="5ad88-105">Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="5ad88-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="5ad88-106">También puede configurar muchas acciones de cliente cambiando las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="5ad88-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="5ad88-107">En este tema se enumeran todas las claves de registro de cliente de Application Virtualization (App-V) y se explica su uso.</span><span class="sxs-lookup"><span data-stu-id="5ad88-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="5ad88-108">Importante</span><span class="sxs-lookup"><span data-stu-id="5ad88-108">Important</span></span>**  
<span data-ttu-id="5ad88-109">En un equipo que ejecute un sistema operativo de 64 bits, las claves y los valores que se describen en las siguientes secciones estarán bajo HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="5ad88-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="5ad88-110">Clave de configuración</span><span class="sxs-lookup"><span data-stu-id="5ad88-110">Configuration Key</span></span>


<span data-ttu-id="5ad88-111">En la tabla siguiente se proporciona información acerca de los valores del registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="5ad88-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-112">Name</span></span></th>
<th align="left"><span data-ttu-id="5ad88-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-113">Type</span></span></th>
<th align="left"><span data-ttu-id="5ad88-114">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="5ad88-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="5ad88-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-118">Cliente de escritorio de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5ad88-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-119">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-120">Versión</span><span class="sxs-lookup"><span data-stu-id="5ad88-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="5ad88-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-123">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-124">Controladores</span><span class="sxs-lookup"><span data-stu-id="5ad88-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="5ad88-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-127">Si este valor de clave está presente, contiene el nombre del controlador que causó un error de detención la última vez que se inició el núcleo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="5ad88-128">Después de corregir el error de detención, debe eliminar este valor de clave para que sftlist se inicie.</span><span class="sxs-lookup"><span data-stu-id="5ad88-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-129">InstallPath</span><span class="sxs-lookup"><span data-stu-id="5ad88-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-131">Predeterminado = C:\Archivos de Programa\microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="5ad88-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-132">La ubicación en la que el cliente está instalado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-132">The location where the client is installed.</span></span> <span data-ttu-id="5ad88-133">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-134">Nombrearchivoregistro</span><span class="sxs-lookup"><span data-stu-id="5ad88-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-136">Default = CSIDL_COMMON_APPDATA \Microsoft\Application Virtualization Client\sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="5ad88-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-137">La ruta de acceso y el nombre del archivo de registro del cliente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5ad88-138">Nota</span><span class="sxs-lookup"><span data-stu-id="5ad88-138">Note</span></span></strong><br/><p><span data-ttu-id="5ad88-139">Si está ejecutando una versión anterior a la de App-V 4,6, SP1 y modifica el nombre o la ubicación del archivo de registro, debe reiniciar el servicio sftlist para que el cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-140">LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="5ad88-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-142">Valor predeterminado = 4, informativo</span><span class="sxs-lookup"><span data-stu-id="5ad88-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-143">Controla qué mensajes se escriben en el registro.</span><span class="sxs-lookup"><span data-stu-id="5ad88-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="5ad88-144">El valor indica el umbral de lo que se registra: todo menor que o igual a ese valor se registra.</span><span class="sxs-lookup"><span data-stu-id="5ad88-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="5ad88-145">Por ejemplo, un valor de 0X3 (ADVERTENCIA) indica que se registran las advertencias (0X3), los errores (0X2) y los errores críticos (0x1).</span><span class="sxs-lookup"><span data-stu-id="5ad88-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="5ad88-146">Intervalo de valores: 0X0 = ninguno, 0x1 = crítico, 0X2 = error, 0X3 = ADVERTENCIA, 0x4 = información (predeterminado), 0X5 = detallado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="5ad88-147">El nivel de registro se puede configurar desde la consola de cliente de Application Virtualization (App-V) y desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="5ad88-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="5ad88-148">En el símbolo del sistema, el comando sftlist.exe/verboselog aumentará el nivel de registro a verbose.</span><span class="sxs-lookup"><span data-stu-id="5ad88-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="5ad88-149">Para obtener más información sobre los detalles de la línea de comandos, consulte</span><span class="sxs-lookup"><span data-stu-id="5ad88-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="5ad88-150">.</span><span class="sxs-lookup"><span data-stu-id="5ad88-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="5ad88-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-153">Valor predeterminado = 4</span><span class="sxs-lookup"><span data-stu-id="5ad88-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-154">Define el número de copias de seguridad del archivo de registro que se conservan cuando se restablece.</span><span class="sxs-lookup"><span data-stu-id="5ad88-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="5ad88-155">El intervalo válido es de 0 a 9999.</span><span class="sxs-lookup"><span data-stu-id="5ad88-155">The valid range is 0–9999.</span></span> <span data-ttu-id="5ad88-156">El valor predeterminado es 4.</span><span class="sxs-lookup"><span data-stu-id="5ad88-156">The default is 4.</span></span> <span data-ttu-id="5ad88-157">Un valor de 0 significa que no se conservarán copias.</span><span class="sxs-lookup"><span data-stu-id="5ad88-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-158">LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="5ad88-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-160">Valor predeterminado = 256</span><span class="sxs-lookup"><span data-stu-id="5ad88-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-161">Define el tamaño máximo en megabytes (MB) que puede alcanzar el archivo de registro antes de restablecerlo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="5ad88-162">El tamaño predeterminado es 256 MB.</span><span class="sxs-lookup"><span data-stu-id="5ad88-162">The default size is 256 MB.</span></span> <span data-ttu-id="5ad88-163">Cuando se alcanza este tamaño, se forzará un restablecimiento de registro en el siguiente intento de escritura.</span><span class="sxs-lookup"><span data-stu-id="5ad88-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="5ad88-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-166">Valor predeterminado = 0x4 (App-V 4,5)</span><span class="sxs-lookup"><span data-stu-id="5ad88-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="5ad88-167">Valor predeterminado = 0X3 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="5ad88-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-168">Indica el nivel de registro en el que los mensajes de registro se escriben en el registro de eventos de NT.</span><span class="sxs-lookup"><span data-stu-id="5ad88-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="5ad88-169">El valor indica un umbral de lo que se registra (es decir, se registra todo igual a o menor que ese valor).</span><span class="sxs-lookup"><span data-stu-id="5ad88-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="5ad88-170">Por ejemplo, un valor de 0X3 (ADVERTENCIA) indica que se registran las advertencias (0X3), los errores (0X2) y los errores críticos (0x1).</span><span class="sxs-lookup"><span data-stu-id="5ad88-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="5ad88-171">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="5ad88-171">Value Range</span></span></p>
<p><span data-ttu-id="5ad88-172">0X0 = ninguno</span><span class="sxs-lookup"><span data-stu-id="5ad88-172">0x0 = None</span></span></p>
<p><span data-ttu-id="5ad88-173">0x1 = crítico</span><span class="sxs-lookup"><span data-stu-id="5ad88-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="5ad88-174">0X2 = error</span><span class="sxs-lookup"><span data-stu-id="5ad88-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="5ad88-175">0X3 = Warning</span><span class="sxs-lookup"><span data-stu-id="5ad88-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="5ad88-176">0x4 = información (predeterminada)</span><span class="sxs-lookup"><span data-stu-id="5ad88-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="5ad88-177">0X5 = verbose</span><span class="sxs-lookup"><span data-stu-id="5ad88-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="5ad88-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-180">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-181">Indica si se habilitará la transmisión desde un archivo independientemente de cómo se haya configurado el cliente con el parámetro APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="5ad88-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="5ad88-182">Si se establece en FALSE, el transporte no habilitará la transmisión por secuencias de archivos incluso si el OSD HREF o el parámetro APPLICATIONSOURCEROOT contienen una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="5ad88-183">0X0 = falso (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="5ad88-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="5ad88-184">0x1 = verdadero</span><span class="sxs-lookup"><span data-stu-id="5ad88-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="5ad88-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-186">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="5ad88-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="5ad88-188">archivo://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="5ad88-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="5ad88-189">archivo://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="5ad88-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-190">Permite a un administrador o un sistema de distribución electrónica de software (ESD) garantizar la carga de la aplicación según el esquema de administración de la topología.</span><span class="sxs-lookup"><span data-stu-id="5ad88-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="5ad88-191">Use este valor de clave para invalidar el código base del OSD para el elemento HREF (por ejemplo, la ubicación de origen) de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="5ad88-192">La raíz de origen de la aplicación admite direcciones URL y formatos de ruta de acceso UNC (Convención de nomenclatura universal).</span><span class="sxs-lookup"><span data-stu-id="5ad88-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="5ad88-193">El formato correcto para la ruta de acceso de la dirección URL es protocolo: \ \ [puerto] [/path] [/], donde puerto y ruta de acceso son opcionales.</span><span class="sxs-lookup"><span data-stu-id="5ad88-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="5ad88-194">Si no se especifica un puerto, se usa el puerto predeterminado para el protocolo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="5ad88-195">Solo se reemplaza la parte Protocol://Server: Port de la dirección URL de la OSD.</span><span class="sxs-lookup"><span data-stu-id="5ad88-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="5ad88-196">El formato correcto para la ruta de acceso UNC es \computername\sharefolder [carpeta] [], donde carpeta es opcional.</span><span class="sxs-lookup"><span data-stu-id="5ad88-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="5ad88-197">El nombre del equipo puede ser un nombre de dominio completo (FQDN) o una dirección IP, y ShareFolder puede ser una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="5ad88-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="5ad88-198">Solo se reemplaza la parte de \computername\sharefolder o letra de unidad de la ruta de acceso de la OSD.</span><span class="sxs-lookup"><span data-stu-id="5ad88-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="5ad88-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="5ad88-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="5ad88-202">\computername\content</span><span class="sxs-lookup"><span data-stu-id="5ad88-202">\computername\content</span></span></p>
<p><span data-ttu-id="5ad88-203">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="5ad88-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="5ad88-204">Permite a un administrador especificar una ubicación de origen para la recuperación de archivos OSD para un paquete de aplicación de secuencia durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="5ad88-205">Los formatos aceptados para el OSDSourceRoot incluyen rutas de dirección y direcciones URL (http o https).</span><span class="sxs-lookup"><span data-stu-id="5ad88-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="5ad88-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="5ad88-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="5ad88-209">\computername\content</span><span class="sxs-lookup"><span data-stu-id="5ad88-209">\computername\content</span></span></p>
<p><span data-ttu-id="5ad88-210">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="5ad88-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="5ad88-211">Permite a un administrador especificar una ubicación de origen para la recuperación de archivos de icono para un paquete de aplicación de secuencia durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="5ad88-212">Los formatos aceptados para el IconSourceRoot incluyen rutas de dirección y direcciones URL (http o https).</span><span class="sxs-lookup"><span data-stu-id="5ad88-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="5ad88-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-215">Valor predeterminado = 5</span><span class="sxs-lookup"><span data-stu-id="5ad88-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-216">Autoload es un parámetro de configuración de la Directiva de tiempo de ejecución del cliente que permite que el bloque de características secundario de una aplicación virtualizada se transmita automáticamente al cliente en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5ad88-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="5ad88-217">Los desencadenadores de carga automática son marcas para indicar eventos que inician la carga automática de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5ad88-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="5ad88-218">Autoload usa implícitamente la transmisión por secuencias de fondo para permitir que la aplicación se cargue por completo en la caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="5ad88-219">El bloque de características principal se cargará en primer lugar y los bloques de características restantes se cargarán en segundo plano para permitir que se realicen operaciones en primer plano, como la interacción del usuario con aplicaciones, y ofrezcan un rendimiento óptimo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="5ad88-220">Valores de máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="5ad88-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="5ad88-221">(0) nunca: no se establecen bits (el valor es 0), no se realizará la carga automática porque no hay ningún desencadenador configurado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="5ad88-222">(1) Onlaunched: la carga se inicia cuando un usuario inicia una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="5ad88-223">(2) alactualizar: la carga se iniciará cuando se publique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="5ad88-224">Esto sucede siempre que el registro del paquete se agrega o se actualiza, por ejemplo, cuando se produce una actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="5ad88-225">(4) Inicio de sesión: la carga se inicia cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="5ad88-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="5ad88-226">(5) Onlaunched y inicio de sesión: default.</span><span class="sxs-lookup"><span data-stu-id="5ad88-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="5ad88-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-229">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-230">Indica qué se cargará automáticamente cuando se produzcan desencadenadores de carga automática.</span><span class="sxs-lookup"><span data-stu-id="5ad88-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="5ad88-231">Valores de máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="5ad88-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="5ad88-232">(0) ninguno: sin carga automática, independientemente de los desencadenadores que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="5ad88-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="5ad88-233">(1) PreviouslyUsed (valor predeterminado): Si algún desencadenador de carga automático está habilitado, carga solo los paquetes en los que se ha usado al menos una aplicación del paquete, es decir, iniciado o prealmacenado previamente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="5ad88-234">(2) todos: si se habilita algún desencadenador de carga automática, todas las aplicaciones del paquete (por paquete) o todos los paquetes (establecidos para el cliente) se cargarán automáticamente, tanto si se han iniciado como si no.</span><span class="sxs-lookup"><span data-stu-id="5ad88-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="5ad88-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-237">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-238">Indica que siempre se necesita autorización, independientemente de si una aplicación ya está en la caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="5ad88-239">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="5ad88-239">Possible values:</span></span></p>
<p><span data-ttu-id="5ad88-240">0 = falso: siempre intenta conectar con el servidor.</span><span class="sxs-lookup"><span data-stu-id="5ad88-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="5ad88-241">Si no se puede establecer una conexión con el servidor, el cliente seguirá permitiendo que el usuario inicie una aplicación que se haya cargado previamente en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="5ad88-242">1 = true (valor predeterminado): la aplicación siempre debe estar autorizada en el inicio.</span><span class="sxs-lookup"><span data-stu-id="5ad88-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="5ad88-243">Para las aplicaciones de transmisión RTSP, el token de autorización del usuario se envía al servidor para su autorización.</span><span class="sxs-lookup"><span data-stu-id="5ad88-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="5ad88-244">Para las aplicaciones basadas en archivos, las ACL de archivos controlan si un usuario puede acceder a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="5ad88-245">Reinicie el servicio sftlist para que el cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="5ad88-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-247">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-248">APPDATA</span><span class="sxs-lookup"><span data-stu-id="5ad88-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-249">Ubicación donde se almacenan la configuración de la caché de iconos y del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ad88-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="5ad88-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-251">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="5ad88-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-253">Directorio que se debe usar para datos globales de App-V, incluidas las cachés de archivos OSD, archivos de iconos, información de acceso directo y recursos del guardián del programa, como los archivos. ini.</span><span class="sxs-lookup"><span data-stu-id="5ad88-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="5ad88-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-256">0 o 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-257">Default = 0: un valor de 0 significa que el cliente intenta detectar las excepciones de programa internas para que otras aplicaciones de usuario puedan recuperarse y continuar cuando se produzca un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="5ad88-258">El valor 1 significa que el cliente permite que se produzcan las excepciones del programa interno para poder capturarlas en un depurador.</span><span class="sxs-lookup"><span data-stu-id="5ad88-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-261">60</span><span class="sxs-lookup"><span data-stu-id="5ad88-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-262">Tiempo de espera en segundos para las solicitudes IPC internas entre el núcleo y el front-end.</span><span class="sxs-lookup"><span data-stu-id="5ad88-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="5ad88-263">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="5ad88-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-266">base10</span><span class="sxs-lookup"><span data-stu-id="5ad88-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-267">Este valor se usa para indicar la rapidez con la que un programa puede cerrarse y no generar ningún mensaje de error cuando se está ejecutando otra aplicación en el mismo conjunto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-270">Valor predeterminado = 60000</span><span class="sxs-lookup"><span data-stu-id="5ad88-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-271">Define cuánto tiempo en milisegundos esperará el cliente cuando intente serializar el programa en el mismo conjunto de programas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="5ad88-272">Si el cliente agota el tiempo de espera, el inicio del programa continuará, pero no se serializará.</span><span class="sxs-lookup"><span data-stu-id="5ad88-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-275">300</span><span class="sxs-lookup"><span data-stu-id="5ad88-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-276">Tiempo de espera predeterminado en segundos para los scripts en el archivo OSD si WAIT = TRUE.</span><span class="sxs-lookup"><span data-stu-id="5ad88-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="5ad88-277">Puede especificar los tiempos de espera de cada script con el tiempo de espera en lugar de esperar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="5ad88-278">Un valor de 0 significa no esperar, y 0xFFFFFFFF significa esperar indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="5ad88-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-280">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5ad88-281">Si, en HKLM o HKCU, este valor contiene una ruta de acceso válida para un archivo de registro, SFTTray escribirá en este registro cuando se inicien los programas, se apague, se producirá un error de inicio y se entrará en el modo desconectado o se saldrá de él.</span><span class="sxs-lookup"><span data-stu-id="5ad88-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="5ad88-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-284">0x1A (26) registrar errores de inicio y de entrada y salida de modo desconectado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="5ad88-285">0x1F (31) registra todo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="5ad88-286">0X0 (0) no registra nada.</span><span class="sxs-lookup"><span data-stu-id="5ad88-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-287">Especifica cuáles de los cinco eventos se registran (valores de máscara de la máscara):</span><span class="sxs-lookup"><span data-stu-id="5ad88-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="5ad88-288">1 para inicio de programa</span><span class="sxs-lookup"><span data-stu-id="5ad88-288">1 for program starts</span></span></p>
<p><span data-ttu-id="5ad88-289">2 para errores de inicio</span><span class="sxs-lookup"><span data-stu-id="5ad88-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="5ad88-290">4 para apagados</span><span class="sxs-lookup"><span data-stu-id="5ad88-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="5ad88-291">8 para entrar en modo desconectado</span><span class="sxs-lookup"><span data-stu-id="5ad88-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="5ad88-292">16 para salir del modo desconectado para volver a conectarse a un servidor</span><span class="sxs-lookup"><span data-stu-id="5ad88-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="5ad88-293">Agrega cualquier combinación de esos números para activar los mensajes respectivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="5ad88-294">El valor predeterminado es 0x1F si no está en el registro.</span><span class="sxs-lookup"><span data-stu-id="5ad88-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-297">Valor predeterminado = 3000</span><span class="sxs-lookup"><span data-stu-id="5ad88-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-298">Especifica en milisegundos cuánto debe esperar la bandeja al intentar escribir en el registro de inicio si otro proceso lo está usando.</span><span class="sxs-lookup"><span data-stu-id="5ad88-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="5ad88-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-300">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-301">d:\files; C:\Documents and settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="5ad88-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-302">Una lista delimitada por puntos y comas de hasta cinco directorios para buscar archivos SFT portátiles antes de solicitar al usuario que seleccione un directorio.</span><span class="sxs-lookup"><span data-stu-id="5ad88-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="5ad88-303">La barra diagonal inversa al final de paths es opcional.</span><span class="sxs-lookup"><span data-stu-id="5ad88-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="5ad88-304">Este valor no está presente de forma predeterminada y debe establecerse manualmente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="5ad88-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-306">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="5ad88-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="5ad88-308">Válido únicamente en HKCU.</span><span class="sxs-lookup"><span data-stu-id="5ad88-308">Valid only under HKCU.</span></span> <span data-ttu-id="5ad88-309">Última ubicación en la que el usuario ha buscado al encontrar un archivo SFT para la importación de paquete.</span><span class="sxs-lookup"><span data-stu-id="5ad88-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="5ad88-310">Se establece automáticamente si el SFT se encuentra correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="5ad88-311">Se usa en las importaciones sucesivas cuando se intenta ubicar automáticamente los archivos de SFT.</span><span class="sxs-lookup"><span data-stu-id="5ad88-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-312">Clave compartida</span><span class="sxs-lookup"><span data-stu-id="5ad88-312">Shared Key</span></span>


<span data-ttu-id="5ad88-313">La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared controla los valores que se comparten en los componentes de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad88-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="5ad88-314">En la tabla siguiente se proporciona información sobre los valores de registro asociados a la clave compartida.</span><span class="sxs-lookup"><span data-stu-id="5ad88-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-315">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-317">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-318">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-319">DumpPath</span><span class="sxs-lookup"><span data-stu-id="5ad88-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-320">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-321">Valor predeterminado = C:</span><span class="sxs-lookup"><span data-stu-id="5ad88-321">Default=C:</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="5ad88-322">Ruta de acceso predeterminada para crear archivos de volcado al generar un minivolcado en una excepción.</span><span class="sxs-lookup"><span data-stu-id="5ad88-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="5ad88-323">El valor predeterminado es C:\ Si no se especifica.</span><span class="sxs-lookup"><span data-stu-id="5ad88-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="5ad88-324">El instalador del cliente establece esta clave en el &lt; Directorio de datos global de virtualización de la aplicación &gt; \Dumps.</span><span class="sxs-lookup"><span data-stu-id="5ad88-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="5ad88-325">El instalador del secuenciador establece esta clave en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-326">DumpPathSizeLimit</span><span class="sxs-lookup"><span data-stu-id="5ad88-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-328">1000</span><span class="sxs-lookup"><span data-stu-id="5ad88-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-329">Especifica la cantidad total máxima de espacio en megabytes que se puede usar para almacenar minivolcados.</span><span class="sxs-lookup"><span data-stu-id="5ad88-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="5ad88-330">Valor predeterminado = 1000 MB.</span><span class="sxs-lookup"><span data-stu-id="5ad88-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-331">Clave de red</span><span class="sxs-lookup"><span data-stu-id="5ad88-331">Network Key</span></span>


<span data-ttu-id="5ad88-332">La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network controla una variedad de parámetros relacionados con la red.</span><span class="sxs-lookup"><span data-stu-id="5ad88-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="5ad88-333">Esta clave la usa principalmente el agente de transporte de red.</span><span class="sxs-lookup"><span data-stu-id="5ad88-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="5ad88-334">En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave de red.</span><span class="sxs-lookup"><span data-stu-id="5ad88-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-335">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-336">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-337">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-338">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-339">Online</span><span class="sxs-lookup"><span data-stu-id="5ad88-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-341">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-342">Habilita o deshabilita el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad88-342">Enables or disables offline mode.</span></span> <span data-ttu-id="5ad88-343">Si se establece en 0, el cliente no se comunicará con los servidores de administración de App-V o servidores de publicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="5ad88-344">En las operaciones de desconexión, el cliente puede iniciar una aplicación cargada incluso cuando no está conectada a un servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad88-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="5ad88-345">En el modo sin conexión, el cliente no intenta conectarse a un servidor de administración de App-V o de publicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="5ad88-346">Debe permitir que las operaciones desconectadas puedan trabajar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad88-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="5ad88-347">El valor predeterminado es 1 habilitado (en línea) y 0 está deshabilitado (sin conexión).</span><span class="sxs-lookup"><span data-stu-id="5ad88-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="5ad88-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-350">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-351">Habilita o deshabilita la operación desconectada.</span><span class="sxs-lookup"><span data-stu-id="5ad88-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="5ad88-352">El valor predeterminado es 1 habilitado y 0 está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="5ad88-353">Cuando se habilitan las operaciones de desconexión, el cliente de App-V puede iniciar una aplicación cargada incluso cuando no está conectada a un servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad88-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-356">Valor predeterminado = 1000</span><span class="sxs-lookup"><span data-stu-id="5ad88-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-357">Este valor especifica el tiempo de espera de conexión TCP en milisegundos para determinar cuándo entrar en el modo de operaciones desconectado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="5ad88-358">Este valor se puede usar para invalidar el ConnectTimeout predeterminado de 20 segundos (el tiempo de espera de conexión de App-V para las transacciones de red) o el tiempo TCP del sistema de 25 segundos aproximadamente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="5ad88-359">Esto hace que el cliente esté en modo de operaciones desconectadas rápidamente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="5ad88-360">Aplicar en la próxima conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad88-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="5ad88-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-363">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-364">Aplicable solo si AllowDisconnectedOperation es 1, habilitado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="5ad88-365">Este valor determina si habrá un límite de tiempo para el tiempo durante el cual se permitirá que el cliente opere en operaciones no conectadas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="5ad88-366">1 = Limited.</span><span class="sxs-lookup"><span data-stu-id="5ad88-366">1=limited.</span></span> <span data-ttu-id="5ad88-367">0 = sin límites.</span><span class="sxs-lookup"><span data-stu-id="5ad88-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="5ad88-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-370">Valor predeterminado = 129600</span><span class="sxs-lookup"><span data-stu-id="5ad88-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-371">Indica cuántos minutos se puede usar una aplicación en modo de operación desconectada.</span><span class="sxs-lookup"><span data-stu-id="5ad88-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5ad88-372">Los valores válidos son de 1 a 999999 en días (1-1439998560 minutos).</span><span class="sxs-lookup"><span data-stu-id="5ad88-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="5ad88-373">El valor predeterminado es 90 días o 129.600 minutos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-374">Protocolo</span><span class="sxs-lookup"><span data-stu-id="5ad88-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-376">Valor predeterminado = 8</span><span class="sxs-lookup"><span data-stu-id="5ad88-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-377">Protocolo predeterminado para usar (TCP frente a SSL).</span><span class="sxs-lookup"><span data-stu-id="5ad88-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="5ad88-378">Configurar en el cuadro de diálogo Opciones.</span><span class="sxs-lookup"><span data-stu-id="5ad88-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-381">veinte</span><span class="sxs-lookup"><span data-stu-id="5ad88-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-382">Tiempo de espera de lectura para las transacciones de red, en segundos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="5ad88-383">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-386">veinte</span><span class="sxs-lookup"><span data-stu-id="5ad88-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-387">Tiempo de espera de escritura para las transacciones de red, en segundos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="5ad88-388">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="5ad88-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-391">veinte</span><span class="sxs-lookup"><span data-stu-id="5ad88-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-392">Conecte el tiempo de espera para las transacciones de red, en segundos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="5ad88-393">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="5ad88-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-396">2</span><span class="sxs-lookup"><span data-stu-id="5ad88-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-397">El número de veces para intentar restablecer una sesión interrumpida.</span><span class="sxs-lookup"><span data-stu-id="5ad88-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="5ad88-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-400">4,5</span><span class="sxs-lookup"><span data-stu-id="5ad88-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-401">Número de segundos que se va a esperar entre intentos para restablecer una sesión interrumpida.</span><span class="sxs-lookup"><span data-stu-id="5ad88-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-402">Clave http</span><span class="sxs-lookup"><span data-stu-id="5ad88-402">Http Key</span></span>


<span data-ttu-id="5ad88-403">La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http controla los parámetros relacionados con la transmisión de http.</span><span class="sxs-lookup"><span data-stu-id="5ad88-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="5ad88-404">Esta clave la usa principalmente el agente de transporte de red.</span><span class="sxs-lookup"><span data-stu-id="5ad88-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="5ad88-405">En la tabla siguiente se proporciona información sobre los valores del registro asociados a la clave http.</span><span class="sxs-lookup"><span data-stu-id="5ad88-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-406">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-407">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-408">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-409">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="5ad88-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-412">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-413">Controla el comportamiento de las transmisiones por secuencias de HTTP cuando se puede establecer una conexión con el servidor HTTP y el archivo de paquete ya no existe en el servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="5ad88-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="5ad88-414">Si el valor no existe o no se establece en 1, el cliente de App-V no le permite iniciar una aplicación que se haya cargado previamente en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5ad88-415">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-416">Si este valor se establece en 1, el cliente de App-V le permite iniciar una aplicación que se ha cargado previamente en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-417">Clave del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="5ad88-417">File System Key</span></span>


<span data-ttu-id="5ad88-418">Los valores contenidos en la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS controlan los parámetros del sistema de archivos de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad88-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="5ad88-419">En la tabla siguiente se proporciona información sobre los valores del registro asociados con la tecla AppFS.</span><span class="sxs-lookup"><span data-stu-id="5ad88-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-420">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-421">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-422">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-423">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="5ad88-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-426">4096</span><span class="sxs-lookup"><span data-stu-id="5ad88-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-427">Tamaño máximo en megabytes del archivo de caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="5ad88-428">Si cambia este valor en el registro, debe establecer State en 0 y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-429">FileName</span><span class="sxs-lookup"><span data-stu-id="5ad88-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-430">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="5ad88-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-432">Ubicación del archivo de caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-432">Location of file system cache file.</span></span> <span data-ttu-id="5ad88-433">Si cambia este valor en el registro, debe dejar los mismos y reiniciar, o establecer el estado a 0 y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-434">LetraDeUnidad</span><span class="sxs-lookup"><span data-stu-id="5ad88-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-435">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-436">P:</span><span class="sxs-lookup"><span data-stu-id="5ad88-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-437">Unidad donde se montará el sistema de archivos de App-V, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="5ad88-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="5ad88-438">Este valor lo establece el agente de escucha o el instalador, y lo lee el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-439">Estado</span><span class="sxs-lookup"><span data-stu-id="5ad88-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-441">0x100</span><span class="sxs-lookup"><span data-stu-id="5ad88-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-442">Estado del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-442">State of file system.</span></span> <span data-ttu-id="5ad88-443">Establezca en 0 y reinicie para borrar por completo la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="5ad88-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-445">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="5ad88-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-447">Ruta de vínculos simbólicos, establezca en HKCU.</span><span class="sxs-lookup"><span data-stu-id="5ad88-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="5ad88-448">No modifique (use el directorio de datos en configuración para cambiar).</span><span class="sxs-lookup"><span data-stu-id="5ad88-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="5ad88-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-450">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ad88-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-451">C:\Users\Public\Documents\SoftGrid Client\AppFS almacenamiento</span><span class="sxs-lookup"><span data-stu-id="5ad88-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-452">Ruta de acceso a los datos del sistema de archivos global.</span><span class="sxs-lookup"><span data-stu-id="5ad88-452">Path for global file system data.</span></span> <span data-ttu-id="5ad88-453">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="5ad88-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-456">Valor predeterminado = 90</span><span class="sxs-lookup"><span data-stu-id="5ad88-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-457">Especifica el porcentaje máximo del archivo de caché del sistema de archivos que puede bloquearse.</span><span class="sxs-lookup"><span data-stu-id="5ad88-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="5ad88-458">No modificar.</span><span class="sxs-lookup"><span data-stu-id="5ad88-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="5ad88-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-461">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-462">La característica de administración del espacio de caché del sistema de archivos usa un algoritmo LRU (el menos usado recientemente) y está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ad88-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="5ad88-463">Si el espacio necesario para un nuevo paquete excedería el espacio libre disponible en la memoria caché, el cliente de App-V usa esta característica para determinar qué paquetes existentes pueden eliminar de la caché con el fin de hacer sitio para el nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="5ad88-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="5ad88-464">El cliente elimina el paquete con la fecha de último acceso más antigua si es anterior al valor especificado en el valor de registro MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="5ad88-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="5ad88-465">Los valores son 0 (deshabilitado) y 1 (predeterminado, habilitado).</span><span class="sxs-lookup"><span data-stu-id="5ad88-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="5ad88-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-468">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-469">Para determinar cuándo se puede seleccionar el paquete para descartar, establezca este valor del registro para que sea igual al número mínimo de días que desea que transcurran desde que se por última vez al paquete.</span><span class="sxs-lookup"><span data-stu-id="5ad88-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="5ad88-470">Los paquetes que se han usado más recientemente no se descartan.</span><span class="sxs-lookup"><span data-stu-id="5ad88-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-471">Clave de permisos</span><span class="sxs-lookup"><span data-stu-id="5ad88-471">Permissions Key</span></span>


<span data-ttu-id="5ad88-472">Para ayudar a evitar que los usuarios hagan errores, los administradores pueden usar la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions para controlar el acceso a algunas acciones para los usuarios no administrativos, por ejemplo, para impedir que los usuarios descarguen accidentalmente programas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="5ad88-473">Los usuarios con derechos administrativos pueden otorgarse a sí mismos cualquiera de estos permisos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="5ad88-474">En sistemas compartidos, como un sistema de host de sesión de escritorio remoto (antes Terminal Server), tenga cuidado al conceder permisos adicionales a los usuarios, ya que algunos de estos permisos permitirán a los usuarios controlar las aplicaciones que usan todos los usuarios del sistema.</span><span class="sxs-lookup"><span data-stu-id="5ad88-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="5ad88-475">Los valores posibles para esta configuración son 1 (permitir) y 0 (no permitir).</span><span class="sxs-lookup"><span data-stu-id="5ad88-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="5ad88-476">La configuración de clave de permisos controla todas las interfaces que habilitan las acciones con nombre.</span><span class="sxs-lookup"><span data-stu-id="5ad88-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="5ad88-477">Esto incluye el cuadro de diálogo Opciones, SFTTray y SFTMime.</span><span class="sxs-lookup"><span data-stu-id="5ad88-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="5ad88-478">Esta configuración no afecta a los administradores.</span><span class="sxs-lookup"><span data-stu-id="5ad88-478">These settings do not affect administrators.</span></span> <span data-ttu-id="5ad88-479">En la tabla siguiente se proporciona información sobre los valores del registro asociados a la clave de permisos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="5ad88-480">Nombre tipo datos (ejemplos) Descripción ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="5ad88-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="5ad88-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-481">DWORD</span></span>

<span data-ttu-id="5ad88-482">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-482">Default=0</span></span>

<span data-ttu-id="5ad88-483">Un valor de 1 permite que los usuarios elijan una letra de unidad diferente para usarla como unidad del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5ad88-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="5ad88-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="5ad88-484">ChangeCacheSize</span></span>

<span data-ttu-id="5ad88-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-485">DWORD</span></span>

<span data-ttu-id="5ad88-486">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-486">Default=0</span></span>

<span data-ttu-id="5ad88-487">Un valor de 1 permite a los usuarios cambiar el tamaño de la caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="5ad88-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="5ad88-488">ChangeLogSettings</span></span>

<span data-ttu-id="5ad88-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-489">DWORD</span></span>

<span data-ttu-id="5ad88-490">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-490">Default=0</span></span>

<span data-ttu-id="5ad88-491">Un valor de 1 permite a los usuarios modificar el nivel de registro, cambiar su ubicación y restablecerlo a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ad88-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="5ad88-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-492">AddApp</span></span>

<span data-ttu-id="5ad88-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-493">DWORD</span></span>

<span data-ttu-id="5ad88-494">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-494">Default=0</span></span>

<span data-ttu-id="5ad88-495">Un valor de 1 permite a los usuarios agregar aplicaciones de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="5ad88-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="5ad88-496">Esto no afecta a las aplicaciones que se agregan mediante la actualización de publicaciones ni impide que los usuarios se inicien (y agregan implícitamente) aplicaciones que aún no se han agregado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="5ad88-497">Los valores son 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="5ad88-497">Values are 0 or 1.</span></span>

<span data-ttu-id="5ad88-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-498">LoadApp</span></span> 

<span data-ttu-id="5ad88-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-499">DWORD</span></span> 

<span data-ttu-id="5ad88-500">,0</span><span class="sxs-lookup"><span data-stu-id="5ad88-500">0</span></span>

<span data-ttu-id="5ad88-501">No permite que un usuario cargue una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="5ad88-502">Este es el valor predeterminado para los hosts de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="5ad88-503">Si es un usuario móvil, es posible que desee cargar completamente las aplicaciones en la caché para usarlas durante la operación de desconexión o el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad88-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="5ad88-504">Para transmitir aplicaciones desde el servidor de administración de App-V o del servidor de streaming de App-V, debe estar conectado a un servidor para cargar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5ad88-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="5ad88-505">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-505">1</span></span>

<span data-ttu-id="5ad88-506">Permite que un usuario cargue una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-506">Allows a user to load an application.</span></span> <span data-ttu-id="5ad88-507">Este es el valor predeterminado para los escritorios de Windows.</span><span class="sxs-lookup"><span data-stu-id="5ad88-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="5ad88-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-508">UnloadApp</span></span> 

<span data-ttu-id="5ad88-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-509">DWORD</span></span> 

<span data-ttu-id="5ad88-510">,0</span><span class="sxs-lookup"><span data-stu-id="5ad88-510">0</span></span>

<span data-ttu-id="5ad88-511">No permite que un usuario descargue una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="5ad88-512">Al cargar o descargar un paquete, todas las aplicaciones del paquete se cargan o se quitan de la caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="5ad88-513">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-513">1</span></span>

<span data-ttu-id="5ad88-514">Permite a un usuario descargar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="5ad88-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-515">LockApp</span></span> 

<span data-ttu-id="5ad88-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-516">DWORD</span></span> 

<span data-ttu-id="5ad88-517">,0</span><span class="sxs-lookup"><span data-stu-id="5ad88-517">0</span></span>

<span data-ttu-id="5ad88-518">No permite que un usuario bloquee y desbloquee una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="5ad88-519">Este es el valor predeterminado para los hosts de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="5ad88-520">No se puede quitar una aplicación bloqueada de la caché para hacer sitio para nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5ad88-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="5ad88-521">Para quitar una aplicación bloqueada del escritorio de App-V o del cliente para servicios de escritorio remoto (antes, Terminal Services), debe desbloquearla.</span><span class="sxs-lookup"><span data-stu-id="5ad88-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="5ad88-522">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-522">1</span></span>

<span data-ttu-id="5ad88-523">Permite que un usuario bloquee y desbloquee una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="5ad88-524">Este es el valor predeterminado para los escritorios de Windows.</span><span class="sxs-lookup"><span data-stu-id="5ad88-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="5ad88-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="5ad88-525">ManageTypes</span></span> 

<span data-ttu-id="5ad88-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-526">DWORD</span></span> 

<span data-ttu-id="5ad88-527">,0</span><span class="sxs-lookup"><span data-stu-id="5ad88-527">0</span></span>

<span data-ttu-id="5ad88-528">No permite que un usuario agregue, edite o quite asociaciones de tipo de archivo solo para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="5ad88-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="5ad88-529">Este es el valor predeterminado para los hosts de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="5ad88-530">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-530">1</span></span>

<span data-ttu-id="5ad88-531">Permite a un usuario agregar, editar y quitar asociaciones de tipos de archivo para ese usuario únicamente y no de forma global.</span><span class="sxs-lookup"><span data-stu-id="5ad88-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="5ad88-532">Este es el valor predeterminado para los escritorios de Windows.</span><span class="sxs-lookup"><span data-stu-id="5ad88-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="5ad88-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="5ad88-533">RefreshServer</span></span> 

<span data-ttu-id="5ad88-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-534">DWORD</span></span> 

<span data-ttu-id="5ad88-535">,0</span><span class="sxs-lookup"><span data-stu-id="5ad88-535">0</span></span>

<span data-ttu-id="5ad88-536">No permite que un usuario desencadene una actualización de la configuración MIME.</span><span class="sxs-lookup"><span data-stu-id="5ad88-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="5ad88-537">Este es el valor predeterminado para los hosts de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5ad88-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="5ad88-538">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-538">1</span></span>

<span data-ttu-id="5ad88-539">Permite a un usuario desencadenar una actualización de la configuración de MIME.</span><span class="sxs-lookup"><span data-stu-id="5ad88-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="5ad88-540">Este es el valor predeterminado para los escritorios de Windows.</span><span class="sxs-lookup"><span data-stu-id="5ad88-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="5ad88-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="5ad88-541">UpdateOSDFile</span></span>

<span data-ttu-id="5ad88-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-542">DWORD</span></span>

<span data-ttu-id="5ad88-543">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-543">Default= 0</span></span>

<span data-ttu-id="5ad88-544">Un valor de 1 permite a un usuario usar un archivo OSD modificado.</span><span class="sxs-lookup"><span data-stu-id="5ad88-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="5ad88-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-545">ImportApp</span></span> 

<span data-ttu-id="5ad88-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-546">DWORD</span></span> 

<span data-ttu-id="5ad88-547">,0</span><span class="sxs-lookup"><span data-stu-id="5ad88-547">0</span></span>

<span data-ttu-id="5ad88-548">No permite que un usuario importe aplicaciones en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="5ad88-549">La diferencia entre cargar e importar es que cuando se desencadena una carga, el cliente obtiene el paquete de la ubicación configurada en la URL OSD, ASR o override.</span><span class="sxs-lookup"><span data-stu-id="5ad88-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="5ad88-550">Al usar Import, debe especificarse una ubicación desde la que obtener el paquete.</span><span class="sxs-lookup"><span data-stu-id="5ad88-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="5ad88-551">uno</span><span class="sxs-lookup"><span data-stu-id="5ad88-551">1</span></span>

<span data-ttu-id="5ad88-552">Permite a un usuario importar aplicaciones en la caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="5ad88-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="5ad88-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="5ad88-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-554">DWORD</span></span>

<span data-ttu-id="5ad88-555">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-555">Default=0</span></span>

<span data-ttu-id="5ad88-556">Un valor de 1 permite a los usuarios modificar la configuración de actualización de los servidores (actualizar al iniciar sesión y actualizar periódicamente).</span><span class="sxs-lookup"><span data-stu-id="5ad88-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="5ad88-557">Esto no implica que el usuario pueda modificar otras opciones de configuración del servidor (Path, host, etc.).</span><span class="sxs-lookup"><span data-stu-id="5ad88-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="5ad88-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="5ad88-558">ManageServers</span></span>

<span data-ttu-id="5ad88-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-559">DWORD</span></span>

<span data-ttu-id="5ad88-560">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-560">Default=0</span></span>

<span data-ttu-id="5ad88-561">El valor 1 permite al usuario agregar, editar y quitar servidores, excepto editar la configuración de actualización, que está controlada por el permiso ChangeRefreshSettings.</span><span class="sxs-lookup"><span data-stu-id="5ad88-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="5ad88-562">PublishShortcut</span><span class="sxs-lookup"><span data-stu-id="5ad88-562">PublishShortcut</span></span>

<span data-ttu-id="5ad88-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-563">DWORD</span></span>

<span data-ttu-id="5ad88-564">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-564">Default=0</span></span>

<span data-ttu-id="5ad88-565">Un valor de 1 permite a los usuarios publicar accesos directos a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ad88-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="5ad88-566">Esto no afecta a los métodos abreviados que se publican durante una actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="5ad88-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="5ad88-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="5ad88-567">ViewAllApplications</span></span>

<span data-ttu-id="5ad88-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-568">DWORD</span></span>

<span data-ttu-id="5ad88-569">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-569">Default=0</span></span>

<span data-ttu-id="5ad88-570">Un valor de 1 muestra todas las aplicaciones a través de la interfaz de usuario; de lo contrario, solo se mostrarán las aplicaciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ad88-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="5ad88-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-571">RepairApp</span></span>

<span data-ttu-id="5ad88-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-572">DWORD</span></span>

<span data-ttu-id="5ad88-573">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-573">Default=1</span></span>

<span data-ttu-id="5ad88-574">Un valor de 1 permite al usuario usar la acción de reparación en las aplicaciones de SFTMime o en la consola de administración de clientes.</span><span class="sxs-lookup"><span data-stu-id="5ad88-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="5ad88-575">Al reparar una aplicación, se elimina la configuración de usuario personalizada y se restaura la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ad88-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="5ad88-576">Esta acción no cambia ni elimina accesos directos ni asociaciones de tipos de archivo, y no quita la aplicación de la caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="5ad88-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-577">ClearApp</span></span>

<span data-ttu-id="5ad88-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-578">DWORD</span></span>

<span data-ttu-id="5ad88-579">Valor predeterminado = 1</span><span class="sxs-lookup"><span data-stu-id="5ad88-579">Default=1</span></span>

<span data-ttu-id="5ad88-580">Un valor de 1 permite al usuario usar la acción borrar en las aplicaciones de SFTMime o en la consola de administración de clientes.</span><span class="sxs-lookup"><span data-stu-id="5ad88-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="5ad88-581">Al borrar una aplicación de la consola, ya no podrá usarla.</span><span class="sxs-lookup"><span data-stu-id="5ad88-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="5ad88-582">Sin embargo, la aplicación permanece en la caché y sigue estando disponible para otros usuarios en el mismo sistema.</span><span class="sxs-lookup"><span data-stu-id="5ad88-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="5ad88-583">Después de una actualización de publicación, las aplicaciones desactivadas volverán a estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="5ad88-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="5ad88-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="5ad88-584">DeleteApp</span></span>

<span data-ttu-id="5ad88-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-585">DWORD</span></span>

<span data-ttu-id="5ad88-586">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-586">Default=0</span></span>

<span data-ttu-id="5ad88-587">Un valor de 1 permite al usuario usar la acción eliminar en las aplicaciones de SFTMime o en la consola de administración de clientes.</span><span class="sxs-lookup"><span data-stu-id="5ad88-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="5ad88-588">Al eliminar una aplicación, la aplicación seleccionada dejará de estar disponible para los usuarios de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="5ad88-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="5ad88-589">Los accesos directos y las asociaciones de los tipos de archivo se eliminan y la aplicación se elimina de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5ad88-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="5ad88-590">Sin embargo, si otra aplicación hace referencia a datos en la caché del sistema de archivos o a los datos de configuración de la aplicación seleccionada, estos elementos no se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="5ad88-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="5ad88-591">Después de una actualización de publicación, las aplicaciones eliminadas volverán a estar disponibles para usted.</span><span class="sxs-lookup"><span data-stu-id="5ad88-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="5ad88-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="5ad88-592">ToggleOfflineMode</span></span>

<span data-ttu-id="5ad88-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-593">DWORD</span></span>

<span data-ttu-id="5ad88-594">Un valor de 1 permite a los usuarios seleccionar la ejecución del cliente en modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5ad88-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="5ad88-595">En el modo sin conexión, el cliente de virtualización de aplicaciones puede iniciar una aplicación cargada incluso cuando no está conectada a un servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5ad88-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="5ad88-596">Configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="5ad88-596">Custom Settings</span></span>


<span data-ttu-id="5ad88-597">La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contiene valores específicos para los componentes de front-end.</span><span class="sxs-lookup"><span data-stu-id="5ad88-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="5ad88-598">Todas las configuraciones personalizadas se almacenan como cadenas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="5ad88-599">En la siguiente tabla se proporciona información sobre los valores del registro asociados a la clave CustomSettings.</span><span class="sxs-lookup"><span data-stu-id="5ad88-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-600">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-601">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-602">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-603">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="5ad88-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-606">Valor predeterminado = 30</span><span class="sxs-lookup"><span data-stu-id="5ad88-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-607">Tiempo en segundos durante el que el área de notificación de Application Virtualization mostrará mensajes de error como &quot; error al iniciar &quot; .</span><span class="sxs-lookup"><span data-stu-id="5ad88-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="5ad88-608">Valor mínimo de 1.</span><span class="sxs-lookup"><span data-stu-id="5ad88-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="5ad88-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-611">Valor predeterminado = 10</span><span class="sxs-lookup"><span data-stu-id="5ad88-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="5ad88-612">Tiempo en segundos en el que el área de notificación de appvmed mostrará mensajes de éxito, como el &quot; lanzamiento &quot; de Word o el &quot; cierre de Excel &quot; .</span><span class="sxs-lookup"><span data-stu-id="5ad88-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="5ad88-613">Si es 0, se suprimirán esos mensajes.</span><span class="sxs-lookup"><span data-stu-id="5ad88-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="5ad88-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-616">Valor predeterminado = 0</span><span class="sxs-lookup"><span data-stu-id="5ad88-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-617">0 = Mostrar bandeja cuando se usan aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="5ad88-618">1 = Mostrar bandeja siempre.</span><span class="sxs-lookup"><span data-stu-id="5ad88-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="5ad88-619">2 = nunca Mostrar bandeja.</span><span class="sxs-lookup"><span data-stu-id="5ad88-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="5ad88-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5ad88-622">Cuando está presente y se establece en un valor de 1, permite que las aplicaciones de actualización de elemento de menú se muestren en el menú de bandeja y que el usuario pueda obtener acceso a ellas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="5ad88-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="5ad88-625">Cuando está presente y se establece en un valor de 1, permite que las aplicaciones de carga de elemento de menú se muestren en el menú de bandeja y que el usuario pueda obtener acceso a ellas.</span><span class="sxs-lookup"><span data-stu-id="5ad88-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-626">Configuración de informes</span><span class="sxs-lookup"><span data-stu-id="5ad88-626">Reporting Settings</span></span>


<span data-ttu-id="5ad88-627">La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contiene valores específicos para la creación de informes en un servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ad88-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="5ad88-628">En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave de informe.</span><span class="sxs-lookup"><span data-stu-id="5ad88-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ad88-629">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ad88-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-630">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad88-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-631">Datos (ejemplos)</span><span class="sxs-lookup"><span data-stu-id="5ad88-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="5ad88-632">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad88-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ad88-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="5ad88-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-635">Valor predeterminado = 20</span><span class="sxs-lookup"><span data-stu-id="5ad88-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-636">Este valor especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes.</span><span class="sxs-lookup"><span data-stu-id="5ad88-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="5ad88-637">El tamaño se aplica a la memoria caché en memoria.</span><span class="sxs-lookup"><span data-stu-id="5ad88-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="5ad88-638">Cuando se alcance el límite, el archivo de registro se retirará.</span><span class="sxs-lookup"><span data-stu-id="5ad88-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="5ad88-639">Cuando se agrega un nuevo registro (en la parte inferior de la lista), se eliminarán uno o más de los registros más antiguos (en la parte superior de la lista) para dejar espacio.</span><span class="sxs-lookup"><span data-stu-id="5ad88-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="5ad88-640">Se registrará una advertencia en el registro del cliente y en el registro de eventos la primera vez que se produzca, y no se registrará de nuevo hasta que la caché se haya borrado correctamente durante la transmisión y el registro se haya rellenado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ad88-641">BlockSize</span><span class="sxs-lookup"><span data-stu-id="5ad88-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="5ad88-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-643">Valor predeterminado = 65536</span><span class="sxs-lookup"><span data-stu-id="5ad88-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ad88-644">Este valor especifica el tamaño máximo en bytes que se va a transmitir al servidor a la vez en la actualización de publicaciones, para evitar errores de transmisión permanentes cuando el registro haya alcanzado un tamaño significativo.</span><span class="sxs-lookup"><span data-stu-id="5ad88-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="5ad88-645">El valor predeterminado es 65536.</span><span class="sxs-lookup"><span data-stu-id="5ad88-645">The default value is 65536.</span></span> <span data-ttu-id="5ad88-646">Cuando se transmiten datos del informe al servidor, un bloque de registros de la aplicación (menor o igual que el tamaño de bloque en bytes de datos XML) se quitará de la caché y se enviará al servidor.</span><span class="sxs-lookup"><span data-stu-id="5ad88-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="5ad88-647">Cada bloque incluirá los datos generales de los clientes y los datos de la lista de paquetes globales, y estos no se verán incluidos en los cálculos de tamaño de bloque. es posible que haya una lista de paquetes extremadamente grande para que se produzcan errores de transmisión con un ancho de banda bajo o conexiones no confiables.</span><span class="sxs-lookup"><span data-stu-id="5ad88-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ad88-648">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ad88-648">Related topics</span></span>


[<span data-ttu-id="5ad88-649">Referencia del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5ad88-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)









