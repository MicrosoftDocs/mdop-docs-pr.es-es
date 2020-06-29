---
title: Descripción de los informes MBAM.
description: Descripción de los informes MBAM.
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822870"
---
# Descripción de los informes MBAM.


Administración y supervisión de Microsoft BitLocker (MBAM) genera varios informes para supervisar el uso de BitLocker y el cumplimiento. En este tema se describen los informes de MBAM de cumplimiento empresarial, los equipos individuales, la compatibilidad de hardware y la actividad de recuperación de claves.

## Descripción de los informes


Para acceder a la característica informes de MBAM, abra el sitio web de administración de MBAM. Seleccione **informes** en el panel de navegación. A continuación, en el panel contenido principal, haga clic en la pestaña del tipo de informe: **Informe de cumplimiento**de la empresa, informe de **cumplimiento de equipos**, informe de auditoría de **hardware**o informe de **Auditoría de recuperación**.

### Informe de cumplimiento de la empresa

Un informe de cumplimiento empresarial proporciona información sobre el cumplimiento general de BitLocker de su organización. Los filtros disponibles para este informe le permiten restringir los resultados de la búsqueda según el estado de cumplimiento y el estado de error. Este informe se ejecuta cada seis horas.

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
<td align="left"><p>El nombre DNS especificado por el usuario que se administra mediante MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de dominio</p></td>
<td align="left"><p>El nombre de dominio completo, donde reside el equipo cliente y es administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>El estado de cumplimiento del equipo, según la Directiva especificada para el equipo. Los posibles Estados son no conformes y conformes. Para obtener más información, consulte Estados de cumplimiento del informe de cumplimiento de la empresa en este tema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>El estado del hardware del equipo para determinar la identificación del tipo de hardware y si el equipo está exento de la Directiva. Hay tres posibles estados: hardware desconocido (el tipo de hardware no ha sido identificado por MBAM), el hardware está exento (el tipo de hardware se identificó y se marcó como exento de la Directiva MBAM) y no está exento (el hardware se identificó y no está exento de la Directiva).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de dispositivos</p></td>
<td align="left"><p>Usuarios conocidos en el equipo administrado por MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado sobre el estado de cumplimiento del equipo según la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. Esta vez es configurable. Consulta la configuración de la Directiva de MBAM.</p></td>
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
<td align="left"><p>El equipo no es compatible según la Directiva especificada, y el tipo de hardware no se ha indicado como excluido de la Directiva.</p></td>
<td align="left"><p>Haga clic en <strong> nombre del equipo </strong> para expandir el informe de cumplimiento de equipos y determinar si el estado de cada unidad cumple con la Directiva especificada. Si el estado de cifrado indica que el equipo no está cifrado, es posible que el cifrado aún esté en proceso o que haya un error en el equipo. Si no hay ningún error, la causa probable es que el equipo aún está en proceso de conectar o establecer el estado de cifrado. Vuelva a comprobar más tarde para determinar si el estado cambia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>No exentas</p></td>
<td align="left"><p>El equipo cumple con los requisitos de la Directiva especificada.</p></td>
<td align="left"><p>No es necesario realizar ninguna acción. De manera opcional, puede ver el informe de cumplimiento de equipos para confirmar el estado del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>Exención de hardware</p></td>
<td align="left"><p>Si el tipo de hardware está exento. Independientemente de cómo esté configurada la Directiva o del estado individual de cada unidad de disco duro, se considera que el estado general es compatible.</p></td>
<td align="left"><p>No es necesario realizar ninguna acción.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Reglamenta</p></td>
<td align="left"><p>Hardware desconocido</p></td>
<td align="left"><p>MBAM reconoce el tipo de hardware, pero MBAM no sabe si está exento o no está exento. Esto sucede si el administrador no ha establecido el estado compatible del hardware. Por lo tanto, MBAM revierte al estado de cumplimiento de las normas de forma predeterminada.</p></td>
<td align="left"><p>Este es el estado inicial de un cliente MBAM recién implementado. Normalmente, es solo un estado transitorio. Incluso si el administrador marcó el hardware como compatible, puede haber un retraso significativo o un tiempo de espera configurable antes de que el equipo cliente informe de vuelta. Anote la hora del último contacto y vuelva a protegerlo después del intervalo especificado para ver si el estado ha cambiado. Si el estado no ha cambiado, es posible que haya un error en este equipo o tipo de hardware.</p></td>
</tr>
</tbody>
</table>

 

