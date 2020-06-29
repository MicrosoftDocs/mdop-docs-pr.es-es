---
title: Cómo empaquetar una imagen de MED-V
description: Cómo empaquetar una imagen de MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824680"
---
# Cómo empaquetar una imagen de MED-V


Una imagen de MED-V debe estar empaquetada antes de que se pueda agregar a un paquete de implementación o cargar en el servidor.

**Para crear una imagen de MED-V empaquetada**

1.  Haga clic en el botón de administración de **imágenes** .

2.  En el módulo **imágenes** , en el panel **imágenes empaquetadas locales** , haga clic en **nuevo**.

3.  En el cuadro de diálogo **creación de imágenes empaquetadas** , seleccione la imagen de la máquina virtual de una de las siguientes maneras:

    -   En el campo **archivo de imagen base** , escriba la ruta de acceso completa del directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.

    -   Haga clic en **examinar** para buscar el directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.

4.  Especifique el nombre de la nueva imagen siguiendo uno de estos procedimientos:

    -   En el campo **nombre de imagen** , escriba el nombre que desee.

        **Nota**  
        Los siguientes caracteres no se pueden incluir en el nombre de la imagen: Space " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. Haga clic en **Aceptar**.

   Se crea una nueva imagen empaquetada de MED-V en el equipo host con las propiedades definidas en la tabla siguiente.

**Nota**  
En las imágenes **empaquetadas locales** y **en las imágenes empaquetadas** de los paneles del servidor, la versión más reciente de cada imagen se muestra como nodo primario. Haga clic en el nodo principal para ver todas las demás versiones existentes de la imagen.



**Propiedades de imágenes empaquetadas locales**

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
<td align="left"><p>Nombre de imagen</p></td>
<td align="left"><p>El nombre de la imagen empaquetada tal y como se definió cuando el administrador creó la imagen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión</p></td>
<td align="left"><p>La versión de la imagen que se muestra.</p>
<div class="alert">
<strong>Nota</strong><br/><p>A menos que se eliminen, se guardarán todas las versiones anteriores.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Tamaño de archivo (comprimido)</p></td>
<td align="left"><p>El tamaño físico comprimido de la imagen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tamaño de la imagen (sin comprimir)</p></td>
<td align="left"><p>El tamaño físico sin comprimir de la imagen.</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Cómo instalar el cliente MED-V y la consola de administración de MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de una imagen de Virtual PC para MED-V](creating-a-virtual-pc-image-for-med-v.md)









