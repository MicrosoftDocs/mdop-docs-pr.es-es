---
title: Valores del registro de cliente de App-V
description: Valores del registro de cliente de App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819810"
---
# Valores del registro de cliente de App-V


El cliente de Microsoft Application Virtualization (App-V) almacena su configuración en el registro. Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro. También puede configurar muchas acciones de cliente cambiando las entradas del registro. En este tema se enumeran todas las claves de registro de cliente de Application Virtualization (App-V) y se explica su uso.

**Importante**  
En un equipo que ejecute un sistema operativo de 64 bits, las claves y los valores que se describen en las siguientes secciones estarán bajo HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.



## Clave de configuración


En la tabla siguiente se proporciona información acerca de los valores del registro asociados a la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

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
<th align="left">Datos (ejemplos)</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Cliente de escritorio de Microsoft Application Virtualization</p></td>
<td align="left"><p>No modificar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>4.5.0.xxx </p></td>
<td align="left"><p>No modificar. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controladores </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>Sftfs.sys </p></td>
<td align="left"><p>Si este valor de clave está presente, contiene el nombre del controlador que causó un error de detención la última vez que se inició el núcleo. Después de corregir el error de detención, debe eliminar este valor de clave para que sftlist se inicie.</p></td>
</tr>
<tr class="even">
<td align="left"><p>InstallPath </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>Predeterminado = C:\Archivos de Programa\microsoft Application Virtualization Client</p></td>
<td align="left"><p>La ubicación en la que el cliente está instalado. No modificar. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombrearchivoregistro </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>Default = CSIDL_COMMON_APPDATA \Microsoft\Application Virtualization Client\sftlog.txt</p></td>
<td align="left"><p>La ruta de acceso y el nombre del archivo de registro del cliente.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si está ejecutando una versión anterior a la de App-V 4,6, SP1 y modifica el nombre o la ubicación del archivo de registro, debe reiniciar el servicio sftlist para que el cambio surta efecto.</p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMinSeverity </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 4, informativo</p></td>
<td align="left"><p>Controla qué mensajes se escriben en el registro. El valor indica el umbral de lo que se registra: todo menor que o igual a ese valor se registra. Por ejemplo, un valor de 0X3 (ADVERTENCIA) indica que se registran las advertencias (0X3), los errores (0X2) y los errores críticos (0x1).</p>
<p>Intervalo de valores: 0X0 = ninguno, 0x1 = crítico, 0X2 = error, 0X3 = ADVERTENCIA, 0x4 = información (predeterminado), 0X5 = detallado.</p>
<p>El nivel de registro se puede configurar desde la consola de cliente de Application Virtualization (App-V) y desde el símbolo del sistema. En el símbolo del sistema, el comando sftlist.exe/verboselog aumentará el nivel de registro a verbose. Para obtener más información sobre los detalles de la línea de comandos, consulte</p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogRolloverCount</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 4</p></td>
<td align="left"><p>Define el número de copias de seguridad del archivo de registro que se conservan cuando se restablece. El intervalo válido es de 0 a 9999. El valor predeterminado es 4. Un valor de 0 significa que no se conservarán copias.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMaxSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 256</p></td>
<td align="left"><p>Define el tamaño máximo en megabytes (MB) que puede alcanzar el archivo de registro antes de restablecerlo. El tamaño predeterminado es 256 MB. Cuando se alcanza este tamaño, se forzará un restablecimiento de registro en el siguiente intento de escritura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SystemEventLogLevel</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0x4 (App-V 4,5)</p>
<p>Valor predeterminado = 0X3 (App-V 4,6)</p></td>
<td align="left"><p>Indica el nivel de registro en el que los mensajes de registro se escriben en el registro de eventos de NT. El valor indica un umbral de lo que se registra (es decir, se registra todo igual a o menor que ese valor). Por ejemplo, un valor de 0X3 (ADVERTENCIA) indica que se registran las advertencias (0X3), los errores (0X2) y los errores críticos (0x1).</p>
<p>Intervalo de valores</p>
<p>0X0 = ninguno</p>
<p>0x1 = crítico</p>
<p>0X2 = error</p>
<p>0X3 = Warning</p>
<p>0x4 = información (predeterminada)</p>
<p>0X5 = verbose</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowIndependentFileStreaming</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Indica si se habilitará la transmisión desde un archivo independientemente de cómo se haya configurado el cliente con el parámetro APPLICATIONSOURCEROOT. Si se establece en FALSE, el transporte no habilitará la transmisión por secuencias de archivos incluso si el OSD HREF o el parámetro APPLICATIONSOURCEROOT contienen una ruta de acceso de archivo.</p>
<p>0X0 = falso (predeterminado)</p>
<p>0x1 = verdadero</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ApplicationSourceRoot</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps</p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p>archivo://\uncserver\share\prodapps</p>
<p>archivo://\uncserver\share</p></td>
<td align="left"><p>Permite a un administrador o un sistema de distribución electrónica de software (ESD) garantizar la carga de la aplicación según el esquema de administración de la topología. Use este valor de clave para invalidar el código base del OSD para el elemento HREF (por ejemplo, la ubicación de origen) de una aplicación. La raíz de origen de la aplicación admite direcciones URL y formatos de ruta de acceso UNC (Convención de nomenclatura universal).</p>
<p>El formato correcto para la ruta de acceso de la dirección URL es protocolo: \ \ [puerto] [/path] [/], donde puerto y ruta de acceso son opcionales. Si no se especifica un puerto, se usa el puerto predeterminado para el protocolo. Solo se reemplaza la parte Protocol://Server: Port de la dirección URL de la OSD. </p>
<p>El formato correcto para la ruta de acceso UNC es \computername\sharefolder [carpeta] [], donde carpeta es opcional. El nombre del equipo puede ser un nombre de dominio completo (FQDN) o una dirección IP, y ShareFolder puede ser una letra de unidad. Solo se reemplaza la parte de \computername\sharefolder o letra de unidad de la ruta de acceso de la OSD. </p></td>
</tr>
<tr class="even">
<td align="left"><p>OSDSourceRoot</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Permite a un administrador especificar una ubicación de origen para la recuperación de archivos OSD para un paquete de aplicación de secuencia durante la publicación. Los formatos aceptados para el OSDSourceRoot incluyen rutas de dirección y direcciones URL (http o https).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IconSourceRoot</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Permite a un administrador especificar una ubicación de origen para la recuperación de archivos de icono para un paquete de aplicación de secuencia durante la publicación. Los formatos aceptados para el IconSourceRoot incluyen rutas de dirección y direcciones URL (http o https).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoadTriggers</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 5</p></td>
<td align="left"><p>Autoload es un parámetro de configuración de la Directiva de tiempo de ejecución del cliente que permite que el bloque de características secundario de una aplicación virtualizada se transmita automáticamente al cliente en segundo plano. Los desencadenadores de carga automática son marcas para indicar eventos que inician la carga automática de aplicaciones. Autoload usa implícitamente la transmisión por secuencias de fondo para permitir que la aplicación se cargue por completo en la caché. El bloque de características principal se cargará en primer lugar y los bloques de características restantes se cargarán en segundo plano para permitir que se realicen operaciones en primer plano, como la interacción del usuario con aplicaciones, y ofrezcan un rendimiento óptimo.</p>
<p>Valores de máscara de bits:</p>
<p>(0) nunca: no se establecen bits (el valor es 0), no se realizará la carga automática porque no hay ningún desencadenador configurado.</p>
<p>(1) Onlaunched: la carga se inicia cuando un usuario inicia una aplicación.</p>
<p>(2) alactualizar: la carga se iniciará cuando se publique la aplicación. Esto sucede siempre que el registro del paquete se agrega o se actualiza, por ejemplo, cuando se produce una actualización de publicación.</p>
<p>(4) Inicio de sesión: la carga se inicia cuando un usuario inicia sesión.</p>
<p>(5) Onlaunched y inicio de sesión: default.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AutoLoadTarget</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Indica qué se cargará automáticamente cuando se produzcan desencadenadores de carga automática. Valores de máscara de bits:</p>
<p>(0) ninguno: sin carga automática, independientemente de los desencadenadores que se pueden establecer.</p>
<p>(1) PreviouslyUsed (valor predeterminado): Si algún desencadenador de carga automático está habilitado, carga solo los paquetes en los que se ha usado al menos una aplicación del paquete, es decir, iniciado o prealmacenado previamente.</p>
<p>(2) todos: si se habilita algún desencadenador de carga automática, todas las aplicaciones del paquete (por paquete) o todos los paquetes (establecidos para el cliente) se cargarán automáticamente, tanto si se han iniciado como si no.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RequireAuthorizationIfCached</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Indica que siempre se necesita autorización, independientemente de si una aplicación ya está en la caché. Valores posibles:</p>
<p>0 = falso: siempre intenta conectar con el servidor. Si no se puede establecer una conexión con el servidor, el cliente seguirá permitiendo que el usuario inicie una aplicación que se haya cargado previamente en la memoria caché.</p>
<p>1 = true (valor predeterminado): la aplicación siempre debe estar autorizada en el inicio. Para las aplicaciones de transmisión RTSP, el token de autorización del usuario se envía al servidor para su autorización. Para las aplicaciones basadas en archivos, las ACL de archivos controlan si un usuario puede acceder a la aplicación.</p>
<p>Reinicie el servicio sftlist para que el cambio surta efecto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserDataDirectory </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>APPDATA</p></td>
<td align="left"><p>Ubicación donde se almacenan la configuración de la caché de iconos y del usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalDataDirectory </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>C:\Users\Public\Documents </p></td>
<td align="left"><p>Directorio que se debe usar para datos globales de App-V, incluidas las cachés de archivos OSD, archivos de iconos, información de acceso directo y recursos del guardián del programa, como los archivos. ini.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowCrashes </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0 o 1 </p></td>
<td align="left"><p>Default = 0: un valor de 0 significa que el cliente intenta detectar las excepciones de programa internas para que otras aplicaciones de usuario puedan recuperarse y continuar cuando se produzca un bloqueo. El valor 1 significa que el cliente permite que se produzcan las excepciones del programa interno para poder capturarlas en un depurador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CoreInternalTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>60</p></td>
<td align="left"><p>Tiempo de espera en segundos para las solicitudes IPC internas entre el núcleo y el front-end. No modificar. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DefaultSuiteCombineTime </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>base10</p></td>
<td align="left"><p>Este valor se usa para indicar la rapidez con la que un programa puede cerrarse y no generar ningún mensaje de error cuando se está ejecutando otra aplicación en el mismo conjunto. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SerializedSuiteLaunchTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 60000</p></td>
<td align="left"><p>Define cuánto tiempo en milisegundos esperará el cliente cuando intente serializar el programa en el mismo conjunto de programas. Si el cliente agota el tiempo de espera, el inicio del programa continuará, pero no se serializará. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ScriptTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>300</p></td>
<td align="left"><p>Tiempo de espera predeterminado en segundos para los scripts en el archivo OSD si WAIT = TRUE. Puede especificar los tiempos de espera de cada script con el tiempo de espera en lugar de esperar. Un valor de 0 significa no esperar, y 0xFFFFFFFF significa esperar indefinidamente. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordLogPath </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p></p></td>
<td align="left"><p>Si, en HKLM o HKCU, este valor contiene una ruta de acceso válida para un archivo de registro, SFTTray escribirá en este registro cuando se inicien los programas, se apague, se producirá un error de inicio y se entrará en el modo desconectado o se saldrá de él.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LaunchRecordMask </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x1A (26) registrar errores de inicio y de entrada y salida de modo desconectado.</p>
<p>0x1F (31) registra todo.</p>
<p>0X0 (0) no registra nada. </p></td>
<td align="left"><p>Especifica cuáles de los cinco eventos se registran (valores de máscara de la máscara):</p>
<p>1 para inicio de programa</p>
<p>2 para errores de inicio</p>
<p>4 para apagados</p>
<p>8 para entrar en modo desconectado</p>
<p>16 para salir del modo desconectado para volver a conectarse a un servidor</p>
<p>Agrega cualquier combinación de esos números para activar los mensajes respectivos. El valor predeterminado es 0x1F si no está en el registro. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordWriteTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 3000</p></td>
<td align="left"><p>Especifica en milisegundos cuánto debe esperar la bandeja al intentar escribir en el registro de inicio si otro proceso lo está usando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ImportSearchPath </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>d:\files; C:\Documents and settings\user1\SFTs </p></td>
<td align="left"><p>Una lista delimitada por puntos y comas de hasta cinco directorios para buscar archivos SFT portátiles antes de solicitar al usuario que seleccione un directorio. La barra diagonal inversa al final de paths es opcional. Este valor no está presente de forma predeterminada y debe establecerse manualmente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserImportPath</p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>D:\SFTs\ </p></td>
<td align="left"><p>Válido únicamente en HKCU. Última ubicación en la que el usuario ha buscado al encontrar un archivo SFT para la importación de paquete. Se establece automáticamente si el SFT se encuentra correctamente. Se usa en las importaciones sucesivas cuando se intenta ubicar automáticamente los archivos de SFT.</p></td>
</tr>
</tbody>
</table>



