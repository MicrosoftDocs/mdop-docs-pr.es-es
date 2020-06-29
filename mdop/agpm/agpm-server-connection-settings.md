---
title: Configuración de conexión del servidor AGPM
description: Configuración de conexión del servidor AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813022"
---
# Configuración de conexión del servidor AGPM


Puede usar la configuración de la plantilla administrativa para administración de directivas de grupo (AGPM) avanzada para configurar conexiones de servidor AGPM de forma centralizada para los administradores de directiva de grupo a quienes se aplica un objeto de directiva de grupo (GPO) con esta configuración.

La siguiente configuración está disponible en Configuration\\Administrative de usuario de Templates\\Windows Components\\AGPM al editar un GPO. Si esta ruta de acceso no está visible, haga clic con el botón secundario en **plantillas administrativas**y agregue la plantilla AGPM. ADMX o AGPM. adm.

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
<td align="left"><p><strong>Servidor de AGPM (todos los dominios)</strong></p></td>
<td align="left"><p>Si se habilita, esta configuración configura de forma centralizada una conexión de servidor de AGPM para su uso por parte de todos los dominios y deshabilita la configuración de la <strong> </strong> pestaña servidor de AGPM para los administradores de la Directiva de grupo. Para varios servidores de AGPM, configure esta opción con un servidor predeterminado y, a continuación, configure la <strong> configuración del servidor </strong> de AGPM en la plantilla administrativa para invalidar este servidor para otros dominios.</p>
<p>Si se deshabilita o no se configura, cada administrador de directiva de grupo debe seleccionar el servidor de AGPM que se va a mostrar para cada dominio en la <strong> </strong> pestaña servidor de AGPM en AGPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Servidor de AGPM</strong></p></td>
<td align="left"><p>Si se habilita, esta configuración configura de forma centralizada varios servidores de AGPM específicos del dominio, lo que invalida la <strong> configuración del servidor de AGPM (todos los dominios) </strong> en la plantilla administrativa. Si su entorno requiere solo un servidor de AGPM, use solo el <strong> valor de servidor de AGPM (todos los dominios) </strong> en la plantilla administrativa.</p>
<p>Si se deshabilita o no se configura, la <strong> configuración del servidor de AGPM (todos los dominios) </strong> en la plantilla administrativa configura la conexión del servidor de AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Configuración de plantilla administrativa](administrative-template-settings.md)

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

 

 





