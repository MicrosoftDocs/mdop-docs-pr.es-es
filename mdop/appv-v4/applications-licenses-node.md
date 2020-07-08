---
title: Nodo de licencias de aplicaciones
description: Nodo de licencias de aplicaciones
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819511"
---
# Nodo de licencias de aplicaciones


El nodo **aplicaciones de licencias** está un nivel por debajo del nodo del sistema de virtualización de aplicaciones en el panel de **ámbitos** de la consola de administración del servidor de virtualización de aplicaciones. Al seleccionar este nodo, el panel **resultados** muestra una lista de licencias y grupos de licencias. Están disponibles los siguientes tipos de licencia:

-   **Licencia ilimitada**: proporciona acceso a cualquier número de usuarios simultáneos. Este método de licencias es adecuado cuando desea asociar una licencia de toda la empresa con una aplicación.

-   **Licencia concurrente**: le permite definir la cantidad máxima de usuarios simultáneos que pueden usar la aplicación.

-   **Licencia con nombre**: le permite asignar una licencia a un usuario individual. Una licencia con nombre se puede usar para asegurarse de que un usuario determinado siempre pueda ejecutar la aplicación.

**Nota:**  Puede combinar licencias simultáneas y con nombre para la misma aplicación.

 

Haga clic con el botón derecho en el nodo de **licencias aplicaciones** para mostrar un menú emergente que contiene los siguientes elementos.

<a href="" id="new-unlimited-license"></a>**Nueva licencia sin límites**  
Muestra el nuevo Asistente para licencias ilimitadas. Este asistente consta de las siguientes páginas:

1.  Escriba el nombre del grupo de licencias en el campo **nombre del grupo de licencias aplicaciones** y escriba un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia. (Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.

2.  Escriba un breve mensaje descriptivo en el campo Descripción de la **licencia** y seleccione la casilla de verificación **habilitado** para habilitar la licencia.

    De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia. Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.

3.  Haga clic en **Finalizar** para agregar la nueva licencia.

<a href="" id="new-concurrent-license"></a>**Nueva licencia concurrente**  
Muestra el nuevo Asistente para licencias simultáneas. Este asistente consta de las tres páginas siguientes y es casi idéntica al nuevo Asistente para licencias ilimitadas:

1.  Escriba el nombre del grupo de licencias en el campo **nombre del grupo de licencias aplicaciones** y escriba un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia. (Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.

2.  Escriba un breve texto descriptivo en el campo Descripción de la **licencia** y escriba un valor en el campo **cantidad de licencias simultánea** .

    También puede usar las flechas arriba y abajo para especificar el número de licencias simultáneas. Seleccione la casilla de verificación **habilitado** para habilitar la licencia.

    De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia. Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.

3.  Haga clic en **Finalizar** para agregar las nuevas licencias.

<a href="" id="new-named-license"></a>**Nueva licencia con nombre**  
Muestra el Asistente para nueva licencia. Este asistente consta de las cuatro páginas siguientes:

1.  Escriba el nombre del grupo de licencias en el campo **nombre del grupo de licencias aplicaciones** y escriba un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia. (Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.

2.  Escriba un breve mensaje descriptivo en el campo Descripción de la **licencia** y seleccione la casilla de verificación **habilitado** para habilitar la licencia.

    De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia. Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.

3.  Haga clic en **Agregar**, **Editar**o **quitar** usuarios con nombre.

4.  Haga clic en **Finalizar** para agregar la nueva licencia.

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

Si hace clic en un grupo de licencias o licencia que aparece bajo el nodo **licencias de aplicación** en el panel **ámbito** , están disponibles los siguientes elementos.

<a href="" id="view"></a>**Ver**  
Cambia la apariencia y el contenido del panel **resultados** .

<a href="" id="new-window-from-here"></a>**Nueva ventana desde aquí**  
Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.

<a href="" id="delete"></a>**Eliminar**  
Elimina un paquete del panel **resultados** .

<a href="" id="rename"></a>**Cambiar nombre**  
Cambia el nombre de un paquete en el panel **resultados** .

<a href="" id="export-list"></a>**Exportar lista**  
Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.

<a href="" id="properties"></a>**Propiedades**  
Muestra el cuadro de diálogo **propiedades** del grupo de licencias seleccionado. La pestaña **General** del cuadro de diálogo **propiedades** muestra información sobre el grupo de licencias y le permite cambiar el valor de hora en el campo ADVERTENCIA de caducidad de la **licencia** . La pestaña **aplicaciones** muestra la lista de aplicaciones asociadas al grupo de licencias.

<a href="" id="help"></a>**Ayuda**  
Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.

## Temas relacionados


[Acerca de las licencias de aplicaciones](about-application-licensing.md)

[Cómo administrar licencias de aplicaciones en la consola de administración de servidor](how-to-manage-application-licenses-in-the-server-management-console.md)

[Consola de administración de servidor: Nodo de licencias de aplicaciones](server-management-console-application-licenses-node.md)

 

 





