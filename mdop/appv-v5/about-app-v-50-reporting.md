---
title: Acerca de la generación de informes de App-V5.0
description: Acerca de la generación de informes de App-V5.0
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815021"
---
# Acerca de la generación de informes de App-V5.0


Microsoft Application Virtualization (App-V) 5,0 incluye una característica de creación de informes integrada que le ayuda a recopilar información sobre los equipos que ejecutan el cliente de App-V 5,0, así como información sobre el uso de paquetes de aplicaciones virtuales. Puede usar esta información para generar informes desde una base de datos centralizada.

## <a href="" id="---------app-v-5-0-reporting-overview"></a> Información general de informes de App-V 5,0


En la siguiente lista se muestra el flujo de trabajo de alto nivel end-to-end para informes en App-V 5,0.

1.  El servidor de informes de Microsoft Application Virtualization (App-V) 5,0 tiene los siguientes requisitos previos:

    -   Rol de servidor Web de Internet Information Services (IIS)

    -   Rol de autenticación de Windows (en **IIS/seguridad**)

    -   SQL Server instalado y ejecutándose con SQL Server Reporting Services (SSRS)

    Para confirmar que SQL Server Reporting Services está en ejecución, vea `http://localhost/Reports` en un explorador Web como administrador en el servidor que hospedará informes de App-V 5,0. Aparecerá la Página principal de SQL Server Reporting Services.

2.  Instale el servidor de informes de App-V 5,0 y la base de datos asociada. Para obtener más información sobre cómo instalar el servidor de informes [, vea Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md). Configure la hora en la que el equipo que ejecuta el cliente de App-V 5,0 debe enviar datos al servidor de informes.

3.  Si no usa un sistema electrónico de distribución de software, como Configuration Manager, para ver los informes, puede definir informes en SQL Server Reporting Services. Descargue los informes predefinidos de appvshort desde el centro de descarga en <https://go.microsoft.com/fwlink/?LinkId=397255> .

    **Nota:**  Si está usando la integración de Configuration Manager con App-V 5,0, la mayoría de los informes se generan desde Configuration Manager en lugar de desde App-V 5,0.

     

4.  Después de importar el módulo de PowerShell App-V 5,0 usando `Import-Module AppvClient` como administrador, habilite el cliente de App-v 5,0. Este cmdlet de PowerShell de ejemplo habilita informes de App-V 5,0:

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    Para enviar inmediatamente datos del informe de App-V 5,0, ejecute `Send-AppvClientReport` en el cliente de App-v 5,0.

    Para obtener más información sobre cómo instalar el cliente de App-V 5,0 con informes habilitados, consulte [acerca de](about-client-configuration-settings.md)la configuración del cliente. Para administrar los informes de App-V 5,0 con Windows PowerShell, vea [Cómo habilitar la creación de informes en el cliente de App-v 5,0 con PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).

5.  Después de que el servidor de informes reciba los datos del cliente de App-V 5,0, envía los datos a la base de datos de informes. Cuando la base de datos recibe y procesa los datos del cliente, se envía una respuesta correcta al servidor de informes y, a continuación, se envía una notificación al cliente de App-V 5,0.

6.  Cuando el cliente de App-V 5,0 recibe la notificación de éxito, vacía la memoria caché de datos para ahorrar espacio.

    **Nota:**  De forma predeterminada, la caché se borra después de que el servidor confirme la recepción de los datos. Puede configurar manualmente el cliente para guardar la caché de datos.

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> Preguntas más frecuentes sobre App-V 5,0 Server

