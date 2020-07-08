---
title: Permisos de acceso de usuario en el cliente de virtualización de aplicaciones
description: Permisos de acceso de usuario en el cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815120"
---
# Permisos de acceso de usuario en el cliente de virtualización de aplicaciones


En la pestaña **permisos** en el cuadro de diálogo **propiedades** , accesible haciendo clic con el botón secundario en el nodo de **virtualización de aplicaciones** en la consola de administración del cliente de virtualización de aplicaciones, los administradores pueden conceder permisos a los usuarios para que usen las distintas funciones de cliente.

**Nota:**  Antes de cambiar los permisos de los usuarios, asegúrese de que los cambios de permisos son coherentes con las pautas de la organización para conceder permisos de usuario.

 

En la tabla siguiente se enumeran y describen los permisos que se pueden conceder a los usuarios.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre del permiso</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Agregar aplicaciones</p></td>
<td align="left"><p>Registre nuevas aplicaciones pasando un nuevo archivo OSD al cliente mediante sfttray.exe, sftmime.exe o MMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cambiar el tamaño de la caché del sistema de archivos</p></td>
<td align="left"><p>Aumente el tamaño de la caché del sistema de archivos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cambiar la unidad del sistema de archivos</p></td>
<td align="left"><p>Seleccione otra letra de unidad preferida para el sistema de archivos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cambiar la configuración del registro</p></td>
<td align="left"><p>Cambie el nivel de registro o la ruta de acceso al registro del archivo de registro del cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cambiar archivos OSD</p></td>
<td align="left"><p>Modifique los archivos OSD para las aplicaciones registradas y paselos al cliente. Esto no afecta a la actualización de publicaciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Borrar la configuración de la aplicación</p></td>
<td align="left"><p>Elimine los tipos de archivo, los accesos directos y cualquier configuración del usuario actual.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eliminar aplicaciones</p></td>
<td align="left"><p>Quite todas las referencias a una aplicación del sistema de archivos y la caché OSD para todos los usuarios del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Importar aplicaciones a la caché</p></td>
<td align="left"><p>Cargue los datos de la aplicación directamente desde un archivo SFT especificado en la caché del sistema de archivos. Esto afecta a todos los usuarios.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cargar aplicaciones en la caché</p></td>
<td align="left"><p>Inicie una carga del archivo SFT de una aplicación desde el origen configurado, como un servidor de streaming de App-V. Esto carga la aplicación para todos los usuarios del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bloquear y desbloquear aplicaciones en la caché</p></td>
<td align="left"><p>Impedir o permitir que se descarguen aplicaciones de la memoria caché del sistema de archivos. Esto afecta a todos los usuarios del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrar asociaciones de tipo de archivo</p></td>
<td align="left"><p>Agregar, modificar o eliminar asociaciones de tipo de archivo solo para el usuario actual.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administrar la configuración de actualización de publicaciones</p></td>
<td align="left"><p>Cambie la configuración que controla la temporización de las actualizaciones de publicación para todos los usuarios del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrar servidores de publicación</p></td>
<td align="left"><p>Agregue, modifique o elimine servidores de publicación para todos los usuarios del equipo. Este permiso incluye implícitamente permisos para administrar la configuración de actualización de publicaciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar accesos directos</p></td>
<td align="left"><p>Crear nuevos accesos directos a las aplicaciones registradas. El usuario también debe tener permiso para crear archivos en el sistema de archivos local.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reparar aplicaciones</p></td>
<td align="left"><p>Quitar configuraciones específicas de la aplicación para el usuario actual sin eliminar accesos directos ni asociaciones de tipos de archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Iniciar una actualización de publicación</p></td>
<td align="left"><p>Iniciar una actualización de publicación no programada para el usuario actual.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Activar o desactivar el modo sin conexión</p></td>
<td align="left"><p>Cambie el cliente completo del modo en línea a sin conexión para todos los usuarios.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descargar aplicaciones de la caché</p></td>
<td align="left"><p>Borrar los datos de la aplicación de la caché del sistema de archivos para todos los usuarios sin quitar la configuración, los accesos directos ni las asociaciones de tipos de archivo específicos del usuario.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ver todas las aplicaciones</p></td>
<td align="left"><p>Permite al usuario ver las aplicaciones virtuales de todos los usuarios registrados en el equipo.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Cómo cambiar los permisos de acceso de usuario](how-to-change-user-access-permissions.md)

 

 





