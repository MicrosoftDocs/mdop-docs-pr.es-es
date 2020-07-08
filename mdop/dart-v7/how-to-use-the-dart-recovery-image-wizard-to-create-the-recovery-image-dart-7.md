---
title: Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación
description: Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822921"
---
# Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 incluye el **Asistente de imagen de recuperación de DART** que se usa en Windows para crear una imagen de inicio de la organización internacional para la estandarización (ISO). Una imagen ISO es un archivo que representa el contenido sin formato de un CD.

El **Asistente de imagen de recuperación DART** requiere la siguiente información:

-   **Imagen de arranque**° c debe proporcionar la ruta de acceso de los archivos de origen de Windows 7 DVD o Windows 7 necesarios para crear la imagen de recuperación de DART.

-   **Selección de herramientas**: °, puede seleccionar las herramientas que desea incluir en la imagen de recuperación de DART.

-   **Conexiones remotas**: puede seleccionar si desea que la imagen de recuperación de DART incluya la capacidad de establecer una conexión remota entre el Departamento de soporte técnico y el equipo del usuario final.

-   **Herramientas de depuración para Windows**° c se le pedirá que proporcione la ubicación de las herramientas de depuración para Windows.

-   **Definiciones para el sistema independiente de limpieza**° puede decidir si desea descargar las definiciones más recientes en el momento de crear la imagen de recuperación o descargar las definiciones más adelante.

-   **Drivers**° c se le preguntará si desea agregar drivers a la imagen ISO.

-   **Archivos adicionales**° c puede Agregar archivos a la imagen ISO que pueden ayudar a diagnosticar problemas.

-   **Ubicación de la imagen ISO**: se le solicita que especifique dónde debe ubicarse la imagen ISO.

-   **Unidad de CD/DVD**: todo lo que se le pide que especifique si la unidad de CD o DVD debe usarse para grabar el CD o el DVD.

**Nota:**  El tamaño de la imagen ISO puede variar en función de las herramientas que se seleccionaron en el **Asistente de imagen de recuperación de DART**.

 

## Para crear la imagen de recuperación con el Asistente de imagen de recuperación de DaRT


Siga estas instrucciones para usar el **Asistente de imagen de recuperación de DART** para crear la imagen de recuperación de DART.

### Para seleccionar las herramientas que se incluirán en la imagen de recuperación de DaRT

El **Asistente de imagen de recuperación de DART** presenta un cuadro de diálogo de **selección de herramientas** . Puede seleccionar o quitar herramientas de la lista de herramientas que se van a incluir en la imagen de recuperación de DaRT resaltando una herramienta y, a continuación, haciendo clic en los botones **Habilitar** o **deshabilitar** .

Una vez que haya seleccionado todas las herramientas que desea incluir en la imagen de recuperación, haga clic en **siguiente**.

### Para agregar la opción de permitir la conectividad remota

Puede seleccionar la casilla **permitir conexiones remotas** para proporcionar la opción en la ventana **conjunto de herramientas de diagnóstico y recuperación** para establecer una conexión remota entre el agente de asistencia al cliente y un equipo de usuario final. Después de que un agente de asistencia haya establecido una conexión remota, puede ejecutar las herramientas de DaRT en el equipo del usuario final desde una ubicación remota.

Puede seleccionar la casilla **especificar el número de Puerto** para introducir un número de puerto específico que se usará al establecer una conexión remota. Puede especificar un número de Puerto entre 1 y 65535. Le recomendamos que el número de Puerto sea 1024 o superior para minimizar la posibilidad de que se produzca un conflicto.

También puede crear un mensaje personalizado que recibirá un usuario final al establecer una conexión remota. El mensaje puede tener un máximo de 2048 caracteres.

