---
title: Equipos de recuperación que usan DaRT 7.0
description: Equipos de recuperación que usan DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822770"
---
# Equipos de recuperación que usan DaRT 7.0


Hay dos métodos disponibles para recuperar equipos con Microsoft Diagnostics and Recovery Toolset (DaRT) 7. Puede ejecutar la imagen de recuperación de DaRT7 localmente o usar la característica de conexión remota disponible en DaRT7 para recuperar un equipo remoto. Ambos métodos se describen más detalladamente en esta sección.

## Recuperar equipos locales con la imagen de recuperación de DaRT


Para recuperar un equipo local mediante DaRT7, debe estar presente físicamente en el equipo del usuario final que está experimentando problemas que requieren DaRT.

Puede elegir entre varios métodos diferentes para iniciar en DaRT, en función de cómo implemente la imagen de recuperación de DaRT.

-   Inserte un CD, DVD o una unidad flash USB de la imagen de recuperación de DaRT en el equipo problemático y utilícelo para arrancar en el equipo.

-   Inicie DaRT desde una partición de recuperación en el equipo con problemas.

-   Inicie en DaRT desde una partición remota en la red.

Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.

**Nota:**  La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.

 

[Cómo recuperar los equipos locales con la imagen para recuperación de DaRT](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## Recuperar equipos remotos con la imagen de recuperación de DaRT


La característica de conexión remota de DaRT permite que un administrador de TI ejecute las herramientas de DaRT de manera remota en un equipo de usuario final. Después de que el usuario final proporcione determinada información (o de un profesional del Departamento de soporte técnico que trabaje en el equipo del usuario final), el administrador de ti o el agente de asistencia pueden tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.

**Importante**  Los dos equipos que establecen una conexión remota deben formar parte de la misma red.

 

La ventana del **conjunto de herramientas de diagnóstico y recuperación** incluye la opción de ejecutar DART en un equipo del usuario final de forma remota desde un equipo de administrador. El usuario final abre las herramientas de DaRT en el equipo problemático e inicia la sesión remota haciendo clic en **conexión remota**.

La característica de conexión remota en el equipo del usuario final crea la siguiente información de conexión: un número de vale, un puerto y una lista de todas las direcciones IP disponibles. El número y el puerto del vale se generan de forma aleatoria.

El administrador de ti o el agente de asistencia escribe esta información en el **visor de conexión remota de DART** para establecer la conexión de servicios de Terminal Server con el equipo del usuario final. La conexión de servicios de Terminal Server que se establece permite que un administrador de ti interactúe de forma remota con las herramientas de DaRT en el equipo del usuario final. Después, el equipo del usuario final procesa la información de conexión, comparte su pantalla y responde a las instrucciones del PC administrador de ti.

[Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## Otros recursos para recuperar equipos mediante DaRT7


[Operaciones para DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





