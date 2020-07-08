---
title: Notas de la versión de DaRT 8.0 SP1
description: Notas de la versión de DaRT 8.0 SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824771"
---
# Notas de la versión de DaRT 8.0 SP1


**Para buscar estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 Service Pack 1 (SP1).

Estas notas de la versión contienen información necesaria para instalar correctamente los diagnósticos y el conjunto de herramientas de recuperación 8,0 SP1. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de DaRT, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Acerca de la documentación del producto


Para obtener información sobre la documentación de DaRT, consulte la [Página de inicio de DART](https://go.microsoft.com/fwlink/?LinkID=252096) en Microsoft TechNet.

## Problemas conocidos con DaRT 8,0 SP1


### Restaurar sistema falla al ejecutar locksmith o el editor del registro

Si ejecuta locksmith, el editor del registro y posiblemente otras herramientas, se produce un error en Restaurar sistema.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie Restaurar sistema.

### El examen de SFC no se ejecuta después de iniciar y cerrar locksmith o administración de equipos

Si inicia y cierra las locksmith o las herramientas de administración de equipos, el comprobador de archivos de sistema no podrá ejecutarse.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> El instalador de DaRT no falla cuando ADK no se ha instalado

Si instala DaRT 8,0 SP1 mediante la línea de comandos para ejecutar el MSI y no se ha instalado ADK, la instalación de DaRT debería fallar. En la actualidad, el instalador de DaRT 8,0 SP1 instala todos los componentes excepto la imagen de recuperación de DaRT.

**Solución alternativa:** Nada.

### Defender no se puede iniciar después de que locksmith, regedit, analizador de bloqueos y administración de equipos se hayan iniciado

Defender no se inicia si ya ha iniciado locksmith, regedit, Crash Analyzer y administración de equipos.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie defender.

### Defender puede ser lento para iniciarse

En ocasiones, defender tarda unos minutos en iniciarse. La barra de progreso indica el estado de carga actual.

**Solución alternativa:** Nada.

## Información de copyright de notas de versión


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft. El resto de marcas comerciales pertenecen a sus respectivos dueños.



## Temas relacionados


[Acerca de DaRT 8.0 SP1](about-dart-80-sp1.md)

 

 