Para obtener más información sobre la ejecución remota de las herramientas de DaRT, consulte [Cómo recuperar equipos remotos con la imagen de recuperación de DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

### Para agregar las herramientas de depuración para Windows a la imagen de recuperación de DaRT

En el cuadro de diálogo **analizador de bloqueo** del asistente de imágenes de **recuperación de DART**, se le pedirá que especifique la ubicación de las herramientas de depuración para Windows. Si no tiene una copia de las herramientas, puede descargarlas desde Microsoft. En el asistente se proporciona el siguiente vínculo a la página de descarga: [Descargar e instalar herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

Puede especificar la ubicación de las herramientas de depuración en el equipo en el que está ejecutando el **Asistente para imágenes de recuperación de DART**, o bien, puede optar por usar las herramientas que se encuentran en el equipo de destino. Si decide usar una copia en otro equipo, debe asegurarse de que las herramientas estén instaladas en cada uno de los equipos en los que esté diagnosticando un bloqueo.

**Nota:**  Si incluye el **analizador de bloqueos** en la imagen ISO, le recomendamos que también incluya las herramientas de depuración para Windows.

 

Siga estos pasos para agregar las herramientas de depuración para Windows:

1.  Faculta Haga clic en el hipervínculo para descargar las herramientas de depuración para Windows.

2.  Seleccione una de las siguientes opciones:

    -   **Use las herramientas de depuración para Windows en la siguiente ubicación**. Si selecciona esta opción, puede desplazarse hasta la ubicación de las herramientas.

    -   **Busque las herramientas de depuración para Windows en el sistema que está**reparando. Si selecciona esta opción, el **analizador de bloqueos** no funcionará si no se encuentran las herramientas de depuración para Windows en el equipo problemático.

3.  Cuando haya terminado, haga clic en **siguiente**.

### Para agregar definiciones para el sistema independiente de limpieza a la imagen de recuperación de DaRT

Las definiciones son un repositorio de malware conocido y de otro software potencialmente no deseado. Debido a que el malware se está desarrollando continuamente, el **sistema de limpieza independiente** se basa en las definiciones actuales para determinar si el software que está intentando instalar, ejecutar o cambiar la configuración en un equipo es software potencialmente no deseado o malintencionado.

Para incluir las definiciones más recientes en la imagen de recuperación de DaRT (recomendado), haga clic en **sí, descargar las definiciones más recientes.** La actualización de definiciones se inicia automáticamente. Para completar este proceso, debe estar conectado a Internet.

Para omitir la actualización de definición, haga clic en **no, descargar manualmente las definiciones más tarde**. Las definiciones no se incluirán en la imagen de recuperación de DaRT.

Si decide no incluir las definiciones más recientes en la imagen de recuperación o si las definiciones incluidas en la imagen de recuperación ya no son actuales en el momento en que está listo para usar el **sistema de limpieza independiente**, obtenga las definiciones más recientes antes de comenzar un examen siguiendo las instrucciones que se proporcionan en el **sistema de limpieza independiente**.

**Importante**  No puede explorar si no hay definiciones.

 

Cuando haya terminado, haga clic en **siguiente**.

### Para agregar drivers a la imagen de recuperación de DaRT

**PRECAUCIÓN**  De forma predeterminada, al agregar un controlador a la imagen de recuperación de DaRT, todos los archivos y subcarpetas adicionales que se encuentren en esa carpeta se agregarán a la imagen de recuperación. Para obtener más información, consulte [solución de problemas de DaRT 7,0](troubleshooting-dart-70-new-ia.md).

 

Debe incluir drivers adicionales en la imagen de recuperación para DaRT7 que puede necesitar al reparar un equipo. Por lo general, pueden incluir controladores de red o de almacenamiento que no estén incluidos en el DVD de Windows.

**Importante**  Cuando selecciones los drivers que deseas incluir, ten en cuenta que DaRT no admite la conectividad inalámbrica (como Bluetooth o 802.11 a/b/g/n).

 

**Para agregar un controlador de almacenamiento o controlador de red a la imagen de recuperación**

1.  En el cuadro de diálogo **drivers adicionales** del **Asistente de imagen de recuperación DART**, haga clic en **Agregar dispositivo**.

2.  Busque el archivo que desea agregar al controlador y, a continuación, haga clic en **abrir**.

    **Nota:**  El fabricante del controlador de almacenamiento o de la red proporciona el archivo de **controlador** .

     

3.  Repita los pasos 1 y 2 para cada controlador que desee incluir.

4.  Cuando haya terminado, haga clic en **siguiente**.

### Para agregar archivos a la imagen de recuperación de DaRT

Siga estos pasos para agregar archivos a la imagen de recuperación de modo que pueda usarlos para diagnosticar problemas del equipo.

1.  En el cuadro de diálogo **archivos adicionales** del **Asistente para recuperación de imágenes de DART**, haga clic en **Mostrar archivos**. Se abrirá una ventana del explorador que muestra la carpeta que contiene los archivos compartidos.

2.  Cree una subcarpeta en la carpeta que aparece en el cuadro de diálogo.

3.  Copie los archivos que desee en la nueva subcarpeta.

4.  Cuando haya terminado, haga clic en **siguiente.**

### Para seleccionar una ubicación para la ISO que contiene la imagen de recuperación de DaRT

Siga estos pasos para especificar la ubicación en la que se crea la imagen ISO:

1.  En el cuadro de diálogo **crear imagen de inicio** del **Asistente de imagen de recuperación de DART**, haga clic en **examinar**.

2.  Vaya a la ubicación preferida en la ventana **Guardar como** y, a continuación, haga clic en **Guardar**.

3.  Cuando haya terminado, haga clic en **siguiente**.

El tamaño de la imagen ISO variará en función de las herramientas que seleccione y de los archivos que agregue en el asistente.

El asistente requiere que la imagen ISO tenga una extensión de nombre de archivo **. ISO** porque la mayoría de los programas que graban un CD o DVD requieren esa extensión. Si no especifica una ubicación diferente, la imagen ISO se crea en el escritorio con el nombre **DaRT70. ISO**.

### Para grabar la imagen de recuperación en un CD o DVD

Si el **Asistente de recuperación de imágenes de DART** detecta una unidad de CD-RW compatible en el equipo, ofrece la grabación de la imagen ISO en un disco para usted. Si desea grabar un CD o un DVD y el asistente no reconoce su unidad, debe usar otro programa, como el programa incluido en la unidad. Puede usar un duplicador, un servicio de duplicación o un software de grabación de CD o DVD para hacer copias adicionales.

1.  En el cuadro de diálogo **grabar en un CD/DVD grabable** del **Asistente para recuperación de imágenes de DART**, seleccione **grabar la imagen en la siguiente unidad de CD/DVD grabable**.

2.  Seleccione la unidad de CD o DVD.

    **Nota:**  Si no se reconoce una unidad e instala una nueva, puede hacer clic en **Actualizar lista** para que el asistente actualice la lista de unidades disponibles.

     

3.  Haz clic en **Siguiente**.

## Temas relacionados


[Creación de la imagen para recuperación de DaRT 7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





