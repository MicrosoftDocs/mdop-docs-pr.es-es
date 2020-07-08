---
title: Cómo restablecer un bloqueo de TPM
description: Cómo restablecer un bloqueo de TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812919"
---
# Cómo restablecer un bloqueo de TPM


La característica de recuperación de unidades cifradas de administración y supervisión de BitLocker de Microsoft (MBAM) engloba la captura y el almacenamiento de datos, así como la disponibilidad de las herramientas necesarias para administrar el módulo de plataforma segura (TPM). En este tema, se explica cómo acceder al sistema centralizado de datos de recuperación de claves en el _admmon \ _tlanextref sitio web de administración. El sistema de datos de recuperación de claves puede proporcionar un archivo de contraseña de propietario de TPM cuando se proporciona la identidad del equipo y el identificador de usuario asociado.

Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces. El número de veces que un usuario puede escribir un PIN incorrecto antes de que el bloqueo de TPM se base en la especificación del fabricante del equipo.

**Para restablecer un bloqueo de TPM**

1.  Abra el sitio web de administración de MBAM.

2.  En el panel de navegación, seleccione **administrar TPM**. Se abrirá la página **Manage TPM** .

3.  Escriba el nombre de dominio completo (FQDN) del equipo y el nombre del equipo. Escriba el dominio de inicio de sesión de Windows del usuario y el nombre de usuario del usuario. Seleccione una de las opciones predefinidas en el menú desplegable motivo por el que se **solicita un archivo de contraseña de propietario de TPM** . Haz clic en **Enviar**.

4.  MBAM devolverá una de las siguientes opciones:

    -   Mensaje de error si no se encuentra ningún archivo de contraseña de propietario de TPM coincidente

    -   El archivo de contraseña de propietario de TPM para el equipo enviado

    **Nota:**  Si es un usuario avanzado del servicio de asistencia, los campos dominio del usuario e identificador de usuario no son obligatorios.

     

5.  Después de la recuperación, se muestra la contraseña de propietario. Para guardar esta contraseña en un archivo. TPM, haga clic en el botón **Guardar** .

6.  El usuario ejecutará la consola de administración de TPM y seleccionará la opción **restablecer el bloqueo de TPM** y proporcionará el archivo de contraseña de propietario de TPM para restablecer el bloqueo de TPM.

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





