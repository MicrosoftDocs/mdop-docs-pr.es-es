---
title: Mensajes de registro de eventos de MED-V
description: Mensajes de registro de eventos de MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823080"
---
# Mensajes de registro de eventos de MED-V


Los archivos de registro de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 proporcionan información detallada sobre cómo implementar y administrar MED-V en su empresa y ayudar a comprobar la funcionalidad o a solucionar problemas.

## Identificadores de evento


A continuación se muestra una lista de identificadores de eventos de MED-V para ayudar a solucionar problemas que pueden surgir al implementar o administrar MED-V.

### Generan

Muestra los identificadores de evento para la configuración de primera vez.

### IDENTIFICADOR de evento 3066

Error en la operación iniciar máquina virtual.

<a href="" id="description"></a>**Descripción**  
Existe un posible problema con el disco duro virtual (VHD) que usa para crear un área de trabajo de MED-V.

<a href="" id="solution"></a>**Solución**  
Compruebe que puede crear una máquina virtual con el VHD para MED-V y que se puede iniciar.

### IDENTIFICADOR de evento 3071

Error en la preparación de la máquina virtual.

<a href="" id="description"></a>**Descripción**  
Se produjo un problema con la configuración por primera vez que puede haber sido causada por muchos problemas diferentes. Esto incluye problemas con la conectividad de red.

<a href="" id="solution"></a>**Solución**  
Reinicie el agente de host MED-V para volver a ejecutar la configuración de la primera vez.

### IDENTIFICADOR de evento 3078

Error en la preparación de la máquina virtual.

<a href="" id="description"></a>**Descripción**  
Existe un posible problema con el VHD que está usando para crear un área de trabajo de MED-V.

<a href="" id="solution"></a>**Solución**  
Compruebe que puede crear una máquina virtual con el VHD para MED-V y que se puede iniciar.

### IDENTIFICADOR de evento 3079

Reintentando la preparación de la máquina virtual.

<a href="" id="description"></a>**Descripción**  
MED-V está intentando preparar la máquina virtual.

<a href="" id="solution"></a>**Solución**  
No se requiere ninguna acción. Permitir que finalice la configuración por primera vez.

### IDENTIFICADOR de evento 3080

El cliente se detuvo al preparar la máquina virtual.

<a href="" id="description"></a>**Descripción**  
MED-V se detiene de forma inesperada cuando intenta preparar la máquina virtual.

<a href="" id="solution"></a>**Solución**  
Iniciar el agente de host MED-V y permitir que se complete la configuración por primera vez

### IDENTIFICADOR de evento 3084

La máquina virtual no es válida. Es necesario volver a ejecutar la configuración por primera vez.

<a href="" id="description"></a>**Descripción**  
El agente de host MED-V detectó un problema con la máquina virtual.

<a href="" id="solution"></a>**Solución**  
No se requiere ninguna acción. Permitir que finalice la configuración por primera vez.

### IDENTIFICADOR de evento 3099

Error al llamar a la máquina virtual de inicio.

<a href="" id="description"></a>**Descripción**  
Existe un posible problema con el VHD que usas para crear un área de trabajo de MED-V.

<a href="" id="solution"></a>**Solución**  
Compruebe que puede crear una máquina virtual con el VHD para MED-V y que se puede abrir.

### Administración de VM

### IDENTIFICADOR de evento 4022

VMManagerException error grave al emitir el comando a la VM.

<a href="" id="description"></a>**Descripción**  
El usuario final ha intentado salir de MED-V cerrando sesión o cerrando el host MED-V y se ha superado la configuración de configuración VMTaskTimeout.

<a href="" id="solution"></a>**Solución**  
Reinicie MED-V.

### IDENTIFICADOR de evento 4028

Se agotó el tiempo de espera de la operación de VM.

<a href="" id="description"></a>**Descripción**  
El usuario final intentó salir de MED-V al cerrar sesión o apagar el host, y se superó la configuración de configuración VMTaskTimeout.

<a href="" id="solution"></a>**Solución**  
Reinicie MED-V.

### IDENTIFICADOR de evento 4038

Vmsal publicó un mensaje de error para el usuario.

<a href="" id="description"></a>**Descripción**  
Se muestra un mensaje de error al usuario final en el que se indica que MED-V no pudo iniciar la aplicación virtual.

