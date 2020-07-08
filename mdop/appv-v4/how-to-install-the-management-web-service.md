---
title: Cómo instalar el servicio web de administración
description: Cómo instalar el servicio web de administración
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817280"
---
# Cómo instalar el servicio web de administración


Use el siguiente procedimiento para instalar el servicio Web de administración de virtualización de aplicaciones en un equipo de destino de la red, con una cuenta de inicio de sesión que tenga privilegios de administrador local. Aunque no es necesario, le recomendamos que instale este componente en su servidor Web.

**Para instalar el servicio Web de administración**

1.  Compruebe que ninguna de las versiones anteriores del servicio Web de virtualización de aplicaciones están instaladas en el equipo de destino.

2.  Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en **Setup.exe**.

3.  Una vez que se abra el Asistente de instalación, en la página **principal** , haga clic en **siguiente**.

4.  En la página **contrato de licencia** , para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de licencia**y, a continuación, haga clic en **siguiente**.

5.  En la página **información de registro** , especifique el nombre de **usuario** y la información de la organización y, a continuación, haga clic en **siguiente**.

6.  En la página **tipo de configuración** , haga clic en **personalizado**y, a continuación, haga clic en **siguiente**.

    **Nota:**  Si este no es el primer componente que instaló en este equipo, se muestra la página **mantenimiento del programa** . En la página **mantenimiento del programa** , haga clic en **modificar**.

     

7.  En la página **instalación personalizada** , desactive todos los componentes del sistema de Application Virtualization, excepto el **servicio de administración de virt**de aplicaciones y haga clic en **siguiente**.

    **Nota:**  Si un componente ya está instalado en el equipo, al borrarlo en la página de **instalación personalizada** , se desinstalará automáticamente.

     

8.  En la página **servidor de base de datos** , haga clic en **conectarse a la base de datos disponible**y, a continuación, en **siguiente**.

    **Nota:**  En un entorno de producción, Microsoft da por supuesto que se conectará a una base de datos existente. Si desea instalar una base de datos, vea [Cómo instalar una base de datos](how-to-install-a-database.md). Después de instalar la base de datos, continúe con el paso 13.

     

9.  En la página **tipo de servidor de base de datos** , seleccione un tipo de base de datos de la lista y haga clic en **siguiente**.

10. En la página **Ubicación del servidor de base** de datos, seleccione un servidor de base de datos de la lista de servidores disponibles o agregue un servidor activando la casilla de verificación **usar el siguiente nombre de host** y escribiendo información en los cuadros nombre del **servidor** y **número de Puerto** y, a continuación, haga clic en **siguiente**.

11. En la página **Seleccionar base de datos** , seleccione la base de datos que desee y, a continuación, haga clic en **siguiente**.

12. En la página **configuración de usuario de base** de datos, escriba las credenciales que usará el servicio Web de administración para obtener acceso al almacén de datos y, a continuación, haga clic en **siguiente**.

13. En la página **listo para modificar el programa** , haga clic en **instalar**.

    **Nota:**  Si este es el primer componente que instala, se muestra la página **preparado para instalar el programa** . En la página, haga clic en **instalar**.

     

14. En la página **Asistente para la instalación completada** , haga clic en **Finalizar**.

## Temas relacionados


[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)

 

 





