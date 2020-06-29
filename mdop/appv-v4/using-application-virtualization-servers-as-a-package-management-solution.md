---
title: Uso de servidores de virtualización de aplicaciones como solución de administración de paquetes
description: Uso de servidores de virtualización de aplicaciones como solución de administración de paquetes
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815121"
---
# Uso de servidores de virtualización de aplicaciones como solución de administración de paquetes


Si no tiene un sistema ESD existente para implementar su solución de virtualización de aplicaciones o no desea usar uno, tendrá que instalar uno o varios servidores de administración de virtualización de aplicaciones como núcleo de la arquitectura del sistema. El servidor de administración de virtualización de aplicaciones requiere un equipo de servidor dedicado y necesita una base de datos de Microsoft SQL Server. La base de datos puede estar en el mismo servidor o puede configurarse en un servidor de base de datos corporativo que sea accesible para el servidor de administración de virtualización de la aplicación a través de una conexión LAN de alta velocidad. Además, tendrá que instalar la consola de administración de Microsoft Application Virtualization en el servidor de administración de Application Virtualization o en una estación de trabajo de administración designada, y tendrá que instalar el servicio Web de administración de virtualización de aplicaciones de Microsoft, que también se puede instalar en el servidor de administración de virtualización de aplicaciones o en un servidor IIS independiente. La consola de administración de virtualización de aplicaciones se usa para conectarse al servicio Web de administración de virtualización de aplicaciones, lo que permite que el administrador del sistema interactúe con el servidor de Application Virtualization Management.

**Nota:**  El acceso a las aplicaciones se controla mediante grupos de seguridad en los servicios de dominio de Active Directory, por lo que tendrá que planear un proceso para configurar un grupo de seguridad para cada aplicación virtualizada y para administrar los usuarios que se agregan a cada grupo. El administrador del servidor de Application Virtualization Management configura el servidor para usar estos grupos de Active Directory y, a continuación, el servidor controla automáticamente el acceso a los paquetes según la pertenencia a grupos de Active Directory.

 

## En esta sección


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Introducción a los componentes del sistema de virtualización de aplicaciones](overview-of-the-application-virtualization-system-components.md)  
Enumera y describe los componentes principales del sistema de administración de virtualización de aplicaciones de Microsoft.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
Proporciona una breve introducción sobre cómo se publican las aplicaciones virtuales en un escenario de implementación basado en el servidor de virtualización de aplicaciones.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
Describe las opciones disponibles para usar servidores de streaming de Application Virtualization junto con la implementación basada en el servidor de virtualización de aplicaciones.

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)

 

 





