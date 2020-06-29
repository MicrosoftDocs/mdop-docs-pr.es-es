---
title: Cómo recuperar una unidad dañada
description: Cómo recuperar una unidad dañada
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822871"
---
# Cómo recuperar una unidad dañada


Para recuperar una unidad dañada protegida por BitLocker, un usuario del servicio de asistencia de supervisión y administración de Microsoft BitLocker (MBAM) necesitará crear un archivo de paquete de claves de recuperación. Este archivo de paquete puede copiarse en el equipo que contiene la unidad dañada y, a continuación, usarse para recuperar la unidad. Use el procedimiento siguiente para los pasos necesarios para hacerlo.

**Importante**  Para evitar una posible pérdida de datos, se recomienda encarecidamente que lea la ayuda "repair-BDE" y entienda claramente cómo usar el comando antes de completar las siguientes instrucciones.

 

**Para recuperar una unidad dañada**

1.  Para crear el paquete de claves de recuperación necesario para recuperar una unidad dañada, inicie un explorador Web y abra el sitio web de administración y supervisión de MBAM.

2.  Seleccione **recuperación de unidades** en el panel de navegación izquierdo. Escriba el nombre de dominio del usuario, el nombre de usuario, el motivo de desbloqueo de la unidad y el identificador de contraseña de recuperación del usuario.

    **Nota:**  Si es miembro del rol de administradores del servicio de asistencia, no es necesario que escriba el nombre de dominio o el nombre de usuario del usuario.

     

3.  Haz clic en **Enviar**. Se mostrará la clave de recuperación.

4.  Haga clic en **Guardar**y, a continuación, seleccione **paquete de claves de recuperación**. Se creará el paquete de claves de recuperación en el equipo.

5.  Copie el paquete de claves de recuperación en el equipo que tiene la unidad dañada.

6.  Abre un símbolo del sistema con privilegios elevados. Para ello, haga clic en **Inicio** y escriba `cmd` en el **cuadro Buscar programas y archivos**. Haga clic con el botón derecho en **cmd.exe** y seleccione **Ejecutar como administrador**.

7.  En el símbolo del sistema, escriba lo siguiente:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Nota:**  Reemplazar &lt; una unidad fija &gt; por una unidad de disco duro disponible que tenga un espacio libre igual o mayor que los datos de la unidad dañada. Los datos de la unidad dañada se recuperan y se mueven a la unidad de disco duro especificada.

     

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





