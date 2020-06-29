---
title: Introducción a la virtualización de aplicaciones
description: Introducción a la virtualización de aplicaciones
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816061"
---
# <span data-ttu-id="dd10b-103">Introducción a la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="dd10b-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="dd10b-104">Microsoft Application Virtualization (App-V) puede hacer que las aplicaciones estén disponibles para los equipos de los usuarios finales sin tener que instalar las aplicaciones directamente en esos equipos.</span><span class="sxs-lookup"><span data-stu-id="dd10b-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="dd10b-105">Esto es posible gracias a un proceso conocido como *la secuenciación de la aplicación*, que permite que cada aplicación se ejecute en su propio entorno virtual independiente en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="dd10b-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="dd10b-106">Las aplicaciones secuenciadas están aisladas entre sí.</span><span class="sxs-lookup"><span data-stu-id="dd10b-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="dd10b-107">Esto elimina los conflictos de la aplicación, pero las aplicaciones todavía pueden interactuar con el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="dd10b-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="dd10b-108">El cliente de App-V es la característica que permite que el usuario final interactúe con las aplicaciones después de que se hayan publicado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="dd10b-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="dd10b-109">El cliente administra el entorno virtual en el que se ejecutan las aplicaciones virtualizadas en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="dd10b-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="dd10b-110">Una vez instalado el cliente en un equipo, las aplicaciones deben estar disponibles para el equipo a través de un proceso conocido como *publicación*, que permite al usuario final ejecutar las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="dd10b-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="dd10b-111">El proceso de publicación copia los iconos de la aplicación virtual y los accesos directos en el equipo (por lo general, en el escritorio de Windows o en el menú **Inicio** ) y también copia la definición del paquete y la información de la Asociación de tipos de archivo en el equipo.</span><span class="sxs-lookup"><span data-stu-id="dd10b-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="dd10b-112">La publicación también hace que el contenido del paquete de la aplicación esté disponible para el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="dd10b-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="dd10b-113">El contenido del paquete de la aplicación virtual se puede copiar en uno o varios servidores de virtualización de aplicaciones para que pueda transmitirse a los clientes a petición y almacenarse en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="dd10b-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="dd10b-114">Los servidores de archivos y los servidores web también se pueden usar como servidores de transmisión por secuencias o el contenido se puede copiar directamente en el equipo del usuario final; por ejemplo, si usa un sistema de distribución de software electrónico, como Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dd10b-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="dd10b-115">En una implementación de varios servidores, mantener el contenido del paquete y mantenerlo actualizado en todos los servidores de transmisión requiere una solución completa de administración de paquetes.</span><span class="sxs-lookup"><span data-stu-id="dd10b-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="dd10b-116">Según el tamaño de su organización, es posible que tenga muchas aplicaciones virtuales disponibles para los usuarios finales de todo el mundo.</span><span class="sxs-lookup"><span data-stu-id="dd10b-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="dd10b-117">Administrar los paquetes para asegurarse de que las aplicaciones adecuadas estén disponibles para todos los usuarios donde y cuando necesiten tener acceso a ellos es por lo tanto un requisito importante.</span><span class="sxs-lookup"><span data-stu-id="dd10b-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="dd10b-118">Características del sistema de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dd10b-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="dd10b-119">En la siguiente tabla se describen las características principales del sistema de administración de virtualización de aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dd10b-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dd10b-120">Característica</span><span class="sxs-lookup"><span data-stu-id="dd10b-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="dd10b-121">Función</span><span class="sxs-lookup"><span data-stu-id="dd10b-121">Function</span></span></th>
<th align="left"><span data-ttu-id="dd10b-122">Información adicional</span><span class="sxs-lookup"><span data-stu-id="dd10b-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd10b-123">Servidor de Microsoft Application Virtualization Management</span><span class="sxs-lookup"><span data-stu-id="dd10b-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-124">Responsable de transmitir por secuencias el contenido del paquete y de publicar los accesos directos y las asociaciones de los tipos de archivo en el cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd10b-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-125">El servidor de administración de virtualización de aplicaciones admite actualizaciones activas, administración de licencias y una base de datos que se pueden usar para los informes.</span><span class="sxs-lookup"><span data-stu-id="dd10b-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="dd10b-126">Carpeta de contenido </strong></span><span class="sxs-lookup"><span data-stu-id="dd10b-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-127">Indica la ubicación de los paquetes de virtualización de aplicaciones para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="dd10b-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-128">Esta carpeta puede encontrarse en un recurso compartido en el servidor de administración de virtualización de aplicaciones o fuera de él.</span><span class="sxs-lookup"><span data-stu-id="dd10b-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd10b-129">Consola de administración de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dd10b-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-130">Esta consola es una herramienta de administración de complementos de 3,0 MMC que se usa para la administración de Microsoft Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="dd10b-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-131">Esta herramienta se puede instalar en el servidor de Microsoft Application Virtualization o en una estación de trabajo independiente que tenga Microsoft Management Console (MMC) 3.0 y Microsoft. NETFramework 2,0 instalado.</span><span class="sxs-lookup"><span data-stu-id="dd10b-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd10b-132">Servicio Web de administración de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dd10b-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-133">Responsable de comunicar las solicitudes de lectura y escritura al almacén de datos de la virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd10b-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-134">El servicio Web de administración se puede instalar en el servidor de Microsoft Application Virtualization Management o en un equipo independiente que tenga instalado Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="dd10b-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd10b-135">Almacén de datos de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dd10b-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-136">La base de datos de App-V SQL Server responsable de almacenar toda la información relacionada con la infraestructura de virtualización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd10b-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-137">Esta información incluye todos los registros de aplicaciones, asignaciones de aplicaciones y los grupos responsables de administrar el entorno de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd10b-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd10b-138">Servidor de streaming de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dd10b-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-139">Responsable de hospedar los paquetes de Application Virtualization para la transmisión por secuencias a los clientes de una sucursal, donde el vínculo al servidor de Application Virtualization Management se considera una conexión de redes de área extensa (WAN).</span><span class="sxs-lookup"><span data-stu-id="dd10b-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-140">Este servidor solo contiene funcionalidad de transmisión por secuencias y no proporciona ni la consola de administración de virtualización de aplicaciones ni el servicio Web de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd10b-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd10b-141">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="dd10b-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-142">El secuenciador se usa para supervisar y capturar la instalación de aplicaciones para crear paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="dd10b-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-143">La salida consta de los iconos de la aplicación, un archivo. OSD que contiene información sobre la definición del paquete, un archivo de manifiesto del paquete y el archivo. SFT que contiene los archivos de contenido del programa de aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd10b-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd10b-144">Cliente de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="dd10b-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-145">El cliente de escritorio de Application Virtualization y el cliente de virtualización de aplicaciones para servicios de escritorio remoto proporcionan y administran el entorno virtual de las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="dd10b-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd10b-146">El cliente de Microsoft Application Virtualization administra la transmisión de paquetes en la memoria caché, la actualización de publicaciones, el transporte y toda la interacción con los servidores de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd10b-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





