---
title: Instalar y quitar una aplicación en el área de trabajo de MED-V
description: Instalar y quitar una aplicación en el área de trabajo de MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827220"
---
# Instalar y quitar una aplicación en el área de trabajo de MED-V


Las aplicaciones que no son compatibles con el sistema operativo del host se pueden ejecutar en el área de trabajo de MED-V y se pueden abrir en el área de trabajo de MED-V de la misma manera en que se abren desde el equipo host, en el menú **Inicio** o mediante un acceso directo de localhost.

Después de implementar un área de trabajo de MED-V, tiene varias opciones diferentes disponibles para instalar y quitar aplicaciones en el área de trabajo de MED-V. Entre estas opciones se incluyen las siguientes:

-   [Uso de directivas de grupo](#bkmk-grouppolicy)

-   [Uso de un sistema electrónico de distribución de software](#bkmk-esd)

-   [Usar la virtualización de aplicaciones (APP-V)](#bkmk-appv)

-   [Actualización de la imagen principal](#bkmk-coreimage)

**Importante**  Para asegurarse de que una aplicación instalada se publique automáticamente en el host, instale la aplicación en la máquina virtual para **todos los usuarios**. Para obtener más información sobre la publicación de aplicaciones, vea [Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).

 

**Sugerencia**  MED-V no admite el redireccionamiento de invitado a host para la administración de contenido, como, por ejemplo, hacer doble clic en un documento de Microsoft Word en Internet Explorer en el área de trabajo de MED-V. Por lo tanto, las aplicaciones necesarias, como Microsoft Word, deben instalarse en el área de trabajo de MED-V para proporcionar la funcionalidad de administración de contenido predeterminada que puede esperar un usuario final.

 

## <a href="" id="bkmk-grouppolicy"></a> Agregar y quitar aplicaciones mediante la Directiva de grupo


Puede usar la Directiva de grupo y los objetos de directiva de grupo para asignar o publicar aplicaciones a todas o algunas áreas de trabajo de MED-V de su empresa. Para las aplicaciones asignadas, cuando un usuario final inicia sesión en su equipo, la aplicación aparece en el menú **Inicio** . Cuando seleccionan la nueva aplicación por primera vez, la aplicación se instala y está lista para su uso. Para las aplicaciones publicadas, la aplicación no aparece en el menú **Inicio** . Solo está disponible para que el usuario final la instale mediante **Agregar o quitar programas** en el **Panel de control** o al abrir un archivo asociado a la aplicación.

También puede usar la Directiva de grupo y los objetos de directiva de grupo de la misma manera para quitar aplicaciones del área de trabajo de MED-V.

Para obtener más información acerca de cómo agregar y quitar aplicaciones con la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

## <a href="" id="bkmk-esd"></a> Agregar y quitar aplicaciones con un sistema ESD


Un sistema de distribución electrónica de software (ESD) está diseñado para implementar de forma eficaz software y otra información en muchos equipos diferentes a través de conexiones de red. Si su organización usa un sistema ESD para implementar software, puede usarlo para agregar y quitar aplicaciones en áreas de trabajo de MED-V, de la misma manera que agrega y quita aplicaciones en equipos físicos.

## <a href="" id="bkmk-appv"></a> Agregar y quitar aplicaciones con APP-V


Microsoft Application Virtualization (App-V) proporciona la capacidad administrativa de poner las aplicaciones a disposición de los equipos de los usuarios finales sin tener que instalar las aplicaciones directamente en esos equipos. Es posible que desee usar MED-V y App-V conjuntamente si, por ejemplo, su organización tiene aplicaciones que ha secuenciado con App-V en Windows XP y la resecuenciación retrasa la migración a Windows 7.

Puede usar MED-V junto con App-V para agregar y quitar aplicaciones virtuales en un área de trabajo de MED-V implementada. Para administrar las aplicaciones de esta manera, primero debe instalar el agente de App-V en el sistema operativo invitado MED-V. Después, puede usar App-V en el área de trabajo de MED-V para agregar y quitar las aplicaciones virtuales.

Para obtener más información sobre cómo instalar y usar App-V, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

**Importante**  Las aplicaciones de App-V que publique en el área de trabajo MED-V tienen asociaciones de tipo de archivo que no se pueden redirigir desde el equipo host a la máquina virtual invitada. Sin embargo, el usuario final aún puede acceder a estos tipos de archivo haciendo clic en **archivo**y, a continuación, haciendo clic en **abrir** en la aplicación de App-V publicada.

Para forzar el redireccionamiento de esas asociaciones de tipo de archivo, consulte App-V para las asociaciones de tipos de archivo asignados escribiendo lo siguiente en un símbolo del sistema en la máquina virtual invitada: **sftmime/Query OBJ: tipo**. A continuación, asigne esas asociaciones de tipos de archivo en el equipo host.

 

## <a href="" id="bkmk-coreimage"></a> Agregar y quitar aplicaciones en la imagen principal


Aunque no se considere un procedimiento recomendado por MED-V, puede Agregar y quitar aplicaciones directamente en la imagen principal. Después de agregar o quitar una aplicación, puede volver a implementar el área de trabajo de MED-V en su empresa, de la misma manera en que lo implementó originalmente.

Para obtener más información sobre cómo agregar o quitar aplicaciones en la imagen principal, consulte [instalar aplicaciones en una imagen de Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md).

**Importante**  No se recomienda este método de administración de aplicaciones. Si agrega o quita aplicaciones en la imagen principal y vuelve a implementar el área de trabajo de MED-V en su empresa, la configuración debe volver a ejecutarse y todos los datos guardados en la máquina virtual se perderán.

 

**Nota:**  Aunque una aplicación se instala en un área de trabajo de MED-V, también es posible que tenga que publicar la aplicación antes de que esté disponible para el usuario final. Por ejemplo, es posible que tenga que publicar una aplicación instalada si la instalación no ha creado automáticamente un acceso directo en el menú **Inicio** . Del mismo modo, para anular la publicación de una aplicación, es posible que tenga que quitar manualmente un acceso directo del menú **Inicio** .

De forma predeterminada, la mayoría de las aplicaciones se publican en el momento en que se instalan, cuando los accesos directos se crean y se habilitan automáticamente.

 

## Temas relacionados


[Cómo probar la publicación de aplicaciones](how-to-test-application-publishing.md)

[Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





