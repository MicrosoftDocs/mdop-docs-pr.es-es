---
title: Actualización desde versiones anteriores de MBAM
description: Actualización desde versiones anteriores de MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823810"
---
# Actualización desde versiones anteriores de MBAM


Puede actualizar la administración y supervisión de Microsoft BitLocker (MBAM) a MBAM 2.0, con la topología independiente o la topología del administrador de configuración, de la siguiente manera:

-   **Sustitución de servidor manual local** : para actualizar el servidor de MBAM, desinstale manualmente MBAM con el instalador o el panel de control y, a continuación, instale la infraestructura de MBAM 2.0. No es necesario quitar las bases de datos. La desinstalación de MBAM 1,0 Server deja intacta las bases de datos de MBAM. Si especifica las mismas bases de datos que MBAM 1,0, la instalación de MBAM 2.0 conserva los datos de MBAM 1,0 en las bases de datos y convierte las bases de datos para que funcionen con MBAM 2.0.

-   **Actualización de cliente distribuido** : Si usa la topología de MBAM independiente, puede actualizar los clientes de MBAM gradualmente después de instalar la infraestructura de servidor de MBAM 2,0. El servidor de MBAM 2,0 detecta la versión del cliente existente y realiza los pasos necesarios para actualizar al cliente de 2,0.

    Después de actualizar la infraestructura de servidor de MBAM 2,0, los clientes de MBAM 1,0 continúan reportando correctamente al servidor de MBAM 2,0, depósito de garantía de datos de recuperación, pero el cumplimiento se basará en las políticas de MBAM 1,0. Debe actualizar los clientes a MBAM 2,0 para que los equipos cliente notifiquen de forma precisa el cumplimiento de las directivas de MBAM 2,0. Puede actualizar los clientes al cliente de MBAM 2,0 sin desinstalar el cliente anterior y el cliente comenzará a aplicar y notificará las directivas de MBAM 2,0.

    Si está usando MBAM con Configuration Manager, debe actualizar los clientes de MBAM 1,0 a MBAM 2,0.

## Actualización de MBAM desde una arquitectura de dos servidores


Use las siguientes instrucciones para actualizar una versión anterior de MBAM cuando esté usando una arquitectura de dos servidores, donde un servidor está hospedando los componentes de Microsoft SQL Server y el otro servidor hospeda los sitios web y los servicios.

**Para actualizar MBAM de una arquitectura de dos servidores**

1.  En el servidor con las características de SQL Server, en el panel de control, seleccione **programas y características**y, a continuación, desinstale **Administración y administración de Microsoft BitLocker**. La base de datos de recuperación y la base de datos de auditoría y cumplimiento permanecen sin cambios.

2.  Ejecute **MBAMSetup.exe** para la versión MBAM 2,0, seleccione, opcionalmente, el programa para la mejora de la **experiencia del usuario**y, a continuación, haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la **Página selección de topología** , seleccione la topología de integración independiente o **de** **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.

5.  En la página **seleccionar características para instalar** , desactive las características servidor de **autoservicio** , **Administración y supervisión** y, a continuación, haga clic en **siguiente**.

6.  Espere a que finalicen las comprobaciones de requisitos previos y, a continuación, haga clic en **siguiente**. Si se detecta un requisito previo que falta, resuelva los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.

7.  En la página **proporcionar la cuenta usada para acceder a las bases de datos de MBAM** , proporcione el nombre del equipo del servidor que hospedará los sitios y servicios y, a continuación, haga clic en **siguiente**.

8.  En la página **configurar la base** de datos de recuperación, especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación. También debe especificar dónde se ubicarán los archivos de base de datos y la información de registro.

9.  Haz clic en **Siguiente** para continuar.

10. En la página **Configure the Compliance and Audit Database** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de cumplimiento y comprobación.

11. Haz clic en **Siguiente** para continuar.

12. En la página **configurar los informes de cumplimiento y cumplimiento** , especifique la instancia de SQL Server Reporting Services en la que se instalarán los informes de cumplimiento y cumplimiento, y proporcione una cuenta de usuario y contraseña de dominio para obtener acceso a la base de datos de cumplimiento y comprobación. Configure la contraseña de esta cuenta para que nunca expire. La cuenta de usuario puede tener acceso a todos los datos disponibles para el grupo de usuarios de informes de MBAM.

