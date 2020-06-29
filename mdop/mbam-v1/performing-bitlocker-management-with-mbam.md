---
title: Realizar la administración de BitLocker con MBAM
description: Realizar la administración de BitLocker con MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825891"
---
# Realizar la administración de BitLocker con MBAM


Después de implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurar y usar MBAM para administrar el cifrado de BitLocker empresarial. En esta sección se describen las tareas de administración de cifrado de BitLocker posteriores a la instalación que se pueden llevar a cabo con MBAM.

## Restablecer un bloqueo de TPM con MBAM


Un microchip de módulo de plataforma segura (TPM) proporciona funciones básicas de seguridad. Estas funciones se realizan principalmente mediante el uso de claves de cifrado. El TPM suele instalarse en la placa base de un equipo o portátil y se comunica con el resto del sistema mediante un bus de hardware. Los equipos que incorporan un TPM pueden crear claves criptográficas que solo TPM puede descifrar. Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces. El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro. El sistema de datos de recuperación de claves del sitio web de administración de MBAM le permite obtener un archivo de contraseña de propietario de TPM restablecido.

[Cómo restablecer un bloqueo de TPM](how-to-reset-a-tpm-lockout-mbam-1.md)

## Recuperar unidades con MBAM


Asegúrese de que sabe cómo intentar recuperar datos desde unidades cifradas en el caso de que se produzca un error de hardware, cambios en el personal u otras situaciones en las que se pierdan las claves de cifrado. Las características de recuperación de unidades cifradas de MBAM proporcionan la captura y el almacenamiento de los datos y la disponibilidad de las herramientas necesarias para acceder a un volumen protegido por BitLocker cuando el volumen pasa al modo de recuperación, se mueve o se daña.

[Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[Cómo recuperar una unidad que se ha movido](how-to-recover-a-moved-drive-mbam-1.md)

[Cómo recuperar una unidad dañada](how-to-recover-a-corrupted-drive-mbam-1.md)

## Determinar el estado de cifrado de BitLocker de equipos perdidos con MBAM


Al usar MBAM, puede determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.

[Cómo determinar el estado de cifrado de BitLocker de equipos perdidos](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## Otros recursos para realizar la administración de BitLocker con MBAM


[Operaciones para MBAM 1.0](operations-for-mbam-10.md)

 

 





