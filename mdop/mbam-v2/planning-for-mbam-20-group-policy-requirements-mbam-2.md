---
title: Planificación de los requisitos de directiva de grupo de MBAM 2.0
description: Planificación de los requisitos de directiva de grupo de MBAM 2.0
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812830"
---
# Planificación de los requisitos de directiva de grupo de MBAM 2.0


Para administrar equipos cliente de supervisión y administración de Microsoft BitLocker (MBAM), debe tener en cuenta los tipos de protectores de BitLocker que desea admitir en su organización y, a continuación, configurar las opciones de directiva de grupo correspondientes que desea aplicar. En este tema se describen las opciones de configuración de directiva de grupo que se pueden usar cuando se usa la administración y la supervisión de Microsoft BitLocker para administrar el cifrado de unidad BitLocker en la empresa.

MBAM es compatible con los siguientes tipos de protectores de BitLocker para unidades de sistema operativo: módulo de plataforma segura (TPM), TPM + PIN, clave USB de TPM y TPM + PIN + clave USB, contraseña, contraseña numérica y agente de recuperación de datos. El protector de contraseña solo es compatible con los dispositivos Windows to Go y los dispositivos Windows 8 que no tengan TPM. MBAM admite la tecla TPM + USB y los protectores de clave USB y TPM + PIN solo cuando el volumen del sistema operativo se cifra antes de instalar MBAM.

MBAM admite los siguientes tipos de protectores de BitLocker para unidades de datos fijas: contraseña, desbloqueo automático, contraseña numérica y agente de recuperación de datos.

El protector de contraseña numérica se aplica automáticamente como parte del cifrado de volumen y no es necesario configurarlo.

**Importante**  
La configuración predeterminada del objeto de directiva de grupo (GPO) de cifrado de unidad BitLocker de Windows no se usa en MBAM y puede provocar un comportamiento conflictivo si está habilitado. Para habilitar MBAM para administrar BitLocker, debe definir la configuración de directiva de grupo MBAM solo después de instalar la plantilla de directiva de grupo MBAM.



Los pin de inicio mejorados pueden contener caracteres, como letras en mayúsculas y minúsculas, y números. A diferencia de BitLocker, MBAM no admite el uso de símbolos y espacios para los bordes mejorados.

Instale la plantilla de directiva de grupo MBAM en un equipo capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la tecnología de MDOP de administración avanzada de directivas de grupo (AGPM). Para editar la configuración de GPO que habilita la funcionalidad de MBAM, primero debe instalar la plantilla de directiva de grupo MBAM, abrir la GPMC o AGPM para editar el GPO aplicable y, a continuación, navegar hasta el siguiente nodo GPO: directivas de **configuración del equipo** \\ **Policies** \\ **plantillas administrativas**de \\ **Windows componentes de Windows** \\ **(administración de BitLocker).**

El nodo de GPO MBAM de MDOP (administración de BitLocker) contiene cuatro configuraciones de directiva global y cuatro nodos de configuración de GPO secundarios: administración de clientes, unidad fija, unidad de sistema operativo y unidad extraíble. En las siguientes secciones se proporcionan definiciones de directiva y sugerencias de configuración de directivas para ayudarle a planear los requisitos de configuración de directiva de GPO de MBAM.

**Nota**  
Para obtener más información sobre cómo configurar las opciones mínimas de GPO recomendadas para habilitar MBAM para administrar el cifrado de BitLocker, consulte [Cómo editar la configuración de GPO de MBAM 2,0](how-to-edit-mbam-20-gpo-settings-mbam-2.md).



## Definiciones de directiva global


En esta sección se describen las definiciones de directiva global de MBAM que se encuentran en el siguiente nodo GPO: directivas de **configuración de equipos** \\ **Policies** \\ **Administrative Templates** \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencia de configuración de directivas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Elija el método de cifrado de unidad y la intensidad de cifrado</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para usar un método de cifrado específico y la intensidad de cifrado.</p>
<p>Cuando esta Directiva no está configurada, BitLocker usa el método de cifrado predeterminado de AES 128 bits con difusor o el método de cifrado especificado por el script de configuración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Evitar la sobrescritura de memoria al reiniciar</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para mejorar el rendimiento de reinicio sin sobrescribir los secretos de BitLocker en memoria al reiniciar.</p>
<p>Cuando esta Directiva no está configurada, los secretos de BitLocker se quitan de la memoria cuando se reinicia el equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Validar regla de uso de certificados de tarjeta inteligente</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para usar la protección de BitLocker basada en certificados de tarjeta inteligente.</p>
<p>Cuando esta Directiva no está configurada, se usa un identificador de objeto predeterminado 1.3.6.1.4.1.311.67.1.1 para especificar un certificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Proporcionar los identificadores únicos para la organización</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para usar un agente de recuperación de datos basado en certificados o el lector de BitLocker To Go.</p>
<p>Cuando esta Directiva no está configurada <strong> , </strong> no se usa el campo de identificación.</p>
<p>Si su empresa requiere medidas de seguridad mayores, es posible que desee configurar el <strong> campo de identificación para asegurarse de </strong> que todos los dispositivos USB tienen este conjunto de campos y que están alineados con esta configuración de directiva de grupo.</p></td>
</tr>
</tbody>
</table>



