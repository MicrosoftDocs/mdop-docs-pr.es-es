---
title: Acerca de la configuración dinámica de App-V 5.0
description: Acerca de la configuración dinámica de App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815031"
---
# Acerca de la configuración dinámica de App-V 5.0


Puede usar la configuración dinámica para personalizar un paquete de App-V 5,0 para un usuario. Use la siguiente información para crear o editar un archivo de configuración dinámica existente.

Al editar el archivo de configuración dinámica, se personaliza cómo se ejecutará un paquete de App-V 5,0 para un usuario o un grupo. Esto ayuda a proporcionar un método más adecuado para la personalización de paquetes eliminando la necesidad de volver a ensecuenciar paquetes con la configuración deseada y proporciona una forma de mantener el contenido del paquete y la configuración personalizada de forma independiente.

## Avanzada: configuración dinámica


Los paquetes de aplicaciones virtuales contienen un manifiesto que proporciona toda la información básica del paquete. Esta información incluye los valores predeterminados para la configuración del paquete y determina la configuración en el formato más básico (sin ninguna personalización adicional). Si desea ajustar estos valores predeterminados para un usuario o grupo en particular, puede crear y editar los siguientes archivos:

-   Archivo de configuración de usuario

-   Archivo de configuración de implementación

Los archivos. XML anteriores especifican la configuración de paquetes y permiten personalizar los paquetes sin afectar directamente a los paquetes. Cuando se crea un paquete, el secuenciador genera automáticamente los archivos de implementación y configuración de usuario. XML predeterminados con los datos del manifiesto del paquete. Por lo tanto, estos archivos de configuración generados automáticamente simplemente reflejan los valores predeterminados del paquete de la manera en que se configuraron las cosas durante la secuenciación. Si aplica estos archivos de configuración a un paquete en el formulario generado por el secuenciador, los paquetes tendrán la misma configuración predeterminada que viene de su manifiesto. Esto le proporciona una plantilla específica de paquete para empezar si se debe cambiar cualquiera de los valores predeterminados.

**Nota:**  La siguiente información solo se puede usar para modificar los archivos de configuración generados por el secuenciador para personalizar paquetes con el fin de cumplir con requisitos específicos de grupo o usuario.

 

### Contenido del archivo de configuración dinámica

Todas las adiciones, eliminaciones y actualizaciones de los archivos de configuración deben realizarse en relación con los valores predeterminados especificados por la información del manifiesto del paquete. Revise la tabla siguiente:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Archivo Configuration. XML de usuario</p></td>
</tr>
<tr class="even">
<td align="left"><p>Archivo Configuration. XML de implementación</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manifiesto del paquete</p></td>
</tr>
</tbody>
</table>

 

La tabla anterior representa cómo se leerán los archivos. La primera entrada representa lo que se leerá en último lugar, por lo que su contenido tiene prioridad. Por lo tanto, todos los paquetes contienen de forma inherente la configuración predeterminada del manifiesto del paquete. Si se aplica un archivo Configuration. XML de implementación con una configuración personalizada, se anularán los valores predeterminados del manifiesto del paquete. Si se aplica un archivo Configuration. XML de usuario con una configuración personalizada antes de ese, se reemplazará la configuración de implementación y los valores predeterminados del manifiesto del paquete.

En la siguiente lista se muestra más información sobre los dos tipos de archivo:

-   **Archivo de configuración de usuario (UserConfig)** : permite especificar o modificar la configuración personalizada de un paquete. Esta configuración se aplicará a un usuario específico cuando el paquete se implemente en un equipo que ejecute el cliente de App-V 5,0.

-   **Archivo de configuración de implementación (DeploymentConfig)** : permite especificar o modificar la configuración predeterminada de un paquete. Esta configuración se aplicará a todos los usuarios cuando se implemente un paquete en un equipo que ejecute el cliente de App-V 5,0.

Para personalizar la configuración de un paquete para un conjunto específico de usuarios de un equipo o para realizar cambios que se aplicarán a ubicaciones de usuarios locales, como HKCU, debe usar el archivo UserConfig. Para modificar la configuración predeterminada de un paquete para todos los usuarios de un equipo o para realizar cambios que se aplicarán a ubicaciones globales como HKEY \ _LOCAL \ _MACHINE y la carpeta todos los usuarios, se debe usar el archivo DeploymentConfig.

