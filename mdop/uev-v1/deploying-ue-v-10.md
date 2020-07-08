---
title: Implementación de UE-V 1.0
description: Implementación de UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827150"
---
# Implementación de UE-V 1.0


Hay varias configuraciones de implementación diferentes que admite Microsoft User Experience Virtualization (UE-V). Esta sección incluye información general y procedimientos paso a paso que le ayudarán a realizar correctamente las tareas que debe completar en diferentes fases de la implementación.

## Información de implementación para UE-V


Una implementación de UE-V requiere una ubicación de almacenamiento de configuración en un recurso compartido de red y un agente de UE-V instalado en todos los equipos que sincronizan la configuración. Las plantillas de directiva de grupo de UE-V se pueden usar para administrar la configuración de UE-V. En los temas siguientes se describe cómo implementar estas características.

[Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

Todas las implementaciones de UE-V requieren una ubicación de almacenamiento de configuración donde se encuentren los paquetes de configuración que contienen los valores de configuración sincronizados.

[Implementación del agente de UE-V](deploying-the-ue-v-agent.md)

Para sincronizar la configuración con UE-V, un equipo debe tener el agente de UE-V instalado y en ejecución.

[Instalación de las plantillas ADMX de directiva de grupo de UE-V](installing-the-ue-v-group-policy-admx-templates.md)

Puede usar la Directiva de grupo para preconfigurar la configuración de UE-V antes de implementar el agente de UE-V, así como la configuración estándar de UE-V.

## Información de implementación para la implementación de una plantilla personalizada


Si planea crear plantillas de ubicación de configuración personalizada para aplicaciones distintas de las aplicaciones de Microsoft que se incluyen en la UE-V, como las aplicaciones de línea de negocio, puede implementar un catálogo de plantillas de configuración y debe instalar el generador de UE-V para crear esas plantillas. Para obtener más información, vea [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

[Instalación del generador de UE-V](installing-the-ue-v-generator.md)

Use el generador de UE-V para crear, editar y validar plantillas de ubicación de configuración personalizadas que ayuden a sincronizar la configuración de aplicaciones distintas de las aplicaciones predeterminadas.

[Implementación del catálogo de plantillas de configuración de UE-V 1.0](deploying-the-settings-template-catalog-for-ue-v-10.md)

Si necesita implementar plantillas de ubicación de configuración personalizada para admitir aplicaciones que no sean las predeterminadas en el agente de UE-V, debe configurar un catálogo de plantillas de configuración para almacenarlas.

[Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

Si necesita sincronizar aplicaciones que no sean las aplicaciones predeterminadas en el agente de UE-V, las plantillas de ubicación de configuración personalizadas creadas con el generador de UE-v se pueden distribuir al catálogo de plantillas de configuración de UE-V.

**Nota:**  La implementación de plantillas personalizadas requiere un catálogo de plantillas de configuración. Las plantillas de aplicación de Microsoft predeterminadas se implementan con el agente de UE-V.

 

## Temas para este producto


[Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0](index.md)

[Introducción a la virtualización de la experiencia del usuario 1.0](getting-started-with-user-experience-virtualization-10.md)

[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

[Solución de problemas de UE-V 1.0](troubleshooting-ue-v-10.md)

 

 





