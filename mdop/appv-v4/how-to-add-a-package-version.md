---
title: Cómo agregar una versión de paquete
description: Cómo agregar una versión de paquete
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821401"
---
# Cómo agregar una versión de paquete


En la consola de administración de Application Virtualization Server, cuando reordene un paquete, puede usar el siguiente procedimiento para agregar la nueva versión a los servidores para la transmisión.

**Nota:**  Cuando actualiza un paquete con una nueva versión, puede dejar la versión existente en contexto o eliminarla y dejar solo la más reciente. Es posible que desee dejar la versión anterior vigente para la compatibilidad con documentos heredados o bien, puede probar la nueva versión antes de ponerla a disposición de todos los usuarios.

 

**Para agregar una versión de paquete**

1.  Copie el nuevo archivo SFT a la carpeta de contenido del servidor de aplicaciones. Si la resecuenciación no ha agregado los cambios en los archivos del descriptor de software abierto (OSD), de icono (ICO) o del SPRJ (SPRJ), no es necesario que los copie. Puede incluir esos archivos si quiere que todos los archivos muestren la misma fecha.

2.  En el panel izquierdo de la consola de administración de Application Virtualization Server, expanda el nodo **paquetes** .

3.  Haga clic con el botón derecho en el paquete que quiera actualizar y elija **Agregar versión**.

4.  En el cuadro de diálogo **Agregar versión del paquete** , busque o escriba el nombre de la ruta de acceso del nuevo archivo de aplicación en el campo **ruta de acceso completa del archivo de paquete** . Debe ser un archivo de SFT.

5.  Haz clic en **Siguiente**.

6.  El cuadro de diálogo **Resumen** muestra la ubicación del archivo y le pide que copie el archivo allí si aún no lo ha hecho. Haga clic en **Finalizar** una vez que haya verificado la información.

    La nueva versión ya está completa y lista para transmitirse.

## Temas relacionados


[Cómo eliminar un paquete](how-to-delete-a-packageserver.md)

[Cómo administrar paquetes en la consola de administración de servidor](how-to-manage-packages-in-the-server-management-console.md)

 

 





