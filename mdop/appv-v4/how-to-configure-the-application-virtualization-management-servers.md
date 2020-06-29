---
title: Cómo configurar los servidores de administración de virtualización de aplicaciones
description: Cómo configurar los servidores de administración de virtualización de aplicaciones
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817841"
---
# Cómo configurar los servidores de administración de virtualización de aplicaciones


Antes de que las aplicaciones virtualizadas se puedan transmitir por secuencias al cliente de escritorio de virtualización de aplicaciones o al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server), debe configurarse el servidor de administración de virtualización de aplicaciones. Al configurar el servidor, está configurando el *Directorio de contenido* en el que se cargan y almacenan los archivos de SFT. Los archivos SFT contienen la aplicación virtualizada (o aplicaciones).

**Importante**  Los servidores de virtualización de aplicaciones transmiten archivos SFT al cliente de escritorio y al cliente para servicios de escritorio remoto que solo usan protocolos RTSP o RTSPs. El archivo ICO (icono) y el archivo OSD (descriptor de software abierto) se pueden configurar para transmitirlos desde un archivo o servidor HTTP diferente.

 

**Para configurar el servidor de administración de virtualización de aplicaciones**

1.  Complete el procedimiento siguiente:

    [Cómo instalar el servidor de administración de virtualización de aplicaciones](how-to-install-application-virtualization-management-server.md)

    **Nota:**  Durante el procedimiento de instalación, especifique la ubicación del directorio \\Content en la pantalla **ruta de contenido** .

     

2.  Vaya a la ubicación que especificó para el directorio \\Content y, si es necesario, cree el directorio.

3.  Cuando se cree el directorio de contenido, configure este directorio como un recurso compartido de archivos estándar.

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Requisitos de sistema de virtualización de aplicaciones](application-virtualization-system-requirements.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Cómo configurar servidores para implementación basada en servidor](how-to-configure-servers-for-server-based-deployment.md)

 

 