<a href="" id="solution"></a>**Solución**  
Si el error se registra dos o más veces en una fila, detenga MED-V y conéctese a la máquina virtual con la consola de Virtual PC e intente iniciar la aplicación en pantalla completa.

### IDENTIFICADOR de evento 4040

Las adiciones de reciclaje porque TerminalServices no está inicializado en el invitado.

<a href="" id="description"></a>**Descripción**  
MED-V reinició la máquina virtual porque no se inicializaron los servicios de escritorio remoto en la máquina virtual.

<a href="" id="solution"></a>**Solución**  
Si el error se registra dos o más veces seguidas, detenga MED-V y conéctese a la máquina virtual mediante la consola de Windows Virtual PC.

### IDENTIFICADOR de evento 4042

Error al reciclar adiciones en el invitado.

<a href="" id="description"></a>**Descripción**  
MED-V no pudo reciclar las adiciones de máquina virtual en la máquina virtual.

<a href="" id="solution"></a>**Solución**  
Si el error se registra dos o más veces seguidas, detenga MED-V y conéctese a la máquina virtual mediante la consola de Windows Virtual PC.

### IDENTIFICADOR de evento 4043

Error al restablecer la contraseña expirada en la máquina virtual.

<a href="" id="description"></a>**Descripción**  
El usuario final no restableció la contraseña en la máquina virtual antes de que expirara. Como resultado, es posible que el usuario no pueda obtener acceso a los recursos de red ni guardar el trabajo.

<a href="" id="solution"></a>**Solución**  
Cierre el invitado MED-V y reinícielo.

### Redireccionamiento de URL

### IDENTIFICADOR de evento 5005

No se puede obtener el nombre de la VM de la configuración; no se puede iniciar el explorador invitado.

<a href="" id="description"></a>**Descripción**  
El redireccionamiento de URL no pudo obtener el nombre del área de trabajo MED-V de la configuración. Por lo tanto, no puede informar a Windows Virtual PC para que abra la dirección URL redirigida en el explorador de área de trabajo de MED-V.

<a href="" id="solution"></a>**Solución**  
Asegúrese de que el nombre del área de trabajo MED-V está establecido y que coincide con el nombre de una máquina virtual en el directorio C:\\Users\\ de \\Virtual de &lt; *usuario*de &gt; equipos. El nombre del área de trabajo MED-V se encuentra en HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Por ejemplo, si el usuario es "Matt" y el nombre del área de trabajo es "mattsworkspace", el valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name debe ser "mattsworkspace" y debe haber un archivo denominado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.VCMX.

### IDENTIFICADOR de evento 5006

Error al crear el servidor de canalización.

<a href="" id="description"></a>**Descripción**  
El servicio de redireccionamiento de URL no pudo crear el servidor de canalización para comunicarse con Internet Explorer.

<a href="" id="solution"></a>**Solución**  
Consulte los registros de eventos del sistema para intentar crear un archivo o recurso cuya ruta de acceso empiece de forma similar a la siguiente: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" y termine con el nombre de usuario y el nombre de dominio del usuario. Si no está presente en el registro de eventos, reinicie el equipo.

### ConfigMgr (invitado)

### IDENTIFICADOR de evento 7001

Los datos de configuración de la red de hospedaje no tienen el formato correcto.

<a href="" id="description"></a>**Descripción**  
La configuración de red recibida del host es una cadena XML con formato incorrecto o la información de red devuelta del host no se puede escribir en un documento XML.

<a href="" id="solution"></a>**Solución**  
Reinicie el equipo host y la máquina virtual.

### IDENTIFICADOR de evento 7005

Se detectó un cambio en la configuración de la red de hospedaje, pero no se pudo aplicar porque los datos de configuración de la red de hospedaje no tienen el formato correcto.

<a href="" id="description"></a>**Descripción**  
Se comunicó un cambio en la configuración de la red de hospedaje a la máquina virtual, pero no se pudo procesar en la máquina virtual debido a un error. Este error puede deberse a datos con formato incorrecto o a la incapacidad de establecer la información en la instancia CCMNetworkAdapter de instrumental de administración de Windows (WMI).

<a href="" id="solution"></a>**Solución**  
Reinicie el host y la máquina virtual.

