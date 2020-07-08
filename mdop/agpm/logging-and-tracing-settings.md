---
title: Registro y seguimiento de configuración
description: Registro y seguimiento de configuración
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820590"
---
# Registro y seguimiento de configuración


La configuración de la plantilla administrativa de administración de directivas de grupo (AGPM) avanzada le permite configurar de forma centralizada las opciones de registro y seguimiento para clientes y servidores AGPM a los que se aplica un objeto de directiva de grupo (GPO) con esta configuración.

La siguiente opción está disponible en equipo Configuration\\Administrative Templates\\Windows Components\\AGPM en el **Editor de objetos de directiva de grupo** al editar un GPO en la consola de administración de directivas de grupo (GPMC). Si esta ruta de acceso no está visible, haga clic con el botón secundario en **plantillas administrativas**y agregue la plantilla AGPM. ADMX o AGPM. adm.

**Ubicaciones del archivo de seguimiento**:

-   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Servidor:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registro de AGPM</strong></p></td>
<td align="left"><p>Si se habilita, este valor de configuración configura si el seguimiento está activado y el nivel de detalle. Esta configuración afecta tanto a los componentes del cliente como del servidor de AGPM.</p>
<p>Si se deshabilita o no se configura, esta configuración no surte efecto.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Configuración de plantilla administrativa](administrative-template-settings.md)

 

 





