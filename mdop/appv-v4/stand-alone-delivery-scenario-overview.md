---
title: Introducción al escenario de distribución independiente
description: Introducción al escenario de distribución independiente
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815310"
---
# Introducción al escenario de distribución independiente


El escenario de entrega independiente es una solución ideal de virtualización de aplicaciones para entornos en los que la conectividad de bajo nivel de ancho de banda o sin conectividad limita la capacidad del cliente de escritorio de virtualización de aplicaciones para transmitir aplicaciones desde servidores centralizados. En estos entornos, los usuarios a menudo trabajan de manera remota y los propietarios de dispositivos instalan aplicaciones con los archivos de Windows Installer.

Puede usar el secuenciador de Application Virtualization para crear aplicaciones secuenciadas que incluyan archivos de Windows Installer. Estos paquetes incluyen las aplicaciones virtualizadas, la información de publicación y las rutinas de instalación necesarias para instalar los paquetes en los sistemas cliente. El instalador agrega el paquete de la aplicación virtual al cliente de escritorio de Microsoft Application Virtualization. La información de la publicación está configurada para cargar aplicaciones desde una ubicación local en lugar de transmitirlas a través de una WAN. Los usuarios pueden conectarse temporalmente a una red para recuperar los archivos de Windows Installer o pueden ejecutarlos desde un DVD.

El escenario de entrega independiente proporciona a los usuarios las siguientes ventajas:

-   Operación de implementación simple.

-   No se necesitan redes y servidores en tiempo de ejecución.

-   Aplicaciones previamente almacenadas en caché y disponibles para todos los usuarios.

El escenario de entrega independiente tiene las siguientes limitaciones:

-   Los informes integrados y automatizados no están disponibles; los informes deben generarse con herramientas externas de creación de informes.

-   Las aplicaciones se deben entregar al cliente de forma manual, como los archivos originales de Windows Installer.

## Temas relacionados


[Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)

[Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md)

 

 





