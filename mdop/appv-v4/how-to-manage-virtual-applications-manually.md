---
title: Cómo administrar aplicaciones virtuales manualmente
description: Cómo administrar aplicaciones virtuales manualmente
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817111"
---
# Cómo administrar aplicaciones virtuales manualmente


Puede usar la consola de administración de clientes de Application Virtualization (App-V) para administrar aplicaciones virtuales en el cliente de escritorio de App-V o en el cliente de App-v para servicios de escritorio remoto (anteriormente servicios de Terminal Server). Los administradores de App-V pueden usar realizar las siguientes tareas:

## Cómo cargar o descargar una aplicación de App-V


Puede usar los procedimientos siguientes para cargar o descargar una aplicación de la caché, directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones. Al seleccionar este nodo, el panel **resultados** muestra una lista de aplicaciones.

**Nota:**  Al cargar o descargar un paquete, todas las aplicaciones del paquete se cargan o se quitan de la caché. Al cargar un paquete, si no tiene suficiente espacio en la caché para cargar las aplicaciones, aumente el tamaño de la caché. Para obtener más información sobre el tamaño de la caché, consulte [Cómo cambiar el tamaño de la caché y la designación de letra de unidad](how-to-change-the-cache-size-and-the-drive-letter-designation.md).

 

**Para cargar una aplicación de App-V**

1.  Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **cargar** en el menú emergente.

2.  La aplicación se carga automáticamente. Se realiza un seguimiento del progreso en la columna denominada **Package status**. Debe actualizar la vista para ver que la carga está completa o para ver el progreso.

**Para descargar una aplicación de App-V**

1.  Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **Descargar** en el menú emergente.

2.  La aplicación se descarga automáticamente y la columna de **Estado del paquete** se actualiza para reflejar el cambio.

## Cómo borrar una aplicación de App-V


Puede borrar una aplicación de la consola directamente desde el panel de **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones. Al borrar una aplicación, el sistema quita la configuración, los accesos directos y las asociaciones de tipo de archivo que corresponden a la aplicación y también quita la aplicación de la lista de aplicaciones del usuario.

**Nota:**  Al borrar una aplicación de la consola, ya no podrá usarla. Sin embargo, la aplicación permanece en la caché y sigue estando disponible para otros usuarios en el mismo sistema. Después de una actualización de publicación, las aplicaciones desactivadas volverán a estar disponibles. Si hay varias aplicaciones en un paquete, la configuración del usuario no se quitará hasta que se borren todas las aplicaciones.

 

**Para borrar una aplicación de la consola**

1.  Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **Borrar** en el menú emergente.

2.  En el mensaje de confirmación, haga clic en **sí** para quitar la aplicación o en **no** para cancelar la operación.

## Cómo reparar una aplicación de App-V


Para reparar una aplicación seleccionada, puede realizar el siguiente procedimiento directamente desde el panel de **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones. Al reparar una aplicación, se elimina la configuración de usuario personalizada y se restaura la configuración predeterminada. Esta acción no cambia ni elimina accesos directos ni asociaciones de tipos de archivo, y no quita la aplicación de la caché.

**Para reparar una aplicación de App-V**

1.  Mover el cursor al panel **resultados** .

2.  Haga clic con el botón derecho en la aplicación que desee y seleccione **reparar** en el menú emergente.

3.  En el mensaje de confirmación, haga clic en **sí** para reparar la aplicación o en **no** para cancelar.

## Cómo importar una aplicación de App-V


Puede usar el siguiente procedimiento para importar una aplicación a la caché directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.

**Para importar una aplicación de App-V**

1.  Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **importar** en el menú emergente.

2.  En la ventana **examinar** , vaya a la ubicación del archivo de paquete para la aplicación que desee y, a continuación, haga clic en **Aceptar**.

    **Nota:**  Si ya ha configurado una ruta de búsqueda de importación o si el archivo SFT se encuentra en la misma ruta que la última importación correcta, el paso 2 no es necesario.

     

## Cómo bloquear o desbloquear una aplicación de App-V


Puede usar los procedimientos siguientes para bloquear o desbloquear cualquier aplicación en la memoria caché del cliente de escritorio de Application Virtualization o en el cliente para la caché de servicios de escritorio remoto (anteriormente Terminal Services). No se puede quitar una aplicación bloqueada de la caché para hacer sitio para nuevas aplicaciones. Para quitar una aplicación bloqueada de la memoria caché del cliente de escritorio de Application Virtualization o del cliente para la memoria caché de servicios de escritorio remoto, primero debe desbloquearla.

