---
title: Guía de planeación e implementación del sistema de virtualización de aplicaciones
description: Guía de planeación e implementación del sistema de virtualización de aplicaciones
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815960"
---
# Guía de planeación e implementación del sistema de virtualización de aplicaciones


La administración de Microsoft Application Virtualization proporciona la capacidad de hacer que las aplicaciones estén disponibles para los equipos de los usuarios finales sin tener que instalar las aplicaciones directamente en esos equipos. Esto es posible gracias a un proceso conocido como *la secuenciación de la aplicación*, que permite que cada aplicación se ejecute en su propio entorno virtual independiente en el equipo cliente. Las aplicaciones secuenciadas se aíslan entre sí, lo que elimina los conflictos de las aplicaciones y aún así puede interactuar con el equipo cliente.

El cliente de virtualización de aplicaciones es el componente del sistema de virtualización de aplicaciones que permite al usuario final interactuar con las aplicaciones después de que se hayan publicado en el equipo. El cliente administra el entorno virtual en el que se ejecutan las aplicaciones virtualizadas en cada equipo. Una vez instalado el cliente en un equipo, las aplicaciones deben estar disponibles para el equipo a través de un proceso conocido como *publicación*, que permite al usuario final ejecutar las aplicaciones virtuales. El proceso de publicación coloca los iconos de aplicación virtual y los accesos directos en el equipo (por lo general en el escritorio de Windows o en el menú **Inicio** ) y también coloca la definición de paquete y la información de Asociación de tipo de archivo en el equipo. La publicación también hace que el contenido del paquete de la aplicación esté disponible para el equipo del usuario final.

El contenido del paquete de la aplicación virtual se puede colocar en uno o varios servidores de virtualización de aplicaciones para que pueda transmitirse a los clientes a petición y almacenarse en la memoria caché local. Los servidores de archivos y los servidores web también se pueden usar como servidores de transmisión por secuencias, o el contenido se puede colocar directamente en el equipo del usuario final, por ejemplo, si está usando un sistema de distribución de software electrónico, como Microsoft Endpoint Configuration Manager. En una implementación de varios servidores, mantener el contenido del paquete y mantenerlo actualizado en todos los servidores de transmisión requiere una solución completa de administración de paquetes. Según el tamaño de su organización, es posible que tenga que tener muchas aplicaciones virtuales accesibles para los usuarios finales de todo el mundo. Administración de paquetes para asegurarse de que las aplicaciones correctas estén disponibles para todos los usuarios donde y cuando necesiten tener acceso a ellas es por lo tanto un requisito esencial.

La guía de planeación e implementación de virtualización de aplicaciones proporciona información que le ayudará a comprender e implementar mejor la aplicación de virtualización de Microsoft Application y sus componentes. También proporciona procedimientos paso a paso para implementar los escenarios de implementación clave.

## En esta sección


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)  
Proporciona las instrucciones necesarias para planear la implementación y la implementación de su sistema de virtualización de aplicaciones.

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones](application-virtualization-deployment-and-upgrade-considerations.md)  
Proporciona información sobre los requisitos de hardware y software para instalar los diversos componentes de virtualización de aplicaciones, así como información de actualización.

<a href="" id="electronic-software-distribution-based-scenario"></a>[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)  
Proporciona información sobre cómo implementar la virtualización de aplicaciones mediante un sistema de distribución de software electrónico (ESD).

<a href="" id="application-virtualization-server-based-scenario"></a>[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)  
Proporciona información sobre cómo implementar la virtualización de aplicaciones con el servidor de administración de virtualización de aplicaciones.

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[Escenario de distribución independiente para clientes de virtualización de aplicaciones](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
Describe cómo implementar la virtualización de aplicaciones en modo independiente, sin necesidad de usar los recursos ESD o basados en el servidor.

<a href="" id="application-virtualization-reference"></a>[Referencia de virtualización de aplicaciones](application-virtualization-reference.md)  
Contiene material de referencia técnica detallado relacionado con la instalación y la administración de componentes del sistema.

 

 





