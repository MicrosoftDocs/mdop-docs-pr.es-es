---
title: Cómo configurar Windows Server 2008 para servidores de administración de App-V
description: Cómo configurar Windows Server 2008 para servidores de administración de App-V
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817721"
---
# Cómo configurar Windows Server 2008 para servidores de administración de App-V


El servidor de Windows Server 2008 en el que se instala el servicio Web de administración de Microsoft Application Virtualization (App-V) requiere que los servicios de Internet Information Services (IIS) se instalen como un rol en el servidor. Use el siguiente procedimiento para configurar Windows Server 2008 para admitir la instalación de App-vServer.

**Para instalar IIS en un equipo con Windows Server2008**

1.  En el equipo con Windows Server2008, haga clic en **Inicio**, haga clic en **todos los programas**, en **herramientas administrativas**y, a continuación, haga clic en **Administrador de servidores** para iniciar el administrador del servidor. En Administrador del servidor, haga clic con el botón secundario en el nodo **roles** y haga clic en **Agregar roles** para iniciar el **Asistente para agregar roles**.

2.  En el **Asistente para agregar roles**, en la página **Seleccionar roles de servidor** , seleccione **servidor Web (IIS)**. Cuando se le solicite, haga clic en **Agregar características obligatorias** para agregar las características dependientes.

3.  En la página **Seleccionar roles de servidor** , haga clic en **siguiente**y, después, vuelva a hacer clic en **siguiente** .

4.  En el **Asistente para agregar roles**, en la página **seleccionar servicios de rol** :

    1.  En **desarrollo de aplicaciones**, seleccione **ASP.net** y, cuando se le solicite, haga clic en **Agregar servicios de rol obligatorios** para agregar las características y los servicios de roles dependientes.

    2.  En **seguridad**, seleccione **autenticación de Windows**.

    3.  En el nodo **herramientas de administración** , seleccione **herramientas y scripts de administración de IIS**. En **compatibilidad con Iis6 Management**, asegúrese de que estén seleccionadas la compatibilidad con IIS de **IIS6 metabase Compatibility** y **IIS6** y, después, haga clic en **siguiente**.

5.  En la página **confirmar selecciones de instalación** , haga clic en **instalar**y, a continuación, complete el resto del asistente.

6.  Haga clic en **cerrar** para salir del **Asistente para agregar roles**y, a continuación, cierre el administrador del servidor.

## Temas relacionados


[Requisitos de implementación de virtualización de aplicaciones](application-virtualization-deployment-requirements.md)

[Implementación de virtualización de aplicaciones y listas de comprobación de actualización](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





