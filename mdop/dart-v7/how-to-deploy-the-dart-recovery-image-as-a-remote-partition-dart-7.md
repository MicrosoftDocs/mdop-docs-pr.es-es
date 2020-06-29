---
title: Cómo implementar la imagen para recuperación de DaRT como una partición remota
description: Cómo implementar la imagen para recuperación de DaRT como una partición remota
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823570"
---
# Cómo implementar la imagen para recuperación de DaRT como una partición remota


Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y haya creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición remota en la red.

**Para implementar DaRT como una partición remota**

1.  Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.

    1.  Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** con el método preferido de su empresa para montar una imagen.

    2.  Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.

        **Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el archivo boot. Wim desde la carpeta \\sources. Esto le permite omitir la necesidad de montar la imagen.

         

2.  Implemente el archivo boot. Wim en un servidor WDS al que se puede obtener acceso desde los equipos de los usuarios finales de su empresa.

3.  Configure el servidor WDS para usar el archivo boot. Wim para DaRT siguiendo los procedimientos de implementación de WDS estándar.

Para obtener más información sobre cómo implementar DaRT como una partición remota, consulte lo siguiente:

-   [Tutorial: implementar una imagen mediante PXE](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [Guía de introducción a servicios de implementación de Windows](https://go.microsoft.com/fwlink/?LinkId=212106)

## Temas relacionados


[Implementación de la imagen para recuperación de DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





