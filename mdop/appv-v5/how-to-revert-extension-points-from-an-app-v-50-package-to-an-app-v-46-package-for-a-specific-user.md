---
ms.reviewer: ''
title: Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico
description: Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813742"
---
# Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico

*Nota:** App-V 4,6 ha salido del soporte técnico estándar.

Use el siguiente procedimiento para revertir un paquete de App-V 5,0 al formato de archivo de App-V con el archivo de configuración de usuario.

**Para revertir un paquete**

1.  Asegúrese de que el paquete de App-V 4,6 se haya publicado para los usuarios, pero el FTAs y los accesos directos se han asumido en el paquete de App-V 5,0 con el siguiente método de migración, [Cómo migrar puntos de extensión desde un paquete de App-v 4,6 a App-v 5,0 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).

    En la sección **userConfiguration** del archivo de configuración de implementación para el paquete convertido, para establecer la Directiva, realice la siguiente actualización en la sección **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" packagename = &lt; identificador &gt; de paquete**

2.  Desde un símbolo del sistema con privilegios elevados, escriba:

    PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath** &lt; ruta de acceso al archivo de configuración de usuario&gt;

3.  Realice una actualización de publicación o espere a la siguiente actualización de publicación programada para App-V 4,6. Abra la aplicación mediante FTAs o accesos directos. La aplicación debería abrirse ahora con App-V 4,6 SP2.

    **Nota**  
    Si ya no necesita el paquete de App-V 5,0, puede anular la publicación del paquete de App-V 5,0 y los puntos de extensión volverán a App-V 4,6 automáticamente.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)












