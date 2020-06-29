---
title: Acerca de MBAM 2.0 SP1
description: Acerca de MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823551"
---
# Acerca de MBAM 2.0 SP1

En este tema se describen los cambios en administración y supervisión de Microsoft BitLocker (MBAM) 2,0 Service Pack 1 (SP1). Para obtener una descripción general de MBAM, consulte [Introducción a MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>Novedades de MBAM 2,0 SP1

Esta versión de MBAM ofrece las siguientes características y funcionalidades nuevas.

### Soporte técnico para Windows 8,1, Windows Server 2012 R2 y System Center 2012 R2 Configuration Manager

Administración y supervisión de Microsoft BitLocker (MBAM) 2,0 Service Pack 1 (SP1) agrega compatibilidad con Windows 8,1, Windows Server 2012 R2 y el administrador de configuración de System Center 2012 R2.

### Compatibilidad con Microsoft SQL Server 2008 R2 SP2

Administración y supervisión de Microsoft BitLocker (MBAM) 2,0 Service Pack 1 (SP1) agrega compatibilidad con Microsoft SQL Server 2008 R2 SP2. Debe usar Microsoft SQL Server 2008 R2 o versiones posteriores si está ejecutando Microsoft System Center Configuration Manager 2007 R2.

### Informe de comentarios del cliente

MBAM 2,0 SP1 incluye un resumen de las correcciones para solucionar los problemas encontrados desde la versión de administración y supervisión de Microsoft BitLocker (MBAM) 2,0. Como parte de estos cambios, el campo Nombre del equipo aparece ahora en los informes de cumplimiento normativo de equipos y detalles de cumplimiento de BitLocker de BitLocker cuando ejecuta MBAM con Microsoft System Center Configuration Manager 2007.

### La excepción del firewall debe establecerse en los puertos para el portal de autoservicio y el sitio web de administración y supervisión

Cuando configure el portal de autoservicio y el sitio web de administración y supervisión, debe establecer una excepción de Firewall para habilitar la comunicación a través de los puertos especificados. Anteriormente, la instalación del servidor de MBAM abrió automáticamente los puertos en el Firewall de Windows.

### La ubicación de los informes de MBAM ha cambiado en Configuration Manager

Los informes de MBAM para la topología integrada de Configuration Manager ahora están disponibles en subcarpetas dentro del nodo MBAM. Los nombres de las subcarpetas representan el idioma de los informes dentro de la subcarpeta.

### Capacidad de instalar MBAM en un servidor de sitio principal al instalar MBAM con Configuration Manager

Puede instalar MBAM en un servidor de sitio principal o en un servidor de sitio de administración central al instalar MBAM con la topología integrada de Configuration Manager. Anteriormente, se necesitaba instalar MBAM en un servidor de sitio de administración central.

**Importante**  
El servidor en el que instale MBAM debe ser el servidor de nivel superior de la jerarquía.



La instalación de MBAM funciona de forma diferente en Microsoft System Center Configuration Manager 2007 y Microsoft System Center 2012 Configuration Manager de la siguiente manera:

-   **Configuration Manager 2007** : Si instala MBAM en un servidor de sitio principal que forma parte de una jerarquía de Configuration Manager mayor y tiene un servidor principal de sitio central, MBAM resuelve el servidor principal de sitio central y realiza todas las acciones de instalación en ese servidor principal. Las acciones de instalación incluyen la comprobación de los requisitos previos y la instalación de los objetos e informes de Configuration Manager. Por ejemplo, si instala MBAM en un servidor de sitio principal que es un elemento secundario de un servidor principal del sitio central, MBAM instala todos los objetos e informes de Configuration Manager en el servidor principal. Si instala MBAM en el servidor principal, MBAM realiza todas las acciones de instalación en ese servidor principal.

-   **System Center 2012 Configuration Manager** : Si instala MBAM en un servidor de sitio principal o en un servidor de administración central, MBAM realiza todas las acciones de instalación en ese servidor de sitio.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> La consola de Configuration Manager debe instalarse en el equipo en el que se instala el servidor de MBAM

Al instalar MBAM con la topología integrada de Configuration Manager, debe instalar la consola de Configuration Manager en el mismo equipo en el que se instalará MBAM. Si usa la arquitectura recomendada, que se describe en [Introducción: uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), debe instalar MBAM en el servidor de sitio principal de Configuration Manager.

### Nuevos parámetros de la línea de comandos de configuración para la topología integrada de Configuration Manager

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro de la línea de comandos</th>
<th align="left">Descripción</th>
<th align="left">Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>Le permite instalar los informes de Configuration Manager en un servidor remoto de SQL Server Reporting Services (SSRS) que forma parte del mismo sitio de Configuration Manager en el que está instalado MBAM. Puede establecer el valor en el nombre de dominio completo del servidor de roles de Remote SSRS Point.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>Le permite instalar solo los informes de Configuration Manager, sin otros objetos de Configuration Manager, como los elementos de la línea base, la colección y la configuración.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Debe combinar este parámetro con el parámetro CM_REPORTS_COLLECTION_ID.</p>
</div>
<div>

</div>
<p>Valores de parámetro válidos:</p>
<ul>
<li><p>Verdadero</p></li>
<li><p>Falso</p></li>
</ul>
<p>Puede combinar este parámetro con el parámetro CM_SSRS_REMOTE_SERVER_NAME si desea instalar los informes solo en un servidor de roles de SSRS remoto.</p>
<p>Si no establece el parámetro o si lo establece en false, MBAM el programa de instalación instala todos los objetos de Configuration Manager, incluidos los informes.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>Un identificador de colección existente que identifica la colección para la que se mostrarán los datos de cumplimiento de informes. Puede especificar cualquier identificador de colección. No es necesario que use el identificador de colección "equipos compatibles con MBAM".</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### Capacidad para activar o desactivar el texto del portal de autoservicio

MBAM 2,0 SP1 le permite desactivar el texto del aviso en el portal de autoservicio. Anteriormente, el texto del aviso se mostraba de forma predeterminada y no podía desactivarlo.

**Para desactivar el texto del aviso**

1.  En el servidor donde instaló el portal de autoservicio, abra servicios de información de Internet (IIS) y vaya a **sitios &gt; configuración de administración y administración de Microsoft BitLocker &gt; SelfService &gt; configuración**de la aplicación.

2.  En la columna **nombre** , seleccione **DisplayNotice**y establezca el valor en **falso**.

### Capacidad para localizar la instrucción HelpdeskText que dirige a los usuarios a más información del portal de autoservicio

Puede configurar una versión localizada de la instrucción "HelpdeskText" del portal de autoservicio, que indica a los usuarios finales cómo obtener ayuda adicional cuando usan el portal de autoservicio. Si configura el texto localizado de la instrucción, tal y como se describe en las siguientes instrucciones, MBAM mostrará la versión localizada. Si MBAM no encuentra la versión localizada, muestra el valor que está en el parámetro **HelpdeskText** .

**Para mostrar una versión localizada de la instrucción HelpdeskText**

1.  En el servidor en el que ha instalado el portal de autoservicio, abra IIS y vaya a **sitios &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; configuración**de la aplicación.

2.  En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .

3.  En el campo **nombre** , escriba **HelpdeskText**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para el texto. Por ejemplo, para crear una instrucción HelpdeskText localizada en español, tendría que nombrar el parámetro HelpdeskText \ _es-es. Para obtener una lista de los códigos de idioma válidos que puede usar, vea referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  En el campo **valor** , escriba el texto localizado que desea mostrar a los usuarios finales.

### Capacidad para localizar el portal de autoservicio HelpdeskURL

Puede configurar una versión localizada del portal de autoservicio HelpdeskURL para mostrar a los usuarios finales de forma predeterminada. Si crea una versión localizada, tal y como se describe en las siguientes instrucciones, MBAM encuentra y muestra la versión localizada. Si MBAM no encuentra una versión localizada, muestra la dirección URL que está configurada para el parámetro HelpDeskURL.

**Para mostrar una HelpdeskURL localizada**

1.  En el servidor en el que ha instalado el portal de autoservicio, abra IIS y vaya a **sitios &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; configuración**de la aplicación.

2.  En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .

3.  En el campo **nombre** , escriba **HelpdeskURL**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para la dirección URL. Por ejemplo, para crear un HelpdeskURL localizado en español, tendría que nombrar el parámetro HelpdeskURL \ _es-es. Para obtener una lista de los códigos de idioma válidos que puede usar, consulte referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  En el campo **valor** , escriba la HelpdeskURL localizada que desea mostrar a los usuarios finales.

### Capacidad para localizar el texto de aviso del portal de autoservicio

Puede configurar el texto del aviso localizado para que se muestre a los usuarios finales de forma predeterminada en el portal de autoservicio. El archivo de notice.txt, que muestra el texto del aviso, se encuentra en el siguiente directorio raíz:

&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

Para mostrar texto de aviso localizado, cree un archivo de notice.txt localizado y guárdelo en una carpeta de idioma específica en el siguiente directorio:

&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

MBAM muestra el texto del aviso, en función de las siguientes reglas:

-   Si crea un archivo notice.txt localizado en la carpeta de idioma correspondiente, MBAM muestra el texto del aviso localizado.

-   Si MBAM no encuentra una versión localizada del archivo notice.txt, muestra el texto en el archivo predeterminado notice.txt.

-   Si MBAM no encuentra un archivo notice.txt predeterminado, muestra el texto predeterminado en el portal de autoservicio.

**Nota**  
Si el explorador de un usuario final se establece en un idioma que no tiene una subcarpeta de idioma correspondiente o notice.txt, se muestra el texto que está en el archivo de notice.txt en el siguiente directorio raíz:

&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self



**Para crear un archivo de notice.txt localizado**

1.  En el servidor donde instaló el portal de autoservicio, cree una &lt; *language* &gt; carpeta de idioma en el siguiente directorio, donde &lt; *idioma* &gt; representa el nombre del idioma localizado:

    &lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

    **Nota**  
    Algunas carpetas de idioma ya existen, por lo que es posible que no tenga que crearlas. Si necesita crear una carpeta de idioma, vea referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947) para obtener una lista de los nombres válidos que puede usar para la carpeta de &lt; *idioma* &gt; .



