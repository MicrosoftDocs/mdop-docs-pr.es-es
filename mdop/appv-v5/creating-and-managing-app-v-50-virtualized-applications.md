---
title: Creación y administración de aplicaciones virtualizadas de App-V 5.0
description: Creación y administración de aplicaciones virtualizadas de App-V 5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814702"
---
# Creación y administración de aplicaciones virtualizadas de App-V 5.0


Después de implementar correctamente el secuenciador de Microsoft Application Virtualization (App-V) 5,0, puede usarlo para supervisar y registrar el proceso de instalación y configuración para que una aplicación se ejecute como una aplicación virtualizada.

**Nota:**  Para obtener más información sobre cómo configurar Microsoft Application Virtualization (App-V) 5,0 secuenciador, procedimientos recomendados de secuencias y un ejemplo de creación y actualización de una aplicación virtual, consulte la [Guía de secuenciación de Microsoft Application virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 secuencias Guide.docx).

 

## Secuenciar una aplicación


Puede usar el secuenciador de aplicaciones-V 5,0 para realizar las siguientes tareas:

-   Cree paquetes virtuales que se puedan implementar en equipos que ejecuten el cliente de App-V 5,0.

-   Actualizar paquetes existentes. Puede expandir un paquete existente en el equipo que ejecuta el secuenciador y, a continuación, actualizar la aplicación para crear una versión más reciente.

-   Editar la información de configuración asociada a un paquete existente. Por ejemplo, puede Agregar un acceso directo o modificar una asociación de tipo de archivo.

    **Nota:**  Debe crear accesos directos y guardarlos en una ubicación de red disponible para permitir la itinerancia. Si se crea un acceso directo y se guarda en una ubicación privada, el paquete debe publicarse localmente en el equipo que ejecuta el cliente de App-V 5,0.

     

-   Convertir paquetes virtuales existentes.

El secuenciador utiliza **% TMP% \ \ Scratch** o **% temp% \ \ Scratch** Directory y el directorio **temp** para almacenar los archivos temporales durante la secuenciación. En el equipo que ejecuta el secuenciador, debe configurar estos directorios con espacio libre en disco equivalente a los requisitos estimados de instalación de la aplicación. La configuración de los directorios temporales y el directorio Temp en distintas particiones del disco duro puede ayudar a mejorar el rendimiento durante la secuenciación.

Al usar el secuenciador para crear una nueva aplicación virtual, se crean los siguientes archivos de la lista. Estos archivos constituyen el paquete de App-V 5,0.

-   archivo. msi. El secuenciador crea este archivo de Windows Installer (. msi) y se usa para instalar el paquete virtual en los equipos de destino.

-   Archivo de Report.xml. En este archivo, el secuenciador guarda todos los problemas, advertencias y errores detectados durante la secuenciación. Muestra la información después de que se haya creado el paquete. Puede obtener este informe para diagnosticar y solucionar problemas.

-   archivo. appv. Este es el archivo de aplicación virtual.

-   Archivo de configuración de implementación. El archivo de configuración de implementación determina cómo se implementará la aplicación virtual en los equipos de destino.

-   Archivo de configuración de usuario. El archivo de configuración de usuario determina cómo se ejecutará la aplicación virtual en los equipos de destino.

**Importante**  Debe configurar las carpetas% TMP% y% TEMP% que el convertidor de paquetes usa para ser una ubicación y un directorio seguros. Un administrador solo puede tener acceso a una ubicación segura. Además, cuando ordene el paquete, debe guardar el paquete en una ubicación segura o asegurarse de que ningún otro usuario pueda iniciar sesión durante el proceso de conversión y supervisión.

 

El cuadro de diálogo **Opciones** en la consola del secuenciador contiene las siguientes pestañas:

-   **General**. Use esta pestaña para habilitar la ejecución de actualizaciones de Microsoft durante la secuenciación. Seleccione **anexar la versión del paquete al nombre del archivo** para configurar la secuencia para agregar un número de versión al paquete virtualizado que se secuencia. Seleccione **confiar siempre en la fuente de aceleradores de paquetes** para crear paquetes virtuales con un acelerador de paquetes sin que se le pida autorización.

    **Importante**  Los aceleradores de paquetes creados con App-V 4.6 no son compatibles con App-V 5,0.

     

-   **Elementos de análisis**. Esta pestaña muestra las ubicaciones de la ruta de acceso de los archivos asociada que se analizarán o se convertirán en token en en el entorno virtual. Los tokens son útiles para agregar archivos mediante la pestaña **archivos del paquete** en la **Edición avanzada**.

