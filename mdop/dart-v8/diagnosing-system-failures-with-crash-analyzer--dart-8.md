---
title: Diagnóstico de errores del sistema con el analizador de bloqueo
description: Diagnóstico de errores del sistema con el analizador de bloqueo
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824541"
---
# Diagnóstico de errores del sistema con el analizador de bloqueo


El **analizador de bloqueo** de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 le permite depurar un archivo de volcado de memoria en un equipo basado en Windows y, a continuación, diagnosticar errores de equipos relacionados. El **analizador de bloqueo** usa las herramientas de depuración de Microsoft para Windows para examinar un archivo de volcado de memoria para el controlador que causó el error del equipo. Puede ejecutar el analizador de bloqueos en un equipo del usuario final o en el modo independiente en un equipo que no sea un equipo de usuario final.

## Ejecutar el analizador de bloqueo en un equipo de usuario final


Normalmente, el **analizador de bloqueos** se ejecuta desde la ventana del **conjunto de herramientas de diagnóstico y recuperación** en un equipo del usuario final que está experimentando el problema. El **analizador de bloqueo** intenta localizar las herramientas de depuración para Windows en el equipo problemático. Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o ir a la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft). También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.

Si incluyó las herramientas de depuración de Microsoft para Windows y los archivos de símbolos cuando creó la imagen de recuperación de DaRT 8,0, las herramientas y los archivos de símbolos deberían estar disponibles cuando ejecute el **analizador de bloqueos** en el equipo problemático. Si no los incluía en la imagen de recuperación de DaRT, o si hay problemas de conectividad de red o de tamaño de disco que le impiden obtenerlos, también puede ejecutar el analizador de bloqueos autónomos en un equipo que no sea el equipo del usuario final, como se describe en la siguiente sección.

[Cómo ejecutar el analizador de bloqueo en un equipo de usuario final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a>Ejecutar el analizador de bloqueos en el modo independiente en un equipo que no sea el equipo del usuario final


Aunque normalmente ejecuta el **analizador de bloqueos** en el equipo del usuario final que está experimentando el problema, también puede ejecutar el analizador de bloqueos en el modo independiente, en un equipo que no sea un equipo de usuario final. Puede elegir esta opción si no ha incluido las herramientas de depuración de Windows en la imagen de recuperación de DaRT, o si hay problemas de conectividad de red o de tamaño de disco que impiden la obtención de las herramientas de depuración. En este caso, puede copiar el archivo de volcado desde el equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del **analizador de bloqueo** , como en el equipo de un agente de asistencia.

[Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## Cómo garantizar que el analizador de bloqueo pueda tener acceso a los archivos de símbolos


Para depurar las aplicaciones que han dejado de responder, necesita tener acceso al archivo de símbolos, que es independiente del programa. Aunque los archivos de símbolos se descargan automáticamente al ejecutar Crash Analyzer, puede haber ocasiones en las que el equipo problemático no tenga acceso a Internet. Hay varias maneras de asegurarse de que ha garantizado el acceso a los archivos de símbolos.

[Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## Otros recursos para diagnosticar errores del sistema con el analizador de bloqueo


[Operaciones para DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





