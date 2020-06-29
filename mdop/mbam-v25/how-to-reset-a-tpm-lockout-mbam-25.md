---
title: Cómo restablecer un bloqueo de TPM
description: Cómo restablecer un bloqueo de TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823321"
---
# Cómo restablecer un bloqueo de TPM


En este tema se explica cómo usar el sitio web de administración y supervisión (también conocido como soporte técnico) para restablecer un bloqueo de TPM. Los bloqueos de TPM pueden producirse si un usuario final escribe el PIN incorrecto demasiadas veces. El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro.

Desde el área **administrar TPM** del sitio web administración y supervisión, puede acceder al sistema centralizado de datos de recuperación de claves, que proporciona un archivo de contraseña de propietario de TPM cuando se proporciona un identificador de equipo y un identificador de usuario asociado.

Para acceder al área administrar TPM del sitio web de administración y supervisión, debe tener asignado el rol de usuarios del Departamento de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico de MBAM. Estos roles son grupos que los administradores crean en Active Directory. Puede usar cualquier nombre para estos grupos. Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

Para obtener información sobre la propiedad de MBAM y TPM, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

**Para restablecer un bloqueo de TPM**

1.  Abra un explorador Web y vaya al **sitio web de administración y supervisión**.

2.  En el panel de la izquierda, haga clic en **administrar TPM** para abrir la página **administrar TPM** .

3.  Escriba el nombre de dominio completo del equipo y el nombre del equipo.

4.  Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario final para recuperar el archivo de contraseña de propietario de TPM.

    **Nota:**  Si se encuentra en el grupo de usuarios del servicio de asistencia MBAM avanzado, los campos dominio del usuario e identificador de usuario no son obligatorios.

     

5.  En la lista de **archivos de contraseña de propietario de TPM** , seleccione un motivo para la solicitud y haga clic en **Enviar**.

    MBAM devuelve una de las siguientes opciones:

    -   Mensaje de error si no se encuentra ningún archivo de contraseña de propietario de TPM coincidente

    -   El archivo de contraseña de propietario de TPM para el equipo enviado

    Después de que se recupera la contraseña de propietario de TPM, se muestra la contraseña de propietario.

6.  Para guardar la contraseña en un archivo. TPM, haga clic en el botón **Guardar** .

7.  En el área **administrar TPM** del **sitio web de administración y supervisión**, seleccione la opción **restablecer el bloqueo de TPM** y proporcione el archivo de contraseña de propietario de TPM.

    Se restablece el bloqueo de TPM y se restaura el acceso del usuario final.

    **Importante**  No asigne el valor de hash de TPM o el archivo de contraseña de propietario de TPM a los usuarios finales. Debido a que la información de TPM no cambia, ofrecer el archivo a los usuarios finales supone un riesgo de seguridad.

     



## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





