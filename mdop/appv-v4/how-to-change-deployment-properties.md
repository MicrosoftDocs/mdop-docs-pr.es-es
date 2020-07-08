---
title: Cómo cambiar las propiedades de implementación
description: Cómo cambiar las propiedades de implementación
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818061"
---
# Cómo cambiar las propiedades de implementación


Puede usar los procedimientos siguientes para cambiar la información de la pestaña **implementación** para una aplicación que está transformando, lo que incluye la dirección URL del servidor de virtualización de aplicaciones, los sistemas operativos requeridos por las aplicaciones virtualizadas y las opciones de salida de la aplicación virtual que se van a instalar.

**Para cambiar la dirección URL del servidor**

1.  Seleccione el protocolo de transmisión por secuencias en el cuadro de lista desplegable.

2.  Escriba el nombre de host del servidor de aplicaciones virtual o del equilibrador de carga del grupo de servidores. Puede usar el nombre de host o la dirección IP reales.

3.  Especifique el número de puerto en el que el servidor de aplicaciones virtual o el equilibrador de carga escuchará una solicitud de cliente de escritorio de virtualización de aplicaciones para la aplicación transmitida.

4.  Especifique la ruta de acceso relativa en el servidor de aplicaciones virtual donde se encuentra almacenado el paquete de software.

**Para cambiar los requisitos de los sistemas operativos de la aplicación**

1.  Para agregar los sistemas operativos necesarios, selecciónelos en la lista **disponible** y haga clic en el botón de flecha que apunta al control de lista sistemas operativos **seleccionados** .

2.  Para quitar un sistema operativo, selecciónelo en el control de lista **seleccionado** y haga clic en el botón de flecha que apunta al control de lista sistemas operativos **disponibles** .

**Para cambiar las opciones de resultados de la aplicación**

1.  En la lista desplegable **algoritmo de compresión** , seleccione el método de compresión que desee usar al transmitir la aplicación.

2.  Seleccione la casilla **exigir descriptores de seguridad** para garantizar que los descriptores de seguridad de las aplicaciones empaquetadas se aplican al implementarse.

3.  Seleccione **generar archivo de diferencias** para generar un archivo de diferencias para la aplicación a partir de la versión anterior de la secuencia.

4.  Seleccione **generar paquete de Microsoft Windows Installer (MSI)** para crear un paquete de instalador.

## Temas relacionados


[Acerca de la pestaña Implementación](about-the-deployment-tab.md)

[Consola de secuenciador](sequencer-console.md)

 

 





