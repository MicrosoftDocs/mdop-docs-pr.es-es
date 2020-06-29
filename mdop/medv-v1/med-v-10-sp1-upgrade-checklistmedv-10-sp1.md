---
title: Lista de comprobación de actualización MED-V 1.0 SP1
description: Lista de comprobación de actualización MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827270"
---
# <span data-ttu-id="c8d63-103">Lista de comprobación de actualización MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c8d63-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="c8d63-104">Para actualizar Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 a MED-V 1.0 Service Pack1 (SP1), el cliente debe estar actualizado.</span><span class="sxs-lookup"><span data-stu-id="c8d63-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="c8d63-105">De forma opcional, el servidor puede actualizarse.</span><span class="sxs-lookup"><span data-stu-id="c8d63-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="c8d63-106">Actualización de servidor</span><span class="sxs-lookup"><span data-stu-id="c8d63-106">Server Upgrade</span></span>


**<span data-ttu-id="c8d63-107">Para actualizar el servidor MED-V 1.0 a MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c8d63-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="c8d63-108">Haga una copia de seguridad de los siguientes archivos que se encuentran en el directorio \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* :</span><span class="sxs-lookup"><span data-stu-id="c8d63-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="c8d63-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="c8d63-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="c8d63-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="c8d63-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="c8d63-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="c8d63-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="c8d63-112">Haga una copia de seguridad del archivo \* &lt; INSTALLDIR &gt; /servers/ServerSettings.xml\* .</span><span class="sxs-lookup"><span data-stu-id="c8d63-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="c8d63-113">Desinstale el servidor MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="c8d63-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="c8d63-114">Instale el servidor MED-V 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c8d63-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="c8d63-115">Restaure los archivos de copia de seguridad en los directorios apropiados.</span><span class="sxs-lookup"><span data-stu-id="c8d63-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="c8d63-116">Reinicie el servicio de servidor de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c8d63-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="c8d63-117">**Nota:**  Si la configuración del servidor se ha cambiado de la predeterminada, es posible que los archivos se hayan almacenado en una ubicación diferente.</span><span class="sxs-lookup"><span data-stu-id="c8d63-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="c8d63-118">Actualización de cliente</span><span class="sxs-lookup"><span data-stu-id="c8d63-118">Client Upgrade</span></span>


<span data-ttu-id="c8d63-119">Para actualizar el cliente MED-V 1.0 a MED-V 1.0 SP1, instale el archivo. MSP en un cliente MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="c8d63-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="c8d63-120">El cliente y MED-V se actualizan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c8d63-120">The client and MED-V are automatically upgraded.</span></span>

 

 





