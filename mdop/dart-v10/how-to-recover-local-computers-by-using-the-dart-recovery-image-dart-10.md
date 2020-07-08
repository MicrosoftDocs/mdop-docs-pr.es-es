---
title: Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT
description: Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822590"
---
# Cómo recuperar equipos locales mediante el uso de la imagen para recuperación de DaRT


Siga estas instrucciones para recuperar un equipo cuando esté físicamente presente en el equipo del usuario final que tiene problemas.

**Cómo recuperar un equipo local mediante la imagen de recuperación de DaRT**

1.  Inicie el equipo del usuario final con la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

    Mientras se inicia el equipo en la imagen de recuperación de DaRT 10, aparece el cuadro de diálogo **netstart** .

2.  Cuando se le pregunte si desea inicializar los servicios de red, seleccione una de las opciones siguientes:

    **Sí** : se supone que un servidor DHCP está presente en la red y se intenta obtener una dirección IP del servidor. Si la red usa direcciones IP estáticas en lugar de DHCP, puede usar posteriormente la herramienta de **configuración TCP/IP** en DART para especificar una dirección IP estática.

    **No** , omitir el proceso de inicialización de red.

3.  Indique si desea volver a asignar las letras de unidad. Cuando se ejecuta Windows online, el volumen del sistema suele asignarse a la unidad C. Sin embargo, cuando ejecuta Windows sin conexión en WinRE, es posible que el volumen del sistema original se asigne a otra unidad y esto puede causar confusión. Si decide reasignar, DaRT intenta asignar las letras de unidad sin conexión para que coincidan con las letras de unidad en línea. La reasignación se realiza solo si se selecciona un sistema operativo sin conexión más adelante en el proceso de inicio.

4.  En el cuadro de diálogo **Opciones de recuperación del sistema** , seleccione una distribución de teclado.

5.  Compruebe el directorio raíz del sistema que se muestra, el tipo de sistema operativo instalado y el tamaño de la partición. Si no ve su sistema operativo en la lista y sospecha que la falta de drivers es una posible causa del error, haga clic en **cargar drivers** para cargar los drivers sospechosos y, a continuación, inserte los medios de instalación para el dispositivo y seleccione el controlador.

6.  Seleccione la instalación que desea reparar o diagnosticar y, a continuación, haga clic en **siguiente**.

    **Nota**  
    Si el entorno de recuperación de Windows (WinRE) detecta o sospecha que Windows 10 no se inició correctamente la última vez que se intentó, **reparación de inicio** puede empezar a ejecutarse automáticamente.



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. En la ventana **Opciones de recuperación del sistema** , haga clic en **Microsoft Diagnostics and Recovery Toolset**.

   Se abrirá la ventana **conjunto de herramientas de diagnóstico y recuperación** . Ahora puede ejecutar cualquiera de las herramientas o asistentes individuales que se incluyeron cuando se creó la imagen de recuperación de DaRT.

Puede hacer clic en **ayuda** en la ventana **conjunto de herramientas de diagnósticos y recuperación** para abrir el archivo de ayuda del cliente que proporciona instrucciones detalladas e información necesaria para ejecutar las herramientas de DART individuales. También puede hacer clic en el **Asistente para soluciones** en la ventana conjunto de herramientas de **diagnóstico y recuperación** para elegir la mejor herramienta para la situación, en función de una breve entrevista que proporciona el asistente.

Para obtener información general sobre cualquiera de las herramientas de DaRT, consulte [información general sobre las herramientas de DART 10](overview-of-the-tools-in-dart-10.md).

**Cómo ejecutar DaRT en el símbolo del sistema**

- Para ejecutar DaRT en el símbolo del sistema, especifique el comando **netstart.exe** y, a continuación, use cualquiera de los siguientes parámetros:

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong>Parámetro</strong></p></td>
  <td align="left"><p><strong>Descripción</strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-red</p></td>
  <td align="left"><p>Inicializa los servicios de red.</p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p>-volver a montar</p></td>
  <td align="left"><p>Reasigna las letras de unidad.</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-prompt</p></td>
  <td align="left"><p>Muestra mensajes que piden al usuario final que especifique si desea inicializar la red y reasignar las unidades.</p>
  <div class="alert">
  <strong>Advertencia</strong><br/><p>La respuesta del usuario final a la solicitud reemplaza los modificadores – Network y-Mount.</p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## Temas relacionados


[Operaciones para DaRT 10](operations-for-dart-10.md)

[Equipos de recuperación que usan DaRT 10](recovering-computers-using-dart-10.md)









