---
title: Notas de la versión de MBAM 2.5 SP1
description: Notas de la versión de MBAM 2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824990"
---
# Notas de la versión de MBAM 2.5 SP1


Para buscar estas notas de la versión, presione Ctrl + F.

Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. Estas notas de la versión contienen información necesaria para instalar MBAM correctamente y pueden contener información que no está disponible en la documentación del producto. Si estas notas de la versión difieren de otra documentación de MBAM 2,5 SP1, considere el cambio más reciente para que sea autoritativo. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> Problemas conocidos de MBAM 2,5 SP1


Esta sección contiene notas de la versión para MBAM 2,5 SP1.

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a>Los cmdlets de lectura de AD \ * de PowerShell no proporcionan comentarios si el usuario no tiene derechos suficientes

Si un usuario que intenta usar los cmdlets de lectura-AD \ * de PowerShell para el servidor de MBAM no tiene derechos de usuario para leer la información de recuperación de Active Directory o para leer la información de TPM, los cmdlets no proporcionarán al usuario ningún error o advertencia.

**Solución alternativa:** Use solo los cmdlets de lectura de AD \ * de PowerShell si tiene los derechos de usuario requeridos.

### MBAM cmdlets de migración de Active Directory (AD) no recuperan información de recuperación de volúmenes

MBAM cmdlets de migración de Active Directory (AD) no pueden recuperar información de recuperación de volúmenes de equipos en unidades organizativas (OU) si el carácter de barra diagonal (/) forma parte del nombre de la uo. Las extracciones de anuncios repetidas fallarán con un error de terminación de canalización cuando se detecte este error.

**Detalles técnicos:** Verá este error al ejecutar el comando:

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

Además, el seguimiento de pila de excepción tendrá el siguiente `Error[0].Exception.StackTrace` aspecto:

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

**Solución alternativa:** Realice una de estas tareas para resolver esta situación:

-   Cambie el nombre de la OU para quitar el carácter de barra diagonal y, a continuación, ejecute el script.

-   Para excluir cualquier unidad organizativa problemática del proceso de copia de seguridad, busque una lista de unidades organizativas cuyos nombres no contengan el carácter de barra diagonal. Ejecute la secuencia de comandos en estas unidades organizativas, una por una.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM no cifra un volumen e informa de un error Si estableces un protector de TPM + PIN en un dispositivo de tableta

Si los usuarios finales intentan establecer un protector de anclaje + PIN en un dispositivo de tableta, MBAM no se cifrará y notificará un error. Este problema se produce porque los dispositivos de tableta no tienen un teclado de entorno de preinicialización.

**Solución alternativa:** Habilite la configuración **Habilitar el uso de la autenticación de BitLocker que requiera la entrada del teclado de prearranque en tabletas** . Esta opción es una configuración de directiva de grupo de BitLocker y no está disponible en las plantillas de directiva de grupo MBAM.

### El nombre principal de usuario es necesario para todas las cuentas de servicio

Debe establecerse un nombre principal de usuario (UPN) para todas las cuentas de servicio en MBAM. Si no puede crear un UPN para una cuenta, aparecerá un mensaje de error durante el proceso de configuración para indicar que el usuario o grupo no se pudo encontrar en Active Directory.

**Solución alternativa:** Agregue el UPN a la cuenta de servicio.

### El portal de autoservicio y el sitio web de administración y supervisión no se abren después de actualizar IIS a .NET Framework 4,5

Al actualizar Internet Information Services (IIS) a Microsoft .NET Framework 4,5, el portal de autoservicio y el sitio web de administración y supervisión no se abren.

