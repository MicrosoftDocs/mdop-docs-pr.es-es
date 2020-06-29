---
title: Cómo publicar una aplicación virtual en el cliente
description: Cómo publicar una aplicación virtual en el cliente
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816871"
---
# <span data-ttu-id="f1201-103">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="f1201-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="f1201-104">Al implementar la virtualización de aplicaciones mediante un sistema electrónico de distribución de software, puede usar uno de los procedimientos siguientes para publicar un paquete de aplicación para sus usuarios.</span><span class="sxs-lookup"><span data-stu-id="f1201-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="f1201-105">Para publicar un paquete con un archivo de Windows Installer independiente</span><span class="sxs-lookup"><span data-stu-id="f1201-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="f1201-106">El cliente debe instalarse con el parámetro *REQUIREAUTHORIZATIONIFCACHED* establecido en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="f1201-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="f1201-107">Para obtener más información sobre la configuración de este parámetro, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="f1201-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="f1201-108">Copie el archivo de Windows Installer y el archivo SFT a la misma carpeta del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="f1201-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="f1201-109">Ejecute el siguiente comando en el equipo:</span><span class="sxs-lookup"><span data-stu-id="f1201-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="f1201-110">Para publicar un paquete con Windows Installer y el manifiesto del paquete</span><span class="sxs-lookup"><span data-stu-id="f1201-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="f1201-111">Copie el archivo de Windows Installer en el equipo de destino y el archivo SFT en el recurso compartido de contenido del servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="f1201-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="f1201-112">Ejecute el siguiente comando en el equipo de cada usuario:</span><span class="sxs-lookup"><span data-stu-id="f1201-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="f1201-113">**Importante**  Para OVERRIDEURL todos los caracteres de barra invertida se deben escapar con una barra diagonal inversa anterior, o la ruta de acceso de OVERRIDEURL no se analizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1201-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="f1201-114">Además, las propiedades y los valores deben escribirse en mayúsculas, excepto en el caso de que el valor sea una ruta de acceso a un archivo.</span><span class="sxs-lookup"><span data-stu-id="f1201-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="f1201-115">Para publicar un paquete con SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f1201-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="f1201-116">Para obtener un ejemplo de cómo publicar una aplicación para todos los usuarios de un equipo, ejecute el siguiente comando en el equipo del usuario:</span><span class="sxs-lookup"><span data-stu-id="f1201-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="f1201-117">Para obtener más información sobre estos y otros comandos de SFTMIME, consulte [SFTMIME referencia de comandos](sftmime--command-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f1201-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="f1201-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1201-118">Related topics</span></span>


[<span data-ttu-id="f1201-119">Determinar el método de publicación</span><span class="sxs-lookup"><span data-stu-id="f1201-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="f1201-120">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="f1201-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="f1201-121">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f1201-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="f1201-122">Escenario de distribución independiente para clientes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f1201-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





