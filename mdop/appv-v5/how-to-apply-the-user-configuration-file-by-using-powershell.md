---
title: Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell
description: Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814438"
---
# <span data-ttu-id="29db1-103">Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="29db1-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="29db1-104">El archivo de configuración de usuario dinámico se aplica cuando se publica un paquete para un usuario específico y determina cómo se ejecutará el paquete.</span><span class="sxs-lookup"><span data-stu-id="29db1-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="29db1-105">Use el procedimiento siguiente para especificar un archivo de configuración específico del usuario.</span><span class="sxs-lookup"><span data-stu-id="29db1-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="29db1-106">El siguiente procedimiento se basa en el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="29db1-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="29db1-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="29db1-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="29db1-108">Para aplicar un archivo de configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="29db1-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="29db1-109">Para agregar el paquete al equipo mediante la consola de PowerShell, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="29db1-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="29db1-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**</span><span class="sxs-lookup"><span data-stu-id="29db1-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="29db1-111">Use el comando siguiente para publicar el paquete para el usuario y especificar el archivo de configuración de usuario dinámico actualizado:</span><span class="sxs-lookup"><span data-stu-id="29db1-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="29db1-112">Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="29db1-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="29db1-113">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="29db1-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="29db1-114">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="29db1-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="29db1-115">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="29db1-115">Got an App-V issue?</span></span>** <span data-ttu-id="29db1-116">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="29db1-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="29db1-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29db1-117">Related topics</span></span>


[<span data-ttu-id="29db1-118">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="29db1-118">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





