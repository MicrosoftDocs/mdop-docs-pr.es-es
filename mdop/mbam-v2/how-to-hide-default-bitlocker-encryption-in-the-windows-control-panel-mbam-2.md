---
title: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
description: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824081"
---
# Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows


Administración y supervisión de Microsoft BitLocker (MBAM) ofrece un panel de control personalizado para los equipos cliente de supervisión y administración de Microsoft BitLocker, denominados opciones de cifrado de BitLocker. Este panel de control personalizado puede reemplazar el panel de control predeterminado de BitLocker de Windows, que se denomina cifrado de unidad BitLocker. El panel de control personalizado, que se encuentra en el panel de control, está en sistema y seguridad, permite a los usuarios administrar su PIN y contraseñas y desbloquear unidades, y oculta la interfaz que permite a los administradores descifrar una unidad o reanudar o reanudar el cifrado de unidad BitLocker.

**Para ocultar el cifrado de unidad BitLocker predeterminado en el panel de control de Windows**

1.  En la consola de administración de directivas de grupo (GPMC), la administración avanzada de directivas de grupo (AGPM) o el editor de directivas de grupo local en el equipo de directivas de grupo de BitLocker, vaya a **configuración de usuario**.

2.  A continuación, haga clic en **directivas**, seleccione **plantillas administrativas**y, a continuación, haga clic en **Panel de control**.

3.  Haga doble clic en **ocultar los elementos especificados del panel de control** en el panel de **detalles** y, a continuación, seleccione **habilitado**.

4.  Haga clic en **Mostrar**, en **Agregar**y, a continuación, escriba **Microsoft. BitLockerDriveEncryption**. Esta directiva oculta la herramienta de administración predeterminada de BitLocker de Windows del panel de control de Windows y, en el panel de control, permite al usuario abrir la herramienta de opciones de cifrado de MBAM BitLocker actualizada en sistema y seguridad.

## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





