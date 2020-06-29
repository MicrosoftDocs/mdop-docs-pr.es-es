---
title: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
description: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824291"
---
# Cómo determinar el estado de cifrado de BitLocker de equipos perdidos


Administración y supervisión de Microsoft BitLocker (MBAM) le permite determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados. Use el procedimiento siguiente para determinar si los volúmenes se han cifrado en equipos que ya no están en su poder.

**Determinar el último estado de cifrado de BitLocker conocido de un equipo**

1.  Abra el sitio web de MBAM.

    **Nota:**  La dirección predeterminada del sitio web de MBAM es http://* &lt; NombreDeEquipo &gt; *. Use el nombre completo del servidor para que los resultados de la navegación sean más rápidos.

     

2.  Seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de cumplimiento de equipos**.

3.  Use los campos de filtro en el panel de la derecha para restringir los resultados de búsqueda y, a continuación, haga clic en **Buscar**. Los resultados se mostrarán debajo de la consulta de búsqueda.

4.  Lleve a cabo la acción adecuada determinada por la Directiva para los dispositivos perdidos.

    **Nota:**  El cumplimiento del dispositivo viene determinado por las directivas de BitLocker implementadas. Debe comprobar estas directivas implementadas al intentar determinar el estado de cifrado de BitLocker de un dispositivo.

     

## Temas relacionados


[Realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





