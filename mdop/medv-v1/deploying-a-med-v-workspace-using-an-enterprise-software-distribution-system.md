---
title: Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa
description: Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823630"
---
# Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa


El cliente de MED-V se puede distribuir mediante un sistema de distribución de software empresarial, como Microsoft System Center Configuration Manager.

**Nota:**  Si MED-V se instala con Microsoft System Center Configuration Manager, al crear un paquete para MED-V, establezca el modo de ejecución en derechos administrativos.

 

Antes de implementar MED-V mediante un sistema de distribución de software empresarial, asegúrese de haber creado una imagen de MED-V lista para la implementación. Para obtener más información sobre cómo crear una imagen de MED-V, vea [crear una imagen de Med-v](creating-a-med-v-image.md).

Después de preparar la imagen de MED-V, considere el mejor método para distribuir la imagen en su entorno. La imagen se puede distribuir de una de las siguientes maneras:

-   Cargados en Internet y distribuidos a través de descargas Web, con la opción de transferencia de recorte.

-   Se distribuye con preensayo de imágenes.

## Implementar la imagen a través de la web


Si va a implementar la imagen a través de Internet, cargue la imagen de MED-V en un servidor de distribución Web de imágenes. Para obtener información sobre cómo configurar un servidor de distribución Web de imágenes, consulte [Cómo configurar el servidor de distribución Web de imágenes](how-to-configure-the-image-web-distribution-server.md). Para obtener información sobre cómo cargar una imagen en el servidor, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).

## Implementación de la imagen a través del ensayo previo


Si va a implementar la imagen a través del ensayo previo de la imagen, configure la carpeta prestage y empuje la imagen de MED-V a la carpeta. Para obtener más información sobre cómo configurar preensayo de imagen, consulte [Cómo configurar la preconfiguración de imagen previa](how-to-configure-image-pre-staging.md).

**Nota:**  Si está usando preensayo de imagen, es importante que configure la carpeta prestage de la imagen antes de insertar el paquete. msi de cliente. La ruta de la carpeta debe incluirse en el paquete Client. msi.

 

Por último, inserte el paquete Client. msi con su centro de distribución de software empresarial. A continuación, se puede instalar MED-V y se debe implementar la imagen. Para obtener más información sobre cómo instalar el cliente de MED-V, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientesds.md). Para obtener más información sobre la implementación de la imagen, consulte [cómo implementar una imagen de área de trabajo](how-to-deploy-a-workspace-imageesds.md).

 

 