### ConfigMgr (host)

### IDENTIFICADOR de evento 8006

No se puede encontrar la máquina virtual.

<a href="" id="description"></a>**Descripción**  
Windows Virtual PC 7 no puede ubicar la máquina virtual. Es posible que la máquina virtual haya sido eliminada, movida, eliminada o que se haya denegado el acceso.

<a href="" id="solution"></a>**Solución**  
Vuelva a instalar la máquina virtual.

### IDENTIFICADOR de evento 8008

No se pudo recuperar la información de configuración de red de la estación de trabajo.

<a href="" id="description"></a>**Descripción**  
No se pudo recopilar la información de configuración de red del host MED-V, probablemente a causa de un error de llamada del sistema en .NET Framework. Este error también se puede producir si la información de red devuelta desde el host MED-V no se puede escribir en un documento XML.

<a href="" id="solution"></a>**Solución**  
Reinicie la estación de trabajo host.

### IDENTIFICADOR de evento 8010

No se pudieron establecer los datos de configuración de red en la máquina virtual.

<a href="" id="description"></a>**Descripción**  
La traducción de direcciones hostnetwork (NAT) MED-V no se pudo comunicar a la máquina virtual, probablemente porque la máquina virtual se encuentra en mal estado o no se instalaron o habilitaron las adiciones de Virtual PC de Windows.

<a href="" id="solution"></a>**Solución**  
Apague y reinicie la máquina virtual. Además, es posible que tenga que volver a instalar la máquina virtual.

### IDENTIFICADOR de evento 8011

No se pudieron restablecer los datos de configuración de red en la máquina virtual.

<a href="" id="description"></a>**Descripción**  
La configuración hostnetwork de MED-V (puente) no se pudo comunicar a la máquina virtual, probablemente porque la máquina virtual se encuentra en estado incorrecto o no se instalaron o habilitaron las adiciones de Virtual PC de Windows.

<a href="" id="solution"></a>**Solución**  
Apague y reinicie la máquina virtual. Además, es posible que tenga que volver a instalar la máquina virtual.

### Redirección de impresora

### IDENTIFICADOR de evento 9001

Error de permisos de archivo.

<a href="" id="description"></a>**Descripción**  
El usuario final no tiene autorización para acceder a la carpeta requerida para abrir o crear el archivo de impresora MED-V para leerlo.

<a href="" id="solution"></a>**Solución**  
Compruebe que se puede tener acceso a la ruta de User\\AppData\\ y que el usuario tiene permiso para leer y escribir en ella. Por ejemplo, si el usuario es "Matt", la ruta de acceso C:\\Users\\Matt\\AppData\\ y todos los archivos que contenga deben tener permisos de lectura y escritura. Y, si existe, la ruta de acceso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ y todos los archivos que allí deberían tener permisos de lectura y escritura.

### IDENTIFICADOR de evento 9002

Error de permisos de archivo.

<a href="" id="description"></a>**Descripción**  
El usuario final no tiene autorización para acceder a la carpeta requerida para abrir o crear el archivo de impresora MED-V para escritura.

<a href="" id="solution"></a>**Solución**  
Asegúrese de que se puede acceder a la ruta de User\\AppData\\ y de que el usuario tiene permiso para leer y escribir en ella. Por ejemplo, si el usuario es "Matt", la ruta de acceso C:\\Users\\Matt\\AppData\\ y todos los archivos que contenga deben tener permisos de lectura y escritura. Y, si existe, la ruta de acceso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ y todos los archivos que allí deberían tener permisos de lectura y escritura.

### IDENTIFICADOR de evento 9004

No se puede crear la ruta para almacenar archivos de impresora MEDV.

<a href="" id="description"></a>**Descripción**  
El servicio de redirección de impresoras no pudo acceder a los archivos o crear directorios necesarios para almacenar la información de la impresora.

<a href="" id="solution"></a>**Solución**  
Compruebe que se puede tener acceso a la ruta de User\\AppData\\ y que el usuario tiene permiso para leer y escribir en ella. Por ejemplo, si el usuario es "Matt", la ruta de acceso C:\\Users\\Matt\\AppData\\ y todos los archivos que contenga deben tener permisos de lectura y escritura. Y, si existe, la ruta de acceso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ y todos los archivos que allí deberían tener permisos de lectura y escritura.

