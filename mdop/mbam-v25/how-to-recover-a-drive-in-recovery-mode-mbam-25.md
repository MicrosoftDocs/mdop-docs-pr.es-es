---
title: Cómo recuperar una unidad en modo de recuperación
description: Cómo recuperar una unidad en modo de recuperación
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823370"
---
# Cómo recuperar una unidad en modo de recuperación


En este tema se explica cómo usar el sitio web de administración y supervisión (también conocido como servicio de asistencia) para obtener una contraseña de recuperación que conceder a los usuarios finales si su unidad protegida con BitLocker pasa al modo de recuperación. Las unidades entran en el modo de recuperación si los usuarios pierden su PIN o su contraseña, o si el chip de la plataforma de módulo de confianza (TPM) detecta cambios en el BIOS o los archivos de inicio de un equipo.

Para obtener una contraseña de recuperación, use el área de **recuperación de Drive** del sitio web de administración y supervisión. Para acceder a esta área del sitio web, debe tener asignados los roles de usuarios de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico.

**Nota**  
Es posible que haya dado a estos roles nombres diferentes al crearlos. Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).



**Importante**  
Las contraseñas de recuperación vencen después de un solo uso. En las unidades de sistema operativo y las unidades de datos fijas, la regla de uso único se aplica automáticamente. En las unidades extraíbles, se aplica cuando se quita la unidad y se vuelve a insertar y a desbloquear en un equipo que tiene activada la configuración de directiva de grupo para administrar unidades extraíbles.



**Para recuperar una unidad en modo de recuperación**

1.  Abra un explorador Web y vaya al **sitio web de administración y supervisión**.

2.  En el panel izquierdo, seleccione **recuperación de unidades** para abrir la página **recuperar el acceso a una unidad cifrada** .

3.  Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario final para ver la información de recuperación.

    **Nota**  
    Si se encuentra en el grupo de usuarios del servicio de asistencia MBAM avanzado, los campos dominio del usuario e identificador de usuario no son obligatorios.



4.  Escriba los primeros ocho dígitos de la identificación de la clave de recuperación para ver una lista de las posibles claves de recuperación coincidentes, o bien escriba la identificación de la clave de recuperación completa para obtener la clave de recuperación exacta.

5.  En la lista **motivo de desbloqueo** de la unidad, seleccione una de las opciones predefinidas y, a continuación, haga clic en **Enviar**.

    MBAM devuelve lo siguiente:

    -   Mensaje de error si no se encuentra ninguna contraseña de recuperación coincidente

    -   Varias coincidencias posibles si el usuario tiene varias contraseñas de recuperación coincidentes

    -   La contraseña de recuperación y el paquete de recuperación para el usuario enviado

        **Nota**  
        Si está recuperando una unidad dañada, la opción paquete de recuperación proporciona a BitLocker información crítica que necesita para recuperar la unidad.



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. Para copiar la contraseña, haga clic en **copiar clave**y, a continuación, pegue la contraseña de recuperación en un mensaje de correo electrónico. También puede hacer clic en **Guardar** para guardar la contraseña de recuperación en un archivo.

   Cuando el usuario escribe la contraseña de recuperación en el sistema o usa el paquete de recuperación, la unidad se desbloquea.



## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





