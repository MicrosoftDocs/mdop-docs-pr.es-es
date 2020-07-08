---
title: Cómo implementar una imagen de área de trabajo
description: Cómo implementar una imagen de área de trabajo
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827011"
---
# Cómo implementar una imagen de área de trabajo


Al usar un paquete de implementación, se puede implementar una nueva imagen en los equipos cliente de una de las siguientes maneras:

-   [Descarga de Internet](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Preensayo de imagen preconfigurada](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [Implementar la imagen dentro del paquete de implementación](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Cómo implementar una imagen de área de trabajo a través de la web


**Para implementar una imagen de área de trabajo a través de la web**

1.  Cargue la imagen de MED-V en el servidor.

    Para obtener información sobre cómo cargar la imagen, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).

2.  Cree un paquete de implementación e incluya la ruta de acceso del servidor a la ubicación de la imagen.

    Para obtener información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).

3.  Implementar el paquete para los usuarios finales.

    Para obtener información sobre cómo implementar el paquete, vea [Cómo instalar el cliente de MED-V](how-to-install-med-v-clientdeployment-package.md).

    El cliente MED-V se instala y se inicia por primera vez. Al iniciar por primera vez, el cliente descarga la imagen desde la dirección del servidor especificada en la instalación del cliente.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Cómo implementar una imagen de área de trabajo con preensayo de imagen


**Para implementar una imagen de área de trabajo con preensayo de imagen**

1.  Cree una carpeta preconfigurada de imagen e inserte la imagen en la carpeta.

    Para obtener información sobre la configuración del ensayo previo de la imagen, consulte [Cómo configurar la preconfiguración preconfigurada de imagen](how-to-configure-image-pre-staging.md).

2.  Cree un paquete de implementación e incluya la ruta de acceso a la carpeta previa de la imagen.

    Para obtener información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).

3.  Implementar el paquete para los usuarios finales.

    Para obtener información sobre cómo implementar el paquete, vea [Cómo instalar el cliente de MED-V](how-to-install-med-v-clientdeployment-package.md).

    El cliente MED-V se instala y se inicia por primera vez. Al iniciar por primera vez, el cliente obtiene la imagen de la carpeta prestage especificada en la instalación del cliente.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a>Cómo implementar una imagen de área de trabajo con un paquete de implementación


**Para implementar una imagen de área de trabajo con un paquete de implementación**

1.  Cree un paquete de implementación e incluya la imagen en el paquete.

    Para obtener información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).

2.  Implementar el paquete para los usuarios finales.

    Para obtener información sobre cómo implementar el paquete, vea [Cómo instalar el cliente de MED-V](how-to-install-med-v-clientdeployment-package.md).

    La imagen se importa al host como parte de la instalación del paquete.

## Temas relacionados


[Cómo configurar el servidor de distribución de imagen web](how-to-configure-the-image-web-distribution-server.md)

[Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md)

 

 





