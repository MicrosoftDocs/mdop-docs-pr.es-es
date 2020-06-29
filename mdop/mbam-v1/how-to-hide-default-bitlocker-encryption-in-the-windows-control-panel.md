---
title: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
description: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824510"
---
# Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows


Administración y supervisión de Microsoft BitLocker (MBAM) ofrece un panel de control personalizado para los equipos cliente de MBAM denominados opciones de cifrado de BitLocker. Este panel de control personalizado puede reemplazar el panel de control predeterminado de BitLocker de Windows, denominado cifrado de unidad BitLocker. El panel de control de las opciones de cifrado de BitLocker, que se encuentra en sistema y seguridad en el panel de control de Windows, permite a los usuarios administrar su PIN y contraseñas, desbloquear unidades y ocultar la interfaz que permite a los administradores descifrar una unidad o reanudar o reanudar el cifrado de BitLocker.

**Para ocultar el cifrado de BitLocker predeterminado en el panel de control de Windows**

1.  Vaya a **configuración de usuario** mediante la consola de administración de directivas de grupo (GPMC), la administración de directivas de grupo avanzada (AGPM) o el editor de directivas de grupo local en el equipo de directivas de grupo de BitLocker.

2.  Haga clic en **directivas**, seleccione **plantillas administrativas**y, a continuación, haga clic en **Panel de control**.

3.  En el panel de **detalles** , haga doble clic en **Ocultar elementos especificados del panel de control**y, a continuación, seleccione **habilitado**.

4.  Haga clic en **Mostrar**, **haga clic en Agregar...** y, a continuación, escriba Microsoft. BitLockerDriveEncryption. Esta directiva oculta la herramienta de administración predeterminada de BitLocker de Windows del panel de control de Windows y permite al usuario abrir la herramienta de opciones de cifrado de MBAM BitLocker actualizada en el panel de control de Windows.

## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