2.  Cree un archivo de notice.txt que contenga el texto del aviso localizado.

3.  Guarde el archivo de notice.txt en la carpeta de &lt; *idioma* &gt; . Por ejemplo, para crear un archivo de notice.txt localizado en español, guardaría el archivo notice.txt localizado en la siguiente carpeta:

    &lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\es-es de servicio \\Self

## Actualización a MBAM 2,0 SP1


Puede actualizar a MBAM 2,0 SP1 desde cualquier versión anterior de MBAM.

### Actualización de la infraestructura de MBAM

Puede actualizar la infraestructura del servidor de MBAM a MBAM 2,0 SP1 de la siguiente manera:

**Sustitución de servidor manual local**: debe desinstalar manualmente la infraestructura de servidor de MBAM existente y, a continuación, instalar la infraestructura de servidor de MBAM 2,0 SP1. No es necesario quitar las bases de datos para realizar la actualización. En su lugar, seleccione las bases de datos existentes, que ha creado la versión anterior de MBAM. Después, la instalación de la actualización de MBAM 2,0 SP1 migra las bases de datos existentes a MBAM 2,0 SP1.

**Actualización de cliente distribuido**: Si usa la topología de MBAM independiente, puede actualizar los clientes de MBAM gradualmente después de instalar la infraestructura de servidor de MBAM 2,0 SP1.

