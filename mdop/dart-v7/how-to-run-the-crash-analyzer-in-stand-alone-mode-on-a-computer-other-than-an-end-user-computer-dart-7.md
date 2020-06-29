---
title: Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final
description: Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822790"
---
# Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final


Si no puede acceder a las herramientas de depuración de Microsoft para Windows o a los archivos de símbolos en el equipo del usuario final, puede copiar el archivo de volcado desde el equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del analizador de bloqueos, por ejemplo, en el equipo de un administrador del servicio de asistencia al cliente.

**Para ejecutar el analizador de bloqueos en el modo independiente**

1.  En un equipo con DaRT7 instalado, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft DART 7**.

2.  Proporcione la información necesaria para lo siguiente:

    -   Herramientas de depuración de Microsoft para Windows

    -   Archivos de símbolos

        Para obtener más información acerca de los archivos de símbolos, consulte [Cómo asegurarse de que el analizador de bloqueo puede acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Archivo de volcado

        **Nota:**  Use la herramienta de búsqueda de DaRT7 para localizar el archivo de volcado de sucesos copiado.

         

3.  El **analizador de bloqueo** examina el archivo de volcado de sucesos e informa de la causa probable del bloqueo. Puede ver más información sobre el bloqueo, como el mensaje de bloqueo específico y la descripción, los drivers cargados en el momento del bloqueo y la salida completa del análisis.

4.  Decidir cuál es la estrategia adecuada para resolver el problema. Esto puede requerir que se deshabilite o actualice el controlador de dispositivo que causó el bloqueo mediante el nodo **servicios y drivers** de la herramienta **Administración de equipos** de DART.

## Temas relacionados


[Diagnóstico de errores del sistema con el analizador de bloqueo](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





