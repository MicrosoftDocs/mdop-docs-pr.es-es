---
title: Cómo actualizar el cliente de virtualización de aplicaciones
description: Cómo actualizar el cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816451"
---
# Cómo actualizar el cliente de virtualización de aplicaciones


Puede usar los procedimientos siguientes para actualizar el cliente de escritorio de Application Virtualization (App-V) o el cliente App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server). Para actualizar el cliente, instale una nueva versión sobre la versión anterior instalada previamente. Al actualizar los clientes, el software del instalador automáticamente conserva y migra la configuración del usuario para las aplicaciones virtuales. Los derechos administrativos son necesarios para ejecutar el programa de instalación.

**Nota:**  Durante la actualización a Application Virtualization (App-V) 4.5 o versiones posteriores, los permisos para la clave del registro HKCU cambian. Por ello, los usuarios perderán las configuraciones de usuario que se establecieron anteriormente, como la configuración del modo desconectado configurado por el usuario. Si el usuario no tiene permisos de forma activa para configurar el comportamiento de la interfaz de usuario del cliente mediante un bloqueo de permisos, el usuario puede restablecer estas preferencias después de una actualización de publicación.

 

**Importante**  Al actualizar a la versión 4.6 o a una versión posterior del cliente de App-V, debe usar el instalador correcto para el sistema operativo del equipo, 32 bits o 64 bits. La instalación no se realizará y aparecerá un mensaje de error si usa el instalador equivocado.

 

**Para actualizar el cliente de escritorio de virtualización de aplicaciones**

1.  Cierre todas las aplicaciones virtuales, haga clic con el botón derecho en el icono del cliente de escritorio de App-V que aparece en el área de notificación del escritorio de Windows y seleccione **salir** para cerrar el cliente existente.

2.  Una vez que haya obtenido el archivo de instalación de instalador correcto y lo haya guardado en el equipo, haga doble clic en él para expandir el archivo.

3.  Busque el archivo de setup.exe y haga doble clic en setup.exe para iniciar la instalación.

4.  El asistente comprueba el sistema para asegurarse de que haya instalado todo el software necesario y le pedirá que instale cualquiera de las siguientes opciones, si no la encuentra:

    -   Paquete redistribuible Microsoft VisualC + + 2005SP1 (x86)

    -   Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

    -   Informes de errores de aplicaciones de Microsoft

    **Nota:**  Para la versión 4.6 o superior, el Asistente también instalará el siguiente requisito previo de software:

    -   Paquete redistribuible Microsoft VisualC + + 2008SP1 (x86)

     

5.  Haz clic en **Instalar**. Se muestra el progreso de instalación y el estado cambia de **pendiente** a **instalación**. El estado de la instalación cambiará a **correcto** , ya que cada paso se completa correctamente.

6.  Cuando aparezca el cuadro de diálogo de **cliente de escritorio de Application Virtualization** y se muestre un mensaje que indica que se ha encontrado una versión anterior del cliente en el equipo, haga clic en **siguiente** para actualizar a la nueva versión.

7.  Cuando aparezca la pantalla **contrato de licencia** , lea el contrato de licencia y, si está de acuerdo, haga clic en Acepto **las condiciones del contrato de licencia**y, a continuación, haga clic en **siguiente**.

8.  Cuando el asistente InstallShield muestra la pantalla de diálogo **listo para actualizar el programa** , haga clic en **Actualizar** para iniciar la actualización. La siguiente pantalla indica que el cliente se está instalando.

    **ADVERTENCIA**  Si no ha cerrado el programa cliente en el paso 1, es posible que aparezca la advertencia **archivos en uso** . Si esto sucede, haga clic con el botón derecho en el icono del cliente de App-V que se muestra en el área de notificación del escritorio y seleccione **salir** para cerrar el cliente existente. A continuación, haga clic en **Reintentar** para continuar.

     

9.  Cuando la instalación se complete correctamente, se le pedirá que reinicie el equipo. Debe reiniciar el equipo para completar la instalación.

    **PRECAUCIÓN**  Si la actualización no se realiza por algún motivo, tendrá que reiniciar el equipo antes de volver a intentar la actualización.

     

**Para actualizar el cliente de virtualización de aplicaciones mediante la línea de comandos**

1.  Si actualiza el cliente de App-V con el programa setup.msi, asegúrese de que se haya instalado todo el software necesario.

    **Importante**  
    -   Para la versión 4.6 y posteriores del cliente de App-V, el programa de setup.msi comprueba el sistema y generará un mensaje de error que indica que la instalación no puede continuar si el software necesario no está instalado.

    -   Para la versión 4.6 de App-V, los parámetros de la línea de comandos no se pueden usar durante una actualización y se omitirán.

     

2.  En el siguiente ejemplo de línea de comandos se usa el archivo setup.msi para actualizar el cliente de App-V. Tendrá que usar el programa de instalación de cliente correcto, en función de si está actualizando el cliente de escritorio de App-V o el cliente App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server).

    **msiexec.exe/i "setup.msi"**

    **Importante**  Las comillas solo son necesarias cuando el valor contiene un espacio. Por coherencia, todas las instancias del ejemplo anterior se muestran con comillas.

     

**Para actualizar el cliente de virtualización de aplicaciones para servicios de escritorio remoto**

1.  Siga las directivas estándar de su organización para instalar o actualizar aplicaciones en el servidor de host de sesión de escritorio remoto (host RDSession). Si el sistema forma parte de un conjunto de servidores, quite el host RDSession del conjunto de servidores.

2.  Para actualizar el cliente de App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server), debe usar la línea de comandos porque no puede actualizar el cliente manualmente en el host de RDSession.

    **Nota:**  En la versión 4,6 y posteriores de App-V, además de usar la línea de comandos para actualizar el cliente, también puede usar una sesión de escritorio remoto. No se necesitan parámetros especiales para iniciar la sesión de escritorio remoto.

     

3.  Una vez completada la actualización del cliente para servicios de escritorio remoto, reinicie e inicie sesión en el host RDSession.

4.  Después de reiniciar el sistema, agregue el servidor a la granja de servidores.

    **PRECAUCIÓN**  Si la actualización no se realiza por algún motivo, tendrá que reiniciar el equipo antes de volver a intentar la actualización.

     

## Temas relacionados


[Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





