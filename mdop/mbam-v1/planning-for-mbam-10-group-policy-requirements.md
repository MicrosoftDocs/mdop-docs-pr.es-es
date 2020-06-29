---
title: Planificación de los requisitos de directiva de grupo de MBAM 1.0
description: Planificación de los requisitos de directiva de grupo de MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812438"
---
# Planificación de los requisitos de directiva de grupo de MBAM 1.0


Administración de clientes de Microsoft BitLocker Administration and Monitoring (MBAM) requiere que se aplique una configuración de directiva de grupo personalizada. En este tema se describen las opciones de directiva disponibles para el objeto de directiva de grupo (GPO) cuando usa MBAM para administrar el cifrado de unidad BitLocker en la empresa.

**Importante**  
MBAM no usa la configuración de GPO predeterminada para el cifrado de unidad BitLocker de Windows. Si la configuración predeterminada está habilitada, se puede producir un comportamiento conflictivo. Para habilitar MBAM para administrar BitLocker, debe definir la configuración de directiva de GPO después de instalar la plantilla de directiva de grupo MBAM.



Después de instalar la plantilla de directiva de grupo MBAM, puede ver y modificar la configuración de directiva de GPO de MBAM personalizada que permite a MBAM administrar el cifrado de BitLocker de la empresa. La plantilla de directiva de grupo MBAM debe instalarse en un equipo que sea capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la tecnología de MDOP de administración avanzada de directivas de grupo (AGPM). A continuación, para editar el objeto de directiva de grupo aplicable, abra la GPMC o AGPM y, a continuación, vaya al nodo GPO siguiente: **configuración del equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**.

El nodo de GPO MBAM de MDOP (administración de BitLocker) contiene cuatro parámetros de directiva global y cuatro nodos de configuración de GPO secundarios, respectivamente. Los cuatro parámetros de configuración de directiva global de GPO son: administración de clientes, unidad fija, unidad de sistema operativo y unidad extraíble. En las siguientes secciones se proporcionan definiciones de directiva y sugerencias de configuración de directivas para ayudarle a planear los requisitos de configuración de directiva de GPO MBAM.

**Nota**  
Para obtener más información sobre cómo configurar las opciones mínimas de GPO sugeridas para habilitar MBAM para administrar el cifrado de BitLocker, consulte [Cómo editar la configuración de GPO de MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).



## Definiciones de directiva global


En esta sección se describen las definiciones de la directiva global MBAM, que se pueden encontrar en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**.

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


En esta sección se describen las definiciones de directiva de administración de clientes para MBAM, que se encuentran en el siguiente nodo GPO: **configuración de equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**  \\  **Administración de clientes**.

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
<li><p><strong>Extremo de servicio de hardware y recuperación de MBAM </strong> . Esta es la primera opción de directiva que debe configurar para habilitar la administración del cifrado de BitLocker en el cliente de MBAM. Para esta configuración, escriba la ubicación del extremo de forma similar al siguiente ejemplo: <strong> http:// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; Puerto el servicio web está enlazado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.SVC </strong> .</p></li>
<li><p><strong>Seleccione la información de recuperación de BitLocker para almacenar </strong> . Esta configuración de directiva le permite configurar el servicio de recuperación de claves para realizar una copia de seguridad de la información de recuperación de BitLocker. También le permite configurar el servicio de informes de estado para recopilar informes de cumplimiento y cumplimiento normativo. La Directiva proporciona un método administrativo para recuperar datos cifrados con BitLocker para ayudar a evitar la pérdida de datos a causa de la falta de información clave. El informe de estado y la actividad de recuperación de claves se enviarán de forma automática y silencio a la ubicación del servidor de informes configurado.</p>
<p>Si no configura o si deshabilita esta configuración de Directiva, la información de recuperación de clave no se guardará y no se notificará al servidor la actividad de recuperación de clave y el informe de estado. Cuando esta opción se establece en <strong> contraseña de recuperación y paquete de claves </strong> , la contraseña de recuperación y el paquete de claves se copian automáticamente en la ubicación del servidor de recuperación de claves configurado.</p></li>
<li><p><strong>Escriba la frecuencia de estado de comprobación del cliente en minutos </strong> . Esta configuración de directiva administra la frecuencia con la que el cliente comprueba las directivas de protección de BitLocker y el estado en el equipo cliente. Esta Directiva también administra la frecuencia con la que se guarda el estado de cumplimiento del cliente en el servidor. El cliente comprueba el estado y las directivas de protección de BitLocker en el equipo cliente, y también realiza una copia de seguridad de la clave de recuperación del cliente a la frecuencia configurada.</p>
<p>Establezca esta frecuencia según el requisito establecido por su empresa sobre la frecuencia con la que comprobar el estado de cumplimiento del equipo y la frecuencia con la que se realiza la copia de seguridad de la clave de recuperación del cliente.</p></li>
<li><p><strong>Extremo del servicio de informes de estado de MBAM </strong> . Esta es la configuración de la Directiva segunda que debe configurar para habilitar la administración del cifrado de BitLocker en el cliente de MBAM. Para esta configuración, escriba la ubicación del extremo mediante el siguiente ejemplo: <strong> http:// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; Puerto al que está enlazado el servicio Web &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService. SVC </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Permitir la comprobación de compatibilidad de hardware</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta configuración de directiva le permite administrar la comprobación de la compatibilidad del hardware antes de habilitar la protección de BitLocker en las unidades de los equipos cliente de MBAM.</p>
<p>Debe habilitar esta opción de Directiva si su empresa tiene hardware o equipos antiguos que no son compatibles con el módulo de plataforma segura (TPM). Si alguno de estos criterios es verdadero, habilite la comprobación de compatibilidad de hardware para asegurarse de que MBAM se aplica solo a los modelos de equipo que son compatibles con BitLocker. Si todos los equipos de su organización son compatibles con BitLocker, no tiene que implementar la compatibilidad de hardware y puede establecer esta directiva en <strong> no configurado </strong> .</p>
<p>Si habilita esta configuración de Directiva, el modelo del equipo se validará en la lista de compatibilidad de hardware una vez cada 24 horas, antes de que la Directiva habilite la protección de BitLocker en una unidad de equipo.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Antes de habilitar esta configuración de Directiva, asegúrese de que ha configurado la <strong> configuración de extremo del servicio de recuperación y hardware </strong> de MBAM en las <strong> Opciones de directiva configurar servicios de MBAM </strong> .</p>
</div>
<div>

