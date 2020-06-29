---
title: Cómo actualizar una imagen de MED-V
description: Cómo actualizar una imagen de MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812495"
---
# Cómo actualizar una imagen de MED-V


## Cómo actualizar una imagen de MED-V


Una imagen de MED-V existente se puede actualizar, lo que crea una nueva versión de la imagen. La nueva versión se puede implementar en los equipos cliente, reemplazando la imagen existente.

**Nota:**  Cuando se implementa una nueva versión en el cliente, se sobrescribe la imagen existente. Al actualizar una imagen, asegúrese de que no se debe guardar ningún dato en el cliente.

 

**Para actualizar una imagen de MED-V**

1.  Abra la imagen existente en virtual PC2007.

2.  Realice los cambios necesarios en la imagen, actualizando la imagen (por ejemplo, instalando nuevo software).

3.  Cierre PC2007 virtual.

4.  Pruebe la imagen.

5.  Después de probar la imagen, empaquela en el repositorio local con el mismo nombre que la imagen existente.

    **Nota:**  Si asigna a la imagen un nombre diferente al de la versión existente, se creará una nueva imagen en lugar de una nueva versión de la imagen existente.

     

6.  Cargue la nueva versión en el servidor o distribúyala a través de un paquete de implementación.

## Temas relacionados


[Creación de una imagen de Virtual PC para MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Cómo crear y probar una imagen de MED-V](how-to-create-and-test-a-med-v-image.md)

[Cómo empaquetar una imagen de MED-V](how-to-pack-a-med-v-image.md)

[Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md)

[Actualización de una imagen de área de trabajo de MED-V](updating-a-med-v-workspace-image.md)

 

 





