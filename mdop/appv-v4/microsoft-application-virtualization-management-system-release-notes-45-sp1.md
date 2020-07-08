---
title: Notas de la versión de Microsoft Application Virtualization Management System 4,5 SP1
description: Notas de la versión de Microsoft Application Virtualization Management System 4,5 SP1
author: dansimp
ms.assetid: 5d6b11ea-7b87-4084-9a7c-0d831f247aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c24d2e98ad09460ca22e4b29d75ae2b9c72d0bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816160"
---
# Notas de la versión de Microsoft Application Virtualization Management System 4,5 SP1


Para buscar estas notas de la versión, presione CTRL + F.

**Importante**  Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de virtualización de aplicaciones. Estas notas de la versión contienen información que necesita para instalar correctamente el sistema de administración de virtualización de aplicaciones. Estas notas de la versión contienen información que no está disponible en la documentación del producto. Si hay una discrepancia entre estas notas de la versión y otra documentación del sistema de administración de virtualización de aplicaciones, el cambio más reciente debe considerarse autoritario.

 

Para obtener información actualizada sobre problemas conocidos, visite la biblioteca de Microsoft TechNet en <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Acerca de Microsoft Application Virtualization 4,5 Service Pack 1


Estas notas de la versión se han actualizado para reflejar los cambios introducidos en Microsoft Application Virtualization (App-V) 4.5 Service Pack1 (SP1). Este Service Pack contiene los siguientes cambios:

-   Soporte técnico para Windows 7 y Windows Server 2008 R2: App-V 4,5 SP1 proporciona soporte técnico para Windows 7 y Windows Server 2008 R2, incluida la compatibilidad con características de Windows 7, como la barra de tareas, AppLocker, BranchCache y BitLocker To Go.La compatibilidad de Windows Server 2008 R2 solo es para el servidor de virtualización de aplicaciones. Para obtener más información sobre la compatibilidad de AppLocker en Windows 7, consulte <https://go.microsoft.com/fwlink/?LinkID=156732> .

-   Compatibilidad con territorios Kerberos de terceros: App-V 4,5 SP1 proporciona compatibilidad para entornos que tienen una relación de confianza y cuentas de usuario asignadas entre un dominio de Windows y un territorio MIT Kerberos, que es un escenario común en muchas universidades. Para obtener información sobre cómo habilitar esta compatibilidad, visite la biblioteca de Microsoft TechNet en <https://go.microsoft.com/fwlink/?LinkId=166004> .

-   Se ha mejorado la compatibilidad con la publicación de aplicaciones y la transmisión por secuencias a través de HTTP/HTTPS: App-V 4,5 SP1 proporciona soporte técnico para la publicación de aplicaciones y la transmisión por secuencias a través de los protocolos HTTP/HTTPS para Windows XP Home Edition, Windows Vista Home Basic y Windows 7 Home Basic.

-   Comentarios de los clientes y Resumen de revisiones: App-V 4.5 SP1 también incluye un resumen de las correcciones para solucionar los problemas encontrados desde la versión de Microsoft Application Virtualization (App-V) 4.5 CU1. Las actualizaciones son el resultado de una combinación de problemas conocidos y comentarios de los clientes de nuestros equipos internos, socios y clientes que usan App-V 4.5. Para obtener una lista completa de las actualizaciones, consulte el artículo de KB en <https://go.microsoft.com/fwlink/?LinkId=167121> .

## Acerca de la documentación del producto


Encontrará documentación completa de Application Virtualization (App-V) en Microsoft TechNet en el TechCenter de Application Virtualization (App-V) en <https://go.microsoft.com/fwlink/?LinkId=122939> . La documentación de TechNet incluye la ayuda en línea de Application Virtualization Sequencer, el cliente de virtualización de aplicaciones y el servidor de virtualización de aplicaciones. También incluye la guía de planeación e implementación de virtualización de aplicaciones y la guía de operaciones de virtualización de aplicaciones.

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudarle a protegerse contra virus y vulnerabilidades de seguridad, le recomendamos que instale las últimas actualizaciones de seguridad disponibles para cualquier software nuevo que se instale. Para obtener más información, visite el sitio web de seguridad de Microsoft en <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Proporcionar comentarios


Puede proporcionar comentarios, realizar una sugerencia o informar de un problema con el sistema de administración de Microsoft Application Virtualization (App-V) a través de un foro de la comunidad en Microsoft Application Virtualization TechCenter ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

También puede enviar sus comentarios sobre la documentación directamente al equipo de documentación de App-V. Envíe sus comentarios sobre la documentación a appvdocs@microsoft.com.

## Problemas conocidos con Application Virtualization 4.5 SP1


Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.5 SP1. Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Siempre que sea posible, estos problemas se resolverán en versiones posteriores del software.

### Instrucciones para instalar la consola de administración de servidores

