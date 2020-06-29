---
title: Realización de la administración de BitLocker con MBAM 2.5
description: Realización de la administración de BitLocker con MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826010"
---
# Realización de la administración de BitLocker con MBAM 2.5


Después de planear y de implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurarlo y usarlo para administrar el cifrado de unidad BitLocker en toda la empresa. La información de esta sección describe las tareas de administración de cifrado de BitLocker posteriores a la instalación que se realizan mediante la administración y supervisión de Microsoft BitLocker.

## Restablecer un bloqueo de TPM


Un módulo de plataforma segura (TPM) es un microchip diseñado para proporcionar funciones básicas de seguridad, principalmente relacionadas con las claves de cifrado. El TPM generalmente se instala en la placa base de un equipo y se comunica con el resto del sistema con un adaptador de bus host. En los equipos que incorporan un TPM, puede crear claves criptográficas y cifrarlas para que solo el TPM pueda descifrarlas.

Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces. El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen según el fabricante. Puede usar MBAM para acceder al sistema de datos de recuperación de claves centralizado en el sitio web de administración y supervisión, donde puede recuperar un archivo de contraseña de propietario de TPM al proporcionar un identificador de equipo y un identificador de usuario asociado.

[Cómo restablecer un bloqueo de TPM](how-to-reset-a-tpm-lockout-mbam-25.md)

## Recuperar unidades


Cuando trabaje con el cifrado de datos, especialmente en un entorno empresarial, considere cómo se pueden recuperar los datos en caso de que se produzca un error de hardware, cambios en el personal u otras situaciones en las que se puedan perder las claves de cifrado.

Las características de recuperación de unidades cifradas de MBAM garantizan que los datos se pueden capturar y almacenar y que las herramientas necesarias están disponibles para acceder a un volumen protegido con BitLocker cuando se produce BitLocker entra en modo de recuperación, se mueve o se daña.

[Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[Cómo recuperar una unidad que se ha movido](how-to-recover-a-moved-drive-mbam-25.md)

[Cómo recuperar una unidad dañada](how-to-recover-a-corrupted-drive-mbam-25.md)

## Determinar el estado de cifrado de BitLocker de equipos perdidos


Al usar MBAM, puede determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.

[Cómo determinar el estado de cifrado de BitLocker de equipos perdidos](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## Usar el portal de autoservicio para recuperar el acceso a un equipo


Si los usuarios finales se bloquean en Windows mediante BitLocker, pueden usar las instrucciones de esta sección para obtener una clave de recuperación de BitLocker para volver a obtener acceso a su equipo.

[Cómo usar el portal de autoservicio para recuperar el acceso a un equipo](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## Temas relacionados


[Operaciones para MBAM 2.5](operations-for-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





