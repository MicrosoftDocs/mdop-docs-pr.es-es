---
title: Diagnóstico de errores del sistema con el analizador de bloqueo
description: Diagnóstico de errores del sistema con el analizador de bloqueo
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823470"
---
# Diagnóstico de errores del sistema con el analizador de bloqueo


El analizador de bloqueo de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 le permite depurar un archivo de volcado en un equipo basado en Windows y, a continuación, diagnosticar errores de equipos relacionados. El analizador de bloqueo utiliza las herramientas de depuración de Microsoft para Windows para examinar un archivo de volcado para el controlador que causó el error del equipo.

## Ejecutar el analizador de bloqueos en un equipo de usuario final


Normalmente, el analizador de bloqueos se ejecuta desde la ventana del conjunto de herramientas de diagnóstico y recuperación en un equipo de usuario final que tiene problemas. El analizador de bloqueo intenta localizar las herramientas de depuración para Windows en el equipo problemático. Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o examinar la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft). También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.

Si incluyó las herramientas de depuración de Microsoft para Windows y los archivos de símbolos cuando creó la imagen de recuperación de DaRT, deberían estar disponibles cuando ejecute el analizador de bloqueos en el equipo problemático.

[Cómo ejecutar el analizador de bloqueo en un equipo de usuario final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## Ejecutar el analizador de bloqueos en modo independiente en un equipo que no sea un equipo de usuario final


El analizador de bloqueo intenta localizar las herramientas de depuración para Windows en el equipo problemático. Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o examinar la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft). También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.

Si no incluía las herramientas de depuración de Microsoft para Windows y los archivos de símbolos cuando creó la imagen de recuperación de DaRT, o si hay problemas de conectividad de red o de tamaño de disco que le impiden obtenerla, puede copiar el archivo de volcado del equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del analizador de bloqueo , como el equipo de un administrador del servicio de asistencia.

[Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## Asegurarse de que el analizador de bloqueos puede tener acceso a los archivos de símbolos


Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del ejecutable. Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si se ha bloqueado.

Los archivos de símbolos se descargan automáticamente al ejecutar Crash Analyzer. Si el equipo no tiene una conexión a Internet o la red requiere que el equipo tenga acceso a un servidor proxy HTTP, los archivos de símbolos no se pueden descargar.

[Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## Otros recursos para diagnosticar errores del sistema con el analizador de bloqueo


[Operaciones para DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





