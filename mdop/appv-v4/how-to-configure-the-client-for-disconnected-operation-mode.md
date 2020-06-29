---
title: Cómo configurar al cliente para el modo de operación desconectado
description: Cómo configurar al cliente para el modo de operación desconectado
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817820"
---
# <span data-ttu-id="02205-103">Cómo configurar al cliente para el modo de operación desconectado</span><span class="sxs-lookup"><span data-stu-id="02205-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="02205-104">El modo de operación desconectado habilita el cliente de escritorio de Application Virtualization (App-V) o el cliente de Application Virtualization (App-V) para servicios de escritorio remoto (anteriormente servicios de Terminal Server) para ejecutar aplicaciones que se almacenan en la caché del sistema de archivos del cliente cuando el cliente no puede conectarse al servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="02205-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="02205-105">**Importante**  En una organización grande en la que varios servidores de host de sesión de escritorio remoto (anteriormente host de sesión de RD) (antes Terminal Servers) están vinculados en una granja de servidores para admitir muchos usuarios, el uso de un único servidor de administración de aplicaciones-V para admitir la granja representa un único punto de error.</span><span class="sxs-lookup"><span data-stu-id="02205-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="02205-106">Para proporcionar una alta disponibilidad para admitir la granja de servidores RDSession, considere la posibilidad de vincular dos o más servidores de administración de App-V para usar la misma base de datos.</span><span class="sxs-lookup"><span data-stu-id="02205-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="02205-107">Para habilitar el modo de funcionamiento desconectado</span><span class="sxs-lookup"><span data-stu-id="02205-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="02205-108">Establezca el siguiente valor de clave del registro igual a 1 para habilitar el modo de operación desconectada:</span><span class="sxs-lookup"><span data-stu-id="02205-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="02205-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="02205-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="02205-110">Para establecer un límite de tiempo en el modo de funcionamiento desconectado, use</span><span class="sxs-lookup"><span data-stu-id="02205-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="02205-111">Establezca el valor de la clave del Registro siguiente en 1:</span><span class="sxs-lookup"><span data-stu-id="02205-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="02205-112">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="02205-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="02205-113">Establezca el valor de la clave del Registro siguiente en el número de minutos que desee limitar el modo de funcionamiento desconectado.</span><span class="sxs-lookup"><span data-stu-id="02205-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="02205-114">El intervalo válido de valores es de 1 – 999999.</span><span class="sxs-lookup"><span data-stu-id="02205-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="02205-115">El valor predeterminado es 90 días o 129.600 minutos.</span><span class="sxs-lookup"><span data-stu-id="02205-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="02205-116">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="02205-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="02205-117">Para configurar el cliente para servicios de escritorio remoto para el modo de operación de desconexión</span><span class="sxs-lookup"><span data-stu-id="02205-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="02205-118">Establezca el valor de la clave del Registro siguiente en 1 para habilitar el modo de operación desconectada:</span><span class="sxs-lookup"><span data-stu-id="02205-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="02205-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="02205-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="02205-120">Establezca el valor de la clave del Registro siguiente en 0 (cero) para permitir el uso sin límites del modo de operación desconectada:</span><span class="sxs-lookup"><span data-stu-id="02205-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="02205-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="02205-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="02205-122">Asegúrese de que todos los paquetes se cargan previamente en la memoria caché para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="02205-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="02205-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02205-123">Related topics</span></span>


[<span data-ttu-id="02205-124">Modo de operación desconectado</span><span class="sxs-lookup"><span data-stu-id="02205-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="02205-125">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="02205-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





