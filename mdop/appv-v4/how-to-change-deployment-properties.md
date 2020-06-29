---
title: Cómo cambiar las propiedades de implementación
description: Cómo cambiar las propiedades de implementación
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818061"
---
# <span data-ttu-id="34ea7-103">Cómo cambiar las propiedades de implementación</span><span class="sxs-lookup"><span data-stu-id="34ea7-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="34ea7-104">Puede usar los procedimientos siguientes para cambiar la información de la pestaña **implementación** para una aplicación que está transformando, lo que incluye la dirección URL del servidor de virtualización de aplicaciones, los sistemas operativos requeridos por las aplicaciones virtualizadas y las opciones de salida de la aplicación virtual que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="34ea7-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="34ea7-105">Para cambiar la dirección URL del servidor</span><span class="sxs-lookup"><span data-stu-id="34ea7-105">To change the server URL</span></span>**

1.  <span data-ttu-id="34ea7-106">Seleccione el protocolo de transmisión por secuencias en el cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="34ea7-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="34ea7-107">Escriba el nombre de host del servidor de aplicaciones virtual o del equilibrador de carga del grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="34ea7-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="34ea7-108">Puede usar el nombre de host o la dirección IP reales.</span><span class="sxs-lookup"><span data-stu-id="34ea7-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="34ea7-109">Especifique el número de puerto en el que el servidor de aplicaciones virtual o el equilibrador de carga escuchará una solicitud de cliente de escritorio de virtualización de aplicaciones para la aplicación transmitida.</span><span class="sxs-lookup"><span data-stu-id="34ea7-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="34ea7-110">Especifique la ruta de acceso relativa en el servidor de aplicaciones virtual donde se encuentra almacenado el paquete de software.</span><span class="sxs-lookup"><span data-stu-id="34ea7-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="34ea7-111">Para cambiar los requisitos de los sistemas operativos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="34ea7-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="34ea7-112">Para agregar los sistemas operativos necesarios, selecciónelos en la lista **disponible** y haga clic en el botón de flecha que apunta al control de lista sistemas operativos **seleccionados** .</span><span class="sxs-lookup"><span data-stu-id="34ea7-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="34ea7-113">Para quitar un sistema operativo, selecciónelo en el control de lista **seleccionado** y haga clic en el botón de flecha que apunta al control de lista sistemas operativos **disponibles** .</span><span class="sxs-lookup"><span data-stu-id="34ea7-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="34ea7-114">Para cambiar las opciones de resultados de la aplicación</span><span class="sxs-lookup"><span data-stu-id="34ea7-114">To change the application output options</span></span>**

1.  <span data-ttu-id="34ea7-115">En la lista desplegable **algoritmo de compresión** , seleccione el método de compresión que desee usar al transmitir la aplicación.</span><span class="sxs-lookup"><span data-stu-id="34ea7-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="34ea7-116">Seleccione la casilla **exigir descriptores de seguridad** para garantizar que los descriptores de seguridad de las aplicaciones empaquetadas se aplican al implementarse.</span><span class="sxs-lookup"><span data-stu-id="34ea7-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="34ea7-117">Seleccione **generar archivo de diferencias** para generar un archivo de diferencias para la aplicación a partir de la versión anterior de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="34ea7-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="34ea7-118">Seleccione **generar paquete de Microsoft Windows Installer (MSI)** para crear un paquete de instalador.</span><span class="sxs-lookup"><span data-stu-id="34ea7-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="34ea7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34ea7-119">Related topics</span></span>


[<span data-ttu-id="34ea7-120">Acerca de la pestaña Implementación</span><span class="sxs-lookup"><span data-stu-id="34ea7-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="34ea7-121">Consola de secuenciador</span><span class="sxs-lookup"><span data-stu-id="34ea7-121">Sequencer Console</span></span>](sequencer-console.md)

 

 





