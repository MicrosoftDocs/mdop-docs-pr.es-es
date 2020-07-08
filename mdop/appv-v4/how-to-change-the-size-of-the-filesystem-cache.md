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
# Cómo cambiar el tamaño de la caché de sistema de archivos


Puede cambiar el tamaño de la caché del sistema de archivos mediante la línea de comandos. Esta acción requiere un reinicio completo de la caché y requiere derechos administrativos.

**Para cambiar el tamaño de la caché del sistema de archivos**

1.  Establezca el siguiente valor del registro en 0 (cero):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Establezca el valor de registro siguiente en el tamaño máximo de caché, en MB, que es necesario para mantener los paquetes, por ejemplo, 8192 MB:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize

3.  Reinicie el equipo.

## Temas relacionados


[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





