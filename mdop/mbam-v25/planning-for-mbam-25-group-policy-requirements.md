---
title: Planificación para requisitos de directiva de grupo de MBAM 2.5
description: Planificación para requisitos de directiva de grupo de MBAM 2.5
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823770"
---
# Planificación para requisitos de directiva de grupo de MBAM 2.5


Use la siguiente información para determinar los tipos de protectores de BitLocker que puede usar para administrar los equipos cliente de supervisión y administración de Microsoft BitLocker (MBAM) de su empresa.

## Tipos de protectores de BitLocker que MBAM admite


MBAM admite los siguientes tipos de protectores de BitLocker.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de unidad o volumen</th>
<th align="left">Protectores de BitLocker compatibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Volúmenes del sistema operativo</p></td>
<td align="left"><ul>
<li><p><strong>Módulo de plataforma segura (TPM)</strong></p></li>
<li><p><strong>TPM + PIN</strong></p></li>
<li><p><strong>Clave de TPM + USB </strong> : solo se admite cuando el volumen del sistema operativo está cifrado antes de instalar MBAM</p></li>
<li><p><strong>TPM + PIN + tecla USB </strong> - solo es compatible cuando el volumen del sistema operativo está cifrado antes de instalar MBAM</p></li>
<li><p><strong>Contraseña </strong> - compatible solo con dispositivos Windows to Go, unidades de datos fijas y dispositivos Windows 8, Windows 8,1 y Windows 10 que no tengan un TPM</p></li>
<li><p><strong>La contraseña numérica se </strong> - aplica automáticamente como parte del cifrado de volumen y no es necesario configurarla excepto en el modo FIPS en Windows 7.</p></li>
<li><p><strong>Agente de recuperación de datos (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Unidades de datos fijas</p></td>
<td align="left"><ul>
<li><p><strong>Contraseña</strong></p></li>
<li><p><strong>Desbloqueo automático</strong></p></li>
<li><p><strong>La contraseña numérica se </strong> - aplica automáticamente como parte del cifrado de volumen y no es necesario configurarla excepto en el modo FIPS en Windows 7.</p></li>
<li><p><strong>Agente de recuperación de datos (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidades extraíbles</p></td>
<td align="left"><ul>
<li><p><strong>Contraseña</strong></p></li>
<li><p><strong>Desbloqueo automático</strong></p></li>
<li><p><strong>La contraseña numérica </strong> - se aplica automáticamente como parte del cifrado de volumen y no es necesario configurarla</p></li>
<li><p><strong>Agente de recuperación de datos (DRA)</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### Compatibilidad con la Directiva de BitLocker de cifrado de espacio usado

En MBAM 2,5 SP1, si habilita el cifrado de espacio usado mediante la Directiva de grupo de BitLocker, el cliente de MBAM lo respetará.

Esta configuración de directiva de grupo se denomina **exigir tipo de cifrado de unidad en unidades de sistema operativo** y se encuentra en el siguiente nodo GPO: **configuración del equipo** &gt; **plantillas administrativas** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **unidades del sistema operativo**de cifrado de unidad BitLocker. Si habilita esta directiva y selecciona el tipo de cifrado como **cifrado solo de espacio usado**, MBAM cumplirá la Directiva y BitLocker solo cifrará el espacio en disco que se usa en el volumen.

## Cómo obtener las plantillas de directiva de grupo MBAM y editar la configuración


Cuando esté listo para configurar las opciones de directiva de grupo MBAM, haga lo siguiente:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pasos que debe seguir</th>
<th align="left">Dónde obtener instrucciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copie las plantillas de directiva de grupo MBAM de <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> Cómo obtener las plantillas de la Directiva de grupo de MDOP </a> e instalarlas en un equipo que sea capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copia de plantillas de directiva de grupo de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure las opciones de directiva de grupo que desea usar en su empresa.</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Edición de configuración de directiva de grupo de MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>



## Descripciones de la configuración de directiva de grupo MBAM


El nodo de GPO **MBAM de MDOP (administración de BitLocker)** contiene cuatro configuraciones de directiva global y cuatro nodos de GPO secundarios: **Administración de clientes**, **unidad fija**, **unidad de sistema operativo**y **unidad extraíble**. En las siguientes secciones se describen y sugieren las opciones de configuración de la Directiva de grupo MBAM.

**Importante**  
No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** o MBAM no funcionará correctamente. MBAM configurará automáticamente la configuración de este nodo cuando establezca la configuración del nodo **MBAM de MDOP (administración de BitLocker)** .



### Definiciones de directivas de grupo globales

En esta sección se describen las definiciones de directiva de grupo globales de MBAM en el siguiente nodo GPO: directivas de **configuración de equipos** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencias de configuración de directiva de grupo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Elija el método de cifrado de unidad y la intensidad de cifrado</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Configure esta directiva para usar un método de cifrado específico y la intensidad de cifrado.</p>
<p>Cuando esta Directiva no está configurada, BitLocker usa el método de cifrado predeterminado: AES 128 bits con difusor.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Un problema con el informe de cumplimiento de equipos con BitLocker provoca que se muestre &quot; desconocido &quot; para la intensidad de cifrado, incluso si está utilizando el valor predeterminado. Para evitar este problema, asegúrese de habilitar esta configuración y establecer un valor para la intensidad de cifrado.</p>
</div>
<div>

</div>
<ul>
<li><p>AES 128 bits con difusor: solo para Windows 7</p></li>
<li><p>AES 128 para Windows 8, Windows 8,1 y Windows 10</p></li>
</ul></td>
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
<p>Cuando esta Directiva no está configurada, se usa el identificador de objeto predeterminado 1.3.6.1.4.1.311.67.1.1 para especificar un certificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Proporcionar los identificadores únicos para la organización</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para usar un agente de recuperación de datos basado en certificados o el lector de BitLocker To Go.</p>
<p>Cuando esta Directiva no está configurada <strong> , </strong> no se usa el campo de identificación.</p>
<p>Si su empresa requiere una medida de seguridad superior, puede configurar el <strong> campo de identificación para asegurarse de </strong> que todos los dispositivos USB tienen este conjunto de campos y de que están alineados con esta configuración de directiva de grupo.</p></td>
</tr>
</tbody>
</table>



### Definiciones de directiva de grupo de administración de clientes

En esta sección se describen las definiciones de directivas de administración de clientes para MBAM en el siguiente nodo GPO: directivas de **configuración del equipo** &gt; **Policies** &gt; **plantillas administrativas** de &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)** &gt; **Administración de clientes**.

Puede establecer la misma configuración de directiva de grupo para las topologías de integración independiente y de System Center Configuration Manager, con solo una excepción: deshabilite la configuración de **extremo del servicio de informes de estado de MBAM Services &gt; MBAM** si está usando la topología de integración de Configuration Manager, como se indica en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencias de configuración de directiva de grupo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurar servicios de MBAM</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<ul>
<li><p><strong>Extremo de servicio de hardware y recuperación de MBAM </strong> . Use esta configuración para habilitar la administración de cifrado de BitLocker de MBAM cliente. Escriba una ubicación de extremo similar a la siguiente: <strong> http (s):// </strong><em> &lt; MBAM administración y supervisión nombre del servidor &gt; </em><strong> : </strong><em> &lt; el puerto que el servicio web está enlazado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.SVC </strong> .</p></li>
<li><p><strong>Seleccione la información de recuperación de BitLocker para almacenar </strong> . Esta configuración de directiva le permite configurar el servicio de recuperación de claves para hacer una copia de seguridad de la información de recuperación de BitLocker. También le permite configurar un servicio de informes de estado para recopilar informes. La Directiva proporciona un método administrativo para recuperar datos cifrados con BitLocker a fin de evitar la pérdida de datos a causa de la falta de información clave. El informe de estado y la actividad de recuperación de claves se envían de forma automática y silencio a la ubicación del servidor de informes configurado.</p>
<p>Si no establece esta configuración de directiva o la deshabilita, la información de recuperación de clave no se guardará y la actividad de recuperación de claves y los informes de estado no se notificarán en el servidor. Cuando esta configuración está configurada para la <strong> contraseña de recuperación y el paquete de claves </strong> , la contraseña de recuperación y el paquete de claves se copian automáticamente en la ubicación del servidor de recuperación de claves configurado.</p></li>
<li><p><strong>Especifique la frecuencia del estado de comprobación del cliente en minutos </strong> . Esta configuración de directiva administra la frecuencia con la que el cliente comprueba el estado y las directivas de protección de BitLocker en el equipo cliente. Esta Directiva también administra la frecuencia con la que se guarda el estado de cumplimiento del cliente en el servidor. El cliente comprueba el estado y las directivas de protección de BitLocker en el equipo cliente, además de hacer una copia de seguridad de la clave de recuperación del cliente en la frecuencia configurada.</p>
<p>Establezca esta frecuencia en función del requisito establecido por su empresa sobre la frecuencia con la que comprobar el estado de cumplimiento del equipo y la frecuencia con la que se realiza la copia de seguridad de la clave de recuperación del cliente.</p></li>
<li><p><strong>Extremo del servicio de informes de estado de MBAM:</strong></p>
<p><strong>Para MBAM en una topología independiente </strong> : debe configurar esta opción para habilitar la administración de cifrado de BitLocker de MBAM de cliente.</p>
<p>Escriba una ubicación de punto final similar a la del ejemplo siguiente:</p>
<p><strong>http (s):// </strong><em> &lt; MBAM administración y supervisión nombre &gt; </em><strong> del servidor: </strong><em> &lt; el puerto al que está enlazado el servicio Web &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.SVC</strong></p>
<p><strong>Para MBAM en la topología de integración de Configuration Manager </strong> : deshabilite esta configuración.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar la Directiva de exención de usuarios</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar la dirección de un sitio web, la dirección de correo electrónico o el número de teléfono que indica a un usuario que solicite una exención del cifrado de BitLocker.</p>
<p>Si habilita esta configuración de directiva y proporciona una dirección de sitio web, una dirección de correo electrónico o un número de teléfono, los usuarios verán un cuadro de diálogo con instrucciones sobre cómo solicitar una exención de la protección de BitLocker. Para obtener más información sobre cómo habilitar exenciones de cifrado de BitLocker para los usuarios, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> Cómo administrar las exenciones de cifrado de BitLocker </a> .</p>
<p>Si deshabilita o no establece esta configuración de Directiva, las instrucciones de solicitud de exención no se mostrarán a los usuarios.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La exención de usuarios se administra por usuario, no por equipo. Si varios usuarios inician sesión en el mismo equipo y ninguno de los usuarios está exento, el equipo se cifra.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar el programa para la mejora de la experiencia del usuario</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta configuración de directiva le permite configurar cómo los usuarios de MBAM pueden unirse al programa para la mejora de la experiencia del usuario. Este programa recopila información sobre el hardware del equipo y cómo los usuarios usan MBAM sin interrumpir su trabajo. La información ayuda a Microsoft a identificar las características de MBAM que deben mejorar. Microsoft no usa esta información para identificar o ponerse en contacto con usuarios de MBAM.</p>
<p>Si habilita esta configuración de Directiva, los usuarios podrán unirse al programa para la mejora de la experiencia del usuario.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán unirse al programa para la mejora de la experiencia del usuario.</p>
<p>Si no establece esta configuración de Directiva, los usuarios tendrán la opción de unirse al programa para la mejora de la experiencia del usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Proporcionar la dirección URL para el vínculo de directiva de seguridad</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Use esta configuración de directiva para especificar una dirección URL que se muestra a los usuarios finales como un vínculo denominado Directiva de seguridad de la &quot; empresa. &quot; El vínculo apunta a la Directiva de seguridad interna de su empresa y proporciona información acerca de los requisitos de cifrado a los usuarios finales. El vínculo aparece cuando MBAM se lo pide a los usuarios para cifrar una unidad.</p>
<p>Si habilita esta configuración de Directiva, puede configurar la dirección URL para el vínculo Directiva de seguridad.</p>
<p>Si deshabilita o no establece esta configuración de Directiva, el vínculo Directiva de seguridad no se mostrará a los usuarios.</p></td>
</tr>
</tbody>
</table>



### Definiciones de directivas de grupo de unidades fijas

En esta sección se describen las definiciones de directiva de unidad fija para administración y supervisión de Microsoft BitLocker en el siguiente nodo GPO: directivas de **configuración del equipo** &gt; **Policies** &gt; **plantillas administrativas** de &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)** &gt; **unidad fija**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencias de configuración de directiva de grupo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de cifrado de unidad de datos fija</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta configuración de directiva le permite administrar si se deben cifrar las unidades de datos fijas.</p>
<p>Si es necesario que el volumen del sistema operativo se Cifre, haga clic en <strong> Habilitar el bloqueo automático de la unidad de datos fija </strong> .</p>
<p>Al habilitar esta Directiva, no debe deshabilitar la <strong> directiva configurar el uso de la contraseña para unidades de datos fijas, </strong> a menos que esté habilitando o requiriendo el uso del bloqueo automático para las unidades de datos fijas.</p>
<p>Si tiene que usar el bloqueo automático para las unidades de datos fijas, debe configurar los volúmenes del sistema operativo para que se cifren.</p>
<p>Si habilita esta configuración de Directiva, los usuarios tendrán que poner todas las unidades de datos fijas en la protección de BitLocker y las unidades de datos se cifrarán.</p>
<p>Si no establece esta configuración de Directiva, los usuarios no tendrán que poner unidades de datos fijas en la protección de BitLocker. Si aplica esta directiva después de que se cifren las unidades de datos fijas, el agente de MBAM descifra las unidades de datos fijas cifradas.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no pueden poner sus unidades de datos fijas en la protección de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Denegar el acceso de escritura a unidades fijas no protegidas por BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva determina si se requiere la protección de BitLocker para que las unidades de datos fijas sean modificables en un equipo. Esta configuración de Directiva se aplica al activar BitLocker.</p>
<p>Cuando la Directiva no está configurada, todas las unidades de datos fijas en el equipo se montan con permisos de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir el acceso a unidades fijas protegidas con BitLocker desde versiones anteriores de Windows</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para que las unidades fijas con el sistema de archivos FAT se desbloqueen y se visualicen en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Cuando la Directiva está habilitada o no configurada, las unidades fijas formateadas con el sistema de archivos FAT se pueden desbloquear y su contenido se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP SP3 o Windows XP con SP2. Estos sistemas operativos tienen permisos de solo lectura para las unidades protegidas con BitLocker.</p>
<p>Cuando la Directiva está deshabilitada, las unidades fijas formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de la contraseña para unidades fijas</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Use esta directiva para especificar si se requiere una contraseña para desbloquear las unidades de datos fijas protegidas por BitLocker.</p>
<p>Si habilita esta configuración de Directiva, los usuarios podrán configurar una contraseña que cumpla los requisitos que usted defina. BitLocker permite a los usuarios desbloquear una unidad con cualquiera de los protectores disponibles en la unidad.</p>
<p>Esta configuración se aplica al activar BitLocker, no al desbloquear un volumen.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán usar una contraseña.</p>
<p>Cuando la Directiva no está configurada, las contraseñas son compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de las contraseñas y que solo requieren ocho caracteres.</p>
<p>Para mayor seguridad, habilite esta directiva y, después, seleccione <strong> requerir contraseña para una unidad de datos fija </strong> , haga clic en <strong> requerir complejidad de la contraseña </strong> y establezca la <strong> longitud mínima de la contraseña </strong> que desea.</p>
<p>Si deshabilita esta configuración de Directiva, los usuarios no podrán usar una contraseña.</p>
<p>Si no establece esta configuración de Directiva, las contraseñas se admiten con la configuración predeterminada, que no incluye los requisitos de complejidad de las contraseñas y que solo requieren ocho caracteres.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades fijas protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando la Directiva no está configurada, se permite el agente de recuperación de datos de BitLocker y no se realiza una copia de seguridad de la información de recuperación en AD DS. MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración de la aplicación de directivas de cifrado</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Use esta configuración de directiva para configurar el número de días que las unidades de datos fijas pueden permanecer como no compatibles hasta que se obliguen a cumplir con las directivas de MBAM. Los usuarios no pueden posponer la acción necesaria ni solicitar una exención de la misma después del período de gracia. El período de gracia comienza cuando se determina que la unidad de datos fijas no es compatible. Sin embargo, la Directiva de unidad de disco fija no se aplica hasta que la unidad de sistema operativo sea compatible.</p>
<p>Si el período de gracia vence y la unidad de datos fija sigue sin cumplirse, los usuarios no tienen la opción de posponer o solicitar una exención. Si el proceso de cifrado requiere la intervención del usuario, aparece un cuadro de diálogo que indica que los usuarios no pueden cerrar hasta que proporcionen la información necesaria.</p>
<p>Escriba <strong> 0 </strong> en el <strong> número de días de período de gracia de no cumplimiento para las unidades fijas </strong> para forzar el inicio del proceso de cifrado inmediatamente después del vencimiento del período de gracia para la unidad del sistema operativo.</p>
<p>Si deshabilita o no establece esta configuración, los usuarios no estarán obligados a cumplir con las directivas de MBAM.</p>
<p>Si no se necesita ninguna interacción por el usuario para agregar un protector, el cifrado comienza en segundo plano después de que venza el período de gracia.</p></td>
</tr>
</tbody>
</table>



