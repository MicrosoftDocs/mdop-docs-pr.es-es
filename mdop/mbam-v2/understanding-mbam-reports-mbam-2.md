---
title: Descripción de los informes MBAM.
description: Descripción de los informes MBAM.
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823811"
---
# Descripción de los informes MBAM.


Si eligió la topología independiente al instalar Microsoft BitLocker Administration and Monitoring (MBAM), puede ejecutar diferentes informes en MBAM para supervisar el uso y el cumplimiento de BitLocker. MBAM informa del cumplimiento y otra información sobre todos los equipos y dispositivos que administra. La información de este tema se puede usar para ayudarle a comprender los informes de administración y administración de Microsoft BitLocker para la actividad de cumplimiento de equipos y de la clave de recuperación individuales.

**Nota:**  Si ha elegido la topología del administrador de configuración al instalar Microsoft BitLocker Administration and Monitoring (MBAM), los informes se generan desde Configuration Manager en lugar de desde MBAM. Para obtener más información sobre los informes que se ejecutan desde Configuration Manager, vea Descripción de los [informes de MBAM en Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).

 

## Descripción de los informes


Para acceder a la característica informes de administración y supervisión de Microsoft BitLocker, abra un explorador Web y abra el sitio web de administración y supervisión. Seleccione **informes** en la barra de menús de la izquierda y, a continuación, seleccione de la barra de menús superior el tipo de informe que desea generar.

### Informe de cumplimiento de la empresa

Use este tipo de informe para recopilar información sobre el cumplimiento general de BitLocker de su organización. Puede usar distintos filtros para restringir los resultados de la búsqueda al estado de cumplimiento y al estado de error. La información del informe se actualiza cada seis horas.

**Campos del informe de cumplimiento de la empresa**

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
<td align="left"><p>Nombre DNS especificado por el usuario administrado por MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de dominio</p></td>
<td align="left"><p>Nombre de dominio completo en el que reside el equipo cliente y administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>Estado de cumplimiento del equipo, según la Directiva especificada para el equipo. Los Estados son no conformes y conformes. Para obtener más información sobre cómo interpretar los Estados de cumplimiento, consulte la tabla Estados de cumplimiento del informe de cumplimiento de la empresa.</p></td>
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

 

**Estados de cumplimiento de informe de cumplimiento empresarial**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estado de cumplimiento</th>
<th align="left">Franquicia</th>
<th align="left">Descripción</th>
<th align="left">Acción de usuario</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>No conforme</p></td>
<td align="left"><p>No exentas</p></td>
<td align="left"><p>El equipo no cumple con los requisitos de la Directiva especificada.</p></td>
<td align="left"><p>Expanda los detalles del informe de cumplimiento de equipos haciendo clic en <strong> nombre del equipo </strong> y determine si el estado de cada unidad cumple con la Directiva especificada. Si el estado de cifrado indica que el equipo no está cifrado, es posible que el cifrado esté en proceso o que haya un error en el equipo. Si no hay ningún error, la causa probable es que el equipo aún está en proceso de conectar o establecer el estado de cifrado. Vuelva a comprobar más tarde para determinar si el estado cambia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>No exentas</p></td>
<td align="left"><p>El equipo cumple con los requisitos de la Directiva especificada.</p></td>
<td align="left"><p>No es necesario realizar ninguna acción; el estado del equipo se puede confirmar viendo el informe de cumplimiento de equipos.</p></td>
</tr>
</tbody>
</table>

 

### Informe de cumplimiento de equipos

Use este tipo de informe para recopilar información específica de un equipo o usuario.

Para ver este informe, haga clic en el nombre del equipo en el informe de cumplimiento de la empresa o escriba el nombre del equipo en el informe de cumplimiento normativo de equipos. El informe de cumplimiento de equipos proporciona información de cifrado detallada acerca de cada unidad (sistema operativo y unidades de datos fijas) en un equipo, así como una indicación de la Directiva que se aplica a cada tipo de unidad en el equipo. Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.

**Nota:**  El estado de cifrado del volumen de datos extraíbles no se mostrará en el informe.

 

