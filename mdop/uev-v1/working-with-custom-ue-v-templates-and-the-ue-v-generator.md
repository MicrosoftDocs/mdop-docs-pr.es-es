---
title: Trabajo con plantillas personalizadas de UE-V y el generador de UE-V
description: Trabajo con plantillas personalizadas de UE-V y el generador de UE-V
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823980"
---
# Trabajo con plantillas personalizadas de UE-V y el generador de UE-V


Para que las aplicaciones móviles entre equipos de usuario, la virtualización de la experiencia del usuario de Microsoft (UE-V) usa *plantillas de ubicación de configuración*. La virtualización de la experiencia del usuario incluye algunas plantillas de ubicación de configuración. También puede crear, editar o validar plantillas de ubicación de configuración personalizadas con el generador de UE-V.

El generador de UE-V supervisa una aplicación para descubrir y capturar las ubicaciones donde la aplicación almacena su configuración. La aplicación que se está supervisando debe ser una aplicación tradicional. El generador de UE-V no puede crear una plantilla de ubicación de configuración para los siguientes tipos de aplicaciones:

-   Aplicaciones virtualizadas

-   Aplicación ofrecida a través de servicios de Terminal Server

-   Aplicaciones Java

-   Aplicaciones para Windows 8

## Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V


Cómo usar el generador de UE-V para crear plantillas de ubicación de configuración.

[Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V


Cómo usar el generador de UE-V para editar plantillas de ubicación de configuración.

[Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Validar plantillas de ubicación de la configuración de UE-V con el generador de UE-V


Cómo usar el generador de UE-V para validar las plantillas de ubicación de configuración modificadas fuera del generador de UE-V.

[Validar plantillas de ubicación de la configuración de UE-V con el generador de UE-V](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a>Ubicaciones de configuración estándar y no estándar


El generador de UE-V le ayuda a identificar las aplicaciones que buscan los archivos de configuración y la configuración del registro que las aplicaciones usan para almacenar la información de configuración. Puede usar el generador de UE-V para abrir la aplicación como parte del proceso de detección para capturar la configuración en ubicaciones estándar. Entre las ubicaciones estándar se incluyen las siguientes:

-   **Configuración del registro** : ubicaciones del registro en **HKEY \ _CURRENT \ _USER**

-   **Archivos de configuración** de la aplicación: archivos almacenados en \ \ **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming**

El generador de UE-V excluye las ubicaciones que normalmente almacenan los archivos de software de aplicaciones no se mueven correctamente entre equipos o entornos de usuario. El generador de UE-V excluye estas ubicaciones. Las ubicaciones excluidas son las siguientes:

-   HKEY \ _CURRENT \ _USER claves de registro y archivos en los que el usuario que ha iniciado sesión no puede escribir valores

-   HKEY \ _CURRENT \ _USER claves de registro y archivos asociados a la funcionalidad básica del sistema operativo Windows

-   Todas las claves del registro que se encuentran en la sección HKEY \ _LOCAL \ _MACHINE (requieren derechos de administrador y pueden requerir el establecimiento de un contrato de UAC)

-   Los archivos que se encuentran en los directorios de archivos de programa (requieren derechos de administrador y pueden requerir el establecimiento de un contrato de UAC)

-   Archivos que se encuentran en los usuarios \ \ \ [nombre de usuario \] \ \ AppData \ \ LocalLow

-   Los archivos del sistema operativo Windows que se encuentran en% systemroot% (requieren derechos de administrador y pueden requerir el establecimiento de un contrato de UAC)

Si las claves del registro y los archivos almacenados en estas ubicaciones son necesarios para poder mover la configuración de la aplicación, puede Agregar manualmente las ubicaciones excluidas a la plantilla de ubicación de configuración durante el proceso de creación de la plantilla.

## Otros recursos para este producto


[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

[Administración de UE-V 1.0](administering-ue-v-10.md)

 

 





