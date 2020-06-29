---
title: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
description: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824471"
---
# Cómo determinar el estado de cifrado de BitLocker de equipos perdidos


Use este procedimiento con el sitio web de administración y supervisión para determinar lo siguiente:

-   El último estado de cifrado de BitLocker conocido de equipos perdidos o robados

-   Si los volúmenes de un equipo perdido o robado estaban cifrados

Para completar esta tarea, necesita tener acceso al área **informes** del sitio web de administración y supervisión. Para obtener acceso a esta área, debe tener asignado el rol de usuarios de informes de MBAM. Es posible que haya dado a estos roles nombres diferentes al crearlos. Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Nota:**  El cumplimiento del dispositivo viene determinado por las directivas de BitLocker que ha implementado su empresa. Es posible que desee comprobar las directivas implementadas antes de intentar determinar el estado de cifrado de BitLocker de un dispositivo.

 

**Para determinar el último estado de cifrado de BitLocker conocido de equipos perdidos**

1.  Abra un explorador Web y vaya al **sitio web de administración y supervisión**.

2.  En el panel izquierdo, seleccione **informes** para abrir la página informes.

3.  Seleccione el **Informe de cumplimiento de equipos**.

4.  Use los campos de filtro en el panel derecho para restringir los resultados de la búsqueda y, a continuación, haga clic en **Buscar**. Los resultados se muestran en la consulta de búsqueda.

5.  Lleve a cabo la acción adecuada determinada por su directiva para los dispositivos perdidos.



## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





