---
title: Información acerca de la configuración de cliente
description: Información acerca de la configuración de cliente
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814942"
---
# Información acerca de la configuración de cliente


El cliente de Microsoft Application Virtualization (App-V) 5,0 almacena su configuración en el registro. Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro. También puede configurar muchas acciones de cliente cambiando las entradas del registro. En este tema se enumeran los valores de configuración del cliente de App-V 5,0 y se explica su uso. Puede usar PowerShell para modificar la configuración del cliente. Para obtener más información sobre cómo usar PowerShell y App-V 5,0 [, consulte Administración de App-v con PowerShell](administering-app-v-by-using-powershell.md).

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> Configuración de cliente de App-V 5,0


En la siguiente tabla se muestra información sobre la configuración del cliente de App-V 5,0:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de configuración</th>
<th align="left">Marca de configuración</th>
<th align="left">Descripción</th>
<th align="left">Opciones de configuración</th>
<th align="left">Valor de la clave del registro</th>
<th align="left">Valores y claves de estado de directiva deshabilitados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>PACKAGEINSTALLATIONROOT</p></td>
<td align="left"><p>Especifica el directorio donde se instalarán todas las nuevas aplicaciones y actualizaciones.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>Invalida la ubicación de origen para descargar el contenido del paquete.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Esta opción controla si las aplicaciones virtualizadas se inician en equipos Windows 8 conectados a través de una conexión de red de uso medido (por ejemplo, 4G).</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el número de veces que se debe volver a intentar una sesión interrumpida.</p></td>
<td align="left"><p>Entero (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el número de segundos entre intentos para restablecer una sesión eliminada.</p></td>
<td align="left"><p>Entero (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autocargar</p></td>
<td align="left"><p>Autocargar</p></td>
<td align="left"><p>Especifica cómo App-V debe cargar automáticamente los paquetes nuevos en un equipo específico.</p></td>
<td align="left"><p>(0X0) ninguno; (0x1) previamente usado; (0X2) todos</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocationProvider</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el CLSID de una implementación compatible de la interfaz IAppvPackageLocationProvider.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica la ruta de acceso a un certificado válido en el almacén de certificados.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Comprueba el estado de revocación del certificado de servidor antes de hervir con HTTPS.</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>Especifica que el contenido del paquete transmitido no se guardará en el disco duro local.</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>Muestra el nombre del servidor de publicación.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ FriendlyName</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dirección URL</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>Muestra la URL del servidor de publicación.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ URL</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>Permite la actualización global de publicaciones (booleana)</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalEnabled</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>Desencadena una actualización de publicación global al iniciar sesión. Booleana</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalLogonRefresh</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>Especifica el intervalo de actualización de publicación mediante el GlobalRefreshIntervalUnit. Para deshabilitar la actualización del paquete, seleccione 0.</p></td>
<td align="left"><p>Entero (0-744</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>Especifica la unidad de intervalo (hour 0-23, Day 0-31). </p></td>
<td align="left"><p>0 para la hora, 1 para el día</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>uno</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>Habilita la actualización de publicaciones de usuario (booleana)</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserEnabled</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>Desencadena una actualización de publicación de usuario de inicio de sesión. Booleana</p>
<p>Recuento de palabras (con espacios): 60</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserLogonRefresh</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>Especifica el intervalo de actualización de publicación mediante el UserRefreshIntervalUnit. Para deshabilitar la actualización del paquete, seleccione 0.</p>
<p>Recuento de palabras (con espacios): 85</p></td>
<td align="left"><p>Entero (0-744 horas)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserPeriodicRefreshInterval</p></td>
<td align="left"><p>,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esta configuración no se puede modificar con el <strong> cmdLet Set-AppvclientConfiguration </strong> . Debe usar el <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>Especifica la unidad de intervalo (hour 0-23, Day 0-31). </p></td>
<td align="left"><p>0 para la hora, 1 para el día</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>uno</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MigrationMode</p></td>
<td align="left"><p>MIGRATIONMODE</p></td>
<td align="left"><p>El modo de migración permite que el cliente de App-V modifique los accesos directos y los FTA para los paquetes creados con una versión anterior de App-V.</p></td>
<td align="left"><p>Verdadero (estado habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>Permite que el equipo que ejecuta el cliente de App-V 5,0 recopile y devuelva determinada información de uso para ayudar a mejorar aún más la aplicación.</p></td>
<td align="left"><p>0 para deshabilitado; 1 para habilitado</p></td>
<td align="left"><p>SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</p></td>
<td align="left"><p>,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>Habilita los scripts definidos en el manifiesto del paquete de los archivos de configuración que se deben ejecutar.</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>Especifica las rutas de archivo relativas a% userprofile% que no se mueven con un perfil de usuario&#39;s. Ejemplo de uso:/ROAMINGFILEEXCLUSIONS =&#39;Desktop; mis imágenes&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>Especifica las rutas de registro que no se mueven con un perfil de usuario. Ejemplo de uso:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica la ubicación para crear vínculos simbólicos asociados a la versión actual de un paquete publicado por usuario. todas las extensiones de aplicaciones virtuales, por ejemplo, los accesos directos y las asociaciones de tipos de archivo, señalarán a esta ruta. Si no especifica una ruta de acceso, los vínculos simbólicos no se usarán al publicar el paquete. Por ejemplo:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica la ubicación para crear vínculos simbólicos asociados a la versión actual de un paquete publicado globalmente. todas las extensiones de aplicaciones virtuales, por ejemplo, los accesos directos y las asociaciones de tipos de archivo, señalarán a esta ruta. Si no especifica una ruta de acceso, los vínculos simbólicos no se usarán al publicar el paquete. Por ejemplo:%allusersprofile%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Una lista delimitada por comas de extensiones de nombre de archivo que se pueden usar para determinar si una aplicación instalada de forma local se puede ejecutar en el entorno virtual.</p>
<p>Cuando se crean accesos directos, FTAs y otros puntos de extensión durante la publicación, App-V comparará la extensión de nombre de archivo con la lista si la aplicación que está asociada con el punto de extensión está instalada de forma local. Si se encuentra la extensión, se <strong> </strong> agregará el parámetro de la línea de comandos RunVirtual y la aplicación se ejecutará prácticamente.</p>
<p>Para obtener más información sobre <strong> el </strong> parámetro RunVirtual, vea <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> ejecutar una aplicación instalada de forma local dentro de un entorno virtual con aplicaciones virtualizadas </a> .</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>Valor de Directiva no escrito</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Permite al cliente devolver información a un servidor de informes.</p></td>
<td align="left"><p>Verdadero (habilitado); Falso (Estado deshabilitado)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica la ubicación en el servidor de informes donde se guarda la información del cliente.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes. El tamaño se aplica a la memoria caché en memoria. Cuando se alcance el límite, el archivo de registro se retirará. Establecer entre 0 y 1024.</p></td>
<td align="left"><p>Entero [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el tamaño máximo en bytes que se va a transmitir al servidor para notificar las solicitudes de carga. Esto puede ayudar a evitar errores de transmisión permanentes cuando el registro ha alcanzado un tamaño significativo. Establecer entre 1024 y sin límites.</p></td>
<td align="left"><p>Entero [1024-Unlimited]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica la hora de inicio del cliente para enviar datos al servidor de informes. Debe especificar un entero válido entre 0-23 que corresponda a la hora del día. De forma predeterminada, el ReportingStartTime comenzará <strong> </strong> en el día en curso a 10 P. M. o 22.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Debe configurar esta opción en una hora en la que es menos probable que los equipos que ejecutan el cliente de App-V 5,0 estén desconectados.</p>
</div>
<div>

</div></td>
<td align="left"><p>Entero (0-23)</p></td>
<td align="left"><p>Informes \ StartTime</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el intervalo de reintento que usará el cliente para volver a enviar datos al servidor de informes.</p></td>
<td align="left"><p>Integer</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes. Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre 0 y <strong> ReportingRandomDelay, </strong> y esperará la duración especificada antes de enviar los datos. Esto puede ayudar a evitar colisiones en el servidor.</p></td>
<td align="left"><p>Entero [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>Valor de Directiva no escrito (igual que no configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>Importante</strong><br/><p>Esta opción solo está disponible con App-V 5,0 SP2 o posterior.</p>
</div>
<div>

</div></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Permite virtualizar las extensiones de Shell, los objetos de ayuda del explorador y los controles de Active X admitidos y ejecutar las aplicaciones virtuales.</p></td>
<td align="left"><p>1 (habilitado), 0 (deshabilitado)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>Importante</strong><br/><p>Esta opción solo está disponible con App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Habilita la barra de progreso de actualización de publicaciones para el equipo que ejecuta el cliente de App-V 5,0.</p></td>
<td align="left"><p>1 (habilitado), 0 (deshabilitado)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>Importante</strong><br/><p>Esta opción solo está disponible con App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Oculta la barra de progreso de actualización de publicaciones.</p></td>
<td align="left"><p>1 (habilitado), 0 (deshabilitado)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>No está disponible.</p></td>
<td align="left"><p>Especifica una lista de rutas de procesos (que pueden contener caracteres comodín), que son candidatas para usar la virtualización dinámica (extensiones de Shell admitidas, objetos auxiliares del explorador y controles ActiveX). Solo los procesos cuya ruta completa coincida con uno de estos elementos pueden usar la virtualización dinámica.</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Cadena vacía.</p></td>
</tr>
</tbody>
</table>








## Temas relacionados


[Implementación del secuenciador y del cliente de App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

[Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[Cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md)









