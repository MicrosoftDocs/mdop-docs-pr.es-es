---
title: Panel de resultados de aplicaciones en la consola de administración del servidor
description: Panel de resultados de aplicaciones en la consola de administración del servidor
author: dansimp
ms.assetid: 686218bc-6156-40e2-92aa-90981c3d112a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d592173dff21a3d5d7ab92bbb26f15e67b7c878
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822001"
---
# Panel de resultados de aplicaciones en la consola de administración del servidor


El panel **resultados de aplicaciones** muestra una lista de las aplicaciones disponibles.

Haga clic con el botón derecho en cualquier parte del panel **resultados** , excepto en un grupo de aplicaciones o aplicaciones, para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="refresh"></a>**Actualizar**  
Actualiza la lista de aplicaciones.

<a href="" id="export-list"></a>**Exportar lista**  
Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando. Para obtener más información sobre la característica **Exportar lista** , consulte la documentación de Microsoft Management Console.

<a href="" id="view"></a>**Ver**  
Cambia la apariencia y el contenido del panel **resultados** .

<a href="" id="arrange-line-up-icons"></a>**Iconos organizar y alinear**  
Organiza los iconos en el panel **resultados** .

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración de virtualización de aplicaciones.

Haga clic con el botón secundario en cualquier aplicación en el panel **resultados** para mostrar un menú emergente que contenga los siguientes elementos.

<a href="" id="move"></a>**Move**  
Mueve las aplicaciones a grupos de aplicaciones y fuera de ellos.

<a href="" id="copy"></a>**Copiar**  
Copia la aplicación en otro sistema de virtualización de aplicaciones.

<a href="" id="duplicate"></a>**Duplicar**  
Duplica la aplicación en el panel **resultados** .

<a href="" id="delete"></a>**Eliminar**  
Quita la aplicación del sistema de virtualización de aplicaciones.

<a href="" id="rename"></a>**Cambiar nombre**  
Le permite cambiar el nombre de la aplicación.

<a href="" id="properties"></a>**Propiedades**  
Muestra el cuadro de diálogo **propiedades** de la aplicación seleccionada. Este cuadro de diálogo tiene las siguientes pestañas:

-   Pestaña **General** : muestra el icono de la aplicación, el nombre de la aplicación y el nombre del paquete. Esta pestaña también muestra la siguiente información específica sobre la aplicación que puede cambiar:

    -   **Versión**: permite introducir el número de versión apropiado. Active la casilla **Habilitar** la numeración de versiones.

    -   **Descripción**: le permite escribir una breve descripción de la aplicación.

    -   **Ruta de acceso a OSD**: le permite introducir o examinar la ubicación del archivo de descriptor de software abierto (OSD) correspondiente.

    -   **Ruta de icono**: le permite introducir o examinar la ubicación del archivo de icono que desea asociar a la aplicación.

    -   **Grupo de licencias de aplicaciones**: le permite seleccionar el grupo de licencias de la lista desplegable de grupos de licencias.

    -   **Grupo de servidores**: permite seleccionar el grupo de servidores de la lista desplegable de grupos de servidores.

-   Pestaña de **accesos directos** : muestra las casillas correspondientes a las ubicaciones en las que se publican los accesos directos. Puede activar o desactivar las casillas de verificación de esta pestaña.

-   Ficha **asociaciones de tipo de archivo** : muestra una lista de los tipos de archivo asociados a la aplicación seleccionada. En esta pestaña, puede Agregar, editar o eliminar la Asociación de tipo de archivo.

-   Pestaña **permisos de acceso** : muestra la lista de grupos que tienen permisos de acceso a la aplicación seleccionada. En esta pestaña, puede Agregar, editar o eliminar grupos.

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración de virtualización de aplicaciones.

Haga clic con el botón secundario en cualquier grupo de aplicaciones para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="new-application-group"></a>**Nuevo grupo de aplicaciones**  
Muestra el Asistente para nuevo grupo de aplicaciones. Agregue el nombre del nuevo grupo de aplicaciones en el campo correspondiente y, a continuación, haga clic en **Finalizar**.

<a href="" id="new-application"></a>**Nueva aplicación**  
Muestra el Asistente para nueva aplicación. Desplácese por el Asistente para agregar aplicaciones.

<a href="" id="import-applications"></a>**Importar aplicaciones**  
Muestra un cuadro de diálogo examinar que puede usar para importar aplicaciones existentes a la consola de administración de virtualización de aplicaciones. Puede importar un archivo OSD o un archivo SPRJ (SPRJ).

<a href="" id="move"></a>**Move**  
Mueve el grupo de aplicaciones hacia y fuera de grupos de aplicaciones.

<a href="" id="copy"></a>**Copiar**  
Copia el grupo de aplicaciones en un nuevo servidor.

<a href="" id="new-window-from-here"></a>**Nueva ventana desde aquí**  
Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.

<a href="" id="delete"></a>**Eliminar**  
Quita el grupo de aplicaciones del servidor.

<a href="" id="rename"></a>**Cambiar nombre**  
Cambia el nombre del grupo de aplicaciones.

<a href="" id="refresh"></a>**Actualizar**  
Actualiza el grupo de aplicaciones. Si el panel **resultados** muestra todo el nodo de la aplicación, el panel cambiará para mostrar el contenido del grupo de aplicaciones.

<a href="" id="properties"></a>**Propiedades**  
Muestra el cuadro de diálogo **propiedades** del grupo de aplicaciones seleccionado. Este cuadro de diálogo tiene las siguientes pestañas:

-   Ficha **General** : muestra el icono del grupo de aplicaciones y el nombre del grupo de aplicaciones. Esta pestaña también muestra la siguiente información sobre el grupo de aplicaciones que puede cambiar.

    -   **Versión**: permite especificar un número de versión para el grupo de aplicaciones.

    -   **Descripción**: le permite escribir una breve descripción del grupo de aplicaciones.

    -   **Ruta de visualización OSD**: le permite introducir o examinar la ubicación en la que se encuentra el archivo OSD.

    -   **Ruta de icono**: permite introducir o examinar la ubicación en la que se encuentra el archivo de icono.

    -   **Grupo de licencias de aplicaciones**: le permite seleccionar el grupo de licencias de la lista desplegable de grupos de licencias.

    -   **Grupo de servidores**: permite seleccionar el grupo de servidores de la lista desplegable de grupos de servidores.

-   Pestaña de **accesos directos** : muestra las casillas correspondientes a las ubicaciones en las que se publican los accesos directos. Puede activar o desactivar las casillas de verificación de esta pestaña.

-   Ficha **asociaciones de archivos** : muestra la lista de asociaciones de tipos de archivo. Puede Agregar, modificar o eliminar las asociaciones de tipos de archivo en esta pestaña.

-   Pestaña **permisos de acceso** : muestra la lista de grupos que tienen permisos de acceso al grupo de aplicaciones seleccionado. En esta pestaña, puede Agregar, editar o eliminar grupos.

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración de virtualización de aplicaciones.

## Temas relacionados


[Consola de administración de servidor: Nodo de aplicaciones](server-management-console-applications-node.md)

 

 