Si necesita instalar software de administración en sistemas distintos del servidor principal de publicación y streaming de la virtualización de aplicaciones, la instalación del servidor admite la instalación de la consola de administración y el servicio Web de administración en servidores independientes del servidor de administración de App-V principal. Para distribuir los componentes de administración en varios servidores, la delegación Kerberos debe estar habilitada en el servidor en el que está instalado el servicio Web. Para obtener información sobre cómo habilitar este soporte técnico, visite la biblioteca de Microsoft TechNet en <https://go.microsoft.com/fwlink/?LinkId=166682>

### Instrucciones para instalar o actualizar clientes a App-V 4.5 SP1 con setup.msi

Al instalar o actualizar los clientes de App-V a App-V 4,5 SP1 mediante setup.msi, los requisitos previos no se instalan automáticamente.

WORKAROUNDYou debe instalar manualmente los requisitos previos antes de instalar o actualizar el cliente de App-V toApp-V 4,5 SP1. Para obtener los procedimientos detallados para instalar los requisitos previos y el cliente de App-V, consulte <https://go.microsoft.com/fwlink/?LinkId=144106> .

Cuando haya finalizado, instale el cliente de App-V 4,5 SP1 con setup.msi con privilegios elevados. Este archivo está disponible en el soporte de la versión App-V 4,5 SP1 de la carpeta Installers\\Client.

Al instalar informes de errores de aplicaciones de Microsoft, use el comando siguiente si está instalando o actualizando el cliente de escritorio de App-V 4,5 SP1:

    msiexec /i dw20shared.msi APPGUID={93468B43-C19D-44F9-8BCC-114076DB0443}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Como alternativa, si está instalando o actualizando el cliente de App-V 4,5 SP1 para servicios de escritorio remoto (anteriormente servicios de Terminal Server), use el siguiente comando:

    msiexec /i dw20shared.msi APPGUID={0042AD3C-99A4-4E58-B5F0-744D5AD96E1C} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Nota:**  El parámetro APPGUID hace referencia al código de producto del cliente de App-V que instala o actualiza. El código de producto es único para cada setup.msi. Puede usar el editor de bases de datos Orca o una herramienta similar para examinar los archivos de Windows Installer y determinar el código de producto. Este paso es necesario para todas las instalaciones o actualizaciones de App-V 4,5 SP1.

 

### Mejorar el rendimiento al secuenciar .NET Framework

Al secuenciar .NET Framework, es posible que se reduzca el rendimiento del sistema porque el servicio NGEN de Microsoft .NET Framework intenta precompilar los ensamblados como una tarea en segundo plano.

WORKAROUNDWhen en secuencia de .NET Framework, deshabilite el servicio NGEN de Microsoft .NET Framework (mscorsvw.exe) después de completar la fase de supervisión. Debe usar la pestaña de **servicios virtuales** en el secuenciador y cambiar el tipo de inicio a deshabilitado.

### Al desinstalar el cliente de Microsoft Application Virtualization, se eliminará la configuración de usuario asociada al usuario que realiza la desinstalación.

Al desinstalar el cliente de App-V, Windows Installer quitará la configuración de virtualización de la aplicación del perfil del usuario actual. Si su equipo usa perfiles móviles, no use su cuenta de red personal para desinstalar el cliente porque quitará la configuración de las aplicaciones virtuales en todos los equipos.

WORKAROUNDYou debe realizar la desinstalación del cliente de App-V con una cuenta administrativa que no se use para ejecutar aplicaciones virtuales.

### Las modificaciones realizadas en las fichas sistema de archivos virtual y registro virtual se deben guardar mientras se ejecuta el Asistente para secuenciación

Si abre un paquete para realizar una actualización o si ya ha ejecutado el Asistente para secuenciación con un nuevo paquete y realiza cambios en el paquete en las fichas sistema de archivos virtual o registro virtual, esos cambios no se guardan automáticamente.

WORKAROUNDSave los cambios antes de volver a ejecutar el Asistente para asegurarse de que se reflejan en el entorno virtual del asistente.

### El secuenciador de línea de comandos debe ejecutarse desde un símbolo del sistema con privilegios elevados

Al usar el secuenciador de línea de comandos, no se solicita la elevación.

WORKAROUNDRun el secuenciador de línea de comandos con un símbolo del sistema con privilegios elevados.

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

### Cambios en la compatibilidad de .NET

Los update1 acumulativos de Microsoft Application Virtualization (App-V) o versiones posteriores admiten la secuenciación de .NET Framework en WindowsXP (SP2 o posterior). Es posible que tenga que actualizar las rutinas de secuencia para las aplicaciones .NET escritas para SoftGrid 4.2 cuando se usa con el secuenciador de aplicaciones-V 4,5. Para obtener detalles y soluciones alternativas, consulte el artículo de Knowledge base en <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Después de la actualización del cliente de App-V 4.2, algunas aplicaciones no se muestran.