Después de actualizar la infraestructura del servidor de MBAM, los clientes de MBAM 1,0 o 2,0 informarán al servidor de MBAM 2,0 SP1 correctamente y guardarán los datos de recuperación, pero el cumplimiento se basará en las directivas disponibles para la versión de cliente MBAM que está instalada en ese momento. Para habilitar la creación de informes con las directivas de MBAM 2,0 SP1, debe actualizar los equipos cliente a MBAM 2,0 SP1. Puede actualizar los equipos cliente al cliente de MBAM 2,0 SP1 sin desinstalar el cliente anterior y el cliente comenzará a solicitarse y notificar, en función de las directivas de MBAM 2,0 SP1.

Para obtener más información sobre cómo actualizar los servidores de MBAM, vea [actualizar desde versiones anteriores de MBAM](upgrading-from-previous-versions-of-mbam.md).

### Actualización del cliente de MBAM a MBAM 2,0 SP1

Para actualizar los equipos de los usuarios finales al cliente de MBAM 2,0 SP1, ejecute **MbamClientSetup.exe** en cada equipo cliente. El instalador actualiza automáticamente el cliente al cliente de MBAM 2,0 SP1. Después de la instalación, los equipos cliente no tienen que reiniciarse y el cliente de MBAM 2,0 SP1 comienza a aplicarse y notificarse contra las directivas de MBAM 2,0 SP1.

