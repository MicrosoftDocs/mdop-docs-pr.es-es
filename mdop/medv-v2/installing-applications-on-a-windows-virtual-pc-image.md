---
title: Instalar aplicaciones en una imagen de Windows Virtual PC
description: Instalar aplicaciones en una imagen de Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826831"
---
# Instalar aplicaciones en una imagen de Windows Virtual PC


Después de crear una imagen de Windows Virtual PC para usarla con Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, puede instalar otros componentes que sean útiles al ejecutar MED-V, como un sistema de distribución electrónica de software (ESD) y software antivirus.

La siguiente sección proporciona información para ayudarle a instalar software en la imagen de MED-V.

**PRECAUCIÓN**  Para facilitar la administración de áreas de trabajo de MED-V después de la implementación, le recomendamos que limite el número de componentes que instale en la imagen de MED-V a los componentes necesarios o que sean útiles cuando use MED-V. Por ejemplo, aunque no es necesario ejecutar MED-V, puede instalar un sistema ESD para usar más tarde para instalar aplicaciones en un área de trabajo de MED-V y software antivirus para la seguridad de la imagen.

 

**Instalar software en una imagen de MED-V**

1.  Si no se está ejecutando en este momento, abra su máquina virtual de MED-V.

    1.  Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC** y, a continuación, haga clic en **Windows Virtual PC**.

    2.  Haga doble clic en su máquina virtual de MED-V.

2.  Desde el sistema operativo de la máquina virtual, busque los archivos de instalación del software que desea instalar.

3.  Siga las instrucciones de instalación proporcionadas por el proveedor del software.

    **Nota:**  Una vez completada la instalación, es posible que tenga que cerrar y reiniciar la máquina virtual.

     

Repita estos pasos para cualquier software o aplicación que desee instalar en la imagen de MED-V. Le recomendamos que limite el número de aplicaciones que preinstale en la imagen. El proceso recomendado para instalar aplicaciones y otro software de la imagen es preinstalar ahora un sistema ESD y usarlo más adelante para implementar el software en la imagen. Como alternativa, también puede usar la Directiva de grupo o App-V para agregar o quitar aplicaciones en un área de trabajo de MED-V. Para obtener más información, vea [Administración de aplicaciones implementadas en áreas de trabajo de MED-V](managing-applications-deployed-to-med-v-workspaces.md).

Para obtener más información sobre cómo instalar software en una imagen virtual, consulte los artículos siguientes:

-   [Publicar y usar aplicaciones virtuales](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .

-   [Ayuda de Virtual PC de Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Una vez que haya instalado todo el software que desea en la imagen de MED-V, la imagen estará lista para empaquetarse.

## Temas relacionados


[Configurar una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Preparar una imagen de MED-V](prepare-a-med-v-image.md)

 

 





