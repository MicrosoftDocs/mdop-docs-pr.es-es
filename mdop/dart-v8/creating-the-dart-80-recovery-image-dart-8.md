---
title: Creación de la imagen para recuperación de DaRT 8.0
description: Creación de la imagen para recuperación de DaRT 8.0
author: dansimp
ms.assetid: 39001b8e-86c0-45ef-8f34-2d6199f9922d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/21/2017
ms.openlocfilehash: 79ce5859e7d0eacf95124c2a7409ff6c21890d65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812551"
---
# Creación de la imagen para recuperación de DaRT 8.0


Después de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, se crea una imagen de recuperación de DaRT 8,0. La imagen de recuperación inicia Windows RE, desde la que puede iniciar las herramientas de DaRT. Puede generar archivos de organización internacional de normalización (ISO) e imágenes de formato de imágenes de Windows (WIM). Además, puede usar PowerShell para generar scripts que usen la configuración que seleccione en el Asistente de imagen de recuperación de DaRT. Puede usar la secuencia de comandos más adelante para reconstruir las imágenes de recuperación con la misma configuración. La imagen de recuperación ofrece una variedad de herramientas de recuperación. Para obtener una descripción de las herramientas, consulte [información general sobre las herramientas de DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

Después de arrancar el equipo en DaRT, puede ejecutar las diferentes herramientas de DaRT para intentar diagnosticar y reparar el equipo. Esta sección le guiará a través del proceso de creación de la imagen de recuperación de DaRT y le permitirá seleccionar las herramientas y características que desea incluir como parte de la imagen.

Puede crear la imagen de recuperación de DaRT con cualquiera de estos dos métodos:

-   Use el Asistente de imagen de recuperación de DaRT, que se ejecuta en un entorno Windows.

-   Modifique un script de PowerShell de ejemplo con los valores que desee. Para obtener más información, vea [Cómo usar un script de PowerShell para crear la imagen de recuperación](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).

Puede escribir la ISO en un CD o DVD grabable, guardarla en una unidad flash USB o guardarla en un formato que pueda usar para arrancar en DaRT desde una partición remota o desde una partición de recuperación.

Una vez que haya creado la imagen ISO, puede grabarla en un CD o DVD en blanco (si su equipo tiene una unidad de CD o DVD). Si su equipo no tiene una unidad para este propósito, puede usar la mayoría de los programas genéricos que se usan para grabar CDs o DVDs.

## Seleccione la arquitectura de la imagen y especifique la ruta de acceso


En la página multimedia de Windows 8, seleccione si desea crear una imagen de recuperación de DaRT de 32 bits o de 64 bits. Use el Windows de 32 bits para compilar imágenes de recuperación de DaRT de 32 bits y Windows de 64 para crear imágenes de recuperación de DaRT de 64 bits. Puede usar un solo equipo para crear imágenes de recuperación para ambos tipos de arquitectura, pero no puede crear una imagen que funcione en arquitecturas de 32 bits y de 64 bits. También indica la ruta de acceso de los medios de instalación de Windows 8. Elija la arquitectura que coincida con la imagen de recuperación que está creando.

**Para seleccionar la arquitectura de la imagen y especificar la ruta de acceso**

1.  En la página **multimedia de Windows 8** , seleccione una de las siguientes opciones:

    -   Si va a crear una imagen de recuperación para equipos de 64 bits, seleccione **crear imagen de DART x64 (64 bits)**.

    -   Si va a crear una imagen de recuperación de equipos de 32 bits, seleccione **crear imagen de DART x86 (32 bits)**.

2.  En el cuadro **especificar la ruta de acceso raíz del medio de instalación de Windows 8 &lt; 64 &gt; -bit o 32** bits, escriba la ruta de acceso de los archivos de instalación de Windows 8. Use una ruta de acceso que coincida con la arquitectura de la imagen de recuperación que está creando.

3.  Haz clic en **Siguiente**.

## Seleccione las herramientas que desea incluir en la imagen de recuperación


En la página herramientas, puede seleccionar numerosas herramientas para incluirlas en la imagen de recuperación. Estas herramientas estarán disponibles para los usuarios finales cuando inicien en la imagen de DaRT. Sin embargo, si habilita la conectividad remota al crear la imagen de DaRT, todas las herramientas estarán disponibles cuando un trabajador del Departamento de soporte se conecte al equipo del usuario final, independientemente de las herramientas que decida incluir en la imagen.

Para restringir el acceso de los usuarios finales a estas herramientas, pero conservar el acceso completo a las herramientas a través del visor de conexión remota, no seleccione estas herramientas en la página herramientas. Los usuarios finales solo podrán usar la conexión remota y podrán ver, pero no acceder, las herramientas que excluya de la imagen de recuperación.

**Para seleccionar las herramientas que se incluirán en la imagen de recuperación**

1.  En la página **herramientas** , active la casilla situada junto a cada herramienta que desee incluir en la imagen.

2.  Haz clic en **Siguiente**.

## Elegir si desea permitir la conectividad remota por parte de un servicio de asistencia


En la página conexión remota, puede elegir si desea habilitar a un trabajador del Departamento de soporte técnico para que se conecte de forma remota y ejecute las herramientas de DaRT en el equipo de un usuario final. La opción conectividad remota se muestra como una opción disponible en la ventana conjunto de herramientas de diagnóstico y recuperación. Después de que los trabajadores del servicio de asistencia establezcan una conexión remota, podrán ejecutar las herramientas de DaRT en el equipo del usuario final desde una ubicación remota.

**Para elegir si desea permitir la conectividad remota por parte de los trabajadores del servicio de asistencia**

1.  En la página **conexión remota** , active la casilla de verificación **permitir conexiones remotas** para permitir conexiones remotas o desactive la casilla para evitar conexiones remotas.

2.  Si ha desactivado la casilla **permitir conexiones remotas** , haga clic en **siguiente**. En caso contrario, vaya al paso siguiente para continuar con la configuración de la conectividad remota.

3.  Selecciona uno de los motivos siguientes:

    -   Deje que Windows elija un número de puerto abierto.

    -   Especifique el número de puerto. Si selecciona esta opción, escriba un número de puerto comprendido entre 1 y 65535 en el campo que se encuentra debajo de la opción. Este número de puerto se usará al establecer una conexión remota. Le recomendamos que el número de Puerto sea 1024 o superior para minimizar la posibilidad de que se produzca un conflicto.

4.  (Opcional) en el cuadro de mensaje de **bienvenida de conexión remota** , cree un mensaje personalizado que recibirán los usuarios finales cuando establezcan una conexión remota. El mensaje puede tener un máximo de 2048 caracteres.

5.  Haz clic en **Siguiente**.

    Para obtener más información sobre cómo ejecutar las herramientas de DaRT de manera remota, consulte [Cómo recuperar equipos remotos con la imagen de recuperación de DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).

## Agregar drivers a la imagen de recuperación


En la pestaña drivers de la página de opciones avanzadas, puede agregar controladores de dispositivos adicionales que puede que necesite al reparar un equipo. Por lo general, los dispositivos de almacenamiento o de red que Windows 8 no proporciona. Los drivers se instalan cuando se crea la imagen.

**Importante**  Cuando selecciones los drivers que deseas incluir, ten en cuenta que DaRT no admite la conectividad inalámbrica (como Bluetooth o 802.11 a/b/g/n).

 

**Para agregar controladores a la imagen de recuperación**

1.  En la página **Opciones avanzadas** , haga clic en la pestaña **drivers** .

2.  Haz clic en **Agregar**.

3.  Busque el archivo que desea agregar al controlador y, a continuación, haga clic en **abrir**.

    **Nota:**  El fabricante del controlador de almacenamiento o de la red proporciona el archivo de controlador.

     

4.  Repita los pasos 2 y 3 para cada controlador que desee incluir.

5.  Haz clic en **Siguiente**.

## Agregar paquetes opcionales de WinPE a la imagen de recuperación


En la pestaña WinPE de la página Opciones avanzadas, puede agregar paquetes opcionales de WinPE a la imagen de DaRT. Estos paquetes forman parte de Windows ADK, que es un requisito previo de instalación para el Asistente de imagen de recuperación de DaRT. Las herramientas que puede seleccionar son opcionales. Los paquetes necesarios se agregan automáticamente, en función de las herramientas que haya seleccionado en la página herramientas.

También puede especificar el tamaño del espacio de desecho. Espacio de desecho es la cantidad de espacio en disco RAM que se dedica a la ejecución de DaRT. El espacio de desecho es útil en el caso de que el disco duro del usuario final no esté disponible. Si está ejecutando herramientas y drivers adicionales, es posible que desee aumentar el espacio de desecho.

**Para agregar paquetes opcionales de WinPE a la imagen de recuperación**

1.  En la página **Opciones avanzadas** , haga clic en la pestaña **WinPE** .

2.  Active la casilla situada junto a cada paquete que desee incluir en la imagen, o haga clic en la casilla **nombre** para seleccionar todos los paquetes.

3.  En el campo **espacio de desecho** , seleccione la cantidad de espacio en disco RAM que se asignará para la ejecución de DART en caso de que el disco duro del usuario final no esté disponible.

4.  Haz clic en **Siguiente**.

## Agregar las herramientas de depuración para el analizador de bloqueos


Si incluye la herramienta analizador de bloqueo en la imagen ISO, también debe incluir las herramientas de depuración para Windows. En la pestaña analizador de bloqueo de la página Opciones avanzadas, escriba la ruta de las herramientas de depuración de Windows 8, que el analizador de bloqueos usa para analizar los archivos de volcado de memoria. Puede usar las herramientas que se encuentran en el equipo en el que está ejecutando el Asistente para imágenes de recuperación de DaRT, o bien, puede usar las herramientas que se encuentran en el equipo del usuario final. Si decide usar las herramientas en el equipo del usuario final, recuerde que cada equipo que diagnostiqu debe tener instaladas las herramientas de depuración.

Si instaló el kit de desarrollo de software (SDK) de Microsoft Windows o el kit de desarrollo de software de Microsoft Windows (WDK), las herramientas de depuración de Windows 8 se agregan automáticamente a la imagen de recuperación y la ruta de acceso a las herramientas de depuración se rellena automáticamente. Puede cambiar la ruta de las herramientas de depuración de Windows 8 si los archivos se encuentran en una ubicación distinta de la indicada por la ruta de acceso predeterminada del archivo. Un vínculo del asistente le permite descargar e instalar herramientas de depuración para Windows si aún no están instaladas.

Para descargar las herramientas de depuración de Windows, vea [herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=266248). Instale las herramientas de depuración en la ubicación predeterminada.

**Nota:**  El Asistente de DaRT comprueba las herramientas de la `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` clave de registro. Si el valor del registro no está allí, el asistente busca en una de las siguientes ubicaciones, según la arquitectura del sistema:

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x86`

 

**Para agregar las herramientas de depuración del analizador de bloqueos**

1.  En la página **Opciones avanzadas** , haga clic en la pestaña **analizador de bloqueos** .

2.  Faculta Haga clic en **descargar las herramientas de depuración** para descargar las herramientas de depuración para Windows.

3.  Seleccione una de las siguientes opciones:

    -   **Incluya las herramientas de &lt; &gt; depuración de 64 bits o 32 bits de Windows 8**. Si selecciona esta opción, busque y seleccione la ubicación de las herramientas si la ruta de acceso no se muestra.

    -   **Use las herramientas de depuración del sistema que se está depurando**. Si selecciona esta opción, el analizador de bloqueos no funcionará si no se encuentran las herramientas de depuración para Windows en el equipo problemático.

4.  Haz clic en **Siguiente**.

## Agregar definiciones para la herramienta de defender


En la pestaña defender de la página Opciones avanzadas, agregue definiciones, que usa la herramienta de defender para determinar si el software que intenta instalar, ejecutar o cambiar la configuración de un equipo es software no deseado o malintencionado.

**Para agregar definiciones para la herramienta de defender**

1.  En la página **Opciones avanzadas** , haga clic en la pestaña **defender** .

2.  Seleccione una de las siguientes opciones:

    -   **Descargar las definiciones más recientes (recomendado)** : la actualización de definiciones se inicia automáticamente y las definiciones se agregan a la imagen de recuperación de DART. Se recomienda esta opción para ayudarle a evitar casos en los que es posible que las definiciones no estén disponibles. Para descargar las definiciones, debe estar conectado a Internet.

    -   **Descargar las definiciones más adelante** : las definiciones no se incluirán en la imagen de recuperación de DART y tendrá que descargar las definiciones desde el equipo que ejecuta DART.

        Si decide no incluir las definiciones más recientes en la imagen de recuperación o si las definiciones incluidas en la imagen de recuperación ya no son actuales en el momento en que ya está listo para usar defender, obtenga las definiciones más recientes antes de comenzar un examen siguiendo las instrucciones que se proporcionan en defender.

        **Importante**  No puede explorar si no hay definiciones.

         

3.  Haz clic en **Siguiente**.

## Seleccionar los tipos de archivos de imagen de recuperación que se van a crear


En la página crear imagen, elija una carpeta de salida para la imagen de recuperación, escriba un nombre de imagen y seleccione los tipos de archivos de imagen de recuperación de DaRT que desea crear. Durante el proceso de creación de la imagen de recuperación, los archivos de origen de Windows se desempaquetan, los archivos de DaRT se copian en él y la imagen se "vuelve a empaquetar" en los formatos de archivo que seleccione en esta página.

Los tipos de archivo de imagen disponibles son:

-   **Archivo de procesamiento de imágenes de Windows (WIM)** : se usa para implementar DART en un entorno de ejecución de preinicio (PXE) o una partición local.

-   **Archivo de imagen ISO** : se usa para implementar en CD o DVD, o para su uso en máquinas virtuales (VM). El asistente requiere que la imagen ISO tenga una extensión de nombre de archivo. ISO porque la mayoría de los programas que graban un CD o DVD requieren esa extensión. Si no especifica una ubicación diferente, la imagen ISO se crea en el escritorio con el nombre DaRT8. ISO.

-   **Script de PowerShell** : crea una imagen de recuperación de DART con comandos que proporcionan esencialmente las mismas opciones que puede seleccionar con el Asistente para imágenes de recuperación de DART. El script también le permite agregar o cambiar archivos en la imagen de recuperación de DaRT.

Si activa la casilla Editar imagen en esta página, puede personalizar la imagen de recuperación durante el proceso de creación de la imagen. Por ejemplo, puede cambiar el archivo "winpeshl.ini" para crear un orden de inicio personalizado o para agregar herramientas de terceros.

**Para seleccionar los tipos de archivos de imagen de recuperación que desea crear**

1.  En la página **crear imagen** , haga clic en **examinar** para elegir la carpeta de salida del archivo de imagen.

    **Nota:**  El tamaño de la imagen variará en función de las herramientas que seleccione y de los archivos que agregue en el asistente.

     

2.  En el cuadro **nombre de imagen** , escriba un nombre para la imagen de recuperación de DART o acepte el nombre predeterminado, que es DaRT8.

    El asistente crea una subcarpeta en la ruta de acceso de salida por este nombre.

3.  Seleccione los tipos de archivos de imagen que desea crear.

4.  Elija una de las opciones siguientes:

    -   Para cambiar los archivos de la imagen de recuperación antes de crear los archivos de imagen, seleccione la casilla **Editar imagen** y, a continuación, haga clic en **preparar**.

    -   Para crear la imagen de recuperación sin cambiar los archivos, haga clic en **crear**.

5.  

    Haz clic en **Siguiente**.

## Modificar los archivos de imagen de recuperación


Puede editar la imagen de recuperación solo si seleccionó la casilla de verificación Editar imagen en la página crear imagen. Una vez que la imagen de recuperación se haya preparado para editarla, puede Agregar y modificar los archivos de imagen de recuperación antes de crear el medio de inicio. Por ejemplo, puede crear un orden personalizado para el inicio, agregar varias herramientas de terceros, etc.

**Para editar los archivos de imagen de recuperación**

1.  En la página **Editar imagen** , haga clic en **abrir** en el explorador de Windows.

2.  Cree una subcarpeta en la carpeta que aparece en el cuadro de diálogo.

3.  Copie los archivos que desee en la nueva subcarpeta o quite los archivos que no desee.

4.  Haga clic en **crear** para empezar a crear la imagen de recuperación.

## Generar los archivos de imagen de recuperación


En la página generar archivos, se genera la imagen de recuperación de DaRT para los tipos de archivo que seleccionó en la página crear imagen.

**Para generar los archivos de imagen de recuperación**

-   En la página **generar archivos** , haga clic en **siguiente** para generar los archivos de imagen de recuperación.

## Copiar la imagen de recuperación en un CD, DVD o USB


En la página crear medio de arranque, puede copiar el archivo de imagen en un CD, DVD o unidad flash USB (UFD). También puede crear medios de arranque adicionales desde esta página reiniciando el asistente.

**Nota:**  Esta herramienta no admite de forma nativa el entorno de ejecución de inicio previo (PXE) ni la implementación de imágenes locales, ya que requieren herramientas empresariales adicionales, como System Center Configuration Manager Server y Microsoft Development Toolkit.

 

**Para copiar la imagen de recuperación en un CD, DVD o USB**

1.  En la página **crear medio de arranque** , seleccione el archivo ISO que desea copiar.

2.  Inserte un CD, DVD o USB y, a continuación, seleccione la unidad.

    **Nota:**  Si no se reconoce una unidad e instala una nueva unidad, puede hacer clic en **Actualizar** para obligar al asistente a actualizar la lista de unidades disponibles.

     

3.  Haga clic en el botón **crear medio de arranque** .

4.  Para crear otra imagen de recuperación, haga clic en reiniciar o haga clic en **cerrar** si ha terminado de crear todos los elementos multimedia que desea.

## Temas relacionados


[Introducción a las herramientas de DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md)

[Implementación de DaRT 8.0](deploying-dart-80-dart-8.md)

 

 