**Campos del informe de cumplimiento del equipo**

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
<td align="left"><p>Tipo de sistema operativo que se encuentra en el equipo cliente administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>Estado general de cumplimiento del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes. Observe que el estado de cumplimiento por unidad (consulte la tabla siguiente) puede indicar diferentes Estados de cumplimiento. Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Intensidad de cifrado de Directiva</p></td>
<td align="left"><p>Intensidad de cifrado seleccionada por el Administrador durante la especificación de la Directiva MBAM (por ejemplo, 128 bits con difusor).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidad de sistema operativo de Directiva</p></td>
<td align="left"><p>Indica si el sistema operativo necesita el cifrado y muestra el tipo de protector adecuado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Directiva: unidad de datos fija</p></td>
<td align="left"><p>Indica si el cifrado es necesario para la unidad de datos fija.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidad de datos extraíble de la Directiva</p></td>
<td align="left"><p>Indica si es necesario el cifrado de la unidad extraíble.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de dispositivos</p></td>
<td align="left"><p>Usuarios conocidos en el equipo administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>Nombre del fabricante del equipo, tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>Nombre del modelo de fabricante del equipo, tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado del estado de cumplimiento del equipo, de acuerdo con la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</p></td>
</tr>
</tbody>
</table>

 

**Campos de la unidad del informe cumplimiento normativo**

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
<td align="left"><p>Tipo de protector</p></td>
<td align="left"><p>Tipo de protector seleccionado mediante la directiva usada para cifrar un sistema operativo o un volumen de datos fijo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado del protector</p></td>
<td align="left"><p>Indica que el equipo administrado por MBAM tiene habilitado el tipo de protector especificado en la Directiva. Los Estados válidos son activado o desactivado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de cifrado</p></td>
<td align="left"><p>Estado de cifrado de la unidad. Los Estados válidos son cifrados, no cifrados y cifrados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>Estado que indica si la unidad está conforme con la Directiva. Los Estados son no conformes y conformes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado del estado de cumplimiento del equipo, según la Directiva especificada.</p></td>
</tr>
</tbody>
</table>

 

### Informe de auditoría de recuperación

Use este tipo de informe para auditar los usuarios que han solicitado el acceso a las claves de recuperación. El informe ofrece varios filtros basados en los criterios de filtrado deseados. Los usuarios pueden filtrar por un tipo específico de usuario, ya sea un usuario del servicio de asistencia o un usuario final, si la solicitud falló o se realizó correctamente, el tipo específico de clave solicitada y un intervalo de fechas durante el cual se produjo la recuperación. El administrador puede generar informes contextuales basados en necesidades.

**Campos de informe de auditoría de recuperación**

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
<td align="left"><p>Fecha y hora de la solicitud</p></td>
<td align="left"><p>Fecha y hora en que un usuario final o un usuario del servicio de asistencia realizó una solicitud de recuperación de clave.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de la solicitud</p></td>
<td align="left"><p>Estado de la solicitud. Los Estados válidos se han realizado correctamente (la clave se ha recuperado) o han fallado (la clave no se ha recuperado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuario del Departamento de soporte técnico</p></td>
<td align="left"><p>Usuario del servicio de asistencia que inició la solicitud de recuperación de claves. Nota: Si el usuario del servicio de asistencia recupera la clave en nombre de un usuario final, el campo del usuario final estará en blanco.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuario</p></td>
<td align="left"><p>Usuario final que inició la solicitud de recuperación de clave.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de clave</p></td>
<td align="left"><p>Tipo de clave que solicitó el usuario del servicio de asistencia o el usuario final. Los tres tipos de claves que recopila MBAM son: contraseña de la clave de recuperación (usada para recuperar un equipo en modo de recuperación), identificador de clave de recuperación (se usa para recuperar un equipo en el modo de recuperación en nombre de otro usuario) y hash de contraseña de TPM (se usa para recuperar un equipo con un TPM bloqueado).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción del motivo</p></td>
<td align="left"><p>Motivo por el que el usuario del servicio de asistencia o el usuario final solicitó el tipo de clave especificado. Las razones se especifican en las características recuperación y administración de TPM del sitio web de administración y supervisión. Las entradas válidas son texto escrito por el usuario o uno de los siguientes códigos de motivo:</p>
<ul>
<li><p>Se cambió el orden de inicio del sistema operativo</p></li>
<li><p>BIOS cambiado</p></li>
<li><p>Archivos de sistema operativo modificados</p></li>
<li><p>Clave de inicio perdida</p></li>
<li><p>PIN perdido</p></li>
<li><p>Reinicio de TPM</p></li>
<li><p>Contraseña perdida</p></li>
<li><p>Tarjeta inteligente perdida</p></li>
<li><p>Restablecer el bloqueo del PIN</p></li>
<li><p>Activar TPM</p></li>
<li><p>Desactivar TPM</p></li>
<li><p>Cambiar contraseña de TPM</p></li>
<li><p>Borrar TPM</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Nota:**  Los resultados del informe se pueden guardar en un archivo haciendo clic en el botón **exportar** de la barra de menús informes. Para obtener más información sobre cómo ejecutar informes de MBAM, consulte [Cómo generar informes de MBAM](how-to-generate-mbam-reports-mbam-2.md).

 

## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





