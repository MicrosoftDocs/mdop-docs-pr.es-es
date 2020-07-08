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
# Cómo restablecer la caché de sistema de archivos


El restablecimiento de la caché del sistema de archivos no es algo que normalmente es necesario. Sin embargo, si necesita restablecer por completo la caché del sistema de archivos, por ejemplo, con fines de solución de problemas, puede usar el procedimiento siguiente. Se necesitan derechos administrativos para realizar esta acción.

**Para restablecer la caché del sistema de archivos**

1.  Establezca el siguiente valor del registro en 0 (cero):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Reinicie el equipo.

## Temas relacionados


[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





