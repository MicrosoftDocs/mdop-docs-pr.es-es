---
title: Creación de la imagen para recuperación de DaRT 7.0
description: Creación de la imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823281"
---
# Creación de la imagen para recuperación de DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 incluye el **Asistente de imagen de recuperación de DART** que se usa en Windows para crear una imagen de inicio de la organización internacional para la estandarización (ISO). Una imagen ISO es un archivo que representa el contenido sin formato de un CD.

## Usar el Asistente de recuperación de imágenes de DaRT para crear la imagen de recuperación


La ISO creada por el Asistente de imágenes de recuperación de DaRT contiene la imagen de recuperación de DaRT que le permite arrancar un equipo problemático, incluso si, de otro modo, no se inicia. Después de arrancar el equipo en DaRT, puede ejecutar las diferentes herramientas de DaRT para intentar diagnosticar y reparar el equipo.

Puede escribir la ISO en un CD o DVD grabable, guardarla en una unidad flash USB o guardarla en un formato que pueda usar para arrancar en DaRT desde una partición remota o desde una partición de recuperación. Para obtener más información, consulte [implementación de la imagen de recuperación de DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

**Nota:**  Si su equipo incluye una unidad de CD-RW, el asistente le permite grabar la imagen ISO en un CD o DVD en blanco. Si su equipo no incluye una unidad admitida por el asistente, puede grabarla en un CD o DVD usando la mayoría de los programas que pueden grabar un CD o DVD.

 

Para crear un CD o DVD de arranque a partir de la imagen ISO, debe tener:

-   Una unidad de CD-RW.

-   Un CD o DVD grabable (en un formato compatible con la unidad grabable).

-   Software que admite la unidad grabable y admite la grabación de una imagen ISO directamente en un CD o DVD.

    **Importante**  Pruebe el CD o DVD que cree en los distintos tipos de equipos que desea admitir porque algunos equipos no se pueden iniciar desde todos los tipos de medios grabables.

     

Para guardar la imagen ISO en una unidad flash USB (UFD), debe tener:

-   Una UFD con formato correcto.

-   Un programa que puede usar para montar la imagen ISO.

[Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## Crear una imagen de recuperación de tiempo limitado


Puede crear una imagen de recuperación de DaRT que solo se puede usar durante un número determinado de días después de su generación. Para hacerlo, debe ejecutar el Asistente de **imagen de recuperación de DART** en un símbolo del sistema y especificar el número de días.

[Cómo crear una imagen para recuperación de límite de tiempo](how-to-create-a-time-limited-recovery-image-dart-7.md)

## Otros recursos para crear la imagen de recuperación de DaRT7


-   [Implementación de DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





