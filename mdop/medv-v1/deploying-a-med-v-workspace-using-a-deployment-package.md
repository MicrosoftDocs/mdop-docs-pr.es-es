---
title: Implementación de un área de trabajo de MED-V mediante un paquete de implementación
description: Implementación de un área de trabajo de MED-V mediante un paquete de implementación
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823631"
---
# Implementación de un área de trabajo de MED-V mediante un paquete de implementación


La instalación del paquete de implementación proporciona un método de instalación del cliente de MED-V junto con todos los requisitos previos necesarios, así como cualquier configuración predefinida por el administrador.

Al usar un paquete de implementación, el paquete se distribuye a través de una red compartida o un medio extraíble. La imagen se puede incluir en el paquete o se puede distribuir por separado.

Antes de crear un paquete de implementación, asegúrese de que ha creado una imagen de MED-V lista para la implementación. Para obtener más información sobre cómo crear una imagen de MED-V, vea [crear una imagen de Med-v](creating-a-med-v-image.md).

Después de preparar la imagen de MED-V, considere el mejor método para distribuir la imagen en su entorno. La imagen se puede distribuir de una de las siguientes maneras:

-   Cargados en Internet y distribuidos a través de descargas Web, con la tecnología de transferencia de recorte opcional.

-   Se distribuye con preensayo de imágenes.

-   Incluido en el paquete de implementación y distribuido junto con todos los demás componentes de MED-V.

Si la imagen se va a incluir en el paquete, no es necesario realizar ninguna otra configuración para la imagen. Si la imagen no se va a incluir en el paquete de implementación, realice una de las siguientes acciones:

-   Si va a implementar la imagen a través de Internet, cargue la imagen MED-V en el servidor de distribución Web de imágenes. Para obtener información sobre cómo configurar un servidor de distribución Web de imágenes, consulte [Cómo configurar el servidor de distribución Web de imágenes](how-to-configure-the-image-web-distribution-server.md). Para obtener información sobre cómo cargar una imagen en el servidor, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).

-   Si va a implementar la imagen a través del ensayo previo de la imagen, configure la carpeta prestage y empuje la imagen de MED-V a la carpeta. Para obtener más información sobre la configuración del ensayo previo de la imagen, consulte [Cómo configurar la preconfiguración de imagen previa](how-to-configure-image-pre-staging.md).

**Nota:**  Si está usando preensayo de imagen, es importante que configure la carpeta previa de la imagen antes de crear el paquete de implementación. La ruta de acceso a la carpeta debe incluirse en el paquete de implementación.

 

Por último, cree el paquete de implementación. Para obtener más información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md). Una vez completado el paquete, distribúyalo para su implementación.

Una vez distribuido el paquete de implementación, se puede instalar el cliente de MED-V y se implementa la imagen. Para obtener más información sobre cómo instalar el cliente de MED-V, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientdeployment-package.md). Para obtener más información sobre la implementación de la imagen, consulte [cómo implementar una imagen de área de trabajo](how-to-deploy-a-workspace-imagedeployment-package.md).

 

 