### IDENTIFICADOR de evento 9005

No se puede obtener el nombre de la VM de la configuración; no se puede iniciar el instalador invitado. No se puede actualizar MED-V: no se detectó ninguna red de host.

<a href="" id="description"></a>**Descripción**  
El servicio de redirección de impresoras no pudo obtener el nombre del área de trabajo de MED-V de la configuración de MED-V y no puede notificar al equipo virtual de Windows que inicie el instalador en el invitado MED-V.

<a href="" id="solution"></a>**Solución**  
Asegúrese de que el nombre del área de trabajo MED-V está establecido y que coincide con el nombre de una máquina virtual en el directorio C:\\Users\\ de \\Virtual de &lt; *usuario*de &gt; equipos. El nombre del área de trabajo MED-V se encuentra en HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Por ejemplo, si el usuario es "Matt" y el nombre del área de trabajo es "mattsworkspace", el valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name debe ser "mattsworkspace" y debe haber un archivo denominado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.VCMX.

### Publicación de aplicaciones

### IDENTIFICADOR de evento 10015

Se produjo un error en el sistema de archivos durante el proceso de conciliación. El proceso de conciliación no procesará el nombre de archivo, &lt; *filename* &gt; pero continuará procesando cualquier otro cambio.

<a href="" id="description"></a>**Descripción**  
Se produjo un error de e/s o de acceso no autorizado al crear o eliminar un acceso directo.

<a href="" id="solution"></a>**Solución**  
Compruebe que se puede tener acceso a la ruta de acceso del archivo y que el usuario tiene permisos para crear o eliminar el archivo especificado.

### IDENTIFICADOR de evento 10021

Error &lt; *\ _information* &gt; para la operación de operación de archivo &lt; *\ _name* &gt; en el nombre de archivo &lt; *filename* &gt; .

<a href="" id="description"></a>**Descripción**  
Se produjo un error de e/s o de acceso no autorizado al crear o eliminar un acceso directo.

<a href="" id="solution"></a>**Solución**  
Compruebe que se puede tener acceso a la ruta de acceso del archivo y que el usuario tiene permisos para crear o eliminar el archivo especificado.

### Revisiones de invitados

### IDENTIFICADOR de evento 11001

Mensaje de uso de la tarea de activación del invitado.

<a href="" id="description"></a>**Descripción**  
MedvHost.exe con la opción/GuestWakeup se ejecutó incorrectamente o el comando no tiene el formato correcto.

<a href="" id="solution"></a>**Solución**  
Asegúrese de que el comando se ejecuta con el siguiente formato:

Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *Workspace \ _name* &gt; " donde

&lt;*Duration \ _in \ _minutes* &gt; es el número de minutos que la máquina virtual debe permanecer en activo (el valor predeterminado es 240) y

&lt;*área de trabajo \ _name* &gt; es el nombre de la máquina virtual que se debe reactivar.

### IDENTIFICADOR de evento 11002

No se puede actualizar MED-V: no se detectó ninguna red de host.

<a href="" id="description"></a>**Descripción**  
No se pudo completar la revisión de invitados porque no se detectó ninguna conexión de red de host.

<a href="" id="solution"></a>**Solución**  
Conecte el host MED-V a una conexión de red activa antes de ejecutar la revisión de invitados.

### IDENTIFICADOR de evento 11003

No se puede actualizar MED-V – el host no se está ejecutando en el/C powerFailed para crear el servidor de canalización.

<a href="" id="description"></a>**Descripción**  
No se pudo completar la revisión de invitados porque el host parece estar funcionando con batería en lugar de un cable de alimentación.

<a href="" id="solution"></a>**Solución**  
Conecte el equipo host a un cable de alimentación antes de ejecutar la revisión de invitados.

### UX de cliente

### IDENTIFICADOR de evento 14003

El siguiente mensaje de estado de la bandeja era demasiado largo y no se pudo mostrar: &lt; *bandeja \ _status \ _message*&gt;

<a href="" id="description"></a>**Descripción**  
MED-V creó una cadena inesperada demasiado larga para la información sobre herramientas de la bandeja o el mensaje del globo. Como resultado, se truncó el mensaje que se muestra.

