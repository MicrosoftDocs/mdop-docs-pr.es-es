---
title: Cómo agregar manualmente una aplicación
description: Cómo agregar manualmente una aplicación
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817100"
---
# Cómo agregar manualmente una aplicación


Al agregar una aplicación al servidor de administración de virtualización de la aplicación, se recomienda que la importe. Puede Agregar una aplicación manualmente, pero debe proporcionar la información precisa y detallada sobre la aplicación a la que se ha llamado en esta sección.

**Para agregar manualmente una nueva aplicación**

1.  En el panel de la izquierda, haga clic con el botón derecho en el nodo **aplicaciones** y elija **nueva aplicación**.

2.  En el **Asistente para nueva aplicación**, complete el cuadro de diálogo **información general** :

    1.  **Nombre**de la aplicación: escriba el nombre que desea que vean los usuarios.

    2.  **Versión**: escriba la versión de la aplicación.

    3.  **Habilitado**: este cuadro debe estar seleccionado para transmitir la aplicación después de crearla.

    4.  **Descripción**: escriba una descripción opcional para el uso administrativo.

    5.  **Ruta de acceso a OSD**: examine la red hasta el archivo descriptor de software abierto (OSD) de la aplicación. Este archivo debe estar en una carpeta de red compartida.

    6.  **Ruta de icono**: Busque el archivo ICO de la aplicación.

    7.  **Grupo de licencias de aplicación**: Si ha configurado grupos de licencias, puede asignar la aplicación a una si la selecciona en la lista desplegable.

    8.  **Grupo de servidores**: Si tiene varios servidores de virtualización de aplicaciones, puede asignar la aplicación a uno seleccionándolo en la lista desplegable.

3.  Haz clic en **Siguiente**.

4.  En el cuadro de diálogo **seleccionar paquete** , seleccione el paquete relacionado y haga clic en **siguiente**.

5.  En la pantalla **accesos directos publicados** , seleccione las casillas de las ubicaciones en las que desea que aparezcan los accesos directos de la aplicación en los equipos cliente y haga clic en **siguiente**.

6.  En la pantalla **asociaciones de archivos** , puede agregar nuevas asociaciones de archivo de tipo a esta aplicación. Para ello, haga clic en **Agregar**, escriba la extensión (sin un punto anterior), escriba una descripción y haga clic en **Aceptar**.

7.  Haz clic en **Siguiente**.

8.  En el cuadro de diálogo **permisos de acceso** , haga clic en **Agregar**.

9.  En el cuadro de diálogo **Agregar/editar grupo de usuarios** , vaya al grupo de usuarios. También puede especificar el dominio y el grupo escribiendo la información en los campos respectivos. Cuando termine, haga clic en **Aceptar**. Puede agregar otros grupos con las mismas páginas.

10. Haz clic en **Siguiente**.

11. En la pantalla **Resumen** , puede revisar la configuración de importación. Haga clic en **Finalizar** para agregar la aplicación, haga clic en **atrás** para cambiar la información, o haga clic en **Cancelar**.

## Temas relacionados


[Cómo administrar aplicaciones en la consola de administración de servidor](how-to-manage-applications-in-the-server-management-console.md)

 

 





