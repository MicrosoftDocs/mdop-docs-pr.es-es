---
title: Cómo recuperar una unidad dañada
description: Cómo recuperar una unidad dañada
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812943"
---
# Cómo recuperar una unidad dañada


Para recuperar una unidad dañada que ha sido protegida por BitLocker, un usuario del servicio de asistencia de supervisión y administración de Microsoft BitLocker (MBAM) debe crear un archivo de paquete de claves de recuperación. Este archivo de paquete puede copiarse en el equipo que contiene la unidad dañada y, a continuación, usarse para recuperar la unidad. Para ello, use el procedimiento siguiente.

**Para recuperar una unidad dañada**

1.  Abra el sitio web de administración de MBAM.

2.  Seleccione **recuperación de unidades** en el panel de navegación. Escriba el nombre de dominio y el nombre de usuario del usuario, el motivo por el que se desbloqueó la unidad y el identificador de contraseña de recuperación del usuario.

    **Nota:**  Si es miembro del rol de administradores del servicio de asistencia, no es necesario que escriba el nombre de dominio o el nombre de usuario del usuario.

     

3.  Haz clic en **Enviar**. Se mostrará la clave de recuperación.

4.  Haga clic en **Guardar**y, a continuación, seleccione **paquete de claves de recuperación**. Se creará el paquete de claves de recuperación en el equipo.

5.  Copie el paquete de claves de recuperación en el equipo que tiene la unidad dañada.

6.  Abre un símbolo del sistema con privilegios elevados. Para ello, haga clic en **Inicio** y escriba `cmd` en el cuadro **Buscar programas y archivos** . En la lista de resultados de la búsqueda, haga clic con el botón derecho en **cmd.exe** y seleccione **Ejecutar como administrador**.

7.  En el símbolo del sistema, escriba lo siguiente:

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **Nota:**  Para la &lt; unidad fija &gt; en el comando, especifique un dispositivo de almacenamiento disponible que tenga espacio libre igual o mayor que los datos de la unidad dañada. Los datos de la unidad dañada se recuperan y se mueven a la unidad fija especificada.

     

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