### Definiciones de directiva de grupo de unidad de sistema operativo

En esta sección se describen las definiciones de directiva de la unidad del sistema operativo para administración y supervisión de Microsoft BitLocker en el siguiente nodo GPO: directivas de **configuración del equipo** &gt; **Policies** &gt; **plantillas administrativas plantillas administrativas** de &gt; **Windows componentes** &gt; **MDOP MBAM (administración de BitLocker)** &gt; **unidad del sistema operativo**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencias de configuración de directiva de grupo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de cifrado de unidad del sistema operativo</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta configuración de directiva te permite administrar si la unidad del sistema operativo debe estar cifrada.</p>
<p>Para una mayor seguridad, considere la posibilidad de deshabilitar la siguiente configuración de directiva en la <strong> configuración de suspensión de administración de energía del sistema </strong> &gt; <strong> cuando las </strong> &gt; <strong> </strong> habilite con el protector de TPM + PIN:</p>
<ul>
<li><p>Permitir Estados de espera (S1-S3) cuando está en espera (conectado)</p></li>
<li><p>Permitir Estados de espera (S1-S3) cuando está en suspensión (con batería)</p></li>
</ul>
<p>Si está ejecutando Microsoft Windows 8 o una versión posterior y quiere usar BitLocker en un equipo sin un TPM, active la <strong> casilla Permitir BitLocker sin un TPM compatible </strong> . En este modo, se requiere una contraseña para el inicio. Si olvida la contraseña, tendrá que usar una de las opciones de recuperación de BitLocker para acceder a la unidad.</p>
<p>En un equipo con un TPM compatible, se pueden usar dos tipos de métodos de autenticación al inicio para proporcionar protección adicional para los datos cifrados. Cuando el equipo se inicia, solo puede usar el TPM para la autenticación, o bien también puede requerir la entrada de un número de identificación personal (PIN).</p>
<p>Si habilita esta configuración de Directiva, los usuarios tendrán que colocar la unidad del sistema operativo en protección de BitLocker y la unidad se cifrará.</p>
<p>Si deshabilita esta Directiva, los usuarios no pueden poner la unidad del sistema operativo en protección de BitLocker. Si aplica esta directiva después de que la unidad del sistema operativo esté cifrada, la unidad se descifrará.</p>
<p>Si no configura esta Directiva, no es necesario que la unidad del sistema operativo esté incluida en la protección de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permitir PIN mejorados para el inicio</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Use esta configuración de directiva para configurar si se usan los pin de inicio mejorados con BitLocker. Los pines de inicio mejorados permiten el uso de caracteres como letras en mayúsculas y minúsculas, símbolos, números y espacios. Esta configuración de Directiva se aplica al activar BitLocker.</p>
<p>Si habilita esta configuración de Directiva, todos los pin de inicio de BitLocker nuevos establecidos permitirán que el usuario final cree PIN mejorados. Sin embargo, no todos los equipos pueden admitir pines mejorados en el entorno previo al inicio. Recomendamos encarecidamente que los administradores evalúen si sus sistemas son compatibles con esta característica antes de habilitar su uso.</p>
<p>Seleccione la <strong> casilla de verificación requerir PIN solo ASCII </strong> para ayudar a que los pines mejorados sean más compatibles con los equipos que limitan el tipo o el número de caracteres que se pueden escribir en el entorno previo a la inicialización.</p>
<p>Si deshabilita o no establece esta configuración de Directiva, no se usarán los pin mejorados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elegir cómo se pueden recuperar las unidades de sistema operativo protegidas con BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Configure esta directiva para habilitar el agente de recuperación de datos de BitLocker o para guardar la información de recuperación de BitLocker en servicios de dominio de Active Directory (AD DS).</p>
<p>Cuando esta Directiva no está configurada, se permite el agente de recuperación de datos y no se realiza una copia de seguridad de la información de recuperación en AD DS.</p>
<p>La operación MBAM no requiere que se haga una copia de seguridad de la información de recuperación en AD DS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de contraseñas para unidades de sistema operativo</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Use esta configuración de directiva para establecer las restricciones de contraseñas que se usan para desbloquear las unidades de sistema operativo protegidas con BitLocker. Si se permiten protectores que no son TPM en unidades de sistema operativo, puede proporcionar una contraseña, exigir requisitos de complejidad en la contraseña y configurar una longitud mínima para la contraseña. Para que la configuración de requisito de complejidad sea efectiva, también debe habilitar la configuración de directiva de grupo que &quot; debe cumplir los requisitos &quot; de complejidad ubicados en configuración del equipo Configuración de Windows configuración de &gt; &gt; seguridad &gt; directivas de &gt; contraseñas Directiva de contraseñas.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración se aplica al activar BitLocker, no al desbloquear un volumen. BitLocker permite desbloquear una unidad con cualquiera de los protectores disponibles en la unidad.</p>
</div>
<div>

