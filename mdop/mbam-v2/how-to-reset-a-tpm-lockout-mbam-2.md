---
title: Cómo restablecer un bloqueo de TPM
description: Cómo restablecer un bloqueo de TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825051"
---
# Cómo restablecer un bloqueo de TPM


La característica de recuperación de unidades cifradas de administración y supervisión de BitLocker de Microsoft (MBAM) engloba la captura y el almacenamiento de datos, así como la disponibilidad de las herramientas necesarias para administrar el módulo de plataforma segura (TPM). En este tema, se explica cómo acceder al sistema de datos de recuperación de claves centralizado en el sitio web de administración y supervisión, que puede proporcionar un archivo de contraseña de propietario de TPM cuando se proporciona un identificador de equipo y el identificador de usuario asociado.

Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces. El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro.

Puede restablecer un bloqueo de TPM solo si MBAM es propietario del TPM.

**Para restablecer un bloqueo de TPM**

1.  Abra un explorador Web y vaya al sitio web de administración y supervisión.

2.  En el panel de navegación izquierdo, seleccione **administrar TPM** para abrir la página **administrar TPM** .

3.  Escriba el nombre de dominio completo del equipo y el nombre del equipo, y escriba el dominio de inicio de sesión de Windows del usuario y el nombre de usuario del usuario para recuperar el archivo de contraseña de propietario de TPM.

4.  En la lista de **archivos de contraseña de propietario de TPM** , seleccione un motivo para la solicitud y haga clic en **Enviar**.

    MBAM devuelve una de las siguientes opciones:

    -   Un mensaje de error, si no se encuentra ningún archivo de contraseña de propietario de TPM coincidente

    -   El archivo de contraseña de propietario de TPM para el equipo enviado

    **Nota**  
    Si es un usuario avanzado del servicio de asistencia, los campos dominio del usuario e identificador de usuario no son obligatorios.



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. Para guardar la contraseña en un archivo. TPM, haga clic en el botón **Guardar** .

   El usuario ejecutará la consola de administración de TPM, selecciona la opción **restablecer el bloqueo de TPM** y proporciona el archivo de contraseña de propietario de TPM para restablecer el bloqueo de TPM.

   **Importante**  
   Los administradores del servicio de asistencia no deben conceder el valor de hash de TPM o el archivo de contraseña de propietario de TPM a los usuarios finales. La información del TPM no cambia, por lo que puede suponer un riesgo de seguridad si el archivo se proporciona a los usuarios finales.



## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









