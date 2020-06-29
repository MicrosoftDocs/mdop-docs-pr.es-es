---
title: Cómo configurar la configuración de web para un área de trabajo de MED-V
description: Cómo configurar la configuración de web para un área de trabajo de MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827070"
---
# Cómo configurar la configuración de web para un área de trabajo de MED-V


Los sitios web que solo se pueden mostrar en versiones anteriores de Internet Explorer y que no existen en el sistema operativo host se pueden ver en versiones anteriores de Internet Explorer en el área de trabajo de MED-V. El usuario no necesita abrir un explorador en el área de trabajo de MED-V para ver los sitios web especificados. El usuario puede abrir un explorador en el host y redireccionarlo automáticamente al área de trabajo de MED-V y viceversa.

Los procedimientos siguientes describen cómo se puede establecer una lista de reglas de navegación web para un área de trabajo de MED-V. Todos los sitios incluidos en las reglas se pueden examinar en el área de trabajo de MED-V o en el host, según lo defina el administrador. Todos los sitios no definidos en las reglas se examinan desde el entorno en el que se solicitaron. Sin embargo, también puede configurarlos como un grupo para poder examinarlos en el área de trabajo de MED-V o en el host.

**Nota**  
La configuración Web se aplica únicamente a Internet Explorer y no a otros exploradores.



Todas las opciones de configuración del Web se configuran en el módulo **Directiva** , en la pestaña **Web** .

## Cómo configurar las opciones de web para el área de trabajo de MED-V


**Para configurar la configuración web para el área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V que desea configurar.

2.  Seleccione la casilla **examinar la lista de direcciones URL definidas en la siguiente tabla** para redirigir al usuario a un explorador dentro del área de trabajo o al host MED-V, cuando el usuario se desplaza a una dirección URL que cumpla con las reglas web especificadas.

3.  Haga clic en una de las siguientes opciones:

    -   **En el área de trabajo**: redirigir a un explorador en el área de trabajo de MED-V.

    -   **En el host**: redirige a un explorador en el host.

4.  Seleccione la casilla **examinar todas las demás direcciones URL** para redirigir todas las direcciones URL excluidas de las reglas web al host o al área de trabajo de MED-V.

5.  Haga clic en una de las siguientes opciones:

    -   **En el área de trabajo**: redirija todas las demás direcciones URL a un explorador en el área de trabajo de MED-V.

    -   **En el host**: redirija el resto de las direcciones URL a un explorador del host.

6.  En el menú **Directiva** , seleccione **confirmar**.

## Cómo agregar una regla Web


**Para agregar una regla Web**

1.  Seleccione la casilla **examinar la lista de direcciones URL definidas en la siguiente tabla** para habilitar las reglas de exploración Web.

2.  Haz clic en **Agregar**.

    Se agrega una nueva regla Web.

3.  Configure las propiedades de la regla web como se describe en la tabla siguiente.

4.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades web del área de trabajo de MED-V**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propiedad</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tipo</p></td>
<td align="left"><ul>
<li><p><strong>Sufijo de dominio </strong> : acceso a cualquier dirección de host que termine con el sufijo especificado en la <strong> propiedad de valor </strong> y se establece de acuerdo con la opción establecida en <strong> exploración Web </strong> .</p></li>
<li><p><strong>Prefijo IP </strong> : acceso a cualquier dirección IP completa o parcial en el intervalo del prefijo especificado en <strong> la </strong> propiedad valor y se establece de acuerdo con la opción establecida en <strong> exploración Web </strong> .</p></li>
<li><p><strong>Todas las direcciones locales </strong> : acceso a todas las direcciones sin un &#39;. &#39; y se establece de acuerdo con la opción establecida en la <strong> exploración Web </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Valor</p></td>
<td align="left"><ul>
<li><p>Si <strong> </strong> se selecciona sufijo de dominio en <strong> la </strong> propiedad tipo, escriba un sufijo de dominio.</p>
<div class="alert">
<strong>Nota</strong><br/><ul>
<li><p>No escriba &quot; * &quot; antes del sufijo.</p></li>
<li><p>Los sufijos de dominio también admiten alias.</p></li>
</ul>
</div>
<div>

</div></li>
<li><p>Si el prefijo IP está seleccionado en la <strong> </strong> propiedad tipo, escriba una dirección IP completa o parcial.</p></li>
</ul></td>
</tr>
</tbody>
</table>



## Cómo eliminar una regla Web


**Para eliminar una regla Web**

1.  En el panel **Web** , seleccione la regla web que desea eliminar.

2.  Haga clic en **quitar**.

    Se elimina la regla Web.

## Temas relacionados


[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









