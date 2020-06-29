---
title: Administrar opciones de configuración de área de trabajo de MED-V
description: Administrar opciones de configuración de área de trabajo de MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826160"
---
# Administrar opciones de configuración de área de trabajo de MED-V


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 almacena su configuración de configuración en el registro. La información que incluimos aquí sobre el registro puede ayudarte a administrar mejor tus servicios de MED-V.

MED-V usa la siguiente ruta de búsqueda al buscar los valores de configuración resultantes:

MED-V busca primero en la Directiva de equipo.

Si no se encuentra el valor, MED-V busca en la Directiva de usuario.

Si no se encuentra el valor, MED-V busca en la sección HKEY \ _LOCAL \ _MACHINE \\System.

Si no se encuentra el valor, MED-V busca en la sección HKEY \ _CURRENT USER del registro.

Si aún no se encuentra el valor, MED-V usa el valor predeterminado.

Una práctica recomendada general es establecer el valor en el subárbol HKEY \ _LOCAL \ _MACHINE \\System o en la Directiva de equipo. Pero si desea que el usuario final pueda configurar una configuración determinada, debe dejarla.

**Nota**  
Antes de implementar sus áreas de trabajo de MED-V, puede usar un editor de scripts para cambiar el script de Windows PowerShell (archivo. PS1) que ha creado el paquete de área de trabajo MED-V. Para obtener más información, vea [Configuración avanzada mediante Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

Después de implementar sus áreas de trabajo de MED-V, puede cambiar determinadas opciones de configuración de MED-V modificando las entradas del registro.



En esta sección se enumeran todas las claves del registro MED-V configurables y se explican sus usos.

## Clave de diagnóstico


En la tabla siguiente se proporciona información acerca de los valores del registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre </th>
<th align="left">Tipo </th>
<th align="left">Datos/valor predeterminado </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 3</p></td>
<td align="left"><p>El tipo de información que se registra en el registro de eventos. Entre los niveles se incluyen los siguientes: 0 (ninguno), 1 (error), 2 (ADVERTENCIA), 3 (información), 4 (depurar).</p></td>
</tr>
</tbody>
</table>



## Tecla FTS


En la tabla siguiente se proporciona información acerca de los valores del registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Tipo</th>
<th align="left">Datos/valor predeterminado</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura la primera vez que el programa de instalación agrega automáticamente el usuario final al grupo&#39;s de administrador. 0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: la configuración de la primera vez no agrega automáticamente el usuario final al grupo&#39;s del administrador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: el programa de instalación agrega automáticamente el usuario final al grupo&#39;s de administrador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>MEDV* </p></td>
<td align="left"><p>La máscara de nombre de equipo que se usa para crear la máquina virtual invitada&#39;el nombre del equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>La máscara puede contener una etiqueta% username% para insertar el nombre de usuario como parte del nombre del equipo. Del mismo modo, la etiqueta% hostname% inserta el nombre del equipo host.</p>
<p>Cada &quot; # &quot; carácter de la máscara se reemplaza por un dígito aleatorio. Un carácter de asterisco (*) al final de la máscara se reemplaza por caracteres alfanuméricos aleatorios.</p>
<p>Se puede capturar un número específico de caracteres de% hostname% y% username% con corchetes. Por ejemplo, &quot; % username% [3] &quot; usaría los primeros tres caracteres del nombre de usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 90</p></td>
<td align="left"><p>El valor de tiempo de espera, en segundos, la primera vez que la configuración intenta eliminar la máquina virtual. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 120</p></td>
<td align="left"><p>El valor de tiempo de espera, en segundos, la primera vez que la instalación intenta desasociar el disquete virtual de la máquina virtual. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Dirección URL personalizable que se vincula a la página web interna y se muestra en los mensajes de diálogo de configuración por primera vez. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 900</p></td>
<td align="left"><p>El valor de tiempo de espera, en segundos, que la primera vez de la configuración espera el explorador de Windows. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>El mensaje se encuentra en el archivo de recursos </p></td>
<td align="left"><p>Mensaje personalizable que se muestra al usuario final cuando no se puede completar la configuración por primera vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 3</p></td>
<td align="left"><p>Número máximo de veces que MED-V intenta proporcionar derechos de grupo de usuarios finales. Si se supera el valor de reintentos especificado sin que sea posible conceder correctamente a un usuario final los derechos de grupo es probable que el error de preparación de la máquina virtual se someta al valor MaxRetryCount. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 300</p></td>
<td align="left"><p>El valor de tiempo de espera, en segundos, al otorgar derechos de grupo de usuarios. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Una lista de las rutas de los archivos de registro que MED-V recopila durante la configuración de la primera vez. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 120</p></td>
<td align="left"><p>El número máximo de horas que el usuario final puede posponer la configuración por primera vez. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 3</p></td>
<td align="left"><p>El número máximo de veces que MED-V intenta preparar una máquina virtual si cada intento finaliza en un error que no es de software. Cuando se produce un error en la preparación de la máquina virtual y se supera el número de reintentos de configuración por primera vez, MED-V informa al usuario final sobre el error y no le da la opción de reintentar. El recuento se vuelve a establecer cada vez que se inicia MED-V. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modo </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Valor predeterminado = desatendida</p></td>
<td align="left"><p>Configura la manera en que la configuración interactúa por primera vez con el usuario. Los valores posibles son los siguientes:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Asistida.</strong> El usuario final debe escribir la información durante la configuración por primera vez.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si creó el archivo Sysprep. inf para que la instalación mínima requiera que se complete la entrada del usuario, debe seleccionar el <strong> </strong> modo atendido o los problemas pueden ocurrir durante la primera configuración.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Desatendida </strong> . La máquina virtual no se muestra al usuario final durante la configuración de la primera vez, pero se solicita al usuario final antes de que se inicie la instalación por primera vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Silencioso </strong> . La máquina virtual no se muestra al usuario final en ningún momento durante la configuración por primera vez.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 15</p></td>
<td align="left"><p>El valor de tiempo de espera, en minutos, que debe completarse la primera configuración en el modo interactivo de configuración por primera vez al volver a intentar la instalación. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 45</p></td>
<td align="left"><p>El valor de tiempo de espera, en minutos, que la primera vez debe completarse la configuración en el modo interactivo de primera configuración. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>La fecha y hora, en formato de fecha UTC, que se puede posponer la primera configuración. Escriba en el formato &quot; AAAA-MM-DD HH: mm &quot; con las horas especificadas usando el estándar de reloj de 24 horas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>El mensaje se encuentra en el archivo de recursos </p></td>
<td align="left"><p>Mensaje personalizable que se muestra al usuario final cuando la primera vez la configuración debe volver a intentar la instalación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si la entrada ComputerName de la sección [UserData] del archivo Sysprep. inf en el invitado debe actualizarse de acuerdo con el ComputerNameMask especificado.   0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: la entrada ComputerName del archivo Sysprep. inf no se actualiza según el ComputerNameMask.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: la entrada ComputerName en el archivo Sysprep. inf se actualiza según el ComputerNameMask.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si la configuración de JoinDomain de la sección [Identification] del archivo Sysprep. inf del invitado debe actualizarse para que coincida con la configuración del host.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: la configuración de JoinDomain del archivo Sysprep. inf no se actualiza para coincidir con la del host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: la configuración de JoinDomain del archivo Sysprep. inf se actualiza para coincidir con la del host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si la configuración MachineObjectOU de la sección [Identification] del archivo Sysprep. inf en el invitado se actualiza para coincidir con el host.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: el valor de MachineObjectOU en el archivo Sysprep. inf no se actualiza para coincidir con la configuración del host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: el valor MachineObjectOU en el archivo Sysprep. inf se actualiza para coincidir con la configuración del host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetRegionalSettingsEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si la configuración de la sección [RegionalSettings] del archivo Sysprep. inf en el invitado se actualiza para coincidir con el host.  0 = falso; 1 = true.</p>
<div class="alert">
<strong>Nota</strong><br/><p>De forma predeterminada, la configuración de TimeZone en el invitado siempre se sincroniza con la configuración de la zona horaria en el host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: la configuración de la sección [RegionalSettings] del archivo Sysprep. inf del invitado no se actualiza para coincidir con el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: la configuración de la sección [RegionalSettings] del archivo Sysprep. inf en el invitado se actualiza para coincidir con el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si la configuración FullName y OrgName de la sección [UserData] del archivo Sysprep. inf en el invitado se actualiza para coincidir con la configuración del host.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: la configuración FullName y OrgName del archivo Sysprep. inf no se actualiza para coincidir con la configuración del host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: la configuración FullName y OrgName en el archivo Sysprep. inf se actualiza para coincidir con la configuración del host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>El mensaje se encuentra en el archivo de recursos </p></td>
<td align="left"><p>Mensaje personalizable que se muestra al usuario final cuando está listo para iniciar la configuración por primera vez. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 30</p></td>
<td align="left"><p>El valor de tiempo de espera, en segundos, que la primera vez de la configuración espera una respuesta de la máquina virtual para una operación de cancelación. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 60</p></td>
<td align="left"><p>El valor de tiempo de espera, en segundos, que la primera vez la configuración espera a que se cierre la máquina virtual. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 600</p></td>
<td align="left"><p>El tiempo, en segundos, antes de que se agote el tiempo de espera de la actualización del software de agente invitado de MED-V. Intervalo = 0 a 2147483647.</p></td>
</tr>
</tbody>
</table>



## Tecla UserExperience


En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience y la clave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Tipo</th>
<th align="left">Datos/valor predeterminado</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si la publicación de la aplicación del invitado en el host está habilitada.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: deshabilita la publicación de aplicaciones del invitado en el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: habilita la publicación de aplicaciones desde el invitado al host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si el uso compartido del dispositivo de audio e/s entre el invitado y el host está habilitado.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: deshabilita el uso compartido del dispositivo de e/s de audio entre el invitado y el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permite compartir el dispositivo de audio e/s entre el invitado y el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si el uso compartido del portapapeles entre el invitado y el host está habilitado.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: deshabilita el uso compartido del portapapeles entre el invitado y el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: permite compartir el portapapeles entre el invitado y el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 300</p></td>
<td align="left"><p>El tiempo, en segundos, antes de que el cuadro de diálogo iniciar por primera vez se agote el tiempo de espera. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HideVmTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 30</p></td>
<td align="left"><p>El valor de tiempo de espera, en minutos, que la ventana del equipo virtual de pantalla completa está oculta para el usuario final durante un largo intento de inicio de sesión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si el invitado debe iniciarse cuando el usuario final inicia sesión en el escritorio o cuando se inicia la primera aplicación invitado.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: el invitado se inicia cuando se inicia la primera aplicación invitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: el invitado se inicia cuando el usuario final inicia sesión en el escritorio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si el uso compartido de las impresoras entre el invitado y el host está habilitado.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: deshabilita el uso compartido de impresoras entre el invitado y el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permite el uso compartido de impresoras entre el invitado y el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1440</p></td>
<td align="left"><p>El valor de tiempo de espera, en minutos, que la primera vez de la configuración espera un reinicio. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Lista de direcciones URL especificada</p></td>
<td align="left"><p>Especifica una lista de direcciones URL que el host debe redirigir al invitado. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SmartCardLogonEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si las tarjetas inteligentes se pueden usar para autenticar usuarios en MED-V. 0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: no permite que las tarjetas inteligentes autentiquen a los usuarios finales en MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadero: permite que las tarjetas inteligentes autentiquen a los usuarios finales en MED-V.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Si SmartCardLogonEnabled y CredentialCacheEnabled están habilitados, SmartCardLogonEnabled invalida CredentialCacheEnabled.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si el uso compartido de tarjetas inteligentes entre el invitado y el host está habilitado.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: deshabilita el uso compartido de tarjetas inteligentes entre el invitado y el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permite el uso compartido de tarjetas inteligentes entre el invitado y el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si el uso compartido de dispositivos USB entre el invitado y el host está habilitado.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: deshabilita el uso compartido de dispositivos USB entre el invitado y el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permite el uso compartido de dispositivos USB entre el invitado y el host.</p></td>
</tr>
</tbody>
</table>



## Clave de VM


En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM y la clave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Tipo</th>
<th align="left">Datos/valor predeterminado</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CloseAction </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Predeterminado = HIBERNAr</p></td>
<td align="left"><p>La acción que realiza la máquina virtual después de que se cierre la última aplicación que se está ejecutando. Este valor se pasa por alto si el valor LogonStartEnabled está habilitado. Las opciones posibles son las siguientes:</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>HIBERNAr </strong> . Esta opción libera todos los recursos físicos que usa la máquina virtual, como la memoria y la CPU, y guarda el estado de todas las aplicaciones y operaciones en ejecución.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>SHUTDOWN </strong> . Esta opción cierra el sistema operativo invitado de manera segura y luego libera todos los recursos físicos que usa la máquina virtual, como la memoria y la CPU.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>DESACTIVAR </strong> . Esta opción puede provocar pérdida de datos porque es lo mismo que desactivar el botón de encendido o extraer el cable de alimentación en un equipo físico. Use esta opción solo si no puede usar una de las otras dos opciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>Una lista de los valores de memoria (MB) del invitado. Este valor se usa para determinar cuánta RAM está disponible para el invitado. En combinación con HostMemToGuestMem, se crea una tabla de búsqueda para determinar cuánta RAM se debe asignar en la máquina virtual invitada. Los valores posibles pueden estar comprendidos entre 128 y 3712.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 240</p></td>
<td align="left"><p>Número de minutos que MED-V debe mantener al invitado activo para su actualización automática, a partir de la hora especificada en el valor GuestUpdateTime. Intervalo = 0 a 1440. Al establecer este valor en cero (0), se deshabilita la funcionalidad de corrección de invitados.</p>
<p>Para obtener más información sobre las revisiones de invitado para las actualizaciones automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Administración de actualizaciones automáticas para áreas de trabajo de MED-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Valor predeterminado = 00:00</p></td>
<td align="left"><p>La hora y el minuto cada día en que MED-V debe reactivar al invitado para su actualización automática, mediante el estándar de reloj de 24 horas. Especificar la hora en el formato HH: MM  </p>
<p>Para obtener más información sobre las revisiones de invitado para las actualizaciones automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> Administración de actualizaciones automáticas para áreas de trabajo de MED-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>Una lista de los valores de memoria (MB) para el invitado, determinado por la RAM disponible en el host. En combinación con GuestMemFromHostMem, se crea una tabla de búsqueda para determinar cuánta RAM se debe asignar en la máquina virtual invitada. Los valores posibles pueden estar comprendidos entre 1024 y 16384.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Configura si la memoria asignada al invitado se calcula a partir de la memoria presente en el host.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: la memoria asignada al invitado no se calcula a partir de la memoria presente en el host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: la memoria asignada al invitado se calcula a partir de la memoria presente en el host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Memoria </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 512</p></td>
<td align="left"><p>La RAM (MB) que se debe asignar a la máquina virtual invitada. Esta configuración se pasa por alto si la configuración HostMemToGuestMemEnabled está habilitada. Intervalo = 128 a 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Configura si varios usuarios comparten el mismo área de trabajo de MED-V.  0 = falso; 1 = true.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: varios usuarios no comparten el mismo área de trabajo de MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: varios usuarios comparten el mismo área de trabajo de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NetworkingMode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Predeterminado = NAT</p></td>
<td align="left"><p>El tipo de conexión de red que se usa en el invitado. Los valores posibles son los siguientes:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Con puente </strong> . MED-V tiene su propia dirección de red, que normalmente se obtiene a través de DHCP.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>NAT </strong> . MED-V usa la traducción de direcciones de red (NAT) para compartir el host&#39;s IP para el tráfico saliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 600</p></td>
<td align="left"><p>Un valor de tiempo de espera general, en segundos, que MED-V espera a que se complete una tarea, como reiniciar y apagar. Intervalo = 0 a 2147483647.</p></td>
</tr>
</tbody>
</table>



## Configuración del registro de invitados


En esta sección se enumeran las claves del registro de invitado de MED-V configurables y se explican sus usos.

### 2

En la tabla siguiente se proporciona información sobre el valor del registro invitado asociado a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre </th>
<th align="left">Tipo </th>
<th align="left">Datos/valor predeterminado </th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 1 </p></td>
<td align="left"><p>Configura la forma en que MED-V controla las claves BufferPolicyReads y GroupPolicyMinTransferRate.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>De forma predeterminada, MED-V establece estas claves de la siguiente manera:</p>
<p>BufferPolicyReads = 1 y GroupPolicyMinTransferRate = 0.</p>
<p>Cree la clave EnableGPWorkarounds, si es necesario, y establezca la clave en cero si no quiere que MED-V cambie la configuración predeterminada de BufferPolicyReads y GroupPolicyMinTransferRate.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si el área de trabajo de MED-V se ejecuta en modo NAT, EnableGPWorkarounds afecta a las claves del registro BufferPolicyReads y GroupPolicyMinTransferRate. Si el área de trabajo de MED-V se ejecuta en modo puente, EnableGPWorkarounds solo afectará a la clave del registro BufferPolicyReads.</p>
</div>
<div>

</div>
<p>1 = verdadero: MED-V establece las claves BufferPolicyReads = 1 y GroupPolicyMinTransferRate = 0 (si se ejecuta en modo NAT) o simplemente BufferPolicyReads = 1 (si se ejecuta en modo BRIDGEd).</p>
<p>0 = falso: MED-V no realiza cambios en las claves BufferPolicyReads y GroupPolicyMinTransferRate.</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Administrar aplicaciones de área de trabajo de MED-V](manage-med-v-workspace-applications.md)

[Administrar la redirección de la dirección URL de MED-V](manage-med-v-url-redirection.md)

[Administrar la configuración del área de trabajo de MED-V](manage-med-v-workspace-settings.md)









