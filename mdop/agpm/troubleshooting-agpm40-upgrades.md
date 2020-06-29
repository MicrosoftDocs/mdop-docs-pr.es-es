---
title: Solución de problemas de actualizaciones de AGPM
description: Solución de problemas de actualizaciones de AGPM
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818250"
---
# Solución de problemas de actualizaciones de AGPM

En esta sección se enumeran los problemas comunes que pueden surgir al actualizar el servidor de administración de directivas de grupo (AGPM) avanzado a una versión más reciente (por ejemplo, AGPM 4,0 a AGPM 4,3). Para diagnosticar problemas que no se encuentran aquí, puede ser útil ver la [solución de problemas AGPM](troubleshooting-agpm-agpm40.md) o un administrador AGPM (control total) para usar el registro y el seguimiento. Para obtener más información, vea [configurar el registro y el seguimiento](configure-logging-and-tracing-agpm40.md).

## ¿Qué problemas tienes?

-   [Error al generar un informe de diferencias de GPO HTML (código de error 80004003)](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a>Error al generar un informe de diferencias de GPO HTML (código de error 80004003)

-   **Causa**: ha instalado el paquete de actualización de AGPM con una cuenta incorrecta.

-   **Solución**: debe ser administrador de AGPM para poder corregir este problema.
    
    -   Asegúrese de que conoce el nombre de usuario & la contraseña de su **cuenta de servicio de AGPM**.

    -   Inicie sesión en su servidor de AGPM de forma interactiva como su cuenta de servicio de AGPM.
        
        -   Esto es muy importante, ya que se producirá un error en la instalación si usas una cuenta diferente.

    -   Cierre el servicio AGPM.
    
    -   Instale el Hotfix requerido.
    
    -   Conéctese a AGPM con un cliente de AGPM para comprobar que los informes de diferencias ya están funcionando.
    
## Instalar el paquete de revisiones 1 para Microsoft Advanced Group Policy Management 4,0 SP3
    
**Problema corregido en este Hotfix**: AGPM no puede generar informes de diferencias al controlar o administrar nuevos objetos de directiva de grupo (GPO).

**Cómo obtener esta actualización**: Instale la última versión de Microsoft Desktop Optimization Pack ([lanzamiento de marzo de 2017 de servicio](https://www.microsoft.com/download/details.aspx?id=54967)). Para obtener más información, consulte [KB 4014009](https://support.microsoft.com/help/4014009/) .

Más específicamente, puedes elegir descargar solo el primer archivo, `AGPM4.0SP1_Server_X64_KB4014009.exe` en la lista que aparece después de pulsar el botón Descargar.
      
El vínculo de descarga del paquete de optimización de escritorio de Microsoft (lanzamiento de marzo de 2017 de servicio) se puede encontrar [aquí](https://www.microsoft.com/download/details.aspx?id=54967).
      
      
## Vínculo de referencia
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
