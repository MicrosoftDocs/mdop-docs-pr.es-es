---
title: Solución de problemas de instalación de MBAM 2.5
description: Introducción a la solución de problemas de instalación de MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812863"
---
# Solución de problemas de instalación de MBAM 2.5

En este artículo se presenta cómo solucionar problemas de instalación de Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 en una configuración independiente.

## Referencia de los archivos de registro de MBAM para la solución de problemas

MBAM incluye el registro de instalación de servidor, instalación de cliente y eventos. Debe hacerse referencia a este registro para la solución de problemas. 
 
### Archivos de registro de instalación de MBAM Server

MBAMServerSetup.exe genera los siguientes archivos de registro en la carpeta% Temp% del usuario durante la instalación de MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 números>. log**

MBAMServerSetup.exe registra las acciones que se llevaron a cabo durante la instalación de MBAM y MBAM Server Feature:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log**

MBAMServerSetup.exe registra las acciones adicionales que se llevaron a cabo durante la instalación.

### Archivo de registro de instalación del cliente MBAM

La instalación del cliente se registra en el siguiente archivo de registro en la carpeta% Temp% (o en una ubicación personalizada, según la instalación del cliente): <br />**MSI \<five random characters\> . log**

Este registro contiene las acciones que se realizan durante la instalación del cliente de MBAM.
 
### Canal de registro de eventos de cliente de MBAM

MBAM tiene canales de registro de eventos separados. Los archivos de registro, analítico y operativo se encuentran en el visor de eventos, en **registros de aplicaciones y servicios**de  >  **Microsoft**  >  **Windows**  >  **MBAM**.

En la tabla siguiente se proporciona una breve descripción de cada registro de eventos.
 
|Registro de eventos| Descripción|
|----------|-------|
|Microsoft-Windows-MBAM/admin|  Contiene mensajes de error|
|Microsoft-Windows-MBAM/analítico|   Contiene información de registro avanzada|
|Microsoft-Windows-MBAM/Operational|    Contiene mensajes de éxito|

### MBAM: canal de registro de eventos del servidor

Los archivos de registro se encuentran en el visor de eventos, en **registros de aplicaciones y servicios**de  >  **Microsoft**  >  **Windows**  >  **MBAM**. En la tabla siguiente se incluyen los registros de eventos del servidor que se introdujeron en MBAM 2,5:

|Registro de eventos| Descripción|
|--------|-------------|
|Microsoft-Windows-MBAM/admin|  Contiene mensajes de error|
|Microsoft-Windows-MBAM/analítico|   Contiene información de registro avanzada|
|Microsoft-Windows-MBAM/Operational|    Contiene mensajes de éxito|

### Registros de servicio Web de MBAM

Cada registro del servicio Web de MBAM escribe la información de registro en un archivo de SVCLOG. De forma predeterminada, cada servicio web escribe el archivo de seguimiento en una carpeta que usa su nombre en la carpeta C:\inetpub\Microsoft de administración de BitLocker de Solution\Logs.

Puede usar la herramienta Service Trace Viewer (parte de Microsoft Visual Studio) para revisar los seguimientos de svclog.

## Solución de problemas de cifrado e informes

Esta sección contiene información de solución de problemas para la funcionalidad del servidor, la funcionalidad del cliente, la configuración y los problemas conocidos:
 
### Instalación de cliente de MBAM, configuración de directiva de grupo

Determine si el agente de MBAM está instalado en el equipo cliente. Cuando MBAM está instalado, crea un servicio que se denomina servicio de cliente de administración de BitLocker. Este servicio está configurado para iniciarse automáticamente. Determine si el servicio se está ejecutando.

Asegúrese de que la configuración de directiva de grupo MBAM se aplica en el equipo cliente. Si la configuración de directiva de grupo se aplicó en el equipo cliente, se crea la siguiente subclave del registro: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Compruebe que esta clave existe y se rellena mediante valores por configuración de directiva de grupo.

