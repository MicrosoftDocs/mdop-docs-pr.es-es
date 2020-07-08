---
title: Uso de la consola de administración de cliente de App-V 5.0
description: Uso de la consola de administración de cliente de App-V 5.0
author: dansimp
ms.assetid: 36398307-57dd-40f3-9d4f-b09f44fd37c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8541e5bc59334b9074a3940dad7cdf0114205d4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813262"
---
# Uso de la consola de administración de cliente de App-V 5.0


Este tema proporciona información sobre cómo configurar y administrar el cliente de App-V 5,0.

## Modificar la configuración de cliente de App-V 5,0


El cliente de App-V 5,0 tiene una configuración asociada que se puede configurar para determinar cómo se ejecutará el cliente en su entorno. Puede administrar esta configuración en el equipo que ejecuta el cliente o mediante una directiva de grupo o PowerShell. Para obtener más información sobre cómo modificar el cliente mediante PowerShell o la configuración de la Directiva de grupo, consulte [Cómo modificar la configuración del cliente con PowerShell](how-to-modify-client-configuration-by-using-powershell.md).

## <a href="" id="the-app-v-5-0-client-management-console-"></a>La consola de administración de clientes de App-V 5,0


Puede obtener información sobre el cliente de App-V 5,0 o realizar tareas específicas mediante la consola de administración de clientes de App-V 5,0. Muchas de las tareas que puede realizar en la consola de administración de clientes también se pueden realizar con PowerShell. Los cmdlets de PowerShell asociados para cada acción también se muestran en la tabla siguiente. Para obtener más información sobre cómo usar PowerShell, consulte [Administración de App-V con PowerShell](administering-app-v-by-using-powershell.md).

La consola de administración de clientes contiene las siguientes pestañas principales descritas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tabulador</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Introducción</p></td>
<td align="left"><p>La <strong> ficha Información general </strong> contiene los siguientes elementos:</p>
<ul>
<li><p>Actualizar: Use el <strong> </strong> icono Actualizar para actualizar una aplicación virtualizada o recibir un nuevo paquete virtualizado.</p>
<p>La <strong> última actualización </strong> muestra la versión actual del paquete virtualizado.</p></li>
<li><p>Descargar todas las aplicaciones virtuales: use <strong> el </strong> icono de descarga para descargar todos los paquetes aprovisionados para el usuario actual.</p>
<p>(Cmdlet de PowerShell asociado: <strong> Mount-AppvClientPackage </strong> )</p>
<p></p></li>
<li><p>Trabajar sin conexión: Use este icono para deshabilitar todas las actualizaciones de aplicaciones virtuales automáticas y manuales.</p>
<p>(Cmdlet de PowerShell asociado: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicaciones virtuales</p></td>
<td align="left"><p>La <strong> pestaña de aplicaciones virtuales </strong> muestra todos los paquetes que se han publicado para el usuario. También puede hacer clic en un paquete específico y ver todas las aplicaciones que forman parte de ese paquete. Esto muestra información sobre los paquetes que se están usando y sobre cuánto de cada paquete se ha descargado en el equipo. También puedes iniciar y detener descargas de paquetes. Además, puede reparar el estado del usuario. Una reparación eliminará todos los datos de usuario asociados a un paquete.</p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupos de conexión de aplicaciones</p></td>
<td align="left"><p>La <strong> pestaña grupos de conexión de la aplicación </strong> muestra todos los grupos de conexión que están disponibles para el usuario actual. Haga clic en un grupo de conexiones específico para ver todos los paquetes que forman parte del grupo seleccionado. Esto muestra información acerca de los grupos de conexión que ya están en uso y qué parte del contenido del grupo de conexión se ha descargado en el equipo. Además, puede iniciar y detener descargas de grupos de conexiones. Puede usar esta sección para iniciar una reparación. Una reparación quitará todo el estado del usuario asociado a un grupo de conexiones.</p>
<p>(Cmdlets de <strong> PowerShell asociados: Descargar: Mount-AppvClientConnectionGroup </strong> . Repair- <strong> AppvClientConnectionGroup </strong> .)</p>
<p></p></td>
</tr>
</tbody>
</table>

 

[Cómo tener acceso a la consola de administración de cliente](how-to-access-the-client-management-console.md)

[Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-beta.md)






## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





