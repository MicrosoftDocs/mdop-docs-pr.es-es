---
title: Notas de la versión de App-V 4.5 SP2
description: Notas de la versión de App-V 4.5 SP2
author: dansimp
ms.assetid: 1b3a8a83-4523-4634-9f75-29bc22ca5815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 35cff3b2a2c110a4d8beba883a4cf9332381ea60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819851"
---
# Notas de la versión de App-V 4.5 SP2


Para buscar estas notas de la versión, presione CTRL + F.

**Importante**  Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de virtualización de aplicaciones de Microsoft. Estas notas de la versión contienen información que necesita para instalar correctamente el sistema de administración de virtualización de aplicaciones. Estas notas de la versión contienen información que no está disponible en la documentación del producto. Si hay una discrepancia entre estas notas de la versión y otra documentación del sistema de administración de virtualización de aplicaciones, el cambio más reciente debe considerarse autoritario.

 

Para obtener información actualizada sobre problemas conocidos, visite la biblioteca de Microsoft TechNet en las [notas de la versión de App-V 4,5 SP2](https://go.microsoft.com/fwlink/?LinkId=184640) ( https://go.microsoft.com/fwlink/?LinkId=184640) .

## Acerca de Microsoft Application Virtualization 4,5 Service Pack 2


Estas notas de la versión se han actualizado para reflejar los cambios que se introdujeron con Microsoft Application Virtualization (App-V) 4.5 Service Pack2 (SP2). Este Service Pack contiene los siguientes cambios:

-   Soporte técnico para Office 2010: App-V 4.5 SP2 ahora es compatible con la virtualización de Microsoft Office 2010. Para obtener instrucciones preceptivas para la secuenciación de Microsoft Office 2010 con App-V 4,5 SP2, consulte [directrices preceptivas para la secuencia de Office 2010 en Microsoft App-v 4,6](https://go.microsoft.com/fwlink/?LinkId=191539) ( https://go.microsoft.com/fwlink/?LinkId=191539) .

-   Compatibilidad con la creación de reflejo de base de datos: App-V 4.5 SP2 ahora es compatible con el reflejo de base de datos de Microsoft SQL Server. Para obtener más información sobre cómo configurar el reflejo de base de datos en el entorno de App-V, consulte [Cómo configurar la compatibilidad con el reflejo de Microsoft SQL Server para App-v](https://go.microsoft.com/fwlink/?LinkId=190880) ( https://go.microsoft.com/fwlink/?LinkId=190880) .

-   Comentarios de los clientes y Resumen de revisiones: App-V 4.5 SP2 también incluye un resumen de las correcciones para solucionar los problemas que se hayan encontrado después del lanzamiento de App-V 4.5 SP1. Las actualizaciones tratan una combinación de problemas conocidos y comentarios de los clientes de equipos internos de Microsoft, socios y clientes que usan App-V 4.5. Para obtener una lista completa de las actualizaciones, consulte el artículo 980847 de Microsoft Knowledge base (KB) en la [Descripción de Microsoft Application virtualization 4,5 Service Pack 2](https://go.microsoft.com/fwlink/?LinkId=191540) ( https://go.microsoft.com/fwlink/?LinkId=191540) .

## Acerca de la documentación del producto


Encontrará documentación completa de Application Virtualization (App-V) en Microsoft TechNet, en la [biblioteca de TechCenter de Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) . La documentación de TechNet incluye la ayuda en línea del Application Virtualization Sequencer, los clientes de virtualización de aplicaciones y el servidor de virtualización de aplicaciones. También incluye la guía de planeación e implementación de virtualización de aplicaciones y la guía de operaciones de virtualización de aplicaciones.

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudarle a protegerse contra virus y vulnerabilidades de seguridad, le recomendamos que instale las últimas actualizaciones de seguridad disponibles para cualquier software nuevo que se instale. Para obtener más información, consulte [seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Enviar comentarios


Puede proporcionar comentarios, realizar una sugerencia o informar de un problema con el sistema de administración de Microsoft Application Virtualization (App-V) a través del Foro de la comunidad en el foro de documentación de Application Virtualization TechCenter [de App-v](https://go.microsoft.com/fwlink/?LinkId=122917) ( https://go.microsoft.com/fwlink/?LinkId=122917) .

También puede enviar sus comentarios sobre la documentación directamente al equipo de documentación de App-V en <appvdocs@microsoft.com> .

## Problemas conocidos con Application Virtualization 4.5 SP2


Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.5 SP2. Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Siempre que sea posible, estos problemas se resolverán en versiones posteriores del software.

### Instrucciones para instalar la consola de administración de servidores

Si tiene que instalar software de administración en sistemas distintos del servidor principal de publicación y streaming de virtualización de aplicaciones, la instalación del servidor admite la instalación de la consola de administración de virtualización de aplicaciones y el servicio Web de administración de virtualización de aplicaciones en servidores independientes del servidor de administración principal de App-V. Para distribuir los componentes de administración en varios servidores, la delegación Kerberos debe estar habilitada en el servidor donde esté instalado el servicio Web de virtualización de aplicaciones. Para obtener más información sobre cómo habilitar esta compatibilidad, vea [Cómo configurar el servidor para que sea de confianza para la delegación](https://go.microsoft.com/fwlink/?LinkId=166682) ( https://go.microsoft.com/fwlink/?LinkId=166682) .

### Instrucciones para instalar o actualizar clientes a App-V 4.5 SP2 con Setup.msi

Al instalar o actualizar los clientes de App-V a App-V 4,5 SP2 mediante Setup.msi, los requisitos previos no se instalan automáticamente.

WORKAROUNDYou debe instalar manualmente los requisitos previos antes de instalar o actualizar los clientes de App-V a la aplicación-V 4.5 SP2. Para obtener procedimientos detallados sobre cómo instalar los requisitos previos y el cliente de App-V, consulte [Cómo instalar el cliente mediante la línea de comandos](https://go.microsoft.com/fwlink/?LinkId=144106) ( https://go.microsoft.com/fwlink/?LinkId=144106) .

Cuando haya finalizado, instale los clientes de App-V 4,5 SP2 con Setup.msi con credenciales administrativas. Este archivo está disponible en el medio de la versión App-V 4,5 SP2 de la carpeta Installers\\Client.

Al instalar informes de errores de aplicaciones de Microsoft, use el siguiente comando si está instalando o actualizando el cliente de escritorio de App-V 4,5 SP2:

**msiexec/i dw20shared.msi APPGUID = {C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D} ALLUSERS = 1 reboot = suprimir REINSTALL = ALL REINSTALLMODE = vomus**

Como alternativa, si está instalando o actualizando el cliente de App-V 4,5 SP2 para servicios de escritorio remoto (anteriormente servicios de Terminal Server), use el siguiente comando:

**msiexec/i dw20shared.msi APPGUID = {ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5} ALLUSERS = 1 reboot = suprimir REINSTALL = ALL REINSTALLMODE = vomus**

**Nota**  
-   El parámetro APPGUID hace referencia al código de producto de los clientes de App-V que instale o actualice. El código de producto es único para cada Setup.msi. Puede usar el editor de bases de datos Orca o una herramienta similar para examinar los archivos de Windows Installer y determinar el código de producto. Este paso es necesario para todas las instalaciones o actualizaciones de App-V 4,5 SP2.

-   Este paso no es necesario si está actualizando y ha instalado previamente Dw20shared.msi.

 

### Mejorar el rendimiento al secuenciar .NET Framework

Al secuenciar Microsoft .NET Framework, es posible que se reduzca el rendimiento del sistema porque el servicio NGEN de .NET Framework intenta precompilar los ensamblados como una tarea en segundo plano.

WORKAROUNDWhen la secuencia de .NET Framework, deshabilite el servicio NGEN de .NET Framework (Mscorsvw.exe) después de completar la fase de supervisión. Debe usar la pestaña de **servicios virtuales** en el secuenciador de App-V y cambiar el tipo de inicio a **deshabilitado**.

### Al desinstalar el cliente de Microsoft Application Virtualization, se elimina la configuración de usuario asociada al usuario que realiza la desinstalación.

Al desinstalar el cliente de App-V, Windows Installer quita la configuración de virtualización de la aplicación del perfil del usuario actual. Si su equipo usa perfiles móviles, no use su cuenta de red personal para desinstalar el cliente porque quitará la configuración de las aplicaciones virtuales en todos los equipos.

WORKAROUNDYou debe desinstalar el cliente de App-V con una cuenta administrativa que no se use para ejecutar aplicaciones virtuales.

### Las modificaciones realizadas en las fichas sistema de archivos virtual y registro virtual se deben guardar mientras se ejecuta el Asistente para secuenciación

Si abre un paquete para realizar una actualización o si ya ha ejecutado el Asistente para secuenciación con un nuevo paquete y realiza cambios en el paquete en las fichas sistema de archivos virtual o registro virtual, esos cambios no se guardan automáticamente.

WORKAROUNDSave los cambios antes de volver a ejecutar el Asistente para asegurarse de que se reflejan en el entorno virtual del asistente.

### El secuenciador de línea de comandos debe ejecutarse desde un símbolo del sistema con privilegios elevados

Al usar el secuenciador de línea de comandos, no se solicita la elevación.

WORKAROUNDRun el secuenciador de línea de comandos mediante un símbolo del sistema con privilegios elevados.

### Los nombres de variable de ruta corta en archivos OSD pueden provocar errores

Si recibe el error 450478-1F702339-0000010B "el nombre del directorio no es válido" al iniciar una aplicación virtual en el cliente, es posible que la variable de la OSD no esté configurada correctamente. Esto puede suceder si el instalador de la aplicación establece un nombre de ruta corto durante la secuenciación.

WORKAROUNDRemove la tilde final de cualquier variable CSIDL que exista en el archivo OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Sintaxis correcta para el parámetro DECODEPATH para el secuenciador de la línea de comandos

En el secuenciador de línea de comandos, al abrir un paquete para actualizarlo y descodificarlo en la raíz de la unidad Q, la sintaxis del parámetro *DECODEPATH* no debe incluir una barra diagonal.

WORKAROUNDYou puede usar **Q:** en lugar de **Q:\\** (omitiendo el carácter "\ \" final).

### <a href="" id="when-upgrading-app-v-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Cuando los paquetes upgradingAPP-V 4,2, se producen problemas causados por los archivos de Windows Installer en el sistema de archivos virtual

Al actualizar un paquete de APP-V 4.2, es posible que se produzcan problemas relacionados con la falta de coincidencia de los archivos de sistema de Windows Installer que se incluyeron de forma predeterminada en APP-V 4.2 y las bibliotecas de Windows Installer instaladas de forma local en su estación de trabajo de secuenciación. Los siguientes archivos se encuentran en CSIDL \ _SYSTEM \ \:

Cabinet.dll

Msi.dll

Msiexec.exe

Msihnd.dll

Msimsg.dlll

WORKAROUNDDelete todos los archivos anteriores del paquete. Elimine las asignaciones de la ficha **VFS** y los archivos reales de la carpeta CSIDL \ _SYSTEM en la ruta de descodificación.

### <a href="" id="on-windows-xp--by-default--client-installation-logging-is-not-enabled-"></a>En WindowsXP, de forma predeterminada, el registro de instalación del cliente no está habilitado

Al instalar el cliente, para asegurarse de que se capturan los errores de instalación para la solución de problemas, debe habilitar el registro mediante la línea de comandos.

WORKAROUNDAdd el parámetro */l\ * VX! log.txt* a la línea de comandos, como se muestra en el siguiente ejemplo:

**setup.exe/s/v "/QN/l\ * VX! log.txt "**

**msiexec.exe/i setup.msi/QN/l\ * VX! log.txt**

Como alternativa, puede establecer la clave del registro en el valor siguiente:

**\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"**

### Para que la autenticación Kerberos funcione, los nombres principales de servicio (SPN) deben registrarse para IIS

Cuando se usa Internet Information Services (IIS) 6.0 orIIS 7.0 para la recuperación y la transmisión de archivos OSD o de iconos, para habilitar la autenticación Kerberos, los SPN deben registrarse de la siguiente manera:

-   En el servidor IIS, ejecute los siguientes comandos con la herramienta kit de recursos de SETSPN.EXE. Debe usarse el nombre de dominio completo (FQDN) del servidor.

    **Setspn-r SOFTGRID/ &lt; Server FQDN&gt;**

    **Setspn-r FQDN de &lt; servidor o http&gt;**

Para obtener más información, consulte [autenticación integrada de Windows (IIS 6,0)](https://go.microsoft.com/fwlink/?LinkId=131407) ( https://go.microsoft.com/fwlink/?LinkId=131407) .

### Cambios en la compatibilidad de .NET

Los update1 acumulativos de Microsoft Application Virtualization (App-V) o versiones posteriores admiten la secuenciación de .NET Framework en WindowsXP SP2 o versiones posteriores. Es posible que las rutinas de secuencias para las aplicaciones .NET escritas para SoftGrid 4.2 deban actualizarse cuando se usan con el secuenciador de aplicaciones-V 4,5. Para obtener más detalles y soluciones alternativas, consulte el artículo TechCenter de Application Virtualization en [soporte técnico para .net en Microsoft Application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=123412) ( https://go.microsoft.com/fwlink/?LinkId=123412) .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Después de la actualización del cliente de App-V 4.2, algunas aplicaciones no se muestran.

Consulte el siguiente error en el registro: "el cliente de Application Virtualization no pudo analizar el archivo OSD". El cliente de App-V 4,5 filtra las aplicaciones que tienen un archivo OSD que contiene una etiqueta de sistema operativo vacía ( &lt; os &gt; &lt; /os &gt; ).

WORKAROUNDDelete la etiqueta de OS vacía del archivo OSD.

### El servidor de App-V requiere exenciones en su firewall para ciertos procesos

Para que el servidor pueda transmitir aplicaciones correctamente, los procesos básicos del servidor, incluido el distribuidor, requieren acceso a través del firewall.

WORKAROUNDSet exenciones en el firewall del servidor para los siguientes procesos: Sghwsvr.exe y Sghwdsptr.exe. Esto se aplica al servidor de administración de App-V y al servidor de streaming de App-V.

### Cuando el instalador del servidor se ejecuta en modo silencioso, no comprueba correctamente si MSXML6

El servidor de administración de App-V depende de MSXML6. Sin embargo, si ejecuta el instalador en modo silencioso, por ejemplo, usando el comando **msiexec-i setup.msi/QN** en un sistema donde MSXML6 no está ya instalado, el instalador no detecta la dependencia que falta y se instala de todos modos. Por lo tanto, cuando los clientes intenten actualizar la información de publicación desde App-V Management Server, recibirán errores.

WORKAROUNDVerify que MSXML6 se instala en el sistema antes de intentar una instalación silenciosa del servidor de administración de App-V.

### Código de error 000C800 al intentar conectarse a la consola de administración de virtualización de aplicaciones

Un administrador de virtualización de aplicaciones que no sea un administrador local en el servidor de servicio Web de App-V recibe un error (código de error: 000C800) al intentar conectarse a la consola de administración de App-V y la entrada Sftmmc. log indica que se ha denegado el acceso a SftMgmt. udl. Para conectarse correctamente a la consola de administración de App-V, un administrador que no tenga derechos de administrador local en el servidor del servicio Web de administración de App-V debe tener al menos permisos de lectura y ejecución en el archivo SftMgmt. udl.

Los administradores de Application Virtualization deben tener permisos de lectura y ejecución en el archivo SftMgmt. UDL en carpeta%systemdrive%\\Program de Programa\\microsoft System Center App virt Management Server\\App virt Management Service.

### Los parámetros de la línea de comandos del instalador del cliente se omiten cuando se usan conjuntamente con KEEPCURRENTSETTINGS = 1

Cuando se usa junto con KEEPCURRENTSETTINGS = 1, se omiten los siguientes parámetros de línea de comandos del instalador de cliente: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA y REQUIRESECURECONNECTION.

WORKAROUNDIf tiene una configuración que desea conservar, use KEEPCURRENTSETTINGS = 1 y, a continuación, establezca los otros parámetros después de la implementación. La plantilla ADM de App-V se puede usar para establecer la siguiente configuración de cliente: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES y ALLOWINDEPENDENTFILESTREAMING. Puede descargar la plantilla ADM desde el centro de descarga de Microsoft en la [plantilla administrativa de Microsoft Application Virtualization (plantilla ADM)](https://go.microsoft.com/fwlink/?LinkId=121835) ( https://go.microsoft.com/fwlink/?LinkId=121835) .

### Información de copyright de notas de versión

Este documento se proporciona “tal cual”. La información y las vistas expresadas en este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, pueden cambiar sin previo aviso. Usted asume el riesgo de su uso.

Algunos ejemplos que se describen en este artículo se proporcionan solo para la ilustración y son ficticios.No se pretende ni se debe deducir ninguna asociación o conexión real.

Este documento no le proporciona derechos legales sobre ninguna propiedad intelectual en ningún producto de Microsoft. Puede copiar y usar este documento para su referencia interna. Puede modificar este documento para su referencia interna.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer y Windows Vista son marcas comerciales del grupo de compañías Microsoft.

El resto de marcas comerciales pertenecen a sus respectivos dueños.

 

 





