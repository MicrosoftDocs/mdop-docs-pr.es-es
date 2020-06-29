---
title: Panel de resultados de aplicaciones
description: Panel de resultados de aplicaciones
author: dansimp
ms.assetid: 977a4d35-5344-41fa-af66-14957b38ed47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdabaeee0b9aaa1c96b6ae732ae4bb5b6d63ef3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819491"
---
# Panel de resultados de aplicaciones


El panel de **resultados de aplicaciones** en la consola de administración de cliente de Application Virtualization muestra una lista de las aplicaciones disponibles. Los usuarios pueden ver una lista de las aplicaciones para las que se les ha concedido privilegios de acceso.

Para obtener más información sobre los procedimientos que puede realizar en este panel, consulte [Cómo administrar las aplicaciones en la consola de administración de clientes](how-to-manage-applications-in-the-client-management-console.md).

Haga clic con el botón secundario en cualquier aplicación para mostrar un menú emergente que contenga los siguientes elementos.

<a href="" id="new-shortcut"></a>**Nuevo acceso directo**  
Este elemento de menú muestra el Asistente para crear accesos directos. Este asistente consta de tres páginas:

1.  Seleccione un icono y especifique un nombre para el acceso directo:

    1.  **Cambiar icono**: muestra un explorador de iconos estándar de Windows. Busque y seleccione el icono que quiera.

    2.  **Título del acceso directo**: escriba el nombre que desea asignar al acceso directo. El valor predeterminado de este campo es el nombre y la versión existentes de la aplicación.

2.  Determinar la ubicación del acceso directo publicado.

    1.  **Ubicación del método abreviado**: Seleccione una ubicación seleccionando una de las casillas de verificación. Las ubicaciones disponibles son **escritorio**, **barra de herramientas de inicio rápido**, **menú enviar a**, **menú Inicio**y **otra ubicación**.

    2.  **Programas en el menú Inicio**: cuando se activa la casilla de verificación **menú Inicio** , este campo se activa. Deje este campo en blanco para publicar el acceso directo directamente en la raíz de la carpeta programas o escriba un nombre de carpeta o jerarquía, por ejemplo, "My \ _Computer aplicaciones \\Office". Los accesos directos creados de esta manera solo están disponibles para el usuario actual.

    3.  **Otra ubicación** y botón examinar: al seleccionar la casilla **otra ubicación** , este campo se activa. Escriba cualquier ubicación válida en el equipo o cualquier ruta de acceso de Convención de nomenclatura universal (UNC) disponible (archivo o directorio compartido en una red). El botón examinar muestra un cuadro de diálogo estándar de **apertura de archivo** de Windows.

3.  Escriba los parámetros de la línea de comandos que desee y, a continuación, haga clic en **Finalizar** para salir del asistente.

<a href="" id="new-association"></a>**Nueva asociación**  
Este elemento de menú muestra el Asistente para nueva asociación. Este asistente consta de dos páginas:

1.  Escriba una extensión de nombre de archivo y asocie la extensión a un tipo de archivo.

    1.  **Extensión**: especifique una extensión de nombre de archivo. De forma predeterminada, este campo está en blanco.

    2.  **Crear un nuevo tipo de archivo con esta descripción**: Seleccione este botón de radio para especificar una nueva descripción de tipo de archivo en el campo activo. Este botón está seleccionado de forma predeterminada y el campo activo está en blanco.

    3.  **Aplicar este tipo de archivo a todos los usuarios**: Seleccione esta casilla cuando desee que esta asociación sea global para todos los usuarios. De forma predeterminada, este cuadro no está seleccionado.

    4.  **Vincular esta extensión con un tipo de archivo existente**: Seleccione este botón de radio para asociar la extensión con un tipo de archivo existente. Elija un tipo de archivo de la lista desplegable. Si elige esta opción, **Next** cambiará a **Finish**.

2.  Seleccione la aplicación que abrirá los archivos con la extensión especificada:

    1.  **Abrir archivos con la aplicación seleccionada**: Seleccione este botón de radio para abrir el archivo con una aplicación existente. Elija una aplicación de la lista desplegable de aplicaciones disponibles.

    2.  **Abrir archivo con la asociación que se describe en este archivo OSD**: Seleccione este botón de radio para especificar un archivo de descriptor de software abierto (OSD) que determine la aplicación que se ha usado para abrir el archivo. Use el botón Examinar para seleccionar una ubicación existente o escriba una ruta de acceso o una dirección URL con formato HTTP en este campo.

