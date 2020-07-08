---
title: Cómo recuperar los equipos locales con la imagen para recuperación de DaRT
description: Cómo recuperar los equipos locales con la imagen para recuperación de DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823761"
---
# Cómo recuperar los equipos locales con la imagen para recuperación de DaRT


Para recuperar un equipo local mediante Microsoft Diagnostics and Recovery Toolset (DaRT) 7, debe estar presente físicamente en el equipo del usuario final que está experimentando problemas que requieren DaRT. También puede ejecutar DaRT de manera remota siguiendo las instrucciones que encontrará en [Cómo recuperar equipos remotos con la imagen de recuperación de DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

**Para recuperar un equipo local con DaRT**

1.  Mientras se inicia el equipo en la imagen de recuperación de DaRT, aparece el cuadro de diálogo **netstart** . Se le pregunta si desea inicializar los servicios de red. Si hace clic en **sí**, se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor. Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.

    Para omitir el proceso de inicialización de red, haga clic en **no**.

2.  Siguiendo el cuadro de diálogo inicialización de red, se le preguntará si desea volver a asignar las letras de unidad. Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión. Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea. La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.

3.  Siguiendo el cuadro de diálogo reasignación, aparece un cuadro de diálogo **Opciones de recuperación del sistema** y le pide que seleccione una distribución de teclado. Después, se muestra el directorio raíz del sistema, el tipo de sistema operativo instalado y el tamaño de la partición. Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos. Esto le pedirá que inserte los medios de instalación para el dispositivo y que seleccione el controlador. Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.

    **Nota**  
    Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 7 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente.



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. En la ventana **Opciones de recuperación del sistema** , haga clic en **Microsoft Diagnostics and Recovery Toolset**.

   Se abrirá la ventana **conjunto de herramientas de diagnóstico y recuperación** . Ahora puede ejecutar cualquiera de las herramientas o asistentes individuales que se incluyeron cuando se creó la imagen de recuperación de DaRT.

Puede hacer clic en **ayuda** en la ventana **conjunto de herramientas de diagnósticos y recuperación** para abrir el archivo de ayuda del cliente que proporciona instrucciones detalladas e información necesaria para ejecutar las herramientas de DART individuales. También puede hacer clic en el **Asistente para soluciones** en la ventana conjunto de herramientas de **diagnóstico y recuperación** para elegir la mejor herramienta para la situación, en función de una breve entrevista que proporciona el asistente.

Para obtener información general sobre cualquiera de las herramientas de DaRT, consulte [información general sobre las herramientas de dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

**Para ejecutar DaRT en el símbolo del sistema**

1. Puede ejecutar DaRT en el símbolo del sistema especificando el comando **netstart.exe** y utilizando cualquiera de los siguientes parámetros:

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
   <td align="left"><p>-red</p></td>
   <td align="left"><p>Inicializa los servicios de red.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>-volver a montar</p></td>
   <td align="left"><p>Reasigna las letras de unidad.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>-prompt</p></td>
   <td align="left"><p>Muestra mensajes que piden al usuario final que especifique si desea inicializar la red y reasignar las unidades.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>La respuesta del usuario final a las preguntas reemplaza a los modificadores-Network y-remount.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Puede personalizar DaRT para que un equipo que inicie en DaRT abra automáticamente la herramienta de **conexión remota** que se usa para establecer una conexión remota con el Departamento de soporte técnico.

## Temas relacionados


[Equipos de recuperación que usan DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









