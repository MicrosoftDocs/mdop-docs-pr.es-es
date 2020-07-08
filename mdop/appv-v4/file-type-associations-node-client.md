---
title: Nodo de asociaciones de tipo de archivo
description: Nodo de asociaciones de tipo de archivo
author: dansimp
ms.assetid: 48e4d9eb-00bd-4231-a68a-f8597ab683ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d94621a1d418f0af29ef9e73b8d430c81a7181c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821531"
---
# Nodo de asociaciones de tipo de archivo


El nodo **asociaciones de tipo de archivo** está un nivel por debajo del nodo de **virtualización de aplicaciones** en el panel de **ámbito** de la consola de administración del cliente de virtualización de aplicaciones. Al seleccionar este nodo, el panel **resultados** muestra una lista de asociaciones de tipos de archivo.

Haga clic con el botón derecho en el nodo **asociaciones de tipo de archivo** para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="new-association"></a>**Nueva asociación**  
Este elemento de menú muestra el Asistente para nueva asociación. Este asistente consta de dos páginas:

1.  Escriba una extensión de nombre de archivo nueva o existente y asocie la extensión con un tipo de archivo:

    -   **Extensión**: especifique una extensión de nombre de archivo nueva o existente. De forma predeterminada, este campo está en blanco.

    -   **Crear un nuevo tipo de archivo con esta descripción**: Seleccione este botón de radio para especificar una nueva descripción de tipo de archivo en el campo activo. Este botón está seleccionado de forma predeterminada y el campo activo está en blanco.

    -   **Aplicar este tipo de archivo a todos los usuarios**: Seleccione esta casilla cuando desee que esta asociación sea global para todos los usuarios. De forma predeterminada, este cuadro no está seleccionado.

    -   **Vincular esta extensión con un tipo de archivo existente**: Seleccione este botón de radio para asociar la extensión con un tipo de archivo existente. Elija un tipo de archivo de la lista desplegable. Si elige esta opción, **Next** cambiará a **Finish**.

2.  Seleccione la aplicación que abrirá los archivos con la extensión especificada:

    -   **Abrir archivos con la aplicación seleccionada**: Seleccione este botón de radio para abrir el archivo con una aplicación existente. Elija una aplicación de la lista desplegable de aplicaciones disponibles.

    -   **Abrir archivos con la aplicación que se describe en este archivo OSD**: Seleccione este botón de radio para especificar un archivo de descriptor de software abierto (OSD) que determine la aplicación que se ha usado para abrir el archivo. Examine para seleccionar una ubicación existente o escriba una ruta de acceso o una dirección URL con formato HTTP en este campo.

<a href="" id="new-window-from-here"></a>**Nueva ventana desde aquí**  
Seleccione este elemento de menú para abrir una nueva consola de administración con el nodo seleccionado como nodo raíz.

<a href="" id="export-list"></a>**Exportar lista**  
Puede usar este elemento de menú para crear un archivo de texto delimitado por tabulaciones que incluya el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.

<a href="" id="view"></a>**Ver**  
Esta lista emergente de elementos de menú le permite cambiar la apariencia y el contenido del panel **resultados** .

<a href="" id="refresh"></a>**Actualizar**  
Seleccione este elemento para actualizar la consola de administración.

<a href="" id="help"></a>**Ayuda**  
Con este elemento de menú, puede mostrar el sistema de ayuda de la consola de administración.

## Temas relacionados


[Panel de resultados de asociaciones de tipo de archivo](file-type-association-results-pane.md)

[Columnas del panel de resultados de asociaciones de tipo de archivo](file-type-association-results-pane-columns.md)

 

 





