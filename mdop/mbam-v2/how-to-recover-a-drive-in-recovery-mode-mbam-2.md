---
title: Cómo recuperar una unidad en modo de recuperación
description: Cómo recuperar una unidad en modo de recuperación
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825060"
---
# Cómo recuperar una unidad en modo de recuperación


Las características de recuperación de unidades cifradas de administración y supervisión de BitLocker de Microsoft (MBAM) garantizan la captura y el almacenamiento de los datos y la disponibilidad de las herramientas necesarias para acceder a un volumen protegido con BitLocker cuando BitLocker pasa al modo de recuperación. Un volumen protegido por BitLocker pasa al modo de recuperación cuando se pierde o se olvida una contraseña o un PIN, o cuando el chip de la plataforma de módulo de confianza (TPM) detecta cambios en el BIOS o los archivos de inicio de un equipo.

Use este procedimiento para acceder al sistema de datos de recuperación de claves centralizado, que puede proporcionar una contraseña de recuperación si se proporciona un identificador de contraseña de recuperación y un identificador de usuario asociado.

**Importante**  
Administración y supervisión de Microsoft BitLocker usa claves de recuperación de un solo uso que vencen al usarlas. El único uso de una contraseña de recuperación se aplica automáticamente a las unidades de sistema operativo y las unidades fijas. En las unidades extraíbles, se aplica cuando se quita la unidad y, a continuación, se vuelve a insertar y a desbloquear en un equipo que tiene activada la configuración de directiva de grupo para administrar unidades extraíbles.



**Para recuperar una unidad en modo de recuperación**

1.  Abra un explorador Web y vaya al sitio web de administración y supervisión.

2.  En el panel de navegación, haga clic en **recuperación de unidades**. Se abrirá la página web "recuperar acceso a una unidad cifrada".

3.  Escriba el dominio de inicio de sesión de Windows y el nombre de usuario del usuario para ver la información de recuperación y los primeros ocho dígitos de la identificación de la clave de recuperación para recibir una lista de las posibles claves de recuperación coincidentes o la identificación de la clave de recuperación completa para recibir la clave de recuperación exacta.

4.  Seleccione una de las opciones predefinidas de la lista **motivo de desbloqueo de unidades** y, a continuación, haga clic en **Enviar**.

    **Nota**  
    Si es un usuario avanzado de MBAM Helpdesk, no es necesario que las entradas del dominio del usuario y del identificador de usuario.



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. Para copiar la contraseña, haga clic en **copiar clave**y, a continuación, pegue la contraseña de recuperación en un mensaje de correo electrónico. También puede hacer clic en **Guardar** para guardar la contraseña de recuperación en un archivo.

   Cuando el usuario escribe la contraseña de recuperación en el sistema o usa el paquete de recuperación, la unidad se desbloquea.

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









