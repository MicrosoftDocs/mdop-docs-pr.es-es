---
title: Notas de la versión de Microsoft Application Virtualization Management System
description: Notas de la versión de Microsoft Application Virtualization Management System
author: dansimp
ms.assetid: e1a4d5ee-53c7-4b48-814c-a34ce0e698dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c34abab9a49bd69f760a9b531d0950cc581253c1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816161"
---
# Notas de la versión de Microsoft Application Virtualization Management System


Para buscar estas notas de la versión, presione CTRL + F.

**Importante**  Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de virtualización de aplicaciones. Estas notas de la versión contienen información que necesita para instalar correctamente el sistema de administración de virtualización de aplicaciones. Este documento contiene información que no está disponible en la documentación del producto. Si hay una discrepancia entre estas notas de la versión y otra documentación del sistema de administración de virtualización de aplicaciones, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan al contenido incluido en este producto.

 

Para obtener información actualizada sobre problemas conocidos, visite la biblioteca de Microsoft TechNet en <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Acerca de la actualización acumulativa 1 de Microsoft Application Virtualization 4,5


Estas notas de la versión se han actualizado para reflejar los cambios introducidos con los update1 acumulativos de Microsoft Application Virtualization 4.5 (App-V 4.5 CU1), que proporciona las actualizaciones más recientes de Application Virtualization (App-V) 4.5. Esta actualización acumulativa contiene los siguientes cambios:

-   Compatibilidad con la versión beta de Windows7 y Windows Server2008R2 beta: App-V 4.5 CU1 soluciona problemas de compatibilidad con Windows7 beta y Windows Server2008R2 beta. Se proporcionará soporte técnico para bloquear los problemas que impiden que se ejecuten las aplicaciones-V 4.5 CU1 en un entorno de prueba en versiones anteriores al RTM de windows7. Esto le ayudará a asegurarse de que sus aplicaciones virtuales se pueden ejecutar correctamente en un entorno de prueba donde se necesite compatibilidad entre App-V 4.5 Client y Windows7 beta.

    **Importante**  No se admite la ejecución de App-V 4.5 CU1 en cualquier versión de Windows7 o Windows Server2008R2 en un entorno operativo en vivo.

     

-   Se ha mejorado la compatibilidad para la secuenciación de .NET Framework: App-V 4.5 CU1 soluciona problemas anteriores relacionados con la secuenciación de .NET Framework 3.5 y versiones anteriores en WindowsXP (SP2 o posterior). Para obtener más información sobre las nuevas capacidades, consulte el artículo de TechNet en <https://go.microsoft.com/fwlink/?LinkId=123412> .

-   Comentarios de los clientes y Resumen de revisiones: App-V 4.5 CU1 también incluye un resumen de las correcciones para resolver los problemas encontrados desde el lanzamiento de App-V 4.5 RTM. Esto incluye una combinación de problemas conocidos y comentarios de los clientes de nuestros equipos internos, socios y clientes que usan App-V 4.5. Para obtener una lista completa de las actualizaciones incluidas, consulte el artículo de KB en <https://go.microsoft.com/fwlink/?LinkId=141258> .

## Acerca de la documentación del producto


Encontrará documentación completa de Application Virtualization (App-V) en Microsoft TechNet en el TechCenter de Application Virtualization (App-V) en <https://go.microsoft.com/fwlink/?LinkId=122939> . La documentación de TechNet incluye la ayuda en línea de Application Virtualization Sequencer, el cliente de virtualización de aplicaciones y el servidor de virtualización de aplicaciones. También incluye la guía de planeación e implementación de virtualización de aplicaciones y la guía de operaciones de virtualización de aplicaciones.

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudar a protegerse contra virus y vulnerabilidades de seguridad, es importante instalar las últimas actualizaciones de seguridad disponibles para cualquier nuevo software que se instale. Para obtener más información, visite el sitio web de seguridad de Microsoft en <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Proporcionar comentarios


Puede proporcionar comentarios, realizar una sugerencia o informar de un problema con el sistema de administración de Microsoft Application Virtualization (App-V) a través de un foro de la comunidad en Microsoft Application Virtualization TechCenter ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

También puede enviar sus comentarios sobre la documentación directamente al equipo de documentación de App-V. Envíe sus comentarios sobre la documentación a appvdocs@microsoft.com.

## Problemas conocidos con Application Virtualization 4.5 CU1


Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.5 CU1. Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Siempre que sea posible, estos problemas se resolverán en versiones posteriores.

