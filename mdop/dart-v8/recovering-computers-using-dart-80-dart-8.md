---
title: Equipos de recuperación que usan DaRT 8.0
description: Equipos de recuperación que usan DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824870"
---
# Equipos de recuperación que usan DaRT 8.0


Después de implementar la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, puede usar DaRT 8,0 para recuperar equipos. En la información de esta sección se describen las tareas de recuperación que puede realizar.

Puede elegir entre varios métodos diferentes para iniciar en DaRT, en función de cómo implemente la imagen de recuperación de DaRT.

-   Inserte un CD, DVD o una unidad flash USB de la imagen de recuperación de DaRT en el equipo problemático y utilícelo para arrancar en el equipo.

-   Inicie DaRT desde una partición de recuperación en el equipo con problemas.

-   Inicie en DaRT desde una partición remota en la red.

Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.

**Nota:**  La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.

 

## Recuperar un equipo local con la imagen de recuperación de DaRT


Para recuperar un equipo local con DaRT, debe estar físicamente presente en el equipo del usuario final que está experimentando problemas que requieren DaRT.

[Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## Recuperar un equipo remoto con la imagen de recuperación de DaRT


La característica de conexión remota de DaRT permite que un administrador de TI ejecute las herramientas de DaRT de manera remota en un equipo de usuario final. Una vez que el usuario final proporcione cierta información (o un profesional del Departamento de soporte técnico trabajando en el equipo del usuario final), el administrador de ti o el trabajador del Departamento de soporte puede tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.

**Importante**  Los dos equipos que establecen una conexión remota deben formar parte de la misma red.

 

La ventana del **conjunto de herramientas de diagnóstico y recuperación** incluye la opción de ejecutar DART en un equipo del usuario final de forma remota desde un equipo de administrador. El usuario final abre las herramientas de DaRT en el equipo problemático e inicia la sesión remota haciendo clic en **conexión remota**.

La característica de conexión remota en el equipo del usuario final crea la siguiente información de conexión: un número de vale, un puerto y una lista de todas las direcciones IP disponibles. El número y el puerto del vale se generan de forma aleatoria.

El administrador de ti o el trabajador del Departamento de soporte introduce esta información en el **visor de conexión remota de DART** para establecer la conexión de servicios de Terminal Server con el equipo del usuario final. La conexión de servicios de Terminal Server que se establece permite que un administrador de ti interactúe de forma remota con las herramientas de DaRT en el equipo del usuario final. Después, el equipo del usuario final procesa la información de conexión, comparte su pantalla y responde a las instrucciones del PC administrador de ti.

[Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## Otros recursos para recuperar equipos con DaRT 8,0


[Operaciones para DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





