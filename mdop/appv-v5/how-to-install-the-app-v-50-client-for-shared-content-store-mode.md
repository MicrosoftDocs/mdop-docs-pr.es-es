---
title: Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido
description: Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814055"
---
# <span data-ttu-id="2fac8-103">Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido</span><span class="sxs-lookup"><span data-stu-id="2fac8-103">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="2fac8-104">Use el siguiente procedimiento para instalar el cliente de Microsoft Application Virtualization (App-V) 5,0 de modo que use el modo de almacén de contenido compartido (SCS) de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2fac8-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 client so that it uses the App-V 5.0 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="2fac8-105">Debe asegurarse de que todos los requisitos previos necesarios estén instalados en el equipo en el que planea instalar.</span><span class="sxs-lookup"><span data-stu-id="2fac8-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="2fac8-106">Use el siguiente vínculo para los [requisitos previos de App-V 5,0](app-v-50-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="2fac8-106">Use the following link for a [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

<span data-ttu-id="2fac8-107">**Nota:**  Antes de realizar este procedimiento, si es necesario, desinstale las versiones existentes del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2fac8-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.0 client.</span></span>

 

<span data-ttu-id="2fac8-108">Para más información sobre el modo SCS, vea [almacenamiento de contenido compartido en Microsoft App-V 5,0](https://go.microsoft.com/fwlink/?LinkId=316879) , entre bastidores ( https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="2fac8-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="2fac8-109">Instalar y configurar el cliente de App-V 5,0 para el modo SCS</span><span class="sxs-lookup"><span data-stu-id="2fac8-109">Install and configure the App-V 5.0 client for SCS mode</span></span>**

1.  <span data-ttu-id="2fac8-110">Copie los archivos de instalación del cliente App-V 5,0 en el equipo en el que se instalará.</span><span class="sxs-lookup"><span data-stu-id="2fac8-110">Copy the App-V 5.0 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="2fac8-111">Abra una línea de comandos y, desde el directorio donde se guardan los archivos de instalación, escriba una de las siguientes opciones en función de la versión del cliente que esté instalando:</span><span class="sxs-lookup"><span data-stu-id="2fac8-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="2fac8-112">Para instalar la versión de RDS del tipo de cliente App-V 5,0: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="2fac8-112">To install the RDS version of the App-V 5.0 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="2fac8-113">Para instalar la versión estándar del tipo de cliente App-V 5,0: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="2fac8-113">To install the standard version of the App-V 5.0 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="2fac8-114">**Importante**  Debe realizar una instalación silenciosa o se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="2fac8-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="2fac8-115">Después de completar la instalación, puede implementar paquetes en el equipo en el que se ejecuta el cliente y todo el contenido del paquete se transmitirá a través de la red.</span><span class="sxs-lookup"><span data-stu-id="2fac8-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="2fac8-116">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="2fac8-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2fac8-117">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="2fac8-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2fac8-118">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="2fac8-118">Got an App-V issue?</span></span>** <span data-ttu-id="2fac8-119">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2fac8-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2fac8-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fac8-120">Related topics</span></span>


[<span data-ttu-id="2fac8-121">Implementación del secuenciador y del cliente de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2fac8-121">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





