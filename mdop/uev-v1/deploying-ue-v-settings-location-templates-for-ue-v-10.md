---
title: Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0
description: Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827121"
---
# Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0


La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración que la virtualización de la experiencia de usuario captura y aplica. UE-V incluye un conjunto de plantillas estándar, así como una herramienta, el generador de UE-V, que le permite crear plantillas de ubicación de configuración personalizadas. Después de crear una plantilla de ubicación de configuración, debe probarla para asegurarse de que la configuración de la aplicación se hace correctamente en un entorno de prueba. Después, puede implementar de forma segura la plantilla de ubicación de configuración en los equipos de la empresa.

Las plantillas de ubicación de configuración se pueden implementar mediante la distribución de software empresarial (ESD), preferencias de directiva de grupo o configurando un catálogo de plantillas de configuración de UE-V. Las plantillas que se implementan mediante ESD o una directiva de grupo se deben registrar mediante el WMI o PowerShell de UE-V. Las plantillas que se almacenan en la ubicación del catálogo de plantillas de configuración son registradas automáticamente por el agente de UE-V.

## Implementar las plantillas de ubicación de configuración con una ruta de acceso del catálogo de plantillas de configuración


La ruta de acceso del catálogo de plantillas de la configuración de UE-V se puede definir mediante los métodos siguientes: Directiva de grupo, los parámetros de la línea de comandos de instalación del agente, WMI o PowerShell. Una vez que se ha definido la ruta de acceso al catálogo de plantillas, UE-V Agent recupera las plantillas nuevas o actualizadas de esta ubicación. UE-V Agent comprueba esta ubicación una vez cada día y actualiza el comportamiento de sincronización según las plantillas que se encuentran en esta carpeta. Las plantillas que se han agregado o actualizado en esta carpeta desde la última comprobación son registradas por el agente de UE-V. El agente de UE-V también elimina el registro de plantillas que se han quitado de esta carpeta. El programador de tareas registra las plantillas y las registra una vez al día.

**Para usar la ruta del catálogo de plantillas de configuración para implementar las plantillas de ubicación de configuración de UE-V**

1.  Vaya a la carpeta de recursos compartidos de red que se define como el catálogo de plantillas de configuración.

2.  Agregue, quite o actualice plantillas de ubicación de configuración en el catálogo de plantillas de configuración para reflejar la configuración de la plantilla del agente UE-V deseada para equipos UE-V.

3.  Las plantillas de los equipos se actualizan diariamente en función de los cambios en el catálogo de plantillas de configuración.

4.  Abra un símbolo del sistema con privilegios elevados y vaya a **% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 o x64 &gt; **y, a continuación, ejecute **ApplySettingsTemplateCatalog.exe** para actualizar manualmente las plantillas en un equipo que ejecute UE-V Agent.

## Temas relacionados


[Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0](index.md)

[Implementación de UE-V 1.0](deploying-ue-v-10.md)

[Planificación de las aplicaciones a sincronizar con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





