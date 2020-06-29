---
title: Cómo recuperar una unidad en modo de recuperación
description: Cómo recuperar una unidad en modo de recuperación
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812951"
---
# Cómo recuperar una unidad en modo de recuperación


Administración y supervisión de Microsoft BitLocker (MBAM) incluye características de recuperación de unidades cifradas. Estas características garantizan la captura y el almacenamiento de los datos y la disponibilidad de las herramientas necesarias para acceder a un volumen protegido con BitLocker cuando BitLocker coloca ese volumen en modo de recuperación. Un volumen protegido por BitLocker pasa al modo de recuperación cuando se pierde o se olvida una contraseña o un PIN, o cuando el chip de la plataforma de módulo de confianza (TPM) detecta un cambio en el BIOS o los archivos de inicio del equipo.

Use este procedimiento para acceder al sistema centralizado de datos de recuperación de claves que puede proporcionar una contraseña de recuperación cuando se proporciona un identificador de contraseña de recuperación y un identificador de usuario asociado.

**Importante**  MBAM genera claves de recuperación de un solo uso. Bajo esta limitación, una clave de recuperación solo se puede usar una vez y, después, ya no es válida. El único uso de una contraseña de recuperación se aplica automáticamente a las unidades de sistema operativo y las unidades fijas. En las unidades extraíbles, el uso único se aplica cuando se quita la unidad y, a continuación, se vuelve a insertar y a desbloquear en un equipo que tenga activada la configuración de directiva de grupo para administrar unidades extraíbles.

 

**Para recuperar una unidad en modo de recuperación**

1.  Abra el sitio web de MBAM.

2.  En el panel de navegación, haga clic en **recuperación de unidades**. Se abrirá la Página Web **recuperar acceso a una unidad cifrada** .

3.  Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario y los primeros ocho dígitos del identificador de la clave de recuperación para obtener una lista de las posibles claves de recuperación coincidentes. También puede escribir la identificación de la clave de recuperación completa para recibir la clave de recuperación exacta. Seleccione una de las opciones predefinidas en la lista desplegable **motivo del bloqueo de la unidad** y, a continuación, haga clic en **Enviar**.

    **Nota:**  Si es un usuario avanzado de MBAM Helpdesk, no es necesario que las entradas del dominio del usuario y del identificador de usuario.

     

4.  MBAM devuelve lo siguiente:

    1.  Mensaje de error si no se encuentra ninguna contraseña de recuperación coincidente

    2.  Varias coincidencias posibles si el usuario tiene varias contraseñas de recuperación coincidentes

    3.  La contraseña de recuperación y el paquete de recuperación para el usuario enviado

        **Nota:**  Si está recuperando una unidad dañada, la opción paquete de recuperación proporciona BitLocker con la información crítica necesaria para intentar la recuperación.

         

5.  Después de recuperar la contraseña de recuperación y el paquete de recuperación, aparecerá la contraseña de recuperación. Para copiar la contraseña, haga clic en **copiar clave**y, a continuación, pegue la contraseña de recuperación en un correo electrónico u otro archivo de texto para su almacenamiento temporal. O bien, para guardar la contraseña de recuperación en un archivo, haga clic en **Guardar**.

6.  Cuando el usuario escribe la contraseña de recuperación en el sistema o usa el paquete de recuperación, la unidad se desbloquea.

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