El archivo UserConfig proporciona opciones de configuración que se pueden aplicar a un solo usuario sin afectar a ningún otro usuario de un cliente:

-   Extensiones que se integrarán en el sistema nativo por usuario:-accesos directos, asociaciones de tipo de archivo, protocolos de URL, AppPaths, clientes de software y COM

-   Subsistemas virtuales:-objetos de aplicaciones, variables de entorno, modificaciones de registro, servicios y fuentes

-   Scripts (solo contexto de usuario)

-   Administración de la autoridad (para controlar la coexistencia del paquete con App-V 4,6)

El archivo DeploymentConfig proporciona opciones de configuración en dos secciones, una en relación con el contexto de equipo y una en relación con el contexto de usuario que proporciona las mismas funciones que aparecen en la lista anterior de UserConfig:

-   Toda la configuración de UserConfig arriba

-   Extensiones que solo se pueden aplicar globalmente a todos los usuarios

-   Subsistemas virtuales que se pueden configurar para las ubicaciones de la máquina internacional, por ejemplo, el registro

-   Dirección URL de origen del producto

-   Scripts (solo en el contexto de equipo)

-   Controles para finalizar procesos secundarios

### Estructura de archivos

La estructura del archivo de configuración dinámica de App-V 5,0 se explica en la siguiente sección.

### Archivo de configuración de usuario dinámico

**Header** : el encabezado de un archivo de configuración de usuario dinámico es el siguiente:

&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

El **PackageId** es el mismo valor que existe en el archivo de manifiesto.

**Cuerpo** : el cuerpo del archivo de configuración de usuario dinámico puede incluir todos los puntos de extensión de aplicación que se definen en el archivo de manifiesto, así como información para configurar aplicaciones virtuales. Hay cuatro subsecciones permitidas en el cuerpo:

1. **Aplicaciones** : todas las extensiones de aplicación que se encuentran en el archivo de manifiesto de un paquete se asignan con un identificador de aplicación, que también se define en el archivo de manifiesto. Esto le permite habilitar o deshabilitar todas las extensiones para una aplicación determinada dentro de un paquete. El **identificador** de la aplicación debe existir en el archivo de manifiesto o se omitirá.

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Aplicaciones&gt;

   &lt;!--No se puede definir ninguna aplicación nueva en la Directiva. El cliente de AppV ignorará cualquier identificador de aplicación que no esté incluido en el archivo de manifiesto:&gt;

   &lt;Application ID = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/Applications&gt;

   …

   &lt;/UserConfiguration&gt;

