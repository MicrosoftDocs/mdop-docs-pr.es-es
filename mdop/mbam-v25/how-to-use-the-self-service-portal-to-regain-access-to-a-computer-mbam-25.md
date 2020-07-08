---
title: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
description: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826701"
---
# Cómo usar el portal de autoservicio para recuperar el acceso a un equipo


El portal de autoservicio es un sitio web que los administradores de TI pueden configurar como parte de su implementación de administración y supervisión de Microsoft BitLocker (MBAM) 2,5. El sitio web permite que los usuarios finales vuelvan a obtener acceso de forma independiente a sus equipos si se bloquean en Windows. El portal de autoservicio no requiere asistencia del personal del servicio de asistencia.

Las siguientes instrucciones están escritas a partir de la perspectiva de los usuarios finales, pero la información puede resultar útil para que los administradores de ti la entiendan.

**Importante**  Un usuario final debe haber iniciado sesión físicamente en el equipo (no de forma remota) al menos una vez como mínimo para poder recuperar su clave con el portal de autoservicio. De lo contrario, deben usar el portal de asistencia para la recuperación de claves.

 

Los usuarios finales pueden experimentar bloqueos si:

-   Olvidar su contraseña o PIN

-   Cambiar los archivos del sistema operativo, el BIOS o el módulo de plataforma segura (TPM)

**Nota:**  Si el administrador de ti ha configurado el tiempo de espera de un estado de sesión de IIS, se muestra un mensaje en el portal de autoservicio 60 segundos antes del tiempo de espera.

 

**Para usar el portal de autoservicio para recuperar el acceso a un equipo**

1.  En el **campo ID de identificación** , escriba un mínimo de ocho dígitos de la clave de bitlocker de 32 dígitos que se muestra en la pantalla de recuperación de BitLocker de su equipo. Si los primeros ocho dígitos coinciden con varias claves, se muestra un mensaje que requiere que escriba todos los dígitos de 32 del identificador de la clave de recuperación.

2.  En el campo **Reason** , seleccione el motivo de la solicitud de la clave de recuperación.

3.  Haga clic en **obtener tecla**. La clave de recuperación de BitLocker se muestra en el campo **clave de recuperación de BitLocker** .

4.  Escribe el código de 48 dígitos en la pantalla de recuperación de BitLocker de tu equipo para recuperar el acceso al equipo.



## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





