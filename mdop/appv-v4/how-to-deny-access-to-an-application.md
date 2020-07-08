---
title: Cómo denegar acceso a una aplicación
description: Cómo denegar acceso a una aplicación
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817520"
---
# Cómo denegar acceso a una aplicación


Los usuarios deben estar en la lista de **permisos de acceso** de una aplicación para cargar y usar la aplicación. Aunque la consola de administración del servidor de virtualización de aplicaciones no admite la denegación explícita de acceso de un grupo de usuarios a una aplicación, puede quitar los grupos de usuarios de las propiedades de una aplicación para lograrlo.

**Para denegar el acceso a una aplicación**

1.  Para una aplicación existente, haga clic en el nodo **aplicaciones** en el panel izquierdo.

2.  Haga clic con el botón derecho en una aplicación en el panel derecho y elija **propiedades**. A continuación, seleccione la pestaña **permisos de acceso** .

3.  Para quitar el acceso para un grupo de usuarios, resalte el grupo de usuarios y haga clic en **quitar**.

4.  Haga clic en **Aceptar**.

    **Nota:**  Para controlar el acceso a las aplicaciones, también puede limitar las licencias de la aplicación. La configuración de los grupos de usuarios adecuados en servicios de dominio de Active Directory proporciona la manera más sencilla de conceder y denegar el acceso a conjuntos de usuarios específicos.

     

## Temas relacionados


[Cómo conceder acceso a una aplicación](how-to-grant-access-to-an-application.md)

[Cómo administrar licencias de aplicaciones en la consola de administración de servidor](how-to-manage-application-licenses-in-the-server-management-console.md)

[Cómo administrar aplicaciones en la consola de administración de servidor](how-to-manage-applications-in-the-server-management-console.md)

 

 





