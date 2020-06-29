---
title: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
description: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823560"
---
# Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación


Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 7.

**Para implementar DaRT en la partición de recuperación de una imagen de Windows 7**

1.  Cree una partición de destino en la imagen de Windows 7 que sea igual o mayor que el tamaño del archivo de imagen ISO que creó mediante el **Asistente para imágenes de recuperación de DART**.

    El tamaño mínimo requerido para una partición de DaRT es de aproximadamente 300 MB. Sin embargo, recomendamos que 450MB se adapte a la funcionalidad de la conexión remota en DaRT.

2.  Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.

    1.  Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** con el método preferido de su empresa para montar una imagen.

    2.  Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.

        **Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el archivo boot. Wim desde la carpeta \\sources. Esto le permite omitir la necesidad de montar la imagen.

         

3.  Use el archivo boot. Wim para crear una partición de recuperación de arranque con el método estándar de su compañía para crear una imagen de Windows RE personalizada.

    Para obtener más información sobre cómo crear o personalizar una partición de recuperación, consulte [Personalización de la experiencia de Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Reemplace la partición de destino de su imagen de Windows 7 con la partición de recuperación.

Una vez que la imagen de Windows 7 esté lista, distribuya la imagen a los equipos de su empresa con el proceso de implementación de imágenes estándar de su empresa. Para obtener más información sobre cómo crear una imagen de Windows 7, consulte [creación de una imagen estándar de Windows 7: guía paso a paso](https://go.microsoft.com/fwlink/?LinkId=212103).

Para obtener más información sobre cómo implementar una solución de recuperación para reinstalar la imagen de fábrica en el caso de que se produzca un error del sistema, consulte [implementar una imagen de recuperación del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).

## Temas relacionados


[Implementación de la imagen para recuperación de DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





