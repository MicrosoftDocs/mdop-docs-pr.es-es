---
title: Cómo compartir carpetas entre el host y el área de trabajo de MED-V
description: Cómo compartir carpetas entre el host y el área de trabajo de MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825751"
---
# Cómo compartir carpetas entre el host y el área de trabajo de MED-V


Puede compartir carpetas entre el host y el área de trabajo de MED-V. Las carpetas compartidas se pueden almacenar en lo siguiente:

-   Un equipo externo de la red

-   El equipo host

Los procedimientos siguientes muestran cómo compartir carpetas entre el host y el área de trabajo MED-V.

**Para compartir carpetas ubicadas en la red**

1.  Configure MED-V en el modo de escritorio completo.

2.  En administración de MED-V, en la pestaña red, haga clic en **usar una dirección IP distinta de la del host (puente)**.

3.  Haga lo siguiente en el equipo host:

    1.  En el panel de control, haga clic en **ver el estado y las tareas de red**y establecer **detección de red** en **activado**.

    2.  En el menú Inicio, haga clic con el botón derecho en **equipo**y haga clic en **conectar a unidad de red**.

    3.  En el cuadro de diálogo **asignar unidad de red** , en el campo **unidad** , seleccione una unidad.

        **Nota:**  Asegúrese de que no se esté usando la misma letra de unidad en los dos equipos.

         

    4.  Haz clic en **Examinar**.

    5.  En el cuadro de diálogo **Buscar carpeta** , busque la unidad compartida y haga clic en **Aceptar**.

    6.  Haz clic en **Finalizar**.

4.  Repita el paso 3 en el área de trabajo de MED-V. Apunte a la misma unidad que en el equipo host.

**Para compartir carpetas ubicadas en el host**

1.  Configure la carpeta que se va a compartir con los permisos adecuados.

2.  Desde el área de trabajo de MED-V, vaya a **mis sitios de red** y busque la carpeta compartida.

3.  En el área de trabajo de MED-V, busque la carpeta compartida.

**Nota:**  Asegúrese de que los equipos del área de trabajo de host y MED-V estén en el mismo dominio o grupo de trabajo.

 

 

 





