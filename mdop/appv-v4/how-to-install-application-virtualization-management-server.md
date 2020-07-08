---
title: Cómo instalar el servidor de administración de virtualización de aplicaciones
description: Cómo instalar el servidor de administración de virtualización de aplicaciones
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817361"
---
# Cómo instalar el servidor de administración de virtualización de aplicaciones


El servidor de administración de virtualización de aplicaciones publica sus aplicaciones para los clientes. En un entorno con equilibrio de carga, que es típico de implementaciones grandes, todos los servidores de un grupo de servidores deben transmitir las mismas aplicaciones. Si los servidores de administración de Application Virtualization van a publicar distintas aplicaciones, asigne los servidores a diferentes grupos de servidores. En este caso, es posible que también tenga que aumentar la capacidad de un grupo de servidores.

Si ha designado un equipo de destino en la red y tiene una cuenta de inicio de sesión con privilegios de administrador local, puede usar el siguiente procedimiento para instalar el servidor de administración de virtualización de aplicaciones y asignarlo al grupo de servidores correspondiente.

**Nota**  
El Asistente para la instalación puede crear un registro de grupo de servidores, si no existe alguno, así como un registro de la pertenencia del servidor de virtualización de Application Virtualization en este grupo.



Después de completar el proceso de instalación, reinicie el servidor.

**Para instalar un servidor de administración de virtualización de aplicaciones**

1.  Compruebe y, si es necesario, desinstale versiones anteriores del servidor de administración de virtualización de aplicaciones que estén instaladas en el equipo de destino.

2.  Para abrir el Asistente para la **instalación de Microsoft Application Virtualization Management Server** , vaya a la ubicación del sistema de virtualización de aplicaciones **setup.exe** en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en el archivo de **Setup.exe** .

3.  En la página **principal** , haga clic en **siguiente**.

4.  En la página **contrato de licencia** , lea el contrato de licencia y, para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de la licencia**. Haz clic en **Siguiente**.

5.  En la página **información de registro** , debe escribir el nombre de usuario y la **organización**. Haz clic en **Siguiente**.

6.  En la página **tipo de configuración** , seleccione **personalizado**. Haz clic en **Siguiente**. En la página **Configuración personalizada** , anule la selección de todos los componentes del sistema de Application Virtualization, excepto **servidor de virtualización de aplicaciones**y haga clic en **siguiente**.

    **Actúe**  
    Si un componente ya está instalado en el equipo, cuando lo anule en la ventana de **instalación personalizada** , el componente se desinstalará automáticamente.



7.  En la **página base de datos de configuración** , seleccione un servidor de base de datos de la lista de servidores disponibles o agregar un servidor seleccionando **usar el siguiente nombre de host** y especificando los datos de nombre del **servidor** y **número de Puerto** . Haz clic en **Siguiente**.

    **Nota**  
    El servidor de administración de virtualización de aplicaciones no admite SQL con distinción entre mayúsculas y minúsculas.



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. En la página **modo de seguridad de conexión** , seleccione el certificado deseado de la lista desplegable. Haz clic en **Siguiente**.

   **Nota**  
   La configuración del **modo de conexión segura** requiere que el servidor tenga un certificado de servidor provisto de una infraestructura de clave pública. Si un certificado de servidor no está instalado en el servidor, esta opción no está disponible y no se puede seleccionar. Debe conceder acceso de lectura a la cuenta de servicio de red al certificado que se está usando.



9. En la página **configuración del puerto TCP** , para usar el puerto predeterminado (554), seleccione **usar puerto predeterminado (554)**. Para especificar un puerto personalizado, seleccione **usar puerto personalizado** y especifique el número de puerto que se usará. Haz clic en **Siguiente**.

   **Nota**  
   Al instalar el servidor en un entorno no seguro, puede usar el puerto predeterminado (554) o puede definir un puerto personalizado.



10. En la página **grupo de administradores** , especifique el nombre del grupo de seguridad autorizado para administrar este servidor en nombre de **Grupo**. Haz clic en **Siguiente**. Confirme el grupo especificado y haga clic en **siguiente**.

11. En la página **grupo de proveedores predeterminado** , especifique el nombre del grupo de proveedores predeterminado y, a continuación, haga clic en **siguiente**.

12. En la página **ruta de contenido** , especifique la ubicación en el equipo de destino donde se guardarán los archivos de SFT y, a continuación, haga clic en **siguiente**.

   **Nota**  
   Si el puerto HTTP o RTSP del servidor de administración ya está asignado, se le pedirá que elija un nuevo puerto. Seleccione el puerto que desee y, a continuación, haga clic en **siguiente**.



13. En la página **listo para instalar el programa** , para instalar el servidor de administración de virtualización de aplicaciones, haga clic en **instalar**.

   **Nota**  
   Si se muestra el error 25120 al intentar completar este paso, debe habilitar **las herramientas de administración y los scripts de administración de**IIS. Para habilitar esta característica de Windows, abra el panel de control **programas y características** , seleccione **activar o desactivar las características de Windows**y vaya a **servicios de información de Internet.**

   En **herramientas de administración web**, habilite **scripts y herramientas de administración de IIS**.



14. En la pantalla Asistente para la **instalación finalizada** , haga clic en **Finalizar**para cerrar el asistente.

   **Importante**  
   La instalación puede demorar unos minutos en finalizar. Un mensaje de estado parpadeará por encima del área de notificación del escritorio de Windows, lo que indica que la instalación se realizó correctamente.

   No es necesario reiniciar el equipo cuando se le solicite. Sin embargo, para optimizar el rendimiento del sistema, se recomienda un reinicio.



## Temas relacionados


[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)









