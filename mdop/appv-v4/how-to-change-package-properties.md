---
title: Cómo cambiar las propiedades del paquete
description: Cómo cambiar las propiedades del paquete
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818041"
---
# Cómo cambiar las propiedades del paquete


Puede usar los procedimientos siguientes para modificar un nombre de paquete de virtualización de aplicaciones y sus comentarios asociados.

Si esta es la primera vez que se ha creado el paquete, también puede cambiar el tamaño de bloque del parámetro de secuenciación, que determina cómo se transmite un paquete de aplicación secuencial desde un servidor de virtualización de aplicaciones a un cliente de escritorio de virtualización de aplicaciones.

**Nota:**  Cuando seleccione un tamaño de bloque, tenga en cuenta el tamaño del archivo SFT y el ancho de banda de la red. Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda. Los archivos con tamaños de bloque mayores pueden transmitirse más rápido, pero usan más ancho de banda de la red. Mediante la experimentación, puede descubrir el tamaño de bloque óptimo para las aplicaciones de transmisión en su red.

 

El resto de las propiedades del paquete en la ficha **propiedades** se genera automáticamente y no se puede modificar en esta pestaña.

**Para cambiar el nombre del paquete o los comentarios**

1.  Haga clic en la pestaña **propiedades** .

2.  En el cuadro de texto **nombre del paquete** , escriba o edite el nombre único que se usa para el paquete, que puede contener varias aplicaciones.

3.  En el cuadro de texto **comentarios** , si lo desea, puede escribir o editar cualquier comentario. El procedimiento recomendado es proporcionar información detallada sobre el paquete y la secuenciación.

4.  En el menú **archivo** , seleccione **Guardar**.

**Para cambiar el tamaño de bloque**

1.  Haga clic en la pestaña **propiedades** .

2.  En la lista desplegable **bloquear tamaño** , seleccione **4 KB**, **16 kb**, **32 KB**o **64 KB**.

3.  En el menú **archivo** , seleccione **Guardar**.

## Temas relacionados


[Acerca de la pestaña Propiedades](about-the-properties-tab.md)

[Consola de secuenciador](sequencer-console.md)

 

 