-   **Elementos de exclusión**. Use esta pestaña para especificar qué carpetas y directorios no se deben supervisar durante la secuenciación. Para agregar datos de la aplicación local que se guardan en la carpeta de datos de la aplicación local en el paquete, haga clic en **nuevo** y especifique la ubicación y el **tipo de asignación**asociada. Esta opción es necesaria para algunos paquetes.

App-V 5,0 admite aplicaciones que incluyen servicios de Microsoft Windows. Si una aplicación incluye un servicio de Windows, el servicio se incluirá en el paquete virtual secuencial siempre que esté instalado mientras lo supervisa el secuenciador. Si una aplicación virtual crea un servicio de Windows cuando se ejecuta por primera vez, después de la instalación, la aplicación debe ejecutarse mientras el secuenciador está supervisando para que el servicio de Windows se agregue al paquete. Solo se admiten los servicios que se ejecutan en la cuenta del sistema local. Los servicios que están configurados para AutoStart o AutoStart retardado se inician antes de que la primera aplicación virtual de un paquete se ejecute dentro del entorno virtual del paquete. Los servicios de Windows que están configurados para iniciarse a petición de una aplicación se inician cuando la aplicación virtual dentro del paquete inicia el servicio mediante una llamada de API.

[Cómo secuenciar una nueva aplicación con App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> Compatibilidad con la extensión Shell de App-V 5.0 SP2


App-V 5.0 SP2 admite extensiones de Shell. Las extensiones de Shell se detectarán e incrustarán en el paquete durante la secuenciación.

Las extensiones de Shell se incrustan automáticamente en el paquete durante el proceso de secuenciación. Cuando se publica el paquete, la extensión de Shell proporciona a los usuarios la misma funcionalidad que si la aplicación se instalara de forma local.

**Requisitos para usar extensiones de Shell:**

-   Los paquetes que contienen extensiones de Shell insertadas deben publicarse globalmente. La aplicación no requiere ninguna configuración ni configuración adicional en el cliente para habilitar la funcionalidad de la extensión de Shell.

-   El "bits" de la aplicación, el secuenciador y el cliente de App-V deben coincidir, o las extensiones de Shell no funcionarán. Por ejemplo:

    -   La versión de la aplicación es 64 bits.

    -   El secuenciador se está ejecutando en un equipo de 64 bits.

    -   El paquete se está entregando a un equipo cliente de aplicación de 64 bits de-V.

En la siguiente tabla se enumeran las extensiones de Shell compatibles:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Administrador</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controlador del menú contextual</p></td>
<td align="left"><p>Agrega elementos de menú al menú contextual. Se llama antes de mostrar el menú contextual.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de arrastrar y colocar</p></td>
<td align="left"><p>Controla la acción en la que se hace clic con el botón derecho, arrastra y coloca y modifica el menú contextual que aparece.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de destino de colocación</p></td>
<td align="left"><p>Controla la acción después de arrastrar un objeto de datos y colocarlo sobre un destino de colocación, como un archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de objetos de datos</p></td>
<td align="left"><p>Controla la acción después de copiar un archivo en el portapapeles o arrastrarlo y colocarlo sobre un destino. Puede proporcionar formatos adicionales del portapapeles para el destino de colocación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de hoja de propiedades</p></td>
<td align="left"><p>Reemplaza o agrega páginas al cuadro de diálogo de la hoja de propiedades de un objeto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de insugerencias</p></td>
<td align="left"><p>Permite recuperar indicadores y información de recuadro de sugerencias para un elemento y mostrarlo dentro de una información emergente al pasar el mouse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de columnas</p></td>
<td align="left"><p>Permite crear y mostrar columnas personalizadas en la <strong> vista de detalles del explorador de Windows </strong> . Puede usarse para ampliar la ordenación y la agrupación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de vista previa</p></td>
<td align="left"><p>Habilita una vista previa de un archivo para que se muestre en el panel de vista previa del explorador de Windows.</p></td>
</tr>
</tbody>
</table>

 

## Compatibilidad con la extensión de archivo de copia en escritura (CoW)


Las extensiones de archivo de copia en escritura (CoW) permiten que App-V 5,0 se escriba dinámicamente en ubicaciones específicas del paquete virtual mientras se está usando.

En la siguiente tabla se muestran los tipos de archivo que pueden existir en un paquete virtual en el directorio VFS, pero que no se pueden actualizar en el equipo que ejecuta el cliente de App-V 5,0. Se pueden modificar todos los demás archivos y directorios.

. ACM

. asa

.asp

. aspx

. AX

.bat

.cer

.chm

. CLB

.cmd

.cnt

. CNV

.com

.cpl

.cpx

.crt

.dll

.drv

.exe

.fon

.grp

.hlp

.hta

. IME

.inf

.ins

.isp

. su

.js

.jse

.lnk

.msc

.msi

.msp

.mst

. MUI

. NLS

.ocx

. PAL

.pcd

.pif

.reg

.scf

.scr

. SCT

.shb

.shs

.sys

. tlb

. TSP

.url

.vb

.vbe

.vbs

.vsmacros

.ws

. ESC

.wsf

.wsh

 

## Modificar un paquete de aplicación virtual existente


Puede usar el secuenciador para modificar un paquete existente. El equipo en el que realiza esta acción debe coincidir con la arquitectura de chip del equipo que usó para crear la aplicación. Por ejemplo, si inicialmente ha secuenciado un paquete con un equipo que ejecuta un sistema operativo de 64 bits, debe modificar el paquete con un equipo que ejecute un sistema operativo de 64 bits.

[Cómo modificar un paquete de aplicaciones virtuales existentes](how-to-modify-an-existing-virtual-application-package-beta.md)

## Crear una plantilla de proyecto


Un archivo. appvt es una plantilla de proyecto que se puede usar para guardar la configuración personalizada más frecuentemente. Puede usar esta configuración más fácilmente para futuras secuencias.

Las plantillas de proyecto de App-V 5,0 difieren de los aceleradores de aplicaciones de App-V 5,0 porque los aceleradores de aplicaciones de App-V 5,0 son específicos de la aplicación y las plantillas de proyecto de App-V 5,0 se pueden aplicar a varias aplicaciones. Además, no puede usar una plantilla de proyecto cuando usa un acelerador de paquetes para crear un paquete de aplicaciones virtual. La siguiente configuración general se guarda con una plantilla de proyecto de App-V 5,0:

Una plantilla puede especificar y almacenar varias opciones de configuración de la siguiente manera:

-   **Opciones de supervisión avanzadas**. Permite que Microsoft Update se ejecute durante la supervisión. Guarda la configuración de la opción permitir interacción local

-   **Opciones generales**. Permite usar **Windows Installer**, **anexar la versión del paquete al nombre de archivo**.

-   **Elementos de exclusión.** Contiene la lista de patrones de exclusión.

[Cómo crear y usar una plantilla de proyecto](how-to-create-and-use-a-project-template.md)

## Crear un acelerador de paquetes


**Nota:**  Los aceleradores de paquetes creados con una versión anterior de App-V deben volver a crearse con App-V 5,0.

 

Puede usar los aceleradores de paquetes de App-V 5,0 para generar automáticamente nuevos paquetes de aplicaciones virtuales. Después de crear correctamente un acelerador de paquetes, puede volver a usar y compartir el acelerador de paquetes.

En algunas situaciones, para crear el acelerador de paquetes es posible que tenga que instalar la aplicación de forma local en el equipo que ejecuta el secuenciador. En tal caso, primero debe intentar crear el acelerador de paquetes con los medios de instalación. Si se necesitan varios archivos que faltan, debe instalar la aplicación localmente en el equipo que ejecuta el secuenciador y, a continuación, crear el acelerador de paquetes.

Después de crear correctamente un acelerador de paquetes, puede volver a usar y compartir el acelerador de paquetes. La creación de aceleradores de paquetes de App-V 5,0 es una tarea avanzada. Los aceleradores de paquetes pueden contener contraseña e información específica del usuario. Por lo tanto, debe guardar los aceleradores de paquetes y los medios de instalación asociados en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes de App-V 5,0.

[Cómo crear un acelerador de paquetes](how-to-create-a-package-accelerator.md)

[Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## Informe de errores de secuenciador


El secuenciador de 5,0 de App-V puede detectar problemas de secuencia comunes durante la secuencia. La página del **Informe de instalación** al final del asistente de secuenciación muestra mensajes de diagnóstico clasificados en **errores**, **advertencias**e **información** , según la gravedad del problema.

También puede encontrar información adicional sobre errores de secuenciación con el visor de eventos de Windows.






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a>Otros recursos para el secuenciador de aplicaciones-V 5,0


-   [Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





