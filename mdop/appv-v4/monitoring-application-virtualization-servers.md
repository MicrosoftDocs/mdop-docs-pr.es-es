---
title: Supervisión de servidores de virtualización de aplicaciones
description: Supervisión de servidores de virtualización de aplicaciones
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816141"
---
# Supervisión de servidores de virtualización de aplicaciones


Para simplificar la administración de servidores de Application Virtualization (App-V), puede usar el módulo de administración de System Center Operations Manager2007. Este módulo de administración solo admite servidores de virtualización de aplicaciones (App-V) 4,5; no es compatible con versiones anteriores del servidor. El módulo de administración maximiza la disponibilidad del servidor de App-V para administrar solicitudes de cliente de App-V.

## Indicadores de estado


Los indicadores de estado de estado del servidor de App-V están codificados por colores. Los colores representan los siguientes valores de estado:

-   Sin color indica que el servidor se está ejecutando sin errores no recuperables.

-   Amarillo indica que uno de los componentes no funciona correctamente. La funcionalidad general del servidor está desactualizada, pero el servidor aún está disponible.

-   Rojo indica que el servidor no está disponible y que no puede proporcionar servicios clave o comunicarse con dependencias de servicio externo.

## Criterios de supervisión


El módulo de administración supervisa los siguientes aspectos de estado del servidor:

-   Estado del servidor: supervisa los eventos del servidor para validar que el servidor proporciona los servicios esperados.

-   Acceso a almacén de datos: realiza un seguimiento de la capacidad de uno o varios de los servidores de administración de App-V para obtener acceso al almacén de datos de App-V y comunicarse con él.

-   Acceso a datos de contenido: supervisa el acceso al directorio \\Content, que puede ser un directorio local o un recurso compartido de red, y la capacidad de leer los archivos solicitados.

-   Seguridad: informa de errores con el certificado del servidor de App-V y las comunicaciones seguras.

-   Administración de solicitudes de cliente: supervisa la capacidad de uno o más de los servidores de App-V para controlar y responder correctamente a las solicitudes de los clientes. Estas solicitudes incluyen publicar elementos tales como solicitudes de configuración, solicitudes de carga de paquetes y solicitudes fuera de secuencia.

-   Configuración del servidor: comprueba los valores de configuración del servidor de App-V. Estas opciones de configuración incluyen la configuración en el registro y en el almacén de datos de App-V.

## Diferencias de servidor


Las principales diferencias entre el servidor de administración de App-V y el servidor de streaming de App-V son las siguientes:

-   Los servidores de administración de App-V pueden proporcionar servicios de publicación, transmisión, administración y creación de informes. Por lo tanto, el módulo de administración puede administrar más aspectos del servidor de administración de App-V que puede administrar en el servidor de streaming de App-V, que solo proporciona transmisión por secuencias de paquetes.

-   El servidor de streaming de App-V no tiene un almacén de datos de App-V, por lo que el acceso al almacén de datos no se supervisa. La información de configuración del servidor de streaming de App-V se administra en el registro.

-   El servidor de streaming de App-V no usa la interfaz de la consola de administración de servidores de App-V; use otras herramientas para administrar la configuración.

## Temas relacionados


[Servidor de virtualización de aplicaciones](application-virtualization-server.md)

 

 





