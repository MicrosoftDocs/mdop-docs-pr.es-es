---
title: Acerca de la pestaña Implementación
description: Acerca de la pestaña Implementación
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819961"
---
# <span data-ttu-id="fc21a-103">Acerca de la pestaña Implementación</span><span class="sxs-lookup"><span data-stu-id="fc21a-103">About the Deployment Tab</span></span>


<span data-ttu-id="fc21a-104">Use la pestaña **implementación** en la consola de Application Virtualization Sequencer para cambiar la información de una aplicación que va a secuenciar.</span><span class="sxs-lookup"><span data-stu-id="fc21a-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="fc21a-105">Esta pestaña contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="fc21a-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="fc21a-106">Dirección URL del servidor</span><span class="sxs-lookup"><span data-stu-id="fc21a-106">Server URL</span></span>


<span data-ttu-id="fc21a-107">Use los controles de **dirección URL del servidor** para especificar los valores de configuración del servidor de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="fc21a-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc21a-108">Control</span><span class="sxs-lookup"><span data-stu-id="fc21a-108">Control</span></span></th>
<th align="left"><span data-ttu-id="fc21a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc21a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fc21a-110">Protocolo</span><span class="sxs-lookup"><span data-stu-id="fc21a-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-111">Le permite seleccionar el protocolo que transmitirá el paquete de aplicación secuenciado de un servidor de aplicaciones virtual a un cliente de escritorio de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fc21a-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="fc21a-112">Están disponibles los siguientes protocolos:</span><span class="sxs-lookup"><span data-stu-id="fc21a-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="fc21a-113">RTSP </strong> : el valor predeterminado especifica que el protocolo de transmisión por secuencias en tiempo real controla el intercambio de aplicaciones habilitadas para la virtualización.</span><span class="sxs-lookup"><span data-stu-id="fc21a-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="fc21a-114">RTSPs </strong> : especifica que el protocolo de transmisión por secuencias en tiempo real con seguridad de la capa de transporte controla el intercambio de un paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="fc21a-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="fc21a-115">Archivo </strong> : especifica que la aplicación secuenciada se transmitirá desde un recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="fc21a-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="fc21a-116">HTTPS </strong> : especifica que el protocolo de transporte de hipertexto seguro controla el intercambio de un paquete.</span><span class="sxs-lookup"><span data-stu-id="fc21a-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fc21a-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc21a-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-118">Le permite seleccionar el servidor de aplicaciones virtual o el equilibrador de carga delante de un grupo de servidores de aplicaciones virtuales que transmitirán el paquete de software a un cliente de escritorio de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fc21a-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="fc21a-119">Debe completar este elemento para crear un paquete de aplicación de secuencia, pero puede cambiar la variable de entorno% SFT_SOFTGRIDSERVER% predeterminada al nombre de host o la dirección IP reales de un servidor de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="fc21a-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fc21a-120">Nota</span><span class="sxs-lookup"><span data-stu-id="fc21a-120">Note</span></span></strong><br/><p><span data-ttu-id="fc21a-121">Si decide no especificar una dirección IP o un nombre de host estático, en cada cliente de escritorio de virtualización de aplicaciones debe configurar una variable de entorno denominada SFT_SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="fc21a-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="fc21a-122">Su valor debe ser el nombre de host o la dirección IP del servidor de aplicaciones virtual o del equilibrador de carga que es este cliente&#39;es el origen de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fc21a-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="fc21a-123">Debe convertir esta variable de entorno en una variable del sistema en lugar de una variable de usuario.</span><span class="sxs-lookup"><span data-stu-id="fc21a-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="fc21a-124">Cualquier sesión del cliente de escritorio de virtualización de aplicaciones que se esté ejecutando en este equipo durante la asignación de esta variable debe cerrarse y, a continuación, abrirse para que la sesión reanudada tenga conocimiento de su nuevo origen de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc21a-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fc21a-125">Port</span><span class="sxs-lookup"><span data-stu-id="fc21a-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-126">Le permite especificar el puerto en el que escuchará el servidor de aplicaciones virtual o el equilibrador de carga para un cliente de escritorio de virtualización de aplicaciones&#39;s para el paquete.</span><span class="sxs-lookup"><span data-stu-id="fc21a-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="fc21a-127">Esta información es necesaria para crear un paquete, pero puedes cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="fc21a-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="fc21a-128">El puerto predeterminado es 554.</span><span class="sxs-lookup"><span data-stu-id="fc21a-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fc21a-129">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="fc21a-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-130">Le permite especificar la ruta de acceso relativa en el servidor de aplicaciones virtual donde se almacena el paquete de software y desde el que se transmitirá.</span><span class="sxs-lookup"><span data-stu-id="fc21a-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="fc21a-131">Esta información es necesaria para crear un paquete si el archivo SFT se almacena en un subdirectorio de contenido. de lo contrario, esta información no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="fc21a-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fc21a-132">Sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="fc21a-132">Operating Systems</span></span>


