---
title: Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB
description: Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823670"
---
# Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB


Una vez que haya terminado de ejecutar el **Asistente de imagen de recuperación de DART**, puede usar la herramienta en <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar el archivo de imagen ISO en una unidad flash USB (UFD).

También puede copiar manualmente el archivo de imagen ISO en una UFD siguiendo los pasos provistos en esta sección.

**Para guardar la imagen de recuperación de DaRT en una unidad flash USB**

1.  Formatear la unidad flash USB.

    1.  Desde un sistema operativo válido o una sesión WindowsPE en ejecución, inserte la UFD.

    2.  En el símbolo del sistema con permisos de administrador, escriba **DiskPart** y, a continuación, escriba **List Disk**.

        La ventana del símbolo del sistema muestra el número de disco de la UFD, por ejemplo, **disco 1**.

    3.  Escriba los siguientes comandos de uno en uno en el símbolo del sistema.

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        **Nota:**  En el ejemplo de código anterior se supone que Disk1 es la UFD. Si es necesario, cambie el disco 1 por el número de disco.

         

2.  Con el método preferido de su empresa para montar una imagen, Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** del **Asistente de imagen de recuperación de DART**. Para ello, es necesario disponer de un método disponible para montar un archivo de imagen.

3.  Abra el archivo de imagen ISO montado y copie todo su contenido en la unidad flash USB con formato.

    **Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el contenido en la UFD. Esto le permite omitir la necesidad de montar la imagen.

     

## Temas relacionados


[Implementación de la imagen para recuperación de DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