<a href="" id="repair"></a>**Reparar**  
Restablece la configuración predeterminada de la aplicación y elimina toda la configuración definida por el usuario para la aplicación seleccionada.

<a href="" id="load-or-unload"></a>**Cargar** o **Descargar**  
Carga o descarga la aplicación seleccionada en la caché. Este comando no está disponible si el 100 por ciento de la aplicación está en la caché.

<a href="" id="clear"></a>**Borrar**  
Quita la configuración del usuario, los accesos directos y las asociaciones de tipos de archivo de la aplicación seleccionada. Este elemento no está disponible si un usuario ejecuta una aplicación de un conjunto de aplicaciones. Muestra un mensaje de confirmación.

<a href="" id="lock-or-unlock"></a>**Bloquear** o **desbloquear**  
Bloquea o desbloquea una aplicación en la memoria caché. Cuando una aplicación está bloqueada, no se puede eliminar ni sobrescribir.

<a href="" id="import"></a>**Importar**  
Importa una aplicación a la caché directamente desde este comando en el nodo **aplicaciones** .

<a href="" id="delete"></a>**Eliminar**  
Elimina una aplicación del panel **resultados** y del equipo, y borra la aplicación de la caché.

<a href="" id="refresh"></a>**Actualizar**  
Actualiza el contenido del panel **resultados** .

<a href="" id="properties"></a>**Propiedades**  
Muestra el cuadro de diálogo **propiedades** de la aplicación seleccionada. Este cuadro de diálogo tiene dos pestañas:

1.  La pestaña **General** muestra el icono y el nombre de la aplicación, la ubicación desde la que se transmitió la aplicación y la ruta de acceso al archivo OSD local. En esta pestaña, puede cambiar el icono de la aplicación o puede borrar la configuración (que quita los accesos directos y las asociaciones de los tipos de archivo).

2.  La **pestaña paquete** muestra información sobre el paquete de la aplicación, y puede **bloquear**, **desbloquear**, **cargar**, **Descargar**e **importar** aplicaciones.

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración de clientes.

## Mostrar las opciones generales del panel resultados


Haga clic con el botón secundario en cualquier lugar del panel **resultados** para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="new-application"></a>**Nueva aplicación**  
Este elemento de menú muestra el Asistente para nueva aplicación. Este asistente consiste en una página en la que puede seleccionar un icono para la aplicación y examinar o escribir una dirección URL o una ruta de acceso al archivo OSD:

1.  **Cambiar icono**: muestra un explorador de iconos estándar de Windows. Busque y seleccione el icono que quiera.

2.  **Ruta de acceso o URL del archivo OSD**: escriba una ruta de acceso absoluta local, una ruta de acceso UNC completa o una dirección URL http.

3.  **... (Botón examinar de la OSD)** : Muestra el cuadro de diálogo de **archivo abierto** estándar de Windows. Busque el archivo que desea encontrar.

<a href="" id="refresh"></a>**Actualizar**  
Actualiza el panel **resultados** .

<a href="" id="export-list"></a>**Exportar lista**  
Puede usar este elemento de menú para crear un archivo de texto delimitado por tabulaciones que incluya el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.

<a href="" id="view"></a>**Ver**  
Esta lista emergente de elementos de menú le permite cambiar la apariencia y el contenido del panel **resultados** .

<a href="" id="arrange-line-up-icons"></a>**Iconos organizar y alinear**  
Estos elementos de menú se pueden usar para cambiar la forma en que se muestran los iconos en el panel **resultados** .

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración.

## Temas relacionados


[Nodo de aplicaciones](applications-node.md)

[Columnas del panel de resultados de aplicaciones](applications-results-pane-columns.md)

[Referencia de la consola de administración de cliente de virtualización de aplicaciones](application-virtualization-client-management-console-reference.md)

[Cómo administrar aplicaciones en la consola de administración de cliente](how-to-manage-applications-in-the-client-management-console.md)

 

 





