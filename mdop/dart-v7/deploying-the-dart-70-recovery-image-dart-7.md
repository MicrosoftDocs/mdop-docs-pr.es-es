---
title: Implementación de la imagen para recuperación de DaRT 7.0
description: Implementación de la imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812655"
---
# Implementación de la imagen para recuperación de DaRT 7.0


Una vez que haya creado el archivo de la organización internacional de normalización (ISO) que contiene la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7, puede implementar la imagen de recuperación de DaRT en toda su empresa para que esté disponible para los usuarios finales y los agentes del Departamento de soporte técnico. Existen cuatro métodos admitidos que puede usar para implementar la imagen de recuperación de DaRT.

-   Grabar el archivo de imagen ISO en un CD o DVD

-   Guardar el contenido del archivo de imagen ISO en una unidad flash USB (UFD)

-   Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo como una partición remota que esté disponible para los equipos de los usuarios finales.

-   Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo en la partición de recuperación de una nueva instalación de Windows 7.

**Importante**  El **Asistente de imagen de recuperación de DART** solo proporciona la opción de grabar un CD o DVD. Todos los demás métodos de guardado e implementación de la imagen de recuperación requieren pasos adicionales que incluyen herramientas que no se incluyen en DaRT. En esta sección se proporcionan instrucciones y vínculos para estos otros métodos.

 

## Implementar la imagen de recuperación de DaRT con una unidad flash USB


Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT, puede usar la herramienta en <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar el archivo de imagen ISO en una unidad flash USB (UFD).

[Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## Implementar la imagen de recuperación de DaRT como parte de una partición de recuperación


Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 7.

[Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## Implementar la imagen de recuperación de DaRT como una partición remota


Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y haya creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición remota en la red.

[Cómo implementar la imagen para recuperación de DaRT como una partición remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## Otros recursos para el mantenimiento de la implementación de la imagen de recuperación de DaRT


-   [Implementación de DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





