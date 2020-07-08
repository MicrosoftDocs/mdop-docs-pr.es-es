---
title: Acerca de la configuración dinámica de App-V 5,1
description: Puede usar la configuración dinámica para personalizar un paquete de App-V 5,1 para un usuario. Use la siguiente información para crear o editar un archivo de configuración dinámica existente.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814961"
---
# Acerca de la configuración dinámica de App-V 5,1 
Con la configuración dinámica, puede editar el archivo de configuración dinámica para personalizar cómo se ejecuta un paquete de App-V 5,1 para un usuario o un grupo. La personalización de paquetes elimina la necesidad de reordenar los paquetes con la configuración deseada.  También proporciona una manera de mantener la configuración personalizada y el contenido del paquete.

Los paquetes de aplicaciones virtuales contienen un manifiesto que proporciona toda la información básica del paquete. Esta información incluye los valores predeterminados para la configuración del paquete y determina la configuración en el formato más básico (sin ninguna personalización adicional). 

Cuando se crea un paquete, el secuenciador genera automáticamente los archivos de implementación y configuración de usuario. XML predeterminados con los datos del manifiesto del paquete. Por lo tanto, estos archivos generados reflejan la configuración predeterminada establecida durante la secuenciación. Si aplica estos archivos a un paquete en el formulario generado por el secuenciador, los paquetes tienen la misma configuración predeterminada que viene de su manifiesto. 

Use estos archivos generados para realizar cambios, si es necesario, que no afecten directamente al paquete. Si desea agregar, eliminar o actualizar los archivos de configuración, realice los cambios en los valores predeterminados de la información del manifiesto.

>[!TIP]
>El orden en que se leen los archivos es el siguiente:<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>Manifiesta</li></ul><p>La primera entrada representa lo que se lee en último lugar. Por lo tanto, el contenido tiene prioridad y todos los paquetes contienen y proporcionan la configuración predeterminada del manifiesto del paquete.<ol><li> Si personaliza el DeploymentConfig.xml archivo y aplica la configuración personalizada, se reemplazará la configuración predeterminada del manifiesto del paquete. </li><li> Si personaliza la UserConfig.xml y aplica la configuración personalizada, se reemplazará la configuración predeterminada de la configuración de implementación y el manifiesto del paquete. </li></ol>

## Contenido del archivo de configuración de usuario (UserConfig.xml)
El archivo UserConfig proporciona opciones de configuración que se aplican a un usuario específico al implementar el paquete en un equipo que ejecuta el cliente de App-V 5,1.  Esta configuración no afecta a ningún otro usuario del cliente.

Use el archivo UserConfig para especificar o modificar la configuración personalizada de un paquete:

-   Extensiones integradas en el sistema nativo por usuario: métodos abreviados, asociaciones de tipo de archivo, protocolos de URL, AppPaths, clientes de software y COM
-   Subsistemas virtuales: objetos de aplicaciones, variables de entorno, modificaciones de registro, servicios y fuentes
-   Scripts (solo contexto de usuario)
-   Administración de la autoridad (para controlar la coexistencia del paquete con App-V 4,6)

### Encabezado

El encabezado de un archivo de configuración de usuario dinámico tiene el siguiente aspecto:

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

El **PackageId** es el mismo valor que existe en el archivo de manifiesto.


### Body

El cuerpo del archivo de configuración de usuario dinámico puede incluir todos los puntos de extensión de aplicación definidos en el archivo de manifiesto, así como información para configurar aplicaciones virtuales. Hay cuatro subsecciones permitidas en el cuerpo:

