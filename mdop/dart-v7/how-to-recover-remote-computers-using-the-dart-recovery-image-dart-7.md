---
title: Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT
description: Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822791"
---
# Cómo recuperar equipos remotos mediante la imagen para recuperación de DaRT


La característica de conexión remota de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 permite a un administrador de ti ejecutar las herramientas de DaRT de forma remota en un equipo de usuario final. Después de que el usuario final proporcione determinada información (o de un profesional del Departamento de soporte técnico que trabaje en el equipo del usuario final), el administrador de ti o el agente de asistencia pueden tomar el control del equipo del usuario final y ejecutar las herramientas de DaRT necesarias de forma remota.

**Importante**  
Los dos equipos que establecen una conexión remota deben formar parte de la misma red.



**Para recuperar un equipo remoto con DaRT**

1.  Inicie un equipo de usuario final con la imagen de recuperación de DaRT.

    Por lo general, puede usar uno de los siguientes métodos para arrancar DaRT y recuperar un equipo remoto, en función de cómo implemente la imagen de recuperación de DaRT. Para obtener más información sobre la implementación de la imagen de recuperación de DaRT, consulte [implementación de la imagen de recuperación de dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

    -   Inicie DaRT desde una partición de recuperación en el equipo con problemas.

    -   Inicie en DaRT desde una partición remota en la red.

    Para obtener información sobre las ventajas y desventajas de cada método, consulte [planificación cómo guardar e implementar la imagen de recuperación de DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

    Independientemente del método que use para arrancar DaRT, debe habilitar el dispositivo de inicio en el BIOS para la opción de inicio u opciones que desee que estén disponibles para el usuario final.

    **Nota**  
    La configuración del BIOS es única, según el tipo de unidad de disco duro, los adaptadores de red y el hardware que se usa en la organización.



2.  Mientras se inicia el equipo en la imagen de recuperación de DaRT, aparece el cuadro de diálogo **netstart** . Se le pregunta si desea inicializar los servicios de red. Si hace clic en **sí**, se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor. Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.

    Para omitir el proceso de inicialización de red, haga clic en **no**.

3.  Siguiendo el cuadro de diálogo inicialización de red, se le preguntará si desea volver a asignar las letras de unidad. Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión. Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea. La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.

4.  Siguiendo el cuadro de diálogo reasignación, aparece un cuadro de diálogo **Opciones de recuperación del sistema** y le pide que seleccione una distribución de teclado. Después, se muestra el directorio raíz del sistema, el tipo de sistema operativo instalado y el tamaño de la partición. Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos. Esto le pedirá que inserte los medios de instalación para el dispositivo y que seleccione el controlador. Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.

    **Nota**  
    Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 7 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente. Para obtener más información sobre cómo resolver este problema, consulte [solución de problemas de DaRT 7,0](troubleshooting-dart-70-new-ia.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. En la ventana **Opciones de recuperación del sistema** , seleccione **Microsoft Diagnostics and Recovery Toolset** para abrir la ventana **conjunto de herramientas de diagnóstico y recuperación** .

6. En la ventana **conjunto de herramientas de diagnóstico y recuperación** , haga clic en **conexión remota** para abrir la ventana **conexión remota de DART** . Si se le pide que proporcione el acceso remoto del Departamento de soporte técnico, haga clic en **Aceptar**.

   Se abrirá la ventana conexión remota de DaRT, que muestra un número de ticket, una dirección IP e información de puerto.

7. En el equipo agente de asistencia, abra el **visor de conexión remota de DART**.

   Haga clic en **Inicio**, haga clic en **todos los programas**, **Microsoft DART 7**y, a continuación, haga clic en **visor de conexión remota DART**.

8. En la ventana **conexión remota de DART** , escriba el vale, la dirección IP y la información del puerto que desee.

   **Nota**  
   Esta información se crea en el equipo del usuario final y debe ser proporcionada por el usuario final. Es posible que haya varias direcciones IP para elegir, en función de cuántos estén disponibles en el equipo del usuario final.



9. Haz clic en **Connect**.

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

**Para ejecutar el visor de conexión remota en el símbolo del sistema**

1.  Puede ejecutar el **visor de conexión remota de DART** en el símbolo del sistema especificando el comando **DartRemoteViewer.exe** y usando los siguientes parámetros:

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


[Equipos de recuperación que usan DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









