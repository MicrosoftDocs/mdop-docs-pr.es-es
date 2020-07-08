---
title: Migración de paquetes de configuración de UE-V
description: Migración de paquetes de configuración de UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823210"
---
# Migración de paquetes de configuración de UE-V


En el ciclo de vida de una implementación de virtualización de Microsoft User Experience (UE-V), es posible que tenga que cambiar la ubicación de los paquetes de configuración de usuario al migrar a un nuevo servidor o con fines de copia de seguridad. Es posible que se necesite la migración de paquetes de configuración en los siguientes escenarios:

-   Actualizar el hardware de servidor existente a un servidor más moderno.

-   Migración de un recurso compartido de ubicación de almacenamiento de configuración de un laboratorio a un servidor de producción.

Simplemente copiando los archivos y carpetas no se conservarán los permisos ni la configuración de seguridad. Los pasos descritos a continuación copiarán correctamente los archivos del paquete de configuración con sus permisos NTFS en un nuevo recurso compartido.

**Cómo mantener los paquetes de configuración de UE-V al migrar a un nuevo servidor**

1.  En una nueva ubicación de un servidor diferente, cree una nueva carpeta; por ejemplo, bisettings.

2.  Deshabilite el uso compartido para el antiguo recurso compartido de carpetas en el servidor antiguo.

3.  Mueva los paquetes de configuración existentes al nuevo servidor con Robocopy desde la línea de comandos. Por ejemplo:

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Nota:**  Para supervisar el progreso de la copia, abra MySettings.txt con un lector de archivos de registro, como Trace32.

     

4.  Otorgue permisos de nivel compartido al nuevo recurso compartido. Deje los permisos NTFS tal y como fueron establecidos por Robocopy.

    En los equipos que ejecutan el agente de UE-V, actualice la opción de configuración SettingsStoragePath a la ruta de acceso UNC del nuevo recurso compartido.

## Temas relacionados


[Administración de UE-V 1.0](administering-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