<span data-ttu-id="fc21a-133">Use los controles de **sistemas operativos** para especificar los requisitos del sistema operativo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc21a-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="fc21a-134">Si un cliente de escritorio de virtualización de aplicaciones no puede admitir ninguno de los sistemas operativos seleccionados, la aplicación no se iniciará.</span><span class="sxs-lookup"><span data-stu-id="fc21a-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc21a-135">Controles</span><span class="sxs-lookup"><span data-stu-id="fc21a-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="fc21a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc21a-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fc21a-137">Sistemas operativos disponibles</span><span class="sxs-lookup"><span data-stu-id="fc21a-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-138">Muestra una lista de los sistemas operativos que pueden admitir las aplicaciones del paquete.</span><span class="sxs-lookup"><span data-stu-id="fc21a-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fc21a-139">Sistemas operativos seleccionados</span><span class="sxs-lookup"><span data-stu-id="fc21a-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-140">Muestra una lista de los sistemas operativos seleccionados que admiten las aplicaciones del paquete.</span><span class="sxs-lookup"><span data-stu-id="fc21a-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fc21a-141">Opciones de salida</span><span class="sxs-lookup"><span data-stu-id="fc21a-141">Output Options</span></span>


<span data-ttu-id="fc21a-142">Use los controles de **Opciones de resultados** para especificar las opciones de salida de la aplicación que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="fc21a-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc21a-143">Control</span><span class="sxs-lookup"><span data-stu-id="fc21a-143">Control</span></span></th>
<th align="left"><span data-ttu-id="fc21a-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc21a-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fc21a-145">Algoritmo de compresión</span><span class="sxs-lookup"><span data-stu-id="fc21a-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-146">Usar para seleccionar el método para comprimir el archivo SFT para la transmisión por secuencias a través de una red.</span><span class="sxs-lookup"><span data-stu-id="fc21a-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="fc21a-147">Seleccione uno de los siguientes métodos de compresión:</span><span class="sxs-lookup"><span data-stu-id="fc21a-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="fc21a-148">Comprimido </strong> : especifica que el archivo SFT se comprimirá en <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> formato zlib </a> .</span><span class="sxs-lookup"><span data-stu-id="fc21a-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="fc21a-149">No comprimido </strong> : es el valor predeterminado; especifica que el archivo SFT no se comprimirá.</span><span class="sxs-lookup"><span data-stu-id="fc21a-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fc21a-150">Exigir descriptores de seguridad</span><span class="sxs-lookup"><span data-stu-id="fc21a-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-151">Seleccione esta opción para aplicar los descriptores de seguridad de las aplicaciones en el paquete después de que se implemente en el cliente.</span><span class="sxs-lookup"><span data-stu-id="fc21a-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fc21a-152">Generar el paquete de Microsoft Windows Installer (MSI)</span><span class="sxs-lookup"><span data-stu-id="fc21a-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fc21a-153">Seleccione para instalar o implementar un paquete de aplicación de secuencia con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fc21a-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="fc21a-154">Si ha realizado algún cambio con el secuenciador, los cambios no se incluirán en el archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fc21a-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="fc21a-155">El archivo de Windows Installer siempre se creará con el archivo. SFT guardado en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="fc21a-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fc21a-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc21a-156">Related topics</span></span>


[<span data-ttu-id="fc21a-157">Cómo cambiar las propiedades de implementación</span><span class="sxs-lookup"><span data-stu-id="fc21a-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="fc21a-158">Consola de secuenciador</span><span class="sxs-lookup"><span data-stu-id="fc21a-158">Sequencer Console</span></span>](sequencer-console.md)









