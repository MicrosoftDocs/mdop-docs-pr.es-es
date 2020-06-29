---
title: Cómo generar informes
description: Cómo generar informes
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826991"
---
# Cómo generar informes


Los administradores pueden crear los siguientes tipos de informes en MED-V:

-   [Estado](#bkmk-generatingastatusreport): Use el informe de estado para revisar el estado actual de todos los usuarios activos y todas las áreas de trabajo de MED-V de cada usuario en función de un período de tiempo definido. Esto incluye la visualización de equipos que están conectados al servidor o, si actualmente no están conectados, la fecha y la hora en que se conectó por última vez al servidor, el estado de cada equipo y otra información relevante.

-   [Registro de actividades](#bkmk-generatinganactivitylogreport): Use este informe para revisar los eventos que se han originado desde un determinado host o usuario en un intervalo de fechas definido.

-   [Registro de errores](#bkmk-generatinganerrorlogreport): Use este informe para ver los errores originados en un determinado host o usuario de un intervalo de fechas definido.

Los resultados del informe se pueden ordenar por cualquier columna haciendo clic en el nombre de columna correspondiente.

Los resultados del informe se pueden agrupar arrastrando un encabezado de columna hasta la parte superior del informe. Arrastre los encabezados de varias columnas para agrupar una columna después de otra.

## <a href="" id="bkmk-generatingastatusreport"></a>Cómo generar un informe de estado


**Para generar un informe de estado**

1.  Haga clic en el botón Administración de **informes** .

2.  En el módulo **informes** , en el menú **tipos de informe** , seleccione **Estado**y haga clic en **generar**.

    Aparece el cuadro de diálogo parámetros de informe.

3.  En el cuadro de diálogo **parámetros de informe** , en el campo **número de días** , escriba un número o use las flechas para seleccionar el número de días que desea incluir en el informe de estado y haga clic en **Aceptar**.

    Se genera un informe de estado. Los parámetros del informe se definen en la tabla siguiente.

**Propiedades del área de trabajo cliente MED-V**

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
<td align="left"><p>Tiempo</p></td>
<td align="left"><p>La fecha y hora en que se produjo el evento.</p>
<div class="alert">
<strong>Nota</strong><br/><p>De forma predeterminada, los eventos se muestran en orden de fecha descendente. Sin embargo, se puede modificar haciendo clic en la columna hora de recepción.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de usuario</p></td>
<td align="left"><p>El usuario que ha iniciado el evento.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si el evento se produjo antes de que un usuario iniciara sesión, el nombre de usuario es sistema.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de host</p></td>
<td align="left"><p>El nombre del equipo host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre del área de trabajo</p></td>
<td align="left"><p>El nombre del área de trabajo de MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre del equipo del área de trabajo</p></td>
<td align="left"><p>El nombre del equipo en el que se está ejecutando el área de trabajo de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Online</p></td>
<td align="left"><p>El estado actual del equipo cliente:</p>
<ul>
<li><p><strong>Detenga</strong></p></li>
<li><p><strong>Comenzado en &lt; la fecha y la hora en que se inició el área de trabajo&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Versión de cliente</p></td>
<td align="left"><p>El número de versión del cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión de Directiva</p></td>
<td align="left"><p>La versión de la Directiva que el área de trabajo de MED-V está usando actualmente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de imagen</p></td>
<td align="left"><p>El nombre de la imagen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión de la imagen</p></td>
<td align="left"><p>La versión de la imagen que el área de trabajo de MED-V está usando actualmente.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La versión del área de trabajo MED-V puede ser desconocida si aún no se ha descargado en un equipo.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a>Cómo generar un informe de registro de actividades


**Para generar un informe de registro de actividades**

1.  Haga clic en el botón Administración de **informes** .

    Aparece el módulo informes.

2.  En el módulo **informes** , en el menú **tipos de informe** , seleccione Registro de **actividades**y haga clic en **generar**.

3.  En el cuadro de diálogo **parámetros de informe** , configure uno o varios de los siguientes parámetros:

    -   **Número de días**: el número de días que se muestran en el informe.

    -   **Nombre de usuario contiene**: cualquier evento en el que el nombre de usuario contenga el texto escrito se incluye en el informe.

    -   **Nombre de host contiene**: cualquier evento en el que el nombre de host contenga el texto escrito se incluye en el informe.

4.  Haga clic en **Aceptar**.

    Se genera un informe con los eventos y las fechas seleccionadas. Los parámetros del informe se definen en la tabla siguiente.

**Propiedades del informe de registro de actividades**

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
<td align="left"><p>Id. de evento</p></td>
<td align="left"><p>IDENTIFICADOR de evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gravedad</p></td>
<td align="left"><p><strong>Información, error, ADVERTENCIA</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Categoría</p></td>
<td align="left"><p>El módulo al que hace referencia el informe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción del evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Hora de recepción</p></td>
<td align="left"><p>La fecha y hora en que se recibió el evento en el servidor.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si el cliente está trabajando sin conexión, el servidor recibe los informes cuando el cliente está conectado.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>De forma predeterminada, los eventos se muestran en orden de fecha descendente. Sin embargo, se puede modificar haciendo clic en la <strong> columna hora de recepción </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Hora del cliente</p></td>
<td align="left"><p>La fecha y hora en que se produjo el evento según el reloj del cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de host</p></td>
<td align="left"><p>El nombre del equipo host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de usuario</p></td>
<td align="left"><p>El usuario que ha iniciado el evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre del área de trabajo</p></td>
<td align="left"><p>El nombre del área de trabajo de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre del equipo del área de trabajo</p></td>
<td align="left"><p>El nombre del equipo en el que se está ejecutando el área de trabajo de MED-V.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a>Cómo generar un informe de registro de errores


**Para generar un informe de registro de errores**

1.  Haga clic en el botón Administración de **informes** .

2.  En el módulo **informes** , en el menú **tipos de informe** , seleccione Registro de **errores**y haga clic en **generar**.

3.  En el cuadro de diálogo **parámetros de informe** , configure uno o varios de los siguientes parámetros:

    -   **Número de días**: el número de días que se muestran en el informe.

    -   **Nombre de usuario contiene**: cualquier evento en el que el nombre de usuario contenga el texto escrito se incluye en el informe.

    -   **Nombre de host contiene**: cualquier evento en el que el nombre de host contenga el texto escrito se incluye en el informe.

4.  Haga clic en **Aceptar**.

    Se genera un informe con los eventos y las fechas seleccionadas. Los parámetros del informe se definen en la tabla siguiente.

**Propiedades del informe de registro de errores**

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
<td align="left"><p>Id. de evento</p></td>
<td align="left"><p>IDENTIFICADOR de evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Categoría</p></td>
<td align="left"><p>El módulo al que hace referencia el informe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción del evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hora de recepción</p></td>
<td align="left"><p>La fecha y hora en que se recibió el evento en el servidor.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si el cliente está trabajando sin conexión, el servidor recibe los informes cuando el cliente está conectado.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>De forma predeterminada, los eventos se muestran en orden de fecha descendente. Sin embargo, se puede modificar haciendo clic en la <strong> columna hora de recepción </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Hora del cliente</p></td>
<td align="left"><p>La fecha y hora en que se produjo el evento según el reloj del cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de host</p></td>
<td align="left"><p>El nombre del equipo host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de usuario</p></td>
<td align="left"><p>El usuario que ha iniciado el evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre del área de trabajo</p></td>
<td align="left"><p>El nombre del área de trabajo de MED-V.</p></td>
</tr>
</tbody>
</table>











