---
title: Cómo actualizar un paquete
description: Cómo actualizar un paquete
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816501"
---
# Cómo actualizar un paquete


El proceso de actualización automática es el mismo que para agregar una versión de paquete en la consola de administración de Application Virtualization Server. Una actualización automática se realiza al reordenar la aplicación en un paquete existente. Después, puede Agregar esta nueva versión a los servidores para la transmisión.

Cuando actualiza un paquete con una nueva versión, puede dejar la versión existente en contexto o eliminarla y dejar solo la más reciente. Es posible que desee dejar la versión anterior vigente para la compatibilidad con documentos heredados o bien, puede probar la nueva versión antes de ponerla a disposición de todos los usuarios.

**Para actualizar un paquete automáticamente**

1.  Copie el nuevo archivo SFT a la carpeta de contenido del servidor de virtualización de aplicaciones.

    **Nota:**  Si la resecuenciación no agrega características que hayan cambiado los archivos descriptor de software abierto (OSD), icono (ICO) o proyecto SPRJ (SPRJ), no es necesario copiarlos. Puede incluir estos archivos si desea que todos estos archivos muestren la misma fecha.

     

2.  En el panel izquierdo de la consola de administración de Application Virtualization Server, expanda **Packages**.

3.  Haga clic con el botón derecho en el paquete que desea actualizar y seleccione **Agregar versión**.

4.  En el cuadro de diálogo **Agregar versión de paquete** , busque o escriba el nombre completo de la ruta de acceso para la nueva versión de la aplicación en la **ruta de acceso completa del campo de archivo** . Debe ser un archivo de SFT.

5.  Haz clic en **Siguiente**.

6.  El cuadro de diálogo **Resumen** muestra la ubicación del archivo y le pide que copie el archivo allí si aún no lo ha hecho. Haga clic en **Finalizar** una vez que haya verificado la información.

    La nueva versión ya está completa y lista para transmitirse.

## Temas relacionados


[Cómo administrar paquetes en la consola de administración de servidor](how-to-manage-packages-in-the-server-management-console.md)

 

 