1.  **[Aplicaciones](#applications)** 
2.  **[Subsistemas](#subsystems)**
3.  **[UserScripts](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### Aplicaciones

Todas las extensiones de aplicación contenidas en el archivo de manifiesto de un paquete tienen asignado un identificador de aplicación, que se encuentra en el archivo de manifiesto. El identificador de la aplicación le permite habilitar o deshabilitar todas las extensiones para una aplicación determinada dentro de un paquete. El identificador de la aplicación debe existir en el archivo de manifiesto o se omite.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### Subsistemas

AppExtensions y otros subsistemas dispuestos como subnodos.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

Puede habilitar o deshabilitar cada subsistema con el atributo **habilitado** .

**Extensions** 

Algunos subsistemas (subsistemas de extensión) controlan las extensiones. Esos subsistemas son accesos directos, asociaciones de tipo de archivo, protocolos de URL, AppPaths, clientes de software y COM.

Los subsistemas de extensión se pueden habilitar y deshabilitar independientemente del contenido. Por ejemplo, si habilita los métodos abreviados, el cliente usa los accesos directos incluidos en el manifiesto de forma predeterminada. Cada subsistema de extensión puede contener un \<Extensions\> nodo. Si este elemento secundario está presente, el cliente omite el contenido en el archivo de manifiesto de ese subsistema y solo usa el contenido del archivo de configuración. 

_**Ejemplos:**_ 

- Si se define en el archivo de configuración de implementación o usuario, se omite el contenido del manifiesto.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- Si define solo lo siguiente, el contenido del manifiesto se integrará durante la publicación.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- Si define lo siguiente, se omitirán todos los accesos directos del manifiesto. En otras palabras, los accesos directos no se integran.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**Subsistemas de extensión admitidos:**_ 

El subsistema de extensión de **accesos directos** controla los métodos abreviados que se integran en el sistema local.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

Extensión **de asociados de tipo de archivo** Subsystem asocia tipos de archivo con programas para abrir de forma predeterminada, así como configurar el menú contextual. 

>[!TIP]
>Puede configurar el subsistema con tipos MIME.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

El subsistema de extensión de **protocolos URL** controla los protocolos URL integrados en el registro local del equipo cliente, por ejemplo, _mailto:_. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

El subsistema de extensión de **clientes de software** permite que la aplicación se registre como un cliente de correo electrónico, un lector de noticias, un reproductor multimedia y haga que la aplicación esté visible en la interfaz de usuario de configuración de acceso y programas predeterminados del equipo. En la mayoría de los casos, solo deberás habilitarlo y deshabilitarlo. También hay un control para habilitar y deshabilitar el cliente de correo electrónico específicamente si desea que los otros clientes sigan habilitados, excepto el cliente.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

El subsistema de extensión de **AppPaths** abre aplicaciones registradas con una ruta de acceso de la aplicación. Por ejemplo, si contoso.exe tiene un nombre AppPath de _MyApp_, los usuarios pueden escribir _MyApp_ en el menú ejecutar, abriendo contoso.exe.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

El subsistema de extensiones **com** permite una aplicación registrada en servidores com locales. El modo puede ser:

-   Integrada
-   Dividido 
-   Desactivado

```XML

<COM Mode="Isolated"/>
```

**Objetos de núcleo virtual**

```XML

<Objects Enabled="false" />
```

El **registro virtual** establece un registro en el registro virtual dentro de HKCU.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Sistema de archivos virtual**

```XML

    <FileSystem Enabled="true" />
```

**Fuentes virtuales**

```XML

      <Fonts Enabled="false" />
```

**Variables de entorno virtual**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**Servicios virtuales**

```XML

      <Services Enabled="false" />
```

#### UserScripts

Use UserScripts para configurar o modificar el entorno virtual.  También puede ejecutar scripts en el momento de la implementación o para limpiar el entorno después de que finalice la aplicación. Para ver un script de ejemplo, consulte el archivo de configuración de usuario generado por el secuenciador. La sección de scripts que se muestra a continuación proporciona más información sobre los diversos desencadenadores que se pueden usar.

#### ManagingAuthority

Use ManagingAuthority cuando dos versiones de su paquete coexistan en el mismo equipo, una implementada en App-V 4,6 y otra implementada en App-V 5,0. Para permitir que App-V vNext tome el control de App-V 4,6 puntos de extensión para el paquete nombrado, escriba lo siguiente en el archivo UserConfig (donde PackageName es el GUID del paquete en App-V 4,6:

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## Archivo de configuración de implementación (DeploymentConfig.xml)

El archivo DeploymentConfig proporciona opciones de configuración para el contexto del equipo y el contexto del usuario, y proporciona las mismas funciones que aparecen en el archivo UserConfig. La configuración se aplica al implementar el paquete en un equipo que ejecuta el cliente de App-V 5,1.

Use el archivo DeploymentConfig para especificar o modificar la configuración personalizada de un paquete:

- Toda la configuración de UserConfig
- Extensiones que solo se pueden aplicar globalmente a todos los usuarios
- Subsistemas virtuales para ubicaciones de máquinas globales, por ejemplo, el registro
- Dirección URL de origen del producto
- Scripts (solo en el contexto de equipo)
- Controles para finalizar procesos secundarios

### Encabezado

El encabezado de un archivo de configuración de implementación dinámico tiene el siguiente aspecto:

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

El **PackageId** es el mismo valor que existe en el archivo de manifiesto.

### Body

El cuerpo del archivo de configuración de implementación dinámica incluye dos secciones:

- **UserConfiguration:** permite el mismo contenido que el archivo de configuración de usuario descrito en la sección anterior.  Al publicar el paquete para un usuario, cualquier valor de configuración de appextensions en esta sección reemplaza la configuración correspondiente en el manifiesto dentro del paquete, a menos que proporcione un archivo de configuración de usuario. Si también proporciona un archivo UserConfig, se usa en lugar de la configuración de usuario en el archivo de configuración de implementación. Si publica el paquete globalmente, solo el contenido del archivo de configuración de la implementación se usa en combinación con el manifiesto. Para obtener más información, consulte [contenido del archivo de configuración de usuario (UserConfig.xml)](#user-configuration-file-contents-userconfigxml).

- **MachineConfiguration:** contiene información que se puede configurar solo para un equipo completo, no para un usuario específico en el equipo. Por ejemplo, HKEY_LOCAL_MACHINE las claves del registro en el VFS.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### UserConfiguration

Para obtener información sobre la configuración proporcionada para esta sección [, consulte contenido del archivo de configuración de usuario (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) . 

### MachineConfiguration

Use la sección MachineConfiguration para configurar información de todo un equipo; no es para un usuario específico en el equipo. Por ejemplo, HKEY_LOCAL_MACHINE claves de registro en el registro virtual. Hay cuatro subsecciones permitidas en este elemento:

1.  **[Subsistemas](#subsystems-1)**
2.  **[ProductSourceURLOptOut](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### Subsistemas

AppExtensions y otros subsistemas dispuestos como subnodos.

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

Puede habilitar o deshabilitar cada subsistema con el atributo **habilitado** .

**Extensions** 

Algunos subsistemas (subsistemas de extensión) controlan las extensiones. El subsistema es la funcionalidad de las aplicaciones que usan los programas predeterminados. Para este tipo de extensión, el paquete debe publicarse globalmente para integrarse en el sistema local. Las mismas reglas para los controles y la configuración que se aplican a las extensiones de la configuración de usuario también se aplican a las que figuran en la sección MachineConfiguration.

**Capacidades**de la aplicación: utilizan programas predeterminados que permiten que una aplicación se registre como sigue:

- Posibilidad de abrir extensiones de archivo específicas
- Un espacio para el área del explorador de Internet del menú Inicio
- Posibilidad de abrir tipos específicos de MIME de Windows

Esta extensión también hace que la aplicación virtual esté visible en la interfaz de usuario de programas predeterminados.

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**Subsistemas de extensión admitidos:**_ 

El subsistema de extensión de **registro virtual para todo el equipo** establece una clave del registro en el registro Virtual en HKEY_LOCAL_MACHINE.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Objetos de núcleo virtual de todo el equipo**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### ProductSourceURLOptOut

Use ProductSourceURLOptOut para indicar que la dirección URL para el paquete se puede modificar globalmente a través de _PackageSourceRoot_ (para admitir escenarios de sucursales). Los cambios se aplicarán en el próximo inicio. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

El paquete se puede configurar para que ejecute scripts en el momento de la implementación, la publicación o la eliminación. Para ver un script de ejemplo, consulte el archivo de configuración de implementación generado por el secuenciador. 

La sección de scripts que se muestra a continuación proporciona más información sobre los diversos desencadenadores que se pueden usar.

#### TerminateChildProcess

Se puede especificar un ejecutable de la aplicación, cuyos procesos secundarios se terminan cuando el proceso exe de la aplicación finaliza.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## Scripts

En la tabla siguiente se describen los diversos eventos de script y el contexto en el que se pueden ejecutar.

| Tiempo de ejecución de script       | Puede especificarse en la configuración de implementación | Se puede especificar en configuración de usuario | Puede ejecutarse en el entorno virtual del paquete | Puede ejecutarse en el contexto de una aplicación específica | Se ejecuta en el contexto sistema o usuario: (configuración de implementación, configuración de usuario) |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (SISTEMA, N/A)                                                               |
| PublishPackage              | X                                            | X                                      |                                                   |                                                     | (Sistema, usuario)                                                              |
| UnpublishPackage            | X                                            | X                                      |                                                   |                                                     | (Sistema, usuario)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (SISTEMA, N/A)                                                               |
| StartProcess                | X                                            | X                                      | X                                                 | X                                                   | (Usuario, usuario)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (Usuario, usuario)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (Usuario, usuario)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (Usuario, usuario)                                                                |

### Uso de varios scripts en un solo desencadenador de eventos

App-V 5,1 admite el uso de varios scripts en un solo desencadenador de eventos para paquetes de App-V, incluidos los paquetes que se convierten de App-V 4,6 a App-V 5,0 o posterior. Para habilitar el uso de varios scripts, App-V 5,1 usa una aplicación de iniciador de scripts, denominada ScriptRunner.exe, que se instala como parte de la instalación del cliente de App-V.

### Cómo usar varios scripts en un único desencadenador de eventos

Para cada script que desee ejecutar, pase el script como un argumento a la aplicación ScriptRunner.exe. Después, la aplicación ejecuta cada script por separado, junto con los argumentos especificados para cada script. Use solo un script (ScriptRunner.exe) por desencadenador.

> [!NOTE]
> 
> Le recomendamos que ejecute la línea de varias secuencias de comandos desde un símbolo del sistema en primer lugar para asegurarse de que todos los argumentos se generan correctamente antes de agregarlos al archivo de configuración de implementación.

### Scripts de ejemplo y descripciones de parámetros

Con el siguiente ejemplo de archivo y tabla, modifique el archivo de configuración de implementación o de usuario para agregar los scripts que desee ejecutar.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**Entre los parámetros del archivo de ejemplo se incluyen:**

#### \<AddPackage\>

Nombre del desencadenador de eventos para el que se está ejecutando una secuencia de comandos, como agregar un paquete o publicar un paquete.

#### \<Path\>ScriptRunner.exe\</Path\>

La aplicación script iniciador que se instala como parte de la instalación del cliente de App-V.

> [!NOTE]
> 
> Aunque ScriptRunner.exe se instala como parte del cliente de App-V, la ubicación del cliente de App-V debe ser% path% o ScriptRunner no se ejecutará. Por lo general, ScriptRunner.exe se encuentra en el C:FilesApplication Virtualizationfolder.

#### \<Arguments\>

`-appvscript` -Token que representa el script real que desea ejecutar.

`script1.exe` : Nombre del script que desea ejecutar.

`arg1 arg2` : Argumentos para el script que desea ejecutar.

`-appvscriptrunnerparameters` : Token que representa las opciones de ejecución de script1.exe.

`-wait` – Token que informa a ScriptRunner de que debe esperar a que se complete la ejecución de script1.exe antes de continuar con el siguiente script.

`-timeout=x` : Token que informa a ScriptRunner de que deje de ejecutar el script actual después de x cantidad de segundos. El resto de las secuencias de comandos especificadas aún se ejecutan.

`-rollbackonerror` – Token que informa a ScriptRunner detener la ejecución de todos los scripts que aún no se han ejecutado y para deshacer un error en el cliente de App-V.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

Espera a que se complete globalmente ScriptRunner.exe.

Configure el valor de tiempo de espera para que el corredor global sea mayor o igual que la suma de los valores de tiempo de espera en los scripts individuales.

Si algún script individual informó de un error y rollbackonerror se estableció en true, ScriptRunner notificaría el error al cliente App-V.

ScriptRunner ejecuta cualquier script cuyo tipo de archivo esté asociado a una aplicación instalada en el equipo. Si falta la aplicación asociada o el tipo de archivo del script no está asociado con ninguna aplicación del equipo, el script no se ejecuta.

### Crear un archivo de configuración dinámica con un archivo de manifiesto de App-V 5,1

Puede crear el archivo de configuración dinámica con uno de estos tres métodos: manualmente, usando la consola de administración de App-V 5,1 o secuenciando un paquete, que genera dos archivos de ejemplo. Para obtener más información sobre cómo crear el archivo con la consola de administración de App-V 5,1, consulte [Cómo crear un archivo de configuración personalizado con la consola de administración de App-v 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

Para crear el archivo manualmente, la información anterior de las secciones anteriores se puede combinar en un solo archivo. Le recomendamos que use los archivos generados por el secuenciador.



- Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).
- Para los problemas de App-V, use el [Foro de TechNet de App-v](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados

- [Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [Operaciones de App-V 5.1](operations-for-app-v-51.md)

---
