---
title: Cómo instalar MBAM con Administrador de configuración
description: Cómo instalar MBAM con Administrador de configuración
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825130"
---
# Cómo instalar MBAM con Administrador de configuración


En esta sección se describen los pasos necesarios para instalar MBAM con Configuration Manager mediante la configuración recomendada, que se muestra en [Introducción, uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). Los pasos se dividen en las siguientes tareas:

-   Instalar y configurar MBAM en el servidor de Configuration Manager

-   Instalar las bases de datos de recuperación y de auditoría en el servidor de bases de datos

-   Instalar las características del servidor de administración y supervisión en el servidor de administración y supervisión

Antes de comenzar la instalación, asegúrese de que ha editado o creado los archivos MOF necesarios. Para obtener instrucciones, consulte [Cómo crear o editar archivos MOF](how-to-create-or-edit-the-mof-files.md).

**Importante**  Si está usando una instancia no predeterminada de SQL Server Reporting Services (SSRS), debe iniciar el programa de instalación de MBAM con la siguiente línea de comandos para especificar la instancia con nombre de SSRS:

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**Para instalar MBAM en el servidor de Configuration Manager**

1.  En el servidor de Configuration Manager, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.

    **Nota:**  Para obtener los archivos de registro de instalación, tiene que usar el paquete msiexec y la opción de ubicación **/l** &lt; &gt; para instalar el administrador de configuración. Los archivos de registro se crean en la ubicación que especifique.

    Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% en el equipo del usuario que está instalando el administrador de configuración.

     

2.  En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la página **selección de topología** , seleccione **integración de System Center Configuration Manager**y, a continuación, haga clic en **siguiente**.

5.  En la página **seleccionar características para instalar** , seleccione **integración de System Center Configuration Manager**.

    **Nota:**  En la página **comprobando requisitos** , haga clic en **siguiente** después de que el Asistente para la instalación Revise los requisitos previos para su instalación y confirme que no se ha perdido ninguna. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos.**

     

6.  Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**. El uso de actualizaciones de Microsoft no activa las actualizaciones automáticas en Windows.

7.  Haz clic en **Siguiente** para continuar.

8.  En la página Resumen de la **instalación** , revise la lista de características que se instalarán y haga clic en **instalar** para empezar a instalar las características de MBAM. Haga clic en **atrás** para retroceder por el asistente si necesita revisar o cambiar la configuración de instalación, o bien haga clic en **Cancelar** para salir de la instalación. El programa de instalación instala las características de MBAM y le notifica que se ha completado la instalación.

9.  Haga clic en **Finalizar** para salir del asistente.

**Para instalar las bases de datos de recuperación y auditoría en el servidor de bases de datos**

1.  En el servidor de base de datos, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.

2.  En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la página **selección de topología** , seleccione la topología de integración de **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.

5.  En la lista de características que se instalarán, seleccione **base de datos de recuperación** y base de datos de **Auditoría**, y borre las características restantes.

    **Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.

     

6.  En la página **configurar la base de datos de recuperación** , especifique los nombres de los equipos que ejecutarán la característica de servidor de administración y supervisión. Después de implementar la característica de servidor de administración y supervisión, se usa su cuenta de dominio para conectarse a la base de datos.

7.  Haz clic en **Siguiente** para continuar.

8.  Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación. También debe especificar dónde se ubicará la base de datos y dónde se ubicará la información de registro.

9.  Haga clic en **siguiente** para continuar con el Asistente para la instalación de MBAM.

10. En la página **configurar la base de datos de auditoría** , especifique la cuenta de usuario que se usará para obtener acceso a la base de datos para los informes.

11. Especifique los nombres de los equipos que ejecutarán el servidor de administración y supervisión y los informes de auditoría. Después de implementar las características administración y supervisión y los informes de auditoría, sus cuentas de dominio se usarán para conectarse a las bases de datos.

    **Nota:**  Si va a instalar la base de datos de auditoría sin la característica informes de auditoría, debe agregar una excepción en el equipo de la base de datos de auditoría para habilitar el tráfico entrante en el puerto de Microsoft SQL Server. El número de puerto predeterminado es 1433.

     

12. Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de auditoría. También debe especificar dónde se ubicarán la información de la base de datos y del registro.

13. Haga clic en **instalar** para iniciar la instalación y, a continuación, haga clic en **Finalizar** para completar la instalación.

**Para instalar las características de servidor de administración y supervisión en el servidor de administración y supervisión**

1.  En el servidor de administración y supervisión, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.

2.  En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la página **selección de topología** , seleccione la topología de integración de **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.

5.  En la lista de características que se instalarán, seleccione **servidor de administración y supervisión** y portal de **autoservicio**y borre las características restantes.

    **Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.

     

6.  Instale el portal de autoservicio siguiendo los pasos de la sección **para instalar el portal de autoservicio** en [Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

    **Nota:**  Si los equipos cliente no tendrán acceso a la red de entrega de contenido (CDN) de Microsoft, que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript, complete los pasos del **para configurar el portal de autoservicio cuando los usuarios finales no pueden acceder a la** sección de la red de entrega de contenido de Microsoft [Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) para configurar el portal de autoservicio con el fin de hacer referencia a los archivos de JavaScript desde un origen accesible.

     

7.  Instale las características de servidor de administración y supervisión siguiendo los pasos de la sección **para instalar la característica servidor de administración y supervisión** en [Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

8.  Haga clic en **Finalizar** para completar la instalación.

## Temas relacionados


[Cómo validar la instalación de MBAM con Administrador de configuración](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[Implementación de MBAM con Administrador de configuración](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





