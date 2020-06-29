---
title: Información acerca de la configuración de cliente
description: Información acerca de la configuración de cliente
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814943"
---
# Información acerca de la configuración de cliente


El cliente de Microsoft Application Virtualization (App-V) 5,1 almacena su configuración en el registro. Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro. También puede configurar muchas acciones de cliente cambiando las entradas del registro. En este tema se enumeran los valores de configuración del cliente de App-V 5,1 y se explica su uso. Puede usar PowerShell para modificar la configuración del cliente. Para obtener más información sobre cómo usar PowerShell y App-V 5,1 [, consulte Administración de App-v 5,1 con PowerShell](administering-app-v-51-by-using-powershell.md).

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> Configuración de cliente de App-V 5,1


En la siguiente tabla se muestra información sobre la configuración del cliente de App-V 5,1:

|Nombre del valor de configuración | Marca de configuración | Descripción | Opciones de configuración | Valor de la clave del registro | Valores y claves de estado de directiva deshabilitados |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| PackageInstallationRoot | PACKAGEINSTALLATIONROOT | Especifica el directorio donde se instalarán todas las nuevas aplicaciones y actualizaciones. | Cadena | Streaming\PackageInstallationRoot | Valor de Directiva no escrito (igual que no configurado) |
| PackageSourceRoot | PACKAGESOURCEROOT | Invalida la ubicación de origen para descargar el contenido del paquete. | Cadena | Streaming\PackageSourceRoot | Valor de Directiva no escrito (igual que no configurado) |
| AllowHighCostLaunch | No está disponible. |Esta opción controla si las aplicaciones virtualizadas se inician en equipos con Windows 10 conectados a través de una conexión de red de uso medido (por ejemplo, 4G). | Verdadero (habilitado); Falso (Estado deshabilitado) | Streaming\AllowHighCostLaunch | ,0 |
| ReestablishmentRetries | No está disponible. | Especifica el número de veces que se debe volver a intentar una sesión interrumpida. | Entero (0-99) | Streaming\ReestablishmentRetries | Valor de Directiva no escrito (igual que no configurado) |
| ReestablishmentInterval | No está disponible. | Especifica el número de segundos entre intentos para restablecer una sesión eliminada. | Entero (0-3600) | Streaming\ReestablishmentInterval | Valor de Directiva no escrito (igual que no configurado) |
| LocationProvider | No está disponible. | Especifica el CLSID de una implementación compatible de la interfaz IAppvPackageLocationProvider. | Cadena | Streaming\LocationProvider | Valor de Directiva no escrito (igual que no configurado) |
| CertFilterForClientSsl | No está disponible. | Especifica la ruta de acceso a un certificado válido en el almacén de certificados. | Cadena | Streaming\CertFilterForClientSsl | Valor de Directiva no escrito (igual que no configurado) |
| VerifyCertificateRevocationList | No está disponible. | Comprueba el estado de revocación del certificado de servidor antes de hervir con HTTPS. | Verdadero (habilitado); Falso (Estado deshabilitado) | Streaming\VerifyCertificateRevocationList | ,0 |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | Especifica que el contenido del paquete transmitido no se guardará en el disco duro local. | Verdadero (habilitado); Falso (Estado deshabilitado) | Streaming\SharedContentStoreMode | ,0 |
| Nombre<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | PUBLISHINGSERVERNAME | Muestra el nombre del servidor de publicación. | Cadena | Publishing\Servers\ {serverId} \ FriendlyName | Valor de Directiva no escrito (igual que no configurado) |
| Dirección URL<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | PUBLISHINGSERVERURL | Muestra la URL del servidor de publicación. | Cadena | Publishing\Servers\ {serverId} \ URL | Valor de Directiva no escrito (igual que no configurado) |
| GlobalRefreshEnabled<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHENABLED | Permite la actualización global de publicaciones (booleana) | Verdadero (habilitado); Falso (Estado deshabilitado) | Publishing\Servers\ {serverId} \ GlobalEnabled | Falso |
| GlobalRefreshOnLogon<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHONLOGON | Desencadena una actualización de publicación global al iniciar sesión. Booleana | Verdadero (habilitado); Falso (Estado deshabilitado) | Publishing\Servers\ {serverId} \ GlobalLogonRefresh | Falso |
| GlobalRefreshInterval<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHINTERVAL | Especifica el intervalo de actualización de publicación mediante el GlobalRefreshIntervalUnit. Para deshabilitar la actualización del paquete, seleccione 0. | Entero (0-744) | Publishing\Servers\ {serverId} \ GlobalPeriodicRefreshInterval | ,0 |
| GlobalRefreshIntervalUnit <br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHINTERVALUNI | Especifica la unidad de intervalo (hour 0-23, Day 0-31). | 0 para la hora, 1 para el día | Publishing\Servers\ {serverId} \ GlobalPeriodicRefreshIntervalUnit | uno |
| UserRefreshEnabled<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | USERREFRESHENABLED | Habilita la actualización de publicaciones de usuario (booleana) | Verdadero (habilitado); Falso (Estado deshabilitado) | Publishing\Servers\ {serverId} \ UserEnabled | Falso |
| UserRefreshOnLogon<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | USERREFRESHONLOGON | Desencadena una actualización de publicación de usuario de inicio de sesión. Booleana<br>Recuento de palabras (con espacios): 60 | Verdadero (habilitado); Falso (Estado deshabilitado) | Publishing\Servers\ {serverId} \ UserLogonRefresh | Falso |
| UserRefreshInterval<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | USERREFRESHINTERVAL | Especifica el intervalo de actualización de publicación mediante el UserRefreshIntervalUnit. Para deshabilitar la actualización del paquete, seleccione 0. | Recuento de palabras (con espacios): 85<br>Entero (0-744 horas) | Publishing\Servers\ {serverId} \ UserPeriodicRefreshInterval | ,0 |
| UserRefreshIntervalUnit<br>**Nota:** Esta configuración no se puede modificar con el cmdLet **set-AppvclientConfiguration** . Debe usar el cmdlet **set-AppvPublishingServer** . | USERREFRESHINTERVALUNIT | Especifica la unidad de intervalo (hour 0-23, Day 0-31). | 0 para la hora, 1 para el día | Publishing\Servers\ {serverId} \ UserPeriodicRefreshIntervalUnit | uno |
| MigrationMode | MIGRATIONMODE | El modo de migración permite que el cliente de App-V modifique los accesos directos y los FTA para los paquetes creados con una versión anterior de App-V. | Verdadero (estado habilitado); Falso (Estado deshabilitado) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | Permite que el equipo que ejecuta el cliente de App-V 5,1 recopile y devuelva determinada información de uso para ayudar a mejorar aún más la aplicación. | 0 para deshabilitado; 1 para habilitado | SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable | ,0 | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | Habilita los scripts definidos en el manifiesto del paquete de los archivos de configuración que se deben ejecutar. | Verdadero (habilitado); Falso (Estado deshabilitado) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | Especifica las rutas de archivo relativas a% userprofile% que no se mueven con el perfil de un usuario. Ejemplo de uso:/ROAMINGFILEEXCLUSIONS = ' escritorio; mis imágenes ' | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | Especifica las rutas de registro que no se mueven con un perfil de usuario. Ejemplo de uso:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | Cadena | Integration\RoamingRegistryExclusions | Valor de Directiva no escrito (igual que no configurado) |
| IntegrationRootUser | No está disponible. | Especifica la ubicación para crear vínculos simbólicos asociados a la versión actual de un paquete publicado por usuario. todas las extensiones de aplicaciones virtuales, por ejemplo, los accesos directos y las asociaciones de tipos de archivo, señalarán a esta ruta. Si no especifica una ruta de acceso, los vínculos simbólicos no se usarán al publicar el paquete. Por ejemplo:%localappdata%\Microsoft\AppV\Client\Integration.| Cadena | Integration\IntegrationRootUser | Valor de Directiva no escrito (igual que no configurado) |
|IntegrationRootGlobal | No está disponible.| Especifica la ubicación para crear vínculos simbólicos asociados a la versión actual de un paquete publicado globalmente. todas las extensiones de aplicaciones virtuales, por ejemplo, los accesos directos y las asociaciones de tipos de archivo, señalarán a esta ruta. Si no especifica una ruta de acceso, los vínculos simbólicos no se usarán al publicar el paquete. Por ejemplo:%allusersprofile%\Microsoft\AppV\Client\Integration | Cadena | Integration\IntegrationRootGlobal | Valor de Directiva no escrito (igual que no configurado) |
| VirtualizableExtensions | No está disponible. | Una lista delimitada por comas de extensiones de nombre de archivo que se pueden usar para determinar si una aplicación instalada de forma local se puede ejecutar en el entorno virtual.<br>Cuando se crean accesos directos, FTAs y otros puntos de extensión durante la publicación, App-V comparará la extensión de nombre de archivo con la lista si la aplicación que está asociada con el punto de extensión está instalada de forma local. Si se encuentra la extensión, se agregará el parámetro de la línea de comandos **RunVirtual** y la aplicación se ejecutará prácticamente.<br>Para obtener más información sobre el parámetro **RunVirtual** , vea [ejecutar una aplicación instalada de forma local dentro de un entorno virtual con aplicaciones virtualizadas](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md). | Cadena | Integration\VirtualizableExtensions | Valor de Directiva no escrito |
| ReportingEnabled | No está disponible. | Permite al cliente devolver información a un servidor de informes. | Verdadero (habilitado); Falso (Estado deshabilitado) | Reporting\EnableReporting | Falso |
| ReportingServerURL | No está disponible. | Especifica la ubicación en el servidor de informes donde se guarda la información del cliente. | Cadena | Reporting\ReportingServer | Valor de Directiva no escrito (igual que no configurado) |
| ReportingDataCacheLimit | No está disponible. | Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes. El tamaño se aplica a la memoria caché en memoria. Cuando se alcance el límite, el archivo de registro se retirará. Establecer entre 0 y 1024. | Entero [0-1024] | Reporting\DataCacheLimit | Valor de Directiva no escrito (igual que no configurado) |
| ReportingDataBlockSize| No está disponible. | Especifica el tamaño máximo en bytes que se va a transmitir al servidor para notificar las solicitudes de carga. Esto puede ayudar a evitar errores de transmisión permanentes cuando el registro ha alcanzado un tamaño significativo. Establecer entre 1024 y sin límites. | Entero [1024-Unlimited] | Reporting\DataBlockSize | Valor de Directiva no escrito (igual que no configurado) |
| ReportingStartTime | No está disponible. | Especifica la hora de inicio del cliente para enviar datos al servidor de informes. Debe especificar un entero válido entre 0-23 que corresponda a la hora del día. De forma predeterminada, el **ReportingStartTime** comenzará en el día en curso a 10 P. M. o 22.<br>**Nota:** Debe configurar esta opción en una hora en la que es menos probable que los equipos que ejecutan el cliente de App-V 5,1 estén desconectados. | Entero (0-23) | Informes \ StartTime | Valor de Directiva no escrito (igual que no configurado) |
| ReportingInterval | No está disponible. | Especifica el intervalo de reintento que usará el cliente para volver a enviar datos al servidor de informes. | Integer | Reporting\RetryInterval | Valor de Directiva no escrito (igual que no configurado) |
| ReportingRandomDelay | No está disponible. | Especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes. Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre 0 y **ReportingRandomDelay** , y esperará la duración especificada antes de enviar los datos. Esto puede ayudar a evitar colisiones en el servidor. | Entero [0-ReportingRandomDelay] | Reporting\RandomDelay | Valor de Directiva no escrito (igual que no configurado) |
| EnableDynamicVirtualization<br>**Importante** Esta opción solo está disponible con App-V 5,0 SP2 o posterior. | No está disponible. | Permite virtualizar las extensiones de Shell, los objetos de ayuda del explorador y los controles de Active X admitidos y ejecutar las aplicaciones virtuales. | 1 (habilitado), 0 (deshabilitado) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization | |
| EnablePublishingRefreshUI<br>**Importante** Esta opción solo está disponible con App-V 5,0 SP2. | No está disponible. | Habilita la barra de progreso de actualización de publicaciones para el equipo que ejecuta el cliente de App-V 5,1. | 1 (habilitado), 0 (deshabilitado) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing | |
| HideUI<br>**Importante**  Esta opción solo está disponible con App-V 5,0 SP2.| No está disponible. | Oculta la barra de progreso de actualización de publicaciones. | 1 (habilitado), 0 (deshabilitado) | | |
| ProcessesUsingVirtualComponents | No está disponible. | Especifica una lista de rutas de procesos (que pueden contener caracteres comodín), que son candidatas para usar la virtualización dinámica (extensiones de Shell admitidas, objetos auxiliares del explorador y controles ActiveX). Solo los procesos cuya ruta completa coincida con uno de estos elementos pueden usar la virtualización dinámica. | Cadena | Virtualization\ProcessesUsingVirtualComponents | Cadena vacía. |






## Temas relacionados


[Implementación del secuenciador y del cliente de App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

[Cómo modificar la configuración del cliente de App-V 5.1 mediante la plantilla ADMX y la directiva de grupo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[Cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





