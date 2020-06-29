---
title: Introducción a escenario basado en la distribución electrónica de software
description: Introducción a escenario basado en la distribución electrónica de software
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821600"
---
# Introducción a escenario basado en la distribución electrónica de software


Si planea usar una solución de distribución electrónica de software (ESD) para implementar aplicaciones virtuales, es importante comprender los factores que entran en la misma y que se ven afectados por esta decisión. En este tema se describen las ventajas de usar un escenario basado en ESD y se proporciona información sobre los métodos de transferencia de paquetes y publicación que necesitará tener en cuenta a medida que continúa con la implementación.

**Importante**  Sea cual sea la solución ESD que use, debe estar familiarizado con los requisitos de su solución en particular. Si está usando Microsoft Endpoint Configuration Manager, consulte la documentación de Configuration Manager en <https://go.microsoft.com/fwlink/?LinkId=66999> .

 

El uso de un sistema ESD existente le ofrece las siguientes ventajas:

-   Elimina las infraestructuras de administración duales

-   Reduce el costo de hardware adicional

-   Reduce el costo de las licencias de sistemas operativos y bases de datos adicionales

## Métodos de publicación


Al usar un escenario basado en ESD, tiene las siguientes opciones para publicar la aplicación en los clientes:

-   **Windows Installer independiente.** El archivo de Windows Installer contiene el manifiesto y los archivos OSD y OSD que usan los clientes para configurar un paquete. El archivo de Windows Installer también copia el archivo SFT al cliente porque este escenario no usa un servidor.

-   **Windows Installer con el manifiesto del paquete.** El archivo de Windows Installer contiene el manifiesto y los archivos OSD y OSD que usan los clientes para configurar un paquete. El archivo SFT se almacena en un servidor. Un parámetro de la línea de comandos dirige al cliente a la ubicación del archivo SFT.

-   **Comandos SFTMIME.** Los comandos de SFTMIME se usan con los archivos manifest, OSD, ICO y SFT para agregar paquetes al cliente. El archivo de manifiesto debe estar en el equipo cliente o debe ser accesible a través de una ruta UNC. Dependiendo de la configuración del cliente y de las opciones de la línea de comandos, los archivos OSD, ICO y SFT pueden encontrarse en el equipo cliente o en un servidor.

Para obtener información más detallada sobre los métodos de publicación anteriores, vea [determinar el método de publicación](determine-your-publishing-method.md).

## Métodos de streaming de paquetes


Tendrá que determinar el método que usará el sistema de virtualización de aplicaciones para transmitir los paquetes de aplicaciones virtuales o los archivos SFT del servidor a los clientes. Las siguientes opciones de transmisión por secuencias están disponibles:

-   **Servidor de streaming de Application Virtualization.** Si usa un servidor de streaming de Application Virtualization en su configuración, los archivos SFT se transmiten a los clientes de ese servidor con los protocolos RTSP o RTSPs. Debe instalar el software de servidor en un equipo y debe configurarlo a través del registro, pero esta configuración no depende de servicios como SQL o servicios de dominio de Active Directory. Los archivos de SFT se almacenan en el servidor en una ubicación accesible para los clientes. La información de publicación se puede distribuir a los clientes a través de cualquier mecanismo de distribución. Sin embargo, cuando se configura, el cliente recibe actualizaciones de paquetes de forma automática y se admite la actualización activa.

-   **Servidor de administración de virtualización de aplicaciones.** Si usa un servidor de administración de virtualización de aplicaciones en su configuración, los archivos SFT se transmiten a los clientes de ese servidor con los protocolos RTSP o RTSPs. Este servidor se administra a través de la consola de administración de virtualización de aplicaciones. Esta configuración usa una base de datos SQL y servicios de Active Directory. El servidor puede distribuir información de publicación a los clientes, por lo que no es necesario realizar otros mecanismos de publicación.

-   **Servidor de archivos.** Si usa un servidor de archivos en su configuración, los archivos SFT se transmiten a los otros equipos cliente mediante protocolos SMB. Los servidores de archivos usados en esta configuración se administran mediante la creación de listas de control de acceso (ACLs) en los archivos compartidos y SFT. Debe tener cuidado para dirigir a los clientes a los archivos correctos en el servidor de archivos.

-   **Servidor IIS.** Si usa un servidor IIS en su configuración, los archivos SFT se transmiten a los clientes de ese servidor mediante protocolos HTTP o HTTPS. El servidor IIS es fácil de configurar y administrar. Debe tener cuidado para dirigir a los clientes a los archivos correctos en el servidor IIS.

Para obtener información más detallada sobre los métodos anteriores de transmisión por secuencias, vea [determinar el método de transmisión por secuencias](determine-your-streaming-method.md).

## Temas relacionados


[Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md)

[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Determinar el método de publicación](determine-your-publishing-method.md)

[Determinar el método de streaming](determine-your-streaming-method.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





