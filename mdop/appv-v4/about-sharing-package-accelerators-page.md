---
title: Acerca del uso compartido de la página de aceleradores de paquetes
description: Acerca del uso compartido de la página de aceleradores de paquetes
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819991"
---
# Acerca del uso compartido de la página de aceleradores de paquetes


Esta información proporciona la información de procedimientos recomendados sobre cómo compartir aceleradores de paquetes. Si planea compartir archivos de aceleradores de paquetes, es posible que la información, como los nombres de los equipos, la información de la cuenta de usuario y la información sobre las aplicaciones incluidas en las transformaciones, se incluyan en el archivo de aceleradores de paquetes. Debe revisar cualquier configuración o archivos de configuración asociados con el paquete de aplicación virtual para asegurarse de que las aplicaciones no contienen información personal. Esta página contiene los siguientes elementos.

-   **Nombre de usuario**. Al iniciar sesión en el equipo que ejecuta el secuenciador de Microsoft App-V, debe usar una cuenta de usuario genérica, como la cuenta de **Administrador** integrada. No debe usar una cuenta basada en un nombre de usuario existente.

-   **Nombre del equipo**. Especifique un nombre general, no Identificativo, del equipo que ejecuta el secuenciador.

-   **Dirección URL del servidor**. En la consola del secuenciador de App-V, en la pestaña **implementación** , use la configuración predeterminada para la información de configuración de la dirección URL del servidor.

-   **Las aplicaciones**. Si no desea compartir la lista de aplicaciones que se instalaron en el equipo que ejecuta el secuenciador cuando creó el acelerador de paquetes, debe eliminar el archivo de **appv\_manifest.xml** . Este archivo se encuentra en el directorio raíz del paquete de la aplicación virtual.

## Temas relacionados


[Crear asistente del acelerador de paquetes (AppV 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

[Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





