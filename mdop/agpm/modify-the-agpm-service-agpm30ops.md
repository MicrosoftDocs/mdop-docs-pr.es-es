---
title: Modificar el servicio AGPM
description: Modificar el servicio AGPM
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820501"
---
# Modificar el servicio AGPM


El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción. Si este servicio se detiene o deshabilita, los clientes de AGPM no podrán realizar operaciones a través del servidor. Puede modificar la ruta de acceso al archivo, la cuenta del servicio AGPM y el puerto en el que escucha el servicio AGPM.

**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo. Esto puede impedir que el servicio AGPM se inicie.

 

Una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso al servidor de AGPM (el equipo en el que está instalado Microsoft Advanced Group Management-Server) para completar este procedimiento. Además, debe proporcionar las credenciales de la cuenta de servicio de AGPM para completar este procedimiento.

**Para modificar el servicio AGPM**

1.  En el equipo en el que está instalado administración avanzada de directivas de grupo de Microsoft (servidor):

    -   Para WindowsServer2008, haga clic en **Inicio**, **Panel de control**, y **programas y características**.

    -   Para vista, haga clic en **Inicio**, **Panel de control**, **programas**y **programas y características**.

2.  Haga clic con el botón secundario en **Administración avanzada de directivas de grupo de Microsoft**y, a continuación, haga clic en **cambiar**.

3.  Haga clic en **siguiente**y, a continuación, en **modificar**.

4.  Siga las instrucciones para configurar el servicio AGPM:

    1.  En el cuadro de diálogo **ruta de acceso del archivo** , escriba una nueva ubicación para el archivo en relación con el servidor de AGPM o confirme la ruta de archivo actual y, a continuación, haga clic en **siguiente**.

        **Importante**  La ruta de acceso de archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero la ubicación debería tener suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.

         

    2.  En el cuadro de diálogo **cuenta de servicio AGPM** , escriba las credenciales de una cuenta de servicio en la que se ejecutará el servicio AGPM y haga clic en **siguiente**.

        **Importante**  Al modificar la instalación, se borran las credenciales de la cuenta de servicio AGPM. Debe volver a escribir las credenciales, pero no es necesario que coincidan con las credenciales usadas durante la instalación original.

        La cuenta de servicio de AGPM debe tener acceso completo a los GPO que se van a administrar y se le concederá permiso **de inicio de sesión como servicio** . Si va a administrar GPO en un solo dominio, puede convertir la cuenta del sistema local del controlador principal de dominio en la cuenta de servicio AGPM.

        Si va a administrar GPO en varios dominios o si un servidor miembro será el servidor de AGPM, debe configurar una cuenta diferente como cuenta de servicio de AGPM porque la cuenta del sistema local para un controlador de dominio no puede tener acceso a los GPO de otros dominios.

         

    3.  En el cuadro de diálogo **propietario del archivo** , escriba el nombre de usuario de un administrador de AGPM (control total) o de un grupo de administradores de AGPM y haga clic en **siguiente**.

        **Nota:**  Al modificar la instalación, se borran las credenciales del propietario del archivo. Debe volver a escribir las credenciales, pero no es necesario que coincidan con las credenciales usadas durante la instalación original.

         

    4.  En el cuadro de diálogo **configuración de Puerto** , escriba un nuevo puerto en el que el servicio AGPM debe escuchar o confirmar el puerto seleccionado actualmente y haga clic en **siguiente**.

        **Nota:**  De forma predeterminada, el servicio AGPM escucha en el puerto 4600.

        Si configura manualmente las excepciones de puerto o tiene reglas de configuración de excepciones de puerto, puede desactivar la casilla **Agregar excepción al firewall** .

         

5.  Haga clic en **cambiar**y cuando se complete la instalación, haga clic en **Finalizar**.

6.  Si ha cambiado el puerto en el que el servicio AGPM escucha, modifique el puerto en la conexión del servidor de AGPM para cada administrador de directiva de grupo. Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm30ops.md).

7.  Repita el procedimiento para cada servidor de AGPM al que deben aplicarse los cambios de configuración.

### Referencias adicionales

-   [Administrar el servicio AGPM](managing-the-agpm-service-agpm30ops.md)

 

 





