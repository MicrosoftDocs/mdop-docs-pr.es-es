---
title: Cómo cambiar el tamaño de la caché de sistema de archivos
description: Cómo cambiar el tamaño de la caché de sistema de archivos
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818001"
---
# <span data-ttu-id="eae83-103">Cómo cambiar el tamaño de la caché de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="eae83-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="eae83-104">Puede cambiar el tamaño de la caché del sistema de archivos mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="eae83-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="eae83-105">Esta acción requiere un reinicio completo de la caché y requiere derechos administrativos.</span><span class="sxs-lookup"><span data-stu-id="eae83-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="eae83-106">Para cambiar el tamaño de la caché del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="eae83-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="eae83-107">Establezca el siguiente valor del registro en 0 (cero):</span><span class="sxs-lookup"><span data-stu-id="eae83-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="eae83-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="eae83-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="eae83-109">Establezca el valor de registro siguiente en el tamaño máximo de caché, en MB, que es necesario para mantener los paquetes, por ejemplo, 8192 MB:</span><span class="sxs-lookup"><span data-stu-id="eae83-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="eae83-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span><span class="sxs-lookup"><span data-stu-id="eae83-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="eae83-111">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="eae83-111">Restart the computer.</span></span>

## <span data-ttu-id="eae83-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eae83-112">Related topics</span></span>


[<span data-ttu-id="eae83-113">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="eae83-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