### Informe de cumplimiento de equipos

El informe de cumplimiento de equipos muestra información específica de un equipo o usuario.

El informe de cumplimiento de equipos proporciona información de cifrado detallada y directivas aplicables para cada unidad de un equipo, incluidas las unidades de sistema operativo y las unidades de datos fijas. Para ver este tipo de informe, haga clic en el nombre del equipo en el informe de compatibilidad empresarial o escriba el nombre del equipo en el informe de cumplimiento normativo de equipos. Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.

**Nota:**  Este informe no proporciona el estado de cifrado de los volúmenes de datos extraíbles.

 

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
<td align="left"><p>El nombre del equipo DNS especificado por el usuario que está siendo administrado por MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de dominio</p></td>
<td align="left"><p>El nombre de dominio completo, donde reside el equipo cliente y es administrado por MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de equipo</p></td>
<td align="left"><p>El tipo de portabilidad de un equipo. Los tipos válidos son no portátiles y portátiles.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operativo</p></td>
<td align="left"><p>Tipo de sistema operativo instalado en el equipo cliente administrado de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>El estado de cumplimiento general del equipo administrado por MBAM. Los Estados válidos son conformes y no conformes. Aunque es posible tener unidades compatibles y no compatibles en el mismo equipo, este campo indica el cumplimiento general de equipos por directiva especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Intensidad de descifrado de Directiva</p></td>
<td align="left"><p>La intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM. Por ejemplo, 128 bits con difusor</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidad de sistema operativo de Directiva</p></td>
<td align="left"><p>Indica si se requiere cifrado para el O/S y el tipo de protector según corresponda.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unidad de datos fija de la Directiva</p></td>
<td align="left"><p>Indica si es necesario el cifrado para la unidad fija.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidad de datos extraíble de la Directiva</p></td>
<td align="left"><p>Indica si es necesario el cifrado para la unidad extraíble.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de dispositivos</p></td>
<td align="left"><p>Proporciona la identidad de los usuarios conocidos en el equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Franquicia</p></td>
<td align="left"><p>Indica si el tipo de hardware del equipo es reconocido por MBAM y, si se conoce, si el equipo se ha indicado que está exento de la Directiva. Hay tres Estados: hardware desconocido (el tipo de hardware no ha sido identificado por MBAM); Exención de hardware (el tipo de hardware se identificó y se marcó como exento de la Directiva de MBAM); y no está exenta (el hardware se identificó y no está exento de la Directiva).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>El nombre del fabricante del equipo tal y como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>El nombre del modelo de fabricante del equipo como aparece en el BIOS del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contacto</p></td>
<td align="left"><p>Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento. T</p></td>
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
<td align="left"><p>Letra de unidad del equipo que el usuario asignó a esta unidad en particular.</p></td>
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
<td align="left"><p>Tipo de protector seleccionado mediante la Directiva utilizada para cifrar un sistema operativo o un volumen fijo. Los tipos de protector válidos de una unidad de sistema operativo son TPM o TPM + PIN. El único tipo de protector válido para un volumen de datos fijo es password.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado del protector</p></td>
<td align="left"><p>Este campo indica si el equipo ha habilitado el tipo de protector especificado en la Directiva. Los Estados válidos son activado o desactivado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de cifrado</p></td>
<td align="left"><p>Este es el estado de cifrado actual de la unidad. Los Estados válidos son cifrados, no cifrados y cifrados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado de cumplimiento</p></td>
<td align="left"><p>Indica si la unidad está conforme con la Directiva. Los Estados son no conformes y conformes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalles del estado de cumplimiento</p></td>
<td align="left"><p>Contiene mensajes de estado y error relacionados con el estado de cumplimiento del equipo.</p></td>
</tr>
</tbody>
</table>

 

