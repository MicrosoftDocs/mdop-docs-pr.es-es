---
title: Nodo de directivas de proveedor
description: Nodo de directivas de proveedor
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815831"
---
# Nodo de directivas de proveedor


El nodo de **directivas de proveedor** es un nivel por debajo del nodo del sistema de virtualización de aplicaciones en el panel de **ámbito** de la consola de administración del servidor de virtualización de aplicaciones. Al seleccionar este nodo, el panel **resultados** muestra una lista de directivas de proveedor. Haga clic con el botón secundario en el nodo de **directivas de proveedor** para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="new-provider-policy"></a>**Nueva Directiva de proveedor**  
Muestra el Asistente para nueva Directiva de proveedor. Este asistente consta de las siguientes páginas:

1.  Escriba un nombre en el campo Nombre de la **Directiva del proveedor** . Seleccione la casilla de verificación **administrar el escritorio del cliente con la consola de administración** si quiere esa capacidad. Seleccione una o ambas de las siguientes casillas de verificación si quiere la funcionalidad asociada:

    -   **Actualizar la configuración de publicación cuando un usuario inicia sesión**

    -   **Actualizar la configuración cada**. Después de seleccionar esta opción, escriba un número y seleccione la unidad en el menú desplegable. Las entradas válidas van desde un mínimo de **30 minutos** hasta un máximo de **999 días**.

2.  Haga clic en **Agregar** o **quitar** para agregar o quitar una asignación de grupo. Use el cuadro de diálogo de exploración estándar de **Windows** para buscar un grupo de usuarios.

3.  Seleccione una de las siguientes casillas en el cuadro de diálogo **configuración de canalización del proveedor** para habilitar la característica asociada:

    -   **Autenticación**: seleccione el tipo de autenticación de la lista desplegable.

    -   **Exigir configuración de permisos de acceso**

    -   **Información de uso de registros**

    -   **Licencias**: Seleccione un esquema de cumplimiento de la lista desplegable.

4.  Haga clic en **Finalizar** para agregar la nueva Directiva de proveedor.

<a href="" id="view"></a>**Ver**  
Cambia la apariencia y el contenido del panel **resultados** .

<a href="" id="new-window-from-here"></a>**Nueva ventana desde aquí**  
Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.

<a href="" id="refresh"></a>**Actualizar**  
Actualiza la vista del servidor.

<a href="" id="export-list"></a>**Exportar lista**  
Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.

## Temas relacionados


[Consola de administración de servidor: Nodo de directivas de proveedor](server-management-console-provider-policies-node.md)

 

 





