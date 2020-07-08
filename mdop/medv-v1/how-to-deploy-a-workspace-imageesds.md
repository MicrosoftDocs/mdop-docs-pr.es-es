---
title: Cómo implementar una imagen de área de trabajo
description: Cómo implementar una imagen de área de trabajo
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827001"
---
# Cómo implementar una imagen de área de trabajo


Al usar un sistema de distribución de software empresarial, se puede implementar una nueva imagen en los equipos cliente de una de las siguientes maneras:

-   [Descarga de Internet](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Preensayo de imagen preconfigurada](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Cómo implementar una imagen de área de trabajo a través de la web


**Para implementar una imagen de área de trabajo a través de la web**

1.  Cargue la imagen de MED-V en el servidor.

    Para obtener información sobre cómo cargar la imagen, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).

2.  Con el sistema de distribución de software de empresa, instale el paquete de cliente MED-V. msi en los equipos de los usuarios.

    Para obtener información sobre cómo instalar el paquete de cliente MED-V. msi, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientesds.md).

    El cliente MED-V se instala y se inicia por primera vez. Al iniciar por primera vez, el cliente descarga la imagen desde la dirección del servidor especificada en la instalación del cliente.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Cómo implementar una imagen de área de trabajo con preensayo de imagen


**Para implementar una imagen de área de trabajo con preensayo de imagen**

1.  Cree una carpeta preconfigurada de imagen e inserte la imagen en la carpeta.

    Para obtener información sobre la configuración del ensayo previo de la imagen, consulte [Cómo configurar la preconfiguración preconfigurada de imagen](how-to-configure-image-pre-staging.md).

2.  Con el sistema de distribución de software de empresa, instale el paquete de cliente MED-V. msi en los equipos de los usuarios.

    Para obtener información sobre cómo instalar el paquete de cliente MED-V. msi, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientesds.md).

    El cliente MED-V se instala y se inicia por primera vez. Al iniciar por primera vez, el cliente obtiene la imagen de la carpeta prestage especificada en la instalación del cliente.

## Temas relacionados


[Cómo configurar el servidor de distribución de imagen web](how-to-configure-the-image-web-distribution-server.md)

 

 