## Clave compartida


La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared controla los valores que se comparten en los componentes de App-V. En la tabla siguiente se proporciona información sobre los valores de registro asociados a la clave compartida.

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
<th align="left">Datos (ejemplos) </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DumpPath </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>Valor predeterminado = C:\ </p></td>
<td align="left"><p>Ruta de acceso predeterminada para crear archivos de volcado al generar un minivolcado en una excepción. El valor predeterminado es C:\ Si no se especifica. El instalador del cliente establece esta clave en el &lt; Directorio de datos global de virtualización de la aplicación &gt; \Dumps. El instalador del secuenciador establece esta clave en el directorio de instalación. </p></td>
</tr>
<tr class="even">
<td align="left"><p>DumpPathSizeLimit </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1000</p></td>
<td align="left"><p>Especifica la cantidad total máxima de espacio en megabytes que se puede usar para almacenar minivolcados. Valor predeterminado = 1000 MB.</p></td>
</tr>
</tbody>
</table>



## Clave de red


La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network controla una variedad de parámetros relacionados con la red. Esta clave la usa principalmente el agente de transporte de red. En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave de red.

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
<th align="left">Datos (ejemplos) </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Online</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Habilita o deshabilita el modo sin conexión. Si se establece en 0, el cliente no se comunicará con los servidores de administración de App-V o servidores de publicación. En las operaciones de desconexión, el cliente puede iniciar una aplicación cargada incluso cuando no está conectada a un servidor de administración de App-V. En el modo sin conexión, el cliente no intenta conectarse a un servidor de administración de App-V o de publicación. Debe permitir que las operaciones desconectadas puedan trabajar sin conexión. El valor predeterminado es 1 habilitado (en línea) y 0 está deshabilitado (sin conexión).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowDisconnectedOperation </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>Habilita o deshabilita la operación desconectada. El valor predeterminado es 1 habilitado y 0 está deshabilitado. Cuando se habilitan las operaciones de desconexión, el cliente de App-V puede iniciar una aplicación cargada incluso cuando no está conectada a un servidor de administración de App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FastConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1000</p></td>
<td align="left"><p>Este valor especifica el tiempo de espera de conexión TCP en milisegundos para determinar cuándo entrar en el modo de operaciones desconectado. Este valor se puede usar para invalidar el ConnectTimeout predeterminado de 20 segundos (el tiempo de espera de conexión de App-V para las transacciones de red) o el tiempo TCP del sistema de 25 segundos aproximadamente. Esto hace que el cliente esté en modo de operaciones desconectadas rápidamente. Aplicar en la próxima conexión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LimitDisconnectedOperation</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1 </p></td>
<td align="left"><p>Aplicable solo si AllowDisconnectedOperation es 1, habilitado. Este valor determina si habrá un límite de tiempo para el tiempo durante el cual se permitirá que el cliente opere en operaciones no conectadas. 1 = Limited. 0 = sin límites.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DOTimeoutMinutes</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 129600</p></td>
<td align="left"><p>Indica cuántos minutos se puede usar una aplicación en modo de operación desconectada.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Los valores válidos son de 1 a 999999 en días (1-1439998560 minutos). El valor predeterminado es 90 días o 129.600 minutos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocolo</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 8</p></td>
<td align="left"><p>Protocolo predeterminado para usar (TCP frente a SSL). Configurar en el cuadro de diálogo Opciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReadTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>veinte</p></td>
<td align="left"><p>Tiempo de espera de lectura para las transacciones de red, en segundos. No modificar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WriteTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>veinte</p></td>
<td align="left"><p>Tiempo de espera de escritura para las transacciones de red, en segundos. No modificar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>veinte</p></td>
<td align="left"><p>Conecte el tiempo de espera para las transacciones de red, en segundos. No modificar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>2</p></td>
<td align="left"><p>El número de veces para intentar restablecer una sesión interrumpida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>4,5</p></td>
<td align="left"><p>Número de segundos que se va a esperar entre intentos para restablecer una sesión interrumpida.</p></td>
</tr>
</tbody>
</table>



