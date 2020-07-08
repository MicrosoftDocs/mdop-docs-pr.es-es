---
title: Cómo crear y usar una plantilla de proyecto
description: Cómo crear y usar una plantilla de proyecto
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814247"
---
# Cómo crear y usar una plantilla de proyecto


Puede usar una plantilla de proyecto de App-V 5,1 para guardar la configuración aplicada comúnmente asociada con un paquete de aplicaciones virtual existente. Esta configuración se puede aplicar al crear nuevos paquetes de aplicaciones virtuales en el entorno. El uso de una plantilla de proyecto puede simplificar el proceso de creación de paquetes de aplicaciones virtuales.

**Nota**  
Puede, y a menudo, aplicar una plantilla de proyecto de App-V 5,1 durante una actualización de paquete. Por ejemplo, si ha secuencial una aplicación con una lista de exclusión personalizada, se recomienda crear y guardar una plantilla asociada para usarla más adelante durante la actualización de la aplicación de secuencia.



Las plantillas de proyecto de App-V 5,1 difieren de los aceleradores de aplicaciones de App-V 5,1 porque los aceleradores de aplicaciones de App-V 5,1 son específicos de la aplicación y las plantillas de proyecto de App-V 5,1 se pueden aplicar a varias aplicaciones.

Use los procedimientos siguientes para crear y aplicar una plantilla nueva.

**Para crear una plantilla de proyecto**

1.  Para iniciar el secuenciador de 5,1 de App-V, en el equipo que ejecuta el secuenciador, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  **Nota**  
    Si el paquete de aplicación virtual está abierto actualmente en la consola del secuenciador de App-V 5,1, vaya al paso 3 de este procedimiento.



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. En la consola de App-V 5,1 Sequencer, para guardar el archivo de plantilla, haga clic en **archivo**  /  **Guardar como plantilla**. Una vez que haya revisado la configuración que se guardará con la nueva plantilla, haga clic en **Aceptar**. Especifique un nombre que se asociará con la nueva plantilla de proyecto de App-V 5,1. Haga clic en guardar.

   La nueva plantilla de proyecto App-V 5,1 se guarda en el directorio especificado en el paso 3 de este procedimiento.

**Para aplicar una plantilla de proyecto**

1.  **Importante**  
    No se admite la creación de un paquete de aplicaciones virtual mediante una plantilla de proyecto junto con un acelerador de paquetes.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Para crear o actualizar un nuevo paquete de aplicaciones virtual con una plantilla de proyecto de App-V 5,1, haga clic en **archivo**  /  **nuevo a partir de plantilla**.

3. Para seleccionar la plantilla de proyecto que desea usar, vaya al directorio donde se guarda la plantilla de proyecto, seleccione la plantilla de proyecto y, a continuación, haga clic en **abrir**.

   Cree el nuevo paquete de aplicación virtual. La configuración guardada con la plantilla especificada se aplicará al nuevo paquete de aplicaciones virtual que está creando.

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)









