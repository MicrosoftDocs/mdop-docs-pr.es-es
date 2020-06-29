---
title: Visualización de informes MBAM 2.5 para la topología de integración de Administrador de configuración
description: Visualización de informes MBAM 2.5 para la topología de integración de Administrador de configuración
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824041"
---
# Visualización de informes MBAM 2.5 para la topología de integración de Administrador de configuración


En este tema se describen los informes que están disponibles al configurar administración y supervisión de Microsoft BitLocker (MBAM) con la topología de integración de Configuration Manager. Los informes muestran el cumplimiento de BitLocker para la empresa y para equipos y dispositivos individuales que administra MBAM. Los informes proporcionan información tabular y gráficos, y tienen filtros que le permiten ver datos desde distintas perspectivas.

En la topología de integración de Configuration Manager, puede ver los informes desde Configuration Manager en lugar de desde el sitio web de administración y supervisión, con la excepción del **Informe de auditoría de recuperación**, que puede seguir visualizando desde el sitio web de administración y supervisión.

Para obtener información sobre los informes de MBAM para la topología independiente, vea [ver informes de MBAM 2,5 para la topología independiente](viewing-mbam-25-reports-for-the-stand-alone-topology.md).

## Acceso a informes en Configuration Manager


Para acceder a la característica informes de Configuration Manager:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de Configuration Manager</th>
<th align="left">Cómo ver los informes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SystemCenter2012 ConfigurationManager</p></td>
<td align="left"><ol>
<li><p>En el panel de la izquierda, seleccione el <strong> </strong> área de trabajo supervisión.</p></li>
<li><p>En el árbol, expanda <strong> información general informes de informes </strong> &gt; <strong> </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel derecho.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager2007</p></td>
<td align="left"><ol>
<li><p>En el panel izquierdo, expanda Administración de equipos Reporting Reporting <strong> </strong> &gt; <strong> </strong> &gt; <strong> Services </strong> &gt; <strong> &lt; nombres de servidor &gt; </strong> &gt; <strong> carpetas </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel derecho.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## Descripción de los informes en Configuration Manager


Existen algunas diferencias menores en los informes para la topología de integración de Configuration Manager y la topología independiente. En las siguientes secciones se describen los datos de los informes de MBAM para la topología de integración de Configuration Manager:

