---
title: Generación de informes independientes de MBAM 2.5
description: Generación de informes independientes de MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823121"
---
# Generación de informes independientes de MBAM 2.5


Al configurar administración y supervisión de Microsoft BitLocker (MBAM) con la topología independiente, puede generar informes para supervisar el uso del cifrado de unidad BitLocker y el cumplimiento. Este tema contiene los procedimientos siguientes:

-   [Para abrir el sitio web de administración y supervisión](#bkmk-openadmin)

-   [Para generar un informe de compatibilidad empresarial](#bkmk-enterprise)

-   [Para generar un informe de cumplimiento de equipos](#bkmk-computercomp)

-   [Para generar un informe de auditoría de clave de recuperación](#bkmk-recoverykey)

Para obtener descripciones de los informes independientes, consulte [Understanding MBAM 2,5 informes independientes](understanding-mbam-25-stand-alone-reports.md).

**Nota:**  Para ejecutar los informes, debe ser miembro del grupo de **usuarios de informes de MBAM** , que puede configurar en los servicios de dominio de Active Directory. Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

 

<a href="" id="bkmk-openadmin"></a>**Para abrir el sitio web de administración y supervisión**

1.  Abra un explorador Web y vaya al sitio web de administración y supervisión. La dirección URL predeterminada para el sitio web de administración y supervisión es:

    *http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; Puerto &gt; /Helpdesk*

2.  En el panel de la izquierda, haga clic en **informes**. En la barra de menús superior, seleccione el informe que desea ejecutar.

    Los datos del cliente de MBAM se conservan en la base de datos de cumplimiento y auditoría para las referencias históricas en caso de pérdida o robo de un equipo. Cuando se ejecutan informes empresariales, le recomendamos que use las fechas de inicio y finalización apropiadas para el ámbito de los intervalos de tiempo para los informes de una a dos semanas, lo que aumentará la precisión de los datos.

    Después de generar un informe, puede guardar los resultados en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.

    **Nota:**  Configure SQL Server Reporting Services (SSRS) para usar la capa de sockets seguros (SSL) antes de configurar el sitio web de administración y supervisión. Si, por cualquier motivo, SSRS no está configurado para usar SSL, la dirección URL de los informes se establecerá en HTTP en lugar de en HTTPS cuando configure el sitio web de administración y supervisión. Si, a continuación, visita el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro". Para mostrar el informe, haga clic en **Mostrar todo el contenido**.

     

<a href="" id="bkmk-enterprise"></a>**Para generar un informe de compatibilidad empresarial**

1.  Desde el sitio web de administración y supervisión, seleccione el nodo **informes** en el panel de navegación izquierdo, seleccione **Informe de cumplimiento**de la empresa y seleccione los filtros que desea usar. Los filtros disponibles para el informe de cumplimiento de la empresa son:

    -   **Estado de cumplimiento**. Use este filtro para especificar los tipos de estado de cumplimiento del informe (por ejemplo, compatible o no compatible).

    -   **Estado de error**. Use este filtro para especificar los tipos de estado de error del informe (por ejemplo, sin errores o errores).

2.  Haga clic en **Ver informe** para mostrar el informe seleccionado.

3.  Seleccione un nombre de equipo para ver información sobre el equipo en el informe de cumplimiento de equipos.

4.  Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.

<a href="" id="bkmk-computercomp"></a>**Para generar un informe de cumplimiento de equipos**

1.  En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione **Informe de cumplimiento de equipos**. Use el informe de cumplimiento de equipos para buscar el **nombre de usuario** o **el nombre del equipo**.

2.  Haga clic en **Ver informe** para ver el informe de cumplimiento de equipos.

3.  Seleccione el nombre de un equipo para mostrar más información sobre el equipo en el informe cumplimiento de equipos.

4.  Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.

    **Nota:**  Un equipo cliente de MBAM se considera conforme si el equipo cumple o supera los requisitos de la configuración de directiva de grupo de MBAM.

<a href="" id="bkmk-recoverykey"></a>**Para generar un informe de auditoría de clave de recuperación**

1.  En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione **Informe de auditoría de recuperación**. Seleccione los filtros para el informe de auditoría de clave de recuperación. Los filtros disponibles para auditorías de claves de recuperación son los siguientes:

    -   **Usuario del servicio de asistencia**. Este filtro permite a los usuarios especificar el nombre de usuario del solicitante. El solicitante es la persona del servicio de asistencia que ha tenido acceso a la clave en nombre de un usuario final.

    -   **Usuario final**. Este filtro permite a los usuarios especificar el nombre de usuario del solicitante. El solicitante es el usuario final que llamó al servicio de asistencia para obtener una clave de recuperación.

    -   **Resultado**de la solicitud. Este filtro permite a los usuarios especificar los tipos de resultado de la solicitud (por ejemplo, éxito o error) en los que desean basar el informe. Por ejemplo, es posible que los usuarios deseen ver los intentos fallidos de acceso clave.

    -   **Tipo de clave**. Este filtro permite a los usuarios especificar el tipo de clave (por ejemplo, la contraseña de la clave de recuperación o el hash de contraseña de TPM) en el que desean basar el informe.

    -   **Fecha de inicio**. Este filtro se usa para definir la parte de fecha de inicio del intervalo de fechas para el que el usuario desea informar.

    -   **Fecha de finalización**. Este filtro se usa para definir la fecha de finalización del intervalo de fechas en la que los usuarios desean informar.

2.  Haga clic en **Ver informe** para ver el informe.



## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Descripción de informes independientes de MBAM 2.5](understanding-mbam-25-stand-alone-reports.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





