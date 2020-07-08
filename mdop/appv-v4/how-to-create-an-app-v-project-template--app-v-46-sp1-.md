---
title: Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)
description: Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817650"
---
# Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)


Puede usar una plantilla de proyecto de App-V para guardar la configuración que se aplica normalmente asociada a un paquete de aplicaciones virtual existente. Esta configuración se puede aplicar al crear nuevos paquetes de aplicaciones virtuales en su entorno, lo que puede ayudarle a simplificar el proceso de creación de paquetes de aplicaciones virtuales.

**Nota:**  Solo puede aplicar una plantilla de proyecto de App-V al crear un nuevo paquete de aplicaciones virtual. No se admite la aplicación de plantillas de proyecto a paquetes de aplicaciones virtuales existentes.

 

Para obtener más información sobre cómo aplicar una plantilla de proyecto de App-V, consulte [Cómo aplicar una plantilla de proyecto de App-v (App-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).

Las plantillas de proyecto de App-V difieren de los aceleradores de aplicaciones de App-V porque los aceleradores de aplicaciones de App-V son específicos de la aplicación y las plantillas de proyecto de App-V pueden aplicarse a varias aplicaciones. Además, no puede usar una plantilla de proyecto cuando usa un acelerador de paquetes para crear un paquete de aplicaciones virtual.

La siguiente configuración general se guarda con una plantilla de proyecto de App-V:

-   **Opciones de supervisión avanzadas**. Permite que Microsoft Update se ejecute durante la supervisión, el **archivo. dll**.

-   **Configuración**de la implementación del paquete. Contiene el **Protocolo**, **el nombre de host, el** **Puerto**, la **ruta de acceso**, **sistemas operativos**, **exigir descriptores de seguridad**, **crear MSI**, **comprimir paquete**.

-   **Opciones generales**. Le permite generar un paquete de **Microsoft Windows Installer (MSI)** , **permitir la virtualización de eventos**, **permitir la virtualización de servicios**, **anexar la versión del paquete al nombre de archivo**.

-   **Elementos de exclusión**. Contiene la lista de patrones de exclusión.

**Para crear una plantilla de proyecto**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Si el paquete de aplicación virtual está abierto actualmente en el secuenciador de App-V, vaya al paso 3 de este procedimiento. Para abrir el paquete de la aplicación virtual existente que contiene la configuración que desea guardar con la plantilla de proyecto de APP- **File**V, haga clic en  /  **abrir** archivo y haga clic en **Editar** **paquete**. En la página **seleccionar paquete** , haga clic en **examinar** y busque el paquete de aplicación virtual que desea abrir. Haz clic en **Editar**.

3.  En la consola del secuenciador de App-V **File**, haga clic en  /  **Guardar como plantilla**de archivo. Una vez que haya revisado la configuración que se guardará con la nueva plantilla, haga clic en **Aceptar**. Especifique un nombre que se asociará a la nueva plantilla de proyecto de App-V. Haga clic en **Guardar**.

    La nueva plantilla de proyecto App-V se guarda en el directorio especificado en el paso 3 de este procedimiento.

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Cómo aplicar una plantilla de proyecto de App-V (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





