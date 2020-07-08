---
title: Actualización de una imagen de área de trabajo de MED-V
description: Actualización de una imagen de área de trabajo de MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825851"
---
# Actualización de una imagen de área de trabajo de MED-V


Una imagen se puede actualizar de una de las siguientes maneras:

-   La actualización se puede insertar en el sistema operativo invitado usando su sistema de distribución de software empresarial.

-   La actualización se puede cargar en el servidor de distribución Web de imágenes y, a continuación, el cliente la descarga y se aplica a la imagen de MED-V.

-   La imagen base de MED-V se puede actualizar y volver a implementar.

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a>Cómo actualizar una imagen de MED-V con un sistema de distribución de software empresarial


**Para actualizar una imagen de MED-V con un sistema de distribución de software empresarial**

-   Consulte la documentación del sistema que esté usando.

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a>Cómo actualizar una imagen de MED-V con la descarga de Web


**Para actualizar una imagen de MED-V con la descarga de Web**

1.  En administración de MED-V, en la pestaña **máquina virtual** , asegúrese de que se aplica la siguiente configuración a las directivas de área de trabajo de Med-v que están asociadas a la imagen de Med-v que se está actualizando:

    -   La casilla de verificación **sugerir actualización cuando esté disponible una nueva versión** está activada.

    -   De forma opcional, la casilla de verificación los **clientes deberían usar la transferencia de recorte al descargar imágenes para esta área de trabajo** está activada.

    Para obtener más información, consulte [Cómo aplicar la configuración de la máquina virtual a un área de trabajo de MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).

2.  Cargue la actualización de imagen en el servidor de distribución Web de imágenes.

    Todos los clientes con imágenes que necesitan actualizarse automáticamente descargan la actualización y la aplican a la imagen.

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a>Cómo actualizar una imagen base de MED-V


**Para actualizar una imagen base de MED-V**

1.  Abra la imagen existente en virtual PC2007.

2.  Realice los cambios necesarios en la imagen, actualizando la imagen (por ejemplo, instalando nuevo software).

3.  Cierre PC2007 virtual.

4.  Pruebe la imagen.

5.  Después de probar la imagen, empaquela en el repositorio local con el mismo nombre que la imagen existente.

    **Nota:**  Si asigna a la imagen un nombre diferente al de la versión existente, se creará una nueva imagen en lugar de una nueva versión de la imagen existente.

     

6.  Cargue la nueva versión en el servidor, insértela en la carpeta preconfigurada de la imagen o distribúyala a través de un paquete de implementación.

## Temas relacionados


[Creación de una imagen de MED-V](creating-a-med-v-image.md)

[Cómo actualizar una imagen de MED-V](how-to-update-a-med-v-image.md)

[Configuración de directivas de área de trabajo de MED-V](configuring-med-v-workspace-policies.md)

[Cómo configurar el servidor de distribución de imagen web](how-to-configure-the-image-web-distribution-server.md)

 

 





