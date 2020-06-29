---
title: Cómo actualizar los servidores y componentes del sistema
description: Cómo actualizar los servidores y componentes del sistema
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816421"
---
# Cómo actualizar los servidores y componentes del sistema


Use el siguiente procedimiento para actualizar los componentes de software instalados en todos los equipos del sistema de virtualización de aplicaciones. Los servicios del sistema de Application Virtualization se reiniciarán automáticamente en cada equipo después de que se haya actualizado.

**Nota**  
-   El proceso de actualización detiene todos los servicios del sistema de virtualización de aplicaciones, por lo que el sistema queda fuera de servicio. Las sesiones de usuario deben cerrarse antes de comenzar el proceso de actualización y debe detener todos los servicios del servidor de virtualización de aplicaciones en su entorno.

-   Si tiene más de un servidor que comparte el acceso a la base de datos de virtualización de la aplicación, todos esos servidores deben estar desconectados mientras se actualiza la base de datos. Debe seguir las prácticas normales de negocios para la actualización de la base de datos, pero es muy aconsejable que pruebe la actualización de la base de datos con una copia de seguridad de la base de datos en primer lugar en un servidor de prueba. Después, seleccione uno de los servidores para la primera actualización, que actualizará el esquema de la base de datos. Una vez que la base de datos de producción se ha actualizado correctamente, puede actualizar los otros servidores.

-   Solo puede actualizar a Microsoft Application Virtualization (App-V) 4.5 desde Microsoft Application Virtualization (App-V) 4.1 ó 4.1 SP1. Es necesario que App-V 4.0 y versiones anteriores se desinstalen o actualicen a 4.1 ó 4.1 SP1 antes de actualizar a App-V 4.5.

 

**Para actualizar los componentes de software en Application Virtualization System Computers**

1.  Vaya a la ubicación del programa de instalación en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en el archivo Setup.exe.

2.  En la página **principal** del asistente de instalación, haga clic en **siguiente**.

3.  En la página **contrato de licencia** , lea el contrato de licencia, seleccione Acepto **las condiciones del contrato de licencia**y haga clic en **siguiente**.

4.  Cuando se abra la página **software instalado** y se muestre una lista de los componentes del sistema de virtualización de aplicaciones instalados y la versión de cada componente, haga clic en **siguiente**.

5.  En la página **Advertencia de pérdida de sesión** , lea el mensaje que se muestra y haga clic en **siguiente**.

6.  En la página **conectar con la base de datos de configuración** , revise el contenido de la página y haga clic en **siguiente**.

7.  Si se muestra la página actualización de la **base de datos requerida** , es necesaria una actualización de la base de datos. Escriba las credenciales administrativas de la base de datos y haga clic en **siguiente**. Si no se muestra esta página, vaya al paso 9.

8.  En la página **configuración de copia de seguridad** de la base de datos, active las casillas correspondientes para realizar la copia de seguridad y exportarla a una ubicación existente, y haga clic en **siguiente**.

    **Importante**  Si desea poder revertir a la versión anterior en el caso de que se produzca un error de actualización, asegúrese de que activa la casilla **realizar una copia de seguridad de la base de datos de configuración** o perderá los datos de configuración.

    Cuando desee restaurar una base de datos con VSS, primero debe detener el servicio de servidor de App-V en el servidor de administración. Debe hacerse en todos los servidores de administración si hay más de un servidor conectado a la misma base de datos.

     

9.  En la primera página de **validación del paquete** , lea el contenido y, a continuación, haga clic en **siguiente**.

10. En la segunda página de **validación del paquete** , tiene la opción de mostrar los detalles de la validación del paquete en una ventana del Bloc de notas. Para ver los detalles, haga clic en **detalles**; en caso contrario, haga clic en **siguiente**.

11. En la página **listo para actualizar el programa** , haga clic en **siguiente**.

12. En la página **Asistente para la instalación completada** , haga clic en **Finalizar**.

13. Repita los pasos 1 a 12 en todos los demás equipos en los que instaló la consola de administración de virtualización de aplicaciones o el componente de software del servidor de virtualización de aplicaciones.

    Después de actualizar el almacén de datos, puede reanudar el funcionamiento normal. (El almacén de datos se actualiza cuando actualiza cualquier servidor o el servicio Web de administración de App-V).

## Temas relacionados


[Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





