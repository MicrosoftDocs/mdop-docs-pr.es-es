---
title: Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones
description: Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819720"
---
# Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones


En la tabla siguiente se muestra una lista de todos los parámetros de la línea de comandos del instalador del cliente de virtualización de Microsoft Application Virtualization disponibles, sus valores y una breve descripción de cada parámetro. Los parámetros distinguen entre mayúsculas y minúsculas y deben escribirse como letras mayúsculas. Todos los valores de los parámetros deben ir entre comillas dobles.

**Nota**  
-   Para la versión 4,6 de App-V, los parámetros de la línea de comandos no se pueden usar durante una actualización de cliente.

-   Los parámetros *SWICACHESIZE* y *MINFREESPACEMB* no se pueden combinar en la línea de comandos. Si se usan ambas, se omitirá el parámetro *SWICACHESIZE* .



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Los</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indica si se habilitará la transmisión desde un archivo independientemente de cómo se haya configurado el cliente con el <em> </em> parámetro APPLICATIONSOURCEROOT. Si se establece en FALSE, el transporte no habilitará la transmisión por secuencias de archivos incluso si el OSD HREF o el <em> </em> parámetro APPLICATIONSOURCEROOT contienen una ruta de acceso de archivo.</p>
<p>Valores posibles:</p>
<ul>
<li><p>TRUE: la aplicación implementada manualmente se puede cargar desde el disco.</p></li>
<li><p>FALSE: todas las aplicaciones deben proceder de un servidor de streaming de origen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>APPLICATIONSOURCEROOT</em></p></td>
<td align="left"><p><em>URL </em> de rtsp://(para la entrega de paquetes dinámico)</p>
<p>File:// <em> URL </em> o <em> UNC </em> (para la carga desde paquetes de archivos)</p></td>
<td align="left"><p>Para habilitar un administrador o un sistema electrónico de distribución de software para asegurarse de que la carga de la aplicación se realice de conformidad con el esquema de administración de la topología, permite reemplazar el código base del OSD para el elemento HREF de la aplicación (la ubicación de origen). Si el valor es "", que es el valor predeterminado, se usa la configuración del archivo OSD existente.</p>
<p>Una dirección URL tiene varias partes:</p>
<p>&lt;Protocolo &gt; :// &lt; servidor &gt; : &lt; ruta de acceso del puerto &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</p>
<p>Una ruta de acceso UNC tiene tres partes:</p>
<p>&amp;lt; nombreDeEquipo &gt; &amp; lt; compartir carpeta &gt; &amp; lt; recursos&gt;</p>
<p>Si <em> </em> se especifica el parámetro APPLICATIONSOURCEROOT en un cliente, el cliente romperá la ruta de acceso UNC o URL de un archivo OSD a sus partes constituyentes y reemplazará las secciones OSD por las <em> secciones APPLICATIONSOURCEROOT correspondientes </em> .</p>
<div class="alert">
<strong>Importante</strong><br/><p>Asegúrese de usar el formato correcto al usar file://con una ruta de acceso UNC. El formato correcto es file:// &amp; lt; servidor &gt; &amp; lt; compartir &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>ICONSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>HTTP:// <em> URL </em> o https:// <em> URL</em></p></td>
<td align="left"><p>Permite a un administrador especificar una ubicación de origen para la recuperación de iconos para un paquete de aplicación de secuencia durante la publicación. Las raíces de origen de iconos admiten rutas de direcciones y direcciones URL (HTTP o HTTPS). Si el valor es "", que es el valor predeterminado, se usa la configuración del archivo OSD existente.</p>
<p>Una dirección URL tiene varias partes:</p>
<p>&lt;Protocolo &gt; :// &lt; servidor &gt; : &lt; ruta de acceso del puerto &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</p>
<p>Una ruta de acceso UNC tiene tres partes:</p>
<p>&amp;lt; nombreDeEquipo &gt; &amp; lt; compartir carpeta &gt; &amp; lt; recursos&gt;</p>
<div class="alert">
<strong>Importante</strong><br/><p>Asegúrese de usar el formato correcto al usar una ruta de acceso UNC. Los formatos aceptables son &amp; lt; servidor &gt; &amp; lt; compartir &gt; o &lt; letra de unidad &gt; : &amp; lt; carpeta &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>HTTP:// <em> URL </em> o https:// <em> URL</em></p></td>
<td align="left"><p>Permite a un administrador especificar una ubicación de origen para la recuperación de archivos OSD para un paquete de aplicación durante la publicación. Las raíces de origen OSD son compatibles con rutas UNC y direcciones URL (HTTP o HTTPS). Si el valor es "", que es el valor predeterminado, se usa la configuración del archivo OSD existente.</p>
<p>Una dirección URL tiene varias partes:</p>
<p>&lt;Protocolo &gt; :// &lt; servidor &gt; : &lt; ruta de acceso del puerto &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</p>
<p>Una ruta de acceso UNC tiene tres partes:</p>
<p>&amp;lt; nombreDeEquipo &gt; &amp; lt; compartir carpeta &gt; &amp; lt; recursos&gt;</p>
<div class="alert">
<strong>Importante</strong><br/><p>Asegúrese de usar el formato correcto al usar una ruta de acceso UNC. Los formatos aceptables son &amp; lt; servidor &gt; &amp; lt; compartir &gt; o &lt; letra de unidad &gt; : &amp; lt; carpeta &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Los desencadenadores de carga automática que definen los eventos que inician la carga automática de aplicaciones. Autoload usa implícitamente la transmisión por secuencias de fondo para permitir que la aplicación se cargue por completo en la caché.</p>
<p>El bloque de características principal se cargará lo antes posible. Los bloques de características restantes se cargarán en segundo plano para habilitar las operaciones en primer plano, como la interacción del usuario con las aplicaciones, para que tengan prioridad y ofrezcan un rendimiento óptimo.</p>
<div class="alert">
<strong>Nota</strong><br/><p>El <em> </em> parámetro AUTOLOADTARGET determina qué aplicaciones se cargan automáticamente. De forma predeterminada, los paquetes que se han usado se cargan automáticamente a menos que <em> </em> se establezca AUTOLOADTARGET.</p>
</div>
<div>

