---
title: Modificar la ruta de acceso del archivo
description: Modificar la ruta de acceso del archivo
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820491"
---
# Modificar la ruta de acceso del archivo


La ruta de acceso de archivo es la ubicación del archivo en relación con el servidor de AGPM. La ruta de acceso de archivo puede apuntar a una carpeta en el servidor de AGPM o en otro servidor del mismo bosque.

La ruta de acceso al archivo y la cuenta del servicio AGPM se configuran durante la instalación del servidor de AGPM y se pueden cambiar posteriormente mediante **Agregar o quitar programas** en el servidor de AGPM.

Una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso al servidor de AGPM (el equipo en el que está instalado Microsoft Advanced Group Management-Server) para completar este procedimiento.

**Para modificar la ruta de archivo**

1.  En el equipo en el que está instalado administración avanzada de directivas de grupo de Microsoft, haga clic en **Inicio**, haga clic en **Panel de control**, haga clic en **Agregar o quitar programas**.

2.  Haga clic en **Microsoft Advanced Group Management-Server**y, a continuación, haga clic en **cambiar**.

3.  Haga clic en **siguiente**y, a continuación, en **modificar**.

4.  Siga las instrucciones en pantalla para configurar la configuración del servicio AGPM:

    1.  Para la ruta de archivo, escriba una nueva ubicación para el archivo en relación con el servidor de AGPM. La ruta de acceso de archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero la ubicación debería tener suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.

    2.  Escriba las credenciales de la cuenta de servicio de AGPM.

        **Importante**  Al modificar la instalación, se borran las credenciales de la cuenta de servicio AGPM. Debe volver a escribir las credenciales, pero no es necesario que coincidan con las credenciales usadas durante la instalación original.

        La cuenta de servicio AGPM debe tener acceso completo a los GPO que administrará. Si va a administrar GPO en un solo dominio, puede convertir la cuenta del sistema local del controlador principal de dominio en la cuenta de servicio AGPM.

        Si va a administrar GPO en varios dominios o si un servidor miembro será el servidor de AGPM, debe configurar una cuenta diferente como cuenta de servicio de AGPM porque la cuenta del sistema local para un controlador de dominio no puede tener acceso a los GPO de otros dominios.

         

    3.  Para el propietario del archivo, escriba las credenciales de un administrador de AGPM (control total).

5.  Haga clic en **cambiar**y cuando se complete la instalación, haga clic en **Finalizar**.

### Referencias adicionales

-   [Administrar el servicio AGPM](managing-the-agpm-service.md)

 

 