</div>
<p>Si habilita esta configuración de Directiva, los usuarios podrán configurar una contraseña que cumpla los requisitos que usted defina. Para cumplir los requisitos de complejidad de la contraseña, haga clic en <strong> requerir complejidad de la contraseña </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar el perfil de validación de plataforma de TPM para configuraciones de firmware basadas en BIOS</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar cómo el equipo&#39;s hardware de seguridad de módulo de plataforma segura (TPM) protege la clave de cifrado de BitLocker. Esta configuración de Directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya se ha activado con la protección de TPM.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Esta configuración de directiva de grupo solo se aplica a equipos con configuraciones de BIOS o a equipos con firmware UEFI con un módulo de servicio de compatibilidad (CSM) habilitado. Los equipos que usan una configuración de firmware UEFI nativa almacenan diferentes valores en los registros de configuración de la plataforma (PCRs). Use la &quot; opción configurar el perfil de validación de plataforma de TPM para las configuraciones de firmware nativa UEFI para &quot; configurar el perfil PCR de TPM para equipos que usen el firmware UEFI nativo.</p>
</div>
<div>

</div>
<p>Si habilita esta configuración de Directiva antes de Activar BitLocker, puede configurar los componentes de arranque que el TPM validará antes de desbloquear el acceso a la unidad del sistema operativo cifrada con BitLocker. Si se cambia alguno de estos componentes mientras la protección de BitLocker está activa, el TPM no libera la clave de cifrado para desbloquear la unidad y el equipo en su lugar muestra la consola de recuperación de BitLocker y requiere que proporcione la contraseña de recuperación o la clave de recuperación para desbloquear la unidad.</p>
<p>Si deshabilita o no establece esta configuración de Directiva, BitLocker usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de configuración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el perfil de validación de plataforma TPM</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar cómo el equipo&#39;s hardware de seguridad de módulo de plataforma segura (TPM) protege la clave de cifrado de BitLocker. Esta configuración de Directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya se ha activado con la protección de TPM.</p>
<p>Si habilita esta configuración de Directiva antes de Activar BitLocker, puede configurar los componentes de arranque que el TPM validará antes de desbloquear el acceso a la unidad del sistema operativo cifrada con BitLocker. Si se cambia alguno de estos componentes mientras la protección de BitLocker está activa, el TPM no libera la clave de cifrado para desbloquear la unidad y el equipo en su lugar muestra la consola de recuperación de BitLocker y requiere que proporcione la contraseña de recuperación o la clave de recuperación para desbloquear la unidad.</p>
<p>Si deshabilita o no establece esta configuración de Directiva, BitLocker usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de configuración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar el perfil de validación de plataforma de TPM para configuraciones de firmware UEFI nativas</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite configurar cómo el equipo&#39;s hardware de seguridad de módulo de plataforma segura (TPM) protege la clave de cifrado de BitLocker. Esta configuración de Directiva no se aplica si el equipo no tiene un TPM compatible o si BitLocker ya se ha activado con la protección de TPM.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Esta configuración de directiva de grupo solo se aplica a los equipos con una configuración de firmware UEFI nativa.</p>
</div>
<div>

