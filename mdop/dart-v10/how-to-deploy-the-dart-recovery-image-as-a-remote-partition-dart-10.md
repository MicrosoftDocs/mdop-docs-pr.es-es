---
title: Cómo implementar la imagen para recuperación de DaRT como una partición remota
description: Cómo implementar la imagen para recuperación de DaRT como una partición remota
author: dansimp
ms.assetid: 06a5e250-b992-4f6a-ad74-e7715f9e96e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3cdb1313a64bacd652a5253c09f36fa792d0fa3c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813063"
---
# Cómo implementar la imagen para recuperación de DaRT como una partición remota


Una vez que haya terminado de ejecutar el Asistente para imágenes de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 10 y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de imagen ISO e implementarlo como una partición remota en la red.

**Para implementar DaRT 10 como una partición remota**

1.  Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.

    1.  Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** con el método preferido de su empresa para montar una imagen.

    2.  Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.

        **Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el archivo boot. Wim desde la carpeta \\sources. Esto le permite omitir la necesidad de montar la imagen.

         

2.  Implemente el archivo boot. Wim en un servidor WDS al que se puede obtener acceso desde los equipos de los usuarios finales de su empresa.

3.  Configure el servidor WDS para usar el archivo boot. Wim para DaRT siguiendo los procedimientos de implementación de WDS estándar.

Para obtener más información sobre cómo implementar DaRT como una partición remota, consulte [Tutorial: implementar una imagen mediante PXE](https://go.microsoft.com/fwlink/?LinkId=212108) y la [Guía](https://go.microsoft.com/fwlink/?LinkId=212106)de introducción a los servicios de implementación de Windows.

## Temas relacionados


[Creación de la imagen para recuperación de DaRT 10](creating-the-dart-10-recovery-image.md)

[Implementación de la imagen para recuperación de DaRT](deploying-the-dart-recovery-image-dart-10.md)

[Planificación para DaRT 10](planning-for-dart-10.md)

 

 