**Solución alternativa:** Vea el artículo [mensaje de error después de instalar .NET Framework 4,0: "no se pudo cargar el tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).

### Sitio web de supervisión y administración muestra el mensaje de error "no se puede encontrar el informe" cuando no se han configurado los informes

Si configura el sitio web de administración y supervisión y, a continuación, intenta ver un informe sin configurar la característica informes en primer lugar, un mensaje de error indica que no se puede encontrar el informe.

**Solución alternativa:** Configure la característica informes antes de configurar las aplicaciones Web.

### Los informes del sitio web de administración y supervisión muestran una advertencia si SSL no está configurado en SSRS

Si SQL Server Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de la característica de informes se establecerá en HTTP en lugar de en HTTPS al configurar el servidor MBAM. Si abre el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje de error: "solo se muestra el contenido seguro".

**Solución alternativa:** Para mostrar el informe, haga clic en **Mostrar todo el contenido**. Para corregir este problema, vaya al equipo MBAM donde está instalado SQL Server Reporting Services, ejecute el **Administrador de configuración de Reporting Services**y, a continuación, haga clic en **URL de servicio Web**. Seleccione el certificado SSL adecuado para el servidor, escriba el puerto SSL adecuado (el puerto predeterminado es 443) y, a continuación, haga clic en **aplicar**.

### Al hacer clic en "atrás" en el informe Resumen de compatibilidad de BitLocker, se puede producir un error

Si explora en profundidad un informe de Resumen de cumplimiento de BitLocker y luego hace clic en el vínculo **atrás** en el informe de SSRS, se puede producir un error.

**Solución alternativa:** Nada.

### La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos con BitLocker

Si no establece una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado, el informe de cumplimiento de BitLocker Computer en la topología de integración del administrador de configuración siempre muestra "desconocido" para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits. El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.

**Solución alternativa:** Establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.

### La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración

Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.

**Solución alternativa:** Nada. No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.

### La configuración de seguridad mejorada puede provocar que los informes muestren un mensaje de error incorrectamente

Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca un mensaje de error "acceso denegado" cuando intente ver informes en el servidor de MBAM. De forma predeterminada, ESC se activa para proteger el servidor disminuyendo la exposición del servidor ante posibles ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.

**Solución alternativa:** Si aparece el mensaje de error "acceso denegado" al intentar ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada. También puede ver los informes desde otro equipo en el que la ESC no está habilitada.

### Compatibilidad con el algoritmo de cifrado XTS-AES de BitLocker
BitLocker agregó compatibilidad para el algoritmo de cifrado XTS-AES en Windows 10, versión 1511. Con HF02, MBAM agregó compatibilidad de cliente para esta opción de BitLocker y en HF04, agregó la compatibilidad del lado del servidor. Sin embargo, hay una limitación conocida:

* Los clientes deben usar la misma intensidad de cifrado para el sistema operativo y los volúmenes de datos en el mismo equipo.
Si se usan diferentes niveles de cifrado, MBAM notificará el equipo como **no conforme**.

### El portal de autoservicio agrega automáticamente "-" en la entrada del identificador de clave
A partir de la HF02, el portal de autoservicio de MBAM agrega automáticamente la "-" en la entrada del identificador de clave.  
**Nota:** El servidor debe reconfigurarse para que el JavaScript surta efecto.

### Los informes de MBAM 2,5 SP1 no funcionan o se representan correctamente
La página de informes no se representa correctamente cuando SSRS se hospeda en SQL Server 2016 Edition. 
Por ejemplo, para navegar al servicio de asistencia al usuario (haciendo clic en informes) (la parte resaltada tiene "x"), lo que hace que sea más de Fiddler; parece que una vez que hacemos clic en los informes, se llama a la página de SSRS con el formato de representación HTML 4,0.

**Solución alternativa:** Mirar el código de site. Master e observado que el modo X-UA se dictó como IE8. Como IE8 se retrasó al final de la vida útil y el cliente usa IE11. Actualice la configuración al código que se muestra a continuación. Esto permite al sitio usar tecnologías de representación de IE11

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

La configuración original es: 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


Este es el motivo por el que el problema no se ha visto con otros exploradores como Chrome, Firefox, etc.



## Temas relacionados


[Acerca de MBAM 2.5](about-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





