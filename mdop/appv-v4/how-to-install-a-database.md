---
title: Cómo instalar una base de datos
description: Cómo instalar una base de datos
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817380"
---
# Cómo instalar una base de datos


Puede usar el siguiente procedimiento para instalar una base de datos para la implementación basada en servidor de la virtualización de aplicaciones si aún no está disponible una base de datos. Por lo general, en un entorno de producción, se conectará a una base de datos existente.

**Importante**  Para instalar la base de datos, debe usar una cuenta de red con los permisos adecuados. Si su organización requiere que solo los administradores de bases de datos puedan crear y llevar a cabo actualizaciones de la base de datos, están disponibles las secuencias de comandos que permiten realizar esta tarea.

 

**Para instalar una base de datos**

1.  Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en **Setup.exe**.

2.  En la **Página principal**, haga clic en **siguiente**.

3.  En la página **contrato de licencia** , para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de licencia**y haga clic en **siguiente**.

4.  En la página **información de registro** , especifique el **nombre de usuario** y la información de la **organización** y, a continuación, haga clic en **siguiente**.

5.  En la página **tipo de configuración** , seleccione **personalizado** y, a continuación, haga clic en **siguiente**.

6.  En la página **Configuración personalizada** , anule la selección de todos los componentes del sistema de Application Virtualization, excepto **servidor de virtualización de aplicaciones**y haga clic en **siguiente**.

    **Nota:**  Si un componente ya está instalado en el equipo, anulando la selección en la pantalla de **instalación personalizada** , se desinstalará automáticamente.

     

7.  En la página **servidor de base de datos** , escriba las contraseñas, asigne una ruta de instalación, guarde la información y haga clic en **siguiente**.

8.  Seleccione un nombre para la base de datos y, a continuación, haga clic en **siguiente**.

    **Nota:**  Si se muestra el error 25109 al intentar completar este paso, no ha configurado correctamente los permisos necesarios para instalar la base de datos. Para obtener más información sobre cómo configurar los permisos de SQL necesarios, consulte <https://go.microsoft.com/fwlink/?LinkId=132144> .

     

9.  En la pantalla **servidor de directorio** , escriba un nombre de dominio y las credenciales que usarán los servidores de virtualización de aplicaciones y el servicio Web de administración para obtener acceso al controlador de dominio, guarde esta información y, a continuación, haga clic en **siguiente**.

    **Nota:**  La instalación se establecerá de forma predeterminada en el dominio del equipo actual.

     

10. En la página **grupo de administradores** , escriba el nombre de un grupo que tendrá privilegios de administrador, guarde esta información y, a continuación, haga clic en **siguiente**.

    **Nota:**  También puede introducir los primeros caracteres del nombre de un grupo que tendrá privilegios de administración, hacer clic en **siguiente**y, en la pantalla **Seleccionar grupo de administradores** , seleccionar el grupo de la lista resultante. A continuación, guarda esta información y haz clic en **siguiente**.

     

11. En la página **grupo de proveedores predeterminado** , escriba el nombre completo de un grupo que controlará el acceso a las aplicaciones, guarde esta información y, a continuación, haga clic en **siguiente**.

    **Nota:**  También puede introducir los primeros caracteres del nombre de un grupo que controlará el acceso a las aplicaciones, hacer clic en **siguiente**y, en la pantalla **Seleccionar grupo de proveedores predeterminado** , seleccione el grupo en la lista. A continuación, guarda esta información y haz clic en **siguiente**.

     

12. En la página Asistente para la **instalación finalizada** , haga clic en **Finalizar**para cerrar el asistente.

    **Importante**  La instalación puede demorar unos minutos en finalizar. Un mensaje de estado parpadeará por encima del área de notificación del escritorio de Windows, lo que indica si la instalación se realizó correctamente.

     

## Temas relacionados


[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)

 

 





