---
title: Panel de resultados de asociaciones de tipo de archivo
description: Panel de resultados de asociaciones de tipo de archivo
author: dansimp
ms.assetid: bc5ceb48-1b9f-45d9-a770-1bac90629c76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 73ea8e0e4145aeae309abff362a790287f19f6af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821561"
---
# Panel de resultados de asociaciones de tipo de archivo


El panel de **resultados** de **Asociación de archivos** es un nivel por debajo del panel **del sistema** en la consola de administración de cliente de Application Virtualization y muestra una lista de las asociaciones de tipos de archivo disponibles. Los usuarios pueden ver una lista de extensiones de tipos de archivo y las aplicaciones a las que corresponden.

Para mostrar opciones específicas de tipos de archivo, haga clic con el botón secundario en cualquier extensión de aplicación para mostrar un menú emergente que contenga los siguientes elementos.

<a href="" id="delete"></a>**Eliminar**  
Elimina la extensión de nombre de archivo de la lista y quita la asociación al tipo de archivo.

<a href="" id="properties"></a>**Propiedades**  
Muestra el cuadro de diálogo **propiedades** de la extensión de la aplicación seleccionada. Este cuadro de diálogo tiene dos pestañas:

-   En la pestaña **General** se muestra información general sobre la Asociación de tipo de archivo, incluido el icono y el nombre de la aplicación:

    -   **Icono**: muestra el icono seleccionado para el tipo de archivo asociado.

    -   **Nombre**de la Asociación: muestra el nombre del tipo de archivo.

    -   **Cambiar icono**: haga clic en este botón para cambiar el icono de la Asociación de tipo de archivo.

    -   **Extensión**: muestra la extensión o extensiones asociadas a un tipo de archivo concreto.

    -   **Desvincular**: este botón está habilitado cuando hay más de una extensión asociada a una aplicación. Haga clic en **desvincular** para administrar la extensión de tipo de archivo por separado de la extensión con la que está vinculada.

    -   **Aplicación especificada**: Seleccione este botón de radio y elija una aplicación de la lista desplegable de aplicaciones disponibles. Está cambiando la aplicación que se usa en la acción predeterminada. También puede buscar una aplicación si no está disponible en la lista desplegable.

    -   **Archivo OSD**: Seleccione este botón de radio y especifique una ruta de acceso a un archivo descriptor de software abierto (OSD). También puede ir a un archivo OSD.

-   La pestaña **avanzadas** muestra información detallada sobre la Asociación de tipo de archivo:

    -   **Acción**: muestra una lista de las acciones disponibles para el tipo de archivo asociado.

    -   **Tipo de contenido**: muestra una descripción del contenido del tipo de archivo. Si este campo se deja en blanco, el cliente lo rellenará.

    -   **Tipo percibido**: muestra el tipo de archivo. Puede seleccionar una de las opciones de la lista desplegable o agregar las suyas propias.

    -   **Confirmar apertura después**de la descarga: Seleccione esta casilla para mostrar un mensaje de confirmación después de cargar un archivo. Si se selecciona este cuadro, al intentar abrir un archivo de este tipo descargándolo en un explorador Web, el explorador le preguntará si desea guardar el archivo en lugar de abrirlo directamente en el explorador sin confirmación.

    -   **Mostrar siempre la extensión**: Seleccione esta casilla para especificar que las extensiones se deben mostrar incluso cuando el usuario solicite que el sistema oculte las extensiones de los tipos de archivo conocidos.

    -   **Agregar al nuevo menú**: Seleccione esta casilla para especificar que la extensión o las extensiones deben mostrarse en el menú contextual **nuevo** del shell.

    -   **Aplicar a todos los usuarios**: Seleccione esta casilla para especificar que las extensiones deben estar disponibles para todos los usuarios.

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración de clientes.

Para mostrar las opciones generales del panel **resultados** , haga clic con el botón secundario en cualquier lugar del panel **resultados** para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="new-association"></a>**Nueva asociación**  
Este elemento de menú muestra el Asistente para nueva asociación. Este asistente consta de dos páginas:

1.  Escriba una extensión de nombre de archivo nueva o existente y asocie la extensión con un tipo de archivo:

    -   **Extensión**: especifique una nueva extensión de nombre de archivo. De forma predeterminada, este campo está en blanco.

    -   **Crear un nuevo tipo de archivo con esta descripción**: Seleccione este botón de radio para especificar una nueva descripción de tipo de archivo en el campo activo. Este botón está seleccionado de forma predeterminada y el campo activo está en blanco.

    -   **Aplicar este tipo de archivo a todos los usuarios**: Seleccione esta casilla cuando desee que esta asociación sea global para todos los usuarios. De forma predeterminada, este cuadro no está seleccionado.

    -   **Vincular esta extensión con un tipo de archivo existente**: Seleccione este botón de radio para asociar la extensión con un tipo de archivo existente. Seleccione un tipo de archivo de la lista desplegable. Si elige esta opción, **Next** cambiará a **Finish**.

2.  Seleccione la aplicación que abrirá los archivos con la extensión especificada:

    -   **Abrir archivos con la aplicación seleccionada**: Seleccione este botón de radio para abrir el archivo con una aplicación existente. Elija una aplicación de la lista desplegable de aplicaciones disponibles.

    -   **Abrir archivo con la Asociación descrita en este archivo OSD**: Seleccione este botón de radio para especificar un archivo OSD que determine la aplicación que se usó para abrir el archivo. Use el botón Examinar para seleccionar una ubicación existente o escriba una ruta de acceso o una dirección URL con formato HTTP en este campo.

<a href="" id="refresh"></a>**Actualizar**  
Este elemento actualiza el panel **resultados** .

<a href="" id="export-list"></a>**Exportar lista**  
Con este elemento de menú, puede crear un archivo de texto delimitado por tabulaciones que incluya el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.

<a href="" id="view"></a>**Ver**  
Esta lista emergente de elementos de menú le permite cambiar la apariencia y el contenido del panel **resultados** .

<a href="" id="arrange-line-up-icons"></a>**Iconos organizar y alinear**  
Estos elementos de menú se pueden usar para cambiar la forma en que se muestran los iconos en el panel **resultados** .

<a href="" id="help"></a>**Ayuda**  
Este elemento muestra el sistema de ayuda de la consola de administración.

## Temas relacionados


[Cómo cambiar un icono de aplicación](how-to-change-an-application-icon.md)

[Nodo de asociaciones de tipo de archivo](file-type-associations-node-client.md)

[Columnas del panel de resultados de asociaciones de tipo de archivo](file-type-association-results-pane-columns.md)

 

 





