---
title: Ayuda a los usuarios finales para administrar BitLocker
description: Ayuda a los usuarios finales para administrar BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824780"
---
# Ayuda a los usuarios finales para administrar BitLocker


El contenido de un equipo perdido o robado es vulnerable a acceso no autorizado, que puede presentar un riesgo de seguridad tanto para personas como para empresas. Administración y supervisión de Microsoft BitLocker (MBAM) usa BitLocker para ayudar a evitar el acceso no autorizado bloqueando el equipo con el fin de proteger los datos confidenciales de usuarios maliciosos.

## ¿Qué es BitLocker?


El cifrado de unidad BitLocker puede proporcionar protección a las unidades de sistema operativo, unidades de datos y unidades extraíbles (por ejemplo, una unidad USB) mediante el cifrado de las unidades. Según el modo en que se configure BitLocker, los usuarios pueden tener que proporcionar una clave (una contraseña o PIN) para desbloquear la información almacenada en las unidades cifradas.

Al agregar nuevos archivos a una unidad cifrada con BitLocker, BitLocker los cifra automáticamente. Los archivos permanecen cifrados mientras se almacenan en la unidad cifrada. Los archivos que se copian a otra unidad o equipo se descifran. Si comparte archivos con otros usuarios, como a través de una red, estos archivos se cifran y se almacenan en la unidad cifrada, pero los usuarios autorizados pueden obtener acceso a ellos en forma normal.

Si cifra la unidad del sistema operativo, BitLocker comprueba el equipo durante el inicio en busca de condiciones que puedan representar un riesgo de seguridad (por ejemplo, un cambio en el BIOS o en los archivos de inicio). Si se detecta un riesgo potencial de seguridad, BitLocker bloqueará la unidad del sistema operativo y requerirá una clave de recuperación de BitLocker especial para desbloquearla. Asegúrese de crear esta clave de recuperación al activar BitLocker por primera vez. De lo contrario, podrás perder el acceso a tus archivos de forma permanente.

Si cifra las unidades de datos (fijas o extraíbles), puede desbloquear una unidad cifrada con una contraseña o una tarjeta inteligente, o configurar la unidad para que se desbloquee automáticamente cuando inicie sesión en el equipo.

Además de las contraseñas y los pin, BitLocker puede usar el chip módulo de plataforma segura (TPM) que se proporciona en muchos equipos más nuevos. El chip de TPM se usa para asegurarse de que el equipo no ha sido manipulado antes de que BitLocker desbloquee la unidad del sistema operativo. Durante el proceso de cifrado, es posible que tenga que habilitar el chip TPM. Al iniciar el equipo, BitLocker pide a TPM las teclas a la unidad y la desbloquea. Para habilitar el chip TPM, tendrá que reiniciar el equipo y, a continuación, cambiar una configuración en el BIOS, una capa anterior a Windows del software de su equipo. Para obtener más información sobre el TPM, consulte [acerca del chip TPM del equipo](about-the-computer-tpm-chip.md).

Una vez que su equipo esté protegido por BitLocker, es posible que tenga que escribir un PIN o una contraseña cada vez que el equipo se reactive tras la hibernación o el inicio. El Departamento de soporte técnico de su empresa u organización puede ayudarle si alguna vez olvida su PIN o contraseña.

Puede desactivar BitLocker, ya sea de forma temporal, al suspenderlo, o de forma permanente, descifrando la unidad.

**Nota:**  Como BitLocker cifra toda la unidad y no solo los archivos individuales, tenga cuidado al mover datos confidenciales entre unidades. Si mueve un archivo de una unidad protegida con BitLocker a una unidad no cifrada, el archivo ya no se cifrará.

 

## Acerca de la aplicación de opciones de cifrado de BitLocker


Para desbloquear las unidades de disco duro de su equipo y administrar el PIN y las contraseñas, use la aplicación de opciones de cifrado de BitLocker en el panel de control de Windows siguiendo el procedimiento que se describe aquí. Puede escribir contraseñas para desbloquear unidades protegidas y puede comprobar el estado de BitLocker de las unidades conectadas mediante esta aplicación.

**Para abrir la aplicación de opciones de cifrado de BitLocker**

1.  Haga clic en **Inicio**y seleccione **Panel de control**. El panel de control se abre en una ventana nueva.

2.  En el **Panel de control**, seleccione **sistema y seguridad**.

3.  Seleccione **Opciones de cifrado de BitLocker** para abrir la aplicación de opciones de cifrado de BitLocker.

    Para obtener una descripción de las opciones disponibles, consulte la sección siguiente.

## Opciones de la aplicación de opciones de cifrado de BitLocker


La aplicación de opciones de cifrado de BitLocker del panel de control le permite administrar el PIN y las contraseñas, que BitLocker usa para proteger el equipo.

**Cifrado de unidad BitLocker: unidades de disco fijo:**

En esta sección, puede ver información sobre las unidades de disco duro conectadas a su equipo y su estado de cifrado actual de BitLocker.

-   **Administrar su PIN** : cambia el PIN usado por BitLocker para desbloquear la unidad del sistema operativo.

-   **Administrar la contraseña** : cambia la contraseña que usa BitLocker para desbloquear las otras unidades internas.

**Cifrado de unidad BitLocker: unidades externas:**

En esta sección, puede ver información sobre las unidades externas (como una unidad USB) conectada a su equipo y su estado actual de cifrado de BitLocker.

-   **Administrar la contraseña** : cambia la contraseña que usa BitLocker para desbloquear las otras unidades internas.

**Expertos**

-   **Administración de TPM** : abre la herramienta de administración de TPM en una ventana independiente. Desde aquí puede configurar tareas comunes de TPM y obtener información sobre el conjunto de chips de TPM. Para tener acceso a esta herramienta, debe tener permisos administrativos en el equipo.

-   **Administración de discos** : Abra la herramienta Administración de discos. Desde aquí puede ver la información de todos los discos duros conectados al equipo y configurar las particiones y las opciones de unidad. Para obtener acceso a esta herramienta, debe tener derechos administrativos en el equipo.

 

 





