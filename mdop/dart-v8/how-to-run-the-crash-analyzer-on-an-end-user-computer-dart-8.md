---
title: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
description: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
author: dansimp
ms.assetid: d36213e5-7719-44d7-be65-971c3ef7df2c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 028f1dd0a1651809ec54ae19094302586d864f99
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824370"
---
# Cómo ejecutar el analizador de bloqueo en un equipo de usuario final


Para ejecutar el **analizador de bloqueos** de la ventana del **conjunto de herramientas de diagnóstico y recuperación** en un equipo del usuario final que tiene problemas, debe tener instaladas las herramientas de depuración de Microsoft para Windows y los archivos de símbolos. Para descargar las herramientas de depuración de Windows, vea [herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).

**Para ejecutar el analizador de bloqueos en un equipo de usuario final**

1.  En la ventana **conjunto de herramientas de diagnóstico y recuperación** en un equipo de usuario final, haga clic en **analizador de bloqueos**.

2.  Proporcione la información necesaria para las herramientas de depuración de Microsoft para Windows.

3.  Proporcione la información necesaria para los archivos de símbolos. Para obtener más información sobre los archivos de símbolos, vea [Cómo asegurarse de que el analizador de bloqueo puede acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).

4.  Proporcione la información necesaria para un archivo de volcado de memoria. Para determinar la ubicación del archivo de volcado de memoria:

    1.  Abra la ventana **propiedades del sistema** .

    2.  Haga clic en **Inicio**, escriba **sysdm.cpl**y, a continuación, presione **entrar**.

    3.  Haz clic en la pestaña **Opciones avanzadas**.

    4.  En el área **Inicio y recuperación** , haga clic en **configuración**.

        Si no tiene acceso a la ventana **propiedades del sistema** , puede buscar archivos de volcado en el equipo del usuario final con la herramienta de **búsqueda** de Microsoft Diagnostics and Recovery Toolset (DART) 8,0.

    El **analizador de bloqueo** examina el archivo de volcado de memoria e informa de la causa probable del problema. Puede ver más información sobre el error, como el mensaje específico de volcado de memoria y la descripción, los drivers cargados en el momento del error y el resultado completo del análisis.

5.  Identifique la estrategia adecuada para resolver el problema. La estrategia puede requerir que se deshabilite o actualice el controlador de dispositivo que causó el error con el nodo **servicios y drivers** de la herramienta **Administración de equipos** de DART 8,0.

## Temas relacionados


[Diagnóstico de errores del sistema con el analizador de bloqueo](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[Operaciones para DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





