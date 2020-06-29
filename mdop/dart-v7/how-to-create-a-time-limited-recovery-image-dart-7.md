---
title: Cómo crear una imagen para recuperación de límite de tiempo
description: Cómo crear una imagen para recuperación de límite de tiempo
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812631"
---
# Cómo crear una imagen para recuperación de límite de tiempo


Puede crear una imagen de recuperación de DaRT que solo se puede usar durante un número determinado de días después de su generación. Para hacerlo, debe ejecutar el Asistente de **imagen de recuperación de DART** en un símbolo del sistema y especificar el número de días.

**Para crear una imagen de recuperación que tenga un límite de tiempo**

1.  Abra un símbolo del sistema con credenciales de administrador.

2.  Cambie el directorio a la ubicación del programa de ERDC.exe.

3.  Con la siguiente sintaxis, ejecute el **Asistente de imagen de recuperación de DART**. *NumberOfDays* es un entero positivo que representa el número de días que se puede usar la imagen de recuperación de DART.

    ``` syntax
    ERDC /e NumberOfDays
    ```

## Temas relacionados


[Creación de la imagen para recuperación de DaRT 7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





