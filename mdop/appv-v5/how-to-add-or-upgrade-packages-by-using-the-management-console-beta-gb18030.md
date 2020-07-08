---
title: Cómo agregar o actualizar paquetes mediante el uso de la consola de administración
description: Cómo agregar o actualizar paquetes mediante el uso de la consola de administración
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814470"
---
# Cómo agregar o actualizar paquetes mediante el uso de la consola de administración


Puede realizar el procedimiento siguiente para agregar o actualizar un paquete a la consola de administración de App-V 5,0. Para actualizar un paquete que ya existe en la consola de administración, siga estos pasos e importe el paquete actualizado con el mismo **nombre**de paquete.

**Para agregar un paquete a la consola de administración**

1.  Haga clic en la ficha **paquetes** en el panel de navegación de la pantalla de la consola de administración.

    La consola muestra la lista de paquetes que se han agregado al servidor junto con la información de estado de cada paquete. Cuando se selecciona un paquete, se muestra información detallada sobre el paquete en el panel **paquetes** .

    Haga clic en el cuadro de lista desplegable **desagrupado** y especifique cómo se mostrarán los paquetes en la consola. También puede hacer clic en el encabezado de la columna asociada para ordenar los paquetes.

2.  Para especificar el paquete que desea agregar, haga clic en **Agregar o actualizar paquetes**.

3.  Escriba la ruta de acceso completa del paquete que desea agregar. Use el formato de ruta UNC o HTTP, por ejemplo **\\\\servername\\sharename\\foldername\\packagename.appv** o **http://server.1234/file.appv** y, a continuación, haga clic en **Agregar**.

    **Importante**  Debe seleccionar un paquete con la extensión de nombre de archivo **. appv** .

     

4.  La página muestra el mensaje de estado **agregando &lt; packagename &gt; **. Haga clic en **importar estado** para comprobar el estado de un paquete que ha importado.

    Haga clic en **Aceptar** para agregar el paquete y cerrar la página **Agregar paquete** . Si se produjo un error durante la importación, haga clic en **detalles** en la página de **importación de paquetes** para obtener más información. El paquete recién agregado está ahora disponible en el panel **paquetes** .

5.  Haga clic en **cerrar** para cerrar la página **Agregar o actualizar paquetes** .

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





