---
title: Cómo cargar una imagen de MED-V en el servidor
description: Cómo cargar una imagen de MED-V en el servidor
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825701"
---
# Cómo cargar una imagen de MED-V en el servidor


Después de probar una imagen de MED-V, se puede embalar y cargar en el servidor. Para obtener información sobre cómo configurar un servidor de distribución Web de imágenes, consulte [Cómo configurar el servidor de distribución Web de imágenes](how-to-configure-the-image-web-distribution-server.md).

Una vez que una imagen de MED-V se empaqueta y se carga en el servidor, se puede distribuir a los usuarios mediante un centro de distribución de software empresarial o los usuarios pueden descargarla mediante un paquete de implementación. Para obtener información sobre la implementación con un centro de distribución de software empresarial, consulte [implementación de un área de trabajo de MED-V con un sistema de distribución de software empresarial](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md). Para obtener información sobre la implementación con un paquete, consulte [implementación de un área de trabajo de MED-V con un paquete de implementación](deploying-a-med-v-workspace-using-a-deployment-package.md).

**Nota**  
Antes de cargar una imagen, compruebe que un proxy web no está definido en la configuración del explorador y que Windows Update no se está ejecutando actualmente.



**Para cargar una imagen de MED-V en el servidor**

1.  En el panel **imágenes empaquetadas locales** , seleccione la imagen que ha creado.

2.  Haga clic en **cargar**.

    La imagen se carga en el servidor. Esto puede demorar bastante tiempo.

    Las imágenes del servidor se definen con las propiedades que aparecen en la tabla siguiente.

**Imágenes empaquetadas en las propiedades del servidor**

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

[Cómo empaquetar una imagen de MED-V](how-to-pack-a-med-v-image.md)









