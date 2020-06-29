---
title: Modificar el puerto en el que el servicio AGPM escucha
description: Modificar el puerto en el que el servicio AGPM escucha
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820490"
---
# <span data-ttu-id="76ab7-103">Modificar el puerto en el que el servicio AGPM escucha</span><span class="sxs-lookup"><span data-stu-id="76ab7-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="76ab7-104">El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción.</span><span class="sxs-lookup"><span data-stu-id="76ab7-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="76ab7-105">De forma predeterminada, el servicio AGPM escucha en el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="76ab7-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="76ab7-106">Puede cambiar este puerto modificando el archivo de índice de archivo de administración avanzada de directivas de grupo (AGPM) para cada archivo.</span><span class="sxs-lookup"><span data-stu-id="76ab7-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="76ab7-107">**Nota:**  Antes de modificar el puerto en el que el servicio AGPM escucha, se recomienda que haga una copia de seguridad del archivo de índice de archivo de AGPM (gpostate.xml).</span><span class="sxs-lookup"><span data-stu-id="76ab7-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="76ab7-108">Este archivo se encuentra en la carpeta especificada como la ruta de acceso al archivo durante la instalación de administración avanzada de directivas de grupo-servidor.</span><span class="sxs-lookup"><span data-stu-id="76ab7-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="76ab7-109">De forma predeterminada, esta ubicación de este archivo es% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="76ab7-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="76ab7-110">Si no sabe qué equipo hospeda el archivo, puede seguir el procedimiento para modificar la ruta de archivo para mostrar la ruta de archivo actual.</span><span class="sxs-lookup"><span data-stu-id="76ab7-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="76ab7-111">Para obtener más información, vea [modificar la ruta de acceso del archivo](modify-the-archive-path.md).</span><span class="sxs-lookup"><span data-stu-id="76ab7-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="76ab7-112">Para completar este procedimiento, se necesita una cuenta de usuario con acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y el archivo de índice de archivo.</span><span class="sxs-lookup"><span data-stu-id="76ab7-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="76ab7-113">Para modificar el puerto en el que escucha el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="76ab7-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="76ab7-114">En el equipo que hospeda el archivo, abra el archivo de índice de archivo (gpostate.xml) en un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="76ab7-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="76ab7-115">En el archivo, busque **AGPM: Port = "4600"**.</span><span class="sxs-lookup"><span data-stu-id="76ab7-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="76ab7-116">Reemplazar **4600** por el puerto en el que debería escuchar el servicio AGPM; después, guarde y cierre el archivo.</span><span class="sxs-lookup"><span data-stu-id="76ab7-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="76ab7-117">En el servidor de AGPM, reinicie el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="76ab7-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="76ab7-118">(Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service.md)).</span><span class="sxs-lookup"><span data-stu-id="76ab7-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="76ab7-119">Modifique el puerto en la conexión del servidor de AGPM para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="76ab7-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="76ab7-120">Para obtener más información, vea [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="76ab7-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="76ab7-121">Repita este paso para cada archivo y servidor AGPM.</span><span class="sxs-lookup"><span data-stu-id="76ab7-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="76ab7-122">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="76ab7-122">Additional references</span></span>

-   [<span data-ttu-id="76ab7-123">Administrar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="76ab7-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





