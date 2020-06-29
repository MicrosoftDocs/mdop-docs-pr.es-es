---
title: Cómo modificar la configuración del cliente de App-V 5.1 mediante la plantilla ADMX y la directiva de grupo
description: Cómo modificar la configuración del cliente de App-V 5.1 mediante la plantilla ADMX y la directiva de grupo
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813823"
---
# Cómo modificar la configuración del cliente de App-V 5.1 mediante la plantilla ADMX y la directiva de grupo


Use la plantilla Microsoft Application Virtualization (App-V) 5,1 ADMX para configurar la configuración del cliente de App-V 5,1 con la plantilla ADMX y la Directiva de grupo.

**Para modificar la configuración de cliente de App-V 5,1 con la Directiva de grupo**

1.  Para modificar la configuración del cliente de App-V 5,1, busque los archivos de **ADMXTemplate** que están disponibles con App-v 5,1.

    **Nota:**  Use el siguiente vínculo para descargar las plantillas de App-V 5,1 **ADMX**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  En el equipo donde administra la Directiva de grupo, generalmente el controlador de dominio, copie el archivo template **. ADMX** en el siguiente directorio: ** &lt; unidad de instalación &gt; \ \ Windows \ \ PolicyDefinitions**.

    A continuación, en el mismo equipo, copie el archivo **. ADML** en el siguiente directorio: ** &lt; InstallationDrive &gt; \ \ Windows \ \ PolicyDefinitions \ \ en-** es.

3.  Una vez que haya copiado los archivos, abra la consola de administración de directivas de grupo para modificar las directivas asociadas a los clientes de **Computer Configuration**App-V 5,1 examinar  /  **las directivas**de configuración  /  del equipo sistema de**plantillas administrativas**  /  **System**  /  **: V**.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación de App-V 5.1](deploying-app-v-51.md)

[Información acerca de la configuración de cliente](about-client-configuration-settings51.md)

 

 





