---
title: Cómo configurar las aplicaciones publicadas
description: Cómo configurar las aplicaciones publicadas
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824311"
---
# Cómo configurar las aplicaciones publicadas


Las aplicaciones que no son compatibles con el sistema operativo del host se pueden ejecutar en el área de trabajo de MED-V e iniciarse desde el área de trabajo de MED-V de la misma manera en que se inician desde el escritorio, desde el menú Inicio o desde un acceso directo de host local. Las aplicaciones seleccionadas y definidas se denominan aplicaciones publicadas. Los procedimientos de esta sección describen cómo agregar y quitar aplicaciones publicadas.

Una aplicación se puede publicar de una de las siguientes maneras:

-   Como una aplicación: Seleccione una aplicación específica escribiendo en la línea de comandos de la aplicación. Solo se publica la aplicación seleccionada.

-   Como menú: Seleccione una carpeta que contenga varias aplicaciones. Todas las aplicaciones de la carpeta se publican y se muestran como un menú.

## <a href="" id="bkmk-addingapublishedapplication"></a>Cómo agregar una aplicación publicada a un área de trabajo de MED-V


**Para agregar una aplicación al área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V para configurar.

2.  En el panel **aplicaciones** , en la sección **aplicaciones publicadas** , haga clic en **Agregar** para agregar una nueva aplicación.

3.  Configure las propiedades de la aplicación tal y como se describe en la tabla siguiente.

4.  En el menú **Directiva** , seleccione **confirmar**.

    **Nota**  
    Si va a configurar Internet Explorer como una aplicación publicada para garantizar que la redirección web funcione correctamente, asegúrese de que los parámetros no estén entre paréntesis.



**Propiedades de la aplicación publicada**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propiedad</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Habilitado</p></td>
<td align="left"><p>Seleccione esta casilla para habilitar la aplicación publicada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre para mostrar</p></td>
<td align="left"><p>El nombre del acceso directo en el menú Inicio del usuario&#39;s de Windows.</p>
<div class="alert">
<strong>Nota</strong><br/><p>El nombre para mostrar <strong> no distingue </strong> entre mayúsculas y minúsculas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Descripción de la aplicación publicada, que aparece como información sobre herramientas cuando el usuario&#39;s pasa el mouse sobre el acceso directo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Línea de comandos</p></td>
<td align="left"><p>El comando usado para ejecutar la aplicación desde el área de trabajo de MED-V. La ruta de acceso completa es obligatoria, y los parámetros se pueden pasar a la aplicación de manera similar, como en cualquier otro comando de Windows.</p>
<p>En un área de trabajo revertida de MED-V, puede asignar una unidad de red con sintaxis MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; &gt; &lt; ruta de acceso de unidad, &gt; </em> &quot; por ejemplo, &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</p>
<p>Por ejemplo, para publicar el explorador de Windows, use la sintaxis siguiente: &quot; <em> c: &lt; /em &gt; &quot; o &quot; <em> c:\Windows </em> .&quot;</p>
<div class="alert">
<strong>Nota</strong><br/><p>Para tener una resolución de nombres, debe realizar una de las siguientes acciones:</p>
</div>
<div>

</div>
<ul>
<li><p>Configure el DNS en la imagen del área de trabajo base MED-V.</p></li>
<li><p>Compruebe que la resolución DNS está definida en el host y configúrela para usar el DNS de host.</p></li>
<li><p>Use el IP para definir la unidad de red.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Si la ruta de acceso incluye espacios, toda la ruta debe estar entre comillas.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>La ruta de acceso no debe terminar con una barra diagonal inversa ().</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Menú Inicio</p></td>
<td align="left"><p>Seleccione esta casilla para crear un acceso directo para la aplicación en el menú Inicio del usuario&#39;s Windows.</p></td>
</tr>
</tbody>
</table>



Todas las aplicaciones publicadas aparecen como accesos directos en el menú **Inicio** de Windows (**iniciar &gt; todas &gt; las aplicaciones de MED-V**).

## Cómo quitar una aplicación publicada de un área de trabajo de MED-V


**Para quitar una aplicación del área de trabajo de MED-V**

1.  Haga clic en un área de trabajo de MED-V.

2.  En el panel **aplicaciones** , en la sección **aplicaciones publicadas** , seleccione una aplicación para quitarla.

3.  Haga clic en **quitar**.

    La aplicación se quita de la lista de aplicaciones publicadas.

4.  En el menú **Directiva** , seleccione **confirmar**.

## Cómo agregar un menú publicado a un área de trabajo de MED-V


**Para agregar un menú publicado al área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V para configurar.

2.  En el panel **aplicaciones** , en la sección **menús publicados** , haga clic en **Agregar** para agregar un menú nuevo.

3.  Configure las propiedades del menú tal como se describe en la tabla siguiente.

4.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades de menú publicadas**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propiedad</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Habilitado</p></td>
<td align="left"><p>Seleccione esta casilla para habilitar el menú publicado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre para mostrar</p></td>
<td align="left"><p>El nombre del acceso directo en el menú Inicio del usuario&#39;s de Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>La descripción, que aparece como una información sobre herramientas cuando el usuario&#39;s el mouse se desplaza sobre el acceso directo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Carpeta en el área de trabajo</p></td>
<td align="left"><p>Seleccione la carpeta que desea publicar como un menú que contiene todas las aplicaciones de la carpeta.</p>
<p>El texto que se muestra es una ruta de acceso relativa desde la carpeta programas.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si se deja en blanco, todos los programas del host se publicarán como un menú.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Todos los menús publicados aparecen como accesos directos en el menú **Inicio** de Windows (**iniciar &gt; todas &gt; las aplicaciones de MED-V**). Puede cambiar el nombre del acceso directo en el campo de **carpeta accesos directos del menú Inicio** .

**Nota**  
Al configurar dos áreas de trabajo de MED-V, se recomienda configurar un nombre diferente para la carpeta de accesos directos del menú Inicio.



## Cómo quitar un menú publicado de un área de trabajo de MED-V


**Para quitar un menú publicado de un área de trabajo de MED-V**

1.  Haga clic en un área de trabajo de MED-V.

2.  En el panel **aplicaciones** , en la sección **menús publicados** , seleccione un menú para quitarlo.

3.  Haga clic en **quitar**.

    El menú se quita de la lista de menús publicados.

4.  En el menú **Directiva** , seleccione **confirmar**.

## Ejecutar una aplicación publicada desde una línea de comandos en el cliente


El administrador puede ejecutar aplicaciones publicadas desde cualquier ubicación, como un acceso directo de escritorio, con el siguiente comando:

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**Nota**  
El área de trabajo de MED-V en la que se define la aplicación publicada debe estar ejecutándose.



## Temas relacionados


[Cómo modificar una aplicación publicada con la configuración avanzada](how-to-edit-a-published-application-with-advanced-settings.md)

[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









