---
title: Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V
description: Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825971"
---
# Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V


Cada área de trabajo de MED-V debe tener una imagen de Microsoft Virtual PC asociada con ella. La configuración de la máquina virtual le permite asignar una imagen de Virtual PC, así como establecer otras propiedades de máquina virtual.

La configuración de todas las máquinas virtuales se establece en el módulo de **directivas** , en la pestaña **configuración de máquina virtual** .

**Para aplicar la configuración de la máquina virtual a un área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V para configurar.

2.  Configure las propiedades de la máquina virtual como se describe en la tabla siguiente.

3.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades de la máquina virtual**

Descripción de la propiedad de *máquina virtual*

Imagen asignada

La imagen real de Microsoft Virtual PC asignada al área de trabajo de MED-V. El menú proporciona una lista de todas las imágenes de Virtual PC disponibles. Los siguientes tipos de imagen están en la lista de imágenes **activas** :

-   **Imágenes de prueba locales**: imágenes en el equipo local que aún no están empaquetadas. Estos nombres de imagen van seguidos de la palabra "prueba" entre paréntesis (prueba) y son solo con fines de prueba.

-   **Imágenes empaquetadas locales**: imágenes empaquetadas en el equipo local. Estas imágenes van seguidas de la palabra "local" entre paréntesis (locales) y los clientes no pueden descargarlas hasta que el administrador las cargue en el servidor.

    Se puede seleccionar una imagen local si está creando un paquete que se distribuirá al cliente a través de medios extraíbles (como USB o DVD).

-   **Imágenes empaquetadas en el servidor**: imágenes que están en el servidor y que los clientes pueden descargar. Haga clic en actualizar para actualizar la lista de imágenes.

    **Nota:**  Cada imagen del área de trabajo de MED-V solo la puede usar un usuario de Windows.

     

El área de trabajo es persistente

Active esta casilla para configurar el área de trabajo de MED-V como persistente. En un área de trabajo de MED-V persistente, cuando se detiene el área de trabajo de MED-V, los cambios y las adiciones en el área de trabajo de Med-v se guardan en el área de trabajo de MED-V.

Para un área de trabajo de dominio MED-V, esta opción debe estar seleccionada.

**Nota:**  Esta configuración no se debe cambiar después de implementar un área de trabajo de MED-V para los usuarios.

 

Cerrar la VM al detener el área de trabajo

Seleccione esta casilla para apagar la máquina virtual al detener el área de trabajo de MED-V. Si esta casilla está desactivada, al finalizar cada sesión, la máquina virtual no se apaga, sino que toma una instantánea de la máquina virtual. Una vez iniciada una nueva sesión, Windows se inicia desde la instantánea (es decir, Windows no se reinicia y no se necesita inicio de sesión).

**Nota:**  Esta propiedad solo está habilitada si está seleccionado el **área de trabajo persistente** .

 

Iniciar sesión en Windows en VM con credenciales MED-V (SSO)

Seleccione esta casilla para iniciar sesión en Windows en la máquina virtual con las credenciales de MED-V especificadas al iniciar sesión en el cliente de MED-V.

**Nota:**  Esta propiedad solo se habilita cuando está seleccionado el **área de trabajo persistente** .

 

El área de trabajo es revertida

Active esta casilla para configurar el área de trabajo de MED-V como revertida. En un área de trabajo revertida de MED-V, al finalizar cada sesión (es decir, cuando el usuario detiene el área de trabajo de MED-V), el área de trabajo de MED-V vuelve al estado original en el que se encontraba durante la implementación. Los cambios o adiciones que el usuario ha realizado se guardan en el área de trabajo de MED-V entre sesiones.

**Nota:**  Esta configuración no se debe cambiar después de implementar un área de trabajo de MED-V para los usuarios.

 

Sincronizar la zona horaria del área de trabajo con el host

Seleccione esta casilla para sincronizar la zona horaria en el área de trabajo de MED-V con el host.

La sincronización funciona de forma diferente en función de si el área de trabajo de MED-V es persistente o revertida, de la siguiente manera:

-   En un área de trabajo de MED-V persistente, la zona horaria intenta sincronizar primero con el servidor. Si se produce un error, se sincroniza con el host.

-   En un área de trabajo revertida de MED-V, la zona horaria se sincroniza con el host.

*Bloquear configuración*

Bloquear el área de trabajo en el evento de suspensión e hibernación del host

Seleccione esta casilla para bloquear automáticamente el área de trabajo de MED-V cuando el equipo host entra en modo de espera o de hibernación.

Bloquear el área de trabajo después de

Seleccione esta casilla para bloquear el área de trabajo de MED-V cuando el área de trabajo de MED-V está inactiva durante un período de tiempo específico. Cuando se selecciona, el cuadro número está habilitado. Escriba el número de minutos de inactividad antes de bloquear el área de trabajo de MED-V.

**Nota:**  El tiempo de inactividad se refiere a las aplicaciones de áreas de trabajo de MED-V (no las aplicaciones host).

 

*Configuración de actualización de imagen*

Mantener solo

Seleccione esta casilla para limitar el número de versiones antiguas de la imagen que desea conservar.

Cuando se selecciona, el cuadro número está habilitado. Escriba el número de versiones anteriores que desea conservar.

Sugerir una actualización cuando hay una nueva versión disponible

Seleccione esta casilla para sugerir (pero no exigir) una actualización cuando esté disponible una nueva versión de la imagen.

Los clientes deben usar la transferencia de recorte al descargar imágenes para esta área de trabajo

Seleccione esta casilla para habilitar la transferencia de recorte (para obtener más información, consulte [tecnología de transferencia de recorte de Med-v](med-v-trim-transfer-technology-medvv2.md)) al descargar imágenes asociadas con este área de trabajo de Med-v. Si esta casilla está desactivada, la imagen completa se descargará.

**Nota:**  Recortar transferencia requiere indizar el disco duro, lo cual puede demorar una cantidad considerable de tiempo. Se recomienda usar recortar transferencia al indizar el disco duro es más eficaz que descargar la nueva versión de la imagen, por ejemplo, cuando se descarga una versión de imagen similar a la de la versión existente.

 

 

## Temas relacionados


[Creación de una imagen de MED-V](creating-a-med-v-image.md)

[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





