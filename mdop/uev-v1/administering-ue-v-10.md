---
title: Administración de UE-V 1.0
description: Administración de UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822700"
---
# Administración de UE-V 1.0


Una vez implementada la virtualización de la experiencia del usuario de Microsoft (UE-V), debe poder realizar diversas tareas administrativas en curso. Estas tareas posteriores a la instalación se describen en las siguientes secciones.

## Administración de recursos de UE-V


Durante el ciclo de vida de UE-V, tendrá que administrar la configuración de el agente de UE-V y también administrar las ubicaciones de almacenamiento de recursos, como paquetes de configuración. Es posible que tenga que realizar otras tareas como restaurar la configuración de un usuario a su estado original desde antes de que se instale UE-V para recuperar la configuración perdida. En los siguientes temas se proporcionan instrucciones para la administración de recursos de UE-V.

### Cambiar la frecuencia de las tareas programadas de UE-V

Puede configurar las tareas programadas que se van a administrar cuando UE-V comprueba si hay plantillas de ubicación de configuración personalizadas nuevas, actualizadas o eliminadas en el catálogo de plantillas de configuración.

[Cambiar la frecuencia de las tareas programadas de UE-V](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a>Plantillas de ubicación de la configuración de uso compartido con la galería de plantillas de UE-V

La galería de plantillas de UE-V facilita el uso compartido de plantillas de ubicación de configuración de UE-V. La Galería permite cargar las plantillas de ubicación de configuración para compartirlas con otras personas y descargar plantillas que otras personas han creado.

[Plantillas de ubicación de la configuración de uso compartido con la galería de plantillas de UE-V](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### Restaurando la configuración de la aplicación y de Windows sincronizada con UE-V 1,0

Las características de WMI y PowerShell de UE-V proporcionan la capacidad de restaurar paquetes de configuración. Los comandos WMI y PowerShell permiten restaurar la configuración de la aplicación y de Windows a los valores de configuración que se encontraban en el equipo la primera vez que se inició la aplicación después de que se inició el agente de UE-V.

[Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### Configurar UE-V con objetos de directiva de grupo

Puede usar la Directiva de grupo para modificar la configuración que define cómo UE-V sincroniza la configuración de los equipos.

[Configurar UE-V con objetos de directiva de grupo](configuring-ue-v-with-group-policy-objects.md)

### Administrar UE-V con PowerShell y WMI

Puede usar PowerShell y WMI para modificar la configuración que define cómo UE-V sincroniza la configuración de los equipos.

[Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### Migración de paquetes de configuración de UE-V

Puede cambiar la ubicación de los paquetes de configuración de usuario al migrar a un nuevo servidor o por motivos de seguridad.

[Migración de paquetes de configuración de UE-V](migrating-ue-v-settings-packages.md)

## Otros recursos para este producto


[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