Consulte el siguiente error en el registro: "el cliente de Application Virtualization no pudo analizar el archivo OSD". El cliente de App-V 4,5 filtra las aplicaciones que tienen un archivo OSD que contiene una etiqueta de sistema operativo vacía ( &lt; sistema operativo &gt; &lt; /os &gt; ).

WORKAROUNDDelete la etiqueta de OS vacía del archivo OSD.

### El servidor de App-V requiere exenciones en su firewall para ciertos procesos

Para que el servidor pueda transmitir aplicaciones correctamente, los procesos básicos del servidor, incluido el distribuidor, necesitan tener acceso a través del firewall.

WORKAROUNDSet exenciones en el firewall del servidor para los siguientes procesos: sghwsvr.exe y sghwdsptr.exe. Esto se aplica al servidor de administración de App-V y al servidor de streaming de App-V.

### Cuando el instalador del servidor se ejecuta en modo silencioso, no comprueba correctamente si MSXML6

El servidor de administración de App-V depende de MSXML6. Sin embargo, si ejecuta el instalador en modo silencioso, por ejemplo, con el comando "msiexec-i setup.msi/QN" en un sistema donde MSXML6 ya no está instalado, el instalador no detecta la dependencia que falta y se instala de todos modos. Por lo tanto, cuando los clientes intenten actualizar la información de publicación desde App-V Management Server, verán errores.

WORKAROUNDVerify que MSXML6 se instala en el sistema antes de intentar una instalación silenciosa del servidor de administración de App-V.

### Código de error 000C800 al intentar conectarse a la consola de administración de virtualización de aplicaciones

Un administrador de virtualización de aplicaciones que no sea un administrador local en el servidor del servicio Web de administración de aplicaciones-V recibirá un error (código de error: 000C800) cuando intente conectarse a la consola de administración de App-V y la entrada sftmmc. log indicará que se ha denegado el acceso a SftMgmt. udl. Para conectarse correctamente a la consola de administración de App-V, un administrador que no tenga derechos de administrador local en el servidor del servicio Web de administración de App-V debe tener al menos permisos de lectura y ejecución en el archivo SftMgmt. udl.

Los administradores de Application Virtualization deben recibir permisos de lectura y ejecución en el archivo SftMgmt. UDL en%systemdrive%\\Program de Programa\\microsoft System Center App virt Management Server\\App virt Management Service.

### Los parámetros de la línea de comandos del instalador del cliente se omiten cuando se usan conjuntamente con KEEPCURRENTSETTINGS = 1

Cuando se usa junto con KEEPCURRENTSETTINGS = 1, se omiten los siguientes parámetros de línea de comandos del instalador de cliente: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA y REQUIRESECURECONNECTION.

WORKAROUNDIf tiene una configuración que desea conservar, use KEEPCURRENTSETTINGS = 1 y, a continuación, establezca los otros parámetros después de la implementación. La plantilla ADM de App-V se puede usar para establecer la siguiente configuración de cliente: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES y ALLOWINDEPENDENTFILESTREAMING. La plantilla ADM puede encontrarse en <https://go.microsoft.com/fwlink/?LinkId=121835> .

## Información de copyright de notas de versión


La información de este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, está sujeta a cambios sin previo aviso y se proporciona solo con fines informativos. El usuario asume todo riesgo de uso o resultados del uso de este documento, y Microsoft Corporation no otorga garantías expresas ni implícitas. A menos que se indique lo contrario, las empresas, las organizaciones, los productos, los nombres de dominio, las direcciones de correo electrónico, los logotipos, las personas, los lugares y los acontecimientos representados en los ejemplos son ficticios. No se pretende indicar ni debe deducirse ninguna asociación con ninguna compañía, organización, producto, nombre de dominio, dirección de correo electrónico, logotipo, persona, lugar o acontecimiento reales. El cumplimiento de todas las leyes de propiedad intelectual vigentes es responsabilidad del usuario. Sin limitación de los derechos de propiedad intelectual, ninguna parte de este documento puede ser reproducida, almacenada o introducida en un sistema de recuperación, o transmitida de ninguna forma ni por ningún medio (electrónico, mecánico, Fotocopiado, grabación o de cualquier otro modo), ni con ningún propósito, sin la autorización expresa y por escrito de Microsoft Corporation.

Microsoft puede tener patentes, solicitudes de patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual sobre los contenidos de este documento. A excepción de lo estipulado expresamente en un contrato de licencia por escrito de Microsoft, el suministro de este documento no le otorga ninguna licencia para estas patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer y Windows Vista son marcas comerciales del grupo de compañías Microsoft.

El resto de marcas comerciales pertenecen a sus respectivos dueños.

 

 





