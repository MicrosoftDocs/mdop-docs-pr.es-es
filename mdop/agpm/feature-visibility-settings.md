---
title: Configuración de visibilidad de funciones
description: Configuración de visibilidad de funciones
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820810"
---
# Configuración de visibilidad de funciones


La configuración de la plantilla administrativa de administración de directivas de grupo (AGPM) avanzada le permite configurar de forma centralizada la visibilidad del nodo **control de cambios** y la pestaña **historial** para los administradores de directiva de grupo a los que se aplica un objeto de directiva de grupo (GPO) con esta configuración.

La siguiente configuración está disponible en la consola de administración de Configuration\\Administrative Templates\\Windows de usuario de Components\\Microsoft \ \ restricciones/permitidos Snap-ins\\Extension en el **Editor de objetos de directiva de grupo** al editar un GPO en la consola de administración de directivas de grupo (GPMC). Si esta ruta de acceso no está visible, haga clic con el botón secundario en **plantillas administrativas**y agregue la plantilla AGPM. ADMX o AGPM. adm.

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
<td align="left"><p><strong>Control de cambios de AGPM</strong></p></td>
<td align="left"><p>Si se habilita o no se configura, el <strong> </strong> nodo de control de cambios estará visible en la GPMC.</p>
<p>Si se deshabilita, el <strong> </strong> nodo de control de cambios no es visible en la GPMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Extensión de vínculo de AGPM</strong></p></td>
<td align="left"><p>Si se habilita o no se configura <strong> , </strong> aparece una ficha historial en la GPMC para cada GPO vinculado.</p>
<p>Si está deshabilitada, la <strong> </strong> ficha historial no está visible para los GPO vinculados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Extensión de GPO de AGPM</strong></p></td>
<td align="left"><p>Si se habilita o no se configura <strong> , </strong> aparece una ficha historial en la GPMC para cada GPO.</p>
<p>Si se deshabilita, <strong> la </strong> ficha historial no está visible para los GPO.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Configuración de plantilla administrativa](administrative-template-settings.md)

 

 





