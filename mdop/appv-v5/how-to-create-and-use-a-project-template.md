---
title: Cómo crear y usar una plantilla de proyecto
description: Cómo crear y usar una plantilla de proyecto
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814262"
---
# Cómo crear y usar una plantilla de proyecto


Puede usar una plantilla de proyecto de App-V 5,0 para guardar la configuración aplicada comúnmente asociada con un paquete de aplicaciones virtual existente. Esta configuración se puede aplicar al crear nuevos paquetes de aplicaciones virtuales en el entorno. El uso de una plantilla de proyecto puede simplificar el proceso de creación de paquetes de aplicaciones virtuales.

**Nota:**  Puede, y a menudo, aplicar una plantilla de proyecto de App-V 5,0 durante una actualización de paquete. Por ejemplo, si ha secuencial una aplicación con una lista de exclusión personalizada, se recomienda crear y guardar una plantilla asociada para usarla más adelante durante la actualización de la aplicación de secuencia.

Las plantillas de proyecto de App-V 5,0 difieren de los aceleradores de aplicaciones de App-V 5,0 porque los aceleradores de aplicaciones de App-V 5,0 son específicos de la aplicación y las plantillas de proyecto de App-V 5,0 se pueden aplicar a varias aplicaciones.

Use los procedimientos siguientes para crear y aplicar una plantilla nueva.

**Para crear una plantilla de proyecto**

1.  Para iniciar el secuenciador de 5,0 de App-V, en el equipo que ejecuta el secuenciador, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

**Nota:**  Si el paquete de aplicación virtual está abierto actualmente en la consola del secuenciador de App-V 5,0, vaya al paso 3 de este procedimiento.

2. Para abrir el paquete de la aplicación virtual existente que contiene la configuración que desea guardar con la plantilla de proyecto App-V 5,0 **File**, haga clic en  /  **abrir**archivo y, a continuación, haga clic en **Editar paquete**. En la página **seleccionar paquete** , haga clic en **examinar** y busque el paquete de aplicación virtual que desea abrir. Haz clic en **Editar**.

3. En la consola de App-V 5,0 Sequencer, para guardar el archivo de plantilla, haga clic en **archivo**  /  **Guardar como plantilla**. Una vez que haya revisado la configuración que se guardará con la nueva plantilla, haga clic en **Aceptar**. Especifique un nombre que se asociará con la nueva plantilla de proyecto de App-V 5,0. Haga clic en guardar.
   La nueva plantilla de proyecto App-V 5,0 se guarda en el directorio especificado en el paso 3 de este procedimiento.

**Para aplicar una plantilla de proyecto**

**Importante**  No se admite la creación de un paquete de aplicaciones virtual mediante una plantilla de proyecto junto con un acelerador de paquetes.

1.  Para iniciar el secuenciador de 5,0 de App-V, en el equipo que ejecuta el secuenciador, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para crear o actualizar un nuevo paquete de aplicaciones virtual con una plantilla de proyecto de App-V 5,0, haga clic en **archivo**  /  **nuevo a partir de plantilla**.

3.  Para seleccionar la plantilla de proyecto que desea usar, vaya al directorio donde se guarda la plantilla de proyecto, seleccione la plantilla de proyecto y, a continuación, haga clic en **abrir**.

    Cree el nuevo paquete de aplicación virtual. La configuración guardada con la plantilla especificada se aplicará al nuevo paquete de aplicaciones virtual que está creando.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)









