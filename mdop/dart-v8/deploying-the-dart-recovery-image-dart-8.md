---
title: Implementación de la imagen para recuperación de DaRT
description: Implementación de la imagen para recuperación de DaRT
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824111"
---
# Implementación de la imagen para recuperación de DaRT


Una vez que haya creado el archivo de la organización internacional de normalización (ISO) que contiene la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT 8,0), puede implementar la imagen de recuperación de DaRT 8,0 en toda la empresa para que esté disponible para los usuarios finales y los trabajadores del Departamento de soporte técnico. Existen cuatro métodos admitidos que puede usar para implementar la imagen de recuperación de DaRT. Para revisar las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Grabe el archivo de imagen ISO en un CD o DVD usando el Asistente de imagen de recuperación de DaRT.

Guardar el contenido del archivo de imagen ISO en una unidad flash USB (UFD) mediante el Asistente para imágenes de recuperación DaRT

Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo como una partición remota que esté disponible para los equipos de los usuarios finales.

Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo en la partición de recuperación de una nueva instalación de Windows 8.

**Importante**  El **Asistente de imágenes de recuperación DART** ofrece la opción de grabar la imagen en un CD, DVD o UFD, pero los otros métodos para guardar e implementar la imagen de recuperación requieren pasos adicionales que incluyen herramientas que no se incluyen en DART. En esta sección se proporcionan instrucciones y vínculos para estos otros métodos.

 

## Implementar la imagen de recuperación de DaRT como parte de una partición de recuperación


Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 8.

[Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## Implementar la imagen de recuperación de DaRT como una partición remota


Puede hospedar la imagen de recuperación en un servidor central de arranque de red, como servicios de implementación de Windows, y permitir que los usuarios o el personal de soporte técnico transmita la imagen a equipos a petición.

[Cómo implementar la imagen para recuperación de DaRT como una partición remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## Otros recursos para implementar la imagen de recuperación de DaRT


[Implementación de DaRT 8.0](deploying-dart-80-dart-8.md)

 

 





