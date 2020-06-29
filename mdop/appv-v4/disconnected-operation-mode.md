---
title: Modo de operación desconectado
description: Modo de operación desconectado
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821621"
---
# <span data-ttu-id="ad614-103">Modo de operación desconectado</span><span class="sxs-lookup"><span data-stu-id="ad614-103">Disconnected Operation Mode</span></span>


<span data-ttu-id="ad614-104">La configuración del modo de funcionamiento desconectado: accesible haciendo clic con el botón secundario en el nodo de **virtualización de aplicaciones** , seleccionando **propiedades**y haciendo clic en la pestaña **Conectividad** , permite que el cliente de escritorio de Application Virtualization o el cliente de servicios de escritorio remoto (anteriormente servicios de Terminal Server) ejecuten aplicaciones que se almacenan en la memoria caché del sistema de archivos cuando el cliente no</span><span class="sxs-lookup"><span data-stu-id="ad614-104">The disconnected operation mode settings—accessible by right-clicking the **Application Virtualization** node, selecting **Properties**, and clicking the **Connectivity** tab—enables the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client is unable to connect to the Application Virtualization Management Server.</span></span>

<span data-ttu-id="ad614-105">Las razones por las que no se puede conectar con el servidor son: error del servidor, interrupción de la red o desconexión de la red.</span><span class="sxs-lookup"><span data-stu-id="ad614-105">Reasons for failure to connect to the server include server failure, network outage, or disconnection from the network.</span></span> <span data-ttu-id="ad614-106">Si se produce algún error, el cliente cambiará automáticamente a la operación desconectada.</span><span class="sxs-lookup"><span data-stu-id="ad614-106">If any failure occurs, the client will automatically switch to disconnected operation.</span></span> <span data-ttu-id="ad614-107">Una vez desconectado, si el cliente necesita más datos del servidor para continuar ejecutando una aplicación o si el tiempo de espera de la operación de desconexión se agota, el cliente intentará volver a conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="ad614-107">After it is disconnected, if the client needs additional data from the server to continue to run an application or if the disconnected operation time-out expires, the client will attempt to reconnect to the server.</span></span> <span data-ttu-id="ad614-108">Si se produce un error en este intento de conexión, la aplicación se cerrará.</span><span class="sxs-lookup"><span data-stu-id="ad614-108">If this connection attempt fails, the application will be shut down.</span></span>

<span data-ttu-id="ad614-109">De forma predeterminada, la operación desconectada está habilitada y el tiempo de espera está establecido en 90 días.</span><span class="sxs-lookup"><span data-stu-id="ad614-109">By default, disconnected operation is enabled and the time-out is set to 90 days.</span></span> <span data-ttu-id="ad614-110">El valor de tiempo de espera se especifica como el número de días que desea limitar el modo de funcionamiento desconectado y puede escribir un valor de 1 a 999.</span><span class="sxs-lookup"><span data-stu-id="ad614-110">The time-out value is specified as the number of days you want to limit disconnected operation mode, and you can enter a value from 1–999.</span></span>

## <span data-ttu-id="ad614-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad614-111">Related topics</span></span>


[<span data-ttu-id="ad614-112">Cómo deshabilitar o modificar la configuración de modo de operación desconectado</span><span class="sxs-lookup"><span data-stu-id="ad614-112">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





