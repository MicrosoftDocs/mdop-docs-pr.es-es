---
title: Administrar las actualizaciones de Software para áreas de trabajo de MED-V
description: Administrar las actualizaciones de Software para áreas de trabajo de MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824811"
---
# Administrar las actualizaciones de Software para áreas de trabajo de MED-V


Tiene varias opciones diferentes disponibles para proporcionar actualizaciones de software para las aplicaciones en el área de trabajo de MED-V implementada.

**Nota:**  Para obtener información sobre cómo especificar las opciones de configuración que definen cómo el MED-V recibe actualizaciones automáticas, consulte [Administración de actualizaciones automáticas para áreas de trabajo de Med-v](managing-automatic-updates-for-med-v-workspaces.md).

 

**Actualización de software en un área de trabajo de MED-V**

1.  **Uso de un sistema electrónico de distribución de software**

    Si su organización usa un sistema de sistema de distribución de software electrónico (ESD) para implementar software, puede usarlo para proporcionar actualizaciones de software para las aplicaciones en áreas de trabajo de MED-V, de la misma forma en que proporciona actualizaciones para aplicaciones en equipos físicos.

2.  **Uso de directivas de grupo**

    Si su organización implementa software mediante una directiva de grupo, puede usarlo para proporcionar actualizaciones de software para las aplicaciones en áreas de trabajo de MED-V, de la misma forma en que proporciona actualizaciones para las aplicaciones en equipos físicos.

3.  **Usar la virtualización de aplicaciones (APP-V)**

    Si usa MED-V junto con App-V, puede proporcionar actualizaciones de software para las aplicaciones en el área de trabajo de MED-V siguiendo los pasos que necesita App-V para actualizar el software. Para obtener más información, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

4.  **Actualización de software en la imagen principal**

    Aunque no se considere una recomendación de MED-V, puede instalar actualizaciones de software en las aplicaciones de la imagen principal. Después de instalar las actualizaciones, puede volver a implementar el área de trabajo de MED-V en su empresa de la misma manera en que lo implementó originalmente.

    **Importante**  No se recomienda este método de administración de actualizaciones de software. Además, si actualiza el software en la imagen principal y vuelve a implementar el área de trabajo de MED-V en su empresa, la configuración debe volver a ejecutarse y todos los datos guardados en la máquina virtual se perderán.

     

## Temas relacionados


[Administrar las actualizaciones automáticas para áreas de trabajo de MED-V](managing-automatic-updates-for-med-v-workspaces.md)

[Cómo probar la publicación de aplicaciones](how-to-test-application-publishing.md)

[Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





