---
title: Uso del PIN o contraseña
description: Uso del PIN o contraseña
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823791"
---
# Uso del PIN o contraseña


BitLocker ayuda a proteger el equipo al requerir un número de identificación personal (PIN) o una contraseña para desbloquear la información almacenada en el equipo. Los requisitos de PIN o contraseña están establecidos por la organización y dependen del tipo de unidad que se va a cifrar. Los datos de las unidades cifradas no se pueden ver sin escribir el PIN ni la contraseña. Si el hardware de su equipo incluye un módulo de plataforma de confianza (TPM) habilitado, el chip de TPM le pedirá su PIN antes de iniciar Windows en el equipo.

## Acerca del PIN y las contraseñas de BitLocker


Tu empresa especifica la complejidad necesaria para tu PIN o contraseña. Estos requisitos para su PIN o contraseña se explican durante el proceso de configuración de BitLocker.

La contraseña se usa para desbloquear unidades en el equipo que no contienen el sistema operativo. BitLocker le pedirá la contraseña una vez que se solicite el PIN durante el inicio. Cada disco duro protegido con BitLocker de su equipo tiene su propia contraseña exclusiva. No se puede desbloquear una unidad protegida con BitLocker hasta que se proporcione la contraseña.

**Nota:**  El Departamento de soporte puede configurar unidades para que se desbloqueen automáticamente. Esto elimina la necesidad de proporcionar un PIN o una contraseña para ver la información de las unidades.

 

## Desbloquear el equipo si olvida su PIN o contraseña


Si olvida su PIN o la contraseña, el servicio de asistencia puede ayudarle a desbloquear las unidades protegidas con BitLocker. Para desbloquear una unidad protegida con BitLocker, póngase en contacto con el Departamento de soporte técnico si necesita ayuda.

**Cómo desbloquear el equipo si olvida su PIN o contraseña**

1.  Cuando se comunique con el Departamento de soporte técnico, tendrá que proporcionarle la siguiente información:

    -   Tu nombre de usuario

    -   Su dominio

    -   Los primeros ocho dígitos de la identificación de la clave de recuperación. Este es un código de 32 dígitos que BitLocker mostrará Si olvidas tu PIN o contraseña.

        -   Si olvida su PIN, tendrá que escribir los primeros ocho dígitos de la identificación de la clave de recuperación, que aparecerá en la consola de recuperación de BitLocker. La consola de recuperación de BitLocker es una pantalla anterior a Windows que se mostrará si no escribe el PIN correcto.

        -   Si olvida su contraseña, busque el identificador de clave de recuperación en la aplicación panel de control de opciones de cifrado de BitLocker. Seleccione **desbloquear unidad** y, a continuación, haga clic en **no puedo recordar mi contraseña**. La aplicación opciones de cifrado de BitLocker mostrará un identificador de clave de recuperación que usted proporcione al servicio de asistencia.

2.  Una vez que el servicio de asistencia reciba la información necesaria, le proporcionará una clave de recuperación por teléfono o por correo electrónico.

    -   Si olvidó el PIN, escriba la clave de recuperación en la consola de recuperación de BitLocker para desbloquear el equipo.

    -   Si olvidó la contraseña, escriba la clave de recuperación en la aplicación panel de control de opciones de cifrado de BitLocker, en la misma ubicación en la que encontró la identificación de clave de recuperación anterior. Esto desbloqueará el disco duro protegido.

## Cambiar el PIN o la contraseña


Para poder cambiar la contraseña en una unidad protegida con BitLocker, debe desbloquear la unidad. Si la unidad no está desbloqueada, seleccione **desbloquear unidad**y, a continuación, escriba la contraseña actual. Tan pronto como se desbloquee la unidad, puede seleccionar **administrar su contraseña** para cambiar su contraseña actual.

**Cómo cambiar el PIN o la contraseña**

1.  Haga clic en **Inicio**y, a continuación, seleccione **Panel de control**. El panel de control se abre en una ventana nueva.

2.  Seleccione **sistema y seguridad**y, a continuación, seleccione **Opciones de cifrado de BitLocker**.

    -   Para cambiar el PIN, seleccione **administrar su PIN**. Escriba el nuevo PIN en ambos campos y seleccione **restablecer PIN**.

    -   Para cambiar la contraseña, seleccione **administrar la contraseña**. Escriba la nueva contraseña en ambos campos y seleccione **Restablecer contraseña**.

 

 