## Definiciones de directivas de administración de clientes


En esta sección se describen las definiciones de directiva de administración de clientes para administración y supervisión de Microsoft BitLocker en el siguiente nodo GPO: directivas de **configuración del equipo** \\ **Policies** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)** \\ **Administración de clientes**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencias de configuración de directivas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurar servicios de MBAM</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<ul>
<li><p><strong>Extremo de servicio de hardware y recuperación de MBAM </strong> . Use esta configuración para habilitar la administración de cifrado de BitLocker de MBAM cliente. Escriba una ubicación de extremo que sea similar a la del ejemplo siguiente: <strong> http:// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; Puerto el servicio web está enlazado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.SVC </strong> .</p></li>
<li><p><strong>Seleccione la información de recuperación de BitLocker para almacenar </strong> . Esta configuración de directiva le permite configurar el servicio de recuperación de claves para hacer una copia de seguridad de la información de recuperación de BitLocker. También le permite configurar el servicio de informes de estado para recopilar informes de cumplimiento y cumplimiento. La Directiva proporciona un método administrativo para recuperar datos cifrados con BitLocker a fin de evitar la pérdida de datos a causa de la falta de información clave. El informe de estado y la actividad de recuperación de claves se enviarán de forma automática y silencio a la ubicación del servidor de informes configurado.</p>
<p>Si no configura o si deshabilita esta configuración de Directiva, la información de recuperación de clave no se guardará y no se notificará al servidor la actividad de recuperación de clave y el informe de estado. Cuando esta opción se establece en <strong> contraseña de recuperación y paquete de claves </strong> , la contraseña de recuperación y el paquete de claves se copian automáticamente en la ubicación del servidor de recuperación de claves configurado.</p></li>
<li><p><strong>Especifique la frecuencia del estado de comprobación del cliente en minutos </strong> . Esta configuración de directiva administra la frecuencia con la que el cliente comprueba el estado y las directivas de protección de BitLocker en el equipo cliente. Esta Directiva también administra la frecuencia con la que se guarda el estado de cumplimiento del cliente en el servidor. El cliente comprueba el estado y las directivas de protección de BitLocker en el equipo cliente, además de hacer una copia de seguridad de la clave de recuperación del cliente en la frecuencia configurada.</p>
<p>Establezca esta frecuencia en función de los requisitos establecidos por su empresa sobre la frecuencia con que se comprueba el estado de cumplimiento del equipo y la frecuencia con la que se realiza la copia de seguridad de la clave de recuperación del cliente.</p></li>
<li><p><strong>Extremo del servicio de informes de estado de MBAM </strong> . Debe configurar esta opción para habilitar la administración del cifrado de BitLocker en el cliente de MBAM. Escriba una ubicación de extremo que sea similar a la del ejemplo siguiente: <strong> http:// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; Puerto el servicio web está enlazado a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.SVC </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar la Directiva de exención de usuarios</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar la dirección de un sitio web, la dirección de correo electrónico o el número de teléfono que le indicará a un usuario que solicite una exención del cifrado de BitLocker.</p>
<p>Si habilita esta configuración de directiva y proporciona una dirección del sitio web, una dirección de correo electrónico o un número de teléfono, los usuarios verán un cuadro de diálogo que les proporciona instrucciones sobre cómo solicitar una exención de la protección de BitLocker. Para obtener más información sobre cómo habilitar exenciones de cifrado de BitLocker para los usuarios, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> Cómo administrar las exenciones de cifrado de BitLocker </a> .</p>
<p>Si deshabilita o no establece esta configuración de Directiva, las instrucciones de solicitud de exención no se presentarán a los usuarios.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La exención de usuarios se administra por usuario, no por equipo. Si varios usuarios inician sesión en el mismo equipo y ninguno de los usuarios está exento, el equipo se cifrará.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar el programa para la mejora de la experiencia del usuario</p></td>
<td align="left"><p>Esta configuración de directiva le permite configurar cómo los usuarios de MBAM pueden unirse al programa para la mejora de la experiencia del usuario. Este programa recopila información sobre el hardware del equipo y cómo los usuarios usan MBAM sin interrumpir su trabajo. La información ayuda a Microsoft a identificar las características de MBAM que deben mejorar. Microsoft no usará esta información para identificar a los usuarios de MBAM o ponerse en contacto con ellos.</p>
<p>Si habilita esta configuración de Directiva, los usuarios podrán unirse al programa para la mejora de la experiencia del usuario.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán unirse al programa para la mejora de la experiencia del usuario.</p>
<p>Si no establece esta configuración de Directiva, los usuarios tendrán la opción de unirse al programa para la mejora de la experiencia del usuario.</p></td>
</tr>
</tbody>
</table>