</div>
<p>Si habilita esta configuración de Directiva antes de Activar BitLocker, puede configurar los componentes de arranque que el TPM valida antes de desbloquear el acceso a la unidad del sistema operativo cifrada con BitLocker. Si se cambia alguno de estos componentes mientras la protección de BitLocker está activa, el TPM no libera la clave de cifrado para desbloquear la unidad y el equipo en su lugar muestra la consola de recuperación de BitLocker y requiere que proporcione la contraseña de recuperación o la clave de recuperación para desbloquear la unidad.</p>
<p>Si deshabilita o no establece esta configuración de Directiva, BitLocker usa el perfil de validación de plataforma predeterminado o el perfil de validación de plataforma especificado por el script de configuración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Restablecer datos de validación de plataforma después de la recuperación de BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Use esta configuración de directiva para controlar si los datos de validación de la plataforma se actualizan cuando Windows se inicia después de la recuperación de BitLocker.</p>
<p>Si habilita esta configuración de Directiva, los datos de validación de la plataforma se actualizarán cuando se inicie Windows después de la recuperación de BitLocker. Si deshabilita esta configuración de Directiva, los datos de validación de la plataforma no se actualizan cuando se inicia Windows después de la recuperación de BitLocker. Si no establece esta configuración de Directiva, los datos de validación de la plataforma se actualizarán cuando se inicie Windows después de la recuperación de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usar el perfil de validación de datos de configuración de arranque mejorado</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Esta configuración de directiva le permite elegir una configuración específica de datos de configuración de arranque (BCD) para comprobar durante la validación de la plataforma.</p>
<p>Si habilita esta configuración de Directiva, puede agregar opciones de configuración adicionales, quitar la configuración predeterminada o ambas. Si deshabilita esta configuración de Directiva, el equipo volverá a un perfil BCD similar al perfil BCD predeterminado usado por Windows 7. Si no establece esta configuración de Directiva, el equipo comprueba la configuración predeterminada de BCD de Windows.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Cuando BitLocker usa el arranque seguro para la validación de integridad de datos de configuración de arranque y plataforma (BCD), tal como se define en la &quot; Directiva permitir el arranque seguro para validación de integridad &quot; , &quot; se omite la Directiva usar Perfil de validación de datos de configuración de arranque mejorado &quot; .</p>
</div>
<div>

