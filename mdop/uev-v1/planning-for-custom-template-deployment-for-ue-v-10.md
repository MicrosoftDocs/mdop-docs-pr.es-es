---
title: Planificación de la implementación de la plantilla personalizada para UE-V 1.0
description: Planificación de la implementación de la plantilla personalizada para UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821191"
---
# Planificación de la implementación de la plantilla personalizada para UE-V 1.0


La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración que captura y aplica UE-V. Puede usar el generador de UE-V para crear plantillas de ubicación de configuración personalizadas que permitan a los usuarios desplazar la configuración de aplicaciones distintas de las incluidas en las plantillas predeterminadas de la versión de. Después de probar la plantilla personalizada para asegurarse de que la configuración de la aplicación se mueve correctamente en un entorno de prueba, puede implementar estas plantillas de ubicación de configuración en los equipos de la empresa.

Puede implementar sus plantillas de ubicación de configuración personalizadas con una infraestructura de implementación existente, como la distribución de software de empresa (ESD), con preferencias de directiva de grupo o configurando un catálogo de plantillas de configuración de UE-V. Las plantillas que se implementan mediante ESD o Directiva de grupo se deben registrar con WMI o PowerShell de UE-V.

## Catálogo de plantillas de configuración


El catálogo de plantillas configuración de virtualización de la experiencia del usuario es una ruta de carpeta en equipos de UE-V o un recurso de bloque de mensajes de servidor (SMB) que almacena todas las plantillas de ubicación de configuración personalizada. UE-V Agent recupera plantillas nuevas o actualizadas desde esta ubicación. UE-V Agent comprueba esta ubicación una vez cada día y actualiza el comportamiento de sincronización según las plantillas de esta carpeta. Las plantillas que se han agregado o actualizado en esta carpeta desde la última vez que la carpeta se ha activado está registradas por el agente de UE-V. UE-V Agent cancela el registro de las plantillas que se quitan de esta carpeta. De forma predeterminada, las plantillas se registran y se registran una vez al día a las 3:30 A.M. hora local por el programador de tareas. Para obtener más información sobre las tareas de UE-V, consulte [cambiar la frecuencia de las tareas programadas de UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).

Puede configurar la ruta del catálogo de plantillas de configuración con las opciones de la línea de comandos de instalación, Directiva de grupo, WMI o PowerShell. Las plantillas que se almacenan en la ruta del catálogo de plantillas de configuración se registran automáticamente y no se registran mediante una tarea programada. Puede personalizar esta tarea programada según sea necesario.

## Reemplazar las plantillas predeterminadas de Microsoft


UE-V Agent instala un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows. Si su empresa necesita versiones personalizadas de estas plantillas, el agente de UE-V se puede configurar para que use un catálogo de plantillas de configuración y, a continuación, debe reemplazar las plantillas predeterminadas de Microsoft.

Durante la instalación de UE-V Agent, se puede usar el parámetro de la línea de comandos `RegisterMSTemplates` para deshabilitar el registro de las plantillas predeterminadas de Microsoft. Para obtener más información sobre cómo configurar los parámetros de UE-V, consulte [planificación de métodos de configuración de UE-v](planning-for-ue-v-configuration-methods.md).

Al usar una directiva de grupo para configurar la ruta del catálogo de plantillas de configuración, puede elegir reemplazar las plantillas predeterminadas de Microsoft. Si establece la configuración de la Directiva para reemplazar las plantillas predeterminadas de Microsoft, todas las plantillas de Microsoft predeterminadas que instala el agente UE-V se eliminarán del equipo y solo se usarán las plantillas que se encuentren en el catálogo de plantillas de configuración. La configuración de configuración de UE-V Agent `RegisterMSTemplates` debe establecerse en true para poder invalidar la plantilla predeterminada de Microsoft.

**Nota:**  Si deshabilita esta configuración de directiva después de que se haya habilitado, UE-V Agent no restaurará las plantillas predeterminadas de Microsoft.

 

Si hay plantillas personalizadas en el catálogo de plantillas de configuración que usan el mismo identificador que las plantillas predeterminadas de Microsoft, y el agente UE-V no está configurado para reemplazar las plantillas de Microsoft predeterminadas, se omitirán las plantillas de Microsoft en el catálogo.

También puede reemplazar las plantillas predeterminadas mediante las características de PowerShell de UE-V. Para reemplazar la plantilla predeterminada de Microsoft por PowerShell, anule el registro de todas las plantillas predeterminadas de Microsoft y, a continuación, registre las plantillas personalizadas.

**Nota:**  Los paquetes de configuración antigua permanecen en la ubicación de almacenamiento de configuración aunque se implementen nuevas plantillas de configuración para una aplicación. El agente no lee estos paquetes, pero ninguno de ellos se elimina automáticamente.

 

## Temas relacionados


[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

[Planificación de las aplicaciones a sincronizar con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planificación de métodos de configuración de UE-V](planning-for-ue-v-configuration-methods.md)

Planeamiento de la implementación de plantillas personalizadas
 

 