13. Haz clic en **Siguiente** para continuar.

14. Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**. Esto no activa las actualizaciones automáticas en Windows. Si anteriormente decidió usar Microsoft Update para este producto o para otro producto, la página de Microsoft Update no aparece.

15. En la página Resumen de la **instalación** , revise las características que se instalarán y, a continuación, haga clic en **instalar** para iniciar la instalación.

**Para desinstalar las características del servidor de administración y supervisión y para completar la actualización**

1.  En el equipo que hospeda las características de servidor de administración y supervisión, en el panel de control, seleccione **programas y características**y, después, desinstale MBAM para quitar los sitios web y servicios previamente instalados.

2.  Ejecute el **MBAMSetup.exe** para la versión 2,0, opcionalmente, seleccione el programa para la mejora de la **experiencia del usuario**y, a continuación, haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la **Página selección de topología** , seleccione la topología de integración independiente o **de** **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.

5.  En la **página seleccionar las características que desea instalar** , desactive las características base de **datos de recuperación** , **base** de datos de recuperación y cumplimiento de **normas y auditoría** y, a continuación, haga clic en **siguiente**.

6.  Espere a que finalicen las comprobaciones de requisitos previos y, a continuación, haga clic en **siguiente**. Si se detecta un requisito previo que falta, resuelva primero los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.

7.  En la página **configurar la seguridad de comunicaciones de red** , elija si desea usar el cifrado de nivel de socket seguro (SSL) para los sitios web y los servicios. Si decide cifrar la comunicación, seleccione el certificado de la entidad de certificación (CA) que quiere usar para el cifrado.

    **Nota:**  El certificado debe crearse antes de este paso para poder seleccionarlo en esta página.

     

8.  En la página **configurar la ubicación de la base de datos de estado de cumplimiento** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacena los datos de cumplimiento y de auditoría. También debe especificar dónde se ubicarán los archivos de base de datos y la información de registro.

9.  Haz clic en **Siguiente** para continuar.

10. En la página **configurar la ubicación de la base de datos de recuperación** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacena los datos de recuperación.

11. Haz clic en **Siguiente** para continuar.

12. En la página **configurar los informes de cumplimiento y cumplimiento** , escriba la dirección URL de la instancia de informes que ha configurado en el otro servidor. Use el botón **prueba** para comprobar que puede comunicarse con el sitio.

13. Haz clic en **Siguiente** para continuar.

14. En la página **configurar el portal de autoservicio** , escriba el número de puerto, el nombre de host, el nombre del directorio virtual y la ruta de instalación para el portal de autoservicio.

    **Nota:**  El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host.

     

15. En la página **configurar el servidor de administración y supervisión** , especifique el directorio virtual que desee para el sitio web del Departamento de soporte.

16. Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**. Este paso no activa las actualizaciones automáticas en Windows. Si anteriormente decidió usar Microsoft Update para este producto o para otro producto, la página de Microsoft Update no aparece.

17. En la página Resumen de la **instalación** , revise las características que se instalarán y, a continuación, haga clic en **instalar** para iniciar la instalación.

18. Para validar que la actualización se ha realizado correctamente, compruebe que puede comunicarse con cada sitio desde otro equipo del dominio.

## Actualización del cliente de MBAM en equipos de usuario final


Para actualizar los equipos de los usuarios finales al cliente de MBAM 2,0, ejecute **MbamClientSetup.exe** en cada equipo cliente. El instalador actualiza automáticamente el cliente al cliente de MBAM 2,0. Puede instalar el cliente de MBAM a través de un sistema electrónico de distribución de software, herramientas como Active Directory Domain Services o System Center Configuration Manager.

Para validar la actualización del cliente, haga lo siguiente:

1.  Espere hasta que el ciclo de informes configurado haya finalizado y, a continuación, inicie **SQL Server Management Studio** en el equipo con SQL Server.

2.  En el equipo con SQL Server, inicie **SQL Server Management Studio**.

3.  Compruebe que la tabla **RecoveryAndHardwareCore. Machines** contiene una fila que muestra el nombre del equipo del usuario final.

## Temas relacionados


[Implementación de MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





