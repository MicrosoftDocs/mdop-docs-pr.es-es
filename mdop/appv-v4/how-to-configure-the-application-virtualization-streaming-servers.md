---
title: Cómo configurar los servidores de streaming de virtualización de aplicaciones
description: Cómo configurar los servidores de streaming de virtualización de aplicaciones
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817821"
---
# Cómo configurar los servidores de streaming de virtualización de aplicaciones


Antes de que las aplicaciones virtuales se puedan transmitir por secuencias al cliente de escritorio de virtualización de aplicaciones o al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server), los servidores de streaming de Application Virtualization deben estar configurados. Al configurar los servidores, está configurando el *Directorio de contenido* en el que se cargan y almacenan los archivos de SFT. Los archivos SFT contienen la aplicación virtual (o aplicaciones).

**Importante**  Los servidores de virtualización de aplicaciones transmiten archivos SFT al cliente de escritorio y al cliente para servicios de escritorio remoto que solo usan protocolos RTSP o RTSPs. El archivo ICO (icono) y el archivo OSD (descriptor de software abierto) se pueden configurar para transmitirlos desde un archivo o servidor HTTP diferente.

 

**Para configurar los servidores de streaming de Application Virtualization**

1.  Complete el procedimiento de instalación del servidor de streaming de Application Virtualization. Durante el procedimiento de instalación, especifique la ubicación del directorio \\Content en la pantalla **ruta de contenido** .

2.  Vaya a la ubicación que especificó para el directorio \\Content y, si es necesario, cree el directorio.

3.  Cuando se cree el directorio de contenido, configure este directorio como un recurso compartido de archivos estándar.

4.  Configure los permisos del sistema de archivos NTFS en el directorio de contenido y en las carpetas de paquetes en el directorio de contenido. Debe usar grupos de seguridad en los servicios de dominio de Active Directory que definan qué usuarios pueden tener acceso a cada aplicación.

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Cómo configurar los servidores de administración de virtualización de aplicaciones](how-to-configure-the-application-virtualization-management-servers.md)

[Cómo configurar el servidor de archivos](how-to-configure-the-file-server.md)

[Cómo configurar el servidor para IIS](how-to-configure-the-server-for-iis.md)

 

 





