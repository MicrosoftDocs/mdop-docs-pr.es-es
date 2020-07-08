---
title: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
description: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826080"
---
# Cómo usar el portal de autoservicio para recuperar el acceso a un equipo


Si los usuarios finales se bloquean en Windows mediante BitLocker porque han olvidado su contraseña o su PIN, o porque han cambiado los archivos del sistema operativo o cambiado el BIOS o el módulo de plataforma segura (TPM), pueden usar el portal de autoservicio para recuperar el acceso a Windows sin tener que pedir asistencia al servicio de asistencia.

**Nota:**  Si el administrador de ti configuró el tiempo de espera de una sesión de IIS, se mostrará un mensaje de error 60 segundos antes de que se agote el tiempo de espera.

 

**Nota:**  Estas instrucciones están escritas para la perspectiva de los usuarios finales y desde la misma.

 

**Para usar el portal de autoservicio para recuperar el acceso a un equipo**

1.  En el **campo ID de identificación** , escriba un mínimo de ocho dígitos de la clave de bitlocker de 32 dígitos que se muestra en la pantalla de recuperación de BitLocker de su equipo.

    **Nota:**  Si los primeros ocho dígitos coinciden con varias claves, se muestra un mensaje que requiere que escriba todos los dígitos de 32 del identificador de la clave de recuperación.

     

2.  En el campo **Reason** , seleccione el motivo de la solicitud de la clave de recuperación.

3.  Haga clic en **obtener tecla**. La clave de recuperación de BitLocker se muestra en el campo "su clave de recuperación de BitLocker".

4.  Escribe el código de 48 dígitos en la pantalla de recuperación de BitLocker de tu equipo para recuperar el acceso al equipo.

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