**Para bloquear una aplicación**

1.  Mover el cursor al panel **resultados** .

2.  Haga clic con el botón derecho en la aplicación que desee y seleccione **bloquear** en el menú emergente. La aplicación seleccionada está bloqueada en la caché.

**Para desbloquear una aplicación**

1.  Mover el cursor al panel **resultados** .

2.  Haga clic con el botón derecho en la aplicación que desee y seleccione **desbloquear** en el menú emergente. La aplicación seleccionada se desbloquea en la caché y se puede quitar.

## Cómo eliminar una aplicación de App-V


Al seleccionar el nodo de la **aplicación** en la consola de administración de cliente de Application Virtualization, el panel **resultados** muestra una lista de aplicaciones. Puede usar el procedimiento siguiente para eliminar una aplicación del panel **resultados** , que también quita la aplicación de la memoria caché.

**Nota:**  Al eliminar una aplicación, la aplicación seleccionada dejará de estar disponible para los usuarios de ese cliente. Los accesos directos y las asociaciones de los tipos de archivo están ocultos y la aplicación se elimina de la memoria caché. Sin embargo, si otra aplicación hace referencia a datos en los datos de la caché del sistema de archivos de la aplicación seleccionada, estos elementos no se eliminarán.

Después de una actualización de publicación, las aplicaciones eliminadas volverán a estar disponibles para usted.

 

**Para eliminar una aplicación**

1.  Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **eliminar** en el menú emergente.

2.  En el mensaje de confirmación, haga clic en **sí** para quitar la aplicación o en **no** para cancelar la operación.

## Cómo cambiar un icono de aplicación de App-V


Puede usar el siguiente procedimiento para cambiar un icono asociado a la aplicación seleccionada directamente desde el panel de **resultados** del nodo de la **aplicación** en la consola de administración del cliente de Application Virtualization.

**Para cambiar el icono de una aplicación**

1.  Coloque el cursor en el panel **resultados** y haga clic con el botón secundario en la aplicación que desee.

2.  Seleccione **propiedades**.

3.  En la pestaña **General** , haga clic en **Cambiar icono**.

4.  Seleccione el icono que desee o busque otra ubicación para seleccionar el icono. Una vez que haya seleccionado el icono, haga clic en **Aceptar**. El nuevo icono aparece en el panel **resultados** .

## Cómo agregar una aplicación de App-V


Puede usar el siguiente procedimiento para agregar una aplicación directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.

**Para agregar una aplicación**

1.  En el panel de **resultados** , haga clic con el botón derecho y seleccione **nueva aplicación** en el menú emergente.

2.  En la página del asistente, puede realizar las siguientes tareas:

    1.  **Cambiar icono**: muestra un explorador de iconos estándar de Windows. Busque y seleccione el icono que quiera.

    2.  **Ruta de acceso del archivo OSD o URL**: escriba una ruta de acceso absoluta local, una ruta de acceso UNC completa (archivo o directorio compartido en una red) o una dirección URL http.

    3.  **(Botón examinar de la OSD)**: muestra el cuadro de diálogo de **archivo abierto** estándar de Windows. Busque el archivo que desea encontrar.

3.  Haga clic en **Finalizar** para agregar la aplicación al panel **resultados** .

## Cómo publicar un acceso directo a la aplicación App-V


Puede usar el procedimiento siguiente para publicar accesos directos a una aplicación directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.

**Para publicar accesos directos a aplicaciones**

1.  Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **nuevo acceso directo** en el menú emergente para mostrar el Asistente para nuevo acceso directo.

2.  En la primera página del Asistente para crear accesos directos, seleccione un icono y especifique un nombre para el acceso directo.

    1.  **Cambiar icono**: muestra un explorador de iconos estándar de Windows. Busque y seleccione el icono que quiera.

    2.  **Título del acceso directo**: escriba el nombre que desea asignar al acceso directo. El valor predeterminado de este campo es el nombre y la versión existentes de la aplicación.

