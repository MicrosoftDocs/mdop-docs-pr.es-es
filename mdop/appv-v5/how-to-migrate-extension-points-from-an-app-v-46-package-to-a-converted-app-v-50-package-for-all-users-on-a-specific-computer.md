---
title: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico
description: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813886"
---
# Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico

**Nota:** App-V 4,6 ha salido del soporte técnico estándar.

Use el siguiente procedimiento para migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5,0 con el archivo de configuración de implementación.

**Nota:**  El siguiente procedimiento no requiere un servidor de administración de App-V 5,0.

 

**Para migrar los puntos de extensión de un paquete de un paquete de App-V 4.6 a un paquete App-V 5,0 que usa el archivo de configuración de implementación**

1. Busque el directorio que contiene el archivo de configuración de implementación para el paquete que desea migrar. Para establecer la Directiva, realice la siguiente actualización a la sección **userConfiguration** :

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; identificador de paquete&gt;**

   A continuación se encuentra un ejemplo del contenido de un archivo de configuración de implementación:

   &lt;? ¿versión? XML = "1.0"?&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; Package ID &gt; displayName = &lt; nombre para mostrar&gt;

   &lt;MachineConfiguration/&gt;

   &lt;UserConfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID. de paquete&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. Para agregar el paquete de App-V 5,0, en el símbolo del sistema de PowerShell con privilegios elevados, escriba:

   PS &gt; **$pkg = Add-AppvClientPackage** **–** ruta path &lt; a la ubicación &gt;  - del paquete**DynamicDeploymentConfiguration** &lt; ruta de acceso al archivo de configuración de implementación&gt;

   &gt;**Publicación de PS-AppVClientPackage $pkg**

3. Para probar la migración, abra la aplicación virtual con FTAs o accesos directos relacionados. La aplicación se abre con App-V 5,0. Ambos, el paquete de App-V 4,6 y el paquete de App-V 5,0 convertido se publican en el usuario, pero el FTAs y los accesos directos de las aplicaciones se han asumido en el paquete App-V 5,0.

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





