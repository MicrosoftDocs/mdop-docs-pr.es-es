---
title: Cómo configurar el servidor de archivos
description: Cómo configurar el servidor de archivos
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817781"
---
# Cómo configurar el servidor de archivos


Puede usar el procedimiento siguiente para configurar un equipo local que se usa como un recurso compartido de archivos y secuencias aplicaciones al cliente de escritorio de virtualización de aplicaciones y al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server). Este escenario se usa cuando no desea agregar una infraestructura de servidor adicional a su entorno de hardware existente.

Si usa un servidor de administración de virtualización de aplicaciones como punto de distribución para el recurso compartido de archivos instalado en oficinas locales, debe configurar este servidor para que las aplicaciones virtuales se puedan transmitir a los equipos que se usan como recursos compartidos de archivos. Al configurar los servidores y los recursos compartidos de archivos, está configurando el directorio de contenido en el que se cargan y almacenan los archivos de SFT. Los archivos SFT contienen la aplicación virtual (o aplicaciones).

**Importante**  Para que las aplicaciones se transmitan correctamente al cliente de escritorio de virtualización de aplicaciones y al cliente para servicios de escritorio remoto, el archivo SFT se transmite desde el directorio de contenido en el servidor en el que se almacena la aplicación virtual; el archivo ICO (icono) y el archivo OSD (Open software descriptor) se pueden configurar para transmitir desde un servidor diferente.

 

**Para configurar el servidor de archivos de virtualización de aplicaciones**

1.  Complete el siguiente procedimiento de instalación para configurar el servidor que se usa como punto de distribución:

    [Cómo instalar el servidor de administración de virtualización de aplicaciones](how-to-install-application-virtualization-management-server.md)

    **Nota:**  Durante el procedimiento de instalación, especifique la ubicación del directorio \\Content en la pantalla **ruta de contenido** .

     

2.  Cree un directorio \\Content, que se corresponde con el directorio que especificó al instalar el servidor, en cada equipo que use como recurso compartido de archivos.

    **Importante**  Configure los clientes de escritorio de la virtualización de aplicaciones para transmitir las aplicaciones desde el equipo que está usando como un recurso compartido de archivos en lugar de un servidor de virtualización de aplicaciones o servidor IIS.

     

3.  Cuando se crea el directorio \\Content, configure este directorio como un recurso compartido de archivos estándar.

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Cómo configurar los servidores de administración de virtualización de aplicaciones](how-to-configure-the-application-virtualization-management-servers.md)

[Cómo configurar los servidores de streaming de virtualización de aplicaciones](how-to-configure-the-application-virtualization-streaming-servers.md)

[Cómo configurar el servidor para IIS](how-to-configure-the-server-for-iis.md)

 

 





