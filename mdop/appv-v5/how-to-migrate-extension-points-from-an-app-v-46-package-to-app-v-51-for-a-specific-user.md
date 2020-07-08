---
title: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico
description: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813870"
---
# Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico


Use el siguiente procedimiento para migrar paquetes creados con App-V mediante el archivo de configuración de usuario.

**Nota:**  En este procedimiento se supone que está ejecutando la última versión de App-V 4,6.

**Para convertir un paquete**

1. Busque el archivo de configuración de usuario del paquete que desea convertir. Para establecer la Directiva, realice las siguientes actualizaciones en la sección **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" packagename = &lt; identificador &gt; de paquete**.

   A continuación se encuentra un ejemplo de un archivo de configuración de usuario:

   &lt;? ¿versión? XML = "1.0"?&gt;

   &lt;UserConfiguration PackageId = &lt; Package ID &gt; displayName = &lt; nombre del paquete&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID. de paquete&gt;

   &lt;/UserConfiguration&gt;

2. Para agregar el paquete de App-V 5,1, escriba lo siguiente en una ventana del símbolo del sistema de PowerShell con privilegios elevados:

   PS &gt; **$pkg = Add-AppvClientPackage –** ruta path &lt; a la ubicación del paquete&gt;

   PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; ruta de acceso al archivo de configuración de usuario&gt;

3. Abra la aplicación con FTAs o accesos directos ahora. La aplicación debería abrirse con App-V 5,1.

   El paquete de App-V 4,6 y el paquete de App-V 5,1 convertido se publican en el usuario, pero el FTAs y los accesos directos de las aplicaciones se han asumido por el paquete de App-V 5,1.

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

[Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





