---
title: Cómo restablecer la caché de sistema de archivos
description: Cómo restablecer la caché de sistema de archivos
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816711"
---
# <span data-ttu-id="112d6-103">Cómo restablecer la caché de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="112d6-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="112d6-104">El restablecimiento de la caché del sistema de archivos no es algo que normalmente es necesario.</span><span class="sxs-lookup"><span data-stu-id="112d6-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="112d6-105">Sin embargo, si necesita restablecer por completo la caché del sistema de archivos, por ejemplo, con fines de solución de problemas, puede usar el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="112d6-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="112d6-106">Se necesitan derechos administrativos para realizar esta acción.</span><span class="sxs-lookup"><span data-stu-id="112d6-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="112d6-107">Para restablecer la caché del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="112d6-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="112d6-108">Establezca el siguiente valor del registro en 0 (cero):</span><span class="sxs-lookup"><span data-stu-id="112d6-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="112d6-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="112d6-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="112d6-110">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="112d6-110">Restart the computer.</span></span>

## <span data-ttu-id="112d6-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="112d6-111">Related topics</span></span>


[<span data-ttu-id="112d6-112">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="112d6-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