### Agente de MBAM en el período de demora inicial

El cliente de MBAM no inicia la operación inmediatamente después de la instalación. Hay un retraso aleatorio inicial de 1 a 18 minutos antes de que el agente de MBAM inicie su funcionamiento. Además del retraso inicial, se produce un retraso de al menos 90 minutos. (El retraso depende de la configuración de directiva de grupo que se haya configurado para la frecuencia de comprobar el estado del cliente). Por lo tanto, el retraso total antes de que se inicie un cliente es el *Inicio aleatorio*retraso de la  +  *frecuencia de comprobación del cliente*.

Si los registros de eventos operativos y de administración están en blanco, el cliente aún no ha iniciado la operación y se encuentra en el período de retraso que se mencionó anteriormente. Si desea eludir el retraso, siga estos pasos:
 
1. Detenga el servicio del cliente de administración de BitLocker.

2. En la subclave del registro **HKEY_LOCAL_MACHINE \software\microsoft\mbam** , cree el valor del registro **NoStartupDelay** , establezca su tipo en **REG_DWORD**y, a continuación, establezca su valor en **1**.

3. En **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**, establezca los valores de **ClientWakeupFrequency** y **StatusReportingFrequency** en **1**. Estos valores volverán a la configuración original después de que las actualizaciones de la Directiva de grupo estén en el equipo.

4. Inicie el servicio del cliente de administración de BitLocker.

Después de iniciar el servicio, si inicia sesión de forma local en el equipo y no se producen errores, debe recibir una solicitud para cifrar el equipo en un minuto. Si no recibe una solicitud, debe revisar los registros del administrador de MBAM para ver si hay alguna entrada de error.

### El equipo no tiene un dispositivo TPM o el dispositivo TPM no está habilitado en el BIOS

Revise el registro de eventos del administrador de MBAM. Verá una entrada de evento similar a la siguiente en el registro de eventos de administración de MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

Abra administración de TPM (TPM. msc) y compruebe si el equipo tiene un dispositivo TPM. Si TPM. msc no muestra un dispositivo, abra el administrador de dispositivos (devmgmt. msc) y compruebe si hay un módulo de plataforma de confianza en dispositivos de seguridad. Si no ves un dispositivo módulo de plataforma segura, esto puede deberse a una de las siguientes razones:

* El sistema no tiene un dispositivo de módulo de plataforma segura (TPM o seguridad).

* El dispositivo TPM está deshabilitado en el BIOS.

* El dispositivo TPM está habilitado en el BIOS, pero la administración del dispositivo TPM de la configuración del sistema operativo está deshabilitada en el BIOS.

* No está usando un controlador de Microsoft para el dispositivo TPM. Revise los dispositivos que aparecen en el administrador de dispositivos para identificar el controlador de dispositivo TPM de Microsoft.

Si el dispositivo TPM no usa el controlador de C:\Windows\System32\tpm.sys, debe actualizar el controlador seleccionando el archivo C:\Windows\Inf\tpm.inf.

### El equipo no tiene una partición de sistema válida

Revise el registro de eventos del administrador de MBAM. Verá una entrada de evento similar a la siguiente en el registro de eventos de administración de MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

