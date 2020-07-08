---
title: Cómo configurar servidores de publicación
description: Cómo configurar servidores de publicación
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816530"
---
# Cómo configurar servidores de publicación


Puede usar los procedimientos siguientes para agregar y configurar servidores de virtualización de aplicaciones directamente desde la consola de administración de clientes.

**Para agregar un servidor de publicación de aplicaciones**

1.  En el panel de **resultados** , haga clic con el botón secundario del mouse y seleccione **nuevo servidor** en el menú emergente para iniciar el nuevo Asistente para servidor de virtualización de aplicaciones, o bien, haga clic con el botón derecho en el nodo **Publishing Server** y seleccione **nuevo servidor** en el menú emergente.

2.  En la página uno del asistente, escriba el nombre del servidor en el campo **nombre para mostrar** y seleccione el tipo de servidor de la lista desplegable **tipo** . Puede elegir **Application Virtualization Server**, **servidor de virtualización de aplicaciones de seguridad mejorada**, servidor **http estándar**o **servidor HTTP de seguridad mejorado** de la lista desplegable de tipos de servidor.

3.  Haz clic en **Siguiente**.

4.  En la página dos del asistente, escriba la información adecuada en los campos **nombre de host** y **Puerto** . El campo **path** no se puede editar en servidores de virtualización de aplicaciones. Debes escribir una ruta de acceso para el servidor HTTP estándar o el servidor HTTP de seguridad mejorado.

5.  Haga clic en **Finalizar** para agregar el servidor.

**Para configurar un servidor de publicación de aplicaciones**

1.  En el panel de **resultados** , haga clic con el botón derecho en el servidor deseado y seleccione **propiedades** en el menú emergente.

2.  Haga clic en la pestaña **General** , donde puede cambiar el nombre del servidor, seleccionar un tipo de la lista desplegable de tipos de servidor y especificar el nombre de host y el puerto. Cuando el tipo de servidor es un servidor HTTP estándar o un servidor HTTP de seguridad mejorado, el campo **ruta** también se puede editar.

3.  Haga clic en la pestaña **Actualizar** , donde la casilla **de verificación actualizar la publicación en el inicio de sesión del usuario** está activada de forma predeterminada. Para cambiar la frecuencia de actualización, active la casilla **Actualizar publicación cada** y escriba un número que represente la frecuencia en el campo. A continuación, seleccione **minutos**, **horas**y **días** en el menú desplegable. (La cantidad mínima de tiempo que puedes introducir es de 30 minutos).

4.  Haga clic en **aplicar** para cambiar la configuración.

5.  Cuando haya terminado de publicar, haga clic en **Aceptar** para salir del cuadro de diálogo y volver a la consola de administración de cliente.

## Temas relacionados


[Cómo deshabilitar o modificar la configuración de modo de operación desconectado](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





