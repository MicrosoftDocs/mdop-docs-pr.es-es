---
title: Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación
description: Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814390"
---
# Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación


La implementación de paquetes y grupos de conexión mediante el servidor de publicación de App-V 5,0 es útil porque ofrece administración de punto único y escalabilidad alta.

Siga estos pasos para configurar el cliente de App-V 5,0 para recibir actualizaciones del servidor de publicación.

**Nota:**  Para los siguientes procedimientos, el servidor de administración se instaló en un equipo denominado **MyMgmtSrv**y el servidor de publicación se instaló en un equipo denominado **MyPubSrv**.

 

**Para configurar el cliente de App-V 5,0 para recibir actualizaciones del servidor de publicación**

1.  Implementar los servidores de administración y publicación de App-V 5,0 y agregar los paquetes necesarios y los grupos de conexión. Para obtener más información sobre cómo agregar paquetes y grupos de conexión, consulte [Cómo agregar o actualizar paquetes mediante la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) y [Cómo crear un grupo de conexión](how-to-create-a-connection-group.md).

2.  Para abrir la consola de administración, haga clic en el vínculo siguiente, abra un explorador y escriba lo siguiente: http://MyMgmtSrv/AppvManagement/Console.html en un explorador Web, e importe, publique y contenga todos los paquetes y grupos de conexión que sean necesarios para un conjunto de usuarios en particular.

3.  En el equipo que ejecuta el cliente de App-V 5,0, abra un símbolo del sistema de PowerShell con privilegios elevados, ejecute el siguiente comando:

    **Add-AppvPublishingServer ABC-URL http://MyPubSrv/AppvPublishing**

    Este comando configurará el servidor de publicación especificado. Debería ver un resultado similar al siguiente:

    ID: 1

    SetByGroupPolicy: falso

    Nombre: ABC

    URL: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: falso

    GlobalRefreshOnLogon: falso

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: día

    UserRefreshEnabled: verdadero

    UserRefreshOnLogon: verdadero

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: día

    El identificador devuelto, en este caso 1

4.  En el equipo que ejecuta el cliente de App-V 5,0, abra un símbolo del sistema de PowerShell y escriba el siguiente comando:

    **Sync-AppvPublishingServer-ServerId 1**

    El comando consultará al servidor de publicación los paquetes y grupos de conexión que deben agregarse o quitarse para este cliente en particular en función de los derechos de los paquetes y grupos de conexión que se hayan configurado en el servidor de administración.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





