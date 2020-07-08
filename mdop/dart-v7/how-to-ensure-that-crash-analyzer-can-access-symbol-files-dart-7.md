---
title: Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos
description: Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos
author: dansimp
ms.assetid: 150a2f88-68a5-40eb-8471-e5008488ab6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db56bb21ad885d1e3aa73bcbd922a7e8bde77080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822801"
---
# Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos


Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del ejecutable. Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si se ha bloqueado.

Los archivos de símbolos se descargan automáticamente al ejecutar el analizador de bloqueo de Microsoft Diagnostics and Recovery Toolset (DaRT) 7. Si el equipo no tiene una conexión a Internet o la red requiere que el equipo tenga acceso a un servidor proxy HTTP, los archivos de símbolos no se pueden descargar.

## Garantizar el acceso a los archivos de símbolos


Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del ejecutable. Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si se ha bloqueado.

Los archivos de símbolos se descargan automáticamente al ejecutar **Crash Analyzer**. Si el equipo no tiene una conexión a Internet o la red requiere que el equipo tenga acceso a un servidor proxy HTTP, los archivos de símbolos no se pueden descargar.

A continuación se muestra una lista de las opciones que están disponibles para garantizar el acceso a los archivos de símbolos:

-   **Copie el archivo de volcado a otro equipo.** Si los símbolos no se pueden descargar debido a la falta de conexión a Internet, copie el archivo de volcado en un equipo que tenga conexión a Internet y ejecute el **Asistente para bloqueo de bloqueo** independiente en ese equipo.

-   **Acceder a los archivos de símbolos desde otro equipo.** Si los símbolos no se pueden descargar debido a la falta de conexión a Internet, puede descargar los símbolos de un equipo que tenga una conexión a Internet y, después, copiarlos en el equipo que no tiene conexión a Internet, o bien puede asignar una unidad de red a una ubicación en la que los símbolos estén disponibles en la red local. Si ejecuta el **analizador de bloqueos** en un entorno de recuperación de Windows (WindowsRE), puede incluir los archivos de símbolos en la imagen de recuperación de DART. Para obtener más información sobre cómo crear una imagen de recuperación, consulte [creación de la imagen de recuperación de DaRT 7,0](creating-the-dart-70-recovery-image-dart-7.md).

-   **Acceder a archivos de símbolos a través de un servidor proxy HTTP.** Si los símbolos no se pueden descargar porque se debe acceder a un servidor proxy HTTP, siga los pasos siguientes para acceder a un servidor proxy HTTP. En DaRT7, el **Asistente para analizar el analizador** tiene una configuración disponible en la página de diálogo **especificar la ubicación de los archivos de símbolos** , marcada con el servidor proxy de etiqueta **(opcional, con el formato "servidor: puerto")**. Puede usar este cuadro de texto para especificar un servidor proxy. Escriba la dirección de proxy con el formato ** &lt; hostname &gt; : &lt; Port &gt; **, donde el nombre de &lt; **host** &gt; es un nombre DNS o una dirección IP, y el &lt; **Puerto** &gt; es un número de puerto TCP, normalmente 80. Hay dos modos en los que se puede ejecutar el **analizador de bloqueos** . A continuación se describe cómo usar la configuración de proxy en cada uno de estos modos:

    -   **Modo en línea:** En este modo, si el campo de servidor proxy se deja en blanco, el asistente usará la configuración de proxy de opciones de Internet en el panel de control. Si escribe una dirección de proxy en el cuadro de texto que se proporciona, se usará esa dirección y se anulará la configuración de las opciones de Internet.

    -   **Entorno de recuperación de Windows (WindowsRE):** Cuando ejecuta **Crash Analyzer** desde la ventana **conjunto de herramientas de diagnóstico y recuperación** , no hay ninguna dirección de proxy predeterminada. Si el equipo está conectado directamente a Internet, no se necesita una dirección de proxy. Por lo tanto, puede dejar este campo en blanco en la configuración del asistente. Si el equipo no está directamente conectado a Internet y se encuentra en un entorno de red que tiene un servidor proxy, debe establecer el campo de proxy en el Asistente para obtener acceso al almacén de símbolos. La dirección de proxy puede obtenerse del administrador de red. La configuración del servidor proxy es importante solo cuando el almacén de símbolos público está conectado a Internet. Si los símbolos ya están en la imagen de recuperación de DaRT, o si están disponibles de forma local, no es necesario configurar el servidor proxy.

## Temas relacionados


[Diagnóstico de errores del sistema con el analizador de bloqueo](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