</div>
<p>La configuración que controla la depuración de arranque (0x16000010) siempre se valida y no surte efecto si se incluye en los campos proporcionados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración de la aplicación de directivas de cifrado</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Use esta configuración de directiva para configurar el número de días que los usuarios pueden posponer cumpliendo con las directivas de MBAM para la unidad del sistema operativo. El período de gracia comienza cuando el sistema operativo se detecta por primera vez como no conforme. Una vez transcurrido este período de gracia, los usuarios no pueden posponer la acción necesaria ni solicitar una exención de la misma.</p>
<p>Si el proceso de cifrado requiere la intervención del usuario, aparece un cuadro de diálogo que indica que los usuarios no pueden cerrar hasta que proporcionen la información necesaria.</p>
<p>Si deshabilita o no establece esta configuración, los usuarios no estarán obligados a cumplir con las directivas de MBAM.</p>
<p>Si no se necesita ninguna interacción por el usuario para agregar un protector, el cifrado comienza en segundo plano después de que venza el período de gracia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar el mensaje de recuperación y la URL de recuperación previa al arranque</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta configuración de directiva para configurar un mensaje de recuperación personalizado o para especificar una dirección URL que se muestra en la pantalla de recuperación de BitLocker anterior a la inicialización cuando la unidad del sistema operativo está bloqueada. Esta opción solo está disponible en los equipos cliente que ejecutan Windows 10.</p>
<p>Cuando esta directiva está habilitada, puede seleccionar una de estas opciones para el mensaje de recuperación previo al inicio:</p>
<ul>
<li><p><strong>Usar mensaje de recuperación personalizado </strong> : Seleccione esta opción para incluir un mensaje personalizado en la pantalla de recuperación de BitLocker anterior a la inicialización. En el <strong> cuadro de opción mensaje de recuperación personalizado </strong> , escriba el mensaje que desea que se muestre. Si también desea especificar una dirección URL de recuperación, puede incluirla como parte de su mensaje de recuperación personalizado.</p></li>
<li><p><strong>Usar una dirección URL de recuperación personalizada </strong> : Seleccione esta opción para reemplazar la dirección URL predeterminada que se muestra en la pantalla de recuperación de BitLocker anterior a la inicialización. En el <strong> cuadro de opción dirección URL de recuperación personalizada </strong> , escriba la dirección URL que desea que se muestre.</p></li>
<li><p><strong>Usar el mensaje de recuperación y la dirección URL predeterminados </strong> : Seleccione esta opción para mostrar el mensaje de recuperación de BitLocker predeterminado y la dirección URL en la pantalla de recuperación de BitLocker anterior a la inicialización. Si ha configurado previamente un mensaje de recuperación personalizado o una dirección URL y desea volver al mensaje predeterminado, debe habilitar esta directiva y seleccionar la <strong> opción usar el mensaje de recuperación predeterminado y la dirección URL </strong> .</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>No todos los caracteres e idiomas se admiten en preinicio. Le recomendamos que pruebe que los caracteres que use para el mensaje personalizado o la dirección URL se muestran correctamente en la pantalla de recuperación de BitLocker anterior a la inicialización.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### Definiciones de directiva de grupo de unidades extraíbles

