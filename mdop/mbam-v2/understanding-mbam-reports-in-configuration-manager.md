---
title: Descripción de informes MBAM en Administrador de configuración
description: Descripción de informes MBAM en Administrador de configuración
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823821"
---
# Descripción de informes MBAM en Administrador de configuración


Cuando se instala la administración y supervisión de Microsoft BitLocker (MBAM) con la topología integrada de Configuration Manager, las características de compatibilidad de hardware y de creación de informes se mueven a la infraestructura de Configuration Manager y salen de MBAM. Cuando se usa la topología del administrador de configuración, los informes se ejecutan desde Configuration Manager en lugar de desde MBAM, excepto para el informe de auditoría de recuperación al que se sigue teniendo acceso a través del sitio web de administración y supervisión.

Los informes para la topología integrada de Configuration Manager muestran la compatibilidad de BitLocker para la empresa y para los equipos y dispositivos individuales que administra MBAM. Los informes proporcionan información de tabla y gráficos, y permiten filtrar informes para ver los datos desde distintas perspectivas.

La información de este tema describe los informes de MBAM que se ejecuta desde Configuration Manager. Para obtener información sobre los informes de MBAM para la topología independiente, consulte [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).

## Acceso a informes en Configuration Manager


Para acceder a la característica informes de Configuration Manager, abra la **consola de Configuration Manager**. Para mostrar la lista de los informes disponibles:

-   En el administrador de configuración 2007, expanda el nodo **Administración de equipos** y, a continuación, expanda el nodo **informes** .

-   En SystemCenter2012 ConfigurationManager, en **información general**, expanda el nodo **informes** y, a continuación, haga clic en **informes**.

### Panel de cumplimiento de BitLocker Enterprise

El panel de cumplimiento de BitLocker Enterprise proporciona los siguientes gráficos, que muestran el estado de cumplimiento de BitLocker en toda la empresa:

-   Distribución del estado de cumplimiento

-   Distribución de errores no conformes

-   Distribución del estado de cumplimiento por tipo de unidad

**Distribución del estado de cumplimiento**

Este gráfico circular muestra los Estados de compatibilidad de equipos dentro de la empresa y muestra el porcentaje de equipos, comparado con el número total de equipos de la colección seleccionada, que tienen ese estado de cumplimiento. También se muestra el número real de equipos con cada Estado. El gráfico circular muestra los siguientes Estados de cumplimiento:

-   Reglamenta

-   No conforme

-   Exención de usuarios

-   Exención de usuarios temporales

-   Directiva no exigida

-   Desconocido: equipos cuyo estado se notificó como un error o dispositivos que forman parte de la colección pero que nunca han informado de su estado de cumplimiento, por ejemplo, si se han desconectado de la organización.

**Distribución de errores no conformes**

Este gráfico circular muestra las categorías de equipos de la empresa que no son compatibles con la Directiva de cifrado de unidad BitLocker y muestra el número de equipos de cada categoría. Cada categoría se calcula a partir del número total de equipos no compatibles de la colección.

-   Usuario pospuesto

-   No se puede encontrar el TPM compatible

-   La partición del sistema no está disponible o es lo suficientemente grande

-   Conflicto de directivas

-   Esperando el aprovisionamiento automático de TPM

-   Se ha producido un error desconocido

-   No hay información: los equipos que no tienen instalado el cliente de MBAM o que tienen el cliente de MBAM instalado pero no activado, por ejemplo, el servicio no funciona.

**Distribución del estado de cumplimiento por tipo de unidad**

Este gráfico de barras muestra el estado de compatibilidad actual de BitLocker por tipo de unidad. Los Estados son "conforme" y "no conforme". Se muestran barras para las unidades de datos fijas y las unidades del sistema operativo. Se incluyen los equipos que no tienen una unidad de datos fija y solo muestran un valor en la barra de unidades del sistema operativo. El gráfico no incluye los usuarios a los que se les ha concedido una exención de la Directiva de cifrado de unidad BitLocker o de la categoría "sin directiva".

### Informe de detalles de cumplimiento de BitLocker Enterprise

Este informe muestra información sobre la compatibilidad general de BitLocker en toda la empresa para la colección de equipos que se destina para uso de BitLocker.

**Campos del informe detalles de cumplimiento de BitLocker Enterprise**

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
<td align="left"><p>Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De exención</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De no exento</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
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
<td align="left"><p>Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</p></td>
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

 

**Informe detalles de cumplimiento de BitLocker Enterprise-Estados de cumplimiento**

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

 

### Informe Resumen de cumplimiento de BitLocker Enterprise

Use este tipo de informe para mostrar información sobre el cumplimiento general de BitLocker en toda la empresa y para mostrar la compatibilidad de equipos individuales que se encuentran en la colección de equipos de destino para el uso de BitLocker.

**Campos del informe Resumen de cumplimiento de BitLocker Enterprise**

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
<td align="left"><p>Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De exención</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De no exento</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
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
<td align="left"><p>Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</p></td>
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

 

**Informe Resumen de cumplimiento de BitLocker Enterprise-detalles del equipo**

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
<td align="left"><p>Estado general de cumplimiento del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes. Observe que el estado de cumplimiento por unidad (vea la tabla que sigue) puede indicar diferentes Estados de cumplimiento. Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Estado que indica si el usuario está exento o no exención de la Directiva de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de dispositivos</p></td>
<td align="left"><p>Usuario del dispositivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</p></td>
</tr>
</tbody>
</table>

 

### Informe de cumplimiento de equipos con BitLocker

Use este tipo de informe para recopilar información específica de un equipo. El informe de cumplimiento de equipos proporciona información de cifrado detallada acerca de cada unidad (sistema operativo y unidades de datos fijas) en un equipo, así como una indicación de la Directiva que se aplica a cada tipo de unidad en el equipo. Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.

**Nota:**  El estado de cifrado del volumen de datos extraíbles no se muestra en el informe.

 

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
<td align="left"><p>Estado general de cumplimiento del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes. Observe que el estado de cumplimiento por unidad (vea la tabla que sigue) puede indicar diferentes Estados de cumplimiento. Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</p></td>
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
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Estado que indica si el usuario está exento o no exención de la Directiva de BitLocker.</p></td>
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
<td align="left"><p>Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intensidad de cifrado de Directiva</p></td>
<td align="left"><p>Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM. (por ejemplo, 128 bits con difusor).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Directiva: unidad de sistema operativo</p></td>
<td align="left"><p>Indica si es necesario el cifrado para el O/S y el tipo de protector adecuado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Directiva: unidad de datos fija</p></td>
<td align="left"><p>Indica si es necesario el cifrado de la unidad fija.</p></td>
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
<td align="left"><p>Tipo de protector seleccionado mediante la Directiva utilizada para cifrar un sistema operativo o un volumen fijo. Los tipos de protector válidos de un sistema operativo son TPM o TPM + PIN y para un volumen de datos fijos es contraseña.</p></td>
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


[Uso de MBAM con Administrador de configuración](using-mbam-with-configuration-manager.md)

 

 