BitLocker requiere una partición de sistema para habilitar el cifrado ([cifrado de unidad BitLocker en Windows 7: preguntas más frecuentes](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM no crea la partición del sistema automáticamente. Puede usar la utilidad de preparación de unidad BitLocker (bdehdcfg.exe) para crear la partición del sistema y mover los archivos de inicio necesarios.

Por ejemplo, puede usar el comando **% WINDIR% \system32\bdeHdCfg.exe-tamaño predeterminado 300-Quiet** para preparar la unidad silenciosamente antes de implementar MBAM para cifrar las unidades. Esto requiere un reinicio. También puede crear una secuencia de comandos para la acción si es necesario. En el siguiente documento se describe la herramienta de preparación de unidad BitLocker:

[Descripción de la herramienta de preparación de unidad BitLocker](https://support.microsoft.com/help/933246)

### Las unidades no tienen el formato de un sistema de archivos compatible

Consulte el [artículo de TechNet para conocer los requisitos del sistema de archivos para BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).

### Conflicto de directiva de grupo

Verá una entrada de evento similar a la siguiente en el registro de eventos de administración de MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

Compruebe la configuración de directiva de grupo para asegurarse de que no tiene una configuración conflictiva entre la configuración de directiva de grupo MBAM.

Debe configurar la Directiva de grupo mediante la plantilla MDOP MBAM y no la plantilla cifrado de unidad BitLocker.

Por ejemplo:

En configuración de cifrado de unidad del sistema operativo, seleccionó TPM como protector y también seleccionó **permitir PIN mejorados para el inicio**. Se trata de una configuración en conflicto porque la protección de TPM solo necesita un PIN. Por lo tanto, debe deshabilitar la configuración de PIN mejorados.

### Es posible que el usuario haya solicitado una exención

Si habilitó la configuración de directiva configuración del Equipo\plantillas Administrativas\componentes de Components\MDOP MBAM (administración de BitLocker) \Client Management\Configure la Directiva de exención de usuarios, se le ofrecerá a los usuarios la opción de solicitar una exención.

De forma predeterminada, si el usuario solicita una exención, la exención será válida durante 7 días y el usuario no recibirá mensajes para cifrar durante este período. (El valor predeterminado se puede aumentar o disminuir durante la configuración de la Directiva). Una vez que haya finalizado el período de exención, se le pedirá que lo Cifre el usuario.

Verá la siguiente entrada en el registro de eventos del administrador de MBAM cuando un equipo se encuentra en exención de usuario:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

Si desea invalidar manualmente la exención de usuario para un equipo, siga estos pasos:
 
1. Establezca el valor AllowUserExemption en **0** debajo de la siguiente subclave del registro: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Elimine todos los valores del registro de la subclave del Registro siguiente, excepto para **AgentVersion**, **EncodedComputerName**e **instalado**:<br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM**

    **Nota:** Debe reiniciar el agente de MBAM para que los cambios surtan efecto.

Tenga en cuenta que después de aplicar la Directiva de grupo al equipo, estos valores pueden revertir a su configuración original.

### Problema de WMI

MBAM usa los métodos de la clase win32_encryptablevolume para administrar BitLocker. Si este módulo no está registrado o está dañado, el cliente de MBAM no funcionará correctamente y verá la siguiente entrada de evento en el registro de eventos del administrador de MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

Además, es posible que observe que las directivas de recuperación y de hardware no se aplican con el código de error 0x8007007e. Esto se traduce en "no se pudo encontrar el módulo especificado".

Para resolver este problema, debe volver a registrar la clase **win32_encryptablevolume** con el siguiente comando:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## Solución de problemas de comunicación del agente de MBAM

Esta sección contiene información para la solución de problemas de los siguientes problemas relacionados con la comunicación del agente de MBAM:

### Dirección URL de servicio MBAM incorrecta

Si el valor de MBAM servicio de estado de cumplimiento o servicio de recuperación y hardware es incorrecto, verá una entrada de evento similar a la siguiente en el registro de eventos del administrador de MBAM en el equipo cliente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

Compruebe los valores de **KeyRecoveryServiceEndPoint** y **StatusReportingServiceEndpoint** bajo la siguiente subclave del registro en el equipo cliente: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

De forma predeterminada, la dirección URL de KeyRecoveryServiceEndPoint (MBAM recuperación y el extremo del servicio de hardware) tiene el siguiente formato: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.SVC**

De forma predeterminada, la dirección URL de StatusReportingServiceEndpoint (MBAM de servicio de informes de estado) tiene el siguiente formato:<br />
**http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.SVC**

> [!Note]
> No debe haber espacios en la dirección URL.

Si la dirección URL del servicio es incorrecta, debe corregir la dirección URL del servicio en la siguiente configuración de directiva de Grupo:

**Configuración**  >  del equipo **Directivas**  >  **Plantillas administrativas**  >  **Componentes**  >  de Windows **MDOP MBAM (administración de BitLocker)**  >  **Administración**  >  de clientes **Configurar servicios de MBAM**

### Problema de conectividad que afecta al servidor de administración de MBAM

El agente de MBAM no podrá enviar actualizaciones a la base de datos si existen problemas de conectividad entre el agente de cliente y el servidor de administración de MBAM. En este caso, observará entradas de errores de conectividad en el registro de eventos del administrador de MBAM en el equipo cliente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

Comprobaciones básicas:

* Para comprobar la conectividad básica, haga ping al servidor de administración de MBAM por nombre y dirección IP. Compruebe si puede conectarse al sitio web de administración de MBAM o al puerto de servicio mediante telnet o Portqry.

* Compruebe que el servicio de IIS se está ejecutando en el servidor de supervisión y administración de MBAM y que el servicio Web de MBAM está escuchando en el mismo puerto que está configurado en el equipo cliente de MBAM ( `netstat –ano | find "portnumber"` ).

* Compruebe que el número de puerto configurado para el sitio web de MBAM está usando IIS Manager (inetmgr). Asegúrese de que el número de puerto es el mismo que el número de puerto en el que está escuchando el cliente. Asegúrese de que otra aplicación no comparta el número de puerto. Por ejemplo, otra aplicación del servidor no debe usar el mismo puerto.

* Si hay un firewall, asegúrese de que el puerto está abierto en el firewall o en el servidor proxy.

* Si la comunicación entre el cliente y el servidor es segura, asegúrese de que está usando un certificado SSL válido.

* Compruebe la conectividad de red entre el servidor Web y el servidor de base de datos al que se envían los datos para su inserción. Puede comprobar la conectividad de la base de datos desde el servidor Web con el servidor de base de datos mediante el administrador de orígenes de datos ODBC. La información detallada sobre la solución de problemas de conexión de SQL Server está disponible [para solucionar problemas de conexión con el motor de base de datos de SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### Solución de problemas de conectividad

Asegúrese de que la dirección URL de servicio configurada en el cliente es correcta. Copie el valor de la dirección URL de KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) desde el registro y ábralo en Internet Explorer.

De forma similar, copie el valor de la dirección URL para StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) y ábralo en Internet Explorer.

> [!Note]
> Si no puede ir a la dirección URL desde el equipo cliente, debe probar la conectividad de red básica desde el cliente al servidor que ejecuta IIS. Vea los puntos 1, 2, 3 y 4 de la sección anterior.

Además, revise los registros de la aplicación en el servidor de supervisión y administración en busca de errores.

Puede realizar un seguimiento de red simultáneo entre el cliente y el servidor, y revisar el seguimiento para determinar la causa de un error de conexión entre el agente del cliente y el servidor de administración de MBAM.

> [!Note]
> Si puede ir a las direcciones URL del servicio desde el equipo cliente y se han producido errores de conectividad en los registros de eventos de administración de MBAM, esto puede deberse a un error de conectividad entre el servidor de administración y el servidor de base de datos.

Si puede examinar correctamente las direcciones URL del servicio y hay conectividad entre el cliente y el servidor que se está ejecutando, IIS está funcionando. Sin embargo, es posible que haya un problema en la comunicación entre el servidor que ejecuta IIS y el servidor de base de datos.

Es posible que los servicios de MBAM no puedan conectarse al servidor de base de datos debido a un problema de red o a una configuración incorrecta de la cadena de conexión de la base de datos. Revise los registros de aplicaciones en el servidor de administración y supervisión. Es posible que aparezcan entradas de errores o advertencias de ASP.NET de origen 2.0.50727.0 que se parezcan a la entrada de registro siguiente:

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### Posibles causas

##### Causa 1

El administrador puede haber especificado un nombre de instancia de base de datos o un nombre de base de datos no válidos durante la instalación de los componentes del servidor de supervisión y administración.

Puede comprobar y corregir las cadenas de conexión de la base de datos con la consola de administración de IIS. Para ello, abra el administrador de IIS y vaya a administración y supervisión de Microsoft BitLocker. Para cada servicio que aparece en la parte izquierda, siga estos pasos para cambiar las cadenas de conexión de la base de datos:

1. En la **vista características**, seleccione las **cadenas de conexión**.

2. En la página **cadenas de conexión** , seleccione la cadena de conexión que quiere cambiar.

3. En el panel **acciones** , seleccione **Editar**.

4. En el cuadro de diálogo **Editar cadena de conexión** , cambie las propiedades que desee cambiar y, a continuación, seleccione **Aceptar**.

##### Causa 2

Puerto de SQL Server bloqueado en el firewall. Compruebe el número de puerto al que está configurado SQL Server para que escuche y asegúrese de que el puerto está abierto en el Firewall entre el servidor de administración y el servidor de base de datos.

##### Causa 3

Enlaces TCP/IP incorrectos de SQL Server. Compruebe los enlaces TCP/IP de SQL en el administrador de configuración de SQL Server en el servidor de bases de datos. MBAM requiere que los protocolos TCP/IP y las canalizaciones con nombre estén habilitados para conectarse a la base de datos.

##### Causa 4

La cuenta de equipo del servidor NT Authority\Network Service o de la administración de MBAM no tiene los permisos necesarios para conectarse a la base de datos SQL.

Durante la instalación de los componentes de base de datos en el servidor de base de datos, el instalador crea dos grupos locales: MBAM de cumplimiento de la auditoría de cumplimiento y MBAM recuperación y acceso de BD de hardware.

La cuenta NT Authority\Network Service, la cuenta de equipo del servidor de administración de MBAM y el usuario que instala los componentes de base de datos se agregan automáticamente a estos grupos.

A estos grupos se les conceden los permisos necesarios en la base de datos durante la instalación. Todos los usuarios que forman parte de este grupo reciben automáticamente los permisos necesarios en la base de datos.

El servicio Web no puede conectarse al servidor de base de datos debido a un problema de permisos si se cumplen una o varias de las condiciones siguientes:

* Los grupos mencionados anteriormente se quitan de los grupos locales en el servidor de base de datos.

* La cuenta NT Authority\Network Service y la cuenta de equipo del servidor de administración de MBAM no son miembros de estos grupos.

* Estos grupos no tienen los permisos necesarios en la base de datos.

Observará errores relacionados con los permisos en los registros de aplicaciones en el servidor de supervisión y administración de MBAM si se cumple alguna de las condiciones anteriores. En ese caso, debe agregar manualmente la cuenta NT Authority\Network Service y la cuenta de equipo del servidor de administración de MBAM y concederles una función pública para todo el servidor en el servidor de bases de datos SQL que usa SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### Revisar los registros del servicio Web

Si no hay eventos registrados en los registros de aplicaciones del servidor de administración de MBAM, es el momento de revisar los registros de servicio Web (. svclog) del servicio Web de MBAM que se hospeda en el servidor de supervisión y administración de MBAM. Para ver el archivo de registro, tendrá que usar la herramienta Service Trace Viewer (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .

Debe investigar principalmente los registros de seguimiento de servicios de RecoveryandHardwareService y ComplianceStatusService. De forma predeterminada, los registros del servicio Web se encuentran en la C:\inetpub\Microsoft de administración de BitLocker de Solution\Logs. Allí, cada servicio escribe el archivo. svclog en su propia carpeta.

Revise la actividad en el registro de seguimiento del servicio para comprobar si hay errores o advertencias. De forma predeterminada, las entradas de error se resaltan en rojo. Seleccione la descripción del error en el panel derecho del visor de seguimiento para ver información detallada sobre la entrada de error. A continuación se muestra un error de la entrada del registro de seguimiento:

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## Reinstalación o reconfiguración de la infraestructura de MBAM

Para reinstalar o volver a configurar la infraestructura de MBAM, debe conocer las siguientes características:

* Cuenta del grupo de aplicaciones

* Grupos MBAM (Departamento de soporte técnico, avanzado, grupo de usuarios de informes)

* URL de informes de MBAM

* Nombre de servidor SQL Server y nombres de bases de datos

* Cuentas de MBAM ReadWrite y ReadOnly

### Cuenta del grupo de aplicaciones

Para encontrar la cuenta del grupo de aplicaciones, inicie sesión en el servidor Web de MBAM, Abra **Administrador de Internet Information Services (IIS)** y, a continuación, seleccione **grupos de aplicaciones**:

![grupos de aplicaciones](images/troubleshooting-MBAM-installation-1.png)

El nombre principal de servicio (SPN) debe establecerse en esta cuenta. Esta configuración es muy importante para la funcionalidad de MBAM.

### Grupos MBAM (soporte, avanzado, grupo de usuarios de informes e URL de informes)

![Grupos de MBAM](images/troubleshooting-MBAM-installation-2.png)

Proporciona información como, por ejemplo, grupo de soporte técnico, grupo avanzado de Helpdesk, grupo de usuarios de informes y URL de informes de MBAM. La dirección URL de los informes de MBAM debe proporcionarse en la configuración de MBAM y debe ser: http (s)://servername/ReportServer.

### Nombre de SQL Server y nombres de base de datos (DB)

Para encontrar los nombres e instancias de SQL Server que hospedan las DBs de MBAM, inicie sesión en el servidor Web de MBAM (IIS) y vaya a la siguiente subclave del registro:

**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

Las partes resaltadas son cadenas de conexión. Deben tener el nombre del servidor SQL, los nombres de base de datos e instancias (si tiene nombre).

### Cuentas de MBAM ReadWrite y ReadOnly

Esta información estará en la base de datos de SQL Server, en la que ya encontramos el nombre del servidor Web.

#### Cuenta ReadWrite

1. Inicie sesión en SQL Management Studio.

2. Haga clic con el botón secundario en **MBAM recuperación y hardware**, seleccione **propiedades**y, a continuación, seleccione **permisos**.

Por ejemplo, el nombre de la cuenta de laboratorio es **MBAMWrite**. El grupo de aplicaciones y las cuentas ReadWrite se configuran para ser iguales.

![BD DE SQL](images/troubleshooting-MBAM-installation-4.png)

![Propiedades de BD](images/troubleshooting-MBAM-installation-5.png)

Vaya a **seguridad** y, a continuación, **inicie sesión** en SQL Management Studio. Vaya a la cuenta que se muestra en la captura de pantalla anterior.

![Seguridad de SQL](images/troubleshooting-MBAM-installation-6.png)

Haga clic con el botón derecho en las cuentas, vaya a **asignación de usuarios de propiedades**y busque la base de datos de recuperación y hardware de MBAM:

![Asignación de usuarios](images/troubleshooting-MBAM-installation-7.png)

#### Cuenta de solo lectura

Abra el administrador de configuración de SQL Server Reporting Services en el servidor SSRS. Seleccione **URL del administrador de informes**y, a continuación, examine las **direcciones URL**:

![Administrador de informes](images/troubleshooting-MBAM-installation-8.png)

Seleccione **Administración y supervisión de Microsoft BitLocker**:

![Administración y supervisión de BitLocker](images/troubleshooting-MBAM-installation-9.png)

Seleccione **MaltaDatasource**:

![Bases](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource debe tener el nombre de cuenta ReadOnly y debe usarse en la configuración de MBAM.

## Referencia

Para obtener más información, consulta los artículos siguientes:

[Implementar MBAM 2,5 en una configuración independiente](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