3.  En la segunda página del asistente, determine la ubicación del acceso directo publicado.

    1.  **El escritorio**: Seleccione esta casilla para publicar el acceso directo en el escritorio.

    2.  **La barra de herramientas de inicio rápido**: Seleccione esta casilla para publicar el acceso directo en la barra de herramientas Inicio rápido.

    3.  **El menú enviar a**: Seleccione esta casilla para publicar el acceso directo en el menú **Enviar a** .

    4.  **Programas en el menú Inicio**: cuando se activa la casilla de verificación **menú Inicio** , este campo se activa. Deje este campo en blanco para publicar el acceso directo directamente en la raíz de la carpeta programas o escriba un nombre de carpeta o jerarquía, por ejemplo, "My \ _Computer aplicaciones \\Office". Los accesos directos creados de esta manera solo están disponibles para el usuario actual.

    5.  **Otra ubicación** y botón **examinar** : al seleccionar la casilla **otra ubicación** , este campo se activa. Escriba cualquier ubicación válida en el equipo o cualquier ruta UNC disponible (archivo o directorio compartido en una red). El botón **examinar** muestra un cuadro de diálogo estándar de **apertura de archivo** de Windows.

4.  En la tercera página del asistente, escriba los parámetros de la línea de comandos que desee.

5.  Haga clic en **Finalizar** para publicar los métodos abreviados y salir en el panel **resultados** .

## Cómo agregar una asociación de tipo de archivo para una aplicación de App-V


Puede usar el siguiente procedimiento para agregar una asociación de tipo de archivo mediante el nodo **asociaciones de tipo de archivo** de la consola de administración del cliente de virtualización de aplicaciones.

**Para agregar una asociación de tipo de archivo**

1.  Haga clic con el botón derecho en el nodo **asociaciones de tipo de archivo** y seleccione **nueva asociación** en el menú emergente.

2.  Complete el primer paso del cuadro de diálogo completando la información siguiente y, a continuación, haga clic en **siguiente**:

    1.  **Extensión**: especifique una nueva extensión de nombre de archivo. De forma predeterminada, este campo está en blanco.

    2.  **Crear un nuevo tipo de archivo con esta descripción**: Seleccione este botón de radio para especificar una nueva descripción de tipo de archivo en el campo activo. Este botón está seleccionado de forma predeterminada y el campo activo está en blanco.

    3.  **Aplicar este tipo de archivo a todos los usuarios**: Seleccione esta casilla cuando desee que esta asociación sea global para todos los usuarios. De forma predeterminada, este cuadro está desactivado.

    4.  **Vincular esta extensión con un tipo de archivo existente**: Seleccione este botón de radio para asociar la extensión con un tipo de archivo existente. Seleccione un tipo de archivo de la lista desplegable. Si elige esta opción, **Next** cambiará a **Finish**.

3.  Complete el segundo paso del cuadro de diálogo completando la información siguiente y, a continuación, haga clic en **Finalizar** para volver a la consola de administración de cliente:

    1.  **Cambiar icono**: haga clic en este botón para cambiar el icono de la aplicación. Seleccione uno de los iconos disponibles, busque una nueva ubicación y seleccione un icono.

    2.  **Abrir archivos con la aplicación seleccionada**: Seleccione este botón de radio para abrir el archivo con una aplicación existente. Elija una aplicación de la lista desplegable de aplicaciones disponibles.

    3.  **Abrir archivo con la asociación que se describe en este archivo OSD**: Seleccione este botón de radio para especificar un archivo de descriptor de software abierto (OSD) que determine la aplicación que se ha usado para abrir el archivo. Use el botón Examinar para seleccionar una ubicación existente o escriba una ruta de acceso o una dirección URL con formato HTTP en este campo.

## Cómo eliminar una asociación de tipo de archivo para una aplicación de App-V


Puede usar el procedimiento siguiente para eliminar una asociación de tipo de archivo. El nodo **asociaciones de tipo de archivo** está un nivel por debajo del nodo de **virtualización de aplicaciones** en el panel de **ámbito** . Al seleccionar este nodo, el panel **resultados** muestra una lista de asociaciones de tipos de archivo.

**Para quitar una asociación de tipo de archivo**

1.  En el panel de **resultados** , haga clic con el botón secundario en la extensión de la Asociación de tipo de archivo que desea eliminar.

2.  Seleccione **eliminar** en el menú emergente.

3.  Haga clic en **sí** para eliminar la asociación o en **no** para volver al panel **resultados** .

## Temas relacionados


[Cliente de virtualización de aplicaciones](application-virtualization-client.md)

 

 