</div>
<p>Cada parámetro afecta al comportamiento de carga de la siguiente manera:</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> : la carga comienza cuando el usuario inicia sesión.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> : la carga comienza cuando el usuario inicia una aplicación.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> : la carga comienza cuando se actualiza una publicación.</p></li>
</ul>
<p>Los tres valores se pueden combinar. En el siguiente ejemplo, los desencadenadores de carga automática están habilitados al iniciar sesión el usuario y cuando se actualiza la publicación:</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONREFRESH</em></p>
<div class="alert">
<strong>Nota</strong><br/><p>Si el cliente está configurado con estos valores en la primera instalación, la carga previa no se desencadenará hasta la próxima vez que el usuario cierre sesión y vuelva a iniciar sesión.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>NADA</p>
<p>LAS</p>
<p>PREVUSED</p></td>
<td align="left"><p>Indica qué se cargará automáticamente cuando se produzcan desencadenadores de carga automática.</p>
<p>Valores posibles:</p>
<ul>
<li><p>NINGUNA: sin carga automática, independientemente de los desencadenadores que se pueden establecer.</p></li>
<li><p>ALL: si se habilita cualquier desencadenador de carga automática, todos los paquetes se cargan automáticamente, independientemente de si se han iniciado.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración se configura para paquetes individuales usando los comandos SFTMIME <strong> Agregar paquete </strong> y <strong> configurar paquete </strong> . Para obtener más información sobre estos comandos, consulte <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> referencia de comandos de SFTMIME </a> .</p>
</div>
<div>