En esta sección se describen las definiciones de directiva de grupo de unidades extraíbles de administración y supervisión de Microsoft BitLocker en el siguiente nodo GPO: directivas de **configuración del equipo** &gt; **Policies** &gt; **plantillas administrativas** de &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)** &gt; **unidad extraíble**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de directiva</th>
<th align="left">Información general y sugerencias de configuración de directiva de grupo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controlar el uso de BitLocker en unidades extraíbles</p></td>
<td align="left"><p>Configuración sugerida: <strong> habilitado</strong></p>
<p>Esta directiva controla el uso de BitLocker en unidades de datos extraíbles.</p>
<p>Haga clic en <strong> permitir a los usuarios aplicar la protección de BitLocker en unidades de datos extraíbles </strong> para permitir que los usuarios ejecuten el Asistente de configuración de BitLocker en una unidad de datos extraíble.</p>
<p>Haga clic en <strong> permitir a los usuarios suspender y descifrar BitLocker en unidades de datos extraíbles </strong> para permitir a los usuarios quitar el cifrado de unidad BitLocker de la unidad o para suspender el cifrado mientras se realiza el mantenimiento.</p>
<p>Cuando esta directiva está habilitada y hace clic en <strong> permitir que los usuarios apliquen la protección de BitLocker en unidades de datos extraíbles </strong> , el cliente de MBAM guarda la información de recuperación de las unidades extraíbles en el servidor de recuperación de claves MBAM y permite a los usuarios recuperar la unidad si se pierde la contraseña.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Denegar el acceso de escritura a unidades extraíbles no protegidas por BitLocker</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para permitir solo el permiso de escritura en unidades protegidas con BitLocker.</p>
<p>Cuando esta directiva está habilitada, todas las unidades de datos extraíbles en el equipo requieren cifrar para que se permita el permiso de escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir el acceso a unidades extraíbles protegidas con BitLocker desde versiones anteriores de Windows</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para permitir que las unidades fijas con el sistema de archivos FAT se desbloqueen y se vean en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Cuando esta Directiva no está configurada, las unidades extraíbles formateadas con el sistema de archivos FAT se pueden desbloquear en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP, y se puede ver su contenido. Estos sistemas operativos tienen permisos de solo lectura para las unidades protegidas con BitLocker.</p>
<p>Cuando la Directiva está deshabilitada, las unidades extraíbles formateadas con el sistema de archivos FAT no se pueden desbloquear y su contenido no se puede ver en equipos que ejecutan Windows Server 2008, Windows Vista, Windows XP o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el uso de la contraseña para unidades de datos extraíbles</p></td>
<td align="left"><p>Configuración sugerida: <strong> no configurada</strong></p>
<p>Habilite esta directiva para configurar la protección con contraseña en unidades de datos extraíbles.</p>
<p>Cuando esta Directiva no está configurada, las contraseñas son compatibles con la configuración predeterminada, que no incluye los requisitos de complejidad de las contraseñas y que solo requieren ocho caracteres.</p>
<p>Para una mayor seguridad, puede habilitar esta directiva y seleccionar <strong> requerir contraseña para la unidad de datos extraíbles </strong> , hacer clic en <strong> requerir complejidad de </strong> la contraseña y establecer la longitud mínima de la contraseña preferida <strong> </strong> .</p></td>
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


[Preparación del entorno para MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Requisitos previos de implementación de MBAM 2.5](mbam-25-deployment-prerequisites.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