## Definiciones de directivas de unidades fijas


En esta sección se describen las definiciones de directiva de unidades fijas de administración y supervisión de Microsoft BitLocker que se encuentran en el siguiente nodo GPO: directivas de **configuración de equipos** \\ **Policies** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)** \\ **unidad fija**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencia de configuración de directivas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de cifrado de unidad de datos fija</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta configuración de directiva le permite administrar si las unidades fijas se deben cifrar.</p>
<p>Si es necesario que el volumen del sistema operativo se Cifre, seleccione la <strong> opción Habilitar desbloqueo automático de la unidad de datos fijos </strong> .</p>
<p>Al habilitar esta Directiva, no debe deshabilitar la <strong> directiva configurar el uso de la contraseña para unidades de datos fijos </strong> a menos que el uso de la opción de bloqueo automático para las unidades de datos fijas esté permitido o sea necesario.</p>
<p>Si necesita el uso del bloqueo automático para las unidades de datos fijas, debe configurar los volúmenes del sistema operativo para que se cifren.</p>
<p>Si habilita esta configuración de Directiva, los usuarios deberán poner todas las unidades fijas en la protección de BitLocker y las unidades se cifrarán.</p>
<p>Si no establece esta configuración de Directiva, los usuarios no tendrán que poner unidades fijas en la protección de BitLocker. Si aplica esta directiva después de que las unidades de datos fijas estén cifradas, el agente de MBAM descifra las unidades fijas cifradas.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán poner sus unidades de datos fijas en la protección de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Denegar el acceso de escritura a unidades fijas no protegidas por BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva determina si se requiere la protección de BitLocker para que las unidades fijas puedan escribirse en un equipo. Esta configuración de Directiva se aplica al activar BitLocker.</p>
<p>Cuando la Directiva no está configurada, todas las unidades de datos fijas en el equipo se montan con acceso de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir el acceso a unidades fijas protegidas con BitLocker desde versiones anteriores de Windows</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilitar esta directiva para permitir que las unidades fijas con el sistema de archivos FAT se desbloqueen y se visualicen en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Cuando la Directiva está habilitada o no configurada, las unidades fijas formateadas con el sistema de archivos FAT se pueden desbloquear y su contenido se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2. Estos sistemas operativos tienen acceso de solo lectura a las unidades protegidas con BitLocker.</p>
<p>Cuando la Directiva está deshabilitada, las unidades fijas formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de la contraseña para unidades fijas</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Use esta directiva para especificar si se requiere una contraseña para desbloquear las unidades de datos fijas protegidas por BitLocker.</p>
<p>Si habilita esta configuración de Directiva, los usuarios podrán configurar una contraseña que cumpla los requisitos que defina. BitLocker permitirá a los usuarios desbloquear una unidad con cualquiera de los protectores disponibles en la unidad.</p>
<p>Esta configuración se aplica al activar BitLocker, no al desbloquear un volumen.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán usar una contraseña.</p>
<p>Cuando la Directiva no está configurada, las contraseñas son compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de las contraseñas y que solo requieren ocho caracteres.</p>
<p>Para mayor seguridad, habilite esta directiva y seleccione <strong> requerir contraseña para unidad de datos fija </strong> , seleccione <strong> requerir complejidad de la contraseña </strong> y establezca la <strong> longitud mínima de la contraseña deseada </strong> .</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán usar una contraseña.</p>
<p>Si no establece esta configuración de Directiva, las contraseñas serán compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de las contraseñas y que solo requieran ocho caracteres.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades fijas protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando la Directiva no está configurada, se permite el agente de recuperación de datos de BitLocker y no se realiza una copia de seguridad de la información de recuperación en AD DS. MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
</tbody>
</table>



## Definiciones de directiva de unidad de sistema operativo


