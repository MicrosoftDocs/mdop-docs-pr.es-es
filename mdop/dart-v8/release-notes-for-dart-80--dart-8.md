---
title: Notas de la versión de DaRT 8.0
description: Notas de la versión de DaRT 8.0
author: dansimp
ms.assetid: e8b373c8-7aa5-4930-a8f9-743d26145dad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 894708585ff4006c37085e71f365690b8424d43e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824790"
---
# Notas de la versión de DaRT 8.0


**Para buscar estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

Estas notas de la versión contienen la información necesaria para instalar correctamente DaRT 8,0. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de DaRT, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

Para obtener el software de DaRT, consulte [Cómo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).

## Acerca de la documentación del producto


Para obtener información sobre la documentación de DaRT, consulte la [Página de inicio de DART](https://go.microsoft.com/fwlink/?LinkID=252096) en Microsoft TechNet.

Para obtener una copia descargable de la documentación de DaRT, consulte <https://go.microsoft.com/fwlink/?LinkID=267420> en el centro de descarga de Microsoft.

## Comentarios


Nos interesan tus comentarios sobre DaRT 8,0. Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .

**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios para la documentación y las versiones de producto.

 

Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conocidos con DaRT 8,0


### Restaurar sistema falla al ejecutar locksmith o el editor del registro

Si ejecuta locksmith, el editor del registro y posiblemente otras herramientas, se produce un error en Restaurar sistema.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie Restaurar sistema.

### El examen de SFC no se ejecuta después de iniciar y cerrar locksmith o administración de equipos

Si inicia y cierra las locksmith o las herramientas de administración de equipos, el comprobador de archivos de sistema no podrá ejecutarse.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> El instalador de DaRT no falla cuando ADK no se ha instalado

Si instala DaRT 8,0 mediante la línea de comandos para ejecutar el MSI y no se ha instalado ADK, la instalación de DaRT debería fallar. En la actualidad, el instalador de DaRT 8,0 instala todos los componentes excepto la imagen de recuperación de DaRT 8,0.

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


[Acerca de DaRT 8.0](about-dart-80-dart-8.md)

 

 