En la siguiente tabla se muestran respuestas a las preguntas más frecuentes sobre los informes de App-V 5,0

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pregunta</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>¿Cuál es la frecuencia con que se envía la información de informes a la base de datos de informes?</p></td>
<td align="left"><p>La frecuencia depende de la configuración de la tarea de informes en el equipo que ejecuta el cliente de App-V 5,0. Debe configurar la frecuencia o el intervalo para enviar los datos de informes. Los informes de App-V 5,0 no están habilitados de forma predeterminada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>¿Qué información se almacena en la base de datos del servidor de informes?</p></td>
<td align="left"><p>En la siguiente lista se muestra lo que se almacena en la base de datos de informes:</p>
<ul>
<li><p>El sistema operativo que se ejecuta en el equipo que ejecuta el cliente de App-V 5,0: nombre de host, versión, Service Pack, tipo-cliente/servidor, arquitectura de procesador.</p></li>
<li><p>Información del cliente de App-V 5,0: versión.</p></li>
<li><p>Lista de paquetes publicados: GUID, GUID de versión, nombre.</p></li>
<li><p>Información de uso de la aplicación: nombre, versión, servidor de streaming, usuario (domain\alias), GUID de versión de paquete, estado y hora de inicio, hora de cierre.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>¿Cuál es el volumen medio de información que se envía al servidor de informes?</p></td>
<td align="left"><p>Depende. En la siguiente lista se muestran los tres conjuntos de datos enviados al servidor de informes:</p>
<ol>
<li><p>Sistema operativo y información del cliente de App-V 5,0. ~ 150 bytes, cada vez que se envían estos datos.</p></li>
<li><p>Lista de paquetes publicados. ~ 7 KB para 30 paquetes. Esto se envía solo cuando la lista de paquetes se actualiza con una actualización de publicación, lo cual se hace con poca frecuencia; Si no hay ningún cambio, esta información no se envía.</p></li>
<li><p>Información de uso de aplicaciones virtuales: aproximadamente 0,25 KB por evento. El recuento de apertura y cierre como un evento si ambos ocurren antes de enviar la información. Al enviar mediante una tarea programada, solo se envían al servidor los datos desde la última carga correcta. Si se envía manualmente a través del cmdlet de PowerShell, hay un argumento opcional que controla si los datos necesitan volver a enviarse la próxima vez, ese argumento es <strong> DeleteOnSuccess </strong> .</p>
<p></p>
<p>Así, por ejemplo, si se abren y cierran veinte aplicaciones y se programa que la información se envíe diariamente, el tráfico diario típico debe ser de 0,15 KB + 20 x 0,25 KB o de 5KB/usuario</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>¿Se pueden programar informes?</p></td>
<td align="left"><p>Sí. Además de enviar informes de forma manual mediante cmdlets de PowerShell ( <strong> send-AppvClientReport </strong> ), la tarea se puede programar para que se produzca de forma automática. Existen dos formas de programar los informes:</p>
<ol>
<li><p>Usar cmdlets de PowerShell- <strong> set-AppvClientConfiguration </strong> . Por ejemplo:</p>
<p>Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</a></p>
<p></p>
<p>Para obtener una lista completa de las opciones de configuración del cliente, consulte Acerca de la configuración del <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> cliente </a> y busque las siguientes entradas: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay, ReportingInterval </strong> <strong> </strong> .</p>
<p></p></li>
<li><p>Mediante la Directiva de grupo. Si se distribuye con el controlador de dominio, la configuración es la misma que la mencionada anteriormente.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La configuración de directiva de grupo invalida la configuración local establecida mediante PowerShell.</p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> Informes de cliente de App-V 5,0


Para usar los informes de 5,0 de App-V, debe instalar y configurar el cliente de App-V 5,0. Una vez instalado el cliente, use el cmdlet **de PowerShell Set-AppVClientConfiguration** o la **plantilla ADMX** para configurar los informes. Los cmdlets de características de creación de informes están disponibles usando el siguiente vínculo y están precedidos por los **informes**. Para obtener una lista completa de las opciones de configuración de cliente, consulte Acerca de los [parámetros de configuración de cliente](about-client-configuration-settings.md). En la siguiente sección se proporcionan ejemplos de la configuración de informes de cliente de App-V 5,0 con PowerShell.

### Configuración de informes de clientes de App-V con PowerShell

En los siguientes ejemplos se muestra cómo los parámetros de PowerShell pueden configurar las características de informes del cliente de App-V 5,0.

**Nota**  
La siguiente tarea de configuración también se puede configurar con la configuración de directiva de grupo de la plantilla App-V 5,0 ADMX. Para obtener más información sobre el uso de la plantilla ADMX, consulte [Cómo modificar la configuración de cliente de App-V 5,0 con la plantilla ADMX y la Directiva de grupo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).
 


**Para habilitar los informes e iniciar la recopilación de datos en el equipo que ejecuta el cliente de App-V 5,0**:

`Set-AppVClientConfiguration –ReportingEnabled 1`

**Para configurar el cliente para que envíe datos automáticamente a un servidor de informes específico**:

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

En este ejemplo se configura el cliente para que envíe automáticamente los datos de informes a la dirección URL del servidor de informes <strong> http://MyReportingServer:MyPort/ </strong> . Además, los datos de informes se enviarán todos los días entre 8:00 y 8:30 PM, según el retraso aleatorio generado para la sesión.

**Para limitar el tamaño de la caché de datos en el cliente**, haga lo siguiente:

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

Configura el tamaño máximo de la caché de informes en el equipo que ejecuta el cliente de App-V 5,0 en 100 MB. Si se alcanza el límite de la caché antes de que los datos se envíen al servidor, el inicio de sesión y los datos se sobrescribirán según sea necesario.

**Para configurar el tamaño del bloque de datos transmitido a través de la red entre el cliente y el servidor**:

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

Especifica el bloque de datos máximo que el cliente envía a 10240 MB.

### Tipos de datos recopilados

