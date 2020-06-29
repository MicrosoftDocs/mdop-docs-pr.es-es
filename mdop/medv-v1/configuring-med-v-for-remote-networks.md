---
title: Configurar MED-V para redes remotas
description: Configurar MED-V para redes remotas
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826721"
---
# <span data-ttu-id="13a77-103">Configurar MED-V para redes remotas</span><span class="sxs-lookup"><span data-stu-id="13a77-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="13a77-104">Puede configurar MED-V para que funcione desde dentro de una red, de forma remota o desde dentro de la red y de forma remota.</span><span class="sxs-lookup"><span data-stu-id="13a77-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="13a77-105">Para configurar MED-V para que funcione desde dentro de una red</span><span class="sxs-lookup"><span data-stu-id="13a77-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="13a77-106">Configurar un servidor de MED-V y una distribución de imágenes dentro de la red.</span><span class="sxs-lookup"><span data-stu-id="13a77-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="13a77-107">Para configurar MED-V para que funcionen de forma remota</span><span class="sxs-lookup"><span data-stu-id="13a77-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="13a77-108">Configurar un servidor de MED-V y un servidor de distribución de imágenes accesibles desde Internet.</span><span class="sxs-lookup"><span data-stu-id="13a77-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="13a77-109">Si es necesario, configure un proxy inverso de red perimetral (también llamado DMZ).</span><span class="sxs-lookup"><span data-stu-id="13a77-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="13a77-110">Establezca el método de autenticación, en el archivo *ClientSettings.xml* , que puede encontrarse en la carpeta **Servers\\Configuration Server\\**</span><span class="sxs-lookup"><span data-stu-id="13a77-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="13a77-111">Para configurar MED-V para que funcione desde dentro de una red y de forma remota</span><span class="sxs-lookup"><span data-stu-id="13a77-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="13a77-112">Configurar un servidor de MED-V y un servidor de distribución de imágenes en la red.</span><span class="sxs-lookup"><span data-stu-id="13a77-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="13a77-113">Asegúrese de que los servidores son accesibles desde Internet.</span><span class="sxs-lookup"><span data-stu-id="13a77-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="13a77-114">Configure la resolución DNS para que cuando el cliente intente conectarse a un servidor, se conecte automáticamente al servidor correcto (dentro de la red o a través de Internet) en función de la ubicación del cliente.</span><span class="sxs-lookup"><span data-stu-id="13a77-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="13a77-115">Si es necesario, configure un proxy inverso de red perimetral.</span><span class="sxs-lookup"><span data-stu-id="13a77-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="13a77-116">Establezca el método de autenticación, en el archivo *ClientSettings.xml* , que puede encontrarse en la carpeta **Servers\\Configuration Server\\**</span><span class="sxs-lookup"><span data-stu-id="13a77-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="13a77-117">**Nota:**  Al aplicar la nueva configuración, se debe reiniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="13a77-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="13a77-118">Puede cambiar el esquema de autenticación de IIS a uno de los siguientes: básico, implícito, NTLM o NEGOTIATE.</span><span class="sxs-lookup"><span data-stu-id="13a77-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="13a77-119">El valor predeterminado es NEGOTIATE y usa la siguiente entrada:</span><span class="sxs-lookup"><span data-stu-id="13a77-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="13a77-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13a77-120">Related topics</span></span>


[<span data-ttu-id="13a77-121">Diseño y planificación de la infraestructura de MED-V</span><span class="sxs-lookup"><span data-stu-id="13a77-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





