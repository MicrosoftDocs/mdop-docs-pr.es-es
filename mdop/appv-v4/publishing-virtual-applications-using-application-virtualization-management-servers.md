---
title: Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones
description: Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815770"
---
# Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones


En una implementación basada en un servidor de virtualización de aplicaciones, los paquetes de aplicaciones virtuales que se han secuencial, probado y encontrado implementados se copian en el recurso de contenido principal que usará el servidor de administración de virtualización de Application Virtualization. Después de importar los paquetes en el servidor de administración de virtualización de aplicaciones, se pueden publicar para los usuarios finales.

**Nota:**  El recurso compartido de contenido debe estar ubicado en el almacenamiento en disco conectado del servidor. El uso de un dispositivo de almacenamiento de red como un SAN o un recurso compartido de DFS debe considerarse detenidamente debido al impacto de la red.

 

Las aplicaciones se suministran a los grupos de Active Directory. Normalmente, el administrador de virtualización de la aplicación creará grupos de Active Directory para cada aplicación virtual que se va a publicar y, a continuación, agregará los usuarios adecuados a esos grupos. Cuando los usuarios inician sesión en sus estaciones de trabajo, el cliente de virtualización de la aplicación, de forma predeterminada, realiza una actualización de publicación con las credenciales del usuario que ha iniciado sesión. Después, el usuario puede iniciar las aplicaciones desde cualquier lugar en el que se hayan colocado los métodos abreviados. El administrador de la aplicación virtualización de la aplicación determina dónde y cuántos métodos abreviados se encuentran en el sistema cliente durante la secuenciación de la aplicación.

**Nota:**  Una *actualización de publicación* es una llamada al servidor de virtualización de aplicaciones que se define en el cliente de virtualización de aplicaciones, para determinar qué accesos directos a aplicaciones virtuales se envían al cliente para su uso por parte del usuario final.

 

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Introducción a los componentes del sistema de virtualización de aplicaciones](overview-of-the-application-virtualization-system-components.md)

[Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