## Clave http


La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http controla los parámetros relacionados con la transmisión de http. Esta clave la usa principalmente el agente de transporte de red. En la tabla siguiente se proporciona información sobre los valores del registro asociados a la clave http.

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
<th align="left">Datos (ejemplos) </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>LaunchIfNotFound</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>Controla el comportamiento de las transmisiones por secuencias de HTTP cuando se puede establecer una conexión con el servidor HTTP y el archivo de paquete ya no existe en el servidor HTTP. Si el valor no existe o no se establece en 1, el cliente de App-V no le permite iniciar una aplicación que se haya cargado previamente en la memoria caché.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>uno</p></td>
<td align="left"><p>Si este valor se establece en 1, el cliente de App-V le permite iniciar una aplicación que se ha cargado previamente en la memoria caché.</p></td>
</tr>
</tbody>
</table>



## Clave del sistema de archivos


Los valores contenidos en la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS controlan los parámetros del sistema de archivos de App-V. En la tabla siguiente se proporciona información sobre los valores del registro asociados con la tecla AppFS.

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
<th align="left">Datos (ejemplos) </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FileSize </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>4096</p></td>
<td align="left"><p>Tamaño máximo en megabytes del archivo de caché del sistema de archivos. Si cambia este valor en el registro, debe establecer State en 0 y reiniciar. </p></td>
</tr>
<tr class="even">
<td align="left"><p>FileName </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd </p></td>
<td align="left"><p>Ubicación del archivo de caché del sistema de archivos. Si cambia este valor en el registro, debe dejar los mismos y reiniciar, o establecer el estado a 0 y reiniciar. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LetraDeUnidad </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>P: </p></td>
<td align="left"><p>Unidad donde se montará el sistema de archivos de App-V, si está disponible. Este valor lo establece el agente de escucha o el instalador, y lo lee el sistema de archivos. </p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x100 </p></td>
<td align="left"><p>Estado del sistema de archivos. Establezca en 0 y reinicie para borrar por completo la caché del sistema de archivos. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileSystemStorage </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>C:\Profiles\Joe\SG </p></td>
<td align="left"><p>Ruta de vínculos simbólicos, establezca en HKCU. No modifique (use el directorio de datos en configuración para cambiar). </p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalFileSystemStorage </p></td>
<td align="left"><p>Cadena </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\AppFS almacenamiento </p></td>
<td align="left"><p>Ruta de acceso a los datos del sistema de archivos global. No modificar. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPercentToLockInCache </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 90 </p></td>
<td align="left"><p>Especifica el porcentaje máximo del archivo de caché del sistema de archivos que puede bloquearse. No modificar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UnloadLeastRecentlyUsed</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 1</p></td>
<td align="left"><p>La característica de administración del espacio de caché del sistema de archivos usa un algoritmo LRU (el menos usado recientemente) y está habilitado de forma predeterminada. Si el espacio necesario para un nuevo paquete excedería el espacio libre disponible en la memoria caché, el cliente de App-V usa esta característica para determinar qué paquetes existentes pueden eliminar de la caché con el fin de hacer sitio para el nuevo paquete. El cliente elimina el paquete con la fecha de último acceso más antigua si es anterior al valor especificado en el valor de registro MinPkgAge. Los valores son 0 (deshabilitado) y 1 (predeterminado, habilitado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MinPackageAge</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>uno</p></td>
<td align="left"><p>Para determinar cuándo se puede seleccionar el paquete para descartar, establezca este valor del registro para que sea igual al número mínimo de días que desea que transcurran desde que se por última vez al paquete. Los paquetes que se han usado más recientemente no se descartan.</p></td>
</tr>
</tbody>
</table>



## Clave de permisos


Para ayudar a evitar que los usuarios hagan errores, los administradores pueden usar la clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions para controlar el acceso a algunas acciones para los usuarios no administrativos, por ejemplo, para impedir que los usuarios descarguen accidentalmente programas. Los usuarios con derechos administrativos pueden otorgarse a sí mismos cualquiera de estos permisos. En sistemas compartidos, como un sistema de host de sesión de escritorio remoto (antes Terminal Server), tenga cuidado al conceder permisos adicionales a los usuarios, ya que algunos de estos permisos permitirán a los usuarios controlar las aplicaciones que usan todos los usuarios del sistema. Los valores posibles para esta configuración son 1 (permitir) y 0 (no permitir).

La configuración de clave de permisos controla todas las interfaces que habilitan las acciones con nombre. Esto incluye el cuadro de diálogo Opciones, SFTTray y SFTMime. Esta configuración no afecta a los administradores. En la tabla siguiente se proporciona información sobre los valores del registro asociados a la clave de permisos.

Nombre tipo datos (ejemplos) Descripción ChangeFSDrive

DWORD

Valor predeterminado = 0

Un valor de 1 permite que los usuarios elijan una letra de unidad diferente para usarla como unidad del sistema de archivos.

ChangeCacheSize

DWORD

Valor predeterminado = 0

Un valor de 1 permite a los usuarios cambiar el tamaño de la caché.

ChangeLogSettings

DWORD

Valor predeterminado = 0

Un valor de 1 permite a los usuarios modificar el nivel de registro, cambiar su ubicación y restablecerlo a través de la interfaz de usuario.

AddApp

DWORD

Valor predeterminado = 0

Un valor de 1 permite a los usuarios agregar aplicaciones de forma explícita. Esto no afecta a las aplicaciones que se agregan mediante la actualización de publicaciones ni impide que los usuarios se inicien (y agregan implícitamente) aplicaciones que aún no se han agregado. Los valores son 0 o 1.

LoadApp 

DWORD 

,0

No permite que un usuario cargue una aplicación. Este es el valor predeterminado para los hosts de sesión de escritorio remoto. Si es un usuario móvil, es posible que desee cargar completamente las aplicaciones en la caché para usarlas durante la operación de desconexión o el modo sin conexión. Para transmitir aplicaciones desde el servidor de administración de App-V o del servidor de streaming de App-V, debe estar conectado a un servidor para cargar las aplicaciones.

uno

Permite que un usuario cargue una aplicación. Este es el valor predeterminado para los escritorios de Windows. 

UnloadApp 

DWORD 

,0

No permite que un usuario descargue una aplicación. Al cargar o descargar un paquete, todas las aplicaciones del paquete se cargan o se quitan de la caché.

uno

Permite a un usuario descargar una aplicación. 

LockApp 

DWORD 

,0

No permite que un usuario bloquee y desbloquee una aplicación. Este es el valor predeterminado para los hosts de sesión de escritorio remoto. No se puede quitar una aplicación bloqueada de la caché para hacer sitio para nuevas aplicaciones. Para quitar una aplicación bloqueada del escritorio de App-V o del cliente para servicios de escritorio remoto (antes, Terminal Services), debe desbloquearla.

uno

Permite que un usuario bloquee y desbloquee una aplicación. Este es el valor predeterminado para los escritorios de Windows. 

ManageTypes 

DWORD 

,0

No permite que un usuario agregue, edite o quite asociaciones de tipo de archivo solo para ese usuario. Este es el valor predeterminado para los hosts de sesión de escritorio remoto. 

uno

Permite a un usuario agregar, editar y quitar asociaciones de tipos de archivo para ese usuario únicamente y no de forma global. Este es el valor predeterminado para los escritorios de Windows. 

RefreshServer 

DWORD 

,0

No permite que un usuario desencadene una actualización de la configuración MIME. Este es el valor predeterminado para los hosts de sesión de escritorio remoto. 

uno

Permite a un usuario desencadenar una actualización de la configuración de MIME. Este es el valor predeterminado para los escritorios de Windows. 

UpdateOSDFile

DWORD

Valor predeterminado = 0

Un valor de 1 permite a un usuario usar un archivo OSD modificado.

ImportApp 

DWORD 

,0

No permite que un usuario importe aplicaciones en la memoria caché. La diferencia entre cargar e importar es que cuando se desencadena una carga, el cliente obtiene el paquete de la ubicación configurada en la URL OSD, ASR o override. Al usar Import, debe especificarse una ubicación desde la que obtener el paquete. 

uno

Permite a un usuario importar aplicaciones en la caché. 

ChangeRefreshSettings

DWORD

Valor predeterminado = 0

Un valor de 1 permite a los usuarios modificar la configuración de actualización de los servidores (actualizar al iniciar sesión y actualizar periódicamente). Esto no implica que el usuario pueda modificar otras opciones de configuración del servidor (Path, host, etc.).

ManageServers

DWORD

Valor predeterminado = 0

El valor 1 permite al usuario agregar, editar y quitar servidores, excepto editar la configuración de actualización, que está controlada por el permiso ChangeRefreshSettings.

PublishShortcut

DWORD

Valor predeterminado = 0

Un valor de 1 permite a los usuarios publicar accesos directos a través de la interfaz de usuario. Esto no afecta a los métodos abreviados que se publican durante una actualización de publicación.

ViewAllApplications

DWORD

Valor predeterminado = 0

Un valor de 1 muestra todas las aplicaciones a través de la interfaz de usuario; de lo contrario, solo se mostrarán las aplicaciones del usuario.

RepairApp

DWORD

Valor predeterminado = 1

Un valor de 1 permite al usuario usar la acción de reparación en las aplicaciones de SFTMime o en la consola de administración de clientes. Al reparar una aplicación, se elimina la configuración de usuario personalizada y se restaura la configuración predeterminada. Esta acción no cambia ni elimina accesos directos ni asociaciones de tipos de archivo, y no quita la aplicación de la caché.

ClearApp

DWORD

Valor predeterminado = 1

Un valor de 1 permite al usuario usar la acción borrar en las aplicaciones de SFTMime o en la consola de administración de clientes. Al borrar una aplicación de la consola, ya no podrá usarla. Sin embargo, la aplicación permanece en la caché y sigue estando disponible para otros usuarios en el mismo sistema. Después de una actualización de publicación, las aplicaciones desactivadas volverán a estar disponibles.

DeleteApp

DWORD

Valor predeterminado = 0

Un valor de 1 permite al usuario usar la acción eliminar en las aplicaciones de SFTMime o en la consola de administración de clientes. Al eliminar una aplicación, la aplicación seleccionada dejará de estar disponible para los usuarios de ese cliente. Los accesos directos y las asociaciones de los tipos de archivo se eliminan y la aplicación se elimina de la memoria caché. Sin embargo, si otra aplicación hace referencia a datos en la caché del sistema de archivos o a los datos de configuración de la aplicación seleccionada, estos elementos no se eliminarán.

Después de una actualización de publicación, las aplicaciones eliminadas volverán a estar disponibles para usted.

ToggleOfflineMode

DWORD

Un valor de 1 permite a los usuarios seleccionar la ejecución del cliente en modo sin conexión. En el modo sin conexión, el cliente de virtualización de aplicaciones puede iniciar una aplicación cargada incluso cuando no está conectada a un servidor de virtualización de aplicaciones.



## Configuración personalizada


La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contiene valores específicos para los componentes de front-end. Todas las configuraciones personalizadas se almacenan como cadenas. En la siguiente tabla se proporciona información sobre los valores del registro asociados a la clave CustomSettings.

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
<th align="left">Datos (ejemplos) </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TrayErrorDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 30 </p></td>
<td align="left"><p>Tiempo en segundos durante el que el área de notificación de Application Virtualization mostrará mensajes de error como &quot; error al iniciar &quot; . Valor mínimo de 1. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TraySuccessDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valor predeterminado = 10 </p></td>
<td align="left"><p>Tiempo en segundos en el que el área de notificación de appvmed mostrará mensajes de éxito, como el &quot; lanzamiento &quot; de Word o el &quot; cierre de Excel &quot; . Si es 0, se suprimirán esos mensajes. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayVisibility</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0</p></td>
<td align="left"><p>0 = Mostrar bandeja cuando se usan aplicaciones virtualizadas.</p>
<p>1 = Mostrar bandeja siempre.</p>
<p>2 = nunca Mostrar bandeja.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TrayShowRefresh</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Cuando está presente y se establece en un valor de 1, permite que las aplicaciones de actualización de elemento de menú se muestren en el menú de bandeja y que el usuario pueda obtener acceso a ellas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayShowLoad</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Cuando está presente y se establece en un valor de 1, permite que las aplicaciones de carga de elemento de menú se muestren en el menú de bandeja y que el usuario pueda obtener acceso a ellas.</p></td>
</tr>
</tbody>
</table>



## Configuración de informes


La clave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contiene valores específicos para la creación de informes en un servidor de administración de App-V. En la tabla siguiente se proporciona información acerca de los valores de registro asociados a la clave de informe.

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
<th align="left">Datos (ejemplos) </th>
<th align="left">Descripción </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DataCacheLimit</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 20</p></td>
<td align="left"><p>Este valor especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes. El tamaño se aplica a la memoria caché en memoria. Cuando se alcance el límite, el archivo de registro se retirará. Cuando se agrega un nuevo registro (en la parte inferior de la lista), se eliminarán uno o más de los registros más antiguos (en la parte superior de la lista) para dejar espacio. Se registrará una advertencia en el registro del cliente y en el registro de eventos la primera vez que se produzca, y no se registrará de nuevo hasta que la caché se haya borrado correctamente durante la transmisión y el registro se haya rellenado de nuevo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BlockSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 65536</p></td>
<td align="left"><p>Este valor especifica el tamaño máximo en bytes que se va a transmitir al servidor a la vez en la actualización de publicaciones, para evitar errores de transmisión permanentes cuando el registro haya alcanzado un tamaño significativo. El valor predeterminado es 65536. Cuando se transmiten datos del informe al servidor, un bloque de registros de la aplicación (menor o igual que el tamaño de bloque en bytes de datos XML) se quitará de la caché y se enviará al servidor. Cada bloque incluirá los datos generales de los clientes y los datos de la lista de paquetes globales, y estos no se verán incluidos en los cálculos de tamaño de bloque. es posible que haya una lista de paquetes extremadamente grande para que se produzcan errores de transmisión con un ancho de banda bajo o conexiones no confiables.</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Referencia del cliente de virtualización de aplicaciones](application-virtualization-client-reference.md)









