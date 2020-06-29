---
title: Acerca de DaRT 7.0
description: Acerca de DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823271"
---
# Acerca de DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 le ayuda a solucionar problemas y reparar equipos de escritorio basados en Windows. Esto incluye los escritorios que no se pueden iniciar. DaRT es un conjunto de herramientas eficaz que amplía el entorno de recuperación de Windows (WinRE). Al usar DaRT, puede analizar un problema para determinar su causa, por ejemplo, inspeccionando el registro de eventos del equipo o el registro del sistema.

DaRT también proporciona herramientas para ayudarle a corregir un problema tan pronto como determine la causa. Por ejemplo, puede usar las herramientas de DaRT para deshabilitar un controlador de dispositivo defectuoso, quitar revisiones, restaurar archivos eliminados y buscar malware en el equipo incluso cuando no puede o no debe iniciar el sistema operativo Windows instalado.

DaRT puede ayudarle a recuperar rápidamente los equipos que ejecutan versiones de 32 o 64 bits de Windows 7, generalmente en menos tiempo de los que llevaría para volver a crear una imagen del equipo.

## Acerca de la imagen de recuperación de DaRT 7


La funcionalidad de DaRT le permite crear una imagen de recuperación basada en WinRE combinada con un conjunto de herramientas que DaRT ofrece. La imagen de recuperación de DaRT aprovecha WinRE, desde la que puede acceder a la ventana **conjunto de herramientas de diagnóstico y recuperación** .

Use el **Asistente de recuperación de imágenes de DART** para crear la imagen de recuperación de DART. De forma predeterminada, el asistente crea un archivo de imagen de la organización internacional de normalización (ISO) en el escritorio denominado DaRT70. ISO, aunque puede especificar una ubicación y un nombre de archivo diferentes. El Asistente también le permite grabar la imagen en un CD o DVD. Una vez que haya finalizado el asistente, puede guardar la imagen de recuperación en una unidad flash USB o guardarla en un formato que puede usar para crear una partición remota o una partición de recuperación.

Cuando tenga que usar DaRT para iniciar un equipo de usuario final que no se inicia, puede seguir las instrucciones de recuperación de [equipos locales mediante la imagen de recuperación de DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).

Para obtener información detallada sobre las herramientas de DaRT, vea información [General sobre las herramientas de dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

## <a href="" id="what-s-new-in-dart-7"></a>Novedades de DaRT 7


DaRT7 continúa admitiendo todos los escenarios incluidos en versiones anteriores y agrega una nueva característica de conexión remota además de tres nuevas opciones de implementación.

### Creación de imágenes de DaRT 7

El asistente que usa para crear imágenes de la ISO de DaRT ahora se denomina **imagen de recuperación de DART** y ahora es compatible con una opción para habilitar o deshabilitar la nueva característica de conexión remota. La conexión remota permite a un agente del Departamento de soporte técnico ejecutar las herramientas de DaRT desde una ubicación remota. En versiones anteriores, el agente del Departamento de soporte técnico tenía que estar físicamente presente en el equipo del usuario final para ejecutar las herramientas de DaRT.

El Asistente también le permite personalizar el mensaje de bienvenida de la característica de conexión remota (el mensaje se muestra cuando los usuarios finales ejecutan la herramienta de conexión remota). Los administradores de ti también pueden configurar el número de puerto que debe usar conexión remota.

Para obtener más información sobre el **Asistente de imágenes de recuperación de DART** o una conexión remota, consulte [creación de la imagen de recuperación de DART 7,0](creating-the-dart-70-recovery-image-dart-7.md).

### Implementación de DaRT 7 ISO

Además de grabar en un CD o DVD, DaRT7 agrega tres nuevas opciones al implementar el ISO que contiene la imagen de recuperación de DaRT:

-   Implementación de unidad flash USB

-   Implementación de particiones remotas

-   Implementación de la partición de recuperación

La opción de implementación de unidad flash USB permite que una empresa use DaRT en equipos que no tienen unidades de CD o DVD disponibles. Las opciones de recuperación y de partición remota permiten a los usuarios finales acceder fácilmente a la imagen de DaRT y habilitar la funcionalidad de conexión remota.

Para obtener más información sobre cómo implementar imágenes de recuperación de DaRT, consulte [implementación de la imagen de recuperación de dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

## Temas relacionados


[Tareas iniciales con DaRT 7.0](getting-started-with-dart-70-new-ia.md)

[Notas de la versión de DaRT 7.0](release-notes-for-dart-70-new-ia.md)

 

 





