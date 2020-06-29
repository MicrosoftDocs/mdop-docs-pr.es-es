---
title: Cómo instalar el servidor de streaming de virtualización de aplicaciones
description: Cómo instalar el servidor de streaming de virtualización de aplicaciones
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817330"
---
# Cómo instalar el servidor de streaming de virtualización de aplicaciones


El servidor de streaming de Application Virtualization publica sus aplicaciones para los clientes. En un entorno con equilibrio de carga, que es típico de implementaciones grandes, todos los servidores de un grupo de servidores deben transmitir las mismas aplicaciones. Si los servidores de streaming de Application Virtualization van a transmitir aplicaciones distintas, asigne los servidores a diferentes grupos de servidores. En este caso, es posible que también tenga que aumentar la capacidad de un grupo de servidores.

Si ha designado un equipo de destino en la red, con una cuenta de inicio de sesión con privilegios administrativos locales, puede usar el siguiente procedimiento para instalar el servidor de streaming de virtualización de aplicaciones y asignarlo al grupo de servidores correspondiente.

**Nota:**  El Asistente para la instalación puede crear un registro de grupo de servidores, si no existe alguno, y un registro de la pertenencia a un servidor de streaming de Application Virtualization en este grupo.

 

Después de completar el proceso de instalación, reinicie el servidor.

**Para instalar un servidor de streaming de virtualización de aplicaciones**

1.  Compruebe que ninguna de las versiones anteriores del servidor de streaming de Application Virtualization están instaladas en el equipo de destino.

    **Importante**  Asegúrese de que el servidor de administración de App-V no esté instalado en este equipo. Los dos productos no se pueden instalar en el mismo equipo.

     

2.  Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en el archivo **Setup.exe** .

3.  En la página **principal** , haga clic en **siguiente**.

4.  En la página **contrato de licencia** , para aceptar los términos de licencia, seleccione Acepto **los términos y condiciones de la**licencia y, a continuación, haga clic en **siguiente**.

5.  En la página **información del cliente** , especifique el nombre de **usuario** y la organización y, a continuación, haga clic en **siguiente**.

6.  En la página **ruta de instalación** , haga clic en **examinar**, especifique la ubicación en la que desea instalar el servidor de streaming y, a continuación, haga clic en **siguiente**.

7.  En la página **modo de seguridad de conexión** , seleccione el certificado que desee de la lista desplegable y, a continuación, haga clic en **siguiente**.

    **Nota:**  La configuración del **modo de conexión segura** requiere que el servidor tenga un certificado de servidor provisto de una infraestructura de clave pública. Si un certificado de servidor no está instalado en el servidor, esta opción no está disponible y no se puede seleccionar. Debe conceder acceso de lectura a la cuenta de servicio de red al certificado que se está usando.

     

8.  En la página **configuración del puerto TCP** , para usar el puerto estándar (554), seleccione **usar puerto predeterminado (554)**. Para especificar un puerto personalizado, seleccione **usar puerto personalizado**, especifique el número de puerto en el campo correspondiente y, a continuación, haga clic en **siguiente**.

    **Nota:**  Al instalar el servidor en un escenario no seguro, puede usar el puerto predeterminado (554) o puede definir un puerto personalizado.

     

9.  En la página **raíz de contenido** , especifique la ubicación en el equipo de destino donde se guardarán los archivos de SFT y, a continuación, haga clic en **siguiente**.

    **Nota:**  Si el puerto HTTP o RTSP del servidor de streaming de aplicaciones virtuales ya está asignado, se le pedirá que seleccione un nuevo puerto. Especifique el puerto que desee y, a continuación, haga clic en **siguiente**.

     

10. En la pantalla **Configuración avanzada** , escriba la información siguiente:

    1.  **Número máximo de conexiones de cliente**

    2.  **Tiempo de espera de conexión (s)**

    3.  **Tamaño del grupo de subprocesos RTSP**

    4.  **Tiempo de espera de RTSP (SEC)**

    5.  **Número de procesos principales**

    6.  **Tiempo de espera del núcleo (SEC)**

    7.  **Habilitar autenticación de usuario**

    8.  **Habilitar autorización de usuario**

    9.  **Tamaño de bloque de caché (KB)**

    10. **Tamaño máximo de la caché (MB)**

    **Nota:**  El servidor de streaming de App-V usa permisos de sistema de archivos NTFS para controlar el acceso a las aplicaciones en el recurso compartido de contenido. Use **Habilitar autenticación de usuario** y **Habilitar autorización de usuario** para controlar si el servidor comprueba y aplica esas listas de control de acceso (ACL) o no.

     

11. En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.

12. En la pantalla Asistente para la **instalación finalizada** , haga clic en **Finalizar**para cerrar el asistente.

    **Importante**  La instalación puede demorar varios minutos en finalizar. Un mensaje de estado parpadeará por encima del área de notificación del escritorio de Windows, lo que indica que la instalación se realizó correctamente.

    No es necesario que reinicie el equipo cuando se le pida. Sin embargo, para optimizar el rendimiento del sistema, recomendamos un reinicio.

     

13. Repita los pasos 1 a 12 para cada servidor de aplicaciones virtual que tenga que instalar.

## Temas relacionados


[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)

 

 