</div>
<p>Si deshabilita o no establece esta configuración de Directiva, el modelo de equipo no se validará en relación con la lista de compatibilidad de hardware.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar la Directiva de exención de usuarios</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar la dirección de un sitio web, la dirección de correo electrónico o el número de teléfono que le indicará a un usuario que solicite una exención del cifrado de BitLocker.</p>
<p>Si habilita esta configuración de directiva y proporciona una dirección del sitio web, una dirección de correo electrónico o un número de teléfono, los usuarios verán un cuadro de diálogo con instrucciones sobre cómo solicitar una exención de la protección de BitLocker. Para obtener más información sobre cómo habilitar exenciones de cifrado de BitLocker para los usuarios, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> Cómo administrar las exenciones de cifrado de BitLocker </a> .</p>
<p>Si deshabilita o no establece esta configuración de Directiva, las instrucciones sobre cómo solicitar una solicitud de exención no se mostrarán a los usuarios.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La exención de usuarios se administra por usuario, no por equipo. Si varios usuarios inician sesión en el mismo equipo y un usuario no está exento, el equipo se cifrará.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Definiciones de directivas de unidades fijas


En esta sección se describen las definiciones de directivas de unidades fijas para MBAM, que pueden encontrarse en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas**de \\ **Windows Components** \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad fija**.

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
<td align="left"><p>Sugerencia de configuración: <strong> habilitada </strong> y seleccione la <strong> casilla de verificación Habilitar autobloqueo de unidad de datos fijos </strong> si es necesario cifrar el volumen del sistema operativo.</p>
<p>Esta configuración de directiva te permite administrar si deseas cifrar o no las unidades fijas.</p>
<p>Al habilitar esta Directiva, no deshabilite la <strong> directiva configurar el uso de la contraseña para las unidades de datos fijas </strong> .</p>
<p>Si la <strong> casilla habilitar autobloqueo de unidad de datos fijos </strong> está activada, el volumen del sistema operativo se debe cifrar.</p>
<p>Si habilita esta configuración de Directiva, los usuarios tendrán que poner todas las unidades fijas en la protección de BitLocker, que cifrarán las unidades.</p>
<p>Si no configura esta Directiva o si deshabilita esta Directiva, los usuarios no tendrán que poner unidades fijas en la protección de BitLocker.</p>
<p>Si deshabilita esta Directiva, el agente de MBAM descifra cualquier unidad fija cifrada.</p>
<p>Si no es necesario cifrar el volumen del sistema operativo, desactive la <strong> casilla habilitar el bloqueo automático de la unidad de datos fijos </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Denegar el permiso de "escritura" a las unidades fijas que no están protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva determina si se requiere la protección de BitLocker para las unidades fijas en un equipo para que se puedan escribir. Esta configuración de Directiva se aplica al activar BitLocker.</p>
<p>Cuando la Directiva no está configurada, todas las unidades fijas del equipo se montan con permisos de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir el acceso a unidades fijas protegidas con BitLocker desde versiones anteriores de Windows</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para desbloquear y ver las unidades fijas que se han formateado con el sistema de archivos de tabla de asignación de archivos (FAT) en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p>
<p>Estos sistemas operativos tienen permisos de solo lectura para las unidades protegidas con BitLocker.</p>
<p>Cuando la Directiva está deshabilitada, las unidades fijas formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de la contraseña para unidades fijas</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para configurar la protección con contraseña en unidades fijas.</p>
<p>Cuando la Directiva no está configurada, las contraseñas serán compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de contraseña y solo requiere ocho caracteres.</p>
<p>Para mayor seguridad, habilite esta directiva y seleccione <strong> requerir contraseña para unidad de datos fija </strong> , seleccione <strong> requerir complejidad de la contraseña </strong> y establezca la <strong> longitud mínima de la contraseña deseada </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades fijas protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando esta Directiva no está configurada, se permite el agente de recuperación de datos de BitLocker y no se realiza una copia de seguridad de la información de recuperación en AD DS. MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
</tbody>
</table>



