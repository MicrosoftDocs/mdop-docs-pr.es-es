---
title: Cómo usar Dynamic Suite Composition
description: Cómo usar Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816420"
---
# Cómo usar Dynamic Suite Composition


La composición de conjuntos dinámicos en la virtualización de aplicaciones le permite definir una aplicación como dependiente de otra aplicación, como un middleware o un complemento. Esto permite que la aplicación interactúe con el middleware o el complemento en el entorno virtual, donde normalmente esto se evita. Esto es útil porque un paquete de aplicación secundario se puede usar con varias aplicaciones, conocidas como *aplicaciones principales*, lo que permite que cada aplicación principal haga referencia al mismo paquete secundario.

Puede usar la composición de conjuntos dinámicos cuando secuencia aplicaciones que dependen de complementos, como controles ActiveX o para aplicaciones que dependen de middleware, como OLE DB o Java Runtime Environment (JRE). Si todas las aplicaciones que usaban estos componentes dependientes requirieron secuencias, incluidos los componentes, las actualizaciones de esos componentes requerirían volver a secuenciar todas las aplicaciones principales. Si se hace una secuencia de las aplicaciones principales sin los componentes y después se secuencia el middleware o el complemento como un paquete secundario, solo debe actualizarse el paquete secundario.

Una ventaja de este enfoque es que reduce el tamaño de los paquetes principales. Otra ventaja es que le proporciona un mayor control de los permisos de acceso en las aplicaciones secundarias. Tenga en cuenta que la aplicación secundaria se puede transmitir de la forma habitual y no es necesario que esté en la memoria caché completa para ejecutarla.

Un paquete principal puede tener más de un paquete secundario. Sin embargo, solo se admite un nivel de dependencia, por lo que no puede definir un paquete secundario como dependiente de otro paquete secundario. Además, la aplicación secundaria solo puede ser middleware o un complemento, y no puede ser otro producto de software completo.

Si tiene previsto hacer varias aplicaciones principales dependientes de un único producto middleware, asegúrese de probar esta configuración para determinar el efecto potencial en el rendimiento del sistema antes de implementarlo.

**Importante**  Las dependencias de paquetes pueden especificarse como obligatorias para una aplicación principal. Si un paquete secundario se marca como obligatorio y no se puede acceder a él por algún motivo durante la carga, la carga del paquete secundario fallará. Además, se producirá un error en la aplicación principal cuando el usuario intente iniciarla.

 

Puede usar los procedimientos siguientes para crear un paquete secundario, para un complemento o un componente middleware, y luego puede usar el procedimiento final para definir la dependencia en el archivo OSD del paquete secundario.

**Para crear un paquete secundario para un complemento con la composición de conjunto dinámico**

1.  En un equipo de secuencias que esté configurado con una imagen limpia, instale Application Virtualization Sequencer y guarde el estado del equipo.

2.  Ordene la aplicación principal y guarde el paquete en la carpeta de contenido en el servidor.

3.  Restaure el equipo de secuenciación a su estado guardado en el paso 1.

4.  Instale y configure la aplicación principal de forma local en el equipo de secuencias.

    **Importante**  Debes especificar una nueva raíz de paquete para el paquete secundario.

     

5.  Iniciar la fase de supervisión del secuenciador.

6.  Instale el complemento en el equipo de secuenciación y configúrelo según sea necesario.

7.  Abra la aplicación principal y confirme que el complemento está funcionando correctamente.

8.  En la consola del secuenciador, cree una aplicación ficticia que represente el paquete secundario que contendrá el complemento y seleccione un icono.

9.  Guarde el paquete en la carpeta de contenido en el servidor.

    **Nota:**  Para ayudar con la administración de paquetes secundarios, se recomienda que el nombre del paquete incluya el término "paquete secundario" para enfatizar que se trata de un paquete que no funcionará como una aplicación independiente; por ejemplo, **el paquete secundario \ [nombre de complemento \]**.

     

**Para crear un paquete secundario para un software intermedio con composición dinámica Suite**

1.  En un equipo de secuencias que esté configurado con una imagen limpia, instale Application Virtualization Sequencer y guarde el estado del equipo.

2.  Instale el middleware de forma local en el equipo de secuenciación y configúrelo.

3.  Ordene la aplicación principal y guarde el paquete en la carpeta de contenido en el servidor.

4.  Restaure el equipo de secuenciación a su estado guardado en el paso 1.

5.  Inicie el secuenciador para crear un nuevo paquete.

6.  Iniciar la fase de supervisión del secuenciador.

7.  Instale la aplicación middleware en el equipo de secuenciación y configúrela como en una instalación típica.

8.  Complete el proceso de secuenciación.

9.  Guarde el paquete en la carpeta de contenido en el servidor.

    **Nota:**  Para ayudar con la administración de paquetes secundarios, se recomienda que el nombre del paquete incluya el término "paquete secundario" para enfatizar que se trata de un paquete que no funcionará como una aplicación independiente, por ejemplo, un **paquete secundario de \ [nombre del middleware \]**.

     

**Para definir la dependencia en el paquete principal**

1. En el servidor, abra el archivo OSD del paquete secundario para su edición. (Es una buena idea usar un editor XML para realizar cambios en el archivo OSD; sin embargo, puede usar el Bloc de notas como alternativa).

2. Copie la línea **href del código base** desde ese archivo.

3. Abra el archivo OSD del paquete principal para su edición.

4. Inserte la <strong> &lt; etiqueta dependencies &gt; </strong> después de cerrar la etiqueta ** &lt; /ENVLIST &gt; ** al final de la sección ** &lt; VIRTUALENV &gt; ** justo antes de la etiqueta ** &lt; /VIRTUALENV &gt; ** .

5. Pegue la línea **href de código base** desde el paquete secundario después de la etiqueta de ** &lt; &gt; dependencias** que acaba de crear.

6. Si el paquete secundario es un paquete obligatorio, lo que significa que debe iniciarse antes de que se inicie el paquete principal, agregue la propiedad **obligatoria = "true"** dentro de la etiqueta **codebase** . Si no es obligatoria, se puede omitir la propiedad.

7. Para cerrar la etiqueta ** &lt; dependencies &gt; ** , inserte lo siguiente:

   **&lt;/DEPENDENCIES&gt;**

8. Revise los cambios realizados en el archivo OSD y, a continuación, guarde y cierre el archivo. En el ejemplo siguiente se muestra cómo debería aparecer la sección agregada. Los valores de la etiqueta que se muestran aquí solo son por ejemplo.

   **&lt;VIRTUALENV&gt;**

        **&lt;ENVLIST&gt;**

   **…**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **&lt;/VIRTUALENV&gt;**

9. Si el paquete secundario tiene entradas en la sección ** &lt; ENVLIST &gt; ** del archivo OSD, debe copiarlas en la misma sección del paquete principal.

## Temas relacionados


[Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