En la siguiente tabla se muestran los tipos de información que puede recopilar mediante el uso de informes de App-V 5,0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Información del cliente</th>
<th align="left">Información de paquete</th>
<th align="left">Uso de aplicaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre de host</p></td>
<td align="left"><p>Nombre del paquete</p></td>
<td align="left"><p>Horas de inicio y finalización</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión de cliente de App-V 5,0</p></td>
<td align="left"><p>Versión del paquete</p></td>
<td align="left"><p>Estado de ejecución</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquitectura del procesador</p></td>
<td align="left"><p>Origen del paquete</p></td>
<td align="left"><p>Estado de apagado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión del sistema operativo</p></td>
<td align="left"><p>Porcentaje en caché</p></td>
<td align="left"><p>Nombre de la aplicación</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nivel de Service Pack</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Versión de la aplicación</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de sistema operativo</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Nombre de usuario</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Grupo de conexión</p></td>
</tr>
</tbody>
</table>
 


El cliente recopila y guarda estos datos en un formato **. XML** . La caché de datos está oculta de forma predeterminada y requiere derechos de administrador para abrir el archivo XML.

### Enviar datos al servidor

Puede configurar el equipo que ejecuta el cliente de App-V 5,0 para que envíe datos automáticamente al servidor de informes especificado. Para especificar el servidor, use el cmdlet **set-AppvClientConfiguration** con la siguiente configuración:

-   ReportingEnabled

-   ReportingServerURL

-   ReportingStartTime

-   ReportingInterval

-   ReportingRandomDelay

Una vez configurada la configuración anterior, debe crear una tarea programada. La tarea programada se pondrá en contacto con el servidor especificado por la configuración de **ReportingServerURL** y iniciará la transferencia. Si desea enviar datos de forma manual fuera de las horas programadas, use el siguiente cmdlet de PowerShell:

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

Si el servidor de informes se ha configurado previamente, se puede omitir el parámetro **– URL** . Como alternativa, si los datos se deben enviar a una ubicación alternativa, especifique una dirección URL diferente para invalidar el **ReportingServerURL** configurado para esta recopilación de datos.

El parámetro **-DeleteOnSuccess** indica que si la transferencia se realiza correctamente, la caché de datos se borrará. Si no se especifica, la caché no se borrará.

### Recopilación de datos manual

También puede usar el cmdlet **send-AppVClientReport** para recopilar datos de forma manual. Esta solución es útil con o sin un servidor de informes existente. En la siguiente lista se muestra información sobre la recopilación de datos con o sin un servidor de informes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Con un servidor de informes</th>
<th align="left">Sin un servidor de informes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Si ya tiene un servidor de informes de App-V 5,0, cree una tarea o una secuencia de comandos personalizada. Especificar que el cliente envíe los datos a la ubicación especificada con la frecuencia que desee.</p></td>
<td align="left"><p>Si no tiene un servidor de informes de App-V 5,0, use el <strong> parámetro – URL </strong> para enviar los datos a un recurso compartido especificado. Por ejemplo:</p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p>El ejemplo anterior enviará los datos de informes a la <strong> &lt; &gt; Ubicación de \MyShare\MyData/Strong indicada por el <strong> parámetro-URL </strong> . Una vez enviados los datos, la caché se borra.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si se especifica una ubicación que no sea el servidor de informes, los datos se envían con el <strong> formato. XML </strong> sin ningún procesamiento adicional.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### Creación de informes

Para recuperar información del informe y crear informes con App-V 5,0, debe usar uno de los siguientes métodos:

-   **Microsoft SQL Server Reporting Services (SSRs)** : Microsoft SQL Server Reporting Services está disponible con Microsoft SQL Server. SSRS no se instala al instalar el servidor de informes de App-V 5,0. Debe implementarse por separado para generar los informes asociados.

    Use el siguiente vínculo para obtener más información sobre cómo usar [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).

-   **Scripting** : puede generar informes mediante scripting directamente con la base de datos de informes de App-V 5,0. Por ejemplo:

    **Procedimiento almacenado:**

    **spProcessClientReport** se ha programado para ejecutarse a medianoche o 12:00 a.m.

    Para ejecutar el procedimiento almacenado programado Microsoft SQL Server, debe estar ejecutándose el Agente SQL Server de Microsoft. Debe asegurarse de que el Agente SQL Server de Microsoft esté configurado para **iniciar automáticamente**. Para obtener más información [, consulte AUTOSTART SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).

    El procedimiento almacenado también se crea al usar los scripts de base de datos de App-V 5,0.

También debe asegurarse de que el **número máximo de conexiones simultáneas** del servicio Web del servidor de informes esté establecido como un valor que el servidor podrá administrar sin afectar a la disponibilidad. El número recomendado de **conexiones simultáneas máximas** para el **servicio Web de informes** es **10.000**.






## Temas relacionados


[Implementación del servidor de App-V 5.0](deploying-the-app-v-50-server.md)

[Cómo instalar el servidor de informes en un equipo independiente y conectarlo a la base de datos](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





