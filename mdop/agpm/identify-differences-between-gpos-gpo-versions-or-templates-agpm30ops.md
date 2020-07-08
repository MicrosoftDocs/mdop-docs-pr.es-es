---
title: Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas
description: Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas
author: dansimp
ms.assetid: e391fa91-3956-4150-9d43-900cfc88d543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88c37a3723c31fb110e731084237a8d89350a4ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820771"
---
# Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas


Puede generar informes de diferencias basados en HTML o en XML para analizar las diferencias entre los objetos de directiva de grupo (GPO), las plantillas o las distintas versiones de un GPO.

Para completar este procedimiento, se requiere una cuenta de usuario con el rol de revisor, editor, aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

## Identificar las diferencias entre objetos de directiva de grupo, versiones de GPO o plantillas


-   [Entre dos GPO o plantillas](#bkmk-two-gpos)

-   [Entre un GPO y una plantilla](#bkmk-gpo-and-template)

-   [Entre dos versiones de un objeto de directiva de grupo](#bkmk-two-versions)

-   [Entre una versión de GPO y una plantilla](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**Para identificar las diferencias entre dos GPO o plantillas**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).

3.  Seleccione los dos GPO o las plantillas.

4.  Haga clic con el botón secundario en uno de los GPO o plantillas, haga clic en **diferencias**y, a continuación, haga clic en informe **html** o **Informe XML** para mostrar un informe de diferencias que resuma la configuración de los objetos de directiva de grupo o de las plantillas.

### <a href="" id="bkmk-gpo-and-template"></a>

**Para identificar las diferencias entre un objeto de directiva de grupo y una plantilla**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).

3.  Haga clic con el botón secundario en el GPO, haga clic en **diferencias**y luego en **plantilla**.

4.  Seleccione la plantilla y el tipo de informe y, a continuación, haga clic en **Aceptar** para mostrar un informe de diferencias que resuma la configuración del objeto de directiva de grupo y de la plantilla.

### <a href="" id="bkmk-two-versions"></a>

**Para identificar las diferencias entre dos versiones de un objeto de directiva de grupo**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).

3.  Haga doble clic en el GPO para mostrar su historial y, a continuación, resalte las versiones que se van a comparar.

4.  Haga clic con el botón secundario en una de las versiones, haga clic en **diferencias**y, a continuación, haga clic en informe **html** o **Informe XML** para mostrar un informe de diferencias que resuma la configuración de los objetos de directiva de grupo.

### <a href="" id="bkmk-gpo-version-and-template"></a>

**Para identificar las diferencias entre una versión de GPO y una plantilla**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).

3.  Haga doble clic en el GPO para mostrar su historial.

4.  Haga clic con el botón secundario en la versión de interés del GPO, seleccione **diferencias**y, a continuación, haga clic en **plantilla**.

5.  Seleccione la plantilla y el tipo de informe y, a continuación, haga clic en **Aceptar** para mostrar un informe de diferencias que resume la configuración de la versión y la plantilla del objeto de directiva de grupo.

## Clave para los informes de diferencias


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Símbolo</th>
<th align="left">Significado</th>
<th align="left">Color</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>El elemento tiene una configuración idéntica en ambos GPO</p></td>
<td align="left"><p>Varía según el nivel</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>El elemento se encuentra en los dos GPO, pero con la configuración cambiada</p></td>
<td align="left"><p>Azulado</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>El elemento solo existe en el primer GPO</p></td>
<td align="left"><p>Rojo</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>El elemento solo existe en el segundo GPO</p></td>
<td align="left"><p>Verde</p></td>
</tr>
</tbody>
</table>

 

-   En el caso de los elementos con la configuración cambiada, la configuración cambiada se identifica cuando se expande el elemento. El valor del atributo de cada objeto de directiva de grupo se muestra en el mismo orden en que se muestran en el informe.

-   Algunos cambios en la configuración pueden hacer que un elemento se notifique como dos elementos diferentes (uno presente solo en el primer GPO, uno solo presente en el segundo) en lugar de como un elemento que ha cambiado.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el GPO. Además, para mostrar la lista de GPO, debe tener permiso de **contenido de lista** para el dominio.

### Referencias adicionales

-   [Realización de tareas de revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