<a href="" id="solution"></a>**Solución**  
Se trata de un error poco frecuente que puede ocurrir cuando MED-V está creando de forma aleatoria el texto de información sobre herramientas. No hay ninguna solución.

### IDENTIFICADOR de evento 14004

MED-V detenidas debido a una excepción no controlada.

<a href="" id="description"></a>**Descripción**  
Una excepción no controlada hizo que MED-V se detuviera de forma inesperada.

<a href="" id="solution"></a>**Solución**  
Reinicie MED-V.

### IDENTIFICADOR de evento 14005

El servidor ha intentado crear una exclusión mutua, pero ya existía.

<a href="" id="description"></a>**Descripción**  
Una segunda instancia de MedvHost.exe se bloquea en la memoria.

<a href="" id="solution"></a>**Solución**  
Abra TaskManager y finalice todos los procesos de MedvHost.exe.

### IDENTIFICADOR de evento 14006

Error al modificar o eliminar registro de valores de registro &lt; *\ _value* &gt; .

<a href="" id="description"></a>**Descripción**  
MED-V no puede modificar la entrada especificada en el registro.

<a href="" id="solution"></a>**Solución**  
Asegúrese de instalar o desinstalar MED-V con credenciales administrativas.

### IDENTIFICADOR de evento 14007

El archivo especificado ( &lt; *filename* &gt; ) no es válido.

<a href="" id="description"></a>**Descripción**  
Durante la instalación o desinstalación, se pasó un archivo temporal dañado al host MED-V.

<a href="" id="solution"></a>**Solución**  
Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.

### IDENTIFICADOR de evento 14008

Archivo no encontrado: &lt; *nombre*de archivo &gt; .

<a href="" id="description"></a>**Descripción**  
Durante la instalación o desinstalación, no se encontró una ruta de acceso al archivo temporal requerido.

<a href="" id="solution"></a>**Solución**  
Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V.

### IDENTIFICADOR de evento 14009

No se puede leer el nombre de archivo del parámetro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descripción**  
Durante el proceso de instalación o desinstalación, MED-V no pudo leer un archivo temporal.

<a href="" id="solution"></a>**Solución**  
Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V. Además, compruebe que el usuario tiene los derechos y permisos necesarios para la carpeta Temp.

### IDENTIFICADOR de evento 14010

Error al deserializar el nombre de archivo del parámetro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descripción**  
Durante el proceso de instalación o desinstalación, MED-V encontró un archivo temporal dañado.

<a href="" id="solution"></a>**Solución**  
Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V. Además, compruebe que el usuario tiene los derechos y permisos necesarios para la carpeta Temp.

### IDENTIFICADOR de evento 14011

Error inesperado al deserializar el nombre de archivo del parámetro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descripción**  
Durante el proceso de instalación o desinstalación, MED-V encontró un archivo temporal dañado.

<a href="" id="solution"></a>**Solución**  
Elimine todos los archivos de la carpeta Temp y reinstale o desinstale MED-V. Además, compruebe que el usuario tiene los derechos y permisos necesarios para la carpeta Temp.

### IDENTIFICADOR de evento 14012

Error inesperado al configurar los derechos de la &lt; *carpeta \ _name* &gt; de usuario para el nombre de usuario &lt; *username* &gt; .

<a href="" id="description"></a>**Descripción**  
Se produce un error cuando MED-V no puede establecer derechos ni permisos en determinadas carpetas durante la instalación.

<a href="" id="solution"></a>**Solución**  
Compruebe los derechos de administrador en las carpetas siguientes:

@"%ProgramData%\\Microsoft\\Medv\\AllUsers"

@"%ProgramData%\\Microsoft\\Medv\\MedvLock"

@"%ProgramData%\\Microsoft\\Medv\\Monitoring"

### IDENTIFICADOR de evento 14013

Error inesperado al crear el archivo de bloqueo.

<a href="" id="description"></a>**Descripción**  
Se produce un error cuando MED-V no puede crear un archivo en la carpeta @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" durante la instalación.

<a href="" id="solution"></a>**Solución**  
Compruebe los derechos de administrador en la carpeta MedvLock.

## Temas relacionados


[Solución de problemas de MED-V](troubleshooting-med-vmedv2.md)

 

 





