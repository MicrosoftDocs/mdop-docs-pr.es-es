---
title: Acerca de MBAM 2.5 SP1
description: Acerca de MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823781"
---
# Acerca de MBAM 2.5 SP1


MBAM 2,5 SP1 proporciona una interfaz administrativa simplificada para el cifrado de unidad BitLocker. BitLocker ofrece una protección mejorada contra el robo de datos o la exposición de datos para equipos que se han perdido o robado. BitLocker cifra todos los datos que se almacenan en el sistema operativo Windows y las unidades de datos configuradas.

## Información general de MBAM


MBAM 2,5 SP1 tiene las siguientes características:

-   Permite a los administradores automatizar el proceso de cifrado de volúmenes en los equipos cliente en toda la empresa.

-   Permite que los responsables de seguridad determinen rápidamente el estado de cumplimiento de equipos individuales o incluso de la empresa.

-   Proporciona administración de informes y hardware centralizada con Microsoft System Center Configuration Manager.

-   Reduce la carga de trabajo del Departamento de soporte técnico para ayudar a los usuarios finales con PIN de BitLocker y solicitudes de clave de recuperación.

-   Permite a los usuarios finales recuperar dispositivos cifrados de forma independiente mediante el Portal de autoservicio.

-   Permite a los responsables de seguridad auditar fácilmente el acceso para recuperar información clave.

-   Permite a los usuarios de Windows Enterprise continuar trabajando en cualquier lugar con la garantía de que sus datos de la empresa están protegidos.

MBAM exige las opciones de directiva de cifrado de BitLocker que haya establecido para su empresa, supervisa la compatibilidad de equipos cliente con esas directivas e informa del estado de cifrado de los equipos de la empresa y de los individuos. Además, MBAM le permite acceder a la información de la clave de recuperación cuando los usuarios olvidan su PIN o su contraseña, o cuando sus registros de arranque o BIOS cambian.

Es posible que los siguientes grupos estén interesados en usar MBAM para administrar BitLocker:

-   Administradores, profesionales de la seguridad de ti y responsables del cumplimiento responsables de garantizar que los datos confidenciales no se revelen sin autorización

-   Administradores responsables de la seguridad del equipo en oficinas remotas o sucursales

-   Administradores responsables de equipos cliente que ejecutan Windows

**Nota:**  BitLocker no se explica detalladamente en esta documentación de MBAM. Para obtener más información, consulte [Introducción al cifrado de unidad BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a>Novedades de MBAM 2,5 SP1


En esta sección se describen las nuevas características de MBAM 2,5 SP1.

### Nuevos idiomas admitidos para el cliente de MBAM 2,5 SP1

Ahora solo se admiten los siguientes idiomas adicionales en MBAM 2,5 SP1 para el cliente de MBAM, incluido el portal de autoservicio:

Checo (República Checa) CS-CZ

Danés (Dinamarca) da-DK

Neerlandés (Países Bajos) nl-NL

Finés (Finlandia) fi-FI

Griego (Grecia) el-GR

Húngaro (Hungría) Hu-HU

Noruego, Bokmål (Noruega) NB-NO

Polaco (Polonia) PL: PL

Portugués (Portugal) pt-PT

República Eslovaca (Eslovaquia) SK-SK

Esloveno (Eslovenia) SL-SI

Sueco (Suecia) VP-SE

Turco (Turquía) tr-TR

Para obtener una lista de todos los idiomas admitidos para el cliente y el servidor en MBAM 2,5 y MBAM 2,5 SP1, consulte [MBAM 2,5 configuraciones compatibles](mbam-25-supported-configurations.md).

### Compatibilidad con Windows 10

MBAM 2,5 SP1 agrega compatibilidad con Windows 10 y Windows Server 2016, además del mismo software que se admite en versiones anteriores de MBAM.

Windows 10 es compatible tanto en MBAM 2,5 como en MBAM 2,5 SP1.

### Compatibilidad con Microsoft SQL Server 2014 SP1

MBAM 2,5 SP1 agrega compatibilidad con Microsoft SQL Server 2014 SP1, además del mismo software que se admite en versiones anteriores de MBAM.

### MBAM ya no se distribuye con un MSI diferente

A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM. Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto.

### MBAM puede proteger OwnerAuth contraseñas sin poseer el TPM

Anteriormente, si MBAM no tuviera el TPM, no se podía enviar la OwnerAuth de TPM a la base de datos de MBAM. Para configurar MBAM de forma que sea el propietario del TPM y para almacenar las contraseñas, debe deshabilitar el aprovisionamiento automático de TPM y borrar el TPM en el equipo cliente.

En Windows 8 y versiones posteriores, MBAM 2,5 SP1 ahora puede proteger las contraseñas OwnerAuth sin poseer el TPM. Durante el inicio del servicio, MBAM consultas para ver si el TPM ya es propietario y, si es así, solicita las contraseñas del sistema operativo. Después, las contraseñas se encuentran en la base de datos MBAM. Además, se debe establecer la Directiva de grupo para evitar que se elimine el OwnerAuth de forma local.

En Windows 7, MBAM debe poseer el TPM para custodiar automáticamente la información de OwnerAuth de TPM en la base de datos de MBAM. Si MBAM no posee el TPM y la copia de seguridad de Active Directory (AD) de TPM se configura mediante la Directiva de grupo, debe usar los **cmdlets de importación de datos de Active Directory (ad) de MBAM** para copiar el TPM OWNERAUTH de ad a la base de datos MBAM. Estos son cinco nuevos cmdlets de PowerShell que rellenan previamente las bases de datos de MBAM con la información de la recuperación por volumen y el propietario de TPM almacenada en Active Directory.

Para obtener más información, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

### MBAM puede desbloquear automáticamente el TPM después de un bloqueo

En los equipos que ejecutan el TPM 1,2, ahora puede configurar MBAM para que desbloquee automáticamente el TPM en caso de bloqueo. Si la característica de restablecimiento automático de bloqueo de TPM está habilitada, MBAM puede detectar que un usuario está bloqueado y, a continuación, obtener la contraseña de OwnerAuth de la base de datos de MBAM para desbloquear automáticamente el TPM para el usuario.

Esta característica debe habilitarse tanto en el lado del servidor como en la Directiva de grupo en el cliente. Para obtener más información, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).

