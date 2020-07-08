---
title: Cómo configurar un usuario de dominio o un grupo
description: Cómo configurar un usuario de dominio o un grupo
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827200"
---
# Cómo configurar un usuario de dominio o un grupo


La configuración de implementación le permite controlar qué usuarios o grupos pueden acceder al área de trabajo de MED-V, así como el tiempo que se puede usar el área de trabajo de MED-V y si se puede usar sin conexión. También puede configurar reglas adicionales para controlar el acceso entre el área de trabajo de MED-V y el host.

Todos los permisos de área de trabajo de MED-V se configuran en el módulo **Directiva** , en la pestaña **implementación** .

Para permitir que los usuarios usen el área de trabajo de MED-V, primero debe agregar usuarios del dominio o grupos a permisos de área de trabajo de MED-V. Después, puede establecer permisos para cada usuario o grupo.

## Cómo agregar un usuario o grupo de dominio


**Para agregar un usuario o grupo de dominio**

1.  En la ventana **usuarios/grupos** , haga clic en **Agregar.**

2.  En el cuadro de diálogo **Escriba los nombres de usuario o grupo** , seleccione usuarios o grupos del dominio mediante una de las siguientes acciones:

    -   En el campo **Escriba los nombres de usuario o grupo** , escriba un usuario o grupo que exista en el dominio o como un grupo o usuario local en el equipo. A continuación, haga clic en **Comprobar nombres** para resolver el nombre completo.

    -   Haga clic en **Buscar** para abrir el cuadro de diálogo **Seleccionar usuarios o grupos** estándar. Después, seleccione usuarios o grupos del dominio.

3.  Haga clic en **Aceptar**.

    Se agregan los usuarios o grupos del dominio.

    **Nota**  
    Los usuarios de dominios de confianza deben agregarse de forma manual.



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## Cómo quitar un usuario o grupo de dominio


**Para quitar un usuario o grupo de dominio**

1.  En la ventana **usuarios/grupos** , seleccione un usuario o un grupo.

2.  Haga clic en **quitar**.

    Se elimina el usuario o el grupo.

## Cómo establecer permisos para un usuario o un grupo


**Para establecer permisos para un usuario o un grupo**

1.  Haga clic en el usuario o grupo para el que está configurando los permisos.

2.  Configure las propiedades del área de trabajo de MED-V tal como se describe en la tabla siguiente.

3.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades de implementación de área de trabajo**

Descripción *General* de la propiedad

Habilitar área de trabajo para &lt; usuario o grupo&gt;

Seleccione esta casilla para habilitar el área de trabajo de MED-V para este usuario o grupo.

El área de trabajo vence en esta fecha

Seleccione esta casilla para asignar una fecha de expiración para el conjunto de permisos para este usuario o grupo.

Cuando se selecciona, el cuadro de fecha está habilitado. Establezca la fecha y los permisos vencerán al final de la fecha especificada.

El trabajo sin conexión está restringido a

Seleccione esta casilla para asignar un período de tiempo en el que se debe actualizar la Directiva para este usuario o grupo. Cuando se selecciona, el cuadro período de tiempo está habilitado. Establezca el número de días u horas, y al final del período de tiempo especificado, el usuario o el grupo no se podrá conectar si la Directiva no se actualiza.

Opciones de eliminación de área de trabajo

Haga clic para establecer las opciones de eliminación del área de trabajo de MED-V. Para obtener más información, vea [Cómo configurar las opciones de eliminación del área de trabajo de MED-V](how-to-set-med-v-workspace-deletion-options.md).

*Transferencia de datos*

Compatibilidad del portapapeles entre el host y el área de trabajo

Active esta casilla para habilitar la copia y pegado entre el área de trabajo de host y MED-V.

Admitir la transferencia de archivos entre el host y el área de trabajo

Active esta casilla para habilitar la transferencia de archivos entre el host y el área de trabajo MED-V. Seleccione una de las siguientes opciones en el cuadro **transferencia de archivos** :

-   **Ambos**: permite transferir archivos entre el host y el área de trabajo de MED-V.

-   **Hospedar en el área de trabajo**: permite la transferencia de archivos desde el host al área de trabajo de MED-V.

-   **Área de trabajo para hospedar**: permite transferir archivos desde el área de trabajo de MED-V al host.

**Nota**  
Si un usuario sin permisos intenta transferir archivos, aparece una ventana que le pide que escriba las credenciales de un usuario con permisos para realizar la transferencia de archivos.



**Importante**  
Para admitir la transferencia de archivos en Windows XP SP3, debe deshabilitar la sincronización de archivos sin conexión modificando el registro de la siguiente manera:

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



Avanzado

Haga clic para establecer las opciones avanzadas de transferencia de archivos. Para obtener más información, consulte [cómo establecer opciones avanzadas de transferencia de archivos](how-to-set-advanced-file-transfer-options.md).

*Control de dispositivo*

Habilitar la impresión en impresoras conectadas al host

Active esta casilla para permitir que los usuarios impriman desde el área de trabajo de MED-V con la impresora de host.

**Nota**  
La impresión es realizada por las impresoras definidas en el host.



Habilitar el acceso a CD/DVD

Active esta casilla para permitir el acceso a una unidad de CD o DVD desde este área de trabajo de MED-V.



**Varias pertenencias**

1.  Si el usuario forma parte de un grupo y los permisos se aplican al usuario, así como al grupo del que forman parte, se aplicarán todos los permisos.

2.  Si el usuario es miembro de dos grupos diferentes, se aplican los permisos menos restrictivos.

## Temas relacionados


[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Cómo configurar las opciones de eliminación de área de trabajo de MED-V](how-to-set-med-v-workspace-deletion-options.md)

[Cómo configurar las opciones de transferencia de archivos avanzadas](how-to-set-advanced-file-transfer-options.md)









