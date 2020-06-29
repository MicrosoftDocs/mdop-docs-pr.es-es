---
title: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
description: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824381"
---
# Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación


Una vez que haya terminado de ejecutar el Asistente de recuperación de imágenes 8,0 de Microsoft Diagnostics y de recuperación (DaRT) y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 8. Se recomienda usar una partición porque cualquier problema de daños que impida el inicio del sistema operativo Windows también evitará que la imagen de recuperación se inicie. Una partición independiente también elimina la necesidad de proporcionar la clave de recuperación de BitLocker dos veces. Considere la posibilidad de ocultar la partición para impedir que los usuarios almacenen archivos en ella.

**Para implementar DaRT en la partición de recuperación de una imagen de Windows 8**

1.  Cree una partición de destino en la imagen de Windows 8 que sea igual o mayor que el tamaño del archivo de imagen ISO que creó mediante el **Asistente para imágenes de recuperación de DaRT 8,0**.

    El tamaño mínimo requerido para una partición de DaRT es de 500 MB para dar cabida a la funcionalidad de conexión remota en DaRT.

2.  Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.

    1.  Con el método preferido de su empresa, Monte el archivo de imagen ISO que creó en la página **crear imagen de inicio** .

    2.  Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.

        **Nota:**  Si grabó un CD, DVD o USB de la imagen de recuperación, puede abrir los archivos en los medios extraíbles y copiar el archivo boot. Wim de la carpeta \\sources. Si copia el archivo boot. Wim, no necesita montar la imagen.

         

3.  Use el archivo boot. Wim para crear una partición de recuperación de arranque con el método estándar de su compañía para crear una imagen de Windows RE personalizada.

    Para obtener más información sobre cómo crear o personalizar una partición de recuperación, consulte [Personalización de la experiencia de Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Reemplace la partición de destino de la imagen de Windows 8 con la partición de recuperación.

    Para obtener más información sobre cómo implementar una solución de recuperación para reinstalar la imagen de fábrica en el caso de que se produzca un error del sistema, consulte [implementar una imagen de recuperación del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).

## Temas relacionados


[Creación de la imagen para recuperación de DaRT 8.0](creating-the-dart-80-recovery-image-dart-8.md)

[Implementación de la imagen para recuperación de DaRT](deploying-the-dart-recovery-image-dart-8.md)

[Planificación para DaRT 8.0](planning-for-dart-80-dart-8.md)

 

 





