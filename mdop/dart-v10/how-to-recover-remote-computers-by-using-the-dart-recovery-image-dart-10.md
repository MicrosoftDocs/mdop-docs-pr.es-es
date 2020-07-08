---
title: Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT
description: Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT
author: dansimp
ms.assetid: c0062208-39cd-4e01-adf8-36a11386e2ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 42d49c6c5c494da866785764e1c93a6bda2d667e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822591"
---
# Cómo recuperar equipos remotos mediante el uso de la imagen para recuperación de DaRT


Use la característica de conexión remota de Microsoft Diagnostics and Recovery Toolset (DaRT) 10 para ejecutar las herramientas de DaRT de forma remota en un equipo de usuario final. Una vez que el usuario final proporciona a un administrador o a un trabajador del servicio de asistencia información, el administrador de ti o el trabajador del servicio de asistencia pueden tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.

Si ha deshabilitado las herramientas de DaRT al crear la imagen de recuperación, aún tiene acceso a todas las herramientas. Todas las herramientas, excepto la conexión remota, no están disponibles para los usuarios finales.

**Para recuperar un equipo remoto con la imagen de recuperación de DaRT**

1.  Inicie un equipo de usuario final con la imagen de recuperación de DaRT.

    Por lo general, puede usar uno de los siguientes métodos para arrancar DaRT y recuperar un equipo remoto, en función de cómo implemente la imagen de recuperación de DaRT. Para obtener más información sobre la implementación de la imagen de recuperación de DaRT, consulte [implementación de DART 10](deploying-dart-10.md).

    -   Inicie DaRT desde una partición de recuperación en el equipo con problemas.

    -   Inicie en DaRT desde una partición remota en la red.

    Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).

    Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.

    **Nota**  
    La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. Cuando se le pregunte si desea inicializar los servicios de red, seleccione una de las opciones siguientes:

   **Sí** : se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor. Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.

   **No** , omitir el proceso de inicialización de red.

3. Indique si desea volver a asignar las letras de unidad. Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión. Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea. La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.

4. En el cuadro de diálogo **Opciones de recuperación del sistema** , seleccione una distribución de teclado.

5. Compruebe el directorio raíz del sistema que se muestra, el tipo de sistema operativo instalado y el tamaño de la partición. Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos y, a continuación, inserte los medios de instalación para el dispositivo y seleccione el controlador.

6. Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.

   **Nota**  
   Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 10 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente. Para obtener más información sobre cómo resolver este problema, consulte [solución de problemas de DART 10](troubleshooting-dart-10.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. En la ventana **Opciones de recuperación del sistema** , haga clic en **Microsoft Diagnostics and Recovery Toolset** para abrir el **conjunto de herramientas de diagnóstico y recuperación**.

8. En la ventana **conjunto de herramientas de diagnóstico y recuperación** , haga clic en **conexión remota** para abrir la ventana **conexión remota de DART** . Si se le pide que proporcione el acceso remoto del Departamento de soporte técnico, haga clic en **Aceptar**.

   Se abrirá la ventana conexión remota de DaRT, que muestra un número de ticket, una dirección IP e información de puerto.

9. En el equipo de asistencia, abra el **visor de conexión remota de DART**.

10. Haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft DART 10**y, a continuación, haga clic en **visor de conexión remota DART**.

11. En la ventana **conexión remota de DART** , escriba el vale, la dirección IP y la información del puerto que desee.

   **Nota**  
   Esta información se crea en el equipo del usuario final y debe ser proporcionada por el usuario final. Es posible que haya varias direcciones IP para elegir, en función de cuántos estén disponibles en el equipo del usuario final.



12. Haz clic en **Connect**.

El administrador de TI ahora asume el control del equipo de usuario final y puede ejecutar las herramientas de DaRT de forma remota.

**Nota**  
Se proporciona un archivo que se denomina inv32.xml y contiene información de conexión remota, como el número de puerto y la dirección IP. De forma predeterminada, el archivo suele encontrarse en%WINDIR%\\system32.



**Para personalizar el proceso de conexión remota**

1. Puede personalizar el proceso de conexión remota editando el archivo winpeshl.ini. Para obtener más información sobre cómo editar el archivo de winpeshl.ini, consulte [Winpeshl.ini archivos](https://go.microsoft.com/fwlink/?LinkId=219413).

   Especifique los siguientes comandos y parámetros para personalizar cómo se establece una conexión remota con un equipo de usuario final:

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Comando</th>
   <th align="left">Parámetro</th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>RemoteRecovery.exe</strong></p></td>
   <td align="left"><p>-nomessage</p></td>
   <td align="left"><p>Especifica que no se muestre la pregunta de confirmación. <strong>La conexión remota </strong> continúa como si el usuario final hubiera respondido &quot; afirmativamente &quot; a la pregunta de confirmación.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>WaitForConnection.exe</strong></p></td>
   <td align="left"><p>ninguno</p></td>
   <td align="left"><p>Impide que un script personalizado continúe hasta que <strong> no se esté ejecutando una conexión remota </strong> o se haya establecido una conexión válida con el equipo del usuario final.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Este comando no funciona si se especifica de forma independiente. Debe especificarse en un script para funcionar correctamente.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Este es un ejemplo de un archivo de winpeshl.ini que se personaliza para abrir la herramienta de **conexión remota** tan pronto como se intente iniciar en DART:

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

Cuando se inicia DaRT, crea el archivo inv32.xml en \\Windows\\System32\\ en el disco RAM. Este archivo contiene información de conexión: dirección IP, puerto y número de incidencia. Puede copiar este archivo en un recurso compartido de red para desencadenar un flujo de trabajo de asistencia. Por ejemplo, un programa personalizado puede comprobar el recurso compartido de red para los archivos de conexión y, después, crear una incidencia de soporte técnico o enviar notificaciones de correo electrónico.

**Para ejecutar el visor de conexión remota en el símbolo del sistema**

1.  Para ejecutar el **visor de conexión remota de DART** en el símbolo del sistema, especifique el comando **DartRemoteViewer.exe** y use los siguientes parámetros:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>-Ticket = &lt; <em> ticketnumber</em>&gt;</p></td>
    <td align="left"><p>Donde &lt; <em> ticketnumber </em> &gt; es el número de la incidencia, incluidos los guiones, que genera la conexión remota.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>-IPAddress = &lt; <em> IPAddress</em>&gt;</p></td>
    <td align="left"><p>Donde &lt; <em> direcciónIP </em> &gt; es la dirección IP generada por la conexión remota.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>-Port = &lt; <em> Puerto</em>&gt;</p></td>
    <td align="left"><p>Donde &lt; <em> Puerto </em> &gt; es el puerto que corresponde a la dirección IP especificada.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. Si se especifican los tres parámetros y los datos son válidos, se intentará inmediatamente una conexión cuando se inicie el programa. Si alguno de los parámetros no es válido, el programa se inicia como si no se hubiera especificado ningún parámetro.

## Temas relacionados


[Operaciones para DaRT 10](operations-for-dart-10.md)

[Equipos de recuperación que usan DaRT 10](recovering-computers-using-dart-10.md)









