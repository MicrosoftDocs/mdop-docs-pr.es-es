---
title: Migrar paquetes de configuración de UE-V 2. x
description: Migrar paquetes de configuración de UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825520"
---
# Migrar paquetes de configuración de UE-V 2. x


En el ciclo de vida de una implementación de Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, es posible que tenga que cambiar la ubicación de los paquetes de configuración de usuario al migrar a un nuevo servidor o al realizar copias de seguridad. Es posible que los paquetes de configuración deban migrarse en los siguientes escenarios:

-   Actualizar el hardware de servidor existente a un servidor más moderno.

-   Migración de un recurso compartido de ubicación de almacenamiento de configuración de un servidor de prueba a un servidor de producción.

Simplemente copiando los archivos y carpetas no se conservan los permisos ni la configuración de seguridad. Los pasos siguientes describen cómo copiar correctamente el paquete de configuración junto con los permisos del sistema de archivos NTFS en un nuevo recurso compartido.

**Para conservar los paquetes de configuración de UE-V 2 al migrar a un nuevo servidor**

1.  En una nueva ubicación de un servidor diferente, cree una nueva carpeta, por ejemplo, a través de la configuración.

2.  Deshabilite el uso compartido para el antiguo recurso compartido de carpetas en el servidor antiguo.

3.  Para copiar los paquetes de configuración existentes en el nuevo servidor con Robocopy

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Nota:**  Para supervisar el progreso de la copia, abra MySettings.txt con un visor de registro como Trace32.

     

4.  Otorgue permisos de nivel compartido al nuevo recurso compartido. Deje los permisos del sistema de archivos NTFS tal y como fueron establecidos por Robocopy.

    En los equipos que ejecutan el agente de UE-V, actualice la opción de configuración **SettingsStoragePath** a la ruta de acceso UNC (Convención de nomenclatura universal) del nuevo recurso compartido.

    **¿Tiene una sugerencia para UE-V**? Agregue o vote por sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **¿Tienes un problema de UE-V**? Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Temas relacionados


[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





