---
title: Acerca de la pestaña Propiedades
description: Acerca de la pestaña Propiedades
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819921"
---
# Acerca de la pestaña Propiedades


Use la pestaña **propiedades** para ver información estadística básica sobre un paquete de aplicación de secuencia. La información se genera automáticamente a menos que se indique lo contrario. Esta pestaña contiene los siguientes elementos.

## Información de paquete


<a href="" id="package-name"></a>**Nombre del paquete**  
El único nombre que se usa para un paquete de aplicación de secuencia que puede contener una o más aplicaciones (por ejemplo, Microsoft Office se puede usar para etiquetar un paquete de aplicación de secuencia que contiene aplicaciones de Microsoft Word y Microsoft Excel que se ejecutan en el mismo entorno virtual).

<a href="" id="comments"></a>**Observaciones**  
Muestra una breve descripción del paquete de software que aparecerá en el elemento ABSTRACT del archivo de descriptor de software abierto (OSD). Este elemento es opcional.

<a href="" id="package-version"></a>**Versión del paquete**  
La versión de paquete de la aplicación secuenciada.

<a href="" id="package-guid"></a>**GUID de paquete**  
El identificador único global (GUID) se asigna automáticamente al paquete de la aplicación de secuencia para distinguirlo de otros paquetes de aplicación secuenciados que se pueden estar ejecutando en el equipo al que se transmite un paquete de aplicación de secuencia.

<a href="" id="package-version-guid"></a>**GUID de versión de paquete**  
El GUID de versión del paquete de aplicaciones secuenciados.

<a href="" id="root-directory"></a>**Directorio raíz**  
El directorio del equipo de secuenciación en el que se instalan los archivos para el paquete de aplicación de secuencia. Este directorio también se crea en el equipo al que se transmitirá un paquete de aplicación de secuencia. Para la compatibilidad con versiones anteriores, se recomienda un nombre de directorio de formato 8,3 en la raíz de la unidad Q, como Q:\\MyApp.1\\.

<a href="" id="created"></a>**Crear**  
La fecha y la hora en que se creó el paquete de aplicación de la secuencia.

<a href="" id="modified"></a>**Modificado**  
La fecha y la hora en que se modificó por última vez el paquete de aplicación de la secuencia.

<a href="" id="package-size"></a>**Tamaño del paquete**  
El tamaño del paquete en megabytes.

<a href="" id="launch-size"></a>**Tamaño de inicio**  
El tamaño en megabytes de la parte del archivo SFT necesaria para iniciar la aplicación.

## Parámetros de secuenciación


<a href="" id="block-size"></a>**Tamaño de bloque**  
Especifica el tamaño de los bloques de características principales y secundarios en los que se divide el archivo SFT por transmisión a través de una red. Todos los bloques son iguales al tamaño especificado; sin embargo, el último bloque puede ser más pequeño de lo especificado. Verá uno de los siguientes valores:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

**Nota:**  Una vez creado el paquete inicial, el valor de tamaño de bloque no se modifica.

 

## Temas relacionados


[Cómo cambiar las propiedades del paquete](how-to-change-package-properties.md)

[Consola de secuenciador](sequencer-console.md)

 

 





