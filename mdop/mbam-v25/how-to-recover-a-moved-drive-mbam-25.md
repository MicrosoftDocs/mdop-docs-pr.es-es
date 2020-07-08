---
title: Cómo recuperar una unidad que se ha movido
description: Cómo recuperar una unidad que se ha movido
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823341"
---
# Cómo recuperar una unidad que se ha movido
En este tema se explica cómo usar el sitio web de administración y supervisión (también conocido como servicio de asistencia) para recuperar una unidad de sistema operativo que se movió después de ser cifrada por la supervisión y administración de BitLocker de Microsoft (MBAM). Cuando se mueve una unidad, ya no acepta el PIN que se usó en el equipo anterior porque el chip módulo de plataforma segura (TPM) ha cambiado. Para recuperar la unidad movida, debe obtener la identificación de la clave de recuperación para recuperar la contraseña de recuperación.

Para recuperar una unidad movida, debe usar el área de **recuperación de unidad** del sitio web de administración y supervisión. Para acceder al área de **recuperación de unidades** , debe tener asignado el rol de usuarios del Departamento de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico de MBAM. Para obtener más información sobre estos roles, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Para recuperar una unidad movida**
1.  En el equipo que contiene la unidad movida, inicie el equipo en modo entorno de recuperación de Windows (WinRE) o inicie el equipo con el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT).

2.  Una vez que el equipo se haya iniciado con WinRE o DaRT, MBAM tratará la unidad de sistema operativo movida como una unidad de datos fija. MBAM mostrará el identificador de la contraseña de recuperación de la unidad y le pedirá la contraseña de recuperación.

    **Nota:**  En algunos casos, es posible que pueda hacer clic en **olvidé el PIN** durante el proceso de inicio y, después, especificar el modo de recuperación para mostrar la identificación de la clave de recuperación.

     

3.  Use la identificación de la clave de recuperación para recuperar la contraseña de recuperación y desbloquear la unidad desde el sitio web de administración y supervisión. Para obtener instrucciones, consulte [Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).

    Si la unidad movida se configuró para usar un chip TPM en el equipo original, complete los siguientes pasos adicionales. En caso contrario, el proceso de recuperación ha finalizado.

4.  Después de desbloquear la unidad y completar el proceso de inicio, abra un símbolo del sistema en el modo de WinRE y use el `manage-bde` comando para descifrar la unidad. El uso de esta herramienta es la única forma de quitar el TPM más el protector del PIN sin el chip TPM original. Para obtener información sobre el `manage-bde` comando, consulte [Manage-BDE](https://go.microsoft.com/fwlink/?LinkId=393567).

5.  Una vez completada la eliminación, inicie el equipo de forma normal. El agente de MBAM aplicará ahora la Directiva para cifrar la unidad con el TPM del nuevo equipo más el PIN.



## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





