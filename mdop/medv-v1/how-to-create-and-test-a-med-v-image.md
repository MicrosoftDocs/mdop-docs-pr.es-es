---
title: Cómo crear y probar una imagen de MED-V
description: Cómo crear y probar una imagen de MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827041"
---
# Cómo crear y probar una imagen de MED-V


El administrador de MED-V crea una imagen de MED-V para que se pueda cargar, asociar a un área de trabajo de MED-V y, después, distribuirse al cliente a través de la web, agregar a un paquete de MED-V o descargarse al cliente mediante un sistema de terceros. Se recomienda crear primero una imagen de prueba y probarla en el cliente de MED-V antes de implementarla.

Al crear una imagen de MED-V, pasa por las siguientes fases:

1.  **Imagen de prueba local**: una imagen básica que se puede probar de forma local.

2.  **Imagen empaquetada local**: después de probar la imagen, la imagen se empaqueta como existía antes de la prueba. Los cambios realizados durante las pruebas no se incluyen en la imagen empaquetada.

3.  **Imagen empaquetada en el servidor**: la imagen empaquetada se carga en el servidor.

## Cómo crear una imagen de prueba de MED-V


**Para crear una nueva imagen de prueba de MED-V**

1.  Haga clic en el botón de administración de **imágenes** .

    Aparece el módulo **imágenes** .

    -   El módulo **imágenes** consta de los siguientes paneles:

        -   **Imágenes de prueba locales**: imágenes locales no empaquetadas.

        -   **Imágenes empaquetadas locales**: todas las imágenes empaquetadas en el equipo local.

        -   **Imágenes empaquetadas en el servidor**: todas las imágenes que se han embalado y cargado en el servidor.

    -   En las imágenes **empaquetadas locales** y **en las imágenes empaquetadas** de los paneles del servidor, la versión más reciente de cada imagen se muestra como nodo primario. Haga clic en el nodo principal para ver todas las demás versiones existentes de la imagen.

2.  En el panel **imágenes de prueba local** , haga clic en **nuevo**.

3.  En el cuadro de diálogo **prueba de creación de imagen** , seleccione la imagen de la máquina virtual que desea configurar como imagen de prueba de MED-V de una de las siguientes maneras:

    -   En el campo archivo de **imagen base** , escriba la ruta de acceso completa del directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.

    -   Haga clic en **examinar** para buscar el directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.

4.  En el campo **nombre de imagen** , escriba o seleccione el nombre que desee.

    **Nota:**  Los siguientes caracteres no se pueden incluir en el nombre de la imagen: Space " &lt; &gt; | \\ / : \* ?

     

5.  Haga clic en **Aceptar**.

    Se crea una nueva imagen de prueba de MED-V en el equipo host con las propiedades definidas en la tabla siguiente.

    Para obtener más información sobre la configuración de la imagen del área de trabajo de MED-V, consulte [configuración de directivas de área de trabajo de Med-v](configuring-med-v-workspace-policies.md).

**Propiedades de las imágenes de prueba local**

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
<td align="left"><p>El nombre de la imagen de prueba tal como se definió cuando el administrador creó la imagen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ruta de la imagen</p></td>
<td align="left"><p>La ruta de acceso local de la imagen de prueba.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Crear</p></td>
<td align="left"><p>La fecha de creación de la imagen de prueba.</p></td>
</tr>
</tbody>
</table>

 

## Cómo probar una imagen de MED-V desde el cliente MED-V


Después de crear una imagen de prueba de MED-V, use el siguiente procedimiento para probar la imagen de forma local.

**Para probar una imagen de MED-V**

1.  Haga clic en el botón Administración de **directivas** .

2.  En el módulo de **directivas** , asigne la imagen de prueba de Med-v a un área de trabajo de Med-v mediante el siguiente procedimiento:

    1.  Haga clic en la pestaña **máquina virtual** .

    2.  En el campo de la **imagen asignada** , seleccione la imagen de prueba de MED-V que ha creado. Si la imagen de prueba no está en la lista, haga clic en **Actualizar**.

    3.  En la barra de herramientas, haga clic en **Guardar cambios**.

3.  Configure cualquier otra configuración de área de trabajo de MED-V que desee probar. Para obtener más información, consulte [configuración de directivas de área de trabajo de MED-V](configuring-med-v-workspace-policies.md).

4.  Inicie el cliente MED-V.

5.  En el cuadro de confirmación **confirmar ejecución de prueba** , haga clic en **usar imagen de prueba**.

6.  Pruebe la imagen de prueba del área de trabajo MED-V.

    Para obtener información sobre cómo iniciar y ejecutar el cliente de MED-V, consulte [operaciones de cliente de Med-v](med-v-client-operations.md).

**Nota:**  Mientras prueba una imagen, no abra VPC y realice cambios en la imagen.

 

**Nota:**  Al probar una imagen, los cambios no se guardan en la imagen entre sesiones; en su lugar, se guardan en un archivo temporal independiente. Esto garantiza que cuando la imagen se haya embalado y ejecutado en el entorno de producción, será la imagen original y limpia.

 

## Temas relacionados


[Creación de una imagen de Virtual PC para MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Configuración de directivas de área de trabajo de MED-V](configuring-med-v-workspace-policies.md)

[Operaciones de cliente de MED-V](med-v-client-operations.md)

 

 