## Definiciones de directiva de unidad de sistema operativo


En esta sección se describen las definiciones de directiva de unidad del sistema operativo para MBAM, que se encuentran en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas plantillas**de \\ **Windows componentes de Windows**de \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad del sistema operativo**.

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
<p>Esta configuración de directiva determina si se cifrará la unidad del sistema operativo.</p>
<p>Configure esta directiva para hacer lo siguiente:</p>
<ul>
<li><p>Exigir la protección de BitLocker para la unidad del sistema operativo.</p></li>
<li><p>Configure el uso de PIN para usar un PIN de módulo de plataforma segura (TPM) para la protección del sistema operativo.</p></li>
<li><p>Configure los pines de inicio mejorados para que admitan caracteres como letras mayúsculas y minúsculas, y números. MBAM no admite el uso de símbolos y espacios para los bordes mejorados, aunque BitLocker admita símbolos y espacios.</p></li>
</ul>
<p>Si habilita esta configuración de Directiva, los usuarios deberán proteger la unidad del sistema operativo con BitLocker.</p>
<p>Si no configura o si deshabilita la configuración, los usuarios no tendrán que proteger la unidad del sistema operativo con BitLocker.</p>
<p>Si deshabilita esta Directiva, el agente de MBAM descifra el volumen del sistema operativo Si está cifrado.</p>
<p>Cuando está habilitada, esta configuración de directiva requiere que los usuarios protejan el sistema operativo con la protección de BitLocker y la unidad está cifrada. En función de los requisitos de cifrado, puede seleccionar el método de protección de la unidad del sistema operativo.</p>
<p>Para los requisitos de seguridad más altos, use TPM + PIN, permita PIN mejorados y establezca la longitud mínima del PIN en ocho caracteres.</p>
<p>Cuando esta directiva está habilitada con el protector de TPM + PIN, puede considerar deshabilitar las siguientes directivas en <strong> configuración de suspensión de administración del sistema </strong>  /  <strong> </strong>  /  <strong> </strong> :</p>
<ul>
<li><p>Permitir Estados de espera (S1-S3) cuando está en espera (conectado)</p></li>
<li><p>Permitir Estados de espera (S1-S3) cuando está en suspensión (con batería)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el perfil de validación de plataforma TPM</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar cómo el hardware de seguridad TPM de un equipo protege la clave de cifrado de BitLocker. Esta configuración de Directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya tiene habilitada la protección de TPM.</p>
<p>Cuando esta Directiva no está configurada, el TPM usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de configuración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo recuperar unidades de sistema operativo protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando esta Directiva no está configurada, se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</p>
<p>La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
</tbody>
</table>



## Definiciones de directivas de unidades extraíbles


En esta sección se describen las definiciones de directivas de unidades extraíbles para MBAM, que se encuentran en el siguiente nodo GPO: **configuración del equipo** \\ **plantillas administrativas plantillas**de \\ **Windows componentes de Windows**de \\ **MDOP MBAM (administración de BitLocker)**  \\  **unidad extraíble**.

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
<td align="left"><p>Denegar los permisos de "escritura" a unidades extraíbles que no estén protegidas por BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para permitir permisos de solo escritura en unidades protegidas con BitLocker.</p>
<p>Cuando esta directiva está habilitada, todas las unidades de datos extraíbles en el equipo requieren cifrar para que se permitan los permisos de escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir el acceso a unidades extraíbles protegidas con BitLocker desde versiones anteriores de Windows</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para desbloquear y ver las unidades fijas formateadas con el sistema de archivos (FAT) en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Estos sistemas operativos tienen permisos de solo lectura para las unidades protegidas con BitLocker.</p>
<p>Cuando la Directiva está deshabilitada, las unidades extraíbles formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de la contraseña para unidades de datos extraíbles</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para configurar la protección con contraseña en unidades de datos extraíbles.</p>
<p>Cuando esta Directiva no está configurada, las contraseñas son compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de contraseña y solo requiere ocho caracteres.</p>
<p>Para una mayor seguridad, puede habilitar esta directiva y seleccionar <strong> requerir contraseña para la unidad de datos extraíbles </strong> , seleccionar <strong> requerir complejidad de </strong> la contraseña y, a continuación, establecer la <strong> longitud mínima de la contraseña </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades extraíbles protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Puede configurar esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando la Directiva se establece en <strong> no configurada </strong> , se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</p>
<p>La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Preparación del entorno para MBAM 1.0](preparing-your-environment-for-mbam-10.md)









