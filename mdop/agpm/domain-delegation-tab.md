---
title: Pestaña Delegación de dominio
description: Pestaña Delegación de dominio
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818630"
---
# Pestaña Delegación de dominio


La pestaña **delegación de dominios** del panel control de **cambios** proporciona una lista de administradores de directivas de grupo que tienen acceso en el nivel de dominio al archivo y indican las funciones de cada uno de ellos. Además, esta pestaña permite a los administradores de AGPM (control total) configurar permisos de nivel de dominio para editores, aprobadores, revisores y otros administradores de AGPM. Hay dos secciones en la pestaña **delegación de dominios** : configuración de notificaciones de correo electrónico y delegación basada en roles para la administración avanzada de directivas de grupo (AGPM) en el nivel de dominio.

## Configuración de la notificación de correo electrónico


En la sección notificación de correo electrónico de esta pestaña se identifican los aprobadores que recibirán una notificación cuando haya operaciones pendientes en AGPM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Desde</strong></p></td>
<td align="left"><p>Alias de AGPM desde el que se envía la notificación a los aprobadores. En un entorno con varios dominios, puede ser el mismo alias en todo el entorno o un alias diferente para cada dominio.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Para</strong></p></td>
<td align="left"><p>Una lista delimitada por comas de las direcciones de correo electrónico de los aprobadores a las que se va a enviar la notificación</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Servidor SMTP</strong></p></td>
<td align="left"><p>El nombre del servidor de correo electrónico, como mail.contoso.com</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nombre de usuario</strong></p></td>
<td align="left"><p>Un usuario con acceso al servidor SMTP</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Contraseña</strong></p></td>
<td align="left"><p>Contraseña del usuario para la autenticación en el servidor SMTP</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Confirmar contraseña</strong></p></td>
<td align="left"><p>Confirmar la contraseña del usuario</p></td>
</tr>
</tbody>
</table>

 

## Delegación basada en roles de nivel de dominio


La sección delegación basada en roles de esta pestaña muestra y permite a un administrador de AGPM delegar permisos permitidos, denegados y heredados para cada grupo y usuario del dominio con acceso al archivo. Un administrador de AGPM puede configurar permisos para todo el dominio con roles de AGPM estándar (editor, aprobador, revisor y administrador de AGPM) o una combinación personalizada de permisos para cada administrador de directiva de grupo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Botón</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Agregar</strong></p></td>
<td align="left"><p>Agregue una nueva entrada al descriptor de seguridad. Todos los usuarios o grupos de Active Directory se pueden agregar como administradores de directiva de grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eliminar</strong></p></td>
<td align="left"><p>Quitar los administradores de directivas de grupo seleccionados de la lista de control de acceso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propiedades</strong></p></td>
<td align="left"><p>Mostrar las propiedades de los administradores de directivas de grupo seleccionados. La página de propiedades es la misma que se muestra para un objeto en <strong> usuarios y equipos de Active Directory </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avanzado</strong></p></td>
<td align="left"><p>Abra el <strong> Editor de la lista de control de acceso </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Consideraciones adicionales

-   Para obtener información sobre los roles y los permisos relacionados con tareas específicas, consulte las tareas de realizar tareas de [Administrador de AGPM](performing-agpm-administrator-tasks.md), [realizar tareas de editor](performing-editor-tasks.md), [realizar tareas de aprobador](performing-approver-tasks.md)y [realizar tareas de revisor](performing-reviewer-tasks.md).

### Referencias adicionales

-   [Interfaz de usuario: Administración avanzada de directivas de grupo](user-interface-advanced-group-policy-management.md)

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

 

 





