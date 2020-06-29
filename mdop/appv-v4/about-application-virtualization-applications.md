---
title: Acerca de las aplicaciones de virtualización de aplicaciones
description: Acerca de las aplicaciones de virtualización de aplicaciones
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820090"
---
# Acerca de las aplicaciones de virtualización de aplicaciones


En la virtualización de aplicaciones, una *aplicación* es un programa ejecutable, como Microsoft Visio, que se transmite al cliente o cliente de escritorio de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server) desde un servidor de administración de virtualización de aplicaciones. Antes de que se pueda transmitir una aplicación a un cliente, la aplicación debe estar preparada para la transmisión por secuencias al procesarla con el secuenciador de Application Virtualization.

## Administración de aplicaciones


Para que los usuarios puedan disponer de las aplicaciones, debe agregar las aplicaciones al sistema. El método más común para agregar aplicaciones al sistema es importarlas. Para obtener acceso a esta característica, haga clic con el botón derecho en el nodo **aplicaciones** en la consola de administración del servidor de virtualización de aplicaciones y elija **importar aplicaciones**.

Puede importar más de un archivo descriptor de software abierto (OSD) al mismo tiempo o importar un archivo SPRJ (SPRJ) que pueda contener varios archivos OSD. Esta funcionalidad le permite configurar aplicaciones relacionadas de forma similar.

También puede usar las siguientes características para ayudarle a administrar sus aplicaciones:

-   **Grupos de aplicaciones**: le permite crear grupos lógicos de aplicaciones para simplificar la administración. Cuando se realizan cambios en un grupo (por ejemplo, permisos de acceso), los cambios se aplican a todas las aplicaciones del grupo. Las aplicaciones de un grupo pueden provenir de diferentes paquetes.

-   **Selección múltiple**: permite seleccionar varias aplicaciones al mismo tiempo manteniendo presionada la tecla Ctrl al hacer clic en una aplicación para modificar las propiedades de la aplicación. Sin embargo, si desea mantener una relación entre las aplicaciones, debe crear un grupo de aplicaciones para que contenga las aplicaciones.

-   **Copia entre sistemas**: le permite copiar aplicaciones de un entorno a otro entorno que ejecute la misma versión de App-V en un solo paso. Por ejemplo, es posible que tenga un entorno de prueba de aceptación de usuario en el que inicialmente implemente y configure las aplicaciones. Después de finalizar la fase de prueba, es posible que desee replicar el mismo conjunto de aplicaciones (incluidos los permisos) en el entorno de producción.

## Temas relacionados


[Acerca de los paquetes de virtualización de aplicaciones](about-application-virtualization-packages.md)

[Acerca de la consola de administración de servidor de virtualización de aplicaciones](about-the-application-virtualization-server-management-console.md)

[Cómo administrar grupos de aplicaciones en la consola de administración de servidor](how-to-manage-application-groups-in-the-server-management-console.md)

[Cómo administrar aplicaciones en la consola de administración de servidor](how-to-manage-applications-in-the-server-management-console.md)

 

 





