---
title: Cómo instalar la consola de administración
description: Cómo instalar la consola de administración
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817301"
---
# Cómo instalar la consola de administración


Puede usar el siguiente procedimiento para instalar la consola de administración de virtualización de aplicaciones en un equipo de destino de la red. Debe usar una cuenta de red que tenga privilegios de administrador en el equipo de destino. Puede usar la consola para configurar y administrar la plataforma del sistema de virtualización de aplicaciones.

Para poder completar este procedimiento, debe instalar el servicio Web de administración de virtualización de aplicaciones en este equipo o en otro. El servicio Web de administración le permite obtener acceso al almacén de datos y al controlador de dominio. Para obtener más información sobre cómo instalar el servicio Web, vea [Cómo instalar el servicio Web de administración](how-to-install-the-management-web-service.md).

**Para instalar la consola de administración**

1.  Compruebe que ninguna de las versiones anteriores de la consola de administración estén instaladas en el equipo de destino.

2.  Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en **Setup.exe**.

3.  En la **Página principal**, haga clic en **siguiente**.

4.  En la página **contrato de licencia** , para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de licencia**y, a continuación, haga clic en **siguiente**.

5.  En la página **información de registro** , especifique el nombre de **usuario** y la información de la **organización** y, a continuación, haga clic en **siguiente**.

6.  En la página **tipo de configuración** , haga clic en **personalizar** y, a continuación, haga clic en **siguiente**.

7.  En la página **Configuración personalizada** , anule la selección de todos los componentes del sistema de Application Virtualization, excepto la **consola de administración**y haga clic en **siguiente**.

    **Nota:**  Si un componente ya está instalado en el equipo, anulando la selección en la pantalla de instalación personalizada, se desinstalará automáticamente.

     

8.  En la pantalla **listo para modificar el programa** , haga clic en **instalar**.

    **Nota:**  Si este es el primer componente que instala, se muestra la página **preparado para instalar el programa** . Para iniciar la instalación, haga clic en **instalar**.

     

9.  En la pantalla **Asistente para la instalación completada** , haga clic en **Finalizar**. Haga clic en **Aceptar** para reiniciar el equipo y completar la instalación.

10. En el panel de control de Windows, haga doble clic en **herramientas administrativas** y, a continuación, en **consola de administración de Application Virtualization** para mostrar la consola de administración.

11. Haga clic en el icono **conectar** , o haga clic con el botón secundario en el contenedor **sistemas de virtualización de aplicaciones** y luego haga clic en **conectar con el sistema de virtualización de aplicaciones**.

12. En la pantalla **conectar a Application Virtualization System** , escriba el nombre de host y el puerto del equipo de servicio Web de administración, cambie la información de seguridad y las credenciales de inicio de sesión si es necesario, y haga clic en **Aceptar**.

13. Después de conectar con el equipo del servicio Web de administración, haga clic en **archivo** en el menú de **consola** y, a continuación, haga clic en **salir**. Haga clic en **sí** para guardar la configuración de la consola.

## Temas relacionados


[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)

 

 





