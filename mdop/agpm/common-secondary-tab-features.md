---
title: Funciones comunes de la pestaña Secundarias
description: Funciones comunes de la pestaña Secundarias
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819090"
---
# Funciones comunes de la pestaña Secundarias


Cada pestaña secundaria tiene dos secciones:**objetos de directiva de grupo** y **grupos y usuarios**.

## Sección objetos de directiva de grupo


En la sección **objetos de directiva de grupo** se muestra una lista filtrada de objetos de directiva de grupo (GPO) y se identifican las siguientes características de cada GPO:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica de GPO</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nombre del objeto de directiva de grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>PC (COMP)</strong></p></td>
<td align="left"><p>Versión generada automáticamente de la parte de configuración del equipo del GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Usuario</strong></p></td>
<td align="left"><p>Versión generada automáticamente de la parte de configuración de usuario del GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>El estado del GPO seleccionado:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>No controlado: </strong> AGPM.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Protegido: </strong> disponible para los editores autorizados que se desprotegen para su edición o para que los implemente un administrador de directiva de grupo.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Desprotegido: </strong> se está editando. No disponible para que otros editores las desprotejan hasta el editor que la ha desprotegido o un administrador de AGPM la protege.</p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong>Pendiente: </strong> se espera la aprobación de un administrador de directiva de grupo antes de crearse, controlarse, implementarse o eliminarse.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Eliminado: </strong> eliminado del archivo, pero que aún se puede restaurar.</p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong>Plantilla: </strong> versión estática de un objeto de directiva de grupo para usarlo como punto de partida al crear nuevos GPO.</p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong>Plantilla (valor predeterminado): de </strong> forma predeterminada, esta plantilla es el punto de partida que se usa al crear un nuevo GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Estado de GPO</strong></p></td>
<td align="left"><p>La configuración del equipo y la configuración del usuario se pueden administrar por separado. El estado del GPO indica qué partes del GPO están habilitadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Filtro WMI</strong></p></td>
<td align="left"><p>Mostrar todos los filtros WMI que se aplican a este GPO. Los filtros WMI se administran en el <strong> nodo filtros WMI </strong> del dominio en el árbol de consola de la GPMC.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificado</strong></p></td>
<td align="left"><p>Para un GPO controlado, la fecha más reciente en la que se protegió después de modificarlo o desprotegerlo para modificarlo. Para un GPO no controled, la fecha en la que se modificó por última vez.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Propietario</strong></p></td>
<td align="left"><p>El editor que protegió o el aprobador que implementó el GPO seleccionado.</p></td>
</tr>
</tbody>
</table>

 

## Sección grupos y usuarios


Cuando se selecciona un GPO, la sección **grupos y usuarios** muestra una lista de los grupos y usuarios con acceso a ese GPO. Los permisos y la herencia permitidos se muestran para cada grupo o usuario. Un administrador de AGPM puede configurar permisos con roles de AGPM estándar (editor, aprobador y revisor) o una combinación personalizada de permisos.

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
<td align="left"><p>Agregue una nueva entrada al descriptor de seguridad. Se puede Agregar a cualquier usuario o grupo de Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eliminar</strong></p></td>
<td align="left"><p>Quitar la entrada seleccionada de la lista de control de acceso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propiedades</strong></p></td>
<td align="left"><p>Mostrar las propiedades del objeto seleccionado. La página de propiedades es la misma que se muestra para un objeto en <strong> usuarios y equipos de Active Directory </strong> .</p></td>
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

-   [Pestaña Contenido](contents-tab.md)

 

 





