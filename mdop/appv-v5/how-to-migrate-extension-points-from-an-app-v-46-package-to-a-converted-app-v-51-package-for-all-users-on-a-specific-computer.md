---
title: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico
description: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico
author: dansimp
ms.assetid: 4ef823a5-3106-44c5-aecc-29edf69c2fbb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 7bac244804b46309a0e0a75cb3742dfe22e92e8f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813879"
---
# Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico


Use el siguiente procedimiento para migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5,1 con el archivo de configuración de implementación.

**Nota:**  En este procedimiento se supone que está ejecutando la última versión de App-V 4,6.  
El siguiente procedimiento no requiere un servidor de administración de App-V 5,1.

 

**Para migrar los puntos de extensión de un paquete de un paquete de App-V 4.6 a un paquete App-V 5,1 que usa el archivo de configuración de implementación**

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

2. Para agregar el paquete de App-V 5,1, en el símbolo del sistema de PowerShell con privilegios elevados, escriba:

   PS &gt; **$pkg = Add-AppvClientPackage** **–** ruta path &lt; a la ubicación &gt;  - del paquete**DynamicDeploymentConfiguration** &lt; ruta de acceso al archivo de configuración de implementación&gt;

   &gt;**Publicación de PS-AppVClientPackage $pkg**

3. Para probar la migración, abra la aplicación virtual con FTAs o accesos directos relacionados. La aplicación se abre con App-V 5,1. Ambos, el paquete de App-V 4,6 y el paquete de App-V 5,1 convertido se publican en el usuario, pero el FTAs y los accesos directos de las aplicaciones se han asumido en el paquete App-V 5,1.

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





