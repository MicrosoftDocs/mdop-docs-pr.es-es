---
title: Consideraciones sobre seguridad de MBAM 2.5
description: Consideraciones sobre seguridad de MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826840"
---
# Consideraciones sobre seguridad de MBAM 2.5


Este tema contiene la siguiente información sobre cómo proteger la administración y supervisión de Microsoft BitLocker (MBAM):

-   [Configurar MBAM para custodiar TPM y almacenar OwnerAuth contraseñas](#bkmk-tpm)

-   [Configurar MBAM para que desbloquee TPM automáticamente después de un bloqueo](#bkmk-autounlock)

-   [Conexiones seguras a SQL Server](#bkmk-secure-databases)

-   [Crear cuentas y grupos](#bkmk-accts-groups)

-   [Usar archivos de registro de MBAM](#bkmk-logfiles)

-   [Revisar las consideraciones de la base de datos de MBAM TDE](#bkmk-tde)

-   [Comprender las consideraciones generales de seguridad](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a>Configurar MBAM para custodiar TPM y almacenar OwnerAuth contraseñas

**Nota:** Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM. Además, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM. Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

En función de su configuración, el módulo de plataforma segura (TPM) se bloqueará en determinadas situaciones: como cuando se escriben demasiadas contraseñas incorrectas: y puede permanecer bloqueada durante un período de tiempo. Durante el bloqueo de TPM, BitLocker no puede obtener acceso a las claves de cifrado para realizar operaciones de desbloqueo o descifrado, lo que requiere que el usuario escriba su clave de recuperación de BitLocker para obtener acceso a la unidad del sistema operativo. Para restablecer el bloqueo de TPM, debe proporcionar la contraseña del TPM OwnerAuth.

MBAM puede almacenar la contraseña de OwnerAuth de TPM en la base de datos de MBAM si es propietaria de TPM o si la contraseña se custodia. Las contraseñas de OwnerAuth son fácilmente accesibles en el sitio web de administración y supervisión cuando debe recuperarse desde un bloqueo de TPM, lo que elimina la necesidad de esperar a que el bloqueo se resuelva por sí mismo.

### Custodia de OwnerAuth TPM en Windows 8 y versiones posteriores

**Nota:** Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM. En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM. Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

En Windows 8 o versiones posteriores, MBAM ya no debe poseer el TPM para almacenar la contraseña de OwnerAuth, siempre que la OwnerAuth esté disponible en la máquina local.

Para habilitar MBAM para el depósito de garantía y, a continuación, almacenar las contraseñas de OwnerAuth de TPM, debe configurar estas opciones de directiva de grupo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración de directiva de grupo</th>
<th align="left">Configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Activar la copia de seguridad de TPM en servicios de dominio de Active Directory</p></td>
<td align="left"><p>Deshabilitado o no configurado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar el nivel de información de autorización de propietario de TPM disponible para el sistema operativo</p></td>
<td align="left"><p>Delegado/ninguno o no configurado</p></td>
</tr>
</tbody>
</table>

 

La ubicación de esta configuración de directiva de grupo es **configuración de equipo** &gt; **plantillas administrativas** &gt; **System** &gt; **servicios de módulo de plataforma segura**.

**Nota:**  Windows elimina el OwnerAuth de forma local después de que MBAM lo logró correctamente con esta configuración.

 

### Custodia de OwnerAuth TPM en Windows 7

En Windows 7, MBAM debe poseer el TPM para custodiar automáticamente la información de OwnerAuth de TPM en la base de datos de MBAM. Si MBAM no posee el TPM, debe usar los cmdlets de importación de datos de Active Directory (AD) MBAM para copiar OwnerAuth de TPM de Active Directory a la base de datos MBAM.

### MBAM cmdlets de importación de datos de Active Directory

Los cmdlets de importación de datos de Active Directory de MBAM le permiten recuperar paquetes de claves de recuperación y OwnerAuth contraseñas almacenadas en Active Directory.

El servidor MBAM 2,5 SP1 se suministra con cuatro cmdlets de PowerShell que previamente rellenan las bases de datos de MBAM con la información de recuperación por volumen y de propietario de TPM almacenada en Active Directory.

Para claves de recuperación de volumen y paquetes:

-   Lectura-ADRecoveryInformation

-   Escritura MbamRecoveryInformation

Para información de propietario de TPM:

-   Lectura-ADTpmInformation

-   Escritura MbamTpmInformation

Para asociar usuarios a equipos:

-   Escritura MbamComputerUser

Los cmdlets de lectura de AD \ * leen la información de Active Directory. El cmdlet Write-Mbam \ * inserta los datos en las bases de datos de MBAM. Consulte [Referencia del cmdlet de administración y 2,5 supervisión de Microsoft BitLocker](https://technet.microsoft.com/library/dn459018.aspx) para obtener información detallada sobre estos cmdlets, incluida la sintaxis, los parámetros y los ejemplos.

**Crear asociaciones entre usuarios:** Los cmdlets de importación de datos de Active Directory MBAM recopilan información de Active Directory e insertan los datos en MBAM base de datos. Sin embargo, no asocian usuarios a los volúmenes. Puede descargar el script de PowerShell Add-ComputerUser.ps1 para crear asociaciones entre equipos, lo que permite a los usuarios recuperar el acceso a un equipo a través del sitio web de administración y supervisión o mediante el portal de autoservicio para la recuperación. El script de Add-ComputerUser.ps1 recopila los datos del atributo **administrado por** en Active Directory (ad), el propietario del objeto en ad o un archivo CSV personalizado. La secuencia de comandos agrega los usuarios detectados al objeto de canal información de recuperación, que se debe pasar a write-MbamRecoveryInformation para insertar los datos en la base de datos de recuperación.

Descargue el Add-ComputerUser.ps1 script de PowerShell desde el [centro de descarga de Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).

Puede especificar la **ayuda Add-ComputerUser.ps1** para obtener ayuda sobre el script, incluidos ejemplos de uso de los cmdlets y el script.

Para crear asociaciones entre usuarios después de haber instalado el servidor MBAM, use el cmdlet de PowerShell Write-MbamComputerUser. Al igual que el script de PowerShell de Add-ComputerUser.ps1, este cmdlet le permite especificar los usuarios que pueden usar el portal de autoservicio para obtener información de OwnerAuth de TPM o contraseñas de recuperación de volúmenes para el equipo especificado.

**Nota:**  El agente de MBAM invalidará las asociaciones entre usuarios cuando el equipo comienza a notificar al servidor.

 

**Requisitos previos:** Los cmdlets de lectura-AD \ * solo pueden recuperar información de AD si se ejecutan como una cuenta de usuario con privilegios elevados, como un administrador de dominio, o como una cuenta en un grupo de seguridad personalizado con acceso de lectura a la información (recomendado).

[Guía de operaciones de cifrado de unidad BitLocker: recuperar volúmenes cifrados con AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) proporciona detalles sobre cómo crear un grupo de seguridad personalizado (o varios grupos) con acceso de lectura a la información del anuncio.

**Permisos de escritura de los servicios Web de recuperación y hardware de MBAM:** Los cmdlets \ * de escritura Mbam aceptan la dirección URL del servicio de recuperación y hardware de MBAM, que se usa para publicar la información del TPM o la recuperación. Normalmente, solo una cuenta de servicio de equipo de dominio puede comunicarse con el servicio de hardware y recuperación de MBAM. En MBAM 2,5 SP1, puede configurar el servicio de hardware y recuperación de MBAM con un grupo de seguridad denominado DataMigrationAccessGroup cuyos miembros pueden omitir la comprobación de la cuenta de servicio de equipo del dominio. Los cmdlets \ * de escritura Mbam deben ejecutarse como un usuario que pertenece a este grupo configurado. (También, las credenciales de un usuario individual en el grupo configurado se pueden especificar con el parámetro – credential en los cmdlets \ * de escritura Mbam.)

Puede configurar el servicio de hardware y recuperación de MBAM con el nombre de este grupo de seguridad de una de las siguientes maneras:

-   Proporcione el nombre del grupo de seguridad (o individual) en el parámetro-DataMigrationAccessGroup del cmdlet enable-MbamWebApplication – AgentService de PowerShell.

-   Configure el grupo después de instalar el servicio de hardware y recuperación de MBAM editando el archivo web.config de la &lt; carpeta de administración de BitLocker de Inetpub &gt; \\Microsoft Solution\\Recovery y de hardware Service\\.

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    donde &lt; GroupName &gt; se reemplaza con el dominio y el nombre del grupo (o el usuario individual) que se usará para permitir la migración de datos desde Active Directory.

-   Use el editor de configuración del administrador de IIS para modificar esta appSetting.

En el siguiente ejemplo, el comando, cuando se ejecuta como miembro del grupo ADRecoveryInformation y del grupo usuarios de migración de datos, extrae la información de recuperación de volumen de los equipos de la unidad organizativa (Uo) estaciones de trabajo del dominio contoso.com y la escribe en MBAM con el servicio de hardware y recuperación MBAM que se ejecuta en el servidor mbam.contoso.com.

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

Los **cmdlets de lectura-ad \ *** aceptan el nombre o la dirección IP de un equipo de servidor de hospedaje de Active Directory para consultar información de recuperación o de TPM. Le recomendamos que proporcione los nombres distintivos de los contenedores de AD en los que el objeto de equipo reside como valor del parámetro SearchBase. Si los equipos se almacenan en varias unidades organizativas, los cmdlets pueden aceptar la entrada de canalización una vez para cada contenedor. El nombre distintivo de un contenedor de AD tendrá un aspecto similar a OU = máquinas, DC = Contoso, DC = com. Realizar una búsqueda dirigida a contenedores específicos ofrece las siguientes ventajas:

-   Reduce el riesgo de tiempo de espera al consultar un conjunto de objetos de AD grande para objetos de equipo.

-   Puede omitir las unidades organizativas que contienen servidores de centro de datos u otras clases de equipos para los que es posible que la copia de seguridad no se desee o sea necesaria.

Otra opción es proporcionar la marca de recursividad con o sin el SearchBase opcional para buscar objetos de equipo en todos los contenedores en la SearchBase especificada o en todo el dominio, respectivamente. Al usar la bandera-recurse, también puede usar el parámetro-MaxPageSize para controlar la cantidad de memoria local y remota necesaria para atender la consulta.

Estos cmdlets escriben en los objetos de canalización de tipo PsObject. Cada instancia de PsObject contiene una única clave de recuperación de volumen o una cadena de propietario de TPM con el nombre de equipo asociado, la marca de hora y otra información necesaria para publicarla en el almacén de datos MBAM.

**Cmdlets de Write-Mbam \ *** aceptan valores de parámetros de información de recuperación de la canalización por nombre de propiedad. Esto permite que los cmdlets \ * de escritura Mbam acepten la salida de la canalización de los cmdlets de lectura-AD \ * (por ejemplo, Read-ADRecoveryInformation-Server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).

El **cmdlet Write-Mbam \ *** incluye parámetros opcionales que proporcionan opciones para la tolerancia a errores, registro detallado y preferencias para Whatif y confirm.

Los **cmdlets \ * de escritura Mbam** también incluyen un parámetro de *hora* opcional cuyo valor es un objeto **DateTime** . Este objeto incluye un atributo *Kind* que puede establecerse en `Local` , `UTC` o `Unspecified` . Cuando se rellena el parámetro de *hora* a partir de los datos tomados de Active Directory, la hora se convierte en UTC y este atributo de *tipo* se establece automáticamente en `UTC` . Sin embargo, al rellenar el parámetro de *hora* con otro origen, como un archivo de texto, debe establecer explícitamente el atributo *Kind* en el valor adecuado.

**Nota:**  Los cmdlets de lectura AD \ * no tienen la capacidad de descubrir las cuentas de usuario que representan a los usuarios del equipo. Las asociaciones de cuenta de usuario son necesarias para lo siguiente:

-   A los usuarios recuperar las contraseñas y paquetes de volumen mediante el portal de autoservicio

-   Usuarios que no se encuentran en el MBAM grupo de seguridad avanzado de los usuarios del servicio de asistencia, como se definieron durante la instalación, recuperar en nombre de otros usuarios

 

## <a href="" id="bkmk-autounlock"></a>Configurar MBAM para que desbloquee TPM automáticamente después de un bloqueo


Puede configurar MBAM 2,5 SP1 para que desbloquee automáticamente el TPM en caso de que se bloquee. Si el restablecimiento automático de bloqueo de TPM está habilitado, MBAM puede detectar que un usuario está bloqueado y, a continuación, obtener la contraseña de OwnerAuth de la base de datos de MBAM para desbloquear automáticamente el TPM para el usuario. El bloqueo automático de bloqueo de TPM solo está disponible si la clave de recuperación del sistema operativo para ese equipo se recuperó usando el portal de autoservicio o el sitio web de administración y supervisión.

**Importante**  Para habilitar el restablecimiento automático del bloqueo de TPM, debe configurar esta característica en el lado del servidor y en la Directiva de grupo del cliente.

 

-   Para habilitar el restablecimiento automático del bloqueo de TPM en el cliente, establezca la configuración de directiva de grupo "configurar el bloqueo automático de bloqueo de TPM", que se encuentra en **configuración de equipo** &gt; **plantillas administrativas** de &gt; **Windows componentes** de &gt; **MDOP MBAM** &gt; **Client Management**.

-   Para habilitar el restablecimiento automático del bloqueo de TPM en el servidor, puede activar "habilitar el bloqueo automático de bloqueo de TPM" en el Asistente para la configuración del servidor de MBAM durante la instalación.

    También puede habilitar el restablecimiento automático del bloqueo de TPM en PowerShell especificando el modificador "-TPM bloqueo automático" al habilitar el componente web del servicio agente.

Después de que un usuario haya introducido la clave de recuperación de BitLocker que obtuvo del portal de autoservicio o del sitio web de administración y supervisión, el agente de MBAM determinará si el TPM está bloqueado. Si está bloqueado, intentará recuperar el OwnerAuth de TPM para el equipo de la base de datos de MBAM. Si el TPM OwnerAuth se recupera correctamente, se usará para desbloquear el TPM. Desbloquear el TPM hace que el TPM sea completamente funcional y el usuario no se verá obligado a escribir la contraseña de recuperación durante el resto de los reinicios desde un bloqueo de TPM.

El restablecimiento automático del bloqueo de TPM está deshabilitado de forma predeterminada.

**Nota:**  El bloqueo automático de bloqueo de TPM solo se admite en equipos que ejecutan la versión 1,2 de TPM. El TPM 2,0 proporciona funciones de bloqueo automático de bloqueo integrado.

 

**El informe de auditoría de recuperación** incluye eventos relacionados con el restablecimiento automático del bloqueo de TPM. Si una solicitud se realiza desde el cliente de MBAM para recuperar una contraseña de OwnerAuth de TPM, se registra un evento para indicar la recuperación. Las entradas de auditoría incluirán los siguientes eventos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">MOV</th>
<th align="left">Valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Origen de solicitud de auditoría</p></td>
<td align="left"><p>Desbloquear TPM del agente</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de clave</p></td>
<td align="left"><p>Hash de contraseña de TPM</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción del motivo</p></td>
<td align="left"><p>Reinicio de TPM</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a>Conexiones seguras a SQL Server


En MBAM, SQL Server se comunica con SQL Server Reporting Services y con los servicios web para el sitio web de administración y supervisión y el portal de autoservicio. Le recomendamos que proteja la comunicación con SQL Server. Para obtener más información, consulte [cifrar conexiones a SQL Server](https://technet.microsoft.com/library/ms189067.aspx).

Para obtener más información sobre cómo proteger los sitios web de MBAM, consulte [planificación de la seguridad de los sitios web de MBAM](planning-how-to-secure-the-mbam-websites.md).

## <a href="" id="bkmk-accts-groups"></a>Crear cuentas y grupos


El procedimiento recomendado para administrar cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario. Para obtener una descripción de las cuentas y grupos recomendados, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

## <a href="" id="bkmk-logfiles"></a>Usar archivos de registro de MBAM


En esta sección se describen los archivos de registro de MBAM Server y MBAM Client.

**Archivos de registro de instalación de MBAM Server**

El archivo de **MBAMServerSetup.exe** genera los siguientes archivos de registro en la carpeta **% temp%** del usuario durante la instalación de MBAM:

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log**

    Registra las acciones realizadas durante el programa de instalación de MBAM y la configuración de características del servidor de MBAM.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log**

    Registra las acciones adicionales tomadas durante la instalación.

**Archivos de registro de configuración de servidor de MBAM**

-   **Registros de aplicaciones y servicios/Microsoft Windows/MBAM-configuración**

    Registra los errores que se producen al usar cmdlets de Windows PowerShell o el Asistente para la configuración del servidor de MBAM para configurar las características del servidor de MBAM.

**Archivos de registro de configuración de cliente de MBAM**

-   **MSI &lt; cinco caracteres aleatorios &gt; . log**

    Registra las acciones tomadas durante la instalación del cliente de MBAM.

**MBAM: archivos de registro web**

-   Muestra la actividad de los servicios y los portales web.

## <a href="" id="bkmk-tde"></a>Revisar las consideraciones de la base de datos de MBAM TDE


La característica de cifrado de datos transparente (TDE) que está disponible en SQL Server es una instalación opcional para las instancias de base de datos que hospedarán las características de base de datos de MBAM.

Con TDE, puede realizar un cifrado de nivel de base de datos completo en tiempo real. TDE es la mejor opción para el cifrado en masa para cumplir con los estándares de seguridad de datos corporativos o de cumplimiento normativo. TDE funciona en el nivel de archivo, que es similar a dos características de Windows: el sistema de archivos de cifrado (EFS) y el cifrado de unidad BitLocker. Ambas características también cifran los datos del disco duro. TDE no reemplaza el cifrado de nivel de celda, EFS ni BitLocker.

Cuando TDE está habilitado en una base de datos, se cifran todas las copias de seguridad. Por lo tanto, se debe tener especial cuidado para asegurarse de que se realice una copia de seguridad del certificado que se usó para proteger la clave de cifrado de la base de datos con la copia de seguridad de la base de datos. Si este certificado (o certificados) se pierde, no se podrán leer los datos.

Haga una copia de seguridad del certificado en la base de datos. Cada copia de seguridad de certificado debe tener dos archivos. Ambos archivos deben archivarse. Lo ideal es que se haga una copia de seguridad de ellos por separado del archivo de copia de seguridad de la base de datos. También puede considerar la posibilidad de usar la característica Administración de claves extensible (EKM) (consulte Administración de claves extensible) para almacenar y mantener las claves que se usan para TDE.

Para obtener un ejemplo de cómo habilitar TDE para MBAM instancias de base de [datos, vea comprender el cifrado de datos transparente (TDE)](https://technet.microsoft.com/library/bb934049.aspx).

## <a href="" id="bkmk-general-security"></a>Comprender las consideraciones generales de seguridad


**Comprender los riesgos de seguridad.** El riesgo más grave cuando use la administración y la supervisión de Microsoft BitLocker es que un usuario no autorizado podría comprometerse con su funcionalidad, que podría volver a configurar el cifrado de unidad BitLocker y obtener los datos de la clave de cifrado BitLocker en clientes MBAM. Sin embargo, la pérdida de la funcionalidad de MBAM por un breve período de tiempo, debido a un ataque de denegación de servicio, generalmente no tiene un impacto catastrófico, a diferencia de, por ejemplo, la pérdida de mensajes de correo electrónico o comunicaciones de red o la energía.

**Proteja físicamente sus equipos**. No hay seguridad sin seguridad física. Un atacante que obtiene acceso físico a un servidor de MBAM puede utilizarlo para atacar a toda la base de clientes. Todos los posibles ataques físicos se deben considerar de alto riesgo y se pueden mitigar correctamente. Los servidores de MBAM deben almacenarse en una sala de servidores segura con acceso controlado. Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.

**Aplique las actualizaciones de seguridad más recientes a todos los equipos**. Manténgase informado acerca de las nuevas actualizaciones de sistemas operativos de Windows, SQL Server y MBAM al suscribirse al servicio de notificaciones de seguridad en el [TechCenter de seguridad](https://go.microsoft.com/fwlink/?LinkId=28819).

**Use contraseñas seguras o frases**. Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de MBAM. Nunca use contraseñas en blanco. Para obtener más información sobre los conceptos de contraseñas, consulte [Directiva de contraseñas](https://technet.microsoft.com/library/hh994572.aspx).



## Temas relacionados


[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