2. **Subsistemas** : AppExtensions y otros subsistemas se organizan como subnodos debajo de los &lt; subsistemas &gt; :

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Subsistemas&gt;

   ..

   &lt;/Subsystems&gt;

   ..

   &lt;/UserConfiguration&gt;

   Cada subsistema se puede habilitar o deshabilitar mediante el atributo "**habilitado**". A continuación se muestran los diversos subsistemas y ejemplos de uso.

   **Prórroga**

   Algunos subsistemas (subsistemas de extensión) controlan las extensiones. Esos subsistemas son:-accesos directos, asociaciones de tipo de archivo, protocolos de URL, AppPaths, clientes de software y COM

   Los subsistemas de extensión se pueden habilitar y deshabilitar independientemente del contenido.  Por lo tanto, si los accesos directos están habilitados, el cliente usará los accesos directos incluidos en el manifiesto de forma predeterminada. Cada subsistema de extensión puede contener &lt; un &gt; nodo de extensiones. Si este elemento secundario está presente, el cliente omitirá el contenido en el archivo de manifiesto de ese subsistema y solo usará el contenido del archivo de configuración.

   Ejemplo de uso del subsistema de accesos directos:

   1.  Si el usuario lo definió en el archivo de configuración dinámica o de implementación:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  Si el usuario ha definido solo lo siguiente:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  Si el usuario define lo siguiente

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   A continuación, se ignorarán todos los métodos abreviados dentro del manifiesto. No habrá ningún acceso directo integrado.

   Los subsistemas de extensión admitidos son:

   **Métodos abreviados:** Esto controla los accesos directos que se integrarán en el sistema local. A continuación se muestra un ejemplo con 2 métodos abreviados:

   &lt;Subsistemas&gt;

   &lt;Accesos directos habilitado = "verdadero"&gt;

     &lt;Extensions&gt;

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     &lt;/Extension&gt;

     &lt;Extension Category = "AppV. Shortcut"&gt;

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     &lt;/Extension&gt;

    &lt;/Extensions&gt;

   &lt;/Shortcuts&gt;

   **Asociaciones de tipo de archivo:** Asocia tipos de archivo con programas para abrir de forma predeterminada y configurar el menú contextual. (Los tipos MIME también se pueden configurar con este susbsystem). La Asociación de tipo de archivo de ejemplo se muestra a continuación:

   &lt;FileTypeAssociations Enabled = "true"&gt;

   &lt;Extensions&gt;

     &lt;Extension Category = "AppV. FileTypeAssociation"&gt;

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      &lt;/Extension&gt;

     &lt;/Extensions&gt;

     &lt;/FileTypeAssociations&gt;

   **Protocolos URL**: Esto controla los protocolos de dirección URL que se integran en el registro local del equipo cliente; por ejemplo, "mailto:".

   &lt;URLProtocols Enabled = "true"&gt;

   &lt;Extensions&gt;

   &lt;Extension Category = "AppV. URLProtocol"&gt;

   &lt;URLProtocol&gt;

     &lt;Nombre &gt; mailto &lt;&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /EditFlags&gt;

     &lt;Texto&gt;

     &lt;AppUserModelId&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;Sugerencia&gt;

   &lt;SourceFilter /&gt;

     &lt;ShellFolder&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;Identificado&gt;

     &lt;ShellCommands&gt;

     &lt;DefaultCommand &gt; abrir &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;

     &lt;Nombre &gt; abierto &lt; /Name&gt;

     &lt;CommandLine &gt; \ [{ProgramFilesX86} \\microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Nota/m "%1" &lt; /commandLine&gt;

     &lt;DropTargetClassId /&gt;

     &lt;Descriptivo&gt;

     &lt;&gt;0 &lt; /Extended&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler /&gt;

     &lt;Application &gt; contosomail &lt; /Application&gt;

     &lt;Tema &gt; ShellSystem &lt; /topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;

     &lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/Extension&gt;

     &lt;/Extension&gt;

     &lt;/URLProtocols&gt;

   **Clientes de software**: permite que la aplicación se registre como un cliente de correo electrónico, un lector de noticias, un reproductor multimedia y haga que la aplicación esté visible en la interfaz de usuario de configuración de acceso y programas predeterminados del equipo. En la mayoría de los casos solo deberás habilitarlo y deshabilitarlo. También hay un control para habilitar y deshabilitar el cliente de correo electrónico específicamente si desea que los otros clientes sigan habilitados, excepto el cliente.

   &lt;SoftwareClients Enabled = "true"&gt;

     &lt;ClientConfiguration EmailEnabled = "falso"/&gt;

   &lt;/SoftwareClients&gt;

   AppPaths:-Si una aplicación por ejemplo contoso.exe se registra con un nombre de AppPath "MyApp", le permite escribir "MyApp" en el menú ejecutar y se abrirá contoso.exe.

   &lt;AppPaths Enabled = "true"&gt;

   &lt;Extensions&gt;

   &lt;Extension Category = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;

     &lt;Nombre &gt;contosomail.exe&lt; /Name&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; falso &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl /&gt;

   &lt;/AppPath&gt;

   &lt;/Extension&gt;

   &lt;/Extensions&gt;

   &lt;/AppPaths&gt;

   **Com**: permite a una aplicación registrar servidores com locales. El modo puede ser integración, aislado o desactivado. Cuando ISOL.

   &lt;Modo COM = "aislado"/&gt;

   **Otras opciones de configuración**:

   Además de las extensiones, se pueden habilitar/deshabilitar otros subsistemas y editarlos:

   **Objetos de núcleo virtual**:

   &lt;Objects Enabled = "false"/&gt;

   **Registro virtual**: se usa si desea establecer un registro en el registro virtual dentro de HKCU

   &lt;Registro habilitado = "true"&gt;

   &lt;Incluir&gt;

   &lt;Ruta de la clave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;Value Type = "REG \ _SZ" Name = "bar" Data = "Nuevovalor"/&gt;

    &lt;/Key&gt;

     &lt;Ruta de la clave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;Borrar&gt;

     &lt;/Registry&gt;

   **Sistema de archivos virtual**

         &lt;FileSystem Enabled="true" /&gt;

   **Fuentes virtuales**

         &lt;Fonts Enabled="false" /&gt;

   **Variables de entorno virtual**

   &lt;EnvironmentVariables Enabled = "true"&gt;

   &lt;Incluir&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **Servicios virtuales**

         &lt;Services Enabled="false" /&gt;

3. **Userscripts** : los scripts se pueden usar para configurar o modificar el entorno virtual, así como para ejecutar scripts en el momento de la implementación o desinstalación, antes de que se ejecute una aplicación o se pueden usar para "limpiar" el entorno después de que la aplicación finalice. Para ver un script de ejemplo, haga referencia a un archivo de configuración de usuario de ejemplo generado por el secuenciador. La sección de scripts que se muestra a continuación proporciona más información sobre los diversos desencadenadores que se pueden usar.

4. **ManagingAuthority** : se puede usar cuando dos versiones de su paquete están coexistentes en la misma máquina, una implementada en App-v 4,6 y la otra implementada en App-v 5,0. Para permitir que App-V vNext tome el control de App-V 4,6 puntos de extensión para el paquete nombrado, escriba lo siguiente en el archivo UserConfig (donde PackageName es el GUID del paquete en App-V 4,6:

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-Acef-76fc5297fe81"/&gt;

### Archivo de configuración de implementación dinámica

**Header** : el encabezado de un archivo de configuración de implementación es el siguiente:

&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

El **PackageId** es el mismo valor que existe en el archivo de manifiesto.

**Cuerpo** : el cuerpo del archivo de configuración de implementación incluye dos secciones:

-   Sección de configuración de usuario: permite el mismo contenido que el archivo de configuración de usuario descrito en la sección anterior. Cuando el paquete se publique para un usuario, cualquier valor de configuración de appextensions en esta sección reemplazará la configuración correspondiente en el manifiesto dentro del paquete, a menos que se proporcione también un archivo de configuración de usuario. Si también se proporciona un archivo UserConfig, se usará en lugar de la configuración de usuario en el archivo de configuración de implementación. Si el paquete se publica globalmente, solo se utilizará el contenido del archivo de configuración de implementación en combinación con el manifiesto.

-   Sección de configuración de la máquina: contiene información que se puede configurar solo para un equipo completo, no para un usuario específico en el equipo. Por ejemplo, HKEY \ _LOCAL \ _MACHINE claves de registro en el VFS.

&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

&lt;UserConfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**Configuración de usuario** : Use la sección anterior del **archivo de configuración de usuario dinámico** para obtener información sobre la configuración que se proporciona en la sección configuración de usuario del archivo de configuración de implementación.

Configuración de la máquina: la sección de configuración del equipo del archivo de configuración de implementación se usa para configurar información que solo se puede establecer para un equipo completo, no para un usuario específico en el equipo. Por ejemplo, HKEY \ _LOCAL \ _MACHINE claves de registro en el registro virtual. Hay cuatro subsecciones permitidas en este elemento

1.  **Subsistemas** : AppExtensions y otros subsistemas se organizan como subnodos en &lt; subsistemas &gt; :

    &lt;MachineConfiguration&gt;

      &lt;Subsistemas&gt;

      ..

      &lt;/Subsystems&gt;

    ..

    &lt;/MachineConfiguration&gt;

    En la siguiente sección se muestran los diversos subsistemas y ejemplos de uso.

    **Extensiones**:

    Algunos subsistemas (subsistemas de extensión) controlan las extensiones que solo se pueden aplicar a todos los usuarios. El subsistema es una función de aplicación. Como esto solo se puede aplicar a todos los usuarios, el paquete debe publicarse globalmente para que este tipo de extensión se integre en el sistema local. Las mismas reglas para los controles y la configuración que se aplican a las extensiones de la configuración de usuario también se aplican a las de la sección MachineConfiguration.

    **Capacidades**de la aplicación: usadas por programas predeterminados en la interfaz del sistema operativo Windows. Permite que una aplicación se registre como capaz de abrir determinadas extensiones de archivo, como un caso de la ranura del explorador de Internet del menú Inicio, como capaz de abrir determinados tipos MIME de Windows.Esta extensión también hace que la aplicación virtual esté visible en la interfaz de usuario de programas predeterminados.

    &lt;ApplicationCapabilities Enabled = "true"&gt;

      &lt;Extensions&gt;

       &lt;Extension Category = "AppV. ApplicationCapabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;CapabilityGroup&gt;

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/Extension&gt;

    &lt;/Extensions&gt;

    &lt;/ApplicationCapabilities&gt;

    **Otras opciones de configuración**:

    Además de las extensiones, se pueden editar otros subsistemas:

    **Registro virtual en todo el equipo**: se usa cuando desea establecer una clave del registro en el registro virtual en HKEY \ _Local \ _Machine

    &lt;Registro&gt;

    &lt;Incluir&gt;

      &lt;Ruta de la clave = "\\REGISTRY\\Machine\\Software\\ABC"&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Key&gt;

      &lt;Ruta de la clave = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;Borrar&gt;

    &lt;/Registry&gt;

    **Objetos de núcleo virtual de todo el equipo**

    &lt;Objeto&gt;

    &lt;NotIsolate&gt;

       &lt;Object name = "testObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/Objects&gt;

2.  **ProductSourceURLOptOut**: indica si la dirección URL del paquete se puede modificar globalmente a través de PackageSourceRoot (para admitir escenarios de sucursales). El valor predeterminado es falso y el cambio de configuración surte efecto en el próximo inicio.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;ProductSourceURLOptOut Enabled = "true"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** : el paquete se puede configurar para que ejecute los scripts en el momento de la implementación, publicación o desinstalación. Para ver un script de ejemplo, haga referencia a un archivo de configuración de implementación generado por el secuenciador. La sección de scripts que se muestra a continuación proporciona más información sobre los diversos desencadenadores que se pueden usar

4.  **TerminateChildProcess**:-se puede especificar un ejecutable de aplicación, cuyos procesos secundarios finalizarán cuando se termine el proceso exe de la aplicación.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### Scripts

En la tabla siguiente se describen los diversos eventos de script y el contexto en el que se pueden ejecutar.

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
<th align="left">Tiempo de ejecución de script</th>
<th align="left">Puede especificarse en la configuración de implementación</th>
<th align="left">Se puede especificar en configuración de usuario</th>
<th align="left">Puede ejecutarse en el entorno virtual del paquete</th>
<th align="left">Puede ejecutarse en el contexto de una aplicación específica</th>
<th align="left">Se ejecuta en el contexto sistema o usuario: (configuración de implementación, configuración de usuario)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SISTEMA, N/A)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Sistema, usuario)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UnpublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Sistema, usuario)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SISTEMA, N/A)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Usuario, usuario)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Usuario, usuario)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Usuario, usuario)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Usuario, usuario)</p></td>
</tr>
</tbody>
</table>

 

### Crear un archivo de configuración dinámica con un archivo de manifiesto de App-V 5,0

Puede crear el archivo de configuración dinámica con uno de estos tres métodos: manualmente, usando la consola de administración de App-V 5,0 o secuenciando un paquete, que se generará con dos archivos de ejemplo.

Para obtener más información sobre cómo crear el archivo con la consola de administración de App-V 5,0, consulte [Cómo crear un archivo de configuración personalizado con la consola de administración de App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

Para crear el archivo manualmente, la información anterior de las secciones anteriores se puede combinar en un solo archivo. Le recomendamos que use los archivos generados por el secuenciador.






## Temas relacionados


[Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