### Instrucciones para instalar o actualizar clientes a App-V 4.5 CU1 con setup.msi

Al instalar o actualizar los clientes de App-V a App-V 4.5 CU1 con setup.msi, los requisitos previos no se instalan automáticamente.

WORKAROUNDYou debe instalar manualmente los requisitos previos antes de instalar o actualizar el cliente de App-V a la versión 4.5 CU1. Para obtener los procedimientos detallados para instalar los requisitos previos y el cliente de App-V, consulte <https://go.microsoft.com/fwlink/?LinkId=144106> .

Cuando haya finalizado, instale el cliente de App-V 4.5 CU1 con setup.msi con privilegios elevados. Este archivo está disponible en el medio de la versión App-V 4.5 CU1 en la carpeta Installers\\Client.

Al instalar informes de errores de aplicaciones de Microsoft, use el siguiente comando si está instalando o actualizando el cliente de escritorio de App-V 4.5 CU1:

    msiexec /i dw20shared.msi APPGUID={FE495DBC-6D42-4698-B61F-86E655E0796D}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Como alternativa, si va a instalar o actualizar al cliente de servicios de Terminal Server App-V 4,5 CU1, use el siguiente comando:

    msiexec /i dw20shared.msi APPGUID={8A97C241-D92A-47DC-B360-E716C1AAA929} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Nota:**  El parámetro APPGUID hace referencia al código de producto del cliente de App-V que instalas o a los que actualizas. El código de producto es único para cada setup.msi. Puede usar el editor de bases de datos Orca o una herramienta similar para examinar los archivos de Windows Installer y determinar el código de producto. Este paso es necesario para todas las instalaciones o actualizaciones de App-V 4.5 CU1.

 

### <a href="" id="some-applications-might-fail-to-install-during-the-monitoring-phase-when-sequencing-on-windows-7-beta--"></a>Es posible que algunas aplicaciones no se instalen durante la fase de supervisión al realizar la secuencia en la versión beta de Windows7

Al secuenciar en la versión beta de Windows7 o en un equipo con Windows Installer 5.0, es posible que algunas aplicaciones no se instalen durante la fase de supervisión.

WORKAROUNDYou debe conceder de forma manual los permisos de control total para el grupo todos a la siguiente clave del registro:

    HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\SystemGuard

**Importante**  Debe usar el botón **avanzadas** para establecer la opción "incluir los permisos heredables de este objeto primario".

 

### No se pueden guardar paquetes al secuenciar en la versión beta de Windows7

Al realizar la secuenciación en la versión beta de Windows7, es posible que no pueda guardar el paquete secuenciado debido a una infracción de uso compartido.