### Informe de auditoría de hardware

Este informe puede ayudarle a auditar los cambios en el estado de compatibilidad de hardware de modelos y fabricas de equipos específicos. Para ayudarle a restringir los resultados de la búsqueda, este informe incluye el filtrado de criterios, como el tipo de cambio y la hora de ocurrencia. Cada cambio de estado se controla según el usuario y la fecha y hora. El agente de MBAM que se ejecuta en el equipo cliente rellena automáticamente el tipo de hardware. Este informe realiza un seguimiento de los cambios de usuario de la información recopilada directamente desde el equipo administrado MBAM. Un cambio administrativo típico es cambiar de compatible a incompatible. Sin embargo, el administrador también puede revisar cualquier campo.

**Campos de informe de auditoría de hardware**

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
<td align="left"><p>Fecha y hora</p></td>
<td align="left"><p>Fecha y hora en que se realizó un cambio en el tipo de hardware. Tenga en cuenta que cada tipo de hardware único se asigna al menos a una entrada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuario</p></td>
<td align="left"><p>Usuario administrativo que ha realizado el cambio para la entrada en particular.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cambiar tipo</p></td>
<td align="left"><p>Tipo de cambio que se realizó en la información de tipo de hardware. Los valores válidos son suma (nueva entrada), actualizar (cambiar entrada existente) o eliminación (quitar entrada existente).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Valor original</p></td>
<td align="left"><p>Valor de la especificación de tipo de hardware antes de que se realizara el cambio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Valor actual</p></td>
<td align="left"><p>Valor de la especificación de tipo de hardware después de realizar el cambio.</p></td>
</tr>
</tbody>
</table>

 

### Informe de auditoría de recuperación

El informe de auditoría de recuperación puede ayudarle a auditar los usuarios que han solicitado el acceso a las claves de recuperación. Los criterios de filtro para este informe incluyen el tipo de usuario que realiza la solicitud, el tipo de clave solicitada, la hora de ocurrencia, el éxito o el error, la hora de la ocurrencia y el tipo de solicitud de usuario (soporte técnico, usuario final). Este informe permite a los administradores generar informes contextuales basados en las necesidades.

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
<td align="left"><p>La fecha y la hora en las que un usuario final o un usuario del servicio de asistencia hizo una solicitud de recuperación de clave.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de la solicitud</p></td>
<td align="left"><p>Estado de la solicitud. Los Estados válidos se han realizado correctamente (la clave se ha recuperado) o han fallado (la clave no se ha recuperado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuario del Departamento de soporte técnico</p></td>
<td align="left"><p>El usuario del servicio de asistencia que inició la solicitud de recuperación de claves. Si el usuario del servicio de asistencia recupera la clave en nombre de un usuario final, el campo del usuario final estará en blanco.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuario</p></td>
<td align="left"><p>El usuario final que inició la solicitud de recuperación de claves.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de clave</p></td>
<td align="left"><p>El tipo de clave que se solicitó. MBAM recopila tres tipos de clave: contraseña de la clave de recuperación (para recuperar un equipo en modo de recuperación); IDENTIFICADOR de clave de recuperación (para recuperar un equipo en el modo de recuperación en nombre de otro usuario); y hash de contraseña del módulo de plataforma segura (TPM) (para recuperar un equipo con un TPM bloqueado).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción del motivo</p></td>
<td align="left"><p>El motivo por el que se solicitó el tipo de clave especificado. Las razones se especifican en las características recuperación y administrar TPM del sitio web administrativo. Entre las entradas válidas se incluyen texto introducido por el usuario o uno de los siguientes códigos de motivo:</p>
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
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Para guardar los resultados del informe en un archivo, haga clic en el botón **exportar** en la barra de menús informes.

 

## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





