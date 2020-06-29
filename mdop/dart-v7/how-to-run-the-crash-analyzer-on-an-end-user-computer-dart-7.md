---
title: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
description: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823840"
---
# Cómo ejecutar el analizador de bloqueo en un equipo de usuario final


Normalmente, se ejecuta Microsoft Diagnostics and Recovery Toolset (DaRT) 7 Crash Analyzer en la ventana del conjunto de herramientas de diagnóstico y recuperación en un equipo de usuario final que tiene problemas. El analizador de bloqueo intenta localizar las herramientas de depuración para Windows en el equipo problemático. Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o examinar la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft). También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.

**Para abrir y ejecutar el analizador de bloqueo en un equipo de usuario final**

1.  En la ventana **conjunto de herramientas de diagnóstico y recuperación** en un equipo de usuario final, haga clic en **analizador de bloqueos**.

2.  Proporcione la información necesaria para lo siguiente:

    -   Herramientas de depuración de Microsoft para Windows

    -   Archivos de símbolos

        Para obtener más información acerca de los archivos de símbolos, consulte [Cómo asegurarse de que el analizador de bloqueo puede acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Archivo de volcado

        Siga estos pasos para determinar la ubicación del archivo de volcado:

        1.  Abra la ventana **propiedades del sistema** .

            Haga clic en **Inicio**, escriba sysdm.cpl y, a continuación, presione Entrar.

        2.  Haz clic en la pestaña **Opciones avanzadas**.

        3.  En el área **Inicio y recuperación** , haga clic en **configuración**.

        **Nota:**  Si no tiene acceso a la ventana **propiedades del sistema** , puede buscar archivos de volcado en el equipo del usuario final con la herramienta de **búsqueda** de DART.

         

3.  El **analizador de bloqueo** examina el archivo de volcado de sucesos e informa de la causa probable del bloqueo. Puede ver más información sobre el bloqueo, como el mensaje de bloqueo específico y la descripción, los drivers cargados en el momento del bloqueo y la salida completa del análisis.

4.  Decidir cuál es la estrategia adecuada para resolver el problema. Esto puede requerir que se deshabilite o actualice el controlador de dispositivo que causó el bloqueo mediante el nodo **servicios y drivers** de la herramienta **Administración de equipos** de DART.

## Temas relacionados


[Diagnóstico de errores del sistema con el analizador de bloqueo](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