Soluciones alternativas especificadas en la sección de procedimientos recomendados de la guía de secuencias de Microsoft Application Virtualization 4.5 (consulte <https://go.microsoft.com/fwlink/?LinkId=144108> ), debe apagar y deshabilitar los siguientes programas de software antes de comenzar la secuenciación:

-   Windows Defender

-   Software antivirus

-   Software de desfragmentación de disco

-   Windows Search

-   Cualquier sesión del explorador de Windows abierta

Además, si tiene Microsoft Update ejecutándose en la estación de secuenciación para capturar las actualizaciones durante el proceso de actualización del paquete, tendrá que agregar "C:\\Windows\\SoftwareDistribution" como una exclusión de VFS antes de iniciar la secuencia.

### Mejorar el rendimiento al secuenciar .NET Framework

Al secuenciar .NET Framework, es posible que se reduzca el rendimiento del sistema porque el servicio NGEN de Microsoft .NET Framework intenta precompilar los ensamblados como una tarea en segundo plano.

WORKAROUNDWhen en secuencia de .NET Framework, deshabilite el servicio NGEN de Microsoft .NET Framework (mscorsvw.exe) después de completar la fase de supervisión. Debe usar la pestaña de **servicios virtuales** en el secuenciador y cambiar el tipo de inicio a deshabilitado.

### Problemas de interoperabilidad con la barra de tareas de Windows7

Al ejecutar el cliente de virtualización de aplicaciones en Windows7, la barra de tareas de Windows7 no contrae varias instancias de una aplicación virtual en un único botón de la barra de tareas. Además, las listas Jump List no aparecen al hacer clic con el botón secundario en un botón de la barra de tareas de una aplicación virtual, a menos que la aplicación se haya anclado a la barra de tareas de windows7.

### Al desinstalar el cliente de Microsoft Application Virtualization, se eliminará la configuración de usuario asociada al usuario que realiza la desinstalación.

Al desinstalar el cliente de Microsoft Application Virtualization, Windows Installer quitará la configuración de virtualización de la aplicación del perfil del usuario actual. Si su equipo usa perfiles móviles, no use su cuenta de red personal para desinstalar el cliente porque quitará la configuración de las aplicaciones virtuales en todos los equipos.

WORKAROUNDYou debe realizar la desinstalación del cliente de App-V con una cuenta administrativa que no se use para ejecutar aplicaciones virtuales.

### Las modificaciones realizadas en las fichas sistema de archivos virtual y registro virtual se deben guardar mientras se ejecuta el Asistente para secuenciación

Si abre un paquete para realizar una actualización o ya ejecuta el Asistente para secuenciación con un nuevo paquete y realiza cambios en el paquete en las fichas sistema de archivos virtual o registro virtual, esos cambios no se guardan automáticamente.

WORKAROUNDSave los cambios antes de volver a ejecutar el Asistente para asegurarse de que se reflejan en el entorno virtual del asistente.

### El secuenciador de línea de comandos debe ejecutarse desde un símbolo del sistema con privilegios elevados

Al usar el secuenciador de línea de comandos, no se solicita la elevación.

WORKAROUNDRun el secuenciador de línea de comandos con un símbolo del sistema con privilegios elevados.

### Configuración de la consola de administración de servidores en entornos distribuidos

Si necesita instalar componentes de administración en sistemas distintos del servidor de publicación de virtualización de aplicaciones principal y el servidor de streaming, la instalación de servidor admite la instalación de nuestra consola de administración y el servicio Web en servidores independientes del servidor de virtualización de aplicaciones principal cuando se configure correctamente.

Para distribuir los componentes de administración en varios servidores, la delegación Kerberos debe estar habilitada en el servidor en el que está instalado el servicio Web.

### Los nombres de variable de ruta corta en archivos OSD pueden provocar errores

Si recibe el error 450478-1F702339-0000010B "el nombre del directorio no es válido" al iniciar una aplicación virtual en el cliente, es posible que la variable de la OSD no esté configurada correctamente. Esto puede suceder si el instalador de la aplicación establece un nombre de ruta corto durante la secuenciación.

WORKAROUNDRemove la tilde final de cualquier variable CSIDL que exista en el archivo OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Sintaxis correcta para el parámetro DECODEPATH para el secuenciador de la línea de comandos

En el secuenciador de línea de comandos, al abrir un paquete para actualizarlo y descodificarlo en la raíz de la unidad Q, la sintaxis del parámetro *DECODEPATH* no debe incluir una barra diagonal.

WORKAROUNDYou puede usar **Q:** en lugar de **Q:\\** (omitiendo el carácter "\ \" final).

### <a href="" id="when-upgrading-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Al actualizar paquetes 4.2, se producen problemas causados por los archivos de Windows Installer en el sistema de archivos virtual

Al actualizar un paquete de 4.2, es posible que se produzcan problemas relacionados con la falta de coincidencia de los archivos de sistema de Windows Installer que se incluyeron de forma predeterminada en la 4.2 y las bibliotecas de Windows Installer instaladas localmente en la estación de trabajo de secuenciación. Los siguientes archivos se encuentran en CSIDL \ _SYSTEM \ \:

cabinet.dll

msi.dll

msiexec.exe

msihnd.dll

msimsg.dlll

WORKAROUNDDelete todos los archivos anteriores del paquete. Elimine las asignaciones de la pestaña **VFS** , así como los archivos reales de la carpeta CSIDL \ _SYSTEM de la ruta de descodificación.

### <a href="" id="on-windows-xp--client-install-logging-is-not-enabled-by-default-"></a>En WindowsXP, el registro de instalación del cliente no está habilitado de forma predeterminada

Al instalar el cliente, para asegurarse de que se hayan capturado errores de instalación con fines de solución de problemas, debe habilitar el registro mediante la línea de comandos.

WORKAROUNDAdd el parámetro */l\ * VX! log.txt* a la línea de comandos, como se muestra en el siguiente ejemplo:

setup.exe/s/v "/QN/l\ * VX! log.txt "

msiexec.exe/i setup.msi/QN/l\ * VX! log.txt

Como alternativa, puede establecer la clave del registro en el valor siguiente:

\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"

### Para que la autenticación Kerberos funcione, los nombres principales de servicio (SPN) deben registrarse para IIS

Al usar IIS 6.0 o 7.0 para la recuperación de archivos de iconos o OSD, y la transmisión por secuencias de paquetes, para habilitar la autenticación Kerberos, los SPN deben registrarse de la siguiente manera:

-   En el servidor IIS, ejecute los siguientes comandos con la herramienta kit de recursos de SETSPN.EXE. Debe usarse el nombre de dominio completo (FQDN) del servidor.

    Setspn-r SOFTGRID/ &lt; Server FQDN&gt;

    Setspn-r FQDN de &lt; servidor o http&gt;

Para obtener más información, consulte <https://go.microsoft.com/fwlink/?LinkId=131407> .

### Al actualizar desde RC, los permisos predeterminados de los registros del cliente no permiten que los usuarios que no sean administradores tengan acceso a los registros de solución de problemas y soporte técnico

Los permisos predeterminados de los registros de cliente para la aplicación VirtualizationRC el cliente no permitió el acceso de los archivos de registro que no son administradores y los cambios manuales en estos permisos de registro se revirtieron cuando se reiniciaron los clientes. Esto se ha corregido en el lanzamiento de RTM para instalaciones de cliente nuevas, pero al actualizar desde RC, los permisos personalizados en los archivos de registro existentes no se restablecen. Sin embargo, cuando se creen nuevos registros o después de que se restablezca el registro, los archivos tendrán los nuevos permisos predeterminados.

WORKAROUNDAfter la actualización, restablezca los registros de cliente existentes o cambie manualmente sus permisos.

### Cambios en la compatibilidad de .NET

La update1 acumulativa de Microsoft Application Virtualization admite la secuenciación de .NET Framework en WindowsXP (SP2 o posterior). Es posible que tenga que actualizar las rutinas de secuencia para las aplicaciones .NET escritas para SoftGrid 4.2 al usarlas con el secuenciador de App-V 4.5. Para obtener detalles y soluciones alternativas, consulte el artículo de Knowledge base en <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Después de la actualización del cliente de App-V 4.2, algunas aplicaciones no se muestran.

Consulte el siguiente error en el registro: "el cliente de Application Virtualization no pudo analizar el archivo OSD". El cliente de Microsoft Application Virtualization 4.5 filtra las aplicaciones que tienen un archivo OSD que contiene una etiqueta de sistema operativo vacía ( &lt; sistema operativo &gt; &lt; /os &gt; ).

WORKAROUNDDelete la etiqueta de OS vacía del archivo OSD.

### El servidor de App-V requiere exenciones en su firewall para ciertos procesos

Para que el servidor pueda transmitir aplicaciones correctamente, los procesos básicos del servidor, incluido el distribuidor, necesitan tener acceso a través del firewall.

WORKAROUNDSet exenciones en el firewall del servidor para los siguientes procesos: sghwsvr.exe y sghwdsptr.exe. Esto se aplica al servidor de administración de App-V y al servidor de streaming de App-V.

### Es posible que se produzcan errores al secuenciar paquetes que requieren nuevos Runtime de Visual Basic

Si secuencia un paquete que usa una versión más reciente de un Runtime de Visual Basic (VB) en un sistema en el que está instalada una versión anterior de VBruntime, es posible que vea un bloqueo u otro comportamiento inesperado al intentar usar el paquete. Por ejemplo, si intenta secuenciar Microsoft Money2007, que usa la versión 6.00.9782 de la VBruntime, en un sistema WindowsXP con la versión 6.00.9690 de la VBruntime, es posible que vea un bloqueo en el diseñador de facturas al intentar ejecutarlo en otro sistema WindowsXP con ese VBruntime más antiguo.

WORKAROUNDAfter la instalación de la aplicación en el equipo de secuenciación, mientras supervisa, copie las VBruntime correctas (más recientes) en el directorio del paquete desde donde se inicia el ejecutable. Esto permite que la aplicación de secuencia encuentre la versión esperada de VBruntime cuando se inicia.

**Importante**  Este problema se ha corregido en los update1 acumulativos de Microsoft Application Virtualization 4.5.

 

### Cuando el instalador del servidor se ejecuta en modo silencioso, no comprueba correctamente si MSXML6

El servidor de administración de App-V depende de MSXML6. Sin embargo, si ejecuta el instalador en modo silencioso, por ejemplo, con el comando "msiexec-i setup.msi/QN" en un sistema donde MSXML6 ya no está instalado, el instalador no notará la dependencia que falta y se instalará de todos modos. El resultado más común es que cuando los clientes intentan actualizar la información de publicación del servidor de administración de App-V, verán errores.

WORKAROUNDVerify que MSXML6 se instala en el sistema antes de intentar una instalación silenciosa del servidor de administración de App-V.

### Código de error 000C800 al intentar conectarse a la consola de administración de virtualización de aplicaciones

Un administrador de virtualización de aplicaciones que no sea un administrador local en el servidor del servicio de administración de virtualización de aplicaciones recibirá un error (código de error: 000C800) cuando intente conectarse a la consola de administración de virtualización de aplicaciones y la entrada sftmmc. log indicará que se denegó el acceso a SftMgmt. udl. Para conectarse correctamente a la consola de administración de virtualización de aplicaciones, un administrador de virtualización de aplicaciones que no sea un administrador local en el servidor del servicio de administración de virtualización de aplicaciones debe tener al menos acceso de lectura y ejecución en el archivo SftMgmt. udl.

Los administradores de Application Virtualization deben recibir permisos de lectura y ejecución en el archivo SftMgmt. UDL en%systemdrive%\\Program de Programa\\microsoft System Center App virt Management Server\\App virt Management Service.

### Los parámetros de la línea de comandos del instalador del cliente se omiten cuando se usan conjuntamente con KEEPCURRENTSETTINGS = 1

Cuando se usa junto con KEEPCURRENTSETTINGS = 1, se omiten los siguientes parámetros de línea de comandos del instalador de cliente: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA y REQUIRESECURECONNECTION.

WORKAROUNDIf tiene una configuración que desea conservar, use KEEPCURRENTSETTINGS = 1 y, a continuación, establezca los otros parámetros después de la implementación. La plantilla ADM de App-V se puede usar para establecer la siguiente configuración de cliente: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES y ALLOWINDEPENDENTFILESTREAMING. La plantilla ADM puede encontrarse en <https://go.microsoft.com/fwlink/?LinkId=121835> .

### Error al inicializar aplicaciones virtuales con Symantec Endpoint Protection

Al usar Symantec Endpoint Protection con la característica de control de aplicaciones y dispositivos habilitada, es posible que no se inicien las aplicaciones virtuales, con el error "no se pudo inicializar correctamente la aplicación (0xc000007b)". Para obtener detalles y soluciones alternativas, consulte el artículo de Knowledge base en <https://go.microsoft.com/fwlink/?LinkId=125851> .

**Importante**  Este problema se ha corregido en los update1 acumulativos de Microsoft Application Virtualization 4.5.

 

## Información de copyright de notas de versión


La información de este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, está sujeta a cambios sin previo aviso y se proporciona solo a modo informativo. El usuario asume todo riesgo de uso o resultados del uso de este documento, y Microsoft Corporation no otorga garantías expresas ni implícitas. Las compañías, las organizaciones, los productos, las personas y los acontecimientos de ejemplo aquí descritos son ficticios. No se pretende indicar ni debe deducirse ninguna asociación con empresas, organizaciones, productos, personas o eventos reales. El cumplimiento de todas las leyes de propiedad intelectual vigentes es responsabilidad del usuario. Sin limitación de los derechos de propiedad intelectual, ninguna parte de este documento puede ser reproducida, almacenada o introducida en un sistema de recuperación, o transmitida de ninguna forma ni por ningún medio (electrónico, mecánico, Fotocopiado, grabación o de cualquier otro modo), ni con ningún propósito, sin la autorización expresa y por escrito de Microsoft Corporation.

Microsoft puede tener patentes, solicitudes de patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual sobre los contenidos de este documento. A excepción de lo estipulado expresamente en un contrato de licencia por escrito de Microsoft, el suministro de este documento no le otorga ninguna licencia para estas patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual.



Microsoft, MS-DOS, Windows, WindowsServer, Windows Vista, Active Directory y ActiveSync son marcas comerciales registradas o marcas comerciales de MicrosoftCorporation en los Estados Unidos y/o en otros países.

Los nombres de las compañías y productos reales mencionados en el presente pueden ser marcas comerciales de sus respectivos propietarios.

 

 





