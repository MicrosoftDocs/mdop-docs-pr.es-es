---
title: Cómo recuperar una unidad que se ha movido
description: Cómo recuperar una unidad que se ha movido
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825061"
---
# Cómo recuperar una unidad que se ha movido


Al mover una unidad de sistema operativo cifrada mediante Microsoft BitLocker Administration and Monitoring (MBAM), la unidad no aceptará el PIN que se usó en un equipo anterior debido al cambio en el módulo de plataforma segura (TPM). Para usar la unidad movida, necesitará una forma de obtener la identificación de la clave de recuperación para recuperar la contraseña de recuperación. Use el siguiente procedimiento para recuperar una unidad que se ha movido.

**Para recuperar una unidad movida**

1.  En el equipo que contiene la unidad movida, inicie el equipo en modo entorno de recuperación de Windows (WinRE) o inicie el equipo con el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT).

2.  Una vez que el equipo se haya iniciado con WinRE o DaRT, la administración y la supervisión de Microsoft BitLocker tratarán la unidad de sistema operativo movida como una unidad de datos. MBAM mostrará el identificador de la contraseña de recuperación de la unidad y le pedirá la contraseña de recuperación.

    **Nota:**  En algunos casos, es posible que pueda hacer clic en **olvidé el PIN** durante el proceso de inicio y, después, especificar el modo de recuperación para mostrar la identificación de la clave de recuperación.

     

3.  Use la identificación de la clave de recuperación para recuperar la contraseña de recuperación y desbloquear la unidad desde el sitio web de administración y supervisión.

4.  Si la unidad movida se configuró para usar un chip de TPM en el equipo original, debe realizar pasos adicionales después de desbloquear la unidad y completar el proceso de inicio. En el modo de WinRE, abra un símbolo del sistema y use la herramienta **Manage-BDE** para descifrar la unidad. Usar esta herramienta es la única forma de quitar el TPM más el protector del PIN sin el chip TPM original.

5.  Una vez completada la eliminación, inicie el equipo de forma normal. El agente de MBAM aplicará ahora la Directiva para cifrar la unidad con el TPM y el PIN del nuevo equipo.

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





