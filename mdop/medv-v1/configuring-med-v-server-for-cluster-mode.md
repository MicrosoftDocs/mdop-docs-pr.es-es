---
title: Configuración del servidor de MED-V para el modo de clúster
description: Configuración del servidor de MED-V para el modo de clúster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826720"
---
# <span data-ttu-id="8d311-103">Configuración del servidor de MED-V para el modo de clúster</span><span class="sxs-lookup"><span data-stu-id="8d311-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="8d311-104">Puede configurar el servidor de MED-V en el modo de clúster.</span><span class="sxs-lookup"><span data-stu-id="8d311-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="8d311-105">En el modo de clúster, se usan dos servidores y todos los archivos identificados como mutuos en ambos servidores se colocan en un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8d311-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="8d311-106">El servidor accede a los archivos desde el sistema de archivos, en lugar de almacenar los archivos de forma local.</span><span class="sxs-lookup"><span data-stu-id="8d311-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="8d311-107">Para configurar el servidor de MED-V en el modo de clúster</span><span class="sxs-lookup"><span data-stu-id="8d311-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="8d311-108">Instale y configure MED-V en uno de los servidores.</span><span class="sxs-lookup"><span data-stu-id="8d311-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="8d311-109">Cree una red compartida en una ubicación central en la que todos los servidores puedan acceder a ella.</span><span class="sxs-lookup"><span data-stu-id="8d311-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="8d311-110">Copie el contenido de la carpeta \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* en la red compartida.</span><span class="sxs-lookup"><span data-stu-id="8d311-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="8d311-111">Instale MED-V Server en todos los servidores designados.</span><span class="sxs-lookup"><span data-stu-id="8d311-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="8d311-112">En la red compartida, asigne acceso completo a todas las cuentas del sistema de servidor de MED-V.</span><span class="sxs-lookup"><span data-stu-id="8d311-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="8d311-113">En cada servidor, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8d311-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="8d311-114">En el archivo \* &lt; InstallDir &gt; /Servers/ServerConfiguration.xml\* , establezca el valor de \* &lt; StorePath &gt; \* en la ruta de acceso de red compartida.</span><span class="sxs-lookup"><span data-stu-id="8d311-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="8d311-115">Copie el archivo \* &lt; InstsallDir &gt; /Servers/KeyPair.xml\* desde el servidor original a todos los servidores de MED-V.</span><span class="sxs-lookup"><span data-stu-id="8d311-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="8d311-116">Reinicie el servicio MED-V.</span><span class="sxs-lookup"><span data-stu-id="8d311-116">Restart the MED-V service.</span></span>

<span data-ttu-id="8d311-117">**Nota:**  Si todos los servidores tienen la misma configuración local (como puertos de escucha, servidor IIS, permisos de administración, base de datos de informes, etc.), todos los servidores también pueden compartir el \* &lt; &gt; ServerSettings.xmlINSTALLDIR/Servers/\* .</span><span class="sxs-lookup"><span data-stu-id="8d311-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="8d311-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d311-118">Related topics</span></span>


[<span data-ttu-id="8d311-119">Diseño y planificación de la infraestructura de MED-V</span><span class="sxs-lookup"><span data-stu-id="8d311-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