-   [Panel de cumplimiento de BitLocker Enterprise](#bkmk-dashboard)

-   [Detalles de la compatibilidad con BitLocker Enterprise](#bkmk-compliancedetails)

-   [Resumen de cumplimiento de BitLocker Enterprise](#bkmk-compliancesummary)

-   [Informe de cumplimiento de equipos con BitLocker](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a>Panel de cumplimiento de BitLocker Enterprise

El panel de cumplimiento de BitLocker Enterprise proporciona los siguientes gráficos, que muestran el estado de cumplimiento de BitLocker en toda la empresa:

-   Distribución del estado de cumplimiento

-   Distribución de errores no conformes

-   Distribución del estado de cumplimiento por tipo de unidad

**Distribución del estado de cumplimiento**

Este gráfico circular muestra el estado de cumplimiento de los equipos de la empresa. También muestra el porcentaje de equipos, comparado con el número total de equipos de la colección seleccionada, que tiene ese estado de cumplimiento. También se muestra el número real de equipos con cada Estado. El gráfico circular muestra los siguientes Estados de cumplimiento:

-   Reglamenta

-   No conforme

-   Exención de usuarios

-   Exención de usuarios temporales

-   Directiva no exigida

-   Reconoce. Estos equipos han notificado un error de estado o forman parte de la colección, pero nunca han informado de su estado de cumplimiento. La falta de estado de cumplimiento puede producirse si el equipo se desconecta de la organización.

**Distribución de errores no conformes**

Este gráfico circular muestra las categorías de equipos de la empresa que no son compatibles con la Directiva de cifrado de unidad BitLocker y muestra el número de equipos de cada categoría. Cada categoría se calcula a partir del número total de equipos no compatibles de la colección.

-   Usuario pospuesto

-   No se puede encontrar el TPM compatible

-   La partición del sistema no está disponible o es lo suficientemente grande

-   Conflicto de directivas

-   Esperando el aprovisionamiento automático de TPM

-   Se ha producido un error desconocido

-   No hay información. Estos equipos no tienen el cliente MBAM instalado o tienen el cliente de MBAM instalado pero no activado (por ejemplo, el servicio no funciona).

**Distribución del estado de cumplimiento por tipo de unidad**

Este gráfico de barras muestra el estado de compatibilidad actual de BitLocker por tipo de unidad. Los Estados son **conformes** y **no conformes**. Se muestran barras para las unidades de datos fijas y las unidades del sistema operativo. Se incluyen los equipos que no tienen una unidad de datos fija y solo muestran un valor en la barra de **unidades del sistema operativo** . El gráfico no incluye los usuarios a los que se les ha concedido una exención de la Directiva de cifrado de unidad BitLocker o de la categoría sin Directiva.

### <a href="" id="bkmk-compliancedetails"></a>Detalles de la compatibilidad con BitLocker Enterprise

Este informe muestra información sobre la compatibilidad general de BitLocker en toda la empresa para la colección de equipos que se destina para uso de BitLocker.

**Detalles de cumplimiento de BitLocker Enterprise (campos)**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de columna</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Equipos administrados</p></td>
<td align="left"><p>Número de equipos que administra MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De cumplimiento</p></td>
<td align="left"><p>Porcentaje de equipos compatibles de la empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De no conformidad</p></td>
<td align="left"><p>Porcentaje de equipos no conformes de la empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De cumplimiento desconocido</p></td>
<td align="left"><p>Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De exención</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De no exento</p></td>
<td align="left"><p>Porcentaje de equipos no exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>Porcentaje de equipos compatibles de la empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>No conforme</p></td>
<td align="left"><p>Porcentaje de equipos no conformes de la empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cumplimiento desconocido</p></td>
<td align="left"><p>Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Queda</p></td>
<td align="left"><p>Número total de equipos que están exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No exento</p></td>
<td align="left"><p>Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Estados de detalles de cumplimiento de BitLocker Enterprise**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estado de cumplimiento</th>
<th align="left">Franquicia</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>No conforme</p></td>
<td align="left"><p>No exentas</p></td>
<td align="left"><p>El equipo no cumple con los requisitos de la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>No exentas</p></td>
<td align="left"><p>El equipo cumple con los requisitos de la Directiva especificada.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a>Resumen de cumplimiento de BitLocker Enterprise

Use este tipo de informe para mostrar información sobre el cumplimiento general de BitLocker en toda la empresa y para mostrar la compatibilidad de equipos individuales que se encuentran en la colección de equipos de destino para el uso de BitLocker.

**Campos Resumen de la compatibilidad de BitLocker Enterprise**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de columna</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Equipos administrados</p></td>
<td align="left"><p>Número de equipos que administra MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De cumplimiento</p></td>
<td align="left"><p>Porcentaje de equipos compatibles de la empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De no conformidad</p></td>
<td align="left"><p>Porcentaje de equipos no conformes de la empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De cumplimiento desconocido</p></td>
<td align="left"><p>Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De exención</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De no exento</p></td>
<td align="left"><p>Porcentaje de equipos no exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>Porcentaje de equipos compatibles de la empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>No conforme</p></td>
<td align="left"><p>Porcentaje de equipos no conformes de la empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cumplimiento desconocido</p></td>
<td align="left"><p>Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Queda</p></td>
<td align="left"><p>Número total de equipos que están exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No exento</p></td>
<td align="left"><p>Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Resumen de la compatibilidad de BitLocker Enterprise**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de columna</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre del equipo</p></td>
<td align="left"><p>Nombre de equipo DNS especificado por el usuario administrado por MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de dominio</p></td>
<td align="left"><p>Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>Estado general de cumplimiento del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes. Observe que el estado de cumplimiento por unidad (consulte la tabla que sigue) puede indicar diferentes Estados de cumplimiento. Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Estado que indica si el usuario está exento o no exento de la Directiva de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de dispositivos</p></td>
<td align="left"><p>Usuario del dispositivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado sobre el estado de cumplimiento del equipo conforme a la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto se puede configurar a través de la configuración de directiva de grupo.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a>Informe de cumplimiento de equipos con BitLocker

Use este tipo de informe para recopilar información específica de un equipo. El informe de cumplimiento de equipos con BitLocker proporciona información de cifrado detallada sobre cada unidad de un equipo (sistema operativo y unidades de datos fijas). También proporciona una indicación de la Directiva que se aplica a cada tipo de unidad en el equipo. Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.

**Nota:**  El estado del cifrado de volumen de datos extraíbles no se muestra en este informe.

 

**Informe de cumplimiento de equipos con BitLocker: campos detalles del equipo**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de columna</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre del equipo</p></td>
<td align="left"><p>Nombre de equipo DNS especificado por el usuario administrado por MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de dominio</p></td>
<td align="left"><p>Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de equipo</p></td>
<td align="left"><p>Tipo de equipo. Los tipos válidos son no portátiles y portátiles.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operativo</p></td>
<td align="left"><p>Tipo de sistema operativo encontrado en el equipo cliente administrado MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cumplimiento general</p></td>
<td align="left"><p>Estado general de cumplimiento del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes. Observe que el estado de cumplimiento por unidad (consulte la tabla que sigue) puede indicar diferentes Estados de cumplimiento. Sin embargo, este campo representa ese estado de cumplimiento conforme a la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cumplimiento de sistemas operativos</p></td>
<td align="left"><p>Estado de cumplimiento del sistema operativo administrado por MBAM. Los Estados válidos son conformes y no conformes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cumplimiento de unidades de datos fijas</p></td>
<td align="left"><p>Estado de cumplimiento de la unidad de datos fijas administrada por MBAM. Los Estados válidos son conformes y no conformes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fecha de la última actualización</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto se puede configurar a través de la configuración de directiva de grupo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Estado que indica si el usuario está exento o no exento de la Directiva de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuario excluido</p></td>
<td align="left"><p>Usuario que está exento de la Directiva de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fecha de exención</p></td>
<td align="left"><p>Fecha en la que se concedió la exención.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado sobre el estado de cumplimiento del equipo conforme a la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intensidad de cifrado de Directiva</p></td>
<td align="left"><p>Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM (por ejemplo, 128 bits con difusor).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Directiva: unidad de sistema operativo</p></td>
<td align="left"><p>Indica si es necesario el cifrado para el sistema operativo y el tipo de protector adecuado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Directiva: unidad de datos fija</p></td>
<td align="left"><p>Indica si el cifrado es necesario para la unidad de datos fija.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>Nombre del fabricante del equipo tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>Nombre del modelo de fabricante del equipo tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de dispositivos</p></td>
<td align="left"><p>Usuarios conocidos en el equipo administrado por MBAM.</p></td>
</tr>
</tbody>
</table>

 

**Informe de cumplimiento de equipos con BitLocker: campos de volumen del equipo**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de columna</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Letra de unidad</p></td>
<td align="left"><p>Letra de unidad del equipo que el usuario asignó a la unidad particular.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de unidad</p></td>
<td align="left"><p>Tipo de unidad. Los valores válidos son la unidad del sistema operativo y la unidad de datos fija. Se trata de unidades físicas en lugar de volúmenes lógicos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intensidad de cifrado</p></td>
<td align="left"><p>Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipos de protectores</p></td>
<td align="left"><p>Tipo de protector seleccionado mediante la Directiva utilizada para cifrar un sistema operativo o una unidad de datos fija. Los tipos de protector válidos para un sistema operativo son TPM o TPM + PIN. El tipo de protector válido para una unidad de datos fija es una contraseña.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado del protector</p></td>
<td align="left"><p>Indica que el equipo administrado por MBAM tiene habilitado el tipo de protector especificado en la Directiva. Los Estados válidos son activado o desactivado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de cifrado</p></td>
<td align="left"><p>Estado de cifrado de la unidad. Los Estados válidos son cifrados, no cifrados y cifrados.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





