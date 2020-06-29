---
title: Publicación de aplicaciones e interacción de clientes
description: Publicación de aplicaciones e interacción de clientes
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814735"
---
# Publicación de aplicaciones e interacción de clientes


Este artículo ofrece información técnica sobre las operaciones de cliente de App-V comunes y su integración con el sistema operativo local.

-   [Archivos de paquete de App-V creados por el secuenciador](#bkmk-appv-pkg-files-list)

-   [¿Qué hay en el archivo de appv?](#bkmk-appv-file-contents)

-   [Ubicaciones de almacenamiento de datos de cliente de App-V](#bkmk-files-data-storage)

-   [Registro del paquete](#bkmk-pkg-registry)

-   [Comportamiento del almacén de paquetes de App-V](#bkmk-pkg-store-behavior)

-   [Datos y registro de itinerancia](#bkmk-roaming-reg-data)

-   [Administración del ciclo de vida de aplicaciones de cliente de App-V](#bkmk-clt-app-lifecycle)

-   [Integración de paquetes de App-V](#bkmk-integr-appv-pkgs)

-   [Procesamiento de configuración dinámica](#bkmk-dynamic-config)

-   [Ensamblados en paralelo](#bkmk-sidebyside-assemblies)

-   [Registro de cliente](#bkmk-client-logging)

Para obtener información de referencia adicional, consulte [Página de descarga de recursos de documentación de Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-pkg-files-list"></a>Archivos de paquete de App-V creados por el secuenciador


El secuenciador crea paquetes de App-V y genera una aplicación virtualizada. El proceso de secuencia crea los siguientes archivos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Archivo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>. appv</p></td>
<td align="left"><ul>
<li><p>El archivo de paquete principal, que contiene los activos y la información de estado capturados del proceso de secuencia.</p></li>
<li><p>Arquitectura del archivo de paquete, información de publicación y registro en un formulario con token que se puede volver a aplicar a un equipo y a un usuario específico después de su entrega.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>. MS</p></td>
<td align="left"><p>Contenedor de implementación ejecutable que puede usar para implementar archivos. appv de forma manual o mediante una plataforma de implementación de terceros.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Archivo que se usa para personalizar los parámetros de publicación predeterminados de todas las aplicaciones de un paquete que se implementa globalmente para todos los usuarios de un equipo que ejecuta el cliente de App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Archivo que se usa para personalizar los parámetros de publicación de todas las aplicaciones en un paquete que se ha implementado en un usuario específico en un equipo que ejecuta el cliente de App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Resumen de los mensajes resultantes del proceso de secuenciación, incluidos los drivers omitidos, los archivos y las ubicaciones del registro.</p></td>
</tr>
<tr class="even">
<td align="left"><p>. CAB</p></td>
<td align="left"><p><em>Opcional: </em> archivo de acelerador de paquetes que se usa para volver a crear automáticamente un paquete de aplicación virtual secuenciado previamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Opcional: </em> archivo de plantilla de secuenciador que se usa para conservar la configuración del secuenciador reutilizada.</p></td>
</tr>
</tbody>
</table>

 

Para obtener información sobre la secuenciación, consulte [Guía de secuenciación de Application virtualization 5,0](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-file-contents"></a>¿Qué hay en el archivo de appv?


El archivo de appv es un contenedor que almacena archivos XML y no XML juntos en una sola entidad. Este archivo se crea a partir del formato AppX, que se basa en el estándar convenciones de empaquetado abierto (OPC).

Para ver el contenido del archivo de appv, haga una copia del paquete y, a continuación, cambie el nombre del archivo copiado a una extensión ZIP.

El archivo de appv contiene la carpeta y los archivos siguientes, que se usan al crear y publicar una aplicación virtual:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Tipo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Raíz</p></td>
<td align="left"><p>Carpeta de archivos</p></td>
<td align="left"><p>Directorio que contiene el sistema de archivos de la aplicación virtualizada que se captura durante la secuencia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types]. XML</p></td>
<td align="left"><p>Archivo XML</p></td>
<td align="left"><p>Lista de los tipos de contenido principales en el archivo de appv (por ejemplo, DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>Archivo XML</p></td>
<td align="left"><p>Diseño del archivo de appv, que usa los elementos archivo, bloque y BlockMap que permiten la ubicación y validación de archivos en el paquete de App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>Archivo XML</p></td>
<td align="left"><p>Metadatos del paquete que contiene la información necesaria para agregar, publicar e iniciar el paquete. Incluye puntos de extensión (asociaciones de tipo de archivo y accesos directos), así como los nombres y GUID asociados con el paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>Archivo XML</p></td>
<td align="left"><p>Lista de los archivos capturados durante la secuenciación, incluidos los atributos (por ejemplo, directorios, archivos, directorios opacos, directorios vacíos y nombres largos y cortos).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>Archivo XML</p></td>
<td align="left"><p>Información sobre el equipo de secuencia (versión del sistema operativo, versión de Internet Explorer, versión de .NET Framework) y proceso (actualización, versión de paquete).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry. dat</p></td>
<td align="left"><p>Archivo DAT</p></td>
<td align="left"><p>Claves y valores de registro capturados durante el proceso de secuenciación para el paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>Archivo XML</p></td>
<td align="left"><p>Lista de archivos para el bloque de características principal y de publicación. El bloque de características de publicación contiene los archivos ICO y las partes necesarias de los archivos (EXE y DLL) para publicar el paquete. Cuando está presente, el bloque de características principal incluye los archivos que se han optimizado para la transmisión por secuencias durante el proceso de secuenciación.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a>Ubicaciones de almacenamiento de datos de cliente de App-V


El cliente de App-V realiza tareas para garantizar que las aplicaciones virtuales se ejecuten correctamente y funcionen como aplicaciones instaladas de forma local. El proceso de apertura y ejecución de aplicaciones virtuales requiere la asignación desde el sistema de archivos virtual y el registro para garantizar que la aplicación tenga los componentes necesarios de una aplicación tradicional prevista por los usuarios. En esta sección se describen los activos necesarios para ejecutar aplicaciones virtuales y se muestra una lista de la ubicación en la que App-V almacena los activos.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Ubicación</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tienda de paquetes</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Ubicación predeterminada de los archivos de paquete de solo lectura</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catálogo de máquina</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contiene documentos de configuración por máquina</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catálogo de usuarios</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contiene documentos de configuración por usuario</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copias de seguridad de accesos directos</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Almacena los puntos de integración anteriores que permiten la restauración al volver a publicar el paquete</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Itinerancia de copia en escritura (vaca)</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Ubicación de itinerancia grabable para la modificación de paquetes</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copiar en escritura (COW) local</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Ubicación de no movilidad grabable para la modificación de paquetes</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registro del equipo</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contiene información de estado del paquete, incluyendo VReg para equipos o paquetes publicados globalmente (sección equipo)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registro de usuario</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contiene información de estado del paquete de usuario, incluido VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Clases de registro de usuario</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contiene información adicional sobre el estado de un paquete de usuario</p></td>
</tr>
</tbody>
</table>

 

Los detalles adicionales de la tabla se muestran en la sección siguiente y en todo el documento.

### Tienda de paquetes

El cliente de App-V administra los activos de las aplicaciones montados en el almacén de paquetes. Esta ubicación de almacenamiento predeterminada es `%ProgramData%\App-V` , pero puede configurarla durante o después de la instalación mediante el `Set-AppVClientConfiguration` comando PowerShell, que modifica el registro local ( `PackageInstallationRoot` valor de la `HKLM\Software\Microsoft\AppV\Client\Streaming` clave). El almacén de paquetes debe estar ubicado en una ruta local en el sistema operativo del cliente. Los paquetes individuales se almacenan en el almacén de paquetes en los subdirectorios denominados para el GUID del paquete y la GUID de versión.

Ejemplo de una ruta de acceso a una aplicación específica:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Para cambiar la ubicación predeterminada del almacén de paquetes durante la configuración, vea [cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md).

### Almacén de contenido compartido

Si el cliente de App-V está configurado en el modo de almacenamiento de contenido compartido, no se escribirá ningún dato en el disco cuando se produzca un error de transmisión, lo que significa que los paquetes requieren un mínimo de espacio en disco local (datos de publicación). El uso de menos espacio en el disco es muy conveniente en entornos de VDI, donde el almacenamiento local se puede limitar y la transmisión de las aplicaciones desde una ubicación de red de alto rendimiento (como una SAN) es preferible. Para obtener más información sobre el modo de almacén de contenido compartido, consulte <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Nota:**  El almacén de paquetes y equipos debe estar ubicado en una unidad local, incluso si usa configuraciones de almacén de contenido compartido para el cliente de App-V.

 

### Catálogos de paquetes

El cliente de App-V administra las siguientes dos ubicaciones basadas en archivos:

-   **Catálogos (usuario y equipo).**

-   **Ubicaciones del registro** : depende de cómo se destinará el paquete a la publicación. Hay un catálogo (almacén de datos) para el equipo y un catálogo para cada usuario individual. El catálogo de equipos almacena información global aplicable a todos los usuarios o a cualquier usuario, y el catálogo de usuarios almacena la información aplicable a un usuario específico. El catálogo es una colección de configuraciones dinámicas y archivos de manifiesto; hay datos discretos para el archivo y el registro por versión de paquete. 

### Catálogo de máquina

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Almacena los documentos de paquetes que están disponibles para los usuarios en el equipo, cuando se agregan y publican paquetes. Sin embargo, si un paquete es "global" en el momento de la publicación, las integraciones estarán disponibles para todos los usuarios.</p>
<p>Si un paquete no es global, las integraciones se publican solo para usuarios específicos, pero todavía hay recursos globales que se han modificado y visible para cualquier persona en el equipo cliente (por ejemplo, el directorio del paquete se encuentra en una ubicación de disco compartido).</p>
<p>Si hay un paquete disponible para un usuario en el equipo (global o no global), el manifiesto se almacena en el catálogo del equipo. Cuando un paquete se publica globalmente, hay un archivo de configuración dinámica que se almacena en el catálogo del equipo; por lo tanto, la determinación de si un paquete es global se define en función de si hay un archivo de directivas (archivo UserDeploymentConfiguration) en el catálogo del equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación de almacenamiento predeterminada</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Esta ubicación no es la misma que la ubicación del almacén de paquetes. El almacén de paquetes es el oro o la copia original de los archivos del paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivos del catálogo de la máquina</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (paquete publicado globalmente)</p></li>
<li><p>UserDeploymentConfiguration.xml (paquete publicado globalmente)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación adicional del catálogo de equipos, que se usa cuando el paquete forma parte de un grupo de conexiones</p></td>
<td align="left"><p>La siguiente ubicación se agrega a la ubicación de paquete específica mencionada anteriormente:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivos adicionales en el catálogo de equipos cuando el paquete forma parte de un grupo de conexiones</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (grupo de conexión publicado globalmente)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### Catálogo de usuarios

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Creado durante el proceso de publicación. Contiene información usada para publicar el paquete y también se usa en el lanzamiento para garantizar que se aprovisione un paquete a un usuario específico. Creado en una ubicación de itinerancia e incluye información de publicación específica del usuario.</p>
<p>Cuando se publica un paquete para un usuario, el archivo de Directiva se almacena en el catálogo de usuarios. Al mismo tiempo, se almacena una copia del manifiesto en el catálogo de usuarios. Cuando se quita un derecho de paquete para un usuario, los archivos correspondientes del paquete se quitan del catálogo de usuarios. Si observa el catálogo de usuarios, un administrador puede ver la presencia de un archivo de configuración dinámico, lo que indica que el paquete tiene derecho a ese usuario.</p>
<p>Para los usuarios móviles, el catálogo de usuarios debe estar en una ubicación de itinerancia o compartida para preservar el comportamiento de App-V heredado de los usuarios de destino de forma predeterminada. El derecho y la política están vinculadas a un usuario, no a un equipo, por lo que deben moverse con el usuario una vez que se hayan aprovisionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación de almacenamiento predeterminada</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivos en el catálogo de usuarios</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml o UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación adicional del catálogo de usuarios, usada cuando el paquete forma parte de un grupo de conexiones</p></td>
<td align="left"><p>La siguiente ubicación se agrega a la ubicación de paquete específica mencionada anteriormente:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivo adicional en el catálogo de la máquina cuando el paquete forma parte de un grupo de conexiones</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### Copias de seguridad de accesos directos

Durante el proceso de publicación, el cliente de App-V realiza una copia de seguridad de los accesos directos y los puntos de integración en `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` esta copia de seguridad permite la restauración de estos puntos de integración a las versiones anteriores cuando se cancela la publicación del paquete.

### Copiar archivos en escritura

El almacén de paquetes contiene una copia original de los archivos del paquete que se han transmitido desde el servidor de publicación. Durante el funcionamiento normal de una aplicación de App-V, el usuario o el servicio pueden requerir cambios en los archivos. Estos cambios no se realizan en el almacén de paquetes para preservar su capacidad de reparar la aplicación, lo que elimina estos cambios. Estas ubicaciones, denominadas copia en escritura (COW), admiten tanto las ubicaciones de itinerancia como las no móviles. La ubicación en la que se almacenan las modificaciones depende de dónde se ha programado la aplicación para escribir cambios en una experiencia nativa.

### Itinerancia de vaca

La ubicación de itinerancia de VACAntes descrita anteriormente almacena los cambios en archivos y directorios destinados a la ubicación de% AppData% típica o a la ubicación de \\Users\\{username}\\AppData\\Roaming. A continuación, estos directorios y archivos se mueven en función de la configuración del sistema operativo.

### Local de VACAntes

La ubicación local de vaca es similar a la ubicación de itinerancia, pero los directorios y los archivos no se mueven a otros equipos, incluso si se ha configurado la compatibilidad con la itinerancia. La ubicación local de VACAntes descritas anteriormente almacena los cambios aplicables a las ventanas típicas y no a la ubicación de% AppData%. Los directorios que aparecen en la lista variarán, pero habrá dos ubicaciones para las ubicaciones típicas de Windows (por ejemplo, AppData comunes y Common AppDataS). La **S** significa la ubicación restringida cuando el servicio virtual solicita el cambio como un usuario elevado diferente de los usuarios que han iniciado sesión. La ubicación en la que no se almacenan los cambios**basados en usuarios** .

## <a href="" id="bkmk-pkg-registry"></a>Registro del paquete


Antes de que una aplicación pueda acceder a los datos del registro del paquete, el cliente de App-V debe poner los datos del registro del paquete a disposición de las aplicaciones. El cliente de App-V usa el registro real como almacén de respaldo para todos los datos del registro.

Cuando se agrega un paquete nuevo al cliente de App-V, una copia del registro. DAT del paquete se crea en `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . El nombre del archivo es el GUID de versión con el. Extensión DAT. El motivo por el que se realiza esta copia es asegurarse de que el archivo de subárbol real del paquete nunca se esté usando, lo que impedirá que se quite el paquete más adelante.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry. dat del almacén de paquetes</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</strong></p></td>
</tr>
</tbody>
</table>

 

Cuando la primera aplicación del paquete se inicia en el cliente, el cliente fases o copia el contenido del archivo de subárbol, volviendo a crear los datos del registro del paquete en una ubicación alternativa `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . Los datos de registro preconfigurados tienen dos tipos distintos de datos de equipo y datos de usuario. Los datos de la máquina se comparten entre todos los usuarios del equipo. Los datos de los usuarios se almacenan en una ubicación userspecific `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` . Los datos de la máquina se eliminan en última instancia en el tiempo de eliminación del paquete y los datos de usuario se eliminan en una operación de anulación de la publicación del usuario.

### Paquetes de ensayo del registro de paquetes y de grupo de conexiones por fases

Cuando hay grupos de conexión, el proceso anterior de ensayo del registro tiene el valor true, pero en lugar de tener un subárbol para procesar, hay más de uno. Los archivos se procesan en el orden en que aparecen en el XML del grupo de conexión, con el primer editor que gana conflictos.

El registro preconfigurado persiste de la misma manera que en el caso de un único paquete. Los datos del registro de usuario preconfigurados permanecen para el grupo de conexión hasta que se deshabilitan; los datos del registro de la máquina ensayada se quitan de la eliminación del grupo de conexión.

### Registro virtual

El propósito del registro virtual (VREG) es proporcionar una única vista combinada del registro del paquete y del registro nativo en las aplicaciones. También proporciona funcionalidad de copia en escritura (COW), es decir, cualquier cambio realizado en el registro desde el contexto de un proceso virtual se realiza en una ubicación de vaca distinta. Esto significa que el VREG debe combinar hasta tres ubicaciones de registro independientes en una sola vista basada en las ubicaciones rellenadas en el registro de COW- &gt; paquete- &gt; nativo. Cuando se realiza una solicitud de que los datos del registro se encuentren por orden hasta que encuentre los datos que ha solicitado. Es decir, si hay un valor almacenado en una ubicación de vaca, no podrá continuar con otras ubicaciones, sin embargo, si no hay datos en la ubicación de vaca, pasará al paquete y luego a la ubicación nativa hasta que encuentre los datos correspondientes.

### Ubicaciones del registro

Hay dos ubicaciones del registro de paquetes y dos ubicaciones de grupos de conexiones en las que el cliente de App-V almacena la información del registro, en función de si el paquete se publica de forma individual o como parte de un grupo de conexiones. Existen tres ubicaciones de vacas para paquetes y tres para grupos de conexión, que se crean y administran mediante el VREG. La configuración de paquetes y grupos de conexiones no es compartida:

**Un solo paquete VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Ubicación</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>VACA</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\REGISTRY (solo se puede escribir en el proceso de elevación)</p></li>
<li><p>User Registry\Client\Packages\PkgGUID\REGISTRY (usuarios que viajan por escrito en HKCU excepto Software\Classes</p></li>
<li><p>Registro de usuario Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes escrituras y HKLM para procesos no elevados)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paquete</strong></p></td>
<td align="left"><ul>
<li><p>Equipo Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Registro de usuario Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativa</strong></p></td>
<td align="left"><ul>
<li><p>Ubicación nativa del registro de aplicaciones</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**VReg de grupo de conexión:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Ubicación</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>VACA</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (solo se puede escribir en el proceso de elevación)</p></li>
<li><p>User Registry\Client\PackageGroups\GrpGUID\REGISTRY (cualquier cosa que se escriba en HKCU excepto Software\Classes</p></li>
<li><p>Registro de usuario Classes\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paquete</strong></p></td>
<td align="left"><ul>
<li><p>Equipo Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Registro de usuario Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativa</strong></p></td>
<td align="left"><ul>
<li><p>Ubicación nativa del registro de aplicaciones</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Existen dos ubicaciones de vaca para HKLM; procesos elevados y no elevados. Los procesos elevados siempre escriben cambios de HKLM en la seguridad de vaca en HKLM. Los procesos no elevados siempre escriben cambios de HKLM en la vaca no segura en HKCU\\Software\\Classes. Cuando una aplicación Lea los cambios de HKLM, los procesos elevados leerán los cambios de la vaca segura en HKLM. Lecturas no elevadas de ambos, favorecer los cambios realizados en la vaca no segura en primer lugar.

### Teclas de acceso directo

Las teclas de acceso directo permiten a un administrador configurar determinadas teclas para que solo puedan leerlas desde el registro nativo, omitiendo las ubicaciones de los paquetes y las VACAntes. Las ubicaciones de paso a través son globales para el equipo (no específicas del paquete) y se pueden configurar agregando la ruta de acceso a la clave, que debe tratarse como paso a través del valor **reg \ _MULTI \ _SZ** denominado **PassThroughPaths** de la clave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Cualquier tecla que aparezca en este valor de cadena múltiple (y sus elementos secundarios) se tratará como paso a través.

Las siguientes ubicaciones se configuran como ubicaciones de paso a través de forma predeterminada:

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY \ _CURRENT \ _USER configuración \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies

El propósito de las claves de paso a través es garantizar que una aplicación virtual no escribe datos del registro en el VReg que se requiere para las aplicaciones no virtuales para que funcionen o se integran correctamente. La clave de directivas garantiza que la configuración basada en directivas de grupo establecida por el administrador se use y no por configuración de paquete. La clave AppModel es necesaria para la integración con aplicaciones basadas en la interfaz de usuario moderna de Windows. Es recomendable que los complementos no modifiquen ninguna de las teclas de acceso directo predeterminadas, pero en algunos casos, según el comportamiento de la aplicación, es posible que necesite agregar claves de paso a través.

## <a href="" id="bkmk-pkg-store-behavior"></a>Comportamiento del almacén de paquetes de App-V


App-V 5 administra el almacén de paquetes, que es la ubicación en la que se almacenan los archivos de activos expandidos del archivo de appv. De forma predeterminada, esta ubicación se almacena en%ProgramData%\\App-V y está limitada en cuanto a las capacidades de almacenamiento solo por espacio libre en disco. El almacén de paquetes está organizado por los GUID para el paquete y la versión, tal y como se menciona en la sección anterior.

### Agregar paquetes

Los paquetes de App-V se almacenan en el equipo con el cliente de App-V. El cliente de App-V proporciona un almacenamiento provisional a petición. Durante la publicación o un complemento manual Add-AppVClientPackage, la estructura de datos se crea en el almacén de paquetes (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). Los archivos de paquetes identificados en el bloque de publicación definido en el StreamMap.xml se agregan al sistema y las carpetas de nivel superior y los archivos secundarios están preconfigurados para garantizar que los activos de la aplicación sean correctos en el inicio.

### Montar paquetes

Los paquetes se pueden cargar explícitamente con PowerShell `Mount-AppVClientPackage` o mediante la **interfaz de usuario del cliente de App-V** para descargar un paquete. Esta operación carga completamente todo el paquete en el almacén de paquetes.

### Paquetes de streaming

El cliente de App-V puede configurarse para cambiar el comportamiento predeterminado de la transmisión por secuencias. Todas las directivas de transmisión se almacenan en la siguiente clave de registro: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` . Las directivas se establecen con el cmdlet de PowerShell `Set-AppvClientConfiguration` . Las siguientes directivas se aplican a la transmisión por secuencias:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Directiva</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>En Windows 8, permite la transmisión por secuencias a través de redes móviles y 3G.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autocargar</p></td>
<td align="left"><p>Especifica la configuración de carga en segundo plano:</p>
<p><strong>0 </strong> - deshabilitado</p>
<p><strong>1 </strong> : solo paquetes usados previamente</p>
<p><strong>2 </strong> : todos los paquetes</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>La carpeta raíz para el almacén de paquetes en la máquina local</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>El reemplazo de raíz a partir del cual se transfieren los paquetes</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Habilita el uso del almacén de contenido compartido para escenarios de VDI</p></td>
</tr>
</tbody>
</table>

 

 

Esta configuración afecta al comportamiento de la transmisión de flujo de los activos del paquete App-V al cliente. De forma predeterminada, App-V solo descarga los recursos necesarios después de descargar los bloques iniciales de publicación y de características principales. Hay tres comportamientos específicos en relación con los paquetes de transmisión que se deben explicar:

-   Transmisión por secuencias de fondo

-   Transmisión por secuencias optimizada

-   Errores de secuencia

### Transmisión por secuencias de fondo

El cmdlet de PowerShell `Get-AppvClientConfiguration` se puede usar para determinar el modo actual para la transmisión por secuencias de fondo con la configuración de autocarga y modificar el cmdlet Set-AppvClientConfiguration o desde el registro (clave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming). La transmisión por secuencias de fondo es una configuración predeterminada en la que la configuración de autocargar está configurada para descargar paquetes usados previamente. El comportamiento basado en la configuración predeterminada (valor = 1) descarga bloques de datos de App-V en segundo plano después de que se haya iniciado la aplicación. Esta configuración se puede deshabilitar en conjunto (valor = 0) o habilitada para todos los paquetes (valor = 2), ya sea que se hayan iniciado.

### Transmisión por secuencias optimizada

Los paquetes de App-V se pueden configurar con un bloque de características principal durante la secuenciación. Esta configuración permite al ingeniero de secuenciación supervisar los archivos de inicio para una aplicación o aplicaciones específicas, y marcar los bloques de datos en el paquete de App-V para transmitirlos en el primer inicio de cualquier aplicación del paquete.

### Errores de secuencia

Después de la secuencia inicial de cualquier tipo de datos de publicación y el bloque de características principal, las solicitudes de archivos adicionales realizan errores de secuencia. Estos bloques de datos se descargan en el almacén de paquetes según sea necesario. Esto permite a un usuario descargar solo una pequeña parte del paquete, generalmente suficiente para iniciar el paquete y ejecutar las tareas normales. Todos los demás bloques se descargan cuando un usuario inicia una operación que requiere datos que no se encuentran actualmente en el almacén de paquetes.

Para obtener más información sobre la transmisión por secuencias de paquetes de App-V, visite: <https://go.microsoft.com/fwlink/?LinkId=392770> .

La secuencia de optimización para la transmisión por secuencias está disponible en: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### Actualizaciones de paquetes

Los paquetes de App-V necesitan actualizarse a lo largo del ciclo de vida de la aplicación. Las actualizaciones de paquetes de App-V son similares a la operación de publicación de paquetes, ya que cada versión se creará en su propia ubicación de PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . La operación de actualización se optimiza creando vínculos fuertes a archivos idénticos y transmitidos desde otras versiones del mismo paquete.

### Eliminación de paquetes

El comportamiento del cliente de App-V cuando se quitan paquetes depende del método usado para la eliminación. Con una infraestructura completa de App-V para anular la publicación de la aplicación, los archivos de catálogo de usuarios (catálogo de equipos para aplicaciones publicadas globalmente) se quitan, pero conservan la ubicación del almacén de paquetes y las ubicaciones de los VACAntes. Cuando se usa el cmdlet de PowerShell `Remove-AppVClientPackge` para quitar un paquete de App-V, se limpia la ubicación del almacén de paquetes. Recuerde que al anular la publicación de un paquete de App-V desde el servidor de administración no se realiza una operación de eliminación. Ninguna de las operaciones quitará los archivos de paquete del almacén de paquetes.

## <a href="" id="bkmk-roaming-reg-data"></a>Datos y registro de itinerancia


App-V 5 puede ofrecer una experiencia casi nativa en el momento de la itinerancia, en función de cómo se haya escrito la aplicación que se usa. De forma predeterminada, App-V AppData de itinerancia que se almacena en la ubicación de itinerancia, en función de la configuración de itinerancia del sistema operativo. Otras ubicaciones para el almacenamiento de datos basados en archivos no se mueven de un equipo a otro, ya que se encuentran en ubicaciones que no se transfieren.

### <a href="" id="bkmk-clt-inter-roam-reqs"></a>Requisitos de itinerancia y almacenamiento de datos de catálogo de usuarios

App-V almacena datos, que representan el estado del catálogo del usuario, en forma de:

-   Archivos en%appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Configuración del registro en `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

En conjunto, estos archivos y la configuración del registro representan el catálogo del usuario, por lo que ambos deben ser móviles o ninguno de ellos se debe mover a un usuario dado. App-V no es compatible con la itinerancia% AppData%, pero no se mueve el perfil del usuario (registro) o viceversa.

**Nota:**  El cmdlet **repair-AppvClientPackage** no repara el estado de publicación de los paquetes, en los que falta el estado de App-V del usuario `HKEY_CURRENT_USER` o no coincide con los datos de% appdata%.

 

### Datos basados en el registro

La itinerancia del registro de App-V se divide en dos escenarios, tal y como se muestra en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicaciones que se ejecutan como usuarios estándar</p></td>
<td align="left"><p>Cuando un usuario estándar inicia una aplicación de App-V, tanto HKLM como HKCU para aplicaciones de App-V se almacenan en el subárbol HKCU de la máquina. Esto presenta dos rutas distintas:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ SOFTWARE</p></li>
</ul>
<p>Las ubicaciones están habilitadas para roaming en función de la configuración del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicaciones que se ejecutan con elevación</p></td>
<td align="left"><p>Cuando se inicia una aplicación con elevación:</p>
<ul>
<li><p>Los datos de HKLM se almacenan en el subárbol HKLM del equipo local</p></li>
<li><p>Los datos HKCU se almacenan en la ubicación del registro del usuario</p></li>
</ul>
<p>En este escenario, estas opciones de configuración no se trasladan con las configuraciones de itinerancia del sistema operativo normal y los valores y las claves del registro resultantes se almacenan en la siguiente ubicación:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### App-V y redirección de carpetas

App-V 5.0 SP2 admite la redirección de carpetas de la carpeta de roaming (% AppData%). Cuando se inicia el entorno virtual, el estado de AppData de itinerancia del directorio de AppData de roaming del usuario se copia en la memoria caché local. A la inversa, cuando se cierra el entorno virtual, la memoria caché local asociada a un AppData de itinerancia de usuario específico se transfiere a la ubicación real del directorio de AppData de roaming de ese usuario.

Un paquete típico tiene varias ubicaciones asignadas en la tienda de respaldo del usuario para la configuración tanto en AppData\\Local como en AppData\\Roaming. Estas ubicaciones son la copia en ubicaciones de escritura que se almacenan por usuario en el perfil del usuario y que se usan para almacenar los cambios realizados en los directorios de VFS del paquete y proteger el VFS predeterminado del paquete.

En la tabla siguiente se muestran ubicaciones locales y móviles, cuando no se ha implementado el redireccionamiento de carpetas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Directorio de VFS en el paquete</th>
<th align="left">Ubicación asignada de la tienda de respaldo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

En la siguiente tabla se muestran ubicaciones locales y móviles, cuando se ha implementado el redireccionamiento de carpetas para% AppData%, y se ha redirigido la ubicación (normalmente a una ubicación de red).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Directorio de VFS en el paquete</th>
<th align="left">Ubicación asignada de la tienda de respaldo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

El controlador de VFS de cliente de App-V actual no puede escribir en ubicaciones de red, por lo que el cliente de App-V detecta la presencia de redireccionamiento de carpetas y copia los datos en la unidad local durante la publicación y cuando se inicia el entorno virtual. Después de que el usuario cierra la aplicación de App-V y el cliente de App-V cierra el entorno virtual, el almacenamiento local de la AppData de VFS se vuelve a copiar a la red, lo que permite la itinerancia a máquinas adicionales, donde se repetirá el proceso. Los pasos detallados de los procesos son:

1.  Durante el inicio de la publicación o del entorno virtual, el cliente de App-V detecta la ubicación del directorio de AppData.

2.  Si la ruta de AppData de roaming es local o Ino AppData\\Roaming ubicación está asignada, no sucede nada.

3.  Si la ruta de AppData de AppData no es local, el directorio de VFS se asigna al directorio local de appdata.

Este proceso resuelve el problema de un% AppData% no local que no es compatible con el controlador de dispositivo de cliente de App-V. Sin embargo, los datos almacenados en esta nueva ubicación no se mueven con el redireccionamiento de carpetas. Todos los cambios durante la ejecución de la aplicación se producen en la ubicación local AppData y se deben copiar a la ubicación redirigida. Los pasos detallados de este proceso son:

1.  Se cierra la aplicación App-V, que cierra el entorno virtual.

2.  La memoria caché local de la ubicación de AppData de roaming se comprime y se almacena en un archivo ZIP.

3.  Se usa una marca de tiempo al final del proceso de empaquetado ZIP para asignarle un nombre al archivo.

4.  La marca de hora se graba en el registro: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime como la última marca de hora de AppData conocidos.

5.  El proceso de redireccionamiento de carpetas se llama para evaluar e iniciar el archivo ZIP cargado en el directorio AppData de roaming.

La marca de tiempo se usa para determinar un escenario "gana el último escritor" si hay un conflicto y se usa para optimizar la descarga de los datos cuando se publica la aplicación de App-V o se inicia el entorno virtual. El redireccionamiento de carpetas hará que los datos estén disponibles de cualquier otro cliente cubierto por la Directiva de soporte técnico e iniciará el proceso de almacenamiento de los datos de AppData\\Roaming en la ubicación local AppData en el cliente. Los procesos detallados son:

1.  El usuario inicia el entorno virtual iniciando una aplicación.

2.  El entorno virtual de la aplicación comprueba el archivo ZIP de marcado de hora más reciente, si está presente.

3.  Se comprueba si el registro tiene la última marca de hora de carga conocida, si está presente.

4.  Se descarga el archivo ZIP más reciente, a menos que la marca de hora de última carga conocida local sea mayor o igual que la marca de hora del archivo ZIP.

5.  Si la marca de hora de la última carga conocida local es anterior a la del archivo ZIP más reciente en la ubicación de AppData de roaming, el archivo ZIP se extrae en el directorio temporal local del perfil del usuario.

6.  Una vez que el archivo ZIP se haya extraído correctamente, se cambiará el nombre de la memoria caché local del directorio de AppData y los nuevos datos se trasladarán a su sitio.

7.  El directorio cuyo nombre ha cambiado se elimina y la aplicación se abre con los últimos datos de itinerancia que se han guardado.

Esto completa la itinerancia correcta de la configuración de la aplicación que está presente en las ubicaciones de AppData\\Roaming. La única condición que debe solucionarse es una operación de reparación de paquetes. Los detalles del proceso son:

1.  Durante la reparación, detecte si la ruta al directorio de AppData de roaming del usuario no es local.

2.  Los destinos de la ruta de acceso de protección contra roaming no local de AppData se recrean.

3.  Elimine la marca de hora almacenada en el registro, si está presente.

Este proceso volverá a crear las ubicaciones locales y de red de AppData y quitará el registro de registro de la marca de tiempo.

## <a href="" id="bkmk-clt-app-lifecycle"></a>Administración del ciclo de vida de aplicaciones de cliente de App-V


En una infraestructura completa de App-V, después de secuenciar las aplicaciones, se administran y publican en usuarios o equipos a través de los servidores de publicación y administración de App-V. En esta sección se detallan las operaciones que se producen durante las operaciones comunes del ciclo de vida de la aplicación de App-V (agregar, publicar, iniciar, actualizar y quitar), así como las ubicaciones de archivo y registro que se modifican y modifican desde la perspectiva del cliente de App-V. Las operaciones de cliente de App-V se realizan como una serie de comandos de PowerShell iniciados en el equipo en el que se ejecuta el cliente de App-V.

Este documento se centra en las soluciones de infraestructura completa de App-V. Para obtener información específica sobre la integración de App-V con Configuration Manager 2012, visite: <https://go.microsoft.com/fwlink/?LinkId=392773> .

Las tareas de la aplicación App-V del ciclo de vida se desencadenan cuando el inicio de sesión del usuario (predeterminado), el inicio de la máquina o como operaciones de tiempo de fondo. La configuración de las operaciones de cliente de App-V, incluidos los servidores de publicación, los intervalos de actualización, la habilitación del script de paquete y otras, se configura durante la configuración del cliente o después de la instalación con los comandos de PowerShell. Consulte la sección Cómo implementar el cliente en TechNet en: [cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md) o usar PowerShell:

```powershell
get-command *appv*
```

### Actualización de publicaciones

El proceso de actualización de publicaciones consta de varias operaciones más pequeñas que se realizan en el cliente de App-V. Como App-V es una tecnología de virtualización de aplicaciones y no una tecnología de programación de tareas, el programador de tareas de Windows se usa para habilitar el proceso de inicio de sesión del usuario, el inicio del equipo y los intervalos programados. La configuración del cliente durante la instalación mencionada anteriormente es el método preferido al distribuir el cliente a un grupo grande de equipos con la configuración correcta. Estas opciones de configuración de cliente se pueden configurar con los siguientes cmdlets de PowerShell:

-   **Add-AppVPublishingServer:** Configura el cliente con un servidor de publicación de App-V que proporciona paquetes de App-V.

-   **Set-AppVPublishingServer:** Modifica la configuración actual del servidor de publicación de App-V.

-   **Set-AppVClientConfiguration:** Modifica la configuración de los actuales para el cliente de App-V.

-   **Sync-AppVPublishingServer:** Inicia manualmente un proceso de actualización de publicación de App-V. Esto también se usa en las tareas programadas creadas durante la configuración del servidor de publicación.

El objetivo de las siguientes secciones es detallar las operaciones que se producen durante las distintas fases de una actualización de publicación de App-V. Los temas incluyen:

-   Agregar un paquete de App-V

-   Publicar un paquete de App-V

### Agregar un paquete de App-V

Agregar un paquete de App-V al cliente es el primer paso del proceso de actualización de la publicación. El resultado final es el mismo que el `Add-AppVClientPackage` cmdlet en PowerShell, excepto durante el proceso de actualización de publicaciones, se Contacta con el servidor de publicación configurado y se devuelve una lista de aplicaciones de alto nivel al cliente para obtener información más detallada y no una sola operación de adición de paquetes. El proceso continúa con la configuración del cliente para agregar o actualizar paquetes o de grupos de conexiones, a continuación, accede al archivo de appv. A continuación, el contenido del archivo de appv se expande y se coloca en el sistema operativo local en las ubicaciones adecuadas. A continuación se incluye un flujo de trabajo detallado del proceso, asumiendo que el paquete está configurado para la transmisión por secuencias de errores.

**Cómo agregar un paquete de App-V**

1.  Inicio manual a través de PowerShell o la secuencia de tareas iniciada por el proceso de actualización de publicaciones.

    1.  El cliente de App-V realiza una conexión HTTP y solicita una lista de aplicaciones basada en el destino. El proceso de actualización de publicaciones admite equipos o usuarios de destino.

    2.  El servidor de publicación de App-V usa la identidad del destino de inicio, el usuario o el equipo, y consulta la base de datos para obtener una lista de las aplicaciones autorizadas. La lista de aplicaciones se proporciona como respuesta XML, que el cliente usa para enviar solicitudes adicionales al servidor para obtener más información sobre la base de cada paquete.

2.  El agente de publicación en el cliente de App-V realiza todas las acciones que se encuentran debajo de la serialización.

    Evalúe los grupos de conexión que estén sin publicar o deshabilitados, ya que las actualizaciones de la versión del paquete que forman parte del grupo de conexión no se pueden procesar.

3.  Configure los paquetes mediante la identificación de las operaciones de adición o actualización.

    1.  El cliente de App-V usa la API de AppX de Windows y obtiene acceso al archivo de appv desde el servidor de publicación.

    2.  El archivo de paquete se abre y los AppXManifest.xml y StreamMap.xml se descargan en el almacén de paquetes.

    3.  Datos de bloques de publicación completamente definidos en el StreamMap.xml. Almacena los datos del bloque de publicación en el paquete Store\\PkgGUID\\VerGUID\\Root.

        -   Iconos: destinos de los puntos de extensión.

        -   Encabezados ejecutables portables (encabezados PE): los destinos de los puntos de extensión que contienen la información base de la imagen que necesita en el disco, en el que se tiene acceso directamente o a través de tipos de archivo.

        -   Scripts: directorio de scripts de descarga para usar en todo el proceso de publicación.

    4.  Rellenar el almacén de paquetes:

        1.  Cree archivos dispersos en disco que representen el paquete extraído para cualquier directorio de la lista.

        2.  Los directorios y archivos de nivel superior del escenario, en raíz.

        3.  Todos los demás archivos se crean cuando el directorio se muestra como disperso en el disco y se transmite a petición.

    5.  Cree las entradas del catálogo de equipos. Cree el Manifest.xml y DeploymentConfiguration.xml a partir de los archivos de paquete (si no hay DeploymentConfiguration.xml archivo en el paquete creado un marcador de posición).

    6.  Crear la ubicación del almacén de paquetes en el registro de HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Cree el archivo Registry. dat del almacén de paquetes en%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat

    8.  Registrar el paquete con el controlador de modo de núcleo de App-V HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Invoca el scripting desde el archivo AppxManifest.xml o DeploymentConfig.xml para agregar intervalos a los paquetes.

4.  Configure grupos de conexión agregando y habilitando o deshabilitando.

5.  Quitar objetos que no se publican en el destino (usuario o equipo).

    **Nota:**  Esto no hará una eliminación de paquete, sino que quitará los puntos de integración para el destino específico (usuario o equipo) y eliminará los archivos de catálogo de usuarios (archivos de catálogo de equipo para publicación global).

     

6.  Invoca el montaje de carga en segundo plano basado en la configuración del cliente.

7.  Los paquetes que ya tienen información de publicación para el equipo o el usuario se restauran inmediatamente.

    **Nota:**  Esta condición se produce como un producto de desinstalación sin anular la publicación con la adición de fondo del paquete.

     

Esto completa un paquete de App-V que agrega el proceso de actualización de la publicación. El siguiente paso es publicar el paquete en el destino específico (equipo o usuario).

![paquete de adición de archivos y datos de registro](images/packageaddfileandregistrydata.png)

### Publicar un paquete de App-V

Durante la operación de actualización de publicación, la operación de publicación específica (Publish-AppVClientPackage) agrega entradas al catálogo de usuarios, asigna derechos al usuario, identifica el almacén local y termina completando los pasos de integración. A continuación se muestran los pasos detallados.

**Cómo publicar y el paquete de App-V**

1.  Las entradas de paquete se agregan al catálogo de usuarios

    1.  Paquetes dirigidos por el usuario: los UserDeploymentConfiguration.xml y UserManifest.xml se colocan en el equipo del catálogo de usuarios

    2.  Paquetes de destino de la máquina (global): el UserDeploymentConfiguration.xml se coloca en el catálogo de la máquina

2.  Registrar el paquete con el controlador de modo de núcleo para el usuario en HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Realizar tareas de integración.

    1.  Crear puntos de extensión.

    2.  Almacene la información de copia de seguridad en el registro del usuario y en el perfil de itinerancia (accesos directos).

        **Nota:**  Esto habilita los puntos de extensión de restauración si el paquete no se ha publicado.

         

    3.  Ejecutar scripts destinados a intervalos de publicación.

Publicar un paquete de App-V que forma parte de un grupo de conexiones es muy similar al proceso anterior. Para los grupos de conexión, la ruta de acceso que almacena la información de catálogo específica incluye PackageGroups como un elemento secundario del directorio del catálogo. Revise la información del catálogo de usuarios y equipos para obtener más detalles.

![Agregar archivo y datos del registro: global](images/packageaddfileandregistrydata-global.png)

### Inicio de la aplicación

Después del proceso de actualización de la publicación, el usuario inicia y después vuelve a iniciar una aplicación de App-V. El proceso es muy simple y optimizado para iniciarse rápidamente con un mínimo de tráfico de red. El cliente de App-V comprueba la ruta de acceso al catálogo de usuarios para los archivos creados durante la publicación. Después de establecer los derechos para iniciar el paquete, el cliente de App-V crea un entorno virtual, comienza a transmitir los datos necesarios y aplica el manifiesto adecuado y los archivos de configuración de implementación durante la creación del entorno virtual. Con el entorno virtual creado y configurado para el paquete y la aplicación específicos, se inicia la aplicación.

**Cómo iniciar aplicaciones de App-V**

1.  El usuario inicia la aplicación haciendo clic en un acceso directo o en una invocación de tipo de archivo.

2.  El cliente de App-V comprueba la existencia en el catálogo de usuarios para los siguientes archivos

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Si los archivos están presentes, la aplicación tendrá derecho a ese usuario específico y la aplicación iniciará el proceso de inicio. No hay tráfico de red en este momento.

4.  A continuación, el cliente de App-V comprueba que la ruta de acceso del paquete registrada para el servicio de cliente de App-V se encuentre en el registro.

5.  Al encontrar la ruta de acceso al almacén de paquetes, se crea el entorno virtual. Si este es el primer inicio, el bloque de características principal se descarga si está presente.

6.  Después de la descarga, el servicio del cliente de App-V consume el manifiesto y los archivos de configuración de implementación para configurar el entorno virtual y se cargan todos los subsistemas de App-V.

7.  Se inicia la aplicación. Para los archivos que faltan en el almacén de paquetes (archivos dispersos), App-V enviará por error los archivos según sea necesario.

    ![empaquetar Agregar archivo y datos del registro: secuencia](images/packageaddfileandregistrydata-stream.png)

### Actualización de un paquete de App-V

El proceso de actualización del paquete App-V 5 difiere de las versiones anteriores de App-V. App-V es compatible con varias versiones del mismo paquete en un equipo que tiene derecho a usuarios diferentes. Las versiones del paquete se pueden agregar en cualquier momento, ya que el almacén y los catálogos del paquete se actualizan con los nuevos recursos. El único proceso específico de la incorporación de nuevos recursos de versión es la optimización del almacenamiento de información. Durante una actualización, solo se agregan los nuevos archivos a la nueva ubicación del almacén de versiones y se crean vínculos físicos para los archivos que no han cambiado. Esto reduce el almacenamiento general al presentar el archivo en una ubicación del disco y, a continuación, proyectarlo en todas las carpetas con una entrada de ubicación del archivo en el disco. Los detalles específicos de la actualización de un paquete de App-V son los siguientes:

**Cómo actualizar un paquete de App-V**

1.  El cliente de App-V realiza una actualización de publicación y detecta una versión más reciente de un paquete de App-V.

2.  Las entradas de paquete se agregan al catálogo correspondiente para la nueva versión

    1.  Paquetes dirigidos por el usuario: los UserDeploymentConfiguration.xml y UserManifest.xml se colocan en el equipo del catálogo de usuarios en appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Paquetes de destino de la máquina (global): el UserDeploymentConfiguration.xml se coloca en el catálogo de máquina en%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Registrar el paquete con el controlador de modo de núcleo para el usuario en HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Realizar tareas de integración.

    -   Integre puntos de extensión (EP) desde el manifiesto y los archivos de configuración dinámica.

    1.  Los datos de EP basados en archivos se almacenan en la carpeta AppData con puntos de unión del almacén de paquetes.

    2.  La versión 1 de EPs ya existe cuando hay una nueva versión disponible.

    3.  Los puntos de extensión se cambian a la ubicación de la versión 2 en los catálogos de usuario o de equipo para los puntos de extensión nuevos o actualizados.

5.  Ejecutar scripts destinados a intervalos de publicación.

6.  Instale los ensamblados en paralelo según sea necesario.

### Actualización de un paquete de App-V en uso

A **partir de App-V 5 SP2**: Si intenta actualizar un paquete que está usando un usuario final, la tarea de actualización se coloca en un estado pendiente. La actualización se ejecutará más tarde, de acuerdo con las siguientes reglas:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de tarea</th>
<th align="left">Regla aplicable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarea basada en el usuario, por ejemplo, publicar un paquete para un usuario</p></td>
<td align="left"><p>La tarea pendiente se realizará después de que el usuario cierre sesión y vuelva a iniciarla.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarea basada en todo el mundo, por ejemplo, habilitar globalmente un grupo de conexiones</p></td>
<td align="left"><p>La tarea pendiente se realizará cuando el equipo se cierre y se reinicie.</p></td>
</tr>
</tbody>
</table>

 

Cuando una tarea se coloca en un estado pendiente, el cliente de App-V también genera una clave del registro para la tarea pendiente de la siguiente manera:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea basada en usuarios o en todo el mundo</th>
<th align="left">Dónde se genera la clave del registro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tareas basadas en usuarios</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tareas basadas en todo el mundo</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

Las siguientes operaciones deben completarse para que los usuarios puedan usar la versión más reciente del paquete:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Agregar el paquete al equipo</p></td>
<td align="left"><p>Esta tarea es específica del equipo y puede realizarla en cualquier momento completando los pasos de la sección anterior Agregar paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar el paquete</p></td>
<td align="left"><p>Consulte la sección de publicación de paquetes anterior para conocer los pasos. Este proceso requiere que se actualicen los puntos de extensión en el sistema. Los usuarios finales no pueden estar usando la aplicación al completar esta tarea.</p></td>
</tr>
</tbody>
</table>

 

Use los siguientes escenarios de ejemplo como guía para actualizar paquetes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Requisitos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>El paquete de App-V no se usa cuando intenta actualizar</p></td>
<td align="left"><p>Ninguno de los siguientes componentes del paquete puede estar en uso: aplicación virtual, servidor COM o extensiones de Shell.</p>
<p>El administrador publica una versión más reciente del paquete y la actualización funciona la próxima vez que se inicie un componente o una aplicación dentro del paquete. La nueva versión del paquete se transmite y se ejecuta. No ha cambiado nada en este escenario en App-V 5 SP2 de las versiones anteriores de App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>El paquete de App-V se está usando cuando el administrador publica una versión más reciente del paquete.</p></td>
<td align="left"><p>La operación de actualización se establece en pendiente por el cliente de App-V, lo que significa que está en cola y se ejecuta más tarde cuando el paquete no está en uso.</p>
<p>Si la aplicación de paquete está en uso, el usuario cierra la aplicación virtual, después de la cual se puede realizar la actualización.</p>
<p>Si el paquete tiene extensiones de Shell (Office 2013), que el explorador de Windows carga permanentemente, el usuario no puede iniciar sesión. Los usuarios deben cerrar sesión y volver a iniciar sesión para iniciar la actualización del paquete de App-V.</p></td>
</tr>
</tbody>
</table>

 

### Publicación de usuarios global vs

Los paquetes de App-V se pueden publicar de una de dos maneras: Usuario que da derecho a un paquete de App-V a un usuario o grupo de usuarios específico y global que da derecho al paquete de App-V a todo el equipo para todos los usuarios del equipo. Una vez que haya una actualización de paquete pendiente y el paquete App-V no se esté usando, considere los dos tipos de publicación:

-   **Publicado globalmente**: la aplicación se publica en un equipo; todos los usuarios de ese equipo pueden usarla. La actualización se producirá cuando se inicie el servicio de cliente de App-V, lo que significa que el equipo se reiniciará de forma eficaz.

-   **Usuario publicado**: la aplicación se publica para un usuario. Si hay varios usuarios en el equipo, la aplicación se puede publicar en un subconjunto de usuarios. La actualización se producirá cuando el usuario inicie sesión o cuando se publique de nuevo (periódicamente, la actualización y evaluación de directivas de ConfigMgr, o una publicación periódica de App-V o la actualización o explícitamente a través de los comandos de PowerShell).

### Quitar un paquete de App-V

Quitar aplicaciones de App-V en una infraestructura completa es una operación de anulación de la publicación y no realiza una eliminación de paquete. El proceso es el mismo que el proceso de publicación anterior, pero en lugar de agregar el proceso de eliminación, se invierten los cambios realizados para los paquetes de App-V.

### Reparación de un paquete de App-V

La operación de reparación es muy sencilla pero puede afectar a muchas ubicaciones de la máquina. Las ubicaciones de copia en escritura (COW) mencionadas anteriormente se eliminan y los puntos de extensión se integran y se vuelven a integrar. Revise las ubicaciones de colocación de datos de la vaca revisando dónde se encuentran registradas en el registro. Esta operación se realiza automáticamente y no hay ningún control administrativo distinto de iniciar una operación de reparación desde la consola del cliente de App-V o mediante PowerShell (Repair-AppVClientPackage).

## <a href="" id="bkmk-integr-appv-pkgs"></a>Integración de paquetes de App-V


El cliente de App-V y la arquitectura de paquetes proporcionan una integración específica con el sistema operativo local durante la adición y publicación de paquetes. Tres archivos definen la integración o los puntos de extensión para un paquete de App-V:

-   AppXManifest.xml: se almacena dentro del paquete con copias de reserva almacenadas en el almacén de paquetes y el perfil de usuario. Contiene las opciones creadas durante el proceso de secuenciación.

-   DeploymentConfig.xml: proporciona información de configuración de puntos de extensión de integración basados en equipos y usuarios.

-   UserConfig.xml: un subconjunto de la Deploymentconfig.xml que solo proporciona configuraciones basadas en el usuario y solo tiene como destino puntos de extensión basados en el usuario.

### Reglas de integración

Cuando se publican aplicaciones de App-V en un equipo con el cliente de App-V, se realizarán algunas acciones específicas, tal como se describe en la siguiente lista:

-   Publicación global: los accesos directos se almacenan en la ubicación del perfil todos los usuarios y otros puntos de extensión se almacenan en el registro en el subárbol HKLM.

-   Publicación de usuarios: los accesos directos se almacenan en el perfil de la cuenta de usuario actual y otros puntos de extensión se almacenan en el registro en el subárbol HKCU.

-   Copia de seguridad y restauración: se realiza una copia de seguridad de los datos y el registro de la aplicación nativa (como los registros FTA) durante la publicación.

    1.  Los paquetes de App-V reciben la propiedad basada en el último paquete integrado en el que la propiedad se pasa a la nueva aplicación de App-V publicada.

    2.  La propiedad se transfiere de un paquete de App-V a otro cuando se anula la publicación del paquete App-V propietario. Esto no iniciará una restauración de los datos o del registro.

    3.  Restaure los datos de copia de seguridad cuando el último paquete no se haya publicado o eliminado por cada extensión.

### Puntos de extensión

Los archivos de publicación de App-V (manifiesto y configuración dinámica) proporcionan varios puntos de extensión que permiten que la aplicación se integre con el sistema operativo local. Estos puntos de extensión realizan tareas típicas de instalación de aplicaciones, como la colocación de accesos directos, la creación de asociaciones de tipos de archivo y el registro de componentes. Ya que se trata de aplicaciones virtualizadas que no se instalan de la misma manera en una aplicación tradicional, existen algunas diferencias. A continuación se muestra una lista de los puntos de extensión descritos en esta sección:

-   Abreviados

-   Asociaciones de tipo de archivo

-   Extensiones de Shell

-   COM

-   Clientes de software

-   Capacidades de la aplicación

-   Controlador de protocolo URL

-   AppPath

-   Aplicación virtual

### Abreviados

El corto corte es uno de los elementos básicos de integración con el sistema operativo y es la interfaz para iniciar directamente el usuario de una aplicación de App-V. Durante la publicación y la anulación de la publicación de aplicaciones de App-V.

Desde el manifiesto del paquete y los archivos XML de configuración dinámica, la ruta de acceso a un ejecutable de la aplicación específica puede encontrarse en una sección similar a la siguiente:

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

Como se mencionó anteriormente, los accesos directos de App-V se colocan de forma predeterminada en el perfil del usuario en función de la operación de actualización. La actualización global coloca los accesos directos en el perfil todos los usuarios y la actualización de usuario los almacena en el perfil del usuario específico. El ejecutable real se almacena en el almacén de paquetes. La ubicación del archivo ICO es una ubicación con tokens en el paquete de App-V.

### Asociaciones de tipo de archivo

El cliente de App-V administra las asociaciones de tipos de archivo del sistema operativo local durante la publicación, lo que permite a los usuarios usar invocaciones de tipo de archivo o abrir un archivo con una extensión registrada específicamente (. docx) para iniciar una aplicación de App-V. Las asociaciones de tipo de archivo están presentes en el manifiesto y los archivos de configuración dinámico, tal como se representa en el ejemplo siguiente:

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

**Nota:**  En este ejemplo:

-   `<Name>.xdp</Name>` es la extensión

-   `<Name>AcroExch.XDPDoc</Name>` es el valor ProgId (que apunta al identificador de programa (ProgId) adyacente)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` es la línea de comandos, que señala al archivo ejecutable de la aplicación

 

### Extensiones de Shell de :

Las extensiones de Shell se incrustan automáticamente en el paquete durante el proceso de secuenciación. Cuando el paquete se publica globalmente, la extensión de Shell proporciona a los usuarios la misma funcionalidad que si la aplicación se instalara de forma local. La aplicación no requiere ninguna configuración ni configuración adicional en el cliente para habilitar la funcionalidad de la extensión de Shell.

**Requisitos para usar extensiones de Shell:**

-   Los paquetes que contienen extensiones de Shell insertadas deben publicarse globalmente.

-   El "bits" de la aplicación, el secuenciador y el cliente de App-V deben coincidir, o las extensiones de Shell no funcionarán. Por ejemplo:

    -   La versión de la aplicación es 64 bits.

    -   El secuenciador se está ejecutando en un equipo de 64 bits.

    -   El paquete se está entregando a un equipo cliente de aplicación de 64 bits de-V.

En la siguiente tabla se muestran las extensiones de Shell compatibles.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Administrador</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controlador del menú contextual</p></td>
<td align="left"><p>Agrega elementos de menú al menú contextual. Se llama antes de mostrar el menú contextual.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de arrastrar y colocar</p></td>
<td align="left"><p>Controla la acción que se muestra al hacer clic con el botón secundario y modificar el menú contextual que aparece.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de destino de colocación</p></td>
<td align="left"><p>Controla la acción después de arrastrar y colocar un objeto de datos en un destino de colocación, como un archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de objetos de datos</p></td>
<td align="left"><p>Controla la acción después de copiar un archivo en el portapapeles o de arrastrarlo y colocarlo sobre un destino. Puede proporcionar formatos adicionales del portapapeles para el destino de colocación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de hoja de propiedades</p></td>
<td align="left"><p>Reemplaza o agrega páginas al cuadro de diálogo de la hoja de propiedades de un objeto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de insugerencias</p></td>
<td align="left"><p>Permite recuperar los indicadores y la información de recuadro para un elemento y mostrarlo dentro de una información sobre herramientas emergente al mantener el mouse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de columnas</p></td>
<td align="left"><p>Permite crear y mostrar columnas personalizadas en la vista de detalles del explorador de Windows <em> </em> . Puede usarse para ampliar la ordenación y la agrupación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de vista previa</p></td>
<td align="left"><p>Habilita una vista previa de un archivo para que se muestre en el panel de vista previa del explorador de Windows.</p></td>
</tr>
</tbody>
</table>

 

### COM

El cliente de App-V admite aplicaciones de publicación compatibles con la integración COM y la virtualización. La integración COM permite al cliente de App-V registrar objetos COM en el sistema operativo local y en la virtualización de los objetos. A los fines de este documento, la integración de objetos COM requiere más detalles.

App-V admite el registro de objetos COM desde el paquete al sistema operativo local con dos tipos de proceso: fuera de proceso y en proceso. El registro de objetos COM se realiza con una o una combinación de varios modos de funcionamiento para un paquete de App-V específico que incluye apagado, aislamiento e integrado. El modo integrado se configura para el tipo fuera de proceso o en proceso. La configuración de los tipos y modos COM se realiza con los archivos de configuración dinámica (deploymentconfig.xml o userconfig.xml).

Los detalles de la integración de App-V están disponibles en: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### Características de aplicaciones y clientes de software

App-V es compatible con clientes de software específicos y puntos de extensión de funciones de aplicaciones que permiten que las aplicaciones virtualizadas se registren con el cliente de software del sistema operativo. Esto permite a los usuarios seleccionar programas predeterminados para operaciones como el correo electrónico, la mensajería instantánea y el reproductor multimedia. Esta operación se realiza en el panel de control con configurar acceso y programas predeterminados en el equipo, y configurado durante la secuenciación en el manifiesto o los archivos de configuración dinámica. Las funciones de la aplicación solo se admiten cuando las aplicaciones de App-V se publican globalmente.

Ejemplo de registro de clientes de software de un cliente de correo basado en App-V.

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

**Nota:**  En este ejemplo:

-   `<ClientConfiguration EmailEnabled="true" />` es la configuración general de los clientes de software para integrar clientes de correo electrónico

-   `<EMail MakeDefault="true">` es la bandera para establecer un cliente de correo electrónico determinado como cliente de correo electrónico predeterminado

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` es el registro de dll MAPI

 

### Controlador de protocolo URL

Las aplicaciones no siempre se denominan específicamente aplicaciones virtualizadas mediante la invocación de tipo de archivo. Para, por ejemplo, en una aplicación que admite la incrustación de un vínculo mailto: dentro de un documento o una página web, el usuario hace clic en un vínculo mailto: y espera obtener su cliente de correo registrado. App-V es compatible con los controladores de protocolo URL que se pueden registrar por paquete con el sistema operativo local. Durante la secuenciación, los controladores de protocolo URL se agregan automáticamente al paquete.

En situaciones en las que hay más de una aplicación que puede registrar el controlador de protocolo de dirección URL específico, los archivos de configuración dinámica se pueden usar para modificar el comportamiento y suprimir o deshabilitar esta característica para una aplicación que no debe ser la aplicación principal iniciada.

### AppPath

El punto de extensión AppPath admite la llamada a aplicaciones de App-V directamente desde el sistema operativo. Esto se realiza normalmente desde la pantalla de ejecución o de inicio, según el sistema operativo, lo que permite a los administradores proporcionar acceso a aplicaciones de App-V desde scripts o comandos del sistema operativo sin llamar a la ruta de acceso específica del ejecutable. Por lo tanto, evita modificar la variable de entorno PATH del sistema en todos los sistemas, ya que se realiza durante la publicación.

El punto de extensión AppPath se configura en el manifiesto o en los archivos de configuración dinámica y se almacena en el registro del equipo local durante la publicación para el usuario. Para obtener más información sobre la revisión de AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### Aplicación virtual

Este subsistema proporciona una lista de las aplicaciones capturadas durante la secuenciación, que suelen consumir otros componentes de App-V. La integración de puntos de extensión que pertenecen a una aplicación en particular se puede deshabilitar mediante archivos de configuración dinámica. Por ejemplo, si un paquete contiene dos aplicaciones, es posible deshabilitar todos los puntos de extensión que pertenecen a una aplicación para permitir únicamente la integración de puntos de extensión de otra aplicación.

### Reglas de punto de extensión

Los puntos de extensión descritos anteriormente se integran en el sistema operativo en función de la publicación de los paquetes. La publicación global coloca puntos de extensión en ubicaciones de máquinas públicas, donde la publicación de usuarios coloca puntos de extensión en ubicaciones de usuario. Por ejemplo, un acceso directo creado en el escritorio y publicado globalmente tendrá como resultado los datos de archivo del acceso directo (%Public%\\Desktop) y los datos del registro (HKLM\\Software\\Classes). El mismo método abreviado tendría datos de archivo (%UserProfile%\\Desktop) y datos del registro (HKCU\\Software\\Classes).

Los puntos de extensión no se publican de la misma manera, ya que algunos puntos de extensión requerirán la publicación global y otros requieren una secuencia en el sistema operativo y la arquitectura específicos donde se entregan. A continuación se muestra una tabla que describe estas dos reglas clave.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Extensión virtual</th>
<th align="left">Requiere la secuencia de los SO de destino</th>
<th align="left">Requiere publicación global</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Método abreviado</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Asociación de tipo de archivo</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocolos URL</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppPaths</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modo COM</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de software</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Capacidades de la aplicación</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador del menú contextual</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de arrastrar y colocar</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de objetos de datos</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de hoja de propiedades</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de insugerencias</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de columnas</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensiones de Shell</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Objeto auxiliar del explorador</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Objeto X activo</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a>Procesamiento de configuración dinámica


Implementar paquetes de App-V en un equipo o usuario es muy sencillo. Sin embargo, a medida que las organizaciones implementan aplicaciones de AppV a través de líneas empresariales y límites políticos y geográficos, la capacidad de secuenciar una aplicación una vez con un conjunto de configuraciones es imposible. App-V se diseñó para este escenario, ya que captura configuraciones y configuraciones específicas durante la secuenciación en el archivo de manifiesto, pero también admite la modificación con archivos de configuración dinámica.

La configuración dinámica de App-V permite especificar una directiva para un paquete, ya sea en el nivel de equipo o en el nivel de usuario. Los archivos de configuración dinámica permiten a los ingenieros de secuenciación modificar la configuración de un paquete, postsecuenciación, para satisfacer las necesidades de grupos individuales de usuarios o equipos. En algunos casos, puede que sea necesario realizar modificaciones en la aplicación para proporcionar la funcionalidad adecuada en el entorno de App-V. Por ejemplo, puede que sea necesario realizar modificaciones en los archivos \ _ \ * config.xml para permitir que se realicen determinadas acciones en un momento determinado durante la ejecución de la aplicación, como deshabilitar una extensión mailto para evitar que una aplicación virtualizada sobrescriba esa extensión de otra aplicación.

Los paquetes de App-V contienen el archivo de manifiesto dentro del archivo de paquete de appv, que es representativo de las operaciones de secuencia y es la política de elección a menos que los archivos de configuración dinámica se asignen a un paquete específico. Después de la secuenciación, los archivos de configuración dinámica se pueden modificar para permitir la publicación de una aplicación en diferentes escritorios o usuarios con diferentes puntos de extensión. Los dos archivos de configuración dinámica son los archivos de configuración de implementación dinámica (DDC) y de configuración de usuario dinámica (DUC). Esta sección se centra en la combinación del manifiesto y los archivos de configuración dinámica.

### Ejemplo de archivos de configuración dinámica

En el ejemplo siguiente se muestra la combinación del manifiesto, la configuración de implementación y los archivos de configuración de usuario después de la publicación y durante el funcionamiento normal. Estos ejemplos son ejemplos abreviados de cada uno de los archivos. El propósito es mostrar la combinación de los archivos únicamente y no ser una descripción completa de las categorías específicas disponibles en cada uno de los archivos. Para obtener más información, consulte la guía de secuenciación de App-V 5 en: <https://go.microsoft.com/fwlink/?LinkID=269810>

**Manifiesta**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**Configuración de la implementación**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**Configuración de usuario**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a>Ensamblados en paralelo


App-V es compatible con el empaquetado automático de ensamblados en paralelo (SxS) durante la secuenciación y la implementación en el cliente durante la publicación de aplicaciones virtuales. App-V SP2 admite la captura de ensamblados SxS durante la secuenciación para los ensamblados que no están presentes en el equipo de secuenciación. Y para los ensamblados compuestos de Visual C++ (versión 8 y posterior) o de tiempo de ejecución de MSXML, el secuenciador detectará y capturará automáticamente estas dependencias incluso si no se instalaron durante la supervisión. La característica de ensamblados en paralelo elimina las limitaciones de las versiones anteriores de App-V, donde el secuenciador de App-V no captura los ensamblados que ya están presentes en la estación de trabajo de secuenciación, y la protección de los ensamblados que se limita a una versión de bit por paquete. Este comportamiento dio lugar a que los clientes de aplicaciones de App-V implementaran los ensamblados SxS obligatorios, lo que provocaba errores de inicio de la aplicación. Esto forzó el proceso de empaquetado para documentar y, a continuación, asegurarse de que todos los ensamblados necesarios para los paquetes se instalaron de forma local en el sistema operativo cliente del usuario para asegurar la compatibilidad con las aplicaciones virtuales. Según el número de ensamblados y la falta de documentación de la aplicación para las dependencias obligatorias, esta tarea era un desafío de administración e implementación.

El soporte de ensamblado en paralelo en App-V tiene las siguientes características.

-   Capturas automáticas de ensamblado SxS durante la secuenciación, independientemente de si el ensamblado ya se ha instalado en la estación de trabajo de secuenciación.

-   El cliente de App-V instala automáticamente los ensamblados SxS obligatorios en el equipo cliente en el momento de la publicación cuando no están presentes.

-   El secuenciador informa de la dependencia en tiempo de ejecución de VC en el mecanismo de informes SPRJ.

-   El secuenciador permite optar por no empaquetar los ensamblados que ya están instalados en el secuenciador y los escenarios en los que se hayan instalado previamente los ensamblados en los equipos de destino.

### Publicación automática de ensamblados SxS

Durante la publicación de un paquete de App-V con ensamblajes SxS, el cliente de App-V verificará la presencia del ensamblado en el equipo. Si el ensamblado no existe, el cliente implementará el ensamblado en el equipo. Los paquetes que forman parte de grupos de conexión dependerán de las instalaciones de ensamblado en paralelo que forman parte de los paquetes básicos, ya que el grupo de conexión no contiene información sobre la instalación del ensamblado.

**Nota:**  Al anular la publicación o quitar un paquete con un ensamblado, no se quitan los ensamblados de ese paquete.

 

## <a href="" id="bkmk-client-logging"></a>Registro de cliente


El cliente de App-V registra información en el registro de eventos de Windows en el formato ETW estándar. Los eventos de App-V específicos pueden encontrarse en el visor de eventos, en aplicaciones y servicios Logs\\Microsoft\\AppV\\Client.

**Nota:**  En App-V 5,0 SP3, se han consolidado algunos registros y se han movido a la siguiente ubicación:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Para obtener una lista de los registros que se han movido, consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

 

A continuación se describen tres categorías específicas de eventos.

**Administrador**: registra eventos de configuración que se aplican al cliente de App-V y contiene las advertencias y errores principales.

**Operativo**: registra la ejecución general de App-v y el uso de componentes individuales creando un registro de auditoría de las operaciones de App-v que se completaron en el cliente de App-v.

**Aplicación virtual**: registra la aplicación virtual y el uso de subsistemas de virtualización.






 

 