</div></li>
<li><p>PREVUSED: si se habilita algún desencadenador de carga automático, carga solo los paquetes en los que se haya usado al menos una aplicación del paquete (es decir, que se hayan iniciado o que estén previamente en la memoria caché).</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Al instalar el cliente de App-V para usar una caché de solo lectura (por ejemplo, como implementación de servidor VDI), debes establecer el <em> parámetro AUTOLOADTARGET en </em> None para evitar que el cliente intente actualizar aplicaciones en la caché de solo lectura.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (valor predeterminado)</p>
<p>1 a 1439998560 minutos (intervalo)</p></td>
<td align="left"><p>Indica cuántos minutos se puede usar una aplicación en una operación de desconexión.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;pathname&gt;</p></td>
<td align="left"><p>Especifica el directorio de instalación del cliente de App-V.</p>
<p>Ejemplo: INSTALLDIR = &quot; c:\Archivos de Programa\microsoft Application Virtualization Client&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>OPTIn</em></p></td>
<td align="left"><p>AUTÉNTICA</p>
<p>“”</p></td>
<td align="left"><p>Los componentes del cliente de Microsoft Application Virtualization se actualizarán a través de Microsoft Update cuando las actualizaciones estén disponibles para el público en general. El agente de Microsoft Update instalado en sistemas operativos Windows exige que un usuario participe de forma explícita para usar el servicio. Esta suscripción es obligatoria solo una vez para todas las aplicaciones del dispositivo. Si ya ha elegido participar en Microsoft Update, los componentes de Microsoft Application Virtualization del dispositivo aprovecharán el servicio automáticamente.</p>
<p>Para la instalación desde la línea de comandos, el uso de Microsoft Update es de forma predeterminada (a menos que una aplicación anterior ya haya habilitado la participación en el dispositivo) debido al requisito de participar manualmente en Microsoft Update. Por lo tanto, para las instalaciones desde la línea de comandos, debe ser explícita. Establecer el parámetro de la línea de comandos <em> optin </em> en true obliga a que se establezca la opción de suscripción a Microsoft Update.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>REQUIREAUTHORIZATIONIFCACHED</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indica si la autorización siempre es necesaria, si una aplicación ya está en la caché.</p>
<p>Valores posibles:</p>
<ul>
<li><p>TRUE: la aplicación siempre debe estar autorizada en el inicio. Para las aplicaciones de transmisión RTSP, el token de autorización del usuario se envía al servidor para su autorización. En el caso de las aplicaciones basadas en archivos, las ACL de archivos determinan si un usuario puede acceder a la aplicación.</p></li>
<li><p>FALSO: siempre intenta conectar con el servidor. Si no se puede establecer una conexión con el servidor, el cliente seguirá permitiendo que el usuario inicie una aplicación que se haya cargado previamente en la memoria caché.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>Tamaño de caché en MB</p></td>
<td align="left"><p>Especifica el tamaño en megabytes de la caché del cliente. El tamaño predeterminado es 4096 MB y el tamaño máximo es de 1.048.576 MB (1 TB). El sistema comprueba el espacio disponible en el momento de la instalación, pero el espacio no está reservado.</p>
<p>Ejemplo: <strong> SWICACHESIZE = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>Nombre para mostrar</p></td>
<td align="left"><p>Especifica el nombre que se muestra en el servidor de publicación; obligatorio cuando <em> </em> se usa SWIPUBSVRHOST.</p>
<p>Ejemplo: <strong> SWIPUBSVRDISPLAY = &quot; entorno de producción&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[HTTP | RTSP</p></td>
<td align="left"><p>Especifica el tipo de servidor de publicación. El tipo de servidor predeterminado es Application Virtualization Server. El <strong> </strong> modificador/Secure no distingue entre mayúsculas y minúsculas.</p>
<ul>
<li><p>HTTP: servidor HTTP estándar</p></li>
<li><p>HTTP <strong> /Secure </strong> : servidor HTTP de seguridad mejorada</p></li>
<li><p>RTSP: Application Virtualization Server</p></li>
<li><p><strong>/Secure RTSP </strong> : servidor de virtualización mejorada de aplicaciones de seguridad</p></li>
</ul>
<p>Ejemplo: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>Dirección IP | nombre de host</p></td>
<td align="left"><p>Especifica la dirección IP del servidor de virtualización de aplicaciones o un nombre de host del servidor que se resuelve en la dirección IP del servidor&#39;s; obligatorio cuando <em> </em> se usa SWIPUBSVRDISPLAY.</p>
<p>Ejemplo: <strong> SWIPUBSVRHOST = &quot; SERVER01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>Número de Puerto</p></td>
<td align="left"><p>Especifica el puerto lógico usado por este servidor de virtualización de aplicaciones para escuchar las solicitudes del cliente (valor predeterminado = 554).</p>
<ul>
<li><p>Servidor HTTP estándar: predeterminado = 80.</p></li>
<li><p>Servidor HTTP de seguridad mejorada: valor predeterminado = 443.</p></li>
<li><p>Servidor de virtualización de aplicaciones: valor predeterminado = 554.</p></li>
<li><p>Servidor de virtualización de aplicaciones de seguridad mejorado: predeterminado = 322.</p></li>
</ul>
<p>Ejemplo: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>Nombre de ruta de acceso</p></td>
<td align="left"><p>Especifica la ubicación en el servidor de publicación del archivo que define las asociaciones de tipos de archivo (predeterminado =/). requerido cuando el <em> </em> valor del parámetro SWIPUBSVRTYPE es http.</p>
<p>Ejemplo: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[Activado | INICIAR</p></td>
<td align="left"><p>Especifica si el cliente realiza automáticamente una consulta en el servidor de publicación para las asociaciones de tipo de archivo y las aplicaciones cuando un usuario inicia sesión en el cliente (valor predeterminado = activado).</p>
<p>Ejemplo: <strong> SWIPUBSVRREFRESH = &quot; OFF&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>Directorio de datos global</p></td>
<td align="left"><p>Especifica el directorio en el que se almacenan los datos que no son específicos de usuarios concretos (predeterminado = C:\Documents and Settings\All Users\Documents).</p>
<p>Ejemplo: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>Directorio de datos de usuario</p></td>
<td align="left"><p>Especifica el directorio en el que se almacenan los datos específicos para usuarios concretos (valor predeterminado =% APPDATA%).</p>
<p>Ejemplo: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization Client&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>Letra de unidad preferida</p></td>
<td align="left"><p>Corresponde a la letra de unidad que seleccionó para la unidad virtual.</p>
<p>Ejemplo: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 – 4</p></td>
<td align="left"><p>Indica el nivel de registro en el que los mensajes de registro se escriben en el registro de eventos de NT. El valor indica un umbral de lo que se registra (es decir, se registra todo igual a o menor que ese valor). Por ejemplo, un valor de 0X3 (ADVERTENCIA) indica que se registran las advertencias (0X3), los errores (0X2) y los errores críticos (0x1).</p>
<p>Valores posibles:</p>
<ul>
<li><p>0 = = ninguno</p></li>
<li><p>1 = = crítico</p></li>
<li><p>2 = = error</p></li>
<li><p>3 = = ADVERTENCIA</p></li>
<li><p>4 = = información</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>En MB</p></td>
<td align="left"><p>Especifica la cantidad de espacio libre (en megabytes) que debe estar disponible en el host antes de que el tamaño de la caché pueda aumentar. En el ejemplo siguiente se configuraba el cliente para garantizar un mínimo de 5 GB de espacio libre en el disco antes de permitir que aumente el tamaño de la memoria caché. El valor predeterminado es 5000 MB de espacio libre disponible en el disco en el momento de la instalación.</p>
<p>Ejemplo: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Se usa cuando se ha aplicado la configuración del registro antes de implementar un cliente, por ejemplo, mediante una directiva de grupo. Cuando se implementa un cliente, establezca este parámetro en un valor de 1 de modo que no sobrescriba la configuración del registro.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Si se establece en un valor de 1, se omiten los siguientes parámetros de la línea de comandos del instalador de cliente:</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS y </strong> <strong> SWIUSERDATA </strong> .</p>
<p>Para obtener más información sobre la configuración de estos valores después de la instalación, consulte "cómo configurar la configuración del registro del cliente de App-V con la línea de comandos" en la guía de operaciones de Application Virtualization (App-V) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)

[Cómo actualizar el cliente de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-client.md)

[Referencia de comandos de SFTMIME](sftmime--command-reference.md)









