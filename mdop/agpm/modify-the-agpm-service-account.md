---
title: Modificar la cuenta de servicio AGPM
description: Modificar la cuenta de servicio AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820521"
---
# Modificar la cuenta de servicio AGPM


El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción. Si este servicio se detiene o deshabilita, los clientes de AGPM no podrán realizar operaciones a través del servidor.

La ruta de acceso al archivo y la cuenta del servicio AGPM se configuran durante la instalación del servidor de AGPM y se pueden cambiar posteriormente mediante **Agregar o quitar programas** en el servidor de AGPM.

**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo. Esto puede impedir que el servicio AGPM se inicie.

 

Una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso al servidor de AGPM (el equipo en el que está instalado Microsoft Advanced Group Management-Server) para completar este procedimiento.

**Importante**  La cuenta de servicio de AGPM debe tener acceso completo a los GPO que se van a administrar y se le concederá permiso **de inicio de sesión como servicio** . Si va a administrar GPO en un solo dominio, puede convertir la cuenta del sistema local del controlador principal de dominio en la cuenta de servicio AGPM.

Si va a administrar GPO en varios dominios o si un servidor miembro será el servidor de AGPM, debe configurar una cuenta diferente como cuenta de servicio de AGPM porque la cuenta del sistema local para un controlador de dominio no puede tener acceso a los GPO de otros dominios.

 

**Para modificar la cuenta de servicio de AGPM**

1.  En el equipo en el que está instalado administración avanzada de directivas de grupo de Microsoft, haga clic en **Inicio**, haga clic en **Panel de control**, haga clic en **Agregar o quitar programas**.

2.  Haga clic en **Microsoft Advanced Group Management-Server**y, a continuación, haga clic en **cambiar**.

3.  Haga clic en **siguiente**y, a continuación, en **modificar**.

4.  Siga las instrucciones en pantalla para configurar la configuración del servicio AGPM:

    1.  Para la ruta de archivo, confirme o cambie la ubicación del archivo en relación con el servidor de AGPM. La ruta de acceso de archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero la ubicación debería tener suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.

    2.  Escriba nuevas credenciales para la cuenta de servicio de AGPM.

    3.  Para el propietario del archivo, escriba las credenciales de un administrador de AGPM (control total).

5.  Haga clic en **cambiar**y cuando se complete la instalación, haga clic en **Finalizar**.

### Referencias adicionales

-   [Administrar el servicio AGPM](managing-the-agpm-service.md)

 

 





