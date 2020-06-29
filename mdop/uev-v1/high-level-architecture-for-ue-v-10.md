---
title: Arquitectura de alto nivel para UE-V 1.0
description: Arquitectura de alto nivel para UE-V 1.0
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827100"
---
# Arquitectura de alto nivel para UE-V 1.0


En este tema se describen los elementos arquitectónicos de alto nivel de la solución de itinerancia de configuración de Microsoft User Experience Virtualization (UE-V). Los siguientes elementos forman parte de una implementación estándar de UE-V.

![diagrama de arquitectura de UE-v Agent](images/ue-vagentarchitecturaldiagram.gif)

El agente UE-V supervisa las aplicaciones y los procesos del sistema operativo a medida que se identifican en las plantillas de ubicación de configuración de UE-V. Cuando se inicie la aplicación o el sistema operativo, la configuración se leerá desde el paquete de configuración y se aplicará al equipo. Cuando se cierra la aplicación o cuando el sistema operativo está bloqueado o cerrado, la configuración se guarda en un paquete de configuración de UE-V en la ubicación de almacenamiento de configuración.

## Ubicación de almacenamiento de configuración


La ubicación de almacenamiento de configuración es un recurso compartido de archivos al que el usuario tiene acceso a la configuración de lectura y escritura del agente de virtualización. Esta es el directorio principal de Active Directory o definido durante la instalación de UE-V. Puede establecer la ubicación durante la instalación de UE-V Agent o puede establecerla más tarde con Directiva de grupo, WMI o PowerShell. La ubicación puede encontrarse en cualquier recurso compartido de archivos común al que los usuarios puedan tener acceso. Si no se establece ninguna ubicación de almacenamiento de configuración durante la instalación, UE-V usará el directorio principal en Active Directory. El agente UE-V comprueba la ubicación y crea una carpeta del sistema que está oculta para el usuario en el que se almacena y tiene acceso a la configuración de usuario. Para obtener más información sobre el almacenamiento de configuración, vea [preparar el entorno para UE-V](preparing-your-environment-for-ue-v.md).

## UE-V Agent


UE-V Agent se instala en cada equipo con la configuración sincronizada por la virtualización de la experiencia del usuario. El agente supervisa las aplicaciones registradas y el sistema operativo de los cambios que se realicen en la configuración, y sincroniza esa configuración entre equipos. La configuración se aplica desde la ubicación de almacenamiento de configuración a la aplicación cuando se inicia la aplicación. La configuración se vuelve a guardar en la ubicación de almacenamiento de configuración cuando se cierra la aplicación. La configuración del sistema operativo se aplica cuando el usuario inicia sesión, cuando el equipo se desbloquea o cuando el usuario se conecta de forma remota al equipo mediante el protocolo de escritorio remoto (RDP). El agente guarda la configuración cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando se desconecta una conexión remota. Para obtener más información sobre el agente de UE-V, consulte [preparar el entorno para UE-v](preparing-your-environment-for-ue-v.md).

## <a href="" id="bkmk-settingslocationtemplate"></a>Plantillas de ubicación de configuración


La plantilla de ubicación de configuración es un archivo XML que define las ubicaciones de configuración que debe supervisar la virtualización de la experiencia del usuario. Solo las ubicaciones de configuración definidas en estas plantillas de configuración se capturan o aplican en equipos que ejecutan UE-V Agent. La plantilla de ubicación de configuración no contiene valores de configuración, solo las ubicaciones en las que se almacenan los valores en el equipo.

UE-V incluye un conjunto de plantillas de ubicación de configuración que especifican las ubicaciones de configuración de algunas aplicaciones de Microsoft y la configuración de Windows. Un administrador puede crear plantillas de ubicación de configuración personalizadas mediante el generador de UE-V.

[Planificación de las aplicaciones a sincronizar con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planificación de la implementación de la plantilla personalizada para UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Trabajo con plantillas personalizadas de UE-V y el generador de UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## Paquetes de configuración


La configuración de la aplicación y la configuración de Windows se almacenan en paquetes de configuración creados por el agente de UE-V. Un paquete de configuración es una colección de las opciones representadas en las plantillas de ubicación de configuración. Estos paquetes de configuración se generan, se almacenan de forma local y luego se copian en la ubicación de almacenamiento de configuración. "Última escritura gana" determina qué configuración se conserva cuando un solo usuario sincroniza más de un equipo con una ubicación de almacenamiento. El agente que se ejecuta en un equipo Lee y escribe en la ubicación de configuración independiente de los agentes que se ejecutan en otros equipos. La configuración y los valores más recientes se aplican cuando el siguiente agente Lee de la ubicación de almacenamiento de configuración.

![proceso de generación de UE-v](images/ue-vgeneratorprocess.gif)

## Catálogo de plantillas de configuración


El catálogo de plantillas de configuración es una ruta de carpeta en los equipos UE-V o en un recurso compartido de mensajes de servidor (SMB) que almacena todas las plantillas de ubicación de configuración personalizada. UE-V Agent recupera plantillas nuevas o actualizadas desde esta ubicación. UE-V Agent comprueba esta ubicación una vez al día y la actualiza según las plantillas de esta carpeta. Las plantillas que se han agregado o actualizado en esta carpeta desde la última comprobación son registradas por el agente de UE-V. UE-V Agent cancela el registro de las plantillas que se quitaron de esta carpeta. El programador de tareas registra las plantillas y las registra una vez al día. Si va a usar solo las plantillas de ubicación de configuración predeterminada que se incluyen en UE-V, el catálogo de plantillas de configuración no es necesario. Para obtener más información sobre los catálogos de implementación de configuración, vea [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Generador de virtualización de la experiencia del usuario


El generador de virtualización de la experiencia del usuario le permite crear plantillas de ubicación de configuración personalizadas que almacenarán las ubicaciones de configuración de las aplicaciones que se usan en la empresa y que desea incluir en la solución de configuración de itinerancia. El generador de UE-V intentará descubrir las ubicaciones de los valores del registro y los archivos de configuración de las aplicaciones y, después, registrará esas ubicaciones en un archivo XML de la plantilla de ubicación de configuración. Después, puede distribuir estas plantillas de ubicación de configuración a los equipos de los usuarios. El generador de UE-V también permite que un administrador edite una plantilla existente o valide una plantilla creada con otro editor XML.

El generador de UE-V supervisa una aplicación para descubrir y grabar dónde se almacena su configuración. Para ello, supervisa dónde lee o escribe la aplicación en el registro HKEY \ _CURRENT \ _USER o en las carpetas de archivos en **users** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming y usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **local**.

El proceso de descubrimiento excluye las claves del registro y los archivos en los que el usuario que ha iniciado sesión no puede escribir valores. Ninguna de estas opciones se incluirá en el archivo XML. El proceso de descubrimiento también excluye las claves del registro y los archivos asociados a la funcionalidad básica del sistema operativo Windows.

Para más información sobre el generador de UE-V, consulte [Installing the UE-v generator](installing-the-ue-v-generator.md).

## Temas relacionados


[Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0](index.md)

[Introducción a la virtualización de la experiencia del usuario 1.0](getting-started-with-user-experience-virtualization-10.md)

[Acerca de la virtualización de la experiencia del usuario 1.0](about-user-experience-virtualization-10.md)

[Trabajo con plantillas personalizadas de UE-V y el generador de UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





