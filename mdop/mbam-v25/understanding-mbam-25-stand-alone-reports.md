---
title: Descripción de informes independientes de MBAM 2.5
description: Descripción de informes independientes de MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812775"
---
# Descripción de informes independientes de MBAM 2.5


En este tema se describen los informes que están disponibles al ejecutar administración y supervisión de Microsoft BitLocker (MBAM) en la topología independiente.

**Nota**  
Si está ejecutando MBAM con la topología de integración de Configuration Manager, genera informes desde Configuration Manager en lugar de desde MBAM. Para obtener más información sobre estos informes, vea [ver informes de MBAM 2,5 para la topología de integración de Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .



## Descripción de los informes de topología independiente de MBAM


MBAM proporciona tres tipos de informes que puede usar para supervisar la compatibilidad de su organización con BitLocker:

-   [Informe de cumplimiento de la empresa](#bkmk-enterprisecompliance)

-   [Informe de cumplimiento de equipos](#bkmk-compliance)

-   [Informe de auditoría de recuperación](#bkmk-recovery)

Para acceder a los informes de MBAM cuando esté ejecutando MBAM en la topología independiente, abra un explorador Web y, a continuación, abra el sitio web de administración y supervisión. Seleccione **informes** en la barra de menús de la izquierda. En la barra de menús superior, seleccione el tipo de informe que desea generar. Para obtener más información acerca de la generación de estos informes, consulte [generar informes independientes de MBAM 2,5](generating-mbam-25-stand-alone-reports.md).

### <a href="" id="bkmk-enterprisecompliance"></a>Informe de cumplimiento de la empresa

Use este tipo de informe para recopilar información sobre el cumplimiento general de BitLocker de su organización. Puede usar filtros para restringir los resultados de la búsqueda para obtener más información sobre el estado de cumplimiento y el estado de error de los equipos de su organización.

**Información general de cumplimiento empresarial**

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
<td align="left"><p>% De exención</p></td>
<td align="left"><p>Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De no exento</p></td>
<td align="left"><p>Porcentaje de equipos no exentos del requisito de cifrado de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>Porcentaje de equipos compatibles de la empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No conforme</p></td>
<td align="left"><p>Porcentaje de equipos no conformes de la empresa.</p></td>
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



**Detalles del equipo de cumplimiento empresarial**

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
<td align="left"><p>Estado de cumplimiento del equipo, según la Directiva especificada para el equipo. Los Estados son no conformes y conformes. Consulte la siguiente tabla de Estados de cumplimiento de informe de cumplimiento de la empresa para obtener más información sobre cómo interpretar los Estados de cumplimiento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Estado que indica si este equipo está exento de la Directiva de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado sobre el estado de cumplimiento del equipo conforme a la Directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto es configurable. Para obtener más información, consulte la configuración de directiva de grupo MBAM.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a>Informe de cumplimiento de equipos

Use este tipo de informe para recopilar información específica de un equipo o usuario.

Para ver este informe, haga clic en el nombre del equipo en el informe de compatibilidad empresarial o escriba el nombre del equipo en el informe de cumplimiento normativo de equipos. Este informe muestra información de cifrado detallada sobre cada unidad (sistema operativo y unidades de datos fijas) en un equipo. También indica la Directiva que se aplica a cada tipo de unidad en el equipo. Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.

**Nota**  
El estado de cifrado del volumen de datos extraíbles no se muestra en este informe.



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
<td align="left"><p>Nombre de dominio completo en el que reside el equipo cliente y administrado por MBAM.</p></td>
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
<td align="left"><p>Estado general de cumplimiento del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes.</p>
<p>Observe que el estado de cumplimiento por unidad (consulte la tabla siguiente) puede indicar diferentes Estados de cumplimiento. Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</p></td>
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
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Estado que indica si este equipo está exento de la Directiva de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>Nombre del fabricante del equipo, tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>Nombre del modelo de fabricante del equipo, tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado sobre el estado de cumplimiento del equipo, de acuerdo con la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. La frecuencia de contacto es configurable. Para obtener más información, consulte la configuración de directiva de grupo MBAM.</p></td>
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
<td align="left"><p>Tipo de protector seleccionado mediante la configuración de directiva de grupo que se usa para cifrar un sistema operativo o un volumen de datos fijos.</p></td>
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



### <a href="" id="bkmk-recovery"></a>Informe de auditoría de recuperación

Use este tipo de informe para auditar los usuarios que han solicitado acceso a las claves de recuperación de BitLocker. El informe ofrece varios filtros basados en los criterios de filtrado deseados. Puede filtrar por un determinado tipo de usuario (un usuario del servicio de asistencia o un usuario final), si la solicitud ha fallado o ha tenido éxito, el tipo específico de clave solicitada y un intervalo de fechas durante el cual se produjo la recuperación.

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
<td align="left"><p>Origen de solicitud de auditoría</p></td>
<td align="left"><p>El sitio desde el que se inició la solicitud. Esta entrada tendrá uno de dos valores: <strong> portal de autoservicio </strong> o departamento de <strong> soporte técnico </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de la solicitud</p></td>
<td align="left"><p>Estado de la solicitud. Los Estados válidos son satisfactorios (se recuperó la clave) o Falleron (no se recuperó la clave).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuario del Departamento de soporte técnico</p></td>
<td align="left"><p>Usuario del servicio de asistencia que inició la solicitud de recuperación de claves.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si un usuario avanzado del servicio de asistencia recupera la clave sin especificar el usuario final, el <strong> campo del usuario final estará </strong> en blanco. Un usuario estándar del Departamento de soporte técnico debe especificar el usuario final y ese usuario aparecerá en este campo.</p>
<p>Una recuperación a través del portal de autoservicio mostrará la lista del usuario final de la solicitud en este campo y en el <strong> campo de usuario final </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuario final</p></td>
<td align="left"><p>Usuario final que inició la solicitud de recuperación de clave.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ordenador</p></td>
<td align="left"><p>Nombre del equipo del equipo que se ha recuperado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de clave</p></td>
<td align="left"><p>Tipo de clave que solicitó el usuario del servicio de asistencia o el usuario final. Los tres tipos de claves que recopila MBAM son:</p>
<ul>
<li><p>Contraseña de la clave de recuperación (usada para recuperar un equipo en modo de recuperación)</p></li>
<li><p>IDENTIFICADOR de la clave de recuperación (se usa para recuperar un equipo en el modo de recuperación en nombre de otro usuario)</p></li>
<li><p>Hash de contraseña de TPM (usado para recuperar un equipo con un TPM bloqueado)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción del motivo</p></td>
<td align="left"><p>Motivo por el que el usuario del servicio de asistencia o el usuario final solicitó el tipo de clave especificado. Las razones se especifican en las características recuperación y administración de TPM del sitio web de administración y supervisión. Las entradas válidas son texto introducido por el usuario o uno de los siguientes códigos de motivo:</p>
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



**Nota**  
Los resultados del informe se pueden guardar en un archivo haciendo clic en el botón **exportar** de la barra de menús **informes** .




## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Generación de informes independientes de MBAM 2.5](generating-mbam-25-stand-alone-reports.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





