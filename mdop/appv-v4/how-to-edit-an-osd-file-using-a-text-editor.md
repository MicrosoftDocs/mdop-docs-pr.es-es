---
title: Cómo editar un archivo OSD mediante un editor de texto
description: Cómo editar un archivo OSD mediante un editor de texto
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817441"
---
# Cómo editar un archivo OSD mediante un editor de texto


Use el siguiente procedimiento para editar un archivo de descriptor de software abierto (OSD) con un editor de texto.

**Para editar un archivo OSD con un editor de texto**

1.  Abra el archivo OSD con cualquier editor de texto XML o ASCII, por ejemplo, el Bloc de notas de Microsoft.

    **Nota:**  Antes de modificar el archivo OSD, lea el esquema preestablecido por el archivo XSD en el directorio de instalación. Si no sigue este esquema, puede haber errores que impidan que una aplicación secuenciada se inicie correctamente.

     

2.  Edite el archivo OSD con el editor de texto XML o ASCII que prefiera, y cumpla con el esquema prescrito y las siguientes pautas:

    1.  Asegúrese de que los elementos con nombre están anidados dentro del &lt; &gt; elemento raíz SOFTPKG.

    2.  Asegúrese de que los nombres de los elementos están en mayúsculas.

    3.  Ten en cuenta que los valores de atributo distinguen mayúsculas de minúsculas.

    4.  Escriba con cuidado y observe las especificaciones de XML.

## Temas relacionados


[Acerca de la pestaña OSD](about-the-osd-tab.md)

[Cómo editar un archivo OSD](how-to-edit-an-osd-file.md)

[Elementos de archivo OSD](osd-file-elements.md)

 

 





