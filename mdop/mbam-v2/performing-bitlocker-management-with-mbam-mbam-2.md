---
title: Realizar la administración de BitLocker con MBAM
description: Realizar la administración de BitLocker con MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826500"
---
# Realizar la administración de BitLocker con MBAM


Después de planear y de implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurarlo y usarlo para administrar el cifrado de BitLocker empresarial. La información de esta sección describe las tareas posteriores a la instalación de la administración de cifrado de BitLocker que se realizan mediante la administración y supervisión de Microsoft BitLocker.

## Restablecer un bloqueo de TPM mediante MBAM


Un módulo de plataforma segura (TPM) es un microchip diseñado para proporcionar funciones básicas de seguridad, principalmente relacionadas con las claves de cifrado. El TPM suele instalarse en la placa base de un equipo o portátil y se comunica con el resto del sistema mediante un bus de hardware. Los equipos que incorporan un TPM tienen la capacidad de crear claves criptográficas y cifrarlas para que solo el TPM pueda descifrarlas.

Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces. El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro. Puede usar MBAM para acceder al sistema de datos de recuperación de claves centralizado en el sitio web de administración y supervisión, donde puede recuperar un archivo de contraseña de propietario de TPM al proporcionar un identificador de equipo y el identificador de usuario asociado.

[Cómo restablecer un bloqueo de TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

## Recuperar unidades con MBAM


Cuando trabaje con el cifrado de datos, especialmente en un entorno empresarial, considere cómo se pueden recuperar los datos en caso de que se produzca un error de hardware, cambios en el personal u otras situaciones en las que se puedan perder las claves de cifrado.

Las características de recuperación de unidades cifradas de MBAM garantizan que los datos se pueden capturar y almacenar y que las herramientas necesarias están disponibles para acceder a un volumen protegido por BitLocker cuando se produce el modo de recuperación de BitLocker, se mueve o se daña.

[Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[Cómo recuperar una unidad que se ha movido](how-to-recover-a-moved-drive-mbam-2.md)

[Cómo recuperar una unidad dañada](how-to-recover-a-corrupted-drive-mbam-2.md)

## Determinar el estado de cifrado de BitLocker de equipos perdidos con MBAM


Con MBAM, puede determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.

[Cómo determinar el estado de cifrado de BitLocker de equipos perdidos](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## Usar el portal de autoservicio para recuperar el acceso a un equipo


Si los usuarios finales se bloquean en Windows mediante BitLocker, pueden usar las instrucciones de esta sección para obtener una clave de recuperación de BitLocker para volver a obtener acceso a su equipo.

[Cómo usar el portal de autoservicio para recuperar el acceso a un equipo](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## Otros recursos para realizar la administración de BitLocker con MBAM


[Operaciones para MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





