---
title: Planificación de la implementación de DaRT 7.0
description: Planificación de la implementación de DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821320"
---
# Planificación de la implementación de DaRT 7.0


Hay varias configuraciones de implementación y requisitos previos diferentes que debe tener en cuenta antes de crear el plan de implementación. Esta sección incluye información que puede ayudarle a recopilar la información que necesita para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.

Tenga en cuenta lo siguiente cuando planee su instalación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7:

-   Al instalar DaRT, puede instalar toda la funcionalidad en un equipo de administrador de ti donde realizará todas las tareas asociadas con la ejecución de DaRT. También puede instalar la funcionalidad de DaRT que crea la imagen de recuperación en el PC administrador de ti. Después, instale la funcionalidad que se usa para ejecutar DaRT, como el **visor de conexión remota DART** y **Crash Analyzer**, en un equipo agente de asistencia.

-   Para poder ejecutar DaRT de forma remota, asegúrese de que el equipo del agente de asistencia y todos los equipos de los que pueda estar solucionando problemas estén en la misma red.

-   Antes de implementar DaRT en producción, puede crear primero un entorno de laboratorio para pruebas. Un laboratorio de pruebas debe incluir un mínimo de dos equipos, uno para actuar como el equipo del agente de soporte técnico y administrador de ti y otro para actuar como un equipo de usuario final. O bien, puede usar tres equipos en el laboratorio si desea separar las responsabilidades de administrador de TI de las del agente de asistencia al usuario.

## Revisar las configuraciones compatibles


Debe revisar la información de configuración admitida de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 para confirmar que los equipos que ha seleccionado para la instalación de cliente o de características cumplen con los requisitos mínimos de hardware y sistema operativo.

[Configuraciones admitidas de DaRT 7.0](dart-70-supported-configurations-dart-7.md)

## Plan para crear la imagen de recuperación de DaRT


Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen. Cuando tome esta decisión, recuerde que es posible que los usuarios finales tengan acceso ocasionalmente a las diversas herramientas de DaRT. Cuando cree la imagen de recuperación, también deberá especificar si desea incluir controladores o archivos adicionales. Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.

Debe tener en cuenta los requisitos previos y otras recomendaciones de planificación adicionales para crear la imagen de recuperación de DaRT.

[Planificación de creación de imagen para recuperación de DaRT 7.0](planning-to-create-the-dart-70-recovery-image.md)

## Plan para guardar e implementar la imagen de recuperación de DaRT


Se pueden usar varios métodos para guardar e implementar la imagen de recuperación de DaRT. Cuando determine el método que va a usar, tenga en cuenta las ventajas y desventajas de cada uno. Además, tenga en cuenta cómo desea usar DaRT en su empresa.

**Nota:**  Es posible que desee usar más de un método de su organización. Por ejemplo, puede arrancar en DaRT desde una partición remota para la mayoría de las situaciones y tener una unidad flash USB disponible en caso de que el equipo del usuario final no pueda conectarse a la red.

 

[Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## Otros recursos para planificar la implementación de DaRT


[Planificación para DaRT 7.0](planning-for-dart-70-new-ia.md)

 

 





