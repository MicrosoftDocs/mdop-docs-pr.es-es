---
title: Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico
description: Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813727"
---
# Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico

*Nota:** App-V 4,6 ha salido del soporte técnico estándar. A continuación se supone que el cliente de App-V 4,6 SP3 ya está instalado.

Use el siguiente procedimiento para revertir puntos de extensión de un paquete de App-V 5,0 al formato de archivo de App-V 4,6 con el archivo de configuración de implementación.

**Para revertir un paquete**

1.  Asegúrese de que el paquete App-V 4,6 se publique para los usuarios, pero el FTAs y los accesos directos se han asumido en el paquete App-V 5,0 con el siguiente método de migración, [Cómo migrar puntos de extensión desde un paquete app-v 4,6 a un paquete app-v 5,0 para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).

    En la sección **userConfiguration** del archivo de configuración de implementación para el paquete convertido, para establecer la Directiva, realice la siguiente actualización en la sección **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" packagename = &lt; identificador &gt; de paquete**

2.  Desde un símbolo del sistema con privilegios elevados, escriba:

    PS &gt; **set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; ruta de acceso al archivo de configuración de implementación&gt;

    PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationType useDeploymentConfiguration**

3.  Realice una actualización de publicación o espere a la siguiente actualización de publicación programada para el paquete de App-V 4,6 SP2.

    Abra la aplicación mediante FTAs o accesos directos. La aplicación debería abrirse ahora con App-V 4,6.

    **Nota**  
    Si ya no necesita el paquete de App-V 5,0, puede anular la publicación del paquete de App-V 5,0 y los puntos de extensión volverán a App-V 4,6 automáticamente.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)









