---
title: Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final
description: Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final
author: dansimp
ms.assetid: 27c1e1c6-123a-4f8a-b7d2-5bddc9ca3249
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 485823c17d650323ca68cccf1308ac8ec9e5212b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822581"
---
# Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final


Si no puede acceder a las herramientas de depuración de Microsoft para Windows o a los archivos de símbolos en el equipo del usuario final, puede copiar el archivo de volcado desde el equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del analizador de bloqueos, como un equipo del servicio de asistencia que contenga Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

Para ejecutar el analizador de bloqueos en modo independiente, copie el archivo de volcado de memoria del equipo problemático y analicelo en otro equipo, como un equipo del servicio de asistencia, que tenga instalado el **analizador de bloqueos** .

**Para ejecutar el analizador de bloqueos en el modo independiente**

1.  En un equipo que tenga instalado DaRT 10, haga clic en **Inicio**, escriba **Crash Analyzer**y, a continuación, haga clic en **Crash Analyzer**.

2.  Siga los pasos que se indican en el asistente, como se describe en [Cómo ejecutar el analizador de bloqueos en un equipo de usuario final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-10.md).

## Temas relacionados


[Operaciones para DaRT 10](operations-for-dart-10.md)

[Diagnóstico de errores del sistema con el analizador de bloqueo](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md)

 

 





