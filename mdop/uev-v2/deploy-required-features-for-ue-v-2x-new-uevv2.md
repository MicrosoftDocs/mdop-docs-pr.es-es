---
title: Implementar funciones necesarias para UE-V 2.x
description: Implementar funciones necesarias para UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824670"
---
# Implementar funciones necesarias para UE-V 2.x


Todas las implementaciones de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 requieren estas características

-   [Implemente una ubicación de almacenamiento de configuración](#ssl) accesible para los usuarios finales.

    Este es un recurso compartido de red estándar que almacena y recupera la configuración de usuario.

-   [Elegir el método de configuración de UE-V](#config)

    UE-V se puede implementar y configurar con herramientas de administración comunes, como la Directiva de grupo, el administrador de configuración o la infraestructura de administración de Windows y PowerShell.

-   [Implementar un agente de UE-V](#agent) para instalarlo en todos los equipos que sincronizan la configuración.

    Esto supervisa las aplicaciones registradas y el sistema operativo para los cambios de configuración y sincroniza esa configuración entre equipos.

En los temas de esta sección se describe cómo implementar estas características.

## <a href="" id="ssl"></a>Implementar una ubicación de almacenamiento de configuración de UE-V


UE-V requiere una ubicación en la que almacenar la configuración de usuario en los archivos de paquete de configuración. Puede configurar esta ubicación de almacenamiento de configuración de una de las siguientes maneras:

-   Crear su propia ubicación de almacenamiento de configuración

-   Usar Active Directory existente para la ubicación de almacenamiento de configuración

Si no crea una ubicación de almacenamiento de configuración, UE-V Agent usará Active Directory (AD) de forma predeterminada.

**Nota**  
Como cuestión de [rendimiento y planificación de capacidad](https://technet.microsoft.com/library/dn458932.aspx#capacity) y para reducir los problemas con la latencia de red, cree ubicaciones de almacenamiento de configuración en las mismas redes locales donde residen los equipos de los usuarios. Recomendamos 20 MB de espacio en disco por usuario para la ubicación de almacenamiento de configuración.



### Crear una ubicación de almacenamiento de configuración de UE-V

Antes de definir la ubicación de almacenamiento de configuración, debe crear un directorio raíz con permisos de lectura y escritura para los usuarios que almacenan la configuración en el recurso compartido. El agente UE-V crea carpetas específicas de usuario en este directorio raíz.

La ubicación de almacenamiento de configuración se define mediante la configuración de la opción de configuración SettingsStoragePath, que se puede configurar mediante uno de estos métodos:

-   Al [implementar el agente de UE-V](#agent) con un parámetro de línea de comandos o en un script de proceso por lotes

-   Mediante la configuración de [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)

-   Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) para UE-V

-   Después de la instalación de UE-V Agent, mediante [Windows PowerShell o el instrumental de administración de Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)

La ruta de acceso debe estar en una ruta de acceso UNC (Convención de nomenclatura universal) del servidor y el recurso compartido. Por ejemplo, **\\\\Server\\Settingsshare\\**. Esta opción de configuración admite el uso de variables para habilitar escenarios de sincronización específicos. Por ejemplo, puede usar las `%username%\%computername%` variables para conservar la experiencia de configuración de usuario final en estos escenarios:

-   Usuarios finales que usan varios equipos físicos en su empresa

-   Equipos empresariales que usan varios usuarios finales

UE-V Agent crea dinámicamente una ruta de almacenamiento de configuración específica de usuario, con una carpeta de sistema oculta denominada `SettingsPackages` , basada en la opción de configuración de **SettingsStoragePath**. El agente Lee y escribe la configuración en esta ubicación, tal como se define en las plantillas de ubicación de configuración de UE-V registradas.

**La configuración de UE-V está determinada por la regla "última escritura gana":** Si la ubicación de almacenamiento de configuración es la misma para el usuario con varios equipos administrados, un agente de UE-V Lee y escribe en la ubicación de configuración independientemente de los agentes que se ejecutan en otros equipos. Las últimas configuraciones y valores son los que se aplican cuando el siguiente agente Lee de la ubicación de almacenamiento de configuración.

**Implementar la ubicación de almacenamiento de configuración:** Siga estos pasos para definir la ubicación de almacenamiento de configuración en lugar de usar el servicio de Active Directory existente. Debe limitar el acceso al recurso de almacenamiento de configuración a los usuarios que lo requieren, tal y como se muestra en las tablas siguientes.

**Para implementar el recurso compartido de red UE-V**

1.  Cree un nuevo grupo de seguridad para usuarios de UE-V.

2.  Cree una nueva carpeta en el equipo centralizado que almacena los paquetes de configuración de UE-V y, a continuación, conceda a los usuarios de UE-V acceso con permisos de grupo a la carpeta. El administrador que admita UE-V debe tener permisos para esta carpeta compartida.

3.  Establezca los siguientes permisos de bloque de mensajes de servidor (SMB) de nivel de recurso compartido para la carpeta de ubicación de almacenamiento de configuración.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cuenta de usuario</strong></th>
    <th align="left"><strong>Permisos recomendados</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de seguridad de los usuarios de UE-V</p></td>
    <td align="left"><p>Control total</p></td>
    </tr>
    </tbody>
    </table>



4.  Establezca los siguientes permisos del sistema de archivos NTFS en la carpeta de ubicación de almacenamiento de configuración.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cuenta de usuario</strong></th>
    <th align="left"><strong>Permisos recomendados</strong></th>
    <th align="left"><strong>Carpeta</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creador/propietario</p></td>
    <td align="left"><p>Control total</p></td>
    <td align="left"><p>Solo subcarpetas y archivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de seguridad de los usuarios de UE-V</p></td>
    <td align="left"><p>Listar carpeta/leer datos, crear carpetas/anexar datos</p></td>
    <td align="left"><p>Solo esta carpeta</p></td>
    </tr>
    </tbody>
    </table>



Con esta configuración, UE-V Agent crea y protege una carpeta Settingspackage mientras se ejecuta en el contexto del usuario y otorga a cada usuario permiso para crear carpetas para el almacenamiento de la configuración. Los usuarios reciben el control total de su carpeta Settingspackage, mientras que otros usuarios no pueden acceder a ella.

**Nota**  
Si crea el recurso de almacenamiento de configuración en un equipo que ejecuta un sistema operativo Windows Server, configure UE-V para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración. Para habilitar esta seguridad adicional, especifique esta configuración en el editor del registro de Windows Server:

1.  Agregue una clave del registro **reg \ _DWORD** denominada **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Establezca el valor de la clave del registro en *1*.



### Usar Active Directory con UE-V 2. x

El agente UE-V usa Active Directory (AD) de forma predeterminada si una ubicación de almacenamiento de configuración no está definida. En estos casos, UE-V Agent crea dinámicamente la carpeta de almacenamiento de configuración en la raíz del directorio particular de AD de cada usuario. Sin embargo, si una configuración de directorio personalizada está configurada en AD, ese directorio se usa en su lugar.

## <a href="" id="config"></a>Elija el método de configuración de UE-V 2. x


Desea averiguar qué método de configuración usará para administrar UE-V después de la implementación, ya que este es el método de configuración que use para implementar el agente de UE-V. Normalmente, este es el método de configuración que ya usa en su entorno, como Windows PowerShell o Configuration Manager.

Puede configurar UE-V antes, durante o después de la instalación del agente de UE-V, según el método de configuración que use.

-   [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** puede usar su infraestructura de directiva de grupo existente para configurar UE-v antes o después de la implementación del agente de UE-v. La plantilla de ADMX de la Directiva de grupo de UE-V habilita la administración centralizada de las opciones de configuración de agentes comunes de UE-V e incluye la configuración para configurar la sincronización de UE-V.

    **Instalar las plantillas ADMX de la Directiva de grupo de UE-V:** Plantillas ADMX de directiva de grupo para UE-V establecer la configuración de sincronización para el agente UE-V y habilitar la administración centralizada de las opciones de configuración del agente Common UE-V mediante una infraestructura de directiva de grupo existente.

    Entre los sistemas operativos admitidos para el controlador de dominio que implementa los objetos de directiva de grupo se incluyen los siguientes:

    Windows Server 2008 R2

    Windows Server 2012 y Windows Server 2012 R2

-   [Administrador de configuración](https://technet.microsoft.com/library/dn458917.aspx)**:** el paquete de configuración de UE-V le permite usar la característica de configuración de cumplimiento de System Center Configuration Manager 2012 SP1 o posterior para aplicar configuraciones coherentes en los sitios donde se instalan UE-V y Configuration Manager.

-   [Windows PowerShell y WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** puede usar los comandos de scripts para Windows PowerShell y Windows Management Instrumentation (WMI) con el fin de modificar las configuraciones después de instalar UE-V Agent.

    **Nota**  
    La modificación del registro puede provocar pérdida de datos o el equipo deja de responder. Le recomendamos que use otros métodos de configuración.



-   **Instalación de la línea de comandos o del script por lotes:** Los parámetros que se usan al [implementar el agente de UE-v](#agent) tienen configurado muchos parámetros de UE-v. Los sistemas electrónicos de distribución de software, como System Center 2012 Configuration Manager, usan estos parámetros para configurar sus clientes cuando implementan e instalan el software de agente de UE-V.

## <a href="" id="agent"></a>Implementar el agente UE-V 2. x


UE-V Agent es el núcleo de una implementación de UE-V y debe ejecutarse en todos los equipos que usan UE-V para sincronizar la configuración de Windows y de la aplicación.

**Archivos de instalación de UE-V Agent:** Un único archivo de instalación, AgentSetup.exe, instala UE-V Agent en los sistemas operativos de 32 y 64 bits. Además, se proporcionan AgentSetupx86.msi o AgentSetupx64.msi archivos de Windows Installer específicos de la arquitectura, y puesto que son más pequeños, pueden simplificar las implementaciones del agente. Los [parámetros de la línea de comandos para el instalador de AgentSetup.exe](#params) son compatibles también con la instalación de Windows Installer.

**Importante**  
Durante la instalación o desinstalación de un agente de UE-V, puede usar el archivo AgentSetup.exe o &lt; el &gt; archivo AgentSetup. msi, pero no ambos. El mismo archivo debe usarse para desinstalar el agente de UE-V que se usó para instalar el agente de UE-V.



### Para implementar el agente de UE-V

Puede usar los siguientes métodos para implementar el agente de UE-V:

-   Un sistema de solución de distribución electrónica de software (ESD), como Configuration Manager, que puede instalar un archivo de Windows Installer (. msi).

-   Un script de instalación que hace referencia al archivo de Windows Installer (. msi) que se almacena centralmente en un recurso compartido.

-   Un programa de instalación que se ejecuta manualmente en el equipo.

Use el siguiente procedimiento para implementar UE-V Agent desde un recurso compartido de red.

**Para instalar y configurar el agente UE-V desde un recurso compartido de red**

1.  Fase el archivo de instalación de UE-V Agent AgentSetup.exe en un recurso compartido de red en el que los usuarios tienen permiso de lectura.

2.  Implementar una secuencia de comandos en equipos de usuario que instala UE-V Agent. El script debe especificar la ubicación de almacenamiento de configuración.

**Opciones de implementación:** Asegúrese de usar el formato de variable correcto al instalar el agente de UE-V. En la tabla siguiente se proporcionan ejemplos de opciones de implementación para usar el AgentSetup.exe o los archivos de Windows Installer (. msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Tipo de implementación</strong></th>
<th align="left"><strong>Descripción de la implementación</strong></th>
<th align="left"><strong>Ejemplo</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Símbolo del sistema</p></td>
<td align="left"><p>Al instalar el agente de UE-V en un símbolo del sistema, use el <em> formato de variable% ^ username% </em> . Si las comillas son necesarias debido a los espacios en la ruta de almacenamiento de configuración, use un archivo de script por lotes para la implementación.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script por lotes</p></td>
<td align="left"><p>Cuando instale UE-V Agent desde un archivo de script por lotes, use el <em> formato de variable%% username%% </em> . Si usa este método de instalación, debe escapar la variable con los%% caracteres. Sin este carácter, la secuencia de comandos amplía <em> la </em> variable username en el momento de la instalación, en lugar de hacerlo en tiempo de ejecución, lo que hace que UE-V use una sola ubicación de almacenamiento de configuración para todos los usuarios.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell</p></td>
<td align="left"><p>Cuando instale UE-V Agent desde un símbolo del sistema de Windows PowerShell o un script de Windows PowerShell, use el <em> formato de variable% username% </em> .</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribución electrónica de software, como la implementación de la implementación de software de Configuration Manager</p></td>
<td align="left"><p>Al instalar el agente de UE-V mediante el administrador de configuración, use el <em> formato de variable ^% username ^% </em> .</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**Nota**  
La instalación del agente de UE-V requiere derechos de administrador, y el equipo requiere que se reinicie el equipo antes de que se pueda ejecutar el agente de UE-V.



### <a href="" id="params"></a>Parámetros de la línea de comandos para la implementación del agente de UE-V

Los parámetros de la línea de comandos de UE-V Agent son los siguientes.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Parámetro de la línea de comandos</strong></th>
<th align="left"><strong>Definición</strong></th>
<th align="left"><strong>Notas</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help o/h o/?</p></td>
<td align="left"><p>Muestra el cuadro de diálogo de uso de AgentSetup.exe.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define dónde se almacena la configuración.</p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Debe especificar un SettingsStoragePath en UE-V 2,1 y UE-V 2,1 SP1. Puede establecer la cadena AdHomePath para especificar que el usuario&#39;la ruta de acceso de la Página principal de Active Directory. Por ejemplo, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</p>
<p>En UE-V 2,0, puede dejar el SettingsStoragePath en blanco para usar la ruta de acceso de la Página principal de Active Directory.</p>
</div>
<div>

</div>
<p>se aceptan las variables de entorno% username% o% COMPUTERNAME%. El scripting puede requerir variables de escape.</p>
<p><strong>Valor predeterminado </strong> : &lt; ninguno&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsStoragePathReg</p></td>
<td align="left"><p>Obtiene el valor de SettingsStoragePath del registro durante la instalación.</p></td>
<td align="left"><p>En el símbolo del sistema, escriba el siguiente ejemplo para forzar que UE-V use la ruta de acceso de la Página principal de Active Directory en lugar de un UNC específico.</p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la configuración de nuevas plantillas de ubicación de configuración.</p></td>
<td align="left"><p>Solo es necesario para las plantillas de ubicación de configuración personalizada</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.</p></td>
<td align="left"><p>Verdadero | Valor</p>
<p><strong>Valor predeterminado </strong> : verdadero</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Especifica qué método de sincronización debe usarse.</p></td>
<td align="left"><p>SyncProvider | Nada</p>
<p><strong>Valor predeterminado </strong> : SyncProvider</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Especifica el número de milisegundos que el equipo debe esperar antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de almacenamiento de configuración.</p></td>
<td align="left"><p><strong>Valor predeterminado </strong> : 2000 milisegundos</p>
<p>(espera hasta 2 segundos)</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Especifica si la sincronización de UE-V está habilitada o deshabilitada.</p></td>
<td align="left"><p>Verdadero | Valor</p>
<p><strong>Valor predeterminado </strong> : verdadero</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Especifica el tamaño de archivo de un paquete de configuración en bytes cuando el agente de UE-V notifica que los archivos superan el umbral.</p></td>
<td align="left"><p>&lt;su&gt;</p>
<p><strong>Valor predeterminado </strong> : ninguno (no hay umbral de advertencia)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Especifica la configuración de participación en el programa para la mejora de la experiencia del usuario. Si se establece en <strong> true </strong> , la información del instalador se carga en el sitio del programa para la mejora de la experiencia del usuario de Microsoft. Si se establece en <strong> false </strong> , no se cargará ninguna información.</p></td>
<td align="left"><p>Verdadero | Valor</p>
<p><strong>Valor predeterminado </strong> : falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No restar</p></td>
<td align="left"><p>Es compatible con el aplazamiento del reinicio del equipo después de instalar el agente de UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>INSTALLFOLDER</p></td>
<td align="left"><p>Permite establecer una carpeta de instalación diferente para el generador de UE-V Agent o UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MUENABLED</p></td>
<td align="left"><p>Permite que el programa de instalación acepte la opción que se va a incluir en el programa Microsoft Update.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ACCEPTLICENSETERMS</p></td>
<td align="left"><p>Permite que UE-V se instale silenciosamente. Debe establecerse en <strong> true </strong> para instalar UE-v en modo silencioso y evitar el requisito de que el usuario acepte los términos de licencia de UE-v. Si se establece en <strong> false </strong> o se deja vacío, el usuario recibe un mensaje de error y UE-V no está instalado.</p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Este parámetro es necesario para instalar UE-V en modo silencioso.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>No restar</p></td>
<td align="left"><p>Evita un reinicio obligatorio una vez instalado el agente de UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Actualizar el agente de UE-V

Las actualizaciones para el software del agente UE-V se proporcionan a través de Microsoft Update. Puede implementar las actualizaciones del agente de UE-V mediante sistemas de infraestructura de distribución de software para empresas (ESD).

Durante una actualización de UE-V Agent, se puede actualizar el grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows.

### Actualizar el agente UE-V 2. x

El agente UE-V 2. x introduce muchas características nuevas y modifica el modo y el momento en que el agente carga el contenido en el recurso compartido de almacenamiento de configuración. El proceso de actualización automatiza estos cambios. Para actualizar el agente de UE-V, ejecute el paquete de instalación de UE-V Agent (AgentSetup.exe, AgentSetupx86.msi o AgentSetupx64.msi) en los equipos de los usuarios.

**Nota**  
Al actualizar el agente de UE-V, debe usar el mismo tipo de instalador (el archivo. exe o el paquete. msi) que instaló el agente anterior de UE-V. Por ejemplo, use la AgentSetup.exe UE-V 2 para actualizar los agentes de UE-V 1,0 que se instalaron con AgentSetup.exe.



Las siguientes configuraciones se conservan cuando se ejecuta el programa de configuración del agente:

-   Configuración ruta de almacenamiento

-   Configuración del Registro

-   Tareas programadas (la configuración de intervalos se restablece a los valores predeterminados)

**Nota**  
Un equipo con la configuración de UE-V 2. x las plantillas de ubicación registradas en el agente de UE-V 1,0 registran errores en el registro de eventos de Windows.



Puede usar Microsoft System Center 2012 Configuration Manager u otra herramienta de distribución de software empresarial para automatizar y distribuir la actualización del agente de UE-V.

**Recomendaciones:** Le recomendamos que actualice todos los agentes de UE-V 1,0 en un entorno informático, pero no es necesario. UE-V 2. las plantillas de ubicación de configuración de UE pueden interactuar con un agente de UE-V 1,0 porque solo comparten la configuración de la ruta de almacenamiento de configuración. Sin embargo, le recomendamos que mueva las implementaciones a una única versión de agente para simplificar la administración y para que sea compatible con UE-V.

### Reparar el agente UE-V después de una actualización incorrecta

Es posible que se produzcan errores después de intentar una de las siguientes acciones:

-   Actualizar de UE-V 1,0 a UE-V 2

-   Actualice a una versión más reciente de Windows, por ejemplo, de Windows 7 a Windows 8 o de Windows 8 a Windows 8,1.

-   Desinstalar el agente después de actualizar el agente de UE-V

Para resolver cualquier problema, intente reparar el agente UE-V escribiendo este comando en un símbolo del sistema en el equipo en el que está instalado el agente.

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

Puede volver a intentar realizar el proceso de desinstalación o actualizar instalando la versión más reciente de UE-V Agent.






## Temas relacionados


[Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