Si está usando MBAM con Configuration Manager, debe actualizar los equipos cliente de MBAM a 2,0 MBAM SP1.

Para obtener más información sobre cómo actualizar los equipos cliente de MBAM, vea [actualizar desde versiones anteriores de MBAM](upgrading-from-previous-versions-of-mbam.md).

## Instalar o actualizar a MBAM 2,0 SP1 con Configuration Manager


En esta sección se describen los requisitos cuando está instalando MBAM 2,0 SP1 como una instalación nueva o como una actualización a una instalación anterior de 2,0 MBAM SP1.

### Archivos necesarios para instalar MBAM 2,0 SP1 si está usando MBAM con Configuration Manager

Si está instalando MBAM por primera vez y está usando MBAM 2,0 SP1 con System Center Configuration Manager, debe crear o editar archivos MOF para habilitar MBAM funcione correctamente con Configuration Manager.

-   **archivo Configuration. mof**

    -   Si está usando Configuration Manager 2007, debe editar el archivo Configuration. mof completando el paso 3 del elemento **actualizar el archivo Configuration. mof si actualiza a MBAM 2,0 SP1 y está usando MBAM con Configuration Manager 2007**, que sigue a este elemento.

    -   Si está usando System Center 2012 Configuration Manager, edite el archivo Configuration. mof siguiendo las instrucciones de [editar el archivo Configuration. mof](edit-the-configurationmof-file.md).

-   **SMS \ _def archivo. mof** : siga las instrucciones de [crear o editar el archivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).

### Actualice el archivo Configuration. mof si actualiza a MBAM 2,0 SP1 y está usando MBAM con Configuration Manager 2007

Si está actualizando a MBAM 2,0 SP1 y está usando MBAM con Configuration Manager 2007, debe actualizar el archivo Configuration. mof para asegurarse de que MBAM 2,0 SP1 funcione correctamente.

**Para actualizar el archivo Configuration. mof:**

1.  En el servidor de Configuration Manager, vaya a la ubicación del archivo Configuration. mof:

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    En una instalación predeterminada, la ubicación de instalación es%systemdrive%\\Program archivos (x86) \\Microsoft Configuration Manager.

2.  Revise el bloque de código que ha anexado al archivo Configuration. mof y elimínelo. El bloque de código será similar al que se muestra en el siguiente paso.

3.  Copie el siguiente bloque de código y, después, agréguelo al archivo Configuration. mof para agregar las siguientes clases MBAM necesarias al archivo:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### Traducción de MBAM 2,0 SP1

MBAM 2,0 SP1 ya está disponible en los siguientes idiomas:

-   Inglés (Estados Unidos) en-EE.UU.
-   Francés (Francia) fr-FR
-   Italiano (Italia) ti
-   Alemán (Alemania) de-DE
-   Español, alfabetización Internacional (España) es-ES
-   Coreano ko-KR
-   Japonés (Japón) ja-JP
-   Portugués (Brasil) pt-BR
-   Ruso (Rusia) ru-RU
-   Chino tradicional zh-TW
-   ZH-chino simplificado

## Cómo obtener tecnologías de MDOP

MBAM 2,0 SP1 forma parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Temas relacionados

[Notas de la versión de MBAM 2.0 SP1](release-notes-for-mbam-20-sp1.md)









