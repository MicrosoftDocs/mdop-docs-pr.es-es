---
title: Configurar aplicaciones y extensiones de aplicaciones virtuales predeterminadas en la consola de administración
description: Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814703"
---
#   Configurar aplicaciones y extensiones de aplicaciones virtuales predeterminadas en la consola de administración

Use el procedimiento siguiente para *Ver* y *configurar* las extensiones de paquete predeterminadas.

**Para ver y configurar extensiones de aplicaciones virtuales predeterminadas**

1.  Para ver el paquete que desea configurar, abra la consola de administración de App-V 5,1. Seleccione el paquete que desea configurar, haga clic con el botón secundario en el nombre del paquete y seleccione **Editar configuración predeterminada**.

2.  Para ver las aplicaciones contenidas en el paquete especificado, en el panel **configuración predeterminado** , haga clic en **aplicaciones**. Para ver los accesos directos de ese paquete, haga clic en **accesos directos**. Para ver las asociaciones de los tipos de archivo de ese paquete, haga clic en **tipos de archivo**.

3.  Para habilitar las extensiones de la aplicación, seleccione **Habilitar**.

    Para habilitar los métodos abreviados, seleccione **Habilitar métodos abreviados**. Para agregar un nuevo acceso directo para la aplicación seleccionada, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Agregar nuevo acceso directo**. Para quitar un acceso directo, haga clic con el botón derecho en la aplicación en el panel de **accesos directos** y seleccione **Quitar acceso directo**. Para editar un acceso directo existente, haga clic con el botón derecho en la aplicación y seleccione **Editar acceso directo**.

4.  Para ver cualquier otra extensión de la aplicación, haga clic en **avanzadas** y en **exportar configuración**. Escriba un nombre de archivo y haga clic en **Guardar**. Puede ver todas las extensiones de aplicaciones asociadas con el paquete mediante el archivo de configuración.

5.  Para editar otras extensiones de aplicaciones, modifique el archivo de configuración y haga clic en **importar y sobrescriba esta configuración**. Seleccione el archivo modificado y haga clic en **abrir**. En el cuadro de diálogo, haga clic en **sobrescribir** para completar el proceso.

>**Nota:** Si se produce un error en la carga y el tamaño del archivo de configuración es superior a 4 MB, tendrá que aumentar el tamaño de archivo máximo permitido por el servidor. Esto puede hacerse agregando el atributo maxRequestLength con un valor mayor que el tamaño del archivo de configuración (en KB) al elemento httpRuntime de la línea 26 de `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .  
Por ejemplo, si cambia `<httpRuntime targetFramework="4.5"/>` para `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` aumentar el tamaño máximo a 8 MB


**¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





