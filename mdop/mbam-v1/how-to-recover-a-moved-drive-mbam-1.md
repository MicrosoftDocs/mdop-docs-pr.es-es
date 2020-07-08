---
title: Cómo recuperar una unidad que se ha movido
description: Cómo recuperar una unidad que se ha movido
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812927"
---
# Cómo recuperar una unidad que se ha movido


Al mover una unidad de sistema operativo que ha sido cifrada anteriormente mediante Microsoft BitLocker Administration and Monitoring (MBAM), debe resolver determinados problemas. Una vez que se ha conectado un PIN al nuevo equipo, la unidad no aceptará el PIN de inicio que se usó en el equipo anterior. El sistema considera que el PIN no es válido debido al cambio en el chip módulo de plataforma segura (TPM). Para poder usar la unidad movida, debe obtener un identificador de clave de recuperación para recuperar la contraseña de recuperación. Para ello, use el procedimiento siguiente.

**Para recuperar una unidad movida**

1.  En el equipo que contiene la unidad movida, inicie en el modo entorno de recuperación de Windows (WinRE) o inicie el equipo con el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT).

2.  Una vez que el equipo se haya iniciado con WinRE o DaRT, MBAM tratará la unidad de sistema operativo movida como una unidad de datos. MBAM mostrará el identificador de la contraseña de recuperación de la unidad y le pedirá la contraseña de recuperación.

    **Nota:**  En algunos casos, es posible que pueda hacer clic en **olvidar el PIN** durante el proceso de inicio para entrar en el modo de recuperación. También se muestra la identificación de la clave de recuperación.

     

3.  En el sitio web de administración de MBAM, use la identificación de la clave de recuperación para recuperar la contraseña de recuperación y desbloquear la unidad.

4.  Si la unidad movida se configuró para usar un chip de TPM en el equipo original, debe realizar pasos adicionales después de desbloquear la unidad y completar el proceso de inicio. En el modo de WinRE, abra un símbolo del sistema y use la herramienta **Manage-BDE** para descifrar la unidad. El uso de esta herramienta es la única forma de quitar la protección de TPM con PIN sin el chip de TPM original.

5.  Una vez completada la eliminación, inicie el sistema normalmente. El agente de MBAM continuará aplicando la Directiva para cifrar la unidad con el TPM y el PIN del nuevo equipo.

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