En esta sección se describen las definiciones de directiva de la unidad del sistema operativo para administración y supervisión de Microsoft BitLocker en el siguiente nodo GPO: directivas de **configuración del equipo** \\ **Policies** \\ **plantillas administrativas plantillas administrativas**de \\ **Windows componentes** \\ **MDOP MBAM (administración de BitLocker)** \\ **unidad del sistema operativo**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencia de configuración de directivas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de cifrado de unidad del sistema operativo</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta configuración de directiva te permite administrar si la unidad del sistema operativo debe estar cifrada.</p>
<p>Para una mayor seguridad, considere la posibilidad de deshabilitar las siguientes configuraciones de directiva en <strong> configuración sistema/administración de energía/suspensión </strong> al habilitarlas con el protector TPM + PIN:</p>
<ul>
<li><p>Permitir Estados de espera (S1-S3) cuando está en espera (conectado)</p></li>
<li><p>Permitir Estados de espera (S1-S3) cuando está en suspensión (con batería)</p></li>
</ul>
<p>Si está ejecutando Microsoft Windows 8 o una versión posterior y quiere usar BitLocker en un equipo sin un TPM, active la <strong> casilla Permitir BitLocker sin un TPM compatible </strong> . En este modo, se requiere una contraseña para el inicio. Si olvida la contraseña, tendrá que usar una de las opciones de recuperación de BitLocker para acceder a la unidad.</p>
<p>En un equipo con un TPM compatible, se pueden usar dos tipos de métodos de autenticación al inicio para proporcionar protección adicional para los datos cifrados. Cuando el equipo se inicia, solo puede usar el TPM para la autenticación, o bien también puede requerir la entrada de un número de identificación personal (PIN).</p>
<p>Si habilita esta configuración de Directiva, los usuarios tendrán que colocar la unidad del sistema operativo en protección de BitLocker y la unidad se cifrará.</p>
<p>Si deshabilita esta Directiva, los usuarios no podrán poner la unidad de sistema operativo en protección de BitLocker. Si aplica esta directiva después de que la unidad del sistema operativo esté cifrada, la unidad se descifrará.</p>
<p>Si no configura esta Directiva, no es necesario que la unidad del sistema operativo esté incluida en la protección de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el perfil de validación de plataforma TPM</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar cómo el hardware de seguridad TPM de un equipo protege la clave de cifrado de BitLocker. Esta configuración de Directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya se ha activado con la protección de TPM.</p>
<p>Cuando esta configuración de Directiva no está configurada, el TPM usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de configuración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades de sistema operativo protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando esta Directiva no está configurada, se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</p>
<p>La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
</tbody>
</table>



## Definiciones de directivas de unidades extraíbles


En esta sección se describen las definiciones de directivas de unidades extraíbles de Microsoft BitLocker administración y supervisión en el siguiente nodo GPO: directivas de **configuración del equipo** \\ **Policies** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad extraíble**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencia de configuración de directivas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controlar el uso de BitLocker en unidades extraíbles</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta directiva controla el uso de BitLocker en unidades de datos extraíbles.</p>
<p>Habilite la <strong> opción permitir que los usuarios apliquen la protección de BitLocker en unidades de datos extraíbles </strong> para permitir que los usuarios ejecuten el Asistente de configuración de BitLocker en una unidad de datos extraíble.</p>
<p>Habilite la <strong> opción permitir que los usuarios puedan suspender y descifrar BitLocker en unidades de datos extraíbles </strong> para permitir a los usuarios quitar el cifrado de unidad BitLocker de la unidad o para suspender el cifrado mientras se realiza el mantenimiento.</p>
<p>Cuando esta directiva está habilitada y la <strong> opción permitir que los usuarios apliquen protección de BitLocker en unidades de datos extraíbles </strong> está seleccionada, el cliente de MBAM guarda la información de recuperación de las unidades extraíbles en el servidor de recuperación de claves MBAM y permite a los usuarios recuperar la unidad si se pierde la contraseña.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Denegar el acceso de escritura a unidades extraíbles no protegidas por BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para permitir solo el acceso de escritura a las unidades protegidas con BitLocker.</p>
<p>Cuando esta directiva está habilitada, todas las unidades de datos extraíbles en el equipo requieren cifrar para que se permita el acceso de escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir el acceso a unidades extraíbles protegidas con BitLocker desde versiones anteriores de Windows</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para permitir que las unidades fijas con el sistema de archivos FAT se desbloqueen y se vean en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Cuando esta Directiva no está configurada, las unidades de datos extraíbles formateadas con el sistema de archivos FAT se pueden desbloquear en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2, y se puede ver su contenido. Estos sistemas operativos tienen acceso de solo lectura a las unidades protegidas con BitLocker.</p>
<p>Cuando la Directiva está deshabilitada, las unidades extraíbles formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de la contraseña para unidades de datos extraíbles</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para configurar la protección con contraseña en unidades de datos extraíbles.</p>
<p>Cuando esta Directiva no está configurada, las contraseñas son compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de las contraseñas y que solo requieren ocho caracteres.</p>
<p>Para mayor seguridad, puede habilitar esta directiva y activar <strong> Solicitar contraseña para unidades de datos extraíbles </strong> , seleccionar <strong> requerir complejidad de la contraseña </strong> y establecer la longitud mínima de la contraseña preferida <strong> </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades extraíbles protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando se establece en <strong> no configurado </strong> , se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</p>
<p>La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Requisitos previos de implementación de MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)









