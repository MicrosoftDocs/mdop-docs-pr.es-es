---
title: Cómo derivar un paquete
description: Cómo derivar un paquete
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818130"
---
# Cómo derivar un paquete


Use este procedimiento para modificar un paquete de aplicación de secuencia existente para que pueda ejecutarlo en paralelo con el paquete de aplicación secuencial original. Este proceso se denomina bifurcación. Al bifurcar un paquete de aplicación virtual, puede ejecutar dos versiones del mismo paquete. Por ejemplo, puede aplicar un Service Pack a un paquete existente y ejecutarlo en paralelo con el paquete de aplicación virtual secuencial original.

Use el siguiente procedimiento para bifurcar un paquete de aplicación virtual de secuencia.

**Para bifurcar un paquete de aplicación virtual de secuencia**

1.  Abra el secuenciador de Microsoft Application Virtualization (App-V). Para especificar el directorio de destino que contiene el paquete (. SPRJ) que desea bifurcar, seleccione **archivo**, **abrir**.

2.  Vaya al directorio que contiene la aplicación de secuencia que planea bifurcar y haga clic en **abrir**.

3.  Para guardar una copia del paquete, en el secuenciador de App-V, seleccione **archivo**, **Guardar como**. Especifique un nuevo nombre único y especifique un nuevo directorio raíz de paquete único para la copia del paquete. Haga clic en **Guardar**.

    **Importante**  
    Debe especificar un nuevo nombre de paquete o sobrescribir la versión existente del paquete.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. Después de guardar la nueva versión, puede aplicar los cambios de configuración requeridos y guardar los archivos ICO, OSD, SFT y SPRJ asociados en la ubicación correcta en el servidor de Application Virtualization (App-V).

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones](tasks-for-the-application-virtualization-sequencer.md)









