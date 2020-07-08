---
title: Publicación de aplicaciones virtuales mediante distribución electrónica de software
description: Publicación de aplicaciones virtuales mediante distribución electrónica de software
author: dansimp
ms.assetid: 295fbc1d-ed1c-43b4-aeee-0df384d4e630
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0354fc1226aa78d947dd764a0ab6157b563a321
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815741"
---
# Publicación de aplicaciones virtuales mediante distribución electrónica de software


Un sistema de distribución electrónica de software (ESD) está diseñado para mover software de forma eficaz a muchos equipos diferentes a través de conexiones de red lentas o rápidas. Con la virtualización de aplicaciones mediante un sistema ESD, puede usar uno de los siguientes métodos para distribuir paquetes de aplicaciones virtuales:

-   Configure el sistema de ESD para distribuir los paquetes directamente a cada equipo cliente mediante la versión de Windows Installer del paquete generado por Application Virtualization Sequencer. El archivo de Windows Installer contiene los iconos, la información de definición del paquete y el contenido, y cuando usa Windows Installer, publica los iconos en el escritorio de Windows y en el menú Inicio, y carga el contenido del paquete en la memoria caché del cliente de virtualización de aplicaciones. El usuario puede empezar a usar las aplicaciones inmediatamente sin ningún otro requisito de configuración. La actualización de un paquete a una versión más reciente se realiza mediante Windows Installer para desinstalar el archivo de package.msi y, a continuación, instalar la nueva versión.

-   Coloque el contenido del paquete en un punto de distribución de software o un servidor de streaming de Application Virtualization que sea fácilmente accesible para los equipos cliente a través de una conexión de red con un buen ancho de banda, como una LAN. Por ejemplo, puede usar los equipos de punto de distribución de sistema de ESD existentes en cada sucursal. Usar parámetros de la línea de comandos para definir el origen de la transmisión desde el cual los clientes transmitirán por secuencias el paquete de aplicación virtual, el sistema de ESD implementará la versión de Windows Installer del paquete en cada cliente. El sistema ESD también podría usarse para copiar el archivo SFT que contiene el contenido del paquete en el recurso compartido de archivos de todos los servidores de transmisión. La actualización de un paquete a una versión más reciente se realiza mediante Windows Installer para desinstalar el archivo de package.msi y, a continuación, instalar la nueva versión.

-   Como alternativa al uso del archivo independiente de Windows Installer en cualquiera de los modos anteriores para implementar los paquetes, puede controlar la implementación de una forma mucho más detallada con el lenguaje de la línea de comandos de Application Virtualization SFTMIME. Esto proporciona muchos comandos para controlar todos los aspectos de la administración de paquetes. Aunque SFTMIME es muy importante, también es complejo, por lo que los administradores deben planear la creación de todos los comandos como scripts y probarlos minuciosamente en un entorno de prueba antes del uso de producción. Para obtener más información sobre los comandos de SFTMIME disponibles, vea [SFTMIME referencia de comandos](sftmime--command-reference.md).

## Temas relacionados


[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)

[Planificación de la solución de streaming en una implementación de distribución electrónica de software](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)

[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