### Compatibilidad con protectores de contraseña numérico de BitLocker conforme a FIPS

En MBAM 2.5, se agregó compatibilidad con las claves de recuperación de BitLocker conforme al estándar federal de procesamiento de información (FIPS) en dispositivos que ejecutan el sistema operativo Windows 8,1. Sin embargo, Windows no implementó las claves de recuperación compatibles con FIPS en Windows 7. Por lo tanto, los dispositivos con Windows 7 y Windows 8 siguen requiriendo un protector de agente de recuperación de datos (DRA) para la recuperación.

El equipo de Windows cuenta con claves de recuperación de la compatibilidad con FIPS y con un hotfix, y MBAM 2,5 SP1 también ha agregado compatibilidad.

**Nota:**  Los equipos cliente que ejecutan el sistema operativo Windows8 aún necesitan un protector DRA, ya que el Hotfix no se ha importado a ese sistema operativo. Vea el [paquete de revisiones 2 para la administración de BitLocker y la supervisión de 2,5](https://support.microsoft.com/kb/3015477) para descargar e instalar la corrección de BitLocker para equipos con Windows 7 y Windows 8. Para obtener más información sobre DRA, consulte [uso de agentes de recuperación de datos con BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

 

Para habilitar la compatibilidad de FIPS en su organización, debe configurar la configuración de directiva de grupo estándar federal de procesamiento de información (FIPS). Para obtener instrucciones de configuración, consulte Configuración de la [Directiva de grupo de BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

### Personalizar la dirección URL y el mensaje de recuperación previo al inicio con nueva configuración de directiva de grupo

Una nueva configuración de directiva de grupo, **configurar el mensaje y la dirección URL de recuperación previa al arranque**, le permite configurar un mensaje de recuperación personalizado o especificar una dirección URL que se muestra en la pantalla de recuperación de BitLocker anterior a la inicialización cuando la unidad del sistema operativo está bloqueada. Esta opción solo está disponible en los equipos cliente que ejecutan Windows 10.

Si habilita esta configuración de Directiva, puede seleccionar una de estas opciones para el mensaje de recuperación previo al inicio:

-   **Usar mensaje de recuperación personalizado**: Seleccione esta opción para incluir un mensaje personalizado en la pantalla de recuperación de BitLocker anterior a la inicialización.

-   **Usar una dirección URL de recuperación personalizada**: Seleccione esta opción para reemplazar la dirección URL predeterminada que se muestra en la pantalla de recuperación de BitLocker anterior a la inicialización.

-   **Usar el mensaje de recuperación y la dirección URL predeterminados**: Seleccione esta opción para mostrar el mensaje de recuperación de BitLocker predeterminado y la dirección URL en la pantalla de recuperación de BitLocker anterior a la inicialización. Si ha configurado previamente un mensaje de recuperación personalizado o una dirección URL y desea volver al mensaje predeterminado, debe habilitar esta directiva y seleccionar esta opción.

La nueva configuración de directiva de grupo se encuentra en el siguiente nodo GPO: directivas de **configuración del equipo** &gt; **Policies** &gt; **plantillas administrativas** de &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)** &gt; **unidad del sistema operativo**. Para obtener más información, consulte requisitos de la [Directiva de grupo de planificación de MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### MBAM agregó compatibilidad para el cifrado de espacio usado

En MBAM 2,5 SP1, si habilita el cifrado de espacio usado mediante la Directiva de grupo de BitLocker, el cliente de MBAM lo respetará.

Esta configuración de directiva de grupo se denomina **exigir tipo de cifrado de unidad en unidades de sistema operativo** y se encuentra en el siguiente nodo GPO: **configuración del equipo** &gt; **plantillas administrativas** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **unidades del sistema operativo**de cifrado de unidad BitLocker. Si habilita esta directiva y selecciona el tipo de cifrado como **cifrado solo de espacio usado**, MBAM cumplirá la Directiva y BitLocker solo cifrará el espacio en disco que se usa en el volumen.

Para obtener más información, consulte requisitos de la [Directiva de grupo de planificación de MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### Compatibilidad con el cliente de MBAM para unidades de disco duro cifradas

MBAM es compatible con BitLocker en unidades de disco duro cifradas que cumplen los requisitos de especificación de TCG para Opal y las normas IEEE 1667. Cuando BitLocker está habilitado en estos dispositivos, generará claves y realizará funciones de administración en la unidad cifrada. Para obtener más información, consulta [unidad de disco duro cifrada](https://technet.microsoft.com/library/hh831627.aspx) .

### La configuración de Delegación ya no es necesaria al registrar SPN

El requisito de configurar la delegación restringida para los SPN que se registran para la cuenta del grupo de aplicaciones ya no es necesario en MBAM 2,5 SP1. Sin embargo, sigue siendo un requisito para MBAM 2,5.

### Habilitar BitLocker con MBAM como parte de una implementación de Windows

En MBAM 2,5 SP1, puede usar un script de PowerShell para configurar el cifrado de unidad BitLocker y las claves de recuperación del depósito de garantía en el servidor de MBAM.

Para obtener más información, consulte [Cómo habilitar BitLocker con MBAM como parte de una implementación de Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

### El portal de autoservicio se puede personalizar mediante PowerShell o el Asistente de personalización del SSP.

A partir de MBAM 2,5 SP1, el portal de autoservicio puede configurarse con el Asistente de personalización, así como con PowerShell. Vea [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

### El explorador web ya no se ejecuta de forma involuntaria como administrador

Un problema en MBAM 2,5 causó vínculos de ayuda en la herramienta de configuración del servidor para hacer que las ventanas del explorador se abran con derechos de administrador. Este problema se corrigió en MBAM 2,5 SP1.

### Ya no es necesario descargar los archivos de JavaScript para configurar el portal de autoservicio cuando no se puede acceder a la red CDN

En MBAM 2,5 y versiones anteriores, los archivos de jQuery que se usan para la configuración del portal de autoservicio tuvieron que descargarse de la red CDN por adelantado si los clientes que obtienen acceso al portal de autoservicio no tenían acceso a Internet. En MBAM 2,5 SP1, todos los archivos de JavaScript se incluyen en el producto, por lo que no es necesario descargarlos.

### Los informes se pueden abrir en el generador de informes 3,0

En MBAM 2,5 SP1, los informes se han actualizado al esquema del lenguaje de definición de informes más reciente, lo que permite a los usuarios abrir y personalizar los informes en el generador de informes 3,0 y guardarlos inmediatamente sin dañar el archivo de informe.

### Nuevos cmdlets de PowerShell

Los nuevos cmdlets de PowerShell para MBAM 2,5 SP1 le permiten configurar y administrar diferentes características de MBAM, entre las que se incluyen bases de datos, informes y aplicaciones Web. Cada característica tiene un cmdlet de PowerShell correspondiente que puede usar para habilitar o deshabilitar características, o para obtener información sobre la característica.

Se han implementado los siguientes cmdlets para MBAM 2,5 SP1:

-   Escritura MbamTpmInformation

-   Escritura MbamRecoveryInformation

-   Lectura-ADTpmInformation

-   Lectura-ADRecoveryInformation

-   Escritura MbamComputerUser

Los siguientes parámetros se han implementado en los cmdlets enable-MbamWebApplication y test-MbamWebApplication para MBAM SP1 de 2,5:

-   DataMigrationAccessGroup

-   TpmAutoUnlock

Para obtener más información sobre los cmdlets, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md) y ayuda para el [cmdlet de supervisión y administración de Microsoft BitLocker](https://technet.microsoft.com/library/dn720418.aspx).

### El agente de MBAM detecta el modo de presentación

El agente de MBAM puede detectar cuando el equipo está en modo de presentación y evitar invocar la interfaz de usuario de MBAM en ese momento.

### Servicio agente de MBAM ahora configurado para usar Inicio retrasado

Después de la instalación, el servicio configurará el servicio agente de MBAM para que use el Inicio retrasado, lo que disminuirá la cantidad de tiempo que se tarda en iniciar Windows.

### Los volúmenes de datos fijos bloqueados ahora notifican como compatibles

La lógica de cálculo de cumplimiento para los volúmenes de "datos fijos bloqueados" ha sido modificada para notificar los volúmenes como "conforme", pero con un estado de protector y el estado de cifrado "desconocido" y con un detalle de estado de cumplimiento de "el volumen está bloqueado". Anteriormente, los volúmenes bloqueados se mostraban como "no compatibles", un estado de protector "cifrado", un estado de cifrado "desconocido" y un detalle de estado de cumplimiento de "error desconocido".


## Cómo obtener tecnologías de MDOP


MBAM es parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte del programa software Assurance de Microsoft. Para obtener más información sobre el programa Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## Notas de la versión de MBAM 2,5 SP1


Para obtener más información y noticias de última hora que no se incluyen en esta documentación, consulte [notas de la versión de MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Temas relacionados


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Introducción a MBAM 2.5](getting-started-with-mbam-25.md)

 

 





