---
title: Cómo generar informes MBAM.
description: Cómo generar informes MBAM.
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824091"
---
# Cómo generar informes MBAM.


Al instalar la administración y supervisión de Microsoft BitLocker (MBAM) con la topología independiente, puede generar diferentes informes para supervisar el uso y el cumplimiento del cifrado de BitLocker. Los procedimientos de este tema describen cómo abrir el sitio web de administración y supervisión, así como los pasos necesarios para generar informes de administración y supervisión de Microsoft BitLocker sobre el cumplimiento de la norma empresarial, los equipos individuales y la actividad de recuperación de claves. Para obtener información detallada que ayude a comprender los informes de MBAM, consulte [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).

**Nota:**  Para ejecutar los informes, debe ser miembro del **rol de usuarios de informes** en los equipos en los que se instalan las características de servidor administración y supervisión, la base de datos de cumplimiento y la base de datos y los informes de cumplimiento y cumplimiento.

 

**Para abrir el sitio web de administración y supervisión**

1.  Abra un explorador Web y vaya al sitio web de administración y supervisión. La dirección URL predeterminada para el sitio web de administración y supervisión es *http:// &lt; NombreDeEquipo &gt; *.

    **Nota:**  Si el sitio web de administración y supervisión se instaló en un puerto que no es 80, tiene que especificar el puerto en la dirección URL (por ejemplo, *http:// &lt; NombreDeEquipo &gt; : &lt; Port &gt; *. Si especificó un nombre de host para el sitio web de administración y supervisión durante la instalación, la dirección URL es *http:// &lt; hostname &gt; *.

     

2.  En el panel izquierdo, haga clic en **informes** y, a continuación, seleccione el informe que desea ejecutar en la barra de menús superior.

    Los datos históricos de los clientes de MBAM se conservan en la base de datos de cumplimiento para referencia histórica en caso de pérdida o robo de un equipo. Cuando se ejecutan informes empresariales, le recomendamos que use las fechas de inicio y finalización apropiadas para el ámbito de los intervalos de tiempo para los informes de una a dos semanas, lo que aumentará la precisión de los datos.

    **Nota:**  Si SSRS no se configuró para usar el nivel de socket seguro, la dirección URL de los informes se establecerá en HTTP en lugar de en HTTPS cuando instale el servidor MBAM. Si, a continuación, va al portal del servicio de asistencia y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro". Para mostrar el informe, haga clic en **Mostrar todo el contenido**.

     

**Para generar un informe de compatibilidad empresarial**

1.  Desde el sitio web de administración y supervisión, seleccione el nodo **informes** en el panel de navegación izquierdo, seleccione **Informe de cumplimiento**de la empresa y seleccione los filtros que desea usar. Los filtros disponibles para el informe de cumplimiento de la empresa son los siguientes:

    -   **Estado de cumplimiento**. Use este filtro para especificar los tipos de estado de cumplimiento (por ejemplo, conformes o no conformes) del informe.

    -   **Estado de error**. Use este filtro para especificar los tipos de estado de error (por ejemplo, ningún error o error) del informe.

2.  Haga clic en **Ver informe** para mostrar el informe seleccionado.

    Los resultados se pueden guardar en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.

    **Nota:**  El informe de cumplimiento de la empresa se genera a partir de un trabajo de SQL que se ejecuta cada seis horas. Por lo tanto, la primera vez que vea el informe, puede encontrarse con algunos datos que faltan. Puede generar datos de informes actualizados de forma manual mediante SQL Management Studio. En la ventana **Explorador de objetos** , expanda el **Agente SQL Server**, expanda **trabajos**, haga clic con el botón derecho en el trabajo **CreateCache** y seleccione **Iniciar tarea en el paso....**

     

3.  Seleccione un nombre de equipo para ver información sobre el equipo en el informe de cumplimiento de equipos.

4.  Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.

**Para generar el informe de cumplimiento de equipos**

1.  En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione el **Informe de cumplimiento de equipos**. Use el informe de cumplimiento de equipos para buscar el **nombre de usuario** o **el nombre del equipo**.

2.  Haga clic en **Ver informe** para ver el informe del equipo.

    Los resultados se pueden guardar en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.

3.  Seleccione el nombre de un equipo para mostrar más información sobre el equipo en el informe cumplimiento de equipos.

4.  Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.

    **Nota:**  Un equipo cliente de MBAM se considera conforme si el equipo cumple con los requisitos de la configuración de directiva de MBAM.

     

**Para generar el informe de auditoría de clave de recuperación**

1.  En el sitio web de administración y supervisión, seleccione el nodo de **Informe** en el panel de navegación izquierdo y, a continuación, seleccione el **Informe de auditoría de recuperación**. Seleccione los filtros para el informe de auditoría de clave de recuperación. Los filtros disponibles para auditorías de claves de recuperación son los siguientes:

    -   **Solicitante**. Este filtro permite a los usuarios especificar el nombre de usuario del solicitante. El solicitante es la persona del Departamento de soporte que ha tenido acceso a la clave en nombre de un usuario.

    -   **Solicitante**. Este filtro permite a los usuarios especificar el nombre de usuario del solicitante. El solicitante es la persona que llamó al servicio de asistencia para obtener una clave de recuperación.

    -   **Resultado**de la solicitud. Este filtro permite a los usuarios especificar los tipos de resultado de la solicitud (por ejemplo, éxito o error) en los que desean basar el informe. Por ejemplo, es posible que los usuarios deseen ver los intentos fallidos de acceso clave.

    -   **Tipo de clave**. Este filtro permite a los usuarios especificar el tipo de clave (por ejemplo: contraseña de la clave de recuperación o hash de contraseña de TPM) en la que desee basar el informe.

    -   **Fecha de inicio**. Este filtro se usa para definir la parte de fecha de inicio del intervalo de fechas para el que el usuario desea informar.

    -   **Fecha de finalización**. Este filtro se usa para definir la fecha de finalización del intervalo de fechas en la que los usuarios desean informar.

2.  Haga clic en **Ver informe** para ver el informe.

    Los resultados se pueden guardar en diferentes formatos, como HTML, Microsoft Word y Microsoft Excel.

## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





